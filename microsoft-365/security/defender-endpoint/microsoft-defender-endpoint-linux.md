---
title: Microsoft Defender pour point de terminaison Linux
ms.reviewer: ''
description: Décrit comment installer et utiliser Microsoft Defender pour endpoint sur Linux.
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
- m365initiative-defender-endpoint
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 2242d195f4a4ea4b8f0c345d82fa0ad1f947bfa2
ms.sourcegitcommit: e8f5d88f0fe54620308d3bec05263568f9da2931
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2021
ms.locfileid: "52730761"
---
# <a name="microsoft-defender-for-endpoint-on-linux"></a><span data-ttu-id="5271f-104">Microsoft Defender pour point de terminaison Linux</span><span class="sxs-lookup"><span data-stu-id="5271f-104">Microsoft Defender for Endpoint on Linux</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="5271f-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="5271f-105">**Applies to:**</span></span>
- [<span data-ttu-id="5271f-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="5271f-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="5271f-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="5271f-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="5271f-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="5271f-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="5271f-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="5271f-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="5271f-110">Cette rubrique décrit comment installer, configurer, mettre à jour et utiliser Microsoft Defender pour Endpoint sur Linux.</span><span class="sxs-lookup"><span data-stu-id="5271f-110">This topic describes how to install, configure, update, and use Microsoft Defender for Endpoint on Linux.</span></span>

> [!CAUTION]
> <span data-ttu-id="5271f-111">L’exécution d’autres produits de protection de point de terminaison tiers avec Microsoft Defender pour Endpoint sur Linux est susceptible de provoquer des problèmes de performances et des effets secondaires imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="5271f-111">Running other third-party endpoint protection products alongside Microsoft Defender for Endpoint on Linux is likely to lead to performance problems and unpredictable side effects.</span></span> <span data-ttu-id="5271f-112">Si la protection des points de terminaison non-Microsoft est une exigence absolue dans votre environnement, vous pouvez toujours tirer parti en toute sécurité de defender pour point de terminaison sur la fonctionnalité linux PEPT après avoir configuré la fonctionnalité antivirus pour qu’elle s’exécute en [mode](linux-preferences.md#enable--disable-passive-mode)passif.</span><span class="sxs-lookup"><span data-stu-id="5271f-112">If non-Microsoft endpoint protection is an absolute requirement in your environment, you can still safely take advantage of Defender for Endpoint on Linux EDR functionality after configuring the antivirus functionality to run in [Passive mode](linux-preferences.md#enable--disable-passive-mode).</span></span>

## <a name="how-to-install-microsoft-defender-for-endpoint-on-linux"></a><span data-ttu-id="5271f-113">Comment installer Microsoft Defender pour endpoint sur Linux</span><span class="sxs-lookup"><span data-stu-id="5271f-113">How to install Microsoft Defender for Endpoint on Linux</span></span>

### <a name="prerequisites"></a><span data-ttu-id="5271f-114">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="5271f-114">Prerequisites</span></span>

- <span data-ttu-id="5271f-115">Accès au portail Centre de sécurité Microsoft Defender web</span><span class="sxs-lookup"><span data-stu-id="5271f-115">Access to the Microsoft Defender Security Center portal</span></span>
- <span data-ttu-id="5271f-116">Distribution Linux à l’aide [du gestionnaire système](https://systemd.io/)</span><span class="sxs-lookup"><span data-stu-id="5271f-116">Linux distribution using the [systemd](https://systemd.io/) system manager</span></span>
- <span data-ttu-id="5271f-117">Expérience de niveau débutant dans les scripts Linux et BASH</span><span class="sxs-lookup"><span data-stu-id="5271f-117">Beginner-level experience in Linux and BASH scripting</span></span>
- <span data-ttu-id="5271f-118">Privilèges d’administration sur l’appareil (en cas de déploiement manuel)</span><span class="sxs-lookup"><span data-stu-id="5271f-118">Administrative privileges on the device (in case of manual deployment)</span></span>

> [!NOTE]
>  <span data-ttu-id="5271f-119">Microsoft Defender pour point de terminaison sur l’agent Linux est indépendant de [l’agent OMS.](/azure/azure-monitor/agents/agents-overview#log-analytics-agent)</span><span class="sxs-lookup"><span data-stu-id="5271f-119">Microsoft Defender for Endpoint on Linux agent is independent from [OMS agent](/azure/azure-monitor/agents/agents-overview#log-analytics-agent).</span></span> <span data-ttu-id="5271f-120">Microsoft Defender pour le point de terminaison s’appuie sur son propre pipeline de télémétrie indépendant.</span><span class="sxs-lookup"><span data-stu-id="5271f-120">Microsoft Defender for Endpoint relies on its own independent telemetry pipeline.</span></span>
> 
> <span data-ttu-id="5271f-121">Microsoft Defender pour point de terminaison sur Linux n’est pas encore intégré au Centre de sécurité Azure.</span><span class="sxs-lookup"><span data-stu-id="5271f-121">Microsoft Defender for Endpoint on Linux is not yet integrated into Azure Security Center.</span></span>



### <a name="installation-instructions"></a><span data-ttu-id="5271f-122">Instructions d’installation</span><span class="sxs-lookup"><span data-stu-id="5271f-122">Installation instructions</span></span>

<span data-ttu-id="5271f-123">Vous pouvez utiliser plusieurs méthodes et outils de déploiement pour installer et configurer Microsoft Defender pour Endpoint sur Linux.</span><span class="sxs-lookup"><span data-stu-id="5271f-123">There are several methods and deployment tools that you can use to install and configure Microsoft Defender for Endpoint on Linux.</span></span>

<span data-ttu-id="5271f-124">En règle générale, vous devez suivre les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="5271f-124">In general you need to take the following steps:</span></span>

- <span data-ttu-id="5271f-125">Assurez-vous que vous avez un abonnement Microsoft Defender pour points de terminaison et que vous avez accès au portail [Microsoft Defender pour points de terminaison.](microsoft-defender-security-center.md)</span><span class="sxs-lookup"><span data-stu-id="5271f-125">Ensure that you have a Microsoft Defender for Endpoint subscription, and that you have access to the [Microsoft Defender for Endpoint portal](microsoft-defender-security-center.md).</span></span>
- <span data-ttu-id="5271f-126">Déployez Microsoft Defender pour Endpoint sur Linux à l’aide de l’une des méthodes de déploiement suivantes :</span><span class="sxs-lookup"><span data-stu-id="5271f-126">Deploy Microsoft Defender for Endpoint on Linux using one of the following deployment methods:</span></span>
  - <span data-ttu-id="5271f-127">L’outil en ligne de commande :</span><span class="sxs-lookup"><span data-stu-id="5271f-127">The command-line tool:</span></span>
    - [<span data-ttu-id="5271f-128">Déploiement manuel</span><span class="sxs-lookup"><span data-stu-id="5271f-128">Manual deployment</span></span>](linux-install-manually.md)
  - <span data-ttu-id="5271f-129">Outils de gestion tiers :</span><span class="sxs-lookup"><span data-stu-id="5271f-129">Third-party management tools:</span></span>
    - [<span data-ttu-id="5271f-130">Déployer à l’aide de l’outil de gestion de la configuration de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="5271f-130">Deploy using Puppet configuration management tool</span></span>](linux-install-with-puppet.md)
    - [<span data-ttu-id="5271f-131">Déployer à l’aide de l’outil de gestion de la configuration Ansible</span><span class="sxs-lookup"><span data-stu-id="5271f-131">Deploy using Ansible configuration management tool</span></span>](linux-install-with-ansible.md)

<span data-ttu-id="5271f-132">Si vous avez des échecs d’installation, reportez-vous à Résolution des problèmes d’installation dans [Microsoft Defender pour Point de terminaison sur Linux.](linux-support-install.md)</span><span class="sxs-lookup"><span data-stu-id="5271f-132">If you experience any installation failures, refer to [Troubleshooting installation failures in Microsoft Defender for Endpoint on Linux](linux-support-install.md).</span></span>



### <a name="system-requirements"></a><span data-ttu-id="5271f-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5271f-133">System requirements</span></span>

- <span data-ttu-id="5271f-134">Distributions de serveurs Linux et versions x64 (AMD64/EM64T) prise en charge :</span><span class="sxs-lookup"><span data-stu-id="5271f-134">Supported Linux server distributions and x64 (AMD64/EM64T) versions:</span></span>

  - <span data-ttu-id="5271f-135">Red Hat Enterprise Linux 7.2 ou supérieur</span><span class="sxs-lookup"><span data-stu-id="5271f-135">Red Hat Enterprise Linux 7.2 or higher</span></span>
  - <span data-ttu-id="5271f-136">CentOS 7.2 ou supérieur</span><span class="sxs-lookup"><span data-stu-id="5271f-136">CentOS 7.2 or higher</span></span>
  - <span data-ttu-id="5271f-137">Ubuntu 16.04 LTS ou une LTS supérieure</span><span class="sxs-lookup"><span data-stu-id="5271f-137">Ubuntu 16.04 LTS or higher LTS</span></span>
  - <span data-ttu-id="5271f-138">Debian 9 ou supérieur</span><span class="sxs-lookup"><span data-stu-id="5271f-138">Debian 9 or higher</span></span>
  - <span data-ttu-id="5271f-139">SUSE Linux Enterprise Server 12 ou supérieur</span><span class="sxs-lookup"><span data-stu-id="5271f-139">SUSE Linux Enterprise Server 12 or higher</span></span>
  - <span data-ttu-id="5271f-140">Oracle Linux 7.2 ou supérieur</span><span class="sxs-lookup"><span data-stu-id="5271f-140">Oracle Linux 7.2 or higher</span></span>

    > [!NOTE]
    > <span data-ttu-id="5271f-141">Les distributions et les versions qui ne sont pas explicitement répertoriées ne sont pas pris en charge (même s’ils sont dérivés des distributions officiellement pris en charge).</span><span class="sxs-lookup"><span data-stu-id="5271f-141">Distributions and version that are not explicitly listed are unsupported (even if they are derived from the officially supported distributions).</span></span>


- <span data-ttu-id="5271f-142">Version minimale du noyau 3.10.0-327</span><span class="sxs-lookup"><span data-stu-id="5271f-142">Minimum kernel version 3.10.0-327</span></span>

- <span data-ttu-id="5271f-143">`fanotify`L’option noyau doit être activée</span><span class="sxs-lookup"><span data-stu-id="5271f-143">The `fanotify` kernel option must be enabled</span></span>

  > [!CAUTION]
  > <span data-ttu-id="5271f-144">L’exécution de Defender pour Endpoint sur Linux côte à côte avec d’autres solutions de sécurité basées sur `fanotify` n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5271f-144">Running Defender for Endpoint on Linux side by side with other `fanotify`-based security solutions is not supported.</span></span> <span data-ttu-id="5271f-145">Cela peut entraîner des résultats imprévisibles, y compris l’arrêt du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="5271f-145">It can lead to unpredictable results, including hanging the operating system.</span></span>

- <span data-ttu-id="5271f-146">Espace disque : 1 Go</span><span class="sxs-lookup"><span data-stu-id="5271f-146">Disk space: 1 GB</span></span>

- <span data-ttu-id="5271f-147">/opt/microsoft/mdatp/sbin/wdavdaemon requiert une autorisation exécutable.</span><span class="sxs-lookup"><span data-stu-id="5271f-147">/opt/microsoft/mdatp/sbin/wdavdaemon requires executable permission.</span></span> <span data-ttu-id="5271f-148">Pour plus d’informations, voir « S’assurer que le daemon dispose de l’autorisation exécutable » dans Résoudre les problèmes d’installation de [Microsoft Defender pour Endpoint sur Linux.](/microsoft-365/security/defender-endpoint/linux-support-install)</span><span class="sxs-lookup"><span data-stu-id="5271f-148">For more information, see "Ensure that the daemon has executable permission" in [Troubleshoot installation issues for Microsoft Defender for Endpoint on Linux](/microsoft-365/security/defender-endpoint/linux-support-install).</span></span>

- <span data-ttu-id="5271f-149">Mémoire : 1 Go</span><span class="sxs-lookup"><span data-stu-id="5271f-149">Memory: 1 GB</span></span>

    > [!NOTE]
    > <span data-ttu-id="5271f-150">Assurez-vous que vous avez de l’espace disque libre dans /var.</span><span class="sxs-lookup"><span data-stu-id="5271f-150">Please make sure that you have free disk space in /var.</span></span>

- <span data-ttu-id="5271f-151">La solution fournit actuellement une protection en temps réel pour les types de système de fichiers suivants :</span><span class="sxs-lookup"><span data-stu-id="5271f-151">The solution currently provides real-time protection for the following file system types:</span></span>

  - `btrfs`
  - `ecryptfs`
  - `ext2`
  - `ext3`
  - `ext4`
  - `fuse`
  - `fuseblk`
  - `jfs`
  - `nfs`
  - `overlay`
  - `ramfs`
  - `reiserfs`
  - `tmpfs`
  - `udf`
  - `vfat`
  - `xfs`

<span data-ttu-id="5271f-152">Après avoir activé le service, vous devrez peut-être configurer votre réseau ou votre pare-feu pour autoriser les connexions sortantes entre celui-ci et vos points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="5271f-152">After you've enabled the service, you may need to configure your network or firewall to allow outbound connections between it and your endpoints.</span></span>

- <span data-ttu-id="5271f-153">L’infrastructure `auditd` d’audit ( ) doit être activée.</span><span class="sxs-lookup"><span data-stu-id="5271f-153">Audit framework (`auditd`) must be enabled.</span></span>
  > [!NOTE]
  > <span data-ttu-id="5271f-154">Les événements système capturés par les règles ajoutées à s’ajoutent à (s) et peuvent affecter l’audit de l’hôte `/etc/audit/rules.d/` et la collecte en `audit.log` amont.</span><span class="sxs-lookup"><span data-stu-id="5271f-154">System events captured by rules added to `/etc/audit/rules.d/` will add to `audit.log`(s) and might affect host auditing and upstream collection.</span></span> <span data-ttu-id="5271f-155">Les événements ajoutés par Microsoft Defender pour Endpoint sur Linux sont marqués avec une `mdatp` clé.</span><span class="sxs-lookup"><span data-stu-id="5271f-155">Events added by Microsoft Defender for Endpoint on Linux will be tagged with `mdatp` key.</span></span>

### <a name="network-connections"></a><span data-ttu-id="5271f-156">Connexions réseau</span><span class="sxs-lookup"><span data-stu-id="5271f-156">Network connections</span></span>

<span data-ttu-id="5271f-157">La feuille de calcul téléchargeable suivante répertorie les services et les URL associées à qui votre réseau doit pouvoir se connecter.</span><span class="sxs-lookup"><span data-stu-id="5271f-157">The following downloadable spreadsheet lists the services and their associated URLs that your network must be able to connect to.</span></span> <span data-ttu-id="5271f-158">Vous devez vous assurer qu’il n’existe aucune règle de pare-feu ou de filtrage réseau qui refuserait l’accès à ces URL.</span><span class="sxs-lookup"><span data-stu-id="5271f-158">You should ensure that there are no firewall or network filtering rules that would deny access to these URLs.</span></span> <span data-ttu-id="5271f-159">Si c’est le cas, vous devrez peut-être *créer* une règle d’autoriser spécifiquement pour eux.</span><span class="sxs-lookup"><span data-stu-id="5271f-159">If there are, you may need to create an *allow* rule specifically for them.</span></span>

| <span data-ttu-id="5271f-160">Liste de feuilles de calcul de domaines</span><span class="sxs-lookup"><span data-stu-id="5271f-160">Spreadsheet of domains list</span></span> | <span data-ttu-id="5271f-161">Description</span><span class="sxs-lookup"><span data-stu-id="5271f-161">Description</span></span> |
|:-----|:-----|
|![Image miniature de la feuille de calcul DES URL de Microsoft Defender pour les points de terminaison](images/mdatp-urls.png)<br/>  | <span data-ttu-id="5271f-163">Feuille de calcul d’enregistrements DNS spécifiques pour les emplacements de service, les emplacements géographiques et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="5271f-163">Spreadsheet of specific DNS records for service locations, geographic locations, and OS.</span></span> <br><br>[<span data-ttu-id="5271f-164">Téléchargez la feuille de calcul ici.</span><span class="sxs-lookup"><span data-stu-id="5271f-164">Download the spreadsheet here.</span></span>](https://download.microsoft.com/download/8/a/5/8a51eee5-cd02-431c-9d78-a58b7f77c070/mde-urls.xlsx)

> [!NOTE]
> <span data-ttu-id="5271f-165">Pour obtenir une liste d’URL plus spécifique, voir [Configurer les paramètres de proxy et de connectivité Internet.](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/configure-proxy-internet#enable-access-to-microsoft-defender-atp-service-urls-in-the-proxy-server)</span><span class="sxs-lookup"><span data-stu-id="5271f-165">For a more specific URL list, see [Configure proxy and internet connectivity settings](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/configure-proxy-internet#enable-access-to-microsoft-defender-atp-service-urls-in-the-proxy-server).</span></span>

<span data-ttu-id="5271f-166">Defender pour le point de terminaison peut découvrir un serveur proxy à l’aide des méthodes de découverte suivantes :</span><span class="sxs-lookup"><span data-stu-id="5271f-166">Defender for Endpoint can discover a proxy server by using the following discovery methods:</span></span>
- <span data-ttu-id="5271f-167">Proxy transparent</span><span class="sxs-lookup"><span data-stu-id="5271f-167">Transparent proxy</span></span>
- <span data-ttu-id="5271f-168">Configuration manuelle du proxy statique</span><span class="sxs-lookup"><span data-stu-id="5271f-168">Manual static proxy configuration</span></span>

<span data-ttu-id="5271f-169">Si un proxy ou un pare-feu bloque le trafic anonyme, assurez-vous que le trafic anonyme est autorisé dans les URL répertoriées précédemment.</span><span class="sxs-lookup"><span data-stu-id="5271f-169">If a proxy or firewall is blocking anonymous traffic, make sure that anonymous traffic is permitted in the previously listed URLs.</span></span> <span data-ttu-id="5271f-170">Pour les proxies transparents, aucune configuration supplémentaire n’est nécessaire pour Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="5271f-170">For transparent proxies, no additional configuration is needed for Defender for Endpoint.</span></span> <span data-ttu-id="5271f-171">Pour le proxy statique, suivez les étapes de [la configuration manuelle du proxy statique.](linux-static-proxy-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="5271f-171">For static proxy, follow the steps in [Manual Static Proxy Configuration](linux-static-proxy-configuration.md).</span></span>

> [!WARNING]
> <span data-ttu-id="5271f-172">Les pacs, WPAD et les proxies authentifiés ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="5271f-172">PAC, WPAD, and authenticated proxies are not supported.</span></span> <span data-ttu-id="5271f-173">Assurez-vous que seul un proxy statique ou transparent est utilisé.</span><span class="sxs-lookup"><span data-stu-id="5271f-173">Ensure that only a static proxy or transparent proxy is being used.</span></span>
>
> <span data-ttu-id="5271f-174">L’inspection et l’interception des proxies SSL ne sont pas non plus pris en charge pour des raisons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="5271f-174">SSL inspection and intercepting proxies are also not supported for security reasons.</span></span> <span data-ttu-id="5271f-175">Configurez une exception pour l’inspection SSL et votre serveur proxy afin de transmettre directement les données de Defender pour Endpoint sur Linux aux URL pertinentes sans interception.</span><span class="sxs-lookup"><span data-stu-id="5271f-175">Configure an exception for SSL inspection and your proxy server to directly pass through data from Defender for Endpoint on Linux to the relevant URLs without interception.</span></span> <span data-ttu-id="5271f-176">L’ajout de votre certificat d’interception au magasin global n’autorise pas l’interception.</span><span class="sxs-lookup"><span data-stu-id="5271f-176">Adding your interception certificate to the global store will not allow for interception.</span></span>

<span data-ttu-id="5271f-177">Pour les étapes de résolution des problèmes, voir Résoudre les problèmes de connectivité cloud pour [Microsoft Defender pour Endpoint sur Linux.](linux-support-connectivity.md)</span><span class="sxs-lookup"><span data-stu-id="5271f-177">For troubleshooting steps, see [Troubleshoot cloud connectivity issues for Microsoft Defender for Endpoint on Linux](linux-support-connectivity.md).</span></span>

## <a name="how-to-update-microsoft-defender-for-endpoint-on-linux"></a><span data-ttu-id="5271f-178">Comment mettre à jour Microsoft Defender pour endpoint sur Linux</span><span class="sxs-lookup"><span data-stu-id="5271f-178">How to update Microsoft Defender for Endpoint on Linux</span></span>

<span data-ttu-id="5271f-179">Microsoft publie régulièrement des mises à jour logicielles pour améliorer les performances, la sécurité et fournir de nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="5271f-179">Microsoft regularly publishes software updates to improve performance, security, and to deliver new features.</span></span> <span data-ttu-id="5271f-180">Pour mettre à jour Microsoft Defender pour endpoint sur Linux, reportez-vous à Déployer les mises à jour [de Microsoft Defender pour Endpoint sur Linux.](linux-updates.md)</span><span class="sxs-lookup"><span data-stu-id="5271f-180">To update Microsoft Defender for Endpoint on Linux, refer to [Deploy updates for Microsoft Defender for Endpoint on Linux](linux-updates.md).</span></span>

## <a name="how-to-configure-microsoft-defender-for-endpoint-on-linux"></a><span data-ttu-id="5271f-181">Comment configurer Microsoft Defender pour endpoint sur Linux</span><span class="sxs-lookup"><span data-stu-id="5271f-181">How to configure Microsoft Defender for Endpoint on Linux</span></span>

<span data-ttu-id="5271f-182">Des instructions sur la configuration du produit dans les environnements d’entreprise sont disponibles dans Définir les préférences [de Microsoft Defender pour Endpoint sur Linux.](linux-preferences.md)</span><span class="sxs-lookup"><span data-stu-id="5271f-182">Guidance for how to configure the product in enterprise environments is available in [Set preferences for Microsoft Defender for Endpoint on Linux](linux-preferences.md).</span></span>

## <a name="resources"></a><span data-ttu-id="5271f-183">Ressources</span><span class="sxs-lookup"><span data-stu-id="5271f-183">Resources</span></span>

- <span data-ttu-id="5271f-184">Pour plus d’informations sur la journalisation, la désinstallation ou d’autres rubriques, voir [Resources](linux-resources.md).</span><span class="sxs-lookup"><span data-stu-id="5271f-184">For more information about logging, uninstalling, or other topics, see [Resources](linux-resources.md).</span></span>
