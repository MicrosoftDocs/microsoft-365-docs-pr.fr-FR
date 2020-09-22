---
title: Rapports sur les & de surveillance des appareils-Centre de sécurité
description: Décrit comment maintenir vos appareils sécurisés, mis à jour et détecter les menaces potentielles au sein de votre organisation
keywords: sécurité, programmes malveillants, Microsoft 365, M365, centre de sécurité, moniteur, rapport, appareils
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.localizationpriority: medium
f1.keywords:
- NOCSH
ms.author: ellevin
author: levinec
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
search.appverid: met150
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 638fa558d3bc83b94f1a165e8d087e3770357d42
ms.sourcegitcommit: c083602dda3cdcb5b58cb8aa070d77019075f765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2020
ms.locfileid: "48200028"
---
# <a name="device-monitoring-and-reporting-in-the-microsoft-365-security-center"></a><span data-ttu-id="4b41f-104">Surveillance et création de rapports sur les appareils dans le centre de sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="4b41f-104">Device monitoring and reporting in the Microsoft 365 security center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="4b41f-105">Maintenez vos appareils sécurisés, mis à jour, et présentez les menaces potentielles dans le centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4b41f-105">Keep your devices secure, up-to-date, and spot potential threats in the Microsoft 365 security center.</span></span>

## <a name="view-device-alerts"></a><span data-ttu-id="4b41f-106">Afficher les alertes de l’appareil</span><span class="sxs-lookup"><span data-stu-id="4b41f-106">View device alerts</span></span>

<span data-ttu-id="4b41f-107">Obtenez des alertes à jour sur l’activité de violation et d’autres menaces sur vos appareils à partir de Microsoft Defender ATP (disponible avec une licence E5).</span><span class="sxs-lookup"><span data-stu-id="4b41f-107">Get up-to-date alerts about breach activity and other threats on your devices from Microsoft Defender ATP (available with an E5 license).</span></span> <span data-ttu-id="4b41f-108">Le centre de sécurité Microsoft 365 contrôle efficacement ces alertes à un niveau élevé à l’aide de votre flux de travail préféré.</span><span class="sxs-lookup"><span data-stu-id="4b41f-108">Microsoft 365 security center effectively monitors these alerts at a high level using your preferred workflow.</span></span>

### <a name="monitor-high-impact-alerts"></a><span data-ttu-id="4b41f-109">Surveiller les alertes à fort impact</span><span class="sxs-lookup"><span data-stu-id="4b41f-109">Monitor high-impact alerts</span></span>

<span data-ttu-id="4b41f-110">Chaque alerte Microsoft Defender ATP a une gravité correspondante (élevé, moyen, faible ou informatif).</span><span class="sxs-lookup"><span data-stu-id="4b41f-110">Each Microsoft Defender ATP alert has a corresponding severity (high, medium, low, or informational).</span></span> <span data-ttu-id="4b41f-111">Il indique l’impact potentiel sur votre réseau si vous n’êtes pas en mode sans assistance.</span><span class="sxs-lookup"><span data-stu-id="4b41f-111">It indicates potential impact to your network if left unattended.</span></span>  

<span data-ttu-id="4b41f-112">Utilisez la carte de **gravité des alertes de périphérique** pour vous concentrer spécifiquement sur les alertes plus sévères et susceptibles de nécessiter une réponse immédiate.</span><span class="sxs-lookup"><span data-stu-id="4b41f-112">Use the **Device alert severity** card to focus specifically on alerts that are more severe and might require immediate response.</span></span> <span data-ttu-id="4b41f-113">À partir de cette carte, vous pouvez consulter plus d’informations sur le portail du centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="4b41f-113">From this card, you can view more information on the Microsoft Defender Security Center portal.</span></span>

![Carte de gravité des alertes d’appareil](../../media/device-alerts-severity.png)

### <a name="understand-sources-of-alerts"></a><span data-ttu-id="4b41f-115">Comprendre les sources d’alertes</span><span class="sxs-lookup"><span data-stu-id="4b41f-115">Understand sources of alerts</span></span>

<span data-ttu-id="4b41f-116">Microsoft Defender ATP exploite les données d’une large gamme de capteurs de sécurité et de sources d’intelligence pour générer des alertes.</span><span class="sxs-lookup"><span data-stu-id="4b41f-116">Microsoft Defender ATP leverages data from a broad range of security sensors and intelligence sources to generate alerts.</span></span> <span data-ttu-id="4b41f-117">Par exemple, il peut utiliser les informations de détection de l’antivirus Microsoft Defender et du logiciel anti-programme malveillant tiers.</span><span class="sxs-lookup"><span data-stu-id="4b41f-117">For example, it can use detection information from Microsoft Defender Antivirus and third-party antimalware.</span></span> <span data-ttu-id="4b41f-118">Il peut également utiliser votre propre intelligence de menace personnalisée fournie par le biais de l’API de service Web.</span><span class="sxs-lookup"><span data-stu-id="4b41f-118">It can also use your own custom threat intelligence provided through the web service API.</span></span>

<span data-ttu-id="4b41f-119">La carte sources de détection des alertes de **périphérique** affiche la répartition des alertes par source.</span><span class="sxs-lookup"><span data-stu-id="4b41f-119">The **Device alert detection** sources card shows the distribution of alerts by source.</span></span> <span data-ttu-id="4b41f-120">Effectuer le suivi de l’activité liée à certaines sources, en particulier vos sources personnalisées.</span><span class="sxs-lookup"><span data-stu-id="4b41f-120">Track activity related to certain sources, particularly your custom sources.</span></span> <span data-ttu-id="4b41f-121">Vous pouvez également utiliser la carte pour vous concentrer sur les alertes provenant de capteurs qui ne sont pas configurés pour bloquer automatiquement les activités ou les composants malveillants.</span><span class="sxs-lookup"><span data-stu-id="4b41f-121">You can also use the card to focus on alerts coming from sensors that aren't configured to automatically block malicious activity or components.</span></span>

![Carte sources de détection des alertes de périphérique](../../media/device-alert-detection-sources.png)

<span data-ttu-id="4b41f-123">À partir de cette carte, vous pouvez consulter plus d’informations sur le portail du centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="4b41f-123">From this card, you can view more information on the Microsoft Defender Security Center portal.</span></span>

### <a name="understand-the-types-of-threats-that-trigger-alerts"></a><span data-ttu-id="4b41f-124">Comprendre les types de menaces déclenchant des alertes</span><span class="sxs-lookup"><span data-stu-id="4b41f-124">Understand the types of threats that trigger alerts</span></span>

<span data-ttu-id="4b41f-125">Microsoft Defender ATP trie chaque alerte dans une catégorie représentant un certain stade de la chaîne d’attaque ou du type de composant de menace.</span><span class="sxs-lookup"><span data-stu-id="4b41f-125">Microsoft Defender ATP sorts each alert into a category representing a certain stage in the attack chain or type of threat component.</span></span> <span data-ttu-id="4b41f-126">Par exemple, une activité de menace détectée peut être classée « mouvement latéral » pour indiquer qu’il y a eu une tentative d’accès à d’autres appareils sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="4b41f-126">For example, a detected threat activity might be categorized as "lateral movement" to indicate there was an attempt to reach other devices on the network.</span></span> <span data-ttu-id="4b41f-127">L’activité est probablement survenue après que des pirates ont acquis un premier lieu.</span><span class="sxs-lookup"><span data-stu-id="4b41f-127">The activity has likely occurred after attackers gained an initial foothold.</span></span> <span data-ttu-id="4b41f-128">Lorsqu’il est détecté, un composant de menace peut être classé globalement comme logiciel malveillant ou spécifiquement comme type de menace spécifique.</span><span class="sxs-lookup"><span data-stu-id="4b41f-128">When detected, a threat component might be classified broadly as malware or specifically as a specific threat type.</span></span> <span data-ttu-id="4b41f-129">Les caractéristiques incluent les ransomware, le vol d’informations d’identification ou d’autres types de logiciels malveillants ou indésirables.</span><span class="sxs-lookup"><span data-stu-id="4b41f-129">Specifics include ransomware, credential stealing, or other types of malicious or unwanted software.</span></span>

<span data-ttu-id="4b41f-130">La carte des **catégories de menaces du périphérique** affiche la répartition des alertes dans ces catégories.</span><span class="sxs-lookup"><span data-stu-id="4b41f-130">The **Device threat categories** card shows the distribution of alerts into these categories.</span></span> <span data-ttu-id="4b41f-131">Utilisez ces informations pour identifier les activités de menace, telles que les tentatives de vol d’informations d’identification, qui ont généralement un impact plus élevé que les tentatives d’ingénierie sociale.</span><span class="sxs-lookup"><span data-stu-id="4b41f-131">Use this information to identify threat activity, such as credential theft attempts, that usually have higher impact than social engineering attempts.</span></span> <span data-ttu-id="4b41f-132">Vous pouvez également surveiller les menaces pouvant être destructrices telles que les ransomware.</span><span class="sxs-lookup"><span data-stu-id="4b41f-132">You can also to monitor for potentially destructive threats like ransomware.</span></span>

![Carte des catégories de menaces de périphérique](../../media/device-threat-categories.png)

### <a name="monitor-active-alerts"></a><span data-ttu-id="4b41f-134">Surveiller les alertes actives</span><span class="sxs-lookup"><span data-stu-id="4b41f-134">Monitor active alerts</span></span>

<span data-ttu-id="4b41f-135">La carte d' **État des alertes de périphérique** indique le nombre d’alertes qui n’ont pas été résolues et peuvent nécessiter votre attention.</span><span class="sxs-lookup"><span data-stu-id="4b41f-135">The **Device alert status** card indicates the number of alerts that haven't been resolved and may require attention.</span></span> <span data-ttu-id="4b41f-136">À partir de cette carte, vous pouvez consulter plus d’informations sur le portail du centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="4b41f-136">From this card, you can view more information on the Microsoft Defender Security Center portal.</span></span>

![Carte d’état d’alerte de périphérique](../../media/device-alert-status.png)

### <a name="monitor-classification-of-resolved-alerts"></a><span data-ttu-id="4b41f-138">Surveiller la classification des alertes résolues</span><span class="sxs-lookup"><span data-stu-id="4b41f-138">Monitor classification of resolved alerts</span></span>

<span data-ttu-id="4b41f-139">Lors de la résolution d’une alerte Microsoft Defender ATP, votre équipe de sécurité peut spécifier si une alerte a été vérifiée comme suit :</span><span class="sxs-lookup"><span data-stu-id="4b41f-139">When resolving a Microsoft Defender ATP alert, your security staff can specify whether an alert has been verified as:</span></span>

* <span data-ttu-id="4b41f-140">Alerte vraie qui identifie les composants de menace ou d’activité de violation réels</span><span class="sxs-lookup"><span data-stu-id="4b41f-140">A true alert that identifies actual breach activity or threat components</span></span>
* <span data-ttu-id="4b41f-141">Alerte erronée ayant détecté une activité normale de manière incorrecte</span><span class="sxs-lookup"><span data-stu-id="4b41f-141">A false alert that has incorrectly detected normal activity</span></span>

<span data-ttu-id="4b41f-142">La fiche classification des alertes de **périphérique** indique si les alertes résolues ont été classées comme vrai ou faux.</span><span class="sxs-lookup"><span data-stu-id="4b41f-142">The **Device alert classification** card shows whether your resolved alerts have been classified as true or false alerts.</span></span> <span data-ttu-id="4b41f-143">À partir de cette carte, vous pouvez consulter plus d’informations sur le portail du centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="4b41f-143">From this card, you can view more information on the Microsoft Defender Security Center portal.</span></span>

<span data-ttu-id="4b41f-144">Remarque : dans certains cas, les informations de classification ne sont pas disponibles pour certaines alertes.</span><span class="sxs-lookup"><span data-stu-id="4b41f-144">Note: In some cases, classification information is unavailable for certain alerts.</span></span>

![Carte de classification des alertes de périphérique](../../media/device-alert-classification.png)

### <a name="monitor-determination-of-resolved-alerts"></a><span data-ttu-id="4b41f-146">Surveiller la détermination des alertes résolues</span><span class="sxs-lookup"><span data-stu-id="4b41f-146">Monitor determination of resolved alerts</span></span>

<span data-ttu-id="4b41f-147">En plus de déterminer si une alerte est true ou false au cours de la résolution, votre équipe de sécurité peut fournir une détermination.</span><span class="sxs-lookup"><span data-stu-id="4b41f-147">Along with classifying whether an alert is true or false during resolution, your security staff can provide a determination.</span></span> <span data-ttu-id="4b41f-148">Une détermination indique le type d’activité normale ou malveillante qui a été trouvée lors de la validation de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="4b41f-148">A determination indicates the type of normal or malicious activity that was found while validating the alert.</span></span>

<span data-ttu-id="4b41f-149">La carte de **détermination des alertes de périphérique** indique la détermination fournie pour chaque alerte.</span><span class="sxs-lookup"><span data-stu-id="4b41f-149">The **Device alert determination** card shows the determination provided for each alert.</span></span>

* <span data-ttu-id="4b41f-150">**Apt**: menace persistante avancée, indiquant que le composant de menace ou d’activité détecté fait partie d’une violation sophistiquée conçue pour se faire une brèche dans le réseau affecté</span><span class="sxs-lookup"><span data-stu-id="4b41f-150">**APT**: advanced persistent threat, indicating that the detected activity or threat component is part of a sophisticated breach designed to gain a foothold in the affected network</span></span>  
* <span data-ttu-id="4b41f-151">**Programme malveillant**: fichier ou code malveillant</span><span class="sxs-lookup"><span data-stu-id="4b41f-151">**Malware**: malicious file or code</span></span>
* <span data-ttu-id="4b41f-152">**Personnel de sécurité**: activité normale effectuée par le personnel de sécurité</span><span class="sxs-lookup"><span data-stu-id="4b41f-152">**Security personnel**: normal activity performed by security staff</span></span>
* <span data-ttu-id="4b41f-153">**Test de sécurité**: activité ou composants destinés à simuler les menaces réelles et devant déclencher des alertes de sécurité et générer des alertes</span><span class="sxs-lookup"><span data-stu-id="4b41f-153">**Security testing**: activity or components designed to simulate actual threats and expected to trigger security sensors and generate alerts</span></span>
* <span data-ttu-id="4b41f-154">**Logiciels indésirables**: applications et autres logiciels qui ne sont pas considérés comme malveillants, mais enfreignent une stratégie ou des normes d’utilisation acceptables.</span><span class="sxs-lookup"><span data-stu-id="4b41f-154">**Unwanted software**: apps and other software that are not considered malicious, but otherwise violate policy or acceptable use standards</span></span>
* <span data-ttu-id="4b41f-155">**Autres**: toute autre détermination qui ne relève pas des types fournis</span><span class="sxs-lookup"><span data-stu-id="4b41f-155">**Others**: any other determination that doesn't fall under the provided types</span></span>

<span data-ttu-id="4b41f-156">À partir de cette carte, vous pouvez consulter plus d’informations dans le centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="4b41f-156">From this card, you can view more information in Microsoft Defender Security Center.</span></span>

![Carte de détermination d’alerte de périphérique](../../media/device-alert-determination.png)

### <a name="understand-which-devices-are-at-risk"></a><span data-ttu-id="4b41f-158">Comprendre quels périphériques sont exposés</span><span class="sxs-lookup"><span data-stu-id="4b41f-158">Understand which devices are at risk</span></span>

<span data-ttu-id="4b41f-159">**Device protection** indique le niveau de risque pour les appareils.</span><span class="sxs-lookup"><span data-stu-id="4b41f-159">**Device protection** shows the risk level for devices.</span></span> <span data-ttu-id="4b41f-160">Le niveau de risque est basé sur des facteurs tels que le type et la gravité des alertes sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4b41f-160">The risk level is based on factors such as the type and severity of alerts on the device.</span></span>

![Carte de protection des appareils](../../media/device-protection.png)

## <a name="monitor-and-report-status-of-intune-managed-devices"></a><span data-ttu-id="4b41f-162">Surveillance et signalement de l’état des appareils gérés par Intune</span><span class="sxs-lookup"><span data-stu-id="4b41f-162">Monitor and report status of Intune-managed devices</span></span>

<span data-ttu-id="4b41f-163">Les rapports suivants contiennent des données provenant d’appareils intégrés dans Intune.</span><span class="sxs-lookup"><span data-stu-id="4b41f-163">The following reports contain data from devices enrolled in Intune.</span></span> <span data-ttu-id="4b41f-164">Les données provenant d’appareils non inscrits ne sont pas incluses.</span><span class="sxs-lookup"><span data-stu-id="4b41f-164">Data from unenrolled devices isn't included.</span></span> <span data-ttu-id="4b41f-165">Seuls les administrateurs globaux peuvent afficher ces cartes.</span><span class="sxs-lookup"><span data-stu-id="4b41f-165">Only Global Administrators can view these cards.</span></span>

<span data-ttu-id="4b41f-166">Les données d’appareil apportées Intune incluent :</span><span class="sxs-lookup"><span data-stu-id="4b41f-166">Intune enrolled device data includes:</span></span>

* <span data-ttu-id="4b41f-167">Conformité des appareils</span><span class="sxs-lookup"><span data-stu-id="4b41f-167">Device compliance</span></span>
* <span data-ttu-id="4b41f-168">Appareils avec programme malveillant actif</span><span class="sxs-lookup"><span data-stu-id="4b41f-168">Devices with active malware</span></span>
* <span data-ttu-id="4b41f-169">Types de programmes malveillants sur les appareils</span><span class="sxs-lookup"><span data-stu-id="4b41f-169">Types of malware on devices</span></span>
* <span data-ttu-id="4b41f-170">Programmes malveillants sur les appareils</span><span class="sxs-lookup"><span data-stu-id="4b41f-170">Malware on devices</span></span>
* <span data-ttu-id="4b41f-171">Appareils avec des détections de programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="4b41f-171">Devices with malware detections</span></span>
* <span data-ttu-id="4b41f-172">Utilisateurs avec des détections de programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="4b41f-172">Users with malware detections</span></span>

### <a name="monitor-device-compliance"></a><span data-ttu-id="4b41f-173">Surveiller la conformité des appareils</span><span class="sxs-lookup"><span data-stu-id="4b41f-173">Monitor device compliance</span></span>

<span data-ttu-id="4b41f-174">**La conformité des appareils** indique le nombre de périphériques qui sont intégrés dans Intune conformément aux stratégies de configuration.</span><span class="sxs-lookup"><span data-stu-id="4b41f-174">**Device compliance** shows how many devices that are enrolled in Intune comply with configuration policies.</span></span>

![Carte de conformité des appareils](../../media/device-compliance.png)

### <a name="discover-devices-with-malware-detections"></a><span data-ttu-id="4b41f-176">Détecter les appareils avec des détections de programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="4b41f-176">Discover devices with malware detections</span></span>

<span data-ttu-id="4b41f-177">Les **détections de programmes malveillants d’appareils** fournissent le nombre d’appareils apportés Intune avec des programmes malveillants qui n’ont pas été entièrement résolus.</span><span class="sxs-lookup"><span data-stu-id="4b41f-177">**Device malware detections** provide the number of Intune enrolled devices with malware that hasn't been fully resolved.</span></span> <span data-ttu-id="4b41f-178">Un manque de résolution peut être dû à des actions en attente, un redémarrage, une analyse complète, des actions utilisateur manuelles ou si l’action de correction n’a pas abouti.</span><span class="sxs-lookup"><span data-stu-id="4b41f-178">A lack of resolution can be because of pending actions, a restart, a full scan, manual user actions, or if the remediation action was not successfully completed.</span></span>

![Carte de détection des programmes malveillants d’appareils](../../media/device-malware-detections.png)

### <a name="understand-the-types-of-malware-detected"></a><span data-ttu-id="4b41f-180">Comprendre les types de programmes malveillants détectés</span><span class="sxs-lookup"><span data-stu-id="4b41f-180">Understand the types of malware detected</span></span>

<span data-ttu-id="4b41f-181">**Types de programmes malveillants sur les appareils** Affichez les différents types de programmes malveillants qui ont été détectés sur les appareils intégrés dans Intune.</span><span class="sxs-lookup"><span data-stu-id="4b41f-181">**Types of malware on devices** show different kinds of malware that have been detected on devices enrolled in Intune.</span></span> <span data-ttu-id="4b41f-182">Vous pouvez examiner chaque type dans le centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4b41f-182">You can investigate each type in the Microsoft 365 security center.</span></span>

![Types de programmes malveillants sur la carte des appareils](../../media/types-of-malware-on-devices.png)

### <a name="understand-the-specific-malware-detected-on-your-devices"></a><span data-ttu-id="4b41f-184">Comprendre le programme malveillant spécifique détecté sur vos appareils</span><span class="sxs-lookup"><span data-stu-id="4b41f-184">Understand the specific malware detected on your devices</span></span>

<span data-ttu-id="4b41f-185">**Programmes malveillants sur les appareils** fournit une liste des programmes malveillants spécifiques détectés sur vos appareils.</span><span class="sxs-lookup"><span data-stu-id="4b41f-185">**Malware on devices** provides a list of the specific malware detected on your devices.</span></span>

![Carte de programmes malveillants sur les appareils](../../media/malware-on-devices.png)

### <a name="understand-which-devices-have-the-most-malware"></a><span data-ttu-id="4b41f-187">Comprendre quels appareils ont le plus de programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="4b41f-187">Understand which devices have the most malware</span></span>

<span data-ttu-id="4b41f-188">Les **appareils avec des détections de programmes malveillants** indiquent quels appareils ont le plus de détections de programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="4b41f-188">**Devices with malware detections** show which devices have the most malware detections.</span></span> <span data-ttu-id="4b41f-189">dans le centre de sécurité Microsoft 365, vous pouvez rechercher si un programme malveillant est actif, qui utilise l’appareil et son statut de gestion dans Intune.</span><span class="sxs-lookup"><span data-stu-id="4b41f-189">in the Microsoft 365 security center, you can investigate whether malware is active, who uses the device, and its management status in Intune.</span></span>

![Carte périphériques avec des détections de programmes malveillants](../../media/devices-with-malware-detections.png)

### <a name="understand-which-users-have-devices-with-the-most-malware"></a><span data-ttu-id="4b41f-191">Comprendre quels sont les utilisateurs ayant des appareils avec le plus de programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="4b41f-191">Understand which users have devices with the most malware</span></span>

<span data-ttu-id="4b41f-192">**Les utilisateurs disposant de détections de programmes malveillants** affichent les utilisateurs avec des appareils ayant eu le plus de détections de programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="4b41f-192">**Users with malware detections** show users with devices that had the most malware detections.</span></span> <span data-ttu-id="4b41f-193">Dans le centre de sécurité Microsoft 365, vous pouvez voir le nombre d’appareils affectés à chaque utilisateur et des informations sur chaque appareil et le type de programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="4b41f-193">In the Microsoft 365 security center, you can see how many devices are assigned to each user and more information about each device and the type of malware.</span></span>

![Utilisateurs avec carte de détection des programmes malveillants](../../media/users-with-malware-detections.png)

## <a name="monitor-and-manage-attack-surface-reduction-rule-deployment-and-detections"></a><span data-ttu-id="4b41f-195">Surveillance et gestion du déploiement et des détections de règles de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="4b41f-195">Monitor and manage attack surface reduction rule deployment and detections</span></span>

<span data-ttu-id="4b41f-196">Les règles de réduction de la [surface d’attaque (ASR)](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/attack-surface-reduction) permettent d’empêcher les actions et les applications généralement utilisées par les programmes malveillants de recherche d’attaques pour infecter les appareils.</span><span class="sxs-lookup"><span data-stu-id="4b41f-196">[Attack Surface Reduction (ASR) rules](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/attack-surface-reduction) help prevent actions and apps that are typically used by exploit-seeking malware to infect devices.</span></span> <span data-ttu-id="4b41f-197">Ces règles contrôlent quand et comment les fichiers exécutables peuvent être exécutés.</span><span class="sxs-lookup"><span data-stu-id="4b41f-197">These rules control when and how executables can run.</span></span> <span data-ttu-id="4b41f-198">Par exemple, vous pouvez empêcher JavaScript ou VBScript de lancer un exécutable téléchargé, bloquer des appels API Win32 à partir de macros Office, ou bloquer les processus exécutés à partir de lecteurs USB.</span><span class="sxs-lookup"><span data-stu-id="4b41f-198">For example, you can prevent JavaScript or VBScript from launching a downloaded executable, block Win32 API calls from Office macros, or block processes that run from USB drives.</span></span>

![Carte de réduction de surface d’attaque](../../media/attack-surface-reduction-rules.png)

<span data-ttu-id="4b41f-200">La carte **Règles de réduction de la surface d’attaque** offre une vue d’ensemble du déploiement des règles sur vos appareils.</span><span class="sxs-lookup"><span data-stu-id="4b41f-200">The **Attack surface reduction rules** card provides an overview of the deployment of rules across your devices.</span></span>

<span data-ttu-id="4b41f-201">La barre supérieure de la carte affiche le nombre total d’appareils figurant dans les modes de déploiement suivants :</span><span class="sxs-lookup"><span data-stu-id="4b41f-201">The top bar on the card shows the total number of devices that are in the following deployment modes:</span></span>

* <span data-ttu-id="4b41f-202">**Mode blocage**: appareils avec au moins une règle configurée pour bloquer l’activité détectée</span><span class="sxs-lookup"><span data-stu-id="4b41f-202">**Block mode**: devices with at least one rule configured to block detected activity</span></span>
* <span data-ttu-id="4b41f-203">**Mode audit**: appareils pour lesquels aucune règle n’est définie pour bloquer les activités détectées, mais au moins un ensemble de règles pour auditer les activités détectées</span><span class="sxs-lookup"><span data-stu-id="4b41f-203">**Audit mode**: devices with no rules set to block detected activity, but has at least one rule set to audit detected activity</span></span>  
* <span data-ttu-id="4b41f-204">**Désactivé**: les appareils dont toutes les règles de récupération automatique sont désactivées</span><span class="sxs-lookup"><span data-stu-id="4b41f-204">**Off**: devices with all ASR rules turned off</span></span>

<span data-ttu-id="4b41f-205">La partie inférieure de cette carte présente les paramètres par règle sur tous vos appareils.</span><span class="sxs-lookup"><span data-stu-id="4b41f-205">The lower part of this card shows settings by rule across your devices.</span></span> <span data-ttu-id="4b41f-206">Chaque barre indique le nombre de périphériques qui sont configurés pour bloquer, la détection d’audit ou la règle est complètement désactivée.</span><span class="sxs-lookup"><span data-stu-id="4b41f-206">Each bar indicates the number of devices that are set to block, audit detection, or have the rule completely turned off.</span></span>

### <a name="view-asr-detections"></a><span data-ttu-id="4b41f-207">Afficher les détections ASR</span><span class="sxs-lookup"><span data-stu-id="4b41f-207">View ASR detections</span></span>

<span data-ttu-id="4b41f-208">Pour afficher des informations détaillées sur les détections de règles ASR sur votre réseau, sélectionnez **afficher les détections** sur la carte des règles de réduction de la **surface d’attaque** .</span><span class="sxs-lookup"><span data-stu-id="4b41f-208">To view detailed information about ASR rule detections in your network, select **View detections** on the **Attack surface reduction rules** card.</span></span> <span data-ttu-id="4b41f-209">L’onglet **détections** de la page rapport détaillé s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="4b41f-209">The **Detections** tab in the detailed report page will open.</span></span>

![Onglet détections](../../media/detections-tab.png)

<span data-ttu-id="4b41f-211">Le graphique en haut de la page affiche les détections dans le temps de détections de pile qui ont été bloquées ou auditées.</span><span class="sxs-lookup"><span data-stu-id="4b41f-211">The chart at the top of the page shows detections over time stacking detections that were either blocked or audited.</span></span> <span data-ttu-id="4b41f-212">Le tableau en bas répertorie les détections les plus récentes.</span><span class="sxs-lookup"><span data-stu-id="4b41f-212">The table at the bottom lists the most recent detections.</span></span> <span data-ttu-id="4b41f-213">Utilisez les informations suivantes sur le tableau pour comprendre la nature des détections :</span><span class="sxs-lookup"><span data-stu-id="4b41f-213">Use the following information on the table to understand the nature of the detections:</span></span>

* <span data-ttu-id="4b41f-214">**Fichier détecté**: le fichier, généralement un script ou un document, dont le contenu a déclenché l’activité d’attaque suspecte.</span><span class="sxs-lookup"><span data-stu-id="4b41f-214">**Detected file**: the file, typically a script or document, whose contents triggered the suspected attack activity</span></span>
* <span data-ttu-id="4b41f-215">**Règle**: nom décrivant les activités d’attaque la règle est conçue pour être interceptée.</span><span class="sxs-lookup"><span data-stu-id="4b41f-215">**Rule**: name describing the attack activities the rule is designed to catch.</span></span> <span data-ttu-id="4b41f-216">En savoir plus sur les règles ASR existantes</span><span class="sxs-lookup"><span data-stu-id="4b41f-216">Read about existing ASR rules</span></span>
* <span data-ttu-id="4b41f-217">Application **source**: l’application qui a chargé ou exécuté le contenu qui déclenche l’activité d’attaque présumée.</span><span class="sxs-lookup"><span data-stu-id="4b41f-217">**Source app**: the application that loaded or executed content triggering the suspected attack activity.</span></span> <span data-ttu-id="4b41f-218">Il peut s’agir d’une application légitime, telle qu’un navigateur Web, une application Office ou un outil système tel que PowerShell</span><span class="sxs-lookup"><span data-stu-id="4b41f-218">It could be a legitimate application, such as web browser, an Office application, or a system tool like PowerShell</span></span>
* <span data-ttu-id="4b41f-219">**Publisher**: fournisseur qui a publié l’application source</span><span class="sxs-lookup"><span data-stu-id="4b41f-219">**Publisher**: the vendor that released the source app</span></span>

### <a name="review-device-asr-rule-settings"></a><span data-ttu-id="4b41f-220">Vérifier les paramètres de règle ASR de l’appareil</span><span class="sxs-lookup"><span data-stu-id="4b41f-220">Review device ASR rule settings</span></span>

<span data-ttu-id="4b41f-221">Dans la page rapport sur les règles de réduction de la **surface d’attaque** , accédez à l’onglet **configuration** pour vérifier les paramètres de règle pour les appareils individuels.</span><span class="sxs-lookup"><span data-stu-id="4b41f-221">In the **Attack surface reduction rules** report page, go to the **Configuration** tab to review rule settings for individual devices.</span></span> <span data-ttu-id="4b41f-222">Sélectionnez un appareil pour obtenir des informations détaillées sur la façon dont chaque règle est en mode bloquer, mode audit ou désactivé entièrement.</span><span class="sxs-lookup"><span data-stu-id="4b41f-222">Select a device to get detailed information about whether each rule is in block mode, audit mode, or turned off entirely.</span></span>

![Onglet Configuration](../../media/configuration-tab.png)

<span data-ttu-id="4b41f-224">Microsoft Intune offre des fonctionnalités de gestion pour vos règles de récupération automatique du système.</span><span class="sxs-lookup"><span data-stu-id="4b41f-224">Microsoft Intune provides management functionality for your ASR rules.</span></span> <span data-ttu-id="4b41f-225">Si vous souhaitez mettre à jour vos paramètres, sélectionnez **prise en main** sous configurer les **appareils** sous l’onglet pour ouvrir gestion des appareils sur Intune.</span><span class="sxs-lookup"><span data-stu-id="4b41f-225">If you want to update your settings, select **Get started** under **Configure devices** in the tab to open device management on Intune.</span></span>

### <a name="exclude-files-from-asr-rules"></a><span data-ttu-id="4b41f-226">Exclure les fichiers des règles ASR</span><span class="sxs-lookup"><span data-stu-id="4b41f-226">Exclude files from ASR rules</span></span>

<span data-ttu-id="4b41f-227">Le centre de sécurité Microsoft 365 recueille les noms des [fichiers que vous pouvez exclure](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/enable-attack-surface-reduction#exclude-files-and-folders-from-asr-rules) des détections par des règles de réduction de la surface d’attaque.</span><span class="sxs-lookup"><span data-stu-id="4b41f-227">Microsoft 365 security center collects the names of the [files you might want to exclude](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/enable-attack-surface-reduction#exclude-files-and-folders-from-asr-rules) from detections by attack surface reduction rules.</span></span> <span data-ttu-id="4b41f-228">En excluant des fichiers, vous pouvez réduire les faux positifs et déployer en toute confiance les règles de réduction de la surface d’attaque en mode bloc.</span><span class="sxs-lookup"><span data-stu-id="4b41f-228">By excluding files, you can reduce false positive detections and more confidently deploy attack surface reduction rules in block mode.</span></span>

<span data-ttu-id="4b41f-229">Les exclusions sont gérées sur Microsoft Intune, mais le centre de sécurité Microsoft 365 fournit un outil d’analyse pour vous aider à comprendre les fichiers.</span><span class="sxs-lookup"><span data-stu-id="4b41f-229">The exclusions are managed on Microsoft Intune, but Microsoft 365 security center provides an analysis tool to help you understand the files.</span></span> <span data-ttu-id="4b41f-230">Pour commencer à collecter des fichiers pour exclusion, accédez à l’onglet **Ajouter des exclusions** dans la page rapport des règles de réduction de la **surface d’attaque** .</span><span class="sxs-lookup"><span data-stu-id="4b41f-230">To start collecting files for exclusion, go to the **Add exclusions** tab in the **Attack surface reduction rules** report page.</span></span>

>[!NOTE]  
><span data-ttu-id="4b41f-231">L’outil analyse les détections par toutes les règles de réduction de la surface d’attaque, mais [seules certaines règles prennent en charge les exclusions](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/troubleshoot-asr).</span><span class="sxs-lookup"><span data-stu-id="4b41f-231">The tool analyzes detections by all attack surface reduction rules, but [only some rules support exclusions](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/troubleshoot-asr).</span></span>

![Onglet ajouter des exclusions](../../media/add-exclusions-tab.png)

<span data-ttu-id="4b41f-233">Le tableau répertorie tous les noms de fichiers détectés par les règles de réduction de la surface d’attaque.</span><span class="sxs-lookup"><span data-stu-id="4b41f-233">The table lists all the file names detected by your attack surface reduction rules.</span></span> <span data-ttu-id="4b41f-234">Vous pouvez sélectionner des fichiers pour vérifier l’impact de leur exclusion :</span><span class="sxs-lookup"><span data-stu-id="4b41f-234">You can select files to review the impact of excluding them:</span></span>

* <span data-ttu-id="4b41f-235">Nombre de détections moins nombreuses</span><span class="sxs-lookup"><span data-stu-id="4b41f-235">How many fewer detections</span></span>
* <span data-ttu-id="4b41f-236">Nombre d’appareils qui signalent les menaces détectées</span><span class="sxs-lookup"><span data-stu-id="4b41f-236">How many fewer devices report the detections</span></span>

<span data-ttu-id="4b41f-237">Pour obtenir la liste des fichiers sélectionnés avec leur chemin d’accès complet pour l’exclusion, sélectionnez **obtenir les chemins d’exclusion**.</span><span class="sxs-lookup"><span data-stu-id="4b41f-237">To get a list of the selected files with their full paths for exclusion, select **Get exclusion paths**.</span></span>

<span data-ttu-id="4b41f-238">Journaux pour le déchargement des **informations d’identification de blocage de règle ASR du sous-système de l’autorité de sécurité locale (lsass.exe) de Windows** capturez le **lsass.exe**de l’application source.</span><span class="sxs-lookup"><span data-stu-id="4b41f-238">Logs for the ASR rule **Block credential stealing from the Windows local security authority subsystem (lsass.exe)** capture the source app **lsass.exe**.</span></span> <span data-ttu-id="4b41f-239">Il s’agit d’un fichier système normal, mais capturé en tant que fichier détecté.</span><span class="sxs-lookup"><span data-stu-id="4b41f-239">It is a normal system file, but captured as the detected file.</span></span> <span data-ttu-id="4b41f-240">Par conséquent, la liste générée des chemins d’exclusion inclut ce fichier.</span><span class="sxs-lookup"><span data-stu-id="4b41f-240">As a result, the generated list of exclusion paths will include this file.</span></span> <span data-ttu-id="4b41f-241">Pour exclure le fichier qui a déclenché cette règle au lieu de **lsass.exe**, utilisez le chemin d’accès à l’application source au lieu du fichier détecté.</span><span class="sxs-lookup"><span data-stu-id="4b41f-241">To exclude the file that triggered this rule instead of **lsass.exe**, use the path to the source app instead of the detected file.</span></span>

<span data-ttu-id="4b41f-242">Pour localiser l’application source, exécutez la [requête de recherche avancée](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting) suivante pour cette règle spécifique (identifiée par l’ID de règle 9e6c4e1f-7d60-472f-bA1a-a39ef669e4b2) :</span><span class="sxs-lookup"><span data-stu-id="4b41f-242">To locate the source app, run the following [advanced hunting query](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/advanced-hunting) for this specific rule (identified by rule ID 9e6c4e1f-7d60-472f-ba1a-a39ef669e4b2):</span></span>

```kusto
DeviceEvents
| where Timestamp > ago(7d)
| where ActionType startswith "Asr"
| where AdditionalFields contains "9e6c4e1f-7d60-472f-ba1a-a39ef669e4b2"
| project InitiatingProcessFolderPath, InitiatingProcessFileName
```

#### <a name="check-files-for-exclusion"></a><span data-ttu-id="4b41f-243">Vérifier les fichiers pour exclusion</span><span class="sxs-lookup"><span data-stu-id="4b41f-243">Check files for exclusion</span></span>

<span data-ttu-id="4b41f-244">Avant d’exclure un fichier de la récupération automatique du système, nous vous recommandons d’inspecter le fichier afin de déterminer s’il n’est pas malveillant.</span><span class="sxs-lookup"><span data-stu-id="4b41f-244">Before excluding a file from ASR, we recommend that you inspect the file to determine if it's indeed not malicious.</span></span>

<span data-ttu-id="4b41f-245">Pour passer en revue un fichier, utilisez la [page informations](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/investigate-files) sur le fichier sur le centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="4b41f-245">To review a file, use the [file information page](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/investigate-files) on Microsoft Defender Security Center.</span></span> <span data-ttu-id="4b41f-246">La page fournit des informations de récurrence et le ratio de détection antivirus VirusTotal.</span><span class="sxs-lookup"><span data-stu-id="4b41f-246">The page provides prevalence information and the VirusTotal antivirus detection ratio.</span></span> <span data-ttu-id="4b41f-247">Vous pouvez également utiliser la page pour envoyer le fichier pour une analyse approfondie.</span><span class="sxs-lookup"><span data-stu-id="4b41f-247">You can also use the page to submit the file for deep analysis.</span></span>

<span data-ttu-id="4b41f-248">Pour rechercher un fichier détecté dans le centre de sécurité Microsoft Defender, recherchez toutes les détections de récupération automatique du système à l’aide de la requête de chasse avancée suivante :</span><span class="sxs-lookup"><span data-stu-id="4b41f-248">To locate a detected file in Microsoft Defender Security Center, search for all ASR detections using the following advanced hunting query:</span></span>

```kusto
MiscEvents
| where EventTime > ago(7d)
| where ActionType startswith "Asr"
| project FolderPath, FileName, SHA1, InitiatingProcessFolderPath, InitiatingProcessFileName, InitiatingProcessSHA1
```

<span data-ttu-id="4b41f-249">Utilisez **SHA1** ou le **InitiatingProcessSHA1** dans les résultats pour rechercher le fichier à l’aide de la barre de recherche universelle dans le centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="4b41f-249">Use the **SHA1** or the **InitiatingProcessSHA1** in the results to search for the file using the universal search bar in Microsoft Defender Security Center.</span></span>
