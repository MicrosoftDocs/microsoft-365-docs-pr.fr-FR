---
title: Surveillance et création de rapports sur les appareils dans le centre de sécurité Microsoft 365
description: Décrit comment maintenir vos appareils sécurisés, mis à jour et détecter les menaces potentielles au sein de votre organisation
keywords: sécurité, programmes malveillants, Microsoft 365, M365, centre de sécurité, moniteur, rapport, appareils
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.localizationpriority: medium
ms.author: ellevin
author: levinec
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
search.appverid: met150
ms.openlocfilehash: 149b3ab2f30d2387165dd98c0ba21eeac0fc8728
ms.sourcegitcommit: 0c9c28a87201c7470716216d99175356fb3d1a47
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/09/2019
ms.locfileid: "39910387"
---
# <a name="device-monitoring-and-reporting-in-the-microsoft-365-security-center"></a><span data-ttu-id="fec1f-104">Surveillance et création de rapports sur les appareils dans le centre de sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="fec1f-104">Device monitoring and reporting in the Microsoft 365 security center</span></span>

<span data-ttu-id="fec1f-105">Maintenez vos appareils sécurisés, mis à jour, et présentez les menaces potentielles dans le centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="fec1f-105">Keep your devices secure, up-to-date, and spot potential threats in the Microsoft 365 security center.</span></span>

## <a name="view-device-alerts"></a><span data-ttu-id="fec1f-106">Afficher les alertes de l’appareil</span><span class="sxs-lookup"><span data-stu-id="fec1f-106">View device alerts</span></span>

<span data-ttu-id="fec1f-107">Obtenez des alertes à jour sur l’activité de violation et d’autres menaces sur vos appareils à partir de Microsoft Defender ATP (disponible avec une licence E5).</span><span class="sxs-lookup"><span data-stu-id="fec1f-107">Get up-to-date alerts about breach activity and other threats on your devices from Microsoft Defender ATP (available with an E5 license).</span></span> <span data-ttu-id="fec1f-108">Le centre de sécurité Microsoft 365 contrôle efficacement ces alertes à un niveau élevé à l’aide de votre flux de travail préféré.</span><span class="sxs-lookup"><span data-stu-id="fec1f-108">Microsoft 365 security center effectively monitors these alerts at a high level using your preferred workflow.</span></span>

### <a name="monitor-high-impact-alerts"></a><span data-ttu-id="fec1f-109">Surveiller les alertes à fort impact</span><span class="sxs-lookup"><span data-stu-id="fec1f-109">Monitor high-impact alerts</span></span>

<span data-ttu-id="fec1f-110">Chaque alerte Microsoft Defender ATP a une gravité élevée, moyenne, faible ou informatif qui indique son impact potentiel sur votre réseau si elle est sans assistance.</span><span class="sxs-lookup"><span data-stu-id="fec1f-110">Each Microsoft Defender ATP alert has a corresponding severity�high, medium, low, or informational�that indicates its potential impact to your network if left unattended.</span></span>  

<span data-ttu-id="fec1f-111">Utilisez la carte de **gravité des alertes de périphérique** pour vous concentrer spécifiquement sur les alertes plus sévères et susceptibles de nécessiter une réponse immédiate.</span><span class="sxs-lookup"><span data-stu-id="fec1f-111">Use the **Device alert severity** card to focus specifically on alerts that are more severe and might require immediate response.</span></span> <span data-ttu-id="fec1f-112">À partir de cette carte, vous pouvez consulter plus d’informations sur le portail du centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="fec1f-112">From this card, you can view more information on the Microsoft Defender Security Center portal.</span></span>

![Carte de gravité des alertes d’appareil](../images/device-alerts-severity.png)

### <a name="understand-sources-of-alerts"></a><span data-ttu-id="fec1f-114">Comprendre les sources d’alertes</span><span class="sxs-lookup"><span data-stu-id="fec1f-114">Understand sources of alerts</span></span>

<span data-ttu-id="fec1f-115">Microsoft Defender ATP exploite les données d’une large gamme de capteurs de sécurité et de sources d’intelligence pour générer des alertes.</span><span class="sxs-lookup"><span data-stu-id="fec1f-115">Microsoft Defender ATP leverages data from a broad range of security sensors and intelligence sources to generate alerts.</span></span> <span data-ttu-id="fec1f-116">Par exemple, il peut utiliser les informations de détection de l’antivirus Windows Defender et des logiciels malveillants tiers, ainsi que votre propre intelligence de menace personnalisée fournie via l’API de service Web.</span><span class="sxs-lookup"><span data-stu-id="fec1f-116">For example, it can use detection information from Windows Defender Antivirus and third-party antimalware, as well as your own custom threat intelligence provided through the web service API.</span></span>

<span data-ttu-id="fec1f-117">La carte sources de détection des alertes de **périphérique** affiche la répartition des alertes par source.</span><span class="sxs-lookup"><span data-stu-id="fec1f-117">The **Device alert detection** sources card shows the distribution of alerts by source.</span></span> <span data-ttu-id="fec1f-118">Cette carte peut vous aider à suivre l’activité liée à certaines sources, en particulier vos sources personnalisées.</span><span class="sxs-lookup"><span data-stu-id="fec1f-118">This card can help you track activity related to certain sources, particularly your custom sources.</span></span> <span data-ttu-id="fec1f-119">Vous pouvez également l’utiliser pour vous concentrer sur les alertes provenant de capteurs qui ne sont pas configurés pour bloquer automatiquement les activités ou les composants malveillants.</span><span class="sxs-lookup"><span data-stu-id="fec1f-119">You can also use this to focus on alerts coming from sensors that are not configured to automatically block malicious activity or components.</span></span>

![Carte sources de détection des alertes de périphérique](../images/device-alert-detection-sources.png)

<span data-ttu-id="fec1f-121">À partir de cette carte, vous pouvez consulter plus d’informations sur le portail du centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="fec1f-121">From this card, you can view more information on the Microsoft Defender Security Center portal.</span></span>

### <a name="understand-the-types-of-threats-that-trigger-alerts"></a><span data-ttu-id="fec1f-122">Comprendre les types de menaces déclenchant des alertes</span><span class="sxs-lookup"><span data-stu-id="fec1f-122">Understand the types of threats that trigger alerts</span></span>

<span data-ttu-id="fec1f-123">Microsoft Defender ATP trie chaque alerte dans une catégorie représentant une certaine étape de la chaîne d’attaque ou d’un type de composant de menace.</span><span class="sxs-lookup"><span data-stu-id="fec1f-123">Microsoft Defender ATP sorts each alert into a category representing a certain stage in the attack chain or a type of threat component.</span></span> <span data-ttu-id="fec1f-124">Par exemple, l’activité de menace détectée peut être classée en mouvement latéral pour indiquer que l’activité impliquait une tentative d’atteindre d’autres appareils sur le réseau et qu’elle a vraisemblablement été effectuée après que des pirates ont acquis un premier sens.</span><span class="sxs-lookup"><span data-stu-id="fec1f-124">For example, detected threat activity might be categorized into �lateral movement� to indicate that the activity involved an attempt to reach other devices on the network and has likely occurred after attackers have gained an initial foothold.</span></span> <span data-ttu-id="fec1f-125">Lorsqu’il est détecté, un composant de menace peut être classé largement comme un logiciel malveillant ou plus spécifiquement comme ransomware, un vol d’informations d’identification ou d’autres types de logiciels malveillants ou indésirables.</span><span class="sxs-lookup"><span data-stu-id="fec1f-125">When detected, a threat component might either be classified broadly as �malware� or more specifically as �ransomware�, �credential stealing� or other types of malicious or unwanted software.</span></span>

<span data-ttu-id="fec1f-126">La carte des **catégories de menaces du périphérique** affiche la répartition des alertes dans ces catégories.</span><span class="sxs-lookup"><span data-stu-id="fec1f-126">The **Device threat categories** card shows the distribution of alerts into these categories.</span></span> <span data-ttu-id="fec1f-127">Vous pouvez utiliser ces informations pour identifier les activités de menace, telles que les tentatives de vol d’informations d’identification, ce qui peut avoir un impact plus significatif par rapport aux tentatives d’ingénierie sociale, par exemple.</span><span class="sxs-lookup"><span data-stu-id="fec1f-127">You can use this information to identify threat activity, such as attempts at credential theft, which can have more significant impact compared to attempts at social engineering, for example.</span></span> <span data-ttu-id="fec1f-128">Vous pouvez également l’utiliser pour surveiller les menaces pouvant être destructrices telles que les ransomware.</span><span class="sxs-lookup"><span data-stu-id="fec1f-128">You can also use this to monitor for potentially destructive threats like ransomware.</span></span>

![Carte des catégories de menaces de périphérique](../images/device-threat-categories.png)

### <a name="monitor-active-alerts"></a><span data-ttu-id="fec1f-130">Surveiller les alertes actives</span><span class="sxs-lookup"><span data-stu-id="fec1f-130">Monitor active alerts</span></span>

<span data-ttu-id="fec1f-131">La carte d' **État des alertes de périphérique** indique le nombre d’alertes qui n’ont pas été résolues et peuvent nécessiter votre attention.</span><span class="sxs-lookup"><span data-stu-id="fec1f-131">The **Device alert status** card indicates the number of alerts that have not been resolved and might require attention.</span></span> <span data-ttu-id="fec1f-132">À partir de cette carte, vous pouvez consulter plus d’informations sur le portail du centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="fec1f-132">From this card, you can view more information on the Microsoft Defender Security Center portal.</span></span>

![Carte d’état d’alerte de périphérique](../images/device-alert-status.png)

### <a name="monitor-classification-of-resolved-alerts"></a><span data-ttu-id="fec1f-134">Surveiller la classification des alertes résolues</span><span class="sxs-lookup"><span data-stu-id="fec1f-134">Monitor classification of resolved alerts</span></span>

<span data-ttu-id="fec1f-135">Lors de la résolution d’une alerte Microsoft Defender ATP, votre équipe de sécurité peut spécifier si une alerte a été vérifiée comme suit :</span><span class="sxs-lookup"><span data-stu-id="fec1f-135">When resolving a Microsoft Defender ATP alert, your security staff can specify whether an alert has been verified as:</span></span>

* <span data-ttu-id="fec1f-136">Alerte vraie qui identifie les composants de menace ou d’activité de violation réels</span><span class="sxs-lookup"><span data-stu-id="fec1f-136">A true alert that identifies actual breach activity or threat components</span></span>
* <span data-ttu-id="fec1f-137">Alerte erronée ayant détecté une activité normale de manière incorrecte</span><span class="sxs-lookup"><span data-stu-id="fec1f-137">A false alert that has incorrectly detected normal activity</span></span>

<span data-ttu-id="fec1f-138">La fiche classification des alertes de **périphérique** indique si les alertes résolues ont été classées comme vrai ou faux.</span><span class="sxs-lookup"><span data-stu-id="fec1f-138">The **Device alert classification** card shows whether your resolved alerts have been classified as true or false alerts.</span></span> <span data-ttu-id="fec1f-139">À partir de cette carte, vous pouvez consulter plus d’informations sur le portail du centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="fec1f-139">From this card, you can view more information on the Microsoft Defender Security Center portal.</span></span>

<span data-ttu-id="fec1f-140">Remarque : dans certains cas, les informations de classification ne sont pas disponibles pour certaines alertes.</span><span class="sxs-lookup"><span data-stu-id="fec1f-140">Note: In some cases, classification information is unavailable for certain alerts.</span></span>

![Carte de classification des alertes de périphérique](../images/device-alert-classification.png)

### <a name="monitor-determination-of-resolved-alerts"></a><span data-ttu-id="fec1f-142">Surveiller la détermination des alertes résolues</span><span class="sxs-lookup"><span data-stu-id="fec1f-142">Monitor determination of resolved alerts</span></span>

<span data-ttu-id="fec1f-143">En plus de déterminer si une alerte est true ou false au cours de la résolution, votre équipe de sécurité peut fournir une détermination indiquant le type d’activité normale ou malveillante détectée lors de la validation de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="fec1f-143">In addition to classifying whether an alert is true or false during resolution, your security staff can provide a determination, indicating the type of normal or malicious activity that was found while validating the alert.</span></span>

<span data-ttu-id="fec1f-144">La carte de **détermination des alertes de périphérique** indique la détermination fournie pour chaque alerte, en particulier :</span><span class="sxs-lookup"><span data-stu-id="fec1f-144">The **Device alert determination** card shows the determination provided for each alert, specifically:</span></span>

* <span data-ttu-id="fec1f-145">**Apt** Advanced persistent Threat, indiquant que le composant de menace ou d’activité détecté fait partie d’une violation sophistiquée conçue pour se faire une brèche dans le réseau affecté</span><span class="sxs-lookup"><span data-stu-id="fec1f-145">**APT** � advanced persistent threat, indicating that the detected activity or threat component is part of a sophisticated breach designed to gain a foothold in the affected network</span></span>  
* <span data-ttu-id="fec1f-146">Fichier ou **code malveillant malveillant**</span><span class="sxs-lookup"><span data-stu-id="fec1f-146">**Malware** � malicious file or code</span></span>
* <span data-ttu-id="fec1f-147">Activité normale **du personnel de sécurité** effectuée par le personnel de sécurité</span><span class="sxs-lookup"><span data-stu-id="fec1f-147">**Security personnel** � normal activity performed by security staff</span></span>
* <span data-ttu-id="fec1f-148">Activité de **test de sécurité** ou composants conçus pour simuler les menaces réelles et qui doivent déclencher des capteurs de sécurité et générer des alertes</span><span class="sxs-lookup"><span data-stu-id="fec1f-148">**Security testing** � activity or components designed to simulate actual threats and expected to trigger security sensors and generate alerts</span></span>
* <span data-ttu-id="fec1f-149">Les applications **logicielles indésirables** et d’autres logiciels qui ne sont pas considérés comme malveillants, mais enfreignent les normes de stratégie ou d’utilisation acceptable</span><span class="sxs-lookup"><span data-stu-id="fec1f-149">**Unwanted software** � apps and other software that are not considered malicious, but otherwise violate policy or acceptable use standards</span></span>
* <span data-ttu-id="fec1f-150">**Autres** dédéterminations qui ne tombent pas sous les types fournis</span><span class="sxs-lookup"><span data-stu-id="fec1f-150">**Others** � any other determination that does not fall under the provided types</span></span>

<span data-ttu-id="fec1f-151">À partir de cette carte, vous pouvez consulter plus d’informations dans le centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="fec1f-151">From this card, you can view more information in Microsoft Defender Security Center.</span></span>

![Carte de détermination d’alerte de périphérique](../images/device-alert-determination.png)

### <a name="understand-which-devices-are-at-risk"></a><span data-ttu-id="fec1f-153">Comprendre quels périphériques sont exposés</span><span class="sxs-lookup"><span data-stu-id="fec1f-153">Understand which devices are at risk</span></span>

<span data-ttu-id="fec1f-154">**Device protection** indique le niveau de risque pour les appareils.</span><span class="sxs-lookup"><span data-stu-id="fec1f-154">**Device protection** shows the risk level for devices.</span></span> <span data-ttu-id="fec1f-155">Le niveau de risque est basé sur des facteurs tels que le type et la gravité des alertes sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="fec1f-155">The risk level is based on factors such as the type and severity of alerts on the device.</span></span>

![Carte de protection des appareils](../images/device-protection.png)

## <a name="monitor-and-report-status-of-intune-managed-devices"></a><span data-ttu-id="fec1f-157">Surveillance et signalement de l’état des appareils gérés par Intune</span><span class="sxs-lookup"><span data-stu-id="fec1f-157">Monitor and report status of Intune-managed devices</span></span>

<span data-ttu-id="fec1f-158">Les rapports suivants contiennent des données provenant d’appareils intégrés dans Intune.</span><span class="sxs-lookup"><span data-stu-id="fec1f-158">The following reports contain data from devices enrolled in Intune.</span></span> <span data-ttu-id="fec1f-159">Les données provenant d’appareils non inscrits ne sont pas incluses.</span><span class="sxs-lookup"><span data-stu-id="fec1f-159">Data from unenrolled devices is not included.</span></span> <span data-ttu-id="fec1f-160">Seuls les administrateurs globaux peuvent afficher ces cartes.</span><span class="sxs-lookup"><span data-stu-id="fec1f-160">Only Global Administrators can view these cards.</span></span>

<span data-ttu-id="fec1f-161">Les données d’appareil apportées Intune incluent :</span><span class="sxs-lookup"><span data-stu-id="fec1f-161">Intune enrolled device data includes:</span></span>

* <span data-ttu-id="fec1f-162">Conformité des appareils</span><span class="sxs-lookup"><span data-stu-id="fec1f-162">Device compliance</span></span>
* <span data-ttu-id="fec1f-163">Appareils avec programme malveillant actif</span><span class="sxs-lookup"><span data-stu-id="fec1f-163">Devices with active malware</span></span>
* <span data-ttu-id="fec1f-164">Types de programmes malveillants sur les appareils</span><span class="sxs-lookup"><span data-stu-id="fec1f-164">Types of malware on devices</span></span>
* <span data-ttu-id="fec1f-165">Programmes malveillants sur les appareils</span><span class="sxs-lookup"><span data-stu-id="fec1f-165">Malware on devices</span></span>
* <span data-ttu-id="fec1f-166">Appareils avec des détections de programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="fec1f-166">Devices with malware detections</span></span>
* <span data-ttu-id="fec1f-167">Utilisateurs avec des détections de programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="fec1f-167">Users with malware detections</span></span>

### <a name="monitor-device-compliance"></a><span data-ttu-id="fec1f-168">Surveiller la conformité des appareils</span><span class="sxs-lookup"><span data-stu-id="fec1f-168">Monitor device compliance</span></span>

<span data-ttu-id="fec1f-169">**La conformité des appareils** indique le nombre de périphériques qui sont intégrés dans Intune conformément aux stratégies de configuration.</span><span class="sxs-lookup"><span data-stu-id="fec1f-169">**Device compliance** shows how many devices that are enrolled in Intune comply with configuration policies.</span></span>

![Carte de conformité des appareils](../images/device-compliance.png)

### <a name="discover-devices-with-malware-detections"></a><span data-ttu-id="fec1f-171">Détecter les appareils avec des détections de programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="fec1f-171">Discover devices with malware detections</span></span>

<span data-ttu-id="fec1f-172">**Périphériques les détections de programmes malveillants d’appareils** fournissent le nombre d’appareils apportés Intune avec des programmes malveillants qui n’ont pas été entièrement résolus en raison d’actions en attente un redémarrage, une analyse complète ou des actions utilisateur manuelles ou si l’action de correction ne s’est pas exécutée correctement.</span><span class="sxs-lookup"><span data-stu-id="fec1f-172">**Device malware detections** provides the number of Intune enrolled devices with malware that have not been fully resolved due to pending actions�a restart, a full scan or manual user actions�or if the remediation action did not complete successfully.</span></span>

![Carte de détection des programmes malveillants d’appareils](../images/device-malware-detections.png)

### <a name="understand-the-types-of-malware-detected"></a><span data-ttu-id="fec1f-174">Comprendre les types de programmes malveillants détectés</span><span class="sxs-lookup"><span data-stu-id="fec1f-174">Understand the types of malware detected</span></span>

<span data-ttu-id="fec1f-175">**Types de programmes malveillants sur les appareils** affiche différents types de programmes malveillants qui ont été détectés sur les appareils intégrés dans Intune.</span><span class="sxs-lookup"><span data-stu-id="fec1f-175">**Types of malware on devices** shows different kinds of malware that have been detected on devices enrolled in Intune.</span></span> <span data-ttu-id="fec1f-176">Vous pouvez examiner chaque type dans le centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="fec1f-176">You can investigate each type in the Microsoft 365 security center.</span></span>

![Types de programmes malveillants sur la carte des appareils](../images/types-of-malware-on-devices.png)

### <a name="understand-the-specific-malware-detected-on-your-devices"></a><span data-ttu-id="fec1f-178">Comprendre le programme malveillant spécifique détecté sur vos appareils</span><span class="sxs-lookup"><span data-stu-id="fec1f-178">Understand the specific malware detected on your devices</span></span>

<span data-ttu-id="fec1f-179">**Programmes malveillants sur les appareils** fournit une liste des programmes malveillants spécifiques détectés sur vos appareils.</span><span class="sxs-lookup"><span data-stu-id="fec1f-179">**Malware on devices** provides a list of the specific malware detected on your devices.</span></span>

![Carte de programmes malveillants sur les appareils](../images/malware-on-devices.png)

### <a name="understand-which-devices-have-the-most-malware"></a><span data-ttu-id="fec1f-181">Comprendre quels appareils ont le plus de programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="fec1f-181">Understand which devices have the most malware</span></span>

<span data-ttu-id="fec1f-182">**Périphériques avec des détections de programmes malveillants** indique quels périphériques ont le plus de détections de programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="fec1f-182">**Devices with malware detections** shows which devices have the most malware detections.</span></span> <span data-ttu-id="fec1f-183">dans le centre de sécurité Microsoft 365, vous pouvez rechercher si un programme malveillant est actif, qui utilise l’appareil et son statut de gestion dans Intune.</span><span class="sxs-lookup"><span data-stu-id="fec1f-183">in the Microsoft 365 security center, you can investigate whether malware is active, who uses the device, and its management status in Intune.</span></span>

![Carte périphériques avec des détections de programmes malveillants](../images/devices-with-malware-detections.png)

### <a name="understand-which-users-have-devices-with-the-most-malware"></a><span data-ttu-id="fec1f-185">Comprendre quels sont les utilisateurs ayant des appareils avec le plus de programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="fec1f-185">Understand which users have devices with the most malware</span></span>

<span data-ttu-id="fec1f-186">**Les utilisateurs disposant de détections de programmes malveillants** affichent les utilisateurs avec des appareils qui avaient le plus de détections de programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="fec1f-186">**Users with malware detections** shows users with devices that had the most malware detections.</span></span> <span data-ttu-id="fec1f-187">dans le centre de sécurité Microsoft 365, vous pouvez voir le nombre d’appareils affectés à chaque utilisateur et des informations sur chaque appareil et le type de programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="fec1f-187">in the Microsoft 365 security center, you can see how many devices are assigned to each user and more information about each device and the type of malware.</span></span>

![Utilisateurs avec carte de détection des programmes malveillants](../images/users-with-malware-detections.png)

## <a name="monitor-and-manage-asr-rule-deployment-and-detections"></a><span data-ttu-id="fec1f-189">Surveillance et gestion du déploiement et des détections de règles ASR</span><span class="sxs-lookup"><span data-stu-id="fec1f-189">Monitor and manage ASR rule deployment and detections</span></span>

<span data-ttu-id="fec1f-190">Les règles de réduction de la [surface d’attaque (ASR)](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-exploit-guard/attack-surface-reduction-exploit-guard) permettent d’empêcher les actions et les applications généralement utilisées par les programmes malveillants de recherche d’attaques pour infecter les appareils.</span><span class="sxs-lookup"><span data-stu-id="fec1f-190">[Attack Surface Reduction (ASR) rules](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-exploit-guard/attack-surface-reduction-exploit-guard) help prevent actions and apps that are typically used by exploit-seeking malware to infect devices.</span></span> <span data-ttu-id="fec1f-191">Ces règles contrôlent quand et comment les fichiers exécutables peuvent être exécutés.</span><span class="sxs-lookup"><span data-stu-id="fec1f-191">These rules control when and how executables can run.</span></span> <span data-ttu-id="fec1f-192">Par exemple, vous pouvez empêcher JavaScript ou VBScript de lancer un exécutable téléchargé, bloquer des appels API Win32 à partir de macros Office, ou bloquer les processus exécutés à partir de lecteurs USB.</span><span class="sxs-lookup"><span data-stu-id="fec1f-192">For example, you can prevent JavaScript or VBScript from launching a downloaded executable, block Win32 API calls from Office macros, or block processes that run from USB drives.</span></span>

![Carte de réduction de surface d’attaque](../images/attack-surface-reduction-rules.png)

<span data-ttu-id="fec1f-194">La carte **Règles de réduction de la surface d’attaque** offre une vue d’ensemble du déploiement des règles sur vos appareils.</span><span class="sxs-lookup"><span data-stu-id="fec1f-194">The **Attack surface reduction rules** card provides an overview of the deployment of rules across your devices.</span></span>

<span data-ttu-id="fec1f-195">La barre supérieure de la carte affiche le nombre total d’appareils figurant dans les modes de déploiement suivants :</span><span class="sxs-lookup"><span data-stu-id="fec1f-195">The top bar on the card shows the total number of devices that are in the following deployment modes:</span></span>

* <span data-ttu-id="fec1f-196">Appareils **en mode bloc** avec au moins une règle configurée pour bloquer l’activité détectée</span><span class="sxs-lookup"><span data-stu-id="fec1f-196">**Block mode** � devices with at least one rule configured to block detected activity</span></span>
* <span data-ttu-id="fec1f-197">Les appareils **en mode audit** sans règles définies pour bloquer les activités détectées, mais ont au moins un ensemble de règles pour auditer les activités détectées</span><span class="sxs-lookup"><span data-stu-id="fec1f-197">**Audit mode** � devices with no rules set to block detected activity, but has at least one rule set to audit detected activity</span></span>  
* <span data-ttu-id="fec1f-198">**Désactiver** les périphériques lorsque toutes les règles ASR sont désactivées</span><span class="sxs-lookup"><span data-stu-id="fec1f-198">**Off** � devices with all ASR rules turned off</span></span>

<span data-ttu-id="fec1f-199">La partie inférieure de cette carte présente les paramètres par règle sur tous vos appareils.</span><span class="sxs-lookup"><span data-stu-id="fec1f-199">The lower part of this card shows settings by rule across your devices.</span></span> <span data-ttu-id="fec1f-200">Chaque barre indique le nombre d’appareils configurés pour bloquer ou auditer la détection ou pour lesquels la règle est complètement désactivée.</span><span class="sxs-lookup"><span data-stu-id="fec1f-200">Each bar indicates the number of devices that are set to block or audit detection or have the rule completely turned off.</span></span>

### <a name="view-asr-detections"></a><span data-ttu-id="fec1f-201">Afficher les détections ASR</span><span class="sxs-lookup"><span data-stu-id="fec1f-201">View ASR detections</span></span>

<span data-ttu-id="fec1f-202">Pour afficher des informations détaillées sur les détections de règles ASR sur votre réseau, sélectionnez **afficher les détections** sur la carte des règles de réduction de la **surface d’attaque** .</span><span class="sxs-lookup"><span data-stu-id="fec1f-202">To view detailed information about ASR rule detections in your network, select **View detections** on the **Attack surface reduction rules** card.</span></span> <span data-ttu-id="fec1f-203">L’onglet **détections** de la page rapport détaillé s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="fec1f-203">The **Detections** tab in the detailed report page will open.</span></span>

![Onglet détections](../images/detections-tab.png)

<span data-ttu-id="fec1f-205">Le graphique en haut de la page affiche les détections dans le temps de détections de pile qui ont été bloquées ou auditées.</span><span class="sxs-lookup"><span data-stu-id="fec1f-205">The chart at the top of the page shows detections over time stacking detections that were either blocked or audited.</span></span> <span data-ttu-id="fec1f-206">Le tableau en bas répertorie les détections les plus récentes.</span><span class="sxs-lookup"><span data-stu-id="fec1f-206">The table at the bottom lists the most recent detections.</span></span> <span data-ttu-id="fec1f-207">Utilisez les informations suivantes sur le tableau pour comprendre la nature des détections :</span><span class="sxs-lookup"><span data-stu-id="fec1f-207">Use the following information on the table to understand the nature of the detections:</span></span>

* <span data-ttu-id="fec1f-208">**Fichier détecté** le fichier, généralement un script ou un document, dont le contenu a déclenché l’activité d’attaque suspecte</span><span class="sxs-lookup"><span data-stu-id="fec1f-208">**Detected file** � the file, typically a script or a document, whose contents triggered the suspected attack activity</span></span>
* <span data-ttu-id="fec1f-209">Nom de la **règle** décrivant les activités d’attaque la règle est conçue pour être interceptée.</span><span class="sxs-lookup"><span data-stu-id="fec1f-209">**Rule** � name describing the attack activities the rule is designed to catch.</span></span> <span data-ttu-id="fec1f-210">En savoir plus sur les règles ASR existantes</span><span class="sxs-lookup"><span data-stu-id="fec1f-210">Read about existing ASR rules</span></span>
* <span data-ttu-id="fec1f-211">Application **source** application qui a chargé ou exécuté du contenu qui déclenche l’activité d’attaque suspectée.</span><span class="sxs-lookup"><span data-stu-id="fec1f-211">**Source app** � the application that loaded or executed content triggering the suspected attack activity.</span></span> <span data-ttu-id="fec1f-212">Il peut s’agir d’une application légitime, telle qu’un navigateur Web, une application Office ou un outil système tel que PowerShell</span><span class="sxs-lookup"><span data-stu-id="fec1f-212">This could be a legitimate application, such as web browser, an Office application, or a system tool like PowerShell</span></span>
* <span data-ttu-id="fec1f-213">**Publisher** fournisseur qui a publié l’application source</span><span class="sxs-lookup"><span data-stu-id="fec1f-213">**Publisher** � the vendor that released the source app</span></span>

### <a name="review-device-asr-rule-settings"></a><span data-ttu-id="fec1f-214">Vérifier les paramètres de règle ASR de l’appareil</span><span class="sxs-lookup"><span data-stu-id="fec1f-214">Review device ASR rule settings</span></span>

<span data-ttu-id="fec1f-215">Dans la page rapport sur les règles de réduction de la **surface d’attaque** , accédez à l’onglet **configuration** pour vérifier les paramètres de règle pour les appareils individuels.</span><span class="sxs-lookup"><span data-stu-id="fec1f-215">In the **Attack surface reduction rules** report page, go to the **Configuration** tab to review rule settings for individual devices.</span></span> <span data-ttu-id="fec1f-216">Sélectionnez un appareil pour obtenir des informations détaillées sur la façon dont chaque règle est en mode bloquer, mode audit ou désactivé entièrement.</span><span class="sxs-lookup"><span data-stu-id="fec1f-216">Select a device to get detailed information about whether each rule is in block mode, audit mode, or turned off entirely.</span></span>

![Onglet Configuration](../images/configuration-tab.png)

<span data-ttu-id="fec1f-218">Microsoft Intune offre des fonctionnalités de gestion pour vos règles de récupération automatique du système.</span><span class="sxs-lookup"><span data-stu-id="fec1f-218">Microsoft Intune provides management functionality for your ASR rules.</span></span> <span data-ttu-id="fec1f-219">Si vous souhaitez mettre à jour vos paramètres, sélectionnez **prise en main** sous configurer les **appareils** sous l’onglet pour ouvrir gestion des appareils sur Intune.</span><span class="sxs-lookup"><span data-stu-id="fec1f-219">If you want to update your settings, select **Get started** under **Configure devices** in the tab to open device management on Intune.</span></span>

### <a name="exclude-files-from-asr-rules"></a><span data-ttu-id="fec1f-220">Exclure les fichiers des règles ASR</span><span class="sxs-lookup"><span data-stu-id="fec1f-220">Exclude files from ASR rules</span></span>

<span data-ttu-id="fec1f-221">Le centre de sécurité Microsoft 365 recueille les noms des [fichiers que vous pouvez exclure](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-exploit-guard/troubleshoot-asr#add-exclusions-for-a-false-positive) des détections par des règles de réduction de la surface d’attaque.</span><span class="sxs-lookup"><span data-stu-id="fec1f-221">Microsoft 365 security center collects the names of the [files you might want to exclude](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-exploit-guard/troubleshoot-asr#add-exclusions-for-a-false-positive) from detections by attack surface reduction rules.</span></span> <span data-ttu-id="fec1f-222">En excluant des fichiers, vous pouvez réduire les faux positifs et déployer en toute confiance les règles de réduction de la surface d’attaque en mode bloc.</span><span class="sxs-lookup"><span data-stu-id="fec1f-222">By excluding files, you can reduce false positive detections and more confidently deploy attack surface reduction rules in block mode.</span></span>

<span data-ttu-id="fec1f-223">Les exclusions sont gérées sur Microsoft Intune, mais le centre de sécurité Microsoft 365 fournit un outil d’analyse pour vous aider à comprendre les fichiers.</span><span class="sxs-lookup"><span data-stu-id="fec1f-223">The exclusions are managed on Microsoft Intune, but Microsoft 365 security center provides an analysis tool to help you understand the files.</span></span> <span data-ttu-id="fec1f-224">Pour commencer à collecter des fichiers pour exclusion, accédez à l’onglet **Ajouter des exclusions** dans la page rapport des règles de réduction de la **surface d’attaque** .</span><span class="sxs-lookup"><span data-stu-id="fec1f-224">To start collecting files for exclusion, go to the **Add exclusions** tab in the **Attack surface reduction rules** report page.</span></span>

>[!NOTE]  
><span data-ttu-id="fec1f-225">L’outil analyse les détections par toutes les règles de réduction de la surface d’attaque, mais [seules certaines règles prennent en charge les exclusions](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-exploit-guard/attack-surface-reduction-exploit-guard#attack-surface-reduction-rules).</span><span class="sxs-lookup"><span data-stu-id="fec1f-225">The tool analyzes detections by all attack surface reduction rules, but [only some rules support exclusions](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-exploit-guard/attack-surface-reduction-exploit-guard#attack-surface-reduction-rules).</span></span>

![Onglet ajouter des exclusions](../images/add-exclusions-tab.png)

<span data-ttu-id="fec1f-227">Le tableau répertorie tous les noms de fichiers détectés par les règles de réduction de la surface d’attaque.</span><span class="sxs-lookup"><span data-stu-id="fec1f-227">The table lists all the file names detected by your attack surface reduction rules.</span></span> <span data-ttu-id="fec1f-228">Vous pouvez sélectionner des fichiers pour vérifier l’impact de leur exclusion :</span><span class="sxs-lookup"><span data-stu-id="fec1f-228">You can select files to review the impact of excluding them:</span></span>

* <span data-ttu-id="fec1f-229">Nombre de détections moins nombreuses</span><span class="sxs-lookup"><span data-stu-id="fec1f-229">How many fewer detections</span></span>
* <span data-ttu-id="fec1f-230">Nombre d’appareils qui signalent les menaces détectées</span><span class="sxs-lookup"><span data-stu-id="fec1f-230">How many fewer devices report the detections</span></span>

<span data-ttu-id="fec1f-231">Pour obtenir la liste des fichiers sélectionnés avec leur chemin d’accès complet pour l’exclusion, sélectionnez **obtenir les chemins d’exclusion**.</span><span class="sxs-lookup"><span data-stu-id="fec1f-231">To get a list of the selected files with their full paths for exclusion, select **Get exclusion paths**.</span></span>

<span data-ttu-id="fec1f-232">Journaux pour les **informations d’identification de blocage de la règle ASR dérobent du sous-système Windows local Security Authority (lsass. exe)** Capturez l’application source **lsass. exe**, un fichier système normal, comme fichier détecté.</span><span class="sxs-lookup"><span data-stu-id="fec1f-232">Logs for the ASR rule **Block credential stealing from the Windows local security authority subsystem (lsass.exe)** capture the source app **lsass.exe**, a normal system file, as the detected file.</span></span> <span data-ttu-id="fec1f-233">Par conséquent, la liste générée des chemins d’exclusion inclut ce fichier.</span><span class="sxs-lookup"><span data-stu-id="fec1f-233">As a result, the generated list of exclusion paths will include this file.</span></span> <span data-ttu-id="fec1f-234">Pour exclure le fichier qui a déclenché cette règle au lieu de **lsass. exe**, utilisez le chemin d’accès à l’application source au lieu du fichier détecté.</span><span class="sxs-lookup"><span data-stu-id="fec1f-234">To exclude the file that triggered this rule instead of **lsass.exe**, use the path to the source app instead of the detected file.</span></span>

<span data-ttu-id="fec1f-235">Pour localiser l’application source, exécutez la [requête de recherche avancée](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting) suivante pour cette règle spécifique (identifiée par l’ID de règle 9e6c4e1f-7d60-472f-bA1a-a39ef669e4b2) :</span><span class="sxs-lookup"><span data-stu-id="fec1f-235">To locate the source app, run the following [advanced hunting query](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting) for this specific rule (identified by rule ID 9e6c4e1f-7d60-472f-ba1a-a39ef669e4b2):</span></span>

```MiscEvents
| where EventTime > ago(7d)
| where ActionType startswith "Asr"
| where AdditionalFields contains "9e6c4e1f-7d60-472f-ba1a-a39ef669e4b2"
| project InitiatingProcessFolderPath, InitiatingProcessFileName
```

#### <a name="check-files-for-exclusion"></a><span data-ttu-id="fec1f-236">Vérifier les fichiers pour exclusion</span><span class="sxs-lookup"><span data-stu-id="fec1f-236">Check files for exclusion</span></span>
<span data-ttu-id="fec1f-237">Avant d’exclure un fichier de la récupération automatique du système, nous vous recommandons d’inspecter le fichier afin de déterminer s’il n’est pas malveillant.</span><span class="sxs-lookup"><span data-stu-id="fec1f-237">Before excluding a file from ASR, we recommend that you inspect the file to determine if it is indeed not malicious.</span></span>

<span data-ttu-id="fec1f-238">Pour passer en revue un fichier, utilisez la [page informations](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/investigate-files) sur le fichier sur le centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="fec1f-238">To review a file, use the [file information page](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/investigate-files) on Microsoft Defender Security Center.</span></span> <span data-ttu-id="fec1f-239">La page fournit des informations de récurrence ainsi que le ratio de détection antivirus VirusTotal.</span><span class="sxs-lookup"><span data-stu-id="fec1f-239">The page provides prevalence information as well as the VirusTotal antivirus detection ratio.</span></span> <span data-ttu-id="fec1f-240">Vous pouvez également utiliser la page pour envoyer le fichier pour une analyse approfondie.</span><span class="sxs-lookup"><span data-stu-id="fec1f-240">You can also use the page to submit the file for deep analysis.</span></span>

<span data-ttu-id="fec1f-241">Pour rechercher un fichier détecté dans le centre de sécurité Microsoft Defender, recherchez toutes les détections de récupération automatique du système à l’aide de la requête de chasse avancée suivante :</span><span class="sxs-lookup"><span data-stu-id="fec1f-241">To locate a detected file in Microsoft Defender Security Center, search for all ASR detections using the following advanced hunting query:</span></span>

```MiscEvents
| where EventTime > ago(7d)
| where ActionType startswith "Asr"
| project FolderPath, FileName, SHA1, InitiatingProcessFolderPath, InitiatingProcessFileName, InitiatingProcessSHA1
```

<span data-ttu-id="fec1f-242">Utilisez **SHA1** ou le **InitiatingProcessSHA1** dans les résultats pour rechercher le fichier à l’aide de la barre de recherche universelle dans le centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="fec1f-242">Use the **SHA1** or the **InitiatingProcessSHA1** in the results to search for the file using the universal search bar in Microsoft Defender Security Center.</span></span>