---
title: Gérer les mises Antivirus Microsoft Defender jour et appliquer les lignes de base
description: Gérer la façon dont Antivirus Microsoft Defender reçoit les mises à jour de protection et de produit.
keywords: mises à jour, bases de référence de sécurité, protection, planification des mises à jour, forcer les mises à jour, mises à jour mobiles, wsus
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
ms.date: 06/08/2021
ms.openlocfilehash: ccbb57d781196e352e0fed456a1f7cb43eb17300
ms.sourcegitcommit: 50908a93554290ff1157b58d0a868a33e012513c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52822273"
---
# <a name="manage-microsoft-defender-antivirus-updates-and-apply-baselines"></a><span data-ttu-id="28abd-104">Gérer les mises Antivirus Microsoft Defender jour et appliquer les lignes de base</span><span class="sxs-lookup"><span data-stu-id="28abd-104">Manage Microsoft Defender Antivirus updates and apply baselines</span></span>

<span data-ttu-id="28abd-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="28abd-105">**Applies to:**</span></span>

- [<span data-ttu-id="28abd-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="28abd-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)
- <span data-ttu-id="28abd-107">Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="28abd-107">Microsoft Defender Antivirus</span></span>

<span data-ttu-id="28abd-108">Il existe deux types de mises à jour liées au Antivirus Microsoft Defender à jour :</span><span class="sxs-lookup"><span data-stu-id="28abd-108">There are two types of updates related to keeping Microsoft Defender Antivirus up to date:</span></span>

- <span data-ttu-id="28abd-109">Mises à jour de l’intelligence de la sécurité</span><span class="sxs-lookup"><span data-stu-id="28abd-109">Security intelligence updates</span></span>
- <span data-ttu-id="28abd-110">Mises à jour de produit</span><span class="sxs-lookup"><span data-stu-id="28abd-110">Product updates</span></span>

> [!IMPORTANT]
> <span data-ttu-id="28abd-111">Le Antivirus Microsoft Defender à jour est essentiel pour garantir que vos appareils disposent des dernières technologies et fonctionnalités nécessaires pour se protéger contre les nouveaux programmes malveillants et les nouvelles techniques d’attaque.</span><span class="sxs-lookup"><span data-stu-id="28abd-111">Keeping Microsoft Defender Antivirus up to date is critical to assure your devices have the latest technology and features needed to protect against new malware and attack techniques.</span></span>
> 
> <span data-ttu-id="28abd-112">Veillez à mettre à jour votre protection antivirus même si Antivirus Microsoft Defender est en cours d’exécution en [mode passif.](./microsoft-defender-antivirus-compatibility.md)</span><span class="sxs-lookup"><span data-stu-id="28abd-112">Make sure to update your antivirus protection even if Microsoft Defender Antivirus is running in [passive mode](./microsoft-defender-antivirus-compatibility.md).</span></span>
> 
> <span data-ttu-id="28abd-113">Pour voir le moteur, la plateforme et la date de signature les plus à jour, consultez les mises à jour de l’intelligence de sécurité pour Antivirus Microsoft Defender logiciel [anti-programme](https://www.microsoft.com/en-us/wdsi/defenderupdates)malveillant Microsoft.</span><span class="sxs-lookup"><span data-stu-id="28abd-113">To see the most current engine, platform, and signature date, visit the [Security intelligence updates for Microsoft Defender Antivirus and other Microsoft antimalware](https://www.microsoft.com/en-us/wdsi/defenderupdates).</span></span>

## <a name="security-intelligence-updates"></a><span data-ttu-id="28abd-114">Mises à jour de l’intelligence de la sécurité</span><span class="sxs-lookup"><span data-stu-id="28abd-114">Security intelligence updates</span></span>

<span data-ttu-id="28abd-115">Antivirus Microsoft Defender utilise la protection fournie par le [cloud](cloud-protection-microsoft-defender-antivirus.md) (également appelée Microsoft Advanced Protection Service ou MAPS) et télécharge régulièrement les mises à jour de l’intelligence de sécurité pour fournir une protection.</span><span class="sxs-lookup"><span data-stu-id="28abd-115">Microsoft Defender Antivirus uses [cloud-delivered protection](cloud-protection-microsoft-defender-antivirus.md) (also called the Microsoft Advanced Protection Service or MAPS) and periodically downloads security intelligence updates to provide protection.</span></span>

> [!NOTE]
> <span data-ttu-id="28abd-116">Les mises à jour sont publiées sous les numéros de la Ko ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="28abd-116">Updates are released under the below KB numbers:</span></span>  
> - <span data-ttu-id="28abd-117">Antivirus Microsoft Defender : KB2267602</span><span class="sxs-lookup"><span data-stu-id="28abd-117">Microsoft Defender Antivirus: KB2267602</span></span>  
> - <span data-ttu-id="28abd-118">System Center Endpoint Protection : KB2461484</span><span class="sxs-lookup"><span data-stu-id="28abd-118">System Center Endpoint Protection: KB2461484</span></span>

<span data-ttu-id="28abd-119">La protection cloud est toujours active et nécessite une connexion active à Internet pour fonctionner.</span><span class="sxs-lookup"><span data-stu-id="28abd-119">Cloud-delivered protection is always on and requires an active connection to the Internet to function.</span></span> <span data-ttu-id="28abd-120">Les mises à jour des informations de sécurité se produisent à une cadence programmée (configurable via une stratégie).</span><span class="sxs-lookup"><span data-stu-id="28abd-120">Security intelligence updates occur on a scheduled cadence (configurable via policy).</span></span> <span data-ttu-id="28abd-121">Pour plus d’informations, voir Utiliser la protection fournie par le [cloud microsoft dans Antivirus Microsoft Defender](cloud-protection-microsoft-defender-antivirus.md).</span><span class="sxs-lookup"><span data-stu-id="28abd-121">For more information, see [Use Microsoft cloud-provided protection in Microsoft Defender Antivirus](cloud-protection-microsoft-defender-antivirus.md).</span></span> 

<span data-ttu-id="28abd-122">Pour obtenir la liste des mises à jour récentes de l’intelligence de sécurité, voir Les mises à jour de l’intelligence de sécurité pour Antivirus Microsoft Defender logiciel [anti-programme](https://www.microsoft.com/en-us/wdsi/defenderupdates)malveillant Microsoft.</span><span class="sxs-lookup"><span data-stu-id="28abd-122">For a list of recent security intelligence updates, see [Security intelligence updates for Microsoft Defender Antivirus and other Microsoft antimalware](https://www.microsoft.com/en-us/wdsi/defenderupdates).</span></span>

<span data-ttu-id="28abd-123">Les mises à jour du moteur sont incluses dans les mises à jour de l’intelligence de sécurité et sont publiées à une cadence mensuelle.</span><span class="sxs-lookup"><span data-stu-id="28abd-123">Engine updates are included with security intelligence updates and are released on a monthly cadence.</span></span>

## <a name="product-updates"></a><span data-ttu-id="28abd-124">Mises à jour de produit</span><span class="sxs-lookup"><span data-stu-id="28abd-124">Product updates</span></span>

<span data-ttu-id="28abd-125">Antivirus Microsoft Defender nécessite des mises à jour [mensuelles (KB4052623)](https://support.microsoft.com/help/4052623/update-for-windows-defender-antimalware-platform) *(connues* sous le nom de mises à jour de plateforme) et recevra des mises à jour de fonctionnalités majeures avec Windows 10 de publication.</span><span class="sxs-lookup"><span data-stu-id="28abd-125">Microsoft Defender Antivirus requires [monthly updates (KB4052623)](https://support.microsoft.com/help/4052623/update-for-windows-defender-antimalware-platform) (known as *platform updates*), and will receive major feature updates alongside Windows 10 releases.</span></span>

<span data-ttu-id="28abd-126">Vous pouvez gérer la distribution des mises à jour via l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="28abd-126">You can manage the distribution of updates through one of the following methods:</span></span> 

- [<span data-ttu-id="28abd-127">Windows Server Update Service (WSUS)</span><span class="sxs-lookup"><span data-stu-id="28abd-127">Windows Server Update Service (WSUS)</span></span>](/mem/configmgr/protect/deploy-use/endpoint-definitions-wsus#to-synchronize-endpoint-protection-definition-updates-in-standalone-wsus)
- [<span data-ttu-id="28abd-128">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="28abd-128">Microsoft Endpoint Configuration Manager</span></span>](/configmgr/sum/understand/software-updates-introduction)
- <span data-ttu-id="28abd-129">La méthode habituelle que vous utilisez pour déployer Microsoft et Windows mises à jour aux points de terminaison de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="28abd-129">The usual method you use to deploy Microsoft and Windows updates to endpoints in your network.</span></span>

<span data-ttu-id="28abd-130">Pour plus d’informations, [voir Gérer les sources pour les mises à jour Antivirus Microsoft Defender protection des données.](/mem/configmgr/protect/deploy-use/endpoint-definitions-wsus#to-synchronize-endpoint-protection-definition-updates-in-standalone-wsus)</span><span class="sxs-lookup"><span data-stu-id="28abd-130">For more information, see [Manage the sources for Microsoft Defender Antivirus protection updates](/mem/configmgr/protect/deploy-use/endpoint-definitions-wsus#to-synchronize-endpoint-protection-definition-updates-in-standalone-wsus).</span></span>

> [!NOTE]
> <span data-ttu-id="28abd-131">Les mises à jour mensuelles sont publiées par phases, ce qui entraîne la mise à jour de plusieurs packages dans vos services de mise à jour [de serveur Window.](/windows-server/administration/windows-server-update-services/get-started/windows-server-update-services-wsus)</span><span class="sxs-lookup"><span data-stu-id="28abd-131">Monthly updates are released in phases, resulting in multiple packages visible in your [Window Server Update Services](/windows-server/administration/windows-server-update-services/get-started/windows-server-update-services-wsus).</span></span>

## <a name="monthly-platform-and-engine-versions"></a><span data-ttu-id="28abd-132">Versions mensuelles de la plateforme et du moteur</span><span class="sxs-lookup"><span data-stu-id="28abd-132">Monthly platform and engine versions</span></span>

<span data-ttu-id="28abd-133">Pour plus d’informations sur la mise à jour ou l’installation de la mise à jour de la plateforme, voir [Update for Windows Defender antimalware platform](https://support.microsoft.com/help/4052623/update-for-windows-defender-antimalware-platform).</span><span class="sxs-lookup"><span data-stu-id="28abd-133">For information how to update or install the platform update, see [Update for Windows Defender antimalware platform](https://support.microsoft.com/help/4052623/update-for-windows-defender-antimalware-platform).</span></span>

<span data-ttu-id="28abd-134">Toutes nos mises à jour contiennent</span><span class="sxs-lookup"><span data-stu-id="28abd-134">All our updates contain</span></span> 
- <span data-ttu-id="28abd-135">améliorations des performances ;</span><span class="sxs-lookup"><span data-stu-id="28abd-135">performance improvements;</span></span>
- <span data-ttu-id="28abd-136">améliorations de la serviceabilité ; et</span><span class="sxs-lookup"><span data-stu-id="28abd-136">serviceability improvements; and</span></span> 
- <span data-ttu-id="28abd-137">améliorations de l’intégration (Cloud, [Microsoft 365 Defender](/microsoft-365/security/defender/microsoft-365-defender)).</span><span class="sxs-lookup"><span data-stu-id="28abd-137">integration improvements (Cloud, [Microsoft 365 Defender](/microsoft-365/security/defender/microsoft-365-defender)).</span></span>
<br/>
<details>
<summary> <span data-ttu-id="28abd-138">Mai-2021 (plateforme : 4.18.2105.4 | Moteur : 1.1.18200.4)</span><span class="sxs-lookup"><span data-stu-id="28abd-138">May-2021 (Platform: 4.18.2105.4 | Engine: 1.1.18200.4)</span></span></summary>

<span data-ttu-id="28abd-139">&ensp;Version de mise à jour des informations de sécurité **: 1.341.8.0**</span><span class="sxs-lookup"><span data-stu-id="28abd-139">&ensp;Security intelligence update version: **1.341.8.0**</span></span>  
<span data-ttu-id="28abd-140">&ensp;Publication : **4 juin 2021**</span><span class="sxs-lookup"><span data-stu-id="28abd-140">&ensp;Released: **June 4, 2021**</span></span>  
<span data-ttu-id="28abd-141">&ensp;Plateforme : **4.18.2105.4**</span><span class="sxs-lookup"><span data-stu-id="28abd-141">&ensp;Platform: **4.18.2105.4**</span></span>  
<span data-ttu-id="28abd-142">&ensp;Moteur : **1.1.18200.4**</span><span class="sxs-lookup"><span data-stu-id="28abd-142">&ensp;Engine: **1.1.18200.4**</span></span>  
<span data-ttu-id="28abd-143">&ensp;Phase de prise en charge **: Mises à jour critiques et de sécurité**</span><span class="sxs-lookup"><span data-stu-id="28abd-143">&ensp;Support phase: **Security and Critical Updates**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="28abd-144">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="28abd-144">What's new</span></span>
- <span data-ttu-id="28abd-145">Améliorations apportées à la [surveillance du comportement](client-behavioral-blocking.md)</span><span class="sxs-lookup"><span data-stu-id="28abd-145">Improvements to [behavior monitoring](client-behavioral-blocking.md)</span></span> 
- <span data-ttu-id="28abd-146">Fonctionnalité de [filtrage des](network-protection.md) notifications de protection réseau fixe</span><span class="sxs-lookup"><span data-stu-id="28abd-146">Fixed [network protection](network-protection.md) notification filtering feature</span></span>

### <a name="known-issues"></a><span data-ttu-id="28abd-147">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="28abd-147">Known Issues</span></span>
<span data-ttu-id="28abd-148">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="28abd-148">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="28abd-149">Avril-2021 (plateforme : 4.18.2104.14 | Moteur : 1.1.18100.5)</span><span class="sxs-lookup"><span data-stu-id="28abd-149">April-2021 (Platform: 4.18.2104.14 | Engine: 1.1.18100.5)</span></span></summary>

<span data-ttu-id="28abd-150">&ensp;Version de mise à jour des informations de sécurité **: 1.337.2.0**</span><span class="sxs-lookup"><span data-stu-id="28abd-150">&ensp;Security intelligence update version: **1.337.2.0**</span></span>  
<span data-ttu-id="28abd-151">&ensp;Publication : **1er avril 2021**</span><span class="sxs-lookup"><span data-stu-id="28abd-151">&ensp;Released: **April 1, 2021**</span></span>  
<span data-ttu-id="28abd-152">&ensp;Plateforme : **4.18.2104.14**</span><span class="sxs-lookup"><span data-stu-id="28abd-152">&ensp;Platform: **4.18.2104.14**</span></span>  
<span data-ttu-id="28abd-153">&ensp;Moteur : **1.1.18100.5**</span><span class="sxs-lookup"><span data-stu-id="28abd-153">&ensp;Engine: **1.1.18100.5**</span></span>  
<span data-ttu-id="28abd-154">&ensp;Phase de prise en charge **: Mises à jour critiques et de sécurité**</span><span class="sxs-lookup"><span data-stu-id="28abd-154">&ensp;Support phase: **Security and Critical Updates**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="28abd-155">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="28abd-155">What's new</span></span>
- <span data-ttu-id="28abd-156">Logique d’analyse de comportement supplémentaire</span><span class="sxs-lookup"><span data-stu-id="28abd-156">Additional behavior monitoring logic</span></span>
- <span data-ttu-id="28abd-157">Détection améliorée du keylogger en mode noyau</span><span class="sxs-lookup"><span data-stu-id="28abd-157">Improved kernel mode keylogger detection</span></span>
- <span data-ttu-id="28abd-158">Ajout de nouveaux contrôles pour gérer le processus de déploiement progressif pour [les mises à jour De Microsoft Defender](updates.md)</span><span class="sxs-lookup"><span data-stu-id="28abd-158">Added new controls to manage the gradual rollout process for [Microsoft Defender updates](updates.md)</span></span>

### <a name="known-issues"></a><span data-ttu-id="28abd-159">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="28abd-159">Known Issues</span></span>
<span data-ttu-id="28abd-160">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="28abd-160">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="28abd-161">Mars-2021 (plateforme : 4.18.2103.7 | Moteur : 1.1.18000.5)</span><span class="sxs-lookup"><span data-stu-id="28abd-161">March-2021 (Platform: 4.18.2103.7 | Engine: 1.1.18000.5)</span></span></summary>

<span data-ttu-id="28abd-162">&ensp;Version de mise à jour des informations de sécurité **: 1.335.36.0**</span><span class="sxs-lookup"><span data-stu-id="28abd-162">&ensp;Security intelligence update version: **1.335.36.0**</span></span>  
<span data-ttu-id="28abd-163">&ensp;Publication : **1er avril 2021**</span><span class="sxs-lookup"><span data-stu-id="28abd-163">&ensp;Released: **April 1, 2021**</span></span>  
<span data-ttu-id="28abd-164">&ensp;Plateforme : **4.18.2103.7**</span><span class="sxs-lookup"><span data-stu-id="28abd-164">&ensp;Platform: **4.18.2103.7**</span></span>  
<span data-ttu-id="28abd-165">&ensp;Moteur : **1.1.18000.5**</span><span class="sxs-lookup"><span data-stu-id="28abd-165">&ensp;Engine: **1.1.18000.5**</span></span>  
<span data-ttu-id="28abd-166">&ensp;Phase de prise en charge **: Mises à jour critiques et de sécurité**</span><span class="sxs-lookup"><span data-stu-id="28abd-166">&ensp;Support phase: **Security and Critical Updates**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="28abd-167">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="28abd-167">What's new</span></span>

- <span data-ttu-id="28abd-168">Amélioration du moteur d’analyse du comportement</span><span class="sxs-lookup"><span data-stu-id="28abd-168">Improvement to the Behavior Monitoring engine</span></span> 
- <span data-ttu-id="28abd-169">Préventions d’attaques par force brute du réseau étendu</span><span class="sxs-lookup"><span data-stu-id="28abd-169">Expanded network brute-force-attack mitigations</span></span> 
- <span data-ttu-id="28abd-170">Génération d’événements de tentative de falsification en échec supplémentaires lorsque la [protection](prevent-changes-to-security-settings-with-tamper-protection.md) contre la falsification est activée</span><span class="sxs-lookup"><span data-stu-id="28abd-170">Additional failed tampering attempt event generation when [Tamper Protection](prevent-changes-to-security-settings-with-tamper-protection.md) is enabled</span></span>

### <a name="known-issues"></a><span data-ttu-id="28abd-171">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="28abd-171">Known Issues</span></span>
<span data-ttu-id="28abd-172">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="28abd-172">No known issues</span></span>  
<br/>
</details>

### <a name="previous-version-updates-technical-upgrade-support-only"></a><span data-ttu-id="28abd-173">Mises à jour de version précédente : prise en charge de la mise à niveau technique uniquement</span><span class="sxs-lookup"><span data-stu-id="28abd-173">Previous version updates: Technical upgrade support only</span></span>

<span data-ttu-id="28abd-174">Après la publication d’une nouvelle version de package, la prise en charge des deux versions précédentes est réduite au support technique uniquement.</span><span class="sxs-lookup"><span data-stu-id="28abd-174">After a new package version is released, support for the previous two versions is reduced to technical support only.</span></span> <span data-ttu-id="28abd-175">Les versions antérieures à celles répertoriées dans cette section sont fournies uniquement pour la prise en charge de la mise à niveau technique.</span><span class="sxs-lookup"><span data-stu-id="28abd-175">Versions older than that are listed in this section, and are provided for technical upgrade support only.</span></span> 
<br/><br/>
<details>
<summary> <span data-ttu-id="28abd-176">Février-2021 (plateforme : 4.18.2102.3 | Moteur : 1.1.17900.7)</span><span class="sxs-lookup"><span data-stu-id="28abd-176">February-2021 (Platform: 4.18.2102.3 | Engine: 1.1.17900.7)</span></span></summary>

<span data-ttu-id="28abd-177">&ensp;Version de mise à jour des informations de sécurité **: 1.333.7.0**</span><span class="sxs-lookup"><span data-stu-id="28abd-177">&ensp;Security intelligence update version: **1.333.7.0**</span></span>  
<span data-ttu-id="28abd-178">&ensp;Publication : **9 mars 2021**</span><span class="sxs-lookup"><span data-stu-id="28abd-178">&ensp;Released: **March 9, 2021**</span></span>  
<span data-ttu-id="28abd-179">&ensp;Plateforme : **4.18.2102.3**</span><span class="sxs-lookup"><span data-stu-id="28abd-179">&ensp;Platform: **4.18.2102.3**</span></span>  
<span data-ttu-id="28abd-180">&ensp;Moteur : **1.1.17900.7**</span><span class="sxs-lookup"><span data-stu-id="28abd-180">&ensp;Engine: **1.1.17900.7**</span></span>  
<span data-ttu-id="28abd-181">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="28abd-181">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="28abd-182">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="28abd-182">What's new</span></span>

- <span data-ttu-id="28abd-183">Amélioration de la récupération du service par le biais [de la protection contre la falsification](prevent-changes-to-security-settings-with-tamper-protection.md)</span><span class="sxs-lookup"><span data-stu-id="28abd-183">Improved service recovery through [tamper protection](prevent-changes-to-security-settings-with-tamper-protection.md)</span></span>
- <span data-ttu-id="28abd-184">Étendre l’étendue de la protection contre la falsification</span><span class="sxs-lookup"><span data-stu-id="28abd-184">Extend tamper protection scope</span></span>

### <a name="known-issues"></a><span data-ttu-id="28abd-185">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="28abd-185">Known Issues</span></span>
<span data-ttu-id="28abd-186">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="28abd-186">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="28abd-187">Janvier-2021 (plateforme : 4.18.2101.9 | Moteur : 1.1.17800.5)</span><span class="sxs-lookup"><span data-stu-id="28abd-187">January-2021 (Platform: 4.18.2101.9 | Engine: 1.1.17800.5)</span></span></summary>

<span data-ttu-id="28abd-188">&ensp;Version de mise à jour des informations de sécurité **: 1.327.1854.0**</span><span class="sxs-lookup"><span data-stu-id="28abd-188">&ensp;Security intelligence update version: **1.327.1854.0**</span></span>  
<span data-ttu-id="28abd-189">&ensp;Publication : **2 février 2021**</span><span class="sxs-lookup"><span data-stu-id="28abd-189">&ensp;Released: **February 2, 2021**</span></span>  
<span data-ttu-id="28abd-190">&ensp;Plateforme : **4.18.2101.9**</span><span class="sxs-lookup"><span data-stu-id="28abd-190">&ensp;Platform: **4.18.2101.9**</span></span>  
<span data-ttu-id="28abd-191">&ensp;Moteur : **1.1.17800.5**</span><span class="sxs-lookup"><span data-stu-id="28abd-191">&ensp;Engine: **1.1.17800.5**</span></span>  
<span data-ttu-id="28abd-192">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="28abd-192">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="28abd-193">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="28abd-193">What's new</span></span>

- <span data-ttu-id="28abd-194">Améliorations de la détection d’exploits shellcode</span><span class="sxs-lookup"><span data-stu-id="28abd-194">Shellcode exploit detection improvements</span></span>
- <span data-ttu-id="28abd-195">Visibilité accrue des tentatives de vol d’informations d’identification</span><span class="sxs-lookup"><span data-stu-id="28abd-195">Increased visibility for credential stealing attempts</span></span>
- <span data-ttu-id="28abd-196">Améliorations des fonctionnalités antitampering dans Antivirus Microsoft Defender services</span><span class="sxs-lookup"><span data-stu-id="28abd-196">Improvements in antitampering features in Microsoft Defender Antivirus services</span></span>
- <span data-ttu-id="28abd-197">Prise en charge améliorée de l ARM éulation x64</span><span class="sxs-lookup"><span data-stu-id="28abd-197">Improved support for ARM x64 emulation</span></span>
- <span data-ttu-id="28abd-198">Correctif : PEPT notification de blocage reste dans l’historique des menaces après la détection initiale de la protection en temps réel</span><span class="sxs-lookup"><span data-stu-id="28abd-198">Fix: EDR Block notification remains in threat history after real-time protection performed initial detection</span></span>

### <a name="known-issues"></a><span data-ttu-id="28abd-199">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="28abd-199">Known Issues</span></span>
<span data-ttu-id="28abd-200">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="28abd-200">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="28abd-201">Novembre-2020 (plateforme : 4.18.2011.6 | Moteur : 1.1.17700.4)</span><span class="sxs-lookup"><span data-stu-id="28abd-201">November-2020 (Platform: 4.18.2011.6 | Engine: 1.1.17700.4)</span></span></summary>

<span data-ttu-id="28abd-202">&ensp;Version de mise à jour des informations de sécurité **: 1.327.1854.0**</span><span class="sxs-lookup"><span data-stu-id="28abd-202">&ensp;Security intelligence update version: **1.327.1854.0**</span></span>  
<span data-ttu-id="28abd-203">&ensp;Publication : **03 décembre 2020**</span><span class="sxs-lookup"><span data-stu-id="28abd-203">&ensp;Released: **December 03, 2020**</span></span>  
<span data-ttu-id="28abd-204">&ensp;Plateforme : **4.18.2011.6**</span><span class="sxs-lookup"><span data-stu-id="28abd-204">&ensp;Platform: **4.18.2011.6**</span></span>  
<span data-ttu-id="28abd-205">&ensp;Moteur : **1.1.17700.4**</span><span class="sxs-lookup"><span data-stu-id="28abd-205">&ensp;Engine: **1.1.17700.4**</span></span>  
<span data-ttu-id="28abd-206">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="28abd-206">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="28abd-207">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="28abd-207">What's new</span></span>

- <span data-ttu-id="28abd-208">Amélioration de la [journalisation de la prise en](/windows/security/threat-protection/microsoft-defender-smartscreen/microsoft-defender-smartscreen-overview) charge de l’état SmartScreen</span><span class="sxs-lookup"><span data-stu-id="28abd-208">Improved [SmartScreen](/windows/security/threat-protection/microsoft-defender-smartscreen/microsoft-defender-smartscreen-overview) status support logging</span></span>

### <a name="known-issues"></a><span data-ttu-id="28abd-209">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="28abd-209">Known Issues</span></span>
<span data-ttu-id="28abd-210">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="28abd-210">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="28abd-211">Octobre-2020 (plateforme : 4.18.2010.7 | Moteur : 1.1.17600.5)</span><span class="sxs-lookup"><span data-stu-id="28abd-211">October-2020 (Platform: 4.18.2010.7 | Engine: 1.1.17600.5)</span></span></summary>

<span data-ttu-id="28abd-212">&ensp;Version de mise à jour des informations de sécurité **: 1.327.7.0**</span><span class="sxs-lookup"><span data-stu-id="28abd-212">&ensp;Security intelligence update version: **1.327.7.0**</span></span>  
<span data-ttu-id="28abd-213">&ensp;Publication : **29 octobre 2020**</span><span class="sxs-lookup"><span data-stu-id="28abd-213">&ensp;Released: **October 29, 2020**</span></span>  
<span data-ttu-id="28abd-214">&ensp;Plateforme : **4.18.2010.7**</span><span class="sxs-lookup"><span data-stu-id="28abd-214">&ensp;Platform: **4.18.2010.7**</span></span>  
<span data-ttu-id="28abd-215">&ensp;Moteur : **1.1.17600.5**</span><span class="sxs-lookup"><span data-stu-id="28abd-215">&ensp;Engine: **1.1.17600.5**</span></span>  
<span data-ttu-id="28abd-216">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="28abd-216">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="28abd-217">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="28abd-217">What's new</span></span>

- <span data-ttu-id="28abd-218">Nouvelles descriptions pour les catégories de menaces spéciales</span><span class="sxs-lookup"><span data-stu-id="28abd-218">New descriptions for special threat categories</span></span>
- <span data-ttu-id="28abd-219">Fonctionnalités d’émulation améliorées</span><span class="sxs-lookup"><span data-stu-id="28abd-219">Improved emulation capabilities</span></span>
- <span data-ttu-id="28abd-220">Fonctionnalités améliorées d’autoriser/bloquer l’adresse hôte</span><span class="sxs-lookup"><span data-stu-id="28abd-220">Improved host address allow/block capabilities</span></span>
- <span data-ttu-id="28abd-221">Nouvelle option dans le programme CSP Defender pour ignorer la fusion des exclusions des utilisateurs locaux</span><span class="sxs-lookup"><span data-stu-id="28abd-221">New option in Defender CSP to Ignore merging of local user exclusions</span></span>

### <a name="known-issues"></a><span data-ttu-id="28abd-222">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="28abd-222">Known Issues</span></span>

<span data-ttu-id="28abd-223">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="28abd-223">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="28abd-224">Septembre-2020 (plateforme : 4.18.2009.7 | Moteur : 1.1.17500.4)</span><span class="sxs-lookup"><span data-stu-id="28abd-224">September-2020 (Platform: 4.18.2009.7 | Engine: 1.1.17500.4)</span></span></summary>

<span data-ttu-id="28abd-225">&ensp;Version de mise à jour des informations de sécurité **: 1.325.10.0**</span><span class="sxs-lookup"><span data-stu-id="28abd-225">&ensp;Security intelligence update version: **1.325.10.0**</span></span>  
<span data-ttu-id="28abd-226">&ensp;Publication : **01 octobre 2020**</span><span class="sxs-lookup"><span data-stu-id="28abd-226">&ensp;Released: **October 01, 2020**</span></span>  
<span data-ttu-id="28abd-227">&ensp;Plateforme : **4.18.2009.7**</span><span class="sxs-lookup"><span data-stu-id="28abd-227">&ensp;Platform: **4.18.2009.7**</span></span>  
<span data-ttu-id="28abd-228">&ensp;Moteur : **1.1.17500.4**</span><span class="sxs-lookup"><span data-stu-id="28abd-228">&ensp;Engine: **1.1.17500.4**</span></span>  
<span data-ttu-id="28abd-229">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="28abd-229">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="28abd-230">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="28abd-230">What's new</span></span>

- <span data-ttu-id="28abd-231">Des autorisations d’administrateur sont requises pour restaurer les fichiers en quarantaine</span><span class="sxs-lookup"><span data-stu-id="28abd-231">Admin permissions are required to restore files in quarantine</span></span>
- <span data-ttu-id="28abd-232">Les événements au format XML sont désormais pris en charge</span><span class="sxs-lookup"><span data-stu-id="28abd-232">XML formatted events are now supported</span></span>
- <span data-ttu-id="28abd-233">Prise en charge du programme CSP pour ignorer les fusions d’exclusions</span><span class="sxs-lookup"><span data-stu-id="28abd-233">CSP support for ignoring exclusion merges</span></span>
- <span data-ttu-id="28abd-234">Nouvelles interfaces de gestion pour :</span><span class="sxs-lookup"><span data-stu-id="28abd-234">New management interfaces for:</span></span>
   - <span data-ttu-id="28abd-235">UDP Inspection</span><span class="sxs-lookup"><span data-stu-id="28abd-235">UDP Inspection</span></span>
   - <span data-ttu-id="28abd-236">Protection du réseau sur Server 2019</span><span class="sxs-lookup"><span data-stu-id="28abd-236">Network Protection on Server 2019</span></span>
   - <span data-ttu-id="28abd-237">Exclusions d’adresses IP pour la protection du réseau</span><span class="sxs-lookup"><span data-stu-id="28abd-237">IP Address exclusions for Network Protection</span></span>
- <span data-ttu-id="28abd-238">Meilleure visibilité des mesures du TPM</span><span class="sxs-lookup"><span data-stu-id="28abd-238">Improved visibility into TPM measurements</span></span>
- <span data-ttu-id="28abd-239">Amélioration de l Office de module VBA</span><span class="sxs-lookup"><span data-stu-id="28abd-239">Improved Office VBA module scanning</span></span>

### <a name="known-issues"></a><span data-ttu-id="28abd-240">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="28abd-240">Known Issues</span></span>

<span data-ttu-id="28abd-241">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="28abd-241">No known issues</span></span>  
<br/>
</details>
<details>
<summary> <span data-ttu-id="28abd-242">Août-2020 (plateforme : 4.18.2008.9 | Moteur : 1.1.17400.5)</span><span class="sxs-lookup"><span data-stu-id="28abd-242">August-2020 (Platform: 4.18.2008.9 | Engine: 1.1.17400.5)</span></span></summary>

<span data-ttu-id="28abd-243">&ensp;Version de mise à jour des informations de sécurité **: 1.323.9.0**</span><span class="sxs-lookup"><span data-stu-id="28abd-243">&ensp;Security intelligence update version: **1.323.9.0**</span></span>  
<span data-ttu-id="28abd-244">&ensp;Publication : **27 août 2020**</span><span class="sxs-lookup"><span data-stu-id="28abd-244">&ensp;Released: **August 27, 2020**</span></span>  
<span data-ttu-id="28abd-245">&ensp;Plateforme : **4.18.2008.9**</span><span class="sxs-lookup"><span data-stu-id="28abd-245">&ensp;Platform: **4.18.2008.9**</span></span>  
<span data-ttu-id="28abd-246">&ensp;Moteur : **1.1.17400.5**</span><span class="sxs-lookup"><span data-stu-id="28abd-246">&ensp;Engine: **1.1.17400.5**</span></span>  
<span data-ttu-id="28abd-247">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="28abd-247">&ensp;Support phase: **Technical upgrade support (only)**</span></span>

### <a name="whats-new"></a><span data-ttu-id="28abd-248">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="28abd-248">What's new</span></span>

- <span data-ttu-id="28abd-249">Ajouter d’autres événements de télémétrie</span><span class="sxs-lookup"><span data-stu-id="28abd-249">Add more telemetry events</span></span>
- <span data-ttu-id="28abd-250">Télémétrie améliorée des événements d’analyse</span><span class="sxs-lookup"><span data-stu-id="28abd-250">Improved scan event telemetry</span></span>
- <span data-ttu-id="28abd-251">Amélioration de la surveillance du comportement pour les analyses de mémoire</span><span class="sxs-lookup"><span data-stu-id="28abd-251">Improved behavior monitoring for memory scans</span></span>
- <span data-ttu-id="28abd-252">Amélioration de l’analyse des flux de macros</span><span class="sxs-lookup"><span data-stu-id="28abd-252">Improved macro streams scanning</span></span>
- <span data-ttu-id="28abd-253">Ajouté à `AMRunningMode` la Get-MpComputerStatus cmdlet PowerShell</span><span class="sxs-lookup"><span data-stu-id="28abd-253">Added `AMRunningMode` to Get-MpComputerStatus PowerShell cmdlet</span></span>
- <span data-ttu-id="28abd-254">[DisableAntiSpyware](/windows-hardware/customize/desktop/unattend/security-malware-windows-defender-disableantispyware) est ignoré.</span><span class="sxs-lookup"><span data-stu-id="28abd-254">[DisableAntiSpyware](/windows-hardware/customize/desktop/unattend/security-malware-windows-defender-disableantispyware) is ignored.</span></span> <span data-ttu-id="28abd-255">Antivirus Microsoft Defender s’arrête automatiquement lorsqu’il détecte un autre programme antivirus.</span><span class="sxs-lookup"><span data-stu-id="28abd-255">Microsoft Defender Antivirus automatically turns itself off when it detects another antivirus program.</span></span>


### <a name="known-issues"></a><span data-ttu-id="28abd-256">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="28abd-256">Known Issues</span></span>
<span data-ttu-id="28abd-257">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="28abd-257">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="28abd-258">Juillet-2020 (plateforme : 4.18.2007.8 | Moteur : 1.1.17300.4)</span><span class="sxs-lookup"><span data-stu-id="28abd-258">July-2020 (Platform: 4.18.2007.8 | Engine: 1.1.17300.4)</span></span></summary>

<span data-ttu-id="28abd-259">&ensp;Version de mise à jour des informations de sécurité **: 1.321.30.0**</span><span class="sxs-lookup"><span data-stu-id="28abd-259">&ensp;Security intelligence update version: **1.321.30.0**</span></span>  
<span data-ttu-id="28abd-260">&ensp;Publication : **28 juillet 2020**</span><span class="sxs-lookup"><span data-stu-id="28abd-260">&ensp;Released: **July 28, 2020**</span></span>  
<span data-ttu-id="28abd-261">&ensp;Plateforme : **4.18.2007.8**</span><span class="sxs-lookup"><span data-stu-id="28abd-261">&ensp;Platform: **4.18.2007.8**</span></span>  
<span data-ttu-id="28abd-262">&ensp;Moteur : **1.1.17300.4**</span><span class="sxs-lookup"><span data-stu-id="28abd-262">&ensp;Engine: **1.1.17300.4**</span></span>  
<span data-ttu-id="28abd-263">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="28abd-263">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="28abd-264">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="28abd-264">What's new</span></span>

- <span data-ttu-id="28abd-265">Télémétrie améliorée pour BITS</span><span class="sxs-lookup"><span data-stu-id="28abd-265">Improved telemetry for BITS</span></span>
- <span data-ttu-id="28abd-266">Validation améliorée du certificat de signature de code Authenticode</span><span class="sxs-lookup"><span data-stu-id="28abd-266">Improved Authenticode code signing certificate validation</span></span>

### <a name="known-issues"></a><span data-ttu-id="28abd-267">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="28abd-267">Known Issues</span></span>
<span data-ttu-id="28abd-268">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="28abd-268">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="28abd-269">Juin-2020 (plateforme : 4.18.2006.10 | Moteur : 1.1.17200.2)</span><span class="sxs-lookup"><span data-stu-id="28abd-269">June-2020 (Platform: 4.18.2006.10 | Engine: 1.1.17200.2)</span></span></summary>

<span data-ttu-id="28abd-270">&ensp;Version de mise à jour des informations de sécurité **: 1.319.20.0**</span><span class="sxs-lookup"><span data-stu-id="28abd-270">&ensp;Security intelligence update version: **1.319.20.0**</span></span>  
<span data-ttu-id="28abd-271">&ensp;Publication : **22 juin 2020**</span><span class="sxs-lookup"><span data-stu-id="28abd-271">&ensp;Released: **June 22, 2020**</span></span>  
<span data-ttu-id="28abd-272">&ensp;Plateforme : **4.18.2006.10**</span><span class="sxs-lookup"><span data-stu-id="28abd-272">&ensp;Platform: **4.18.2006.10**</span></span>  
<span data-ttu-id="28abd-273">&ensp;Moteur : **1.1.17200.2**</span><span class="sxs-lookup"><span data-stu-id="28abd-273">&ensp;Engine: **1.1.17200.2**</span></span>  
<span data-ttu-id="28abd-274">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="28abd-274">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="28abd-275">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="28abd-275">What's new</span></span>

- <span data-ttu-id="28abd-276">Possibilité de spécifier [l’emplacement des journaux de support](./collect-diagnostic-data.md)</span><span class="sxs-lookup"><span data-stu-id="28abd-276">Possibility to specify the [location of the support logs](./collect-diagnostic-data.md)</span></span>
- <span data-ttu-id="28abd-277">Ignorer l’analyse de rattrapage agressive en mode passif.</span><span class="sxs-lookup"><span data-stu-id="28abd-277">Skipping aggressive catchup scan in Passive mode.</span></span>
- <span data-ttu-id="28abd-278">Autoriser Defender à se mettre à jour sur les connexions à connexions avec des compteurs</span><span class="sxs-lookup"><span data-stu-id="28abd-278">Allow Defender to update on metered connections</span></span>
- <span data-ttu-id="28abd-279">Réglage des performances fixes lorsque la mise en cache est désactivée</span><span class="sxs-lookup"><span data-stu-id="28abd-279">Fixed performance tuning when caching is disabled</span></span> 
- <span data-ttu-id="28abd-280">Requête de Registre fixe</span><span class="sxs-lookup"><span data-stu-id="28abd-280">Fixed registry query</span></span> 
- <span data-ttu-id="28abd-281">Randomisation du scantime fixe dans ADMX</span><span class="sxs-lookup"><span data-stu-id="28abd-281">Fixed scantime randomization in ADMX</span></span>

### <a name="known-issues"></a><span data-ttu-id="28abd-282">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="28abd-282">Known Issues</span></span>
<span data-ttu-id="28abd-283">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="28abd-283">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="28abd-284">Mai-2020 (plateforme : 4.18.2005.4 | Moteur : 1.1.17100.2)</span><span class="sxs-lookup"><span data-stu-id="28abd-284">May-2020 (Platform: 4.18.2005.4 | Engine: 1.1.17100.2)</span></span></summary>

<span data-ttu-id="28abd-285">&ensp;Version de mise à jour des informations de sécurité **: 1.317.20.0**</span><span class="sxs-lookup"><span data-stu-id="28abd-285">&ensp;Security intelligence update version: **1.317.20.0**</span></span>  
<span data-ttu-id="28abd-286">&ensp;Publication : **26 mai 2020**</span><span class="sxs-lookup"><span data-stu-id="28abd-286">&ensp;Released: **May 26, 2020**</span></span>  
<span data-ttu-id="28abd-287">&ensp;Plateforme : **4.18.2005.4**</span><span class="sxs-lookup"><span data-stu-id="28abd-287">&ensp;Platform: **4.18.2005.4**</span></span>  
<span data-ttu-id="28abd-288">&ensp;Moteur : **1.1.17100.2**</span><span class="sxs-lookup"><span data-stu-id="28abd-288">&ensp;Engine: **1.1.17100.2**</span></span>  
<span data-ttu-id="28abd-289">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="28abd-289">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="28abd-290">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="28abd-290">What's new</span></span>

- <span data-ttu-id="28abd-291">Journalisation améliorée des événements d’analyse</span><span class="sxs-lookup"><span data-stu-id="28abd-291">Improved logging for scan events</span></span>
- <span data-ttu-id="28abd-292">Amélioration de la gestion des incidents en mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="28abd-292">Improved user mode crash handling.</span></span>
- <span data-ttu-id="28abd-293">Suivi des événements ajouté pour la protection contre la falsification</span><span class="sxs-lookup"><span data-stu-id="28abd-293">Added event tracing for Tamper protection</span></span>
- <span data-ttu-id="28abd-294">Soumission d’exemple AMSI fixe</span><span class="sxs-lookup"><span data-stu-id="28abd-294">Fixed AMSI Sample submission</span></span>
- <span data-ttu-id="28abd-295">Blocage du cloud AMSI fixe</span><span class="sxs-lookup"><span data-stu-id="28abd-295">Fixed AMSI Cloud blocking</span></span>
- <span data-ttu-id="28abd-296">Journal d’installation des mises à jour de sécurité fixes</span><span class="sxs-lookup"><span data-stu-id="28abd-296">Fixed Security update install log</span></span>

### <a name="known-issues"></a><span data-ttu-id="28abd-297">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="28abd-297">Known Issues</span></span>
<span data-ttu-id="28abd-298">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="28abd-298">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="28abd-299">Avril-2020 (plateforme : 4.18.2004.6 | Moteur : 1.1.17000.2)</span><span class="sxs-lookup"><span data-stu-id="28abd-299">April-2020 (Platform: 4.18.2004.6 | Engine: 1.1.17000.2)</span></span></summary>

<span data-ttu-id="28abd-300">&ensp;Version de mise à jour des informations de sécurité **: 1.315.12.0**</span><span class="sxs-lookup"><span data-stu-id="28abd-300">&ensp;Security intelligence update version: **1.315.12.0**</span></span>  
<span data-ttu-id="28abd-301">&ensp;Publication : **30 avril 2020**</span><span class="sxs-lookup"><span data-stu-id="28abd-301">&ensp;Released: **April 30, 2020**</span></span>  
<span data-ttu-id="28abd-302">&ensp;Plateforme : **4.18.2004.6**</span><span class="sxs-lookup"><span data-stu-id="28abd-302">&ensp;Platform: **4.18.2004.6**</span></span>  
<span data-ttu-id="28abd-303">&ensp;Moteur : **1.1.17000.2**</span><span class="sxs-lookup"><span data-stu-id="28abd-303">&ensp;Engine: **1.1.17000.2**</span></span>  
<span data-ttu-id="28abd-304">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="28abd-304">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="28abd-305">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="28abd-305">What's new</span></span>
- <span data-ttu-id="28abd-306">Améliorations de WDfilter</span><span class="sxs-lookup"><span data-stu-id="28abd-306">WDfilter improvements</span></span>
- <span data-ttu-id="28abd-307">Ajouter des données d’événements actionnables à des événements de détection de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="28abd-307">Add more actionable event data to attack surface reduction detection events</span></span>
- <span data-ttu-id="28abd-308">Informations de version fixes dans les données de diagnostic et WMI</span><span class="sxs-lookup"><span data-stu-id="28abd-308">Fixed version information in diagnostic data and WMI</span></span>
- <span data-ttu-id="28abd-309">Version de plateforme incorrecte corrigée dans l’interface utilisateur après la mise à jour de la plateforme</span><span class="sxs-lookup"><span data-stu-id="28abd-309">Fixed incorrect platform version in UI after platform update</span></span>
- <span data-ttu-id="28abd-310">Intel d’URL dynamique pour la protection contre les menaces sans fichier</span><span class="sxs-lookup"><span data-stu-id="28abd-310">Dynamic URL intel for Fileless threat protection</span></span>
- <span data-ttu-id="28abd-311">Fonctionnalité d’analyse UEFI</span><span class="sxs-lookup"><span data-stu-id="28abd-311">UEFI scan capability</span></span>
- <span data-ttu-id="28abd-312">Étendre la journalisation pour les mises à jour</span><span class="sxs-lookup"><span data-stu-id="28abd-312">Extend logging for updates</span></span>

### <a name="known-issues"></a><span data-ttu-id="28abd-313">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="28abd-313">Known Issues</span></span>
<span data-ttu-id="28abd-314">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="28abd-314">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="28abd-315">Mars-2020 (plateforme : 4.18.2003.8 | Moteur : 1.1.16900.2)</span><span class="sxs-lookup"><span data-stu-id="28abd-315">March-2020 (Platform: 4.18.2003.8 | Engine: 1.1.16900.2)</span></span></summary>

<span data-ttu-id="28abd-316">&ensp;Version de mise à jour des informations de sécurité **: 1.313.8.0**</span><span class="sxs-lookup"><span data-stu-id="28abd-316">&ensp;Security intelligence update version: **1.313.8.0**</span></span>  
<span data-ttu-id="28abd-317">&ensp;Publication : **24 mars 2020**</span><span class="sxs-lookup"><span data-stu-id="28abd-317">&ensp;Released: **March 24, 2020**</span></span>  
<span data-ttu-id="28abd-318">&ensp;Plateforme : **4.18.2003.8**</span><span class="sxs-lookup"><span data-stu-id="28abd-318">&ensp;Platform: **4.18.2003.8**</span></span>  
<span data-ttu-id="28abd-319">&ensp;Moteur : **1.1.16900.4**</span><span class="sxs-lookup"><span data-stu-id="28abd-319">&ensp;Engine: **1.1.16900.4**</span></span>  
<span data-ttu-id="28abd-320">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="28abd-320">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="28abd-321">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="28abd-321">What's new</span></span>

- <span data-ttu-id="28abd-322">Option limitation du processeur ajoutée à [MpCmdRun](./command-line-arguments-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="28abd-322">CPU Throttling option added to [MpCmdRun](./command-line-arguments-microsoft-defender-antivirus.md)</span></span>
- <span data-ttu-id="28abd-323">Améliorer les fonctionnalités de diagnostic</span><span class="sxs-lookup"><span data-stu-id="28abd-323">Improve diagnostic capability</span></span>
- <span data-ttu-id="28abd-324">réduire le délai d’out des informations de sécurité (5 min)</span><span class="sxs-lookup"><span data-stu-id="28abd-324">reduce Security intelligence timeout (5 min)</span></span>
- <span data-ttu-id="28abd-325">Étendre la fonctionnalité de journal interne du moteur AMSI</span><span class="sxs-lookup"><span data-stu-id="28abd-325">Extend AMSI engine internal log capability</span></span>
- <span data-ttu-id="28abd-326">Améliorer la notification pour le blocage des processus</span><span class="sxs-lookup"><span data-stu-id="28abd-326">Improve notification for process blocking</span></span>
   
### <a name="known-issues"></a><span data-ttu-id="28abd-327">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="28abd-327">Known Issues</span></span>
<span data-ttu-id="28abd-328">[**Fixe**] Antivirus Microsoft Defender ignorer les fichiers lors de l’exécution d’une analyse.</span><span class="sxs-lookup"><span data-stu-id="28abd-328">[**Fixed**] Microsoft Defender Antivirus is skipping files when running a scan.</span></span>

<br/>
</details>

<details>

<summary> <span data-ttu-id="28abd-329">Février-2020 (plateforme : - | Moteur : 1.1.16800.2)</span><span class="sxs-lookup"><span data-stu-id="28abd-329">February-2020 (Platform: - | Engine: 1.1.16800.2)</span></span></summary>
  

<span data-ttu-id="28abd-330">&ensp;Version de mise à jour des informations de sécurité **: 1.311.4.0** </span><span class="sxs-lookup"><span data-stu-id="28abd-330">&ensp;Security intelligence update version: **1.311.4.0** </span></span>  
<span data-ttu-id="28abd-331">&ensp;Publication : **25 février 2020**</span><span class="sxs-lookup"><span data-stu-id="28abd-331">&ensp;Released: **February 25, 2020**</span></span>  
<span data-ttu-id="28abd-332">&ensp;Plateforme/Client : **-**</span><span class="sxs-lookup"><span data-stu-id="28abd-332">&ensp;Platform/Client: **-**</span></span>  
<span data-ttu-id="28abd-333">&ensp;Moteur : **1.1.16800.2**</span><span class="sxs-lookup"><span data-stu-id="28abd-333">&ensp;Engine: **1.1.16800.2**</span></span>  
<span data-ttu-id="28abd-334">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="28abd-334">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
     
### <a name="whats-new"></a><span data-ttu-id="28abd-335">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="28abd-335">What's new</span></span>

  
### <a name="known-issues"></a><span data-ttu-id="28abd-336">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="28abd-336">Known Issues</span></span>
<span data-ttu-id="28abd-337">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="28abd-337">No known issues</span></span>
<br/>
</details>

<details>
<summary> <span data-ttu-id="28abd-338">Janvier-2020 (plateforme : 4.18.2001.10 | Moteur : 1.1.16700.2)</span><span class="sxs-lookup"><span data-stu-id="28abd-338">January-2020 (Platform: 4.18.2001.10 | Engine: 1.1.16700.2)</span></span></summary>
  

<span data-ttu-id="28abd-339">Version de mise à jour des informations de sécurité **: 1.309.32.0**</span><span class="sxs-lookup"><span data-stu-id="28abd-339">Security intelligence update version: **1.309.32.0**</span></span>  
<span data-ttu-id="28abd-340">Publication : **30 janvier 2020**</span><span class="sxs-lookup"><span data-stu-id="28abd-340">Released: **January 30, 2020**</span></span>  
<span data-ttu-id="28abd-341">Plateforme/Client : **4.18.2001.10**</span><span class="sxs-lookup"><span data-stu-id="28abd-341">Platform/Client: **4.18.2001.10**</span></span>  
<span data-ttu-id="28abd-342">Moteur : **1.1.16700.2**</span><span class="sxs-lookup"><span data-stu-id="28abd-342">Engine: **1.1.16700.2**</span></span>  
<span data-ttu-id="28abd-343">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="28abd-343">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
     
### <a name="whats-new"></a><span data-ttu-id="28abd-344">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="28abd-344">What's new</span></span>

- <span data-ttu-id="28abd-345">Correction du BSOD sur WS2016 avec Exchange</span><span class="sxs-lookup"><span data-stu-id="28abd-345">Fixed BSOD on WS2016 with Exchange</span></span>
- <span data-ttu-id="28abd-346">Prise en charge des mises à jour de plateforme lorsque le TMP est redirigé vers le chemin d’accès réseau</span><span class="sxs-lookup"><span data-stu-id="28abd-346">Support platform updates when TMP is redirected to network path</span></span>
- <span data-ttu-id="28abd-347">Les versions de plateforme et de moteur sont [ajoutées à WDSI](https://www.microsoft.com/en-us/wdsi/defenderupdates)</span><span class="sxs-lookup"><span data-stu-id="28abd-347">Platform and engine versions are added to [WDSI](https://www.microsoft.com/en-us/wdsi/defenderupdates)</span></span> <!-- The preceding URL must include "/en-us" -->
- <span data-ttu-id="28abd-348">étendre la mise à jour des signatures d’urgence [en mode passif](./microsoft-defender-antivirus-compatibility.md)</span><span class="sxs-lookup"><span data-stu-id="28abd-348">extend Emergency signature update to [passive mode](./microsoft-defender-antivirus-compatibility.md)</span></span>
- <span data-ttu-id="28abd-349">Correction du problème de 4.18.1911.3</span><span class="sxs-lookup"><span data-stu-id="28abd-349">Fix 4.18.1911.3 hang</span></span>
   
### <a name="known-issues"></a><span data-ttu-id="28abd-350">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="28abd-350">Known Issues</span></span>

<span data-ttu-id="28abd-351">[**Fixed**] Devices using [modern standby mode](/windows-hardware/design/device-experiences/modern-standby) may experience a hang with the Windows Defender filter driver that results in a gap of protection.</span><span class="sxs-lookup"><span data-stu-id="28abd-351">[**Fixed**] devices utilizing [modern standby mode](/windows-hardware/design/device-experiences/modern-standby) may experience a hang with the Windows Defender filter driver that results in a gap of protection.</span></span>  <span data-ttu-id="28abd-352">Les ordinateurs concernés semblent ne pas avoir été mis à jour vers la dernière plateforme anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="28abd-352">Affected machines appear to the customer as having not updated to the latest antimalware platform.</span></span>  
<br/>
> [!IMPORTANT]
> <span data-ttu-id="28abd-353">Cette mise à jour est :</span><span class="sxs-lookup"><span data-stu-id="28abd-353">This update is:</span></span>
> - <span data-ttu-id="28abd-354">nécessaire aux appareils RS1 exécutant une version inférieure de la plateforme pour prendre en charge SHA2 ;</span><span class="sxs-lookup"><span data-stu-id="28abd-354">needed by RS1 devices running lower version of the platform to support SHA2;</span></span>
> - <span data-ttu-id="28abd-355">a un indicateur de redémarrage pour les systèmes qui ont des problèmes en suspension ;</span><span class="sxs-lookup"><span data-stu-id="28abd-355">has a reboot flag for systems that have hanging issues;</span></span>
> - <span data-ttu-id="28abd-356">est re-publiée en avril 2020 et ne sera pas recalée par les mises à jour plus nouvelles pour conserver la disponibilité future ;</span><span class="sxs-lookup"><span data-stu-id="28abd-356">is re-released in April 2020 and will not be superseded by newer updates to keep future availability;</span></span>  
> - <span data-ttu-id="28abd-357">est classée en tant que mise à jour en raison de l’exigence de redémarrage ; et</span><span class="sxs-lookup"><span data-stu-id="28abd-357">is categorized as an update due to the reboot requirement; and</span></span>
> - <span data-ttu-id="28abd-358">est uniquement proposée avec [Windows Update](https://support.microsoft.com/help/4027667/windows-10-update).</span><span class="sxs-lookup"><span data-stu-id="28abd-358">is only be offered with [Windows Update](https://support.microsoft.com/help/4027667/windows-10-update).</span></span>
<br/>
</details>

<details>
<summary> <span data-ttu-id="28abd-359">Novembre-2019 (plateforme : 4.18.1911.3 | Moteur : 1.1.16600.7)</span><span class="sxs-lookup"><span data-stu-id="28abd-359">November-2019 (Platform: 4.18.1911.3 | Engine: 1.1.16600.7)</span></span></summary>

<span data-ttu-id="28abd-360">Version de mise à jour des informations de sécurité **: 1.307.13.0**</span><span class="sxs-lookup"><span data-stu-id="28abd-360">Security intelligence update version: **1.307.13.0**</span></span>  
<span data-ttu-id="28abd-361">Publication : **7 décembre 2019**</span><span class="sxs-lookup"><span data-stu-id="28abd-361">Released: **December 7, 2019**</span></span>  
<span data-ttu-id="28abd-362">Plateforme : **4.18.1911.3**</span><span class="sxs-lookup"><span data-stu-id="28abd-362">Platform: **4.18.1911.3**</span></span>  
<span data-ttu-id="28abd-363">Moteur : **1.1.17000.7**</span><span class="sxs-lookup"><span data-stu-id="28abd-363">Engine: **1.1.17000.7**</span></span>  
<span data-ttu-id="28abd-364">Phase de support : **aucune prise en charge**</span><span class="sxs-lookup"><span data-stu-id="28abd-364">Support phase: **No support**</span></span>  
     
### <a name="whats-new"></a><span data-ttu-id="28abd-365">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="28abd-365">What's new</span></span>

- <span data-ttu-id="28abd-366">Niveau de suivi MpCmdRun fixe</span><span class="sxs-lookup"><span data-stu-id="28abd-366">Fixed MpCmdRun tracing level</span></span>
- <span data-ttu-id="28abd-367">Informations de version de WDFilter fixes</span><span class="sxs-lookup"><span data-stu-id="28abd-367">Fixed WDFilter version info</span></span>
- <span data-ttu-id="28abd-368">Améliorer les notifications (PUA)</span><span class="sxs-lookup"><span data-stu-id="28abd-368">Improve notifications (PUA)</span></span>
- <span data-ttu-id="28abd-369">ajouter des journaux MRT pour prendre en charge les fichiers</span><span class="sxs-lookup"><span data-stu-id="28abd-369">add MRT logs to support files</span></span>
   
### <a name="known-issues"></a><span data-ttu-id="28abd-370">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="28abd-370">Known Issues</span></span>
<span data-ttu-id="28abd-371">Lorsque cette mise à jour est installée, l’appareil a besoin du package de saut 4.18.2001.10 pour pouvoir se mettre à jour vers la dernière version de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="28abd-371">When this update is installed, the device needs the jump package 4.18.2001.10 to be able to update to the latest platform version.</span></span>
<br/>
</details>


## <a name="microsoft-defender-antivirus-platform-support"></a><span data-ttu-id="28abd-372">Antivirus Microsoft Defender prise en charge de la plateforme d’Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="28abd-372">Microsoft Defender Antivirus platform support</span></span>
<span data-ttu-id="28abd-373">Les mises à jour de la plateforme et du moteur sont fournies à une cadence mensuelle.</span><span class="sxs-lookup"><span data-stu-id="28abd-373">Platform and engine updates are provided on a monthly cadence.</span></span> <span data-ttu-id="28abd-374">Pour être entièrement pris en charge, tenez à jour les dernières mises à jour de plateforme.</span><span class="sxs-lookup"><span data-stu-id="28abd-374">To be fully supported, keep current with the latest platform updates.</span></span> <span data-ttu-id="28abd-375">Notre structure de support est dynamique et évolue en deux phases en fonction de la disponibilité de la dernière version de plateforme :</span><span class="sxs-lookup"><span data-stu-id="28abd-375">Our support structure is dynamic, evolving into two phases depending on the availability of the latest platform version:</span></span>

- <span data-ttu-id="28abd-376">Phase de maintenance des mises à jour **critiques** et de sécurité : lors de l’exécution de la dernière version de la plateforme, vous serez éligible à la réception des mises à jour de sécurité et critiques sur la plateforme anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="28abd-376">**Security and Critical Updates servicing phase** - When running the latest platform version, you will be eligible to receive both Security and Critical updates to the anti-malware platform.</span></span>
 
- <span data-ttu-id="28abd-377">**Phase de support technique (uniquement)** : après la publication d’une nouvelle version de plateforme, la prise en charge des versions antérieures (N-2) sera réduit au support technique uniquement.</span><span class="sxs-lookup"><span data-stu-id="28abd-377">**Technical Support (Only) phase** - After a new platform version is released, support for older versions (N-2) will reduce to technical support only.</span></span> <span data-ttu-id="28abd-378">Les versions de plateforme antérieures à N-2 ne seront plus pris en charge.\*</span><span class="sxs-lookup"><span data-stu-id="28abd-378">Platform versions older than N-2 will no longer be supported.\*</span></span>

<span data-ttu-id="28abd-379">\*Le support technique continuera d’être fourni pour les mises à niveau de la version Windows 10 (voir la version de plateforme incluse avec [les](#platform-version-included-with-windows-10-releases)versions Windows 10 ) vers la dernière version de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="28abd-379">\* Technical support will continue to be provided for upgrades from the Windows 10 release version (see [Platform version included with Windows 10 releases](#platform-version-included-with-windows-10-releases)) to the latest platform version.</span></span>

<span data-ttu-id="28abd-380">Pendant la phase de support technique (uniquement), les incidents de support commercialement raisonnables sont fournis par le biais du support technique du service clientèle Microsoft & et des offres de support géré de Microsoft (telles que le support Premier).</span><span class="sxs-lookup"><span data-stu-id="28abd-380">During the technical support (only) phase, commercially reasonable support incidents will be provided through Microsoft Customer Service & Support and Microsoft’s managed support offerings (such as Premier Support).</span></span> <span data-ttu-id="28abd-381">Si un incident de support nécessite une escalade vers le développement pour obtenir des conseils supplémentaires, nécessite une mise à jour non de sécurité ou nécessite une mise à jour de sécurité, les clients sont invités à mettre à niveau vers la dernière version de plateforme ou une mise à jour intermédiaire (\*).</span><span class="sxs-lookup"><span data-stu-id="28abd-381">If a support incident requires escalation to development for further guidance, requires a non-security update, or requires a security update, customers will be asked to upgrade to the latest platform version or an intermediate update (\*).</span></span>

### <a name="platform-version-included-with-windows-10-releases"></a><span data-ttu-id="28abd-382">Version de plateforme incluse dans Windows 10 versions</span><span class="sxs-lookup"><span data-stu-id="28abd-382">Platform version included with Windows 10 releases</span></span>
<span data-ttu-id="28abd-383">Le tableau ci-dessous fournit les versions Antivirus Microsoft Defender de plateforme et de moteur qui sont livrées avec les versions les Windows 10 les plus récentes :</span><span class="sxs-lookup"><span data-stu-id="28abd-383">The below table provides the Microsoft Defender Antivirus platform and engine versions that are shipped with the latest Windows 10 releases:</span></span>    

|<span data-ttu-id="28abd-384">Windows 10 version</span><span class="sxs-lookup"><span data-stu-id="28abd-384">Windows 10 release</span></span>  |<span data-ttu-id="28abd-385">Version de la plateforme</span><span class="sxs-lookup"><span data-stu-id="28abd-385">Platform version</span></span>  |<span data-ttu-id="28abd-386">Version du moteur</span><span class="sxs-lookup"><span data-stu-id="28abd-386">Engine version</span></span> |<span data-ttu-id="28abd-387">Phase de prise en charge</span><span class="sxs-lookup"><span data-stu-id="28abd-387">Support phase</span></span> |
|:---|:---|:---|:---|
|<span data-ttu-id="28abd-388">2004 (20H1/20H2)</span><span class="sxs-lookup"><span data-stu-id="28abd-388">2004  (20H1/20H2)</span></span> |<span data-ttu-id="28abd-389">4.18.1909.6</span><span class="sxs-lookup"><span data-stu-id="28abd-389">4.18.1909.6</span></span> |<span data-ttu-id="28abd-390">1.1.17000.2</span><span class="sxs-lookup"><span data-stu-id="28abd-390">1.1.17000.2</span></span> | <span data-ttu-id="28abd-391">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="28abd-391">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="28abd-392">1909 (19H2)</span><span class="sxs-lookup"><span data-stu-id="28abd-392">1909  (19H2)</span></span> |<span data-ttu-id="28abd-393">4.18.1902.5</span><span class="sxs-lookup"><span data-stu-id="28abd-393">4.18.1902.5</span></span> |<span data-ttu-id="28abd-394">1.1.16700.3</span><span class="sxs-lookup"><span data-stu-id="28abd-394">1.1.16700.3</span></span> | <span data-ttu-id="28abd-395">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="28abd-395">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="28abd-396">1903 (19H1)</span><span class="sxs-lookup"><span data-stu-id="28abd-396">1903  (19H1)</span></span> |<span data-ttu-id="28abd-397">4.18.1902.5</span><span class="sxs-lookup"><span data-stu-id="28abd-397">4.18.1902.5</span></span> |<span data-ttu-id="28abd-398">1.1.15600.4</span><span class="sxs-lookup"><span data-stu-id="28abd-398">1.1.15600.4</span></span> | <span data-ttu-id="28abd-399">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="28abd-399">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="28abd-400">1809 (RS5)</span><span class="sxs-lookup"><span data-stu-id="28abd-400">1809  (RS5)</span></span> |<span data-ttu-id="28abd-401">4.18.1807.18075</span><span class="sxs-lookup"><span data-stu-id="28abd-401">4.18.1807.18075</span></span> |<span data-ttu-id="28abd-402">1.1.15000.2</span><span class="sxs-lookup"><span data-stu-id="28abd-402">1.1.15000.2</span></span> | <span data-ttu-id="28abd-403">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="28abd-403">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="28abd-404">1803 (RS4)</span><span class="sxs-lookup"><span data-stu-id="28abd-404">1803  (RS4)</span></span> |<span data-ttu-id="28abd-405">4.13.17134.1</span><span class="sxs-lookup"><span data-stu-id="28abd-405">4.13.17134.1</span></span> |<span data-ttu-id="28abd-406">1.1.14600.4</span><span class="sxs-lookup"><span data-stu-id="28abd-406">1.1.14600.4</span></span> | <span data-ttu-id="28abd-407">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="28abd-407">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="28abd-408">1709 (RS3)</span><span class="sxs-lookup"><span data-stu-id="28abd-408">1709  (RS3)</span></span> |<span data-ttu-id="28abd-409">4.12.16299.15</span><span class="sxs-lookup"><span data-stu-id="28abd-409">4.12.16299.15</span></span> |<span data-ttu-id="28abd-410">1.1.14104.0</span><span class="sxs-lookup"><span data-stu-id="28abd-410">1.1.14104.0</span></span> | <span data-ttu-id="28abd-411">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="28abd-411">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="28abd-412">1703 (RS2)</span><span class="sxs-lookup"><span data-stu-id="28abd-412">1703  (RS2)</span></span> |<span data-ttu-id="28abd-413">4.11.15603.2</span><span class="sxs-lookup"><span data-stu-id="28abd-413">4.11.15603.2</span></span> |<span data-ttu-id="28abd-414">1.1.13504.0</span><span class="sxs-lookup"><span data-stu-id="28abd-414">1.1.13504.0</span></span> | <span data-ttu-id="28abd-415">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="28abd-415">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="28abd-416">1607 (RS1)</span><span class="sxs-lookup"><span data-stu-id="28abd-416">1607 (RS1)</span></span> |<span data-ttu-id="28abd-417">4.10.14393.3683</span><span class="sxs-lookup"><span data-stu-id="28abd-417">4.10.14393.3683</span></span> |<span data-ttu-id="28abd-418">1.1.12805.0</span><span class="sxs-lookup"><span data-stu-id="28abd-418">1.1.12805.0</span></span> | <span data-ttu-id="28abd-419">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="28abd-419">Technical upgrade support (only)</span></span> |  

<span data-ttu-id="28abd-420">Pour Windows 10 de publication, consultez la [Windows de faits sur le cycle de vie.](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet)</span><span class="sxs-lookup"><span data-stu-id="28abd-420">For Windows 10 release information, see the [Windows lifecycle fact sheet](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet).</span></span>

## <a name="updates-for-deployment-image-servicing-and-management-dism"></a><span data-ttu-id="28abd-421">Mises à jour pour la gestion et la maintenance des images de déploiement (DISM)</span><span class="sxs-lookup"><span data-stu-id="28abd-421">Updates for Deployment Image Servicing and Management (DISM)</span></span>

<span data-ttu-id="28abd-422">Nous vous recommandons de mettre à jour vos images d’installation Windows 10 (éditions Enterprise, Pro et Famille), Windows Server 2019 et Windows Server 2016 OS avec les dernières mises à jour antivirus et anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="28abd-422">We recommend updating your Windows 10 (Enterprise, Pro, and Home editions), Windows Server 2019, and Windows Server 2016 OS installation images with the latest antivirus and antimalware updates.</span></span> <span data-ttu-id="28abd-423">La mise à jour de vos images d’installation du système d’exploitation permet d’éviter un écart de protection.</span><span class="sxs-lookup"><span data-stu-id="28abd-423">Keeping your OS installation images up to date helps avoid a gap in protection.</span></span> 

<span data-ttu-id="28abd-424">Pour plus d’informations, voir Mise à [jour de Microsoft Defender pour Windows images d’installation du système d’exploitation.](https://support.microsoft.com/help/4568292/defender-update-for-windows-operating-system-installation-images)</span><span class="sxs-lookup"><span data-stu-id="28abd-424">For more information, see [Microsoft Defender update for Windows operating system installation images](https://support.microsoft.com/help/4568292/defender-update-for-windows-operating-system-installation-images).</span></span>

<details>
<summary><span data-ttu-id="28abd-425">1.1.2106.01</span><span class="sxs-lookup"><span data-stu-id="28abd-425">1.1.2106.01</span></span></summary>

<span data-ttu-id="28abd-426">&ensp;Version du package **: 1.1.2106.01**  </span><span class="sxs-lookup"><span data-stu-id="28abd-426">&ensp;Package version: **1.1.2106.01**  </span></span>  
<span data-ttu-id="28abd-427">&ensp;Version de la plateforme **: 4.18.2104.14** </span><span class="sxs-lookup"><span data-stu-id="28abd-427">&ensp;Platform version: **4.18.2104.14** </span></span>  
<span data-ttu-id="28abd-428">&ensp;Version du moteur **: 1.1.18100.6**</span><span class="sxs-lookup"><span data-stu-id="28abd-428">&ensp;Engine version: **1.1.18100.6**</span></span>  
<span data-ttu-id="28abd-429">&ensp;Version de signature **: 1.339.1923.0**</span><span class="sxs-lookup"><span data-stu-id="28abd-429">&ensp;Signature version: **1.339.1923.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="28abd-430">Correctifs</span><span class="sxs-lookup"><span data-stu-id="28abd-430">Fixes</span></span>
- <span data-ttu-id="28abd-431">Aucun</span><span class="sxs-lookup"><span data-stu-id="28abd-431">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="28abd-432">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="28abd-432">Additional information</span></span>
- <span data-ttu-id="28abd-433">Aucun</span><span class="sxs-lookup"><span data-stu-id="28abd-433">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="28abd-434">1.1.2105.01</span><span class="sxs-lookup"><span data-stu-id="28abd-434">1.1.2105.01</span></span></summary>

<span data-ttu-id="28abd-435">&ensp;Version du package **: 1.1.2105.01**  </span><span class="sxs-lookup"><span data-stu-id="28abd-435">&ensp;Package version: **1.1.2105.01**  </span></span>  
<span data-ttu-id="28abd-436">&ensp;Version de la plateforme **: 4.18.2103.7** </span><span class="sxs-lookup"><span data-stu-id="28abd-436">&ensp;Platform version: **4.18.2103.7** </span></span>  
<span data-ttu-id="28abd-437">&ensp;Version du moteur **: 1.1.18100.6**</span><span class="sxs-lookup"><span data-stu-id="28abd-437">&ensp;Engine version: **1.1.18100.6**</span></span>  
<span data-ttu-id="28abd-438">&ensp;Version de signature **: 1.339.42.0**</span><span class="sxs-lookup"><span data-stu-id="28abd-438">&ensp;Signature version: **1.339.42.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="28abd-439">Correctifs</span><span class="sxs-lookup"><span data-stu-id="28abd-439">Fixes</span></span>
- <span data-ttu-id="28abd-440">Aucun</span><span class="sxs-lookup"><span data-stu-id="28abd-440">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="28abd-441">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="28abd-441">Additional information</span></span>
- <span data-ttu-id="28abd-442">Aucun</span><span class="sxs-lookup"><span data-stu-id="28abd-442">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="28abd-443">1.1.2104.01</span><span class="sxs-lookup"><span data-stu-id="28abd-443">1.1.2104.01</span></span></summary>

<span data-ttu-id="28abd-444">&ensp;Version du package **: 1.1.2104.01**  </span><span class="sxs-lookup"><span data-stu-id="28abd-444">&ensp;Package version: **1.1.2104.01**  </span></span>  
<span data-ttu-id="28abd-445">&ensp;Version de plateforme **: 4.18.2102.4** </span><span class="sxs-lookup"><span data-stu-id="28abd-445">&ensp;Platform version: **4.18.2102.4** </span></span>  
<span data-ttu-id="28abd-446">&ensp;Version du moteur **: 1.1.18000.5**</span><span class="sxs-lookup"><span data-stu-id="28abd-446">&ensp;Engine version: **1.1.18000.5**</span></span>  
<span data-ttu-id="28abd-447">&ensp;Version de signature **: 1.335.232.0**</span><span class="sxs-lookup"><span data-stu-id="28abd-447">&ensp;Signature version: **1.335.232.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="28abd-448">Correctifs</span><span class="sxs-lookup"><span data-stu-id="28abd-448">Fixes</span></span>
- <span data-ttu-id="28abd-449">Aucun</span><span class="sxs-lookup"><span data-stu-id="28abd-449">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="28abd-450">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="28abd-450">Additional information</span></span>
- <span data-ttu-id="28abd-451">Aucun</span><span class="sxs-lookup"><span data-stu-id="28abd-451">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="28abd-452">1.1.2103.01</span><span class="sxs-lookup"><span data-stu-id="28abd-452">1.1.2103.01</span></span></summary>

<span data-ttu-id="28abd-453">&ensp;Version du package **: 1.1.2103.01**  </span><span class="sxs-lookup"><span data-stu-id="28abd-453">&ensp;Package version: **1.1.2103.01**  </span></span>  
<span data-ttu-id="28abd-454">&ensp;Version de plateforme **: 4.18.2101.9** </span><span class="sxs-lookup"><span data-stu-id="28abd-454">&ensp;Platform version: **4.18.2101.9** </span></span>  
<span data-ttu-id="28abd-455">&ensp;Version du moteur **: 1.1.17800.5**</span><span class="sxs-lookup"><span data-stu-id="28abd-455">&ensp;Engine version: **1.1.17800.5**</span></span>  
<span data-ttu-id="28abd-456">&ensp;Version de signature **: 1.331.2302.0**</span><span class="sxs-lookup"><span data-stu-id="28abd-456">&ensp;Signature version: **1.331.2302.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="28abd-457">Correctifs</span><span class="sxs-lookup"><span data-stu-id="28abd-457">Fixes</span></span>
- <span data-ttu-id="28abd-458">Aucun</span><span class="sxs-lookup"><span data-stu-id="28abd-458">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="28abd-459">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="28abd-459">Additional information</span></span>
- <span data-ttu-id="28abd-460">Aucun</span><span class="sxs-lookup"><span data-stu-id="28abd-460">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="28abd-461">1.1.2102.03</span><span class="sxs-lookup"><span data-stu-id="28abd-461">1.1.2102.03</span></span></summary>

<span data-ttu-id="28abd-462">&ensp;Version du package **: 1.1.2102.03**  </span><span class="sxs-lookup"><span data-stu-id="28abd-462">&ensp;Package version: **1.1.2102.03**  </span></span>  
<span data-ttu-id="28abd-463">&ensp;Version de la plateforme **: 4.18.2011.6** </span><span class="sxs-lookup"><span data-stu-id="28abd-463">&ensp;Platform version: **4.18.2011.6** </span></span>  
<span data-ttu-id="28abd-464">&ensp;Version du moteur **: 1.1.17800.5**</span><span class="sxs-lookup"><span data-stu-id="28abd-464">&ensp;Engine version: **1.1.17800.5**</span></span>  
<span data-ttu-id="28abd-465">&ensp;Version de signature **: 1.331.174.0**</span><span class="sxs-lookup"><span data-stu-id="28abd-465">&ensp;Signature version: **1.331.174.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="28abd-466">Correctifs</span><span class="sxs-lookup"><span data-stu-id="28abd-466">Fixes</span></span>
- <span data-ttu-id="28abd-467">Aucun</span><span class="sxs-lookup"><span data-stu-id="28abd-467">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="28abd-468">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="28abd-468">Additional information</span></span>
- <span data-ttu-id="28abd-469">Aucun</span><span class="sxs-lookup"><span data-stu-id="28abd-469">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="28abd-470">1.1.2101.02</span><span class="sxs-lookup"><span data-stu-id="28abd-470">1.1.2101.02</span></span></summary>

<span data-ttu-id="28abd-471">&ensp;Version du package **: 1.1.2101.02**  </span><span class="sxs-lookup"><span data-stu-id="28abd-471">&ensp;Package version: **1.1.2101.02**  </span></span>  
<span data-ttu-id="28abd-472">&ensp;Version de la plateforme **: 4.18.2011.6** </span><span class="sxs-lookup"><span data-stu-id="28abd-472">&ensp;Platform version: **4.18.2011.6** </span></span>  
<span data-ttu-id="28abd-473">&ensp;Version du moteur **: 1.1.17700.4**</span><span class="sxs-lookup"><span data-stu-id="28abd-473">&ensp;Engine version: **1.1.17700.4**</span></span>  
<span data-ttu-id="28abd-474">&ensp;Version de signature **: 1.329.1796.0**</span><span class="sxs-lookup"><span data-stu-id="28abd-474">&ensp;Signature version: **1.329.1796.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="28abd-475">Correctifs</span><span class="sxs-lookup"><span data-stu-id="28abd-475">Fixes</span></span>
- <span data-ttu-id="28abd-476">Aucun</span><span class="sxs-lookup"><span data-stu-id="28abd-476">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="28abd-477">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="28abd-477">Additional information</span></span>
- <span data-ttu-id="28abd-478">Aucun</span><span class="sxs-lookup"><span data-stu-id="28abd-478">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="28abd-479">1.1.2012.01</span><span class="sxs-lookup"><span data-stu-id="28abd-479">1.1.2012.01</span></span></summary>

<span data-ttu-id="28abd-480">&ensp;Version du package **: 1.1.2012.01**  </span><span class="sxs-lookup"><span data-stu-id="28abd-480">&ensp;Package version: **1.1.2012.01**  </span></span>  
<span data-ttu-id="28abd-481">&ensp;Version de plateforme **: 4.18.2010.7** </span><span class="sxs-lookup"><span data-stu-id="28abd-481">&ensp;Platform version: **4.18.2010.7** </span></span>  
<span data-ttu-id="28abd-482">&ensp;Version du moteur **: 1.1.17600.5**</span><span class="sxs-lookup"><span data-stu-id="28abd-482">&ensp;Engine version: **1.1.17600.5**</span></span>  
<span data-ttu-id="28abd-483">&ensp;Version de signature **: 1.327.1991.0**</span><span class="sxs-lookup"><span data-stu-id="28abd-483">&ensp;Signature version: **1.327.1991.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="28abd-484">Correctifs</span><span class="sxs-lookup"><span data-stu-id="28abd-484">Fixes</span></span>
- <span data-ttu-id="28abd-485">Aucun</span><span class="sxs-lookup"><span data-stu-id="28abd-485">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="28abd-486">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="28abd-486">Additional information</span></span>
- <span data-ttu-id="28abd-487">Aucun</span><span class="sxs-lookup"><span data-stu-id="28abd-487">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="28abd-488">1.1.2011.02</span><span class="sxs-lookup"><span data-stu-id="28abd-488">1.1.2011.02</span></span></summary>

<span data-ttu-id="28abd-489">&ensp;Version du package **: 1.1.2011.02**  </span><span class="sxs-lookup"><span data-stu-id="28abd-489">&ensp;Package version: **1.1.2011.02**  </span></span>  
<span data-ttu-id="28abd-490">&ensp;Version de plateforme **: 4.18.2010.7** </span><span class="sxs-lookup"><span data-stu-id="28abd-490">&ensp;Platform version: **4.18.2010.7** </span></span>  
<span data-ttu-id="28abd-491">&ensp;Version du moteur **: 1.1.17600.5**</span><span class="sxs-lookup"><span data-stu-id="28abd-491">&ensp;Engine version: **1.1.17600.5**</span></span>  
<span data-ttu-id="28abd-492">&ensp;Version de signature **: 1.327.658.0**</span><span class="sxs-lookup"><span data-stu-id="28abd-492">&ensp;Signature version: **1.327.658.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="28abd-493">Correctifs</span><span class="sxs-lookup"><span data-stu-id="28abd-493">Fixes</span></span>
- <span data-ttu-id="28abd-494">Aucun</span><span class="sxs-lookup"><span data-stu-id="28abd-494">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="28abd-495">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="28abd-495">Additional information</span></span>
- <span data-ttu-id="28abd-496">Signatures Antivirus Microsoft Defender actualisées</span><span class="sxs-lookup"><span data-stu-id="28abd-496">Refreshed Microsoft Defender Antivirus signatures</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="28abd-497">1.1.2011.01</span><span class="sxs-lookup"><span data-stu-id="28abd-497">1.1.2011.01</span></span></summary>

<span data-ttu-id="28abd-498">&ensp;Version du package **: 1.1.2011.01**  </span><span class="sxs-lookup"><span data-stu-id="28abd-498">&ensp;Package version: **1.1.2011.01**  </span></span>  
<span data-ttu-id="28abd-499">&ensp;Version de la plateforme **: 4.18.2009.7**</span><span class="sxs-lookup"><span data-stu-id="28abd-499">&ensp;Platform version: **4.18.2009.7**</span></span>  
<span data-ttu-id="28abd-500">&ensp;Version du moteur **: 1.1.17600.5**</span><span class="sxs-lookup"><span data-stu-id="28abd-500">&ensp;Engine version: **1.1.17600.5**</span></span>  
<span data-ttu-id="28abd-501">&ensp;Version de signature **: 1.327.344.0**</span><span class="sxs-lookup"><span data-stu-id="28abd-501">&ensp;Signature version: **1.327.344.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="28abd-502">Correctifs</span><span class="sxs-lookup"><span data-stu-id="28abd-502">Fixes</span></span>
- <span data-ttu-id="28abd-503">Aucun</span><span class="sxs-lookup"><span data-stu-id="28abd-503">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="28abd-504">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="28abd-504">Additional information</span></span>
- <span data-ttu-id="28abd-505">Aucun</span><span class="sxs-lookup"><span data-stu-id="28abd-505">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="28abd-506">1.1.2009.10</span><span class="sxs-lookup"><span data-stu-id="28abd-506">1.1.2009.10</span></span></summary>

<span data-ttu-id="28abd-507">&ensp;Version du package **: 1.1.2011.01**  </span><span class="sxs-lookup"><span data-stu-id="28abd-507">&ensp;Package version: **1.1.2011.01**  </span></span>  
<span data-ttu-id="28abd-508">&ensp;Version de la plateforme **: 4.18.2008.9** </span><span class="sxs-lookup"><span data-stu-id="28abd-508">&ensp;Platform version: **4.18.2008.9** </span></span>  
<span data-ttu-id="28abd-509">&ensp;Version du moteur **: 1.1.17400.5**</span><span class="sxs-lookup"><span data-stu-id="28abd-509">&ensp;Engine version: **1.1.17400.5**</span></span>  
<span data-ttu-id="28abd-510">&ensp;Version de signature **: 1.327.2216.0**</span><span class="sxs-lookup"><span data-stu-id="28abd-510">&ensp;Signature version: **1.327.2216.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="28abd-511">Correctifs</span><span class="sxs-lookup"><span data-stu-id="28abd-511">Fixes</span></span>
- <span data-ttu-id="28abd-512">Aucun</span><span class="sxs-lookup"><span data-stu-id="28abd-512">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="28abd-513">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="28abd-513">Additional information</span></span>
- <span data-ttu-id="28abd-514">Ajout de la prise en charge Windows 10 images d’installation du système d’exploitation RS1 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="28abd-514">Added support for Windows 10 RS1 or later OS install images.</span></span>  
<br/>
</details>

## <a name="additional-resources"></a><span data-ttu-id="28abd-515">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="28abd-515">Additional resources</span></span>

| <span data-ttu-id="28abd-516">Article</span><span class="sxs-lookup"><span data-stu-id="28abd-516">Article</span></span> | <span data-ttu-id="28abd-517">Description</span><span class="sxs-lookup"><span data-stu-id="28abd-517">Description</span></span>  |
|:---|:---|
|[<span data-ttu-id="28abd-518">Mise à jour de Microsoft Defender Windows images d’installation du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="28abd-518">Microsoft Defender update for Windows operating system installation images</span></span>](https://support.microsoft.com/help/4568292/defender-update-for-windows-operating-system-installation-images)  | <span data-ttu-id="28abd-519">Passer en revue les packages de mise à jour anti-programme malveillant pour vos images d’installation du système d’exploitation (fichiers WIM et VHD).</span><span class="sxs-lookup"><span data-stu-id="28abd-519">Review antimalware update packages for your OS installation images (WIM and VHD files).</span></span> <span data-ttu-id="28abd-520">Obtenez Antivirus Microsoft Defender mises à jour de Windows 10 (éditions Enterprise, Pro et Famille), Windows Server 2019 et Windows Server 2016 images d’installation.</span><span class="sxs-lookup"><span data-stu-id="28abd-520">Get Microsoft Defender Antivirus updates for Windows 10 (Enterprise, Pro, and Home editions), Windows Server 2019, and Windows Server 2016 installation images.</span></span>  |
|[<span data-ttu-id="28abd-521">Gérer le téléchargement et l’application des mises à jour de protection</span><span class="sxs-lookup"><span data-stu-id="28abd-521">Manage how protection updates are downloaded and applied</span></span>](manage-protection-updates-microsoft-defender-antivirus.md) | <span data-ttu-id="28abd-522">Les mises à jour de protection peuvent être mises à jour via de nombreuses sources.</span><span class="sxs-lookup"><span data-stu-id="28abd-522">Protection updates can be delivered through many sources.</span></span> |
|[<span data-ttu-id="28abd-523">Gérer le moment où les mises à jour de protection doivent être téléchargées et appliquées</span><span class="sxs-lookup"><span data-stu-id="28abd-523">Manage when protection updates should be downloaded and applied</span></span>](manage-protection-update-schedule-microsoft-defender-antivirus.md) | <span data-ttu-id="28abd-524">Vous pouvez planifier le téléchargement des mises à jour de la protection.</span><span class="sxs-lookup"><span data-stu-id="28abd-524">You can schedule when protection updates should be downloaded.</span></span> |
|[<span data-ttu-id="28abd-525">Gérer les mises à jour des points de terminaison qui ne sont plus à jour</span><span class="sxs-lookup"><span data-stu-id="28abd-525">Manage updates for endpoints that are out of date</span></span>](manage-outdated-endpoints-microsoft-defender-antivirus.md) | <span data-ttu-id="28abd-526">Si un point de terminaison manque une mise à jour ou une analyse programmée, vous pouvez forcer une mise à jour ou une analyse la prochaine fois qu’un utilisateur se signe.</span><span class="sxs-lookup"><span data-stu-id="28abd-526">If an endpoint misses an update or scheduled scan, you can force an update or scan the next time a user signs in.</span></span> |
|[<span data-ttu-id="28abd-527">Gérer les mises à jour forcées en fonction des événements</span><span class="sxs-lookup"><span data-stu-id="28abd-527">Manage event-based forced updates</span></span>](manage-event-based-updates-microsoft-defender-antivirus.md) | <span data-ttu-id="28abd-528">Vous pouvez définir des mises à jour de protection à télécharger au démarrage ou après certains événements de protection livrés par le cloud.</span><span class="sxs-lookup"><span data-stu-id="28abd-528">You can set protection updates to be downloaded at startup or after certain cloud-delivered protection events.</span></span> |
|[<span data-ttu-id="28abd-529">Gérer les mises à jour pour les appareils mobiles et les machines virtuelles</span><span class="sxs-lookup"><span data-stu-id="28abd-529">Manage updates for mobile devices and virtual machines (VMs)</span></span>](manage-updates-mobile-devices-vms-microsoft-defender-antivirus.md)| <span data-ttu-id="28abd-530">Vous pouvez spécifier des paramètres, par exemple si des mises à jour doivent être mises à jour sur l’alimentation de la batterie, qui sont particulièrement utiles pour les appareils mobiles et les ordinateurs virtuels.</span><span class="sxs-lookup"><span data-stu-id="28abd-530">You can specify settings, such as whether updates should occur on battery power, that are especially useful for mobile devices and virtual machines.</span></span> |
