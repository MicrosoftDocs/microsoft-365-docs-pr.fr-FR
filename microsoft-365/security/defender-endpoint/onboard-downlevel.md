---
title: Intégrer les versions précédentes de Windows sur Microsoft Defender for Endpoint
description: Intégrer les versions antérieures des appareils Windows pris en charge afin qu’ils peuvent envoyer des données de capteur au capteur Microsoft Defender for Endpoint
keywords: onboard, windows, 7, 81, oms, sp1, enterprise, pro, down level
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: d0cb4a3d01c1380f4fd06999c8f81a4054e2fd00
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52844429"
---
# <a name="onboard-previous-versions-of-windows"></a><span data-ttu-id="3ef18-104">Intégrer des versions antérieures de Windows</span><span class="sxs-lookup"><span data-stu-id="3ef18-104">Onboard previous versions of Windows</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="3ef18-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="3ef18-105">**Applies to:**</span></span>
- [<span data-ttu-id="3ef18-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="3ef18-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="3ef18-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="3ef18-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

<span data-ttu-id="3ef18-108">**Plateformes**</span><span class="sxs-lookup"><span data-stu-id="3ef18-108">**Platforms**</span></span>
- <span data-ttu-id="3ef18-109">Windows 7 SP1 Enterprise</span><span class="sxs-lookup"><span data-stu-id="3ef18-109">Windows 7 SP1 Enterprise</span></span>
- <span data-ttu-id="3ef18-110">Windows 7 SP1 Pro</span><span class="sxs-lookup"><span data-stu-id="3ef18-110">Windows 7 SP1 Pro</span></span>
- <span data-ttu-id="3ef18-111">Windows 8.1 Professionnel</span><span class="sxs-lookup"><span data-stu-id="3ef18-111">Windows 8.1 Pro</span></span>
- <span data-ttu-id="3ef18-112">Windows 8.1 Entreprise</span><span class="sxs-lookup"><span data-stu-id="3ef18-112">Windows 8.1 Enterprise</span></span>


><span data-ttu-id="3ef18-113">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="3ef18-113">Want to experience Defender for Endpoint?</span></span> <span data-ttu-id="3ef18-114">[Inscrivez-vous à une version d’essai gratuite.](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-downlevel-abovefoldlink)</span><span class="sxs-lookup"><span data-stu-id="3ef18-114">[Sign up for a free trial](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-downlevel-abovefoldlink).</span></span>

<span data-ttu-id="3ef18-115">Defender for Endpoint étend la prise en charge pour inclure des systèmes d’exploitation de bas niveau, fournissant des fonctionnalités avancées de détection d’attaques et d’investigation sur les versions Windows pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3ef18-115">Defender for Endpoint extends support to include down-level operating systems, providing advanced attack detection and investigation capabilities on supported Windows versions.</span></span>

<span data-ttu-id="3ef18-116">Pour intégrer des points de terminaison Windows client de niveau inférieur à Defender for Endpoint, vous devez :</span><span class="sxs-lookup"><span data-stu-id="3ef18-116">To onboard down-level Windows client endpoints to Defender for Endpoint, you'll need to:</span></span>
- <span data-ttu-id="3ef18-117">Configurez et mettez à jour System Center Endpoint Protection clients.</span><span class="sxs-lookup"><span data-stu-id="3ef18-117">Configure and update System Center Endpoint Protection clients.</span></span>
- <span data-ttu-id="3ef18-118">Installez et configurez Microsoft Monitoring Agent (MMA) pour signaler les données de capteur à Defender for Endpoint comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="3ef18-118">Install and configure Microsoft Monitoring Agent (MMA) to report sensor data to Defender for Endpoint as instructed below.</span></span>

> [!TIP]
> <span data-ttu-id="3ef18-119">Après avoir intégré l’appareil, vous pouvez choisir d’exécuter un test de détection pour vérifier qu’il est correctement intégré au service.</span><span class="sxs-lookup"><span data-stu-id="3ef18-119">After onboarding the device, you can choose to run a detection test to verify that it is properly onboarded to the service.</span></span> <span data-ttu-id="3ef18-120">Pour plus d’informations, voir Exécuter un test de détection sur un point de terminaison [Defender pour point de terminaison nouvellement intégré.](run-detection-test.md)</span><span class="sxs-lookup"><span data-stu-id="3ef18-120">For more information, see [Run a detection test on a newly onboarded Defender for Endpoint endpoint](run-detection-test.md).</span></span>

## <a name="configure-and-update-system-center-endpoint-protection-clients"></a><span data-ttu-id="3ef18-121">Configurer et mettre à jour System Center Endpoint Protection clients</span><span class="sxs-lookup"><span data-stu-id="3ef18-121">Configure and update System Center Endpoint Protection clients</span></span>
> [!IMPORTANT]
> <span data-ttu-id="3ef18-122">Cette étape est requise uniquement si votre organisation utilise System Center Endpoint Protection (SCEP).</span><span class="sxs-lookup"><span data-stu-id="3ef18-122">This step is required only if your organization uses System Center Endpoint Protection (SCEP).</span></span>

<span data-ttu-id="3ef18-123">Defender pour le point de terminaison s’intègre à System Center Endpoint Protection pour fournir une visibilité aux détections de programmes malveillants et pour arrêter la propagation d’une attaque dans votre organisation en interdit les fichiers potentiellement malveillants ou les programmes malveillants suspects.</span><span class="sxs-lookup"><span data-stu-id="3ef18-123">Defender for Endpoint integrates with System Center Endpoint Protection to provide visibility to malware detections and to stop propagation of an attack in your organization by banning potentially malicious files or suspected malware.</span></span> 

<span data-ttu-id="3ef18-124">Les étapes suivantes sont nécessaires pour activer cette intégration :</span><span class="sxs-lookup"><span data-stu-id="3ef18-124">The following steps are required to enable this integration:</span></span> 
- <span data-ttu-id="3ef18-125">Installer la mise à jour de la plateforme anti-programme malveillant de janvier [2017 Endpoint Protection clients](https://support.microsoft.com/help/3209361/january-2017-anti-malware-platform-update-for-endpoint-protection-clie)</span><span class="sxs-lookup"><span data-stu-id="3ef18-125">Install the [January 2017 anti-malware platform update for Endpoint Protection clients](https://support.microsoft.com/help/3209361/january-2017-anti-malware-platform-update-for-endpoint-protection-clie)</span></span> 
- <span data-ttu-id="3ef18-126">Configurer l’appartenance au service protection cloud client SCEP sur le **paramètre** Avancé</span><span class="sxs-lookup"><span data-stu-id="3ef18-126">Configure the SCEP client Cloud Protection Service membership to the **Advanced** setting</span></span>
- <span data-ttu-id="3ef18-127">Configurez votre réseau pour autoriser les connexions au Antivirus Microsoft Defender cloud.</span><span class="sxs-lookup"><span data-stu-id="3ef18-127">Configure your network to allow connections to the Microsoft Defender Antivirus cloud.</span></span> <span data-ttu-id="3ef18-128">Pour plus d’informations, voir [Autoriser les connexions au Antivirus Microsoft Defender cloud](/windows/security/threat-protection/microsoft-defender-antivirus/configure-network-connections-microsoft-defender-antivirus#allow-connections-to-the-microsoft-defender-antivirus-cloud)</span><span class="sxs-lookup"><span data-stu-id="3ef18-128">For more information, see [Allow connections to the Microsoft Defender Antivirus cloud](/windows/security/threat-protection/microsoft-defender-antivirus/configure-network-connections-microsoft-defender-antivirus#allow-connections-to-the-microsoft-defender-antivirus-cloud)</span></span>

## <a name="install-and-configure-microsoft-monitoring-agent-mma-to-report-sensor-data-to-microsoft-defender-for-endpoint"></a><span data-ttu-id="3ef18-129">Installer et configurer Microsoft Monitoring Agent (MMA) pour signaler les données de capteur à Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="3ef18-129">Install and configure Microsoft Monitoring Agent (MMA) to report sensor data to Microsoft Defender for Endpoint</span></span>

### <a name="before-you-begin"></a><span data-ttu-id="3ef18-130">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="3ef18-130">Before you begin</span></span>
<span data-ttu-id="3ef18-131">Examinez les détails suivants pour vérifier la minimale requise :</span><span class="sxs-lookup"><span data-stu-id="3ef18-131">Review the following details to verify minimum system requirements:</span></span>
- <span data-ttu-id="3ef18-132">Installer le rapport de mise à jour mensuelle de [février 2018](https://support.microsoft.com/help/4074598/windows-7-update-kb4074598)</span><span class="sxs-lookup"><span data-stu-id="3ef18-132">Install the [February 2018 monthly update rollup](https://support.microsoft.com/help/4074598/windows-7-update-kb4074598)</span></span>
  
  > [!NOTE]
  > <span data-ttu-id="3ef18-133">Applicable uniquement pour Windows 7 SP1 Enterprise et Windows 7 SP1 Pro.</span><span class="sxs-lookup"><span data-stu-id="3ef18-133">Only applicable for Windows 7 SP1 Enterprise and Windows 7 SP1 Pro.</span></span> 

- <span data-ttu-id="3ef18-134">Installer la mise [à jour pour la télémétrie d’expérience client et de diagnostic](https://support.microsoft.com/help/3080149/update-for-customer-experience-and-diagnostic-telemetry)</span><span class="sxs-lookup"><span data-stu-id="3ef18-134">Install the [Update for customer experience and diagnostic telemetry](https://support.microsoft.com/help/3080149/update-for-customer-experience-and-diagnostic-telemetry)</span></span>

- <span data-ttu-id="3ef18-135">Installer [.NET Framework 4.5](https://www.microsoft.com/download/details.aspx?id=30653) (ou ultérieur) ou [KB3154518](https://support.microsoft.com/help/3154518/support-for-tls-system-default-versions-included-in-the-net-framework)</span><span class="sxs-lookup"><span data-stu-id="3ef18-135">Install either [.NET framework 4.5](https://www.microsoft.com/download/details.aspx?id=30653) (or later) or [KB3154518](https://support.microsoft.com/help/3154518/support-for-tls-system-default-versions-included-in-the-net-framework)</span></span>

    > [!NOTE]
    > <span data-ttu-id="3ef18-136">Applicable uniquement pour Windows 7 SP1 Enterprise et Windows 7 SP1 Pro.</span><span class="sxs-lookup"><span data-stu-id="3ef18-136">Only applicable for Windows 7 SP1 Enterprise and Windows 7 SP1 Pro.</span></span>
    > <span data-ttu-id="3ef18-137">N’installez pas .NET Framework 4.0.x, car cela va annuler l’installation ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="3ef18-137">Don't install .NET Framework 4.0.x, since it will negate the above installation.</span></span>

- <span data-ttu-id="3ef18-138">Respectez la taille minimale requise de l’agent Azure Log Analytics.</span><span class="sxs-lookup"><span data-stu-id="3ef18-138">Meet the Azure Log Analytics agent minimum system requirements.</span></span> <span data-ttu-id="3ef18-139">Pour plus d’informations, voir [Collecter des données à partir d’ordinateurs](/azure/log-analytics/log-analytics-concept-hybrid#prerequisites)de votre environnement avec Log Analytics.</span><span class="sxs-lookup"><span data-stu-id="3ef18-139">For more information, see [Collect data from computers in your environment with Log Analytics](/azure/log-analytics/log-analytics-concept-hybrid#prerequisites).</span></span>



1. <span data-ttu-id="3ef18-140">Téléchargez le fichier de configuration de [l’agent : Windows agent 64 bits](https://go.microsoft.com/fwlink/?LinkId=828603) ou Windows agent [32 bits.](https://go.microsoft.com/fwlink/?LinkId=828604)</span><span class="sxs-lookup"><span data-stu-id="3ef18-140">Download the agent setup file: [Windows 64-bit agent](https://go.microsoft.com/fwlink/?LinkId=828603) or [Windows 32-bit agent](https://go.microsoft.com/fwlink/?LinkId=828604).</span></span>

2. <span data-ttu-id="3ef18-141">Obtenez l’ID d’espace de travail :</span><span class="sxs-lookup"><span data-stu-id="3ef18-141">Obtain the workspace ID:</span></span>
   - <span data-ttu-id="3ef18-142">Dans le volet de navigation Defender pour les points de terminaison, sélectionnez Paramètres > gestion des > **l’intégration**</span><span class="sxs-lookup"><span data-stu-id="3ef18-142">In the Defender for Endpoint navigation pane, select **Settings > Device management > Onboarding**</span></span>
   - <span data-ttu-id="3ef18-143">Sélectionnez **Windows 7 SP1 et 8.1 comme** système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="3ef18-143">Select **Windows 7 SP1 and 8.1** as the operating system</span></span>
   - <span data-ttu-id="3ef18-144">Copier l’ID d’espace de travail et la clé d’espace de travail</span><span class="sxs-lookup"><span data-stu-id="3ef18-144">Copy the workspace ID and workspace key</span></span>

3. <span data-ttu-id="3ef18-145">À l’aide de l’ID d’espace de travail et de la clé d’espace de travail, choisissez l’une des méthodes d’installation suivantes pour installer l’agent :</span><span class="sxs-lookup"><span data-stu-id="3ef18-145">Using the Workspace ID and Workspace key choose any of the following installation methods to install the agent:</span></span>
    - <span data-ttu-id="3ef18-146">[Installez manuellement l’agent à l’aide du programme d’installation.](/azure/log-analytics/log-analytics-windows-agents#install-agent-using-setup-wizard)</span><span class="sxs-lookup"><span data-stu-id="3ef18-146">[Manually install the agent using setup](/azure/log-analytics/log-analytics-windows-agents#install-agent-using-setup-wizard).</span></span> <br>
      <span data-ttu-id="3ef18-147">Dans la page **Options de configuration** de l’agent, **sélectionnez Connecter l’agent dans Azure Log Analytics (OMS)**</span><span class="sxs-lookup"><span data-stu-id="3ef18-147">On the **Agent Setup Options** page, select **Connect the agent to Azure Log Analytics (OMS)**</span></span>
    - <span data-ttu-id="3ef18-148">[Installez l’agent à l’aide de la ligne de commande.](/azure/log-analytics/log-analytics-windows-agents#install-agent-using-command-line)</span><span class="sxs-lookup"><span data-stu-id="3ef18-148">[Install the agent using the command line](/azure/log-analytics/log-analytics-windows-agents#install-agent-using-command-line).</span></span>
    - <span data-ttu-id="3ef18-149">[Configurez l’agent à l’aide d’un script.](/azure/log-analytics/log-analytics-windows-agents#install-agent-using-dsc-in-azure-automation)</span><span class="sxs-lookup"><span data-stu-id="3ef18-149">[Configure the agent using a script](/azure/log-analytics/log-analytics-windows-agents#install-agent-using-dsc-in-azure-automation).</span></span>

   > [!NOTE]
   > <span data-ttu-id="3ef18-150">Si vous [](gov.md)êtes un client du gouvernement des États-Unis, sous « Azure Cloud », vous devez choisir « Azure US Government » si vous utilisez l’Assistant Installation, ou si vous utilisez une ligne de commande ou un script , définissez le paramètre « OPINSIGHTS_WORKSPACE_AZURE_CLOUD_TYPE » sur 1.</span><span class="sxs-lookup"><span data-stu-id="3ef18-150">If you are a [US Government customer](gov.md), under "Azure Cloud" you'll need to choose "Azure US Government" if using the setup wizard, or if using a command line or a script - set the "OPINSIGHTS_WORKSPACE_AZURE_CLOUD_TYPE" parameter to 1.</span></span>

4. <span data-ttu-id="3ef18-151">Si vous utilisez un proxy pour vous connecter à Internet, consultez la section Configurer les paramètres du proxy.</span><span class="sxs-lookup"><span data-stu-id="3ef18-151">If you're using a proxy to connect to the Internet see the Configure proxy settings section.</span></span>

<span data-ttu-id="3ef18-152">Une fois terminé, vous devriez voir les points de terminaison intégrés dans le portail dans un délai d’une heure.</span><span class="sxs-lookup"><span data-stu-id="3ef18-152">Once completed, you should see onboarded endpoints in the portal within an hour.</span></span>

### <a name="configure-proxy-and-internet-connectivity-settings"></a><span data-ttu-id="3ef18-153">Configurer les paramètres de proxy et de connectivité Internet</span><span class="sxs-lookup"><span data-stu-id="3ef18-153">Configure proxy and Internet connectivity settings</span></span>
 
- <span data-ttu-id="3ef18-154">Chaque Windows point de terminaison doit pouvoir se connecter à Internet à l’aide du protocole HTTPS.</span><span class="sxs-lookup"><span data-stu-id="3ef18-154">Each Windows endpoint must be able to connect to the Internet using HTTPS.</span></span> <span data-ttu-id="3ef18-155">Cette connexion peut être directe, à l’aide d’un proxy ou via la [passerelle OMS.](/azure/log-analytics/log-analytics-oms-gateway)</span><span class="sxs-lookup"><span data-stu-id="3ef18-155">This connection can be direct, using a proxy, or through the [OMS Gateway](/azure/log-analytics/log-analytics-oms-gateway).</span></span>
- <span data-ttu-id="3ef18-156">Si un proxy ou un pare-feu bloque tout le trafic par défaut et n’autorise que des domaines spécifiques ou que l’analyse HTTPS (inspection SSL) est activée, assurez-vous d’activer l’accès aux URL du [service Defender for Endpoint.](/microsoft-365/security/defender-endpoint/configure-proxy-internet#enable-access-to-microsoft-defender-atp-service-urls-in-the-proxy-server)</span><span class="sxs-lookup"><span data-stu-id="3ef18-156">If a proxy or firewall is blocking all traffic by default and allowing only specific domains through or HTTPS scanning (SSL inspection) is enabled, make sure that you [enable access to Defender for Endpoint service URLs](/microsoft-365/security/defender-endpoint/configure-proxy-internet#enable-access-to-microsoft-defender-atp-service-urls-in-the-proxy-server).</span></span>

## <a name="offboard-client-endpoints"></a><span data-ttu-id="3ef18-157">Points de terminaison du client de hors-carte</span><span class="sxs-lookup"><span data-stu-id="3ef18-157">Offboard client endpoints</span></span>
<span data-ttu-id="3ef18-158">Pour désinstaller, vous pouvez désinstaller l’agent MMA du point de terminaison ou le détacher des rapports à votre espace de travail Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="3ef18-158">To offboard, you can uninstall the MMA agent from the endpoint or detach it from reporting to your Defender for Endpoint workspace.</span></span> <span data-ttu-id="3ef18-159">Après l’arrêt de l’agent, le point de terminaison n’envoie plus de données de capteur à Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="3ef18-159">After offboarding the agent, the endpoint will no longer send sensor data to Defender for Endpoint.</span></span> 

> <span data-ttu-id="3ef18-160">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="3ef18-160">Want to experience Defender for Endpoint?</span></span> <span data-ttu-id="3ef18-161">[Inscrivez-vous à une version d’essai gratuite.](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-downlevele-belowfoldlink)</span><span class="sxs-lookup"><span data-stu-id="3ef18-161">[Sign up for a free trial](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-downlevele-belowfoldlink).</span></span>
