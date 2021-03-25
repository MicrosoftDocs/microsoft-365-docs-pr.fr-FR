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
ms.openlocfilehash: ce7b15a727ddfa9b0d2bc68b7901f2e79aaf0721
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51064961"
---
# <a name="microsoft-defender-for-endpoint-for-linux"></a><span data-ttu-id="481e9-104">Microsoft Defender pour point de terminaison pour Linux</span><span class="sxs-lookup"><span data-stu-id="481e9-104">Microsoft Defender for Endpoint for Linux</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="481e9-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="481e9-105">**Applies to:**</span></span>
- [<span data-ttu-id="481e9-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="481e9-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2146631)
- [<span data-ttu-id="481e9-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="481e9-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="481e9-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="481e9-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="481e9-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="481e9-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="481e9-110">Cette rubrique décrit comment installer, configurer, mettre à jour et utiliser Microsoft Defender pour Endpoint pour Linux.</span><span class="sxs-lookup"><span data-stu-id="481e9-110">This topic describes how to install, configure, update, and use Microsoft Defender for Endpoint for Linux.</span></span>

> [!CAUTION]
> <span data-ttu-id="481e9-111">L’exécution d’autres produits de protection de point de terminaison tiers avec Microsoft Defender pour Endpoint pour Linux est susceptible de provoquer des problèmes de performances et des erreurs système imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="481e9-111">Running other third-party endpoint protection products alongside Microsoft Defender for Endpoint for Linux is likely to cause performance problems and unpredictable system errors.</span></span>

## <a name="how-to-install-microsoft-defender-for-endpoint-for-linux"></a><span data-ttu-id="481e9-112">Comment installer Microsoft Defender pour endpoint pour Linux</span><span class="sxs-lookup"><span data-stu-id="481e9-112">How to install Microsoft Defender for Endpoint for Linux</span></span>

### <a name="prerequisites"></a><span data-ttu-id="481e9-113">Prerequisites</span><span class="sxs-lookup"><span data-stu-id="481e9-113">Prerequisites</span></span>

- <span data-ttu-id="481e9-114">Accès au portail Centre de sécurité Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="481e9-114">Access to the Microsoft Defender Security Center portal</span></span>
- <span data-ttu-id="481e9-115">Distribution Linux à l’aide [du gestionnaire système](https://systemd.io/)</span><span class="sxs-lookup"><span data-stu-id="481e9-115">Linux distribution using the [systemd](https://systemd.io/) system manager</span></span>
- <span data-ttu-id="481e9-116">Expérience de niveau débutant dans les scripts Linux et BASH</span><span class="sxs-lookup"><span data-stu-id="481e9-116">Beginner-level experience in Linux and BASH scripting</span></span>
- <span data-ttu-id="481e9-117">Privilèges d’administration sur l’appareil (en cas de déploiement manuel)</span><span class="sxs-lookup"><span data-stu-id="481e9-117">Administrative privileges on the device (in case of manual deployment)</span></span>

### <a name="installation-instructions"></a><span data-ttu-id="481e9-118">Instructions d’installation</span><span class="sxs-lookup"><span data-stu-id="481e9-118">Installation instructions</span></span>

<span data-ttu-id="481e9-119">Vous pouvez utiliser plusieurs méthodes et outils de déploiement pour installer et configurer Microsoft Defender pour Endpoint pour Linux.</span><span class="sxs-lookup"><span data-stu-id="481e9-119">There are several methods and deployment tools that you can use to install and configure Microsoft Defender for Endpoint for Linux.</span></span>

<span data-ttu-id="481e9-120">En règle générale, vous devez suivre les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="481e9-120">In general you need to take the following steps:</span></span>

- <span data-ttu-id="481e9-121">Assurez-vous que vous avez un abonnement Microsoft Defender pour points de terminaison et que vous avez accès au portail [Microsoft Defender pour points de terminaison.](microsoft-defender-security-center.md)</span><span class="sxs-lookup"><span data-stu-id="481e9-121">Ensure that you have a Microsoft Defender for Endpoint subscription, and that you have access to the [Microsoft Defender for Endpoint portal](microsoft-defender-security-center.md).</span></span>
- <span data-ttu-id="481e9-122">Déployez Microsoft Defender pour endpoint pour Linux à l’aide de l’une des méthodes de déploiement suivantes :</span><span class="sxs-lookup"><span data-stu-id="481e9-122">Deploy Microsoft Defender for Endpoint for Linux using one of the following deployment methods:</span></span>
  - <span data-ttu-id="481e9-123">L’outil en ligne de commande :</span><span class="sxs-lookup"><span data-stu-id="481e9-123">The command-line tool:</span></span>
    - [<span data-ttu-id="481e9-124">Déploiement manuel</span><span class="sxs-lookup"><span data-stu-id="481e9-124">Manual deployment</span></span>](linux-install-manually.md)
  - <span data-ttu-id="481e9-125">Outils de gestion tiers :</span><span class="sxs-lookup"><span data-stu-id="481e9-125">Third-party management tools:</span></span>
    - [<span data-ttu-id="481e9-126">Déployer à l’aide de l’outil de gestion de la configuration de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="481e9-126">Deploy using Puppet configuration management tool</span></span>](linux-install-with-puppet.md)
    - [<span data-ttu-id="481e9-127">Déployer à l’aide de l’outil de gestion de la configuration Ansible</span><span class="sxs-lookup"><span data-stu-id="481e9-127">Deploy using Ansible configuration management tool</span></span>](linux-install-with-ansible.md)

<span data-ttu-id="481e9-128">Si vous avez des échecs d’installation, reportez-vous à Résolution des problèmes d’installation dans [Microsoft Defender pour Endpoint pour Linux.](linux-support-install.md)</span><span class="sxs-lookup"><span data-stu-id="481e9-128">If you experience any installation failures, refer to [Troubleshooting installation failures in Microsoft Defender for Endpoint for Linux](linux-support-install.md).</span></span>

### <a name="system-requirements"></a><span data-ttu-id="481e9-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="481e9-129">System requirements</span></span>

- <span data-ttu-id="481e9-130">Distributions et versions de serveur Linux pris en charge :</span><span class="sxs-lookup"><span data-stu-id="481e9-130">Supported Linux server distributions and versions:</span></span>

  - <span data-ttu-id="481e9-131">Red Hat Enterprise Linux 7.2 ou supérieur</span><span class="sxs-lookup"><span data-stu-id="481e9-131">Red Hat Enterprise Linux 7.2 or higher</span></span>
  - <span data-ttu-id="481e9-132">CentOS 7.2 ou supérieur</span><span class="sxs-lookup"><span data-stu-id="481e9-132">CentOS 7.2 or higher</span></span>
  - <span data-ttu-id="481e9-133">Ubuntu 16.04 LTS ou une LTS supérieure</span><span class="sxs-lookup"><span data-stu-id="481e9-133">Ubuntu 16.04 LTS or higher LTS</span></span>
  - <span data-ttu-id="481e9-134">Debian 9 ou supérieur</span><span class="sxs-lookup"><span data-stu-id="481e9-134">Debian 9 or higher</span></span>
  - <span data-ttu-id="481e9-135">SUSE Linux Enterprise Server 12 ou supérieur</span><span class="sxs-lookup"><span data-stu-id="481e9-135">SUSE Linux Enterprise Server 12 or higher</span></span>
  - <span data-ttu-id="481e9-136">Oracle Linux 7.2 ou supérieur</span><span class="sxs-lookup"><span data-stu-id="481e9-136">Oracle Linux 7.2 or higher</span></span>

- <span data-ttu-id="481e9-137">Version minimale du noyau 3.10.0-327</span><span class="sxs-lookup"><span data-stu-id="481e9-137">Minimum kernel version 3.10.0-327</span></span>
- <span data-ttu-id="481e9-138">`fanotify`L’option noyau doit être activée</span><span class="sxs-lookup"><span data-stu-id="481e9-138">The `fanotify` kernel option must be enabled</span></span>
  > [!CAUTION]
  > <span data-ttu-id="481e9-139">L’exécution de Defender pour Endpoint pour Linux côte à côte avec d’autres solutions de sécurité basées sur `fanotify` n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="481e9-139">Running Defender for Endpoint for Linux side by side with other `fanotify`-based security solutions is not supported.</span></span> <span data-ttu-id="481e9-140">Cela peut entraîner des résultats imprévisibles, y compris l’arrêt du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="481e9-140">It can lead to unpredictable results, including hanging the operating system.</span></span>

- <span data-ttu-id="481e9-141">Espace disque : 1 Go</span><span class="sxs-lookup"><span data-stu-id="481e9-141">Disk space: 1GB</span></span>
- <span data-ttu-id="481e9-142">La solution fournit actuellement une protection en temps réel pour les types de système de fichiers suivants :</span><span class="sxs-lookup"><span data-stu-id="481e9-142">The solution currently provides real-time protection for the following file system types:</span></span>

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

<span data-ttu-id="481e9-143">Après avoir activé le service, vous devrez peut-être configurer votre réseau ou votre pare-feu pour autoriser les connexions sortantes entre celui-ci et vos points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="481e9-143">After you've enabled the service, you may need to configure your network or firewall to allow outbound connections between it and your endpoints.</span></span>

- <span data-ttu-id="481e9-144">L’infrastructure `auditd` d’audit ( ) doit être activée.</span><span class="sxs-lookup"><span data-stu-id="481e9-144">Audit framework (`auditd`) must be enabled.</span></span>
  >[!NOTE]
  > <span data-ttu-id="481e9-145">Les événements système capturés par les règles ajoutées aux journaux d’audit s’ajoutent aux journaux d’audit et peuvent affecter l’audit de l’hôte `audit.logs` et la collecte en amont.</span><span class="sxs-lookup"><span data-stu-id="481e9-145">System events captured by rules added to `audit.logs` will add to audit logs and might affect host auditing and upstream collection.</span></span> <span data-ttu-id="481e9-146">Les événements ajoutés par Microsoft Defender pour Endopoint pour Linux sont marqués avec une `mdatp` clé.</span><span class="sxs-lookup"><span data-stu-id="481e9-146">Events added by Microsoft Defender for Endopoint for Linux will be tagged with `mdatp` key.</span></span>

### <a name="network-connections"></a><span data-ttu-id="481e9-147">Connexions réseau</span><span class="sxs-lookup"><span data-stu-id="481e9-147">Network connections</span></span>

<span data-ttu-id="481e9-148">La feuille de calcul téléchargeable suivante répertorie les services et les URL associées à qui votre réseau doit pouvoir se connecter.</span><span class="sxs-lookup"><span data-stu-id="481e9-148">The following downloadable spreadsheet lists the services and their associated URLs that your network must be able to connect to.</span></span> <span data-ttu-id="481e9-149">Vous devez vous assurer qu’il n’existe aucune règle de pare-feu ou de filtrage réseau qui refuserait l’accès à ces URL.</span><span class="sxs-lookup"><span data-stu-id="481e9-149">You should ensure that there are no firewall or network filtering rules that would deny access to these URLs.</span></span> <span data-ttu-id="481e9-150">Si c’est le cas, vous devrez peut-être *créer* une règle d’autoriser spécifiquement pour eux.</span><span class="sxs-lookup"><span data-stu-id="481e9-150">If there are, you may need to create an *allow* rule specifically for them.</span></span>

|<span data-ttu-id="481e9-151">**Liste de feuilles de calcul de domaines**</span><span class="sxs-lookup"><span data-stu-id="481e9-151">**Spreadsheet of domains list**</span></span>|<span data-ttu-id="481e9-152">**Description**</span><span class="sxs-lookup"><span data-stu-id="481e9-152">**Description**</span></span>|
|:-----|:-----|
|![Image miniature de la feuille de calcul DES URL de Microsoft Defender pour les points de terminaison](images/mdatp-urls.png)<br/>  | <span data-ttu-id="481e9-154">Feuille de calcul d’enregistrements DNS spécifiques pour les emplacements de service, les emplacements géographiques et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="481e9-154">Spreadsheet of specific DNS records for service locations, geographic locations, and OS.</span></span> <br><br>[<span data-ttu-id="481e9-155">Téléchargez la feuille de calcul ici.</span><span class="sxs-lookup"><span data-stu-id="481e9-155">Download the spreadsheet here.</span></span>](https://download.microsoft.com/download/8/a/5/8a51eee5-cd02-431c-9d78-a58b7f77c070/mde-urls.xlsx)

> [!NOTE]
> <span data-ttu-id="481e9-156">Pour obtenir une liste d’URL plus spécifique, voir [Configurer les paramètres de proxy et de connectivité Internet.](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/configure-proxy-internet#enable-access-to-microsoft-defender-atp-service-urls-in-the-proxy-server)</span><span class="sxs-lookup"><span data-stu-id="481e9-156">For a more specific URL list, see [Configure proxy and internet connectivity settings](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/configure-proxy-internet#enable-access-to-microsoft-defender-atp-service-urls-in-the-proxy-server).</span></span>

<span data-ttu-id="481e9-157">Defender pour le point de terminaison peut découvrir un serveur proxy à l’aide des méthodes de découverte suivantes :</span><span class="sxs-lookup"><span data-stu-id="481e9-157">Defender for Endpoint can discover a proxy server by using the following discovery methods:</span></span>
- <span data-ttu-id="481e9-158">Proxy transparent</span><span class="sxs-lookup"><span data-stu-id="481e9-158">Transparent proxy</span></span>
- <span data-ttu-id="481e9-159">Configuration manuelle du proxy statique</span><span class="sxs-lookup"><span data-stu-id="481e9-159">Manual static proxy configuration</span></span>

<span data-ttu-id="481e9-160">Si un proxy ou un pare-feu bloque le trafic anonyme, assurez-vous que le trafic anonyme est autorisé dans les URL répertoriées précédemment.</span><span class="sxs-lookup"><span data-stu-id="481e9-160">If a proxy or firewall is blocking anonymous traffic, make sure that anonymous traffic is permitted in the previously listed URLs.</span></span> <span data-ttu-id="481e9-161">Pour les proxies transparents, aucune configuration supplémentaire n’est nécessaire pour Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="481e9-161">For transparent proxies, no additional configuration is needed for Defender for Endpoint.</span></span> <span data-ttu-id="481e9-162">Pour le proxy statique, suivez les étapes de [la configuration manuelle du proxy statique.](linux-static-proxy-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="481e9-162">For static proxy, follow the steps in [Manual Static Proxy Configuration](linux-static-proxy-configuration.md).</span></span>

> [!WARNING]
> <span data-ttu-id="481e9-163">Pac, WPAD et les proxies authentifiés ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="481e9-163">PAC, WPAD, and authenticated proxies are not supported.</span></span> <span data-ttu-id="481e9-164">Assurez-vous que seul un proxy statique ou transparent est utilisé.</span><span class="sxs-lookup"><span data-stu-id="481e9-164">Ensure that only a static proxy or transparent proxy is being used.</span></span>
>
> <span data-ttu-id="481e9-165">L’inspection et l’interception des proxies SSL ne sont pas non plus pris en charge pour des raisons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="481e9-165">SSL inspection and intercepting proxies are also not supported for security reasons.</span></span> <span data-ttu-id="481e9-166">Configurez une exception pour l’inspection SSL et votre serveur proxy pour transmettre directement les données de Defender for Endpoint for Linux aux URL pertinentes sans interception.</span><span class="sxs-lookup"><span data-stu-id="481e9-166">Configure an exception for SSL inspection and your proxy server to directly pass through data from Defender for Endpoint for Linux to the relevant URLs without interception.</span></span> <span data-ttu-id="481e9-167">L’ajout de votre certificat d’interception au magasin global n’autorise pas l’interception.</span><span class="sxs-lookup"><span data-stu-id="481e9-167">Adding your interception certificate to the global store will not allow for interception.</span></span>

<span data-ttu-id="481e9-168">Pour les étapes de résolution des problèmes, voir Résoudre les problèmes de connectivité cloud pour [Microsoft Defender pour Endpoint pour Linux.](linux-support-connectivity.md)</span><span class="sxs-lookup"><span data-stu-id="481e9-168">For troubleshooting steps, see [Troubleshoot cloud connectivity issues for Microsoft Defender for Endpoint for Linux](linux-support-connectivity.md).</span></span>

## <a name="how-to-update-microsoft-defender-for-endpoint-for-linux"></a><span data-ttu-id="481e9-169">Comment mettre à jour Microsoft Defender pour endpoint pour Linux</span><span class="sxs-lookup"><span data-stu-id="481e9-169">How to update Microsoft Defender for Endpoint for Linux</span></span>

<span data-ttu-id="481e9-170">Microsoft publie régulièrement des mises à jour logicielles pour améliorer les performances, la sécurité et fournir de nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="481e9-170">Microsoft regularly publishes software updates to improve performance, security, and to deliver new features.</span></span> <span data-ttu-id="481e9-171">Pour mettre à jour Microsoft Defender pour endpoint pour Linux, reportez-vous à Déployer les mises à jour [de Microsoft Defender pour Endpoint pour Linux.](linux-updates.md)</span><span class="sxs-lookup"><span data-stu-id="481e9-171">To update Microsoft Defender for Endpoint for Linux, refer to [Deploy updates for Microsoft Defender for Endpoint for Linux](linux-updates.md).</span></span>

## <a name="how-to-configure-microsoft-defender-for-endpoint-for-linux"></a><span data-ttu-id="481e9-172">Comment configurer Microsoft Defender pour endpoint pour Linux</span><span class="sxs-lookup"><span data-stu-id="481e9-172">How to configure Microsoft Defender for Endpoint for Linux</span></span>

<span data-ttu-id="481e9-173">Des instructions sur la configuration du produit dans les environnements d’entreprise sont disponibles dans Définir les préférences de [Microsoft Defender pour Endpoint pour Linux.](linux-preferences.md)</span><span class="sxs-lookup"><span data-stu-id="481e9-173">Guidance for how to configure the product in enterprise environments is available in [Set preferences for Microsoft Defender for Endpoint for Linux](linux-preferences.md).</span></span>

## <a name="resources"></a><span data-ttu-id="481e9-174">Ressources</span><span class="sxs-lookup"><span data-stu-id="481e9-174">Resources</span></span>

- <span data-ttu-id="481e9-175">Pour plus d’informations sur la journalisation, la désinstallation ou d’autres rubriques, voir [Resources](linux-resources.md).</span><span class="sxs-lookup"><span data-stu-id="481e9-175">For more information about logging, uninstalling, or other topics, see [Resources](linux-resources.md).</span></span>
