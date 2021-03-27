---
title: Intégrer des serveurs Windows au service Microsoft Defender for Endpoint
description: Intégrer des serveurs Windows afin qu’ils peuvent envoyer des données de capteur au capteur Microsoft Defender for Endpoint.
keywords: onboard server, server, 2012r2, 2016, 2019, server onboarding, device management, configure Windows ATP servers, onboard Microsoft Defender for Endpoint servers, onboard Microsoft Defender for Endpoint servers
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
author: mjcaparas
ms.author: macapara
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 5013d94277eeba7d1df100d2850cb950fe2e0742
ms.sourcegitcommit: a965c498e6b3890877f895d5197898b306092813
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2021
ms.locfileid: "51379348"
---
# <a name="onboard-windows-servers-to-the-microsoft-defender-for-endpoint-service"></a><span data-ttu-id="2678b-104">Intégrer des serveurs Windows au service Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="2678b-104">Onboard Windows servers to the Microsoft Defender for Endpoint service</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="2678b-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="2678b-105">**Applies to:**</span></span>

- <span data-ttu-id="2678b-106">Windows Server 2008 R2 SP1</span><span class="sxs-lookup"><span data-stu-id="2678b-106">Windows Server 2008 R2 SP1</span></span>
- <span data-ttu-id="2678b-107">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="2678b-107">Windows Server 2012 R2</span></span>
- <span data-ttu-id="2678b-108">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2678b-108">Windows Server 2016</span></span>
- <span data-ttu-id="2678b-109">Windows Server (SAC) version 1803 et ultérieure</span><span class="sxs-lookup"><span data-stu-id="2678b-109">Windows Server (SAC) version 1803 and later</span></span>
- <span data-ttu-id="2678b-110">Windows Server 2019 et les ultérieures</span><span class="sxs-lookup"><span data-stu-id="2678b-110">Windows Server 2019 and later</span></span>
- <span data-ttu-id="2678b-111">Édition principale de Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="2678b-111">Windows Server 2019 core edition</span></span>

> <span data-ttu-id="2678b-112">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="2678b-112">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="2678b-113">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="2678b-113">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-configserver-abovefoldlink)


<span data-ttu-id="2678b-114">Defender for Endpoint étend la prise en charge pour inclure également le système d’exploitation Windows Server.</span><span class="sxs-lookup"><span data-stu-id="2678b-114">Defender for Endpoint extends support to also include the Windows Server operating system.</span></span> <span data-ttu-id="2678b-115">Cette prise en charge offre des fonctionnalités avancées de détection d’attaques et d’examens en toute transparence via la console du Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="2678b-115">This support provides advanced attack detection and investigation capabilities seamlessly through the Microsoft Defender Security Center console.</span></span>

<span data-ttu-id="2678b-116">Pour obtenir des conseils pratiques sur ce qui doit être en place pour la gestion des licences et l’infrastructure, voir Protection des serveurs [Windows avec Defender pour Endpoint](https://techcommunity.microsoft.com/t5/What-s-New/Protecting-Windows-Server-with-Windows-Defender-ATP/m-p/267114#M128).</span><span class="sxs-lookup"><span data-stu-id="2678b-116">For a practical guidance on what needs to be in place for licensing and infrastructure, see [Protecting Windows Servers with Defender for Endpoint](https://techcommunity.microsoft.com/t5/What-s-New/Protecting-Windows-Server-with-Windows-Defender-ATP/m-p/267114#M128).</span></span>

<span data-ttu-id="2678b-117">Pour obtenir des instructions sur la façon de télécharger et d’utiliser les lignes de base de sécurité Windows pour les serveurs Windows, voir Lignes de base de sécurité [Windows.](https://docs.microsoft.com/windows/device-security/windows-security-baselines)</span><span class="sxs-lookup"><span data-stu-id="2678b-117">For guidance on how to download and use Windows Security Baselines for Windows servers, see [Windows Security Baselines](https://docs.microsoft.com/windows/device-security/windows-security-baselines).</span></span>

<br>

## <a name="windows-server-2008-r2-sp1-windows-server-2012-r2-and-windows-server-2016"></a><span data-ttu-id="2678b-118">Windows Server 2008 R2 SP1, Windows Server 2012 R2 et Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2678b-118">Windows Server 2008 R2 SP1, Windows Server 2012 R2, and Windows Server 2016</span></span>

<span data-ttu-id="2678b-119">Vous pouvez intégrer Windows Server 2008 R2 SP1, Windows Server 2012 R2 et Windows Server 2016 à Defender for Endpoint en utilisant l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="2678b-119">You can onboard Windows Server 2008 R2 SP1, Windows Server 2012 R2, and Windows Server 2016 to Defender for Endpoint by using any of the following options:</span></span>

- <span data-ttu-id="2678b-120">**Option 1 :** intégrer [en installant et en configurant l’Agent de surveillance Microsoft (MMA)](#option-1-onboard-by-installing-and-configuring-microsoft-monitoring-agent-mma)</span><span class="sxs-lookup"><span data-stu-id="2678b-120">**Option 1**: [Onboard by installing and configuring Microsoft Monitoring Agent (MMA)](#option-1-onboard-by-installing-and-configuring-microsoft-monitoring-agent-mma)</span></span>
- <span data-ttu-id="2678b-121">**Option 2 :** intégration [via le Centre de sécurité Azure](#option-2-onboard-windows-servers-through-azure-security-center)</span><span class="sxs-lookup"><span data-stu-id="2678b-121">**Option 2**: [Onboard through Azure Security Center](#option-2-onboard-windows-servers-through-azure-security-center)</span></span>
- <span data-ttu-id="2678b-122">**Option 3 :** [intégration via Microsoft Endpoint Manager version 2002 et ultérieure](#option-3-onboard-windows-servers-through-microsoft-endpoint-manager-version-2002-and-later)</span><span class="sxs-lookup"><span data-stu-id="2678b-122">**Option 3**: [Onboard through Microsoft Endpoint Manager version 2002 and later](#option-3-onboard-windows-servers-through-microsoft-endpoint-manager-version-2002-and-later)</span></span>


<span data-ttu-id="2678b-123">Après avoir effectué les étapes d’intégration à l’aide de l’une des options fournies, vous devez configurer et mettre à jour [les clients System Center Endpoint Protection](#configure-and-update-system-center-endpoint-protection-clients).</span><span class="sxs-lookup"><span data-stu-id="2678b-123">After completing the onboarding steps using any of the provided options, you'll need to [Configure and update System Center Endpoint Protection clients](#configure-and-update-system-center-endpoint-protection-clients).</span></span>


> [!NOTE]
> <span data-ttu-id="2678b-124">La licence de serveur autonome Defender pour les points de terminaison est requise, par nœud, pour intégrer un serveur Windows via l’Agent de surveillance Microsoft (option 1) ou par le biais de Microsoft Endpoint Manager (option 3).</span><span class="sxs-lookup"><span data-stu-id="2678b-124">Defender for Endpoint standalone server license is required, per node, in order to onboard a Windows server through Microsoft Monitoring Agent (Option 1), or through Microsoft Endpoint Manager (Option 3).</span></span> <span data-ttu-id="2678b-125">Une licence Azure Defender pour les serveurs est également requise, par nœud, pour intégrer un serveur Windows via Azure Security Center (option 2), voir fonctionnalités prise en charge disponibles dans le Centre de sécurité [Azure.](https://docs.microsoft.com/azure/security-center/security-center-services)</span><span class="sxs-lookup"><span data-stu-id="2678b-125">Alternatively, an Azure Defender for Servers license is required, per node, in order to onboard a Windows server through Azure Security Center (Option 2), see [Supported features available in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-services).</span></span>


### <a name="option-1-onboard-by-installing-and-configuring-microsoft-monitoring-agent-mma"></a><span data-ttu-id="2678b-126">Option 1 : intégrer en installant et en configurant l’Agent de surveillance Microsoft (MMA)</span><span class="sxs-lookup"><span data-stu-id="2678b-126">Option 1: Onboard by installing and configuring Microsoft Monitoring Agent (MMA)</span></span>
<span data-ttu-id="2678b-127">Vous devez installer et configurer MMA pour que les serveurs Windows signalent les données de capteur à Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="2678b-127">You'll need to install and configure MMA for Windows servers to report sensor data to Defender for Endpoint.</span></span> <span data-ttu-id="2678b-128">Pour plus d’informations, voir [Collecter les données du journal avec l’agent Azure Log Analytics.](https://docs.microsoft.com/azure/azure-monitor/platform/log-analytics-agent)</span><span class="sxs-lookup"><span data-stu-id="2678b-128">For more information, see [Collect log data with Azure Log Analytics agent](https://docs.microsoft.com/azure/azure-monitor/platform/log-analytics-agent).</span></span>

<span data-ttu-id="2678b-129">Si vous utilisez déjà System Center Operations Manager (SCOM) ou Azure Monitor (anciennement Operations Management Suite (OMS), attachez l’agent de surveillance Microsoft (MMA) pour signaler à votre espace de travail Defender for Endpoint par le biais de la prise en charge multi-accueil.</span><span class="sxs-lookup"><span data-stu-id="2678b-129">If you're already using System Center Operations Manager (SCOM) or Azure Monitor (formerly known as Operations Management Suite (OMS)), attach the Microsoft Monitoring Agent (MMA) to report to your Defender for Endpoint workspace through Multihoming support.</span></span>

<span data-ttu-id="2678b-130">En règle générale, vous devez suivre les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="2678b-130">In general, you'll need to take the following steps:</span></span>
1. <span data-ttu-id="2678b-131">Remplissez les conditions d’intégration décrites dans la section **Avant de commencer.**</span><span class="sxs-lookup"><span data-stu-id="2678b-131">Fulfill the onboarding requirements outlined in **Before you begin** section.</span></span>
2. <span data-ttu-id="2678b-132">Activer la surveillance du serveur à partir du Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="2678b-132">Turn on server monitoring from Microsoft Defender Security center.</span></span>
3. <span data-ttu-id="2678b-133">Installez et configurez MMA pour le serveur afin de signaler les données de capteur à Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="2678b-133">Install and configure MMA for the server to report sensor data to Defender for Endpoint.</span></span>
4. <span data-ttu-id="2678b-134">Configurez et mettez à jour les clients System Center Endpoint Protection.</span><span class="sxs-lookup"><span data-stu-id="2678b-134">Configure and update System Center Endpoint Protection clients.</span></span>


> [!TIP]
> <span data-ttu-id="2678b-135">Après avoir intégré l’appareil, vous pouvez choisir d’exécuter un test de détection pour vérifier qu’il est correctement intégré au service.</span><span class="sxs-lookup"><span data-stu-id="2678b-135">After onboarding the device, you can choose to run a detection test to verify that it is properly onboarded to the service.</span></span> <span data-ttu-id="2678b-136">Pour plus d’informations, voir Exécuter un test de détection sur un point de terminaison [Defender pour point de terminaison nouvellement intégré.](run-detection-test.md)</span><span class="sxs-lookup"><span data-stu-id="2678b-136">For more information, see [Run a detection test on a newly onboarded Defender for Endpoint endpoint](run-detection-test.md).</span></span>


#### <a name="before-you-begin"></a><span data-ttu-id="2678b-137">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="2678b-137">Before you begin</span></span> 
<span data-ttu-id="2678b-138">Pour répondre aux exigences d’intégration, effectuez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="2678b-138">Perform the following steps to fulfill the onboarding requirements:</span></span>

 - <span data-ttu-id="2678b-139">Pour Windows Server 2008 R2 SP1 ou Windows Server 2012 R2, assurez-vous d’installer le correctif logiciel suivant :</span><span class="sxs-lookup"><span data-stu-id="2678b-139">For Windows Server 2008 R2 SP1 or Windows Server 2012 R2, ensure that you install the following hotfix:</span></span>
    - [<span data-ttu-id="2678b-140">Mise à jour pour la télémétrie d’expérience client et de diagnostic</span><span class="sxs-lookup"><span data-stu-id="2678b-140">Update for customer experience and diagnostic telemetry</span></span>](https://support.microsoft.com/help/3080149/update-for-customer-experience-and-diagnostic-telemetry)

 - <span data-ttu-id="2678b-141">En outre, pour Windows Server 2008 R2 SP1, assurez-vous que vous remplissez les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="2678b-141">In addition, for Windows Server 2008 R2 SP1, ensure that you fulfill the following requirements:</span></span>
    - <span data-ttu-id="2678b-142">Installer le rapport de [mise à jour mensuelle de février](https://support.microsoft.com/help/4074598/windows-7-update-kb4074598)</span><span class="sxs-lookup"><span data-stu-id="2678b-142">Install the [February monthly update rollup](https://support.microsoft.com/help/4074598/windows-7-update-kb4074598)</span></span>
    - <span data-ttu-id="2678b-143">Installer [.NET Framework 4.5](https://www.microsoft.com/download/details.aspx?id=30653) (ou ultérieur) ou [KB3154518](https://support.microsoft.com/help/3154518/support-for-tls-system-default-versions-included-in-the-net-framework)</span><span class="sxs-lookup"><span data-stu-id="2678b-143">Install either [.NET framework 4.5](https://www.microsoft.com/download/details.aspx?id=30653) (or later) or [KB3154518](https://support.microsoft.com/help/3154518/support-for-tls-system-default-versions-included-in-the-net-framework)</span></span>
   
   > [!NOTE]
    > <span data-ttu-id="2678b-144">Si vous gérez votre Windows Server 2008 R2 SP1 avec SCCM, l’agent client SCCM installe .Net Framework 4.5.2.</span><span class="sxs-lookup"><span data-stu-id="2678b-144">If you are managing your Windows Server 2008 R2 SP1 with SCCM, the SCCM client agent installs .Net Framework 4.5.2.</span></span> <span data-ttu-id="2678b-145">Vous n’avez donc pas besoin d’installer .NET Framework 4.5 (ou une ultérieure).</span><span class="sxs-lookup"><span data-stu-id="2678b-145">So you don't need to install the .NET framework 4.5 (or later).</span></span>
   
 - <span data-ttu-id="2678b-146">Pour Windows Server 2008 R2 SP1 et Windows Server 2012 R2 : configurez et mettez à jour [les clients System Center Endpoint Protection](#configure-and-update-system-center-endpoint-protection-clients).</span><span class="sxs-lookup"><span data-stu-id="2678b-146">For Windows Server 2008 R2 SP1 and Windows Server 2012 R2: [Configure and update System Center Endpoint Protection clients](#configure-and-update-system-center-endpoint-protection-clients).</span></span>

    > [!NOTE]
    > <span data-ttu-id="2678b-147">Cette étape est requise uniquement si votre organisation utilise System Center Endpoint Protection (SCEP) et que vous intégrerEz Windows Server 2008 R2 SP1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="2678b-147">This step is required only if your organization uses System Center Endpoint Protection (SCEP) and you're onboarding Windows Server 2008 R2 SP1 and Windows Server 2012 R2.</span></span>


<span id="server-mma"/>

### <a name="install-and-configure-microsoft-monitoring-agent-mma-to-report-sensor-data-to-microsoft-defender-for-endpoint"></a><span data-ttu-id="2678b-148">Installer et configurer l’Agent de surveillance Microsoft (MMA) pour signaler les données de capteur à Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="2678b-148">Install and configure Microsoft Monitoring Agent (MMA) to report sensor data to Microsoft Defender for Endpoint</span></span>

1. <span data-ttu-id="2678b-149">Téléchargez le fichier d’installation de [l’agent : Agent Windows 64 bits.](https://go.microsoft.com/fwlink/?LinkId=828603)</span><span class="sxs-lookup"><span data-stu-id="2678b-149">Download the agent setup file: [Windows 64-bit agent](https://go.microsoft.com/fwlink/?LinkId=828603).</span></span>

2. <span data-ttu-id="2678b-150">À l’aide de l’ID d’espace de travail et de la clé d’espace de travail obtenus dans la procédure précédente, choisissez l’une des méthodes d’installation suivantes pour installer l’agent sur le serveur Windows :</span><span class="sxs-lookup"><span data-stu-id="2678b-150">Using the Workspace ID and Workspace key obtained in the previous procedure, choose any of the following installation methods to install the agent on the Windows server:</span></span>
    - <span data-ttu-id="2678b-151">[Installez manuellement l’agent à l’aide du programme d’installation.](https://docs.microsoft.com/azure/log-analytics/log-analytics-windows-agents#install-agent-using-setup-wizard)</span><span class="sxs-lookup"><span data-stu-id="2678b-151">[Manually install the agent using setup](https://docs.microsoft.com/azure/log-analytics/log-analytics-windows-agents#install-agent-using-setup-wizard).</span></span> <br>
    <span data-ttu-id="2678b-152">Dans la page **Options de configuration de** l’agent, **sélectionnez Connecter l’agent à Azure Log Analytics (OMS).**</span><span class="sxs-lookup"><span data-stu-id="2678b-152">On the **Agent Setup Options** page, choose **Connect the agent to Azure Log Analytics (OMS)**.</span></span>
    - <span data-ttu-id="2678b-153">[Installez l’agent à l’aide de la ligne de commande.](https://docs.microsoft.com/azure/log-analytics/log-analytics-windows-agents#install-agent-using-command-line)</span><span class="sxs-lookup"><span data-stu-id="2678b-153">[Install the agent using the command line](https://docs.microsoft.com/azure/log-analytics/log-analytics-windows-agents#install-agent-using-command-line).</span></span>
    - <span data-ttu-id="2678b-154">[Configurez l’agent à l’aide d’un script.](https://docs.microsoft.com/azure/log-analytics/log-analytics-windows-agents#install-agent-using-dsc-in-azure-automation)</span><span class="sxs-lookup"><span data-stu-id="2678b-154">[Configure the agent using a script](https://docs.microsoft.com/azure/log-analytics/log-analytics-windows-agents#install-agent-using-dsc-in-azure-automation).</span></span>

> [!NOTE]
> <span data-ttu-id="2678b-155">Si vous [](gov.md)êtes un client du gouvernement des États-Unis, sous « Azure Cloud », vous devez choisir « Azure US Government » si vous utilisez l’Assistant Installation, ou si vous utilisez une ligne de commande ou un script , définissez le paramètre « OPINSIGHTS_WORKSPACE_AZURE_CLOUD_TYPE » sur 1.</span><span class="sxs-lookup"><span data-stu-id="2678b-155">If you are a [US Government customer](gov.md), under "Azure Cloud" you'll need to choose "Azure US Government" if using the setup wizard, or if using a command line or a script - set the "OPINSIGHTS_WORKSPACE_AZURE_CLOUD_TYPE" parameter to 1.</span></span>


<span id="server-proxy"/>

### <a name="configure-windows-server-proxy-and-internet-connectivity-settings-if-needed"></a><span data-ttu-id="2678b-156">Configurer les paramètres de proxy de serveur Windows et de connectivité Internet si nécessaire</span><span class="sxs-lookup"><span data-stu-id="2678b-156">Configure Windows server proxy and Internet connectivity settings if needed</span></span>
<span data-ttu-id="2678b-157">Si vos serveurs doivent utiliser un proxy pour communiquer avec Defender pour le point de terminaison, utilisez l’une des méthodes suivantes pour configurer MMA afin qu’il utilise le serveur proxy :</span><span class="sxs-lookup"><span data-stu-id="2678b-157">If your servers need to use a proxy to communicate with Defender for Endpoint, use one of the following methods to configure the MMA to use the proxy server:</span></span>


- [<span data-ttu-id="2678b-158">Configurer MMA pour utiliser un serveur proxy</span><span class="sxs-lookup"><span data-stu-id="2678b-158">Configure the MMA to use a proxy server</span></span>](https://docs.microsoft.com/azure/azure-monitor/platform/agent-windows#install-agent-using-setup-wizard)

- [<span data-ttu-id="2678b-159">Configurer Windows pour utiliser un serveur proxy pour toutes les connexions</span><span class="sxs-lookup"><span data-stu-id="2678b-159">Configure Windows to use a proxy server for all connections</span></span>](configure-proxy-internet.md)

<span data-ttu-id="2678b-160">Si un proxy ou un pare-feu est en cours d’utilisation, assurez-vous que les serveurs peuvent accéder à toutes les URL du service Microsoft Defender for Endpoint directement et sans interception SSL.</span><span class="sxs-lookup"><span data-stu-id="2678b-160">If a proxy or firewall is in use, please ensure that servers can access all of the Microsoft Defender for Endpoint service URLs directly and without SSL interception.</span></span> <span data-ttu-id="2678b-161">Pour plus d’informations, voir [activer l’accès aux URL du service Defender for Endpoint.](configure-proxy-internet.md#enable-access-to-microsoft-defender-for-endpoint-service-urls-in-the-proxy-server)</span><span class="sxs-lookup"><span data-stu-id="2678b-161">For more information, see [enable access to Defender for Endpoint service URLs](configure-proxy-internet.md#enable-access-to-microsoft-defender-for-endpoint-service-urls-in-the-proxy-server).</span></span> <span data-ttu-id="2678b-162">L’utilisation de l’interception SSL empêche le système de communiquer avec le service Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="2678b-162">Use of SSL interception will prevent the system from communicating with the Defender for Endpoint service.</span></span> 

<span data-ttu-id="2678b-163">Une fois terminé, vous devriez voir les serveurs Windows intégrés dans le portail dans un délai d’une heure.</span><span class="sxs-lookup"><span data-stu-id="2678b-163">Once completed, you should see onboarded Windows servers in the portal within an hour.</span></span>

### <a name="option-2-onboard-windows-servers-through-azure-security-center"></a><span data-ttu-id="2678b-164">Option 2 : intégrer des serveurs Windows via le Centre de sécurité Azure</span><span class="sxs-lookup"><span data-stu-id="2678b-164">Option 2: Onboard Windows servers through Azure Security Center</span></span>
1. <span data-ttu-id="2678b-165">Dans le volet de navigation du Centre de sécurité Microsoft Defender, sélectionnez **Paramètres** Intégration de  >  **la gestion**  >  **des appareils.**</span><span class="sxs-lookup"><span data-stu-id="2678b-165">In the Microsoft Defender Security Center navigation pane, select **Settings** > **Device management** > **Onboarding**.</span></span>

2. <span data-ttu-id="2678b-166">Sélectionnez **Windows Server 2008 R2 SP1, 2012 R2 et 2016** comme système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="2678b-166">Select **Windows Server 2008 R2 SP1, 2012 R2 and 2016** as the operating system.</span></span>

3. <span data-ttu-id="2678b-167">Cliquez **sur Serveurs intégrés dans le Centre de sécurité Azure.**</span><span class="sxs-lookup"><span data-stu-id="2678b-167">Click **Onboard Servers in Azure Security Center**.</span></span>

4. <span data-ttu-id="2678b-168">Suivez les instructions d’intégration dans [Microsoft Defender pour point de](https://docs.microsoft.com/azure/security-center/security-center-wdatp)terminaison avec Azure Security Center .</span><span class="sxs-lookup"><span data-stu-id="2678b-168">Follow the onboarding instructions in [Microsoft Defender for Endpoint with Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-wdatp).</span></span>

<span data-ttu-id="2678b-169">Après avoir effectué les étapes d’intégration, vous devez configurer et mettre à jour [les clients System Center Endpoint Protection.](#configure-and-update-system-center-endpoint-protection-clients)</span><span class="sxs-lookup"><span data-stu-id="2678b-169">After completing the onboarding steps, you'll need to [Configure and update System Center Endpoint Protection clients](#configure-and-update-system-center-endpoint-protection-clients).</span></span>

> [!NOTE]
> - <span data-ttu-id="2678b-170">Pour que l’intégration via Azure Defender for Servers (anciennement Azure Security Center Standard Edition) fonctionne comme prévu, le serveur doit avoir un espace de travail et une clé appropriés configurés dans les paramètres de l’agent de surveillance Microsoft (MMA).</span><span class="sxs-lookup"><span data-stu-id="2678b-170">For onboarding via Azure Defender for Servers (previously Azure Security Center Standard Edition) to work as expected, the server must have an appropriate workspace and key configured within the Microsoft Monitoring Agent (MMA) settings.</span></span>
> - <span data-ttu-id="2678b-171">Une fois configuré, le pack d’administration cloud approprié est déployé sur l’ordinateur et le processus de capteur (MsSenseS.exe) est déployé et démarré.</span><span class="sxs-lookup"><span data-stu-id="2678b-171">Once configured, the appropriate cloud management pack is deployed on the machine and the sensor process (MsSenseS.exe) will be deployed and started.</span></span> 
> - <span data-ttu-id="2678b-172">Cette configuration est également requise si le serveur est configuré pour utiliser un serveur de passerelle OMS comme proxy.</span><span class="sxs-lookup"><span data-stu-id="2678b-172">This is also required if the server is configured to use an OMS Gateway server as proxy.</span></span>

### <a name="option-3-onboard-windows-servers-through-microsoft-endpoint-manager-version-2002-and-later"></a><span data-ttu-id="2678b-173">Option 3 : intégrer des serveurs Windows via Microsoft Endpoint Manager version 2002 et ultérieure</span><span class="sxs-lookup"><span data-stu-id="2678b-173">Option 3: Onboard Windows servers through Microsoft Endpoint Manager version 2002 and later</span></span>
<span data-ttu-id="2678b-174">Vous pouvez intégrer Windows Server 2012 R2 et Windows Server 2016 à l’aide de Microsoft Endpoint Manager version 2002 et ultérieure.</span><span class="sxs-lookup"><span data-stu-id="2678b-174">You can onboard Windows Server 2012 R2 and Windows Server 2016 by using Microsoft Endpoint Manager version 2002 and later.</span></span> <span data-ttu-id="2678b-175">Pour plus d’informations, [voir Microsoft Defender for Endpoint in Microsoft Endpoint Manager current branch](https://docs.microsoft.com/mem/configmgr/protect/deploy-use/defender-advanced-threat-protection).</span><span class="sxs-lookup"><span data-stu-id="2678b-175">For more information, see [Microsoft Defender for Endpoint in Microsoft Endpoint Manager current branch](https://docs.microsoft.com/mem/configmgr/protect/deploy-use/defender-advanced-threat-protection).</span></span>

<span data-ttu-id="2678b-176">Après avoir effectué les étapes d’intégration, vous devez configurer et mettre à jour [les clients System Center Endpoint Protection.](#configure-and-update-system-center-endpoint-protection-clients)</span><span class="sxs-lookup"><span data-stu-id="2678b-176">After completing the onboarding steps, you'll need to [Configure and update System Center Endpoint Protection clients](#configure-and-update-system-center-endpoint-protection-clients).</span></span>

<br>

## <a name="windows-server-sac-version-1803-windows-server-2019-and-windows-server-2019-core-edition"></a><span data-ttu-id="2678b-177">Windows Server (SAC) version 1803, Windows Server 2019 et Windows Server 2019 Core edition</span><span class="sxs-lookup"><span data-stu-id="2678b-177">Windows Server (SAC) version 1803, Windows Server 2019, and Windows Server 2019 Core edition</span></span>
<span data-ttu-id="2678b-178">Vous pouvez intégrer Windows Server (SAC) version 1803, Windows Server 2019 ou Windows Server 2019 Core edition en utilisant les méthodes de déploiement suivantes :</span><span class="sxs-lookup"><span data-stu-id="2678b-178">You can onboard Windows Server (SAC) version 1803, Windows Server 2019, or Windows Server 2019 Core edition by using the following deployment methods:</span></span>

- [<span data-ttu-id="2678b-179">Script local</span><span class="sxs-lookup"><span data-stu-id="2678b-179">Local script</span></span>](configure-endpoints-script.md) 
- [<span data-ttu-id="2678b-180">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="2678b-180">Group Policy</span></span>](configure-endpoints-gp.md)
- [<span data-ttu-id="2678b-181">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="2678b-181">Microsoft Endpoint Configuration Manager</span></span>](configure-endpoints-sccm.md)
- [<span data-ttu-id="2678b-182">System Center Configuration Manager 2012 /2012 R2 1511 / 1602</span><span class="sxs-lookup"><span data-stu-id="2678b-182">System Center Configuration Manager 2012 / 2012 R2  1511 / 1602</span></span>](configure-endpoints-sccm.md#onboard-devices-using-system-center-configuration-manager)
- [<span data-ttu-id="2678b-183">Scripts d’intégration VDI pour les appareils non persistants</span><span class="sxs-lookup"><span data-stu-id="2678b-183">VDI onboarding scripts for non-persistent devices</span></span>](configure-endpoints-vdi.md)

> [!NOTE]
> - <span data-ttu-id="2678b-184">Le package d’intégration pour Windows Server 2019 via Microsoft Endpoint Manager est actuellement un script.</span><span class="sxs-lookup"><span data-stu-id="2678b-184">The Onboarding package for Windows Server 2019 through Microsoft Endpoint Manager currently ships a script.</span></span> <span data-ttu-id="2678b-185">Pour plus d’informations sur le déploiement de scripts dans Configuration Manager, voir [Packages et programmes dans Configuration Manager.](https://docs.microsoft.com/configmgr/apps/deploy-use/packages-and-programs)</span><span class="sxs-lookup"><span data-stu-id="2678b-185">For more information on how to deploy scripts in Configuration Manager, see [Packages and programs in Configuration Manager](https://docs.microsoft.com/configmgr/apps/deploy-use/packages-and-programs).</span></span>
> - <span data-ttu-id="2678b-186">Un script local convient pour une preuve de concept, mais ne doit pas être utilisé pour le déploiement de production.</span><span class="sxs-lookup"><span data-stu-id="2678b-186">A local script is suitable for a proof of concept but should not be used for production deployment.</span></span> <span data-ttu-id="2678b-187">Pour un déploiement de production, nous vous recommandons d’utiliser la stratégie de groupe ou Microsoft Endpoint Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="2678b-187">For a production deployment, we recommend using Group Policy, or Microsoft Endpoint Configuration Manager.</span></span>

<span data-ttu-id="2678b-188">La prise en charge de Windows Server fournit des informations plus approfondies sur les activités du serveur, la couverture de la détection des attaques du noyau et de la mémoire, et permet des actions de réponse.</span><span class="sxs-lookup"><span data-stu-id="2678b-188">Support for Windows Server provides deeper insight into server activities, coverage for kernel and memory attack detection, and enables response actions.</span></span>

1. <span data-ttu-id="2678b-189">Configurez Defender pour les paramètres d’intégration de point de terminaison sur le serveur Windows à l’aide des mêmes outils et méthodes pour les appareils Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2678b-189">Configure Defender for Endpoint onboarding settings on the Windows server using the same tools and methods for Windows 10 devices.</span></span> <span data-ttu-id="2678b-190">Pour plus d’informations, [voir Appareils Windows 10 intégrés.](configure-endpoints.md)</span><span class="sxs-lookup"><span data-stu-id="2678b-190">For more information, see [Onboard Windows 10 devices](configure-endpoints.md).</span></span>

2. <span data-ttu-id="2678b-191">Si vous exécutez une solution anti-programme malveillant tierce, vous devez appliquer les paramètres suivants du mode passif de l’Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="2678b-191">If you're running a third-party antimalware solution, you'll need to apply the following Microsoft Defender AV passive mode settings.</span></span> <span data-ttu-id="2678b-192">Vérifiez qu’elle a été configurée correctement :</span><span class="sxs-lookup"><span data-stu-id="2678b-192">Verify that it was configured correctly:</span></span>

    1. <span data-ttu-id="2678b-193">Définissez l’entrée de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="2678b-193">Set the following registry entry:</span></span>
       - <span data-ttu-id="2678b-194">Chemin d’accès : `HKLM\SOFTWARE\Policies\Microsoft\Windows Advanced Threat Protection`</span><span class="sxs-lookup"><span data-stu-id="2678b-194">Path: `HKLM\SOFTWARE\Policies\Microsoft\Windows Advanced Threat Protection`</span></span>
       - <span data-ttu-id="2678b-195">Nom : ForceDefenderPassiveMode</span><span class="sxs-lookup"><span data-stu-id="2678b-195">Name: ForceDefenderPassiveMode</span></span>
       - <span data-ttu-id="2678b-196">Type : REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="2678b-196">Type: REG_DWORD</span></span>
       - <span data-ttu-id="2678b-197">Value: 1</span><span class="sxs-lookup"><span data-stu-id="2678b-197">Value: 1</span></span>

    1. <span data-ttu-id="2678b-198">Exécutez la commande PowerShell suivante pour vérifier que le mode passif a été configuré :</span><span class="sxs-lookup"><span data-stu-id="2678b-198">Run the following PowerShell command to verify that the passive mode was configured:</span></span>

       ```PowerShell
       Get-WinEvent -FilterHashtable @{ProviderName="Microsoft-Windows-Sense" ;ID=84}
       ```

    1. <span data-ttu-id="2678b-199">Confirmez qu’un événement récent contenant l’événement en mode passif est trouvé :</span><span class="sxs-lookup"><span data-stu-id="2678b-199">Confirm  that a recent event containing the passive mode event is found:</span></span>

       ![Image du résultat de vérification du mode passif](images/atp-verify-passive-mode.png)

3. <span data-ttu-id="2678b-201">Exécutez la commande suivante pour vérifier si Microsoft Defender AV est installé :</span><span class="sxs-lookup"><span data-stu-id="2678b-201">Run the following command to check if Microsoft Defender AV is installed:</span></span>

   ```sc.exe query Windefend```

    <span data-ttu-id="2678b-202">Si le résultat est « Le service spécifié n’existe pas en tant que service installé » , vous devez installer Microsoft Defender AV.</span><span class="sxs-lookup"><span data-stu-id="2678b-202">If the result is 'The specified service doesn't exist as an installed service', then you'll need to install Microsoft Defender AV.</span></span> <span data-ttu-id="2678b-203">Pour plus d’informations, [voir Antivirus Microsoft Defender dans Windows 10.](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/microsoft-defender-antivirus-in-windows-10)</span><span class="sxs-lookup"><span data-stu-id="2678b-203">For more information, see [Microsoft Defender Antivirus in Windows 10](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/microsoft-defender-antivirus-in-windows-10).</span></span>
    
    <span data-ttu-id="2678b-204">Pour plus d’informations sur l’utilisation de la stratégie de groupe pour configurer et gérer l’Antivirus Microsoft Defender sur vos serveurs Windows, voir Utiliser les paramètres de stratégie de groupe pour configurer et gérer [l’Antivirus Microsoft Defender.](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/use-group-policy-microsoft-defender-antivirus)</span><span class="sxs-lookup"><span data-stu-id="2678b-204">For information on how to use Group Policy to configure and manage Microsoft Defender Antivirus on your Windows servers, see [Use Group Policy settings to configure and manage Microsoft Defender Antivirus](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/use-group-policy-microsoft-defender-antivirus).</span></span>

<br>

## <a name="integration-with-azure-security-center"></a><span data-ttu-id="2678b-205">Intégration au Centre de sécurité Azure</span><span class="sxs-lookup"><span data-stu-id="2678b-205">Integration with Azure Security Center</span></span>
<span data-ttu-id="2678b-206">Defender pour le point de terminaison peut s’intégrer au Centre de sécurité Azure pour fournir une solution complète de protection de serveur Windows.</span><span class="sxs-lookup"><span data-stu-id="2678b-206">Defender for Endpoint can integrate with Azure Security Center to provide a comprehensive Windows server protection solution.</span></span> <span data-ttu-id="2678b-207">Avec cette intégration, Azure Security Center peut utiliser la puissance de Defender for Endpoint pour fournir une détection améliorée des menaces pour les serveurs Windows.</span><span class="sxs-lookup"><span data-stu-id="2678b-207">With this integration, Azure Security Center can use the power of Defender for Endpoint to provide improved threat detection for Windows Servers.</span></span>

<span data-ttu-id="2678b-208">Les fonctionnalités suivantes sont incluses dans cette intégration :</span><span class="sxs-lookup"><span data-stu-id="2678b-208">The following capabilities are included in this integration:</span></span>
- <span data-ttu-id="2678b-209">Intégration automatisée : le capteur Defender for Endpoint est automatiquement activé sur les serveurs Windows intégrés au Centre de sécurité Azure.</span><span class="sxs-lookup"><span data-stu-id="2678b-209">Automated onboarding - Defender for Endpoint sensor is automatically enabled on Windows Servers that are onboarded to Azure Security Center.</span></span> <span data-ttu-id="2678b-210">Pour plus d’informations sur l’intégration du Centre de sécurité Azure, voir Intégration à [Azure Security Center Standard pour une sécurité renforcée.](https://docs.microsoft.com/azure/security-center/security-center-onboarding)</span><span class="sxs-lookup"><span data-stu-id="2678b-210">For more information on Azure Security Center onboarding, see [Onboarding to Azure Security Center Standard for enhanced security](https://docs.microsoft.com/azure/security-center/security-center-onboarding).</span></span>

    > [!NOTE]
    > <span data-ttu-id="2678b-211">L’intégration automatisée s’applique uniquement à Windows Server 2008 R2 SP1, Windows Server 2012 R2 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="2678b-211">Automated onboarding is only applicable for Windows Server 2008 R2 SP1, Windows Server 2012 R2, and Windows Server 2016.</span></span>

- <span data-ttu-id="2678b-212">Les serveurs Windows surveillés par le Centre de sécurité Azure seront également disponibles dans Defender for Endpoint - Azure Security Center se connecte en toute transparence au client Defender for Endpoint, fournissant une vue unique sur les clients et les serveurs.</span><span class="sxs-lookup"><span data-stu-id="2678b-212">Windows servers monitored by Azure Security Center will also be available in Defender for Endpoint - Azure Security Center seamlessly connects to the Defender for Endpoint tenant, providing a single view across clients and servers.</span></span>  <span data-ttu-id="2678b-213">En outre, les alertes Defender pour le point de terminaison seront disponibles dans la console Azure Security Center.</span><span class="sxs-lookup"><span data-stu-id="2678b-213">In addition, Defender for Endpoint alerts will be available in the Azure Security Center console.</span></span>
- <span data-ttu-id="2678b-214">Enquête sur le serveur : les clients du Centre de sécurité Azure peuvent accéder au Centre de sécurité Microsoft Defender pour effectuer une enquête détaillée afin de découvrir l’étendue d’une violation potentielle.</span><span class="sxs-lookup"><span data-stu-id="2678b-214">Server investigation -  Azure Security Center customers can access Microsoft Defender Security Center to perform detailed investigation to uncover the scope of a potential breach.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="2678b-215">Lorsque vous utilisez le Centre de sécurité Azure pour surveiller les serveurs, un client Defender for Endpoint est automatiquement créé (aux États-Unis pour les utilisateurs américains, dans l’UE pour les utilisateurs européens et anglais).</span><span class="sxs-lookup"><span data-stu-id="2678b-215">When you use Azure Security Center to monitor servers, a Defender for Endpoint tenant is automatically created (in the US for US users, in the EU for European and UK users).</span></span><br>
<span data-ttu-id="2678b-216">Les données collectées par Defender pour endpoint sont stockées dans l’emplacement géographique du client, comme identifié lors de l’approvisionnement.</span><span class="sxs-lookup"><span data-stu-id="2678b-216">Data collected by Defender for Endpoint is stored in the geo-location of the tenant as identified during provisioning.</span></span>
> - <span data-ttu-id="2678b-217">Si vous utilisez Defender pour endpoint avant d’utiliser Azure Security Center, vos données seront stockées à l’emplacement que vous avez spécifié lors de la création de votre client, même si vous intégrez le Centre de sécurité Azure ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="2678b-217">If you use Defender for Endpoint before using Azure Security Center, your data will be stored in the location you specified when you created your tenant even if you integrate with Azure Security Center at a later time.</span></span>
> - <span data-ttu-id="2678b-218">Une fois configuré, vous ne pouvez pas modifier l’emplacement où vos données sont stockées.</span><span class="sxs-lookup"><span data-stu-id="2678b-218">Once configured, you cannot change the location where your data is stored.</span></span> <span data-ttu-id="2678b-219">Si vous devez déplacer vos données vers un autre emplacement, vous devez contacter le Support Microsoft pour réinitialiser le client.</span><span class="sxs-lookup"><span data-stu-id="2678b-219">If you need to move your data to another location, you need to contact Microsoft Support to reset the tenant.</span></span> <br>
<span data-ttu-id="2678b-220">La surveillance des points de terminaison du serveur utilisant cette intégration a été désactivée pour les clients Office 365 GCC.</span><span class="sxs-lookup"><span data-stu-id="2678b-220">Server endpoint monitoring utilizing this integration has been disabled for Office 365 GCC customers.</span></span>

<br>

## <a name="configure-and-update-system-center-endpoint-protection-clients"></a><span data-ttu-id="2678b-221">Configurer et mettre à jour les clients System Center Endpoint Protection</span><span class="sxs-lookup"><span data-stu-id="2678b-221">Configure and update System Center Endpoint Protection clients</span></span>

<span data-ttu-id="2678b-222">Defender pour le point de terminaison s’intègre à System Center Endpoint Protection.</span><span class="sxs-lookup"><span data-stu-id="2678b-222">Defender for Endpoint integrates with System Center Endpoint Protection.</span></span> <span data-ttu-id="2678b-223">L’intégration offre une visibilité sur les détections de programmes malveillants et pour arrêter la propagation d’une attaque dans votre organisation en interdit les fichiers potentiellement malveillants ou les programmes malveillants suspectés.</span><span class="sxs-lookup"><span data-stu-id="2678b-223">The integration provides visibility to malware detections and to stop propagation of an attack in your organization by banning potentially malicious files or suspected malware.</span></span>

<span data-ttu-id="2678b-224">Les étapes suivantes sont nécessaires pour activer cette intégration :</span><span class="sxs-lookup"><span data-stu-id="2678b-224">The following steps are required to enable this integration:</span></span>
- <span data-ttu-id="2678b-225">Installez la mise à jour de la plateforme anti-programme malveillant de janvier [2017 pour les clients Endpoint Protection.](https://support.microsoft.com/help/3209361/january-2017-anti-malware-platform-update-for-endpoint-protection-clie)</span><span class="sxs-lookup"><span data-stu-id="2678b-225">Install the [January 2017 anti-malware platform update for Endpoint Protection clients](https://support.microsoft.com/help/3209361/january-2017-anti-malware-platform-update-for-endpoint-protection-clie).</span></span>

- <span data-ttu-id="2678b-226">[Configurez l’appartenance au service protection cloud client SCEP](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/enable-cloud-protection-microsoft-defender-antivirus) sur **le paramètre** Avancé.</span><span class="sxs-lookup"><span data-stu-id="2678b-226">[Configure the SCEP client Cloud Protection Service membership](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/enable-cloud-protection-microsoft-defender-antivirus) to the **Advanced** setting.</span></span>

<br>

## <a name="offboard-windows-servers"></a><span data-ttu-id="2678b-227">Offboard Windows servers</span><span class="sxs-lookup"><span data-stu-id="2678b-227">Offboard Windows servers</span></span>
<span data-ttu-id="2678b-228">Vous pouvez désinserrez Windows Server (SAC), Windows Server 2019 et Windows Server 2019 Core edition dans la même méthode disponible pour les appareils clients Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2678b-228">You can offboard Windows Server (SAC), Windows Server 2019, and Windows Server 2019 Core edition in the same method available for Windows 10 client devices.</span></span>

<span data-ttu-id="2678b-229">Pour les autres versions de serveur Windows, vous avez deux options pour hors-service les serveurs Windows :</span><span class="sxs-lookup"><span data-stu-id="2678b-229">For other Windows server versions, you have two options to offboard Windows servers from the service:</span></span>
- <span data-ttu-id="2678b-230">Désinstaller l’agent MMA</span><span class="sxs-lookup"><span data-stu-id="2678b-230">Uninstall the MMA agent</span></span>
- <span data-ttu-id="2678b-231">Supprimer la configuration de l’espace de travail Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="2678b-231">Remove the Defender for Endpoint workspace configuration</span></span>

> [!NOTE]
> <span data-ttu-id="2678b-232">La mise hors-carte entraîne l’arrêt par le serveur Windows de l’envoi de données de capteur au portail, mais les données du serveur Windows, y compris la référence aux alertes qu’il a eues, seront conservées pendant 6 mois.</span><span class="sxs-lookup"><span data-stu-id="2678b-232">Offboarding causes the Windows server to stop sending sensor data to the portal but data from the Windows server, including reference to any alerts it has had will be retained for up to 6 months.</span></span>

### <a name="uninstall-windows-servers-by-uninstalling-the-mma-agent"></a><span data-ttu-id="2678b-233">Désinstaller des serveurs Windows en désinstallant l’agent MMA</span><span class="sxs-lookup"><span data-stu-id="2678b-233">Uninstall Windows servers by uninstalling the MMA agent</span></span>
<span data-ttu-id="2678b-234">Pour désinstaller le serveur Windows, vous pouvez désinstaller l’agent MMA du serveur Windows ou le détacher des rapports à votre espace de travail Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="2678b-234">To offboard the Windows server, you can uninstall the MMA agent from the Windows server or detach it from reporting to your Defender for Endpoint workspace.</span></span> <span data-ttu-id="2678b-235">Après la mise hors-carte de l’agent, le serveur Windows n’envoie plus de données de capteur à Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="2678b-235">After offboarding the agent, the Windows server will no longer send sensor data to Defender for Endpoint.</span></span>
<span data-ttu-id="2678b-236">Pour plus d’informations, [voir Pour désactiver un agent.](https://docs.microsoft.com/azure/log-analytics/log-analytics-windows-agents#to-disable-an-agent)</span><span class="sxs-lookup"><span data-stu-id="2678b-236">For more information, see [To disable an agent](https://docs.microsoft.com/azure/log-analytics/log-analytics-windows-agents#to-disable-an-agent).</span></span>

### <a name="remove-the-defender-for-endpoint-workspace-configuration"></a><span data-ttu-id="2678b-237">Supprimer la configuration de l’espace de travail Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="2678b-237">Remove the Defender for Endpoint workspace configuration</span></span>
<span data-ttu-id="2678b-238">Pour mettre hors service le serveur Windows, vous pouvez utiliser l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="2678b-238">To offboard the Windows server, you can use either of the following methods:</span></span>

- <span data-ttu-id="2678b-239">Supprimer la configuration de l’espace de travail Defender for Endpoint de l’agent MMA</span><span class="sxs-lookup"><span data-stu-id="2678b-239">Remove the Defender for Endpoint workspace configuration from the MMA agent</span></span>
- <span data-ttu-id="2678b-240">Exécuter une commande PowerShell pour supprimer la configuration</span><span class="sxs-lookup"><span data-stu-id="2678b-240">Run a PowerShell command to remove the configuration</span></span>

#### <a name="remove-the-defender-for-endpoint-workspace-configuration-from-the-mma-agent"></a><span data-ttu-id="2678b-241">Supprimer la configuration de l’espace de travail Defender for Endpoint de l’agent MMA</span><span class="sxs-lookup"><span data-stu-id="2678b-241">Remove the Defender for Endpoint workspace configuration from the MMA agent</span></span>

1. <span data-ttu-id="2678b-242">Dans les **propriétés de l’agent** de surveillance Microsoft, sélectionnez **l’onglet Azure Log Analytics (OMS).**</span><span class="sxs-lookup"><span data-stu-id="2678b-242">In the **Microsoft Monitoring Agent Properties**, select the **Azure Log Analytics (OMS)** tab.</span></span>

2. <span data-ttu-id="2678b-243">Sélectionnez l’espace de travail Defender pour le point de terminaison, puis cliquez sur **Supprimer.**</span><span class="sxs-lookup"><span data-stu-id="2678b-243">Select the Defender for Endpoint workspace, and click **Remove**.</span></span>

    ![Image des propriétés de l’agent de surveillance Microsoft](images/atp-mma.png)

#### <a name="run-a-powershell-command-to-remove-the-configuration"></a><span data-ttu-id="2678b-245">Exécuter une commande PowerShell pour supprimer la configuration</span><span class="sxs-lookup"><span data-stu-id="2678b-245">Run a PowerShell command to remove the configuration</span></span>

1. <span data-ttu-id="2678b-246">Obtenez votre ID d’espace de travail :</span><span class="sxs-lookup"><span data-stu-id="2678b-246">Get your Workspace ID:</span></span>

   1. <span data-ttu-id="2678b-247">Dans le volet de navigation, sélectionnez **Intégration** des  >  **paramètres.**</span><span class="sxs-lookup"><span data-stu-id="2678b-247">In the navigation pane, select **Settings** > **Onboarding**.</span></span>

   1. <span data-ttu-id="2678b-248">Sélectionnez **Windows Server 2008 R2 SP1, 2012 R2 et 2016** comme système d’exploitation et obtenez votre ID d’espace de travail :</span><span class="sxs-lookup"><span data-stu-id="2678b-248">Select **Windows Server 2008 R2 SP1, 2012 R2 and 2016** as the operating system and get your Workspace ID:</span></span>

      ![Image de l’intégration de Windows Server](images/atp-server-offboarding-workspaceid.png)

2. <span data-ttu-id="2678b-250">Ouvrez un PowerShell élevé et exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="2678b-250">Open an elevated PowerShell and run the following command.</span></span> <span data-ttu-id="2678b-251">Utilisez l’ID d’espace de travail que vous avez obtenu et remplacez `WorkspaceID` :</span><span class="sxs-lookup"><span data-stu-id="2678b-251">Use the Workspace ID you obtained and replacing `WorkspaceID`:</span></span>

    ```powershell
    $ErrorActionPreference = "SilentlyContinue"
    # Load agent scripting object
    $AgentCfg = New-Object -ComObject AgentConfigManager.MgmtSvcCfg
    # Remove OMS Workspace
    $AgentCfg.RemoveCloudWorkspace("WorkspaceID")
    # Reload the configuration and apply changes
    $AgentCfg.ReloadConfiguration()

    ```

<br>

## <a name="related-topics"></a><span data-ttu-id="2678b-252">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2678b-252">Related topics</span></span>
- [<span data-ttu-id="2678b-253">Intégrer des appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="2678b-253">Onboard Windows 10 devices</span></span>](configure-endpoints.md)
- [<span data-ttu-id="2678b-254">Intégrer des appareils autres que Windows</span><span class="sxs-lookup"><span data-stu-id="2678b-254">Onboard non-Windows devices</span></span>](configure-endpoints-non-windows.md)
- [<span data-ttu-id="2678b-255">Configurer les paramètres de proxy et de connectivité Internet</span><span class="sxs-lookup"><span data-stu-id="2678b-255">Configure proxy and Internet connectivity settings</span></span>](configure-proxy-internet.md)
- [<span data-ttu-id="2678b-256">Exécuter un test de détection sur un appareil Defender pour point de terminaison nouvellement intégré</span><span class="sxs-lookup"><span data-stu-id="2678b-256">Run a detection test on a newly onboarded Defender for Endpoint device</span></span>](run-detection-test.md)
- [<span data-ttu-id="2678b-257">Résolution des problèmes d’intégration de Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="2678b-257">Troubleshooting Microsoft Defender for Endpoint onboarding issues</span></span>](troubleshoot-onboarding.md)
