---
title: Intégrer Windows serveurs d’accès au service Microsoft Defender for Endpoint
description: Intégrer Windows serveurs afin qu’ils peuvent envoyer des données de capteur au capteur Microsoft Defender for Endpoint.
keywords: onboard server, server, 2012r2, 2016, 2019, server onboarding, device management, configure Microsoft Defender for Endpoint servers, onboard Microsoft Defender for Endpoint servers, onboard Microsoft Defender for Endpoint servers, onboard Microsoft Defender for Endpoint servers
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
ms.openlocfilehash: 47d57e51eca4950f7a8f4284fbc916e9d030b2c7
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52844333"
---
# <a name="onboard-windows-servers-to-the-microsoft-defender-for-endpoint-service"></a><span data-ttu-id="e736a-104">Intégrer Windows serveurs d’accès au service Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="e736a-104">Onboard Windows servers to the Microsoft Defender for Endpoint service</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="e736a-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="e736a-105">**Applies to:**</span></span>

- <span data-ttu-id="e736a-106">Windows Server 2008 R2 SP1</span><span class="sxs-lookup"><span data-stu-id="e736a-106">Windows Server 2008 R2 SP1</span></span>
- <span data-ttu-id="e736a-107">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="e736a-107">Windows Server 2012 R2</span></span>
- <span data-ttu-id="e736a-108">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e736a-108">Windows Server 2016</span></span>
- <span data-ttu-id="e736a-109">Windows Server (SAC) version 1803 et ultérieure</span><span class="sxs-lookup"><span data-stu-id="e736a-109">Windows Server (SAC) version 1803 and later</span></span>
- <span data-ttu-id="e736a-110">Windows Server 2019 et ultérieur</span><span class="sxs-lookup"><span data-stu-id="e736a-110">Windows Server 2019 and later</span></span>
- <span data-ttu-id="e736a-111">Windows Server 2019 Core Edition</span><span class="sxs-lookup"><span data-stu-id="e736a-111">Windows Server 2019 core edition</span></span>

> <span data-ttu-id="e736a-112">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="e736a-112">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="e736a-113">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="e736a-113">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-configserver-abovefoldlink)

<span data-ttu-id="e736a-114">Defender for Endpoint étend la prise en charge pour inclure également le Windows d’exploitation Server.</span><span class="sxs-lookup"><span data-stu-id="e736a-114">Defender for Endpoint extends support to also include the Windows Server operating system.</span></span> <span data-ttu-id="e736a-115">Cette prise en charge offre des fonctionnalités avancées de détection d’attaques et d’examens en toute transparence via Centre de sécurité Microsoft Defender console.</span><span class="sxs-lookup"><span data-stu-id="e736a-115">This support provides advanced attack detection and investigation capabilities seamlessly through the Microsoft Defender Security Center console.</span></span>

<span data-ttu-id="e736a-116">Pour obtenir des instructions pratiques sur ce qui doit être en place pour la gestion des licences et l’infrastructure, voir Protection des serveurs Windows [avec Defender for Endpoint](https://techcommunity.microsoft.com/t5/What-s-New/Protecting-Windows-Server-with-Windows-Defender-ATP/m-p/267114#M128).</span><span class="sxs-lookup"><span data-stu-id="e736a-116">For a practical guidance on what needs to be in place for licensing and infrastructure, see [Protecting Windows Servers with Defender for Endpoint](https://techcommunity.microsoft.com/t5/What-s-New/Protecting-Windows-Server-with-Windows-Defender-ATP/m-p/267114#M128).</span></span>

<span data-ttu-id="e736a-117">Pour obtenir des instructions sur la façon de télécharger et d’utiliser Sécurité Windows de référence pour Windows serveurs, voir Sécurité Windows [baselines](/windows/device-security/windows-security-baselines).</span><span class="sxs-lookup"><span data-stu-id="e736a-117">For guidance on how to download and use Windows Security Baselines for Windows servers, see [Windows Security Baselines](/windows/device-security/windows-security-baselines).</span></span>

## <a name="windows-server-2008-r2-sp1-windows-server-2012-r2-and-windows-server-2016"></a><span data-ttu-id="e736a-118">Windows Server 2008 R2 SP1, Windows Server 2012 R2 et Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e736a-118">Windows Server 2008 R2 SP1, Windows Server 2012 R2, and Windows Server 2016</span></span>

<span data-ttu-id="e736a-119">Vous pouvez intégrer Windows Server 2008 R2 SP1, Windows Server 2012 R2 et Windows Server 2016 à Defender pour Endpoint en utilisant l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="e736a-119">You can onboard Windows Server 2008 R2 SP1, Windows Server 2012 R2, and Windows Server 2016 to Defender for Endpoint by using any of the following options:</span></span>

- <span data-ttu-id="e736a-120">**Option 1**: [intégrer en installant et en configurant Microsoft Monitoring Agent (MMA)](#option-1-onboard-by-installing-and-configuring-microsoft-monitoring-agent-mma)</span><span class="sxs-lookup"><span data-stu-id="e736a-120">**Option 1**: [Onboard by installing and configuring Microsoft Monitoring Agent (MMA)](#option-1-onboard-by-installing-and-configuring-microsoft-monitoring-agent-mma)</span></span>
- <span data-ttu-id="e736a-121">**Option 2 :** intégration [via le Centre de sécurité Azure](#option-2-onboard-windows-servers-through-azure-security-center)</span><span class="sxs-lookup"><span data-stu-id="e736a-121">**Option 2**: [Onboard through Azure Security Center](#option-2-onboard-windows-servers-through-azure-security-center)</span></span>
- <span data-ttu-id="e736a-122">**Option 3**: [intégration via Microsoft Endpoint Manager version 2002 et ultérieures](#option-3-onboard-windows-servers-through-microsoft-endpoint-manager-version-2002-and-later)</span><span class="sxs-lookup"><span data-stu-id="e736a-122">**Option 3**: [Onboard through Microsoft Endpoint Manager version 2002 and later](#option-3-onboard-windows-servers-through-microsoft-endpoint-manager-version-2002-and-later)</span></span>

<span data-ttu-id="e736a-123">Après avoir effectué les étapes d’intégration à l’aide de l’une des options fournies, vous devez configurer et mettre à [jour System Center Endpoint Protection clients.](#configure-and-update-system-center-endpoint-protection-clients)</span><span class="sxs-lookup"><span data-stu-id="e736a-123">After completing the onboarding steps using any of the provided options, you'll need to [Configure and update System Center Endpoint Protection clients](#configure-and-update-system-center-endpoint-protection-clients).</span></span>

> [!NOTE]
> <span data-ttu-id="e736a-124">La licence de serveur autonome Defender pour les points de terminaison est requise, par nœud, pour intégrer un serveur Windows via Microsoft Monitoring Agent (option 1) ou via Microsoft Endpoint Manager (option 3).</span><span class="sxs-lookup"><span data-stu-id="e736a-124">Defender for Endpoint standalone server license is required, per node, in order to onboard a Windows server through Microsoft Monitoring Agent (Option 1), or through Microsoft Endpoint Manager (Option 3).</span></span> <span data-ttu-id="e736a-125">Une licence Azure Defender pour les serveurs est également requise, par nœud, pour intégrer un serveur Windows via Azure Security Center (option 2), voir fonctionnalités pris en charge disponibles dans [Azure Defender.](/azure/security-center/security-center-services)</span><span class="sxs-lookup"><span data-stu-id="e736a-125">Alternatively, an Azure Defender for Servers license is required, per node, in order to onboard a Windows server through Azure Security Center (Option 2), see [Supported features available in Azure Defender](/azure/security-center/security-center-services).</span></span>

### <a name="option-1-onboard-by-installing-and-configuring-microsoft-monitoring-agent-mma"></a><span data-ttu-id="e736a-126">Option 1 : intégrer en installant et en configurant Microsoft Monitoring Agent (MMA)</span><span class="sxs-lookup"><span data-stu-id="e736a-126">Option 1: Onboard by installing and configuring Microsoft Monitoring Agent (MMA)</span></span>

<span data-ttu-id="e736a-127">Vous devez installer et configurer MMA pour que les serveurs Windows rapportent les données de capteur à Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="e736a-127">You'll need to install and configure MMA for Windows servers to report sensor data to Defender for Endpoint.</span></span> <span data-ttu-id="e736a-128">Pour plus d’informations, voir [Collecter les données du journal avec l’agent Azure Log Analytics.](/azure/azure-monitor/platform/log-analytics-agent)</span><span class="sxs-lookup"><span data-stu-id="e736a-128">For more information, see [Collect log data with Azure Log Analytics agent](/azure/azure-monitor/platform/log-analytics-agent).</span></span>

<span data-ttu-id="e736a-129">Si vous utilisez déjà System Center Operations Manager (SCOM) ou Azure Monitor (anciennement Operations Management Suite (OMS), attachez le Microsoft Monitoring Agent (MMA) pour signaler à votre espace de travail Defender for Endpoint par le biais de la prise en charge multi-homing.</span><span class="sxs-lookup"><span data-stu-id="e736a-129">If you're already using System Center Operations Manager (SCOM) or Azure Monitor (formerly known as Operations Management Suite (OMS)), attach the Microsoft Monitoring Agent (MMA) to report to your Defender for Endpoint workspace through Multihoming support.</span></span>

<span data-ttu-id="e736a-130">En règle générale, vous devez suivre les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="e736a-130">In general, you'll need to take the following steps:</span></span>

1. <span data-ttu-id="e736a-131">Remplissez les conditions d’intégration décrites dans la section **Avant de commencer.**</span><span class="sxs-lookup"><span data-stu-id="e736a-131">Fulfill the onboarding requirements outlined in **Before you begin** section.</span></span>
2. <span data-ttu-id="e736a-132">Activer la surveillance du serveur à partir du Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="e736a-132">Turn on server monitoring from Microsoft Defender Security center.</span></span>
3. <span data-ttu-id="e736a-133">Installez et configurez MMA pour le serveur afin de signaler les données de capteur à Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="e736a-133">Install and configure MMA for the server to report sensor data to Defender for Endpoint.</span></span>
4. <span data-ttu-id="e736a-134">Configurez et mettez à jour System Center Endpoint Protection clients.</span><span class="sxs-lookup"><span data-stu-id="e736a-134">Configure and update System Center Endpoint Protection clients.</span></span>

> [!TIP]
> <span data-ttu-id="e736a-135">Après avoir intégré l’appareil, vous pouvez choisir d’exécuter un test de détection pour vérifier qu’il est correctement intégré au service.</span><span class="sxs-lookup"><span data-stu-id="e736a-135">After onboarding the device, you can choose to run a detection test to verify that it is properly onboarded to the service.</span></span> <span data-ttu-id="e736a-136">Pour plus d’informations, voir Exécuter un test de détection sur un point de terminaison [Defender pour point de terminaison nouvellement intégré.](run-detection-test.md)</span><span class="sxs-lookup"><span data-stu-id="e736a-136">For more information, see [Run a detection test on a newly onboarded Defender for Endpoint endpoint](run-detection-test.md).</span></span>

#### <a name="before-you-begin"></a><span data-ttu-id="e736a-137">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="e736a-137">Before you begin</span></span>

<span data-ttu-id="e736a-138">Pour répondre aux exigences d’intégration, effectuez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="e736a-138">Perform the following steps to fulfill the onboarding requirements:</span></span>

<span data-ttu-id="e736a-139">Pour Windows Server 2008 R2 SP1 ou Windows Server 2012 R2, assurez-vous d’installer le correctif logiciel suivant :</span><span class="sxs-lookup"><span data-stu-id="e736a-139">For Windows Server 2008 R2 SP1 or Windows Server 2012 R2, ensure that you install the following hotfix:</span></span>

- [<span data-ttu-id="e736a-140">Mise à jour pour la télémétrie d’expérience client et de diagnostic</span><span class="sxs-lookup"><span data-stu-id="e736a-140">Update for customer experience and diagnostic telemetry</span></span>](https://support.microsoft.com/help/3080149/update-for-customer-experience-and-diagnostic-telemetry)

<span data-ttu-id="e736a-141">Pour Windows Server 2008 R2 SP1, assurez-vous que vous remplissez les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="e736a-141">For Windows Server 2008 R2 SP1, ensure that you fulfill the following requirements:</span></span>

- <span data-ttu-id="e736a-142">Installer le rapport de [mise à jour mensuelle de février](https://support.microsoft.com/help/4074598/windows-7-update-kb4074598)</span><span class="sxs-lookup"><span data-stu-id="e736a-142">Install the [February monthly update rollup](https://support.microsoft.com/help/4074598/windows-7-update-kb4074598)</span></span>
- <span data-ttu-id="e736a-143">Installer [.NET Framework 4.5](https://www.microsoft.com/download/details.aspx?id=30653) (ou ultérieur) ou [KB3154518](https://support.microsoft.com/help/3154518/support-for-tls-system-default-versions-included-in-the-net-framework)</span><span class="sxs-lookup"><span data-stu-id="e736a-143">Install either [.NET framework 4.5](https://www.microsoft.com/download/details.aspx?id=30653) (or later) or [KB3154518](https://support.microsoft.com/help/3154518/support-for-tls-system-default-versions-included-in-the-net-framework)</span></span>

    > [!NOTE]
    > <span data-ttu-id="e736a-144">Si vous gérez votre Windows Server 2008 R2 SP1 avec SCCM, l’agent client SCCM installe .Net Framework 4.5.2.</span><span class="sxs-lookup"><span data-stu-id="e736a-144">If you are managing your Windows Server 2008 R2 SP1 with SCCM, the SCCM client agent installs .Net Framework 4.5.2.</span></span> <span data-ttu-id="e736a-145">Vous n’avez donc pas besoin d’installer .NET Framework 4.5 (ou une ultérieure).</span><span class="sxs-lookup"><span data-stu-id="e736a-145">So you don't need to install the .NET framework 4.5 (or later).</span></span>

<span data-ttu-id="e736a-146">Pour Windows Server 2008 R2 SP1 et Windows Server 2012 R2 : configurer et mettre à jour [System Center Endpoint Protection clients.](#configure-and-update-system-center-endpoint-protection-clients)</span><span class="sxs-lookup"><span data-stu-id="e736a-146">For Windows Server 2008 R2 SP1 and Windows Server 2012 R2: [Configure and update System Center Endpoint Protection clients](#configure-and-update-system-center-endpoint-protection-clients).</span></span>

> [!NOTE]
> <span data-ttu-id="e736a-147">Cette étape est requise uniquement si votre organisation utilise System Center Endpoint Protection (SCEP) et que vous intégrerez Windows Server 2008 R2 SP1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="e736a-147">This step is required only if your organization uses System Center Endpoint Protection (SCEP) and you're onboarding Windows Server 2008 R2 SP1 and Windows Server 2012 R2.</span></span>

### <a name="install-and-configure-microsoft-monitoring-agent-mma-to-report-sensor-data-to-microsoft-defender-for-endpoint"></a><span data-ttu-id="e736a-148">Installer et configurer Microsoft Monitoring Agent (MMA) pour signaler les données de capteur à Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="e736a-148">Install and configure Microsoft Monitoring Agent (MMA) to report sensor data to Microsoft Defender for Endpoint</span></span>

1. <span data-ttu-id="e736a-149">Téléchargez le fichier de configuration de [l’agent : Windows agent 64 bits.](https://go.microsoft.com/fwlink/?LinkId=828603)</span><span class="sxs-lookup"><span data-stu-id="e736a-149">Download the agent setup file: [Windows 64-bit agent](https://go.microsoft.com/fwlink/?LinkId=828603).</span></span>

2. <span data-ttu-id="e736a-150">À l’aide de l’ID d’espace de travail et de la clé d’espace de travail obtenus dans la procédure précédente, choisissez l’une des méthodes d’installation suivantes pour installer l’agent sur Windows serveur :</span><span class="sxs-lookup"><span data-stu-id="e736a-150">Using the Workspace ID and Workspace key obtained in the previous procedure, choose any of the following installation methods to install the agent on the Windows server:</span></span>
    - <span data-ttu-id="e736a-151">[Installez manuellement l’agent à l’aide du programme d’installation.](/azure/log-analytics/log-analytics-windows-agents#install-agent-using-setup-wizard)</span><span class="sxs-lookup"><span data-stu-id="e736a-151">[Manually install the agent using setup](/azure/log-analytics/log-analytics-windows-agents#install-agent-using-setup-wizard).</span></span> 
    <span data-ttu-id="e736a-152">Dans la page **Options d’installation** de l’agent, **Connecter l’agent dans Azure Log Analytics (OMS).**</span><span class="sxs-lookup"><span data-stu-id="e736a-152">On the **Agent Setup Options** page, choose **Connect the agent to Azure Log Analytics (OMS)**.</span></span>
    - <span data-ttu-id="e736a-153">[Installez l’agent à l’aide de la ligne de commande.](/azure/log-analytics/log-analytics-windows-agents#install-agent-using-command-line)</span><span class="sxs-lookup"><span data-stu-id="e736a-153">[Install the agent using the command line](/azure/log-analytics/log-analytics-windows-agents#install-agent-using-command-line).</span></span>
    - <span data-ttu-id="e736a-154">[Configurez l’agent à l’aide d’un script.](/azure/log-analytics/log-analytics-windows-agents#install-agent-using-dsc-in-azure-automation)</span><span class="sxs-lookup"><span data-stu-id="e736a-154">[Configure the agent using a script](/azure/log-analytics/log-analytics-windows-agents#install-agent-using-dsc-in-azure-automation).</span></span>

> [!NOTE]
> <span data-ttu-id="e736a-155">Si vous [](gov.md)êtes un client du gouvernement des États-Unis, sous « Azure Cloud », vous devez choisir « Azure US Government » si vous utilisez l’Assistant Installation, ou si vous utilisez une ligne de commande ou un script , définissez le paramètre « OPINSIGHTS_WORKSPACE_AZURE_CLOUD_TYPE » sur 1.</span><span class="sxs-lookup"><span data-stu-id="e736a-155">If you are a [US Government customer](gov.md), under "Azure Cloud" you'll need to choose "Azure US Government" if using the setup wizard, or if using a command line or a script - set the "OPINSIGHTS_WORKSPACE_AZURE_CLOUD_TYPE" parameter to 1.</span></span>

### <a name="configure-windows-server-proxy-and-internet-connectivity-settings-if-needed"></a><span data-ttu-id="e736a-156">Configurer les paramètres Windows proxy du serveur et de connectivité Internet si nécessaire</span><span class="sxs-lookup"><span data-stu-id="e736a-156">Configure Windows server proxy and Internet connectivity settings if needed</span></span>

<span data-ttu-id="e736a-157">Si vos serveurs doivent utiliser un proxy pour communiquer avec Defender pour le point de terminaison, utilisez l’une des méthodes suivantes pour configurer MMA afin qu’il utilise le serveur proxy :</span><span class="sxs-lookup"><span data-stu-id="e736a-157">If your servers need to use a proxy to communicate with Defender for Endpoint, use one of the following methods to configure the MMA to use the proxy server:</span></span>

- [<span data-ttu-id="e736a-158">Configurer MMA pour utiliser un serveur proxy</span><span class="sxs-lookup"><span data-stu-id="e736a-158">Configure the MMA to use a proxy server</span></span>](/azure/azure-monitor/platform/agent-windows#install-agent-using-setup-wizard)

- [<span data-ttu-id="e736a-159">Configurer Windows pour utiliser un serveur proxy pour toutes les connexions</span><span class="sxs-lookup"><span data-stu-id="e736a-159">Configure Windows to use a proxy server for all connections</span></span>](configure-proxy-internet.md)

<span data-ttu-id="e736a-160">Si un proxy ou un pare-feu est en cours d’utilisation, assurez-vous que les serveurs peuvent accéder à toutes les URL du service Microsoft Defender for Endpoint directement et sans interception SSL.</span><span class="sxs-lookup"><span data-stu-id="e736a-160">If a proxy or firewall is in use, please ensure that servers can access all of the Microsoft Defender for Endpoint service URLs directly and without SSL interception.</span></span> <span data-ttu-id="e736a-161">Pour plus d’informations, voir [activer l’accès aux URL du service Defender for Endpoint.](configure-proxy-internet.md#enable-access-to-microsoft-defender-for-endpoint-service-urls-in-the-proxy-server)</span><span class="sxs-lookup"><span data-stu-id="e736a-161">For more information, see [enable access to Defender for Endpoint service URLs](configure-proxy-internet.md#enable-access-to-microsoft-defender-for-endpoint-service-urls-in-the-proxy-server).</span></span> <span data-ttu-id="e736a-162">L’utilisation de l’interception SSL empêche le système de communiquer avec le service Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="e736a-162">Use of SSL interception will prevent the system from communicating with the Defender for Endpoint service.</span></span>

<span data-ttu-id="e736a-163">Une fois terminé, vous devriez voir les serveurs Windows intégrés dans le portail dans un délai d’une heure.</span><span class="sxs-lookup"><span data-stu-id="e736a-163">Once completed, you should see onboarded Windows servers in the portal within an hour.</span></span>

### <a name="option-2-onboard-windows-servers-through-azure-security-center"></a><span data-ttu-id="e736a-164">Option 2 : intégrer des serveurs Windows par le biais du Centre de sécurité Azure</span><span class="sxs-lookup"><span data-stu-id="e736a-164">Option 2: Onboard Windows servers through Azure Security Center</span></span>

1. <span data-ttu-id="e736a-165">Dans le volet Centre de sécurité Microsoft Defender navigation, **sélectionnez** Paramètres  >  **intégration de la gestion des**  >  **appareils.**</span><span class="sxs-lookup"><span data-stu-id="e736a-165">In the Microsoft Defender Security Center navigation pane, select **Settings** > **Device management** > **Onboarding**.</span></span>

2. <span data-ttu-id="e736a-166">Sélectionnez **Windows Server 2008 R2 SP1, 2012 R2 et 2016** comme système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="e736a-166">Select **Windows Server 2008 R2 SP1, 2012 R2 and 2016** as the operating system.</span></span>

3. <span data-ttu-id="e736a-167">Cliquez **sur Serveurs intégrés dans le Centre de sécurité Azure.**</span><span class="sxs-lookup"><span data-stu-id="e736a-167">Click **Onboard Servers in Azure Security Center**.</span></span>

4. <span data-ttu-id="e736a-168">Suivez les instructions d’intégration dans [Microsoft Defender pour point](/azure/security-center/security-center-wdatp) de terminaison avec Azure Defender et si vous utilisez Azure ARC, suivez les instructions d’intégration dans l’activation de Microsoft Defender pour l’intégration de point de [terminaison.](/azure/security-center/security-center-wdatp#enabling-the-microsoft-defender-for-endpoint-integration)</span><span class="sxs-lookup"><span data-stu-id="e736a-168">Follow the onboarding instructions in [Microsoft Defender for Endpoint with Azure Defender](/azure/security-center/security-center-wdatp) and If you are using Azure ARC, Follow the onboarding instructions in [Enabling the Microsoft Defender for Endpoint integration](/azure/security-center/security-center-wdatp#enabling-the-microsoft-defender-for-endpoint-integration).</span></span>

<span data-ttu-id="e736a-169">Après avoir effectué les étapes d’intégration, vous devez configurer et mettre à jour [System Center Endpoint Protection clients.](#configure-and-update-system-center-endpoint-protection-clients)</span><span class="sxs-lookup"><span data-stu-id="e736a-169">After completing the onboarding steps, you'll need to [Configure and update System Center Endpoint Protection clients](#configure-and-update-system-center-endpoint-protection-clients).</span></span>

> [!NOTE]
>
> - <span data-ttu-id="e736a-170">Pour que l’intégration via Azure Defender for Servers fonctionne comme prévu, le serveur doit avoir un espace de travail et une clé appropriés configurés dans les paramètres Microsoft Monitoring Agent (MMA).</span><span class="sxs-lookup"><span data-stu-id="e736a-170">For onboarding via Azure Defender for Servers to work as expected, the server must have an appropriate workspace and key configured within the Microsoft Monitoring Agent (MMA) settings.</span></span>
> - <span data-ttu-id="e736a-171">Une fois configuré, le pack d’administration cloud approprié est déployé sur l’ordinateur et le processus de capteur (MsSenseS.exe) est déployé et démarré.</span><span class="sxs-lookup"><span data-stu-id="e736a-171">Once configured, the appropriate cloud management pack is deployed on the machine and the sensor process (MsSenseS.exe) will be deployed and started.</span></span>
> - <span data-ttu-id="e736a-172">Cette configuration est également requise si le serveur est configuré pour utiliser un serveur de passerelle OMS comme proxy.</span><span class="sxs-lookup"><span data-stu-id="e736a-172">This is also required if the server is configured to use an OMS Gateway server as proxy.</span></span>

### <a name="option-3-onboard-windows-servers-through-microsoft-endpoint-manager-version-2002-and-later"></a><span data-ttu-id="e736a-173">Option 3 : intégrer Windows serveurs Microsoft Endpoint Manager version 2002 et ultérieures</span><span class="sxs-lookup"><span data-stu-id="e736a-173">Option 3: Onboard Windows servers through Microsoft Endpoint Manager version 2002 and later</span></span>

<span data-ttu-id="e736a-174">Vous pouvez intégrer Windows Server 2012 R2 et Windows Server 2016 en utilisant Microsoft Endpoint Manager version 2002 et ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e736a-174">You can onboard Windows Server 2012 R2 and Windows Server 2016 by using Microsoft Endpoint Manager version 2002 and later.</span></span> <span data-ttu-id="e736a-175">Pour plus d’informations, [voir Microsoft Defender for Endpoint in Microsoft Endpoint Manager current branch](/mem/configmgr/protect/deploy-use/defender-advanced-threat-protection).</span><span class="sxs-lookup"><span data-stu-id="e736a-175">For more information, see [Microsoft Defender for Endpoint in Microsoft Endpoint Manager current branch](/mem/configmgr/protect/deploy-use/defender-advanced-threat-protection).</span></span>

<span data-ttu-id="e736a-176">Après avoir effectué les étapes d’intégration, vous devez configurer et mettre à jour [System Center Endpoint Protection clients.](#configure-and-update-system-center-endpoint-protection-clients)</span><span class="sxs-lookup"><span data-stu-id="e736a-176">After completing the onboarding steps, you'll need to [Configure and update System Center Endpoint Protection clients](#configure-and-update-system-center-endpoint-protection-clients).</span></span>

## <a name="windows-server-sac-version-1803-windows-server-2019-and-windows-server-2019-core-edition"></a><span data-ttu-id="e736a-177">Windows Server (SAC) version 1803, Windows Server 2019 et Windows Server 2019 Core Edition</span><span class="sxs-lookup"><span data-stu-id="e736a-177">Windows Server (SAC) version 1803, Windows Server 2019, and Windows Server 2019 Core edition</span></span>

<span data-ttu-id="e736a-178">Vous pouvez intégrer Windows Server (SAC) version 1803, Windows Server 2019 ou Windows Server 2019 Core edition en utilisant les méthodes de déploiement suivantes :</span><span class="sxs-lookup"><span data-stu-id="e736a-178">You can onboard Windows Server (SAC) version 1803, Windows Server 2019, or Windows Server 2019 Core edition by using the following deployment methods:</span></span>

- [<span data-ttu-id="e736a-179">Script local</span><span class="sxs-lookup"><span data-stu-id="e736a-179">Local script</span></span>](configure-endpoints-script.md)
- [<span data-ttu-id="e736a-180">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e736a-180">Group Policy</span></span>](configure-endpoints-gp.md)
- [<span data-ttu-id="e736a-181">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="e736a-181">Microsoft Endpoint Configuration Manager</span></span>](configure-endpoints-sccm.md)
- [<span data-ttu-id="e736a-182">System Center Configuration Manager 2012 / 2012 R2 1511 / 1602</span><span class="sxs-lookup"><span data-stu-id="e736a-182">System Center Configuration Manager 2012 / 2012 R2  1511 / 1602</span></span>](configure-endpoints-sccm.md#onboard-devices-using-system-center-configuration-manager)
- [<span data-ttu-id="e736a-183">Scripts d’intégration VDI pour les appareils non persistants</span><span class="sxs-lookup"><span data-stu-id="e736a-183">VDI onboarding scripts for non-persistent devices</span></span>](configure-endpoints-vdi.md)

> [!NOTE]
>
> - <span data-ttu-id="e736a-184">Le package d’intégration pour Windows Server 2019 à 2019 Microsoft Endpoint Manager actuellement un script.</span><span class="sxs-lookup"><span data-stu-id="e736a-184">The Onboarding package for Windows Server 2019 through Microsoft Endpoint Manager currently ships a script.</span></span> <span data-ttu-id="e736a-185">Pour plus d’informations sur le déploiement de scripts dans Configuration Manager, voir [Packages et programmes dans Configuration Manager.](/configmgr/apps/deploy-use/packages-and-programs)</span><span class="sxs-lookup"><span data-stu-id="e736a-185">For more information on how to deploy scripts in Configuration Manager, see [Packages and programs in Configuration Manager](/configmgr/apps/deploy-use/packages-and-programs).</span></span>
> - <span data-ttu-id="e736a-186">Un script local convient pour une preuve de concept, mais ne doit pas être utilisé pour le déploiement de production.</span><span class="sxs-lookup"><span data-stu-id="e736a-186">A local script is suitable for a proof of concept but should not be used for production deployment.</span></span> <span data-ttu-id="e736a-187">Pour un déploiement de production, nous vous recommandons d’utiliser une stratégie de groupe ou Microsoft Endpoint Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="e736a-187">For a production deployment, we recommend using Group Policy, or Microsoft Endpoint Configuration Manager.</span></span>

<span data-ttu-id="e736a-188">La prise en charge de Windows Server fournit des informations plus approfondies sur les activités du serveur, la couverture de la détection des attaques du noyau et de la mémoire, et permet des actions de réponse.</span><span class="sxs-lookup"><span data-stu-id="e736a-188">Support for Windows Server provides deeper insight into server activities, coverage for kernel and memory attack detection, and enables response actions.</span></span>

1. <span data-ttu-id="e736a-189">Configurez Defender pour les paramètres d’intégration de point de terminaison sur le serveur Windows à l’aide des mêmes outils et méthodes pour Windows 10 périphériques.</span><span class="sxs-lookup"><span data-stu-id="e736a-189">Configure Defender for Endpoint onboarding settings on the Windows server using the same tools and methods for Windows 10 devices.</span></span> <span data-ttu-id="e736a-190">Pour plus d’informations, [voir Appareils Windows 10 intégrés.](configure-endpoints.md)</span><span class="sxs-lookup"><span data-stu-id="e736a-190">For more information, see [Onboard Windows 10 devices](configure-endpoints.md).</span></span>

2. <span data-ttu-id="e736a-191">Si vous exécutez une solution anti-programme malveillant tierce, vous devez appliquer les paramètres suivants du mode passif de l’Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="e736a-191">If you're running a third-party anti-malware solution, you'll need to apply the following Microsoft Defender AV passive mode settings.</span></span> <span data-ttu-id="e736a-192">Vérifiez qu’elle a été configurée correctement :</span><span class="sxs-lookup"><span data-stu-id="e736a-192">Verify that it was configured correctly:</span></span>

    1. <span data-ttu-id="e736a-193">Définissez l’entrée de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="e736a-193">Set the following registry entry:</span></span>
       - <span data-ttu-id="e736a-194">Chemin d’accès : `HKLM\SOFTWARE\Policies\Microsoft\Windows Advanced Threat Protection`</span><span class="sxs-lookup"><span data-stu-id="e736a-194">Path: `HKLM\SOFTWARE\Policies\Microsoft\Windows Advanced Threat Protection`</span></span>
       - <span data-ttu-id="e736a-195">Nom : ForceDefenderPassiveMode</span><span class="sxs-lookup"><span data-stu-id="e736a-195">Name: ForceDefenderPassiveMode</span></span>
       - <span data-ttu-id="e736a-196">Type : REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="e736a-196">Type: REG_DWORD</span></span>
       - <span data-ttu-id="e736a-197">Value: 1</span><span class="sxs-lookup"><span data-stu-id="e736a-197">Value: 1</span></span>

    1. <span data-ttu-id="e736a-198">Exécutez la commande PowerShell suivante pour vérifier que le mode passif a été configuré :</span><span class="sxs-lookup"><span data-stu-id="e736a-198">Run the following PowerShell command to verify that the passive mode was configured:</span></span>

       ```PowerShell
       Get-WinEvent -FilterHashtable @{ProviderName="Microsoft-Windows-Sense" ;ID=84}
       ```

    1. <span data-ttu-id="e736a-199">Confirmez qu’un événement récent contenant l’événement en mode passif est trouvé :</span><span class="sxs-lookup"><span data-stu-id="e736a-199">Confirm  that a recent event containing the passive mode event is found:</span></span>

       ![Image du résultat de vérification du mode passif](images/atp-verify-passive-mode.png)

3. <span data-ttu-id="e736a-201">Exécutez la commande suivante pour vérifier si Microsoft Defender AV est installé :</span><span class="sxs-lookup"><span data-stu-id="e736a-201">Run the following command to check if Microsoft Defender AV is installed:</span></span>

   ```sc.exe query Windefend```

    <span data-ttu-id="e736a-202">Si le résultat est « Le service spécifié n’existe pas en tant que service installé » , vous devez installer Microsoft Defender AV.</span><span class="sxs-lookup"><span data-stu-id="e736a-202">If the result is 'The specified service doesn't exist as an installed service', then you'll need to install Microsoft Defender AV.</span></span> <span data-ttu-id="e736a-203">Pour plus d’informations, [voir Antivirus Microsoft Defender dans Windows 10](/windows/security/threat-protection/microsoft-defender-antivirus/microsoft-defender-antivirus-in-windows-10).</span><span class="sxs-lookup"><span data-stu-id="e736a-203">For more information, see [Microsoft Defender Antivirus in Windows 10](/windows/security/threat-protection/microsoft-defender-antivirus/microsoft-defender-antivirus-in-windows-10).</span></span>

    <span data-ttu-id="e736a-204">Pour plus d’informations sur l’utilisation de la stratégie de groupe pour configurer et gérer des Antivirus Microsoft Defender sur vos serveurs Windows, voir Utiliser les [paramètres](/windows/security/threat-protection/microsoft-defender-antivirus/use-group-policy-microsoft-defender-antivirus)de stratégie de groupe pour configurer et gérer Antivirus Microsoft Defender .</span><span class="sxs-lookup"><span data-stu-id="e736a-204">For information on how to use Group Policy to configure and manage Microsoft Defender Antivirus on your Windows servers, see [Use Group Policy settings to configure and manage Microsoft Defender Antivirus](/windows/security/threat-protection/microsoft-defender-antivirus/use-group-policy-microsoft-defender-antivirus).</span></span>

## <a name="integration-with-azure-defender"></a><span data-ttu-id="e736a-205">Intégration à Azure Defender</span><span class="sxs-lookup"><span data-stu-id="e736a-205">Integration with Azure Defender</span></span>

<span data-ttu-id="e736a-206">Defender for Endpoint peut s’intégrer à Azure Defender pour fournir une solution de protection Windows serveur complète.</span><span class="sxs-lookup"><span data-stu-id="e736a-206">Defender for Endpoint can integrate with Azure Defender to provide a comprehensive Windows server protection solution.</span></span> <span data-ttu-id="e736a-207">Avec cette intégration, Azure Defender peut utiliser la puissance de Defender for Endpoint pour fournir une détection améliorée des menaces pour Windows serveurs.</span><span class="sxs-lookup"><span data-stu-id="e736a-207">With this integration, Azure Defender can use the power of Defender for Endpoint to provide improved threat detection for Windows Servers.</span></span>

<span data-ttu-id="e736a-208">Les fonctionnalités suivantes sont incluses dans cette intégration :</span><span class="sxs-lookup"><span data-stu-id="e736a-208">The following capabilities are included in this integration:</span></span>

- <span data-ttu-id="e736a-209">Intégration automatisée : le capteur Defender for Endpoint est automatiquement activé sur les serveurs Windows intégrés à Azure Defender.</span><span class="sxs-lookup"><span data-stu-id="e736a-209">Automated onboarding - Defender for Endpoint sensor is automatically enabled on Windows Servers that are onboarded to Azure Defender.</span></span> <span data-ttu-id="e736a-210">Pour plus d’informations sur l’intégration d’Azure Defender, voir Utiliser la [licence Microsoft Defender for Endpoint intégrée.](/azure/security-center/security-center-wdatp)</span><span class="sxs-lookup"><span data-stu-id="e736a-210">For more information on Azure Defender onboarding, see [Use the integrated Microsoft Defender for Endpoint license](/azure/security-center/security-center-wdatp).</span></span>

    > [!NOTE]
    > <span data-ttu-id="e736a-211">L’intégration entre Azure Defender pour serveurs et Microsoft Defender pour point de terminaison a été étendue pour prendre en charge [Windows Server 2019 et Windows Virtual Desktop (WVD).](/azure/security-center/release-notes#microsoft-defender-for-endpoint-integration-with-azure-defender-now-supports-windows-server-2019-and-windows-10-virtual-desktop-wvd-in-preview)</span><span class="sxs-lookup"><span data-stu-id="e736a-211">The integration between Azure Defender for Servers and Microsoft Defender for Endpoint has been expanded to support [Windows Server 2019 and Windows Virtual Desktop (WVD)](/azure/security-center/release-notes#microsoft-defender-for-endpoint-integration-with-azure-defender-now-supports-windows-server-2019-and-windows-10-virtual-desktop-wvd-in-preview).</span></span>

- <span data-ttu-id="e736a-212">Windows serveurs surveillés par Azure Defender seront également disponibles dans Defender pour le point de terminaison : Azure Defender se connecte en toute transparence au client Defender for Endpoint, fournissant une vue unique sur les clients et les serveurs.</span><span class="sxs-lookup"><span data-stu-id="e736a-212">Windows servers monitored by Azure Defender will also be available in Defender for Endpoint - Azure Defender seamlessly connects to the Defender for Endpoint tenant, providing a single view across clients and servers.</span></span>  <span data-ttu-id="e736a-213">En outre, les alertes Defender pour le point de terminaison seront disponibles dans la console Azure Defender.</span><span class="sxs-lookup"><span data-stu-id="e736a-213">In addition, Defender for Endpoint alerts will be available in the Azure Defender console.</span></span>
- <span data-ttu-id="e736a-214">Enquête sur le serveur : les clients Azure Defender peuvent accéder Centre de sécurité Microsoft Defender pour effectuer une enquête détaillée afin de découvrir l’étendue d’une violation potentielle.</span><span class="sxs-lookup"><span data-stu-id="e736a-214">Server investigation -  Azure Defender customers can access Microsoft Defender Security Center to perform detailed investigation to uncover the scope of a potential breach.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="e736a-215">Lorsque vous utilisez Azure Defender pour surveiller les serveurs, un client Defender pour point de terminaison est automatiquement créé (aux États-Unis pour les utilisateurs américains, dans l’UE pour les utilisateurs européens et anglais).</span><span class="sxs-lookup"><span data-stu-id="e736a-215">When you use Azure Defender to monitor servers, a Defender for Endpoint tenant is automatically created (in the US for US users, in the EU for European and UK users).</span></span><br>
<span data-ttu-id="e736a-216">Les données collectées par Defender pour endpoint sont stockées dans l’emplacement géographique du client, comme identifié lors de l’approvisionnement.</span><span class="sxs-lookup"><span data-stu-id="e736a-216">Data collected by Defender for Endpoint is stored in the geo-location of the tenant as identified during provisioning.</span></span>
> - <span data-ttu-id="e736a-217">Si vous utilisez Defender pour Endpoint avant d’utiliser Azure Defender, vos données seront stockées à l’emplacement que vous avez spécifié lors de la création de votre client, même si vous intégrez Azure Defender ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="e736a-217">If you use Defender for Endpoint before using Azure Defender, your data will be stored in the location you specified when you created your tenant even if you integrate with Azure Defender at a later time.</span></span>
> - <span data-ttu-id="e736a-218">Une fois configuré, vous ne pouvez pas modifier l’emplacement où vos données sont stockées.</span><span class="sxs-lookup"><span data-stu-id="e736a-218">Once configured, you cannot change the location where your data is stored.</span></span> <span data-ttu-id="e736a-219">Si vous devez déplacer vos données vers un autre emplacement, vous devez contacter le Support Microsoft pour réinitialiser le client.</span><span class="sxs-lookup"><span data-stu-id="e736a-219">If you need to move your data to another location, you need to contact Microsoft Support to reset the tenant.</span></span> <br>
<span data-ttu-id="e736a-220">La surveillance des points de terminaison de serveur utilisant cette intégration a été désactivée pour Office 365 Cloud de la communauté du secteur public clients.</span><span class="sxs-lookup"><span data-stu-id="e736a-220">Server endpoint monitoring utilizing this integration has been disabled for Office 365 GCC customers.</span></span>

## <a name="configure-and-update-system-center-endpoint-protection-clients"></a><span data-ttu-id="e736a-221">Configurer et mettre à jour System Center Endpoint Protection clients</span><span class="sxs-lookup"><span data-stu-id="e736a-221">Configure and update System Center Endpoint Protection clients</span></span>

<span data-ttu-id="e736a-222">Defender pour le point de terminaison s’intègre à System Center Endpoint Protection.</span><span class="sxs-lookup"><span data-stu-id="e736a-222">Defender for Endpoint integrates with System Center Endpoint Protection.</span></span> <span data-ttu-id="e736a-223">L’intégration offre une visibilité sur les détections de programmes malveillants et pour arrêter la propagation d’une attaque dans votre organisation en interdit les fichiers potentiellement malveillants ou les programmes malveillants suspectés.</span><span class="sxs-lookup"><span data-stu-id="e736a-223">The integration provides visibility to malware detections and to stop propagation of an attack in your organization by banning potentially malicious files or suspected malware.</span></span>

<span data-ttu-id="e736a-224">Les étapes suivantes sont nécessaires pour activer cette intégration :</span><span class="sxs-lookup"><span data-stu-id="e736a-224">The following steps are required to enable this integration:</span></span>

- <span data-ttu-id="e736a-225">Installez la mise à jour de la plateforme anti-programme malveillant de janvier [2017 pour Endpoint Protection clients.](https://support.microsoft.com/help/3209361/january-2017-anti-malware-platform-update-for-endpoint-protection-clie)</span><span class="sxs-lookup"><span data-stu-id="e736a-225">Install the [January 2017 anti-malware platform update for Endpoint Protection clients](https://support.microsoft.com/help/3209361/january-2017-anti-malware-platform-update-for-endpoint-protection-clie).</span></span>

- <span data-ttu-id="e736a-226">[Configurez l’appartenance au service protection cloud client SCEP](/windows/security/threat-protection/microsoft-defender-antivirus/enable-cloud-protection-microsoft-defender-antivirus) sur **le paramètre** Avancé.</span><span class="sxs-lookup"><span data-stu-id="e736a-226">[Configure the SCEP client Cloud Protection Service membership](/windows/security/threat-protection/microsoft-defender-antivirus/enable-cloud-protection-microsoft-defender-antivirus) to the **Advanced** setting.</span></span>

## <a name="offboard-windows-servers"></a><span data-ttu-id="e736a-227">Serveurs de Windows de tableau de bord</span><span class="sxs-lookup"><span data-stu-id="e736a-227">Offboard Windows servers</span></span>

<span data-ttu-id="e736a-228">Vous pouvez désinserrez Windows Server (SAC), Windows Server 2019 et Windows Server 2019 Core edition dans la même méthode disponible pour Windows 10 clients.</span><span class="sxs-lookup"><span data-stu-id="e736a-228">You can offboard Windows Server (SAC), Windows Server 2019, and Windows Server 2019 Core edition in the same method available for Windows 10 client devices.</span></span>

<span data-ttu-id="e736a-229">Pour les autres versions Windows serveur, deux options s’offrent à vous pour Windows serveurs du service :</span><span class="sxs-lookup"><span data-stu-id="e736a-229">For other Windows server versions, you have two options to offboard Windows servers from the service:</span></span>

- <span data-ttu-id="e736a-230">Désinstaller l’agent MMA</span><span class="sxs-lookup"><span data-stu-id="e736a-230">Uninstall the MMA agent</span></span>
- <span data-ttu-id="e736a-231">Supprimer la configuration de l’espace de travail Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="e736a-231">Remove the Defender for Endpoint workspace configuration</span></span>

> [!NOTE]
> <span data-ttu-id="e736a-232">Laboarding entraîne l’arrêt par le serveur Windows de l’envoi de données de capteur au portail, mais les données du serveur Windows, y compris la référence aux alertes qu’il avait, seront conservées pendant 6 mois.</span><span class="sxs-lookup"><span data-stu-id="e736a-232">Offboarding causes the Windows server to stop sending sensor data to the portal but data from the Windows server, including reference to any alerts it has had will be retained for up to 6 months.</span></span>

### <a name="uninstall-windows-servers-by-uninstalling-the-mma-agent"></a><span data-ttu-id="e736a-233">Désinstaller Windows serveurs en désinstallant l’agent MMA</span><span class="sxs-lookup"><span data-stu-id="e736a-233">Uninstall Windows servers by uninstalling the MMA agent</span></span>

<span data-ttu-id="e736a-234">Pour désinstaller le serveur Windows, vous pouvez désinstaller l’agent MMA du serveur Windows ou le détacher des rapports à votre espace de travail Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="e736a-234">To offboard the Windows server, you can uninstall the MMA agent from the Windows server or detach it from reporting to your Defender for Endpoint workspace.</span></span> <span data-ttu-id="e736a-235">Après l’arrêt de l’agent, le serveur Windows n’envoie plus de données de capteur à Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="e736a-235">After offboarding the agent, the Windows server will no longer send sensor data to Defender for Endpoint.</span></span>
<span data-ttu-id="e736a-236">Pour plus d’informations, [voir Pour désactiver un agent.](/azure/log-analytics/log-analytics-windows-agents#to-disable-an-agent)</span><span class="sxs-lookup"><span data-stu-id="e736a-236">For more information, see [To disable an agent](/azure/log-analytics/log-analytics-windows-agents#to-disable-an-agent).</span></span>

### <a name="remove-the-defender-for-endpoint-workspace-configuration"></a><span data-ttu-id="e736a-237">Supprimer la configuration de l’espace de travail Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="e736a-237">Remove the Defender for Endpoint workspace configuration</span></span>

<span data-ttu-id="e736a-238">Pour mettre hors service Windows serveur, vous pouvez utiliser l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="e736a-238">To offboard the Windows server, you can use either of the following methods:</span></span>

- <span data-ttu-id="e736a-239">Supprimer la configuration de l’espace de travail Defender for Endpoint de l’agent MMA</span><span class="sxs-lookup"><span data-stu-id="e736a-239">Remove the Defender for Endpoint workspace configuration from the MMA agent</span></span>
- <span data-ttu-id="e736a-240">Exécuter une commande PowerShell pour supprimer la configuration</span><span class="sxs-lookup"><span data-stu-id="e736a-240">Run a PowerShell command to remove the configuration</span></span>

#### <a name="remove-the-defender-for-endpoint-workspace-configuration-from-the-mma-agent"></a><span data-ttu-id="e736a-241">Supprimer la configuration de l’espace de travail Defender for Endpoint de l’agent MMA</span><span class="sxs-lookup"><span data-stu-id="e736a-241">Remove the Defender for Endpoint workspace configuration from the MMA agent</span></span>

1. <span data-ttu-id="e736a-242">Dans la **Microsoft Monitoring Agent propriétés,** sélectionnez **l’onglet Azure Log Analytics (OMS).**</span><span class="sxs-lookup"><span data-stu-id="e736a-242">In the **Microsoft Monitoring Agent Properties**, select the **Azure Log Analytics (OMS)** tab.</span></span>

2. <span data-ttu-id="e736a-243">Sélectionnez l’espace de travail Defender pour le point de terminaison, puis cliquez sur **Supprimer.**</span><span class="sxs-lookup"><span data-stu-id="e736a-243">Select the Defender for Endpoint workspace, and click **Remove**.</span></span>

    ![Image des propriétés Microsoft Monitoring Agent de l’entreprise](images/atp-mma.png)

#### <a name="run-a-powershell-command-to-remove-the-configuration"></a><span data-ttu-id="e736a-245">Exécuter une commande PowerShell pour supprimer la configuration</span><span class="sxs-lookup"><span data-stu-id="e736a-245">Run a PowerShell command to remove the configuration</span></span>

1. <span data-ttu-id="e736a-246">Obtenez votre ID d’espace de travail :</span><span class="sxs-lookup"><span data-stu-id="e736a-246">Get your Workspace ID:</span></span>

   1. <span data-ttu-id="e736a-247">Dans le volet de navigation, sélectionnez  >  **Paramètres’intégration.**</span><span class="sxs-lookup"><span data-stu-id="e736a-247">In the navigation pane, select **Settings** > **Onboarding**.</span></span>

   1. <span data-ttu-id="e736a-248">Sélectionnez **Windows Server 2008 R2 SP1, 2012 R2 et 2016** comme système d’exploitation et obtenez votre ID d’espace de travail :</span><span class="sxs-lookup"><span data-stu-id="e736a-248">Select **Windows Server 2008 R2 SP1, 2012 R2 and 2016** as the operating system and get your Workspace ID:</span></span>

      ![Image de l’intégration Windows serveur](images/atp-server-offboarding-workspaceid.png)

2. <span data-ttu-id="e736a-250&quot;>Ouvrez un PowerShell élevé et exécutez la commande suivante.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;e736a-250&quot;>Open an elevated PowerShell and run the following command.</span></span> <span data-ttu-id=&quot;e736a-251&quot;>Utilisez l’ID d’espace de travail que vous avez obtenu et remplacez `WorkspaceID` :</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;e736a-251&quot;>Use the Workspace ID you obtained and replacing `WorkspaceID`:</span></span>

    ```powershell
    $ErrorActionPreference = &quot;SilentlyContinue&quot;
    # Load agent scripting object
    $AgentCfg = New-Object -ComObject AgentConfigManager.MgmtSvcCfg
    # Remove OMS Workspace
    $AgentCfg.RemoveCloudWorkspace(&quot;WorkspaceID")
    # Reload the configuration and apply changes
    $AgentCfg.ReloadConfiguration()

    ```

## <a name="onboarding-servers-with-no-management-solution"></a><span data-ttu-id="e736a-252">Intégration de serveurs sans solution de gestion</span><span class="sxs-lookup"><span data-stu-id="e736a-252">Onboarding Servers with no management solution</span></span>

### <a name="using-group-policy"></a><span data-ttu-id="e736a-253">Utilisation de la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e736a-253">Using Group Policy</span></span>

<span data-ttu-id="e736a-254">**Étape 1 : Créez les fichiers nécessaires à copier sur les serveurs.**</span><span class="sxs-lookup"><span data-stu-id="e736a-254">**Step-1: Create the necessary files to copy down to the servers.**</span></span>

1. <span data-ttu-id="e736a-255">Accédez à c:\windows\sysvol\domain\scripts (le contrôle de modification peut être nécessaire sur l’un des contrôleurs de domaine.)</span><span class="sxs-lookup"><span data-stu-id="e736a-255">Navigate to c:\windows\sysvol\domain\scripts (Change control could be needed on one of the domain controllers.)</span></span>
1. <span data-ttu-id="e736a-256">Créez un dossier nommé MMA.</span><span class="sxs-lookup"><span data-stu-id="e736a-256">Create a folder named MMA.</span></span>
1. <span data-ttu-id="e736a-257">Téléchargez les données suivantes et placez-les dans le dossier MMA :</span><span class="sxs-lookup"><span data-stu-id="e736a-257">Download the following and place in the MMA folder:</span></span>

    <span data-ttu-id="e736a-258">**Mise à jour pour la télémétrie de diagnostic et d’expérience client (Windows Server 2008 R2 et Windows Server 2012 R2)**</span><span class="sxs-lookup"><span data-stu-id="e736a-258">**Update for customer experience and diagnostic telemetry (Windows Server 2008 R2 and Windows Server 2012 R2)**</span></span>

    [<span data-ttu-id="e736a-259">Pour Windows 2008 R2 x64</span><span class="sxs-lookup"><span data-stu-id="e736a-259">For Windows 2008 R2 x64</span></span>](https://www.microsoft.com/download/details.aspx?familyid=1bd1d18d-4631-4d8e-a897-327925765f71)

    [<span data-ttu-id="e736a-260">Pour Windows 2012 R2 x64</span><span class="sxs-lookup"><span data-stu-id="e736a-260">For Windows 2012 R2 x64</span></span>](https://www.microsoft.com/download/details.aspx?familyid=94cf6d85-017a-4c4c-afca-7d00721b500f)

    > [!NOTE]
    > <span data-ttu-id="e736a-261">Cet article suppose que vous utilisez des serveurs x64 (agent MMA .exe x64 [nouvelle version compatible SHA-2](https://go.microsoft.com/fwlink/?LinkId=828603))</span><span class="sxs-lookup"><span data-stu-id="e736a-261">This article assumes you are using x64-based servers (MMA Agent .exe x64 [New SHA-2 compliant version](https://go.microsoft.com/fwlink/?LinkId=828603))</span></span>

<span data-ttu-id="e736a-262">**Étape 2 : Créer un nom de fichier DeployMMA.cmd (à l’aide du bloc-notes)** Ajoutez les lignes suivantes au fichier cmd.</span><span class="sxs-lookup"><span data-stu-id="e736a-262">**Step-2: Create a file name DeployMMA.cmd (using notepad)** Add the following lines to the cmd file.</span></span> <span data-ttu-id="e736a-263">Notez que vous aurez besoin de votre ID d’espace de travail et de votre CLÉ.</span><span class="sxs-lookup"><span data-stu-id="e736a-263">Note that you'll need your WORKSPACE ID and KEY.</span></span>

```dos
@echo off 
cd "C:"
IF EXIST "C:\Program Files\Microsoft Monitoring Agent\Agent\MonitoringHost.exe" ( 
exit
) ELSE (
wusa.exe c:\Windows\MMA\Windows6.1-KB123456-x86.msu /quiet /norestart
wusa.exe c:\Windows\MMA\Windows8.1-KB123456-x86.msu /quiet /norestart
"c:\windows\MMA\MMASetup-AMD64.exe" /C:"setup.exe /qn ADD_OPINSIGHTS_WORKSPACE=1
OPINSIGHTS_WORKSPACE_ID=<your workspace ID>
OPINSIGHTS_WORKSPACE_KEY=<your workspace key>== AcceptEndUserLicenseAgreement=1"
)
```

## <a name="group-policy-configuration"></a><span data-ttu-id="e736a-264">Configuration de la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="e736a-264">Group Policy Configuration</span></span>

<span data-ttu-id="e736a-265">Créez une stratégie de groupe spécifique pour l’intégration d’appareils tels que « Microsoft Defender pour l’intégration de point de terminaison ».</span><span class="sxs-lookup"><span data-stu-id="e736a-265">Create a new group policy specifically for onboarding devices such as “Microsoft Defender for Endpoint Onboarding”.</span></span>

- <span data-ttu-id="e736a-266">Créer un dossier de stratégie de groupe nommé « c:\windows\MMA »</span><span class="sxs-lookup"><span data-stu-id="e736a-266">Create a Group Policy Folder named “c:\windows\MMA”</span></span>

     :::image type="content" source="images/grppolicyconfig1.png" alt-text="dossiers":::

    <span data-ttu-id="e736a-268">**Cela ajoute un nouveau dossier sur chaque serveur qui obtient l’GPO appliqué, appelé MMA, et qui sera stocké dans c:\windows. Il contient les fichiers d’installation pour le MMA, les éléments prérequis et le script d’installation.**</span><span class="sxs-lookup"><span data-stu-id="e736a-268">**This will add a new folder on every server that gets the GPO applied, called MMA, and will be stored in c:\windows. This will contain the installation files for the MMA, prerequisites, and install script.**</span></span>

- <span data-ttu-id="e736a-269">Créez une préférence de fichiers de stratégie de groupe pour chacun des fichiers stockés dans l’ouverture de boutique Net.</span><span class="sxs-lookup"><span data-stu-id="e736a-269">Create a Group Policy Files preference for each of the files stored in Net logon.</span></span>

     :::image type="content" source="images/grppolicyconfig2.png" alt-text="image1 de stratégie de groupe":::

<span data-ttu-id="e736a-271">Il copie les fichiers de DOMAIN\NETLOGON\MMA\filename vers C:\windows\MMA\filename , afin que les fichiers **d’installation** soient locaux sur le serveur :</span><span class="sxs-lookup"><span data-stu-id="e736a-271">It copies the files from DOMAIN\NETLOGON\MMA\filename to C:\windows\MMA\filename – **so the installation files are local to the server**:</span></span>

:::image type="content" source="images/deploymma.png" alt-text="déployer mma cmd":::

<span data-ttu-id="e736a-273">Pour les deux ko (l’un pour Windows Server 2008R2/Windows 7 et l’autre pour Windows Server 2012 R2), répétez le processus, mais créez un ciblage au niveau de l’élément sous l’onglet COMMON, afin que le fichier ne soit copié que vers la version de plateforme/système d’exploitation appropriée dans l’étendue :</span><span class="sxs-lookup"><span data-stu-id="e736a-273">For the two KBs (one for Windows Server 2008R2/Windows 7 and the other for Windows Server 2012 R2) repeat the process but create item level targeting on the COMMON tab, so the file only gets copied to the appropriate platform/Operating system version in scope:</span></span>

:::image type="content" source="images/targeteditor.png" alt-text="éditeur cible":::

- <span data-ttu-id="e736a-275">Pour Windows Server 2008 R2, vous avez besoin de Windows6.1-PROXY3080149-x64.msu (et uniquement copié).</span><span class="sxs-lookup"><span data-stu-id="e736a-275">For Windows Server 2008 R2 you need (and it will only copy down) Windows6.1-BJ3080149-x64.msu</span></span>
- <span data-ttu-id="e736a-276">Pour Windows Server 2012 R2, vous avez besoin de Windows8.1-COPI3080149-x64.msu (et uniquement copié).</span><span class="sxs-lookup"><span data-stu-id="e736a-276">For Windows Server 2012 R2 you need (and it will only copy down) Windows8.1-BJ3080149-x64.msu</span></span>

<span data-ttu-id="e736a-277">Une fois cette stratégie effectuée, vous devez créer une stratégie de script de démarrage :</span><span class="sxs-lookup"><span data-stu-id="e736a-277">Once this is done, you'll need to create a start-up script policy:</span></span>

:::image type="content" source="images/startupprops.png" alt-text="démarrer les propriétés":::

<span data-ttu-id="e736a-279">Le nom du fichier à exécuter ici est c:\windows\MMA\DeployMMA.cmd.</span><span class="sxs-lookup"><span data-stu-id="e736a-279">The name of the file to run here is c:\windows\MMA\DeployMMA.cmd.</span></span>
<span data-ttu-id="e736a-280">Une fois que le serveur est redémarré dans le cadre du processus de démarrage, il installe la mise à jour pour la base de données de télémétrie de diagnostic et d’expérience client, puis installe l’agent MMA, lors de la définition de l’ID et de la clé de l’espace de travail, et le serveur est intégré.</span><span class="sxs-lookup"><span data-stu-id="e736a-280">Once the server is restarted as part of the start-up process it will install the Update for customer experience and diagnostic telemetry KB, and then install the MMA Agent, while setting the Workspace ID and Key, and the server will be onboarded.</span></span>

<span data-ttu-id="e736a-281">Vous pouvez également utiliser une **tâche immédiate** pour exécuter le deployMMA.cmd si vous ne souhaitez pas redémarrer tous les serveurs.</span><span class="sxs-lookup"><span data-stu-id="e736a-281">You could also use an **immediate task** to run the deployMMA.cmd if you don't want to reboot all the servers.</span></span>
<span data-ttu-id="e736a-282">Cette étape peut être effectuée en deux phases.</span><span class="sxs-lookup"><span data-stu-id="e736a-282">This could be done in two phases.</span></span> <span data-ttu-id="e736a-283">Tout **d’abord,** créez les fichiers et le dossier dans GPO : donnez au système le temps de s’assurer que l’GPO a été appliqué et que tous les serveurs disposent des fichiers d’installation.</span><span class="sxs-lookup"><span data-stu-id="e736a-283">First create **the files and the folder in** GPO – Give the system time to ensure the GPO has been applied, and all the servers have the install files.</span></span> <span data-ttu-id="e736a-284">Ensuite, ajoutez la tâche immédiate.</span><span class="sxs-lookup"><span data-stu-id="e736a-284">Then, add the immediate task.</span></span> <span data-ttu-id="e736a-285">Cela permettra d’obtenir le même résultat sans nécessiter de redémarrage.</span><span class="sxs-lookup"><span data-stu-id="e736a-285">This will achieve the same result without requiring a reboot.</span></span>

<span data-ttu-id="e736a-286">Étant donné que le script dispose d’une méthode de sortie et ne se ré-exécute pas si le MMA est installé, vous pouvez également utiliser une tâche programmée quotidienne pour obtenir le même résultat.</span><span class="sxs-lookup"><span data-stu-id="e736a-286">As the Script has an exit method and wont re-run if the MMA is installed, you could also use a daily scheduled task to achieve the same result.</span></span> <span data-ttu-id="e736a-287">Similaire à une stratégie de conformité Configuration Manager qu’il vérifie quotidiennement pour s’assurer que le MMA est présent.</span><span class="sxs-lookup"><span data-stu-id="e736a-287">Similar to a Configuration Manager compliance policy it will check daily to ensure the MMA is present.</span></span>

:::image type="content" source="images/schtask.png" alt-text="planifier une tâche":::

:::image type="content" source="images/newtaskprops.png" alt-text="nouvelles propriétés de tâche":::

:::image type="content" source="images/deploymmadowmload.png" alt-text="déployer les props de téléchargement mma":::

:::image type="content" source="images/tasksch.png" alt-text="programmeur de tâches":::

<span data-ttu-id="e736a-292">Comme mentionné dans la documentation d’intégration pour Server spécifiquement autour de Server 2008 R2, voir ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="e736a-292">As mentioned in the onboarding documentation for Server specifically around Server 2008 R2 please see below:</span></span>

<span data-ttu-id="e736a-293">Pour Windows Server 2008 R2 PS1, veillez à respecter les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="e736a-293">For Windows Server 2008 R2 PS1, ensure that you fulfill the following requirements:</span></span>

- <span data-ttu-id="e736a-294">Installer le rapport de mise à jour mensuelle de [février 2018](https://support.microsoft.com/help/4074598/windows-7-update-kb4074598)</span><span class="sxs-lookup"><span data-stu-id="e736a-294">Install the [February 2018 monthly update rollup](https://support.microsoft.com/help/4074598/windows-7-update-kb4074598)</span></span>
  
- <span data-ttu-id="e736a-295">Installer [.NET Framework 4.5](https://www.microsoft.com/download/details.aspx?id=30653) (ou ultérieur) ou [KB3154518](https://support.microsoft.com/help/3154518/support-for-tls-system-default-versions-included-in-the-net-framework)</span><span class="sxs-lookup"><span data-stu-id="e736a-295">Install either [.NET framework 4.5](https://www.microsoft.com/download/details.aspx?id=30653) (or later) or [KB3154518](https://support.microsoft.com/help/3154518/support-for-tls-system-default-versions-included-in-the-net-framework)</span></span>

<span data-ttu-id="e736a-296">Vérifiez que les ko sont présents avant l’intégration de Windows Server 2008 R2. Ce processus vous permet d’intégrer tous les serveurs si configuration Manager ne gère pas les serveurs.</span><span class="sxs-lookup"><span data-stu-id="e736a-296">Please check the KBs are present before onboarding Windows Server 2008 R2 This process allows you to onboard all the servers if you don’t have Configuration Manager managing Servers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e736a-297">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e736a-297">Related topics</span></span>

- [<span data-ttu-id="e736a-298">Intégrer des appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="e736a-298">Onboard Windows 10 devices</span></span>](configure-endpoints.md)
- [<span data-ttu-id="e736a-299">Intégrer des appareils non Windows</span><span class="sxs-lookup"><span data-stu-id="e736a-299">Onboard non-Windows devices</span></span>](configure-endpoints-non-windows.md)
- [<span data-ttu-id="e736a-300">Configurer les paramètres de proxy et de connectivité Internet</span><span class="sxs-lookup"><span data-stu-id="e736a-300">Configure proxy and Internet connectivity settings</span></span>](configure-proxy-internet.md)
- [<span data-ttu-id="e736a-301">Exécuter un test de détection sur un appareil Defender pour point de terminaison nouvellement intégré</span><span class="sxs-lookup"><span data-stu-id="e736a-301">Run a detection test on a newly onboarded Defender for Endpoint device</span></span>](run-detection-test.md)
- [<span data-ttu-id="e736a-302">Résolution des problèmes d’intégration de Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="e736a-302">Troubleshooting Microsoft Defender for Endpoint onboarding issues</span></span>](troubleshoot-onboarding.md)
