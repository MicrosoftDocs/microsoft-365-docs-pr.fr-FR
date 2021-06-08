---
title: Gérer les mises Antivirus Microsoft Defender jour et appliquer les lignes de base
description: Gérer la façon dont Antivirus Microsoft Defender reçoit les mises à jour de protection et de produit.
keywords: mises à jour, bases de référence de sécurité, protection, planifier des mises à jour, forcer les mises à jour, mises à jour mobiles, wsus
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: Normal
audience: ITPro
ms.topic: article
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.reviewer: pahuijbr
manager: dansimp
ms.technology: mde
ms.date: 06/07/2021
ms.openlocfilehash: 33170d4706ed53f4de687c34806bb0492a08836e
ms.sourcegitcommit: e1e275eb88153bafddf93327adf8f82318913a8d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52809106"
---
# <a name="manage-microsoft-defender-antivirus-updates-and-apply-baselines"></a><span data-ttu-id="3cd51-104">Gérer les mises Antivirus Microsoft Defender jour et appliquer les lignes de base</span><span class="sxs-lookup"><span data-stu-id="3cd51-104">Manage Microsoft Defender Antivirus updates and apply baselines</span></span>

<span data-ttu-id="3cd51-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="3cd51-105">**Applies to:**</span></span>

- [<span data-ttu-id="3cd51-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="3cd51-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)
- <span data-ttu-id="3cd51-107">Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="3cd51-107">Microsoft Defender Antivirus</span></span>

<span data-ttu-id="3cd51-108">Il existe deux types de mises à jour liées au Antivirus Microsoft Defender à jour :</span><span class="sxs-lookup"><span data-stu-id="3cd51-108">There are two types of updates related to keeping Microsoft Defender Antivirus up to date:</span></span>

- <span data-ttu-id="3cd51-109">Mises à jour de l’intelligence de la sécurité</span><span class="sxs-lookup"><span data-stu-id="3cd51-109">Security intelligence updates</span></span>
- <span data-ttu-id="3cd51-110">Mises à jour de produit</span><span class="sxs-lookup"><span data-stu-id="3cd51-110">Product updates</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3cd51-111">Le Antivirus Microsoft Defender à jour est essentiel pour garantir que vos appareils disposent des dernières technologies et fonctionnalités nécessaires pour se protéger contre les nouveaux programmes malveillants et les nouvelles techniques d’attaque.</span><span class="sxs-lookup"><span data-stu-id="3cd51-111">Keeping Microsoft Defender Antivirus up to date is critical to assure your devices have the latest technology and features needed to protect against new malware and attack techniques.</span></span>
> 
> <span data-ttu-id="3cd51-112">Veillez à mettre à jour votre protection antivirus même si Antivirus Microsoft Defender est en cours d’exécution [en mode passif.](./microsoft-defender-antivirus-compatibility.md)</span><span class="sxs-lookup"><span data-stu-id="3cd51-112">Make sure to update your antivirus protection even if Microsoft Defender Antivirus is running in [passive mode](./microsoft-defender-antivirus-compatibility.md).</span></span>
> 
> <span data-ttu-id="3cd51-113">Pour voir le moteur, la plateforme et la date de signature les plus à jour, consultez les mises à jour de l’intelligence de sécurité pour Antivirus Microsoft Defender logiciel [anti-programme](https://www.microsoft.com/en-us/wdsi/defenderupdates)malveillant Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3cd51-113">To see the most current engine, platform, and signature date, visit the [Security intelligence updates for Microsoft Defender Antivirus and other Microsoft antimalware](https://www.microsoft.com/en-us/wdsi/defenderupdates).</span></span>

## <a name="security-intelligence-updates"></a><span data-ttu-id="3cd51-114">Mises à jour de l’intelligence de la sécurité</span><span class="sxs-lookup"><span data-stu-id="3cd51-114">Security intelligence updates</span></span>

<span data-ttu-id="3cd51-115">Antivirus Microsoft Defender utilise la protection fournie par le [cloud](cloud-protection-microsoft-defender-antivirus.md) (également appelée Microsoft Advanced Protection Service ou MAPS) et télécharge régulièrement les mises à jour de l’intelligence de sécurité pour fournir une protection.</span><span class="sxs-lookup"><span data-stu-id="3cd51-115">Microsoft Defender Antivirus uses [cloud-delivered protection](cloud-protection-microsoft-defender-antivirus.md) (also called the Microsoft Advanced Protection Service or MAPS) and periodically downloads security intelligence updates to provide protection.</span></span>

> [!NOTE]
> <span data-ttu-id="3cd51-116">Les mises à jour sont publiées sous les numéros de la Ko ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="3cd51-116">Updates are released under the below KB numbers:</span></span>  
> - <span data-ttu-id="3cd51-117">Antivirus Microsoft Defender : KB2267602</span><span class="sxs-lookup"><span data-stu-id="3cd51-117">Microsoft Defender Antivirus: KB2267602</span></span>  
> - <span data-ttu-id="3cd51-118">System Center Endpoint Protection : KB2461484</span><span class="sxs-lookup"><span data-stu-id="3cd51-118">System Center Endpoint Protection: KB2461484</span></span>

<span data-ttu-id="3cd51-119">La protection cloud est toujours active et nécessite une connexion active à Internet pour fonctionner.</span><span class="sxs-lookup"><span data-stu-id="3cd51-119">Cloud-delivered protection is always on and requires an active connection to the Internet to function.</span></span> <span data-ttu-id="3cd51-120">Les mises à jour des informations de sécurité se produisent à une cadence programmée (configurable via une stratégie).</span><span class="sxs-lookup"><span data-stu-id="3cd51-120">Security intelligence updates occur on a scheduled cadence (configurable via policy).</span></span> <span data-ttu-id="3cd51-121">Pour plus d’informations, voir Utiliser la protection fournie par le [cloud microsoft dans Antivirus Microsoft Defender](cloud-protection-microsoft-defender-antivirus.md).</span><span class="sxs-lookup"><span data-stu-id="3cd51-121">For more information, see [Use Microsoft cloud-provided protection in Microsoft Defender Antivirus](cloud-protection-microsoft-defender-antivirus.md).</span></span> 

<span data-ttu-id="3cd51-122">Pour obtenir la liste des mises à jour récentes de l’intelligence de sécurité, voir Les mises à jour de l’intelligence de sécurité pour Antivirus Microsoft Defender logiciel [anti-programme](https://www.microsoft.com/en-us/wdsi/defenderupdates)malveillant Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3cd51-122">For a list of recent security intelligence updates, see [Security intelligence updates for Microsoft Defender Antivirus and other Microsoft antimalware](https://www.microsoft.com/en-us/wdsi/defenderupdates).</span></span>

<span data-ttu-id="3cd51-123">Les mises à jour du moteur sont incluses dans les mises à jour de l’intelligence de sécurité et sont publiées à une cadence mensuelle.</span><span class="sxs-lookup"><span data-stu-id="3cd51-123">Engine updates are included with security intelligence updates and are released on a monthly cadence.</span></span>

## <a name="product-updates"></a><span data-ttu-id="3cd51-124">Mises à jour de produit</span><span class="sxs-lookup"><span data-stu-id="3cd51-124">Product updates</span></span>

<span data-ttu-id="3cd51-125">Antivirus Microsoft Defender nécessite des mises à jour [mensuelles (KB4052623)](https://support.microsoft.com/help/4052623/update-for-windows-defender-antimalware-platform) *(connues* sous le nom de mises à jour de plateforme) et recevra des mises à jour de fonctionnalités majeures avec Windows 10 de publication.</span><span class="sxs-lookup"><span data-stu-id="3cd51-125">Microsoft Defender Antivirus requires [monthly updates (KB4052623)](https://support.microsoft.com/help/4052623/update-for-windows-defender-antimalware-platform) (known as *platform updates*), and will receive major feature updates alongside Windows 10 releases.</span></span>

<span data-ttu-id="3cd51-126">Vous pouvez gérer la distribution des mises à jour via l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="3cd51-126">You can manage the distribution of updates through one of the following methods:</span></span> 

- [<span data-ttu-id="3cd51-127">Windows Server Update Service (WSUS)</span><span class="sxs-lookup"><span data-stu-id="3cd51-127">Windows Server Update Service (WSUS)</span></span>](/mem/configmgr/protect/deploy-use/endpoint-definitions-wsus#to-synchronize-endpoint-protection-definition-updates-in-standalone-wsus)
- [<span data-ttu-id="3cd51-128">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="3cd51-128">Microsoft Endpoint Configuration Manager</span></span>](/configmgr/sum/understand/software-updates-introduction)
- <span data-ttu-id="3cd51-129">La méthode habituelle que vous utilisez pour déployer Microsoft et Windows mises à jour aux points de terminaison de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="3cd51-129">The usual method you use to deploy Microsoft and Windows updates to endpoints in your network.</span></span>

<span data-ttu-id="3cd51-130">Pour plus d’informations, [voir Gérer les sources pour les mises à jour Antivirus Microsoft Defender protection des données.](/mem/configmgr/protect/deploy-use/endpoint-definitions-wsus#to-synchronize-endpoint-protection-definition-updates-in-standalone-wsus)</span><span class="sxs-lookup"><span data-stu-id="3cd51-130">For more information, see [Manage the sources for Microsoft Defender Antivirus protection updates](/mem/configmgr/protect/deploy-use/endpoint-definitions-wsus#to-synchronize-endpoint-protection-definition-updates-in-standalone-wsus).</span></span>

> [!NOTE]
> <span data-ttu-id="3cd51-131">Les mises à jour mensuelles sont publiées par phases, ce qui entraîne la mise à jour de plusieurs packages dans vos services de mise à jour [de serveur Window.](/windows-server/administration/windows-server-update-services/get-started/windows-server-update-services-wsus)</span><span class="sxs-lookup"><span data-stu-id="3cd51-131">Monthly updates are released in phases, resulting in multiple packages visible in your [Window Server Update Services](/windows-server/administration/windows-server-update-services/get-started/windows-server-update-services-wsus).</span></span>

## <a name="monthly-platform-and-engine-versions"></a><span data-ttu-id="3cd51-132">Versions mensuelles de la plateforme et du moteur</span><span class="sxs-lookup"><span data-stu-id="3cd51-132">Monthly platform and engine versions</span></span>

<span data-ttu-id="3cd51-133">Pour plus d’informations sur la mise à jour ou l’installation de la mise à jour de la plateforme, voir [Update for Windows Defender antimalware platform](https://support.microsoft.com/help/4052623/update-for-windows-defender-antimalware-platform).</span><span class="sxs-lookup"><span data-stu-id="3cd51-133">For information how to update or install the platform update, see [Update for Windows Defender antimalware platform](https://support.microsoft.com/help/4052623/update-for-windows-defender-antimalware-platform).</span></span>

<span data-ttu-id="3cd51-134">Toutes nos mises à jour contiennent</span><span class="sxs-lookup"><span data-stu-id="3cd51-134">All our updates contain</span></span> 
- <span data-ttu-id="3cd51-135">améliorations des performances ;</span><span class="sxs-lookup"><span data-stu-id="3cd51-135">performance improvements;</span></span>
- <span data-ttu-id="3cd51-136">améliorations de la serviceabilité ; et</span><span class="sxs-lookup"><span data-stu-id="3cd51-136">serviceability improvements; and</span></span> 
- <span data-ttu-id="3cd51-137">améliorations de l’intégration (Cloud, [Microsoft 365 Defender](/microsoft-365/security/defender/microsoft-365-defender)).</span><span class="sxs-lookup"><span data-stu-id="3cd51-137">integration improvements (Cloud, [Microsoft 365 Defender](/microsoft-365/security/defender/microsoft-365-defender)).</span></span>
<br/>
<details>
<summary> <span data-ttu-id="3cd51-138">Mai-2021 (plateforme : 4.18.2105.4 | Moteur : 1.1.18200.4)</span><span class="sxs-lookup"><span data-stu-id="3cd51-138">May-2021 (Platform: 4.18.2105.4 | Engine: 1.1.18200.4)</span></span></summary>

<span data-ttu-id="3cd51-139">&ensp;Version de mise à jour des informations de sécurité **: 1.341.8.0**</span><span class="sxs-lookup"><span data-stu-id="3cd51-139">&ensp;Security intelligence update version: **1.341.8.0**</span></span>  
<span data-ttu-id="3cd51-140">&ensp;Publication : **4 juin 2021**</span><span class="sxs-lookup"><span data-stu-id="3cd51-140">&ensp;Released: **June 4, 2021**</span></span>  
<span data-ttu-id="3cd51-141">&ensp;Plateforme : **4.18.2105.4**</span><span class="sxs-lookup"><span data-stu-id="3cd51-141">&ensp;Platform: **4.18.2105.4**</span></span>  
<span data-ttu-id="3cd51-142">&ensp;Moteur : **1.1.18200.4**</span><span class="sxs-lookup"><span data-stu-id="3cd51-142">&ensp;Engine: **1.1.18200.4**</span></span>  
<span data-ttu-id="3cd51-143">&ensp;Phase de prise en charge **: Mises à jour critiques et de sécurité**</span><span class="sxs-lookup"><span data-stu-id="3cd51-143">&ensp;Support phase: **Security and Critical Updates**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="3cd51-144">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="3cd51-144">What's new</span></span>
- <span data-ttu-id="3cd51-145">Améliorations apportées à la [surveillance du comportement](client-behavioral-blocking.md)</span><span class="sxs-lookup"><span data-stu-id="3cd51-145">Improvements to [behavior monitoring](client-behavioral-blocking.md)</span></span> 
- <span data-ttu-id="3cd51-146">Fonctionnalité de [filtrage des](network-protection.md) notifications de protection réseau fixe</span><span class="sxs-lookup"><span data-stu-id="3cd51-146">Fixed [network protection](network-protection.md) notification filtering feature</span></span>

### <a name="known-issues"></a><span data-ttu-id="3cd51-147">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="3cd51-147">Known Issues</span></span>
<span data-ttu-id="3cd51-148">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="3cd51-148">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="3cd51-149">Avril-2021 (plateforme : 4.18.2104.14 | Moteur : 1.1.18100.5)</span><span class="sxs-lookup"><span data-stu-id="3cd51-149">April-2021 (Platform: 4.18.2104.14 | Engine: 1.1.18100.5)</span></span></summary>

<span data-ttu-id="3cd51-150">&ensp;Version de mise à jour des informations de sécurité **: 1.337.2.0**</span><span class="sxs-lookup"><span data-stu-id="3cd51-150">&ensp;Security intelligence update version: **1.337.2.0**</span></span>  
<span data-ttu-id="3cd51-151">&ensp;Publication : **1er avril 2021**</span><span class="sxs-lookup"><span data-stu-id="3cd51-151">&ensp;Released: **April 1, 2021**</span></span>  
<span data-ttu-id="3cd51-152">&ensp;Plateforme : **4.18.2104.14**</span><span class="sxs-lookup"><span data-stu-id="3cd51-152">&ensp;Platform: **4.18.2104.14**</span></span>  
<span data-ttu-id="3cd51-153">&ensp;Moteur : **1.1.18100.5**</span><span class="sxs-lookup"><span data-stu-id="3cd51-153">&ensp;Engine: **1.1.18100.5**</span></span>  
<span data-ttu-id="3cd51-154">&ensp;Phase de prise en charge **: Mises à jour critiques et de sécurité**</span><span class="sxs-lookup"><span data-stu-id="3cd51-154">&ensp;Support phase: **Security and Critical Updates**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="3cd51-155">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="3cd51-155">What's new</span></span>
- <span data-ttu-id="3cd51-156">Logique d’analyse de comportement supplémentaire</span><span class="sxs-lookup"><span data-stu-id="3cd51-156">Additional behavior monitoring logic</span></span>
- <span data-ttu-id="3cd51-157">Détection améliorée du keylogger en mode noyau</span><span class="sxs-lookup"><span data-stu-id="3cd51-157">Improved kernel mode keylogger detection</span></span>

### <a name="known-issues"></a><span data-ttu-id="3cd51-158">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="3cd51-158">Known Issues</span></span>
<span data-ttu-id="3cd51-159">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="3cd51-159">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="3cd51-160">Mars-2021 (plateforme : 4.18.2103.7 | Moteur : 1.1.18000.5)</span><span class="sxs-lookup"><span data-stu-id="3cd51-160">March-2021 (Platform: 4.18.2103.7 | Engine: 1.1.18000.5)</span></span></summary>

<span data-ttu-id="3cd51-161">&ensp;Version de mise à jour des informations de sécurité **: 1.335.36.0**</span><span class="sxs-lookup"><span data-stu-id="3cd51-161">&ensp;Security intelligence update version: **1.335.36.0**</span></span>  
<span data-ttu-id="3cd51-162">&ensp;Publication : **1er avril 2021**</span><span class="sxs-lookup"><span data-stu-id="3cd51-162">&ensp;Released: **April 1, 2021**</span></span>  
<span data-ttu-id="3cd51-163">&ensp;Plateforme : **4.18.2103.7**</span><span class="sxs-lookup"><span data-stu-id="3cd51-163">&ensp;Platform: **4.18.2103.7**</span></span>  
<span data-ttu-id="3cd51-164">&ensp;Moteur : **1.1.18000.5**</span><span class="sxs-lookup"><span data-stu-id="3cd51-164">&ensp;Engine: **1.1.18000.5**</span></span>  
<span data-ttu-id="3cd51-165">&ensp;Phase de prise en charge **: Mises à jour critiques et de sécurité**</span><span class="sxs-lookup"><span data-stu-id="3cd51-165">&ensp;Support phase: **Security and Critical Updates**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="3cd51-166">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="3cd51-166">What's new</span></span>

- <span data-ttu-id="3cd51-167">Amélioration du moteur d’analyse du comportement</span><span class="sxs-lookup"><span data-stu-id="3cd51-167">Improvement to the Behavior Monitoring engine</span></span> 
- <span data-ttu-id="3cd51-168">Préventions d’attaques par force brute du réseau étendu</span><span class="sxs-lookup"><span data-stu-id="3cd51-168">Expanded network brute-force-attack mitigations</span></span> 
- <span data-ttu-id="3cd51-169">Génération d’événements de tentative de falsification en échec supplémentaires lorsque la [protection](prevent-changes-to-security-settings-with-tamper-protection.md) contre la falsification est activée</span><span class="sxs-lookup"><span data-stu-id="3cd51-169">Additional failed tampering attempt event generation when [Tamper Protection](prevent-changes-to-security-settings-with-tamper-protection.md) is enabled</span></span>

### <a name="known-issues"></a><span data-ttu-id="3cd51-170">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="3cd51-170">Known Issues</span></span>
<span data-ttu-id="3cd51-171">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="3cd51-171">No known issues</span></span>  
<br/>
</details>

### <a name="previous-version-updates-technical-upgrade-support-only"></a><span data-ttu-id="3cd51-172">Mises à jour de version précédente : prise en charge de la mise à niveau technique uniquement</span><span class="sxs-lookup"><span data-stu-id="3cd51-172">Previous version updates: Technical upgrade support only</span></span>

<span data-ttu-id="3cd51-173">Après la publication d’une nouvelle version de package, la prise en charge des deux versions précédentes est réduite au support technique uniquement.</span><span class="sxs-lookup"><span data-stu-id="3cd51-173">After a new package version is released, support for the previous two versions is reduced to technical support only.</span></span> <span data-ttu-id="3cd51-174">Les versions antérieures à celles répertoriées dans cette section sont fournies uniquement pour la prise en charge de la mise à niveau technique.</span><span class="sxs-lookup"><span data-stu-id="3cd51-174">Versions older than that are listed in this section, and are provided for technical upgrade support only.</span></span> 
<br/><br/>
<details>
<summary> <span data-ttu-id="3cd51-175">Février-2021 (plateforme : 4.18.2102.3 | Moteur : 1.1.17900.7)</span><span class="sxs-lookup"><span data-stu-id="3cd51-175">February-2021 (Platform: 4.18.2102.3 | Engine: 1.1.17900.7)</span></span></summary>

<span data-ttu-id="3cd51-176">&ensp;Version de mise à jour des informations de sécurité **: 1.333.7.0**</span><span class="sxs-lookup"><span data-stu-id="3cd51-176">&ensp;Security intelligence update version: **1.333.7.0**</span></span>  
<span data-ttu-id="3cd51-177">&ensp;Publication : **9 mars 2021**</span><span class="sxs-lookup"><span data-stu-id="3cd51-177">&ensp;Released: **March 9, 2021**</span></span>  
<span data-ttu-id="3cd51-178">&ensp;Plateforme : **4.18.2102.3**</span><span class="sxs-lookup"><span data-stu-id="3cd51-178">&ensp;Platform: **4.18.2102.3**</span></span>  
<span data-ttu-id="3cd51-179">&ensp;Moteur : **1.1.17900.7**</span><span class="sxs-lookup"><span data-stu-id="3cd51-179">&ensp;Engine: **1.1.17900.7**</span></span>  
<span data-ttu-id="3cd51-180">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="3cd51-180">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="3cd51-181">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="3cd51-181">What's new</span></span>

- <span data-ttu-id="3cd51-182">Amélioration de la récupération du service par le biais [de la protection contre la falsification](prevent-changes-to-security-settings-with-tamper-protection.md)</span><span class="sxs-lookup"><span data-stu-id="3cd51-182">Improved service recovery through [tamper protection](prevent-changes-to-security-settings-with-tamper-protection.md)</span></span>
- <span data-ttu-id="3cd51-183">Étendre l’étendue de la protection contre la falsification</span><span class="sxs-lookup"><span data-stu-id="3cd51-183">Extend tamper protection scope</span></span>

### <a name="known-issues"></a><span data-ttu-id="3cd51-184">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="3cd51-184">Known Issues</span></span>
<span data-ttu-id="3cd51-185">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="3cd51-185">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="3cd51-186">Janvier-2021 (plateforme : 4.18.2101.9 | Moteur : 1.1.17800.5)</span><span class="sxs-lookup"><span data-stu-id="3cd51-186">January-2021 (Platform: 4.18.2101.9 | Engine: 1.1.17800.5)</span></span></summary>

<span data-ttu-id="3cd51-187">&ensp;Version de mise à jour des informations de sécurité **: 1.327.1854.0**</span><span class="sxs-lookup"><span data-stu-id="3cd51-187">&ensp;Security intelligence update version: **1.327.1854.0**</span></span>  
<span data-ttu-id="3cd51-188">&ensp;Publication : **2 février 2021**</span><span class="sxs-lookup"><span data-stu-id="3cd51-188">&ensp;Released: **February 2, 2021**</span></span>  
<span data-ttu-id="3cd51-189">&ensp;Plateforme : **4.18.2101.9**</span><span class="sxs-lookup"><span data-stu-id="3cd51-189">&ensp;Platform: **4.18.2101.9**</span></span>  
<span data-ttu-id="3cd51-190">&ensp;Moteur : **1.1.17800.5**</span><span class="sxs-lookup"><span data-stu-id="3cd51-190">&ensp;Engine: **1.1.17800.5**</span></span>  
<span data-ttu-id="3cd51-191">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="3cd51-191">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="3cd51-192">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="3cd51-192">What's new</span></span>

- <span data-ttu-id="3cd51-193">Améliorations de la détection d’exploits shellcode</span><span class="sxs-lookup"><span data-stu-id="3cd51-193">Shellcode exploit detection improvements</span></span>
- <span data-ttu-id="3cd51-194">Visibilité accrue des tentatives de vol d’informations d’identification</span><span class="sxs-lookup"><span data-stu-id="3cd51-194">Increased visibility for credential stealing attempts</span></span>
- <span data-ttu-id="3cd51-195">Améliorations des fonctionnalités antitampering dans Antivirus Microsoft Defender services</span><span class="sxs-lookup"><span data-stu-id="3cd51-195">Improvements in antitampering features in Microsoft Defender Antivirus services</span></span>
- <span data-ttu-id="3cd51-196">Prise en charge améliorée de l ARM éulation x64</span><span class="sxs-lookup"><span data-stu-id="3cd51-196">Improved support for ARM x64 emulation</span></span>
- <span data-ttu-id="3cd51-197">Correctif : PEPT notification de blocage reste dans l’historique des menaces après la détection initiale de la protection en temps réel</span><span class="sxs-lookup"><span data-stu-id="3cd51-197">Fix: EDR Block notification remains in threat history after real-time protection performed initial detection</span></span>

### <a name="known-issues"></a><span data-ttu-id="3cd51-198">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="3cd51-198">Known Issues</span></span>
<span data-ttu-id="3cd51-199">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="3cd51-199">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="3cd51-200">Novembre-2020 (plateforme : 4.18.2011.6 | Moteur : 1.1.17700.4)</span><span class="sxs-lookup"><span data-stu-id="3cd51-200">November-2020 (Platform: 4.18.2011.6 | Engine: 1.1.17700.4)</span></span></summary>

<span data-ttu-id="3cd51-201">&ensp;Version de mise à jour des informations de sécurité **: 1.327.1854.0**</span><span class="sxs-lookup"><span data-stu-id="3cd51-201">&ensp;Security intelligence update version: **1.327.1854.0**</span></span>  
<span data-ttu-id="3cd51-202">&ensp;Publication : **03 décembre 2020**</span><span class="sxs-lookup"><span data-stu-id="3cd51-202">&ensp;Released: **December 03, 2020**</span></span>  
<span data-ttu-id="3cd51-203">&ensp;Plateforme : **4.18.2011.6**</span><span class="sxs-lookup"><span data-stu-id="3cd51-203">&ensp;Platform: **4.18.2011.6**</span></span>  
<span data-ttu-id="3cd51-204">&ensp;Moteur : **1.1.17700.4**</span><span class="sxs-lookup"><span data-stu-id="3cd51-204">&ensp;Engine: **1.1.17700.4**</span></span>  
<span data-ttu-id="3cd51-205">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="3cd51-205">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="3cd51-206">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="3cd51-206">What's new</span></span>

- <span data-ttu-id="3cd51-207">Amélioration de la [journalisation de la prise en](/windows/security/threat-protection/microsoft-defender-smartscreen/microsoft-defender-smartscreen-overview) charge de l’état SmartScreen</span><span class="sxs-lookup"><span data-stu-id="3cd51-207">Improved [SmartScreen](/windows/security/threat-protection/microsoft-defender-smartscreen/microsoft-defender-smartscreen-overview) status support logging</span></span>

### <a name="known-issues"></a><span data-ttu-id="3cd51-208">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="3cd51-208">Known Issues</span></span>
<span data-ttu-id="3cd51-209">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="3cd51-209">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="3cd51-210">Octobre-2020 (plateforme : 4.18.2010.7 | Moteur : 1.1.17600.5)</span><span class="sxs-lookup"><span data-stu-id="3cd51-210">October-2020 (Platform: 4.18.2010.7 | Engine: 1.1.17600.5)</span></span></summary>

<span data-ttu-id="3cd51-211">&ensp;Version de mise à jour des informations de sécurité **: 1.327.7.0**</span><span class="sxs-lookup"><span data-stu-id="3cd51-211">&ensp;Security intelligence update version: **1.327.7.0**</span></span>  
<span data-ttu-id="3cd51-212">&ensp;Publication : **29 octobre 2020**</span><span class="sxs-lookup"><span data-stu-id="3cd51-212">&ensp;Released: **October 29, 2020**</span></span>  
<span data-ttu-id="3cd51-213">&ensp;Plateforme : **4.18.2010.7**</span><span class="sxs-lookup"><span data-stu-id="3cd51-213">&ensp;Platform: **4.18.2010.7**</span></span>  
<span data-ttu-id="3cd51-214">&ensp;Moteur : **1.1.17600.5**</span><span class="sxs-lookup"><span data-stu-id="3cd51-214">&ensp;Engine: **1.1.17600.5**</span></span>  
<span data-ttu-id="3cd51-215">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="3cd51-215">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="3cd51-216">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="3cd51-216">What's new</span></span>

- <span data-ttu-id="3cd51-217">Nouvelles descriptions pour les catégories de menaces spéciales</span><span class="sxs-lookup"><span data-stu-id="3cd51-217">New descriptions for special threat categories</span></span>
- <span data-ttu-id="3cd51-218">Fonctionnalités d’émulation améliorées</span><span class="sxs-lookup"><span data-stu-id="3cd51-218">Improved emulation capabilities</span></span>
- <span data-ttu-id="3cd51-219">Fonctionnalités améliorées d’autoriser/bloquer l’adresse hôte</span><span class="sxs-lookup"><span data-stu-id="3cd51-219">Improved host address allow/block capabilities</span></span>
- <span data-ttu-id="3cd51-220">Nouvelle option dans le programme CSP Defender pour ignorer la fusion des exclusions des utilisateurs locaux</span><span class="sxs-lookup"><span data-stu-id="3cd51-220">New option in Defender CSP to Ignore merging of local user exclusions</span></span>

### <a name="known-issues"></a><span data-ttu-id="3cd51-221">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="3cd51-221">Known Issues</span></span>

<span data-ttu-id="3cd51-222">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="3cd51-222">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="3cd51-223">Septembre-2020 (plateforme : 4.18.2009.7 | Moteur : 1.1.17500.4)</span><span class="sxs-lookup"><span data-stu-id="3cd51-223">September-2020 (Platform: 4.18.2009.7 | Engine: 1.1.17500.4)</span></span></summary>

<span data-ttu-id="3cd51-224">&ensp;Version de mise à jour des informations de sécurité **: 1.325.10.0**</span><span class="sxs-lookup"><span data-stu-id="3cd51-224">&ensp;Security intelligence update version: **1.325.10.0**</span></span>  
<span data-ttu-id="3cd51-225">&ensp;Publication : **01 octobre 2020**</span><span class="sxs-lookup"><span data-stu-id="3cd51-225">&ensp;Released: **October 01, 2020**</span></span>  
<span data-ttu-id="3cd51-226">&ensp;Plateforme : **4.18.2009.7**</span><span class="sxs-lookup"><span data-stu-id="3cd51-226">&ensp;Platform: **4.18.2009.7**</span></span>  
<span data-ttu-id="3cd51-227">&ensp;Moteur : **1.1.17500.4**</span><span class="sxs-lookup"><span data-stu-id="3cd51-227">&ensp;Engine: **1.1.17500.4**</span></span>  
<span data-ttu-id="3cd51-228">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="3cd51-228">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="3cd51-229">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="3cd51-229">What's new</span></span>

- <span data-ttu-id="3cd51-230">Des autorisations d’administrateur sont requises pour restaurer les fichiers en quarantaine</span><span class="sxs-lookup"><span data-stu-id="3cd51-230">Admin permissions are required to restore files in quarantine</span></span>
- <span data-ttu-id="3cd51-231">Les événements au format XML sont désormais pris en charge</span><span class="sxs-lookup"><span data-stu-id="3cd51-231">XML formatted events are now supported</span></span>
- <span data-ttu-id="3cd51-232">Prise en charge du programme CSP pour ignorer les fusions d’exclusions</span><span class="sxs-lookup"><span data-stu-id="3cd51-232">CSP support for ignoring exclusion merges</span></span>
- <span data-ttu-id="3cd51-233">Nouvelles interfaces de gestion pour :</span><span class="sxs-lookup"><span data-stu-id="3cd51-233">New management interfaces for:</span></span>
   - <span data-ttu-id="3cd51-234">UDP Inspection</span><span class="sxs-lookup"><span data-stu-id="3cd51-234">UDP Inspection</span></span>
   - <span data-ttu-id="3cd51-235">Protection du réseau sur Server 2019</span><span class="sxs-lookup"><span data-stu-id="3cd51-235">Network Protection on Server 2019</span></span>
   - <span data-ttu-id="3cd51-236">Exclusions d’adresses IP pour la protection du réseau</span><span class="sxs-lookup"><span data-stu-id="3cd51-236">IP Address exclusions for Network Protection</span></span>
- <span data-ttu-id="3cd51-237">Meilleure visibilité des mesures du TPM</span><span class="sxs-lookup"><span data-stu-id="3cd51-237">Improved visibility into TPM measurements</span></span>
- <span data-ttu-id="3cd51-238">Amélioration de l Office de module VBA</span><span class="sxs-lookup"><span data-stu-id="3cd51-238">Improved Office VBA module scanning</span></span>

### <a name="known-issues"></a><span data-ttu-id="3cd51-239">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="3cd51-239">Known Issues</span></span>

<span data-ttu-id="3cd51-240">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="3cd51-240">No known issues</span></span>  
<br/>
</details>
<details>
<summary> <span data-ttu-id="3cd51-241">Août-2020 (plateforme : 4.18.2008.9 | Moteur : 1.1.17400.5)</span><span class="sxs-lookup"><span data-stu-id="3cd51-241">August-2020 (Platform: 4.18.2008.9 | Engine: 1.1.17400.5)</span></span></summary>

<span data-ttu-id="3cd51-242">&ensp;Version de mise à jour des informations de sécurité **: 1.323.9.0**</span><span class="sxs-lookup"><span data-stu-id="3cd51-242">&ensp;Security intelligence update version: **1.323.9.0**</span></span>  
<span data-ttu-id="3cd51-243">&ensp;Publication : **27 août 2020**</span><span class="sxs-lookup"><span data-stu-id="3cd51-243">&ensp;Released: **August 27, 2020**</span></span>  
<span data-ttu-id="3cd51-244">&ensp;Plateforme : **4.18.2008.9**</span><span class="sxs-lookup"><span data-stu-id="3cd51-244">&ensp;Platform: **4.18.2008.9**</span></span>  
<span data-ttu-id="3cd51-245">&ensp;Moteur : **1.1.17400.5**</span><span class="sxs-lookup"><span data-stu-id="3cd51-245">&ensp;Engine: **1.1.17400.5**</span></span>  
<span data-ttu-id="3cd51-246">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="3cd51-246">&ensp;Support phase: **Technical upgrade support (only)**</span></span>

### <a name="whats-new"></a><span data-ttu-id="3cd51-247">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="3cd51-247">What's new</span></span>

- <span data-ttu-id="3cd51-248">Ajouter d’autres événements de télémétrie</span><span class="sxs-lookup"><span data-stu-id="3cd51-248">Add more telemetry events</span></span>
- <span data-ttu-id="3cd51-249">Télémétrie améliorée des événements d’analyse</span><span class="sxs-lookup"><span data-stu-id="3cd51-249">Improved scan event telemetry</span></span>
- <span data-ttu-id="3cd51-250">Amélioration de la surveillance du comportement pour les analyses de mémoire</span><span class="sxs-lookup"><span data-stu-id="3cd51-250">Improved behavior monitoring for memory scans</span></span>
- <span data-ttu-id="3cd51-251">Amélioration de l’analyse des flux de macros</span><span class="sxs-lookup"><span data-stu-id="3cd51-251">Improved macro streams scanning</span></span>
- <span data-ttu-id="3cd51-252">Ajouté à `AMRunningMode` la Get-MpComputerStatus cmdlet PowerShell</span><span class="sxs-lookup"><span data-stu-id="3cd51-252">Added `AMRunningMode` to Get-MpComputerStatus PowerShell cmdlet</span></span>
- <span data-ttu-id="3cd51-253">[DisableAntiSpyware](/windows-hardware/customize/desktop/unattend/security-malware-windows-defender-disableantispyware) est ignoré.</span><span class="sxs-lookup"><span data-stu-id="3cd51-253">[DisableAntiSpyware](/windows-hardware/customize/desktop/unattend/security-malware-windows-defender-disableantispyware) is ignored.</span></span> <span data-ttu-id="3cd51-254">Antivirus Microsoft Defender s’arrête automatiquement lorsqu’il détecte un autre programme antivirus.</span><span class="sxs-lookup"><span data-stu-id="3cd51-254">Microsoft Defender Antivirus automatically turns itself off when it detects another antivirus program.</span></span>


### <a name="known-issues"></a><span data-ttu-id="3cd51-255">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="3cd51-255">Known Issues</span></span>
<span data-ttu-id="3cd51-256">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="3cd51-256">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="3cd51-257">Juillet-2020 (plateforme : 4.18.2007.8 | Moteur : 1.1.17300.4)</span><span class="sxs-lookup"><span data-stu-id="3cd51-257">July-2020 (Platform: 4.18.2007.8 | Engine: 1.1.17300.4)</span></span></summary>

<span data-ttu-id="3cd51-258">&ensp;Version de mise à jour des informations de sécurité **: 1.321.30.0**</span><span class="sxs-lookup"><span data-stu-id="3cd51-258">&ensp;Security intelligence update version: **1.321.30.0**</span></span>  
<span data-ttu-id="3cd51-259">&ensp;Publication : **28 juillet 2020**</span><span class="sxs-lookup"><span data-stu-id="3cd51-259">&ensp;Released: **July 28, 2020**</span></span>  
<span data-ttu-id="3cd51-260">&ensp;Plateforme : **4.18.2007.8**</span><span class="sxs-lookup"><span data-stu-id="3cd51-260">&ensp;Platform: **4.18.2007.8**</span></span>  
<span data-ttu-id="3cd51-261">&ensp;Moteur : **1.1.17300.4**</span><span class="sxs-lookup"><span data-stu-id="3cd51-261">&ensp;Engine: **1.1.17300.4**</span></span>  
<span data-ttu-id="3cd51-262">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="3cd51-262">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="3cd51-263">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="3cd51-263">What's new</span></span>

- <span data-ttu-id="3cd51-264">Télémétrie améliorée pour BITS</span><span class="sxs-lookup"><span data-stu-id="3cd51-264">Improved telemetry for BITS</span></span>
- <span data-ttu-id="3cd51-265">Validation améliorée du certificat de signature de code Authenticode</span><span class="sxs-lookup"><span data-stu-id="3cd51-265">Improved Authenticode code signing certificate validation</span></span>

### <a name="known-issues"></a><span data-ttu-id="3cd51-266">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="3cd51-266">Known Issues</span></span>
<span data-ttu-id="3cd51-267">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="3cd51-267">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="3cd51-268">Juin-2020 (plateforme : 4.18.2006.10 | Moteur : 1.1.17200.2)</span><span class="sxs-lookup"><span data-stu-id="3cd51-268">June-2020 (Platform: 4.18.2006.10 | Engine: 1.1.17200.2)</span></span></summary>

<span data-ttu-id="3cd51-269">&ensp;Version de mise à jour des informations de sécurité **: 1.319.20.0**</span><span class="sxs-lookup"><span data-stu-id="3cd51-269">&ensp;Security intelligence update version: **1.319.20.0**</span></span>  
<span data-ttu-id="3cd51-270">&ensp;Publication : **22 juin 2020**</span><span class="sxs-lookup"><span data-stu-id="3cd51-270">&ensp;Released: **June 22, 2020**</span></span>  
<span data-ttu-id="3cd51-271">&ensp;Plateforme : **4.18.2006.10**</span><span class="sxs-lookup"><span data-stu-id="3cd51-271">&ensp;Platform: **4.18.2006.10**</span></span>  
<span data-ttu-id="3cd51-272">&ensp;Moteur : **1.1.17200.2**</span><span class="sxs-lookup"><span data-stu-id="3cd51-272">&ensp;Engine: **1.1.17200.2**</span></span>  
<span data-ttu-id="3cd51-273">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="3cd51-273">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="3cd51-274">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="3cd51-274">What's new</span></span>

- <span data-ttu-id="3cd51-275">Possibilité de spécifier [l’emplacement des journaux de support](./collect-diagnostic-data.md)</span><span class="sxs-lookup"><span data-stu-id="3cd51-275">Possibility to specify the [location of the support logs](./collect-diagnostic-data.md)</span></span>
- <span data-ttu-id="3cd51-276">Ignorer l’analyse de rattrapage agressive en mode passif.</span><span class="sxs-lookup"><span data-stu-id="3cd51-276">Skipping aggressive catchup scan in Passive mode.</span></span>
- <span data-ttu-id="3cd51-277">Autoriser Defender à se mettre à jour sur les connexions à connexions avec des compteurs</span><span class="sxs-lookup"><span data-stu-id="3cd51-277">Allow Defender to update on metered connections</span></span>
- <span data-ttu-id="3cd51-278">Réglage des performances fixes lorsque la mise en cache est désactivée</span><span class="sxs-lookup"><span data-stu-id="3cd51-278">Fixed performance tuning when caching is disabled</span></span> 
- <span data-ttu-id="3cd51-279">Requête de Registre fixe</span><span class="sxs-lookup"><span data-stu-id="3cd51-279">Fixed registry query</span></span> 
- <span data-ttu-id="3cd51-280">Randomisation du scantime fixe dans ADMX</span><span class="sxs-lookup"><span data-stu-id="3cd51-280">Fixed scantime randomization in ADMX</span></span>

### <a name="known-issues"></a><span data-ttu-id="3cd51-281">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="3cd51-281">Known Issues</span></span>
<span data-ttu-id="3cd51-282">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="3cd51-282">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="3cd51-283">Mai-2020 (plateforme : 4.18.2005.4 | Moteur : 1.1.17100.2)</span><span class="sxs-lookup"><span data-stu-id="3cd51-283">May-2020 (Platform: 4.18.2005.4 | Engine: 1.1.17100.2)</span></span></summary>

<span data-ttu-id="3cd51-284">&ensp;Version de mise à jour des informations de sécurité **: 1.317.20.0**</span><span class="sxs-lookup"><span data-stu-id="3cd51-284">&ensp;Security intelligence update version: **1.317.20.0**</span></span>  
<span data-ttu-id="3cd51-285">&ensp;Publication : **26 mai 2020**</span><span class="sxs-lookup"><span data-stu-id="3cd51-285">&ensp;Released: **May 26, 2020**</span></span>  
<span data-ttu-id="3cd51-286">&ensp;Plateforme : **4.18.2005.4**</span><span class="sxs-lookup"><span data-stu-id="3cd51-286">&ensp;Platform: **4.18.2005.4**</span></span>  
<span data-ttu-id="3cd51-287">&ensp;Moteur : **1.1.17100.2**</span><span class="sxs-lookup"><span data-stu-id="3cd51-287">&ensp;Engine: **1.1.17100.2**</span></span>  
<span data-ttu-id="3cd51-288">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="3cd51-288">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="3cd51-289">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="3cd51-289">What's new</span></span>

- <span data-ttu-id="3cd51-290">Enregistrement amélioré pour les événements d’analyse</span><span class="sxs-lookup"><span data-stu-id="3cd51-290">Improved logging for scan events</span></span>
- <span data-ttu-id="3cd51-291">Amélioration de la gestion des incidents en mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3cd51-291">Improved user mode crash handling.</span></span>
- <span data-ttu-id="3cd51-292">Suivi des événements ajouté pour la protection contre la falsification</span><span class="sxs-lookup"><span data-stu-id="3cd51-292">Added event tracing for Tamper protection</span></span>
- <span data-ttu-id="3cd51-293">Envoi d’exemples AMSI fixes</span><span class="sxs-lookup"><span data-stu-id="3cd51-293">Fixed AMSI Sample submission</span></span>
- <span data-ttu-id="3cd51-294">Blocage du cloud AMSI fixe</span><span class="sxs-lookup"><span data-stu-id="3cd51-294">Fixed AMSI Cloud blocking</span></span>
- <span data-ttu-id="3cd51-295">Journal d’installation des mises à jour de sécurité fixes</span><span class="sxs-lookup"><span data-stu-id="3cd51-295">Fixed Security update install log</span></span>

### <a name="known-issues"></a><span data-ttu-id="3cd51-296">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="3cd51-296">Known Issues</span></span>
<span data-ttu-id="3cd51-297">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="3cd51-297">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="3cd51-298">Avril-2020 (plateforme : 4.18.2004.6 | Moteur : 1.1.17000.2)</span><span class="sxs-lookup"><span data-stu-id="3cd51-298">April-2020 (Platform: 4.18.2004.6 | Engine: 1.1.17000.2)</span></span></summary>

<span data-ttu-id="3cd51-299">&ensp;Version de mise à jour des informations de sécurité **: 1.315.12.0**</span><span class="sxs-lookup"><span data-stu-id="3cd51-299">&ensp;Security intelligence update version: **1.315.12.0**</span></span>  
<span data-ttu-id="3cd51-300">&ensp;Publication : **30 avril 2020**</span><span class="sxs-lookup"><span data-stu-id="3cd51-300">&ensp;Released: **April 30, 2020**</span></span>  
<span data-ttu-id="3cd51-301">&ensp;Plateforme : **4.18.2004.6**</span><span class="sxs-lookup"><span data-stu-id="3cd51-301">&ensp;Platform: **4.18.2004.6**</span></span>  
<span data-ttu-id="3cd51-302">&ensp;Moteur : **1.1.17000.2**</span><span class="sxs-lookup"><span data-stu-id="3cd51-302">&ensp;Engine: **1.1.17000.2**</span></span>  
<span data-ttu-id="3cd51-303">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="3cd51-303">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="3cd51-304">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="3cd51-304">What's new</span></span>
- <span data-ttu-id="3cd51-305">Améliorations apportées aux filtres WDfilter</span><span class="sxs-lookup"><span data-stu-id="3cd51-305">WDfilter improvements</span></span>
- <span data-ttu-id="3cd51-306">Ajouter des données d’événements actionnables à des événements de détection de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="3cd51-306">Add more actionable event data to attack surface reduction detection events</span></span>
- <span data-ttu-id="3cd51-307">Informations de version fixes dans les données de diagnostic et WMI</span><span class="sxs-lookup"><span data-stu-id="3cd51-307">Fixed version information in diagnostic data and WMI</span></span>
- <span data-ttu-id="3cd51-308">Version de plateforme incorrecte corrigée dans l’interface utilisateur après la mise à jour de la plateforme</span><span class="sxs-lookup"><span data-stu-id="3cd51-308">Fixed incorrect platform version in UI after platform update</span></span>
- <span data-ttu-id="3cd51-309">Intel d’URL dynamique pour la protection contre les menaces sans fichier</span><span class="sxs-lookup"><span data-stu-id="3cd51-309">Dynamic URL intel for Fileless threat protection</span></span>
- <span data-ttu-id="3cd51-310">Fonctionnalité d’analyse UEFI</span><span class="sxs-lookup"><span data-stu-id="3cd51-310">UEFI scan capability</span></span>
- <span data-ttu-id="3cd51-311">Étendre la journalisation pour les mises à jour</span><span class="sxs-lookup"><span data-stu-id="3cd51-311">Extend logging for updates</span></span>

### <a name="known-issues"></a><span data-ttu-id="3cd51-312">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="3cd51-312">Known Issues</span></span>
<span data-ttu-id="3cd51-313">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="3cd51-313">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="3cd51-314">Mars-2020 (plateforme : 4.18.2003.8 | Moteur : 1.1.16900.2)</span><span class="sxs-lookup"><span data-stu-id="3cd51-314">March-2020 (Platform: 4.18.2003.8 | Engine: 1.1.16900.2)</span></span></summary>

<span data-ttu-id="3cd51-315">&ensp;Version de mise à jour des informations de sécurité **: 1.313.8.0**</span><span class="sxs-lookup"><span data-stu-id="3cd51-315">&ensp;Security intelligence update version: **1.313.8.0**</span></span>  
<span data-ttu-id="3cd51-316">&ensp;Publication : **24 mars 2020**</span><span class="sxs-lookup"><span data-stu-id="3cd51-316">&ensp;Released: **March 24, 2020**</span></span>  
<span data-ttu-id="3cd51-317">&ensp;Plateforme : **4.18.2003.8**</span><span class="sxs-lookup"><span data-stu-id="3cd51-317">&ensp;Platform: **4.18.2003.8**</span></span>  
<span data-ttu-id="3cd51-318">&ensp;Moteur : **1.1.16900.4**</span><span class="sxs-lookup"><span data-stu-id="3cd51-318">&ensp;Engine: **1.1.16900.4**</span></span>  
<span data-ttu-id="3cd51-319">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="3cd51-319">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="3cd51-320">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="3cd51-320">What's new</span></span>

- <span data-ttu-id="3cd51-321">Option limitation du processeur ajoutée à [MpCmdRun](./command-line-arguments-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="3cd51-321">CPU Throttling option added to [MpCmdRun](./command-line-arguments-microsoft-defender-antivirus.md)</span></span>
- <span data-ttu-id="3cd51-322">Améliorer les fonctionnalités de diagnostic</span><span class="sxs-lookup"><span data-stu-id="3cd51-322">Improve diagnostic capability</span></span>
- <span data-ttu-id="3cd51-323">réduire le délai d’out des informations de sécurité (5 min)</span><span class="sxs-lookup"><span data-stu-id="3cd51-323">reduce Security intelligence timeout (5 min)</span></span>
- <span data-ttu-id="3cd51-324">Étendre la fonctionnalité de journal interne du moteur AMSI</span><span class="sxs-lookup"><span data-stu-id="3cd51-324">Extend AMSI engine internal log capability</span></span>
- <span data-ttu-id="3cd51-325">Améliorer la notification pour le blocage des processus</span><span class="sxs-lookup"><span data-stu-id="3cd51-325">Improve notification for process blocking</span></span>
   
### <a name="known-issues"></a><span data-ttu-id="3cd51-326">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="3cd51-326">Known Issues</span></span>
<span data-ttu-id="3cd51-327">[**Fixe**] Antivirus Microsoft Defender ignorer les fichiers lors de l’exécution d’une analyse.</span><span class="sxs-lookup"><span data-stu-id="3cd51-327">[**Fixed**] Microsoft Defender Antivirus is skipping files when running a scan.</span></span>

<br/>
</details>

<details>

<summary> <span data-ttu-id="3cd51-328">Février-2020 (plateforme : - | Moteur : 1.1.16800.2)</span><span class="sxs-lookup"><span data-stu-id="3cd51-328">February-2020 (Platform: - | Engine: 1.1.16800.2)</span></span></summary>
  

<span data-ttu-id="3cd51-329">&ensp;Version de mise à jour des informations de sécurité **: 1.311.4.0** </span><span class="sxs-lookup"><span data-stu-id="3cd51-329">&ensp;Security intelligence update version: **1.311.4.0** </span></span>  
<span data-ttu-id="3cd51-330">&ensp;Publication : **25 février 2020**</span><span class="sxs-lookup"><span data-stu-id="3cd51-330">&ensp;Released: **February 25, 2020**</span></span>  
<span data-ttu-id="3cd51-331">&ensp;Plateforme/client : **-**</span><span class="sxs-lookup"><span data-stu-id="3cd51-331">&ensp;Platform/Client: **-**</span></span>  
<span data-ttu-id="3cd51-332">&ensp;Moteur : **1.1.16800.2**</span><span class="sxs-lookup"><span data-stu-id="3cd51-332">&ensp;Engine: **1.1.16800.2**</span></span>  
<span data-ttu-id="3cd51-333">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="3cd51-333">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
     
### <a name="whats-new"></a><span data-ttu-id="3cd51-334">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="3cd51-334">What's new</span></span>

  
### <a name="known-issues"></a><span data-ttu-id="3cd51-335">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="3cd51-335">Known Issues</span></span>
<span data-ttu-id="3cd51-336">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="3cd51-336">No known issues</span></span>
<br/>
</details>

<details>
<summary> <span data-ttu-id="3cd51-337">Janvier-2020 (plateforme : 4.18.2001.10 | Moteur : 1.1.16700.2)</span><span class="sxs-lookup"><span data-stu-id="3cd51-337">January-2020 (Platform: 4.18.2001.10 | Engine: 1.1.16700.2)</span></span></summary>
  

<span data-ttu-id="3cd51-338">Version de mise à jour des informations de sécurité **: 1.309.32.0**</span><span class="sxs-lookup"><span data-stu-id="3cd51-338">Security intelligence update version: **1.309.32.0**</span></span>  
<span data-ttu-id="3cd51-339">Publication : **30 janvier 2020**</span><span class="sxs-lookup"><span data-stu-id="3cd51-339">Released: **January 30, 2020**</span></span>  
<span data-ttu-id="3cd51-340">Plateforme/Client : **4.18.2001.10**</span><span class="sxs-lookup"><span data-stu-id="3cd51-340">Platform/Client: **4.18.2001.10**</span></span>  
<span data-ttu-id="3cd51-341">Moteur : **1.1.16700.2**</span><span class="sxs-lookup"><span data-stu-id="3cd51-341">Engine: **1.1.16700.2**</span></span>  
<span data-ttu-id="3cd51-342">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="3cd51-342">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
     
### <a name="whats-new"></a><span data-ttu-id="3cd51-343">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="3cd51-343">What's new</span></span>

- <span data-ttu-id="3cd51-344">Correction du BSOD sur WS2016 avec Exchange</span><span class="sxs-lookup"><span data-stu-id="3cd51-344">Fixed BSOD on WS2016 with Exchange</span></span>
- <span data-ttu-id="3cd51-345">Prise en charge des mises à jour de plateforme lorsque le TMP est redirigé vers le chemin d’accès réseau</span><span class="sxs-lookup"><span data-stu-id="3cd51-345">Support platform updates when TMP is redirected to network path</span></span>
- <span data-ttu-id="3cd51-346">Les versions de plateforme et de moteur sont [ajoutées à WDSI](https://www.microsoft.com/en-us/wdsi/defenderupdates)</span><span class="sxs-lookup"><span data-stu-id="3cd51-346">Platform and engine versions are added to [WDSI](https://www.microsoft.com/en-us/wdsi/defenderupdates)</span></span> <!-- The preceding URL must include "/en-us" -->
- <span data-ttu-id="3cd51-347">étendre la mise à jour des signatures d’urgence [en mode passif](./microsoft-defender-antivirus-compatibility.md)</span><span class="sxs-lookup"><span data-stu-id="3cd51-347">extend Emergency signature update to [passive mode](./microsoft-defender-antivirus-compatibility.md)</span></span>
- <span data-ttu-id="3cd51-348">Correction du problème de 4.18.1911.3</span><span class="sxs-lookup"><span data-stu-id="3cd51-348">Fix 4.18.1911.3 hang</span></span>
   
### <a name="known-issues"></a><span data-ttu-id="3cd51-349">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="3cd51-349">Known Issues</span></span>

<span data-ttu-id="3cd51-350">[**Fixe**] Les appareils utilisant le [mode](/windows-hardware/design/device-experiences/modern-standby) de veille moderne peuvent se bloquer avec le pilote de filtre Windows Defender, ce qui se traduit par un manque de protection.</span><span class="sxs-lookup"><span data-stu-id="3cd51-350">[**Fixed**] devices utilizing [modern standby mode](/windows-hardware/design/device-experiences/modern-standby) may experience a hang with the Windows Defender filter driver that results in a gap of protection.</span></span>  <span data-ttu-id="3cd51-351">Les ordinateurs concernés semblent ne pas avoir été mis à jour vers la dernière plateforme anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="3cd51-351">Affected machines appear to the customer as having not updated to the latest antimalware platform.</span></span>  
<br/>
> [!IMPORTANT]
> <span data-ttu-id="3cd51-352">Cette mise à jour est :</span><span class="sxs-lookup"><span data-stu-id="3cd51-352">This update is:</span></span>
> - <span data-ttu-id="3cd51-353">nécessaire aux appareils RS1 exécutant une version inférieure de la plateforme pour prendre en charge SHA2 ;</span><span class="sxs-lookup"><span data-stu-id="3cd51-353">needed by RS1 devices running lower version of the platform to support SHA2;</span></span>
> - <span data-ttu-id="3cd51-354">a un indicateur de redémarrage pour les systèmes qui ont des problèmes en suspension ;</span><span class="sxs-lookup"><span data-stu-id="3cd51-354">has a reboot flag for systems that have hanging issues;</span></span>
> - <span data-ttu-id="3cd51-355">est re-publiée en avril 2020 et ne sera pas recalée par les mises à jour plus nouvelles pour conserver la disponibilité future ;</span><span class="sxs-lookup"><span data-stu-id="3cd51-355">is re-released in April 2020 and will not be superseded by newer updates to keep future availability;</span></span>  
> - <span data-ttu-id="3cd51-356">est classée en tant que mise à jour en raison de l’exigence de redémarrage ; et</span><span class="sxs-lookup"><span data-stu-id="3cd51-356">is categorized as an update due to the reboot requirement; and</span></span>
> - <span data-ttu-id="3cd51-357">est uniquement proposée avec [Windows Update](https://support.microsoft.com/help/4027667/windows-10-update).</span><span class="sxs-lookup"><span data-stu-id="3cd51-357">is only be offered with [Windows Update](https://support.microsoft.com/help/4027667/windows-10-update).</span></span>
<br/>
</details>

<details>
<summary> <span data-ttu-id="3cd51-358">Novembre-2019 (plateforme : 4.18.1911.3 | Moteur : 1.1.16600.7)</span><span class="sxs-lookup"><span data-stu-id="3cd51-358">November-2019 (Platform: 4.18.1911.3 | Engine: 1.1.16600.7)</span></span></summary>

<span data-ttu-id="3cd51-359">Version de mise à jour des informations de sécurité **: 1.307.13.0**</span><span class="sxs-lookup"><span data-stu-id="3cd51-359">Security intelligence update version: **1.307.13.0**</span></span>  
<span data-ttu-id="3cd51-360">Publication : **7 décembre 2019**</span><span class="sxs-lookup"><span data-stu-id="3cd51-360">Released: **December 7, 2019**</span></span>  
<span data-ttu-id="3cd51-361">Plateforme : **4.18.1911.3**</span><span class="sxs-lookup"><span data-stu-id="3cd51-361">Platform: **4.18.1911.3**</span></span>  
<span data-ttu-id="3cd51-362">Moteur : **1.1.17000.7**</span><span class="sxs-lookup"><span data-stu-id="3cd51-362">Engine: **1.1.17000.7**</span></span>  
<span data-ttu-id="3cd51-363">Phase de support : **aucune prise en charge**</span><span class="sxs-lookup"><span data-stu-id="3cd51-363">Support phase: **No support**</span></span>  
     
### <a name="whats-new"></a><span data-ttu-id="3cd51-364">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="3cd51-364">What's new</span></span>

- <span data-ttu-id="3cd51-365">Niveau de suivi MpCmdRun fixe</span><span class="sxs-lookup"><span data-stu-id="3cd51-365">Fixed MpCmdRun tracing level</span></span>
- <span data-ttu-id="3cd51-366">Informations de version de WDFilter fixes</span><span class="sxs-lookup"><span data-stu-id="3cd51-366">Fixed WDFilter version info</span></span>
- <span data-ttu-id="3cd51-367">Améliorer les notifications (PUA)</span><span class="sxs-lookup"><span data-stu-id="3cd51-367">Improve notifications (PUA)</span></span>
- <span data-ttu-id="3cd51-368">ajouter des journaux MRT pour prendre en charge les fichiers</span><span class="sxs-lookup"><span data-stu-id="3cd51-368">add MRT logs to support files</span></span>
   
### <a name="known-issues"></a><span data-ttu-id="3cd51-369">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="3cd51-369">Known Issues</span></span>
<span data-ttu-id="3cd51-370">Lorsque cette mise à jour est installée, l’appareil a besoin du package de saut 4.18.2001.10 pour pouvoir se mettre à jour vers la dernière version de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="3cd51-370">When this update is installed, the device needs the jump package 4.18.2001.10 to be able to update to the latest platform version.</span></span>
<br/>
</details>


## <a name="microsoft-defender-antivirus-platform-support"></a><span data-ttu-id="3cd51-371">Antivirus Microsoft Defender prise en charge de la plateforme d’Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="3cd51-371">Microsoft Defender Antivirus platform support</span></span>
<span data-ttu-id="3cd51-372">Les mises à jour de la plateforme et du moteur sont fournies à une cadence mensuelle.</span><span class="sxs-lookup"><span data-stu-id="3cd51-372">Platform and engine updates are provided on a monthly cadence.</span></span> <span data-ttu-id="3cd51-373">Pour être entièrement pris en charge, tenez à jour les dernières mises à jour de plateforme.</span><span class="sxs-lookup"><span data-stu-id="3cd51-373">To be fully supported, keep current with the latest platform updates.</span></span> <span data-ttu-id="3cd51-374">Notre structure de support est dynamique et évolue en deux phases en fonction de la disponibilité de la dernière version de plateforme :</span><span class="sxs-lookup"><span data-stu-id="3cd51-374">Our support structure is dynamic, evolving into two phases depending on the availability of the latest platform version:</span></span>

- <span data-ttu-id="3cd51-375">Phase de maintenance des mises à jour **critiques** et de sécurité : lors de l’exécution de la dernière version de la plateforme, vous serez éligible à la réception des mises à jour de sécurité et critiques sur la plateforme anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="3cd51-375">**Security and Critical Updates servicing phase** - When running the latest platform version, you will be eligible to receive both Security and Critical updates to the anti-malware platform.</span></span>
 
- <span data-ttu-id="3cd51-376">**Phase de support technique (uniquement)** : après la publication d’une nouvelle version de plateforme, la prise en charge des versions antérieures (N-2) sera réduit au support technique uniquement.</span><span class="sxs-lookup"><span data-stu-id="3cd51-376">**Technical Support (Only) phase** - After a new platform version is released, support for older versions (N-2) will reduce to technical support only.</span></span> <span data-ttu-id="3cd51-377">Les versions de plateforme antérieures à N-2 ne seront plus pris en charge.\*</span><span class="sxs-lookup"><span data-stu-id="3cd51-377">Platform versions older than N-2 will no longer be supported.\*</span></span>

<span data-ttu-id="3cd51-378">\*Le support technique continuera d’être fourni pour les mises à niveau de la version Windows 10 (voir la version de plateforme incluse avec [les](#platform-version-included-with-windows-10-releases)versions Windows 10 ) vers la dernière version de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="3cd51-378">\* Technical support will continue to be provided for upgrades from the Windows 10 release version (see [Platform version included with Windows 10 releases](#platform-version-included-with-windows-10-releases)) to the latest platform version.</span></span>

<span data-ttu-id="3cd51-379">Pendant la phase de support technique (uniquement), les incidents de support commercialement raisonnables sont fournis par le biais du support technique du service clientèle Microsoft & et des offres de support géré de Microsoft (telles que le support Premier).</span><span class="sxs-lookup"><span data-stu-id="3cd51-379">During the technical support (only) phase, commercially reasonable support incidents will be provided through Microsoft Customer Service & Support and Microsoft’s managed support offerings (such as Premier Support).</span></span> <span data-ttu-id="3cd51-380">Si un incident de support nécessite une escalade vers le développement pour obtenir des conseils supplémentaires, nécessite une mise à jour non de sécurité ou nécessite une mise à jour de sécurité, les clients sont invités à mettre à niveau vers la dernière version de plateforme ou une mise à jour intermédiaire (\*).</span><span class="sxs-lookup"><span data-stu-id="3cd51-380">If a support incident requires escalation to development for further guidance, requires a non-security update, or requires a security update, customers will be asked to upgrade to the latest platform version or an intermediate update (\*).</span></span>

### <a name="platform-version-included-with-windows-10-releases"></a><span data-ttu-id="3cd51-381">Version de plateforme incluse dans Windows 10 versions</span><span class="sxs-lookup"><span data-stu-id="3cd51-381">Platform version included with Windows 10 releases</span></span>
<span data-ttu-id="3cd51-382">Le tableau ci-dessous fournit les versions Antivirus Microsoft Defender de plateforme et de moteur qui sont livrées avec les versions les Windows 10 les plus récentes :</span><span class="sxs-lookup"><span data-stu-id="3cd51-382">The below table provides the Microsoft Defender Antivirus platform and engine versions that are shipped with the latest Windows 10 releases:</span></span>    

|<span data-ttu-id="3cd51-383">Windows 10 version</span><span class="sxs-lookup"><span data-stu-id="3cd51-383">Windows 10 release</span></span>  |<span data-ttu-id="3cd51-384">Version de la plateforme</span><span class="sxs-lookup"><span data-stu-id="3cd51-384">Platform version</span></span>  |<span data-ttu-id="3cd51-385">Version du moteur</span><span class="sxs-lookup"><span data-stu-id="3cd51-385">Engine version</span></span> |<span data-ttu-id="3cd51-386">Phase de prise en charge</span><span class="sxs-lookup"><span data-stu-id="3cd51-386">Support phase</span></span> |
|:---|:---|:---|:---|
|<span data-ttu-id="3cd51-387">2004 (20H1/20H2)</span><span class="sxs-lookup"><span data-stu-id="3cd51-387">2004  (20H1/20H2)</span></span> |<span data-ttu-id="3cd51-388">4.18.1909.6</span><span class="sxs-lookup"><span data-stu-id="3cd51-388">4.18.1909.6</span></span> |<span data-ttu-id="3cd51-389">1.1.17000.2</span><span class="sxs-lookup"><span data-stu-id="3cd51-389">1.1.17000.2</span></span> | <span data-ttu-id="3cd51-390">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="3cd51-390">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="3cd51-391">1909 (19H2)</span><span class="sxs-lookup"><span data-stu-id="3cd51-391">1909  (19H2)</span></span> |<span data-ttu-id="3cd51-392">4.18.1902.5</span><span class="sxs-lookup"><span data-stu-id="3cd51-392">4.18.1902.5</span></span> |<span data-ttu-id="3cd51-393">1.1.16700.3</span><span class="sxs-lookup"><span data-stu-id="3cd51-393">1.1.16700.3</span></span> | <span data-ttu-id="3cd51-394">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="3cd51-394">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="3cd51-395">1903 (19H1)</span><span class="sxs-lookup"><span data-stu-id="3cd51-395">1903  (19H1)</span></span> |<span data-ttu-id="3cd51-396">4.18.1902.5</span><span class="sxs-lookup"><span data-stu-id="3cd51-396">4.18.1902.5</span></span> |<span data-ttu-id="3cd51-397">1.1.15600.4</span><span class="sxs-lookup"><span data-stu-id="3cd51-397">1.1.15600.4</span></span> | <span data-ttu-id="3cd51-398">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="3cd51-398">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="3cd51-399">1809 (RS5)</span><span class="sxs-lookup"><span data-stu-id="3cd51-399">1809  (RS5)</span></span> |<span data-ttu-id="3cd51-400">4.18.1807.18075</span><span class="sxs-lookup"><span data-stu-id="3cd51-400">4.18.1807.18075</span></span> |<span data-ttu-id="3cd51-401">1.1.15000.2</span><span class="sxs-lookup"><span data-stu-id="3cd51-401">1.1.15000.2</span></span> | <span data-ttu-id="3cd51-402">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="3cd51-402">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="3cd51-403">1803 (RS4)</span><span class="sxs-lookup"><span data-stu-id="3cd51-403">1803  (RS4)</span></span> |<span data-ttu-id="3cd51-404">4.13.17134.1</span><span class="sxs-lookup"><span data-stu-id="3cd51-404">4.13.17134.1</span></span> |<span data-ttu-id="3cd51-405">1.1.14600.4</span><span class="sxs-lookup"><span data-stu-id="3cd51-405">1.1.14600.4</span></span> | <span data-ttu-id="3cd51-406">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="3cd51-406">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="3cd51-407">1709 (RS3)</span><span class="sxs-lookup"><span data-stu-id="3cd51-407">1709  (RS3)</span></span> |<span data-ttu-id="3cd51-408">4.12.16299.15</span><span class="sxs-lookup"><span data-stu-id="3cd51-408">4.12.16299.15</span></span> |<span data-ttu-id="3cd51-409">1.1.14104.0</span><span class="sxs-lookup"><span data-stu-id="3cd51-409">1.1.14104.0</span></span> | <span data-ttu-id="3cd51-410">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="3cd51-410">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="3cd51-411">1703 (RS2)</span><span class="sxs-lookup"><span data-stu-id="3cd51-411">1703  (RS2)</span></span> |<span data-ttu-id="3cd51-412">4.11.15603.2</span><span class="sxs-lookup"><span data-stu-id="3cd51-412">4.11.15603.2</span></span> |<span data-ttu-id="3cd51-413">1.1.13504.0</span><span class="sxs-lookup"><span data-stu-id="3cd51-413">1.1.13504.0</span></span> | <span data-ttu-id="3cd51-414">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="3cd51-414">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="3cd51-415">1607 (RS1)</span><span class="sxs-lookup"><span data-stu-id="3cd51-415">1607 (RS1)</span></span> |<span data-ttu-id="3cd51-416">4.10.14393.3683</span><span class="sxs-lookup"><span data-stu-id="3cd51-416">4.10.14393.3683</span></span> |<span data-ttu-id="3cd51-417">1.1.12805.0</span><span class="sxs-lookup"><span data-stu-id="3cd51-417">1.1.12805.0</span></span> | <span data-ttu-id="3cd51-418">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="3cd51-418">Technical upgrade support (only)</span></span> |  

<span data-ttu-id="3cd51-419">Pour Windows 10 de publication, consultez la [Windows de faits sur](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet)le cycle de vie.</span><span class="sxs-lookup"><span data-stu-id="3cd51-419">For Windows 10 release information, see the [Windows lifecycle fact sheet](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet).</span></span>

## <a name="updates-for-deployment-image-servicing-and-management-dism"></a><span data-ttu-id="3cd51-420">Mises à jour pour la gestion et la maintenance des images de déploiement (DISM)</span><span class="sxs-lookup"><span data-stu-id="3cd51-420">Updates for Deployment Image Servicing and Management (DISM)</span></span>

<span data-ttu-id="3cd51-421">Nous vous recommandons de mettre à jour vos images d’installation Windows 10 (Enterprise, Pro et Éditions Famille), Windows Server 2019 et Windows Server 2016 OS avec les dernières mises à jour antivirus et anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="3cd51-421">We recommend updating your Windows 10 (Enterprise, Pro, and Home editions), Windows Server 2019, and Windows Server 2016 OS installation images with the latest antivirus and antimalware updates.</span></span> <span data-ttu-id="3cd51-422">La mise à jour de vos images d’installation du système d’exploitation permet d’éviter un écart de protection.</span><span class="sxs-lookup"><span data-stu-id="3cd51-422">Keeping your OS installation images up to date helps avoid a gap in protection.</span></span> 

<span data-ttu-id="3cd51-423">Pour plus d’informations, voir mise à [jour de Microsoft Defender pour Windows images d’installation du système d’exploitation.](https://support.microsoft.com/help/4568292/defender-update-for-windows-operating-system-installation-images)</span><span class="sxs-lookup"><span data-stu-id="3cd51-423">For more information, see [Microsoft Defender update for Windows operating system installation images](https://support.microsoft.com/help/4568292/defender-update-for-windows-operating-system-installation-images).</span></span>

<details>
<summary><span data-ttu-id="3cd51-424">1.1.2106.01</span><span class="sxs-lookup"><span data-stu-id="3cd51-424">1.1.2106.01</span></span></summary>

<span data-ttu-id="3cd51-425">&ensp;Version du package **: 1.1.2106.01**  </span><span class="sxs-lookup"><span data-stu-id="3cd51-425">&ensp;Package version: **1.1.2106.01**  </span></span>  
<span data-ttu-id="3cd51-426">&ensp;Version de la plateforme **: 4.18.2104.14** </span><span class="sxs-lookup"><span data-stu-id="3cd51-426">&ensp;Platform version: **4.18.2104.14** </span></span>  
<span data-ttu-id="3cd51-427">&ensp;Version du moteur **: 1.1.18100.6**</span><span class="sxs-lookup"><span data-stu-id="3cd51-427">&ensp;Engine version: **1.1.18100.6**</span></span>  
<span data-ttu-id="3cd51-428">&ensp;Version de signature **: 1.339.1923.0**</span><span class="sxs-lookup"><span data-stu-id="3cd51-428">&ensp;Signature version: **1.339.1923.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="3cd51-429">Correctifs</span><span class="sxs-lookup"><span data-stu-id="3cd51-429">Fixes</span></span>
- <span data-ttu-id="3cd51-430">Aucun</span><span class="sxs-lookup"><span data-stu-id="3cd51-430">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="3cd51-431">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="3cd51-431">Additional information</span></span>
- <span data-ttu-id="3cd51-432">Aucun</span><span class="sxs-lookup"><span data-stu-id="3cd51-432">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="3cd51-433">1.1.2105.01</span><span class="sxs-lookup"><span data-stu-id="3cd51-433">1.1.2105.01</span></span></summary>

<span data-ttu-id="3cd51-434">&ensp;Version du package **: 1.1.2105.01**  </span><span class="sxs-lookup"><span data-stu-id="3cd51-434">&ensp;Package version: **1.1.2105.01**  </span></span>  
<span data-ttu-id="3cd51-435">&ensp;Version de la plateforme **: 4.18.2103.7** </span><span class="sxs-lookup"><span data-stu-id="3cd51-435">&ensp;Platform version: **4.18.2103.7** </span></span>  
<span data-ttu-id="3cd51-436">&ensp;Version du moteur **: 1.1.18100.6**</span><span class="sxs-lookup"><span data-stu-id="3cd51-436">&ensp;Engine version: **1.1.18100.6**</span></span>  
<span data-ttu-id="3cd51-437">&ensp;Version de signature **: 1.339.42.0**</span><span class="sxs-lookup"><span data-stu-id="3cd51-437">&ensp;Signature version: **1.339.42.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="3cd51-438">Correctifs</span><span class="sxs-lookup"><span data-stu-id="3cd51-438">Fixes</span></span>
- <span data-ttu-id="3cd51-439">Aucun</span><span class="sxs-lookup"><span data-stu-id="3cd51-439">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="3cd51-440">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="3cd51-440">Additional information</span></span>
- <span data-ttu-id="3cd51-441">Aucun</span><span class="sxs-lookup"><span data-stu-id="3cd51-441">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="3cd51-442">1.1.2104.01</span><span class="sxs-lookup"><span data-stu-id="3cd51-442">1.1.2104.01</span></span></summary>

<span data-ttu-id="3cd51-443">&ensp;Version du package **: 1.1.2104.01**  </span><span class="sxs-lookup"><span data-stu-id="3cd51-443">&ensp;Package version: **1.1.2104.01**  </span></span>  
<span data-ttu-id="3cd51-444">&ensp;Version de la plateforme **: 4.18.2102.4** </span><span class="sxs-lookup"><span data-stu-id="3cd51-444">&ensp;Platform version: **4.18.2102.4** </span></span>  
<span data-ttu-id="3cd51-445">&ensp;Version du moteur **: 1.1.18000.5**</span><span class="sxs-lookup"><span data-stu-id="3cd51-445">&ensp;Engine version: **1.1.18000.5**</span></span>  
<span data-ttu-id="3cd51-446">&ensp;Version de signature **: 1.335.232.0**</span><span class="sxs-lookup"><span data-stu-id="3cd51-446">&ensp;Signature version: **1.335.232.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="3cd51-447">Correctifs</span><span class="sxs-lookup"><span data-stu-id="3cd51-447">Fixes</span></span>
- <span data-ttu-id="3cd51-448">Aucun</span><span class="sxs-lookup"><span data-stu-id="3cd51-448">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="3cd51-449">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="3cd51-449">Additional information</span></span>
- <span data-ttu-id="3cd51-450">Aucun</span><span class="sxs-lookup"><span data-stu-id="3cd51-450">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="3cd51-451">1.1.2103.01</span><span class="sxs-lookup"><span data-stu-id="3cd51-451">1.1.2103.01</span></span></summary>

<span data-ttu-id="3cd51-452">&ensp;Version du package **: 1.1.2103.01**  </span><span class="sxs-lookup"><span data-stu-id="3cd51-452">&ensp;Package version: **1.1.2103.01**  </span></span>  
<span data-ttu-id="3cd51-453">&ensp;Version de plateforme **: 4.18.2101.9** </span><span class="sxs-lookup"><span data-stu-id="3cd51-453">&ensp;Platform version: **4.18.2101.9** </span></span>  
<span data-ttu-id="3cd51-454">&ensp;Version du moteur **: 1.1.17800.5**</span><span class="sxs-lookup"><span data-stu-id="3cd51-454">&ensp;Engine version: **1.1.17800.5**</span></span>  
<span data-ttu-id="3cd51-455">&ensp;Version de signature **: 1.331.2302.0**</span><span class="sxs-lookup"><span data-stu-id="3cd51-455">&ensp;Signature version: **1.331.2302.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="3cd51-456">Correctifs</span><span class="sxs-lookup"><span data-stu-id="3cd51-456">Fixes</span></span>
- <span data-ttu-id="3cd51-457">Aucun</span><span class="sxs-lookup"><span data-stu-id="3cd51-457">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="3cd51-458">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="3cd51-458">Additional information</span></span>
- <span data-ttu-id="3cd51-459">Aucun</span><span class="sxs-lookup"><span data-stu-id="3cd51-459">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="3cd51-460">1.1.2102.03</span><span class="sxs-lookup"><span data-stu-id="3cd51-460">1.1.2102.03</span></span></summary>

<span data-ttu-id="3cd51-461">&ensp;Version du package **: 1.1.2102.03**  </span><span class="sxs-lookup"><span data-stu-id="3cd51-461">&ensp;Package version: **1.1.2102.03**  </span></span>  
<span data-ttu-id="3cd51-462">&ensp;Version de la plateforme **: 4.18.2011.6** </span><span class="sxs-lookup"><span data-stu-id="3cd51-462">&ensp;Platform version: **4.18.2011.6** </span></span>  
<span data-ttu-id="3cd51-463">&ensp;Version du moteur **: 1.1.17800.5**</span><span class="sxs-lookup"><span data-stu-id="3cd51-463">&ensp;Engine version: **1.1.17800.5**</span></span>  
<span data-ttu-id="3cd51-464">&ensp;Version de signature **: 1.331.174.0**</span><span class="sxs-lookup"><span data-stu-id="3cd51-464">&ensp;Signature version: **1.331.174.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="3cd51-465">Correctifs</span><span class="sxs-lookup"><span data-stu-id="3cd51-465">Fixes</span></span>
- <span data-ttu-id="3cd51-466">Aucun</span><span class="sxs-lookup"><span data-stu-id="3cd51-466">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="3cd51-467">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="3cd51-467">Additional information</span></span>
- <span data-ttu-id="3cd51-468">Aucun</span><span class="sxs-lookup"><span data-stu-id="3cd51-468">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="3cd51-469">1.1.2101.02</span><span class="sxs-lookup"><span data-stu-id="3cd51-469">1.1.2101.02</span></span></summary>

<span data-ttu-id="3cd51-470">&ensp;Version du package **: 1.1.2101.02**  </span><span class="sxs-lookup"><span data-stu-id="3cd51-470">&ensp;Package version: **1.1.2101.02**  </span></span>  
<span data-ttu-id="3cd51-471">&ensp;Version de la plateforme **: 4.18.2011.6** </span><span class="sxs-lookup"><span data-stu-id="3cd51-471">&ensp;Platform version: **4.18.2011.6** </span></span>  
<span data-ttu-id="3cd51-472">&ensp;Version du moteur **: 1.1.17700.4**</span><span class="sxs-lookup"><span data-stu-id="3cd51-472">&ensp;Engine version: **1.1.17700.4**</span></span>  
<span data-ttu-id="3cd51-473">&ensp;Version de signature **: 1.329.1796.0**</span><span class="sxs-lookup"><span data-stu-id="3cd51-473">&ensp;Signature version: **1.329.1796.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="3cd51-474">Correctifs</span><span class="sxs-lookup"><span data-stu-id="3cd51-474">Fixes</span></span>
- <span data-ttu-id="3cd51-475">Aucun</span><span class="sxs-lookup"><span data-stu-id="3cd51-475">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="3cd51-476">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="3cd51-476">Additional information</span></span>
- <span data-ttu-id="3cd51-477">Aucun</span><span class="sxs-lookup"><span data-stu-id="3cd51-477">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="3cd51-478">1.1.2012.01</span><span class="sxs-lookup"><span data-stu-id="3cd51-478">1.1.2012.01</span></span></summary>

<span data-ttu-id="3cd51-479">&ensp;Version du package **: 1.1.2012.01**  </span><span class="sxs-lookup"><span data-stu-id="3cd51-479">&ensp;Package version: **1.1.2012.01**  </span></span>  
<span data-ttu-id="3cd51-480">&ensp;Version de la plateforme **: 4.18.2010.7** </span><span class="sxs-lookup"><span data-stu-id="3cd51-480">&ensp;Platform version: **4.18.2010.7** </span></span>  
<span data-ttu-id="3cd51-481">&ensp;Version du moteur **: 1.1.17600.5**</span><span class="sxs-lookup"><span data-stu-id="3cd51-481">&ensp;Engine version: **1.1.17600.5**</span></span>  
<span data-ttu-id="3cd51-482">&ensp;Version de signature **: 1.327.1991.0**</span><span class="sxs-lookup"><span data-stu-id="3cd51-482">&ensp;Signature version: **1.327.1991.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="3cd51-483">Correctifs</span><span class="sxs-lookup"><span data-stu-id="3cd51-483">Fixes</span></span>
- <span data-ttu-id="3cd51-484">Aucun</span><span class="sxs-lookup"><span data-stu-id="3cd51-484">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="3cd51-485">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="3cd51-485">Additional information</span></span>
- <span data-ttu-id="3cd51-486">Aucun</span><span class="sxs-lookup"><span data-stu-id="3cd51-486">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="3cd51-487">1.1.2011.02</span><span class="sxs-lookup"><span data-stu-id="3cd51-487">1.1.2011.02</span></span></summary>

<span data-ttu-id="3cd51-488">&ensp;Version du package **: 1.1.2011.02**  </span><span class="sxs-lookup"><span data-stu-id="3cd51-488">&ensp;Package version: **1.1.2011.02**  </span></span>  
<span data-ttu-id="3cd51-489">&ensp;Version de la plateforme **: 4.18.2010.7** </span><span class="sxs-lookup"><span data-stu-id="3cd51-489">&ensp;Platform version: **4.18.2010.7** </span></span>  
<span data-ttu-id="3cd51-490">&ensp;Version du moteur **: 1.1.17600.5**</span><span class="sxs-lookup"><span data-stu-id="3cd51-490">&ensp;Engine version: **1.1.17600.5**</span></span>  
<span data-ttu-id="3cd51-491">&ensp;Version de signature **: 1.327.658.0**</span><span class="sxs-lookup"><span data-stu-id="3cd51-491">&ensp;Signature version: **1.327.658.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="3cd51-492">Correctifs</span><span class="sxs-lookup"><span data-stu-id="3cd51-492">Fixes</span></span>
- <span data-ttu-id="3cd51-493">Aucun</span><span class="sxs-lookup"><span data-stu-id="3cd51-493">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="3cd51-494">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="3cd51-494">Additional information</span></span>
- <span data-ttu-id="3cd51-495">Signatures Antivirus Microsoft Defender actualisées</span><span class="sxs-lookup"><span data-stu-id="3cd51-495">Refreshed Microsoft Defender Antivirus signatures</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="3cd51-496">1.1.2011.01</span><span class="sxs-lookup"><span data-stu-id="3cd51-496">1.1.2011.01</span></span></summary>

<span data-ttu-id="3cd51-497">&ensp;Version du package **: 1.1.2011.01**  </span><span class="sxs-lookup"><span data-stu-id="3cd51-497">&ensp;Package version: **1.1.2011.01**  </span></span>  
<span data-ttu-id="3cd51-498">&ensp;Version de la plateforme **: 4.18.2009.7**</span><span class="sxs-lookup"><span data-stu-id="3cd51-498">&ensp;Platform version: **4.18.2009.7**</span></span>  
<span data-ttu-id="3cd51-499">&ensp;Version du moteur **: 1.1.17600.5**</span><span class="sxs-lookup"><span data-stu-id="3cd51-499">&ensp;Engine version: **1.1.17600.5**</span></span>  
<span data-ttu-id="3cd51-500">&ensp;Version de signature **: 1.327.344.0**</span><span class="sxs-lookup"><span data-stu-id="3cd51-500">&ensp;Signature version: **1.327.344.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="3cd51-501">Correctifs</span><span class="sxs-lookup"><span data-stu-id="3cd51-501">Fixes</span></span>
- <span data-ttu-id="3cd51-502">Aucun</span><span class="sxs-lookup"><span data-stu-id="3cd51-502">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="3cd51-503">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="3cd51-503">Additional information</span></span>
- <span data-ttu-id="3cd51-504">Aucun</span><span class="sxs-lookup"><span data-stu-id="3cd51-504">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="3cd51-505">1.1.2009.10</span><span class="sxs-lookup"><span data-stu-id="3cd51-505">1.1.2009.10</span></span></summary>

<span data-ttu-id="3cd51-506">&ensp;Version du package **: 1.1.2011.01**  </span><span class="sxs-lookup"><span data-stu-id="3cd51-506">&ensp;Package version: **1.1.2011.01**  </span></span>  
<span data-ttu-id="3cd51-507">&ensp;Version de la plateforme **: 4.18.2008.9** </span><span class="sxs-lookup"><span data-stu-id="3cd51-507">&ensp;Platform version: **4.18.2008.9** </span></span>  
<span data-ttu-id="3cd51-508">&ensp;Version du moteur **: 1.1.17400.5**</span><span class="sxs-lookup"><span data-stu-id="3cd51-508">&ensp;Engine version: **1.1.17400.5**</span></span>  
<span data-ttu-id="3cd51-509">&ensp;Version de signature **: 1.327.2216.0**</span><span class="sxs-lookup"><span data-stu-id="3cd51-509">&ensp;Signature version: **1.327.2216.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="3cd51-510">Correctifs</span><span class="sxs-lookup"><span data-stu-id="3cd51-510">Fixes</span></span>
- <span data-ttu-id="3cd51-511">Aucun</span><span class="sxs-lookup"><span data-stu-id="3cd51-511">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="3cd51-512">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="3cd51-512">Additional information</span></span>
- <span data-ttu-id="3cd51-513">Ajout de la prise en charge Windows 10 images d’installation du système d’exploitation RS1 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="3cd51-513">Added support for Windows 10 RS1 or later OS install images.</span></span>  
<br/>
</details>

## <a name="additional-resources"></a><span data-ttu-id="3cd51-514">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="3cd51-514">Additional resources</span></span>

| <span data-ttu-id="3cd51-515">Article</span><span class="sxs-lookup"><span data-stu-id="3cd51-515">Article</span></span> | <span data-ttu-id="3cd51-516">Description</span><span class="sxs-lookup"><span data-stu-id="3cd51-516">Description</span></span>  |
|:---|:---|
|[<span data-ttu-id="3cd51-517">Mise à jour de Microsoft Defender Windows images d’installation du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="3cd51-517">Microsoft Defender update for Windows operating system installation images</span></span>](https://support.microsoft.com/help/4568292/defender-update-for-windows-operating-system-installation-images)  | <span data-ttu-id="3cd51-518">Passer en revue les packages de mise à jour anti-programme malveillant pour vos images d’installation du système d’exploitation (fichiers WIM et VHD).</span><span class="sxs-lookup"><span data-stu-id="3cd51-518">Review antimalware update packages for your OS installation images (WIM and VHD files).</span></span> <span data-ttu-id="3cd51-519">Obtenez Antivirus Microsoft Defender mises à jour de Windows 10 (éditions Enterprise, Pro et Famille), Windows Server 2019 et Windows Server 2016 images d’installation.</span><span class="sxs-lookup"><span data-stu-id="3cd51-519">Get Microsoft Defender Antivirus updates for Windows 10 (Enterprise, Pro, and Home editions), Windows Server 2019, and Windows Server 2016 installation images.</span></span>  |
|[<span data-ttu-id="3cd51-520">Gérer le téléchargement et l’application des mises à jour de protection</span><span class="sxs-lookup"><span data-stu-id="3cd51-520">Manage how protection updates are downloaded and applied</span></span>](manage-protection-updates-microsoft-defender-antivirus.md) | <span data-ttu-id="3cd51-521">Les mises à jour de la protection peuvent être livrées via de nombreuses sources.</span><span class="sxs-lookup"><span data-stu-id="3cd51-521">Protection updates can be delivered through many sources.</span></span> |
|[<span data-ttu-id="3cd51-522">Gérer le moment où les mises à jour de protection doivent être téléchargées et appliquées</span><span class="sxs-lookup"><span data-stu-id="3cd51-522">Manage when protection updates should be downloaded and applied</span></span>](manage-protection-update-schedule-microsoft-defender-antivirus.md) | <span data-ttu-id="3cd51-523">Vous pouvez planifier le téléchargement des mises à jour de la protection.</span><span class="sxs-lookup"><span data-stu-id="3cd51-523">You can schedule when protection updates should be downloaded.</span></span> |
|[<span data-ttu-id="3cd51-524">Gérer les mises à jour des points de terminaison qui ne sont pas à jour</span><span class="sxs-lookup"><span data-stu-id="3cd51-524">Manage updates for endpoints that are out of date</span></span>](manage-outdated-endpoints-microsoft-defender-antivirus.md) | <span data-ttu-id="3cd51-525">Si un point de terminaison manque une mise à jour ou une analyse programmée, vous pouvez forcer une mise à jour ou une analyse la prochaine fois qu’un utilisateur se signe.</span><span class="sxs-lookup"><span data-stu-id="3cd51-525">If an endpoint misses an update or scheduled scan, you can force an update or scan the next time a user signs in.</span></span> |
|[<span data-ttu-id="3cd51-526">Gérer les mises à jour forcées en fonction des événements</span><span class="sxs-lookup"><span data-stu-id="3cd51-526">Manage event-based forced updates</span></span>](manage-event-based-updates-microsoft-defender-antivirus.md) | <span data-ttu-id="3cd51-527">Vous pouvez définir des mises à jour de protection à télécharger au démarrage ou après certains événements de protection livrés par le cloud.</span><span class="sxs-lookup"><span data-stu-id="3cd51-527">You can set protection updates to be downloaded at startup or after certain cloud-delivered protection events.</span></span> |
|[<span data-ttu-id="3cd51-528">Gérer les mises à jour pour les appareils mobiles et les machines virtuelles</span><span class="sxs-lookup"><span data-stu-id="3cd51-528">Manage updates for mobile devices and virtual machines (VMs)</span></span>](manage-updates-mobile-devices-vms-microsoft-defender-antivirus.md)| <span data-ttu-id="3cd51-529">Vous pouvez spécifier des paramètres, par exemple si des mises à jour doivent être mises à jour sur l’alimentation de la batterie, qui sont particulièrement utiles pour les appareils mobiles et les ordinateurs virtuels.</span><span class="sxs-lookup"><span data-stu-id="3cd51-529">You can specify settings, such as whether updates should occur on battery power, that are especially useful for mobile devices and virtual machines.</span></span> |
