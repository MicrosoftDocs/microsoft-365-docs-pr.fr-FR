---
title: Configurer le proxy du dispositif et les paramètres de connexion à Internet pour le DLP du point de terminaison
f1.keywords:
- CSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 07/21/2020
audience: ITPro
ms.topic: conceptual
f1_keywords:
- ms.o365.cc.DLPLandingPage
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
- m365solution-mip
- m365initiative-compliance
search.appverid:
- MET150
description: Apprenez comment configurer les paramètres de proxy et de connexion Internet du dispositif pour le DLP Endpoint.
ms.openlocfilehash: 3b8ebdbb08a6a866cc84df2031e77378925eaa0e
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50907004"
---
# <a name="configure-device-proxy-and-internet-connection-settings-for-endpoint-dlp"></a><span data-ttu-id="fe047-103">Configurer le proxy du dispositif et les paramètres de connexion à Internet pour le DLP du point de terminaison</span><span class="sxs-lookup"><span data-stu-id="fe047-103">Configure device proxy and internet connection settings for Endpoint DLP</span></span>

<span data-ttu-id="fe047-104">Microsoft Endpoint DLP utilise Microsoft Windows HTTP (WinHTTP) pour signaler les données et communiquer avec le service Microsoft Endpoint Cloud.</span><span class="sxs-lookup"><span data-stu-id="fe047-104">Microsoft Endpoint DLP uses Microsoft Windows HTTP (WinHTTP) to report data and communicate with the Microsoft endpoint cloud service.</span></span> <span data-ttu-id="fe047-105">Le DLP Endpoint intégré fonctionne dans le contexte du système en utilisant le compte LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="fe047-105">The embedded Endpoint DLP runs in system context using the LocalSystem account.</span></span>

> [!TIP]
> <span data-ttu-id="fe047-106">Pour les organisations qui utilisent des proxies de transfert comme passerelle vers l'Internet, vous pouvez utiliser la protection du réseau pour enquêter derrière un proxy.</span><span class="sxs-lookup"><span data-stu-id="fe047-106">For organizations that use forward proxies as a gateway to the Internet, you can use network protection to investigate behind a proxy.</span></span> <span data-ttu-id="fe047-107">Pour plus d'informations, voir [Enquêter sur les événements de connexion qui se produisent derrière les procurations](/windows/security/threat-protection/microsoft-defender-atp/investigate-behind-proxy).</span><span class="sxs-lookup"><span data-stu-id="fe047-107">For more information, see [Investigate connection events that occur behind forward proxies](/windows/security/threat-protection/microsoft-defender-atp/investigate-behind-proxy).</span></span>

<span data-ttu-id="fe047-108">Le paramètre de configuration de WinHTTP est indépendant des paramètres du proxy de navigation Internet de Windows (WinINet) et ne peut découvrir un serveur proxy qu'en utilisant les méthodes de découverte automatique suivantes :</span><span class="sxs-lookup"><span data-stu-id="fe047-108">The WinHTTP configuration setting is independent of the Windows Internet (WinINet) Internet browsing proxy settings and can only discover a proxy server by using the following auto discovery methods:</span></span>

- <span data-ttu-id="fe047-109">Proxy transparent</span><span class="sxs-lookup"><span data-stu-id="fe047-109">Transparent proxy</span></span>
- <span data-ttu-id="fe047-110">Protocole WPAD (Web Proxy Auto-Discovery Protocol)</span><span class="sxs-lookup"><span data-stu-id="fe047-110">Web Proxy Auto-discovery Protocol (WPAD)</span></span>

> [!NOTE]
> <span data-ttu-id="fe047-111">Si vous utilisez un proxy transparent ou WPAD dans votre topologie de réseau, vous n'avez pas besoin de paramètres de configuration particuliers.</span><span class="sxs-lookup"><span data-stu-id="fe047-111">If you’re using Transparent proxy or WPAD in your network topology, you don’t need special configuration settings.</span></span> <span data-ttu-id="fe047-112">Pour plus d'informations sur le Defender for Endpoint URL exclusions in the proxy, voir[Activer l'accès aux URL des services DLP dans le cloud du point de terminaison dans le serveur proxy](#enable-access-to-endpoint-dlp-cloud-service-urls-in-the-proxy-server).</span><span class="sxs-lookup"><span data-stu-id="fe047-112">For more information on Defender for Endpoint URL exclusions in the proxy, see [Enable access to Endpoint DLP cloud service URLs in the proxy server](#enable-access-to-endpoint-dlp-cloud-service-urls-in-the-proxy-server).</span></span>

- <span data-ttu-id="fe047-113">Configuration manuelle du proxy statique :</span><span class="sxs-lookup"><span data-stu-id="fe047-113">Manual static proxy configuration:</span></span>
    - <span data-ttu-id="fe047-114">Configuration basée sur le registre</span><span class="sxs-lookup"><span data-stu-id="fe047-114">Registry based configuration</span></span>
    - <span data-ttu-id="fe047-115">WinHTTP configuré à l'aide de la commande netsh – Convient uniquement aux ordinateurs de bureau à topologie stable (par exemple : un ordinateur de bureau dans un réseau d'entreprise derrière le même proxy)</span><span class="sxs-lookup"><span data-stu-id="fe047-115">WinHTTP configured using netsh command – Suitable only for desktops in a stable topology (for example: a desktop in a corporate network behind the same proxy)</span></span>

## <a name="configure-the-proxy-server-manually-using-a-registry-based-static-proxy"></a><span data-ttu-id="fe047-116">Configurer le serveur proxy manuellement en utilisant un proxy statique basé sur le registre</span><span class="sxs-lookup"><span data-stu-id="fe047-116">Configure the proxy server manually using a registry-based static proxy</span></span>

<span data-ttu-id="fe047-117">Pour les terminaux qui ne sont pas autorisés à se connecter à Internet, vous devez configurer un proxy statique basé sur le registre.</span><span class="sxs-lookup"><span data-stu-id="fe047-117">For endpoint devices that aren't permitted to connect to the Internet, you need to configure a registry-based static proxy.</span></span> <span data-ttu-id="fe047-118">Vous devez configurer ceci pour autoriser uniquement Microsoft Endpoint DLP à signaler des données de diagnostic et à communiquer avec le service cloud Microsoft Endpoint.</span><span class="sxs-lookup"><span data-stu-id="fe047-118">You need to configure this to allow only Microsoft Endpoint DLP to report diagnostic data and communicate with Microsoft endpoint cloud service.</span></span>

<span data-ttu-id="fe047-119">Le proxy statique est configurable via une stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="fe047-119">The static proxy is configurable through Group Policy (GP).</span></span> <span data-ttu-id="fe047-120">La stratégie de groupe se trouve sous :</span><span class="sxs-lookup"><span data-stu-id="fe047-120">The group policy can be found under:</span></span>

1. <span data-ttu-id="fe047-121">Ouvrir **Modèles administratifs > Composants Windows > Collections de données et Builds d’aperçu > Configurer l’utilisation du proxy authentifié pour l’expérience utilisateur connecté et le service de télémétrie**</span><span class="sxs-lookup"><span data-stu-id="fe047-121">Open **Administrative Templates > Windows Components > Data Collection and Preview Builds > Configure Authenticated Proxy usage for the Connected User Experience and Telemetry Service**</span></span>

2. <span data-ttu-id="fe047-122">Définir sur **Activer** puis sélectionnez **Désactiver l'utilisation d'un proxy authentifié**:</span><span class="sxs-lookup"><span data-stu-id="fe047-122">Set it to **Enabled** and select **Disable Authenticated Proxy usage**:</span></span> 

![Image des paramètres de stratégie de groupe 1](../media/atp-gpo-proxy1.png)
 
3. <span data-ttu-id="fe047-124">Ouvrir **Modèles administratifs > Composants Windows > Collections de données et Builds d’aperçu > Configurer l’utilisation du proxy authentifié pour l’expérience utilisateur connecté et le service de télémétrie**:</span><span class="sxs-lookup"><span data-stu-id="fe047-124">Open **Administrative Templates > Windows Components > Data Collection and Preview Builds > Configure connected user experiences and telemetry**:</span></span>

 <span data-ttu-id="fe047-125">Configurer le proxy</span><span class="sxs-lookup"><span data-stu-id="fe047-125">Configure the proxy</span></span>

![Image des paramètres de stratégie de groupe 2](../media/atp-gpo-proxy2.png)

<span data-ttu-id="fe047-127">La stratégie définit deux valeurs de registre `TelemetryProxyServer` comme REG_SZ et `DisableEnterpriseAuthProxy` comme REG_DWORD sous la clé de registre `HKLM\Software\Policies\Microsoft\Windows\DataCollection`.</span><span class="sxs-lookup"><span data-stu-id="fe047-127">The policy sets two registry values `TelemetryProxyServer` as REG_SZ and `DisableEnterpriseAuthProxy` as REG_DWORD under the registry key `HKLM\Software\Policies\Microsoft\Windows\DataCollection`.</span></span>

<span data-ttu-id="fe047-128">La valeur de registre TelemetryProxyServer est au format \<server name or ip\>:\<port\>.</span><span class="sxs-lookup"><span data-stu-id="fe047-128">The registry value TelemetryProxyServer is in this format \<server name or ip\>:\<port\>.</span></span> <span data-ttu-id="fe047-129">Par exemple, **10.0.0.6:8080**</span><span class="sxs-lookup"><span data-stu-id="fe047-129">For example: **10.0.0.6:8080**</span></span>

<span data-ttu-id="fe047-130">Cette valeur de registre `DisableEnterpriseAuthProxy` doit être égale à 1.</span><span class="sxs-lookup"><span data-stu-id="fe047-130">The registry value `DisableEnterpriseAuthProxy` should be set to 1.</span></span>

## <a name="configure-the-proxy-server-manually-using-netsh-command"></a><span data-ttu-id="fe047-131">Configurer le serveur proxy manuellement à l’aide de la commande « netsh »</span><span class="sxs-lookup"><span data-stu-id="fe047-131">Configure the proxy server manually using "netsh" command</span></span>

<span data-ttu-id="fe047-132">Utiliser netsh pour configurer un proxy statique à l’échelle du système.</span><span class="sxs-lookup"><span data-stu-id="fe047-132">Use netsh to configure a system-wide static proxy.</span></span>

> [!NOTE]
> <span data-ttu-id="fe047-133">Cela affectera toutes les applications, y compris les services Windows qui utilisent WinHTTP avec un proxy par défaut.</span><span class="sxs-lookup"><span data-stu-id="fe047-133">This will affect all applications including Windows services which use WinHTTP with default proxy.</span></span> <span data-ttu-id="fe047-134">- Les ordinateurs portables qui changent de topologie (par exemple : du bureau à la maison) fonctionneront mal avec netsh.</span><span class="sxs-lookup"><span data-stu-id="fe047-134">- Laptops that are changing topology (for example: from office to home) will malfunction with netsh.</span></span> <span data-ttu-id="fe047-135">Utiliser la configuration statique du proxy basée sur le registre.</span><span class="sxs-lookup"><span data-stu-id="fe047-135">Use the registry-based static proxy configuration.</span></span>

1. <span data-ttu-id="fe047-136">Ouvrir une ligne de commandes avec élévation de privilèges :</span><span class="sxs-lookup"><span data-stu-id="fe047-136">Open an elevated command-line:</span></span>
    1. <span data-ttu-id="fe047-137">Accéder à **Démarrer** et taper **cmd**</span><span class="sxs-lookup"><span data-stu-id="fe047-137">Go to **Start** and type **cmd**</span></span>
    1. <span data-ttu-id="fe047-138">Cliquez avec le bouton droit sur **Invite de commandes** et sélectionnez **Exécuter en tant qu'administrateur**.</span><span class="sxs-lookup"><span data-stu-id="fe047-138">Right-click **Command prompt** and select **Run as administrator**.</span></span>
2.  <span data-ttu-id="fe047-139">Entrez la commande suivante et appuyez sur **Entrée** :</span><span class="sxs-lookup"><span data-stu-id="fe047-139">Enter the following command and press **Enter**:</span></span>

    `netsh winhttp set proxy <proxy>:<port>`

    <span data-ttu-id="fe047-140">Par exemple : **netsh winhttp initialiser proxy 10.0.0.6:8080**</span><span class="sxs-lookup"><span data-stu-id="fe047-140">For example: **netsh winhttp set proxy 10.0.0.6:8080**</span></span>

3. <span data-ttu-id="fe047-141">Pour réinitialiser le proxy winhttp, entrez la commande suivante et appuyez sur **Entrée** :</span><span class="sxs-lookup"><span data-stu-id="fe047-141">To reset the winhttp proxy, enter the following command and press **Enter**:</span></span>

     `netsh winhttp reset proxy`

<span data-ttu-id="fe047-142">Pour plus d’informations, voir [la syntaxe, les contextes et le formatage de la commande Netsh](/windows-server/networking/technologies/netsh/netsh-contexts).</span><span class="sxs-lookup"><span data-stu-id="fe047-142">See [Netsh Command Syntax, Contexts, and Formatting](/windows-server/networking/technologies/netsh/netsh-contexts) to learn more.</span></span>


## <a name="enable-access-to-endpoint-dlp-cloud-service-urls-in-the-proxy-server"></a><span data-ttu-id="fe047-143">Activer l’accès aux URL des services cloud DLP de point de terminaison dans le serveur proxy</span><span class="sxs-lookup"><span data-stu-id="fe047-143">Enable access to Endpoint DLP cloud service URLs in the proxy server</span></span>

<span data-ttu-id="fe047-144">Si un proxy ou un pare-feu bloque tout le trafic par défaut et n'autorise le passage que de domaines spécifiques, ajoutez les domaines énumérés dans la feuille téléchargeable à la liste des domaines autorisés.</span><span class="sxs-lookup"><span data-stu-id="fe047-144">If a proxy or firewall is blocking all traffic by default and allowing only specific domains through, add the domains listed in the downloadable sheet to the allowed domains list.</span></span>

<span data-ttu-id="fe047-145">Cette [de calcul téléchargeable](https://github.com/MicrosoftDocs/windows-itpro-docs/raw/public/windows/security/threat-protection/microsoft-defender-atp/downloads/mdatp-urls.xlsx) énumère les services et leurs URL associés auxquels votre réseau doit pouvoir se connecter.</span><span class="sxs-lookup"><span data-stu-id="fe047-145">This [downloadable spreadsheet](https://github.com/MicrosoftDocs/windows-itpro-docs/raw/public/windows/security/threat-protection/microsoft-defender-atp/downloads/mdatp-urls.xlsx) lists the services and their associated URLs that your network must be able to connect to.</span></span> <span data-ttu-id="fe047-146">Vous devez vous assurer qu'il n'y a pas de pare-feu ou de règles de filtrage du réseau qui refuseraient l'accès à ces URL, ou vous pouvez avoir besoin de créer une règle d'autorisation spécifique pour eux.</span><span class="sxs-lookup"><span data-stu-id="fe047-146">You should ensure that there are no firewall or network filtering rules that would deny access to these URLs, or you may need to create an allow rule specifically for them.</span></span>

<span data-ttu-id="fe047-147">Si l’analyse HTTPS (inspection SSL) est activée pour un proxy ou un pare-feu, excluez les domaines répertoriés dans le tableau ci-dessus de l’analyse HTTPS.</span><span class="sxs-lookup"><span data-stu-id="fe047-147">If a proxy or firewall has HTTPS scanning (SSL inspection) enabled, exclude the domains listed in the above table from HTTPS scanning.</span></span>
<span data-ttu-id="fe047-148">Si un proxy ou un pare-feu bloque le trafic anonyme, étant donné que le point de terminaison DLP se connecte à partir du contexte système, assurez-vous que le trafic anonyme est autorisé dans les URL répertoriées précédemment.</span><span class="sxs-lookup"><span data-stu-id="fe047-148">If a proxy or firewall is blocking anonymous traffic, as Endpoint DLP is connecting from system context, make sure anonymous traffic is permitted in the previously listed URLs.</span></span>

## <a name="verify-client-connectivity-to-microsoft-cloud-service-urls"></a><span data-ttu-id="fe047-149">Vérifier la connectivité du client aux URL des services cloud Microsoft</span><span class="sxs-lookup"><span data-stu-id="fe047-149">Verify client connectivity to Microsoft cloud service URLs</span></span>

<span data-ttu-id="fe047-150">Vérifier que la configuration du proxy a été effectuée avec succès, que WinHTTP peut découvrir et communiquer par le biais du serveur proxy dans votre environnement, et que le serveur proxy permet le trafic vers les URL du service Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="fe047-150">Verify the proxy configuration completed successfully, that WinHTTP can discover and communicate through the proxy server in your environment, and that the proxy server allows traffic to the Defender for Endpoint service URLs.</span></span>

1. <span data-ttu-id="fe047-151">Téléchargez l’ [outil Analyseur de client MDATP](https://aka.ms/mdatpanalyzer) sur le PC sur lequel la DLP de point de terminaison est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="fe047-151">Download the [MDATP Client Analyzer tool](https://aka.ms/mdatpanalyzer) to the PC where Endpoint DLP is running on.</span></span>
2. <span data-ttu-id="fe047-152">Extraire le contenu de MDATPClientAnalyzer.zip sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="fe047-152">Extract the contents of MDATPClientAnalyzer.zip on the device.</span></span>
3. <span data-ttu-id="fe047-153">Ouvrir une ligne de commandes avec élévation de privilèges :</span><span class="sxs-lookup"><span data-stu-id="fe047-153">Open an elevated command-line:</span></span>
    1. <span data-ttu-id="fe047-154">Accéder à **Démarrer** et taper **cmd**.</span><span class="sxs-lookup"><span data-stu-id="fe047-154">Go to **Start** and type **cmd**.</span></span>
    1. <span data-ttu-id="fe047-155">Cliquez avec le bouton droit sur **Invite de commandes** et sélectionnez **Exécuter en tant qu'administrateur**.</span><span class="sxs-lookup"><span data-stu-id="fe047-155">Right-click **Command prompt** and select **Run as administrator**.</span></span>
4.  <span data-ttu-id="fe047-156">Entrez la commande suivante et appuyez sur **Entrée** :</span><span class="sxs-lookup"><span data-stu-id="fe047-156">Enter the following command and press **Enter**:</span></span>
    
`HardDrivePath\MDATPClientAnalyzer.cmd`

<span data-ttu-id="fe047-157">Remplacez la *HardDrivePath* par le chemin d’accès dans lequel l’outil MDATPClientAnalyzer automatiquement a été téléchargé, par exemple.</span><span class="sxs-lookup"><span data-stu-id="fe047-157">Replace *HardDrivePath* with the path where the MDATPClientAnalyzer tool was downloaded to, for example</span></span>
    
<span data-ttu-id="fe047-158">**C:\Work\tools\MDATPClientAnalyzer\MDATPClientAnalyzer.cmd**</span><span class="sxs-lookup"><span data-stu-id="fe047-158">**C:\Work\tools\MDATPClientAnalyzer\MDATPClientAnalyzer.cmd**</span></span>


5.  <span data-ttu-id="fe047-159">Extraire le fichier **MDATPClientAnalysult.zip** _ créé par l’outil dans le dossier utilisé dans le _HardDrivePath\*.</span><span class="sxs-lookup"><span data-stu-id="fe047-159">Extract the **MDATPClientAnalyzerResult.zip** _ file created by tool in the folder used in the _HardDrivePath\*.</span></span>

6.  <span data-ttu-id="fe047-160">Open **MDATPClientAnalyzerResult.txt** et vérifiez que vous avez effectué les étapes de configuration du proxy pour permettre la découverte du serveur et l'accès aux URL des services.</span><span class="sxs-lookup"><span data-stu-id="fe047-160">Open **MDATPClientAnalyzerResult.txt** and verify that you have performed the proxy configuration steps to enable server discovery and access to the service URLs.</span></span>  <span data-ttu-id="fe047-161">L'outil vérifie la connectivité des URL du service Defender for Endpoint avec lesquelles le client Defender for Endpoint est configuré pour interagir.</span><span class="sxs-lookup"><span data-stu-id="fe047-161">The tool checks the connectivity of Defender for Endpoint service URLs that Defender for Endpoint client is configured to interact with.</span></span> <span data-ttu-id="fe047-162">Il imprime ensuite les résultats dans le fichier **MDATPClientAnalyzerResult.txt** pour chaque URL pouvant être utilisée pour communiquer avec Defender pour les services Endpoint.</span><span class="sxs-lookup"><span data-stu-id="fe047-162">It then prints the results into the **MDATPClientAnalyzerResult.txt** file for each URL that can potentially be used to communicate with the Defender for Endpoint services.</span></span> <span data-ttu-id="fe047-163">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="fe047-163">For example:</span></span>

    <span data-ttu-id="fe047-164">**URL de test : https://xxx.microsoft.com/xxx </br> 1 – Proxy par défaut : Réussite (200) </br> 2 – Découverte automatique du proxy (WPAD) : Réussite (200)</br> 3 – Proxy désactivé : Réussite (200)</br> 4 – Proxy nommé : n’existe pas</br> 5 – Proxy ligne de commande : n’existe pas**</span><span class="sxs-lookup"><span data-stu-id="fe047-164">**Testing URL : https://xxx.microsoft.com/xxx </br> 1 - Default proxy: Succeeded (200) </br> 2 - Proxy auto discovery (WPAD): Succeeded (200)</br> 3 - Proxy disabled: Succeeded (200)</br> 4 - Named proxy: Doesn't exist</br> 5 - Command line proxy: Doesn't exist**</span></span></br>


<span data-ttu-id="fe047-165">Si au moins une des options de connectivité renvoie un état (200), le client Defender pour le point de terminaison peut communiquer avec l’URL testée correctement à l’aide de cette méthode de connectivité.</span><span class="sxs-lookup"><span data-stu-id="fe047-165">If at least one of the connectivity options returns a (200) status, then the Defender for Endpoint client can communicate with the tested URL properly using this connectivity method.</span></span> 

<span data-ttu-id="fe047-166">Toutefois, si les résultats du contrôle de la connectivité indiquent un échec, une erreur HTTP est affichée (voir Codes d'état HTTP).</span><span class="sxs-lookup"><span data-stu-id="fe047-166">However, if the connectivity check results indicate a failure, an HTTP error is displayed (see HTTP Status Codes).</span></span> <span data-ttu-id="fe047-167">Vous pouvez ensuite utiliser les URL du tableau figurant dans la section [Activer l'accès aux URL du service DLP dans le nuage de points terminaux dans le serveur proxy](#enable-access-to-endpoint-dlp-cloud-service-urls-in-the-proxy-server).</span><span class="sxs-lookup"><span data-stu-id="fe047-167">You can then use the URLs in the table shown in [Enable access to Endpoint DLP cloud service URLs in the proxy server](#enable-access-to-endpoint-dlp-cloud-service-urls-in-the-proxy-server).</span></span> <span data-ttu-id="fe047-168">Les URL que vous utiliserez dépendent de la région sélectionnée au cours de la procédure d’intégration.</span><span class="sxs-lookup"><span data-stu-id="fe047-168">The URLs you’ll use will depend on the region selected during the onboarding procedure.</span></span>
[!NOTE]<span data-ttu-id="fe047-169"> L’outil Analyseur de connectivité n’est pas compatible avec la règle ASR [Bloquer les créations de processus en provenance des commandes PSExec et WMI](/windows/security/threat-protection/windows-defender-exploit-guard/attack-surface-reduction#attack-surface-reduction-rules).</span><span class="sxs-lookup"><span data-stu-id="fe047-169"> The Connectivity Analyzer tool is not compatible with ASR rule [Block process creations originating from PSExec and WMI commands](/windows/security/threat-protection/windows-defender-exploit-guard/attack-surface-reduction#attack-surface-reduction-rules).</span></span> <span data-ttu-id="fe047-170">Vous devrez désactiver temporairement cette règle pour exécuter l’outil connectivité.</span><span class="sxs-lookup"><span data-stu-id="fe047-170">You will need to temporarily disable this rule to run the connectivity tool.</span></span>

[!NOTE] <span data-ttu-id="fe047-171">Lorsque le TelemetryProxyServer est défini, dans le Registre ou via une stratégie de groupe, Le Defender for Endpoint se rabattra sur le direct s'il ne peut pas accéder au proxy défini.</span><span class="sxs-lookup"><span data-stu-id="fe047-171">When the TelemetryProxyServer is set, in Registry or via Group Policy, Defender for Endpoint will fall back to direct if it can’t access the defined proxy.</span></span>
<span data-ttu-id="fe047-172">Sujets connexes – Périphériques Windows 10 embarqués – Dépannage des problèmes d'embarquement des DLP Microsoft Endpoint</span><span class="sxs-lookup"><span data-stu-id="fe047-172">Related topics •   Onboard Windows 10 devices •   Troubleshoot Microsoft Endpoint DLP onboarding issues</span></span>





## <a name="see-also"></a><span data-ttu-id="fe047-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe047-173">See also</span></span>

- [<span data-ttu-id="fe047-174">En savoir plus sur les points de terminaison de protection contre la perte de données (Preview)</span><span class="sxs-lookup"><span data-stu-id="fe047-174">Learn about Endpoint data loss prevention </span></span>](endpoint-dlp-learn-about.md)
- [<span data-ttu-id="fe047-175">Utilisation des points de terminaison de protection contre la perte de données (aperçu)</span><span class="sxs-lookup"><span data-stu-id="fe047-175">Using Endpoint data loss prevention </span></span>](endpoint-dlp-using.md)
- [<span data-ttu-id="fe047-176">Vue d’ensemble de la protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="fe047-176">Overview of data loss prevention</span></span>](data-loss-prevention-policies.md)
- [<span data-ttu-id="fe047-177">Création, test et réglage d’une stratégie DLP</span><span class="sxs-lookup"><span data-stu-id="fe047-177">Create, test, and tune a DLP policy</span></span>](create-test-tune-dlp-policy.md)
- [<span data-ttu-id="fe047-178">Prise en main de l’explorateur d’activités</span><span class="sxs-lookup"><span data-stu-id="fe047-178">Get started with Activity explorer</span></span>](data-classification-activity-explorer.md)
- [<span data-ttu-id="fe047-179">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="fe047-179">Microsoft Defender for Endpoint</span></span>](/windows/security/threat-protection/)
- <span data-ttu-id="fe047-180">[Outils et méthodes d’intégration pour les appareils Windows 10](/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints).</span><span class="sxs-lookup"><span data-stu-id="fe047-180">[Onboarding tools and methods for Windows 10 machines](/windows/security/threat-protection/microsoft-defender-atp/configure-endpoints)</span></span>
- [<span data-ttu-id="fe047-181">Abonnement Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="fe047-181">Microsoft 365 subscription</span></span>](https://www.microsoft.com/microsoft-365/compare-microsoft-365-enterprise-plans?rtc=1)
- [<span data-ttu-id="fe047-182">Azure AD appareils joints</span><span class="sxs-lookup"><span data-stu-id="fe047-182">Azure AD joined devices</span></span>](/azure/active-directory/devices/concept-azure-ad-join)
- [<span data-ttu-id="fe047-183">Télécharger le nouveau Microsoft Edge sur la base de chrome</span><span class="sxs-lookup"><span data-stu-id="fe047-183">Download the new Microsoft Edge based on Chromium</span></span>](https://support.microsoft.com/help/4501095/download-the-new-microsoft-edge-based-on-chromium)