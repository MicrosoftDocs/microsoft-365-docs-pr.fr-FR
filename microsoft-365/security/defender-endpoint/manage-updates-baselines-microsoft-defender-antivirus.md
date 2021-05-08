---
title: Gérer les mises Antivirus Microsoft Defender jour et appliquer les lignes de base
description: Gérer la façon dont Antivirus Microsoft Defender reçoit les mises à jour de protection et de produit.
keywords: mises à jour, bases de référence de sécurité, protection, planifier des mises à jour, forcer les mises à jour, mises à jour mobiles, wsus
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
ms.openlocfilehash: 92f903f750ea5e7f2cb971b535c50bfecced65a2
ms.sourcegitcommit: ff20f5b4e3268c7c98a84fb1cbe7db7151596b6d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2021
ms.locfileid: "52242311"
---
# <a name="manage-microsoft-defender-antivirus-updates-and-apply-baselines"></a><span data-ttu-id="ad35b-104">Gérer les mises Antivirus Microsoft Defender jour et appliquer les lignes de base</span><span class="sxs-lookup"><span data-stu-id="ad35b-104">Manage Microsoft Defender Antivirus updates and apply baselines</span></span>

<span data-ttu-id="ad35b-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="ad35b-105">**Applies to:**</span></span>

- [<span data-ttu-id="ad35b-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="ad35b-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)
- <span data-ttu-id="ad35b-107">Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="ad35b-107">Microsoft Defender Antivirus</span></span>

<span data-ttu-id="ad35b-108">Il existe deux types de mises à jour liées à la mise Antivirus Microsoft Defender jour :</span><span class="sxs-lookup"><span data-stu-id="ad35b-108">There are two types of updates related to keeping Microsoft Defender Antivirus up to date:</span></span>

- <span data-ttu-id="ad35b-109">Mises à jour de l’intelligence de la sécurité</span><span class="sxs-lookup"><span data-stu-id="ad35b-109">Security intelligence updates</span></span>
- <span data-ttu-id="ad35b-110">Mises à jour de produit</span><span class="sxs-lookup"><span data-stu-id="ad35b-110">Product updates</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ad35b-111">Le Antivirus Microsoft Defender à jour est essentiel pour garantir que vos appareils disposent des dernières technologies et fonctionnalités nécessaires pour se protéger contre les nouveaux programmes malveillants et les nouvelles techniques d’attaque.</span><span class="sxs-lookup"><span data-stu-id="ad35b-111">Keeping Microsoft Defender Antivirus up to date is critical to assure your devices have the latest technology and features needed to protect against new malware and attack techniques.</span></span>
> 
> <span data-ttu-id="ad35b-112">Veillez à mettre à jour votre protection antivirus même si Antivirus Microsoft Defender est en cours d’exécution en [mode passif.](./microsoft-defender-antivirus-compatibility.md)</span><span class="sxs-lookup"><span data-stu-id="ad35b-112">Make sure to update your antivirus protection even if Microsoft Defender Antivirus is running in [passive mode](./microsoft-defender-antivirus-compatibility.md).</span></span>
> 
> <span data-ttu-id="ad35b-113">Pour voir le moteur, la plateforme et la date de signature les plus à jour, consultez les mises à jour de l’intelligence de sécurité pour Antivirus Microsoft Defender logiciel [anti-programme](https://www.microsoft.com/en-us/wdsi/defenderupdates)malveillant Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ad35b-113">To see the most current engine, platform, and signature date, visit the [Security intelligence updates for Microsoft Defender Antivirus and other Microsoft antimalware](https://www.microsoft.com/en-us/wdsi/defenderupdates).</span></span>

## <a name="security-intelligence-updates"></a><span data-ttu-id="ad35b-114">Mises à jour de l’intelligence de la sécurité</span><span class="sxs-lookup"><span data-stu-id="ad35b-114">Security intelligence updates</span></span>

<span data-ttu-id="ad35b-115">Antivirus Microsoft Defender utilise la protection fournie par le [cloud](cloud-protection-microsoft-defender-antivirus.md) (également appelée Microsoft Advanced Protection Service ou MAPS) et télécharge régulièrement les mises à jour de l’intelligence de sécurité pour fournir une protection.</span><span class="sxs-lookup"><span data-stu-id="ad35b-115">Microsoft Defender Antivirus uses [cloud-delivered protection](cloud-protection-microsoft-defender-antivirus.md) (also called the Microsoft Advanced Protection Service or MAPS) and periodically downloads security intelligence updates to provide protection.</span></span>

> [!NOTE]
> <span data-ttu-id="ad35b-116">Les mises à jour sont publiées sous les numéros de la Ko ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="ad35b-116">Updates are released under the below KB numbers:</span></span>  
> <span data-ttu-id="ad35b-117">Antivirus Microsoft Defender : KB2267602</span><span class="sxs-lookup"><span data-stu-id="ad35b-117">Microsoft Defender Antivirus: KB2267602</span></span>  
> <span data-ttu-id="ad35b-118">System Center Endpoint Protection : KB2461484</span><span class="sxs-lookup"><span data-stu-id="ad35b-118">System Center Endpoint Protection: KB2461484</span></span>

<span data-ttu-id="ad35b-119">La protection cloud est toujours active et nécessite une connexion active à Internet pour fonctionner.</span><span class="sxs-lookup"><span data-stu-id="ad35b-119">Cloud-delivered protection is always on and requires an active connection to the Internet to function.</span></span> <span data-ttu-id="ad35b-120">Les mises à jour des informations de sécurité se produisent à une cadence programmée (configurable via une stratégie).</span><span class="sxs-lookup"><span data-stu-id="ad35b-120">Security intelligence updates occur on a scheduled cadence (configurable via policy).</span></span> <span data-ttu-id="ad35b-121">Pour plus d’informations, voir Utiliser la protection fournie par le [cloud microsoft dans Antivirus Microsoft Defender](cloud-protection-microsoft-defender-antivirus.md).</span><span class="sxs-lookup"><span data-stu-id="ad35b-121">For more information, see [Use Microsoft cloud-provided protection in Microsoft Defender Antivirus](cloud-protection-microsoft-defender-antivirus.md).</span></span> 

<span data-ttu-id="ad35b-122">Pour obtenir la liste des mises à jour récentes de l’intelligence de sécurité, voir Les mises à jour d’intelligence de sécurité pour Antivirus Microsoft Defender logiciel [anti-programme](https://www.microsoft.com/en-us/wdsi/defenderupdates)malveillant Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ad35b-122">For a list of recent security intelligence updates, see [Security intelligence updates for Microsoft Defender Antivirus and other Microsoft antimalware](https://www.microsoft.com/en-us/wdsi/defenderupdates).</span></span>

<span data-ttu-id="ad35b-123">Les mises à jour du moteur sont incluses dans les mises à jour de l’intelligence de sécurité et sont publiées à une cadence mensuelle.</span><span class="sxs-lookup"><span data-stu-id="ad35b-123">Engine updates are included with security intelligence updates and are released on a monthly cadence.</span></span>

## <a name="product-updates"></a><span data-ttu-id="ad35b-124">Mises à jour de produit</span><span class="sxs-lookup"><span data-stu-id="ad35b-124">Product updates</span></span>

<span data-ttu-id="ad35b-125">Antivirus Microsoft Defender nécessite des mises à jour [mensuelles (KB4052623)](https://support.microsoft.com/help/4052623/update-for-windows-defender-antimalware-platform) *(connues* sous le nom de mises à jour de plateforme) et recevra des mises à jour de fonctionnalités majeures avec Windows 10 de publication.</span><span class="sxs-lookup"><span data-stu-id="ad35b-125">Microsoft Defender Antivirus requires [monthly updates (KB4052623)](https://support.microsoft.com/help/4052623/update-for-windows-defender-antimalware-platform) (known as *platform updates*), and will receive major feature updates alongside Windows 10 releases.</span></span>

<span data-ttu-id="ad35b-126">Vous pouvez gérer la distribution des mises à jour via l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="ad35b-126">You can manage the distribution of updates through one of the following methods:</span></span> 

- [<span data-ttu-id="ad35b-127">Windows Server Update Service (WSUS)</span><span class="sxs-lookup"><span data-stu-id="ad35b-127">Windows Server Update Service (WSUS)</span></span>](/mem/configmgr/protect/deploy-use/endpoint-definitions-wsus#to-synchronize-endpoint-protection-definition-updates-in-standalone-wsus)
- [<span data-ttu-id="ad35b-128">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ad35b-128">Microsoft Endpoint Configuration Manager</span></span>](/configmgr/sum/understand/software-updates-introduction)
- <span data-ttu-id="ad35b-129">La méthode habituelle que vous utilisez pour déployer Microsoft et Windows mises à jour aux points de terminaison de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="ad35b-129">The usual method you use to deploy Microsoft and Windows updates to endpoints in your network.</span></span>

<span data-ttu-id="ad35b-130">Pour plus d’informations, [voir Gérer les sources pour les mises à jour Antivirus Microsoft Defender protection des données.](/mem/configmgr/protect/deploy-use/endpoint-definitions-wsus#to-synchronize-endpoint-protection-definition-updates-in-standalone-wsus)</span><span class="sxs-lookup"><span data-stu-id="ad35b-130">For more information, see [Manage the sources for Microsoft Defender Antivirus protection updates](/mem/configmgr/protect/deploy-use/endpoint-definitions-wsus#to-synchronize-endpoint-protection-definition-updates-in-standalone-wsus).</span></span>

> [!NOTE]
> <span data-ttu-id="ad35b-131">Les mises à jour mensuelles sont publiées par phases, ce qui entraîne la mise à jour de plusieurs packages dans vos services de mise à jour [de serveur Window.](/windows-server/administration/windows-server-update-services/get-started/windows-server-update-services-wsus)</span><span class="sxs-lookup"><span data-stu-id="ad35b-131">Monthly updates are released in phases, resulting in multiple packages visible in your [Window Server Update Services](/windows-server/administration/windows-server-update-services/get-started/windows-server-update-services-wsus).</span></span>

## <a name="monthly-platform-and-engine-versions"></a><span data-ttu-id="ad35b-132">Versions mensuelles de la plateforme et du moteur</span><span class="sxs-lookup"><span data-stu-id="ad35b-132">Monthly platform and engine versions</span></span>

<span data-ttu-id="ad35b-133">Pour plus d’informations sur la mise à jour ou l’installation de la mise à jour de plateforme, voir Mise à [jour Windows Defender plateforme anti-programme malveillant.](https://support.microsoft.com/help/4052623/update-for-windows-defender-antimalware-platform)</span><span class="sxs-lookup"><span data-stu-id="ad35b-133">For information how to update or install the platform update, see [Update for Windows Defender antimalware platform](https://support.microsoft.com/help/4052623/update-for-windows-defender-antimalware-platform).</span></span>

<span data-ttu-id="ad35b-134">Toutes nos mises à jour contiennent</span><span class="sxs-lookup"><span data-stu-id="ad35b-134">All our updates contain</span></span> 
- <span data-ttu-id="ad35b-135">améliorations des performances ;</span><span class="sxs-lookup"><span data-stu-id="ad35b-135">performance improvements;</span></span>
- <span data-ttu-id="ad35b-136">améliorations en matière de serviceabilité ; et</span><span class="sxs-lookup"><span data-stu-id="ad35b-136">serviceability improvements; and</span></span> 
- <span data-ttu-id="ad35b-137">améliorations de l’intégration (Cloud, Microsoft 365 Defender).</span><span class="sxs-lookup"><span data-stu-id="ad35b-137">integration improvements (Cloud, Microsoft 365 Defender).</span></span>
<br/>
<details>
<summary> <span data-ttu-id="ad35b-138">Avril-2021 (plateforme : 4.19.2104.9| Moteur : 1.1.18100.5)</span><span class="sxs-lookup"><span data-stu-id="ad35b-138">April-2021 (Platform: 4.19.2104.9| Engine: 1.1.18100.5)</span></span></summary>

<span data-ttu-id="ad35b-139">&ensp;Version de mise à jour des informations de sécurité **: 1.337.2.0**</span><span class="sxs-lookup"><span data-stu-id="ad35b-139">&ensp;Security intelligence update version: **1.337.2.0**</span></span>  
<span data-ttu-id="ad35b-140">&ensp;Publication : **1er avril 2021**</span><span class="sxs-lookup"><span data-stu-id="ad35b-140">&ensp;Released: **April 1, 2021**</span></span>  
<span data-ttu-id="ad35b-141">&ensp;Plateforme : **4.19.2104.9**</span><span class="sxs-lookup"><span data-stu-id="ad35b-141">&ensp;Platform: **4.19.2104.9**</span></span>  
<span data-ttu-id="ad35b-142">&ensp;Moteur : **1.1.18100.5**</span><span class="sxs-lookup"><span data-stu-id="ad35b-142">&ensp;Engine: **1.1.18100.5**</span></span>  
<span data-ttu-id="ad35b-143">&ensp;Phase de prise en charge **: Mises à jour critiques et de sécurité**</span><span class="sxs-lookup"><span data-stu-id="ad35b-143">&ensp;Support phase: **Security and Critical Updates**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="ad35b-144">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="ad35b-144">What's new</span></span>
- <span data-ttu-id="ad35b-145">Logique de surveillance du comportement supplémentaire</span><span class="sxs-lookup"><span data-stu-id="ad35b-145">Additional behavior monitoring logic</span></span>
- <span data-ttu-id="ad35b-146">Détection améliorée du keylogger en mode noyau</span><span class="sxs-lookup"><span data-stu-id="ad35b-146">Improved kernel mode keylogger detection</span></span>

### <a name="known-issues"></a><span data-ttu-id="ad35b-147">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="ad35b-147">Known Issues</span></span>
<span data-ttu-id="ad35b-148">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="ad35b-148">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="ad35b-149">Mars-2021 (plateforme : 4.19.2103.7 | Moteur : 1.1.18000.5)</span><span class="sxs-lookup"><span data-stu-id="ad35b-149">March-2021 (Platform: 4.19.2103.7 | Engine: 1.1.18000.5)</span></span></summary>

<span data-ttu-id="ad35b-150">&ensp;Version de mise à jour des informations de sécurité **: 1.335.36.0**</span><span class="sxs-lookup"><span data-stu-id="ad35b-150">&ensp;Security intelligence update version: **1.335.36.0**</span></span>  
<span data-ttu-id="ad35b-151">&ensp;Publication : **1er avril 2021**</span><span class="sxs-lookup"><span data-stu-id="ad35b-151">&ensp;Released: **April 1, 2021**</span></span>  
<span data-ttu-id="ad35b-152">&ensp;Plateforme : **4.19.2103.7**</span><span class="sxs-lookup"><span data-stu-id="ad35b-152">&ensp;Platform: **4.19.2103.7**</span></span>  
<span data-ttu-id="ad35b-153">&ensp;Moteur : **1.1.18000.5**</span><span class="sxs-lookup"><span data-stu-id="ad35b-153">&ensp;Engine: **1.1.18000.5**</span></span>  
<span data-ttu-id="ad35b-154">&ensp;Phase de prise en charge **: Mises à jour critiques et de sécurité**</span><span class="sxs-lookup"><span data-stu-id="ad35b-154">&ensp;Support phase: **Security and Critical Updates**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="ad35b-155">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="ad35b-155">What's new</span></span>

- <span data-ttu-id="ad35b-156">Amélioration du moteur d’analyse du comportement</span><span class="sxs-lookup"><span data-stu-id="ad35b-156">Improvement to the Behavior Monitoring engine</span></span> 
- <span data-ttu-id="ad35b-157">Préventions d’attaques par force brute du réseau étendu</span><span class="sxs-lookup"><span data-stu-id="ad35b-157">Expanded network brute-force-attack mitigations</span></span> 
- <span data-ttu-id="ad35b-158">Génération d’événements de tentative de falsification en échec supplémentaires lorsque la [protection](prevent-changes-to-security-settings-with-tamper-protection.md) contre la falsification est activée</span><span class="sxs-lookup"><span data-stu-id="ad35b-158">Additional failed tampering attempt event generation when [Tamper Protection](prevent-changes-to-security-settings-with-tamper-protection.md) is enabled</span></span>

### <a name="known-issues"></a><span data-ttu-id="ad35b-159">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="ad35b-159">Known Issues</span></span>
<span data-ttu-id="ad35b-160">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="ad35b-160">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="ad35b-161">Février-2021 (plateforme : 4.19.2102.3 | Moteur : 1.1.17900.7)</span><span class="sxs-lookup"><span data-stu-id="ad35b-161">February-2021 (Platform: 4.19.2102.3 | Engine: 1.1.17900.7)</span></span></summary>

<span data-ttu-id="ad35b-162">&ensp;Version de mise à jour des informations de sécurité **: 1.333.7.0**</span><span class="sxs-lookup"><span data-stu-id="ad35b-162">&ensp;Security intelligence update version: **1.333.7.0**</span></span>  
<span data-ttu-id="ad35b-163">&ensp;Publication : **9 mars 2021**</span><span class="sxs-lookup"><span data-stu-id="ad35b-163">&ensp;Released: **March 9, 2021**</span></span>  
<span data-ttu-id="ad35b-164">&ensp;Plateforme : **4.19.2102.3**</span><span class="sxs-lookup"><span data-stu-id="ad35b-164">&ensp;Platform: **4.19.2102.3**</span></span>  
<span data-ttu-id="ad35b-165">&ensp;Moteur : **1.1.17900.7**</span><span class="sxs-lookup"><span data-stu-id="ad35b-165">&ensp;Engine: **1.1.17900.7**</span></span>  
<span data-ttu-id="ad35b-166">&ensp;Phase de prise en charge **: Mises à jour critiques et de sécurité**</span><span class="sxs-lookup"><span data-stu-id="ad35b-166">&ensp;Support phase: **Security and Critical Updates**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="ad35b-167">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="ad35b-167">What's new</span></span>

- <span data-ttu-id="ad35b-168">Amélioration de la récupération du service par le biais [de la protection contre la falsification](prevent-changes-to-security-settings-with-tamper-protection.md)</span><span class="sxs-lookup"><span data-stu-id="ad35b-168">Improved service recovery through [tamper protection](prevent-changes-to-security-settings-with-tamper-protection.md)</span></span>
- <span data-ttu-id="ad35b-169">Étendre l’étendue de la protection contre la falsification</span><span class="sxs-lookup"><span data-stu-id="ad35b-169">Extend tamper protection scope</span></span>

### <a name="known-issues"></a><span data-ttu-id="ad35b-170">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="ad35b-170">Known Issues</span></span>
<span data-ttu-id="ad35b-171">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="ad35b-171">No known issues</span></span>  
<br/>
</details>

### <a name="previous-version-updates-technical-upgrade-support-only"></a><span data-ttu-id="ad35b-172">Mises à jour de version précédente : prise en charge de la mise à niveau technique uniquement</span><span class="sxs-lookup"><span data-stu-id="ad35b-172">Previous version updates: Technical upgrade support only</span></span>

<span data-ttu-id="ad35b-173">Après la publication d’une nouvelle version de package, la prise en charge des deux versions précédentes est réduite au support technique uniquement.</span><span class="sxs-lookup"><span data-stu-id="ad35b-173">After a new package version is released, support for the previous two versions is reduced to technical support only.</span></span> <span data-ttu-id="ad35b-174">Les versions antérieures à celles répertoriées dans cette section sont fournies uniquement pour la prise en charge de la mise à niveau technique.</span><span class="sxs-lookup"><span data-stu-id="ad35b-174">Versions older than that are listed in this section, and are provided for technical upgrade support only.</span></span> 
<br/><br/>
<details>
<summary> <span data-ttu-id="ad35b-175">Janvier-2021 (plateforme : 4.18.2101.9 | Moteur : 1.1.17800.5)</span><span class="sxs-lookup"><span data-stu-id="ad35b-175">January-2021 (Platform: 4.18.2101.9 | Engine: 1.1.17800.5)</span></span></summary>

<span data-ttu-id="ad35b-176">&ensp;Version de mise à jour des informations de sécurité **: 1.327.1854.0**</span><span class="sxs-lookup"><span data-stu-id="ad35b-176">&ensp;Security intelligence update version: **1.327.1854.0**</span></span>  
<span data-ttu-id="ad35b-177">&ensp;Publication : **2 février 2021**</span><span class="sxs-lookup"><span data-stu-id="ad35b-177">&ensp;Released: **February 2, 2021**</span></span>  
<span data-ttu-id="ad35b-178">&ensp;Plateforme : **4.18.2101.9**</span><span class="sxs-lookup"><span data-stu-id="ad35b-178">&ensp;Platform: **4.18.2101.9**</span></span>  
<span data-ttu-id="ad35b-179">&ensp;Moteur : **1.1.17800.5**</span><span class="sxs-lookup"><span data-stu-id="ad35b-179">&ensp;Engine: **1.1.17800.5**</span></span>  
<span data-ttu-id="ad35b-180">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="ad35b-180">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="ad35b-181">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="ad35b-181">What's new</span></span>

- <span data-ttu-id="ad35b-182">Améliorations de la détection d’exploits shellcode</span><span class="sxs-lookup"><span data-stu-id="ad35b-182">Shellcode exploit detection improvements</span></span>
- <span data-ttu-id="ad35b-183">Visibilité accrue des tentatives de vol d’informations d’identification</span><span class="sxs-lookup"><span data-stu-id="ad35b-183">Increased visibility for credential stealing attempts</span></span>
- <span data-ttu-id="ad35b-184">Améliorations des fonctionnalités antitampering dans Antivirus Microsoft Defender services</span><span class="sxs-lookup"><span data-stu-id="ad35b-184">Improvements in antitampering features in Microsoft Defender Antivirus services</span></span>
- <span data-ttu-id="ad35b-185">Prise en charge améliorée de l ARM éulation x64</span><span class="sxs-lookup"><span data-stu-id="ad35b-185">Improved support for ARM x64 emulation</span></span>
- <span data-ttu-id="ad35b-186">Correctif : PEPT notification de blocage reste dans l’historique des menaces après la détection initiale de la protection en temps réel</span><span class="sxs-lookup"><span data-stu-id="ad35b-186">Fix: EDR Block notification remains in threat history after real-time protection performed initial detection</span></span>

### <a name="known-issues"></a><span data-ttu-id="ad35b-187">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="ad35b-187">Known Issues</span></span>
<span data-ttu-id="ad35b-188">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="ad35b-188">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="ad35b-189">Novembre-2020 (plateforme : 4.18.2011.6 | Moteur : 1.1.17700.4)</span><span class="sxs-lookup"><span data-stu-id="ad35b-189">November-2020 (Platform: 4.18.2011.6 | Engine: 1.1.17700.4)</span></span></summary>

<span data-ttu-id="ad35b-190">&ensp;Version de mise à jour des informations de sécurité **: 1.327.1854.0**</span><span class="sxs-lookup"><span data-stu-id="ad35b-190">&ensp;Security intelligence update version: **1.327.1854.0**</span></span>  
<span data-ttu-id="ad35b-191">&ensp;Publication : **03 décembre 2020**</span><span class="sxs-lookup"><span data-stu-id="ad35b-191">&ensp;Released: **December 03, 2020**</span></span>  
<span data-ttu-id="ad35b-192">&ensp;Plateforme : **4.18.2011.6**</span><span class="sxs-lookup"><span data-stu-id="ad35b-192">&ensp;Platform: **4.18.2011.6**</span></span>  
<span data-ttu-id="ad35b-193">&ensp;Moteur : **1.1.17700.4**</span><span class="sxs-lookup"><span data-stu-id="ad35b-193">&ensp;Engine: **1.1.17700.4**</span></span>  
<span data-ttu-id="ad35b-194">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="ad35b-194">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="ad35b-195">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="ad35b-195">What's new</span></span>

- <span data-ttu-id="ad35b-196">Amélioration de la [journalisation de la prise en](/windows/security/threat-protection/microsoft-defender-smartscreen/microsoft-defender-smartscreen-overview) charge de l’état SmartScreen</span><span class="sxs-lookup"><span data-stu-id="ad35b-196">Improved [SmartScreen](/windows/security/threat-protection/microsoft-defender-smartscreen/microsoft-defender-smartscreen-overview) status support logging</span></span>

### <a name="known-issues"></a><span data-ttu-id="ad35b-197">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="ad35b-197">Known Issues</span></span>
<span data-ttu-id="ad35b-198">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="ad35b-198">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="ad35b-199">Octobre-2020 (plateforme : 4.18.2010.7 | Moteur : 1.1.17600.5)</span><span class="sxs-lookup"><span data-stu-id="ad35b-199">October-2020 (Platform: 4.18.2010.7 | Engine: 1.1.17600.5)</span></span></summary>

<span data-ttu-id="ad35b-200">&ensp;Version de mise à jour des informations de sécurité **: 1.327.7.0**</span><span class="sxs-lookup"><span data-stu-id="ad35b-200">&ensp;Security intelligence update version: **1.327.7.0**</span></span>  
<span data-ttu-id="ad35b-201">&ensp;Publication : **29 octobre 2020**</span><span class="sxs-lookup"><span data-stu-id="ad35b-201">&ensp;Released: **October 29, 2020**</span></span>  
<span data-ttu-id="ad35b-202">&ensp;Plateforme : **4.18.2010.7**</span><span class="sxs-lookup"><span data-stu-id="ad35b-202">&ensp;Platform: **4.18.2010.7**</span></span>  
<span data-ttu-id="ad35b-203">&ensp;Moteur : **1.1.17600.5**</span><span class="sxs-lookup"><span data-stu-id="ad35b-203">&ensp;Engine: **1.1.17600.5**</span></span>  
<span data-ttu-id="ad35b-204">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="ad35b-204">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="ad35b-205">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="ad35b-205">What's new</span></span>

- <span data-ttu-id="ad35b-206">Nouvelles descriptions pour les catégories de menaces spéciales</span><span class="sxs-lookup"><span data-stu-id="ad35b-206">New descriptions for special threat categories</span></span>
- <span data-ttu-id="ad35b-207">Fonctionnalités d’émulation améliorées</span><span class="sxs-lookup"><span data-stu-id="ad35b-207">Improved emulation capabilities</span></span>
- <span data-ttu-id="ad35b-208">Fonctionnalités améliorées d’autoriser/bloquer l’adresse hôte</span><span class="sxs-lookup"><span data-stu-id="ad35b-208">Improved host address allow/block capabilities</span></span>
- <span data-ttu-id="ad35b-209">Nouvelle option dans le programme CSP Defender pour ignorer la fusion des exclusions des utilisateurs locaux</span><span class="sxs-lookup"><span data-stu-id="ad35b-209">New option in Defender CSP to Ignore merging of local user exclusions</span></span>

### <a name="known-issues"></a><span data-ttu-id="ad35b-210">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="ad35b-210">Known Issues</span></span>

<span data-ttu-id="ad35b-211">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="ad35b-211">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="ad35b-212">Septembre-2020 (plateforme : 4.18.2009.7 | Moteur : 1.1.17500.4)</span><span class="sxs-lookup"><span data-stu-id="ad35b-212">September-2020 (Platform: 4.18.2009.7 | Engine: 1.1.17500.4)</span></span></summary>

<span data-ttu-id="ad35b-213">&ensp;Version de mise à jour des informations de sécurité **: 1.325.10.0**</span><span class="sxs-lookup"><span data-stu-id="ad35b-213">&ensp;Security intelligence update version: **1.325.10.0**</span></span>  
<span data-ttu-id="ad35b-214">&ensp;Publication : **01 octobre 2020**</span><span class="sxs-lookup"><span data-stu-id="ad35b-214">&ensp;Released: **October 01, 2020**</span></span>  
<span data-ttu-id="ad35b-215">&ensp;Plateforme : **4.18.2009.7**</span><span class="sxs-lookup"><span data-stu-id="ad35b-215">&ensp;Platform: **4.18.2009.7**</span></span>  
<span data-ttu-id="ad35b-216">&ensp;Moteur : **1.1.17500.4**</span><span class="sxs-lookup"><span data-stu-id="ad35b-216">&ensp;Engine: **1.1.17500.4**</span></span>  
<span data-ttu-id="ad35b-217">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="ad35b-217">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="ad35b-218">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="ad35b-218">What's new</span></span>

- <span data-ttu-id="ad35b-219">Des autorisations d’administrateur sont requises pour restaurer les fichiers en quarantaine</span><span class="sxs-lookup"><span data-stu-id="ad35b-219">Admin permissions are required to restore files in quarantine</span></span>
- <span data-ttu-id="ad35b-220">Les événements au format XML sont désormais pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad35b-220">XML formatted events are now supported</span></span>
- <span data-ttu-id="ad35b-221">Prise en charge du programme CSP pour ignorer les fusions d’exclusions</span><span class="sxs-lookup"><span data-stu-id="ad35b-221">CSP support for ignoring exclusion merges</span></span>
- <span data-ttu-id="ad35b-222">Nouvelles interfaces de gestion pour :</span><span class="sxs-lookup"><span data-stu-id="ad35b-222">New management interfaces for:</span></span>
   - <span data-ttu-id="ad35b-223">UDP Inspection</span><span class="sxs-lookup"><span data-stu-id="ad35b-223">UDP Inspection</span></span>
   - <span data-ttu-id="ad35b-224">Protection du réseau sur Server 2019</span><span class="sxs-lookup"><span data-stu-id="ad35b-224">Network Protection on Server 2019</span></span>
   - <span data-ttu-id="ad35b-225">Exclusions d’adresses IP pour la protection du réseau</span><span class="sxs-lookup"><span data-stu-id="ad35b-225">IP Address exclusions for Network Protection</span></span>
- <span data-ttu-id="ad35b-226">Meilleure visibilité des mesures du TPM</span><span class="sxs-lookup"><span data-stu-id="ad35b-226">Improved visibility into TPM measurements</span></span>
- <span data-ttu-id="ad35b-227">Amélioration de Office module VBA</span><span class="sxs-lookup"><span data-stu-id="ad35b-227">Improved Office VBA module scanning</span></span>

### <a name="known-issues"></a><span data-ttu-id="ad35b-228">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="ad35b-228">Known Issues</span></span>

<span data-ttu-id="ad35b-229">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="ad35b-229">No known issues</span></span>  
<br/>
</details>
<details>
<summary> <span data-ttu-id="ad35b-230">Août-2020 (plateforme : 4.18.2008.9 | Moteur : 1.1.17400.5)</span><span class="sxs-lookup"><span data-stu-id="ad35b-230">August-2020 (Platform: 4.18.2008.9 | Engine: 1.1.17400.5)</span></span></summary>

<span data-ttu-id="ad35b-231">&ensp;Version de mise à jour des informations de sécurité **: 1.323.9.0**</span><span class="sxs-lookup"><span data-stu-id="ad35b-231">&ensp;Security intelligence update version: **1.323.9.0**</span></span>  
<span data-ttu-id="ad35b-232">&ensp;Publication : **27 août 2020**</span><span class="sxs-lookup"><span data-stu-id="ad35b-232">&ensp;Released: **August 27, 2020**</span></span>  
<span data-ttu-id="ad35b-233">&ensp;Plateforme : **4.18.2008.9**</span><span class="sxs-lookup"><span data-stu-id="ad35b-233">&ensp;Platform: **4.18.2008.9**</span></span>  
<span data-ttu-id="ad35b-234">&ensp;Moteur : **1.1.17400.5**</span><span class="sxs-lookup"><span data-stu-id="ad35b-234">&ensp;Engine: **1.1.17400.5**</span></span>  
<span data-ttu-id="ad35b-235">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="ad35b-235">&ensp;Support phase: **Technical upgrade support (only)**</span></span>

### <a name="whats-new"></a><span data-ttu-id="ad35b-236">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="ad35b-236">What's new</span></span>

- <span data-ttu-id="ad35b-237">Ajouter d’autres événements de télémétrie</span><span class="sxs-lookup"><span data-stu-id="ad35b-237">Add more telemetry events</span></span>
- <span data-ttu-id="ad35b-238">Télémétrie améliorée des événements d’analyse</span><span class="sxs-lookup"><span data-stu-id="ad35b-238">Improved scan event telemetry</span></span>
- <span data-ttu-id="ad35b-239">Amélioration de la surveillance du comportement pour les analyses de mémoire</span><span class="sxs-lookup"><span data-stu-id="ad35b-239">Improved behavior monitoring for memory scans</span></span>
- <span data-ttu-id="ad35b-240">Amélioration de l’analyse des flux de macros</span><span class="sxs-lookup"><span data-stu-id="ad35b-240">Improved macro streams scanning</span></span>
- <span data-ttu-id="ad35b-241">Ajouté à `AMRunningMode` la Get-MpComputerStatus cmdlet PowerShell</span><span class="sxs-lookup"><span data-stu-id="ad35b-241">Added `AMRunningMode` to Get-MpComputerStatus PowerShell cmdlet</span></span>
- <span data-ttu-id="ad35b-242">[DisableAntiSpyware](/windows-hardware/customize/desktop/unattend/security-malware-windows-defender-disableantispyware) est ignoré.</span><span class="sxs-lookup"><span data-stu-id="ad35b-242">[DisableAntiSpyware](/windows-hardware/customize/desktop/unattend/security-malware-windows-defender-disableantispyware) is ignored.</span></span> <span data-ttu-id="ad35b-243">Antivirus Microsoft Defender s’arrête automatiquement lorsqu’il détecte un autre programme antivirus.</span><span class="sxs-lookup"><span data-stu-id="ad35b-243">Microsoft Defender Antivirus automatically turns itself off when it detects another antivirus program.</span></span>


### <a name="known-issues"></a><span data-ttu-id="ad35b-244">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="ad35b-244">Known Issues</span></span>
<span data-ttu-id="ad35b-245">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="ad35b-245">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="ad35b-246">Juillet-2020 (plateforme : 4.18.2007.8 | Moteur : 1.1.17300.4)</span><span class="sxs-lookup"><span data-stu-id="ad35b-246">July-2020 (Platform: 4.18.2007.8 | Engine: 1.1.17300.4)</span></span></summary>

<span data-ttu-id="ad35b-247">&ensp;Version de mise à jour des informations de sécurité **: 1.321.30.0**</span><span class="sxs-lookup"><span data-stu-id="ad35b-247">&ensp;Security intelligence update version: **1.321.30.0**</span></span>  
<span data-ttu-id="ad35b-248">&ensp;Publication : **28 juillet 2020**</span><span class="sxs-lookup"><span data-stu-id="ad35b-248">&ensp;Released: **July 28, 2020**</span></span>  
<span data-ttu-id="ad35b-249">&ensp;Plateforme : **4.18.2007.8**</span><span class="sxs-lookup"><span data-stu-id="ad35b-249">&ensp;Platform: **4.18.2007.8**</span></span>  
<span data-ttu-id="ad35b-250">&ensp;Moteur : **1.1.17300.4**</span><span class="sxs-lookup"><span data-stu-id="ad35b-250">&ensp;Engine: **1.1.17300.4**</span></span>  
<span data-ttu-id="ad35b-251">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="ad35b-251">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="ad35b-252">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="ad35b-252">What's new</span></span>

- <span data-ttu-id="ad35b-253">Télémétrie améliorée pour BITS</span><span class="sxs-lookup"><span data-stu-id="ad35b-253">Improved telemetry for BITS</span></span>
- <span data-ttu-id="ad35b-254">Validation améliorée du certificat de signature de code Authenticode</span><span class="sxs-lookup"><span data-stu-id="ad35b-254">Improved Authenticode code signing certificate validation</span></span>

### <a name="known-issues"></a><span data-ttu-id="ad35b-255">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="ad35b-255">Known Issues</span></span>
<span data-ttu-id="ad35b-256">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="ad35b-256">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="ad35b-257">Juin-2020 (plateforme : 4.18.2006.10 | Moteur : 1.1.17200.2)</span><span class="sxs-lookup"><span data-stu-id="ad35b-257">June-2020 (Platform: 4.18.2006.10 | Engine: 1.1.17200.2)</span></span></summary>

<span data-ttu-id="ad35b-258">&ensp;Version de mise à jour des informations de sécurité **: 1.319.20.0**</span><span class="sxs-lookup"><span data-stu-id="ad35b-258">&ensp;Security intelligence update version: **1.319.20.0**</span></span>  
<span data-ttu-id="ad35b-259">&ensp;Publication : **22 juin 2020**</span><span class="sxs-lookup"><span data-stu-id="ad35b-259">&ensp;Released: **June 22, 2020**</span></span>  
<span data-ttu-id="ad35b-260">&ensp;Plateforme : **4.18.2006.10**</span><span class="sxs-lookup"><span data-stu-id="ad35b-260">&ensp;Platform: **4.18.2006.10**</span></span>  
<span data-ttu-id="ad35b-261">&ensp;Moteur : **1.1.17200.2**</span><span class="sxs-lookup"><span data-stu-id="ad35b-261">&ensp;Engine: **1.1.17200.2**</span></span>  
<span data-ttu-id="ad35b-262">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="ad35b-262">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="ad35b-263">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="ad35b-263">What's new</span></span>

- <span data-ttu-id="ad35b-264">Possibilité de spécifier [l’emplacement des journaux de support](./collect-diagnostic-data.md)</span><span class="sxs-lookup"><span data-stu-id="ad35b-264">Possibility to specify the [location of the support logs](./collect-diagnostic-data.md)</span></span>
- <span data-ttu-id="ad35b-265">Ignorer l’analyse de rattrapage agressive en mode passif.</span><span class="sxs-lookup"><span data-stu-id="ad35b-265">Skipping aggressive catchup scan in Passive mode.</span></span>
- <span data-ttu-id="ad35b-266">Autoriser Defender à mettre à jour les connexions avec des compteurs</span><span class="sxs-lookup"><span data-stu-id="ad35b-266">Allow Defender to update on metered connections</span></span>
- <span data-ttu-id="ad35b-267">Réglage des performances fixes lorsque la mise en cache est désactivée</span><span class="sxs-lookup"><span data-stu-id="ad35b-267">Fixed performance tuning when caching is disabled</span></span> 
- <span data-ttu-id="ad35b-268">Requête de Registre fixe</span><span class="sxs-lookup"><span data-stu-id="ad35b-268">Fixed registry query</span></span> 
- <span data-ttu-id="ad35b-269">Randomisation du scantime fixe dans ADMX</span><span class="sxs-lookup"><span data-stu-id="ad35b-269">Fixed scantime randomization in ADMX</span></span>

### <a name="known-issues"></a><span data-ttu-id="ad35b-270">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="ad35b-270">Known Issues</span></span>
<span data-ttu-id="ad35b-271">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="ad35b-271">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="ad35b-272">Mai-2020 (plateforme : 4.18.2005.4 | Moteur : 1.1.17100.2)</span><span class="sxs-lookup"><span data-stu-id="ad35b-272">May-2020 (Platform: 4.18.2005.4 | Engine: 1.1.17100.2)</span></span></summary>

<span data-ttu-id="ad35b-273">&ensp;Version de mise à jour des informations de sécurité **: 1.317.20.0**</span><span class="sxs-lookup"><span data-stu-id="ad35b-273">&ensp;Security intelligence update version: **1.317.20.0**</span></span>  
<span data-ttu-id="ad35b-274">&ensp;Publication : **26 mai 2020**</span><span class="sxs-lookup"><span data-stu-id="ad35b-274">&ensp;Released: **May 26, 2020**</span></span>  
<span data-ttu-id="ad35b-275">&ensp;Plateforme : **4.18.2005.4**</span><span class="sxs-lookup"><span data-stu-id="ad35b-275">&ensp;Platform: **4.18.2005.4**</span></span>  
<span data-ttu-id="ad35b-276">&ensp;Moteur : **1.1.17100.2**</span><span class="sxs-lookup"><span data-stu-id="ad35b-276">&ensp;Engine: **1.1.17100.2**</span></span>  
<span data-ttu-id="ad35b-277">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="ad35b-277">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="ad35b-278">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="ad35b-278">What's new</span></span>

- <span data-ttu-id="ad35b-279">Journalisation améliorée des événements d’analyse</span><span class="sxs-lookup"><span data-stu-id="ad35b-279">Improved logging for scan events</span></span>
- <span data-ttu-id="ad35b-280">Amélioration de la gestion des incidents en mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ad35b-280">Improved user mode crash handling.</span></span>
- <span data-ttu-id="ad35b-281">Suivi des événements ajouté pour la protection contre la falsification</span><span class="sxs-lookup"><span data-stu-id="ad35b-281">Added event tracing for Tamper protection</span></span>
- <span data-ttu-id="ad35b-282">Soumission d’exemple AMSI fixe</span><span class="sxs-lookup"><span data-stu-id="ad35b-282">Fixed AMSI Sample submission</span></span>
- <span data-ttu-id="ad35b-283">Blocage du cloud AMSI fixe</span><span class="sxs-lookup"><span data-stu-id="ad35b-283">Fixed AMSI Cloud blocking</span></span>
- <span data-ttu-id="ad35b-284">Journal d’installation des mises à jour de sécurité fixes</span><span class="sxs-lookup"><span data-stu-id="ad35b-284">Fixed Security update install log</span></span>

### <a name="known-issues"></a><span data-ttu-id="ad35b-285">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="ad35b-285">Known Issues</span></span>
<span data-ttu-id="ad35b-286">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="ad35b-286">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="ad35b-287">Avril-2020 (plateforme : 4.18.2004.6 | Moteur : 1.1.17000.2)</span><span class="sxs-lookup"><span data-stu-id="ad35b-287">April-2020 (Platform: 4.18.2004.6 | Engine: 1.1.17000.2)</span></span></summary>

<span data-ttu-id="ad35b-288">&ensp;Version de mise à jour des informations de sécurité **: 1.315.12.0**</span><span class="sxs-lookup"><span data-stu-id="ad35b-288">&ensp;Security intelligence update version: **1.315.12.0**</span></span>  
<span data-ttu-id="ad35b-289">&ensp;Publication : **30 avril 2020**</span><span class="sxs-lookup"><span data-stu-id="ad35b-289">&ensp;Released: **April 30, 2020**</span></span>  
<span data-ttu-id="ad35b-290">&ensp;Plateforme : **4.18.2004.6**</span><span class="sxs-lookup"><span data-stu-id="ad35b-290">&ensp;Platform: **4.18.2004.6**</span></span>  
<span data-ttu-id="ad35b-291">&ensp;Moteur : **1.1.17000.2**</span><span class="sxs-lookup"><span data-stu-id="ad35b-291">&ensp;Engine: **1.1.17000.2**</span></span>  
<span data-ttu-id="ad35b-292">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="ad35b-292">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="ad35b-293">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="ad35b-293">What's new</span></span>
- <span data-ttu-id="ad35b-294">Améliorations de WDfilter</span><span class="sxs-lookup"><span data-stu-id="ad35b-294">WDfilter improvements</span></span>
- <span data-ttu-id="ad35b-295">Ajouter des données d’événements actionnables à des événements de détection de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="ad35b-295">Add more actionable event data to attack surface reduction detection events</span></span>
- <span data-ttu-id="ad35b-296">Informations de version fixes dans les données de diagnostic et WMI</span><span class="sxs-lookup"><span data-stu-id="ad35b-296">Fixed version information in diagnostic data and WMI</span></span>
- <span data-ttu-id="ad35b-297">Version de plateforme incorrecte corrigée dans l’interface utilisateur après la mise à jour de la plateforme</span><span class="sxs-lookup"><span data-stu-id="ad35b-297">Fixed incorrect platform version in UI after platform update</span></span>
- <span data-ttu-id="ad35b-298">Intel d’URL dynamique pour la protection contre les menaces sans fichier</span><span class="sxs-lookup"><span data-stu-id="ad35b-298">Dynamic URL intel for Fileless threat protection</span></span>
- <span data-ttu-id="ad35b-299">Fonctionnalité d’analyse UEFI</span><span class="sxs-lookup"><span data-stu-id="ad35b-299">UEFI scan capability</span></span>
- <span data-ttu-id="ad35b-300">Étendre la journalisation pour les mises à jour</span><span class="sxs-lookup"><span data-stu-id="ad35b-300">Extend logging for updates</span></span>

### <a name="known-issues"></a><span data-ttu-id="ad35b-301">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="ad35b-301">Known Issues</span></span>
<span data-ttu-id="ad35b-302">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="ad35b-302">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="ad35b-303">Mars-2020 (plateforme : 4.18.2003.8 | Moteur : 1.1.16900.2)</span><span class="sxs-lookup"><span data-stu-id="ad35b-303">March-2020 (Platform: 4.18.2003.8 | Engine: 1.1.16900.2)</span></span></summary>

<span data-ttu-id="ad35b-304">&ensp;Version de mise à jour des informations de sécurité **: 1.313.8.0**</span><span class="sxs-lookup"><span data-stu-id="ad35b-304">&ensp;Security intelligence update version: **1.313.8.0**</span></span>  
<span data-ttu-id="ad35b-305">&ensp;Publication : **24 mars 2020**</span><span class="sxs-lookup"><span data-stu-id="ad35b-305">&ensp;Released: **March 24, 2020**</span></span>  
<span data-ttu-id="ad35b-306">&ensp;Plateforme : **4.18.2003.8**</span><span class="sxs-lookup"><span data-stu-id="ad35b-306">&ensp;Platform: **4.18.2003.8**</span></span>  
<span data-ttu-id="ad35b-307">&ensp;Moteur : **1.1.16900.4**</span><span class="sxs-lookup"><span data-stu-id="ad35b-307">&ensp;Engine: **1.1.16900.4**</span></span>  
<span data-ttu-id="ad35b-308">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="ad35b-308">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="ad35b-309">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="ad35b-309">What's new</span></span>

- <span data-ttu-id="ad35b-310">Option de limitation du processeur ajoutée à [MpCmdRun](./command-line-arguments-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="ad35b-310">CPU Throttling option added to [MpCmdRun](./command-line-arguments-microsoft-defender-antivirus.md)</span></span>
- <span data-ttu-id="ad35b-311">Améliorer les fonctionnalités de diagnostic</span><span class="sxs-lookup"><span data-stu-id="ad35b-311">Improve diagnostic capability</span></span>
- <span data-ttu-id="ad35b-312">réduire le délai d’out des informations de sécurité (5 min)</span><span class="sxs-lookup"><span data-stu-id="ad35b-312">reduce Security intelligence timeout (5 min)</span></span>
- <span data-ttu-id="ad35b-313">Étendre la fonctionnalité de journal interne du moteur AMSI</span><span class="sxs-lookup"><span data-stu-id="ad35b-313">Extend AMSI engine internal log capability</span></span>
- <span data-ttu-id="ad35b-314">Améliorer la notification pour le blocage des processus</span><span class="sxs-lookup"><span data-stu-id="ad35b-314">Improve notification for process blocking</span></span>
   
### <a name="known-issues"></a><span data-ttu-id="ad35b-315">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="ad35b-315">Known Issues</span></span>
<span data-ttu-id="ad35b-316">[**Fixe**] Antivirus Microsoft Defender ignorer les fichiers lors de l’exécution d’une analyse.</span><span class="sxs-lookup"><span data-stu-id="ad35b-316">[**Fixed**] Microsoft Defender Antivirus is skipping files when running a scan.</span></span>

<br/>
</details>

<details>

<summary> <span data-ttu-id="ad35b-317">Février-2020 (plateforme : - | Moteur : 1.1.16800.2)</span><span class="sxs-lookup"><span data-stu-id="ad35b-317">February-2020 (Platform: - | Engine: 1.1.16800.2)</span></span></summary>
  

<span data-ttu-id="ad35b-318">&ensp;Version de mise à jour des informations de sécurité **: 1.311.4.0** </span><span class="sxs-lookup"><span data-stu-id="ad35b-318">&ensp;Security intelligence update version: **1.311.4.0** </span></span>  
<span data-ttu-id="ad35b-319">&ensp;Publication : **25 février 2020**</span><span class="sxs-lookup"><span data-stu-id="ad35b-319">&ensp;Released: **February 25, 2020**</span></span>  
<span data-ttu-id="ad35b-320">&ensp;Plateforme/Client : **-**</span><span class="sxs-lookup"><span data-stu-id="ad35b-320">&ensp;Platform/Client: **-**</span></span>  
<span data-ttu-id="ad35b-321">&ensp;Moteur : **1.1.16800.2**</span><span class="sxs-lookup"><span data-stu-id="ad35b-321">&ensp;Engine: **1.1.16800.2**</span></span>  
<span data-ttu-id="ad35b-322">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="ad35b-322">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
     
### <a name="whats-new"></a><span data-ttu-id="ad35b-323">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="ad35b-323">What's new</span></span>

  
### <a name="known-issues"></a><span data-ttu-id="ad35b-324">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="ad35b-324">Known Issues</span></span>
<span data-ttu-id="ad35b-325">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="ad35b-325">No known issues</span></span>
<br/>
</details>

<details>
<summary> <span data-ttu-id="ad35b-326">Janvier-2020 (plateforme : 4.18.2001.10 | Moteur : 1.1.16700.2)</span><span class="sxs-lookup"><span data-stu-id="ad35b-326">January-2020 (Platform: 4.18.2001.10 | Engine: 1.1.16700.2)</span></span></summary>
  

<span data-ttu-id="ad35b-327">Version de mise à jour des informations de sécurité **: 1.309.32.0**</span><span class="sxs-lookup"><span data-stu-id="ad35b-327">Security intelligence update version: **1.309.32.0**</span></span>  
<span data-ttu-id="ad35b-328">Publication : **30 janvier 2020**</span><span class="sxs-lookup"><span data-stu-id="ad35b-328">Released: **January 30, 2020**</span></span>  
<span data-ttu-id="ad35b-329">Plateforme/Client : **4.18.2001.10**</span><span class="sxs-lookup"><span data-stu-id="ad35b-329">Platform/Client: **4.18.2001.10**</span></span>  
<span data-ttu-id="ad35b-330">Moteur : **1.1.16700.2**</span><span class="sxs-lookup"><span data-stu-id="ad35b-330">Engine: **1.1.16700.2**</span></span>  
<span data-ttu-id="ad35b-331">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="ad35b-331">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
     
### <a name="whats-new"></a><span data-ttu-id="ad35b-332">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="ad35b-332">What's new</span></span>

- <span data-ttu-id="ad35b-333">Correction du BSOD sur WS2016 avec Exchange</span><span class="sxs-lookup"><span data-stu-id="ad35b-333">Fixed BSOD on WS2016 with Exchange</span></span>
- <span data-ttu-id="ad35b-334">Prise en charge des mises à jour de plateforme lorsque le TMP est redirigé vers le chemin d’accès réseau</span><span class="sxs-lookup"><span data-stu-id="ad35b-334">Support platform updates when TMP is redirected to network path</span></span>
- <span data-ttu-id="ad35b-335">Les versions de plateforme et de moteur sont ajoutées [à WDSI](https://www.microsoft.com/en-us/wdsi/defenderupdates)</span><span class="sxs-lookup"><span data-stu-id="ad35b-335">Platform and engine versions are added to [WDSI](https://www.microsoft.com/en-us/wdsi/defenderupdates)</span></span> <!-- The preceding URL must include "/en-us" -->
- <span data-ttu-id="ad35b-336">étendre la mise à jour des signatures d’urgence [en mode passif](./microsoft-defender-antivirus-compatibility.md)</span><span class="sxs-lookup"><span data-stu-id="ad35b-336">extend Emergency signature update to [passive mode](./microsoft-defender-antivirus-compatibility.md)</span></span>
- <span data-ttu-id="ad35b-337">Correction du hang 4.18.1911.3</span><span class="sxs-lookup"><span data-stu-id="ad35b-337">Fix 4.18.1911.3 hang</span></span>
   
### <a name="known-issues"></a><span data-ttu-id="ad35b-338">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="ad35b-338">Known Issues</span></span>

<span data-ttu-id="ad35b-339">[**Fixe**] Les appareils utilisant le [mode](/windows-hardware/design/device-experiences/modern-standby) de veille moderne peuvent se bloquer avec le pilote de filtre Windows Defender, ce qui se traduit par un manque de protection.</span><span class="sxs-lookup"><span data-stu-id="ad35b-339">[**Fixed**] devices utilizing [modern standby mode](/windows-hardware/design/device-experiences/modern-standby) may experience a hang with the Windows Defender filter driver that results in a gap of protection.</span></span>  <span data-ttu-id="ad35b-340">Les ordinateurs concernés semblent ne pas avoir été mis à jour vers la dernière plateforme anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="ad35b-340">Affected machines appear to the customer as having not updated to the latest antimalware platform.</span></span>  
<br/>
> [!IMPORTANT]
> <span data-ttu-id="ad35b-341">Cette mise à jour est :</span><span class="sxs-lookup"><span data-stu-id="ad35b-341">This update is:</span></span>
> - <span data-ttu-id="ad35b-342">nécessaire aux appareils RS1 exécutant une version inférieure de la plateforme pour prendre en charge SHA2 ;</span><span class="sxs-lookup"><span data-stu-id="ad35b-342">needed by RS1 devices running lower version of the platform to support SHA2;</span></span>
> - <span data-ttu-id="ad35b-343">a un indicateur de redémarrage pour les systèmes qui ont des problèmes en suspension ;</span><span class="sxs-lookup"><span data-stu-id="ad35b-343">has a reboot flag for systems that have hanging issues;</span></span>
> - <span data-ttu-id="ad35b-344">est re-publiée en avril 2020 et ne sera pas recalée par les mises à jour plus nouvelles pour conserver la disponibilité future ;</span><span class="sxs-lookup"><span data-stu-id="ad35b-344">is re-released in April 2020 and will not be superseded by newer updates to keep future availability;</span></span>  
> - <span data-ttu-id="ad35b-345">est classée en tant que mise à jour en raison de l’exigence de redémarrage ; et</span><span class="sxs-lookup"><span data-stu-id="ad35b-345">is categorized as an update due to the reboot requirement; and</span></span>
> - <span data-ttu-id="ad35b-346">est uniquement proposé avec [la mise à jour Windows.](https://support.microsoft.com/help/4027667/windows-10-update)</span><span class="sxs-lookup"><span data-stu-id="ad35b-346">is only be offered with [Windows Update](https://support.microsoft.com/help/4027667/windows-10-update).</span></span>
<br/>
</details>

<details>
<summary> <span data-ttu-id="ad35b-347">Novembre-2019 (plateforme : 4.18.1911.3 | Moteur : 1.1.16600.7)</span><span class="sxs-lookup"><span data-stu-id="ad35b-347">November-2019 (Platform: 4.18.1911.3 | Engine: 1.1.16600.7)</span></span></summary>

<span data-ttu-id="ad35b-348">Version de mise à jour des informations de sécurité **: 1.307.13.0**</span><span class="sxs-lookup"><span data-stu-id="ad35b-348">Security intelligence update version: **1.307.13.0**</span></span>  
<span data-ttu-id="ad35b-349">Publication : **7 décembre 2019**</span><span class="sxs-lookup"><span data-stu-id="ad35b-349">Released: **December 7, 2019**</span></span>  
<span data-ttu-id="ad35b-350">Plateforme : **4.18.1911.3**</span><span class="sxs-lookup"><span data-stu-id="ad35b-350">Platform: **4.18.1911.3**</span></span>  
<span data-ttu-id="ad35b-351">Moteur : **1.1.17000.7**</span><span class="sxs-lookup"><span data-stu-id="ad35b-351">Engine: **1.1.17000.7**</span></span>  
<span data-ttu-id="ad35b-352">Phase de support : **aucune prise en charge**</span><span class="sxs-lookup"><span data-stu-id="ad35b-352">Support phase: **No support**</span></span>  
     
### <a name="whats-new"></a><span data-ttu-id="ad35b-353">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="ad35b-353">What's new</span></span>

- <span data-ttu-id="ad35b-354">Niveau de suivi MpCmdRun fixe</span><span class="sxs-lookup"><span data-stu-id="ad35b-354">Fixed MpCmdRun tracing level</span></span>
- <span data-ttu-id="ad35b-355">Informations de version de WDFilter fixes</span><span class="sxs-lookup"><span data-stu-id="ad35b-355">Fixed WDFilter version info</span></span>
- <span data-ttu-id="ad35b-356">Améliorer les notifications (PUA)</span><span class="sxs-lookup"><span data-stu-id="ad35b-356">Improve notifications (PUA)</span></span>
- <span data-ttu-id="ad35b-357">ajouter des journaux MRT pour prendre en charge les fichiers</span><span class="sxs-lookup"><span data-stu-id="ad35b-357">add MRT logs to support files</span></span>
   
### <a name="known-issues"></a><span data-ttu-id="ad35b-358">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="ad35b-358">Known Issues</span></span>
<span data-ttu-id="ad35b-359">Lorsque cette mise à jour est installée, l’appareil a besoin du package de saut 4.10.2001.10 pour pouvoir se mettre à jour vers la dernière version de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="ad35b-359">When this update is installed, the device needs the jump package 4.10.2001.10 to be able to update to the latest platform version.</span></span>
<br/>
</details>


## <a name="microsoft-defender-antivirus-platform-support"></a><span data-ttu-id="ad35b-360">Antivirus Microsoft Defender prise en charge de la plateforme d’Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="ad35b-360">Microsoft Defender Antivirus platform support</span></span>
<span data-ttu-id="ad35b-361">Les mises à jour de la plateforme et du moteur sont fournies à une cadence mensuelle.</span><span class="sxs-lookup"><span data-stu-id="ad35b-361">Platform and engine updates are provided on a monthly cadence.</span></span> <span data-ttu-id="ad35b-362">Pour être entièrement pris en charge, tenez à jour les dernières mises à jour de plateforme.</span><span class="sxs-lookup"><span data-stu-id="ad35b-362">To be fully supported, keep current with the latest platform updates.</span></span> <span data-ttu-id="ad35b-363">Notre structure de support est dynamique et évolue en deux phases en fonction de la disponibilité de la dernière version de plateforme :</span><span class="sxs-lookup"><span data-stu-id="ad35b-363">Our support structure is dynamic, evolving into two phases depending on the availability of the latest platform version:</span></span>

- <span data-ttu-id="ad35b-364">Phase de maintenance des mises à jour **critiques** et de sécurité : lors de l’exécution de la dernière version de la plateforme, vous serez éligible à la réception des mises à jour de sécurité et critiques sur la plateforme anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="ad35b-364">**Security and Critical Updates servicing phase** - When running the latest platform version, you will be eligible to receive both Security and Critical updates to the anti-malware platform.</span></span>
 
- <span data-ttu-id="ad35b-365">**Phase de support technique (uniquement)** : après la publication d’une nouvelle version de plateforme, la prise en charge des versions antérieures (N-2) sera réduit au support technique uniquement.</span><span class="sxs-lookup"><span data-stu-id="ad35b-365">**Technical Support (Only) phase** - After a new platform version is released, support for older versions (N-2) will reduce to technical support only.</span></span> <span data-ttu-id="ad35b-366">Les versions de plateforme antérieures à N-2 ne seront plus pris en charge.\*</span><span class="sxs-lookup"><span data-stu-id="ad35b-366">Platform versions older than N-2 will no longer be supported.\*</span></span>

<span data-ttu-id="ad35b-367">\*Le support technique continuera d’être fourni pour les mises à niveau de la version Windows 10 (voir la version de plateforme incluse avec [les](#platform-version-included-with-windows-10-releases)versions Windows 10 ) vers la dernière version de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="ad35b-367">\* Technical support will continue to be provided for upgrades from the Windows 10 release version (see [Platform version included with Windows 10 releases](#platform-version-included-with-windows-10-releases)) to the latest platform version.</span></span>

<span data-ttu-id="ad35b-368">Pendant la phase de support technique (uniquement), les incidents de support commercialement raisonnables sont fournis par le biais du support technique du service clientèle Microsoft & et des offres de support géré de Microsoft (telles que le support Premier).</span><span class="sxs-lookup"><span data-stu-id="ad35b-368">During the technical support (only) phase, commercially reasonable support incidents will be provided through Microsoft Customer Service & Support and Microsoft’s managed support offerings (such as Premier Support).</span></span> <span data-ttu-id="ad35b-369">Si un incident de support nécessite une escalade vers le développement pour obtenir des conseils supplémentaires, nécessite une mise à jour non de sécurité ou nécessite une mise à jour de sécurité, les clients sont invités à mettre à niveau vers la dernière version de plateforme ou une mise à jour intermédiaire (\*).</span><span class="sxs-lookup"><span data-stu-id="ad35b-369">If a support incident requires escalation to development for further guidance, requires a non-security update, or requires a security update, customers will be asked to upgrade to the latest platform version or an intermediate update (\*).</span></span>

### <a name="platform-version-included-with-windows-10-releases"></a><span data-ttu-id="ad35b-370">Version de plateforme incluse dans Windows 10 versions</span><span class="sxs-lookup"><span data-stu-id="ad35b-370">Platform version included with Windows 10 releases</span></span>
<span data-ttu-id="ad35b-371">Le tableau ci-dessous fournit les versions Antivirus Microsoft Defender de plateforme et de moteur qui sont livrées avec les versions les Windows 10 les plus récentes :</span><span class="sxs-lookup"><span data-stu-id="ad35b-371">The below table provides the Microsoft Defender Antivirus platform and engine versions that are shipped with the latest Windows 10 releases:</span></span>    

|<span data-ttu-id="ad35b-372">Windows 10 version</span><span class="sxs-lookup"><span data-stu-id="ad35b-372">Windows 10 release</span></span>  |<span data-ttu-id="ad35b-373">Version de la plateforme</span><span class="sxs-lookup"><span data-stu-id="ad35b-373">Platform version</span></span>  |<span data-ttu-id="ad35b-374">Version du moteur</span><span class="sxs-lookup"><span data-stu-id="ad35b-374">Engine version</span></span> |<span data-ttu-id="ad35b-375">Phase de prise en charge</span><span class="sxs-lookup"><span data-stu-id="ad35b-375">Support phase</span></span> |
|:---|:---|:---|:---|
|<span data-ttu-id="ad35b-376">2004 (20H1/20H2)</span><span class="sxs-lookup"><span data-stu-id="ad35b-376">2004  (20H1/20H2)</span></span> |<span data-ttu-id="ad35b-377">4.18.1909.6</span><span class="sxs-lookup"><span data-stu-id="ad35b-377">4.18.1909.6</span></span> |<span data-ttu-id="ad35b-378">1.1.17000.2</span><span class="sxs-lookup"><span data-stu-id="ad35b-378">1.1.17000.2</span></span> | <span data-ttu-id="ad35b-379">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="ad35b-379">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="ad35b-380">1909 (19H2)</span><span class="sxs-lookup"><span data-stu-id="ad35b-380">1909  (19H2)</span></span> |<span data-ttu-id="ad35b-381">4.18.1902.5</span><span class="sxs-lookup"><span data-stu-id="ad35b-381">4.18.1902.5</span></span> |<span data-ttu-id="ad35b-382">1.1.16700.3</span><span class="sxs-lookup"><span data-stu-id="ad35b-382">1.1.16700.3</span></span> | <span data-ttu-id="ad35b-383">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="ad35b-383">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="ad35b-384">1903 (19H1)</span><span class="sxs-lookup"><span data-stu-id="ad35b-384">1903  (19H1)</span></span> |<span data-ttu-id="ad35b-385">4.18.1902.5</span><span class="sxs-lookup"><span data-stu-id="ad35b-385">4.18.1902.5</span></span> |<span data-ttu-id="ad35b-386">1.1.15600.4</span><span class="sxs-lookup"><span data-stu-id="ad35b-386">1.1.15600.4</span></span> | <span data-ttu-id="ad35b-387">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="ad35b-387">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="ad35b-388">1809 (RS5)</span><span class="sxs-lookup"><span data-stu-id="ad35b-388">1809  (RS5)</span></span> |<span data-ttu-id="ad35b-389">4.18.1807.18075</span><span class="sxs-lookup"><span data-stu-id="ad35b-389">4.18.1807.18075</span></span> |<span data-ttu-id="ad35b-390">1.1.15000.2</span><span class="sxs-lookup"><span data-stu-id="ad35b-390">1.1.15000.2</span></span> | <span data-ttu-id="ad35b-391">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="ad35b-391">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="ad35b-392">1803 (RS4)</span><span class="sxs-lookup"><span data-stu-id="ad35b-392">1803  (RS4)</span></span> |<span data-ttu-id="ad35b-393">4.13.17134.1</span><span class="sxs-lookup"><span data-stu-id="ad35b-393">4.13.17134.1</span></span> |<span data-ttu-id="ad35b-394">1.1.14600.4</span><span class="sxs-lookup"><span data-stu-id="ad35b-394">1.1.14600.4</span></span> | <span data-ttu-id="ad35b-395">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="ad35b-395">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="ad35b-396">1709 (RS3)</span><span class="sxs-lookup"><span data-stu-id="ad35b-396">1709  (RS3)</span></span> |<span data-ttu-id="ad35b-397">4.12.16299.15</span><span class="sxs-lookup"><span data-stu-id="ad35b-397">4.12.16299.15</span></span> |<span data-ttu-id="ad35b-398">1.1.14104.0</span><span class="sxs-lookup"><span data-stu-id="ad35b-398">1.1.14104.0</span></span> | <span data-ttu-id="ad35b-399">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="ad35b-399">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="ad35b-400">1703 (RS2)</span><span class="sxs-lookup"><span data-stu-id="ad35b-400">1703  (RS2)</span></span> |<span data-ttu-id="ad35b-401">4.11.15603.2</span><span class="sxs-lookup"><span data-stu-id="ad35b-401">4.11.15603.2</span></span> |<span data-ttu-id="ad35b-402">1.1.13504.0</span><span class="sxs-lookup"><span data-stu-id="ad35b-402">1.1.13504.0</span></span> | <span data-ttu-id="ad35b-403">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="ad35b-403">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="ad35b-404">1607 (RS1)</span><span class="sxs-lookup"><span data-stu-id="ad35b-404">1607 (RS1)</span></span> |<span data-ttu-id="ad35b-405">4.10.14393.3683</span><span class="sxs-lookup"><span data-stu-id="ad35b-405">4.10.14393.3683</span></span> |<span data-ttu-id="ad35b-406">1.1.12805.0</span><span class="sxs-lookup"><span data-stu-id="ad35b-406">1.1.12805.0</span></span> | <span data-ttu-id="ad35b-407">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="ad35b-407">Technical upgrade support (only)</span></span> |  

<span data-ttu-id="ad35b-408">Pour Windows 10 de publication, consultez la [Windows de faits sur](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet)le cycle de vie.</span><span class="sxs-lookup"><span data-stu-id="ad35b-408">For Windows 10 release information, see the [Windows lifecycle fact sheet](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet).</span></span>

## <a name="updates-for-deployment-image-servicing-and-management-dism"></a><span data-ttu-id="ad35b-409">Mises à jour pour la gestion et la maintenance des images de déploiement (DISM)</span><span class="sxs-lookup"><span data-stu-id="ad35b-409">Updates for Deployment Image Servicing and Management (DISM)</span></span>

<span data-ttu-id="ad35b-410">Nous vous recommandons de mettre à jour vos images d’installation Windows 10 (éditions Enterprise, Pro et Famille), Windows Server 2019 et Windows Server 2016 OS avec les dernières mises à jour antivirus et anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="ad35b-410">We recommend updating your Windows 10 (Enterprise, Pro, and Home editions), Windows Server 2019, and Windows Server 2016 OS installation images with the latest antivirus and antimalware updates.</span></span> <span data-ttu-id="ad35b-411">La mise à jour de vos images d’installation du système d’exploitation permet d’éviter un écart de protection.</span><span class="sxs-lookup"><span data-stu-id="ad35b-411">Keeping your OS installation images up to date helps avoid a gap in protection.</span></span> 

<span data-ttu-id="ad35b-412">Pour plus d’informations, voir mise à [jour de Microsoft Defender pour Windows images d’installation du système d’exploitation.](https://support.microsoft.com/help/4568292/defender-update-for-windows-operating-system-installation-images)</span><span class="sxs-lookup"><span data-stu-id="ad35b-412">For more information, see [Microsoft Defender update for Windows operating system installation images](https://support.microsoft.com/help/4568292/defender-update-for-windows-operating-system-installation-images).</span></span>

<details>
<summary><span data-ttu-id="ad35b-413">1.1.2104.01</span><span class="sxs-lookup"><span data-stu-id="ad35b-413">1.1.2104.01</span></span></summary>

<span data-ttu-id="ad35b-414">&ensp;Version du package **: 1.1.2104.01**  </span><span class="sxs-lookup"><span data-stu-id="ad35b-414">&ensp;Package version: **1.1.2104.01**  </span></span>  
<span data-ttu-id="ad35b-415">&ensp;Version de plateforme **: 4.18.2102.4** </span><span class="sxs-lookup"><span data-stu-id="ad35b-415">&ensp;Platform version: **4.18.2102.4** </span></span>  
<span data-ttu-id="ad35b-416">&ensp;Version du moteur **: 1.1.18000.5**</span><span class="sxs-lookup"><span data-stu-id="ad35b-416">&ensp;Engine version: **1.1.18000.5**</span></span>  
<span data-ttu-id="ad35b-417">&ensp;Version de signature **: 1.335.232.0**</span><span class="sxs-lookup"><span data-stu-id="ad35b-417">&ensp;Signature version: **1.335.232.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="ad35b-418">Correctifs</span><span class="sxs-lookup"><span data-stu-id="ad35b-418">Fixes</span></span>
- <span data-ttu-id="ad35b-419">Aucune</span><span class="sxs-lookup"><span data-stu-id="ad35b-419">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="ad35b-420">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ad35b-420">Additional information</span></span>
- <span data-ttu-id="ad35b-421">Aucune</span><span class="sxs-lookup"><span data-stu-id="ad35b-421">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="ad35b-422">1.1.2103.01</span><span class="sxs-lookup"><span data-stu-id="ad35b-422">1.1.2103.01</span></span></summary>

<span data-ttu-id="ad35b-423">&ensp;Version du package **: 1.1.2103.01**  </span><span class="sxs-lookup"><span data-stu-id="ad35b-423">&ensp;Package version: **1.1.2103.01**  </span></span>  
<span data-ttu-id="ad35b-424">&ensp;Version de plateforme **: 4.18.2101.9** </span><span class="sxs-lookup"><span data-stu-id="ad35b-424">&ensp;Platform version: **4.18.2101.9** </span></span>  
<span data-ttu-id="ad35b-425">&ensp;Version du moteur **: 1.1.17800.5**</span><span class="sxs-lookup"><span data-stu-id="ad35b-425">&ensp;Engine version: **1.1.17800.5**</span></span>  
<span data-ttu-id="ad35b-426">&ensp;Version de signature **: 1.331.2302.0**</span><span class="sxs-lookup"><span data-stu-id="ad35b-426">&ensp;Signature version: **1.331.2302.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="ad35b-427">Correctifs</span><span class="sxs-lookup"><span data-stu-id="ad35b-427">Fixes</span></span>
- <span data-ttu-id="ad35b-428">Aucune</span><span class="sxs-lookup"><span data-stu-id="ad35b-428">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="ad35b-429">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ad35b-429">Additional information</span></span>
- <span data-ttu-id="ad35b-430">Aucune</span><span class="sxs-lookup"><span data-stu-id="ad35b-430">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="ad35b-431">1.1.2102.03</span><span class="sxs-lookup"><span data-stu-id="ad35b-431">1.1.2102.03</span></span></summary>

<span data-ttu-id="ad35b-432">&ensp;Version du package **: 1.1.2102.03**  </span><span class="sxs-lookup"><span data-stu-id="ad35b-432">&ensp;Package version: **1.1.2102.03**  </span></span>  
<span data-ttu-id="ad35b-433">&ensp;Version de la plateforme **: 4.18.2011.6** </span><span class="sxs-lookup"><span data-stu-id="ad35b-433">&ensp;Platform version: **4.18.2011.6** </span></span>  
<span data-ttu-id="ad35b-434">&ensp;Version du moteur **: 1.1.17800.5**</span><span class="sxs-lookup"><span data-stu-id="ad35b-434">&ensp;Engine version: **1.1.17800.5**</span></span>  
<span data-ttu-id="ad35b-435">&ensp;Version de signature **: 1.331.174.0**</span><span class="sxs-lookup"><span data-stu-id="ad35b-435">&ensp;Signature version: **1.331.174.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="ad35b-436">Correctifs</span><span class="sxs-lookup"><span data-stu-id="ad35b-436">Fixes</span></span>
- <span data-ttu-id="ad35b-437">Aucune</span><span class="sxs-lookup"><span data-stu-id="ad35b-437">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="ad35b-438">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ad35b-438">Additional information</span></span>
- <span data-ttu-id="ad35b-439">Aucune</span><span class="sxs-lookup"><span data-stu-id="ad35b-439">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="ad35b-440">1.1.2101.02</span><span class="sxs-lookup"><span data-stu-id="ad35b-440">1.1.2101.02</span></span></summary>

<span data-ttu-id="ad35b-441">&ensp;Version du package **: 1.1.2101.02**  </span><span class="sxs-lookup"><span data-stu-id="ad35b-441">&ensp;Package version: **1.1.2101.02**  </span></span>  
<span data-ttu-id="ad35b-442">&ensp;Version de la plateforme **: 4.18.2011.6** </span><span class="sxs-lookup"><span data-stu-id="ad35b-442">&ensp;Platform version: **4.18.2011.6** </span></span>  
<span data-ttu-id="ad35b-443">&ensp;Version du moteur **: 1.1.17700.4**</span><span class="sxs-lookup"><span data-stu-id="ad35b-443">&ensp;Engine version: **1.1.17700.4**</span></span>  
<span data-ttu-id="ad35b-444">&ensp;Version de signature **: 1.329.1796.0**</span><span class="sxs-lookup"><span data-stu-id="ad35b-444">&ensp;Signature version: **1.329.1796.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="ad35b-445">Correctifs</span><span class="sxs-lookup"><span data-stu-id="ad35b-445">Fixes</span></span>
- <span data-ttu-id="ad35b-446">Aucune</span><span class="sxs-lookup"><span data-stu-id="ad35b-446">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="ad35b-447">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ad35b-447">Additional information</span></span>
- <span data-ttu-id="ad35b-448">Aucune</span><span class="sxs-lookup"><span data-stu-id="ad35b-448">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="ad35b-449">1.1.2012.01</span><span class="sxs-lookup"><span data-stu-id="ad35b-449">1.1.2012.01</span></span></summary>

<span data-ttu-id="ad35b-450">&ensp;Version du package **: 1.1.2012.01**  </span><span class="sxs-lookup"><span data-stu-id="ad35b-450">&ensp;Package version: **1.1.2012.01**  </span></span>  
<span data-ttu-id="ad35b-451">&ensp;Version de plateforme **: 4.18.2010.7** </span><span class="sxs-lookup"><span data-stu-id="ad35b-451">&ensp;Platform version: **4.18.2010.7** </span></span>  
<span data-ttu-id="ad35b-452">&ensp;Version du moteur **: 1.1.17600.5**</span><span class="sxs-lookup"><span data-stu-id="ad35b-452">&ensp;Engine version: **1.1.17600.5**</span></span>  
<span data-ttu-id="ad35b-453">&ensp;Version de signature **: 1.327.1991.0**</span><span class="sxs-lookup"><span data-stu-id="ad35b-453">&ensp;Signature version: **1.327.1991.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="ad35b-454">Correctifs</span><span class="sxs-lookup"><span data-stu-id="ad35b-454">Fixes</span></span>
- <span data-ttu-id="ad35b-455">Aucune</span><span class="sxs-lookup"><span data-stu-id="ad35b-455">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="ad35b-456">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ad35b-456">Additional information</span></span>
- <span data-ttu-id="ad35b-457">Aucune</span><span class="sxs-lookup"><span data-stu-id="ad35b-457">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="ad35b-458">1.1.2011.02</span><span class="sxs-lookup"><span data-stu-id="ad35b-458">1.1.2011.02</span></span></summary>

<span data-ttu-id="ad35b-459">&ensp;Version du package **: 1.1.2011.02**  </span><span class="sxs-lookup"><span data-stu-id="ad35b-459">&ensp;Package version: **1.1.2011.02**  </span></span>  
<span data-ttu-id="ad35b-460">&ensp;Version de plateforme **: 4.18.2010.7** </span><span class="sxs-lookup"><span data-stu-id="ad35b-460">&ensp;Platform version: **4.18.2010.7** </span></span>  
<span data-ttu-id="ad35b-461">&ensp;Version du moteur **: 1.1.17600.5**</span><span class="sxs-lookup"><span data-stu-id="ad35b-461">&ensp;Engine version: **1.1.17600.5**</span></span>  
<span data-ttu-id="ad35b-462">&ensp;Version de signature **: 1.327.658.0**</span><span class="sxs-lookup"><span data-stu-id="ad35b-462">&ensp;Signature version: **1.327.658.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="ad35b-463">Correctifs</span><span class="sxs-lookup"><span data-stu-id="ad35b-463">Fixes</span></span>
- <span data-ttu-id="ad35b-464">Aucune</span><span class="sxs-lookup"><span data-stu-id="ad35b-464">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="ad35b-465">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ad35b-465">Additional information</span></span>
- <span data-ttu-id="ad35b-466">Signatures Antivirus Microsoft Defender actualisées</span><span class="sxs-lookup"><span data-stu-id="ad35b-466">Refreshed Microsoft Defender Antivirus signatures</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="ad35b-467">1.1.2011.01</span><span class="sxs-lookup"><span data-stu-id="ad35b-467">1.1.2011.01</span></span></summary>

<span data-ttu-id="ad35b-468">&ensp;Version du package **: 1.1.2011.01**  </span><span class="sxs-lookup"><span data-stu-id="ad35b-468">&ensp;Package version: **1.1.2011.01**  </span></span>  
<span data-ttu-id="ad35b-469">&ensp;Version de la plateforme **: 4.18.2009.7**</span><span class="sxs-lookup"><span data-stu-id="ad35b-469">&ensp;Platform version: **4.18.2009.7**</span></span>  
<span data-ttu-id="ad35b-470">&ensp;Version du moteur **: 1.1.17600.5**</span><span class="sxs-lookup"><span data-stu-id="ad35b-470">&ensp;Engine version: **1.1.17600.5**</span></span>  
<span data-ttu-id="ad35b-471">&ensp;Version de signature **: 1.327.344.0**</span><span class="sxs-lookup"><span data-stu-id="ad35b-471">&ensp;Signature version: **1.327.344.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="ad35b-472">Correctifs</span><span class="sxs-lookup"><span data-stu-id="ad35b-472">Fixes</span></span>
- <span data-ttu-id="ad35b-473">Aucune</span><span class="sxs-lookup"><span data-stu-id="ad35b-473">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="ad35b-474">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ad35b-474">Additional information</span></span>
- <span data-ttu-id="ad35b-475">Aucune</span><span class="sxs-lookup"><span data-stu-id="ad35b-475">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="ad35b-476">1.1.2009.10</span><span class="sxs-lookup"><span data-stu-id="ad35b-476">1.1.2009.10</span></span></summary>

<span data-ttu-id="ad35b-477">&ensp;Version du package **: 1.1.2011.01**  </span><span class="sxs-lookup"><span data-stu-id="ad35b-477">&ensp;Package version: **1.1.2011.01**  </span></span>  
<span data-ttu-id="ad35b-478">&ensp;Version de plateforme **: 4.18.2008.9** </span><span class="sxs-lookup"><span data-stu-id="ad35b-478">&ensp;Platform version: **4.18.2008.9** </span></span>  
<span data-ttu-id="ad35b-479">&ensp;Version du moteur **: 1.1.17400.5**</span><span class="sxs-lookup"><span data-stu-id="ad35b-479">&ensp;Engine version: **1.1.17400.5**</span></span>  
<span data-ttu-id="ad35b-480">&ensp;Version de signature **: 1.327.2216.0**</span><span class="sxs-lookup"><span data-stu-id="ad35b-480">&ensp;Signature version: **1.327.2216.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="ad35b-481">Correctifs</span><span class="sxs-lookup"><span data-stu-id="ad35b-481">Fixes</span></span>
- <span data-ttu-id="ad35b-482">Aucune</span><span class="sxs-lookup"><span data-stu-id="ad35b-482">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="ad35b-483">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ad35b-483">Additional information</span></span>
- <span data-ttu-id="ad35b-484">Ajout de la prise en charge Windows 10 images d’installation du système d’exploitation RS1 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ad35b-484">Added support for Windows 10 RS1 or later OS install images.</span></span>  
<br/>
</details>

## <a name="additional-resources"></a><span data-ttu-id="ad35b-485">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ad35b-485">Additional resources</span></span>

| <span data-ttu-id="ad35b-486">Article</span><span class="sxs-lookup"><span data-stu-id="ad35b-486">Article</span></span> | <span data-ttu-id="ad35b-487">Description</span><span class="sxs-lookup"><span data-stu-id="ad35b-487">Description</span></span>  |
|:---|:---|
|[<span data-ttu-id="ad35b-488">Mise à jour de Microsoft Defender Windows images d’installation du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="ad35b-488">Microsoft Defender update for Windows operating system installation images</span></span>](https://support.microsoft.com/help/4568292/defender-update-for-windows-operating-system-installation-images)  | <span data-ttu-id="ad35b-489">Passer en revue les packages de mise à jour anti-programme malveillant pour vos images d’installation du système d’exploitation (fichiers WIM et VHD).</span><span class="sxs-lookup"><span data-stu-id="ad35b-489">Review antimalware update packages for your OS installation images (WIM and VHD files).</span></span> <span data-ttu-id="ad35b-490">Obtenez Antivirus Microsoft Defender mises à jour de Windows 10 (éditions Enterprise, Pro et Famille), Windows Server 2019 et Windows Server 2016 images d’installation.</span><span class="sxs-lookup"><span data-stu-id="ad35b-490">Get Microsoft Defender Antivirus updates for Windows 10 (Enterprise, Pro, and Home editions), Windows Server 2019, and Windows Server 2016 installation images.</span></span>  |
|[<span data-ttu-id="ad35b-491">Gérer le téléchargement et l’application des mises à jour de protection</span><span class="sxs-lookup"><span data-stu-id="ad35b-491">Manage how protection updates are downloaded and applied</span></span>](manage-protection-updates-microsoft-defender-antivirus.md) | <span data-ttu-id="ad35b-492">Les mises à jour de protection peuvent être mises à jour via de nombreuses sources.</span><span class="sxs-lookup"><span data-stu-id="ad35b-492">Protection updates can be delivered through many sources.</span></span> |
|[<span data-ttu-id="ad35b-493">Gérer le moment où les mises à jour de protection doivent être téléchargées et appliquées</span><span class="sxs-lookup"><span data-stu-id="ad35b-493">Manage when protection updates should be downloaded and applied</span></span>](manage-protection-update-schedule-microsoft-defender-antivirus.md) | <span data-ttu-id="ad35b-494">Vous pouvez planifier le téléchargement des mises à jour de la protection.</span><span class="sxs-lookup"><span data-stu-id="ad35b-494">You can schedule when protection updates should be downloaded.</span></span> |
|[<span data-ttu-id="ad35b-495">Gérer les mises à jour des points de terminaison qui ne sont pas à jour</span><span class="sxs-lookup"><span data-stu-id="ad35b-495">Manage updates for endpoints that are out of date</span></span>](manage-outdated-endpoints-microsoft-defender-antivirus.md) | <span data-ttu-id="ad35b-496">Si un point de terminaison manque une mise à jour ou une analyse programmée, vous pouvez forcer une mise à jour ou une analyse la prochaine fois qu’un utilisateur se signe.</span><span class="sxs-lookup"><span data-stu-id="ad35b-496">If an endpoint misses an update or scheduled scan, you can force an update or scan the next time a user signs in.</span></span> |
|[<span data-ttu-id="ad35b-497">Gérer les mises à jour forcées en fonction des événements</span><span class="sxs-lookup"><span data-stu-id="ad35b-497">Manage event-based forced updates</span></span>](manage-event-based-updates-microsoft-defender-antivirus.md) | <span data-ttu-id="ad35b-498">Vous pouvez définir des mises à jour de protection à télécharger au démarrage ou après certains événements de protection livrés par le cloud.</span><span class="sxs-lookup"><span data-stu-id="ad35b-498">You can set protection updates to be downloaded at startup or after certain cloud-delivered protection events.</span></span> |
|[<span data-ttu-id="ad35b-499">Gérer les mises à jour pour les appareils mobiles et les machines virtuelles</span><span class="sxs-lookup"><span data-stu-id="ad35b-499">Manage updates for mobile devices and virtual machines (VMs)</span></span>](manage-updates-mobile-devices-vms-microsoft-defender-antivirus.md)| <span data-ttu-id="ad35b-500">Vous pouvez spécifier des paramètres, par exemple si des mises à jour doivent être mises à jour sur l’alimentation de la batterie, qui sont particulièrement utiles pour les appareils mobiles et les ordinateurs virtuels.</span><span class="sxs-lookup"><span data-stu-id="ad35b-500">You can specify settings, such as whether updates should occur on battery power, that are especially useful for mobile devices and virtual machines.</span></span> |
