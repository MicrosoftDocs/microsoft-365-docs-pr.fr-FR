---
title: Microsoft Defender pour point de terminaison
description: Microsoft Defender pour point de terminaison est une plateforme de sécurité de point de terminaison d'entreprise qui permet de se défendre contre les menaces avancées persistantes.
keywords: introduction à Microsoft Defender pour point de terminaison, présentation de Microsoft Defender pour endpoint, cyber-sécurité, menace avancée persistante, sécurité d'entreprise, capteur de comportement ordinateur, sécurité cloud, analyse, veille contre les menaces, réduction de la surface d'attaque, protection nouvelle génération, investigation et correction automatisées, experts microsoft en matière de menaces, score de sécurité, recherche avancée, Microsoft 365 Defender, recherche de cybermenace
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
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 57d4506e32db5defe29f2d0e59f72bd4c1998310
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51935928"
---
# <a name="microsoft-defender-for-endpoint"></a><span data-ttu-id="29979-104">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="29979-104">Microsoft Defender for Endpoint</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="29979-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="29979-105">**Applies to:**</span></span>
- [<span data-ttu-id="29979-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="29979-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="29979-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="29979-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="29979-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="29979-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="29979-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="29979-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

> <span data-ttu-id="29979-110">Pour plus d'informations sur les fonctionnalités et fonctionnalités de Windows 10 Édition Entreprise, voir [Windows 10 Édition Entreprise.](https://www.microsoft.com/WindowsForBusiness/buy)</span><span class="sxs-lookup"><span data-stu-id="29979-110">For more info about Windows 10 Enterprise Edition features and functionality, see [Windows 10 Enterprise edition](https://www.microsoft.com/WindowsForBusiness/buy).</span></span>

<span data-ttu-id="29979-111">Microsoft Defender pour point de terminaison est une plateforme de sécurité de point de terminaison d'entreprise conçue pour aider les réseaux d'entreprise à prévenir, détecter, examiner et répondre aux menaces avancées.</span><span class="sxs-lookup"><span data-stu-id="29979-111">Microsoft Defender for Endpoint is an enterprise endpoint security platform designed to help enterprise networks prevent, detect, investigate, and respond to advanced threats.</span></span>
<p></p>

>[!VIDEO https://www.microsoft.com/videoplayer/embed/RE4wDob]

<span data-ttu-id="29979-112">Defender pour le point de terminaison utilise la combinaison de technologie suivante intégrée à Windows 10 et au service cloud robuste de Microsoft :</span><span class="sxs-lookup"><span data-stu-id="29979-112">Defender for Endpoint uses the following combination of technology built into Windows 10 and Microsoft's robust cloud service:</span></span>

-   <span data-ttu-id="29979-113">Capteurs comportementaux de point de terminaison : incorporés dans Windows 10, ces capteurs collectent et traitéent les signaux comportementaux du système d'exploitation et envoient ces données de capteur à votre instance privée, isolée et cloud de Microsoft Defender pour endpoint.</span><span class="sxs-lookup"><span data-stu-id="29979-113">**Endpoint behavioral sensors**: Embedded in Windows 10, these sensors collect and process behavioral signals from the operating system and send this sensor data to your private, isolated, cloud instance of Microsoft Defender for Endpoint.</span></span>


-   <span data-ttu-id="29979-114">Analyse de la sécurité cloud : tirant parti du Big Data, de l'apprentissage des appareils et de l'optique Microsoft unique dans l'écosystème Windows, des produits cloud d'entreprise (tels qu'Office 365) et des ressources en ligne, les signaux comportementaux sont convertis en analyses, détections et réponses recommandées aux menaces avancées.</span><span class="sxs-lookup"><span data-stu-id="29979-114">**Cloud security analytics**: Leveraging big-data, device-learning, and unique Microsoft optics across the Windows ecosystem, enterprise cloud products (such as Office 365), and online assets, behavioral signals are translated into insights, detections, and recommended responses to advanced threats.</span></span>

-   <span data-ttu-id="29979-115">Intelligence contre les menaces : générée par les chercheurs de Microsoft, les équipes de sécurité et renforcée par l'intelligence contre les menaces fournie par les partenaires, l'intelligence des menaces permet à Defender for Endpoint d'identifier les outils, techniques et procédures de l'attaquant et de générer des alertes lorsqu'elles sont observées dans les données de capteur collectées.</span><span class="sxs-lookup"><span data-stu-id="29979-115">**Threat intelligence**: Generated by Microsoft hunters, security teams, and augmented by threat intelligence provided by partners, threat intelligence enables Defender for Endpoint to identify attacker tools, techniques, and procedures, and generate alerts when they are observed in collected sensor data.</span></span>

<center><h2><span data-ttu-id="29979-116">Microsoft Defender pour point de terminaison</center></span><span class="sxs-lookup"><span data-stu-id="29979-116">Microsoft Defender for Endpoint</center></span></span></h2>
<table>
<tr>
<td><a href="#tvm"><center><img src="images/TVM_icon.png" alt="Threat & Vulnerability Management"> <br><span data-ttu-id="29979-117"><b>Gestion des & des menaces</b></center></a></span><span class="sxs-lookup"><span data-stu-id="29979-117"><b>Threat & Vulnerability Management</b></center></a></span></span></td>
<td><a href="#asr"><center><img src="images/asr-icon.png" alt="Attack surface reduction"><br><span data-ttu-id="29979-118"><b>Réduction de la surface d'attaque</b></center></a></span><span class="sxs-lookup"><span data-stu-id="29979-118"><b>Attack surface reduction</b></center></a></span></span></td>
<td><center><a href="#ngp"><img src="images/ngp-icon.png" alt="Next-generation protection"><br> <span data-ttu-id="29979-119"><b>Protection nouvelle génération</b></a></center></span><span class="sxs-lookup"><span data-stu-id="29979-119"><b>Next-generation protection</b></a></center></span></span></td>
<td><center><a href="#edr"><img src="images/edr-icon.png" alt="Endpoint detection and response"><br> <span data-ttu-id="29979-120"><b>Détection et réponse des points de terminaison</b></a></center></span><span class="sxs-lookup"><span data-stu-id="29979-120"><b>Endpoint detection and response</b></a></center></span></span></td>
<td><center><a href="#ai"><img src="images/air-icon.png" alt="Automated investigation and remediation"><br> <span data-ttu-id="29979-121"><b>Examen et correction automatisés</b></a></center></span><span class="sxs-lookup"><span data-stu-id="29979-121"><b>Automated investigation and remediation</b></a></center></span></span></td>
<td><center><a href="#mte"><img src="images/mte-icon.png" alt="Microsoft Threat Experts"><br> <span data-ttu-id="29979-122"><b>Experts microsoft en matière de menaces</b></a></center></span><span class="sxs-lookup"><span data-stu-id="29979-122"><b>Microsoft Threat Experts</b></a></center></span></span></td>
</tr>
<tr>
<td colspan="7"><span data-ttu-id="29979-123">
<a href="#apis"><center><b>Configuration et administration centralisées, API</a></span><span class="sxs-lookup"><span data-stu-id="29979-123">
<a href="#apis"><center><b>Centralized configuration and administration, APIs</a></span></span></b></center></td>
</tr>
<tr>
<td colspan="7"><span data-ttu-id="29979-124"><a href="#mtp"><center><b>Microsoft 365 Defender</a></span><span class="sxs-lookup"><span data-stu-id="29979-124"><a href="#mtp"><center><b>Microsoft 365 Defender</a></span></span></center></b></td>
</tr>
</table>
<br>

<p></p>

>[!VIDEO https://www.microsoft.com/videoplayer/embed/RE4vnC4?rel=0] 

> [!TIP]
> - <span data-ttu-id="29979-125">Découvrez les dernières améliorations de Defender pour point de terminaison : nouveautés de [Microsoft Defender pour point de terminaison.](https://cloudblogs.microsoft.com/microsoftsecure/2018/11/15/whats-new-in-windows-defender-atp/)</span><span class="sxs-lookup"><span data-stu-id="29979-125">Learn about the latest enhancements in Defender for Endpoint: [What's new in Microsoft Defender for Endpoint](https://cloudblogs.microsoft.com/microsoftsecure/2018/11/15/whats-new-in-windows-defender-atp/).</span></span>
> - <span data-ttu-id="29979-126">Microsoft Defender pour point de terminaison a fait la démonstration des fonctionnalités d'optique et de détection de pointe du secteur dans l'évaluation MITRE récente.</span><span class="sxs-lookup"><span data-stu-id="29979-126">Microsoft Defender for Endpoint demonstrated industry-leading optics and detection capabilities in the recent MITRE evaluation.</span></span> <span data-ttu-id="29979-127">Read: [Insights from the MITRE ATT&CK-based evaluation](https://cloudblogs.microsoft.com/microsoftsecure/2018/12/03/insights-from-the-mitre-attack-based-evaluation-of-windows-defender-atp/).</span><span class="sxs-lookup"><span data-stu-id="29979-127">Read: [Insights from the MITRE ATT&CK-based evaluation](https://cloudblogs.microsoft.com/microsoftsecure/2018/12/03/insights-from-the-mitre-attack-based-evaluation-of-windows-defender-atp/).</span></span>

<a name="tvm"></a>

<span data-ttu-id="29979-128">**[Gestion des & des menaces](next-gen-threat-and-vuln-mgt.md)**</span><span class="sxs-lookup"><span data-stu-id="29979-128">**[Threat & Vulnerability Management](next-gen-threat-and-vuln-mgt.md)**</span></span><br>
<span data-ttu-id="29979-129">Cette fonctionnalité intégrée utilise une approche basée sur les risques qui modifie le jeu pour la découverte, la hiér doncisation et la correction des vulnérabilités et des mauvaises configurations des points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="29979-129">This built-in capability uses a game-changing risk-based approach to the discovery, prioritization, and remediation of endpoint vulnerabilities and misconfigurations.</span></span> 

<a name="asr"></a>

<span data-ttu-id="29979-130">**[Réduction de la surface d’attaque](overview-attack-surface-reduction.md)**</span><span class="sxs-lookup"><span data-stu-id="29979-130">**[Attack surface reduction](overview-attack-surface-reduction.md)**</span></span><br>
<span data-ttu-id="29979-131">L'ensemble de fonctionnalités de réduction de la surface d'attaque fournit la première ligne de défense dans la pile.</span><span class="sxs-lookup"><span data-stu-id="29979-131">The attack surface reduction set of capabilities provides the first line of defense in the stack.</span></span> <span data-ttu-id="29979-132">En s'assurant que les paramètres de configuration sont correctement définies et que des techniques d'atténuation des attaques sont appliquées, les fonctionnalités résistant aux attaques et à l'exploitation.</span><span class="sxs-lookup"><span data-stu-id="29979-132">By ensuring configuration settings are properly set and exploit mitigation techniques are applied, the capabilities resist attacks and exploitation.</span></span> <span data-ttu-id="29979-133">Cet ensemble de fonctionnalités inclut également la [protection](network-protection.md) réseau et [la protection web,](web-protection-overview.md)qui régulent l'accès aux adresses IP, domaines et URL malveillants.</span><span class="sxs-lookup"><span data-stu-id="29979-133">This set of capabilities also includes [network protection](network-protection.md) and [web protection](web-protection-overview.md), which regulate access to malicious IP addresses, domains, and URLs.</span></span> 

<a name="ngp"></a>

<span data-ttu-id="29979-134">**[Protection de nouvelle génération](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/microsoft-defender-antivirus-in-windows-10)**</span><span class="sxs-lookup"><span data-stu-id="29979-134">**[Next-generation protection](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/microsoft-defender-antivirus-in-windows-10)**</span></span><br>
<span data-ttu-id="29979-135">Pour renforcer davantage le périmètre de sécurité de votre réseau, Microsoft Defender pour Endpoint utilise une protection nouvelle génération conçue pour capturer tous les types de menaces émergentes.</span><span class="sxs-lookup"><span data-stu-id="29979-135">To further reinforce the security perimeter of your network, Microsoft Defender for Endpoint uses next-generation protection designed to catch all types of emerging threats.</span></span>

<a name="edr"></a>

<span data-ttu-id="29979-136">**[Détection et réponse du point de terminaison](overview-endpoint-detection-response.md)**</span><span class="sxs-lookup"><span data-stu-id="29979-136">**[Endpoint detection and response](overview-endpoint-detection-response.md)**</span></span><br>
<span data-ttu-id="29979-137">Des fonctionnalités de détection et de réponse de point de terminaison sont mises en place pour détecter, examiner et répondre aux menaces avancées qui ont peut-être passé les deux premiers piliers de sécurité.</span><span class="sxs-lookup"><span data-stu-id="29979-137">Endpoint detection and response capabilities are put in place to detect, investigate, and respond to advanced threats that may have made it past the first two security pillars.</span></span> <span data-ttu-id="29979-138">[Le repérage avancé](advanced-hunting-overview.md) fournit un outil de repérage de menaces basé sur une requête qui vous permet de rechercher de manière proactive les violations et de créer des détections personnalisées.</span><span class="sxs-lookup"><span data-stu-id="29979-138">[Advanced hunting](advanced-hunting-overview.md) provides a query-based threat-hunting tool that lets you proactively find breaches and create custom detections.</span></span>

<a name="ai"></a>

<span data-ttu-id="29979-139">**[Examen et correction automatisés](automated-investigations.md)**</span><span class="sxs-lookup"><span data-stu-id="29979-139">**[Automated investigation and remediation](automated-investigations.md)**</span></span><br>
<span data-ttu-id="29979-140">En plus de pouvoir répondre rapidement aux attaques avancées, Microsoft Defender pour point de terminaison offre des fonctionnalités d'examen et de correction automatiques qui permettent de réduire le volume d'alertes en minutes à l'échelle.</span><span class="sxs-lookup"><span data-stu-id="29979-140">In conjunction with being able to quickly respond to advanced attacks, Microsoft Defender for Endpoint offers automatic investigation and remediation capabilities that help reduce the volume of alerts in minutes at scale.</span></span> 

<a name="ss"></a>

<span data-ttu-id="29979-141">**[Niveau de sécurité Microsoft pour les appareils](tvm-microsoft-secure-score-devices.md)**</span><span class="sxs-lookup"><span data-stu-id="29979-141">**[Microsoft Secure Score for Devices](tvm-microsoft-secure-score-devices.md)**</span></span><br>

<span data-ttu-id="29979-142">Defender pour le point de terminaison inclut le Niveau de sécurité Microsoft pour les appareils pour vous aider à évaluer dynamiquement l'état de sécurité de votre réseau d'entreprise, à identifier les systèmes non protégés et à prendre les mesures recommandées pour améliorer la sécurité globale de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="29979-142">Defender for Endpoint includes Microsoft Secure Score for Devices to help you dynamically assess the security state of your enterprise network, identify unprotected systems, and take recommended actions to improve the overall security of your organization.</span></span>

<a name="mte"></a>

<span data-ttu-id="29979-143">**[Spécialistes des menaces Microsoft](microsoft-threat-experts.md)**</span><span class="sxs-lookup"><span data-stu-id="29979-143">**[Microsoft Threat Experts](microsoft-threat-experts.md)**</span></span><br>
<span data-ttu-id="29979-144">Le nouveau service de recherche de menaces gérées de Microsoft Defender pour point de terminaison fournit une recherche proactive, la hiérquage, ainsi que des contextes et des informations supplémentaires qui permettent aux centres d'opérations de sécurité (SOC) d'identifier et de répondre aux menaces rapidement et avec précision.</span><span class="sxs-lookup"><span data-stu-id="29979-144">Microsoft Defender for Endpoint's new managed threat hunting service provides proactive hunting, prioritization, and additional context and insights that further empower Security operation centers (SOCs) to identify and respond to threats quickly and accurately.</span></span>

>[!IMPORTANT]
><span data-ttu-id="29979-145">Les clients Defender pour les points de terminaison doivent demander au service de recherche de menace géré par les experts en menaces Microsoft de recevoir des notifications d'attaques ciblées proactives et de collaborer avec des experts à la demande.</span><span class="sxs-lookup"><span data-stu-id="29979-145">Defender for Endpoint customers need to apply for the Microsoft Threat Experts managed threat hunting service to get proactive Targeted Attack Notifications and to collaborate with experts on demand.</span></span> <span data-ttu-id="29979-146">Experts à la demande est un service de modules.</span><span class="sxs-lookup"><span data-stu-id="29979-146">Experts on Demand is an add-on service.</span></span> <span data-ttu-id="29979-147">Les notifications d'attaques ciblées sont toujours incluses une fois que vous avez été accepté dans le service de recherche de menace géré par les experts microsoft en matière de menaces.</span><span class="sxs-lookup"><span data-stu-id="29979-147">Targeted Attack Notifications are always included after you have been accepted into Microsoft Threat Experts managed threat hunting service.</span></span><p>
><p><span data-ttu-id="29979-148">Si vous n'êtes pas encore inscrit et que vous souhaitez profiter de ses avantages, voir Paramètres généraux Avancés > <b></b> > <b>fonctionnalités</b> > <b>Microsoft Threat Experts</b> à appliquer. <b></b></span><span class="sxs-lookup"><span data-stu-id="29979-148">If you are not enrolled yet and would like to experience its benefits, go to <b>Settings</b> > <b>General</b> > <b>Advanced features</b> > <b>Microsoft Threat Experts</b> to apply.</span></span> <span data-ttu-id="29979-149">Une fois accepté, vous bénéficiez des avantages des notifications d'attaque ciblée et démarrez une version d'essai de 90 jours d'Experts à la demande.</span><span class="sxs-lookup"><span data-stu-id="29979-149">Once accepted, you will get the benefits of Targeted Attack Notifications, and start a  90-day trial of Experts on Demand.</span></span> <span data-ttu-id="29979-150">Contactez votre représentant Microsoft pour obtenir un abonnement Experts à la demande complet.</span><span class="sxs-lookup"><span data-stu-id="29979-150">Contact your Microsoft representative to get a full Experts on Demand subscription.</span></span>

<a name="apis"></a>

<span data-ttu-id="29979-151">**[Configuration et administration centralisées, API](management-apis.md)**</span><span class="sxs-lookup"><span data-stu-id="29979-151">**[Centralized configuration and administration, APIs](management-apis.md)**</span></span><br>
<span data-ttu-id="29979-152">Intégrez Microsoft Defender for Endpoint à vos flux de travail existants.</span><span class="sxs-lookup"><span data-stu-id="29979-152">Integrate Microsoft Defender for Endpoint into your existing workflows.</span></span>

<a name="mtp"></a>

<span data-ttu-id="29979-153">**[Intégration aux solutions Microsoft](threat-protection-integration.md)**</span><span class="sxs-lookup"><span data-stu-id="29979-153">**[Integration with Microsoft solutions](threat-protection-integration.md)**</span></span> <br>
<span data-ttu-id="29979-154">Defender pour le point de terminaison s'intègre directement à différentes solutions Microsoft, notamment :</span><span class="sxs-lookup"><span data-stu-id="29979-154">Defender for Endpoint directly integrates with various Microsoft solutions, including:</span></span>
- <span data-ttu-id="29979-155">Azure Defender</span><span class="sxs-lookup"><span data-stu-id="29979-155">Azure Defender</span></span>
- <span data-ttu-id="29979-156">Azure Sentinel</span><span class="sxs-lookup"><span data-stu-id="29979-156">Azure Sentinel</span></span>
- <span data-ttu-id="29979-157">Intune</span><span class="sxs-lookup"><span data-stu-id="29979-157">Intune</span></span>
- <span data-ttu-id="29979-158">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="29979-158">Microsoft Cloud App Security</span></span>
- <span data-ttu-id="29979-159">Microsoft Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="29979-159">Microsoft Defender for Identity</span></span>
- <span data-ttu-id="29979-160">Microsoft Defender pour Office</span><span class="sxs-lookup"><span data-stu-id="29979-160">Microsoft Defender for Office</span></span>
- <span data-ttu-id="29979-161">Skype Entreprise</span><span class="sxs-lookup"><span data-stu-id="29979-161">Skype for Business</span></span>

<span data-ttu-id="29979-162">**[Microsoft 365 Defender](https://docs.microsoft.com/microsoft-365/security/defender/microsoft-threat-protection)**</span><span class="sxs-lookup"><span data-stu-id="29979-162">**[Microsoft 365 Defender](https://docs.microsoft.com/microsoft-365/security/defender/microsoft-threat-protection)**</span></span><br>
<span data-ttu-id="29979-163">Avec Microsoft 365 Defender, Defender pour le point de terminaison et diverses solutions de sécurité Microsoft constituent une suite de défense d'entreprise unifiée avant et après la violation qui s'intègre en mode natif à travers le point de terminaison, l'identité, le courrier électronique et les applications pour détecter, empêcher, examiner et répondre automatiquement aux attaques sophistiquées.</span><span class="sxs-lookup"><span data-stu-id="29979-163">With Microsoft 365 Defender, Defender for Endpoint and various Microsoft security solutions form a unified pre- and post-breach enterprise defense suite that natively integrates across endpoint, identity, email, and applications to detect, prevent, investigate, and automatically respond to sophisticated attacks.</span></span>


## <a name="related-topic"></a><span data-ttu-id="29979-164">Rubrique connexe</span><span class="sxs-lookup"><span data-stu-id="29979-164">Related topic</span></span>
[<span data-ttu-id="29979-165">Microsoft Defender pour point de terminaison permet de détecter les menaces sophistiquées</span><span class="sxs-lookup"><span data-stu-id="29979-165">Microsoft Defender for Endpoint helps detect sophisticated threats</span></span>](https://www.microsoft.com/itshowcase/microsoft-defender-atps-antivirus-capabilities-boost-malware-protection)
