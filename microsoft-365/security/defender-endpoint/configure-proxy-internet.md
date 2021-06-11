---
title: Configurer les paramètres de proxy d’appareil et de connexion Internet
description: Configurez les paramètres proxy et Internet de Microsoft Defender pour les points de terminaison afin d’activer la communication avec le service cloud.
keywords: configurer, proxy, Internet, connectivité Internet, paramètres, paramètres proxy, netsh, winhttp, serveur proxy
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
ms.collection:
- m365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 0de55eefe2f7dd8c9f891fbe126a68a49699ecd3
ms.sourcegitcommit: b0d3abbccf4dd37e32d69664d3ebc9ab8dea760d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/21/2021
ms.locfileid: "52594096"
---
# <a name="configure-device-proxy-and-internet-connectivity-settings"></a><span data-ttu-id="90975-104">Configurer les paramètres de proxy du dispositif et de connectivité Internet</span><span class="sxs-lookup"><span data-stu-id="90975-104">Configure device proxy and Internet connectivity settings</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="90975-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="90975-105">**Applies to:**</span></span>
- [<span data-ttu-id="90975-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="90975-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="90975-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="90975-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="90975-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="90975-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="90975-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="90975-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/en-us/WindowsForBusiness/windows-atp?ocid=docs-wdatp-configureendpointsscript-abovefoldlink)

<span data-ttu-id="90975-110">Le capteur Defender pour point de terminaison nécessite que Microsoft Windows HTTP (WinHTTP) signale les données du capteur et communique avec le service Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="90975-110">The Defender for Endpoint sensor requires Microsoft Windows HTTP (WinHTTP) to report sensor data and communicate with the Defender for Endpoint service.</span></span>

<span data-ttu-id="90975-111">Le capteur Defender for Endpoint incorporé s’exécute dans le contexte système à l’aide du compte LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="90975-111">The embedded Defender for Endpoint sensor runs in system context using the LocalSystem account.</span></span> <span data-ttu-id="90975-112">Le capteur utilise Microsoft Windows HTTP Services (WinHTTP) pour permettre la communication avec le service cloud Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="90975-112">The sensor uses Microsoft Windows HTTP Services (WinHTTP) to enable communication with the Defender for Endpoint cloud service.</span></span>

>[!TIP]
><span data-ttu-id="90975-113">Pour les organisations qui utilisent des proxies de transfert comme passerelle vers l'Internet, vous pouvez utiliser la protection du réseau pour enquêter derrière un proxy.</span><span class="sxs-lookup"><span data-stu-id="90975-113">For organizations that use forward proxies as a gateway to the Internet, you can use network protection to investigate behind a proxy.</span></span> <span data-ttu-id="90975-114">Pour plus d'informations, voir [Enquêter sur les événements de connexion qui se produisent derrière les procurations](investigate-behind-proxy.md).</span><span class="sxs-lookup"><span data-stu-id="90975-114">For more information, see [Investigate connection events that occur behind forward proxies](investigate-behind-proxy.md).</span></span>

<span data-ttu-id="90975-115">Le paramètre de configuration WinHTTP est indépendant des paramètres proxy de navigation Internet Windows Internet (WinINet) et ne peut découvrir un serveur proxy qu’à l’aide des méthodes de découverte suivantes :</span><span class="sxs-lookup"><span data-stu-id="90975-115">The WinHTTP configuration setting is independent of the Windows Internet (WinINet) Internet browsing proxy settings and can only discover a proxy server by using the following discovery methods:</span></span>

- <span data-ttu-id="90975-116">Méthodes de découverte automatique :</span><span class="sxs-lookup"><span data-stu-id="90975-116">Auto-discovery methods:</span></span>

  - <span data-ttu-id="90975-117">Proxy transparent</span><span class="sxs-lookup"><span data-stu-id="90975-117">Transparent proxy</span></span>

  - <span data-ttu-id="90975-118">Protocole WPAD (Web Proxy Auto-Discovery Protocol)</span><span class="sxs-lookup"><span data-stu-id="90975-118">Web Proxy Auto-discovery Protocol (WPAD)</span></span>

    > [!NOTE]
    > <span data-ttu-id="90975-119">Si vous utilisez un proxy transparent ou WPAD dans votre topologie réseau, vous n’avez pas besoin de paramètres de configuration spéciaux.</span><span class="sxs-lookup"><span data-stu-id="90975-119">If you're using Transparent proxy or WPAD in your network topology, you don't need special configuration settings.</span></span> <span data-ttu-id="90975-120">Pour plus d’informations sur les exclusions d’URL defender pour point de terminaison dans le proxy, voir Activer l’accès à Defender pour les URL de service de point de terminaison dans [le serveur proxy.](#enable-access-to-microsoft-defender-for-endpoint-service-urls-in-the-proxy-server)</span><span class="sxs-lookup"><span data-stu-id="90975-120">For more information on Defender for Endpoint URL exclusions in the proxy, see [Enable access to Defender for Endpoint service URLs in the proxy server](#enable-access-to-microsoft-defender-for-endpoint-service-urls-in-the-proxy-server).</span></span>

- <span data-ttu-id="90975-121">Configuration manuelle du proxy statique :</span><span class="sxs-lookup"><span data-stu-id="90975-121">Manual static proxy configuration:</span></span>

  - <span data-ttu-id="90975-122">Configuration basée sur le registre</span><span class="sxs-lookup"><span data-stu-id="90975-122">Registry based configuration</span></span>

  - <span data-ttu-id="90975-123">WinHTTP configuré à l'aide de la commande netsh – Convient uniquement aux ordinateurs de bureau à topologie stable (par exemple : un ordinateur de bureau dans un réseau d'entreprise derrière le même proxy)</span><span class="sxs-lookup"><span data-stu-id="90975-123">WinHTTP configured using netsh command – Suitable only for desktops in a stable topology (for example: a desktop in a corporate network behind the same proxy)</span></span>

## <a name="configure-the-proxy-server-manually-using-a-registry-based-static-proxy"></a><span data-ttu-id="90975-124">Configurer le serveur proxy manuellement en utilisant un proxy statique basé sur le registre</span><span class="sxs-lookup"><span data-stu-id="90975-124">Configure the proxy server manually using a registry-based static proxy</span></span>

<span data-ttu-id="90975-125">Configurez un proxy statique basé sur le Registre pour autoriser uniquement le capteur Defender for Endpoint à signaler les données de diagnostic et à communiquer avec Defender pour les services Endpoint si un ordinateur n’est pas autorisé à se connecter à Internet.</span><span class="sxs-lookup"><span data-stu-id="90975-125">Configure a registry-based static proxy to allow only Defender for Endpoint sensor to report diagnostic data and communicate with Defender for Endpoint services if a computer is not permitted to connect to the Internet.</span></span>

> [!NOTE]
> <span data-ttu-id="90975-126">Lorsque vous utilisez cette option sur Windows 10 ou Windows Server 2019, il est recommandé d’avoir la version suivante (ou ultérieure) et le cumul des mises à jour cumulatives :</span><span class="sxs-lookup"><span data-stu-id="90975-126">When using this option on Windows 10 or Windows Server 2019, it is recommended to have the following (or later) build and cumulative update rollup:</span></span>
>
> - <span data-ttu-id="90975-127">Windows 10, version 1809 ou Windows Server 2019 -https://support.microsoft.com/kb/5001384</span><span class="sxs-lookup"><span data-stu-id="90975-127">Windows 10, version 1809 or Windows Server 2019 - https://support.microsoft.com/kb/5001384</span></span>
> - <span data-ttu-id="90975-128">Windows 10, version 1909 -https://support.microsoft.com/kb/4601380</span><span class="sxs-lookup"><span data-stu-id="90975-128">Windows 10, version 1909 - https://support.microsoft.com/kb/4601380</span></span>
> - <span data-ttu-id="90975-129">Windows 10, version 2004 -https://support.microsoft.com/kb/4601382</span><span class="sxs-lookup"><span data-stu-id="90975-129">Windows 10, version 2004 - https://support.microsoft.com/kb/4601382</span></span>
> - <span data-ttu-id="90975-130">Windows 10, version 20H2 -https://support.microsoft.com/kb/4601382</span><span class="sxs-lookup"><span data-stu-id="90975-130">Windows 10, version 20H2 - https://support.microsoft.com/kb/4601382</span></span>
>
> <span data-ttu-id="90975-131">Ces mises à jour améliorent la connectivité et la fiabilité du canal CnC (Commande et contrôle).</span><span class="sxs-lookup"><span data-stu-id="90975-131">These updates improve the connectivity and reliability of the CnC (Command and Control) channel.</span></span>

<span data-ttu-id="90975-132">Le proxy statique est configurable via une stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="90975-132">The static proxy is configurable through Group Policy (GP).</span></span> <span data-ttu-id="90975-133">La stratégie de groupe se trouve sous :</span><span class="sxs-lookup"><span data-stu-id="90975-133">The group policy can be found under:</span></span>

- <span data-ttu-id="90975-134">**Modèles d’administration > Windows composants > collecte de données et builds d’aperçu > Configurer l’utilisation du proxy authentifié pour le service Expériences des utilisateurs connectés et télémétrie**</span><span class="sxs-lookup"><span data-stu-id="90975-134">**Administrative Templates > Windows Components > Data Collection and Preview Builds > Configure Authenticated Proxy usage for the Connected User Experience and Telemetry Service**</span></span>

  <span data-ttu-id="90975-135">Définissez-le **sur Activé et** sélectionnez Désactiver l’utilisation du proxy **authentifié.**</span><span class="sxs-lookup"><span data-stu-id="90975-135">Set it to **Enabled** and select **Disable Authenticated Proxy usage**.</span></span>

  ![Image du paramètre de stratégie de groupe1](images/atp-gpo-proxy1.png)

- <span data-ttu-id="90975-137">**Modèles d’administration > Windows composants >** collecte de données et builds d’aperçu > configurer les expériences des utilisateurs connectés et la télémétrie :</span><span class="sxs-lookup"><span data-stu-id="90975-137">**Administrative Templates > Windows Components > Data Collection and Preview Builds > Configure connected user experiences and telemetry**:</span></span>

  <span data-ttu-id="90975-138">Configurer le proxy</span><span class="sxs-lookup"><span data-stu-id="90975-138">Configure the proxy</span></span>

  ![Image du paramètre de stratégie de groupe2](images/atp-gpo-proxy2.png)

  <span data-ttu-id="90975-140">La stratégie définit deux valeurs de Registre, comme REG_SZ et comme REG_DWORD, sous `TelemetryProxyServer` la clé de Registre `DisableEnterpriseAuthProxy` `HKLM\Software\Policies\Microsoft\Windows\DataCollection` .</span><span class="sxs-lookup"><span data-stu-id="90975-140">The policy sets two registry values, `TelemetryProxyServer` as REG_SZ and `DisableEnterpriseAuthProxy` as REG_DWORD, under the registry key `HKLM\Software\Policies\Microsoft\Windows\DataCollection`.</span></span>

  <span data-ttu-id="90975-141">La valeur de Registre `TelemetryProxyServer` prend le format de chaîne suivant :</span><span class="sxs-lookup"><span data-stu-id="90975-141">The registry value `TelemetryProxyServer` takes the following string format:</span></span>

  ```text
  <server name or ip>:<port>
  ```

  <span data-ttu-id="90975-142">Par exemple, 10.0.0.6:8080</span><span class="sxs-lookup"><span data-stu-id="90975-142">For example: 10.0.0.6:8080</span></span>

  <span data-ttu-id="90975-143">Cette valeur de registre `DisableEnterpriseAuthProxy` doit être égale à 1.</span><span class="sxs-lookup"><span data-stu-id="90975-143">The registry value `DisableEnterpriseAuthProxy` should be set to 1.</span></span>

## <a name="configure-the-proxy-server-manually-using-netsh-command"></a><span data-ttu-id="90975-144">Configurer le serveur proxy manuellement à l’aide de la commande netsh</span><span class="sxs-lookup"><span data-stu-id="90975-144">Configure the proxy server manually using netsh command</span></span>

<span data-ttu-id="90975-145">Utiliser netsh pour configurer un proxy statique à l’échelle du système.</span><span class="sxs-lookup"><span data-stu-id="90975-145">Use netsh to configure a system-wide static proxy.</span></span>

> [!NOTE]
> - <span data-ttu-id="90975-146">Cela affectera toutes les applications, y compris les services Windows qui utilisent WinHTTP avec un proxy par défaut.</span><span class="sxs-lookup"><span data-stu-id="90975-146">This will affect all applications including Windows services which use WinHTTP with default proxy.</span></span></br>
> - <span data-ttu-id="90975-147">Les ordinateurs portables qui changent de topologie (par exemple, de bureau à domicile) ne fonctionnent pas correctement avec netsh.</span><span class="sxs-lookup"><span data-stu-id="90975-147">Laptops that are changing topology (for example: from office to home) will malfunction with netsh.</span></span> <span data-ttu-id="90975-148">Utiliser la configuration statique du proxy basée sur le registre.</span><span class="sxs-lookup"><span data-stu-id="90975-148">Use the registry-based static proxy configuration.</span></span>

1. <span data-ttu-id="90975-149">Ouvrir une ligne de commandes avec élévation de privilèges :</span><span class="sxs-lookup"><span data-stu-id="90975-149">Open an elevated command-line:</span></span>

   1. <span data-ttu-id="90975-150">Accéder à **Démarrer** et taper **cmd**.</span><span class="sxs-lookup"><span data-stu-id="90975-150">Go to **Start** and type **cmd**.</span></span>

   1. <span data-ttu-id="90975-151">Cliquez avec le bouton droit sur **Invite de commandes** et sélectionnez **Exécuter en tant qu'administrateur**.</span><span class="sxs-lookup"><span data-stu-id="90975-151">Right-click **Command prompt** and select **Run as administrator**.</span></span>

2. <span data-ttu-id="90975-152">Entrez la commande suivante et appuyez sur **Entrée** :</span><span class="sxs-lookup"><span data-stu-id="90975-152">Enter the following command and press **Enter**:</span></span>

   ```PowerShell
   netsh winhttp set proxy <proxy>:<port>
   ```

   <span data-ttu-id="90975-153">Par exemple : `netsh winhttp set proxy 10.0.0.6:8080`</span><span class="sxs-lookup"><span data-stu-id="90975-153">For example: `netsh winhttp set proxy 10.0.0.6:8080`</span></span>

<span data-ttu-id="90975-154">Pour réinitialiser le proxy winhttp, entrez la commande suivante et appuyez sur **Entrée** :</span><span class="sxs-lookup"><span data-stu-id="90975-154">To reset the winhttp proxy, enter the following command and press **Enter**:</span></span>

```PowerShell
netsh winhttp reset proxy
```

<span data-ttu-id="90975-155">Pour plus d’informations, voir [la syntaxe, les contextes et le formatage de la commande Netsh](/windows-server/networking/technologies/netsh/netsh-contexts).</span><span class="sxs-lookup"><span data-stu-id="90975-155">See [Netsh Command Syntax, Contexts, and Formatting](/windows-server/networking/technologies/netsh/netsh-contexts) to learn more.</span></span>

## <a name="enable-access-to-microsoft-defender-for-endpoint-service-urls-in-the-proxy-server"></a><span data-ttu-id="90975-156">Activer l’accès aux URL du service Microsoft Defender pour les points de terminaison dans le serveur proxy</span><span class="sxs-lookup"><span data-stu-id="90975-156">Enable access to Microsoft Defender for Endpoint service URLs in the proxy server</span></span>

<span data-ttu-id="90975-157">Si un proxy ou un pare-feu bloque tout le trafic par défaut et n'autorise le passage que de domaines spécifiques, ajoutez les domaines énumérés dans la feuille téléchargeable à la liste des domaines autorisés.</span><span class="sxs-lookup"><span data-stu-id="90975-157">If a proxy or firewall is blocking all traffic by default and allowing only specific domains through, add the domains listed in the downloadable sheet to the allowed domains list.</span></span>

<span data-ttu-id="90975-158">La feuille de calcul téléchargeable suivante répertorie les services et les URL associées à qui votre réseau doit pouvoir se connecter.</span><span class="sxs-lookup"><span data-stu-id="90975-158">The following downloadable spreadsheet lists the services and their associated URLs that your network must be able to connect to.</span></span> <span data-ttu-id="90975-159">Vous devez vous assurer qu’il n’existe aucune règle de pare-feu ou de  filtrage réseau qui refuserait l’accès à ces URL, ou que vous devrez peut-être créer une règle d’autoriser spécifiquement pour eux.</span><span class="sxs-lookup"><span data-stu-id="90975-159">You should ensure that there are no firewall or network filtering rules that would deny access to these URLs, or you may need to create an *allow* rule specifically for them.</span></span>


| <span data-ttu-id="90975-160">Liste de feuilles de calcul de domaines</span><span class="sxs-lookup"><span data-stu-id="90975-160">Spreadsheet of domains list</span></span> | <span data-ttu-id="90975-161">Description</span><span class="sxs-lookup"><span data-stu-id="90975-161">Description</span></span> |
|:-----|:-----|
|![Image miniature de la feuille de calcul DES URL de Microsoft Defender pour les points de terminaison](images/mdatp-urls.png)<br/>  | <span data-ttu-id="90975-163">Feuille de calcul d’enregistrements DNS spécifiques pour les emplacements de service, les emplacements géographiques et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="90975-163">Spreadsheet of specific DNS records for service locations, geographic locations, and OS.</span></span> <br><br>[<span data-ttu-id="90975-164">Téléchargez la feuille de calcul ici.</span><span class="sxs-lookup"><span data-stu-id="90975-164">Download the spreadsheet here.</span></span>](https://download.microsoft.com/download/8/a/5/8a51eee5-cd02-431c-9d78-a58b7f77c070/mde-urls.xlsx) 


<span data-ttu-id="90975-165">Si l’analyse HTTPS (inspection SSL) est activée pour un proxy ou un pare-feu, excluez les domaines répertoriés dans le tableau ci-dessus de l’analyse HTTPS.</span><span class="sxs-lookup"><span data-stu-id="90975-165">If a proxy or firewall has HTTPS scanning (SSL inspection) enabled, exclude the domains listed in the above table from HTTPS scanning.</span></span>

> [!NOTE]
> <span data-ttu-id="90975-166">settings-win.data.microsoft.com est nécessaire uniquement si vous avez des Windows 10 exécutant la version 1803 ou une version antérieure.</span><span class="sxs-lookup"><span data-stu-id="90975-166">settings-win.data.microsoft.com is only needed if you have Windows 10 devices running version 1803 or earlier.</span></span><br>


> [!NOTE]
> <span data-ttu-id="90975-167">Les URL qui incluent la version 20 sont nécessaires uniquement si vous avez des Windows 10 exécutant la version 1803 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="90975-167">URLs that include v20 in them are only needed if you have Windows 10 devices running version 1803 or later.</span></span> <span data-ttu-id="90975-168">Par exemple, est nécessaire pour un appareil Windows 10 exécutant la version 1803 ou ultérieure et intégré à la région Stockage `us-v20.events.data.microsoft.com` données américaines.</span><span class="sxs-lookup"><span data-stu-id="90975-168">For example, `us-v20.events.data.microsoft.com` is needed for a Windows 10 device running version 1803 or later and onboarded to US Data Storage region.</span></span>


> [!NOTE]
> <span data-ttu-id="90975-169">Si vous utilisez Antivirus Microsoft Defender dans votre environnement, voir Configurer les connexions réseau [au service cloud Antivirus Microsoft Defender.](/windows/security/threat-protection/microsoft-defender-antivirus/configure-network-connections-microsoft-defender-antivirus)</span><span class="sxs-lookup"><span data-stu-id="90975-169">If you are using Microsoft Defender Antivirus in your environment, see [Configure network connections to the Microsoft Defender Antivirus cloud service](/windows/security/threat-protection/microsoft-defender-antivirus/configure-network-connections-microsoft-defender-antivirus).</span></span>

<span data-ttu-id="90975-170">Si un proxy ou un pare-feu bloque le trafic anonyme, comme le capteur Defender for Endpoint se connecte à partir du contexte système, assurez-vous que le trafic anonyme est autorisé dans les URL répertoriées précédemment.</span><span class="sxs-lookup"><span data-stu-id="90975-170">If a proxy or firewall is blocking anonymous traffic, as Defender for Endpoint sensor is connecting from system context, make sure anonymous traffic is permitted in the previously listed URLs.</span></span>

### <a name="microsoft-monitoring-agent-mma---proxy-and-firewall-requirements-for-older-versions-of-windows-client-or-windows-server"></a><span data-ttu-id="90975-171">Microsoft Monitoring Agent (MMA) : exigences relatives au proxy et au pare-feu pour les versions antérieures Windows client ou Windows Server</span><span class="sxs-lookup"><span data-stu-id="90975-171">Microsoft Monitoring Agent (MMA) - proxy and firewall requirements for older versions of Windows client or Windows Server</span></span>

<span data-ttu-id="90975-172">Les informations ci-dessous répentent les informations de configuration du proxy et du pare-feu requises pour communiquer avec l’agent d’analyse des journaux (souvent appelé Microsoft Monitoring Agent) pour les versions précédentes de Windows telles que Windows 7 SP1, Windows 8.1, Windows Server 2008 R2, Windows Server 2012 R2 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="90975-172">The information below list the proxy and firewall configuration information required to communicate with Log Analytics agent (often referred to as Microsoft Monitoring Agent) for the previous versions of Windows such as Windows 7 SP1, Windows 8.1, Windows Server 2008 R2, Windows Server 2012 R2, and Windows Server 2016.</span></span>

|<span data-ttu-id="90975-173">Ressource Agent</span><span class="sxs-lookup"><span data-stu-id="90975-173">Agent Resource</span></span>|<span data-ttu-id="90975-174">Ports</span><span class="sxs-lookup"><span data-stu-id="90975-174">Ports</span></span> |<span data-ttu-id="90975-175">Direction</span><span class="sxs-lookup"><span data-stu-id="90975-175">Direction</span></span> |<span data-ttu-id="90975-176">Contourner l’inspection HTTPS</span><span class="sxs-lookup"><span data-stu-id="90975-176">Bypass HTTPS inspection</span></span>|
|------|---------|--------|--------|   
|<span data-ttu-id="90975-177">\*.ods.opinsights.azure.com</span><span class="sxs-lookup"><span data-stu-id="90975-177">\*.ods.opinsights.azure.com</span></span> |<span data-ttu-id="90975-178">Port 443</span><span class="sxs-lookup"><span data-stu-id="90975-178">Port 443</span></span> |<span data-ttu-id="90975-179">Sortant</span><span class="sxs-lookup"><span data-stu-id="90975-179">Outbound</span></span>|<span data-ttu-id="90975-180">Oui</span><span class="sxs-lookup"><span data-stu-id="90975-180">Yes</span></span> |  
|<span data-ttu-id="90975-181">\*.oms.opinsights.azure.com</span><span class="sxs-lookup"><span data-stu-id="90975-181">\*.oms.opinsights.azure.com</span></span> |<span data-ttu-id="90975-182">Port 443</span><span class="sxs-lookup"><span data-stu-id="90975-182">Port 443</span></span> |<span data-ttu-id="90975-183">Sortant</span><span class="sxs-lookup"><span data-stu-id="90975-183">Outbound</span></span>|<span data-ttu-id="90975-184">Oui</span><span class="sxs-lookup"><span data-stu-id="90975-184">Yes</span></span> |  
|<span data-ttu-id="90975-185">\*.blob.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="90975-185">\*.blob.core.windows.net</span></span> |<span data-ttu-id="90975-186">Port 443</span><span class="sxs-lookup"><span data-stu-id="90975-186">Port 443</span></span> |<span data-ttu-id="90975-187">Sortant</span><span class="sxs-lookup"><span data-stu-id="90975-187">Outbound</span></span>|<span data-ttu-id="90975-188">Oui</span><span class="sxs-lookup"><span data-stu-id="90975-188">Yes</span></span> |
|<span data-ttu-id="90975-189">\*.azure-automation.net</span><span class="sxs-lookup"><span data-stu-id="90975-189">\*.azure-automation.net</span></span> |<span data-ttu-id="90975-190">Port 443</span><span class="sxs-lookup"><span data-stu-id="90975-190">Port 443</span></span> |<span data-ttu-id="90975-191">Sortant</span><span class="sxs-lookup"><span data-stu-id="90975-191">Outbound</span></span>|<span data-ttu-id="90975-192">Oui</span><span class="sxs-lookup"><span data-stu-id="90975-192">Yes</span></span> |  


> [!NOTE]
> <span data-ttu-id="90975-193">En tant que solution informatique, la plage d’adresses IP peut changer.</span><span class="sxs-lookup"><span data-stu-id="90975-193">As a cloud-based solution, the IP range can change.</span></span> <span data-ttu-id="90975-194">Il est recommandé de passer au paramètre de résolution DNS.</span><span class="sxs-lookup"><span data-stu-id="90975-194">It's recommended you move to DNS resolving setting.</span></span>

## <a name="confirm-microsoft-monitoring-agent-mma-service-url-requirements"></a><span data-ttu-id="90975-195">Confirmer la Microsoft Monitoring Agent’URL du service (MMA)</span><span class="sxs-lookup"><span data-stu-id="90975-195">Confirm Microsoft Monitoring Agent (MMA) Service URL Requirements</span></span> 

<span data-ttu-id="90975-196">Consultez les instructions suivantes pour éliminer les caractères génériques (\*) requis pour votre environnement spécifique lors de l’utilisation de la Microsoft Monitoring Agent (MMA) pour les versions précédentes de Windows.</span><span class="sxs-lookup"><span data-stu-id="90975-196">Please see the following guidance to eliminate the wildcard (\*) requirement for your specific environment when using the Microsoft Monitoring Agent (MMA) for previous versions of Windows.</span></span>

1.  <span data-ttu-id="90975-197">Intégrer un système d’exploitation précédent avec l’Microsoft Monitoring Agent (MMA) dans Defender pour endpoint (pour plus d’informations, voir Intégrer les versions précédentes de Windows sur les serveurs [Defender for Endpoint](https://go.microsoft.com/fwlink/p/?linkid=2010326) et [Onboard Windows.](configure-server-endpoints.md#windows-server-2008-r2-sp1-windows-server-2012-r2-and-windows-server-2016)</span><span class="sxs-lookup"><span data-stu-id="90975-197">Onboard a previous operating system with the Microsoft Monitoring Agent (MMA) into Defender for Endpoint (for more information, see [Onboard previous versions of Windows on Defender for Endpoint](https://go.microsoft.com/fwlink/p/?linkid=2010326) and [Onboard Windows servers](configure-server-endpoints.md#windows-server-2008-r2-sp1-windows-server-2012-r2-and-windows-server-2016).</span></span>

2.  <span data-ttu-id="90975-198">Assurez-vous que l’ordinateur est correctement signalé dans le Centre de sécurité Microsoft Defender web.</span><span class="sxs-lookup"><span data-stu-id="90975-198">Ensure the machine is successfully reporting into the Microsoft Defender Security Center portal.</span></span>

3.  <span data-ttu-id="90975-199">Exécutez l’outil TestCloudConnection.exe à partir de « C:\Program Files\Microsoft Monitoring Agent\Agent » pour valider la connectivité et voir les URL requises pour votre espace de travail spécifique.</span><span class="sxs-lookup"><span data-stu-id="90975-199">Run the TestCloudConnection.exe tool from “C:\Program Files\Microsoft Monitoring Agent\Agent” to validate the connectivity and to see the required URLs for your specific workspace.</span></span>

4.  <span data-ttu-id="90975-200">Consultez la liste des URL de point de terminaison Microsoft Defender pour obtenir la liste complète des conditions requises pour votre région (reportez-vous à la feuille de calcul URL [de](https://download.microsoft.com/download/8/a/5/8a51eee5-cd02-431c-9d78-a58b7f77c070/mde-urls.xlsx)service).</span><span class="sxs-lookup"><span data-stu-id="90975-200">Check the Microsoft Defender for Endpoint URLs list for the complete list of requirements for your region (please refer to the Service URLs [Spreadsheet](https://download.microsoft.com/download/8/a/5/8a51eee5-cd02-431c-9d78-a58b7f77c070/mde-urls.xlsx)).</span></span>

    ![Image de l’administrateur dans Windows PowerShell](images/admin-powershell.png)

<span data-ttu-id="90975-202">Les caractères génériques (\*) utilisés dans les points de terminaison d’URL \*.ods.opinsights.azure.com, \*.oms.opinsights.azure.com et \*.agentsvc.azure-automation.net peuvent être remplacés par votre ID d’espace de travail spécifique.</span><span class="sxs-lookup"><span data-stu-id="90975-202">The wildcards (\*) used in \*.ods.opinsights.azure.com, \*.oms.opinsights.azure.com, and \*.agentsvc.azure-automation.net URL endpoints can be replaced with your specific Workspace ID.</span></span> <span data-ttu-id="90975-203">L’ID d’espace de travail est spécifique à votre environnement et à votre espace de travail et se trouve dans la section Intégration de votre client dans le portail Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="90975-203">The Workspace ID is specific to your environment and workspace and can be found in the Onboarding section of your tenant within the Microsoft Defender Security Center portal.</span></span>

<span data-ttu-id="90975-204">Le point de terminaison d’URL \*.blob.core.windows.net peut être remplacé par les URL affichées dans la section « Règle de pare-feu : \*.blob.core.windows.net » des résultats du test.</span><span class="sxs-lookup"><span data-stu-id="90975-204">The \*.blob.core.windows.net URL endpoint can be replaced with the URLs shown in the “Firewall Rule: \*.blob.core.windows.net” section of the test results.</span></span> 

> [!NOTE]
> <span data-ttu-id="90975-205">Dans le cas de l’intégration via Azure Defender, plusieurs espaces de travail peuvent être utilisés.</span><span class="sxs-lookup"><span data-stu-id="90975-205">In the case of onboarding via Azure Defender, multiple workspaces maybe used.</span></span> <span data-ttu-id="90975-206">Vous devrez effectuer la procédure TestCloudConnection.exe ci-dessus sur un ordinateur intégré à partir de chaque espace de travail (pour déterminer s’il existe des modifications apportées aux URL \*.blob.core.windows.net entre les espaces de travail).</span><span class="sxs-lookup"><span data-stu-id="90975-206">You will need to perform the TestCloudConnection.exe procedure above on an onboarded machine from each workspace (to determine if there are any changes to the \*.blob.core.windows.net URLs between the workspaces).</span></span>

## <a name="verify-client-connectivity-to-microsoft-defender-for-endpoint-service-urls"></a><span data-ttu-id="90975-207">Vérifier la connectivité du client aux URL du service Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="90975-207">Verify client connectivity to Microsoft Defender for Endpoint service URLs</span></span>

<span data-ttu-id="90975-208">Vérifier que la configuration du proxy a été effectuée avec succès, que WinHTTP peut découvrir et communiquer par le biais du serveur proxy dans votre environnement, et que le serveur proxy permet le trafic vers les URL du service Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="90975-208">Verify the proxy configuration completed successfully, that WinHTTP can discover and communicate through the proxy server in your environment, and that the proxy server allows traffic to the Defender for Endpoint service URLs.</span></span>

1. <span data-ttu-id="90975-209">Téléchargez [l MDATP’analyseur client](https://aka.ms/mdatpanalyzer) sur le PC sur lequel le capteur Defender for Endpoint est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="90975-209">Download the [MDATP Client Analyzer tool](https://aka.ms/mdatpanalyzer) to the PC where Defender for Endpoint sensor is running on.</span></span>

2. <span data-ttu-id="90975-210">Extraire le contenu de MDATPClientAnalyzer.zip sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="90975-210">Extract the contents of MDATPClientAnalyzer.zip on the device.</span></span>

3. <span data-ttu-id="90975-211">Ouvrir une ligne de commandes avec élévation de privilèges :</span><span class="sxs-lookup"><span data-stu-id="90975-211">Open an elevated command-line:</span></span>

   1. <span data-ttu-id="90975-212">Accéder à **Démarrer** et taper **cmd**.</span><span class="sxs-lookup"><span data-stu-id="90975-212">Go to **Start** and type **cmd**.</span></span>

   1.  <span data-ttu-id="90975-213">Cliquez avec le bouton droit sur **Invite de commandes** et sélectionnez **Exécuter en tant qu'administrateur**.</span><span class="sxs-lookup"><span data-stu-id="90975-213">Right-click **Command prompt** and select **Run as administrator**.</span></span>

4. <span data-ttu-id="90975-214">Entrez la commande suivante et appuyez sur **Entrée** :</span><span class="sxs-lookup"><span data-stu-id="90975-214">Enter the following command and press **Enter**:</span></span>

    ```PowerShell
    HardDrivePath\MDATPClientAnalyzer.cmd
    ```

    <span data-ttu-id="90975-215">Remplacez *HardDrivePath* par le chemin d’accès où l’outil MDATPClientAnalyzer a été téléchargé, par exemple :</span><span class="sxs-lookup"><span data-stu-id="90975-215">Replace *HardDrivePath* with the path where the MDATPClientAnalyzer tool was downloaded to, for example:</span></span>

    ```PowerShell
    C:\Work\tools\MDATPClientAnalyzer\MDATPClientAnalyzer.cmd
    ```

5. <span data-ttu-id="90975-216">*ExtrayezMDATPClientAnalyzerResult.zip* fichier créé par l’outil dans le dossier utilisé dans *HardDrivePath*.</span><span class="sxs-lookup"><span data-stu-id="90975-216">Extract the *MDATPClientAnalyzerResult.zip* file created by tool in the folder used in the *HardDrivePath*.</span></span>

6. <span data-ttu-id="90975-217">Open *MDATPClientAnalyzerResult.txt* et vérifiez que vous avez effectué les étapes de configuration du proxy pour permettre la découverte du serveur et l'accès aux URL des services.</span><span class="sxs-lookup"><span data-stu-id="90975-217">Open *MDATPClientAnalyzerResult.txt* and verify that you have performed the proxy configuration steps to enable server discovery and access to the service URLs.</span></span>

   <span data-ttu-id="90975-218">L'outil vérifie la connectivité des URL du service Defender for Endpoint avec lesquelles le client Defender for Endpoint est configuré pour interagir.</span><span class="sxs-lookup"><span data-stu-id="90975-218">The tool checks the connectivity of Defender for Endpoint service URLs that Defender for Endpoint client is configured to interact with.</span></span> <span data-ttu-id="90975-219">Il imprime ensuite les résultats dans le fichier *MDATPClientAnalyzerResult.txt* pour chaque URL pouvant être utilisée pour communiquer avec Defender pour les services Endpoint.</span><span class="sxs-lookup"><span data-stu-id="90975-219">It then prints the results into the *MDATPClientAnalyzerResult.txt* file for each URL that can potentially be used to communicate with the Defender for Endpoint services.</span></span> <span data-ttu-id="90975-220">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="90975-220">For example:</span></span>

   ```text
   Testing URL : https://xxx.microsoft.com/xxx
   1 - Default proxy: Succeeded (200)
   2 - Proxy auto discovery (WPAD): Succeeded (200)
   3 - Proxy disabled: Succeeded (200)
   4 - Named proxy: Doesn't exist
   5 - Command line proxy: Doesn't exist
   ```

<span data-ttu-id="90975-221">Si au moins une des options de connectivité renvoie un état (200), le client Defender pour le point de terminaison peut communiquer avec l’URL testée correctement à l’aide de cette méthode de connectivité.</span><span class="sxs-lookup"><span data-stu-id="90975-221">If at least one of the connectivity options returns a (200) status, then the Defender for Endpoint client can communicate with the tested URL properly using this connectivity method.</span></span>

<span data-ttu-id="90975-222">Toutefois, si les résultats du contrôle de la connectivité indiquent un échec, une erreur HTTP est affichée (voir Codes d'état HTTP).</span><span class="sxs-lookup"><span data-stu-id="90975-222">However, if the connectivity check results indicate a failure, an HTTP error is displayed (see HTTP Status Codes).</span></span> <span data-ttu-id="90975-223">Vous pouvez ensuite utiliser les URL dans le tableau indiqué dans Activer l’accès aux URL de [service Defender for Endpoint dans le serveur proxy.](#enable-access-to-microsoft-defender-for-endpoint-service-urls-in-the-proxy-server)</span><span class="sxs-lookup"><span data-stu-id="90975-223">You can then use the URLs in the table shown in [Enable access to Defender for Endpoint service URLs in the proxy server](#enable-access-to-microsoft-defender-for-endpoint-service-urls-in-the-proxy-server).</span></span> <span data-ttu-id="90975-224">Les URL que vous utiliserez dépendent de la région sélectionnée au cours de la procédure d’intégration.</span><span class="sxs-lookup"><span data-stu-id="90975-224">The URLs you'll use will depend on the region selected during the onboarding procedure.</span></span>

> [!NOTE]
> <span data-ttu-id="90975-225"> L’outil Analyseur de connectivité n’est pas compatible avec la règle ASR [Bloquer les créations de processus en provenance des commandes PSExec et WMI](/windows/security/threat-protection/windows-defender-exploit-guard/attack-surface-reduction#attack-surface-reduction-rules).</span><span class="sxs-lookup"><span data-stu-id="90975-225">The Connectivity Analyzer tool is not compatible with ASR rule [Block process creations originating from PSExec and WMI commands](/windows/security/threat-protection/windows-defender-exploit-guard/attack-surface-reduction#attack-surface-reduction-rules).</span></span> <span data-ttu-id="90975-226">Vous devrez désactiver temporairement cette règle pour exécuter l’outil connectivité.</span><span class="sxs-lookup"><span data-stu-id="90975-226">You will need to temporarily disable this rule to run the connectivity tool.</span></span>


> [!NOTE]
> <span data-ttu-id="90975-227">Lorsque telemetryProxyServer est défini, dans le Registre ou via la stratégie de groupe, Defender pour le point de terminaison revient à direct s’il ne peut pas accéder au proxy défini.</span><span class="sxs-lookup"><span data-stu-id="90975-227">When the TelemetryProxyServer is set, in Registry or via Group Policy, Defender for Endpoint will fall back to direct if it can't access the defined proxy.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90975-228">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90975-228">Related topics</span></span>

- [<span data-ttu-id="90975-229">Intégrer des appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="90975-229">Onboard Windows 10 devices</span></span>](configure-endpoints.md)
- [<span data-ttu-id="90975-230">Résoudre les problèmes d’intégration de Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="90975-230">Troubleshoot Microsoft Defender for Endpoint onboarding issues</span></span>](troubleshoot-onboarding.md)
