---
title: Microsoft Defender ATP pour Linux
ms.reviewer: ''
description: Décrit comment installer et utiliser Microsoft Defender ATP pour Linux.
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
ms.openlocfilehash: 08bb4c73cb9df429c4b07194f1c7615f44d745d8
ms.sourcegitcommit: c75aac39ee8d93218a79585113ef6b36f47c9ddf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2021
ms.locfileid: "51408336"
---
# <a name="microsoft-defender-for-endpoint-for-linux"></a><span data-ttu-id="fc4b8-104">Microsoft Defender pour point de terminaison Linux</span><span class="sxs-lookup"><span data-stu-id="fc4b8-104">Microsoft Defender for Endpoint for Linux</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="fc4b8-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="fc4b8-105">**Applies to:**</span></span>
- [<span data-ttu-id="fc4b8-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="fc4b8-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="fc4b8-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="fc4b8-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="fc4b8-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="fc4b8-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="fc4b8-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="fc4b8-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="fc4b8-110">Cette rubrique décrit comment installer, configurer, mettre à jour et utiliser Microsoft Defender pour Endpoint pour Linux.</span><span class="sxs-lookup"><span data-stu-id="fc4b8-110">This topic describes how to install, configure, update, and use Microsoft Defender for Endpoint for Linux.</span></span>

> [!CAUTION]
> <span data-ttu-id="fc4b8-111">L’exécution d’autres produits de protection de point de terminaison tiers avec Microsoft Defender pour Endpoint pour Linux est susceptible de provoquer des problèmes de performances et des erreurs système imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="fc4b8-111">Running other third-party endpoint protection products alongside Microsoft Defender for Endpoint for Linux is likely to cause performance problems and unpredictable system errors.</span></span>

## <a name="how-to-install-microsoft-defender-for-endpoint-for-linux"></a><span data-ttu-id="fc4b8-112">Comment installer Microsoft Defender pour endpoint pour Linux</span><span class="sxs-lookup"><span data-stu-id="fc4b8-112">How to install Microsoft Defender for Endpoint for Linux</span></span>

### <a name="prerequisites"></a><span data-ttu-id="fc4b8-113">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="fc4b8-113">Prerequisites</span></span>

- <span data-ttu-id="fc4b8-114">Accès au portail Centre de sécurité Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="fc4b8-114">Access to the Microsoft Defender Security Center portal</span></span>
- <span data-ttu-id="fc4b8-115">Distribution Linux à l’aide [du gestionnaire système](https://systemd.io/)</span><span class="sxs-lookup"><span data-stu-id="fc4b8-115">Linux distribution using the [systemd](https://systemd.io/) system manager</span></span>
- <span data-ttu-id="fc4b8-116">Expérience de niveau débutant dans les scripts Linux et BASH</span><span class="sxs-lookup"><span data-stu-id="fc4b8-116">Beginner-level experience in Linux and BASH scripting</span></span>
- <span data-ttu-id="fc4b8-117">Privilèges d’administration sur l’appareil (en cas de déploiement manuel)</span><span class="sxs-lookup"><span data-stu-id="fc4b8-117">Administrative privileges on the device (in case of manual deployment)</span></span>

### <a name="installation-instructions"></a><span data-ttu-id="fc4b8-118">Instructions d’installation</span><span class="sxs-lookup"><span data-stu-id="fc4b8-118">Installation instructions</span></span>

<span data-ttu-id="fc4b8-119">Vous pouvez utiliser plusieurs méthodes et outils de déploiement pour installer et configurer Microsoft Defender pour Endpoint pour Linux.</span><span class="sxs-lookup"><span data-stu-id="fc4b8-119">There are several methods and deployment tools that you can use to install and configure Microsoft Defender for Endpoint for Linux.</span></span>

<span data-ttu-id="fc4b8-120">En règle générale, vous devez suivre les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="fc4b8-120">In general you need to take the following steps:</span></span>

- <span data-ttu-id="fc4b8-121">Assurez-vous que vous avez un abonnement Microsoft Defender pour points de terminaison et que vous avez accès au portail [Microsoft Defender pour points de terminaison.](microsoft-defender-security-center.md)</span><span class="sxs-lookup"><span data-stu-id="fc4b8-121">Ensure that you have a Microsoft Defender for Endpoint subscription, and that you have access to the [Microsoft Defender for Endpoint portal](microsoft-defender-security-center.md).</span></span>
- <span data-ttu-id="fc4b8-122">Déployez Microsoft Defender pour endpoint pour Linux à l’aide de l’une des méthodes de déploiement suivantes :</span><span class="sxs-lookup"><span data-stu-id="fc4b8-122">Deploy Microsoft Defender for Endpoint for Linux using one of the following deployment methods:</span></span>
  - <span data-ttu-id="fc4b8-123">L’outil en ligne de commande :</span><span class="sxs-lookup"><span data-stu-id="fc4b8-123">The command-line tool:</span></span>
    - [<span data-ttu-id="fc4b8-124">Déploiement manuel</span><span class="sxs-lookup"><span data-stu-id="fc4b8-124">Manual deployment</span></span>](linux-install-manually.md)
  - <span data-ttu-id="fc4b8-125">Outils de gestion tiers :</span><span class="sxs-lookup"><span data-stu-id="fc4b8-125">Third-party management tools:</span></span>
    - [<span data-ttu-id="fc4b8-126">Déployer à l’aide de l’outil de gestion de la configuration de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="fc4b8-126">Deploy using Puppet configuration management tool</span></span>](linux-install-with-puppet.md)
    - [<span data-ttu-id="fc4b8-127">Déployer à l’aide de l’outil de gestion de la configuration Ansible</span><span class="sxs-lookup"><span data-stu-id="fc4b8-127">Deploy using Ansible configuration management tool</span></span>](linux-install-with-ansible.md)

<span data-ttu-id="fc4b8-128">Si vous avez des échecs d’installation, reportez-vous à Résolution des problèmes d’installation dans [Microsoft Defender pour Endpoint pour Linux.](linux-support-install.md)</span><span class="sxs-lookup"><span data-stu-id="fc4b8-128">If you experience any installation failures, refer to [Troubleshooting installation failures in Microsoft Defender for Endpoint for Linux](linux-support-install.md).</span></span>

### <a name="system-requirements"></a><span data-ttu-id="fc4b8-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc4b8-129">System requirements</span></span>

- <span data-ttu-id="fc4b8-130">Distributions et versions de serveur Linux pris en charge :</span><span class="sxs-lookup"><span data-stu-id="fc4b8-130">Supported Linux server distributions and versions:</span></span>

  - <span data-ttu-id="fc4b8-131">Red Hat Enterprise Linux 7.2 ou supérieur</span><span class="sxs-lookup"><span data-stu-id="fc4b8-131">Red Hat Enterprise Linux 7.2 or higher</span></span>
  - <span data-ttu-id="fc4b8-132">CentOS 7.2 ou supérieur</span><span class="sxs-lookup"><span data-stu-id="fc4b8-132">CentOS 7.2 or higher</span></span>
  - <span data-ttu-id="fc4b8-133">Ubuntu 16.04 LTS ou une LTS supérieure</span><span class="sxs-lookup"><span data-stu-id="fc4b8-133">Ubuntu 16.04 LTS or higher LTS</span></span>
  - <span data-ttu-id="fc4b8-134">Debian 9 ou supérieur</span><span class="sxs-lookup"><span data-stu-id="fc4b8-134">Debian 9 or higher</span></span>
  - <span data-ttu-id="fc4b8-135">SUSE Linux Enterprise Server 12 ou supérieur</span><span class="sxs-lookup"><span data-stu-id="fc4b8-135">SUSE Linux Enterprise Server 12 or higher</span></span>
  - <span data-ttu-id="fc4b8-136">Oracle Linux 7.2 ou supérieur</span><span class="sxs-lookup"><span data-stu-id="fc4b8-136">Oracle Linux 7.2 or higher</span></span>

- <span data-ttu-id="fc4b8-137">Version minimale du noyau 3.10.0-327</span><span class="sxs-lookup"><span data-stu-id="fc4b8-137">Minimum kernel version 3.10.0-327</span></span>
- <span data-ttu-id="fc4b8-138">`fanotify`L’option noyau doit être activée</span><span class="sxs-lookup"><span data-stu-id="fc4b8-138">The `fanotify` kernel option must be enabled</span></span>
  > [!CAUTION]
  > <span data-ttu-id="fc4b8-139">L’exécution de Defender pour Endpoint pour Linux côte à côte avec d’autres solutions de sécurité basées sur la sécurité `fanotify` n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="fc4b8-139">Running Defender for Endpoint for Linux side by side with other `fanotify`-based security solutions is not supported.</span></span> <span data-ttu-id="fc4b8-140">Cela peut entraîner des résultats imprévisibles, y compris la suspension du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="fc4b8-140">It can lead to unpredictable results, including hanging the operating system.</span></span>

- <span data-ttu-id="fc4b8-141">Espace disque : 1 Go</span><span class="sxs-lookup"><span data-stu-id="fc4b8-141">Disk space: 1GB</span></span>
- <span data-ttu-id="fc4b8-142">/opt/microsoft/mdatp/sbin/wdavdaemon requiert une autorisation exécutable.</span><span class="sxs-lookup"><span data-stu-id="fc4b8-142">/opt/microsoft/mdatp/sbin/wdavdaemon requires executable permission.</span></span> <span data-ttu-id="fc4b8-143">Pour plus d’informations, voir « S’assurer que le daemon dispose de l’autorisation exécutable » dans Résoudre les problèmes d’installation de [Microsoft Defender ATP pour Linux.](/microsoft-365/security/defender-endpoint/linux-support-install)</span><span class="sxs-lookup"><span data-stu-id="fc4b8-143">For more information, see "Ensure that the daemon has executable permission" in [Troubleshoot installation issues for Microsoft Defender ATP for Linux](/microsoft-365/security/defender-endpoint/linux-support-install).</span></span>
- <span data-ttu-id="fc4b8-144">Mémoire : 1 Go</span><span class="sxs-lookup"><span data-stu-id="fc4b8-144">Memory: 1GB</span></span>
    > [!NOTE]
    > <span data-ttu-id="fc4b8-145">Assurez-vous que vous avez de l’espace disque libre dans /var.</span><span class="sxs-lookup"><span data-stu-id="fc4b8-145">Please make sure that you have free disk space in /var.</span></span>

- <span data-ttu-id="fc4b8-146">La solution fournit actuellement une protection en temps réel pour les types de système de fichiers suivants :</span><span class="sxs-lookup"><span data-stu-id="fc4b8-146">The solution currently provides real-time protection for the following file system types:</span></span>

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

<span data-ttu-id="fc4b8-147">Après avoir activé le service, vous devrez peut-être configurer votre réseau ou votre pare-feu pour autoriser les connexions sortantes entre celui-ci et vos points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="fc4b8-147">After you've enabled the service, you may need to configure your network or firewall to allow outbound connections between it and your endpoints.</span></span>

- <span data-ttu-id="fc4b8-148">L’infrastructure `auditd` d’audit ( ) doit être activée.</span><span class="sxs-lookup"><span data-stu-id="fc4b8-148">Audit framework (`auditd`) must be enabled.</span></span>
  >[!NOTE]
  > <span data-ttu-id="fc4b8-149">Les événements système capturés par les règles ajoutées aux journaux d’audit s’ajoutent aux journaux d’audit et peuvent affecter l’audit de l’hôte `audit.logs` et la collecte en amont.</span><span class="sxs-lookup"><span data-stu-id="fc4b8-149">System events captured by rules added to `audit.logs` will add to audit logs and might affect host auditing and upstream collection.</span></span> <span data-ttu-id="fc4b8-150">Les événements ajoutés par Microsoft Defender pour Endopoint pour Linux sont marqués avec une `mdatp` clé.</span><span class="sxs-lookup"><span data-stu-id="fc4b8-150">Events added by Microsoft Defender for Endopoint for Linux will be tagged with `mdatp` key.</span></span>

### <a name="network-connections"></a><span data-ttu-id="fc4b8-151">Connexions réseau</span><span class="sxs-lookup"><span data-stu-id="fc4b8-151">Network connections</span></span>

<span data-ttu-id="fc4b8-152">La feuille de calcul téléchargeable suivante répertorie les services et les URL associées à qui votre réseau doit pouvoir se connecter.</span><span class="sxs-lookup"><span data-stu-id="fc4b8-152">The following downloadable spreadsheet lists the services and their associated URLs that your network must be able to connect to.</span></span> <span data-ttu-id="fc4b8-153">Vous devez vous assurer qu’il n’existe aucune règle de pare-feu ou de filtrage réseau qui refuserait l’accès à ces URL.</span><span class="sxs-lookup"><span data-stu-id="fc4b8-153">You should ensure that there are no firewall or network filtering rules that would deny access to these URLs.</span></span> <span data-ttu-id="fc4b8-154">Si c’est le cas, vous devrez peut-être *créer* une règle d’autoriser spécifiquement pour eux.</span><span class="sxs-lookup"><span data-stu-id="fc4b8-154">If there are, you may need to create an *allow* rule specifically for them.</span></span>

|<span data-ttu-id="fc4b8-155">**Liste de feuilles de calcul de domaines**</span><span class="sxs-lookup"><span data-stu-id="fc4b8-155">**Spreadsheet of domains list**</span></span>|<span data-ttu-id="fc4b8-156">**Description**</span><span class="sxs-lookup"><span data-stu-id="fc4b8-156">**Description**</span></span>|
|:-----|:-----|
|![Image miniature de la feuille de calcul DES URL de Microsoft Defender pour les points de terminaison](images/mdatp-urls.png)<br/>  | <span data-ttu-id="fc4b8-158">Feuille de calcul d’enregistrements DNS spécifiques pour les emplacements de service, les emplacements géographiques et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="fc4b8-158">Spreadsheet of specific DNS records for service locations, geographic locations, and OS.</span></span> <br><br>[<span data-ttu-id="fc4b8-159">Téléchargez la feuille de calcul ici.</span><span class="sxs-lookup"><span data-stu-id="fc4b8-159">Download the spreadsheet here.</span></span>](https://download.microsoft.com/download/8/a/5/8a51eee5-cd02-431c-9d78-a58b7f77c070/mde-urls.xlsx)

> [!NOTE]
> <span data-ttu-id="fc4b8-160">Pour obtenir une liste d’URL plus spécifique, voir [Configurer les paramètres de proxy et de connectivité Internet.](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/configure-proxy-internet#enable-access-to-microsoft-defender-atp-service-urls-in-the-proxy-server)</span><span class="sxs-lookup"><span data-stu-id="fc4b8-160">For a more specific URL list, see [Configure proxy and internet connectivity settings](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/configure-proxy-internet#enable-access-to-microsoft-defender-atp-service-urls-in-the-proxy-server).</span></span>

<span data-ttu-id="fc4b8-161">Defender pour le point de terminaison peut découvrir un serveur proxy à l’aide des méthodes de découverte suivantes :</span><span class="sxs-lookup"><span data-stu-id="fc4b8-161">Defender for Endpoint can discover a proxy server by using the following discovery methods:</span></span>
- <span data-ttu-id="fc4b8-162">Proxy transparent</span><span class="sxs-lookup"><span data-stu-id="fc4b8-162">Transparent proxy</span></span>
- <span data-ttu-id="fc4b8-163">Configuration manuelle du proxy statique</span><span class="sxs-lookup"><span data-stu-id="fc4b8-163">Manual static proxy configuration</span></span>

<span data-ttu-id="fc4b8-164">Si un proxy ou un pare-feu bloque le trafic anonyme, assurez-vous que le trafic anonyme est autorisé dans les URL répertoriées précédemment.</span><span class="sxs-lookup"><span data-stu-id="fc4b8-164">If a proxy or firewall is blocking anonymous traffic, make sure that anonymous traffic is permitted in the previously listed URLs.</span></span> <span data-ttu-id="fc4b8-165">Pour les proxies transparents, aucune configuration supplémentaire n’est nécessaire pour Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="fc4b8-165">For transparent proxies, no additional configuration is needed for Defender for Endpoint.</span></span> <span data-ttu-id="fc4b8-166">Pour le proxy statique, suivez les étapes de [la configuration manuelle du proxy statique.](linux-static-proxy-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="fc4b8-166">For static proxy, follow the steps in [Manual Static Proxy Configuration](linux-static-proxy-configuration.md).</span></span>

> [!WARNING]
> <span data-ttu-id="fc4b8-167">Les pacs, WPAD et les proxies authentifiés ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="fc4b8-167">PAC, WPAD, and authenticated proxies are not supported.</span></span> <span data-ttu-id="fc4b8-168">Assurez-vous que seul un proxy statique ou transparent est utilisé.</span><span class="sxs-lookup"><span data-stu-id="fc4b8-168">Ensure that only a static proxy or transparent proxy is being used.</span></span>
>
> <span data-ttu-id="fc4b8-169">L’inspection et l’interception des proxies SSL ne sont pas non plus pris en charge pour des raisons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="fc4b8-169">SSL inspection and intercepting proxies are also not supported for security reasons.</span></span> <span data-ttu-id="fc4b8-170">Configurez une exception pour l’inspection SSL et votre serveur proxy pour transmettre directement les données de Defender for Endpoint for Linux aux URL pertinentes sans interception.</span><span class="sxs-lookup"><span data-stu-id="fc4b8-170">Configure an exception for SSL inspection and your proxy server to directly pass through data from Defender for Endpoint for Linux to the relevant URLs without interception.</span></span> <span data-ttu-id="fc4b8-171">L’ajout de votre certificat d’interception au magasin global n’autorise pas l’interception.</span><span class="sxs-lookup"><span data-stu-id="fc4b8-171">Adding your interception certificate to the global store will not allow for interception.</span></span>

<span data-ttu-id="fc4b8-172">Pour les étapes de résolution des problèmes, voir Résoudre les problèmes de connectivité cloud pour [Microsoft Defender pour Endpoint pour Linux.](linux-support-connectivity.md)</span><span class="sxs-lookup"><span data-stu-id="fc4b8-172">For troubleshooting steps, see [Troubleshoot cloud connectivity issues for Microsoft Defender for Endpoint for Linux](linux-support-connectivity.md).</span></span>

## <a name="how-to-update-microsoft-defender-for-endpoint-for-linux"></a><span data-ttu-id="fc4b8-173">Comment mettre à jour Microsoft Defender pour endpoint pour Linux</span><span class="sxs-lookup"><span data-stu-id="fc4b8-173">How to update Microsoft Defender for Endpoint for Linux</span></span>

<span data-ttu-id="fc4b8-174">Microsoft publie régulièrement des mises à jour logicielles pour améliorer les performances, la sécurité et fournir de nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="fc4b8-174">Microsoft regularly publishes software updates to improve performance, security, and to deliver new features.</span></span> <span data-ttu-id="fc4b8-175">Pour mettre à jour Microsoft Defender pour endpoint pour Linux, reportez-vous à Déployer les mises à jour [de Microsoft Defender pour Endpoint pour Linux.](linux-updates.md)</span><span class="sxs-lookup"><span data-stu-id="fc4b8-175">To update Microsoft Defender for Endpoint for Linux, refer to [Deploy updates for Microsoft Defender for Endpoint for Linux](linux-updates.md).</span></span>

## <a name="how-to-configure-microsoft-defender-for-endpoint-for-linux"></a><span data-ttu-id="fc4b8-176">Comment configurer Microsoft Defender pour endpoint pour Linux</span><span class="sxs-lookup"><span data-stu-id="fc4b8-176">How to configure Microsoft Defender for Endpoint for Linux</span></span>

<span data-ttu-id="fc4b8-177">Des instructions sur la configuration du produit dans les environnements d’entreprise sont disponibles dans Définir les préférences de [Microsoft Defender pour Endpoint pour Linux.](linux-preferences.md)</span><span class="sxs-lookup"><span data-stu-id="fc4b8-177">Guidance for how to configure the product in enterprise environments is available in [Set preferences for Microsoft Defender for Endpoint for Linux](linux-preferences.md).</span></span>

## <a name="resources"></a><span data-ttu-id="fc4b8-178">Ressources</span><span class="sxs-lookup"><span data-stu-id="fc4b8-178">Resources</span></span>

- <span data-ttu-id="fc4b8-179">Pour plus d’informations sur la journalisation, la désinstallation ou d’autres rubriques, voir [Resources](linux-resources.md).</span><span class="sxs-lookup"><span data-stu-id="fc4b8-179">For more information about logging, uninstalling, or other topics, see [Resources](linux-resources.md).</span></span>
