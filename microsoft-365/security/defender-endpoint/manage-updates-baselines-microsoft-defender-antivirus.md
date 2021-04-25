---
title: Gérer les mises à jour de l'Antivirus Microsoft Defender et appliquer les lignes de base
description: Gérer la façon dont l'Antivirus Microsoft Defender reçoit la protection et les mises à jour du produit.
keywords: mises à jour, bases de référence de sécurité, protection, planification des mises à jour, forcer les mises à jour, mises à jour mobiles, wsus
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: normal
audience: ITPro
ms.topic: article
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.reviewer: pahuijbr
manager: dansimp
ms.technology: mde
ms.openlocfilehash: ae17aa6e2cb0cefd460ef0db0730570af8c84bb8
ms.sourcegitcommit: f000358c01a8006e5749a86b256300ee3a73174c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2021
ms.locfileid: "51995032"
---
# <a name="manage-microsoft-defender-antivirus-updates-and-apply-baselines"></a><span data-ttu-id="532fe-104">Gérer les mises à jour de l'Antivirus Microsoft Defender et appliquer les lignes de base</span><span class="sxs-lookup"><span data-stu-id="532fe-104">Manage Microsoft Defender Antivirus updates and apply baselines</span></span>

<span data-ttu-id="532fe-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="532fe-105">**Applies to:**</span></span>

- [<span data-ttu-id="532fe-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="532fe-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)
- <span data-ttu-id="532fe-107">Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="532fe-107">Microsoft Defender Antivirus</span></span>

<span data-ttu-id="532fe-108">Il existe deux types de mises à jour liées à la mise à jour de l'Antivirus Microsoft Defender :</span><span class="sxs-lookup"><span data-stu-id="532fe-108">There are two types of updates related to keeping Microsoft Defender Antivirus up to date:</span></span>

- <span data-ttu-id="532fe-109">Mises à jour de l'intelligence de la sécurité</span><span class="sxs-lookup"><span data-stu-id="532fe-109">Security intelligence updates</span></span>
- <span data-ttu-id="532fe-110">Mises à jour de produit</span><span class="sxs-lookup"><span data-stu-id="532fe-110">Product updates</span></span>

> [!IMPORTANT]
> <span data-ttu-id="532fe-111">Maintenir l'Antivirus Microsoft Defender à jour est essentiel pour garantir que vos appareils disposent des dernières technologies et fonctionnalités nécessaires pour se protéger contre les nouveaux programmes malveillants et les nouvelles techniques d'attaque.</span><span class="sxs-lookup"><span data-stu-id="532fe-111">Keeping Microsoft Defender Antivirus up to date is critical to assure your devices have the latest technology and features needed to protect against new malware and attack techniques.</span></span>
> 
> <span data-ttu-id="532fe-112">Veillez à mettre à jour votre protection antivirus même si l'Antivirus Microsoft Defender s'exécute en [mode passif.](./microsoft-defender-antivirus-compatibility.md)</span><span class="sxs-lookup"><span data-stu-id="532fe-112">Make sure to update your antivirus protection even if Microsoft Defender Antivirus is running in [passive mode](./microsoft-defender-antivirus-compatibility.md).</span></span>
> 
> <span data-ttu-id="532fe-113">Pour voir le moteur, la plateforme et la date de signature les plus à jour, consultez les mises à jour de l'Intelligence de sécurité pour l'Antivirus Microsoft Defender et d'autres logiciels [anti-programme malveillant Microsoft.](https://www.microsoft.com/en-us/wdsi/defenderupdates)</span><span class="sxs-lookup"><span data-stu-id="532fe-113">To see the most current engine, platform, and signature date, visit the [Security intelligence updates for Microsoft Defender Antivirus and other Microsoft antimalware](https://www.microsoft.com/en-us/wdsi/defenderupdates).</span></span>

## <a name="security-intelligence-updates"></a><span data-ttu-id="532fe-114">Mises à jour de l'intelligence de la sécurité</span><span class="sxs-lookup"><span data-stu-id="532fe-114">Security intelligence updates</span></span>

<span data-ttu-id="532fe-115">L'Antivirus Microsoft Defender utilise la protection fournie par le [cloud](cloud-protection-microsoft-defender-antivirus.md) (également appelée Service de protection avancée Microsoft ou MAPS) et télécharge régulièrement les mises à jour de l'intelligence de sécurité pour fournir une protection.</span><span class="sxs-lookup"><span data-stu-id="532fe-115">Microsoft Defender Antivirus uses [cloud-delivered protection](cloud-protection-microsoft-defender-antivirus.md) (also called the Microsoft Advanced Protection Service or MAPS) and periodically downloads security intelligence updates to provide protection.</span></span>

> [!NOTE]
> <span data-ttu-id="532fe-116">Les mises à jour sont publiées sous les numéros de la Ko ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="532fe-116">Updates are released under the below KB numbers:</span></span>  
> <span data-ttu-id="532fe-117">Antivirus Microsoft Defender : KB2267602</span><span class="sxs-lookup"><span data-stu-id="532fe-117">Microsoft Defender Antivirus: KB2267602</span></span>  
> <span data-ttu-id="532fe-118">System Center Endpoint Protection : KB2461484</span><span class="sxs-lookup"><span data-stu-id="532fe-118">System Center Endpoint Protection: KB2461484</span></span>

<span data-ttu-id="532fe-119">La protection cloud est toujours active et nécessite une connexion active à Internet pour fonctionner.</span><span class="sxs-lookup"><span data-stu-id="532fe-119">Cloud-delivered protection is always on and requires an active connection to the Internet to function.</span></span> <span data-ttu-id="532fe-120">Les mises à jour des informations de sécurité se produisent à une cadence programmée (configurable via une stratégie).</span><span class="sxs-lookup"><span data-stu-id="532fe-120">Security intelligence updates occur on a scheduled cadence (configurable via policy).</span></span> <span data-ttu-id="532fe-121">Pour plus d'informations, voir Utiliser la protection fournie par le [cloud Microsoft dans l'Antivirus Microsoft Defender.](cloud-protection-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="532fe-121">For more information, see [Use Microsoft cloud-provided protection in Microsoft Defender Antivirus](cloud-protection-microsoft-defender-antivirus.md).</span></span> 

<span data-ttu-id="532fe-122">Pour obtenir la liste des mises à jour récentes de l'intelligence de sécurité, voir Les mises à jour d'intelligence de sécurité pour l'Antivirus Microsoft Defender et d'autres logiciels [anti-programme](https://www.microsoft.com/en-us/wdsi/defenderupdates)malveillant Microsoft.</span><span class="sxs-lookup"><span data-stu-id="532fe-122">For a list of recent security intelligence updates, see [Security intelligence updates for Microsoft Defender Antivirus and other Microsoft antimalware](https://www.microsoft.com/en-us/wdsi/defenderupdates).</span></span>

<span data-ttu-id="532fe-123">Les mises à jour du moteur sont incluses dans les mises à jour de l'intelligence de sécurité et sont publiées à une cadence mensuelle.</span><span class="sxs-lookup"><span data-stu-id="532fe-123">Engine updates are included with security intelligence updates and are released on a monthly cadence.</span></span>

## <a name="product-updates"></a><span data-ttu-id="532fe-124">Mises à jour de produit</span><span class="sxs-lookup"><span data-stu-id="532fe-124">Product updates</span></span>

<span data-ttu-id="532fe-125">L'Antivirus Microsoft Defender nécessite des mises à jour [mensuelles (KB4052623)](https://support.microsoft.com/help/4052623/update-for-windows-defender-antimalware-platform) *(connues* sous le nom de mises à jour de plateforme) et recevra des mises à jour de fonctionnalités majeures parallèlement aux mises à jour de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="532fe-125">Microsoft Defender Antivirus requires [monthly updates (KB4052623)](https://support.microsoft.com/help/4052623/update-for-windows-defender-antimalware-platform) (known as *platform updates*), and will receive major feature updates alongside Windows 10 releases.</span></span>

<span data-ttu-id="532fe-126">Vous pouvez gérer la distribution des mises à jour via l'une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="532fe-126">You can manage the distribution of updates through one of the following methods:</span></span> 

- [<span data-ttu-id="532fe-127">Windows Server Update Service (WSUS)</span><span class="sxs-lookup"><span data-stu-id="532fe-127">Windows Server Update Service (WSUS)</span></span>](/mem/configmgr/protect/deploy-use/endpoint-definitions-wsus#to-synchronize-endpoint-protection-definition-updates-in-standalone-wsus)
- [<span data-ttu-id="532fe-128">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="532fe-128">Microsoft Endpoint Configuration Manager</span></span>](/configmgr/sum/understand/software-updates-introduction)
- <span data-ttu-id="532fe-129">La méthode habituelle que vous utilisez pour déployer les mises à jour Microsoft et Windows sur les points de terminaison de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="532fe-129">The usual method you use to deploy Microsoft and Windows updates to endpoints in your network.</span></span>

<span data-ttu-id="532fe-130">Pour plus d'informations, voir Gérer les sources des mises à [jour de l'Antivirus Microsoft Defender.](/mem/configmgr/protect/deploy-use/endpoint-definitions-wsus#to-synchronize-endpoint-protection-definition-updates-in-standalone-wsus)</span><span class="sxs-lookup"><span data-stu-id="532fe-130">For more information, see [Manage the sources for Microsoft Defender Antivirus protection updates](/mem/configmgr/protect/deploy-use/endpoint-definitions-wsus#to-synchronize-endpoint-protection-definition-updates-in-standalone-wsus).</span></span>

> [!NOTE]
> <span data-ttu-id="532fe-131">Les mises à jour mensuelles sont publiées par phases, ce qui entraîne la mise à jour de plusieurs packages dans vos services de mise à jour [de serveur Window.](/windows-server/administration/windows-server-update-services/get-started/windows-server-update-services-wsus)</span><span class="sxs-lookup"><span data-stu-id="532fe-131">Monthly updates are released in phases, resulting in multiple packages visible in your [Window Server Update Services](/windows-server/administration/windows-server-update-services/get-started/windows-server-update-services-wsus).</span></span>

## <a name="monthly-platform-and-engine-versions"></a><span data-ttu-id="532fe-132">Versions mensuelles de la plateforme et du moteur</span><span class="sxs-lookup"><span data-stu-id="532fe-132">Monthly platform and engine versions</span></span>

<span data-ttu-id="532fe-133">Pour plus d'informations sur la mise à jour ou l'installation de la mise à jour de la plateforme, voir [Update for Windows Defender antimalware platform](https://support.microsoft.com/help/4052623/update-for-windows-defender-antimalware-platform).</span><span class="sxs-lookup"><span data-stu-id="532fe-133">For information how to update or install the platform update, see [Update for Windows Defender antimalware platform](https://support.microsoft.com/help/4052623/update-for-windows-defender-antimalware-platform).</span></span>

<span data-ttu-id="532fe-134">Toutes nos mises à jour contiennent</span><span class="sxs-lookup"><span data-stu-id="532fe-134">All our updates contain</span></span> 
- <span data-ttu-id="532fe-135">améliorations des performances ;</span><span class="sxs-lookup"><span data-stu-id="532fe-135">performance improvements;</span></span>
- <span data-ttu-id="532fe-136">améliorations en matière de serviceabilité ; et</span><span class="sxs-lookup"><span data-stu-id="532fe-136">serviceability improvements; and</span></span> 
- <span data-ttu-id="532fe-137">améliorations de l'intégration (Cloud, Microsoft 365 Defender).</span><span class="sxs-lookup"><span data-stu-id="532fe-137">integration improvements (Cloud, Microsoft 365 Defender).</span></span>
<br/><br/>

<details>
<summary> <span data-ttu-id="532fe-138">Mars-2021 (plateforme : 4.18.2103.7 | Moteur : 1.1.18000.5)</span><span class="sxs-lookup"><span data-stu-id="532fe-138">March-2021 (Platform: 4.18.2103.7 | Engine: 1.1.18000.5)</span></span></summary>

<span data-ttu-id="532fe-139">&ensp;Version de mise à jour des informations de sécurité **: 1.335.36.0**</span><span class="sxs-lookup"><span data-stu-id="532fe-139">&ensp;Security intelligence update version: **1.335.36.0**</span></span>  
<span data-ttu-id="532fe-140">&ensp;Publication : **1er avril 2021**</span><span class="sxs-lookup"><span data-stu-id="532fe-140">&ensp;Released: **April 1, 2021**</span></span>  
<span data-ttu-id="532fe-141">&ensp;Plateforme : **4.19.2103.7**</span><span class="sxs-lookup"><span data-stu-id="532fe-141">&ensp;Platform: **4.19.2103.7**</span></span>  
<span data-ttu-id="532fe-142">&ensp;Moteur : **1.1.18000.5**</span><span class="sxs-lookup"><span data-stu-id="532fe-142">&ensp;Engine: **1.1.18000.5**</span></span>  
<span data-ttu-id="532fe-143">&ensp;Phase de prise en charge **: Mises à jour critiques et de sécurité**</span><span class="sxs-lookup"><span data-stu-id="532fe-143">&ensp;Support phase: **Security and Critical Updates**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="532fe-144">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="532fe-144">What's new</span></span>

- <span data-ttu-id="532fe-145">Amélioration du moteur d'analyse du comportement</span><span class="sxs-lookup"><span data-stu-id="532fe-145">Improvement to the Behavior Monitoring engine</span></span> 
- <span data-ttu-id="532fe-146">Préventions d'attaques par force brute du réseau étendu</span><span class="sxs-lookup"><span data-stu-id="532fe-146">Expanded network brute-force-attack mitigations</span></span> 
- <span data-ttu-id="532fe-147">Génération d'événements de tentative de falsification en échec supplémentaires lorsque la [protection](prevent-changes-to-security-settings-with-tamper-protection.md) contre la falsification est activée</span><span class="sxs-lookup"><span data-stu-id="532fe-147">Additional failed tampering attempt event generation when [Tamper Protection](prevent-changes-to-security-settings-with-tamper-protection.md) is enabled</span></span>

### <a name="known-issues"></a><span data-ttu-id="532fe-148">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="532fe-148">Known Issues</span></span>
<span data-ttu-id="532fe-149">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="532fe-149">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="532fe-150">Février-2021 (plateforme : 4.18.2102.3 | Moteur : 1.1.17900.7)</span><span class="sxs-lookup"><span data-stu-id="532fe-150">February-2021 (Platform: 4.18.2102.3 | Engine: 1.1.17900.7)</span></span></summary>

<span data-ttu-id="532fe-151">&ensp;Version de mise à jour des informations de sécurité **: 1.333.7.0**</span><span class="sxs-lookup"><span data-stu-id="532fe-151">&ensp;Security intelligence update version: **1.333.7.0**</span></span>  
<span data-ttu-id="532fe-152">&ensp;Publication : **9 mars 2021**</span><span class="sxs-lookup"><span data-stu-id="532fe-152">&ensp;Released: **March 9, 2021**</span></span>  
<span data-ttu-id="532fe-153">&ensp;Plateforme : **4.19.2102.3**</span><span class="sxs-lookup"><span data-stu-id="532fe-153">&ensp;Platform: **4.19.2102.3**</span></span>  
<span data-ttu-id="532fe-154">&ensp;Moteur : **1.1.17900.7**</span><span class="sxs-lookup"><span data-stu-id="532fe-154">&ensp;Engine: **1.1.17900.7**</span></span>  
<span data-ttu-id="532fe-155">&ensp;Phase de prise en charge **: Mises à jour critiques et de sécurité**</span><span class="sxs-lookup"><span data-stu-id="532fe-155">&ensp;Support phase: **Security and Critical Updates**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="532fe-156">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="532fe-156">What's new</span></span>

- <span data-ttu-id="532fe-157">Amélioration de la récupération du service par le biais [de la protection contre la falsification](prevent-changes-to-security-settings-with-tamper-protection.md)</span><span class="sxs-lookup"><span data-stu-id="532fe-157">Improved service recovery through [tamper protection](prevent-changes-to-security-settings-with-tamper-protection.md)</span></span>
- <span data-ttu-id="532fe-158">Étendre l'étendue de la protection contre la falsification</span><span class="sxs-lookup"><span data-stu-id="532fe-158">Extend tamper protection scope</span></span>

### <a name="known-issues"></a><span data-ttu-id="532fe-159">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="532fe-159">Known Issues</span></span>
<span data-ttu-id="532fe-160">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="532fe-160">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="532fe-161">Janvier-2021 (plateforme : 4.18.2101.9 | Moteur : 1.1.17800.5)</span><span class="sxs-lookup"><span data-stu-id="532fe-161">January-2021 (Platform: 4.18.2101.9 | Engine: 1.1.17800.5)</span></span></summary>

<span data-ttu-id="532fe-162">&ensp;Version de mise à jour des informations de sécurité **: 1.327.1854.0**</span><span class="sxs-lookup"><span data-stu-id="532fe-162">&ensp;Security intelligence update version: **1.327.1854.0**</span></span>  
<span data-ttu-id="532fe-163">&ensp;Publication : **2 février 2021**</span><span class="sxs-lookup"><span data-stu-id="532fe-163">&ensp;Released: **February 2, 2021**</span></span>  
<span data-ttu-id="532fe-164">&ensp;Plateforme : **4.18.2101.9**</span><span class="sxs-lookup"><span data-stu-id="532fe-164">&ensp;Platform: **4.18.2101.9**</span></span>  
<span data-ttu-id="532fe-165">&ensp;Moteur : **1.1.17800.5**</span><span class="sxs-lookup"><span data-stu-id="532fe-165">&ensp;Engine: **1.1.17800.5**</span></span>  
<span data-ttu-id="532fe-166">&ensp;Phase de prise en charge **: Mises à jour critiques et de sécurité**</span><span class="sxs-lookup"><span data-stu-id="532fe-166">&ensp;Support phase: **Security and Critical Updates**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="532fe-167">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="532fe-167">What's new</span></span>

- <span data-ttu-id="532fe-168">Améliorations de la détection d'exploits shellcode</span><span class="sxs-lookup"><span data-stu-id="532fe-168">Shellcode exploit detection improvements</span></span>
- <span data-ttu-id="532fe-169">Visibilité accrue des tentatives de vol d'informations d'identification</span><span class="sxs-lookup"><span data-stu-id="532fe-169">Increased visibility for credential stealing attempts</span></span>
- <span data-ttu-id="532fe-170">Améliorations des fonctionnalités anti-virus dans les services antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="532fe-170">Improvements in antitampering features in Microsoft Defender Antivirus services</span></span>
- <span data-ttu-id="532fe-171">Prise en charge améliorée de l ARM éulation x64</span><span class="sxs-lookup"><span data-stu-id="532fe-171">Improved support for ARM x64 emulation</span></span>
- <span data-ttu-id="532fe-172">Correctif : les notifications de blocage EDR restent dans l'historique des menaces après la détection initiale de la protection en temps réel</span><span class="sxs-lookup"><span data-stu-id="532fe-172">Fix: EDR Block notification remains in threat history after real-time protection performed initial detection</span></span>

### <a name="known-issues"></a><span data-ttu-id="532fe-173">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="532fe-173">Known Issues</span></span>
<span data-ttu-id="532fe-174">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="532fe-174">No known issues</span></span>  
<br/>
</details>

### <a name="previous-version-updates-technical-upgrade-support-only"></a><span data-ttu-id="532fe-175">Mises à jour de version précédente : prise en charge de la mise à niveau technique uniquement</span><span class="sxs-lookup"><span data-stu-id="532fe-175">Previous version updates: Technical upgrade support only</span></span>

<span data-ttu-id="532fe-176">Après la publication d'une nouvelle version de package, la prise en charge des deux versions précédentes est réduite au support technique uniquement.</span><span class="sxs-lookup"><span data-stu-id="532fe-176">After a new package version is released, support for the previous two versions is reduced to technical support only.</span></span> <span data-ttu-id="532fe-177">Les versions antérieures à celles répertoriées dans cette section sont fournies uniquement pour la prise en charge de la mise à niveau technique.</span><span class="sxs-lookup"><span data-stu-id="532fe-177">Versions older than that are listed in this section, and are provided for technical upgrade support only.</span></span> 
<br/><br/>
<details>
<summary> <span data-ttu-id="532fe-178">Novembre-2020 (plateforme : 4.18.2011.6 | Moteur : 1.1.17700.4)</span><span class="sxs-lookup"><span data-stu-id="532fe-178">November-2020 (Platform: 4.18.2011.6 | Engine: 1.1.17700.4)</span></span></summary>

<span data-ttu-id="532fe-179">&ensp;Version de mise à jour des informations de sécurité **: 1.327.1854.0**</span><span class="sxs-lookup"><span data-stu-id="532fe-179">&ensp;Security intelligence update version: **1.327.1854.0**</span></span>  
<span data-ttu-id="532fe-180">&ensp;Publication : **03 décembre 2020**</span><span class="sxs-lookup"><span data-stu-id="532fe-180">&ensp;Released: **December 03, 2020**</span></span>  
<span data-ttu-id="532fe-181">&ensp;Plateforme : **4.18.2011.6**</span><span class="sxs-lookup"><span data-stu-id="532fe-181">&ensp;Platform: **4.18.2011.6**</span></span>  
<span data-ttu-id="532fe-182">&ensp;Moteur : **1.1.17700.4**</span><span class="sxs-lookup"><span data-stu-id="532fe-182">&ensp;Engine: **1.1.17700.4**</span></span>  
<span data-ttu-id="532fe-183">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="532fe-183">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="532fe-184">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="532fe-184">What's new</span></span>

- <span data-ttu-id="532fe-185">Amélioration de la [journalisation de la prise en](/windows/security/threat-protection/microsoft-defender-smartscreen/microsoft-defender-smartscreen-overview) charge de l'état SmartScreen</span><span class="sxs-lookup"><span data-stu-id="532fe-185">Improved [SmartScreen](/windows/security/threat-protection/microsoft-defender-smartscreen/microsoft-defender-smartscreen-overview) status support logging</span></span>

### <a name="known-issues"></a><span data-ttu-id="532fe-186">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="532fe-186">Known Issues</span></span>
<span data-ttu-id="532fe-187">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="532fe-187">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="532fe-188">Octobre-2020 (plateforme : 4.18.2010.7 | Moteur : 1.1.17600.5)</span><span class="sxs-lookup"><span data-stu-id="532fe-188">October-2020 (Platform: 4.18.2010.7 | Engine: 1.1.17600.5)</span></span></summary>

<span data-ttu-id="532fe-189">&ensp;Version de mise à jour des informations de sécurité **: 1.327.7.0**</span><span class="sxs-lookup"><span data-stu-id="532fe-189">&ensp;Security intelligence update version: **1.327.7.0**</span></span>  
<span data-ttu-id="532fe-190">&ensp;Publication : **29 octobre 2020**</span><span class="sxs-lookup"><span data-stu-id="532fe-190">&ensp;Released: **October 29, 2020**</span></span>  
<span data-ttu-id="532fe-191">&ensp;Plateforme : **4.18.2010.7**</span><span class="sxs-lookup"><span data-stu-id="532fe-191">&ensp;Platform: **4.18.2010.7**</span></span>  
<span data-ttu-id="532fe-192">&ensp;Moteur : **1.1.17600.5**</span><span class="sxs-lookup"><span data-stu-id="532fe-192">&ensp;Engine: **1.1.17600.5**</span></span>  
<span data-ttu-id="532fe-193">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="532fe-193">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="532fe-194">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="532fe-194">What's new</span></span>

- <span data-ttu-id="532fe-195">Nouvelles descriptions pour les catégories de menaces spéciales</span><span class="sxs-lookup"><span data-stu-id="532fe-195">New descriptions for special threat categories</span></span>
- <span data-ttu-id="532fe-196">Fonctionnalités d'émulation améliorées</span><span class="sxs-lookup"><span data-stu-id="532fe-196">Improved emulation capabilities</span></span>
- <span data-ttu-id="532fe-197">Fonctionnalités améliorées d'autoriser/de bloquer l'adresse hôte</span><span class="sxs-lookup"><span data-stu-id="532fe-197">Improved host address allow/block capabilities</span></span>
- <span data-ttu-id="532fe-198">Nouvelle option dans le programme CSP Defender pour ignorer la fusion des exclusions des utilisateurs locaux</span><span class="sxs-lookup"><span data-stu-id="532fe-198">New option in Defender CSP to Ignore merging of local user exclusions</span></span>

### <a name="known-issues"></a><span data-ttu-id="532fe-199">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="532fe-199">Known Issues</span></span>

<span data-ttu-id="532fe-200">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="532fe-200">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="532fe-201">Septembre-2020 (plateforme : 4.18.2009.7 | Moteur : 1.1.17500.4)</span><span class="sxs-lookup"><span data-stu-id="532fe-201">September-2020 (Platform: 4.18.2009.7 | Engine: 1.1.17500.4)</span></span></summary>

<span data-ttu-id="532fe-202">&ensp;Version de mise à jour des informations de sécurité **: 1.325.10.0**</span><span class="sxs-lookup"><span data-stu-id="532fe-202">&ensp;Security intelligence update version: **1.325.10.0**</span></span>  
<span data-ttu-id="532fe-203">&ensp;Publication : **01 octobre 2020**</span><span class="sxs-lookup"><span data-stu-id="532fe-203">&ensp;Released: **October 01, 2020**</span></span>  
<span data-ttu-id="532fe-204">&ensp;Plateforme : **4.18.2009.7**</span><span class="sxs-lookup"><span data-stu-id="532fe-204">&ensp;Platform: **4.18.2009.7**</span></span>  
<span data-ttu-id="532fe-205">&ensp;Moteur : **1.1.17500.4**</span><span class="sxs-lookup"><span data-stu-id="532fe-205">&ensp;Engine: **1.1.17500.4**</span></span>  
<span data-ttu-id="532fe-206">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="532fe-206">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="532fe-207">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="532fe-207">What's new</span></span>

- <span data-ttu-id="532fe-208">Des autorisations d'administrateur sont requises pour restaurer les fichiers en quarantaine</span><span class="sxs-lookup"><span data-stu-id="532fe-208">Admin permissions are required to restore files in quarantine</span></span>
- <span data-ttu-id="532fe-209">Les événements au format XML sont désormais pris en charge</span><span class="sxs-lookup"><span data-stu-id="532fe-209">XML formatted events are now supported</span></span>
- <span data-ttu-id="532fe-210">Prise en charge du programme CSP pour ignorer les fusions d'exclusions</span><span class="sxs-lookup"><span data-stu-id="532fe-210">CSP support for ignoring exclusion merges</span></span>
- <span data-ttu-id="532fe-211">Nouvelles interfaces de gestion pour :</span><span class="sxs-lookup"><span data-stu-id="532fe-211">New management interfaces for:</span></span>
   - <span data-ttu-id="532fe-212">UDP Inspection</span><span class="sxs-lookup"><span data-stu-id="532fe-212">UDP Inspection</span></span>
   - <span data-ttu-id="532fe-213">Protection du réseau sur Server 2019</span><span class="sxs-lookup"><span data-stu-id="532fe-213">Network Protection on Server 2019</span></span>
   - <span data-ttu-id="532fe-214">Exclusions d'adresses IP pour la protection du réseau</span><span class="sxs-lookup"><span data-stu-id="532fe-214">IP Address exclusions for Network Protection</span></span>
- <span data-ttu-id="532fe-215">Meilleure visibilité des mesures du TPM</span><span class="sxs-lookup"><span data-stu-id="532fe-215">Improved visibility into TPM measurements</span></span>
- <span data-ttu-id="532fe-216">Amélioration de l'analyse du module VBA Office</span><span class="sxs-lookup"><span data-stu-id="532fe-216">Improved Office VBA module scanning</span></span>

### <a name="known-issues"></a><span data-ttu-id="532fe-217">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="532fe-217">Known Issues</span></span>

<span data-ttu-id="532fe-218">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="532fe-218">No known issues</span></span>  
<br/>
</details>
<details>
<summary> <span data-ttu-id="532fe-219">Août-2020 (plateforme : 4.18.2008.9 | Moteur : 1.1.17400.5)</span><span class="sxs-lookup"><span data-stu-id="532fe-219">August-2020 (Platform: 4.18.2008.9 | Engine: 1.1.17400.5)</span></span></summary>

<span data-ttu-id="532fe-220">&ensp;Version de mise à jour des informations de sécurité **: 1.323.9.0**</span><span class="sxs-lookup"><span data-stu-id="532fe-220">&ensp;Security intelligence update version: **1.323.9.0**</span></span>  
<span data-ttu-id="532fe-221">&ensp;Publication : **27 août 2020**</span><span class="sxs-lookup"><span data-stu-id="532fe-221">&ensp;Released: **August 27, 2020**</span></span>  
<span data-ttu-id="532fe-222">&ensp;Plateforme : **4.18.2008.9**</span><span class="sxs-lookup"><span data-stu-id="532fe-222">&ensp;Platform: **4.18.2008.9**</span></span>  
<span data-ttu-id="532fe-223">&ensp;Moteur : **1.1.17400.5**</span><span class="sxs-lookup"><span data-stu-id="532fe-223">&ensp;Engine: **1.1.17400.5**</span></span>  
<span data-ttu-id="532fe-224">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="532fe-224">&ensp;Support phase: **Technical upgrade support (only)**</span></span>

### <a name="whats-new"></a><span data-ttu-id="532fe-225">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="532fe-225">What's new</span></span>

- <span data-ttu-id="532fe-226">Ajouter d'autres événements de télémétrie</span><span class="sxs-lookup"><span data-stu-id="532fe-226">Add more telemetry events</span></span>
- <span data-ttu-id="532fe-227">Télémétrie améliorée des événements d'analyse</span><span class="sxs-lookup"><span data-stu-id="532fe-227">Improved scan event telemetry</span></span>
- <span data-ttu-id="532fe-228">Amélioration de la surveillance du comportement pour les analyses de mémoire</span><span class="sxs-lookup"><span data-stu-id="532fe-228">Improved behavior monitoring for memory scans</span></span>
- <span data-ttu-id="532fe-229">Amélioration de l'analyse des flux de macros</span><span class="sxs-lookup"><span data-stu-id="532fe-229">Improved macro streams scanning</span></span>
- <span data-ttu-id="532fe-230">Ajouté à `AMRunningMode` la Get-MpComputerStatus cmdlet PowerShell</span><span class="sxs-lookup"><span data-stu-id="532fe-230">Added `AMRunningMode` to Get-MpComputerStatus PowerShell cmdlet</span></span>
- <span data-ttu-id="532fe-231">[DisableAntiSpyware](/windows-hardware/customize/desktop/unattend/security-malware-windows-defender-disableantispyware) est ignoré.</span><span class="sxs-lookup"><span data-stu-id="532fe-231">[DisableAntiSpyware](/windows-hardware/customize/desktop/unattend/security-malware-windows-defender-disableantispyware) is ignored.</span></span> <span data-ttu-id="532fe-232">L'Antivirus Microsoft Defender se met automatiquement hors de l'application lorsqu'il détecte un autre programme antivirus.</span><span class="sxs-lookup"><span data-stu-id="532fe-232">Microsoft Defender Antivirus automatically turns itself off when it detects another antivirus program.</span></span>


### <a name="known-issues"></a><span data-ttu-id="532fe-233">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="532fe-233">Known Issues</span></span>
<span data-ttu-id="532fe-234">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="532fe-234">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="532fe-235">Juillet-2020 (plateforme : 4.18.2007.8 | Moteur : 1.1.17300.4)</span><span class="sxs-lookup"><span data-stu-id="532fe-235">July-2020 (Platform: 4.18.2007.8 | Engine: 1.1.17300.4)</span></span></summary>

<span data-ttu-id="532fe-236">&ensp;Version de mise à jour des informations de sécurité **: 1.321.30.0**</span><span class="sxs-lookup"><span data-stu-id="532fe-236">&ensp;Security intelligence update version: **1.321.30.0**</span></span>  
<span data-ttu-id="532fe-237">&ensp;Publication : **28 juillet 2020**</span><span class="sxs-lookup"><span data-stu-id="532fe-237">&ensp;Released: **July 28, 2020**</span></span>  
<span data-ttu-id="532fe-238">&ensp;Plateforme : **4.18.2007.8**</span><span class="sxs-lookup"><span data-stu-id="532fe-238">&ensp;Platform: **4.18.2007.8**</span></span>  
<span data-ttu-id="532fe-239">&ensp;Moteur : **1.1.17300.4**</span><span class="sxs-lookup"><span data-stu-id="532fe-239">&ensp;Engine: **1.1.17300.4**</span></span>  
<span data-ttu-id="532fe-240">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="532fe-240">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="532fe-241">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="532fe-241">What's new</span></span>

- <span data-ttu-id="532fe-242">Télémétrie améliorée pour BITS</span><span class="sxs-lookup"><span data-stu-id="532fe-242">Improved telemetry for BITS</span></span>
- <span data-ttu-id="532fe-243">Validation améliorée du certificat de signature de code Authenticode</span><span class="sxs-lookup"><span data-stu-id="532fe-243">Improved Authenticode code signing certificate validation</span></span>

### <a name="known-issues"></a><span data-ttu-id="532fe-244">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="532fe-244">Known Issues</span></span>
<span data-ttu-id="532fe-245">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="532fe-245">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="532fe-246">Juin-2020 (plateforme : 4.18.2006.10 | Moteur : 1.1.17200.2)</span><span class="sxs-lookup"><span data-stu-id="532fe-246">June-2020 (Platform: 4.18.2006.10 | Engine: 1.1.17200.2)</span></span></summary>

<span data-ttu-id="532fe-247">&ensp;Version de mise à jour des informations de sécurité **: 1.319.20.0**</span><span class="sxs-lookup"><span data-stu-id="532fe-247">&ensp;Security intelligence update version: **1.319.20.0**</span></span>  
<span data-ttu-id="532fe-248">&ensp;Publication : **22 juin 2020**</span><span class="sxs-lookup"><span data-stu-id="532fe-248">&ensp;Released: **June 22, 2020**</span></span>  
<span data-ttu-id="532fe-249">&ensp;Plateforme : **4.18.2006.10**</span><span class="sxs-lookup"><span data-stu-id="532fe-249">&ensp;Platform: **4.18.2006.10**</span></span>  
<span data-ttu-id="532fe-250">&ensp;Moteur : **1.1.17200.2**</span><span class="sxs-lookup"><span data-stu-id="532fe-250">&ensp;Engine: **1.1.17200.2**</span></span>  
<span data-ttu-id="532fe-251">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="532fe-251">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="532fe-252">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="532fe-252">What's new</span></span>

- <span data-ttu-id="532fe-253">Possibilité de spécifier [l'emplacement des journaux de support](./collect-diagnostic-data.md)</span><span class="sxs-lookup"><span data-stu-id="532fe-253">Possibility to specify the [location of the support logs](./collect-diagnostic-data.md)</span></span>
- <span data-ttu-id="532fe-254">Ignorer l'analyse de rattrapage agressive en mode passif.</span><span class="sxs-lookup"><span data-stu-id="532fe-254">Skipping aggressive catchup scan in Passive mode.</span></span>
- <span data-ttu-id="532fe-255">Autoriser Defender à se mettre à jour sur les connexions à connexions avec des compteurs</span><span class="sxs-lookup"><span data-stu-id="532fe-255">Allow Defender to update on metered connections</span></span>
- <span data-ttu-id="532fe-256">Réglage des performances fixes lorsque la mise en cache est désactivée</span><span class="sxs-lookup"><span data-stu-id="532fe-256">Fixed performance tuning when caching is disabled</span></span> 
- <span data-ttu-id="532fe-257">Requête de Registre fixe</span><span class="sxs-lookup"><span data-stu-id="532fe-257">Fixed registry query</span></span> 
- <span data-ttu-id="532fe-258">Randomisation du scantime fixe dans ADMX</span><span class="sxs-lookup"><span data-stu-id="532fe-258">Fixed scantime randomization in ADMX</span></span>

### <a name="known-issues"></a><span data-ttu-id="532fe-259">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="532fe-259">Known Issues</span></span>
<span data-ttu-id="532fe-260">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="532fe-260">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="532fe-261">Mai-2020 (plateforme : 4.18.2005.4 | Moteur : 1.1.17100.2)</span><span class="sxs-lookup"><span data-stu-id="532fe-261">May-2020 (Platform: 4.18.2005.4 | Engine: 1.1.17100.2)</span></span></summary>

<span data-ttu-id="532fe-262">&ensp;Version de mise à jour des informations de sécurité **: 1.317.20.0**</span><span class="sxs-lookup"><span data-stu-id="532fe-262">&ensp;Security intelligence update version: **1.317.20.0**</span></span>  
<span data-ttu-id="532fe-263">&ensp;Publication : **26 mai 2020**</span><span class="sxs-lookup"><span data-stu-id="532fe-263">&ensp;Released: **May 26, 2020**</span></span>  
<span data-ttu-id="532fe-264">&ensp;Plateforme : **4.18.2005.4**</span><span class="sxs-lookup"><span data-stu-id="532fe-264">&ensp;Platform: **4.18.2005.4**</span></span>  
<span data-ttu-id="532fe-265">&ensp;Moteur : **1.1.17100.2**</span><span class="sxs-lookup"><span data-stu-id="532fe-265">&ensp;Engine: **1.1.17100.2**</span></span>  
<span data-ttu-id="532fe-266">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="532fe-266">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="532fe-267">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="532fe-267">What's new</span></span>

- <span data-ttu-id="532fe-268">Journalisation améliorée des événements d'analyse</span><span class="sxs-lookup"><span data-stu-id="532fe-268">Improved logging for scan events</span></span>
- <span data-ttu-id="532fe-269">Amélioration de la gestion des incidents en mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="532fe-269">Improved user mode crash handling.</span></span>
- <span data-ttu-id="532fe-270">Suivi des événements ajouté pour la protection contre la falsification</span><span class="sxs-lookup"><span data-stu-id="532fe-270">Added event tracing for Tamper protection</span></span>
- <span data-ttu-id="532fe-271">Envoi d'exemples AMSI fixes</span><span class="sxs-lookup"><span data-stu-id="532fe-271">Fixed AMSI Sample submission</span></span>
- <span data-ttu-id="532fe-272">Blocage du cloud AMSI fixe</span><span class="sxs-lookup"><span data-stu-id="532fe-272">Fixed AMSI Cloud blocking</span></span>
- <span data-ttu-id="532fe-273">Journal d'installation des mises à jour de sécurité fixes</span><span class="sxs-lookup"><span data-stu-id="532fe-273">Fixed Security update install log</span></span>

### <a name="known-issues"></a><span data-ttu-id="532fe-274">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="532fe-274">Known Issues</span></span>
<span data-ttu-id="532fe-275">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="532fe-275">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="532fe-276">Avril-2020 (plateforme : 4.18.2004.6 | Moteur : 1.1.17000.2)</span><span class="sxs-lookup"><span data-stu-id="532fe-276">April-2020 (Platform: 4.18.2004.6 | Engine: 1.1.17000.2)</span></span></summary>

<span data-ttu-id="532fe-277">&ensp;Version de mise à jour des informations de sécurité **: 1.315.12.0**</span><span class="sxs-lookup"><span data-stu-id="532fe-277">&ensp;Security intelligence update version: **1.315.12.0**</span></span>  
<span data-ttu-id="532fe-278">&ensp;Publication : **30 avril 2020**</span><span class="sxs-lookup"><span data-stu-id="532fe-278">&ensp;Released: **April 30, 2020**</span></span>  
<span data-ttu-id="532fe-279">&ensp;Plateforme : **4.18.2004.6**</span><span class="sxs-lookup"><span data-stu-id="532fe-279">&ensp;Platform: **4.18.2004.6**</span></span>  
<span data-ttu-id="532fe-280">&ensp;Moteur : **1.1.17000.2**</span><span class="sxs-lookup"><span data-stu-id="532fe-280">&ensp;Engine: **1.1.17000.2**</span></span>  
<span data-ttu-id="532fe-281">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="532fe-281">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="532fe-282">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="532fe-282">What's new</span></span>
- <span data-ttu-id="532fe-283">Améliorations de WDfilter</span><span class="sxs-lookup"><span data-stu-id="532fe-283">WDfilter improvements</span></span>
- <span data-ttu-id="532fe-284">Ajouter des données d'événements actionnables à des événements de détection de réduction de la surface d'attaque</span><span class="sxs-lookup"><span data-stu-id="532fe-284">Add more actionable event data to attack surface reduction detection events</span></span>
- <span data-ttu-id="532fe-285">Informations de version fixes dans les données de diagnostic et WMI</span><span class="sxs-lookup"><span data-stu-id="532fe-285">Fixed version information in diagnostic data and WMI</span></span>
- <span data-ttu-id="532fe-286">Version de plateforme incorrecte corrigée dans l'interface utilisateur après la mise à jour de la plateforme</span><span class="sxs-lookup"><span data-stu-id="532fe-286">Fixed incorrect platform version in UI after platform update</span></span>
- <span data-ttu-id="532fe-287">Intel d'URL dynamique pour la protection contre les menaces sans fichier</span><span class="sxs-lookup"><span data-stu-id="532fe-287">Dynamic URL intel for Fileless threat protection</span></span>
- <span data-ttu-id="532fe-288">Fonctionnalité d'analyse UEFI</span><span class="sxs-lookup"><span data-stu-id="532fe-288">UEFI scan capability</span></span>
- <span data-ttu-id="532fe-289">Étendre la journalisation pour les mises à jour</span><span class="sxs-lookup"><span data-stu-id="532fe-289">Extend logging for updates</span></span>

### <a name="known-issues"></a><span data-ttu-id="532fe-290">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="532fe-290">Known Issues</span></span>
<span data-ttu-id="532fe-291">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="532fe-291">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="532fe-292">Mars-2020 (plateforme : 4.18.2003.8 | Moteur : 1.1.16900.2)</span><span class="sxs-lookup"><span data-stu-id="532fe-292">March-2020 (Platform: 4.18.2003.8 | Engine: 1.1.16900.2)</span></span></summary>

<span data-ttu-id="532fe-293">&ensp;Version de mise à jour des informations de sécurité **: 1.313.8.0**</span><span class="sxs-lookup"><span data-stu-id="532fe-293">&ensp;Security intelligence update version: **1.313.8.0**</span></span>  
<span data-ttu-id="532fe-294">&ensp;Publication : **24 mars 2020**</span><span class="sxs-lookup"><span data-stu-id="532fe-294">&ensp;Released: **March 24, 2020**</span></span>  
<span data-ttu-id="532fe-295">&ensp;Plateforme : **4.18.2003.8**</span><span class="sxs-lookup"><span data-stu-id="532fe-295">&ensp;Platform: **4.18.2003.8**</span></span>  
<span data-ttu-id="532fe-296">&ensp;Moteur : **1.1.16900.4**</span><span class="sxs-lookup"><span data-stu-id="532fe-296">&ensp;Engine: **1.1.16900.4**</span></span>  
<span data-ttu-id="532fe-297">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="532fe-297">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="532fe-298">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="532fe-298">What's new</span></span>

- <span data-ttu-id="532fe-299">Option de limitation du processeur ajoutée à [MpCmdRun](./command-line-arguments-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="532fe-299">CPU Throttling option added to [MpCmdRun](./command-line-arguments-microsoft-defender-antivirus.md)</span></span>
- <span data-ttu-id="532fe-300">Améliorer les fonctionnalités de diagnostic</span><span class="sxs-lookup"><span data-stu-id="532fe-300">Improve diagnostic capability</span></span>
- <span data-ttu-id="532fe-301">réduire le délai d'out des informations de sécurité (5 min)</span><span class="sxs-lookup"><span data-stu-id="532fe-301">reduce Security intelligence timeout (5 min)</span></span>
- <span data-ttu-id="532fe-302">Étendre la fonctionnalité de journal interne du moteur AMSI</span><span class="sxs-lookup"><span data-stu-id="532fe-302">Extend AMSI engine internal log capability</span></span>
- <span data-ttu-id="532fe-303">Améliorer la notification pour le blocage des processus</span><span class="sxs-lookup"><span data-stu-id="532fe-303">Improve notification for process blocking</span></span>
   
### <a name="known-issues"></a><span data-ttu-id="532fe-304">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="532fe-304">Known Issues</span></span>
<span data-ttu-id="532fe-305">[**Fixe**] L'Antivirus Microsoft Defender ignorera les fichiers lors de l'exécution d'une analyse.</span><span class="sxs-lookup"><span data-stu-id="532fe-305">[**Fixed**] Microsoft Defender Antivirus is skipping files when running a scan.</span></span>

<br/>
</details>

<details>

<summary> <span data-ttu-id="532fe-306">Février-2020 (plateforme : - | Moteur : 1.1.16800.2)</span><span class="sxs-lookup"><span data-stu-id="532fe-306">February-2020 (Platform: - | Engine: 1.1.16800.2)</span></span></summary>
  

<span data-ttu-id="532fe-307">&ensp;Version de mise à jour des informations de sécurité **: 1.311.4.0** </span><span class="sxs-lookup"><span data-stu-id="532fe-307">&ensp;Security intelligence update version: **1.311.4.0** </span></span>  
<span data-ttu-id="532fe-308">&ensp;Publication : **25 février 2020**</span><span class="sxs-lookup"><span data-stu-id="532fe-308">&ensp;Released: **February 25, 2020**</span></span>  
<span data-ttu-id="532fe-309">&ensp;Plateforme/Client : **-**</span><span class="sxs-lookup"><span data-stu-id="532fe-309">&ensp;Platform/Client: **-**</span></span>  
<span data-ttu-id="532fe-310">&ensp;Moteur : **1.1.16800.2**</span><span class="sxs-lookup"><span data-stu-id="532fe-310">&ensp;Engine: **1.1.16800.2**</span></span>  
<span data-ttu-id="532fe-311">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="532fe-311">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
     
### <a name="whats-new"></a><span data-ttu-id="532fe-312">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="532fe-312">What's new</span></span>

  
### <a name="known-issues"></a><span data-ttu-id="532fe-313">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="532fe-313">Known Issues</span></span>
<span data-ttu-id="532fe-314">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="532fe-314">No known issues</span></span>
<br/>
</details>

<details>
<summary> <span data-ttu-id="532fe-315">Janvier-2020 (plateforme : 4.18.2001.10 | Moteur : 1.1.16700.2)</span><span class="sxs-lookup"><span data-stu-id="532fe-315">January-2020 (Platform: 4.18.2001.10 | Engine: 1.1.16700.2)</span></span></summary>
  

<span data-ttu-id="532fe-316">Version de mise à jour des informations de sécurité **: 1.309.32.0**</span><span class="sxs-lookup"><span data-stu-id="532fe-316">Security intelligence update version: **1.309.32.0**</span></span>  
<span data-ttu-id="532fe-317">Publication : **30 janvier 2020**</span><span class="sxs-lookup"><span data-stu-id="532fe-317">Released: **January 30, 2020**</span></span>  
<span data-ttu-id="532fe-318">Plateforme/Client : **4.18.2001.10**</span><span class="sxs-lookup"><span data-stu-id="532fe-318">Platform/Client: **4.18.2001.10**</span></span>  
<span data-ttu-id="532fe-319">Moteur : **1.1.16700.2**</span><span class="sxs-lookup"><span data-stu-id="532fe-319">Engine: **1.1.16700.2**</span></span>  
<span data-ttu-id="532fe-320">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="532fe-320">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
     
### <a name="whats-new"></a><span data-ttu-id="532fe-321">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="532fe-321">What's new</span></span>

- <span data-ttu-id="532fe-322">BSOD fixe sur WS2016 avec Exchange</span><span class="sxs-lookup"><span data-stu-id="532fe-322">Fixed BSOD on WS2016 with Exchange</span></span>
- <span data-ttu-id="532fe-323">Prise en charge des mises à jour de plateforme lorsque le TMP est redirigé vers le chemin d'accès réseau</span><span class="sxs-lookup"><span data-stu-id="532fe-323">Support platform updates when TMP is redirected to network path</span></span>
- <span data-ttu-id="532fe-324">Les versions de plateforme et de moteur sont ajoutées [à WDSI](https://www.microsoft.com/en-us/wdsi/defenderupdates)</span><span class="sxs-lookup"><span data-stu-id="532fe-324">Platform and engine versions are added to [WDSI](https://www.microsoft.com/en-us/wdsi/defenderupdates)</span></span> <!-- The preceding URL must include "/en-us" -->
- <span data-ttu-id="532fe-325">étendre la mise à jour des signatures d'urgence [en mode passif](./microsoft-defender-antivirus-compatibility.md)</span><span class="sxs-lookup"><span data-stu-id="532fe-325">extend Emergency signature update to [passive mode](./microsoft-defender-antivirus-compatibility.md)</span></span>
- <span data-ttu-id="532fe-326">Correction du problème de 4.18.1911.3</span><span class="sxs-lookup"><span data-stu-id="532fe-326">Fix 4.18.1911.3 hang</span></span>
   
### <a name="known-issues"></a><span data-ttu-id="532fe-327">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="532fe-327">Known Issues</span></span>

<span data-ttu-id="532fe-328">[**Fixed**] Devices using [modern standby mode](/windows-hardware/design/device-experiences/modern-standby) may experience a hang with the Windows Defender filter driver that results in a gap of protection.</span><span class="sxs-lookup"><span data-stu-id="532fe-328">[**Fixed**] devices utilizing [modern standby mode](/windows-hardware/design/device-experiences/modern-standby) may experience a hang with the Windows Defender filter driver that results in a gap of protection.</span></span>  <span data-ttu-id="532fe-329">Les ordinateurs concernés semblent ne pas avoir été mis à jour vers la dernière plateforme anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="532fe-329">Affected machines appear to the customer as having not updated to the latest antimalware platform.</span></span>  
<br/>
> [!IMPORTANT]
> <span data-ttu-id="532fe-330">Cette mise à jour est :</span><span class="sxs-lookup"><span data-stu-id="532fe-330">This update is:</span></span>
> - <span data-ttu-id="532fe-331">nécessaire aux appareils RS1 exécutant une version inférieure de la plateforme pour prendre en charge SHA2 ;</span><span class="sxs-lookup"><span data-stu-id="532fe-331">needed by RS1 devices running lower version of the platform to support SHA2;</span></span>
> - <span data-ttu-id="532fe-332">a un indicateur de redémarrage pour les systèmes qui ont des problèmes en suspension ;</span><span class="sxs-lookup"><span data-stu-id="532fe-332">has a reboot flag for systems that have hanging issues;</span></span>
> - <span data-ttu-id="532fe-333">est re-publiée en avril 2020 et ne sera pas recalée par les mises à jour plus nouvelles pour conserver la disponibilité future ;</span><span class="sxs-lookup"><span data-stu-id="532fe-333">is re-released in April 2020 and will not be superseded by newer updates to keep future availability;</span></span>  
> - <span data-ttu-id="532fe-334">est classée en tant que mise à jour en raison de l'exigence de redémarrage ; et</span><span class="sxs-lookup"><span data-stu-id="532fe-334">is categorized as an update due to the reboot requirement; and</span></span>
> - <span data-ttu-id="532fe-335">est uniquement proposé avec [Windows Update](https://support.microsoft.com/help/4027667/windows-10-update).</span><span class="sxs-lookup"><span data-stu-id="532fe-335">is only be offered with [Windows Update](https://support.microsoft.com/help/4027667/windows-10-update).</span></span>
<br/>
</details>

<details>
<summary> <span data-ttu-id="532fe-336">Novembre-2019 (plateforme : 4.18.1911.3 | Moteur : 1.1.16600.7)</span><span class="sxs-lookup"><span data-stu-id="532fe-336">November-2019 (Platform: 4.18.1911.3 | Engine: 1.1.16600.7)</span></span></summary>

<span data-ttu-id="532fe-337">Version de mise à jour des informations de sécurité **: 1.307.13.0**</span><span class="sxs-lookup"><span data-stu-id="532fe-337">Security intelligence update version: **1.307.13.0**</span></span>  
<span data-ttu-id="532fe-338">Publication : **7 décembre 2019**</span><span class="sxs-lookup"><span data-stu-id="532fe-338">Released: **December 7, 2019**</span></span>  
<span data-ttu-id="532fe-339">Plateforme : **4.18.1911.3**</span><span class="sxs-lookup"><span data-stu-id="532fe-339">Platform: **4.18.1911.3**</span></span>  
<span data-ttu-id="532fe-340">Moteur : **1.1.17000.7**</span><span class="sxs-lookup"><span data-stu-id="532fe-340">Engine: **1.1.17000.7**</span></span>  
<span data-ttu-id="532fe-341">Phase de support : **aucune prise en charge**</span><span class="sxs-lookup"><span data-stu-id="532fe-341">Support phase: **No support**</span></span>  
     
### <a name="whats-new"></a><span data-ttu-id="532fe-342">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="532fe-342">What's new</span></span>

- <span data-ttu-id="532fe-343">Niveau de suivi MpCmdRun fixe</span><span class="sxs-lookup"><span data-stu-id="532fe-343">Fixed MpCmdRun tracing level</span></span>
- <span data-ttu-id="532fe-344">Informations de version de WDFilter fixes</span><span class="sxs-lookup"><span data-stu-id="532fe-344">Fixed WDFilter version info</span></span>
- <span data-ttu-id="532fe-345">Améliorer les notifications (PUA)</span><span class="sxs-lookup"><span data-stu-id="532fe-345">Improve notifications (PUA)</span></span>
- <span data-ttu-id="532fe-346">ajouter des journaux MRT pour prendre en charge les fichiers</span><span class="sxs-lookup"><span data-stu-id="532fe-346">add MRT logs to support files</span></span>
   
### <a name="known-issues"></a><span data-ttu-id="532fe-347">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="532fe-347">Known Issues</span></span>
<span data-ttu-id="532fe-348">Lorsque cette mise à jour est installée, l'appareil a besoin du package de saut 4.10.2001.10 pour pouvoir se mettre à jour vers la dernière version de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="532fe-348">When this update is installed, the device needs the jump package 4.10.2001.10 to be able to update to the latest platform version.</span></span>
<br/>
</details>


## <a name="microsoft-defender-antivirus-platform-support"></a><span data-ttu-id="532fe-349">Prise en charge de la plateforme antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="532fe-349">Microsoft Defender Antivirus platform support</span></span>
<span data-ttu-id="532fe-350">Les mises à jour de la plateforme et du moteur sont fournies à une cadence mensuelle.</span><span class="sxs-lookup"><span data-stu-id="532fe-350">Platform and engine updates are provided on a monthly cadence.</span></span> <span data-ttu-id="532fe-351">Pour être entièrement pris en charge, tenez à jour les dernières mises à jour de plateforme.</span><span class="sxs-lookup"><span data-stu-id="532fe-351">To be fully supported, keep current with the latest platform updates.</span></span> <span data-ttu-id="532fe-352">Notre structure de support est dynamique et évolue en deux phases en fonction de la disponibilité de la dernière version de plateforme :</span><span class="sxs-lookup"><span data-stu-id="532fe-352">Our support structure is dynamic, evolving into two phases depending on the availability of the latest platform version:</span></span>

- <span data-ttu-id="532fe-353">Phase de maintenance des mises à jour **critiques** et de sécurité : lors de l'exécution de la dernière version de la plateforme, vous serez éligible à la réception des mises à jour de sécurité et critiques sur la plateforme anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="532fe-353">**Security and Critical Updates servicing phase** - When running the latest platform version, you will be eligible to receive both Security and Critical updates to the anti-malware platform.</span></span>
 
- <span data-ttu-id="532fe-354">**Phase de support technique (uniquement)** : après la publication d'une nouvelle version de plateforme, la prise en charge des versions antérieures (N-2) sera réduit au support technique uniquement.</span><span class="sxs-lookup"><span data-stu-id="532fe-354">**Technical Support (Only) phase** - After a new platform version is released, support for older versions (N-2) will reduce to technical support only.</span></span> <span data-ttu-id="532fe-355">Les versions de plateforme antérieures à N-2 ne seront plus pris en charge.\*</span><span class="sxs-lookup"><span data-stu-id="532fe-355">Platform versions older than N-2 will no longer be supported.\*</span></span>

<span data-ttu-id="532fe-356">\* Le support technique continuera d'être fourni pour les mises à niveau de la version de Windows 10 (voir la version de plateforme incluse avec les versions [de Windows 10)](#platform-version-included-with-windows-10-releases)vers la dernière version de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="532fe-356">\* Technical support will continue to be provided for upgrades from the Windows 10 release version (see [Platform version included with Windows 10 releases](#platform-version-included-with-windows-10-releases)) to the latest platform version.</span></span>

<span data-ttu-id="532fe-357">Pendant la phase de support technique (uniquement), les incidents de support commercialement raisonnables sont fournis par le biais du support technique du service clientèle Microsoft & et des offres de support géré de Microsoft (telles que le support Premier).</span><span class="sxs-lookup"><span data-stu-id="532fe-357">During the technical support (only) phase, commercially reasonable support incidents will be provided through Microsoft Customer Service & Support and Microsoft’s managed support offerings (such as Premier Support).</span></span> <span data-ttu-id="532fe-358">Si un incident de support nécessite une escalade vers le développement pour obtenir des conseils supplémentaires, nécessite une mise à jour non de sécurité ou nécessite une mise à jour de sécurité, les clients sont invités à mettre à niveau vers la dernière version de plateforme ou une mise à jour intermédiaire (\*).</span><span class="sxs-lookup"><span data-stu-id="532fe-358">If a support incident requires escalation to development for further guidance, requires a non-security update, or requires a security update, customers will be asked to upgrade to the latest platform version or an intermediate update (\*).</span></span>

### <a name="platform-version-included-with-windows-10-releases"></a><span data-ttu-id="532fe-359">Version de plateforme incluse dans les versions de Windows 10</span><span class="sxs-lookup"><span data-stu-id="532fe-359">Platform version included with Windows 10 releases</span></span>
<span data-ttu-id="532fe-360">Le tableau ci-dessous fournit la plateforme antivirus Microsoft Defender et les versions de moteur livrées avec les dernières versions de Windows 10 :</span><span class="sxs-lookup"><span data-stu-id="532fe-360">The below table provides the Microsoft Defender Antivirus platform and engine versions that are shipped with the latest Windows 10 releases:</span></span>    

|<span data-ttu-id="532fe-361">Version de Windows 10</span><span class="sxs-lookup"><span data-stu-id="532fe-361">Windows 10 release</span></span>  |<span data-ttu-id="532fe-362">Version de la plateforme</span><span class="sxs-lookup"><span data-stu-id="532fe-362">Platform version</span></span>  |<span data-ttu-id="532fe-363">Version du moteur</span><span class="sxs-lookup"><span data-stu-id="532fe-363">Engine version</span></span> |<span data-ttu-id="532fe-364">Phase de prise en charge</span><span class="sxs-lookup"><span data-stu-id="532fe-364">Support phase</span></span> |
|:---|:---|:---|:---|
|<span data-ttu-id="532fe-365">2004 (20H1/20H2)</span><span class="sxs-lookup"><span data-stu-id="532fe-365">2004  (20H1/20H2)</span></span> |<span data-ttu-id="532fe-366">4.18.1909.6</span><span class="sxs-lookup"><span data-stu-id="532fe-366">4.18.1909.6</span></span> |<span data-ttu-id="532fe-367">1.1.17000.2</span><span class="sxs-lookup"><span data-stu-id="532fe-367">1.1.17000.2</span></span> | <span data-ttu-id="532fe-368">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="532fe-368">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="532fe-369">1909 (19H2)</span><span class="sxs-lookup"><span data-stu-id="532fe-369">1909  (19H2)</span></span> |<span data-ttu-id="532fe-370">4.18.1902.5</span><span class="sxs-lookup"><span data-stu-id="532fe-370">4.18.1902.5</span></span> |<span data-ttu-id="532fe-371">1.1.16700.3</span><span class="sxs-lookup"><span data-stu-id="532fe-371">1.1.16700.3</span></span> | <span data-ttu-id="532fe-372">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="532fe-372">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="532fe-373">1903 (19H1)</span><span class="sxs-lookup"><span data-stu-id="532fe-373">1903  (19H1)</span></span> |<span data-ttu-id="532fe-374">4.18.1902.5</span><span class="sxs-lookup"><span data-stu-id="532fe-374">4.18.1902.5</span></span> |<span data-ttu-id="532fe-375">1.1.15600.4</span><span class="sxs-lookup"><span data-stu-id="532fe-375">1.1.15600.4</span></span> | <span data-ttu-id="532fe-376">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="532fe-376">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="532fe-377">1809 (RS5)</span><span class="sxs-lookup"><span data-stu-id="532fe-377">1809  (RS5)</span></span> |<span data-ttu-id="532fe-378">4.18.1807.18075</span><span class="sxs-lookup"><span data-stu-id="532fe-378">4.18.1807.18075</span></span> |<span data-ttu-id="532fe-379">1.1.15000.2</span><span class="sxs-lookup"><span data-stu-id="532fe-379">1.1.15000.2</span></span> | <span data-ttu-id="532fe-380">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="532fe-380">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="532fe-381">1803 (RS4)</span><span class="sxs-lookup"><span data-stu-id="532fe-381">1803  (RS4)</span></span> |<span data-ttu-id="532fe-382">4.13.17134.1</span><span class="sxs-lookup"><span data-stu-id="532fe-382">4.13.17134.1</span></span> |<span data-ttu-id="532fe-383">1.1.14600.4</span><span class="sxs-lookup"><span data-stu-id="532fe-383">1.1.14600.4</span></span> | <span data-ttu-id="532fe-384">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="532fe-384">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="532fe-385">1709 (RS3)</span><span class="sxs-lookup"><span data-stu-id="532fe-385">1709  (RS3)</span></span> |<span data-ttu-id="532fe-386">4.12.16299.15</span><span class="sxs-lookup"><span data-stu-id="532fe-386">4.12.16299.15</span></span> |<span data-ttu-id="532fe-387">1.1.14104.0</span><span class="sxs-lookup"><span data-stu-id="532fe-387">1.1.14104.0</span></span> | <span data-ttu-id="532fe-388">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="532fe-388">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="532fe-389">1703 (RS2)</span><span class="sxs-lookup"><span data-stu-id="532fe-389">1703  (RS2)</span></span> |<span data-ttu-id="532fe-390">4.11.15603.2</span><span class="sxs-lookup"><span data-stu-id="532fe-390">4.11.15603.2</span></span> |<span data-ttu-id="532fe-391">1.1.13504.0</span><span class="sxs-lookup"><span data-stu-id="532fe-391">1.1.13504.0</span></span> | <span data-ttu-id="532fe-392">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="532fe-392">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="532fe-393">1607 (RS1)</span><span class="sxs-lookup"><span data-stu-id="532fe-393">1607 (RS1)</span></span> |<span data-ttu-id="532fe-394">4.10.14393.3683</span><span class="sxs-lookup"><span data-stu-id="532fe-394">4.10.14393.3683</span></span> |<span data-ttu-id="532fe-395">1.1.12805.0</span><span class="sxs-lookup"><span data-stu-id="532fe-395">1.1.12805.0</span></span> | <span data-ttu-id="532fe-396">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="532fe-396">Technical upgrade support (only)</span></span> |  

<span data-ttu-id="532fe-397">Pour plus d'informations sur la version de Windows 10, voir la feuille d'informations sur le [cycle de vie de Windows.](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet)</span><span class="sxs-lookup"><span data-stu-id="532fe-397">For Windows 10 release information, see the [Windows lifecycle fact sheet](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet).</span></span>

## <a name="updates-for-deployment-image-servicing-and-management-dism"></a><span data-ttu-id="532fe-398">Mises à jour pour la gestion et la maintenance des images de déploiement (DISM)</span><span class="sxs-lookup"><span data-stu-id="532fe-398">Updates for Deployment Image Servicing and Management (DISM)</span></span>

<span data-ttu-id="532fe-399">Nous vous recommandons de mettre à jour vos images d'installation de système d'exploitation Windows 10 (éditions Entreprise, Professionnel et Famille), Windows Server 2019 et Windows Server 2016 avec les dernières mises à jour antivirus et anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="532fe-399">We recommend updating your Windows 10 (Enterprise, Pro, and Home editions), Windows Server 2019, and Windows Server 2016 OS installation images with the latest antivirus and antimalware updates.</span></span> <span data-ttu-id="532fe-400">La mise à jour de vos images d'installation du système d'exploitation permet d'éviter un écart de protection.</span><span class="sxs-lookup"><span data-stu-id="532fe-400">Keeping your OS installation images up to date helps avoid a gap in protection.</span></span> 

<span data-ttu-id="532fe-401">Pour plus d'informations, voir [Mise à jour de Microsoft Defender pour les images d'installation du système d'exploitation Windows.](https://support.microsoft.com/help/4568292/defender-update-for-windows-operating-system-installation-images)</span><span class="sxs-lookup"><span data-stu-id="532fe-401">For more information, see [Microsoft Defender update for Windows operating system installation images](https://support.microsoft.com/help/4568292/defender-update-for-windows-operating-system-installation-images).</span></span>

<details>
<summary><span data-ttu-id="532fe-402">1.1.2104.01</span><span class="sxs-lookup"><span data-stu-id="532fe-402">1.1.2104.01</span></span></summary>

<span data-ttu-id="532fe-403">&ensp;Version du package **: 1.1.2104.01**  </span><span class="sxs-lookup"><span data-stu-id="532fe-403">&ensp;Package version: **1.1.2104.01**  </span></span>  
<span data-ttu-id="532fe-404">&ensp;Version de plateforme **: 4.18.2102.4** </span><span class="sxs-lookup"><span data-stu-id="532fe-404">&ensp;Platform version: **4.18.2102.4** </span></span>  
<span data-ttu-id="532fe-405">&ensp;Version du moteur **: 1.1.18000.5**</span><span class="sxs-lookup"><span data-stu-id="532fe-405">&ensp;Engine version: **1.1.18000.5**</span></span>  
<span data-ttu-id="532fe-406">&ensp;Version de signature **: 1.335.232.0**</span><span class="sxs-lookup"><span data-stu-id="532fe-406">&ensp;Signature version: **1.335.232.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="532fe-407">Correctifs</span><span class="sxs-lookup"><span data-stu-id="532fe-407">Fixes</span></span>
- <span data-ttu-id="532fe-408">Aucun</span><span class="sxs-lookup"><span data-stu-id="532fe-408">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="532fe-409">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="532fe-409">Additional information</span></span>
- <span data-ttu-id="532fe-410">Aucun</span><span class="sxs-lookup"><span data-stu-id="532fe-410">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="532fe-411">1.1.2103.01</span><span class="sxs-lookup"><span data-stu-id="532fe-411">1.1.2103.01</span></span></summary>

<span data-ttu-id="532fe-412">&ensp;Version du package **: 1.1.2103.01**  </span><span class="sxs-lookup"><span data-stu-id="532fe-412">&ensp;Package version: **1.1.2103.01**  </span></span>  
<span data-ttu-id="532fe-413">&ensp;Version de plateforme **: 4.18.2101.9** </span><span class="sxs-lookup"><span data-stu-id="532fe-413">&ensp;Platform version: **4.18.2101.9** </span></span>  
<span data-ttu-id="532fe-414">&ensp;Version du moteur **: 1.1.17800.5**</span><span class="sxs-lookup"><span data-stu-id="532fe-414">&ensp;Engine version: **1.1.17800.5**</span></span>  
<span data-ttu-id="532fe-415">&ensp;Version de signature **: 1.331.2302.0**</span><span class="sxs-lookup"><span data-stu-id="532fe-415">&ensp;Signature version: **1.331.2302.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="532fe-416">Correctifs</span><span class="sxs-lookup"><span data-stu-id="532fe-416">Fixes</span></span>
- <span data-ttu-id="532fe-417">Aucun</span><span class="sxs-lookup"><span data-stu-id="532fe-417">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="532fe-418">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="532fe-418">Additional information</span></span>
- <span data-ttu-id="532fe-419">Aucun</span><span class="sxs-lookup"><span data-stu-id="532fe-419">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="532fe-420">1.1.2102.03</span><span class="sxs-lookup"><span data-stu-id="532fe-420">1.1.2102.03</span></span></summary>

<span data-ttu-id="532fe-421">&ensp;Version du package **: 1.1.2102.03**  </span><span class="sxs-lookup"><span data-stu-id="532fe-421">&ensp;Package version: **1.1.2102.03**  </span></span>  
<span data-ttu-id="532fe-422">&ensp;Version de la plateforme **: 4.18.2011.6** </span><span class="sxs-lookup"><span data-stu-id="532fe-422">&ensp;Platform version: **4.18.2011.6** </span></span>  
<span data-ttu-id="532fe-423">&ensp;Version du moteur **: 1.1.17800.5**</span><span class="sxs-lookup"><span data-stu-id="532fe-423">&ensp;Engine version: **1.1.17800.5**</span></span>  
<span data-ttu-id="532fe-424">&ensp;Version de signature **: 1.331.174.0**</span><span class="sxs-lookup"><span data-stu-id="532fe-424">&ensp;Signature version: **1.331.174.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="532fe-425">Correctifs</span><span class="sxs-lookup"><span data-stu-id="532fe-425">Fixes</span></span>
- <span data-ttu-id="532fe-426">Aucun</span><span class="sxs-lookup"><span data-stu-id="532fe-426">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="532fe-427">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="532fe-427">Additional information</span></span>
- <span data-ttu-id="532fe-428">Aucun</span><span class="sxs-lookup"><span data-stu-id="532fe-428">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="532fe-429">1.1.2101.02</span><span class="sxs-lookup"><span data-stu-id="532fe-429">1.1.2101.02</span></span></summary>

<span data-ttu-id="532fe-430">&ensp;Version du package **: 1.1.2101.02**  </span><span class="sxs-lookup"><span data-stu-id="532fe-430">&ensp;Package version: **1.1.2101.02**  </span></span>  
<span data-ttu-id="532fe-431">&ensp;Version de la plateforme **: 4.18.2011.6** </span><span class="sxs-lookup"><span data-stu-id="532fe-431">&ensp;Platform version: **4.18.2011.6** </span></span>  
<span data-ttu-id="532fe-432">&ensp;Version du moteur **: 1.1.17700.4**</span><span class="sxs-lookup"><span data-stu-id="532fe-432">&ensp;Engine version: **1.1.17700.4**</span></span>  
<span data-ttu-id="532fe-433">&ensp;Version de signature **: 1.329.1796.0**</span><span class="sxs-lookup"><span data-stu-id="532fe-433">&ensp;Signature version: **1.329.1796.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="532fe-434">Correctifs</span><span class="sxs-lookup"><span data-stu-id="532fe-434">Fixes</span></span>
- <span data-ttu-id="532fe-435">Aucun</span><span class="sxs-lookup"><span data-stu-id="532fe-435">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="532fe-436">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="532fe-436">Additional information</span></span>
- <span data-ttu-id="532fe-437">Aucun</span><span class="sxs-lookup"><span data-stu-id="532fe-437">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="532fe-438">1.1.2012.01</span><span class="sxs-lookup"><span data-stu-id="532fe-438">1.1.2012.01</span></span></summary>

<span data-ttu-id="532fe-439">&ensp;Version du package **: 1.1.2012.01**  </span><span class="sxs-lookup"><span data-stu-id="532fe-439">&ensp;Package version: **1.1.2012.01**  </span></span>  
<span data-ttu-id="532fe-440">&ensp;Version de plateforme **: 4.18.2010.7** </span><span class="sxs-lookup"><span data-stu-id="532fe-440">&ensp;Platform version: **4.18.2010.7** </span></span>  
<span data-ttu-id="532fe-441">&ensp;Version du moteur **: 1.1.17600.5**</span><span class="sxs-lookup"><span data-stu-id="532fe-441">&ensp;Engine version: **1.1.17600.5**</span></span>  
<span data-ttu-id="532fe-442">&ensp;Version de signature **: 1.327.1991.0**</span><span class="sxs-lookup"><span data-stu-id="532fe-442">&ensp;Signature version: **1.327.1991.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="532fe-443">Correctifs</span><span class="sxs-lookup"><span data-stu-id="532fe-443">Fixes</span></span>
- <span data-ttu-id="532fe-444">Aucun</span><span class="sxs-lookup"><span data-stu-id="532fe-444">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="532fe-445">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="532fe-445">Additional information</span></span>
- <span data-ttu-id="532fe-446">Aucun</span><span class="sxs-lookup"><span data-stu-id="532fe-446">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="532fe-447">1.1.2011.02</span><span class="sxs-lookup"><span data-stu-id="532fe-447">1.1.2011.02</span></span></summary>

<span data-ttu-id="532fe-448">&ensp;Version du package **: 1.1.2011.02**  </span><span class="sxs-lookup"><span data-stu-id="532fe-448">&ensp;Package version: **1.1.2011.02**  </span></span>  
<span data-ttu-id="532fe-449">&ensp;Version de plateforme **: 4.18.2010.7** </span><span class="sxs-lookup"><span data-stu-id="532fe-449">&ensp;Platform version: **4.18.2010.7** </span></span>  
<span data-ttu-id="532fe-450">&ensp;Version du moteur **: 1.1.17600.5**</span><span class="sxs-lookup"><span data-stu-id="532fe-450">&ensp;Engine version: **1.1.17600.5**</span></span>  
<span data-ttu-id="532fe-451">&ensp;Version de signature **: 1.327.658.0**</span><span class="sxs-lookup"><span data-stu-id="532fe-451">&ensp;Signature version: **1.327.658.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="532fe-452">Correctifs</span><span class="sxs-lookup"><span data-stu-id="532fe-452">Fixes</span></span>
- <span data-ttu-id="532fe-453">Aucun</span><span class="sxs-lookup"><span data-stu-id="532fe-453">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="532fe-454">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="532fe-454">Additional information</span></span>
- <span data-ttu-id="532fe-455">Signatures de l'Antivirus Microsoft Defender actualisées</span><span class="sxs-lookup"><span data-stu-id="532fe-455">Refreshed Microsoft Defender Antivirus signatures</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="532fe-456">1.1.2011.01</span><span class="sxs-lookup"><span data-stu-id="532fe-456">1.1.2011.01</span></span></summary>

<span data-ttu-id="532fe-457">&ensp;Version du package **: 1.1.2011.01**  </span><span class="sxs-lookup"><span data-stu-id="532fe-457">&ensp;Package version: **1.1.2011.01**  </span></span>  
<span data-ttu-id="532fe-458">&ensp;Version de la plateforme **: 4.18.2009.7**</span><span class="sxs-lookup"><span data-stu-id="532fe-458">&ensp;Platform version: **4.18.2009.7**</span></span>  
<span data-ttu-id="532fe-459">&ensp;Version du moteur **: 1.1.17600.5**</span><span class="sxs-lookup"><span data-stu-id="532fe-459">&ensp;Engine version: **1.1.17600.5**</span></span>  
<span data-ttu-id="532fe-460">&ensp;Version de signature **: 1.327.344.0**</span><span class="sxs-lookup"><span data-stu-id="532fe-460">&ensp;Signature version: **1.327.344.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="532fe-461">Correctifs</span><span class="sxs-lookup"><span data-stu-id="532fe-461">Fixes</span></span>
- <span data-ttu-id="532fe-462">Aucun</span><span class="sxs-lookup"><span data-stu-id="532fe-462">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="532fe-463">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="532fe-463">Additional information</span></span>
- <span data-ttu-id="532fe-464">Aucun</span><span class="sxs-lookup"><span data-stu-id="532fe-464">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="532fe-465">1.1.2009.10</span><span class="sxs-lookup"><span data-stu-id="532fe-465">1.1.2009.10</span></span></summary>

<span data-ttu-id="532fe-466">&ensp;Version du package **: 1.1.2011.01**  </span><span class="sxs-lookup"><span data-stu-id="532fe-466">&ensp;Package version: **1.1.2011.01**  </span></span>  
<span data-ttu-id="532fe-467">&ensp;Version de la plateforme **: 4.18.2008.9** </span><span class="sxs-lookup"><span data-stu-id="532fe-467">&ensp;Platform version: **4.18.2008.9** </span></span>  
<span data-ttu-id="532fe-468">&ensp;Version du moteur **: 1.1.17400.5**</span><span class="sxs-lookup"><span data-stu-id="532fe-468">&ensp;Engine version: **1.1.17400.5**</span></span>  
<span data-ttu-id="532fe-469">&ensp;Version de signature **: 1.327.2216.0**</span><span class="sxs-lookup"><span data-stu-id="532fe-469">&ensp;Signature version: **1.327.2216.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="532fe-470">Correctifs</span><span class="sxs-lookup"><span data-stu-id="532fe-470">Fixes</span></span>
- <span data-ttu-id="532fe-471">Aucun</span><span class="sxs-lookup"><span data-stu-id="532fe-471">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="532fe-472">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="532fe-472">Additional information</span></span>
- <span data-ttu-id="532fe-473">Prise en charge supplémentaire des images d'installation du système d'exploitation windows 10 RS1 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="532fe-473">Added support for Windows 10 RS1 or later OS install images.</span></span>  
<br/>
</details>

## <a name="additional-resources"></a><span data-ttu-id="532fe-474">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="532fe-474">Additional resources</span></span>

| <span data-ttu-id="532fe-475">Article</span><span class="sxs-lookup"><span data-stu-id="532fe-475">Article</span></span> | <span data-ttu-id="532fe-476">Description</span><span class="sxs-lookup"><span data-stu-id="532fe-476">Description</span></span>  |
|:---|:---|
|[<span data-ttu-id="532fe-477">Mise à jour de Microsoft Defender pour les images d'installation du système d'exploitation Windows</span><span class="sxs-lookup"><span data-stu-id="532fe-477">Microsoft Defender update for Windows operating system installation images</span></span>](https://support.microsoft.com/help/4568292/defender-update-for-windows-operating-system-installation-images)  | <span data-ttu-id="532fe-478">Passer en revue les packages de mise à jour anti-programme malveillant pour vos images d'installation du système d'exploitation (fichiers WIM et VHD).</span><span class="sxs-lookup"><span data-stu-id="532fe-478">Review antimalware update packages for your OS installation images (WIM and VHD files).</span></span> <span data-ttu-id="532fe-479">Obtenez les mises à jour de l'Antivirus Microsoft Defender pour les images d'installation de Windows 10 (éditions Entreprise, Professionnel et Famille), Windows Server 2019 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="532fe-479">Get Microsoft Defender Antivirus updates for Windows 10 (Enterprise, Pro, and Home editions), Windows Server 2019, and Windows Server 2016 installation images.</span></span>  |
|[<span data-ttu-id="532fe-480">Gérer le téléchargement et l'application des mises à jour de protection</span><span class="sxs-lookup"><span data-stu-id="532fe-480">Manage how protection updates are downloaded and applied</span></span>](manage-protection-updates-microsoft-defender-antivirus.md) | <span data-ttu-id="532fe-481">Les mises à jour de protection peuvent être mises à jour via de nombreuses sources.</span><span class="sxs-lookup"><span data-stu-id="532fe-481">Protection updates can be delivered through many sources.</span></span> |
|[<span data-ttu-id="532fe-482">Gérer le moment où les mises à jour de protection doivent être téléchargées et appliquées</span><span class="sxs-lookup"><span data-stu-id="532fe-482">Manage when protection updates should be downloaded and applied</span></span>](manage-protection-update-schedule-microsoft-defender-antivirus.md) | <span data-ttu-id="532fe-483">Vous pouvez planifier le téléchargement des mises à jour de la protection.</span><span class="sxs-lookup"><span data-stu-id="532fe-483">You can schedule when protection updates should be downloaded.</span></span> |
|[<span data-ttu-id="532fe-484">Gérer les mises à jour des points de terminaison qui ne sont plus à jour</span><span class="sxs-lookup"><span data-stu-id="532fe-484">Manage updates for endpoints that are out of date</span></span>](manage-outdated-endpoints-microsoft-defender-antivirus.md) | <span data-ttu-id="532fe-485">Si un point de terminaison manque une mise à jour ou une analyse programmée, vous pouvez forcer une mise à jour ou une analyse la prochaine fois qu'un utilisateur se signe.</span><span class="sxs-lookup"><span data-stu-id="532fe-485">If an endpoint misses an update or scheduled scan, you can force an update or scan the next time a user signs in.</span></span> |
|[<span data-ttu-id="532fe-486">Gérer les mises à jour forcées en fonction des événements</span><span class="sxs-lookup"><span data-stu-id="532fe-486">Manage event-based forced updates</span></span>](manage-event-based-updates-microsoft-defender-antivirus.md) | <span data-ttu-id="532fe-487">Vous pouvez définir des mises à jour de protection à télécharger au démarrage ou après certains événements de protection livrés par le cloud.</span><span class="sxs-lookup"><span data-stu-id="532fe-487">You can set protection updates to be downloaded at startup or after certain cloud-delivered protection events.</span></span> |
|[<span data-ttu-id="532fe-488">Gérer les mises à jour pour les appareils mobiles et les machines virtuelles</span><span class="sxs-lookup"><span data-stu-id="532fe-488">Manage updates for mobile devices and virtual machines (VMs)</span></span>](manage-updates-mobile-devices-vms-microsoft-defender-antivirus.md)| <span data-ttu-id="532fe-489">Vous pouvez spécifier des paramètres, par exemple si des mises à jour doivent être mises à jour sur l'alimentation de la batterie, qui sont particulièrement utiles pour les appareils mobiles et les ordinateurs virtuels.</span><span class="sxs-lookup"><span data-stu-id="532fe-489">You can specify settings, such as whether updates should occur on battery power, that are especially useful for mobile devices and virtual machines.</span></span> |
