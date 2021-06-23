---
title: Découverte et découverte de périphériques réseau gestion des vulnérabilités
description: Les recommandations de sécurité et la détection des vulnérabilités sont désormais disponibles pour les systèmes d’exploitation des commutateurs, routeurs, contrôleurs WLAN et pare-feu.
keywords: périphériques réseau, détection de vulnérabilité des périphériques réseau, systèmes d’exploitation de commutateurs, routeurs, contrôleurs WLAN et pare-feu
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: ellevin
author: levinec
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 86b8a37fd6b2d6f9906321b5d74de0e21c45fca3
ms.sourcegitcommit: d34cac68537d6e1c65be757956646e73dea6e1ab
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/22/2021
ms.locfileid: "53062141"
---
# <a name="network-device-discovery-and-vulnerability-management"></a><span data-ttu-id="2fe1a-104">Découverte et découverte de périphériques réseau gestion des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="2fe1a-104">Network device discovery and vulnerability management</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="2fe1a-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="2fe1a-105">**Applies to:**</span></span>

- [<span data-ttu-id="2fe1a-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="2fe1a-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="2fe1a-107">Menaces et gestion des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="2fe1a-107">Threat and vulnerability management</span></span>](next-gen-threat-and-vuln-mgt.md)
- [<span data-ttu-id="2fe1a-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="2fe1a-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="2fe1a-109">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="2fe1a-109">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="2fe1a-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-portaloverview-abovefoldlink)

> [!NOTE]  
> <span data-ttu-id="2fe1a-111">Le [](https://techcommunity.microsoft.com/t5/microsoft-defender-for-endpoint/network-device-discovery-and-vulnerability-assessments/ba-p/2267548) blog sur les évaluations de la vulnérabilité et de la découverte des périphériques réseau publié le \( 13/04/2021 fournit des informations sur les nouvelles fonctionnalités de découverte d’appareils réseau dans \) Defender pour endpoint. </span><span class="sxs-lookup"><span data-stu-id="2fe1a-111">The [Network device discovery and vulnerability assessments](https://techcommunity.microsoft.com/t5/microsoft-defender-for-endpoint/network-device-discovery-and-vulnerability-assessments/ba-p/2267548) Blog \(published 04-13-2021\) provides insights into the new **Network device discovery** capabilities in Defender for Endpoint.</span></span> <span data-ttu-id="2fe1a-112">Cet article fournit une vue  d’ensemble du défi que la découverte de périphériques réseau est conçue pour résoudre, ainsi que des informations détaillées sur la façon de commencer à utiliser ces nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-112">This article provides an overview of the challenge that **Network device discovery** is designed to address, and detailed information about how get started using these new capabilities.</span></span>

<span data-ttu-id="2fe1a-113">Les fonctionnalités de découverte de réseau sont disponibles dans la **section** Inventaire des appareils du centre de sécurité Microsoft 365 et des consoles Centre de sécurité Microsoft Defender réseau.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-113">Network discovery capabilities are available in the **Device inventory** section of the Microsoft 365 security center and Microsoft Defender Security Center consoles.</span></span>  

<span data-ttu-id="2fe1a-114">Un appareil Microsoft Defender for Endpoint désigné sera utilisé sur chaque segment réseau pour effectuer des analyses authentifiées périodiques des périphériques réseau préconfigurés.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-114">A designated Microsoft Defender for Endpoint device will be used on each network segment to perform periodic authenticated scans of preconfigured network devices.</span></span> <span data-ttu-id="2fe1a-115">Une fois découvertes, les fonctionnalités Gestion des menaces et des vulnérabilités de Defender for Endpoint fournissent des flux de travail intégrés pour sécuriser les commutateurs découverts, les routeurs, les contrôleurs WLAN, les pare-feu et les passerelles VPN.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-115">Once discovered, Defender for Endpoint’s threat and vulnerability management capabilities provide integrated workflows to secure discovered switches, routers, WLAN controllers, firewalls, and VPN gateways.</span></span>  

<span data-ttu-id="2fe1a-116">Une fois que les périphériques réseau ont été découverts et classés, les administrateurs de sécurité pourront recevoir les dernières recommandations de sécurité et passer en revue les vulnérabilités récemment découvertes sur les périphériques réseau déployés au sein de leur organisation.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-116">Once the network devices are discovered and classified, security administrators will be able to receive the latest security recommendations and review recently discovered vulnerabilities on network devices deployed across their organizations.</span></span>

## <a name="approach"></a><span data-ttu-id="2fe1a-117">Approche</span><span class="sxs-lookup"><span data-stu-id="2fe1a-117">Approach</span></span>

<span data-ttu-id="2fe1a-118">Les périphériques réseau ne sont pas gérés en tant que points de terminaison standard, car Defender pour point de terminaison ne comprend pas de capteur intégré aux périphériques réseau eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-118">Network devices are not managed as standard endpoints since Defender for Endpoint doesn’t have a sensor built into the network devices themselves.</span></span> <span data-ttu-id="2fe1a-119">Ces types d’appareils nécessitent une approche sans agent dans laquelle une analyse à distance obtient les informations nécessaires des appareils.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-119">These types of devices require an agentless approach where a remote scan will obtain the necessary information from the devices.</span></span> <span data-ttu-id="2fe1a-120">Selon la topologie et les caractéristiques du réseau, un ou plusieurs appareils intégrés à Microsoft Defender pour le point de terminaison effectueront des analyses authentifiées des périphériques réseau à l’aide de SNMP (lecture seule).</span><span class="sxs-lookup"><span data-stu-id="2fe1a-120">Depending on the network topology and characteristics, a single device or a few devices onboarded to Microsoft Defender for Endpoint will perform authenticated scans of network devices using SNMP (read-only).</span></span>

<span data-ttu-id="2fe1a-121">Il y aura deux types d’appareils à garder à l’esprit :</span><span class="sxs-lookup"><span data-stu-id="2fe1a-121">There will be two types of devices to keep in mind:</span></span>

- <span data-ttu-id="2fe1a-122">**Périphérique d’évaluation**: appareil déjà intégré que vous utiliserez pour analyser les périphériques réseau.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-122">**Assessment device**: A device that's already onboarded that you'll use to scan the network devices.</span></span>
- <span data-ttu-id="2fe1a-123">**Périphériques réseau**: périphériques réseau que vous prévoyez d’analyser et d’intégrer.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-123">**Network devices**: The network devices you plan to scan and onboard.</span></span>

### <a name="vulnerability-management-for-network-devices"></a><span data-ttu-id="2fe1a-124">Gestion des vulnérabilités pour les périphériques réseau</span><span class="sxs-lookup"><span data-stu-id="2fe1a-124">Vulnerability management for network devices</span></span> 

<span data-ttu-id="2fe1a-125">Une fois que les périphériques réseau ont été découverts et classés, les administrateurs de sécurité pourront recevoir les dernières recommandations de sécurité et passer en revue les vulnérabilités récemment découvertes sur les périphériques réseau déployés au sein de leur organisation.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-125">Once the network devices are discovered and classified, security administrators will be able to receive the latest security recommendations and review recently discovered vulnerabilities on network devices deployed across their organizations.</span></span>  

## <a name="operating-systems-that-are-supported"></a><span data-ttu-id="2fe1a-126">Systèmes d’exploitation pris en charge</span><span class="sxs-lookup"><span data-stu-id="2fe1a-126">Operating systems that are supported</span></span>

<span data-ttu-id="2fe1a-127">Les systèmes d’exploitation suivants sont actuellement pris en charge :</span><span class="sxs-lookup"><span data-stu-id="2fe1a-127">The following operating systems are currently supported:</span></span>

- <span data-ttu-id="2fe1a-128">Cisco IOS, IOS-XE, NX-OS</span><span class="sxs-lookup"><span data-stu-id="2fe1a-128">Cisco IOS, IOS-XE, NX-OS</span></span>
- <span data-ttu-id="2fe1a-129">Juniper JUNIPERS</span><span class="sxs-lookup"><span data-stu-id="2fe1a-129">Juniper JUNOS</span></span>
- <span data-ttu-id="2fe1a-130">HPE ArubaOS, Procurve Switch Software</span><span class="sxs-lookup"><span data-stu-id="2fe1a-130">HPE ArubaOS, Procurve Switch Software</span></span>
- <span data-ttu-id="2fe1a-131">Palo Alto Networks PAN-OS</span><span class="sxs-lookup"><span data-stu-id="2fe1a-131">Palo Alto Networks PAN-OS</span></span>

<span data-ttu-id="2fe1a-132">D’autres fournisseurs de réseaux et systèmes d’exploitation seront ajoutés au fil du temps, en fonction des données recueillies à partir de l’utilisation des clients.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-132">More networking vendors and OS will be added over time, based on data gathered from customer usage.</span></span> <span data-ttu-id="2fe1a-133">Par conséquent, vous êtes encouragé à configurer tous vos périphériques réseau, même s’ils ne sont pas spécifiés dans cette liste.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-133">Therefore, you are encouraged to configure all your network devices, even if they’re not specified in this list.</span></span>

## <a name="how-to-get-started"></a><span data-ttu-id="2fe1a-134">Prise en main</span><span class="sxs-lookup"><span data-stu-id="2fe1a-134">How to get started</span></span>

<span data-ttu-id="2fe1a-135">La première étape consiste à sélectionner un appareil qui effectuera les analyses réseau authentifiées.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-135">Your first step is to select a device that will perform the authenticated network scans.</span></span>

1. <span data-ttu-id="2fe1a-136">Décidez d’un appareil intégré Defender for Endpoint (client ou serveur) qui dispose d’une connexion réseau au port de gestion pour les périphériques réseau que vous prévoyez d’analyser.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-136">Decide on a Defender for Endpoint onboarded device (client or server) that has a network connection to the management port for the network devices you plan on scanning.</span></span> 

2. <span data-ttu-id="2fe1a-137">Le trafic SNMP entre le périphérique d’évaluation Defender for Endpoint et les périphériques réseau ciblés doit être autorisé (par exemple, par le pare-feu).</span><span class="sxs-lookup"><span data-stu-id="2fe1a-137">SNMP traffic between the Defender for Endpoint assessment device and the targeted network devices must be allowed (for example, by the Firewall).</span></span>

3. <span data-ttu-id="2fe1a-138">Déterminez les périphériques réseau à évaluer pour les vulnérabilités (par exemple, un commutateur Cisco ou un pare-feu Palo Alto Networks).</span><span class="sxs-lookup"><span data-stu-id="2fe1a-138">Decide which network devices will be assessed for vulnerabilities (for example: a Cisco switch or a Palo Alto Networks firewall).</span></span>  

4. <span data-ttu-id="2fe1a-139">Assurez-vous que le SNMP en lecture seule est activé sur tous les périphériques réseau configurés pour permettre au périphérique d’évaluation Defender for Endpoint d’interroger les périphériques réseau configurés.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-139">Make sure SNMP read-only is enabled on all configured network devices to allow the Defender for Endpoint assessment device to query the configured network devices.</span></span> <span data-ttu-id="2fe1a-140">« Écriture SNMP » n’est pas nécessaire pour la fonctionnalité appropriée de cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-140">‘SNMP write’ isn't needed for the proper functionality of this feature.</span></span>

5. <span data-ttu-id="2fe1a-141">Obtenez les adresses IP des périphériques réseau à scanner (ou les sous-réseaux où ces périphériques sont déployés).</span><span class="sxs-lookup"><span data-stu-id="2fe1a-141">Obtain the IP addresses of the network devices to be scanned (or the subnets where these devices are deployed).</span></span>

6. <span data-ttu-id="2fe1a-142">Obtenez les informations d’identification SNMP des périphériques réseau (par exemple : Community String, noAuthNoPriv, authNoPriv, authPriv).</span><span class="sxs-lookup"><span data-stu-id="2fe1a-142">Obtain the SNMP credentials of the network devices (for example: Community String, noAuthNoPriv, authNoPriv, authPriv).</span></span> <span data-ttu-id="2fe1a-143">Vous devez fournir les informations d’identification lors de la configuration d’un nouveau travail d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-143">You’ll be required to provide the credentials when configuring a new assessment job.</span></span>  

7. <span data-ttu-id="2fe1a-144">Configuration du client proxy : aucune configuration supplémentaire n’est requise autre que la configuration requise pour le proxy d’appareil Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-144">Proxy client configuration: No extra configuration is required other than the Defender for Endpoint device proxy requirements.</span></span>

8. <span data-ttu-id="2fe1a-145">Pour permettre à l’analyseur réseau d’être authentifié et de fonctionner correctement, il est essentiel d’ajouter les domaines/URL suivants :</span><span class="sxs-lookup"><span data-stu-id="2fe1a-145">To allow the network scanner to be authenticated and work properly, it's essential that you add the following domains/URLs:</span></span>

    - <span data-ttu-id="2fe1a-146">login.windows.net</span><span class="sxs-lookup"><span data-stu-id="2fe1a-146">login.windows.net</span></span>  
    - <span data-ttu-id="2fe1a-147">\*.securitycenter.windows.com</span><span class="sxs-lookup"><span data-stu-id="2fe1a-147">\*.securitycenter.windows.com</span></span>
    - <span data-ttu-id="2fe1a-148">login.microsoftonline.com</span><span class="sxs-lookup"><span data-stu-id="2fe1a-148">login.microsoftonline.com</span></span>
    - <span data-ttu-id="2fe1a-149">\*.blob.core.windows.net/networkscannerstable/ \*</span><span class="sxs-lookup"><span data-stu-id="2fe1a-149">\*.blob.core.windows.net/networkscannerstable/ \*</span></span>

    > [!NOTE]
    > <span data-ttu-id="2fe1a-150">Toutes les URL ne sont pas spécifiées dans la liste de collecte de données autorisées de Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-150">Not all URLs are specified in the Defender for Endpoint documented list of allowed data collection.</span></span>

## <a name="permissions"></a><span data-ttu-id="2fe1a-151">Autorisations</span><span class="sxs-lookup"><span data-stu-id="2fe1a-151">Permissions</span></span>

<span data-ttu-id="2fe1a-152">Pour configurer les travaux d’évaluation, l’option d’autorisation utilisateur suivante est requise : Gérer les **paramètres de sécurité dans le Centre de sécurité.**</span><span class="sxs-lookup"><span data-stu-id="2fe1a-152">To configure assessment jobs, the following user permission option is required: **Manage security settings in Security Center**.</span></span> <span data-ttu-id="2fe1a-153">Vous pouvez trouver l’autorisation en allant à **Paramètres**  >  **rôles**.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-153">You can find the permission by going to **Settings** > **Roles**.</span></span> <span data-ttu-id="2fe1a-154">Pour plus d’informations, voir Créer et gérer des rôles pour le contrôle [d’accès basé sur les rôles.](user-roles.md)</span><span class="sxs-lookup"><span data-stu-id="2fe1a-154">For more information, see [Create and manage roles for role-based access control](user-roles.md).</span></span>

## <a name="install-the-network-scanner"></a><span data-ttu-id="2fe1a-155">Installer le scanneur réseau</span><span class="sxs-lookup"><span data-stu-id="2fe1a-155">Install the network scanner</span></span>

1. <span data-ttu-id="2fe1a-156">Go to **Microsoft 365 security**  >  **Paramètres**  >  **Endpoints**  >  **Assessment jobs** (under Network **assessments**).</span><span class="sxs-lookup"><span data-stu-id="2fe1a-156">Go to **Microsoft 365 security** > **Settings** > **Endpoints** > **Assessment jobs** (under **Network assessments**).</span></span>
    1. <span data-ttu-id="2fe1a-157">Dans la Centre de sécurité Microsoft Defender, allez à la page Paramètres > travaux d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-157">In the Microsoft Defender Security Center, go to Settings > Assessment jobs page.</span></span>

2. <span data-ttu-id="2fe1a-158">Téléchargez le scanneur réseau et installez-le sur le périphérique d’évaluation Defender for Endpoint désigné.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-158">Download the network scanner and install it on the designated Defender for Endpoint assessment device.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="2fe1a-159">![Bouton Télécharger le scanneur](images/assessment-jobs-download-scanner.png)</span><span class="sxs-lookup"><span data-stu-id="2fe1a-159">![Download scanner button](images/assessment-jobs-download-scanner.png)</span></span>

## <a name="network-scanner-installation--registration"></a><span data-ttu-id="2fe1a-160">Inscription de l’installation du scanneur & réseau</span><span class="sxs-lookup"><span data-stu-id="2fe1a-160">Network scanner installation & registration</span></span>

<span data-ttu-id="2fe1a-161">Le processus de signature peut être effectué sur l’appareil d’évaluation désigné lui-même ou sur tout autre appareil (par exemple, votre appareil client personnel).</span><span class="sxs-lookup"><span data-stu-id="2fe1a-161">The signing-in process can be completed on the designated assessment device itself or any other device (for example, your personal client device).</span></span>

<span data-ttu-id="2fe1a-162">Pour terminer le processus d’inscription du scanneur réseau :</span><span class="sxs-lookup"><span data-stu-id="2fe1a-162">To complete the network scanner registration process:</span></span>

1. <span data-ttu-id="2fe1a-163">Copiez et suivez l’URL qui apparaît sur la ligne de commande et utilisez le code d’installation fourni pour terminer le processus d’inscription.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-163">Copy and follow the URL that appears on the command line and use the provided installation code to complete the registration process.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2fe1a-164">Vous devrez peut-être modifier les paramètres d’invite de commandes pour pouvoir copier l’URL.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-164">You may need to change Command Prompt settings to be able to copy the URL.</span></span>

2. <span data-ttu-id="2fe1a-165">Entrez le code et connectez-vous à l’aide d’un compte Microsoft qui dispose de l’autorisation Defender pour le point de terminaison appelée « Gérer les paramètres de sécurité dans le Centre de sécurité ».</span><span class="sxs-lookup"><span data-stu-id="2fe1a-165">Enter the code and sign in using a Microsoft account that has the Defender for Endpoint permission called "Manage security settings in Security Center."</span></span>

3. <span data-ttu-id="2fe1a-166">Lorsque vous avez terminé, vous devez voir un message vous confirmant que vous êtes bien inscrit.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-166">When finished, you should see a message confirming you have signed in.</span></span>

## <a name="configure-a-new-assessment-job"></a><span data-ttu-id="2fe1a-167">Configurer un nouveau travail d’évaluation</span><span class="sxs-lookup"><span data-stu-id="2fe1a-167">Configure a new assessment job</span></span>  

<span data-ttu-id="2fe1a-168">Dans la page Travaux d’évaluation **Paramètres**, **sélectionnez Ajouter un travail d’évaluation réseau.**</span><span class="sxs-lookup"><span data-stu-id="2fe1a-168">In the Assessment jobs page in **Settings**, select **Add network assessment job**.</span></span> <span data-ttu-id="2fe1a-169">Suivez le processus de mise en place pour choisir les périphériques réseau à scanner régulièrement et ajoutés à l’inventaire des appareils.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-169">Follow the set-up process to choose network devices to be scanned regularly and added to the device inventory.</span></span>

<span data-ttu-id="2fe1a-170">Pour éviter la duplication des appareils dans l’inventaire des périphériques réseau, assurez-vous que chaque adresse IP n’est configurée qu’une seule fois sur plusieurs périphériques d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-170">To prevent device duplication in the network device inventory, make sure each IP address is configured only once across multiple assessment devices.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="2fe1a-171">![Bouton Ajouter un travail d’évaluation réseau](images/assessment-jobs-add.png)</span><span class="sxs-lookup"><span data-stu-id="2fe1a-171">![Add network assessment job button](images/assessment-jobs-add.png)</span></span>

<span data-ttu-id="2fe1a-172">Ajout des étapes d’un travail d’évaluation réseau :</span><span class="sxs-lookup"><span data-stu-id="2fe1a-172">Adding a network assessment job steps:</span></span>

1. <span data-ttu-id="2fe1a-173">Choisissez un nom de « travail d’évaluation » et le « périphérique d’évaluation » sur lequel le scanneur réseau a été installé.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-173">Choose an ‘Assessment job’ name and the ‘Assessment device’ on which the network scanner was installed.</span></span> <span data-ttu-id="2fe1a-174">Cet appareil effectue les analyses authentifiées périodiques.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-174">This device will perform the periodic authenticated scans.</span></span>

2. <span data-ttu-id="2fe1a-175">Ajoutez les adresses IP des périphériques réseau cibles à scanner (ou les sous-réseaux où ces périphériques sont déployés).</span><span class="sxs-lookup"><span data-stu-id="2fe1a-175">Add IP addresses of target network devices to be scanned (or the subnets where these devices are deployed).</span></span> 

3. <span data-ttu-id="2fe1a-176">Ajoutez les informations d’identification SNMP requises des périphériques réseau cibles.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-176">Add required SNMP credentials of the target network devices.</span></span> 

4. <span data-ttu-id="2fe1a-177">Enregistrez le travail d’évaluation réseau nouvellement configuré pour démarrer l’analyse réseau périodique.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-177">Save the newly configured network assessment job to start the periodic network scan.</span></span> 

### <a name="scan-and-add-network-devices"></a><span data-ttu-id="2fe1a-178">Analyser et ajouter des périphériques réseau</span><span class="sxs-lookup"><span data-stu-id="2fe1a-178">Scan and add network devices</span></span>

<span data-ttu-id="2fe1a-179">Pendant le processus de mise en place, vous pouvez effectuer une analyse de test à une seule fois pour vérifier que :</span><span class="sxs-lookup"><span data-stu-id="2fe1a-179">During the set-up process, you can perform a one time test scan to verify that:</span></span>

- <span data-ttu-id="2fe1a-180">Il existe une connectivité entre le périphérique d’évaluation Defender for Endpoint et les périphériques réseau cibles configurés.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-180">There is connectivity between the Defender for Endpoint assessment device and the configured target network devices.</span></span>
- <span data-ttu-id="2fe1a-181">Les informations d’identification SNMP configurées sont correctes.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-181">The configured SNMP credentials are correct.</span></span>

<span data-ttu-id="2fe1a-182">Chaque périphérique d’évaluation peut prendre en charge jusqu’à 1 500 adresses IP réussies.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-182">Each assessment device can support up to 1,500 successful IP addresses scan.</span></span> <span data-ttu-id="2fe1a-183">Par exemple, si vous analysez 10 sous-réseaux différents où seules 100 adresses IP retournent des résultats positifs, vous pourrez analyser 1 400 adresses IP supplémentaires à partir d’autres sous-réseaux sur le même périphérique d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-183">For example, if you scan 10 different subnets where only 100 IP addresses return successful results, you will be able to scan 1,400 IP additional addresses from other subnets on the same assessment device.</span></span>  

<span data-ttu-id="2fe1a-184">S’il existe plusieurs plages d’adresses IP/sous-réseaux à analyser, les résultats de l’analyse de test prennent plusieurs minutes pour s’afficher.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-184">If there are multiple IP address ranges/subnets to scan, the test scan results will take several minutes to show up.</span></span> <span data-ttu-id="2fe1a-185">Une analyse de test sera disponible pour 1 024 adresses au plus.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-185">A test scan will be available for up to 1,024 addresses.</span></span>

<span data-ttu-id="2fe1a-186">Une fois les résultats obtenus, vous pouvez choisir les appareils qui seront inclus dans l’analyse périodique.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-186">Once the results show up, you can choose which devices will be included in the periodic scan.</span></span> <span data-ttu-id="2fe1a-187">Si vous ignorez l’affichage des résultats de l’analyse, toutes les adresses IP configurées sont ajoutées au travail d’évaluation réseau (quelle que soit la réponse de l’appareil).</span><span class="sxs-lookup"><span data-stu-id="2fe1a-187">If you skip viewing the scan results, all configured IP addresses will be added to the network assessment job (regardless of the device’s response).</span></span> <span data-ttu-id="2fe1a-188">Les résultats de l’analyse peuvent également être exportés.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-188">The scan results can also be exported.</span></span>

## <a name="device-inventory"></a><span data-ttu-id="2fe1a-189">Inventaire des appareils</span><span class="sxs-lookup"><span data-stu-id="2fe1a-189">Device inventory</span></span>

<span data-ttu-id="2fe1a-190">Les appareils nouvellement découverts s’afficheront sous le nouvel onglet **Périphériques** réseau dans la page **Inventaire des** appareils.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-190">Newly discovered devices will be shown under the new **Network devices** tab in the **Device inventory** page.</span></span> <span data-ttu-id="2fe1a-191">L’ajout d’un travail d’évaluation peut prendre jusqu’à deux heures jusqu’à ce que les appareils soient mis à jour.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-191">It may take up to two hours after adding an assessment job until the devices are updated.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="2fe1a-192">![Section Périphériques réseau dans l’inventaire des appareils](images/assessment-jobs-device-inventory.png)</span><span class="sxs-lookup"><span data-stu-id="2fe1a-192">![Network devices section in the Device inventory](images/assessment-jobs-device-inventory.png)</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="2fe1a-193">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="2fe1a-193">Troubleshooting</span></span>

### <a name="network-scanner-installation-has-failed"></a><span data-ttu-id="2fe1a-194">Échec de l’installation du scanneur réseau</span><span class="sxs-lookup"><span data-stu-id="2fe1a-194">Network scanner installation has failed</span></span>

<span data-ttu-id="2fe1a-195">Vérifiez que les URL requises sont ajoutées aux domaines autorisés dans vos paramètres de pare-feu.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-195">Verify that the required URLs are added to the allowed domains in your firewall settings.</span></span> <span data-ttu-id="2fe1a-196">Assurez-vous également que les paramètres de proxy sont configurés comme décrit dans Configurer les [paramètres de proxy](configure-proxy-internet.md)d’appareil et de connectivité Internet.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-196">Also, make sure proxy settings are configured as described in [Configure device proxy and Internet connectivity settings](configure-proxy-internet.md).</span></span>

### <a name="the-microsoftcomdevicelogin-web-page-did-not-show-up"></a><span data-ttu-id="2fe1a-197">La page Microsoft.com/devicelogin web de l’application n’a pas été</span><span class="sxs-lookup"><span data-stu-id="2fe1a-197">The Microsoft.com/devicelogin web page did not show up</span></span>

<span data-ttu-id="2fe1a-198">Vérifiez que les URL requises sont ajoutées aux domaines autorisés dans votre pare-feu.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-198">Verify that the required URLs are added to the allowed domains in your firewall.</span></span> <span data-ttu-id="2fe1a-199">Assurez-vous également que les paramètres de proxy sont configurés comme décrit dans Configurer les [paramètres de proxy](configure-proxy-internet.md)d’appareil et de connectivité Internet.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-199">Also, make sure proxy settings are configured as described in [Configure device proxy and Internet connectivity settings](configure-proxy-internet.md).</span></span>

### <a name="network-devices-are-not-shown-in-the-device-inventory-after-several-hours"></a><span data-ttu-id="2fe1a-200">Les périphériques réseau ne sont pas affichés dans l’inventaire des appareils après plusieurs heures</span><span class="sxs-lookup"><span data-stu-id="2fe1a-200">Network devices are not shown in the device inventory after several hours</span></span>

<span data-ttu-id="2fe1a-201">Les résultats de l’analyse doivent être mis à jour quelques heures après l’analyse initiale qui a eu lieu après la fin de la configuration du travail d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-201">The scan results should be updated a few hours after the initial scan that took place after completing the assessment job configuration.</span></span>

<span data-ttu-id="2fe1a-202">Si les appareils ne sont toujours pas affichés, vérifiez que le service « MdatpNetworkScanService » est en cours d’exécution sur vos appareils d’évaluation, sur lesquels vous avez installé le scanneur réseau, et effectuez une « analyse d’exécution » dans la configuration du travail d’évaluation approprié.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-202">If devices are still not shown, verify that the service ‘MdatpNetworkScanService’ is running on your assessment devices, on which you installed the network scanner, and perform a “Run scan” in the relevant assessment job configuration.</span></span>  

<span data-ttu-id="2fe1a-203">Si vous n’obtenez toujours pas de résultats après 5 minutes, redémarrez le service.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-203">If you still don’t get results after 5 minutes, restart the service.</span></span>  

### <a name="devices-last-seen-time-is-longer-than-24-hours"></a><span data-ttu-id="2fe1a-204">La durée de la dernière vue des appareils est de plus de 24 heures</span><span class="sxs-lookup"><span data-stu-id="2fe1a-204">Devices last seen time is longer than 24 hours</span></span>

<span data-ttu-id="2fe1a-205">Vérifier que le scanneur s’exécute correctement.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-205">Validate that the scanner is running properly.</span></span> <span data-ttu-id="2fe1a-206">Ensuite, allez à la définition d’analyse et sélectionnez « Exécuter le test ».</span><span class="sxs-lookup"><span data-stu-id="2fe1a-206">Then go to the scan definition and select “Run test.”</span></span> <span data-ttu-id="2fe1a-207">Vérifiez quels messages d’erreur sont retournés à partir des adresses IP pertinentes.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-207">Check what error messages are returning from the relevant IP addresses.</span></span>

### <a name="required-threat-and-vulnerability-management-user-permission"></a><span data-ttu-id="2fe1a-208">Autorisation utilisateur Gestion des menaces et des vulnérabilités requise</span><span class="sxs-lookup"><span data-stu-id="2fe1a-208">Required threat and vulnerability management user permission</span></span>

<span data-ttu-id="2fe1a-209">L’inscription s’est terminée par une erreur : « Il semble que vous n’avez pas les autorisations suffisantes pour ajouter un nouvel agent.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-209">Registration finished with an error: "It looks like you don't have sufficient permissions for adding a new agent.</span></span> <span data-ttu-id="2fe1a-210">L’autorisation requise est « Gérer les paramètres de sécurité dans le Centre de sécurité ». »</span><span class="sxs-lookup"><span data-stu-id="2fe1a-210">The required permission is 'Manage security settings in Security Center'."</span></span>

<span data-ttu-id="2fe1a-211">Appuyez sur n’importe quelle touche pour quitter.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-211">Press any key to exit.</span></span>

<span data-ttu-id="2fe1a-212">Demandez à votre administrateur système de vous attribuer les autorisations requises.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-212">Ask your system administrator to assign you the required permissions.</span></span> <span data-ttu-id="2fe1a-213">Vous pouvez également demander à un autre membre approprié de vous aider dans le processus de connexion en lui fournissant le code de connexion et le lien.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-213">Alternately, ask another relevant member to help you with the sign-in process by providing them with the sign-in code and link.</span></span>

### <a name="registration-process-fails-using-provided-link-in-the-command-line-in-registration-process"></a><span data-ttu-id="2fe1a-214">Échec du processus d’inscription à l’aide du lien fourni dans la ligne de commande du processus d’inscription</span><span class="sxs-lookup"><span data-stu-id="2fe1a-214">Registration process fails using provided link in the command line in registration process</span></span>

<span data-ttu-id="2fe1a-215">Essayez un autre navigateur ou copiez le lien de connexion et le code sur un autre appareil.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-215">Try a different browser or copy the sign-in link and code to a different device.</span></span>

### <a name="text-too-small-or-cant-copy-text-from-command-line"></a><span data-ttu-id="2fe1a-216">Texte trop petit ou ne peut pas copier le texte à partir d’une ligne de commande</span><span class="sxs-lookup"><span data-stu-id="2fe1a-216">Text too small or can’t copy text from command line</span></span>

<span data-ttu-id="2fe1a-217">Modifiez les paramètres de ligne de commande sur votre appareil pour autoriser la copie et modifier la taille du texte.</span><span class="sxs-lookup"><span data-stu-id="2fe1a-217">Change command-line settings on your device to allow copying and change text size.</span></span>

## <a name="related-articles"></a><span data-ttu-id="2fe1a-218">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="2fe1a-218">Related articles</span></span>

- [<span data-ttu-id="2fe1a-219">Inventaire des appareils</span><span class="sxs-lookup"><span data-stu-id="2fe1a-219">Device inventory</span></span>](machines-view-overview.md)
- [<span data-ttu-id="2fe1a-220">Configurer des fonctionnalités avancées</span><span class="sxs-lookup"><span data-stu-id="2fe1a-220">Configure advanced features</span></span>](advanced-features.md)
