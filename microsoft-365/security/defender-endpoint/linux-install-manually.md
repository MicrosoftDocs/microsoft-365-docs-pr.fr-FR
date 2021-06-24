---
title: Déployer Microsoft Defender pour le point de terminaison sur Linux manuellement
ms.reviewer: ''
description: Décrit comment déployer Microsoft Defender pour Endpoint sur Linux manuellement à partir de la ligne de commande.
keywords: microsoft, defender, Microsoft Defender pour le point de terminaison, linux, installation, déployer, désinstallation, préinstallation, ansible, linux, redhat, ubuntu, debian, sles, suse, centos
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
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 8d7ac39baabca1496a5d2c22521874cfd60c6208
ms.sourcegitcommit: ccbdf2638fc6646bfb89450169953f4c3ce4b9b0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/24/2021
ms.locfileid: "53105571"
---
# <a name="deploy-microsoft-defender-for-endpoint-on-linux-manually"></a><span data-ttu-id="4d5ea-104">Déployer Microsoft Defender pour le point de terminaison sur Linux manuellement</span><span class="sxs-lookup"><span data-stu-id="4d5ea-104">Deploy Microsoft Defender for Endpoint on Linux manually</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="4d5ea-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="4d5ea-105">**Applies to:**</span></span>
- [<span data-ttu-id="4d5ea-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="4d5ea-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="4d5ea-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="4d5ea-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="4d5ea-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="4d5ea-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="4d5ea-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigateip-abovefoldlink)

<span data-ttu-id="4d5ea-110">Cet article explique comment déployer Microsoft Defender pour Endpoint sur Linux manuellement.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-110">This article describes how to deploy Microsoft Defender for Endpoint on Linux manually.</span></span> <span data-ttu-id="4d5ea-111">Un déploiement réussi nécessite l’exécution de toutes les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="4d5ea-111">A successful deployment requires the completion of all of the following tasks:</span></span>

- [<span data-ttu-id="4d5ea-112">Déployer Microsoft Defender pour point de terminaison sur Linux manuellement</span><span class="sxs-lookup"><span data-stu-id="4d5ea-112">Deploy Microsoft Defender for Endpoint on Linux manually</span></span>](#deploy-microsoft-defender-for-endpoint-on-linux-manually)
  - [<span data-ttu-id="4d5ea-113">Conditions préalables et système requis</span><span class="sxs-lookup"><span data-stu-id="4d5ea-113">Prerequisites and system requirements</span></span>](#prerequisites-and-system-requirements)
  - [<span data-ttu-id="4d5ea-114">Configurer le référentiel de logiciels Linux</span><span class="sxs-lookup"><span data-stu-id="4d5ea-114">Configure the Linux software repository</span></span>](#configure-the-linux-software-repository)
    - [<span data-ttu-id="4d5ea-115">RHEL et variantes (CentOS et Oracle Linux)</span><span class="sxs-lookup"><span data-stu-id="4d5ea-115">RHEL and variants (CentOS and Oracle Linux)</span></span>](#rhel-and-variants-centos-and-oracle-linux)
    - [<span data-ttu-id="4d5ea-116">SLES et variantes</span><span class="sxs-lookup"><span data-stu-id="4d5ea-116">SLES and variants</span></span>](#sles-and-variants)
    - [<span data-ttu-id="4d5ea-117">Systèmes Ubuntu et Debian</span><span class="sxs-lookup"><span data-stu-id="4d5ea-117">Ubuntu and Debian systems</span></span>](#ubuntu-and-debian-systems)
  - [<span data-ttu-id="4d5ea-118">Installation de l’application</span><span class="sxs-lookup"><span data-stu-id="4d5ea-118">Application installation</span></span>](#application-installation)
  - [<span data-ttu-id="4d5ea-119">Télécharger le package d’intégration</span><span class="sxs-lookup"><span data-stu-id="4d5ea-119">Download the onboarding package</span></span>](#download-the-onboarding-package)
  - [<span data-ttu-id="4d5ea-120">Configuration du client</span><span class="sxs-lookup"><span data-stu-id="4d5ea-120">Client configuration</span></span>](#client-configuration)
  - [<span data-ttu-id="4d5ea-121">Script du programme d’installation</span><span class="sxs-lookup"><span data-stu-id="4d5ea-121">Installer script</span></span>](#installer-script)
  - [<span data-ttu-id="4d5ea-122">Journal des problèmes d’installation</span><span class="sxs-lookup"><span data-stu-id="4d5ea-122">Log installation issues</span></span>](#log-installation-issues)
  - [<span data-ttu-id="4d5ea-123">Mises à niveau du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="4d5ea-123">Operating system upgrades</span></span>](#operating-system-upgrades)
  - [<span data-ttu-id="4d5ea-124">Désinstallation</span><span class="sxs-lookup"><span data-stu-id="4d5ea-124">Uninstallation</span></span>](#uninstallation)

## <a name="prerequisites-and-system-requirements"></a><span data-ttu-id="4d5ea-125">Conditions préalables et système requis</span><span class="sxs-lookup"><span data-stu-id="4d5ea-125">Prerequisites and system requirements</span></span>

<span data-ttu-id="4d5ea-126">Avant de commencer, consultez [Microsoft Defender pour Endpoint sur Linux](microsoft-defender-endpoint-linux.md) pour obtenir une description des conditions préalables et de la requise pour la version logicielle actuelle.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-126">Before you get started, see [Microsoft Defender for Endpoint on Linux](microsoft-defender-endpoint-linux.md) for a description of prerequisites and system requirements for the current software version.</span></span>

## <a name="configure-the-linux-software-repository"></a><span data-ttu-id="4d5ea-127">Configurer le référentiel de logiciels Linux</span><span class="sxs-lookup"><span data-stu-id="4d5ea-127">Configure the Linux software repository</span></span>

<span data-ttu-id="4d5ea-128">Defender for Endpoint sur Linux peut être déployé à partir de l’un des canaux suivants (indiqués ci-dessous sous le nom *[canal]*) : *insiders-fast,* *insiders-slow* ou *prod*. Chacun de ces canaux correspond à un référentiel de logiciels Linux.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-128">Defender for Endpoint on Linux can be deployed from one of the following channels (denoted below as *[channel]*): *insiders-fast*, *insiders-slow*, or *prod*. Each of these channels corresponds to a Linux software repository.</span></span> <span data-ttu-id="4d5ea-129">Les instructions de configuration de votre appareil pour utiliser l’un de ces référentiels sont fournies ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-129">Instructions for configuring your device to use one of these repositories are provided below.</span></span>

<span data-ttu-id="4d5ea-130">Le choix du canal détermine le type et la fréquence des mises à jour proposées à votre appareil.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-130">The choice of the channel determines the type and frequency of updates that are offered to your device.</span></span> <span data-ttu-id="4d5ea-131">Les appareils *internes rapides* sont les premiers à recevoir des mises à jour et de nouvelles fonctionnalités, suivis ultérieurement par les *insiders-slow* et enfin par *prod*.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-131">Devices in *insiders-fast* are the first ones to receive updates and new features, followed later by *insiders-slow* and lastly by *prod*.</span></span>

<span data-ttu-id="4d5ea-132">Afin d’afficher un aperçu des nouvelles fonctionnalités et de fournir des commentaires préliminaires, il est recommandé de configurer certains appareils dans votre entreprise pour utiliser les *insiders-fast* ou *insider-slow*.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-132">In order to preview new features and provide early feedback, it is recommended that you configure some devices in your enterprise to use either *insiders-fast* or *insiders-slow*.</span></span>

> [!WARNING]
> <span data-ttu-id="4d5ea-133">Le basculement du canal après l’installation initiale nécessite la réinstallation du produit.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-133">Switching the channel after the initial installation requires the product to be reinstalled.</span></span> <span data-ttu-id="4d5ea-134">Pour basculer le canal de produit : désinstallez le package existant, configurez de nouveau votre appareil pour utiliser le nouveau canal et suivez les étapes de ce document pour installer le package à partir du nouvel emplacement.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-134">To switch the product channel: uninstall the existing package, re-configure your device to use the new channel, and follow the steps in this document to install the package from the new location.</span></span>

### <a name="rhel-and-variants-centos-and-oracle-linux"></a><span data-ttu-id="4d5ea-135">RHEL et variantes (CentOS et Oracle Linux)</span><span class="sxs-lookup"><span data-stu-id="4d5ea-135">RHEL and variants (CentOS and Oracle Linux)</span></span>

- <span data-ttu-id="4d5ea-136">Installez `yum-utils` s’il n’est pas encore installé :</span><span class="sxs-lookup"><span data-stu-id="4d5ea-136">Install `yum-utils` if it isn't installed yet:</span></span>

    ```bash
    sudo yum install yum-utils
    ```

- <span data-ttu-id="4d5ea-137">Notez votre distribution et version, et identifiez l’entrée la plus proche (par majeure, puis mineure) sous `https://packages.microsoft.com/config/` .</span><span class="sxs-lookup"><span data-stu-id="4d5ea-137">Note your distribution and version, and identify the closest entry (by major, then minor) for it under `https://packages.microsoft.com/config/`.</span></span> <span data-ttu-id="4d5ea-138">Par exemple, RHEL 7.9 est plus proche de 7,4 que de 8.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-138">For instance, RHEL 7.9 is closer to 7.4 than to 8.</span></span>

    <span data-ttu-id="4d5ea-139">Dans les commandes ci-dessous, *remplacez [distro]* et *[version]* par les informations que vous avez identifiées :</span><span class="sxs-lookup"><span data-stu-id="4d5ea-139">In the below commands, replace *[distro]* and *[version]* with the information you've identified:</span></span>

    > [!NOTE]
    > <span data-ttu-id="4d5ea-140">Dans le cas d’Oracle Linux, *remplacez [distro]* par « rhel ».</span><span class="sxs-lookup"><span data-stu-id="4d5ea-140">In case of Oracle Linux, replace *[distro]* with “rhel”.</span></span>

    ```bash
    sudo yum-config-manager --add-repo=https://packages.microsoft.com/config/[distro]/[version]/[channel].repo
    ```

    <span data-ttu-id="4d5ea-141">Par exemple, si vous exécutez CentOS 7 et que vous souhaitez déployer Defender pour Endpoint sur Linux à partir du *canal prod* :</span><span class="sxs-lookup"><span data-stu-id="4d5ea-141">For example, if you are running CentOS 7 and want to deploy Defender for Endpoint on Linux from the *prod* channel:</span></span>

    ```bash
    sudo yum-config-manager --add-repo=https://packages.microsoft.com/config/centos/7/prod.repo
    ```

    <span data-ttu-id="4d5ea-142">Ou si vous souhaitez explorer de nouvelles fonctionnalités sur des appareils sélectionnés, vous pouvez déployer MDE pour Linux sur un canal rapide pour les *insiders* :</span><span class="sxs-lookup"><span data-stu-id="4d5ea-142">Or if you wish to explore new features on selected devices, you might want to deploy MDE for Linux to *insiders-fast* channel:</span></span>

    ```bash
    sudo yum-config-manager --add-repo=https://packages.microsoft.com/config/centos/7/insiders-fast.repo
    ```

- <span data-ttu-id="4d5ea-143">Installez la clé publique Microsoft GPG :</span><span class="sxs-lookup"><span data-stu-id="4d5ea-143">Install the Microsoft GPG public key:</span></span>

    ```bash
    sudo rpm --import http://packages.microsoft.com/keys/microsoft.asc
    ```

- <span data-ttu-id="4d5ea-144">Téléchargez et rendez utilisables toutes les métadonnées pour les référentiels yum actuellement activés :</span><span class="sxs-lookup"><span data-stu-id="4d5ea-144">Download and make usable all the metadata for the currently enabled yum repositories:</span></span>

    ```bash
    yum makecache
    ```

### <a name="sles-and-variants"></a><span data-ttu-id="4d5ea-145">SLES et variantes</span><span class="sxs-lookup"><span data-stu-id="4d5ea-145">SLES and variants</span></span>

- <span data-ttu-id="4d5ea-146">Notez votre distribution et version, et identifiez l’entrée la plus proche (par majeure, puis mineure) sous `https://packages.microsoft.com/config/` .</span><span class="sxs-lookup"><span data-stu-id="4d5ea-146">Note your distribution and version, and identify the closest entry(by major, then minor) for it under `https://packages.microsoft.com/config/`.</span></span>

    <span data-ttu-id="4d5ea-147">Dans les commandes suivantes, *remplacez [distro]* et *[version]* par les informations que vous avez identifiées :</span><span class="sxs-lookup"><span data-stu-id="4d5ea-147">In the following commands, replace *[distro]* and *[version]* with the information you've identified:</span></span>

    ```bash
    sudo zypper addrepo -c -f -n microsoft-[channel] https://packages.microsoft.com/config/[distro]/[version]/[channel].repo
    ```

    <span data-ttu-id="4d5ea-148">Par exemple, si vous exécutez SLES 12 et que vous souhaitez déployer MDE pour Linux à partir du *canal prod* :</span><span class="sxs-lookup"><span data-stu-id="4d5ea-148">For example, if you are running SLES 12 and wish to deploy MDE for Linux from the *prod* channel:</span></span>

    ```bash
    sudo zypper addrepo -c -f -n microsoft-prod https://packages.microsoft.com/config/sles/12/prod.repo
    ```

- <span data-ttu-id="4d5ea-149">Installez la clé publique Microsoft GPG :</span><span class="sxs-lookup"><span data-stu-id="4d5ea-149">Install the Microsoft GPG public key:</span></span>

    ```bash
    sudo rpm --import http://packages.microsoft.com/keys/microsoft.asc
    ```

### <a name="ubuntu-and-debian-systems"></a><span data-ttu-id="4d5ea-150">Systèmes Ubuntu et Debian</span><span class="sxs-lookup"><span data-stu-id="4d5ea-150">Ubuntu and Debian systems</span></span>

- <span data-ttu-id="4d5ea-151">Installez `curl` s’il n’est pas encore installé :</span><span class="sxs-lookup"><span data-stu-id="4d5ea-151">Install `curl` if it isn't installed yet:</span></span>

    ```bash
    sudo apt-get install curl
    ```

- <span data-ttu-id="4d5ea-152">Installez `libplist-utils` s’il n’est pas encore installé :</span><span class="sxs-lookup"><span data-stu-id="4d5ea-152">Install `libplist-utils` if it isn't installed yet:</span></span>

    ```bash
    sudo apt-get install libplist-utils
    ```

- <span data-ttu-id="4d5ea-153">Notez votre distribution et version, et identifiez l’entrée la plus proche (par majeure, puis mineure) sous `https://packages.microsoft.com/config` .</span><span class="sxs-lookup"><span data-stu-id="4d5ea-153">Note your distribution and version, and identify the closest entry (by major, then minor) for it under `https://packages.microsoft.com/config`.</span></span>

    <span data-ttu-id="4d5ea-154">Dans la commande ci-dessous, *remplacez [distro]* et *[version]* par les informations que vous avez identifiées :</span><span class="sxs-lookup"><span data-stu-id="4d5ea-154">In the below command, replace *[distro]* and *[version]* with the information you've identified:</span></span>

    ```bash
    curl -o microsoft.list https://packages.microsoft.com/config/[distro]/[version]/[channel].list
    ```

    <span data-ttu-id="4d5ea-155">Par exemple, si vous exécutez Ubuntu 18.04 et que vous souhaitez déployer MDE pour Linux à partir du *canal prod* :</span><span class="sxs-lookup"><span data-stu-id="4d5ea-155">For example, if you are running Ubuntu 18.04 and wish to deploy MDE for Linux from the *prod* channel:</span></span>

    ```bash
    curl -o microsoft.list https://packages.microsoft.com/config/ubuntu/18.04/prod.list
    ```

- <span data-ttu-id="4d5ea-156">Installez la configuration du référentiel :</span><span class="sxs-lookup"><span data-stu-id="4d5ea-156">Install the repository configuration:</span></span>

    ```bash
    sudo mv ./microsoft.list /etc/apt/sources.list.d/microsoft-[channel].list
    ```
    <span data-ttu-id="4d5ea-157">Par exemple, si vous avez choisi *le canal prod* :</span><span class="sxs-lookup"><span data-stu-id="4d5ea-157">For example, if you chose *prod* channel:</span></span>

    ```bash
    sudo mv ./microsoft.list /etc/apt/sources.list.d/microsoft-prod.list
    ```

- <span data-ttu-id="4d5ea-158">Installez le `gpg` package s’il n’est pas déjà installé :</span><span class="sxs-lookup"><span data-stu-id="4d5ea-158">Install the `gpg` package if not already installed:</span></span>

    ```bash
    sudo apt-get install gpg
    ```

  <span data-ttu-id="4d5ea-159">Si `gpg` ce n’est pas le cas, `gnupg` installez.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-159">If `gpg` is not available, then install `gnupg`.</span></span>

- <span data-ttu-id="4d5ea-160">Installez la clé publique Microsoft GPG :</span><span class="sxs-lookup"><span data-stu-id="4d5ea-160">Install the Microsoft GPG public key:</span></span>

    ```bash
    curl https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -
    ```

- <span data-ttu-id="4d5ea-161">Installez le pilote https s’il n’est pas déjà présent :</span><span class="sxs-lookup"><span data-stu-id="4d5ea-161">Install the https driver if it's not already present:</span></span>

    ```bash
    sudo apt-get install apt-transport-https
    ```

- <span data-ttu-id="4d5ea-162">Mettez à jour les métadonnées du référentiel :</span><span class="sxs-lookup"><span data-stu-id="4d5ea-162">Update the repository metadata:</span></span>

    ```bash
    sudo apt-get update
    ```

## <a name="application-installation"></a><span data-ttu-id="4d5ea-163">Installation de l’application</span><span class="sxs-lookup"><span data-stu-id="4d5ea-163">Application installation</span></span>

- <span data-ttu-id="4d5ea-164">RHEL et variantes (CentOS et Oracle Linux) :</span><span class="sxs-lookup"><span data-stu-id="4d5ea-164">RHEL and variants (CentOS and Oracle Linux):</span></span>

    ```bash
    sudo yum install mdatp
    ```

    <span data-ttu-id="4d5ea-165">Si plusieurs référentiels Microsoft sont configurés sur votre appareil, vous pouvez être spécifique au référentiel à partir duquel installer le package.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-165">If you have multiple Microsoft repositories configured on your device, you can be specific about which repository to install the package from.</span></span> <span data-ttu-id="4d5ea-166">L’exemple suivant montre comment installer le package à partir du canal si vous avez également configuré le canal de référentiel `production` `insiders-fast` sur cet appareil.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-166">The following example shows how to install the package from the `production` channel if you also have the `insiders-fast` repository channel configured on this device.</span></span> <span data-ttu-id="4d5ea-167">Cette situation peut se produire si vous utilisez plusieurs produits Microsoft sur votre appareil.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-167">This situation can happen if you are using multiple Microsoft products on your device.</span></span> <span data-ttu-id="4d5ea-168">Selon la distribution et la version de votre serveur, l’alias du référentiel peut être différent de celui de l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-168">Depending on the distribution and the version of your server, the repository alias might be different than the one in the following example.</span></span>

    ```bash
    # list all repositories
    yum repolist
    ```
    ```Output
    ...
    packages-microsoft-com-prod               packages-microsoft-com-prod        316
    packages-microsoft-com-prod-insiders-fast packages-microsoft-com-prod-ins      2
    ...
    ```
    ```bash
    # install the package from the production repository
    sudo yum --enablerepo=packages-microsoft-com-prod install mdatp
    ```

- <span data-ttu-id="4d5ea-169">SLES et variantes :</span><span class="sxs-lookup"><span data-stu-id="4d5ea-169">SLES and variants:</span></span>

    ```bash
    sudo zypper install mdatp
    ```

    <span data-ttu-id="4d5ea-170">Si plusieurs référentiels Microsoft sont configurés sur votre appareil, vous pouvez être spécifique au référentiel à partir duquel installer le package.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-170">If you have multiple Microsoft repositories configured on your device, you can be specific about which repository to install the package from.</span></span> <span data-ttu-id="4d5ea-171">L’exemple suivant montre comment installer le package à partir du canal si vous avez également configuré le canal de référentiel `production` `insiders-fast` sur cet appareil.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-171">The following example shows how to install the package from the `production` channel if you also have the `insiders-fast` repository channel configured on this device.</span></span> <span data-ttu-id="4d5ea-172">Cette situation peut se produire si vous utilisez plusieurs produits Microsoft sur votre appareil.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-172">This situation can happen if you are using multiple Microsoft products on your device.</span></span>

    ```bash
    zypper repos
    ```

    ```Output
    ...
    #  | Alias | Name | ...
    XX | packages-microsoft-com-insiders-fast | microsoft-insiders-fast | ...
    XX | packages-microsoft-com-prod | microsoft-prod | ...
    ...
    ```
    ```bash
    sudo zypper install packages-microsoft-com-prod:mdatp
    ```

- <span data-ttu-id="4d5ea-173">Système Ubuntu et Debian :</span><span class="sxs-lookup"><span data-stu-id="4d5ea-173">Ubuntu and Debian system:</span></span>

    ```bash
    sudo apt-get install mdatp
    ```

    <span data-ttu-id="4d5ea-174">Si plusieurs référentiels Microsoft sont configurés sur votre appareil, vous pouvez être spécifique au référentiel à partir duquel installer le package.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-174">If you have multiple Microsoft repositories configured on your device, you can be specific about which repository to install the package from.</span></span> <span data-ttu-id="4d5ea-175">L’exemple suivant montre comment installer le package à partir du canal si vous avez également configuré le canal de référentiel `production` `insiders-fast` sur cet appareil.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-175">The following example shows how to install the package from the `production` channel if you also have the `insiders-fast` repository channel configured on this device.</span></span> <span data-ttu-id="4d5ea-176">Cette situation peut se produire si vous utilisez plusieurs produits Microsoft sur votre appareil.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-176">This situation can happen if you are using multiple Microsoft products on your device.</span></span>

    ```bash
    cat /etc/apt/sources.list.d/*
    ```
    ```Output
    deb [arch=arm64,armhf,amd64] https://packages.microsoft.com/ubuntu/18.04/prod insiders-fast main
    deb [arch=amd64] https://packages.microsoft.com/ubuntu/18.04/prod bionic main
    ```
    ```bash
    sudo apt -t bionic install mdatp
    ```

## <a name="download-the-onboarding-package"></a><span data-ttu-id="4d5ea-177">Télécharger le package d’intégration</span><span class="sxs-lookup"><span data-stu-id="4d5ea-177">Download the onboarding package</span></span>

<span data-ttu-id="4d5ea-178">Téléchargez le package d’intégration à partir Centre de sécurité Microsoft Defender :</span><span class="sxs-lookup"><span data-stu-id="4d5ea-178">Download the onboarding package from Microsoft Defender Security Center:</span></span>

1. <span data-ttu-id="4d5ea-179">In Centre de sécurité Microsoft Defender, go to **Paramètres > Device Management > Onboarding**.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-179">In Microsoft Defender Security Center, go to **Settings > Device Management > Onboarding**.</span></span>
2. <span data-ttu-id="4d5ea-180">Dans le premier menu déroulant, sélectionnez **Linux Server comme** système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-180">In the first drop-down menu, select **Linux Server** as the operating system.</span></span> <span data-ttu-id="4d5ea-181">Dans le deuxième menu déroulant, sélectionnez **Script local (pour 10** appareils au plus) comme méthode de déploiement.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-181">In the second drop-down menu, select **Local Script (for up to 10 devices)** as the deployment method.</span></span>
3. <span data-ttu-id="4d5ea-182">Sélectionnez **Télécharger le package d’intégration.**</span><span class="sxs-lookup"><span data-stu-id="4d5ea-182">Select **Download onboarding package**.</span></span> <span data-ttu-id="4d5ea-183">Enregistrez le fichier sous WindowsDefenderATPOnboardingPackage.zip.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-183">Save the file as WindowsDefenderATPOnboardingPackage.zip.</span></span>

    ![Centre de sécurité Microsoft Defender capture d’écran](images/atp-portal-onboarding-linux.png)

4. <span data-ttu-id="4d5ea-185">À partir d’une invite de commandes, vérifiez que vous avez le fichier.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-185">From a command prompt, verify that you have the file.</span></span>
    <span data-ttu-id="4d5ea-186">Extrayons le contenu de l’archive :</span><span class="sxs-lookup"><span data-stu-id="4d5ea-186">Extract the contents of the archive:</span></span>

    ```bash
    ls -l
    ```

    ```Output
    total 8
    -rw-r--r-- 1 test  staff  5752 Feb 18 11:22 WindowsDefenderATPOnboardingPackage.zip
    ```

    ```bash
    unzip WindowsDefenderATPOnboardingPackage.zip
    ```
    ```Output
    Archive:  WindowsDefenderATPOnboardingPackage.zip
    inflating: MicrosoftDefenderATPOnboardingLinuxServer.py
    ```


## <a name="client-configuration"></a><span data-ttu-id="4d5ea-187">Configuration du client</span><span class="sxs-lookup"><span data-stu-id="4d5ea-187">Client configuration</span></span>

1. <span data-ttu-id="4d5ea-188">Copiez MicrosoftDefenderATPOnboardingLinuxServer.py vers l’appareil cible.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-188">Copy MicrosoftDefenderATPOnboardingLinuxServer.py to the target device.</span></span>

    <span data-ttu-id="4d5ea-189">Initialement, l’appareil client n’est pas associé à une organisation.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-189">Initially the client device is not associated with an organization.</span></span> <span data-ttu-id="4d5ea-190">Notez que *l’attribut orgId* est vide :</span><span class="sxs-lookup"><span data-stu-id="4d5ea-190">Note that the *orgId* attribute is blank:</span></span>

    ```bash
    mdatp health --field org_id
    ```

2. <span data-ttu-id="4d5ea-191">Exécutez MicrosoftDefenderATPOnboardingLinuxServer.py et notez que, pour exécuter cette commande, vous devez avoir `python` installé sur l’appareil :</span><span class="sxs-lookup"><span data-stu-id="4d5ea-191">Run MicrosoftDefenderATPOnboardingLinuxServer.py, and note that, in order to run this command, you must have `python` installed on the device:</span></span>

    ```bash
    python MicrosoftDefenderATPOnboardingLinuxServer.py
    ```

3. <span data-ttu-id="4d5ea-192">Vérifiez que l’appareil est désormais associé à votre organisation et signale un identificateur d’organisation valide :</span><span class="sxs-lookup"><span data-stu-id="4d5ea-192">Verify that the device is now associated with your organization and reports a valid organization identifier:</span></span>

    ```bash
    mdatp health --field org_id
    ```

4. <span data-ttu-id="4d5ea-193">Quelques minutes après avoir terminé l’installation, vous pouvez voir l’état en exécutant la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-193">A few minutes after you complete the installation, you can see the status by running the following command.</span></span> <span data-ttu-id="4d5ea-194">Une valeur de retour `1` de indique que le produit fonctionne comme prévu :</span><span class="sxs-lookup"><span data-stu-id="4d5ea-194">A return value of `1` denotes that the product is functioning as expected:</span></span>

    ```bash
    mdatp health --field healthy
    ```

    > [!IMPORTANT]
    > <span data-ttu-id="4d5ea-195">Lorsque le produit démarre pour la première fois, il télécharge les dernières définitions de logiciel anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-195">When the product starts for the first time, it downloads the latest antimalware definitions.</span></span> <span data-ttu-id="4d5ea-196">Selon votre connexion Internet, cela peut prendre jusqu’à quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-196">Depending on your Internet connection, this can take up to a few minutes.</span></span> <span data-ttu-id="4d5ea-197">Pendant ce temps, la commande ci-dessus renvoie une valeur de `false` .</span><span class="sxs-lookup"><span data-stu-id="4d5ea-197">During this time the above command returns a value of `false`.</span></span> <span data-ttu-id="4d5ea-198">Vous pouvez vérifier l’état de la mise à jour des définitions à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="4d5ea-198">You can check the status of the definition update using the following command:</span></span>
    > ```bash
    > mdatp health --field definitions_status
    > ```
    > <span data-ttu-id="4d5ea-199">Notez que vous devrez peut-être également configurer un proxy après avoir terminé l’installation initiale.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-199">Please note that you may also need to configure a proxy after completing the initial installation.</span></span> <span data-ttu-id="4d5ea-200">Voir Configurer Defender pour endpoint sur Linux pour [la découverte de proxy statique : configuration post-installation.](/microsoft-365/security/defender-endpoint/linux-static-proxy-configuration#post-installation-configuration)</span><span class="sxs-lookup"><span data-stu-id="4d5ea-200">See [Configure Defender for Endpoint on Linux for static proxy discovery: Post-installation configuration](/microsoft-365/security/defender-endpoint/linux-static-proxy-configuration#post-installation-configuration).</span></span>

5. <span data-ttu-id="4d5ea-201">Exécutez un test de détection pour vérifier que l’appareil est correctement intégré et signaler au service.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-201">Run a detection test to verify that the device is properly onboarded and reporting to the service.</span></span> <span data-ttu-id="4d5ea-202">Effectuez les étapes suivantes sur l’appareil nouvellement intégré :</span><span class="sxs-lookup"><span data-stu-id="4d5ea-202">Perform the following steps on the newly onboarded device:</span></span>

    - <span data-ttu-id="4d5ea-203">Assurez-vous que la protection en temps réel est activée (en raison de l’exécution de `1` la commande suivante) :</span><span class="sxs-lookup"><span data-stu-id="4d5ea-203">Ensure that real-time protection is enabled (denoted by a result of `1` from running the following command):</span></span>

        ```bash
        mdatp health --field real_time_protection_enabled
        ```

    - <span data-ttu-id="4d5ea-204">Ouvrez une fenêtre Terminal.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-204">Open a Terminal window.</span></span> <span data-ttu-id="4d5ea-205">Copiez et exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="4d5ea-205">Copy and execute the following command:</span></span>

        ``` bash
        curl -o /tmp/eicar.com.txt https://www.eicar.org/download/eicar.com.txt
        ```

    - <span data-ttu-id="4d5ea-206">Le fichier doit avoir été mis en quarantaine par Defender for Endpoint sur Linux.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-206">The file should have been quarantined by Defender for Endpoint on Linux.</span></span> <span data-ttu-id="4d5ea-207">Utilisez la commande suivante pour lister toutes les menaces détectées :</span><span class="sxs-lookup"><span data-stu-id="4d5ea-207">Use the following command to list all the detected threats:</span></span>

        ```bash
        mdatp threat list
        ```

## <a name="experience-linux-endpoint-detection-and-response-edr-capabilities-with-simulated-attacks"></a><span data-ttu-id="4d5ea-208">Expérience des fonctionnalités protection évolutive des points de terminaison (PEPT) Linux avec des attaques simulées</span><span class="sxs-lookup"><span data-stu-id="4d5ea-208">Experience Linux endpoint detection and response (EDR) capabilities with simulated attacks</span></span>

<span data-ttu-id="4d5ea-209">Pour tester les fonctionnalités de PEPT linux, suivez les étapes ci-dessous pour simuler une détection sur votre serveur Linux et examiner le cas.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-209">To test out the functionalities of EDR for Linux, follow the steps below to simulate a detection on your Linux server and investigate the case.</span></span> 

1.  <span data-ttu-id="4d5ea-210">Vérifiez que le serveur Linux intégré apparaît dans Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-210">Verify that the onboarded Linux server appears in Microsoft Defender Security Center.</span></span> <span data-ttu-id="4d5ea-211">S’il s’agit de la première intégration de l’ordinateur, son apparition peut prendre jusqu’à 20 minutes.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-211">If this is the first onboarding of the machine, it can take up to 20 minutes until it appears.</span></span> 

2.  <span data-ttu-id="4d5ea-212">Téléchargez et extrayez [le fichier de script](https://aka.ms/LinuxDIY) sur un serveur Linux intégré et exécutez la commande suivante : `./mde_linux_edr_diy.sh`</span><span class="sxs-lookup"><span data-stu-id="4d5ea-212">Download and extract the [script file](https://aka.ms/LinuxDIY) to an onboarded Linux server and run the following command: `./mde_linux_edr_diy.sh`</span></span>

3.  <span data-ttu-id="4d5ea-213">Après quelques minutes, une détection doit être détectée dans Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-213">After a few minutes, a detection should be raised in Microsoft Defender Security Center.</span></span>

4.  <span data-ttu-id="4d5ea-214">Regardez les détails de l’alerte, la chronologie de l’ordinateur et effectuez vos étapes d’examen classiques.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-214">Look at the alert details, machine timeline, and perform your typical investigation steps.</span></span>




## <a name="installer-script"></a><span data-ttu-id="4d5ea-215">Script du programme d’installation</span><span class="sxs-lookup"><span data-stu-id="4d5ea-215">Installer script</span></span>

<span data-ttu-id="4d5ea-216">Vous pouvez également utiliser un script bash de [programme](https://github.com/microsoft/mdatp-xplat/blob/master/linux/installation/mde_installer.sh) d’installation automatisé fourni dans notre référentiel [GitHub public.](https://github.com/microsoft/mdatp-xplat/)</span><span class="sxs-lookup"><span data-stu-id="4d5ea-216">Alternatively, you can use an automated [installer bash script](https://github.com/microsoft/mdatp-xplat/blob/master/linux/installation/mde_installer.sh) provided in our [public GitHub repository](https://github.com/microsoft/mdatp-xplat/).</span></span>
<span data-ttu-id="4d5ea-217">Le script identifie la distribution et la version, et définit l’appareil pour qu’il tire le dernier package et l’installe.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-217">The script identifies the distribution and version, and sets up the device to pull the latest package and install it.</span></span>
<span data-ttu-id="4d5ea-218">Vous pouvez également intégrer un script fourni.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-218">You can also onboard with a provided script.</span></span>

```bash
❯ ./mde_installer.sh --help
usage: basename ./mde_installer.sh [OPTIONS]
Options:
-c|--channel      specify the channel from which you want to install. Default: insiders-fast
-i|--install      install the product
-r|--remove       remove the product
-u|--upgrade      upgrade the existing product
-o|--onboard      onboard/offboard the product with <onboarding_script>
-p|--passive-mode set EPP to passive mode
-t|--tag          set a tag by declaring <name> and <value>. ex: -t GROUP Coders
-m|--min_req      enforce minimum requirements
-w|--clean        remove repo from package manager for a specific channel
-v|--version      print out script version
-h|--help         display help
```

<span data-ttu-id="4d5ea-219">En savoir plus [ici.](https://github.com/microsoft/mdatp-xplat/tree/master/linux/installation)</span><span class="sxs-lookup"><span data-stu-id="4d5ea-219">Read more [here](https://github.com/microsoft/mdatp-xplat/tree/master/linux/installation).</span></span>

## <a name="log-installation-issues"></a><span data-ttu-id="4d5ea-220">Journal des problèmes d’installation</span><span class="sxs-lookup"><span data-stu-id="4d5ea-220">Log installation issues</span></span>

<span data-ttu-id="4d5ea-221">Pour [plus d’informations](linux-resources.md#log-installation-issues) sur la recherche du journal généré automatiquement par le programme d’installation en cas d’erreur, voir problèmes d’installation des journaux.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-221">See [Log installation issues](linux-resources.md#log-installation-issues) for more information on how to find the automatically generated log that is created by the installer when an error occurs.</span></span>

## <a name="operating-system-upgrades"></a><span data-ttu-id="4d5ea-222">Mises à niveau du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="4d5ea-222">Operating system upgrades</span></span>

<span data-ttu-id="4d5ea-223">Lors de la mise à niveau de votre système d’exploitation vers une nouvelle version majeure, vous devez d’abord désinstaller Defender pour Endpoint sur Linux, installer la mise à niveau, puis reconfigurer Defender pour Endpoint sur Linux sur votre appareil.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-223">When upgrading your operating system to a new major version, you must first uninstall Defender for Endpoint on Linux, install the upgrade, and finally reconfigure Defender for Endpoint on Linux on your device.</span></span>

## <a name="how-to-migrate-from-insiders-fast-to-production-channel"></a><span data-ttu-id="4d5ea-224">Comment migrer de Insiders-Fast canal de production</span><span class="sxs-lookup"><span data-stu-id="4d5ea-224">How to migrate from Insiders-Fast to Production channel</span></span>

1. <span data-ttu-id="4d5ea-225">Désinstallez la version « Insiders-Fast channel » de MDE pour Linux.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-225">Uninstall the “Insiders-Fast channel” version of MDE for Linux.</span></span>

    ``
    sudo yum remove mdatp
    ``

1. <span data-ttu-id="4d5ea-226">Désactiver le MDE pour le Insiders-Fast Linux  ``
    sudo yum repolist
    ``</span><span class="sxs-lookup"><span data-stu-id="4d5ea-226">Disable the MDE for Linux Insiders-Fast repo  ``
    sudo yum repolist
 ``</span></span>

    > [!NOTE]
    > <span data-ttu-id="4d5ea-227">La sortie doit afficher « packages-microsoft-com-fast-prod ».</span><span class="sxs-lookup"><span data-stu-id="4d5ea-227">The output should show “packages-microsoft-com-fast-prod”.</span></span>

    ``
    sudo yum-config-manager --disable packages-microsoft-com-fast-prod
    ``
1. <span data-ttu-id="4d5ea-228">Redéployer MDE pour Linux à l’aide du « canal de production ».</span><span class="sxs-lookup"><span data-stu-id="4d5ea-228">Redeploy MDE for Linux using the “Production channel”.</span></span>


## <a name="uninstallation"></a><span data-ttu-id="4d5ea-229">Désinstallation</span><span class="sxs-lookup"><span data-stu-id="4d5ea-229">Uninstallation</span></span>

<span data-ttu-id="4d5ea-230">Voir [Désinstaller](linux-resources.md#uninstall) pour plus d’informations sur la suppression de Defender for Endpoint sur Linux des appareils clients.</span><span class="sxs-lookup"><span data-stu-id="4d5ea-230">See [Uninstall](linux-resources.md#uninstall) for details on how to remove Defender for Endpoint on Linux from client devices.</span></span>

## <a name="see-also"></a><span data-ttu-id="4d5ea-231">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d5ea-231">See also</span></span>
- [<span data-ttu-id="4d5ea-232">Rechercher les problèmes d’état d’intégrité de l’agent</span><span class="sxs-lookup"><span data-stu-id="4d5ea-232">Investigate agent health issues</span></span>](health-status.md)
