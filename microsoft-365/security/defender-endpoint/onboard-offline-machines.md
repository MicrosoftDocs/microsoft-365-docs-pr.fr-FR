---
title: Appareils intégrés sans accès à Internet à Microsoft Defender pour le point de terminaison
ms.reviewer: ''
description: Intégrer des appareils sans accès à Internet afin qu’ils peuvent envoyer des données de capteur au capteur Microsoft Defender for Endpoint
keywords: onboard, servers, vm, on-premise, oms gateway, log analytics, azure log analytics, mma
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
ms.openlocfilehash: ed33f67695fddc78c0bac646f72ca0c48887bb04
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52844417"
---
# <a name="onboard-devices-without-internet-access-to-microsoft-defender-for-endpoint"></a><span data-ttu-id="edb6e-104">Appareils intégrés sans accès à Internet à Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="edb6e-104">Onboard devices without Internet access to Microsoft Defender for Endpoint</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="edb6e-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="edb6e-105">**Applies to:**</span></span>
- [<span data-ttu-id="edb6e-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="edb6e-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="edb6e-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="edb6e-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="edb6e-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="edb6e-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="edb6e-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="edb6e-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)


<span data-ttu-id="edb6e-110">Pour intégrer des appareils sans accès à Internet, vous devez suivre les étapes générales suivantes :</span><span class="sxs-lookup"><span data-stu-id="edb6e-110">To onboard devices without Internet access, you'll need to take the following general steps:</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="edb6e-111">Les étapes ci-dessous s’appliquent uniquement aux appareils exécutant des versions antérieures de Windows tels que : Windows Server 2016 et versions antérieures ou antérieures ou Windows 8.1 et versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="edb6e-111">The steps below are applicable only to devices running previous versions of Windows such as: Windows Server 2016 and earlier or Windows 8.1 and earlier.</span></span>

> [!NOTE]
> - <span data-ttu-id="edb6e-112">Un serveur de passerelle OMS ne peut pas être utilisé comme proxy pour les appareils Windows 10 ou Windows Server 2019 déconnectés lorsqu’ils sont configurés via le Registre ou l’GPO « TelemetryProxyServer ».</span><span class="sxs-lookup"><span data-stu-id="edb6e-112">An OMS gateway server cannot be used as proxy for disconnected Windows 10 or Windows Server 2019 devices when configured via 'TelemetryProxyServer' registry or GPO.</span></span>
> - <span data-ttu-id="edb6e-113">Pour Windows 10 ou Windows Server 2019 , alors que vous pouvez utiliser TelemetryProxyServer, il doit pointer vers un périphérique proxy ou une appliance standard.</span><span class="sxs-lookup"><span data-stu-id="edb6e-113">For Windows 10 or Windows Server 2019 - while you may use TelemetryProxyServer, it must point to a standard proxy device or appliance.</span></span>
> - <span data-ttu-id="edb6e-114">En outre, Windows 10 ou Windows Server 2019 dans les environnements déconnectés doivent être en mesure de mettre à jour les listes d’autorisation de certificat hors connexion via un fichier interne ou un serveur web.</span><span class="sxs-lookup"><span data-stu-id="edb6e-114">In addition, Windows 10 or Windows Server 2019 in disconnected environments must be able to update Certificate Trust Lists offline via an internal file or web server.</span></span>
> - <span data-ttu-id="edb6e-115">Pour plus d’informations sur la mise à jour des fichiers CTL hors connexion, voir Configurer un fichier ou un serveur web pour [télécharger les fichiers CTL.](/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/dn265983(v=ws.11)#configure-a-file-or-web-server-to-download-the-ctl-files)</span><span class="sxs-lookup"><span data-stu-id="edb6e-115">For more information about updating CTLs offline, see [Configure a file or web server to download the CTL files](/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/dn265983(v=ws.11)#configure-a-file-or-web-server-to-download-the-ctl-files).</span></span>

<span data-ttu-id="edb6e-116">Pour plus d’informations sur les méthodes d’intégration, consultez les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="edb6e-116">For more information about onboarding methods, see the following articles:</span></span>
- [<span data-ttu-id="edb6e-117">Intégrer des versions antérieures de Windows</span><span class="sxs-lookup"><span data-stu-id="edb6e-117">Onboard previous versions of Windows</span></span>](/microsoft-365/security/defender-endpoint/onboard-downlevel)
- [<span data-ttu-id="edb6e-118">Intégrer des serveurs au service Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="edb6e-118">Onboard servers to the Microsoft Defender for Endpoint service</span></span>](/microsoft-365/security/defender-endpoint/configure-server-endpoints#windows-server-2008-r2-sp1--windows-server-2012-r2-and-windows-server-2016)
- [<span data-ttu-id="edb6e-119">Configurer les paramètres de proxy du dispositif et de connectivité Internet</span><span class="sxs-lookup"><span data-stu-id="edb6e-119">Configure device proxy and Internet connectivity settings</span></span>](/microsoft-365/security/defender-endpoint/configure-proxy-internet#configure-the-proxy-server-manually-using-a-registry-based-static-proxy)

## <a name="on-premise-devices"></a><span data-ttu-id="edb6e-120">Appareils locaux</span><span class="sxs-lookup"><span data-stu-id="edb6e-120">On-premise devices</span></span>

- <span data-ttu-id="edb6e-121">Configurer Azure Log Analytics (anciennement appelé passerelle OMS) pour qu’il agisse en tant que proxy ou hub :</span><span class="sxs-lookup"><span data-stu-id="edb6e-121">Setup Azure Log Analytics (formerly known as OMS Gateway) to act as proxy or hub:</span></span>
  - [<span data-ttu-id="edb6e-122">Azure Log Analytics Agent</span><span class="sxs-lookup"><span data-stu-id="edb6e-122">Azure Log Analytics Agent</span></span>](/azure/azure-monitor/platform/gateway#download-the-log-analytics-gateway)
  - <span data-ttu-id="edb6e-123">[Installer et configurer un point Microsoft Monitoring Agent (MMA)](configure-server-endpoints.md#install-and-configure-microsoft-monitoring-agent-mma-to-report-sensor-data-to-microsoft-defender-for-endpoint) vers la clé d’espace de travail Defender for Endpoint & ID</span><span class="sxs-lookup"><span data-stu-id="edb6e-123">[Install and configure Microsoft Monitoring Agent (MMA)](configure-server-endpoints.md#install-and-configure-microsoft-monitoring-agent-mma-to-report-sensor-data-to-microsoft-defender-for-endpoint) point to Defender for Endpoint Workspace key & ID</span></span>

- <span data-ttu-id="edb6e-124">Appareils hors connexion dans le même réseau d’Azure Log Analytics</span><span class="sxs-lookup"><span data-stu-id="edb6e-124">Offline devices in the same network of Azure Log Analytics</span></span>
  -  <span data-ttu-id="edb6e-125">Configurez MMA pour qu’il pointe vers :</span><span class="sxs-lookup"><span data-stu-id="edb6e-125">Configure MMA to point to:</span></span>
     - <span data-ttu-id="edb6e-126">Adresse IP Azure Log Analytics en tant que proxy</span><span class="sxs-lookup"><span data-stu-id="edb6e-126">Azure Log Analytics IP as a proxy</span></span>
     - <span data-ttu-id="edb6e-127">Clé d’espace de travail Defender for Endpoint & ID</span><span class="sxs-lookup"><span data-stu-id="edb6e-127">Defender for Endpoint workspace key & ID</span></span>

## <a name="azure-virtual-machines"></a><span data-ttu-id="edb6e-128">Machines virtuelles Azure</span><span class="sxs-lookup"><span data-stu-id="edb6e-128">Azure virtual machines</span></span>
- <span data-ttu-id="edb6e-129">Configurer et activer [l’espace de travail Azure Log Analytics](/azure/azure-monitor/platform/gateway)</span><span class="sxs-lookup"><span data-stu-id="edb6e-129">Configure and enable [Azure Log Analytics workspace](/azure/azure-monitor/platform/gateway)</span></span>

    - <span data-ttu-id="edb6e-130">Configurer Azure Log Analytics Gateway (anciennement passerelle OMS) pour qu’elle agisse en tant que proxy ou hub :</span><span class="sxs-lookup"><span data-stu-id="edb6e-130">Setup Azure Log Analytics Gateway (formerly known as OMS Gateway) to act as proxy or hub:</span></span>
      - [<span data-ttu-id="edb6e-131">Passerelle Azure Log Analytics</span><span class="sxs-lookup"><span data-stu-id="edb6e-131">Azure Log Analytics Gateway</span></span>](/azure/azure-monitor/platform/gateway#download-the-log-analytics-gateway)
      - <span data-ttu-id="edb6e-132">[Installer et configurer un point Microsoft Monitoring Agent (MMA)](configure-server-endpoints.md#install-and-configure-microsoft-monitoring-agent-mma-to-report-sensor-data-to-microsoft-defender-for-endpoint) vers la clé d’espace de travail Defender for Endpoint & ID</span><span class="sxs-lookup"><span data-stu-id="edb6e-132">[Install and configure Microsoft Monitoring Agent (MMA)](configure-server-endpoints.md#install-and-configure-microsoft-monitoring-agent-mma-to-report-sensor-data-to-microsoft-defender-for-endpoint) point to Defender for Endpoint Workspace key & ID</span></span>
    - <span data-ttu-id="edb6e-133">Ordinateurs VM Azure hors connexion dans le même réseau de passerelle OMS</span><span class="sxs-lookup"><span data-stu-id="edb6e-133">Offline Azure VMs in the same network of OMS Gateway</span></span>
      - <span data-ttu-id="edb6e-134">Configurer l’adresse IP Azure Log Analytics en tant que proxy</span><span class="sxs-lookup"><span data-stu-id="edb6e-134">Configure Azure Log Analytics IP as a proxy</span></span>
      - <span data-ttu-id="edb6e-135">ID de clé d’espace de travail Azure Log Analytics & ID</span><span class="sxs-lookup"><span data-stu-id="edb6e-135">Azure Log Analytics Workspace Key & ID</span></span>

    - <span data-ttu-id="edb6e-136">Azure Defender</span><span class="sxs-lookup"><span data-stu-id="edb6e-136">Azure Defender</span></span>
      - [<span data-ttu-id="edb6e-137">Espace de travail \> Analyse des journaux de stratégie de sécurité</span><span class="sxs-lookup"><span data-stu-id="edb6e-137">Security Policy \> Log Analytics Workspace</span></span>](/azure/security-center/security-center-wdatp#enable-windows-defender-atp-integration)
      - [<span data-ttu-id="edb6e-138">Détection des \> menaces : autoriser Defender pour le point de terminaison à accéder à mes données</span><span class="sxs-lookup"><span data-stu-id="edb6e-138">Threat Detection \> Allow Defender for Endpoint to access my data</span></span>](/azure/security-center/security-center-wdatp#enable-windows-defender-atp-integration)

        <span data-ttu-id="edb6e-139">Pour plus d’informations, voir [Working with security policies](/azure/security-center/tutorial-security-policy).</span><span class="sxs-lookup"><span data-stu-id="edb6e-139">For more information, see [Working with security policies](/azure/security-center/tutorial-security-policy).</span></span>
