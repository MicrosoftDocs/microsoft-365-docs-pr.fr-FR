---
title: Déployer Microsoft Defender ATP pour Linux avec Sons
ms.reviewer: ''
description: Décrit comment déployer Microsoft Defender ATP pour Linux à l'aide de L'Atelier.
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
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 562433ee52b2e39716e933c67c706f030195bd2f
ms.sourcegitcommit: 3fe7eb32c8d6e01e190b2b782827fbadd73a18e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "51688416"
---
# <a name="deploy-microsoft-defender-for-endpoint-on-linux-with-puppet"></a><span data-ttu-id="c686d-104">Déployer Microsoft Defender pour le point de terminaison sur Linux avec l'ment</span><span class="sxs-lookup"><span data-stu-id="c686d-104">Deploy Microsoft Defender for Endpoint on Linux with Puppet</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="c686d-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="c686d-105">**Applies to:**</span></span>
- [<span data-ttu-id="c686d-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="c686d-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="c686d-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="c686d-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="c686d-108">Vous souhaitez faire l'expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="c686d-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="c686d-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="c686d-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigateip-abovefoldlink)

<span data-ttu-id="c686d-110">Cet article explique comment déployer Defender pour endpoint pour Linux à l'aide de Latra.</span><span class="sxs-lookup"><span data-stu-id="c686d-110">This article describes how to deploy Defender for Endpoint for Linux using Puppet.</span></span> <span data-ttu-id="c686d-111">Un déploiement réussi nécessite l'exécution de toutes les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="c686d-111">A successful deployment requires the completion of all of the following tasks:</span></span>

- [<span data-ttu-id="c686d-112">Télécharger le package d'intégration</span><span class="sxs-lookup"><span data-stu-id="c686d-112">Download the onboarding package</span></span>](#download-the-onboarding-package)
- [<span data-ttu-id="c686d-113">Créer un manifeste d'atelier</span><span class="sxs-lookup"><span data-stu-id="c686d-113">Create Puppet manifest</span></span>](#create-a-puppet-manifest)
- [<span data-ttu-id="c686d-114">Déploiement</span><span class="sxs-lookup"><span data-stu-id="c686d-114">Deployment</span></span>](#deployment)
- [<span data-ttu-id="c686d-115">Vérifier l'état de l'intégration</span><span class="sxs-lookup"><span data-stu-id="c686d-115">Check onboarding status</span></span>](#check-onboarding-status)

## <a name="prerequisites-and-system-requirements"></a><span data-ttu-id="c686d-116">Conditions préalables et système requis</span><span class="sxs-lookup"><span data-stu-id="c686d-116">Prerequisites and system requirements</span></span>

 <span data-ttu-id="c686d-117">Pour obtenir une description des conditions préalables et de la condition système requise pour la version logicielle actuelle, consultez la page principale de [Defender for Endpoint for Linux.](microsoft-defender-endpoint-linux.md)</span><span class="sxs-lookup"><span data-stu-id="c686d-117">For a description of prerequisites and system requirements for the current software version, see [the main Defender for Endpoint for Linux page](microsoft-defender-endpoint-linux.md).</span></span>

<span data-ttu-id="c686d-118">En outre, pour le déploiement de Manière générale, vous devez être familiarisé avec les tâches d'administration de la charge de travail, configurer Configure et savoir comment déployer des packages.</span><span class="sxs-lookup"><span data-stu-id="c686d-118">In addition, for Puppet deployment, you need to be familiar with Puppet administration tasks, have Puppet configured, and know how to deploy packages.</span></span> <span data-ttu-id="c686d-119">Il existe de nombreuses façons d'effectuer la même tâche.</span><span class="sxs-lookup"><span data-stu-id="c686d-119">Puppet has many ways to complete the same task.</span></span> <span data-ttu-id="c686d-120">Ces instructions supposent la disponibilité des modules De jeu pris en charge, par exemple *pour* vous aider à déployer le package.</span><span class="sxs-lookup"><span data-stu-id="c686d-120">These instructions assume availability of supported Puppet modules, such as *apt* to help deploy the package.</span></span> <span data-ttu-id="c686d-121">Votre organisation peut utiliser un flux de travail différent.</span><span class="sxs-lookup"><span data-stu-id="c686d-121">Your organization might use a different workflow.</span></span> <span data-ttu-id="c686d-122">Pour plus d'informations, [reportez-vous](https://puppet.com/docs) à la documentation de Documentation.</span><span class="sxs-lookup"><span data-stu-id="c686d-122">Refer to the [Puppet documentation](https://puppet.com/docs) for details.</span></span>

## <a name="download-the-onboarding-package"></a><span data-ttu-id="c686d-123">Télécharger le package d'intégration</span><span class="sxs-lookup"><span data-stu-id="c686d-123">Download the onboarding package</span></span>

<span data-ttu-id="c686d-124">Téléchargez le package d'intégration à partir du Centre de sécurité Microsoft Defender :</span><span class="sxs-lookup"><span data-stu-id="c686d-124">Download the onboarding package from Microsoft Defender Security Center:</span></span>

1. <span data-ttu-id="c686d-125">Dans le Centre de sécurité Microsoft Defender, go to **Settings > Device Management > Onboarding**.</span><span class="sxs-lookup"><span data-stu-id="c686d-125">In Microsoft Defender Security Center, go to **Settings > Device Management > Onboarding**.</span></span>
2. <span data-ttu-id="c686d-126">Dans le premier menu déroulant, sélectionnez **Linux Server comme** système d'exploitation.</span><span class="sxs-lookup"><span data-stu-id="c686d-126">In the first drop-down menu, select **Linux Server** as the operating system.</span></span> <span data-ttu-id="c686d-127">Dans le deuxième menu déroulant, sélectionnez votre outil de gestion de **configuration Linux préféré** comme méthode de déploiement.</span><span class="sxs-lookup"><span data-stu-id="c686d-127">In the second drop-down menu, select **Your preferred Linux configuration management tool** as the deployment method.</span></span>
3. <span data-ttu-id="c686d-128">Sélectionnez **Télécharger le package d'intégration.**</span><span class="sxs-lookup"><span data-stu-id="c686d-128">Select **Download onboarding package**.</span></span> <span data-ttu-id="c686d-129">Enregistrez le fichier sous WindowsDefenderATPOnboardingPackage.zip.</span><span class="sxs-lookup"><span data-stu-id="c686d-129">Save the file as WindowsDefenderATPOnboardingPackage.zip.</span></span>

    ![Capture d'écran du Centre de sécurité Microsoft Defender](images/atp-portal-onboarding-linux-2.png)

4. <span data-ttu-id="c686d-131">À partir d'une invite de commandes, vérifiez que vous avez le fichier.</span><span class="sxs-lookup"><span data-stu-id="c686d-131">From a command prompt, verify that you have the file.</span></span> 

    ```bash
    ls -l
    ```
    ```Output
    total 8
    -rw-r--r-- 1 test  staff  4984 Feb 18 11:22 WindowsDefenderATPOnboardingPackage.zip
    ```
5. <span data-ttu-id="c686d-132">Extrayons le contenu de l'archive.</span><span class="sxs-lookup"><span data-stu-id="c686d-132">Extract the contents of the archive.</span></span>
    ```bash
    unzip WindowsDefenderATPOnboardingPackage.zip
    ```
    ```Output
    Archive:  WindowsDefenderATPOnboardingPackage.zip
    inflating: mdatp_onboard.json
    ```

## <a name="create-a-puppet-manifest"></a><span data-ttu-id="c686d-133">Créer un manifeste de jeu</span><span class="sxs-lookup"><span data-stu-id="c686d-133">Create a Puppet manifest</span></span>

<span data-ttu-id="c686d-134">Vous devez créer un manifeste Pour déployer Defender pour Point de terminaison pour Linux sur des appareils gérés par un serveur Deas.</span><span class="sxs-lookup"><span data-stu-id="c686d-134">You need to create a Puppet manifest for deploying Defender for Endpoint for Linux to devices managed by a Puppet server.</span></span> <span data-ttu-id="c686d-135">Cet exemple utilise les modules *apt* et *yumrepo* disponibles à partir delabs, et part du principe que les modules ont été installés sur votre serveur Dupont.</span><span class="sxs-lookup"><span data-stu-id="c686d-135">This example makes use of the *apt* and *yumrepo* modules available from puppetlabs, and assumes that the modules have been installed on your Puppet server.</span></span>

<span data-ttu-id="c686d-136">Créez les dossiers *install_mdatp/fichiers* et *install_mdatp/manifestes* sous le dossier modules de votre installation de Latre.</span><span class="sxs-lookup"><span data-stu-id="c686d-136">Create the folders *install_mdatp/files* and *install_mdatp/manifests* under the modules folder of your Puppet installation.</span></span> <span data-ttu-id="c686d-137">Ce dossier se trouve généralement dans */etc/spamlabs/code/environments/production/modules* sur votre serveur Der.</span><span class="sxs-lookup"><span data-stu-id="c686d-137">This folder is typically located in */etc/puppetlabs/code/environments/production/modules* on your Puppet server.</span></span> <span data-ttu-id="c686d-138">Copiez le mdatp_onboard.jssur le fichier créé ci-dessus dans *le dossier install_mdatp/fichiers.*</span><span class="sxs-lookup"><span data-stu-id="c686d-138">Copy the mdatp_onboard.json file created above to the *install_mdatp/files* folder.</span></span> <span data-ttu-id="c686d-139">Créer *un init.pp*</span><span class="sxs-lookup"><span data-stu-id="c686d-139">Create an *init.pp*</span></span> <span data-ttu-id="c686d-140">qui contient les instructions de déploiement :</span><span class="sxs-lookup"><span data-stu-id="c686d-140">file that contains the deployment instructions:</span></span>

```bash
pwd
```
```Output
/etc/puppetlabs/code/environments/production/modules
```

```bash
tree install_mdatp
```
```Output
install_mdatp
├── files
│   └── mdatp_onboard.json
└── manifests
    └── init.pp
```

### <a name="contents-of-install_mdatpmanifestsinitpp"></a><span data-ttu-id="c686d-141">Contenu de `install_mdatp/manifests/init.pp`</span><span class="sxs-lookup"><span data-stu-id="c686d-141">Contents of `install_mdatp/manifests/init.pp`</span></span>

<span data-ttu-id="c686d-142">Defender pour le point de terminaison pour Linux peut être déployé à partir de l'un des canaux suivants (indiqué ci-dessous sous le nom *[canal]*) : *insiders-fast,* *insiders-slow* ou *prod*. Chacun de ces canaux correspond à un référentiel de logiciels Linux.</span><span class="sxs-lookup"><span data-stu-id="c686d-142">Defender for Endpoint for Linux can be deployed from one of the following channels (denoted below as *[channel]*): *insiders-fast*, *insiders-slow*, or *prod*. Each of these channels corresponds to a Linux software repository.</span></span>

<span data-ttu-id="c686d-143">Le choix du canal détermine le type et la fréquence des mises à jour proposées à votre appareil.</span><span class="sxs-lookup"><span data-stu-id="c686d-143">The choice of the channel determines the type and frequency of updates that are offered to your device.</span></span> <span data-ttu-id="c686d-144">Les appareils *internes rapides* sont les premiers à recevoir des mises à jour et de nouvelles fonctionnalités, suivis ultérieurement par les *insiders-slow* et enfin par *prod*.</span><span class="sxs-lookup"><span data-stu-id="c686d-144">Devices in *insiders-fast* are the first ones to receive updates and new features, followed later by *insiders-slow* and lastly by *prod*.</span></span>

<span data-ttu-id="c686d-145">Afin d'afficher un aperçu des nouvelles fonctionnalités et de fournir des commentaires préliminaires, il est recommandé de configurer certains appareils dans votre entreprise pour utiliser les *insiders-fast* ou *insider-slow*.</span><span class="sxs-lookup"><span data-stu-id="c686d-145">In order to preview new features and provide early feedback, it is recommended that you configure some devices in your enterprise to use either *insiders-fast* or *insiders-slow*.</span></span>

> [!WARNING]
> <span data-ttu-id="c686d-146">Le basculement du canal après l'installation initiale nécessite la réinstallation du produit.</span><span class="sxs-lookup"><span data-stu-id="c686d-146">Switching the channel after the initial installation requires the product to be reinstalled.</span></span> <span data-ttu-id="c686d-147">Pour basculer le canal de produit : désinstallez le package existant, configurez de nouveau votre appareil pour utiliser le nouveau canal et suivez les étapes de ce document pour installer le package à partir du nouvel emplacement.</span><span class="sxs-lookup"><span data-stu-id="c686d-147">To switch the product channel: uninstall the existing package, re-configure your device to use the new channel, and follow the steps in this document to install the package from the new location.</span></span>

<span data-ttu-id="c686d-148">Notez votre distribution et version et identifiez l'entrée la plus proche sous `https://packages.microsoft.com/config/` .</span><span class="sxs-lookup"><span data-stu-id="c686d-148">Note your distribution and version and identify the closest entry for it under `https://packages.microsoft.com/config/`.</span></span>

<span data-ttu-id="c686d-149">Dans les commandes ci-dessous, *remplacez [distro]* et *[version]* par les informations que vous avez identifiées :</span><span class="sxs-lookup"><span data-stu-id="c686d-149">In the below commands, replace *[distro]* and *[version]* with the information you've identified:</span></span>

> [!NOTE]
> <span data-ttu-id="c686d-150">Dans le cas de RedHat, Oracle EL et CentOS 8, *remplacez [distro]* par « rhel ».</span><span class="sxs-lookup"><span data-stu-id="c686d-150">In case of RedHat, Oracle EL, and CentOS 8, replace *[distro]* with 'rhel'.</span></span>

```puppet
# Puppet manifest to install Microsoft Defender ATP.
# @param channel The release channel based on your environment, insider-fast or prod.
# @param distro The Linux distribution in lowercase. In case of RedHat, Oracle EL, and CentOS 8, the distro variable should be 'rhel'.
# @param version The Linux distribution release number, e.g. 7.4.

class install_mdatp (
$channel = 'insiders-fast',
$distro = undef,
$version = undef
){
    case $::osfamily {
        'Debian' : {
            apt::source { 'microsoftpackages' :
                location => "https://packages.microsoft.com/${distro}/${version}/prod",
                release  => $channel,
                repos    => 'main',
                key      => {
                    'id'     => 'BC528686B50D79E339D3721CEB3E94ADBE1229CF',
                    'server' => 'keyserver.ubuntu.com',
                },
            }
        }
        'RedHat' : {
            yumrepo { 'microsoftpackages' :
                baseurl  => "https://packages.microsoft.com/${distro}/${version}/${channel}",
                descr    => "packages-microsoft-com-prod-${channel}",
                enabled  => 1,
                gpgcheck => 1,
                gpgkey   => 'https://packages.microsoft.com/keys/microsoft.asc'
            }
        }
        default : { fail("${::osfamily} is currently not supported.") }
    }

    case $::osfamily {
        /(Debian|RedHat)/: {
            file { ['/etc/opt', '/etc/opt/microsoft', '/etc/opt/microsoft/mdatp']:
                ensure => directory,
                owner  => root,
                group  => root,
                mode   => '0755'
            }

            file { '/etc/opt/microsoft/mdatp/mdatp_onboard.json':
                source  => 'puppet:///modules/install_mdatp/mdatp_onboard.json',
                owner   => root,
                group   => root,
                mode    => '0600',
                require => File['/etc/opt/microsoft/mdatp']
            }

            package { 'mdatp':
                ensure  => 'installed',
                require => File['/etc/opt/microsoft/mdatp/mdatp_onboard.json']
            }
        }
        default : { fail("${::osfamily} is currently not supported.") }
    }
}
```

## <a name="deployment"></a><span data-ttu-id="c686d-151">Déploiement</span><span class="sxs-lookup"><span data-stu-id="c686d-151">Deployment</span></span>

<span data-ttu-id="c686d-152">Inclure le manifeste ci-dessus dans votre site.pp</span><span class="sxs-lookup"><span data-stu-id="c686d-152">Include the above manifest in your site.pp</span></span> <span data-ttu-id="c686d-153">fichier :</span><span class="sxs-lookup"><span data-stu-id="c686d-153">file:</span></span>

```bash
cat /etc/puppetlabs/code/environments/production/manifests/site.pp
```
```Output
node "default" {
    include install_mdatp
}
```

<span data-ttu-id="c686d-154">Les appareils d'agent inscrits sondent périodiquement le serveur de contrôle d'accès et installent de nouveaux profils et stratégies de configuration dès qu'ils sont détectés.</span><span class="sxs-lookup"><span data-stu-id="c686d-154">Enrolled agent devices periodically poll the Puppet Server and install new configuration profiles and policies as soon as they are detected.</span></span>

## <a name="monitor-puppet-deployment"></a><span data-ttu-id="c686d-155">Surveiller le déploiement de l'écran de surveillance</span><span class="sxs-lookup"><span data-stu-id="c686d-155">Monitor Puppet deployment</span></span>

<span data-ttu-id="c686d-156">Sur l'appareil de l'agent, vous pouvez également vérifier l'état d'intégration en exécutant :</span><span class="sxs-lookup"><span data-stu-id="c686d-156">On the agent device, you can also check the onboarding status by running:</span></span>

```bash
mdatp health
```
```Output
...
licensed                                : true
org_id                                  : "[your organization identifier]"
...
```

- <span data-ttu-id="c686d-157">**licence :** cela confirme que l'appareil est lié à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c686d-157">**licensed**: This confirms that the device is tied to your organization.</span></span>

- <span data-ttu-id="c686d-158">**orgId :** il s'agit de votre identificateur d'organisation Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="c686d-158">**orgId**: This is your Defender for Endpoint organization identifier.</span></span>

## <a name="check-onboarding-status"></a><span data-ttu-id="c686d-159">Vérifier l'état de l'intégration</span><span class="sxs-lookup"><span data-stu-id="c686d-159">Check onboarding status</span></span>

<span data-ttu-id="c686d-160">Vous pouvez vérifier que les appareils ont été correctement intégrés en créant un script.</span><span class="sxs-lookup"><span data-stu-id="c686d-160">You can check that devices have been correctly onboarded by creating a script.</span></span> <span data-ttu-id="c686d-161">Par exemple, le script suivant vérifie l'état d'intégration des appareils inscrits :</span><span class="sxs-lookup"><span data-stu-id="c686d-161">For example, the following script checks enrolled devices for onboarding status:</span></span>

```bash
mdatp health --field healthy
```

<span data-ttu-id="c686d-162">La commande ci-dessus imprime `1` si le produit est intégré et fonctionne comme prévu.</span><span class="sxs-lookup"><span data-stu-id="c686d-162">The above command prints `1` if the product is onboarded and functioning as expected.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c686d-163">Lorsque le produit démarre pour la première fois, il télécharge les dernières définitions de logiciel anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="c686d-163">When the product starts for the first time, it downloads the latest antimalware definitions.</span></span> <span data-ttu-id="c686d-164">Selon votre connexion Internet, cela peut prendre jusqu'à quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="c686d-164">Depending on your Internet connection, this can take up to a few minutes.</span></span> <span data-ttu-id="c686d-165">Pendant ce temps, la commande ci-dessus renvoie une valeur de `0` .</span><span class="sxs-lookup"><span data-stu-id="c686d-165">During this time the above command returns a value of `0`.</span></span>

<span data-ttu-id="c686d-166">Si le produit n'est pas sain, le code de sortie (qui peut être `echo $?` vérifié) indique le problème :</span><span class="sxs-lookup"><span data-stu-id="c686d-166">If the product is not healthy, the exit code (which can be checked through `echo $?`) indicates the problem:</span></span>

- <span data-ttu-id="c686d-167">1 si l'appareil n'est pas encore intégré.</span><span class="sxs-lookup"><span data-stu-id="c686d-167">1 if the device isn't onboarded yet.</span></span>
- <span data-ttu-id="c686d-168">3 si la connexion au daemon ne peut pas être établie.</span><span class="sxs-lookup"><span data-stu-id="c686d-168">3 if the connection to the daemon cannot be established.</span></span>

## <a name="log-installation-issues"></a><span data-ttu-id="c686d-169">Journaux des problèmes d'installation</span><span class="sxs-lookup"><span data-stu-id="c686d-169">Log installation issues</span></span>

 <span data-ttu-id="c686d-170">Pour plus d'informations sur la recherche du journal généré automatiquement créé par le programme d'installation lorsqu'une erreur se produit, voir Problèmes [d'installation du journal.](linux-resources.md#log-installation-issues)</span><span class="sxs-lookup"><span data-stu-id="c686d-170">For more information on how to find the automatically generated log that is created by the installer when an error occurs, see [Log installation issues](linux-resources.md#log-installation-issues).</span></span>

## <a name="operating-system-upgrades"></a><span data-ttu-id="c686d-171">Mises à niveau du système d'exploitation</span><span class="sxs-lookup"><span data-stu-id="c686d-171">Operating system upgrades</span></span>

<span data-ttu-id="c686d-172">Lors de la mise à niveau de votre système d'exploitation vers une nouvelle version majeure, vous devez d'abord désinstaller Defender pour Endpoint pour Linux, installer la mise à niveau, puis reconfigurer Defender pour Endpoint pour Linux sur votre appareil.</span><span class="sxs-lookup"><span data-stu-id="c686d-172">When upgrading your operating system to a new major version, you must first uninstall Defender for Endpoint for Linux, install the upgrade, and finally reconfigure Defender for Endpoint for Linux on your device.</span></span>

## <a name="uninstallation"></a><span data-ttu-id="c686d-173">Désinstallation</span><span class="sxs-lookup"><span data-stu-id="c686d-173">Uninstallation</span></span>

<span data-ttu-id="c686d-174">Créer un module *remove_mdatp* similaire à *install_mdatp* avec le contenu suivant *dans init.pp*</span><span class="sxs-lookup"><span data-stu-id="c686d-174">Create a module *remove_mdatp* similar to *install_mdatp* with the following contents in *init.pp*</span></span> <span data-ttu-id="c686d-175">fichier :</span><span class="sxs-lookup"><span data-stu-id="c686d-175">file:</span></span>

```bash
class remove_mdatp {
    package { 'mdatp':
        ensure => 'purged',
    }
}
```
