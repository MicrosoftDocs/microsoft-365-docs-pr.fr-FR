---
title: Déployer Microsoft Defender ATP pour Linux manuellement
ms.reviewer: ''
description: Décrit comment déployer Microsoft Defender ATP pour Linux manuellement à partir de la ligne de commande.
keywords: microsoft, defender, atp, linux, installation, déployer, désinstallation, casque, ansible, linux, redhat, ubuntu, debian, sles, suse, centos
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
ms.openlocfilehash: 6726671a1e38d80a91787f495d3e09884bc879f4
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51064254"
---
# <a name="deploy-microsoft-defender-for-endpoint-for-linux-manually"></a><span data-ttu-id="fad8f-104">Déployer Microsoft Defender pour le point de terminaison pour Linux manuellement</span><span class="sxs-lookup"><span data-stu-id="fad8f-104">Deploy Microsoft Defender for Endpoint for Linux manually</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="fad8f-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="fad8f-105">**Applies to:**</span></span>
- [<span data-ttu-id="fad8f-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="fad8f-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2146631)
- [<span data-ttu-id="fad8f-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="fad8f-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="fad8f-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="fad8f-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="fad8f-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="fad8f-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigateip-abovefoldlink)

<span data-ttu-id="fad8f-110">Cet article explique comment déployer Microsoft Defender pour Endpoint pour Linux manuellement.</span><span class="sxs-lookup"><span data-stu-id="fad8f-110">This article describes how to deploy Microsoft Defender for Endpoint for Linux manually.</span></span> <span data-ttu-id="fad8f-111">Un déploiement réussi nécessite l’exécution de toutes les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="fad8f-111">A successful deployment requires the completion of all of the following tasks:</span></span>

- [<span data-ttu-id="fad8f-112">Déployer Microsoft Defender pour le point de terminaison pour Linux manuellement</span><span class="sxs-lookup"><span data-stu-id="fad8f-112">Deploy Microsoft Defender for Endpoint for Linux manually</span></span>](#deploy-microsoft-defender-for-endpoint-for-linux-manually)
  - [<span data-ttu-id="fad8f-113">Conditions préalables et système requis</span><span class="sxs-lookup"><span data-stu-id="fad8f-113">Prerequisites and system requirements</span></span>](#prerequisites-and-system-requirements)
  - [<span data-ttu-id="fad8f-114">Configurer le référentiel de logiciels Linux</span><span class="sxs-lookup"><span data-stu-id="fad8f-114">Configure the Linux software repository</span></span>](#configure-the-linux-software-repository)
    - [<span data-ttu-id="fad8f-115">RHEL et variantes (CentOS et Oracle Linux)</span><span class="sxs-lookup"><span data-stu-id="fad8f-115">RHEL and variants (CentOS and Oracle Linux)</span></span>](#rhel-and-variants-centos-and-oracle-linux)
    - [<span data-ttu-id="fad8f-116">SLES et variantes</span><span class="sxs-lookup"><span data-stu-id="fad8f-116">SLES and variants</span></span>](#sles-and-variants)
    - [<span data-ttu-id="fad8f-117">Systèmes Ubuntu et Debian</span><span class="sxs-lookup"><span data-stu-id="fad8f-117">Ubuntu and Debian systems</span></span>](#ubuntu-and-debian-systems)
  - [<span data-ttu-id="fad8f-118">Installation de l’application</span><span class="sxs-lookup"><span data-stu-id="fad8f-118">Application installation</span></span>](#application-installation)
  - [<span data-ttu-id="fad8f-119">Télécharger le package d’intégration</span><span class="sxs-lookup"><span data-stu-id="fad8f-119">Download the onboarding package</span></span>](#download-the-onboarding-package)
  - [<span data-ttu-id="fad8f-120">Configuration du client</span><span class="sxs-lookup"><span data-stu-id="fad8f-120">Client configuration</span></span>](#client-configuration)
  - [<span data-ttu-id="fad8f-121">Script du programme d’installation</span><span class="sxs-lookup"><span data-stu-id="fad8f-121">Installer script</span></span>](#installer-script)
  - [<span data-ttu-id="fad8f-122">Journaux des problèmes d’installation</span><span class="sxs-lookup"><span data-stu-id="fad8f-122">Log installation issues</span></span>](#log-installation-issues)
  - [<span data-ttu-id="fad8f-123">Mises à niveau du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="fad8f-123">Operating system upgrades</span></span>](#operating-system-upgrades)
  - [<span data-ttu-id="fad8f-124">Désinstallation</span><span class="sxs-lookup"><span data-stu-id="fad8f-124">Uninstallation</span></span>](#uninstallation)

## <a name="prerequisites-and-system-requirements"></a><span data-ttu-id="fad8f-125">Conditions préalables et système requis</span><span class="sxs-lookup"><span data-stu-id="fad8f-125">Prerequisites and system requirements</span></span>

<span data-ttu-id="fad8f-126">Avant de commencer, consultez [Microsoft Defender pour Endpoint pour Linux](microsoft-defender-endpoint-linux.md) pour obtenir une description des conditions préalables et de la requise pour la version logicielle actuelle.</span><span class="sxs-lookup"><span data-stu-id="fad8f-126">Before you get started, see [Microsoft Defender for Endpoint for Linux](microsoft-defender-endpoint-linux.md) for a description of prerequisites and system requirements for the current software version.</span></span>

## <a name="configure-the-linux-software-repository"></a><span data-ttu-id="fad8f-127">Configurer le référentiel de logiciels Linux</span><span class="sxs-lookup"><span data-stu-id="fad8f-127">Configure the Linux software repository</span></span>

<span data-ttu-id="fad8f-128">Defender pour le point de terminaison pour Linux peut être déployé à partir de l’un des canaux suivants (indiqués ci-dessous sous le nom *[canal]*) : *insiders-fast,* *insiders-slow* ou *prod*. Chacun de ces canaux correspond à un référentiel de logiciels Linux.</span><span class="sxs-lookup"><span data-stu-id="fad8f-128">Defender for Endpoint for Linux can be deployed from one of the following channels (denoted below as *[channel]*): *insiders-fast*, *insiders-slow*, or *prod*. Each of these channels corresponds to a Linux software repository.</span></span> <span data-ttu-id="fad8f-129">Les instructions de configuration de votre appareil pour utiliser l’un de ces référentiels sont fournies ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="fad8f-129">Instructions for configuring your device to use one of these repositories are provided below.</span></span>

<span data-ttu-id="fad8f-130">Le choix du canal détermine le type et la fréquence des mises à jour proposées à votre appareil.</span><span class="sxs-lookup"><span data-stu-id="fad8f-130">The choice of the channel determines the type and frequency of updates that are offered to your device.</span></span> <span data-ttu-id="fad8f-131">Les appareils *internes rapides* sont les premiers à recevoir des mises à jour et de nouvelles fonctionnalités, suivis ultérieurement par les *insiders-slow* et enfin par *prod*.</span><span class="sxs-lookup"><span data-stu-id="fad8f-131">Devices in *insiders-fast* are the first ones to receive updates and new features, followed later by *insiders-slow* and lastly by *prod*.</span></span>

<span data-ttu-id="fad8f-132">Afin d’afficher un aperçu des nouvelles fonctionnalités et de fournir des commentaires préliminaires, il est recommandé de configurer certains appareils dans votre entreprise pour utiliser les *insiders-fast* ou *insider-slow*.</span><span class="sxs-lookup"><span data-stu-id="fad8f-132">In order to preview new features and provide early feedback, it is recommended that you configure some devices in your enterprise to use either *insiders-fast* or *insiders-slow*.</span></span>

> [!WARNING]
> <span data-ttu-id="fad8f-133">Le basculement du canal après l’installation initiale nécessite la réinstallation du produit.</span><span class="sxs-lookup"><span data-stu-id="fad8f-133">Switching the channel after the initial installation requires the product to be reinstalled.</span></span> <span data-ttu-id="fad8f-134">Pour basculer le canal de produit : désinstallez le package existant, configurez de nouveau votre appareil pour utiliser le nouveau canal et suivez les étapes de ce document pour installer le package à partir du nouvel emplacement.</span><span class="sxs-lookup"><span data-stu-id="fad8f-134">To switch the product channel: uninstall the existing package, re-configure your device to use the new channel, and follow the steps in this document to install the package from the new location.</span></span>

### <a name="rhel-and-variants-centos-and-oracle-linux"></a><span data-ttu-id="fad8f-135">RHEL et variantes (CentOS et Oracle Linux)</span><span class="sxs-lookup"><span data-stu-id="fad8f-135">RHEL and variants (CentOS and Oracle Linux)</span></span>

- <span data-ttu-id="fad8f-136">Installez `yum-utils` s’il n’est pas encore installé :</span><span class="sxs-lookup"><span data-stu-id="fad8f-136">Install `yum-utils` if it isn't installed yet:</span></span>

    ```bash
    sudo yum install yum-utils
    ```

- <span data-ttu-id="fad8f-137">Notez votre distribution et version, et identifiez l’entrée la plus proche (par majeure, puis mineure) sous `https://packages.microsoft.com/config/` .</span><span class="sxs-lookup"><span data-stu-id="fad8f-137">Note your distribution and version, and identify the closest entry (by major, then minor) for it under `https://packages.microsoft.com/config/`.</span></span> <span data-ttu-id="fad8f-138">Par exemple, RHEL 7.9 est plus proche de 7,4 que de 8.</span><span class="sxs-lookup"><span data-stu-id="fad8f-138">For instance, RHEL 7.9 is closer to 7.4 than to 8.</span></span>

    <span data-ttu-id="fad8f-139">Dans les commandes ci-dessous, *remplacez [distro]* et *[version]* par les informations que vous avez identifiées :</span><span class="sxs-lookup"><span data-stu-id="fad8f-139">In the below commands, replace *[distro]* and *[version]* with the information you've identified:</span></span>

    > [!NOTE]
    > <span data-ttu-id="fad8f-140">Dans le cas d’Oracle Linux, *remplacez [distro]* par « rhel ».</span><span class="sxs-lookup"><span data-stu-id="fad8f-140">In case of Oracle Linux, replace *[distro]* with “rhel”.</span></span>

    ```bash
    sudo yum-config-manager --add-repo=https://packages.microsoft.com/config/[distro]/[version]/[channel].repo
    ```

    <span data-ttu-id="fad8f-141">Par exemple, si vous exécutez CentOS 7 et que vous souhaitez déployer MDE pour Linux à partir du *canal prod* :</span><span class="sxs-lookup"><span data-stu-id="fad8f-141">For example, if you are running CentOS 7 and wish to deploy MDE for Linux from the *prod* channel:</span></span>

    ```bash
    sudo yum-config-manager --add-repo=https://packages.microsoft.com/config/centos/7/prod.repo
    ```

    <span data-ttu-id="fad8f-142">Ou si vous souhaitez explorer de nouvelles fonctionnalités sur des appareils sélectionnés, vous pouvez déployer MDE pour Linux sur un canal rapide pour les *insiders* :</span><span class="sxs-lookup"><span data-stu-id="fad8f-142">Or if you wish to explore new features on selected devices, you might want to deploy MDE for Linux to *insiders-fast* channel:</span></span>

    ```bash
    sudo yum-config-manager --add-repo=https://packages.microsoft.com/config/centos/7/insiders-fast.repo
    ```

- <span data-ttu-id="fad8f-143">Installez la clé publique Microsoft GPG :</span><span class="sxs-lookup"><span data-stu-id="fad8f-143">Install the Microsoft GPG public key:</span></span>

    ```bash
    sudo rpm --import http://packages.microsoft.com/keys/microsoft.asc
    ```

- <span data-ttu-id="fad8f-144">Téléchargez et rendez utilisables toutes les métadonnées pour les référentiels yum actuellement activés :</span><span class="sxs-lookup"><span data-stu-id="fad8f-144">Download and make usable all the metadata for the currently enabled yum repositories:</span></span>

    ```bash
    yum makecache
    ```

### <a name="sles-and-variants"></a><span data-ttu-id="fad8f-145">SLES et variantes</span><span class="sxs-lookup"><span data-stu-id="fad8f-145">SLES and variants</span></span>

- <span data-ttu-id="fad8f-146">Notez votre distribution et version, et identifiez l’entrée la plus proche (par majeure, puis mineure) sous `https://packages.microsoft.com/config/` .</span><span class="sxs-lookup"><span data-stu-id="fad8f-146">Note your distribution and version, and identify the closest entry(by major, then minor) for it under `https://packages.microsoft.com/config/`.</span></span>

    <span data-ttu-id="fad8f-147">Dans les commandes suivantes, *remplacez [distro]* et *[version]* par les informations que vous avez identifiées :</span><span class="sxs-lookup"><span data-stu-id="fad8f-147">In the following commands, replace *[distro]* and *[version]* with the information you've identified:</span></span>

    ```bash
    sudo zypper addrepo -c -f -n microsoft-[channel] https://packages.microsoft.com/config/[distro]/[version]/[channel].repo
    ```

    <span data-ttu-id="fad8f-148">Par exemple, si vous exécutez SLES 12 et que vous souhaitez déployer MDE pour Linux à partir du *canal prod* :</span><span class="sxs-lookup"><span data-stu-id="fad8f-148">For example, if you are running SLES 12 and wish to deploy MDE for Linux from the *prod* channel:</span></span>

    ```bash
    sudo zypper addrepo -c -f -n microsoft-prod https://packages.microsoft.com/config/sles/12/prod.repo
    ```

- <span data-ttu-id="fad8f-149">Installez la clé publique Microsoft GPG :</span><span class="sxs-lookup"><span data-stu-id="fad8f-149">Install the Microsoft GPG public key:</span></span>

    ```bash
    sudo rpm --import http://packages.microsoft.com/keys/microsoft.asc
    ```

### <a name="ubuntu-and-debian-systems"></a><span data-ttu-id="fad8f-150">Systèmes Ubuntu et Debian</span><span class="sxs-lookup"><span data-stu-id="fad8f-150">Ubuntu and Debian systems</span></span>

- <span data-ttu-id="fad8f-151">Installez `curl` s’il n’est pas encore installé :</span><span class="sxs-lookup"><span data-stu-id="fad8f-151">Install `curl` if it isn't installed yet:</span></span>

    ```bash
    sudo apt-get install curl
    ```

- <span data-ttu-id="fad8f-152">Installez `libplist-utils` s’il n’est pas encore installé :</span><span class="sxs-lookup"><span data-stu-id="fad8f-152">Install `libplist-utils` if it isn't installed yet:</span></span>

    ```bash
    sudo apt-get install libplist-utils
    ```

- <span data-ttu-id="fad8f-153">Notez votre distribution et version, et identifiez l’entrée la plus proche (par majeure, puis mineure) sous `https://packages.microsoft.com/config` .</span><span class="sxs-lookup"><span data-stu-id="fad8f-153">Note your distribution and version, and identify the closest entry (by major, then minor) for it under `https://packages.microsoft.com/config`.</span></span>

    <span data-ttu-id="fad8f-154">Dans la commande ci-dessous, *remplacez [distro]* et *[version]* par les informations que vous avez identifiées :</span><span class="sxs-lookup"><span data-stu-id="fad8f-154">In the below command, replace *[distro]* and *[version]* with the information you've identified:</span></span>

    ```bash
    curl -o microsoft.list https://packages.microsoft.com/config/[distro]/[version]/[channel].list
    ```

    <span data-ttu-id="fad8f-155">Par exemple, si vous exécutez Ubuntu 18.04 et que vous souhaitez déployer MDE pour Linux à partir du *canal prod* :</span><span class="sxs-lookup"><span data-stu-id="fad8f-155">For example, if you are running Ubuntu 18.04 and wish to deploy MDE for Linux from the *prod* channel:</span></span>

    ```bash
    curl -o microsoft.list https://packages.microsoft.com/config/ubuntu/18.04/prod.list
    ```

- <span data-ttu-id="fad8f-156">Installez la configuration du référentiel :</span><span class="sxs-lookup"><span data-stu-id="fad8f-156">Install the repository configuration:</span></span>

    ```bash
    sudo mv ./microsoft.list /etc/apt/sources.list.d/microsoft-[channel].list
    ```
    <span data-ttu-id="fad8f-157">Par exemple, si vous avez choisi *le canal prod* :</span><span class="sxs-lookup"><span data-stu-id="fad8f-157">For example, if you chose *prod* channel:</span></span>
    
    ```bash
    sudo mv ./microsoft.list /etc/apt/sources.list.d/microsoft-prod.list
    ```   

- <span data-ttu-id="fad8f-158">Installez le `gpg` package s’il n’est pas déjà installé :</span><span class="sxs-lookup"><span data-stu-id="fad8f-158">Install the `gpg` package if not already installed:</span></span>

    ```bash
    sudo apt-get install gpg
    ```

  <span data-ttu-id="fad8f-159">Si `gpg` ce n’est pas le cas, `gnupg` installez.</span><span class="sxs-lookup"><span data-stu-id="fad8f-159">If `gpg` is not available, then install `gnupg`.</span></span>

- <span data-ttu-id="fad8f-160">Installez la clé publique Microsoft GPG :</span><span class="sxs-lookup"><span data-stu-id="fad8f-160">Install the Microsoft GPG public key:</span></span>

    ```bash
    curl https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -
    ```

- <span data-ttu-id="fad8f-161">Installez le pilote https s’il n’est pas déjà présent :</span><span class="sxs-lookup"><span data-stu-id="fad8f-161">Install the https driver if it's not already present:</span></span>

    ```bash
    sudo apt-get install apt-transport-https
    ```

- <span data-ttu-id="fad8f-162">Mettez à jour les métadonnées du référentiel :</span><span class="sxs-lookup"><span data-stu-id="fad8f-162">Update the repository metadata:</span></span>

    ```bash
    sudo apt-get update
    ```

## <a name="application-installation"></a><span data-ttu-id="fad8f-163">Installation de l’application</span><span class="sxs-lookup"><span data-stu-id="fad8f-163">Application installation</span></span>

- <span data-ttu-id="fad8f-164">RHEL et variantes (CentOS et Oracle Linux) :</span><span class="sxs-lookup"><span data-stu-id="fad8f-164">RHEL and variants (CentOS and Oracle Linux):</span></span>

    ```bash
    sudo yum install mdatp
    ```

    <span data-ttu-id="fad8f-165">Si plusieurs référentiels Microsoft sont configurés sur votre appareil, vous pouvez être spécifique au référentiel à partir duquel installer le package.</span><span class="sxs-lookup"><span data-stu-id="fad8f-165">If you have multiple Microsoft repositories configured on your device, you can be specific about which repository to install the package from.</span></span> <span data-ttu-id="fad8f-166">L’exemple suivant montre comment installer le package à partir du canal si vous avez également configuré le canal de référentiel `production` `insiders-fast` sur cet appareil.</span><span class="sxs-lookup"><span data-stu-id="fad8f-166">The following example shows how to install the package from the `production` channel if you also have the `insiders-fast` repository channel configured on this device.</span></span> <span data-ttu-id="fad8f-167">Cette situation peut se produire si vous utilisez plusieurs produits Microsoft sur votre appareil.</span><span class="sxs-lookup"><span data-stu-id="fad8f-167">This situation can happen if you are using multiple Microsoft products on your device.</span></span> <span data-ttu-id="fad8f-168">Selon la distribution et la version de votre serveur, l’alias du référentiel peut être différent de celui de l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="fad8f-168">Depending on the distribution and the version of your server, the repository alias might be different than the one in the following example.</span></span>

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

- <span data-ttu-id="fad8f-169">SLES et variantes :</span><span class="sxs-lookup"><span data-stu-id="fad8f-169">SLES and variants:</span></span>

    ```bash
    sudo zypper install mdatp
    ```

    <span data-ttu-id="fad8f-170">Si plusieurs référentiels Microsoft sont configurés sur votre appareil, vous pouvez être spécifique au référentiel à partir duquel installer le package.</span><span class="sxs-lookup"><span data-stu-id="fad8f-170">If you have multiple Microsoft repositories configured on your device, you can be specific about which repository to install the package from.</span></span> <span data-ttu-id="fad8f-171">L’exemple suivant montre comment installer le package à partir du canal si vous avez également configuré le canal de référentiel `production` `insiders-fast` sur cet appareil.</span><span class="sxs-lookup"><span data-stu-id="fad8f-171">The following example shows how to install the package from the `production` channel if you also have the `insiders-fast` repository channel configured on this device.</span></span> <span data-ttu-id="fad8f-172">Cette situation peut se produire si vous utilisez plusieurs produits Microsoft sur votre appareil.</span><span class="sxs-lookup"><span data-stu-id="fad8f-172">This situation can happen if you are using multiple Microsoft products on your device.</span></span>

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

- <span data-ttu-id="fad8f-173">Système Ubuntu et Debian :</span><span class="sxs-lookup"><span data-stu-id="fad8f-173">Ubuntu and Debian system:</span></span>

    ```bash
    sudo apt-get install mdatp
    ```

    <span data-ttu-id="fad8f-174">Si plusieurs référentiels Microsoft sont configurés sur votre appareil, vous pouvez être spécifique au référentiel à partir duquel installer le package.</span><span class="sxs-lookup"><span data-stu-id="fad8f-174">If you have multiple Microsoft repositories configured on your device, you can be specific about which repository to install the package from.</span></span> <span data-ttu-id="fad8f-175">L’exemple suivant montre comment installer le package à partir du canal si vous avez également configuré le canal de référentiel `production` `insiders-fast` sur cet appareil.</span><span class="sxs-lookup"><span data-stu-id="fad8f-175">The following example shows how to install the package from the `production` channel if you also have the `insiders-fast` repository channel configured on this device.</span></span> <span data-ttu-id="fad8f-176">Cette situation peut se produire si vous utilisez plusieurs produits Microsoft sur votre appareil.</span><span class="sxs-lookup"><span data-stu-id="fad8f-176">This situation can happen if you are using multiple Microsoft products on your device.</span></span>

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

## <a name="download-the-onboarding-package"></a><span data-ttu-id="fad8f-177">Télécharger le package d’intégration</span><span class="sxs-lookup"><span data-stu-id="fad8f-177">Download the onboarding package</span></span>

<span data-ttu-id="fad8f-178">Téléchargez le package d’intégration à partir du Centre de sécurité Microsoft Defender :</span><span class="sxs-lookup"><span data-stu-id="fad8f-178">Download the onboarding package from Microsoft Defender Security Center:</span></span>

1. <span data-ttu-id="fad8f-179">Dans le Centre de sécurité Microsoft Defender, go to **Settings > Device Management > Onboarding**.</span><span class="sxs-lookup"><span data-stu-id="fad8f-179">In Microsoft Defender Security Center, go to **Settings > Device Management > Onboarding**.</span></span>
2. <span data-ttu-id="fad8f-180">Dans le premier menu déroulant, sélectionnez **Linux Server comme** système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="fad8f-180">In the first drop-down menu, select **Linux Server** as the operating system.</span></span> <span data-ttu-id="fad8f-181">Dans le deuxième menu déroulant, sélectionnez **Script local (pour 10** appareils au plus) comme méthode de déploiement.</span><span class="sxs-lookup"><span data-stu-id="fad8f-181">In the second drop-down menu, select **Local Script (for up to 10 devices)** as the deployment method.</span></span>
3. <span data-ttu-id="fad8f-182">Sélectionnez **Télécharger le package d’intégration.**</span><span class="sxs-lookup"><span data-stu-id="fad8f-182">Select **Download onboarding package**.</span></span> <span data-ttu-id="fad8f-183">Enregistrez le fichier sous WindowsDefenderATPOnboardingPackage.zip.</span><span class="sxs-lookup"><span data-stu-id="fad8f-183">Save the file as WindowsDefenderATPOnboardingPackage.zip.</span></span>

    ![Capture d’écran du Centre de sécurité Microsoft Defender](images/atp-portal-onboarding-linux.png)

4. <span data-ttu-id="fad8f-185">À partir d’une invite de commandes, vérifiez que vous avez le fichier.</span><span class="sxs-lookup"><span data-stu-id="fad8f-185">From a command prompt, verify that you have the file.</span></span>
    <span data-ttu-id="fad8f-186">Extrayons le contenu de l’archive :</span><span class="sxs-lookup"><span data-stu-id="fad8f-186">Extract the contents of the archive:</span></span>

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


## <a name="client-configuration"></a><span data-ttu-id="fad8f-187">Configuration du client</span><span class="sxs-lookup"><span data-stu-id="fad8f-187">Client configuration</span></span>

1. <span data-ttu-id="fad8f-188">Copiez MicrosoftDefenderATPOnboardingLinuxServer.py vers l’appareil cible.</span><span class="sxs-lookup"><span data-stu-id="fad8f-188">Copy MicrosoftDefenderATPOnboardingLinuxServer.py to the target device.</span></span>

    <span data-ttu-id="fad8f-189">Initialement, l’appareil client n’est pas associé à une organisation.</span><span class="sxs-lookup"><span data-stu-id="fad8f-189">Initially the client device is not associated with an organization.</span></span> <span data-ttu-id="fad8f-190">Notez que *l’attribut orgId* est vide :</span><span class="sxs-lookup"><span data-stu-id="fad8f-190">Note that the *orgId* attribute is blank:</span></span>

    ```bash
    mdatp health --field org_id
    ```

2. <span data-ttu-id="fad8f-191">Exécutez MicrosoftDefenderATPOnboardingLinuxServer.py et notez que, pour exécuter cette commande, vous devez avoir `python` installé sur l’appareil :</span><span class="sxs-lookup"><span data-stu-id="fad8f-191">Run MicrosoftDefenderATPOnboardingLinuxServer.py, and note that, in order to run this command, you must have `python` installed on the device:</span></span>

    ```bash
    python MicrosoftDefenderATPOnboardingLinuxServer.py
    ```

3. <span data-ttu-id="fad8f-192">Vérifiez que l’appareil est maintenant associé à votre organisation et signale un identificateur d’organisation valide :</span><span class="sxs-lookup"><span data-stu-id="fad8f-192">Verify that the device is now associated with your organization and reports a valid organization identifier:</span></span>

    ```bash
    mdatp health --field org_id
    ```

4. <span data-ttu-id="fad8f-193">Quelques minutes après avoir terminé l’installation, vous pouvez voir l’état en exécutant la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="fad8f-193">A few minutes after you complete the installation, you can see the status by running the following command.</span></span> <span data-ttu-id="fad8f-194">Une valeur de retour indique que le `1` produit fonctionne comme prévu :</span><span class="sxs-lookup"><span data-stu-id="fad8f-194">A return value of `1` denotes that the product is functioning as expected:</span></span>

    ```bash
    mdatp health --field healthy
    ```

    > [!IMPORTANT]
    > <span data-ttu-id="fad8f-195">Lorsque le produit démarre pour la première fois, il télécharge les dernières définitions de logiciel anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="fad8f-195">When the product starts for the first time, it downloads the latest antimalware definitions.</span></span> <span data-ttu-id="fad8f-196">Selon votre connexion Internet, cela peut prendre jusqu’à quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="fad8f-196">Depending on your Internet connection, this can take up to a few minutes.</span></span> <span data-ttu-id="fad8f-197">Pendant ce temps, la commande ci-dessus renvoie une valeur de `false` .</span><span class="sxs-lookup"><span data-stu-id="fad8f-197">During this time the above command returns a value of `false`.</span></span> <span data-ttu-id="fad8f-198">Vous pouvez vérifier l’état de la mise à jour des définitions à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="fad8f-198">You can check the status of the definition update using the following command:</span></span>
    > ```bash
    > mdatp health --field definitions_status
    > ```
    > <span data-ttu-id="fad8f-199">Notez que vous devrez peut-être également configurer un proxy après avoir terminé l’installation initiale.</span><span class="sxs-lookup"><span data-stu-id="fad8f-199">Please note that you may also need to configure a proxy after completing the initial installation.</span></span> <span data-ttu-id="fad8f-200">Voir [Configure Defender for Endpoint for Linux for static proxy discovery: Post-installation configuration](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/linux-static-proxy-configuration#post-installation-configuration).</span><span class="sxs-lookup"><span data-stu-id="fad8f-200">See [Configure Defender for Endpoint for Linux for static proxy discovery: Post-installation configuration](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/linux-static-proxy-configuration#post-installation-configuration).</span></span>

5. <span data-ttu-id="fad8f-201">Exécutez un test de détection pour vérifier que l’appareil est correctement intégré et signaler au service.</span><span class="sxs-lookup"><span data-stu-id="fad8f-201">Run a detection test to verify that the device is properly onboarded and reporting to the service.</span></span> <span data-ttu-id="fad8f-202">Effectuez les étapes suivantes sur l’appareil nouvellement intégré :</span><span class="sxs-lookup"><span data-stu-id="fad8f-202">Perform the following steps on the newly onboarded device:</span></span>

    - <span data-ttu-id="fad8f-203">Assurez-vous que la protection en temps réel est activée (en raison de l’exécution de `1` la commande suivante) :</span><span class="sxs-lookup"><span data-stu-id="fad8f-203">Ensure that real-time protection is enabled (denoted by a result of `1` from running the following command):</span></span>

        ```bash
        mdatp health --field real_time_protection_enabled
        ```

    - <span data-ttu-id="fad8f-204">Ouvrez une fenêtre Terminal.</span><span class="sxs-lookup"><span data-stu-id="fad8f-204">Open a Terminal window.</span></span> <span data-ttu-id="fad8f-205">Copiez et exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="fad8f-205">Copy and execute the following command:</span></span>

        ``` bash
        curl -o ~/Downloads/eicar.com.txt https://www.eicar.org/download/eicar.com.txt
        ```

    - <span data-ttu-id="fad8f-206">Le fichier doit avoir été mis en quarantaine par Defender pour Endpoint pour Linux.</span><span class="sxs-lookup"><span data-stu-id="fad8f-206">The file should have been quarantined by Defender for Endpoint for Linux.</span></span> <span data-ttu-id="fad8f-207">Utilisez la commande suivante pour lister toutes les menaces détectées :</span><span class="sxs-lookup"><span data-stu-id="fad8f-207">Use the following command to list all the detected threats:</span></span>

        ```bash
        mdatp threat list
        ```

## <a name="installer-script"></a><span data-ttu-id="fad8f-208">Script du programme d’installation</span><span class="sxs-lookup"><span data-stu-id="fad8f-208">Installer script</span></span>

<span data-ttu-id="fad8f-209">Vous pouvez également utiliser un script d’installation [bash](https://github.com/microsoft/mdatp-xplat/blob/master/linux/installation/mde_installer.sh) automatisé fourni dans notre référentiel [GitHub public.](https://github.com/microsoft/mdatp-xplat/)</span><span class="sxs-lookup"><span data-stu-id="fad8f-209">Alternatively, you can use an automated [installer bash script](https://github.com/microsoft/mdatp-xplat/blob/master/linux/installation/mde_installer.sh) provided in our [public GitHub repository](https://github.com/microsoft/mdatp-xplat/).</span></span>
<span data-ttu-id="fad8f-210">Le script identifie la distribution et la version, et définit l’appareil pour qu’il tire le dernier package et l’installe.</span><span class="sxs-lookup"><span data-stu-id="fad8f-210">The script identifies the distribution and version, and sets up the device to pull the latest package and install it.</span></span>
<span data-ttu-id="fad8f-211">Vous pouvez également intégrer un script fourni.</span><span class="sxs-lookup"><span data-stu-id="fad8f-211">You can also onboard with a provided script.</span></span>

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

<span data-ttu-id="fad8f-212">En savoir plus [ici.](https://github.com/microsoft/mdatp-xplat/tree/master/linux/installation)</span><span class="sxs-lookup"><span data-stu-id="fad8f-212">Read more [here](https://github.com/microsoft/mdatp-xplat/tree/master/linux/installation).</span></span>

## <a name="log-installation-issues"></a><span data-ttu-id="fad8f-213">Journaux des problèmes d’installation</span><span class="sxs-lookup"><span data-stu-id="fad8f-213">Log installation issues</span></span>

<span data-ttu-id="fad8f-214">Pour [plus d’informations](linux-resources.md#log-installation-issues) sur la recherche du journal généré automatiquement par le programme d’installation en cas d’erreur, voir problèmes d’installation des journaux.</span><span class="sxs-lookup"><span data-stu-id="fad8f-214">See [Log installation issues](linux-resources.md#log-installation-issues) for more information on how to find the automatically generated log that is created by the installer when an error occurs.</span></span>

## <a name="operating-system-upgrades"></a><span data-ttu-id="fad8f-215">Mises à niveau du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="fad8f-215">Operating system upgrades</span></span>

<span data-ttu-id="fad8f-216">Lors de la mise à niveau de votre système d’exploitation vers une nouvelle version majeure, vous devez d’abord désinstaller Defender pour Endpoint pour Linux, installer la mise à niveau, puis reconfigurer Defender pour Endpoint pour Linux sur votre appareil.</span><span class="sxs-lookup"><span data-stu-id="fad8f-216">When upgrading your operating system to a new major version, you must first uninstall Defender for Endpoint for Linux, install the upgrade, and finally reconfigure Defender for Endpoint for Linux on your device.</span></span>

## <a name="uninstallation"></a><span data-ttu-id="fad8f-217">Désinstallation</span><span class="sxs-lookup"><span data-stu-id="fad8f-217">Uninstallation</span></span>

<span data-ttu-id="fad8f-218">Voir [Désinstaller](linux-resources.md#uninstall) pour plus d’informations sur la suppression de Defender pour Endpoint pour Linux des appareils clients.</span><span class="sxs-lookup"><span data-stu-id="fad8f-218">See [Uninstall](linux-resources.md#uninstall) for details on how to remove Defender for Endpoint for Linux from client devices.</span></span>
