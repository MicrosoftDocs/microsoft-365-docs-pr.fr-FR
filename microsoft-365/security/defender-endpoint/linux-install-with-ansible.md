---
title: Déployer Microsoft Defender pour endpoint sur Linux avec Ansible
ms.reviewer: ''
description: Décrit comment déployer Microsoft Defender pour endpoint sur Linux à l'aide d'Ansible.
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
ms.openlocfilehash: 15ee02d90e81c48bf5ec718e669bf8f88f6424ff
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51934776"
---
# <a name="deploy-microsoft-defender-for-endpoint-on-linux-with-ansible"></a><span data-ttu-id="367bb-104">Déployer Microsoft Defender pour endpoint sur Linux avec Ansible</span><span class="sxs-lookup"><span data-stu-id="367bb-104">Deploy Microsoft Defender for Endpoint on Linux with Ansible</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="367bb-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="367bb-105">**Applies to:**</span></span>
- [<span data-ttu-id="367bb-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="367bb-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="367bb-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="367bb-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="367bb-108">Vous souhaitez faire l'expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="367bb-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="367bb-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="367bb-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigateip-abovefoldlink)

<span data-ttu-id="367bb-110">Cet article explique comment déployer Defender pour endpoint sur Linux à l'aide d'Ansible.</span><span class="sxs-lookup"><span data-stu-id="367bb-110">This article describes how to deploy Defender for Endpoint on Linux using Ansible.</span></span> <span data-ttu-id="367bb-111">Un déploiement réussi nécessite l'exécution de toutes les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="367bb-111">A successful deployment requires the completion of all of the following tasks:</span></span>

- [<span data-ttu-id="367bb-112">Télécharger le package d'intégration</span><span class="sxs-lookup"><span data-stu-id="367bb-112">Download the onboarding package</span></span>](#download-the-onboarding-package)
- [<span data-ttu-id="367bb-113">Créer des fichiers YAML ansibles</span><span class="sxs-lookup"><span data-stu-id="367bb-113">Create Ansible YAML files</span></span>](#create-ansible-yaml-files)
- [<span data-ttu-id="367bb-114">Déploiement</span><span class="sxs-lookup"><span data-stu-id="367bb-114">Deployment</span></span>](#deployment)
- [<span data-ttu-id="367bb-115">References</span><span class="sxs-lookup"><span data-stu-id="367bb-115">References</span></span>](#references)

## <a name="prerequisites-and-system-requirements"></a><span data-ttu-id="367bb-116">Conditions préalables et système requis</span><span class="sxs-lookup"><span data-stu-id="367bb-116">Prerequisites and system requirements</span></span>

<span data-ttu-id="367bb-117">Avant de commencer, consultez la page principale de [Defender for Endpoint sur Linux](microsoft-defender-endpoint-linux.md) pour obtenir une description des conditions préalables et de la requise pour la version logicielle actuelle.</span><span class="sxs-lookup"><span data-stu-id="367bb-117">Before you get started, see [the main Defender for Endpoint on Linux page](microsoft-defender-endpoint-linux.md) for a description of prerequisites and system requirements for the current software version.</span></span>

<span data-ttu-id="367bb-118">En outre, pour le déploiement Ansible, vous devez être familiarisé avec les tâches d'administration Ansible, configurer Ansible et savoir déployer des playbooks et des tâches.</span><span class="sxs-lookup"><span data-stu-id="367bb-118">In addition, for Ansible deployment, you need to be familiar with Ansible administration tasks, have Ansible configured, and know how to deploy playbooks and tasks.</span></span> <span data-ttu-id="367bb-119">Ansible dispose de nombreuses façons d'effectuer la même tâche.</span><span class="sxs-lookup"><span data-stu-id="367bb-119">Ansible has many ways to complete the same task.</span></span> <span data-ttu-id="367bb-120">Ces instructions supposent la disponibilité des modules Ansible pris en charge, tels que *apt* et *unarchive* pour vous aider à déployer le package.</span><span class="sxs-lookup"><span data-stu-id="367bb-120">These instructions assume availability of supported Ansible modules, such as *apt* and *unarchive* to help deploy the package.</span></span> <span data-ttu-id="367bb-121">Votre organisation peut utiliser un flux de travail différent.</span><span class="sxs-lookup"><span data-stu-id="367bb-121">Your organization might use a different workflow.</span></span> <span data-ttu-id="367bb-122">Pour plus d'informations, voir la [documentation Ansible.](https://docs.ansible.com/)</span><span class="sxs-lookup"><span data-stu-id="367bb-122">Refer to the [Ansible documentation](https://docs.ansible.com/) for details.</span></span>

- <span data-ttu-id="367bb-123">Ansible doit être installé sur au moins un ordinateur (nous l'appeller l'ordinateur principal).</span><span class="sxs-lookup"><span data-stu-id="367bb-123">Ansible needs to be installed on at least one computer (we will call it the primary computer).</span></span>
- <span data-ttu-id="367bb-124">SSH doit être configuré pour un compte d'administrateur entre l'ordinateur principal et tous les clients, et il est recommandé d'utiliser l'authentification à clé publique.</span><span class="sxs-lookup"><span data-stu-id="367bb-124">SSH must be configured for an administrator account between the primary computer and all clients, and it is recommended be configured with public key authentication.</span></span>
- <span data-ttu-id="367bb-125">Les logiciels suivants doivent être installés sur tous les clients :</span><span class="sxs-lookup"><span data-stu-id="367bb-125">The following software must be installed on all clients:</span></span>
  - <span data-ttu-id="367bb-126">sous-président</span><span class="sxs-lookup"><span data-stu-id="367bb-126">curl</span></span>
  - <span data-ttu-id="367bb-127">python-apt</span><span class="sxs-lookup"><span data-stu-id="367bb-127">python-apt</span></span>

- <span data-ttu-id="367bb-128">Tous les hôtes doivent être répertoriés au format suivant dans `/etc/ansible/hosts` le fichier ou dans le fichier approprié :</span><span class="sxs-lookup"><span data-stu-id="367bb-128">All hosts must be listed in the following format in the `/etc/ansible/hosts` or relevant file:</span></span>

    ```bash
    [servers]
    host1 ansible_ssh_host=10.171.134.39
    host2 ansible_ssh_host=51.143.50.51
    ```

- <span data-ttu-id="367bb-129">Test ping :</span><span class="sxs-lookup"><span data-stu-id="367bb-129">Ping test:</span></span>

    ```bash
    ansible -m ping all
    ```

## <a name="download-the-onboarding-package"></a><span data-ttu-id="367bb-130">Télécharger le package d'intégration</span><span class="sxs-lookup"><span data-stu-id="367bb-130">Download the onboarding package</span></span>

<span data-ttu-id="367bb-131">Téléchargez le package d'intégration à partir du Centre de sécurité Microsoft Defender :</span><span class="sxs-lookup"><span data-stu-id="367bb-131">Download the onboarding package from Microsoft Defender Security Center:</span></span>

1. <span data-ttu-id="367bb-132">Dans le Centre de sécurité Microsoft Defender, go to **Settings > Device Management > Onboarding**.</span><span class="sxs-lookup"><span data-stu-id="367bb-132">In Microsoft Defender Security Center, go to **Settings > Device Management > Onboarding**.</span></span>
2. <span data-ttu-id="367bb-133">Dans le premier menu déroulant, sélectionnez **Linux Server comme** système d'exploitation.</span><span class="sxs-lookup"><span data-stu-id="367bb-133">In the first drop-down menu, select **Linux Server** as the operating system.</span></span> <span data-ttu-id="367bb-134">Dans le deuxième menu déroulant, sélectionnez votre outil de gestion de **configuration Linux préféré** comme méthode de déploiement.</span><span class="sxs-lookup"><span data-stu-id="367bb-134">In the second drop-down menu, select **Your preferred Linux configuration management tool** as the deployment method.</span></span>
3. <span data-ttu-id="367bb-135">Sélectionnez **Télécharger le package d'intégration.**</span><span class="sxs-lookup"><span data-stu-id="367bb-135">Select **Download onboarding package**.</span></span> <span data-ttu-id="367bb-136">Enregistrez le fichier sous WindowsDefenderATPOnboardingPackage.zip.</span><span class="sxs-lookup"><span data-stu-id="367bb-136">Save the file as WindowsDefenderATPOnboardingPackage.zip.</span></span>

    ![Capture d'écran du Centre de sécurité Microsoft Defender](images/atp-portal-onboarding-linux-2.png)

4. <span data-ttu-id="367bb-138">À partir d'une invite de commandes, vérifiez que vous avez le fichier.</span><span class="sxs-lookup"><span data-stu-id="367bb-138">From a command prompt, verify that you have the file.</span></span> <span data-ttu-id="367bb-139">Extrayons le contenu de l'archive :</span><span class="sxs-lookup"><span data-stu-id="367bb-139">Extract the contents of the archive:</span></span>

    ```bash
    ls -l
    ```
    ```Output
    total 8
    -rw-r--r-- 1 test  staff  4984 Feb 18 11:22 WindowsDefenderATPOnboardingPackage.zip
    ```
    ```bash
    unzip WindowsDefenderATPOnboardingPackage.zip
    ```
    ```Output
    Archive:  WindowsDefenderATPOnboardingPackage.zip
    inflating: mdatp_onboard.json
    ```

## <a name="create-ansible-yaml-files"></a><span data-ttu-id="367bb-140">Créer des fichiers YAML ansibles</span><span class="sxs-lookup"><span data-stu-id="367bb-140">Create Ansible YAML files</span></span>

<span data-ttu-id="367bb-141">Créez une sous-tâche ou des fichiers de rôle qui contribuent à un manuel ou une tâche.</span><span class="sxs-lookup"><span data-stu-id="367bb-141">Create a subtask or role files that contribute to an playbook or task.</span></span>

- <span data-ttu-id="367bb-142">Créez la tâche d'intégration : `onboarding_setup.yml`</span><span class="sxs-lookup"><span data-stu-id="367bb-142">Create the onboarding task, `onboarding_setup.yml`:</span></span>

    ```bash
    - name: Create MDATP directories
      file:
        path: /etc/opt/microsoft/mdatp/
        recurse: true
        state: directory
        mode: 0755
        owner: root
        group: root

    - name: Register mdatp_onboard.json
      stat:
        path: /etc/opt/microsoft/mdatp/mdatp_onboard.json
      register: mdatp_onboard

    - name: Extract WindowsDefenderATPOnboardingPackage.zip into /etc/opt/microsoft/mdatp
      unarchive:
        src: WindowsDefenderATPOnboardingPackage.zip
        dest: /etc/opt/microsoft/mdatp
        mode: 0600
        owner: root
        group: root
      when: not mdatp_onboard.stat.exists
    ```

- <span data-ttu-id="367bb-143">Ajoutez le référentiel et la clé Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="367bb-143">Add the Defender for Endpoint repository and key.</span></span>

    <span data-ttu-id="367bb-144">Defender for Endpoint sur Linux peut être déployé à partir de l'un des canaux suivants (indiqués ci-dessous sous le nom *[canal]*) : *insiders-fast,* *insiders-slow* ou *prod*. Chacun de ces canaux correspond à un référentiel de logiciels Linux.</span><span class="sxs-lookup"><span data-stu-id="367bb-144">Defender for Endpoint on Linux can be deployed from one of the following channels (denoted below as *[channel]*): *insiders-fast*, *insiders-slow*, or *prod*. Each of these channels corresponds to a Linux software repository.</span></span>

    <span data-ttu-id="367bb-145">Le choix du canal détermine le type et la fréquence des mises à jour proposées à votre appareil.</span><span class="sxs-lookup"><span data-stu-id="367bb-145">The choice of the channel determines the type and frequency of updates that are offered to your device.</span></span> <span data-ttu-id="367bb-146">Les appareils *internes rapides* sont les premiers à recevoir des mises à jour et de nouvelles fonctionnalités, suivis ultérieurement par les *insiders-slow* et enfin par *prod*.</span><span class="sxs-lookup"><span data-stu-id="367bb-146">Devices in *insiders-fast* are the first ones to receive updates and new features, followed later by *insiders-slow* and lastly by *prod*.</span></span>

    <span data-ttu-id="367bb-147">Afin d'afficher un aperçu des nouvelles fonctionnalités et de fournir des commentaires préliminaires, il est recommandé de configurer certains appareils dans votre entreprise pour utiliser les *insiders-fast* ou *insider-slow*.</span><span class="sxs-lookup"><span data-stu-id="367bb-147">In order to preview new features and provide early feedback, it is recommended that you configure some devices in your enterprise to use either *insiders-fast* or *insiders-slow*.</span></span>

    > [!WARNING]
    > <span data-ttu-id="367bb-148">Le basculement du canal après l'installation initiale nécessite la réinstallation du produit.</span><span class="sxs-lookup"><span data-stu-id="367bb-148">Switching the channel after the initial installation requires the product to be reinstalled.</span></span> <span data-ttu-id="367bb-149">Pour basculer le canal de produit : désinstallez le package existant, configurez de nouveau votre appareil pour utiliser le nouveau canal et suivez les étapes de ce document pour installer le package à partir du nouvel emplacement.</span><span class="sxs-lookup"><span data-stu-id="367bb-149">To switch the product channel: uninstall the existing package, re-configure your device to use the new channel, and follow the steps in this document to install the package from the new location.</span></span>

    <span data-ttu-id="367bb-150">Notez votre distribution et version et identifiez l'entrée la plus proche sous `https://packages.microsoft.com/config/` .</span><span class="sxs-lookup"><span data-stu-id="367bb-150">Note your distribution and version and identify the closest entry for it under `https://packages.microsoft.com/config/`.</span></span>

    <span data-ttu-id="367bb-151">Dans les commandes suivantes, *remplacez [distro]* et *[version]* par les informations que vous avez identifiées.</span><span class="sxs-lookup"><span data-stu-id="367bb-151">In the following commands, replace *[distro]* and *[version]* with the information you've identified.</span></span>

    > [!NOTE]
    > <span data-ttu-id="367bb-152">Dans le cas d'Oracle Linux, *remplacez [distro]* par « rhel ».</span><span class="sxs-lookup"><span data-stu-id="367bb-152">In case of Oracle Linux, replace *[distro]* with “rhel”.</span></span>

  ```bash
  - name: Add Microsoft APT key
    apt_key:
      keyserver: https://packages.microsoft.com/
      id: BC528686B50D79E339D3721CEB3E94ADBE1229CF
    when: ansible_os_family == "Debian"

  - name: Add Microsoft apt repository for MDATP
    apt_repository:
      repo: deb [arch=arm64,armhf,amd64] https://packages.microsoft.com/[distro]/[version]/prod [channel] main
      update_cache: yes
      state: present
      filename: microsoft-[channel].list
    when: ansible_os_family == "Debian"

  - name: Add Microsoft DNF/YUM key
    rpm_key:
      state: present
      key: https://packages.microsoft.com/keys/microsoft.asc
    when: ansible_os_family == "RedHat"

  - name: Add  Microsoft yum repository for MDATP
    yum_repository:
      name: packages-microsoft-com-prod-[channel]
      description: Microsoft Defender for Endpoint
      file: microsoft-[channel]
      baseurl: https://packages.microsoft.com/[distro]/[version]/[channel]/
      gpgcheck: yes
      enabled: Yes
    when: ansible_os_family == "RedHat"
  ```

- <span data-ttu-id="367bb-153">Créez les fichiers YAML d'installation et de désinstallation Ansible.</span><span class="sxs-lookup"><span data-stu-id="367bb-153">Create the Ansible install and uninstall YAML files.</span></span>

    - <span data-ttu-id="367bb-154">Pour les distributions basées sur apt, utilisez le fichier YAML suivant :</span><span class="sxs-lookup"><span data-stu-id="367bb-154">For apt-based distributions use the following YAML file:</span></span>

        ```bash
        cat install_mdatp.yml
        ```
        ```Output
        - hosts: servers
          tasks:
            - include: ../roles/onboarding_setup.yml
            - include: ../roles/add_apt_repo.yml
            - name: Install MDATP
              apt:
                name: mdatp
                state: latest
                update_cache: yes
        ```

        ```bash
        cat uninstall_mdatp.yml
        ```
        ```Output
        - hosts: servers
          tasks:
            - name: Uninstall MDATP
              apt:
                name: mdatp
                state: absent
        ```

    - <span data-ttu-id="367bb-155">Pour les distributions basées sur dnf, utilisez le fichier YAML suivant :</span><span class="sxs-lookup"><span data-stu-id="367bb-155">For dnf-based distributions use the following YAML file:</span></span>

        ```bash
        cat install_mdatp_dnf.yml
        ```
        ```Output
        - hosts: servers
          tasks:
            - include: ../roles/onboarding_setup.yml
            - include: ../roles/add_yum_repo.yml
            - name: Install MDATP
              dnf:
                name: mdatp
                state: latest
                enablerepo: packages-microsoft-com-prod-[channel]
        ```

        ```bash
        cat uninstall_mdatp_dnf.yml
        ```
        ```Output
        - hosts: servers
          tasks:
            - name: Uninstall MDATP
              dnf:
                name: mdatp
                state: absent
        ```

## <a name="deployment"></a><span data-ttu-id="367bb-156">Déploiement</span><span class="sxs-lookup"><span data-stu-id="367bb-156">Deployment</span></span>

<span data-ttu-id="367bb-157">Exécutez maintenant les fichiers de tâches sous `/etc/ansible/playbooks/` ou dans le répertoire approprié.</span><span class="sxs-lookup"><span data-stu-id="367bb-157">Now run the tasks files under `/etc/ansible/playbooks/` or relevant directory.</span></span>

- <span data-ttu-id="367bb-158">Installation :</span><span class="sxs-lookup"><span data-stu-id="367bb-158">Installation:</span></span>

    ```bash
    ansible-playbook /etc/ansible/playbooks/install_mdatp.yml -i /etc/ansible/hosts
    ```

> [!IMPORTANT]
> <span data-ttu-id="367bb-159">Lorsque le produit démarre pour la première fois, il télécharge les dernières définitions de logiciel anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="367bb-159">When the product starts for the first time, it downloads the latest antimalware definitions.</span></span> <span data-ttu-id="367bb-160">Selon votre connexion Internet, cela peut prendre jusqu'à quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="367bb-160">Depending on your Internet connection, this can take up to a few minutes.</span></span>

- <span data-ttu-id="367bb-161">Validation/configuration :</span><span class="sxs-lookup"><span data-stu-id="367bb-161">Validation/configuration:</span></span>

    ```bash
    ansible -m shell -a 'mdatp connectivity test' all
    ```
    ```bash
    ansible -m shell -a 'mdatp health' all
    ```

- <span data-ttu-id="367bb-162">Désinstallation :</span><span class="sxs-lookup"><span data-stu-id="367bb-162">Uninstallation:</span></span>

    ```bash
    ansible-playbook /etc/ansible/playbooks/uninstall_mdatp.yml -i /etc/ansible/hosts
    ```

## <a name="log-installation-issues"></a><span data-ttu-id="367bb-163">Journal des problèmes d'installation</span><span class="sxs-lookup"><span data-stu-id="367bb-163">Log installation issues</span></span>

<span data-ttu-id="367bb-164">Pour [plus d'informations](linux-resources.md#log-installation-issues) sur la recherche du journal généré automatiquement par le programme d'installation en cas d'erreur, voir problèmes d'installation des journaux.</span><span class="sxs-lookup"><span data-stu-id="367bb-164">See [Log installation issues](linux-resources.md#log-installation-issues) for more information on how to find the automatically generated log that is created by the installer when an error occurs.</span></span>

## <a name="operating-system-upgrades"></a><span data-ttu-id="367bb-165">Mises à niveau du système d'exploitation</span><span class="sxs-lookup"><span data-stu-id="367bb-165">Operating system upgrades</span></span>

<span data-ttu-id="367bb-166">Lors de la mise à niveau de votre système d'exploitation vers une nouvelle version majeure, vous devez d'abord désinstaller Defender pour Endpoint sur Linux, installer la mise à niveau, puis reconfigurer Defender pour Endpoint sur Linux sur votre appareil.</span><span class="sxs-lookup"><span data-stu-id="367bb-166">When upgrading your operating system to a new major version, you must first uninstall Defender for Endpoint on Linux, install the upgrade, and finally reconfigure Defender for Endpoint on Linux on your device.</span></span>

## <a name="references"></a><span data-ttu-id="367bb-167">Références</span><span class="sxs-lookup"><span data-stu-id="367bb-167">References</span></span>

- [<span data-ttu-id="367bb-168">Ajouter ou supprimer des référentiels YUM</span><span class="sxs-lookup"><span data-stu-id="367bb-168">Add or remove YUM repositories</span></span>](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/yum_repository_module.html)

- [<span data-ttu-id="367bb-169">Gérer les packages avec le gestionnaire de package dnf</span><span class="sxs-lookup"><span data-stu-id="367bb-169">Manage packages with the dnf package manager</span></span>](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/dnf_module.html)

- [<span data-ttu-id="367bb-170">Ajouter et supprimer des référentiels APT</span><span class="sxs-lookup"><span data-stu-id="367bb-170">Add and remove APT repositories</span></span>](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/apt_repository_module.html)

- [<span data-ttu-id="367bb-171">Gérer les packages apt</span><span class="sxs-lookup"><span data-stu-id="367bb-171">Manage apt-packages</span></span>](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/apt_module.html)
