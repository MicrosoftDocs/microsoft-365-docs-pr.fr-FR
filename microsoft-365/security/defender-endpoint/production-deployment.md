---
title: Configurer Microsoft Defender pour le déploiement de point de terminaison
description: Découvrez comment configurer le déploiement de Microsoft Defender pour endpoint
keywords: déployer, configuration, validation de licence, configuration du client, configuration réseau
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
- M365-security-compliance
- m365solution-endpointprotect
- m365solution-scenario
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 6b49565c45c1f38d0d2ce71b097af079782ba4de
ms.sourcegitcommit: 17f0aada83627d9defa0acf4db03a2d58e46842f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "52636193"
---
# <a name="set-up-microsoft-defender-for-endpoint-deployment"></a><span data-ttu-id="d2c78-104">Configurer Microsoft Defender pour le déploiement de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="d2c78-104">Set up Microsoft Defender for Endpoint deployment</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="d2c78-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="d2c78-105">**Applies to:**</span></span>
- [<span data-ttu-id="d2c78-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="d2c78-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="d2c78-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="d2c78-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="d2c78-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="d2c78-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="d2c78-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="d2c78-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="d2c78-110">Le déploiement de Defender pour endpoint est un processus en trois phases :</span><span class="sxs-lookup"><span data-stu-id="d2c78-110">Deploying Defender for Endpoint is a three-phase process:</span></span>

| <span data-ttu-id="d2c78-111">[![phase de déploiement : préparer](images/phase-diagrams/prepare.png)](prepare-deployment.md)</span><span class="sxs-lookup"><span data-stu-id="d2c78-111">[![deployment phase - prepare](images/phase-diagrams/prepare.png)](prepare-deployment.md)</span></span><br>[<span data-ttu-id="d2c78-112">Phase 1 : préparation</span><span class="sxs-lookup"><span data-stu-id="d2c78-112">Phase 1: Prepare</span></span>](prepare-deployment.md) | ![phase de déploiement : configuration](images/phase-diagrams/setup.png)<br><span data-ttu-id="d2c78-114">Phase 2 : configuration</span><span class="sxs-lookup"><span data-stu-id="d2c78-114">Phase 2: Setup</span></span> | <span data-ttu-id="d2c78-115">[![phase de déploiement : intégration](images/phase-diagrams/onboard.png)](onboarding.md)</span><span class="sxs-lookup"><span data-stu-id="d2c78-115">[![deployment phase - onboard](images/phase-diagrams/onboard.png)](onboarding.md)</span></span><br>[<span data-ttu-id="d2c78-116">Phase 3 : intégration</span><span class="sxs-lookup"><span data-stu-id="d2c78-116">Phase 3: Onboard</span></span>](onboarding.md) |
| ----- | ----- | ----- |
| | <span data-ttu-id="d2c78-117">*Vous êtes là !*</span><span class="sxs-lookup"><span data-stu-id="d2c78-117">*You are here!*</span></span>||

<span data-ttu-id="d2c78-118">Vous êtes actuellement en phase de mise en place.</span><span class="sxs-lookup"><span data-stu-id="d2c78-118">You are currently in the set-up phase.</span></span>

<span data-ttu-id="d2c78-119">Dans ce scénario de déploiement, vous serez guidé dans les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="d2c78-119">In this deployment scenario, you'll be guided through the steps on:</span></span>
- <span data-ttu-id="d2c78-120">Validation des licences</span><span class="sxs-lookup"><span data-stu-id="d2c78-120">Licensing validation</span></span>
- <span data-ttu-id="d2c78-121">Configuration du client</span><span class="sxs-lookup"><span data-stu-id="d2c78-121">Tenant configuration</span></span>
- <span data-ttu-id="d2c78-122">Configuration réseau</span><span class="sxs-lookup"><span data-stu-id="d2c78-122">Network configuration</span></span>


>[!NOTE]
><span data-ttu-id="d2c78-123">Pour vous guider tout au long d’un déploiement classique, ce scénario couvre uniquement l’utilisation des Microsoft Endpoint Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d2c78-123">For the purpose of guiding you through a typical deployment, this scenario will only cover the use of Microsoft Endpoint Configuration Manager.</span></span> <span data-ttu-id="d2c78-124">Defender pour le point de terminaison prend en charge l’utilisation d’autres outils d’intégration, mais ne couvre pas ces scénarios dans le guide de déploiement.</span><span class="sxs-lookup"><span data-stu-id="d2c78-124">Defender for Endpoint supports the use of other onboarding tools but won't cover those scenarios in the deployment guide.</span></span> <span data-ttu-id="d2c78-125">Pour plus d’informations, [voir Appareils intégrés à Microsoft Defender pour le point de terminaison.](onboard-configure.md)</span><span class="sxs-lookup"><span data-stu-id="d2c78-125">For more information, see [Onboard devices to Microsoft Defender for Endpoint](onboard-configure.md).</span></span>

## <a name="check-license-state"></a><span data-ttu-id="d2c78-126">Vérifier l’état de la licence</span><span class="sxs-lookup"><span data-stu-id="d2c78-126">Check license state</span></span>

<span data-ttu-id="d2c78-127">La vérification de l’état de la licence et si elle a été correctement mise en service peut être effectuée via le Centre d’administration ou via **le portail Microsoft Azure.**</span><span class="sxs-lookup"><span data-stu-id="d2c78-127">Checking for the license state and whether it got properly provisioned, can be done through the admin center or through the **Microsoft Azure portal**.</span></span>

1. <span data-ttu-id="d2c78-128">Pour afficher vos licences, accédez au portail **Microsoft Azure et** accédez à la section [Microsoft Azure licences du portail.](https://portal.azure.com/#blade/Microsoft_AAD_IAM/LicensesMenuBlade/Products)</span><span class="sxs-lookup"><span data-stu-id="d2c78-128">To view your licenses, go to the **Microsoft Azure portal** and navigate to the [Microsoft Azure portal license section](https://portal.azure.com/#blade/Microsoft_AAD_IAM/LicensesMenuBlade/Products).</span></span>

   ![Image de la page de gestion des licences Azure](images/atp-licensing-azure-portal.png)

1. <span data-ttu-id="d2c78-130">Vous pouvez également accéder au Centre d’administration pour accéder **aux**  >  **abonnements de facturation.**</span><span class="sxs-lookup"><span data-stu-id="d2c78-130">Alternately, in the admin center, navigate to **Billing** > **Subscriptions**.</span></span>

    <span data-ttu-id="d2c78-131">Sur l’écran, vous verrez toutes les licences provisionées et leur état **actuel.**</span><span class="sxs-lookup"><span data-stu-id="d2c78-131">On the screen, you'll see all the provisioned licenses and their current **Status**.</span></span>

    ![Image des licences de facturation](images/atp-billing-subscriptions.png)


## <a name="cloud-service-provider-validation"></a><span data-ttu-id="d2c78-133">Validation du fournisseur de services Cloud</span><span class="sxs-lookup"><span data-stu-id="d2c78-133">Cloud Service Provider validation</span></span>

<span data-ttu-id="d2c78-134">Pour accéder aux licences qui sont provisionn es pour votre entreprise et vérifier l’état des licences, accédez au Centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="d2c78-134">To gain access into which licenses are provisioned to your company, and to check the state of the licenses, go to the admin center.</span></span>

1. <span data-ttu-id="d2c78-135">À partir du **portail partenaire,** **sélectionnez Administrer les services > Office 365**.</span><span class="sxs-lookup"><span data-stu-id="d2c78-135">From the **Partner portal**, select **Administer services > Office 365**.</span></span>

2. <span data-ttu-id="d2c78-136">En cliquant sur le **lien du portail** partenaire, l’option **Administrateur** de la part de s’ouvre et vous donne accès au Centre d’administration du client.</span><span class="sxs-lookup"><span data-stu-id="d2c78-136">Clicking on the **Partner portal** link will open the **Admin on behalf** option and will give you access to the customer admin center.</span></span>

   ![Image du portail d’administration O365](images/atp-O365-admin-portal-customer.png)



## <a name="tenant-configuration"></a><span data-ttu-id="d2c78-138">Configuration du client</span><span class="sxs-lookup"><span data-stu-id="d2c78-138">Tenant Configuration</span></span>
<span data-ttu-id="d2c78-139">L’intégration à Microsoft Defender pour le point de terminaison est facile.</span><span class="sxs-lookup"><span data-stu-id="d2c78-139">Onboarding to Microsoft Defender for Endpoint is easy.</span></span> <span data-ttu-id="d2c78-140">Dans le menu de navigation, sélectionnez n’importe quel élément sous la section Points de terminaison ou toute fonctionnalité Microsoft 365 Defender telle que les incidents, le chasse, le centre de traitement ou l’analyse des menaces pour lancer le processus d’intégration.</span><span class="sxs-lookup"><span data-stu-id="d2c78-140">From the navigation menu, select any item under the Endpoints section, or any Microsoft 365 Defender feature such as Incidents, Hunting, Action center, or Threat analytics to initiate the onboarding process.</span></span>

<span data-ttu-id="d2c78-141">À partir d’un navigateur web, accédez au [centre Microsoft 365 sécurité.](https://security.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="d2c78-141">From a web browser, navigate to the [Microsoft 365 Security Center](https://security.microsoft.com).</span></span>

## <a name="network-configuration"></a><span data-ttu-id="d2c78-142">Configuration réseau</span><span class="sxs-lookup"><span data-stu-id="d2c78-142">Network configuration</span></span>
<span data-ttu-id="d2c78-143">Si l’organisation n’exige pas que les points de terminaison utilisent un proxy pour accéder à Internet, ignorez cette section.</span><span class="sxs-lookup"><span data-stu-id="d2c78-143">If the organization doesn't require the endpoints to use a Proxy to access the Internet, skip this section.</span></span>

<span data-ttu-id="d2c78-144">Le capteur Microsoft Defender pour point de terminaison requiert Microsoft Windows HTTP (WinHTTP) pour signaler les données du capteur et communiquer avec le service Microsoft Defender pour point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="d2c78-144">The Microsoft Defender for Endpoint sensor requires Microsoft Windows HTTP (WinHTTP) to report sensor data and communicate with the Microsoft Defender for Endpoint service.</span></span> <span data-ttu-id="d2c78-145">Le capteur Microsoft Defender for Endpoint incorporé s’exécute dans le contexte système à l’aide du compte LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="d2c78-145">The embedded Microsoft Defender for Endpoint sensor runs in the system context using the LocalSystem account.</span></span> <span data-ttu-id="d2c78-146">Le capteur utilise les services Microsoft Windows HTTP Services (WinHTTP) pour activer la communication avec le service Cloud Microsoft Defender pour point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="d2c78-146">The sensor uses Microsoft Windows HTTP Services (WinHTTP) to enable communication with the Microsoft Defender for Endpoint cloud service.</span></span> <span data-ttu-id="d2c78-147">Le paramètre de configuration WinHTTP est indépendant des paramètres de proxy de navigation Internet Windows Internet (WinINet) et peut uniquement découvrir un serveur proxy à l’aide des méthodes de découverte suivantes :</span><span class="sxs-lookup"><span data-stu-id="d2c78-147">The WinHTTP configuration setting is independent of the Windows Internet (WinINet) internet browsing proxy settings and can only discover a proxy server by using the following discovery methods:</span></span>

<span data-ttu-id="d2c78-148">**Méthodes de découverte automatique :**</span><span class="sxs-lookup"><span data-stu-id="d2c78-148">**Autodiscovery methods:**</span></span>

-   <span data-ttu-id="d2c78-149">Proxy transparent</span><span class="sxs-lookup"><span data-stu-id="d2c78-149">Transparent proxy</span></span>

-   <span data-ttu-id="d2c78-150">WPAD (Web Proxy Autodiscovery Protocol)</span><span class="sxs-lookup"><span data-stu-id="d2c78-150">Web Proxy Autodiscovery Protocol (WPAD)</span></span>

<span data-ttu-id="d2c78-151">Si un proxy transparent ou un WPAD a été implémenté dans la topologie réseau, il n’est pas nécessaire de définir des paramètres de configuration spéciaux.</span><span class="sxs-lookup"><span data-stu-id="d2c78-151">If a Transparent proxy or WPAD has been implemented in the network topology, there is no need for special configuration settings.</span></span> <span data-ttu-id="d2c78-152">Pour plus d’informations sur les exclusions d’URL de point de terminaison Microsoft Defender dans le proxy, consultez la section URL du [service](production-deployment.md#proxy-service-urls) proxy dans ce document pour la liste des URL autoriser ou sur configurer les [paramètres](configure-proxy-internet.md#enable-access-to-microsoft-defender-for-endpoint-service-urls-in-the-proxy-server)de connectivité Internet et proxy de périphérique.</span><span class="sxs-lookup"><span data-stu-id="d2c78-152">For more information on Microsoft Defender for Endpoint URL exclusions in the proxy, see the [Proxy Service URLs](production-deployment.md#proxy-service-urls) section in this document for the URLs allow list or on [Configure device proxy and Internet connectivity settings](configure-proxy-internet.md#enable-access-to-microsoft-defender-for-endpoint-service-urls-in-the-proxy-server).</span></span>

<span data-ttu-id="d2c78-153">**Configuration manuelle du proxy statique :**</span><span class="sxs-lookup"><span data-stu-id="d2c78-153">**Manual static proxy configuration:**</span></span>

-   <span data-ttu-id="d2c78-154">Configuration basée sur le registre</span><span class="sxs-lookup"><span data-stu-id="d2c78-154">Registry-based configuration</span></span>

-   <span data-ttu-id="d2c78-155">WinHTTP configuré à l’aide de la commande netsh</span><span class="sxs-lookup"><span data-stu-id="d2c78-155">WinHTTP configured using netsh command</span></span> <br> <span data-ttu-id="d2c78-156">Convient uniquement aux ordinateurs de bureau dans une topologie stable (par exemple : un bureau dans un réseau d’entreprise derrière le même proxy)</span><span class="sxs-lookup"><span data-stu-id="d2c78-156">Suitable only for desktops in a stable topology (for example: a desktop in a corporate network behind the same proxy)</span></span>

### <a name="configure-the-proxy-server-manually-using-a-registry-based-static-proxy"></a><span data-ttu-id="d2c78-157">Configurer le serveur proxy manuellement en utilisant un proxy statique basé sur le registre</span><span class="sxs-lookup"><span data-stu-id="d2c78-157">Configure the proxy server manually using a registry-based static proxy</span></span>

<span data-ttu-id="d2c78-158">Configurez un proxy statique basé sur le Registre pour autoriser uniquement le capteur Microsoft Defender for Endpoint à signaler les données de diagnostic et à communiquer avec Microsoft Defender pour les services Endpoint si un ordinateur n’est pas autorisé à se connecter à Internet.</span><span class="sxs-lookup"><span data-stu-id="d2c78-158">Configure a registry-based static proxy to allow only Microsoft Defender for Endpoint sensor to report diagnostic data and communicate with Microsoft Defender for Endpoint services if a computer isn't permitted to connect to the Internet.</span></span> <span data-ttu-id="d2c78-159">Le proxy statique est configurable via une stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2c78-159">The static proxy is configurable through Group Policy (GP).</span></span> <span data-ttu-id="d2c78-160">La stratégie de groupe se trouve sous :</span><span class="sxs-lookup"><span data-stu-id="d2c78-160">The group policy can be found under:</span></span>

 - <span data-ttu-id="d2c78-161">Modèles d Windows de collecte de données et de builds d’aperçu des composants Configurez l’utilisation du proxy authentifié pour le service Expériences des utilisateurs connectés et \> \> \> télémétrie</span><span class="sxs-lookup"><span data-stu-id="d2c78-161">Administrative Templates \> Windows Components \> Data Collection and Preview Builds \> Configure Authenticated Proxy usage for the Connected User Experience and Telemetry Service</span></span>
     - <span data-ttu-id="d2c78-162">Définissez-le **sur Activé et** sélectionnez Désactiver **l’utilisation du proxy authentifié**</span><span class="sxs-lookup"><span data-stu-id="d2c78-162">Set it to **Enabled** and select **Disable Authenticated Proxy usage**</span></span>

1. <span data-ttu-id="d2c78-163">Ouvrez la console de gestion des stratégies de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2c78-163">Open the Group Policy Management Console.</span></span>
2. <span data-ttu-id="d2c78-164">Créez une stratégie ou modifiez une stratégie existante en fonction des pratiques organisationnelles.</span><span class="sxs-lookup"><span data-stu-id="d2c78-164">Create a policy or edit an existing policy based off the organizational practices.</span></span>
3. <span data-ttu-id="d2c78-165">Modifiez la stratégie de groupe et accédez à Modèles d’administration Windows Collection de données des composants et Builds d’aperçu Configurer l’utilisation du proxy authentifié pour le service Expériences des **\> utilisateurs connectés \> \>** et télémétrie.</span><span class="sxs-lookup"><span data-stu-id="d2c78-165">Edit the Group Policy and navigate to **Administrative Templates \> Windows Components \> Data Collection and Preview Builds \> Configure Authenticated Proxy usage for the Connected User Experience and Telemetry Service**.</span></span> 
    <span data-ttu-id="d2c78-166">![Image de la configuration de la stratégie de groupe](images/atp-gpo-proxy1.png)</span><span class="sxs-lookup"><span data-stu-id="d2c78-166">![Image of Group Policy configuration](images/atp-gpo-proxy1.png)</span></span>

4. <span data-ttu-id="d2c78-167">Sélectionnez **Activé**.</span><span class="sxs-lookup"><span data-stu-id="d2c78-167">Select **Enabled**.</span></span>
5. <span data-ttu-id="d2c78-168">Sélectionnez **Désactiver l’utilisation du proxy authentifié.**</span><span class="sxs-lookup"><span data-stu-id="d2c78-168">Select **Disable Authenticated Proxy usage**.</span></span>
   
6. <span data-ttu-id="d2c78-169">Accédez à Modèles d’administration Windows collecte de données des composants et prévisualisation Permet de configurer les expériences utilisateur connectées **\> et la \> \> télémétrie.**</span><span class="sxs-lookup"><span data-stu-id="d2c78-169">Navigate to **Administrative Templates \> Windows Components \> Data Collection and Preview Builds \> Configure connected user experiences and telemetry**.</span></span>
    <span data-ttu-id="d2c78-170">![Image du paramètre de configuration de la stratégie de groupe](images/atp-gpo-proxy2.png)</span><span class="sxs-lookup"><span data-stu-id="d2c78-170">![Image of Group Policy configuration setting](images/atp-gpo-proxy2.png)</span></span>
7. <span data-ttu-id="d2c78-171">Sélectionnez **Activé**.</span><span class="sxs-lookup"><span data-stu-id="d2c78-171">Select **Enabled**.</span></span>
8. <span data-ttu-id="d2c78-172">Entrez le **nom du serveur proxy.**</span><span class="sxs-lookup"><span data-stu-id="d2c78-172">Enter the **Proxy Server Name**.</span></span>

<span data-ttu-id="d2c78-173">La stratégie définit deux valeurs de registre `TelemetryProxyServer` comme REG_SZ et `DisableEnterpriseAuthProxy` comme REG_DWORD sous la clé de registre `HKLM\Software\Policies\Microsoft\Windows\DataCollection`.</span><span class="sxs-lookup"><span data-stu-id="d2c78-173">The policy sets two registry values `TelemetryProxyServer` as REG_SZ and `DisableEnterpriseAuthProxy` as REG_DWORD under the registry key `HKLM\Software\Policies\Microsoft\Windows\DataCollection`.</span></span>

<span data-ttu-id="d2c78-174">La valeur de Registre `TelemetryProxyServer` prend le format de chaîne suivant :</span><span class="sxs-lookup"><span data-stu-id="d2c78-174">The registry value `TelemetryProxyServer` takes the following string format:</span></span>

```text
<server name or ip>:<port>
```

<span data-ttu-id="d2c78-175">Par exemple, 10.0.0.6:8080</span><span class="sxs-lookup"><span data-stu-id="d2c78-175">For example: 10.0.0.6:8080</span></span>

<span data-ttu-id="d2c78-176">Cette valeur de registre `DisableEnterpriseAuthProxy` doit être égale à 1.</span><span class="sxs-lookup"><span data-stu-id="d2c78-176">The registry value `DisableEnterpriseAuthProxy` should be set to 1.</span></span>

###  <a name="configure-the-proxy-server-manually-using-netsh-command"></a><span data-ttu-id="d2c78-177">Configurer le serveur proxy manuellement à l’aide de la commande netsh</span><span class="sxs-lookup"><span data-stu-id="d2c78-177">Configure the proxy server manually using netsh command</span></span>

<span data-ttu-id="d2c78-178">Utiliser netsh pour configurer un proxy statique à l’échelle du système.</span><span class="sxs-lookup"><span data-stu-id="d2c78-178">Use netsh to configure a system-wide static proxy.</span></span>

> [!NOTE]
> - <span data-ttu-id="d2c78-179">Cela affectera toutes les applications, y compris les services Windows qui utilisent WinHTTP avec un proxy par défaut.</span><span class="sxs-lookup"><span data-stu-id="d2c78-179">This will affect all applications including Windows services which use WinHTTP with default proxy.</span></span></br>
> - <span data-ttu-id="d2c78-180">Les ordinateurs portables qui changent de topologie (par exemple, de bureau à domicile) ne fonctionneront pas correctement avec netsh.</span><span class="sxs-lookup"><span data-stu-id="d2c78-180">Laptops that are changing topology (for example: from office to home) will malfunction with netsh.</span></span> <span data-ttu-id="d2c78-181">Utiliser la configuration statique du proxy basée sur le registre.</span><span class="sxs-lookup"><span data-stu-id="d2c78-181">Use the registry-based static proxy configuration.</span></span>

1. <span data-ttu-id="d2c78-182">Ouvrez une invite de commandes avec élévation de privilèges :</span><span class="sxs-lookup"><span data-stu-id="d2c78-182">Open an elevated command line:</span></span>

    1. <span data-ttu-id="d2c78-183">Accéder à **Démarrer** et taper **cmd**.</span><span class="sxs-lookup"><span data-stu-id="d2c78-183">Go to **Start** and type **cmd**.</span></span>

    1. <span data-ttu-id="d2c78-184">Cliquez avec le bouton droit sur **Invite de commandes** et sélectionnez **Exécuter en tant qu'administrateur**.</span><span class="sxs-lookup"><span data-stu-id="d2c78-184">Right-click **Command prompt** and select **Run as administrator**.</span></span>

2. <span data-ttu-id="d2c78-185">Entrez la commande suivante et appuyez sur **Entrée** :</span><span class="sxs-lookup"><span data-stu-id="d2c78-185">Enter the following command and press **Enter**:</span></span>

   ```PowerShell
   netsh winhttp set proxy <proxy>:<port>
   ```

   <span data-ttu-id="d2c78-186">Par exemple : netsh winhttp initialiser proxy 10.0.0.6:8080</span><span class="sxs-lookup"><span data-stu-id="d2c78-186">For example: netsh winhttp set proxy 10.0.0.6:8080</span></span>


###  <a name="proxy-configuration-for-down-level-devices"></a><span data-ttu-id="d2c78-187">Configuration du proxy pour les appareils de niveau inférieur</span><span class="sxs-lookup"><span data-stu-id="d2c78-187">Proxy Configuration for down-level devices</span></span>

<span data-ttu-id="d2c78-188">Down-Level comprennent les stations de travail Windows 7 SP1 et Windows 8.1, ainsi que Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2 et les versions de Windows Server 2016 antérieures à Windows Server CB 1803.</span><span class="sxs-lookup"><span data-stu-id="d2c78-188">Down-Level devices include Windows 7 SP1 and Windows 8.1 workstations as well as Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2, and versions of Windows Server 2016 prior to Windows Server CB 1803.</span></span> <span data-ttu-id="d2c78-189">Le proxy de ces systèmes d’exploitation est configuré dans le cadre de l’agent de gestion Microsoft pour gérer les communications entre le point de terminaison et Azure.</span><span class="sxs-lookup"><span data-stu-id="d2c78-189">These operating systems will have the proxy configured as part of the Microsoft Management Agent to handle communication from the endpoint to Azure.</span></span> <span data-ttu-id="d2c78-190">Reportez-vous au Guide de déploiement rapide de l’agent de gestion Microsoft pour plus d’informations sur la configuration d’un proxy sur ces appareils.</span><span class="sxs-lookup"><span data-stu-id="d2c78-190">Refer to the Microsoft Management Agent Fast Deployment Guide for information on how a proxy is configured on these devices.</span></span>

### <a name="proxy-service-urls"></a><span data-ttu-id="d2c78-191">URL de service proxy</span><span class="sxs-lookup"><span data-stu-id="d2c78-191">Proxy Service URLs</span></span>
<span data-ttu-id="d2c78-192">Les URL qui incluent la version 20 sont nécessaires uniquement si vous avez des appareils Windows 10 version 1803 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="d2c78-192">URLs that include v20 in them are only needed if you have Windows 10, version 1803 or later devices.</span></span> <span data-ttu-id="d2c78-193">Par exemple, n’est nécessaire que si l’appareil est ```us-v20.events.data.microsoft.com``` Windows 10 version 1803 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="d2c78-193">For example, ```us-v20.events.data.microsoft.com``` is only needed if the device is on Windows 10, version 1803 or later.</span></span>
 

<span data-ttu-id="d2c78-194">Si un proxy ou un pare-feu bloque le trafic anonyme, comme le capteur Microsoft Defender pour point de terminaison se connecte à partir du contexte système, assurez-vous que le trafic anonyme est autorisé dans les URL répertoriées.</span><span class="sxs-lookup"><span data-stu-id="d2c78-194">If a proxy or firewall is blocking anonymous traffic, as Microsoft Defender for Endpoint sensor is connecting from system context, make sure anonymous traffic is permitted in the listed URLs.</span></span>

<span data-ttu-id="d2c78-195">La feuille de calcul téléchargeable suivante répertorie les services et les URL associées à qui votre réseau doit pouvoir se connecter.</span><span class="sxs-lookup"><span data-stu-id="d2c78-195">The following downloadable spreadsheet lists the services and their associated URLs that your network must be able to connect to.</span></span> <span data-ttu-id="d2c78-196">Assurez-vous qu’il n’existe aucune règle de pare-feu ou de  filtrage réseau qui refuserait l’accès à ces URL, ou vous devrez peut-être créer une règle d’autoriser spécifiquement pour eux.</span><span class="sxs-lookup"><span data-stu-id="d2c78-196">Ensure there are no firewall or network filtering rules that would deny access to these URLs, or you may need to create an *allow* rule specifically for them.</span></span>

|<span data-ttu-id="d2c78-197">**Liste de feuilles de calcul de domaines**</span><span class="sxs-lookup"><span data-stu-id="d2c78-197">**Spreadsheet of domains list**</span></span>|<span data-ttu-id="d2c78-198">**Description**</span><span class="sxs-lookup"><span data-stu-id="d2c78-198">**Description**</span></span>|
|:-----|:-----|
|![Image miniature de la feuille de calcul DES URL de Microsoft Defender pour les points de terminaison](images/mdatp-urls.png)<br/>  | <span data-ttu-id="d2c78-200">Feuille de calcul d’enregistrements DNS spécifiques pour les emplacements de service, les emplacements géographiques et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d2c78-200">Spreadsheet of specific DNS records for service locations, geographic locations, and OS.</span></span> <br><br>[<span data-ttu-id="d2c78-201">Téléchargez la feuille de calcul ici.</span><span class="sxs-lookup"><span data-stu-id="d2c78-201">Download the spreadsheet here.</span></span>](https://download.microsoft.com/download/8/a/5/8a51eee5-cd02-431c-9d78-a58b7f77c070/mde-urls.xlsx) 


###  <a name="microsoft-defender-for-endpoint-service-backend-ip-ranges"></a><span data-ttu-id="d2c78-202">Plages d’adresses IP back-end du service Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="d2c78-202">Microsoft Defender for Endpoint service backend IP ranges</span></span>

<span data-ttu-id="d2c78-203">Si vos périphériques réseau ne prisent pas en charge les règles DNS, utilisez plutôt des plages IP.</span><span class="sxs-lookup"><span data-stu-id="d2c78-203">If your network devices don't support DNS-based rules, use IP ranges instead.</span></span>

<span data-ttu-id="d2c78-204">Defender pour le point de terminaison est intégré au cloud Azure, déployé dans les régions suivantes :</span><span class="sxs-lookup"><span data-stu-id="d2c78-204">Defender for Endpoint is built in Azure cloud, deployed in the following regions:</span></span>

- <span data-ttu-id="d2c78-205">AzureCloud.eastus</span><span class="sxs-lookup"><span data-stu-id="d2c78-205">AzureCloud.eastus</span></span>
- <span data-ttu-id="d2c78-206">AzureCloud.eastus2</span><span class="sxs-lookup"><span data-stu-id="d2c78-206">AzureCloud.eastus2</span></span>
- <span data-ttu-id="d2c78-207">AzureCloud.westcentralus</span><span class="sxs-lookup"><span data-stu-id="d2c78-207">AzureCloud.westcentralus</span></span>
- <span data-ttu-id="d2c78-208">AzureCloud.northpé</span><span class="sxs-lookup"><span data-stu-id="d2c78-208">AzureCloud.northeurope</span></span>
- <span data-ttu-id="d2c78-209">AzureCloud.westpét</span><span class="sxs-lookup"><span data-stu-id="d2c78-209">AzureCloud.westeurope</span></span>
- <span data-ttu-id="d2c78-210">AzureCloud.uksouth</span><span class="sxs-lookup"><span data-stu-id="d2c78-210">AzureCloud.uksouth</span></span>
- <span data-ttu-id="d2c78-211">AzureCloud.ukwest</span><span class="sxs-lookup"><span data-stu-id="d2c78-211">AzureCloud.ukwest</span></span>

<span data-ttu-id="d2c78-212">Vous pouvez trouver les plages IP Azure dans [les plages IP azure](https://www.microsoft.com/download/details.aspx?id=56519)et les balises de service – Cloud public .</span><span class="sxs-lookup"><span data-stu-id="d2c78-212">You can find the Azure IP ranges in [Azure IP Ranges and Service Tags – Public Cloud](https://www.microsoft.com/download/details.aspx?id=56519).</span></span>

> [!NOTE]
> <span data-ttu-id="d2c78-213">En tant que solution informatique, les plages d’adresses IP peuvent changer.</span><span class="sxs-lookup"><span data-stu-id="d2c78-213">As a cloud-based solution, the IP address ranges can change.</span></span> <span data-ttu-id="d2c78-214">Il est recommandé de passer aux règles DNS.</span><span class="sxs-lookup"><span data-stu-id="d2c78-214">It's recommended you move to DNS-based rules.</span></span>

> [!NOTE]
> <span data-ttu-id="d2c78-215">Si vous êtes un client du gouvernement américain, consultez la section correspondante dans la page [Defender for Endpoint for US Government.](gov.md#service-backend-ip-ranges)</span><span class="sxs-lookup"><span data-stu-id="d2c78-215">If you are a US Government customer, please see the corresponding section in the [Defender for Endpoint for US Government](gov.md#service-backend-ip-ranges) page.</span></span>

## <a name="next-step"></a><span data-ttu-id="d2c78-216">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="d2c78-216">Next step</span></span>

<span data-ttu-id="d2c78-217">![**Phase 3 : Intégration**](images/onboard.png)</span><span class="sxs-lookup"><span data-stu-id="d2c78-217">![**Phase 3: Onboard**](images/onboard.png)</span></span> <br><span data-ttu-id="d2c78-218">[Phase 3 : Intégration :](onboarding.md)intégrer des appareils au service afin que le service Microsoft Defender pour point de terminaison puisse obtenir des données de capteur à partir de ces derniers.</span><span class="sxs-lookup"><span data-stu-id="d2c78-218">[Phase 3: Onboard](onboarding.md): Onboard devices to the service so that the Microsoft Defender for Endpoint service can get sensor data from them.</span></span> 
