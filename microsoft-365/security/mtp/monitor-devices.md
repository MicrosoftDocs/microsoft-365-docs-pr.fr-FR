---
title: Rapports d'& de surveillance des appareils - Centre de sécurité
description: Décrit comment sécuriser, mettre à jour et repérer les menaces potentielles dans votre organisation
keywords: sécurité, programmes malveillants, Microsoft 365, M365, centre de sécurité, surveiller, signaler, appareils
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.localizationpriority: medium
f1.keywords:
- NOCSH
ms.author: ellevin
author: levinec
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
search.appverid: met150
ms.custom: seo-marvel-apr2020
ms.technology: m365d
ms.openlocfilehash: b9580f904f9cc5043fa3e825007339ce66daaa72
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49930497"
---
# <a name="device-monitoring-and-reporting-in-the-microsoft-365-security-center"></a><span data-ttu-id="767cc-104">Surveillance des appareils et rapports dans le Centre de sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="767cc-104">Device monitoring and reporting in the Microsoft 365 security center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="767cc-105">Maintenez vos appareils sécurisés, à jour et repérer les menaces potentielles dans le Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="767cc-105">Keep your devices secure, up-to-date, and spot potential threats in the Microsoft 365 security center.</span></span>

## <a name="view-device-alerts"></a><span data-ttu-id="767cc-106">Afficher les alertes de périphérique</span><span class="sxs-lookup"><span data-stu-id="767cc-106">View device alerts</span></span>

<span data-ttu-id="767cc-107">Recevez des alertes à jour concernant l’activité de violation et d’autres menaces sur vos appareils à partir de Microsoft Defender for Endpoint (disponible avec une licence E5).</span><span class="sxs-lookup"><span data-stu-id="767cc-107">Get up-to-date alerts about breach activity and other threats on your devices from Microsoft Defender for Endpoint (available with an E5 license).</span></span> <span data-ttu-id="767cc-108">Le Centre de sécurité Microsoft 365 surveille efficacement ces alertes à un niveau élevé à l’aide de votre flux de travail préféré.</span><span class="sxs-lookup"><span data-stu-id="767cc-108">Microsoft 365 security center effectively monitors these alerts at a high level using your preferred workflow.</span></span>

### <a name="monitor-high-impact-alerts"></a><span data-ttu-id="767cc-109">Surveiller les alertes à fort impact</span><span class="sxs-lookup"><span data-stu-id="767cc-109">Monitor high-impact alerts</span></span>

<span data-ttu-id="767cc-110">Chaque alerte Microsoft Defender pour point de terminaison a une gravité correspondante (élevée, moyenne, faible ou informationnelle).</span><span class="sxs-lookup"><span data-stu-id="767cc-110">Each Microsoft Defender for Endpoint alert has a corresponding severity (high, medium, low, or informational).</span></span> <span data-ttu-id="767cc-111">Il indique l’impact potentiel sur votre réseau s’il est laissé sans surveillance.</span><span class="sxs-lookup"><span data-stu-id="767cc-111">It indicates potential impact to your network if left unattended.</span></span>  

<span data-ttu-id="767cc-112">Utilisez la carte **de gravité des** alertes d’appareil pour vous concentrer spécifiquement sur les alertes plus graves et qui peuvent nécessiter une réponse immédiate.</span><span class="sxs-lookup"><span data-stu-id="767cc-112">Use the **Device alert severity** card to focus specifically on alerts that are more severe and might require immediate response.</span></span> <span data-ttu-id="767cc-113">À partir de cette carte, vous pouvez afficher plus d’informations sur le portail centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="767cc-113">From this card, you can view more information on the Microsoft Defender Security Center portal.</span></span>

![Carte de gravité des alertes d’appareil](../../media/device-alerts-severity.png)

### <a name="understand-sources-of-alerts"></a><span data-ttu-id="767cc-115">Comprendre les sources d’alertes</span><span class="sxs-lookup"><span data-stu-id="767cc-115">Understand sources of alerts</span></span>

<span data-ttu-id="767cc-116">Microsoft Defender pour le point de terminaison exploite les données d’un large éventail de capteurs de sécurité et de sources d’intelligence pour générer des alertes.</span><span class="sxs-lookup"><span data-stu-id="767cc-116">Microsoft Defender for Endpoint leverages data from a broad range of security sensors and intelligence sources to generate alerts.</span></span> <span data-ttu-id="767cc-117">Par exemple, il peut utiliser les informations de détection de l’Antivirus Microsoft Defender et des logiciels anti-programme malveillant tiers.</span><span class="sxs-lookup"><span data-stu-id="767cc-117">For example, it can use detection information from Microsoft Defender Antivirus and third-party antimalware.</span></span> <span data-ttu-id="767cc-118">Il peut également utiliser votre propre intelligence contre les menaces personnalisée fournie par le biais de l’API de service web.</span><span class="sxs-lookup"><span data-stu-id="767cc-118">It can also use your own custom threat intelligence provided through the web service API.</span></span>

<span data-ttu-id="767cc-119">La carte **sources de détection des alertes** d’appareil affiche la distribution des alertes par source.</span><span class="sxs-lookup"><span data-stu-id="767cc-119">The **Device alert detection** sources card shows the distribution of alerts by source.</span></span> <span data-ttu-id="767cc-120">Suivre l’activité liée à certaines sources, en particulier vos sources personnalisées.</span><span class="sxs-lookup"><span data-stu-id="767cc-120">Track activity related to certain sources, particularly your custom sources.</span></span> <span data-ttu-id="767cc-121">Vous pouvez également utiliser la carte pour vous concentrer sur les alertes provenant de capteurs qui ne sont pas configurés pour bloquer automatiquement les activités ou composants malveillants.</span><span class="sxs-lookup"><span data-stu-id="767cc-121">You can also use the card to focus on alerts coming from sensors that aren't configured to automatically block malicious activity or components.</span></span>

![Carte sources de détection des alertes d’appareil](../../media/device-alert-detection-sources.png)

<span data-ttu-id="767cc-123">À partir de cette carte, vous pouvez afficher plus d’informations sur le portail centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="767cc-123">From this card, you can view more information on the Microsoft Defender Security Center portal.</span></span>

### <a name="understand-the-types-of-threats-that-trigger-alerts"></a><span data-ttu-id="767cc-124">Comprendre les types de menaces qui déclenchent des alertes</span><span class="sxs-lookup"><span data-stu-id="767cc-124">Understand the types of threats that trigger alerts</span></span>

<span data-ttu-id="767cc-125">Microsoft Defender pour le point de terminaison trie chaque alerte dans une catégorie représentant une étape particulière de la chaîne d’attaque ou du type de composant de menace.</span><span class="sxs-lookup"><span data-stu-id="767cc-125">Microsoft Defender for Endpoint sorts each alert into a category representing a certain stage in the attack chain or type of threat component.</span></span> <span data-ttu-id="767cc-126">Par exemple, une activité de menace détectée peut être classée comme « mouvement latéral » pour indiquer qu’il y a eu une tentative d’atteindre d’autres appareils sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="767cc-126">For example, a detected threat activity might be categorized as "lateral movement" to indicate there was an attempt to reach other devices on the network.</span></span> <span data-ttu-id="767cc-127">L’activité s’est probablement produite après que les attaquants ont pris une première place.</span><span class="sxs-lookup"><span data-stu-id="767cc-127">The activity has likely occurred after attackers gained an initial foothold.</span></span> <span data-ttu-id="767cc-128">Lorsqu’il est détecté, un composant de menace peut être considéré à grande étendue comme programme malveillant ou spécifiquement comme un type de menace spécifique.</span><span class="sxs-lookup"><span data-stu-id="767cc-128">When detected, a threat component might be classified broadly as malware or specifically as a specific threat type.</span></span> <span data-ttu-id="767cc-129">Les détails incluent les ransomware, le vol d’informations d’identification ou d’autres types de logiciels malveillants ou indésirables.</span><span class="sxs-lookup"><span data-stu-id="767cc-129">Specifics include ransomware, credential stealing, or other types of malicious or unwanted software.</span></span>

<span data-ttu-id="767cc-130">La **carte catégories de menaces d’appareil** affiche la distribution des alertes dans ces catégories.</span><span class="sxs-lookup"><span data-stu-id="767cc-130">The **Device threat categories** card shows the distribution of alerts into these categories.</span></span> <span data-ttu-id="767cc-131">Utilisez ces informations pour identifier l’activité des menaces, telles que les tentatives de vol d’informations d’identification, qui ont généralement un impact plus élevé que les tentatives d’ingénierie sociale.</span><span class="sxs-lookup"><span data-stu-id="767cc-131">Use this information to identify threat activity, such as credential theft attempts, that usually have higher impact than social engineering attempts.</span></span> <span data-ttu-id="767cc-132">Vous pouvez également surveiller les menaces potentiellement destructrices telles que les ransomware.</span><span class="sxs-lookup"><span data-stu-id="767cc-132">You can also to monitor for potentially destructive threats like ransomware.</span></span>

![Carte catégories de menaces d’appareil](../../media/device-threat-categories.png)

### <a name="monitor-active-alerts"></a><span data-ttu-id="767cc-134">Surveiller les alertes actives</span><span class="sxs-lookup"><span data-stu-id="767cc-134">Monitor active alerts</span></span>

<span data-ttu-id="767cc-135">La **carte d’état d’alerte** d’appareil indique le nombre d’alertes qui n’ont pas été résolues et qui peuvent nécessiter une attention particulière.</span><span class="sxs-lookup"><span data-stu-id="767cc-135">The **Device alert status** card indicates the number of alerts that haven't been resolved and may require attention.</span></span> <span data-ttu-id="767cc-136">À partir de cette carte, vous pouvez afficher plus d’informations sur le portail centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="767cc-136">From this card, you can view more information on the Microsoft Defender Security Center portal.</span></span>

![Carte d’état d’alerte d’appareil](../../media/device-alert-status.png)

### <a name="monitor-classification-of-resolved-alerts"></a><span data-ttu-id="767cc-138">Surveiller la classification des alertes résolues</span><span class="sxs-lookup"><span data-stu-id="767cc-138">Monitor classification of resolved alerts</span></span>

<span data-ttu-id="767cc-139">Lors de la résolution d’une alerte Microsoft Defender pour point de terminaison, votre personnel de sécurité peut spécifier si une alerte a été vérifiée comme :</span><span class="sxs-lookup"><span data-stu-id="767cc-139">When resolving a Microsoft Defender for Endpoint alert, your security staff can specify whether an alert has been verified as:</span></span>

* <span data-ttu-id="767cc-140">Une alerte réelle qui identifie l’activité de violation réelle ou les composants de menace</span><span class="sxs-lookup"><span data-stu-id="767cc-140">A true alert that identifies actual breach activity or threat components</span></span>
* <span data-ttu-id="767cc-141">Une fausse alerte qui a détecté de manière incorrecte l’activité normale</span><span class="sxs-lookup"><span data-stu-id="767cc-141">A false alert that has incorrectly detected normal activity</span></span>

<span data-ttu-id="767cc-142">La **carte de classification des alertes** d’appareil indique si vos alertes résolues ont été classées en tant qu’alertes vraies ou fausses.</span><span class="sxs-lookup"><span data-stu-id="767cc-142">The **Device alert classification** card shows whether your resolved alerts have been classified as true or false alerts.</span></span> <span data-ttu-id="767cc-143">À partir de cette carte, vous pouvez afficher plus d’informations sur le portail centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="767cc-143">From this card, you can view more information on the Microsoft Defender Security Center portal.</span></span>

<span data-ttu-id="767cc-144">Remarque : dans certains cas, les informations de classification ne sont pas disponibles pour certaines alertes.</span><span class="sxs-lookup"><span data-stu-id="767cc-144">Note: In some cases, classification information is unavailable for certain alerts.</span></span>

![Carte de classification des alertes d’appareil](../../media/device-alert-classification.png)

### <a name="monitor-determination-of-resolved-alerts"></a><span data-ttu-id="767cc-146">Surveiller la détermination des alertes résolues</span><span class="sxs-lookup"><span data-stu-id="767cc-146">Monitor determination of resolved alerts</span></span>

<span data-ttu-id="767cc-147">En plus de classer si une alerte est vraie ou false lors de la résolution, votre personnel de sécurité peut fournir une détermination.</span><span class="sxs-lookup"><span data-stu-id="767cc-147">Along with classifying whether an alert is true or false during resolution, your security staff can provide a determination.</span></span> <span data-ttu-id="767cc-148">Une détermination indique le type d’activité normale ou malveillante qui a été trouvé lors de la validation de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="767cc-148">A determination indicates the type of normal or malicious activity that was found while validating the alert.</span></span>

<span data-ttu-id="767cc-149">La **carte de détermination de l’alerte** d’appareil indique la détermination fournie pour chaque alerte.</span><span class="sxs-lookup"><span data-stu-id="767cc-149">The **Device alert determination** card shows the determination provided for each alert.</span></span>

* <span data-ttu-id="767cc-150">**APT**: menace persistante avancée, indiquant que l’activité détectée ou le composant de menace fait partie d’une violation sophistiquée conçue pour prendre pied dans le réseau concerné</span><span class="sxs-lookup"><span data-stu-id="767cc-150">**APT**: advanced persistent threat, indicating that the detected activity or threat component is part of a sophisticated breach designed to gain a foothold in the affected network</span></span>  
* <span data-ttu-id="767cc-151">**Programmes malveillants**: fichier ou code malveillant</span><span class="sxs-lookup"><span data-stu-id="767cc-151">**Malware**: malicious file or code</span></span>
* <span data-ttu-id="767cc-152">**Personnel de sécurité :** activité normale effectuée par le personnel de sécurité</span><span class="sxs-lookup"><span data-stu-id="767cc-152">**Security personnel**: normal activity performed by security staff</span></span>
* <span data-ttu-id="767cc-153">**Test de sécurité**: activité ou composants conçus pour simuler des menaces réelles et qui doivent déclencher des capteurs de sécurité et générer des alertes</span><span class="sxs-lookup"><span data-stu-id="767cc-153">**Security testing**: activity or components designed to simulate actual threats and expected to trigger security sensors and generate alerts</span></span>
* <span data-ttu-id="767cc-154">**Logiciels indésirables**: applications et autres logiciels qui ne sont pas considérés comme malveillants, mais qui ne respectent pas la politique ou les normes d’utilisation acceptables</span><span class="sxs-lookup"><span data-stu-id="767cc-154">**Unwanted software**: apps and other software that are not considered malicious, but otherwise violate policy or acceptable use standards</span></span>
* <span data-ttu-id="767cc-155">**Autres**: toute autre détermination qui ne relève pas des types fournis</span><span class="sxs-lookup"><span data-stu-id="767cc-155">**Others**: any other determination that doesn't fall under the provided types</span></span>

<span data-ttu-id="767cc-156">À partir de cette carte, vous pouvez afficher plus d’informations dans le Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="767cc-156">From this card, you can view more information in Microsoft Defender Security Center.</span></span>

![Carte de détermination des alertes d’appareil](../../media/device-alert-determination.png)

### <a name="understand-which-devices-are-at-risk"></a><span data-ttu-id="767cc-158">Comprendre les appareils à risque</span><span class="sxs-lookup"><span data-stu-id="767cc-158">Understand which devices are at risk</span></span>

<span data-ttu-id="767cc-159">**La protection des** appareils indique le niveau de risque pour les appareils.</span><span class="sxs-lookup"><span data-stu-id="767cc-159">**Device protection** shows the risk level for devices.</span></span> <span data-ttu-id="767cc-160">Le niveau de risque est basé sur des facteurs tels que le type et la gravité des alertes sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="767cc-160">The risk level is based on factors such as the type and severity of alerts on the device.</span></span>

![Carte de protection de l’appareil](../../media/device-protection.png)

## <a name="monitor-and-report-status-of-intune-managed-devices"></a><span data-ttu-id="767cc-162">Surveiller et signaler l’état des appareils gérés par Intune</span><span class="sxs-lookup"><span data-stu-id="767cc-162">Monitor and report status of Intune-managed devices</span></span>

<span data-ttu-id="767cc-163">Les rapports suivants contiennent des données provenant d’appareils inscrits dans Intune.</span><span class="sxs-lookup"><span data-stu-id="767cc-163">The following reports contain data from devices enrolled in Intune.</span></span> <span data-ttu-id="767cc-164">Les données provenant d’appareils non inscrits ne sont pas incluses.</span><span class="sxs-lookup"><span data-stu-id="767cc-164">Data from unenrolled devices isn't included.</span></span> <span data-ttu-id="767cc-165">Seuls les administrateurs globaux peuvent afficher ces cartes.</span><span class="sxs-lookup"><span data-stu-id="767cc-165">Only Global Administrators can view these cards.</span></span>

<span data-ttu-id="767cc-166">Les données d’appareil inscrites dans Intune incluent :</span><span class="sxs-lookup"><span data-stu-id="767cc-166">Intune enrolled device data includes:</span></span>

* <span data-ttu-id="767cc-167">Conformité des appareils</span><span class="sxs-lookup"><span data-stu-id="767cc-167">Device compliance</span></span>
* <span data-ttu-id="767cc-168">Appareils avec programmes malveillants actifs</span><span class="sxs-lookup"><span data-stu-id="767cc-168">Devices with active malware</span></span>
* <span data-ttu-id="767cc-169">Types de programmes malveillants sur les appareils</span><span class="sxs-lookup"><span data-stu-id="767cc-169">Types of malware on devices</span></span>
* <span data-ttu-id="767cc-170">Programmes malveillants sur les appareils</span><span class="sxs-lookup"><span data-stu-id="767cc-170">Malware on devices</span></span>
* <span data-ttu-id="767cc-171">Appareils avec détection de programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="767cc-171">Devices with malware detections</span></span>
* <span data-ttu-id="767cc-172">Utilisateurs avec détection de programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="767cc-172">Users with malware detections</span></span>

### <a name="monitor-device-compliance"></a><span data-ttu-id="767cc-173">Surveiller la conformité des appareils</span><span class="sxs-lookup"><span data-stu-id="767cc-173">Monitor device compliance</span></span>

<span data-ttu-id="767cc-174">**La conformité des** appareils indique le nombre d’appareils inscrits dans Intune conformes aux stratégies de configuration.</span><span class="sxs-lookup"><span data-stu-id="767cc-174">**Device compliance** shows how many devices that are enrolled in Intune comply with configuration policies.</span></span>

![Carte de conformité de l’appareil](../../media/device-compliance.png)

### <a name="discover-devices-with-malware-detections"></a><span data-ttu-id="767cc-176">Détecter les appareils avec détection de programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="767cc-176">Discover devices with malware detections</span></span>

<span data-ttu-id="767cc-177">**Les détections de programmes malveillants** de périphérique fournissent le nombre d’appareils inscrits à Intune avec des programmes malveillants qui n’ont pas été entièrement résolus.</span><span class="sxs-lookup"><span data-stu-id="767cc-177">**Device malware detections** provide the number of Intune enrolled devices with malware that hasn't been fully resolved.</span></span> <span data-ttu-id="767cc-178">Un manque de résolution peut être dû à des actions en attente, un redémarrage, une analyse complète, des actions manuelles de l’utilisateur ou si l’action de correction n’a pas été correctement effectuée.</span><span class="sxs-lookup"><span data-stu-id="767cc-178">A lack of resolution can be because of pending actions, a restart, a full scan, manual user actions, or if the remediation action was not successfully completed.</span></span>

![Carte de détection des programmes malveillants d’appareil](../../media/device-malware-detections.png)

### <a name="understand-the-types-of-malware-detected"></a><span data-ttu-id="767cc-180">Comprendre les types de programmes malveillants détectés</span><span class="sxs-lookup"><span data-stu-id="767cc-180">Understand the types of malware detected</span></span>

<span data-ttu-id="767cc-181">**Les types de programmes malveillants sur les appareils** indiquent différents types de programmes malveillants détectés sur les appareils inscrits dans Intune.</span><span class="sxs-lookup"><span data-stu-id="767cc-181">**Types of malware on devices** show different kinds of malware that have been detected on devices enrolled in Intune.</span></span> <span data-ttu-id="767cc-182">Vous pouvez examiner chaque type dans le Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="767cc-182">You can investigate each type in the Microsoft 365 security center.</span></span>

![Types de programmes malveillants sur la carte d’appareil](../../media/types-of-malware-on-devices.png)

### <a name="understand-the-specific-malware-detected-on-your-devices"></a><span data-ttu-id="767cc-184">Comprendre les programmes malveillants spécifiques détectés sur vos appareils</span><span class="sxs-lookup"><span data-stu-id="767cc-184">Understand the specific malware detected on your devices</span></span>

<span data-ttu-id="767cc-185">**Les programmes malveillants sur les** appareils fournissent une liste des programmes malveillants spécifiques détectés sur vos appareils.</span><span class="sxs-lookup"><span data-stu-id="767cc-185">**Malware on devices** provides a list of the specific malware detected on your devices.</span></span>

![Carte programmes malveillants sur les appareils](../../media/malware-on-devices.png)

### <a name="understand-which-devices-have-the-most-malware"></a><span data-ttu-id="767cc-187">Comprendre les appareils qui ont le plus de programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="767cc-187">Understand which devices have the most malware</span></span>

<span data-ttu-id="767cc-188">**Les appareils avec détection de programmes malveillants** indiquent les appareils qui ont le plus de détections de programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="767cc-188">**Devices with malware detections** show which devices have the most malware detections.</span></span> <span data-ttu-id="767cc-189">dans le Centre de sécurité Microsoft 365, vous pouvez déterminer si un programme malveillant est actif, qui utilise l’appareil et son état de gestion dans Intune.</span><span class="sxs-lookup"><span data-stu-id="767cc-189">in the Microsoft 365 security center, you can investigate whether malware is active, who uses the device, and its management status in Intune.</span></span>

![Appareils avec carte de détection de programmes malveillants](../../media/devices-with-malware-detections.png)

### <a name="understand-which-users-have-devices-with-the-most-malware"></a><span data-ttu-id="767cc-191">Comprendre quels utilisateurs ont des appareils avec le plus de programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="767cc-191">Understand which users have devices with the most malware</span></span>

<span data-ttu-id="767cc-192">**Les utilisateurs qui ont détecté des programmes malveillants** montrent les utilisateurs ayant le plus de détections de programmes malveillants sur des appareils.</span><span class="sxs-lookup"><span data-stu-id="767cc-192">**Users with malware detections** show users with devices that had the most malware detections.</span></span> <span data-ttu-id="767cc-193">Dans le Centre de sécurité Microsoft 365, vous pouvez voir le nombre d’appareils affectés à chaque utilisateur et plus d’informations sur chaque appareil et le type de programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="767cc-193">In the Microsoft 365 security center, you can see how many devices are assigned to each user and more information about each device and the type of malware.</span></span>

![Utilisateurs avec carte de détection de programmes malveillants](../../media/users-with-malware-detections.png)

## <a name="monitor-and-manage-attack-surface-reduction-rule-deployment-and-detections"></a><span data-ttu-id="767cc-195">Surveiller et gérer le déploiement et les détections des règles de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="767cc-195">Monitor and manage attack surface reduction rule deployment and detections</span></span>

<span data-ttu-id="767cc-196">Les règles de réduction de la surface d’attaque [(ASR)](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/attack-surface-reduction) permettent d’empêcher les actions et les applications généralement utilisées par des programmes malveillants malveillants pour infecter des appareils.</span><span class="sxs-lookup"><span data-stu-id="767cc-196">[Attack Surface Reduction (ASR) rules](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/attack-surface-reduction) help prevent actions and apps that are typically used by exploit-seeking malware to infect devices.</span></span> <span data-ttu-id="767cc-197">Ces règles contrôlent quand et comment les fichiers exécutables peuvent être exécutés.</span><span class="sxs-lookup"><span data-stu-id="767cc-197">These rules control when and how executables can run.</span></span> <span data-ttu-id="767cc-198">Par exemple, vous pouvez empêcher JavaScript ou VBScript de lancer un exécutable téléchargé, bloquer des appels API Win32 à partir de macros Office, ou bloquer les processus exécutés à partir de lecteurs USB.</span><span class="sxs-lookup"><span data-stu-id="767cc-198">For example, you can prevent JavaScript or VBScript from launching a downloaded executable, block Win32 API calls from Office macros, or block processes that run from USB drives.</span></span>

![Carte réduction de la surface d’attaque](../../media/attack-surface-reduction-rules.png)

<span data-ttu-id="767cc-200">La carte **Règles de réduction de la surface d’attaque** offre une vue d’ensemble du déploiement des règles sur vos appareils.</span><span class="sxs-lookup"><span data-stu-id="767cc-200">The **Attack surface reduction rules** card provides an overview of the deployment of rules across your devices.</span></span>

<span data-ttu-id="767cc-201">La barre supérieure de la carte affiche le nombre total d’appareils figurant dans les modes de déploiement suivants :</span><span class="sxs-lookup"><span data-stu-id="767cc-201">The top bar on the card shows the total number of devices that are in the following deployment modes:</span></span>

* <span data-ttu-id="767cc-202">**Mode blocage :** appareils avec au moins une règle configurée pour bloquer l’activité détectée</span><span class="sxs-lookup"><span data-stu-id="767cc-202">**Block mode**: devices with at least one rule configured to block detected activity</span></span>
* <span data-ttu-id="767cc-203">**Mode audit :** appareils sans règles définies pour bloquer l’activité détectée, mais avec au moins une règle définie pour auditer l’activité détectée</span><span class="sxs-lookup"><span data-stu-id="767cc-203">**Audit mode**: devices with no rules set to block detected activity, but has at least one rule set to audit detected activity</span></span>  
* <span data-ttu-id="767cc-204">**Désactivé :** appareils avec toutes les règles de la asr. désactivées</span><span class="sxs-lookup"><span data-stu-id="767cc-204">**Off**: devices with all ASR rules turned off</span></span>

<span data-ttu-id="767cc-205">La partie inférieure de cette carte présente les paramètres par règle sur tous vos appareils.</span><span class="sxs-lookup"><span data-stu-id="767cc-205">The lower part of this card shows settings by rule across your devices.</span></span> <span data-ttu-id="767cc-206">Chaque barre indique le nombre d’appareils qui sont définies pour bloquer, auditer la détection ou dont la règle est complètement désactivée.</span><span class="sxs-lookup"><span data-stu-id="767cc-206">Each bar indicates the number of devices that are set to block, audit detection, or have the rule completely turned off.</span></span>

### <a name="view-asr-detections"></a><span data-ttu-id="767cc-207">Afficher les détections de la asr.</span><span class="sxs-lookup"><span data-stu-id="767cc-207">View ASR detections</span></span>

<span data-ttu-id="767cc-208">Pour afficher des informations détaillées sur les détections de règles de réduction de la surface d’attaque dans votre réseau, sélectionnez Afficher les **détections** sur la carte des règles de réduction de la **surface d’attaque.**</span><span class="sxs-lookup"><span data-stu-id="767cc-208">To view detailed information about ASR rule detections in your network, select **View detections** on the **Attack surface reduction rules** card.</span></span> <span data-ttu-id="767cc-209">**L’onglet Détections** de la page de rapport détaillé s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="767cc-209">The **Detections** tab in the detailed report page will open.</span></span>

![Onglet Détections](../../media/detections-tab.png)

<span data-ttu-id="767cc-211">Le graphique en haut de la page présente les détections au fil du temps de détections d’empilement qui ont été bloquées ou auditées.</span><span class="sxs-lookup"><span data-stu-id="767cc-211">The chart at the top of the page shows detections over time stacking detections that were either blocked or audited.</span></span> <span data-ttu-id="767cc-212">Le tableau en bas répertorie les détections les plus récentes.</span><span class="sxs-lookup"><span data-stu-id="767cc-212">The table at the bottom lists the most recent detections.</span></span> <span data-ttu-id="767cc-213">Utilisez les informations suivantes sur le tableau pour comprendre la nature des détections :</span><span class="sxs-lookup"><span data-stu-id="767cc-213">Use the following information on the table to understand the nature of the detections:</span></span>

* <span data-ttu-id="767cc-214">**Fichier détecté :** le fichier, généralement un script ou un document, dont le contenu a déclenché l’activité d’attaque suspecte</span><span class="sxs-lookup"><span data-stu-id="767cc-214">**Detected file**: the file, typically a script or document, whose contents triggered the suspected attack activity</span></span>
* <span data-ttu-id="767cc-215">**Règle**: nom décrivant les activités d’attaque que la règle est conçue pour capturer.</span><span class="sxs-lookup"><span data-stu-id="767cc-215">**Rule**: name describing the attack activities the rule is designed to catch.</span></span> <span data-ttu-id="767cc-216">En savoir plus sur les règles de asr existantes</span><span class="sxs-lookup"><span data-stu-id="767cc-216">Read about existing ASR rules</span></span>
* <span data-ttu-id="767cc-217">**Application source**: application qui a chargé ou exécuté du contenu déclenchant l’activité d’attaque suspecte.</span><span class="sxs-lookup"><span data-stu-id="767cc-217">**Source app**: the application that loaded or executed content triggering the suspected attack activity.</span></span> <span data-ttu-id="767cc-218">Il peut s’agit d’une application légitime, telle qu’un navigateur web, une application Office ou un outil système tel que PowerShell.</span><span class="sxs-lookup"><span data-stu-id="767cc-218">It could be a legitimate application, such as web browser, an Office application, or a system tool like PowerShell</span></span>
* <span data-ttu-id="767cc-219">**Publisher**: le fournisseur qui a publié l’application source</span><span class="sxs-lookup"><span data-stu-id="767cc-219">**Publisher**: the vendor that released the source app</span></span>

### <a name="review-device-asr-rule-settings"></a><span data-ttu-id="767cc-220">Passer en revue les paramètres de règle asr de l’appareil</span><span class="sxs-lookup"><span data-stu-id="767cc-220">Review device ASR rule settings</span></span>

<span data-ttu-id="767cc-221">Dans la page Du rapport **règles de réduction** de la surface d’attaque, allez dans l’onglet **Configuration** pour passer en revue les paramètres de règle pour les appareils individuels.</span><span class="sxs-lookup"><span data-stu-id="767cc-221">In the **Attack surface reduction rules** report page, go to the **Configuration** tab to review rule settings for individual devices.</span></span> <span data-ttu-id="767cc-222">Sélectionnez un appareil pour obtenir des informations détaillées sur le fait que chaque règle soit en mode blocage, en mode audit ou complètement désactivée.</span><span class="sxs-lookup"><span data-stu-id="767cc-222">Select a device to get detailed information about whether each rule is in block mode, audit mode, or turned off entirely.</span></span>

![Onglet Configuration](../../media/configuration-tab.png)

<span data-ttu-id="767cc-224">Microsoft Intune fournit des fonctionnalités de gestion pour vos règles de astér.</span><span class="sxs-lookup"><span data-stu-id="767cc-224">Microsoft Intune provides management functionality for your ASR rules.</span></span> <span data-ttu-id="767cc-225">Si vous souhaitez mettre à  jour  vos paramètres, sélectionnez Prise en charge sous Configurer les appareils dans l’onglet pour ouvrir la gestion des appareils sur Intune.</span><span class="sxs-lookup"><span data-stu-id="767cc-225">If you want to update your settings, select **Get started** under **Configure devices** in the tab to open device management on Intune.</span></span>

### <a name="exclude-files-from-asr-rules"></a><span data-ttu-id="767cc-226">Exclure des fichiers des règles de la asr.</span><span class="sxs-lookup"><span data-stu-id="767cc-226">Exclude files from ASR rules</span></span>

<span data-ttu-id="767cc-227">Le Centre de sécurité Microsoft 365 collecte les noms des fichiers que vous souhaitez exclure des détections par les règles de réduction de la surface d’attaque. [](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/enable-attack-surface-reduction#exclude-files-and-folders-from-asr-rules)</span><span class="sxs-lookup"><span data-stu-id="767cc-227">Microsoft 365 security center collects the names of the [files you might want to exclude](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/enable-attack-surface-reduction#exclude-files-and-folders-from-asr-rules) from detections by attack surface reduction rules.</span></span> <span data-ttu-id="767cc-228">En excluant des fichiers, vous pouvez réduire les détections de faux positifs et déployer en toute confiance les règles de réduction de la surface d’attaque en mode blocage.</span><span class="sxs-lookup"><span data-stu-id="767cc-228">By excluding files, you can reduce false positive detections and more confidently deploy attack surface reduction rules in block mode.</span></span>

<span data-ttu-id="767cc-229">Les exclusions sont gérées sur Microsoft Intune, mais le Centre de sécurité Microsoft 365 fournit un outil d’analyse pour vous aider à comprendre les fichiers.</span><span class="sxs-lookup"><span data-stu-id="767cc-229">The exclusions are managed on Microsoft Intune, but Microsoft 365 security center provides an analysis tool to help you understand the files.</span></span> <span data-ttu-id="767cc-230">Pour commencer à collecter des fichiers pour l’exclusion, reportez-vous à l’onglet Ajouter des **exclusions** dans la page du rapport règles de réduction de la **surface d’attaque.**</span><span class="sxs-lookup"><span data-stu-id="767cc-230">To start collecting files for exclusion, go to the **Add exclusions** tab in the **Attack surface reduction rules** report page.</span></span>

>[!NOTE]  
><span data-ttu-id="767cc-231">L’outil analyse les détections par toutes les règles de réduction de la surface d’attaque, mais seules certaines règles peuvent prendre en charge [les exclusions.](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/troubleshoot-asr)</span><span class="sxs-lookup"><span data-stu-id="767cc-231">The tool analyzes detections by all attack surface reduction rules, but [only some rules support exclusions](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/troubleshoot-asr).</span></span>

![Onglet Ajouter des exclusions](../../media/add-exclusions-tab.png)

<span data-ttu-id="767cc-233">Le tableau répertorie tous les noms de fichiers détectés par vos règles de réduction de la surface d’attaque.</span><span class="sxs-lookup"><span data-stu-id="767cc-233">The table lists all the file names detected by your attack surface reduction rules.</span></span> <span data-ttu-id="767cc-234">Vous pouvez sélectionner des fichiers pour examiner l’impact de leur exclusion :</span><span class="sxs-lookup"><span data-stu-id="767cc-234">You can select files to review the impact of excluding them:</span></span>

* <span data-ttu-id="767cc-235">Nombre de détections moins nombreuses</span><span class="sxs-lookup"><span data-stu-id="767cc-235">How many fewer detections</span></span>
* <span data-ttu-id="767cc-236">Nombre d’appareils moins signalant les détections</span><span class="sxs-lookup"><span data-stu-id="767cc-236">How many fewer devices report the detections</span></span>

<span data-ttu-id="767cc-237">Pour obtenir une liste des fichiers sélectionnés avec leurs chemins d’accès complets pour l’exclusion, **sélectionnez Obtenir les chemins d’accès d’exclusion.**</span><span class="sxs-lookup"><span data-stu-id="767cc-237">To get a list of the selected files with their full paths for exclusion, select **Get exclusion paths**.</span></span>

<span data-ttu-id="767cc-238">Les journaux de la règle ASR bloquent le vol d’informations d’identification à partir du sous-système de l’autorité de sécurité locale **Windows (lsass.exe)** capturent l’application source **lsass.exe**.</span><span class="sxs-lookup"><span data-stu-id="767cc-238">Logs for the ASR rule **Block credential stealing from the Windows local security authority subsystem (lsass.exe)** capture the source app **lsass.exe**.</span></span> <span data-ttu-id="767cc-239">Il s’agit d’un fichier système normal, mais capturé en tant que fichier détecté.</span><span class="sxs-lookup"><span data-stu-id="767cc-239">It is a normal system file, but captured as the detected file.</span></span> <span data-ttu-id="767cc-240">Par conséquent, la liste des chemins d’exclusion générés inclut ce fichier.</span><span class="sxs-lookup"><span data-stu-id="767cc-240">As a result, the generated list of exclusion paths will include this file.</span></span> <span data-ttu-id="767cc-241">Pour exclure le fichier qui a déclenché cette règle au lieu de **lsass.exe,** utilisez le chemin d’accès à l’application source au lieu du fichier détecté.</span><span class="sxs-lookup"><span data-stu-id="767cc-241">To exclude the file that triggered this rule instead of **lsass.exe**, use the path to the source app instead of the detected file.</span></span>

<span data-ttu-id="767cc-242">Pour localiser l’application source, exécutez la requête de recherche avancée suivante pour cette règle spécifique (identifiée par l’ID de règle 9e6c4e1f-7d60-472f-ba1a-a39ef669e4b2) : [](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting)</span><span class="sxs-lookup"><span data-stu-id="767cc-242">To locate the source app, run the following [advanced hunting query](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting) for this specific rule (identified by rule ID 9e6c4e1f-7d60-472f-ba1a-a39ef669e4b2):</span></span>

```kusto
DeviceEvents
| where Timestamp > ago(7d)
| where ActionType startswith "Asr"
| where AdditionalFields contains "9e6c4e1f-7d60-472f-ba1a-a39ef669e4b2"
| project InitiatingProcessFolderPath, InitiatingProcessFileName
```

#### <a name="check-files-for-exclusion"></a><span data-ttu-id="767cc-243">Vérifier les fichiers pour l’exclusion</span><span class="sxs-lookup"><span data-stu-id="767cc-243">Check files for exclusion</span></span>

<span data-ttu-id="767cc-244">Avant d’exclure un fichier de la RSA, nous vous recommandons d’inspecter le fichier pour déterminer s’il n’est pas malveillant.</span><span class="sxs-lookup"><span data-stu-id="767cc-244">Before excluding a file from ASR, we recommend that you inspect the file to determine if it's indeed not malicious.</span></span>

<span data-ttu-id="767cc-245">Pour consulter un fichier, utilisez la [page d’informations](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/investigate-files) sur le fichier dans le Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="767cc-245">To review a file, use the [file information page](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/investigate-files) on Microsoft Defender Security Center.</span></span> <span data-ttu-id="767cc-246">La page fournit des informations sur la prévalence et le taux de détection antivirus VirusTotal.</span><span class="sxs-lookup"><span data-stu-id="767cc-246">The page provides prevalence information and the VirusTotal antivirus detection ratio.</span></span> <span data-ttu-id="767cc-247">Vous pouvez également utiliser la page pour envoyer le fichier pour analyse approfondie.</span><span class="sxs-lookup"><span data-stu-id="767cc-247">You can also use the page to submit the file for deep analysis.</span></span>

<span data-ttu-id="767cc-248">Pour localiser un fichier détecté dans le Centre de sécurité Microsoft Defender, recherchez toutes les détections de la asr à l’aide de la requête de repérage avancé suivante :</span><span class="sxs-lookup"><span data-stu-id="767cc-248">To locate a detected file in Microsoft Defender Security Center, search for all ASR detections using the following advanced hunting query:</span></span>

```kusto
MiscEvents
| where EventTime > ago(7d)
| where ActionType startswith "Asr"
| project FolderPath, FileName, SHA1, InitiatingProcessFolderPath, InitiatingProcessFileName, InitiatingProcessSHA1
```

<span data-ttu-id="767cc-249">Utilisez **sha1 ou** **InitiatingProcessSHA1** dans les résultats pour rechercher le fichier à l’aide de la barre de recherche universelle dans le Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="767cc-249">Use the **SHA1** or the **InitiatingProcessSHA1** in the results to search for the file using the universal search bar in Microsoft Defender Security Center.</span></span>
