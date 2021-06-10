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
ms.date: 06/08/2021
ms.openlocfilehash: ccbb57d781196e352e0fed456a1f7cb43eb17300
ms.sourcegitcommit: 50908a93554290ff1157b58d0a868a33e012513c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52822273"
---
# <a name="manage-microsoft-defender-antivirus-updates-and-apply-baselines"></a><span data-ttu-id="835a3-104">Gérer les mises Antivirus Microsoft Defender jour et appliquer les lignes de base</span><span class="sxs-lookup"><span data-stu-id="835a3-104">Manage Microsoft Defender Antivirus updates and apply baselines</span></span>

<span data-ttu-id="835a3-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="835a3-105">**Applies to:**</span></span>

- [<span data-ttu-id="835a3-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="835a3-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)
- <span data-ttu-id="835a3-107">Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="835a3-107">Microsoft Defender Antivirus</span></span>

<span data-ttu-id="835a3-108">Il existe deux types de mises à jour liées à la mise Antivirus Microsoft Defender jour :</span><span class="sxs-lookup"><span data-stu-id="835a3-108">There are two types of updates related to keeping Microsoft Defender Antivirus up to date:</span></span>

- <span data-ttu-id="835a3-109">Mises à jour de l’intelligence de la sécurité</span><span class="sxs-lookup"><span data-stu-id="835a3-109">Security intelligence updates</span></span>
- <span data-ttu-id="835a3-110">Mises à jour de produit</span><span class="sxs-lookup"><span data-stu-id="835a3-110">Product updates</span></span>

> [!IMPORTANT]
> <span data-ttu-id="835a3-111">Le Antivirus Microsoft Defender à jour est essentiel pour garantir que vos appareils disposent des dernières technologies et fonctionnalités nécessaires pour se protéger contre les nouveaux programmes malveillants et les nouvelles techniques d’attaque.</span><span class="sxs-lookup"><span data-stu-id="835a3-111">Keeping Microsoft Defender Antivirus up to date is critical to assure your devices have the latest technology and features needed to protect against new malware and attack techniques.</span></span>
> 
> <span data-ttu-id="835a3-112">Veillez à mettre à jour votre protection antivirus même si Antivirus Microsoft Defender est en cours d’exécution [en mode passif.](./microsoft-defender-antivirus-compatibility.md)</span><span class="sxs-lookup"><span data-stu-id="835a3-112">Make sure to update your antivirus protection even if Microsoft Defender Antivirus is running in [passive mode](./microsoft-defender-antivirus-compatibility.md).</span></span>
> 
> <span data-ttu-id="835a3-113">Pour voir le moteur, la plateforme et la date de signature les plus à jour, consultez les mises à jour de l’intelligence de sécurité pour Antivirus Microsoft Defender logiciel [anti-programme](https://www.microsoft.com/en-us/wdsi/defenderupdates)malveillant Microsoft.</span><span class="sxs-lookup"><span data-stu-id="835a3-113">To see the most current engine, platform, and signature date, visit the [Security intelligence updates for Microsoft Defender Antivirus and other Microsoft antimalware](https://www.microsoft.com/en-us/wdsi/defenderupdates).</span></span>

## <a name="security-intelligence-updates"></a><span data-ttu-id="835a3-114">Mises à jour de l’intelligence de la sécurité</span><span class="sxs-lookup"><span data-stu-id="835a3-114">Security intelligence updates</span></span>

<span data-ttu-id="835a3-115">Antivirus Microsoft Defender utilise la protection fournie par le [cloud](cloud-protection-microsoft-defender-antivirus.md) (également appelée Microsoft Advanced Protection Service ou MAPS) et télécharge régulièrement les mises à jour de l’intelligence de sécurité pour fournir une protection.</span><span class="sxs-lookup"><span data-stu-id="835a3-115">Microsoft Defender Antivirus uses [cloud-delivered protection](cloud-protection-microsoft-defender-antivirus.md) (also called the Microsoft Advanced Protection Service or MAPS) and periodically downloads security intelligence updates to provide protection.</span></span>

> [!NOTE]
> <span data-ttu-id="835a3-116">Les mises à jour sont publiées sous les numéros de la Ko ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="835a3-116">Updates are released under the below KB numbers:</span></span>  
> - <span data-ttu-id="835a3-117">Antivirus Microsoft Defender : KB2267602</span><span class="sxs-lookup"><span data-stu-id="835a3-117">Microsoft Defender Antivirus: KB2267602</span></span>  
> - <span data-ttu-id="835a3-118">System Center Endpoint Protection : KB2461484</span><span class="sxs-lookup"><span data-stu-id="835a3-118">System Center Endpoint Protection: KB2461484</span></span>

<span data-ttu-id="835a3-119">La protection cloud est toujours active et nécessite une connexion active à Internet pour fonctionner.</span><span class="sxs-lookup"><span data-stu-id="835a3-119">Cloud-delivered protection is always on and requires an active connection to the Internet to function.</span></span> <span data-ttu-id="835a3-120">Les mises à jour des informations de sécurité se produisent à une cadence programmée (configurable via une stratégie).</span><span class="sxs-lookup"><span data-stu-id="835a3-120">Security intelligence updates occur on a scheduled cadence (configurable via policy).</span></span> <span data-ttu-id="835a3-121">Pour plus d’informations, voir Utiliser la protection fournie par le [cloud microsoft dans Antivirus Microsoft Defender](cloud-protection-microsoft-defender-antivirus.md).</span><span class="sxs-lookup"><span data-stu-id="835a3-121">For more information, see [Use Microsoft cloud-provided protection in Microsoft Defender Antivirus](cloud-protection-microsoft-defender-antivirus.md).</span></span> 

<span data-ttu-id="835a3-122">Pour obtenir la liste des mises à jour récentes de l’intelligence de sécurité, voir Les mises à jour d’intelligence de sécurité pour Antivirus Microsoft Defender logiciel [anti-programme](https://www.microsoft.com/en-us/wdsi/defenderupdates)malveillant Microsoft.</span><span class="sxs-lookup"><span data-stu-id="835a3-122">For a list of recent security intelligence updates, see [Security intelligence updates for Microsoft Defender Antivirus and other Microsoft antimalware](https://www.microsoft.com/en-us/wdsi/defenderupdates).</span></span>

<span data-ttu-id="835a3-123">Les mises à jour du moteur sont incluses dans les mises à jour de l’intelligence de sécurité et sont publiées à une cadence mensuelle.</span><span class="sxs-lookup"><span data-stu-id="835a3-123">Engine updates are included with security intelligence updates and are released on a monthly cadence.</span></span>

## <a name="product-updates"></a><span data-ttu-id="835a3-124">Mises à jour de produit</span><span class="sxs-lookup"><span data-stu-id="835a3-124">Product updates</span></span>

<span data-ttu-id="835a3-125">Antivirus Microsoft Defender nécessite des mises à jour [mensuelles (KB4052623)](https://support.microsoft.com/help/4052623/update-for-windows-defender-antimalware-platform) *(connues* sous le nom de mises à jour de plateforme) et recevra des mises à jour de fonctionnalités majeures avec Windows 10 de publication.</span><span class="sxs-lookup"><span data-stu-id="835a3-125">Microsoft Defender Antivirus requires [monthly updates (KB4052623)](https://support.microsoft.com/help/4052623/update-for-windows-defender-antimalware-platform) (known as *platform updates*), and will receive major feature updates alongside Windows 10 releases.</span></span>

<span data-ttu-id="835a3-126">Vous pouvez gérer la distribution des mises à jour via l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="835a3-126">You can manage the distribution of updates through one of the following methods:</span></span> 

- [<span data-ttu-id="835a3-127">Windows Server Update Service (WSUS)</span><span class="sxs-lookup"><span data-stu-id="835a3-127">Windows Server Update Service (WSUS)</span></span>](/mem/configmgr/protect/deploy-use/endpoint-definitions-wsus#to-synchronize-endpoint-protection-definition-updates-in-standalone-wsus)
- [<span data-ttu-id="835a3-128">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="835a3-128">Microsoft Endpoint Configuration Manager</span></span>](/configmgr/sum/understand/software-updates-introduction)
- <span data-ttu-id="835a3-129">La méthode habituelle que vous utilisez pour déployer Microsoft et Windows mises à jour aux points de terminaison de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="835a3-129">The usual method you use to deploy Microsoft and Windows updates to endpoints in your network.</span></span>

<span data-ttu-id="835a3-130">Pour plus d’informations, [voir Gérer les sources pour les mises à jour Antivirus Microsoft Defender protection des données.](/mem/configmgr/protect/deploy-use/endpoint-definitions-wsus#to-synchronize-endpoint-protection-definition-updates-in-standalone-wsus)</span><span class="sxs-lookup"><span data-stu-id="835a3-130">For more information, see [Manage the sources for Microsoft Defender Antivirus protection updates](/mem/configmgr/protect/deploy-use/endpoint-definitions-wsus#to-synchronize-endpoint-protection-definition-updates-in-standalone-wsus).</span></span>

> [!NOTE]
> <span data-ttu-id="835a3-131">Les mises à jour mensuelles sont publiées par phases, ce qui entraîne la mise à jour de plusieurs packages dans vos services de mise à jour [de serveur Window.](/windows-server/administration/windows-server-update-services/get-started/windows-server-update-services-wsus)</span><span class="sxs-lookup"><span data-stu-id="835a3-131">Monthly updates are released in phases, resulting in multiple packages visible in your [Window Server Update Services](/windows-server/administration/windows-server-update-services/get-started/windows-server-update-services-wsus).</span></span>

## <a name="monthly-platform-and-engine-versions"></a><span data-ttu-id="835a3-132">Versions mensuelles de la plateforme et du moteur</span><span class="sxs-lookup"><span data-stu-id="835a3-132">Monthly platform and engine versions</span></span>

<span data-ttu-id="835a3-133">Pour plus d’informations sur la mise à jour ou l’installation de la mise à jour de la plateforme, voir [Update for Windows Defender antimalware platform](https://support.microsoft.com/help/4052623/update-for-windows-defender-antimalware-platform).</span><span class="sxs-lookup"><span data-stu-id="835a3-133">For information how to update or install the platform update, see [Update for Windows Defender antimalware platform](https://support.microsoft.com/help/4052623/update-for-windows-defender-antimalware-platform).</span></span>

<span data-ttu-id="835a3-134">Toutes nos mises à jour contiennent</span><span class="sxs-lookup"><span data-stu-id="835a3-134">All our updates contain</span></span> 
- <span data-ttu-id="835a3-135">améliorations des performances ;</span><span class="sxs-lookup"><span data-stu-id="835a3-135">performance improvements;</span></span>
- <span data-ttu-id="835a3-136">améliorations de la serviceabilité ; et</span><span class="sxs-lookup"><span data-stu-id="835a3-136">serviceability improvements; and</span></span> 
- <span data-ttu-id="835a3-137">améliorations de l’intégration (Cloud, [Microsoft 365 Defender](/microsoft-365/security/defender/microsoft-365-defender)).</span><span class="sxs-lookup"><span data-stu-id="835a3-137">integration improvements (Cloud, [Microsoft 365 Defender](/microsoft-365/security/defender/microsoft-365-defender)).</span></span>
<br/>
<details>
<summary> <span data-ttu-id="835a3-138">Mai-2021 (plateforme : 4.18.2105.4 | Moteur : 1.1.18200.4)</span><span class="sxs-lookup"><span data-stu-id="835a3-138">May-2021 (Platform: 4.18.2105.4 | Engine: 1.1.18200.4)</span></span></summary>

<span data-ttu-id="835a3-139">&ensp;Version de mise à jour des informations de sécurité **: 1.341.8.0**</span><span class="sxs-lookup"><span data-stu-id="835a3-139">&ensp;Security intelligence update version: **1.341.8.0**</span></span>  
<span data-ttu-id="835a3-140">&ensp;Publication : **4 juin 2021**</span><span class="sxs-lookup"><span data-stu-id="835a3-140">&ensp;Released: **June 4, 2021**</span></span>  
<span data-ttu-id="835a3-141">&ensp;Plateforme : **4.18.2105.4**</span><span class="sxs-lookup"><span data-stu-id="835a3-141">&ensp;Platform: **4.18.2105.4**</span></span>  
<span data-ttu-id="835a3-142">&ensp;Moteur : **1.1.18200.4**</span><span class="sxs-lookup"><span data-stu-id="835a3-142">&ensp;Engine: **1.1.18200.4**</span></span>  
<span data-ttu-id="835a3-143">&ensp;Phase de prise en charge **: Mises à jour critiques et de sécurité**</span><span class="sxs-lookup"><span data-stu-id="835a3-143">&ensp;Support phase: **Security and Critical Updates**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="835a3-144">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="835a3-144">What's new</span></span>
- <span data-ttu-id="835a3-145">Améliorations apportées à la [surveillance du comportement](client-behavioral-blocking.md)</span><span class="sxs-lookup"><span data-stu-id="835a3-145">Improvements to [behavior monitoring](client-behavioral-blocking.md)</span></span> 
- <span data-ttu-id="835a3-146">Fonctionnalité de [filtrage des](network-protection.md) notifications de protection réseau fixe</span><span class="sxs-lookup"><span data-stu-id="835a3-146">Fixed [network protection](network-protection.md) notification filtering feature</span></span>

### <a name="known-issues"></a><span data-ttu-id="835a3-147">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="835a3-147">Known Issues</span></span>
<span data-ttu-id="835a3-148">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="835a3-148">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="835a3-149">Avril-2021 (plateforme : 4.18.2104.14 | Moteur : 1.1.18100.5)</span><span class="sxs-lookup"><span data-stu-id="835a3-149">April-2021 (Platform: 4.18.2104.14 | Engine: 1.1.18100.5)</span></span></summary>

<span data-ttu-id="835a3-150">&ensp;Version de mise à jour des informations de sécurité **: 1.337.2.0**</span><span class="sxs-lookup"><span data-stu-id="835a3-150">&ensp;Security intelligence update version: **1.337.2.0**</span></span>  
<span data-ttu-id="835a3-151">&ensp;Publication : **1er avril 2021**</span><span class="sxs-lookup"><span data-stu-id="835a3-151">&ensp;Released: **April 1, 2021**</span></span>  
<span data-ttu-id="835a3-152">&ensp;Plateforme : **4.18.2104.14**</span><span class="sxs-lookup"><span data-stu-id="835a3-152">&ensp;Platform: **4.18.2104.14**</span></span>  
<span data-ttu-id="835a3-153">&ensp;Moteur : **1.1.18100.5**</span><span class="sxs-lookup"><span data-stu-id="835a3-153">&ensp;Engine: **1.1.18100.5**</span></span>  
<span data-ttu-id="835a3-154">&ensp;Phase de prise en charge **: Mises à jour critiques et de sécurité**</span><span class="sxs-lookup"><span data-stu-id="835a3-154">&ensp;Support phase: **Security and Critical Updates**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="835a3-155">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="835a3-155">What's new</span></span>
- <span data-ttu-id="835a3-156">Logique de surveillance du comportement supplémentaire</span><span class="sxs-lookup"><span data-stu-id="835a3-156">Additional behavior monitoring logic</span></span>
- <span data-ttu-id="835a3-157">Détection améliorée du keylogger en mode noyau</span><span class="sxs-lookup"><span data-stu-id="835a3-157">Improved kernel mode keylogger detection</span></span>
- <span data-ttu-id="835a3-158">Ajout de nouveaux contrôles pour gérer le processus de déploiement progressif pour [les mises à jour de Microsoft Defender](updates.md)</span><span class="sxs-lookup"><span data-stu-id="835a3-158">Added new controls to manage the gradual rollout process for [Microsoft Defender updates](updates.md)</span></span>

### <a name="known-issues"></a><span data-ttu-id="835a3-159">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="835a3-159">Known Issues</span></span>
<span data-ttu-id="835a3-160">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="835a3-160">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="835a3-161">Mars-2021 (plateforme : 4.18.2103.7 | Moteur : 1.1.18000.5)</span><span class="sxs-lookup"><span data-stu-id="835a3-161">March-2021 (Platform: 4.18.2103.7 | Engine: 1.1.18000.5)</span></span></summary>

<span data-ttu-id="835a3-162">&ensp;Version de mise à jour des informations de sécurité **: 1.335.36.0**</span><span class="sxs-lookup"><span data-stu-id="835a3-162">&ensp;Security intelligence update version: **1.335.36.0**</span></span>  
<span data-ttu-id="835a3-163">&ensp;Publication : **1er avril 2021**</span><span class="sxs-lookup"><span data-stu-id="835a3-163">&ensp;Released: **April 1, 2021**</span></span>  
<span data-ttu-id="835a3-164">&ensp;Plateforme : **4.18.2103.7**</span><span class="sxs-lookup"><span data-stu-id="835a3-164">&ensp;Platform: **4.18.2103.7**</span></span>  
<span data-ttu-id="835a3-165">&ensp;Moteur : **1.1.18000.5**</span><span class="sxs-lookup"><span data-stu-id="835a3-165">&ensp;Engine: **1.1.18000.5**</span></span>  
<span data-ttu-id="835a3-166">&ensp;Phase de prise en charge **: Mises à jour critiques et de sécurité**</span><span class="sxs-lookup"><span data-stu-id="835a3-166">&ensp;Support phase: **Security and Critical Updates**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="835a3-167">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="835a3-167">What's new</span></span>

- <span data-ttu-id="835a3-168">Amélioration du moteur d’analyse du comportement</span><span class="sxs-lookup"><span data-stu-id="835a3-168">Improvement to the Behavior Monitoring engine</span></span> 
- <span data-ttu-id="835a3-169">Préventions d’attaques par force brute du réseau étendu</span><span class="sxs-lookup"><span data-stu-id="835a3-169">Expanded network brute-force-attack mitigations</span></span> 
- <span data-ttu-id="835a3-170">Génération d’événements de tentative de falsification en échec supplémentaires lorsque la [protection](prevent-changes-to-security-settings-with-tamper-protection.md) contre la falsification est activée</span><span class="sxs-lookup"><span data-stu-id="835a3-170">Additional failed tampering attempt event generation when [Tamper Protection](prevent-changes-to-security-settings-with-tamper-protection.md) is enabled</span></span>

### <a name="known-issues"></a><span data-ttu-id="835a3-171">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="835a3-171">Known Issues</span></span>
<span data-ttu-id="835a3-172">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="835a3-172">No known issues</span></span>  
<br/>
</details>

### <a name="previous-version-updates-technical-upgrade-support-only"></a><span data-ttu-id="835a3-173">Mises à jour de version précédente : prise en charge de la mise à niveau technique uniquement</span><span class="sxs-lookup"><span data-stu-id="835a3-173">Previous version updates: Technical upgrade support only</span></span>

<span data-ttu-id="835a3-174">Après la publication d’une nouvelle version de package, la prise en charge des deux versions précédentes est réduite au support technique uniquement.</span><span class="sxs-lookup"><span data-stu-id="835a3-174">After a new package version is released, support for the previous two versions is reduced to technical support only.</span></span> <span data-ttu-id="835a3-175">Les versions antérieures à celles répertoriées dans cette section sont fournies uniquement pour la prise en charge de la mise à niveau technique.</span><span class="sxs-lookup"><span data-stu-id="835a3-175">Versions older than that are listed in this section, and are provided for technical upgrade support only.</span></span> 
<br/><br/>
<details>
<summary> <span data-ttu-id="835a3-176">Février-2021 (plateforme : 4.18.2102.3 | Moteur : 1.1.17900.7)</span><span class="sxs-lookup"><span data-stu-id="835a3-176">February-2021 (Platform: 4.18.2102.3 | Engine: 1.1.17900.7)</span></span></summary>

<span data-ttu-id="835a3-177">&ensp;Version de mise à jour des informations de sécurité **: 1.333.7.0**</span><span class="sxs-lookup"><span data-stu-id="835a3-177">&ensp;Security intelligence update version: **1.333.7.0**</span></span>  
<span data-ttu-id="835a3-178">&ensp;Publication : **9 mars 2021**</span><span class="sxs-lookup"><span data-stu-id="835a3-178">&ensp;Released: **March 9, 2021**</span></span>  
<span data-ttu-id="835a3-179">&ensp;Plateforme : **4.18.2102.3**</span><span class="sxs-lookup"><span data-stu-id="835a3-179">&ensp;Platform: **4.18.2102.3**</span></span>  
<span data-ttu-id="835a3-180">&ensp;Moteur : **1.1.17900.7**</span><span class="sxs-lookup"><span data-stu-id="835a3-180">&ensp;Engine: **1.1.17900.7**</span></span>  
<span data-ttu-id="835a3-181">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="835a3-181">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="835a3-182">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="835a3-182">What's new</span></span>

- <span data-ttu-id="835a3-183">Amélioration de la récupération du service par le biais [de la protection contre la falsification](prevent-changes-to-security-settings-with-tamper-protection.md)</span><span class="sxs-lookup"><span data-stu-id="835a3-183">Improved service recovery through [tamper protection](prevent-changes-to-security-settings-with-tamper-protection.md)</span></span>
- <span data-ttu-id="835a3-184">Étendre l’étendue de la protection contre la falsification</span><span class="sxs-lookup"><span data-stu-id="835a3-184">Extend tamper protection scope</span></span>

### <a name="known-issues"></a><span data-ttu-id="835a3-185">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="835a3-185">Known Issues</span></span>
<span data-ttu-id="835a3-186">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="835a3-186">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="835a3-187">Janvier-2021 (plateforme : 4.18.2101.9 | Moteur : 1.1.17800.5)</span><span class="sxs-lookup"><span data-stu-id="835a3-187">January-2021 (Platform: 4.18.2101.9 | Engine: 1.1.17800.5)</span></span></summary>

<span data-ttu-id="835a3-188">&ensp;Version de mise à jour des informations de sécurité **: 1.327.1854.0**</span><span class="sxs-lookup"><span data-stu-id="835a3-188">&ensp;Security intelligence update version: **1.327.1854.0**</span></span>  
<span data-ttu-id="835a3-189">&ensp;Publication : **2 février 2021**</span><span class="sxs-lookup"><span data-stu-id="835a3-189">&ensp;Released: **February 2, 2021**</span></span>  
<span data-ttu-id="835a3-190">&ensp;Plateforme : **4.18.2101.9**</span><span class="sxs-lookup"><span data-stu-id="835a3-190">&ensp;Platform: **4.18.2101.9**</span></span>  
<span data-ttu-id="835a3-191">&ensp;Moteur : **1.1.17800.5**</span><span class="sxs-lookup"><span data-stu-id="835a3-191">&ensp;Engine: **1.1.17800.5**</span></span>  
<span data-ttu-id="835a3-192">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="835a3-192">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="835a3-193">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="835a3-193">What's new</span></span>

- <span data-ttu-id="835a3-194">Améliorations de la détection d’exploits shellcode</span><span class="sxs-lookup"><span data-stu-id="835a3-194">Shellcode exploit detection improvements</span></span>
- <span data-ttu-id="835a3-195">Visibilité accrue des tentatives de vol d’informations d’identification</span><span class="sxs-lookup"><span data-stu-id="835a3-195">Increased visibility for credential stealing attempts</span></span>
- <span data-ttu-id="835a3-196">Améliorations des fonctionnalités antitampering dans Antivirus Microsoft Defender services</span><span class="sxs-lookup"><span data-stu-id="835a3-196">Improvements in antitampering features in Microsoft Defender Antivirus services</span></span>
- <span data-ttu-id="835a3-197">Prise en charge améliorée de l ARM éulation x64</span><span class="sxs-lookup"><span data-stu-id="835a3-197">Improved support for ARM x64 emulation</span></span>
- <span data-ttu-id="835a3-198">Correctif : PEPT notification de blocage reste dans l’historique des menaces après la détection initiale de la protection en temps réel</span><span class="sxs-lookup"><span data-stu-id="835a3-198">Fix: EDR Block notification remains in threat history after real-time protection performed initial detection</span></span>

### <a name="known-issues"></a><span data-ttu-id="835a3-199">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="835a3-199">Known Issues</span></span>
<span data-ttu-id="835a3-200">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="835a3-200">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="835a3-201">Novembre-2020 (plateforme : 4.18.2011.6 | Moteur : 1.1.17700.4)</span><span class="sxs-lookup"><span data-stu-id="835a3-201">November-2020 (Platform: 4.18.2011.6 | Engine: 1.1.17700.4)</span></span></summary>

<span data-ttu-id="835a3-202">&ensp;Version de mise à jour des informations de sécurité **: 1.327.1854.0**</span><span class="sxs-lookup"><span data-stu-id="835a3-202">&ensp;Security intelligence update version: **1.327.1854.0**</span></span>  
<span data-ttu-id="835a3-203">&ensp;Publication : **03 décembre 2020**</span><span class="sxs-lookup"><span data-stu-id="835a3-203">&ensp;Released: **December 03, 2020**</span></span>  
<span data-ttu-id="835a3-204">&ensp;Plateforme : **4.18.2011.6**</span><span class="sxs-lookup"><span data-stu-id="835a3-204">&ensp;Platform: **4.18.2011.6**</span></span>  
<span data-ttu-id="835a3-205">&ensp;Moteur : **1.1.17700.4**</span><span class="sxs-lookup"><span data-stu-id="835a3-205">&ensp;Engine: **1.1.17700.4**</span></span>  
<span data-ttu-id="835a3-206">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="835a3-206">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="835a3-207">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="835a3-207">What's new</span></span>

- <span data-ttu-id="835a3-208">Amélioration de la [journalisation de la prise en](/windows/security/threat-protection/microsoft-defender-smartscreen/microsoft-defender-smartscreen-overview) charge de l’état SmartScreen</span><span class="sxs-lookup"><span data-stu-id="835a3-208">Improved [SmartScreen](/windows/security/threat-protection/microsoft-defender-smartscreen/microsoft-defender-smartscreen-overview) status support logging</span></span>

### <a name="known-issues"></a><span data-ttu-id="835a3-209">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="835a3-209">Known Issues</span></span>
<span data-ttu-id="835a3-210">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="835a3-210">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="835a3-211">Octobre-2020 (plateforme : 4.18.2010.7 | Moteur : 1.1.17600.5)</span><span class="sxs-lookup"><span data-stu-id="835a3-211">October-2020 (Platform: 4.18.2010.7 | Engine: 1.1.17600.5)</span></span></summary>

<span data-ttu-id="835a3-212">&ensp;Version de mise à jour des informations de sécurité **: 1.327.7.0**</span><span class="sxs-lookup"><span data-stu-id="835a3-212">&ensp;Security intelligence update version: **1.327.7.0**</span></span>  
<span data-ttu-id="835a3-213">&ensp;Publication : **29 octobre 2020**</span><span class="sxs-lookup"><span data-stu-id="835a3-213">&ensp;Released: **October 29, 2020**</span></span>  
<span data-ttu-id="835a3-214">&ensp;Plateforme : **4.18.2010.7**</span><span class="sxs-lookup"><span data-stu-id="835a3-214">&ensp;Platform: **4.18.2010.7**</span></span>  
<span data-ttu-id="835a3-215">&ensp;Moteur : **1.1.17600.5**</span><span class="sxs-lookup"><span data-stu-id="835a3-215">&ensp;Engine: **1.1.17600.5**</span></span>  
<span data-ttu-id="835a3-216">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="835a3-216">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="835a3-217">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="835a3-217">What's new</span></span>

- <span data-ttu-id="835a3-218">Nouvelles descriptions pour les catégories de menaces spéciales</span><span class="sxs-lookup"><span data-stu-id="835a3-218">New descriptions for special threat categories</span></span>
- <span data-ttu-id="835a3-219">Fonctionnalités d’émulation améliorées</span><span class="sxs-lookup"><span data-stu-id="835a3-219">Improved emulation capabilities</span></span>
- <span data-ttu-id="835a3-220">Fonctionnalités améliorées d’autoriser/bloquer l’adresse hôte</span><span class="sxs-lookup"><span data-stu-id="835a3-220">Improved host address allow/block capabilities</span></span>
- <span data-ttu-id="835a3-221">Nouvelle option dans le programme CSP Defender pour ignorer la fusion des exclusions des utilisateurs locaux</span><span class="sxs-lookup"><span data-stu-id="835a3-221">New option in Defender CSP to Ignore merging of local user exclusions</span></span>

### <a name="known-issues"></a><span data-ttu-id="835a3-222">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="835a3-222">Known Issues</span></span>

<span data-ttu-id="835a3-223">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="835a3-223">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="835a3-224">Septembre-2020 (plateforme : 4.18.2009.7 | Moteur : 1.1.17500.4)</span><span class="sxs-lookup"><span data-stu-id="835a3-224">September-2020 (Platform: 4.18.2009.7 | Engine: 1.1.17500.4)</span></span></summary>

<span data-ttu-id="835a3-225">&ensp;Version de mise à jour des informations de sécurité **: 1.325.10.0**</span><span class="sxs-lookup"><span data-stu-id="835a3-225">&ensp;Security intelligence update version: **1.325.10.0**</span></span>  
<span data-ttu-id="835a3-226">&ensp;Publication : **01 octobre 2020**</span><span class="sxs-lookup"><span data-stu-id="835a3-226">&ensp;Released: **October 01, 2020**</span></span>  
<span data-ttu-id="835a3-227">&ensp;Plateforme : **4.18.2009.7**</span><span class="sxs-lookup"><span data-stu-id="835a3-227">&ensp;Platform: **4.18.2009.7**</span></span>  
<span data-ttu-id="835a3-228">&ensp;Moteur : **1.1.17500.4**</span><span class="sxs-lookup"><span data-stu-id="835a3-228">&ensp;Engine: **1.1.17500.4**</span></span>  
<span data-ttu-id="835a3-229">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="835a3-229">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="835a3-230">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="835a3-230">What's new</span></span>

- <span data-ttu-id="835a3-231">Des autorisations d’administrateur sont requises pour restaurer les fichiers en quarantaine</span><span class="sxs-lookup"><span data-stu-id="835a3-231">Admin permissions are required to restore files in quarantine</span></span>
- <span data-ttu-id="835a3-232">Les événements au format XML sont désormais pris en charge</span><span class="sxs-lookup"><span data-stu-id="835a3-232">XML formatted events are now supported</span></span>
- <span data-ttu-id="835a3-233">Prise en charge du programme CSP pour ignorer les fusions d’exclusions</span><span class="sxs-lookup"><span data-stu-id="835a3-233">CSP support for ignoring exclusion merges</span></span>
- <span data-ttu-id="835a3-234">Nouvelles interfaces de gestion pour :</span><span class="sxs-lookup"><span data-stu-id="835a3-234">New management interfaces for:</span></span>
   - <span data-ttu-id="835a3-235">UDP Inspection</span><span class="sxs-lookup"><span data-stu-id="835a3-235">UDP Inspection</span></span>
   - <span data-ttu-id="835a3-236">Protection du réseau sur Server 2019</span><span class="sxs-lookup"><span data-stu-id="835a3-236">Network Protection on Server 2019</span></span>
   - <span data-ttu-id="835a3-237">Exclusions d’adresses IP pour la protection du réseau</span><span class="sxs-lookup"><span data-stu-id="835a3-237">IP Address exclusions for Network Protection</span></span>
- <span data-ttu-id="835a3-238">Meilleure visibilité des mesures du TPM</span><span class="sxs-lookup"><span data-stu-id="835a3-238">Improved visibility into TPM measurements</span></span>
- <span data-ttu-id="835a3-239">Amélioration de l Office de module VBA</span><span class="sxs-lookup"><span data-stu-id="835a3-239">Improved Office VBA module scanning</span></span>

### <a name="known-issues"></a><span data-ttu-id="835a3-240">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="835a3-240">Known Issues</span></span>

<span data-ttu-id="835a3-241">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="835a3-241">No known issues</span></span>  
<br/>
</details>
<details>
<summary> <span data-ttu-id="835a3-242">Août-2020 (plateforme : 4.18.2008.9 | Moteur : 1.1.17400.5)</span><span class="sxs-lookup"><span data-stu-id="835a3-242">August-2020 (Platform: 4.18.2008.9 | Engine: 1.1.17400.5)</span></span></summary>

<span data-ttu-id="835a3-243">&ensp;Version de mise à jour des informations de sécurité **: 1.323.9.0**</span><span class="sxs-lookup"><span data-stu-id="835a3-243">&ensp;Security intelligence update version: **1.323.9.0**</span></span>  
<span data-ttu-id="835a3-244">&ensp;Publication : **27 août 2020**</span><span class="sxs-lookup"><span data-stu-id="835a3-244">&ensp;Released: **August 27, 2020**</span></span>  
<span data-ttu-id="835a3-245">&ensp;Plateforme : **4.18.2008.9**</span><span class="sxs-lookup"><span data-stu-id="835a3-245">&ensp;Platform: **4.18.2008.9**</span></span>  
<span data-ttu-id="835a3-246">&ensp;Moteur : **1.1.17400.5**</span><span class="sxs-lookup"><span data-stu-id="835a3-246">&ensp;Engine: **1.1.17400.5**</span></span>  
<span data-ttu-id="835a3-247">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="835a3-247">&ensp;Support phase: **Technical upgrade support (only)**</span></span>

### <a name="whats-new"></a><span data-ttu-id="835a3-248">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="835a3-248">What's new</span></span>

- <span data-ttu-id="835a3-249">Ajouter d’autres événements de télémétrie</span><span class="sxs-lookup"><span data-stu-id="835a3-249">Add more telemetry events</span></span>
- <span data-ttu-id="835a3-250">Télémétrie améliorée des événements d’analyse</span><span class="sxs-lookup"><span data-stu-id="835a3-250">Improved scan event telemetry</span></span>
- <span data-ttu-id="835a3-251">Amélioration de la surveillance du comportement pour les analyses de mémoire</span><span class="sxs-lookup"><span data-stu-id="835a3-251">Improved behavior monitoring for memory scans</span></span>
- <span data-ttu-id="835a3-252">Amélioration de l’analyse des flux de macros</span><span class="sxs-lookup"><span data-stu-id="835a3-252">Improved macro streams scanning</span></span>
- <span data-ttu-id="835a3-253">Ajouté à `AMRunningMode` la Get-MpComputerStatus cmdlet PowerShell</span><span class="sxs-lookup"><span data-stu-id="835a3-253">Added `AMRunningMode` to Get-MpComputerStatus PowerShell cmdlet</span></span>
- <span data-ttu-id="835a3-254">[DisableAntiSpyware](/windows-hardware/customize/desktop/unattend/security-malware-windows-defender-disableantispyware) est ignoré.</span><span class="sxs-lookup"><span data-stu-id="835a3-254">[DisableAntiSpyware](/windows-hardware/customize/desktop/unattend/security-malware-windows-defender-disableantispyware) is ignored.</span></span> <span data-ttu-id="835a3-255">Antivirus Microsoft Defender s’arrête automatiquement lorsqu’il détecte un autre programme antivirus.</span><span class="sxs-lookup"><span data-stu-id="835a3-255">Microsoft Defender Antivirus automatically turns itself off when it detects another antivirus program.</span></span>


### <a name="known-issues"></a><span data-ttu-id="835a3-256">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="835a3-256">Known Issues</span></span>
<span data-ttu-id="835a3-257">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="835a3-257">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="835a3-258">Juillet-2020 (plateforme : 4.18.2007.8 | Moteur : 1.1.17300.4)</span><span class="sxs-lookup"><span data-stu-id="835a3-258">July-2020 (Platform: 4.18.2007.8 | Engine: 1.1.17300.4)</span></span></summary>

<span data-ttu-id="835a3-259">&ensp;Version de mise à jour des informations de sécurité **: 1.321.30.0**</span><span class="sxs-lookup"><span data-stu-id="835a3-259">&ensp;Security intelligence update version: **1.321.30.0**</span></span>  
<span data-ttu-id="835a3-260">&ensp;Publication : **28 juillet 2020**</span><span class="sxs-lookup"><span data-stu-id="835a3-260">&ensp;Released: **July 28, 2020**</span></span>  
<span data-ttu-id="835a3-261">&ensp;Plateforme : **4.18.2007.8**</span><span class="sxs-lookup"><span data-stu-id="835a3-261">&ensp;Platform: **4.18.2007.8**</span></span>  
<span data-ttu-id="835a3-262">&ensp;Moteur : **1.1.17300.4**</span><span class="sxs-lookup"><span data-stu-id="835a3-262">&ensp;Engine: **1.1.17300.4**</span></span>  
<span data-ttu-id="835a3-263">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="835a3-263">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="835a3-264">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="835a3-264">What's new</span></span>

- <span data-ttu-id="835a3-265">Télémétrie améliorée pour BITS</span><span class="sxs-lookup"><span data-stu-id="835a3-265">Improved telemetry for BITS</span></span>
- <span data-ttu-id="835a3-266">Validation améliorée du certificat de signature de code Authenticode</span><span class="sxs-lookup"><span data-stu-id="835a3-266">Improved Authenticode code signing certificate validation</span></span>

### <a name="known-issues"></a><span data-ttu-id="835a3-267">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="835a3-267">Known Issues</span></span>
<span data-ttu-id="835a3-268">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="835a3-268">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="835a3-269">Juin-2020 (plateforme : 4.18.2006.10 | Moteur : 1.1.17200.2)</span><span class="sxs-lookup"><span data-stu-id="835a3-269">June-2020 (Platform: 4.18.2006.10 | Engine: 1.1.17200.2)</span></span></summary>

<span data-ttu-id="835a3-270">&ensp;Version de mise à jour des informations de sécurité **: 1.319.20.0**</span><span class="sxs-lookup"><span data-stu-id="835a3-270">&ensp;Security intelligence update version: **1.319.20.0**</span></span>  
<span data-ttu-id="835a3-271">&ensp;Publication : **22 juin 2020**</span><span class="sxs-lookup"><span data-stu-id="835a3-271">&ensp;Released: **June 22, 2020**</span></span>  
<span data-ttu-id="835a3-272">&ensp;Plateforme : **4.18.2006.10**</span><span class="sxs-lookup"><span data-stu-id="835a3-272">&ensp;Platform: **4.18.2006.10**</span></span>  
<span data-ttu-id="835a3-273">&ensp;Moteur : **1.1.17200.2**</span><span class="sxs-lookup"><span data-stu-id="835a3-273">&ensp;Engine: **1.1.17200.2**</span></span>  
<span data-ttu-id="835a3-274">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="835a3-274">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="835a3-275">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="835a3-275">What's new</span></span>

- <span data-ttu-id="835a3-276">Possibilité de spécifier [l’emplacement des journaux de support](./collect-diagnostic-data.md)</span><span class="sxs-lookup"><span data-stu-id="835a3-276">Possibility to specify the [location of the support logs](./collect-diagnostic-data.md)</span></span>
- <span data-ttu-id="835a3-277">Ignorer l’analyse de rattrapage agressive en mode passif.</span><span class="sxs-lookup"><span data-stu-id="835a3-277">Skipping aggressive catchup scan in Passive mode.</span></span>
- <span data-ttu-id="835a3-278">Autoriser Defender à mettre à jour les connexions avec des compteurs</span><span class="sxs-lookup"><span data-stu-id="835a3-278">Allow Defender to update on metered connections</span></span>
- <span data-ttu-id="835a3-279">Réglage des performances fixes lorsque la mise en cache est désactivée</span><span class="sxs-lookup"><span data-stu-id="835a3-279">Fixed performance tuning when caching is disabled</span></span> 
- <span data-ttu-id="835a3-280">Requête de Registre fixe</span><span class="sxs-lookup"><span data-stu-id="835a3-280">Fixed registry query</span></span> 
- <span data-ttu-id="835a3-281">Randomisation du scantime fixe dans ADMX</span><span class="sxs-lookup"><span data-stu-id="835a3-281">Fixed scantime randomization in ADMX</span></span>

### <a name="known-issues"></a><span data-ttu-id="835a3-282">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="835a3-282">Known Issues</span></span>
<span data-ttu-id="835a3-283">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="835a3-283">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="835a3-284">Mai-2020 (plateforme : 4.18.2005.4 | Moteur : 1.1.17100.2)</span><span class="sxs-lookup"><span data-stu-id="835a3-284">May-2020 (Platform: 4.18.2005.4 | Engine: 1.1.17100.2)</span></span></summary>

<span data-ttu-id="835a3-285">&ensp;Version de mise à jour des informations de sécurité **: 1.317.20.0**</span><span class="sxs-lookup"><span data-stu-id="835a3-285">&ensp;Security intelligence update version: **1.317.20.0**</span></span>  
<span data-ttu-id="835a3-286">&ensp;Publication : **26 mai 2020**</span><span class="sxs-lookup"><span data-stu-id="835a3-286">&ensp;Released: **May 26, 2020**</span></span>  
<span data-ttu-id="835a3-287">&ensp;Plateforme : **4.18.2005.4**</span><span class="sxs-lookup"><span data-stu-id="835a3-287">&ensp;Platform: **4.18.2005.4**</span></span>  
<span data-ttu-id="835a3-288">&ensp;Moteur : **1.1.17100.2**</span><span class="sxs-lookup"><span data-stu-id="835a3-288">&ensp;Engine: **1.1.17100.2**</span></span>  
<span data-ttu-id="835a3-289">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="835a3-289">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="835a3-290">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="835a3-290">What's new</span></span>

- <span data-ttu-id="835a3-291">Enregistrement amélioré pour les événements d’analyse</span><span class="sxs-lookup"><span data-stu-id="835a3-291">Improved logging for scan events</span></span>
- <span data-ttu-id="835a3-292">Amélioration de la gestion des incidents en mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="835a3-292">Improved user mode crash handling.</span></span>
- <span data-ttu-id="835a3-293">Suivi des événements ajouté pour la protection contre la falsification</span><span class="sxs-lookup"><span data-stu-id="835a3-293">Added event tracing for Tamper protection</span></span>
- <span data-ttu-id="835a3-294">Envoi d’exemples AMSI fixes</span><span class="sxs-lookup"><span data-stu-id="835a3-294">Fixed AMSI Sample submission</span></span>
- <span data-ttu-id="835a3-295">Blocage du cloud AMSI fixe</span><span class="sxs-lookup"><span data-stu-id="835a3-295">Fixed AMSI Cloud blocking</span></span>
- <span data-ttu-id="835a3-296">Journal d’installation des mises à jour de sécurité fixes</span><span class="sxs-lookup"><span data-stu-id="835a3-296">Fixed Security update install log</span></span>

### <a name="known-issues"></a><span data-ttu-id="835a3-297">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="835a3-297">Known Issues</span></span>
<span data-ttu-id="835a3-298">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="835a3-298">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="835a3-299">Avril-2020 (plateforme : 4.18.2004.6 | Moteur : 1.1.17000.2)</span><span class="sxs-lookup"><span data-stu-id="835a3-299">April-2020 (Platform: 4.18.2004.6 | Engine: 1.1.17000.2)</span></span></summary>

<span data-ttu-id="835a3-300">&ensp;Version de mise à jour des informations de sécurité **: 1.315.12.0**</span><span class="sxs-lookup"><span data-stu-id="835a3-300">&ensp;Security intelligence update version: **1.315.12.0**</span></span>  
<span data-ttu-id="835a3-301">&ensp;Publication : **30 avril 2020**</span><span class="sxs-lookup"><span data-stu-id="835a3-301">&ensp;Released: **April 30, 2020**</span></span>  
<span data-ttu-id="835a3-302">&ensp;Plateforme : **4.18.2004.6**</span><span class="sxs-lookup"><span data-stu-id="835a3-302">&ensp;Platform: **4.18.2004.6**</span></span>  
<span data-ttu-id="835a3-303">&ensp;Moteur : **1.1.17000.2**</span><span class="sxs-lookup"><span data-stu-id="835a3-303">&ensp;Engine: **1.1.17000.2**</span></span>  
<span data-ttu-id="835a3-304">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="835a3-304">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="835a3-305">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="835a3-305">What's new</span></span>
- <span data-ttu-id="835a3-306">Améliorations apportées aux filtres WDfilter</span><span class="sxs-lookup"><span data-stu-id="835a3-306">WDfilter improvements</span></span>
- <span data-ttu-id="835a3-307">Ajouter des données d’événements actionnables à des événements de détection de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="835a3-307">Add more actionable event data to attack surface reduction detection events</span></span>
- <span data-ttu-id="835a3-308">Informations de version fixes dans les données de diagnostic et WMI</span><span class="sxs-lookup"><span data-stu-id="835a3-308">Fixed version information in diagnostic data and WMI</span></span>
- <span data-ttu-id="835a3-309">Version de plateforme incorrecte corrigée dans l’interface utilisateur après la mise à jour de la plateforme</span><span class="sxs-lookup"><span data-stu-id="835a3-309">Fixed incorrect platform version in UI after platform update</span></span>
- <span data-ttu-id="835a3-310">Intel d’URL dynamique pour la protection contre les menaces sans fichier</span><span class="sxs-lookup"><span data-stu-id="835a3-310">Dynamic URL intel for Fileless threat protection</span></span>
- <span data-ttu-id="835a3-311">Fonctionnalité d’analyse UEFI</span><span class="sxs-lookup"><span data-stu-id="835a3-311">UEFI scan capability</span></span>
- <span data-ttu-id="835a3-312">Étendre la journalisation pour les mises à jour</span><span class="sxs-lookup"><span data-stu-id="835a3-312">Extend logging for updates</span></span>

### <a name="known-issues"></a><span data-ttu-id="835a3-313">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="835a3-313">Known Issues</span></span>
<span data-ttu-id="835a3-314">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="835a3-314">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="835a3-315">Mars-2020 (plateforme : 4.18.2003.8 | Moteur : 1.1.16900.2)</span><span class="sxs-lookup"><span data-stu-id="835a3-315">March-2020 (Platform: 4.18.2003.8 | Engine: 1.1.16900.2)</span></span></summary>

<span data-ttu-id="835a3-316">&ensp;Version de mise à jour des informations de sécurité **: 1.313.8.0**</span><span class="sxs-lookup"><span data-stu-id="835a3-316">&ensp;Security intelligence update version: **1.313.8.0**</span></span>  
<span data-ttu-id="835a3-317">&ensp;Publication : **24 mars 2020**</span><span class="sxs-lookup"><span data-stu-id="835a3-317">&ensp;Released: **March 24, 2020**</span></span>  
<span data-ttu-id="835a3-318">&ensp;Plateforme : **4.18.2003.8**</span><span class="sxs-lookup"><span data-stu-id="835a3-318">&ensp;Platform: **4.18.2003.8**</span></span>  
<span data-ttu-id="835a3-319">&ensp;Moteur : **1.1.16900.4**</span><span class="sxs-lookup"><span data-stu-id="835a3-319">&ensp;Engine: **1.1.16900.4**</span></span>  
<span data-ttu-id="835a3-320">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="835a3-320">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="835a3-321">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="835a3-321">What's new</span></span>

- <span data-ttu-id="835a3-322">Option limitation du processeur ajoutée à [MpCmdRun](./command-line-arguments-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="835a3-322">CPU Throttling option added to [MpCmdRun](./command-line-arguments-microsoft-defender-antivirus.md)</span></span>
- <span data-ttu-id="835a3-323">Améliorer les fonctionnalités de diagnostic</span><span class="sxs-lookup"><span data-stu-id="835a3-323">Improve diagnostic capability</span></span>
- <span data-ttu-id="835a3-324">réduire le délai d’out des informations de sécurité (5 min)</span><span class="sxs-lookup"><span data-stu-id="835a3-324">reduce Security intelligence timeout (5 min)</span></span>
- <span data-ttu-id="835a3-325">Étendre la fonctionnalité de journal interne du moteur AMSI</span><span class="sxs-lookup"><span data-stu-id="835a3-325">Extend AMSI engine internal log capability</span></span>
- <span data-ttu-id="835a3-326">Améliorer la notification pour le blocage des processus</span><span class="sxs-lookup"><span data-stu-id="835a3-326">Improve notification for process blocking</span></span>
   
### <a name="known-issues"></a><span data-ttu-id="835a3-327">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="835a3-327">Known Issues</span></span>
<span data-ttu-id="835a3-328">[**Fixe**] Antivirus Microsoft Defender ignorer les fichiers lors de l’exécution d’une analyse.</span><span class="sxs-lookup"><span data-stu-id="835a3-328">[**Fixed**] Microsoft Defender Antivirus is skipping files when running a scan.</span></span>

<br/>
</details>

<details>

<summary> <span data-ttu-id="835a3-329">Février-2020 (plateforme : - | Moteur : 1.1.16800.2)</span><span class="sxs-lookup"><span data-stu-id="835a3-329">February-2020 (Platform: - | Engine: 1.1.16800.2)</span></span></summary>
  

<span data-ttu-id="835a3-330">&ensp;Version de mise à jour des informations de sécurité **: 1.311.4.0** </span><span class="sxs-lookup"><span data-stu-id="835a3-330">&ensp;Security intelligence update version: **1.311.4.0** </span></span>  
<span data-ttu-id="835a3-331">&ensp;Publication : **25 février 2020**</span><span class="sxs-lookup"><span data-stu-id="835a3-331">&ensp;Released: **February 25, 2020**</span></span>  
<span data-ttu-id="835a3-332">&ensp;Plateforme/Client : **-**</span><span class="sxs-lookup"><span data-stu-id="835a3-332">&ensp;Platform/Client: **-**</span></span>  
<span data-ttu-id="835a3-333">&ensp;Moteur : **1.1.16800.2**</span><span class="sxs-lookup"><span data-stu-id="835a3-333">&ensp;Engine: **1.1.16800.2**</span></span>  
<span data-ttu-id="835a3-334">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="835a3-334">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
     
### <a name="whats-new"></a><span data-ttu-id="835a3-335">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="835a3-335">What's new</span></span>

  
### <a name="known-issues"></a><span data-ttu-id="835a3-336">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="835a3-336">Known Issues</span></span>
<span data-ttu-id="835a3-337">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="835a3-337">No known issues</span></span>
<br/>
</details>

<details>
<summary> <span data-ttu-id="835a3-338">Janvier-2020 (plateforme : 4.18.2001.10 | Moteur : 1.1.16700.2)</span><span class="sxs-lookup"><span data-stu-id="835a3-338">January-2020 (Platform: 4.18.2001.10 | Engine: 1.1.16700.2)</span></span></summary>
  

<span data-ttu-id="835a3-339">Version de mise à jour des informations de sécurité **: 1.309.32.0**</span><span class="sxs-lookup"><span data-stu-id="835a3-339">Security intelligence update version: **1.309.32.0**</span></span>  
<span data-ttu-id="835a3-340">Publication : **30 janvier 2020**</span><span class="sxs-lookup"><span data-stu-id="835a3-340">Released: **January 30, 2020**</span></span>  
<span data-ttu-id="835a3-341">Plateforme/Client : **4.18.2001.10**</span><span class="sxs-lookup"><span data-stu-id="835a3-341">Platform/Client: **4.18.2001.10**</span></span>  
<span data-ttu-id="835a3-342">Moteur : **1.1.16700.2**</span><span class="sxs-lookup"><span data-stu-id="835a3-342">Engine: **1.1.16700.2**</span></span>  
<span data-ttu-id="835a3-343">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="835a3-343">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
     
### <a name="whats-new"></a><span data-ttu-id="835a3-344">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="835a3-344">What's new</span></span>

- <span data-ttu-id="835a3-345">Correction du BSOD sur WS2016 avec Exchange</span><span class="sxs-lookup"><span data-stu-id="835a3-345">Fixed BSOD on WS2016 with Exchange</span></span>
- <span data-ttu-id="835a3-346">Prise en charge des mises à jour de plateforme lorsque le TMP est redirigé vers le chemin d’accès réseau</span><span class="sxs-lookup"><span data-stu-id="835a3-346">Support platform updates when TMP is redirected to network path</span></span>
- <span data-ttu-id="835a3-347">Les versions de plateforme et de moteur sont ajoutées [à WDSI](https://www.microsoft.com/en-us/wdsi/defenderupdates)</span><span class="sxs-lookup"><span data-stu-id="835a3-347">Platform and engine versions are added to [WDSI](https://www.microsoft.com/en-us/wdsi/defenderupdates)</span></span> <!-- The preceding URL must include "/en-us" -->
- <span data-ttu-id="835a3-348">étendre la mise à jour des signatures d’urgence [en mode passif](./microsoft-defender-antivirus-compatibility.md)</span><span class="sxs-lookup"><span data-stu-id="835a3-348">extend Emergency signature update to [passive mode](./microsoft-defender-antivirus-compatibility.md)</span></span>
- <span data-ttu-id="835a3-349">Correction du hang 4.18.1911.3</span><span class="sxs-lookup"><span data-stu-id="835a3-349">Fix 4.18.1911.3 hang</span></span>
   
### <a name="known-issues"></a><span data-ttu-id="835a3-350">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="835a3-350">Known Issues</span></span>

<span data-ttu-id="835a3-351">[**Fixe**] Les appareils utilisant le [mode](/windows-hardware/design/device-experiences/modern-standby) de veille moderne peuvent se bloquer avec le pilote de filtre Windows Defender, ce qui se traduit par un manque de protection.</span><span class="sxs-lookup"><span data-stu-id="835a3-351">[**Fixed**] devices utilizing [modern standby mode](/windows-hardware/design/device-experiences/modern-standby) may experience a hang with the Windows Defender filter driver that results in a gap of protection.</span></span>  <span data-ttu-id="835a3-352">Les ordinateurs concernés semblent ne pas avoir été mis à jour vers la dernière plateforme anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="835a3-352">Affected machines appear to the customer as having not updated to the latest antimalware platform.</span></span>  
<br/>
> [!IMPORTANT]
> <span data-ttu-id="835a3-353">Cette mise à jour est :</span><span class="sxs-lookup"><span data-stu-id="835a3-353">This update is:</span></span>
> - <span data-ttu-id="835a3-354">nécessaire aux appareils RS1 exécutant une version inférieure de la plateforme pour prendre en charge SHA2 ;</span><span class="sxs-lookup"><span data-stu-id="835a3-354">needed by RS1 devices running lower version of the platform to support SHA2;</span></span>
> - <span data-ttu-id="835a3-355">a un indicateur de redémarrage pour les systèmes qui ont des problèmes en suspension ;</span><span class="sxs-lookup"><span data-stu-id="835a3-355">has a reboot flag for systems that have hanging issues;</span></span>
> - <span data-ttu-id="835a3-356">est re-publiée en avril 2020 et ne sera pas recalée par les mises à jour plus nouvelles pour conserver la disponibilité future ;</span><span class="sxs-lookup"><span data-stu-id="835a3-356">is re-released in April 2020 and will not be superseded by newer updates to keep future availability;</span></span>  
> - <span data-ttu-id="835a3-357">est classée en tant que mise à jour en raison de l’exigence de redémarrage ; et</span><span class="sxs-lookup"><span data-stu-id="835a3-357">is categorized as an update due to the reboot requirement; and</span></span>
> - <span data-ttu-id="835a3-358">est uniquement proposée avec [Windows Update](https://support.microsoft.com/help/4027667/windows-10-update).</span><span class="sxs-lookup"><span data-stu-id="835a3-358">is only be offered with [Windows Update](https://support.microsoft.com/help/4027667/windows-10-update).</span></span>
<br/>
</details>

<details>
<summary> <span data-ttu-id="835a3-359">Novembre-2019 (plateforme : 4.18.1911.3 | Moteur : 1.1.16600.7)</span><span class="sxs-lookup"><span data-stu-id="835a3-359">November-2019 (Platform: 4.18.1911.3 | Engine: 1.1.16600.7)</span></span></summary>

<span data-ttu-id="835a3-360">Version de mise à jour des informations de sécurité **: 1.307.13.0**</span><span class="sxs-lookup"><span data-stu-id="835a3-360">Security intelligence update version: **1.307.13.0**</span></span>  
<span data-ttu-id="835a3-361">Publication : **7 décembre 2019**</span><span class="sxs-lookup"><span data-stu-id="835a3-361">Released: **December 7, 2019**</span></span>  
<span data-ttu-id="835a3-362">Plateforme : **4.18.1911.3**</span><span class="sxs-lookup"><span data-stu-id="835a3-362">Platform: **4.18.1911.3**</span></span>  
<span data-ttu-id="835a3-363">Moteur : **1.1.17000.7**</span><span class="sxs-lookup"><span data-stu-id="835a3-363">Engine: **1.1.17000.7**</span></span>  
<span data-ttu-id="835a3-364">Phase de support : **aucune prise en charge**</span><span class="sxs-lookup"><span data-stu-id="835a3-364">Support phase: **No support**</span></span>  
     
### <a name="whats-new"></a><span data-ttu-id="835a3-365">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="835a3-365">What's new</span></span>

- <span data-ttu-id="835a3-366">Niveau de suivi MpCmdRun fixe</span><span class="sxs-lookup"><span data-stu-id="835a3-366">Fixed MpCmdRun tracing level</span></span>
- <span data-ttu-id="835a3-367">Informations de version de WDFilter fixes</span><span class="sxs-lookup"><span data-stu-id="835a3-367">Fixed WDFilter version info</span></span>
- <span data-ttu-id="835a3-368">Améliorer les notifications (PUA)</span><span class="sxs-lookup"><span data-stu-id="835a3-368">Improve notifications (PUA)</span></span>
- <span data-ttu-id="835a3-369">ajouter des journaux MRT pour prendre en charge les fichiers</span><span class="sxs-lookup"><span data-stu-id="835a3-369">add MRT logs to support files</span></span>
   
### <a name="known-issues"></a><span data-ttu-id="835a3-370">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="835a3-370">Known Issues</span></span>
<span data-ttu-id="835a3-371">Lorsque cette mise à jour est installée, l’appareil a besoin du package de saut 4.18.2001.10 pour pouvoir se mettre à jour vers la dernière version de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="835a3-371">When this update is installed, the device needs the jump package 4.18.2001.10 to be able to update to the latest platform version.</span></span>
<br/>
</details>


## <a name="microsoft-defender-antivirus-platform-support"></a><span data-ttu-id="835a3-372">Antivirus Microsoft Defender prise en charge de la plateforme d’Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="835a3-372">Microsoft Defender Antivirus platform support</span></span>
<span data-ttu-id="835a3-373">Les mises à jour de la plateforme et du moteur sont fournies à une cadence mensuelle.</span><span class="sxs-lookup"><span data-stu-id="835a3-373">Platform and engine updates are provided on a monthly cadence.</span></span> <span data-ttu-id="835a3-374">Pour être entièrement pris en charge, tenez à jour les dernières mises à jour de plateforme.</span><span class="sxs-lookup"><span data-stu-id="835a3-374">To be fully supported, keep current with the latest platform updates.</span></span> <span data-ttu-id="835a3-375">Notre structure de support est dynamique et évolue en deux phases en fonction de la disponibilité de la dernière version de plateforme :</span><span class="sxs-lookup"><span data-stu-id="835a3-375">Our support structure is dynamic, evolving into two phases depending on the availability of the latest platform version:</span></span>

- <span data-ttu-id="835a3-376">Phase de maintenance des mises à jour **critiques** et de sécurité : lors de l’exécution de la dernière version de la plateforme, vous serez éligible à la réception des mises à jour de sécurité et critiques sur la plateforme anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="835a3-376">**Security and Critical Updates servicing phase** - When running the latest platform version, you will be eligible to receive both Security and Critical updates to the anti-malware platform.</span></span>
 
- <span data-ttu-id="835a3-377">**Phase de support technique (uniquement)** : après la publication d’une nouvelle version de plateforme, la prise en charge des versions antérieures (N-2) sera réduit au support technique uniquement.</span><span class="sxs-lookup"><span data-stu-id="835a3-377">**Technical Support (Only) phase** - After a new platform version is released, support for older versions (N-2) will reduce to technical support only.</span></span> <span data-ttu-id="835a3-378">Les versions de plateforme antérieures à N-2 ne seront plus pris en charge.\*</span><span class="sxs-lookup"><span data-stu-id="835a3-378">Platform versions older than N-2 will no longer be supported.\*</span></span>

<span data-ttu-id="835a3-379">\*Le support technique continuera d’être fourni pour les mises à niveau de la version Windows 10 (voir la version de plateforme incluse avec [les](#platform-version-included-with-windows-10-releases)versions Windows 10 ) vers la dernière version de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="835a3-379">\* Technical support will continue to be provided for upgrades from the Windows 10 release version (see [Platform version included with Windows 10 releases](#platform-version-included-with-windows-10-releases)) to the latest platform version.</span></span>

<span data-ttu-id="835a3-380">Pendant la phase de support technique (uniquement), les incidents de support commercialement raisonnables sont fournis par le biais du support technique du service clientèle Microsoft & et des offres de support géré de Microsoft (telles que le support Premier).</span><span class="sxs-lookup"><span data-stu-id="835a3-380">During the technical support (only) phase, commercially reasonable support incidents will be provided through Microsoft Customer Service & Support and Microsoft’s managed support offerings (such as Premier Support).</span></span> <span data-ttu-id="835a3-381">Si un incident de support nécessite une escalade vers le développement pour obtenir des conseils supplémentaires, nécessite une mise à jour non de sécurité ou nécessite une mise à jour de sécurité, les clients sont invités à mettre à niveau vers la dernière version de plateforme ou une mise à jour intermédiaire (\*).</span><span class="sxs-lookup"><span data-stu-id="835a3-381">If a support incident requires escalation to development for further guidance, requires a non-security update, or requires a security update, customers will be asked to upgrade to the latest platform version or an intermediate update (\*).</span></span>

### <a name="platform-version-included-with-windows-10-releases"></a><span data-ttu-id="835a3-382">Version de plateforme incluse dans Windows 10 versions</span><span class="sxs-lookup"><span data-stu-id="835a3-382">Platform version included with Windows 10 releases</span></span>
<span data-ttu-id="835a3-383">Le tableau ci-dessous fournit les versions Antivirus Microsoft Defender de plateforme et de moteur qui sont livrées avec les versions les Windows 10 les plus récentes :</span><span class="sxs-lookup"><span data-stu-id="835a3-383">The below table provides the Microsoft Defender Antivirus platform and engine versions that are shipped with the latest Windows 10 releases:</span></span>    

|<span data-ttu-id="835a3-384">Windows 10 version</span><span class="sxs-lookup"><span data-stu-id="835a3-384">Windows 10 release</span></span>  |<span data-ttu-id="835a3-385">Version de la plateforme</span><span class="sxs-lookup"><span data-stu-id="835a3-385">Platform version</span></span>  |<span data-ttu-id="835a3-386">Version du moteur</span><span class="sxs-lookup"><span data-stu-id="835a3-386">Engine version</span></span> |<span data-ttu-id="835a3-387">Phase de prise en charge</span><span class="sxs-lookup"><span data-stu-id="835a3-387">Support phase</span></span> |
|:---|:---|:---|:---|
|<span data-ttu-id="835a3-388">2004 (20H1/20H2)</span><span class="sxs-lookup"><span data-stu-id="835a3-388">2004  (20H1/20H2)</span></span> |<span data-ttu-id="835a3-389">4.18.1909.6</span><span class="sxs-lookup"><span data-stu-id="835a3-389">4.18.1909.6</span></span> |<span data-ttu-id="835a3-390">1.1.17000.2</span><span class="sxs-lookup"><span data-stu-id="835a3-390">1.1.17000.2</span></span> | <span data-ttu-id="835a3-391">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="835a3-391">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="835a3-392">1909 (19H2)</span><span class="sxs-lookup"><span data-stu-id="835a3-392">1909  (19H2)</span></span> |<span data-ttu-id="835a3-393">4.18.1902.5</span><span class="sxs-lookup"><span data-stu-id="835a3-393">4.18.1902.5</span></span> |<span data-ttu-id="835a3-394">1.1.16700.3</span><span class="sxs-lookup"><span data-stu-id="835a3-394">1.1.16700.3</span></span> | <span data-ttu-id="835a3-395">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="835a3-395">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="835a3-396">1903 (19H1)</span><span class="sxs-lookup"><span data-stu-id="835a3-396">1903  (19H1)</span></span> |<span data-ttu-id="835a3-397">4.18.1902.5</span><span class="sxs-lookup"><span data-stu-id="835a3-397">4.18.1902.5</span></span> |<span data-ttu-id="835a3-398">1.1.15600.4</span><span class="sxs-lookup"><span data-stu-id="835a3-398">1.1.15600.4</span></span> | <span data-ttu-id="835a3-399">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="835a3-399">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="835a3-400">1809 (RS5)</span><span class="sxs-lookup"><span data-stu-id="835a3-400">1809  (RS5)</span></span> |<span data-ttu-id="835a3-401">4.18.1807.18075</span><span class="sxs-lookup"><span data-stu-id="835a3-401">4.18.1807.18075</span></span> |<span data-ttu-id="835a3-402">1.1.15000.2</span><span class="sxs-lookup"><span data-stu-id="835a3-402">1.1.15000.2</span></span> | <span data-ttu-id="835a3-403">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="835a3-403">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="835a3-404">1803 (RS4)</span><span class="sxs-lookup"><span data-stu-id="835a3-404">1803  (RS4)</span></span> |<span data-ttu-id="835a3-405">4.13.17134.1</span><span class="sxs-lookup"><span data-stu-id="835a3-405">4.13.17134.1</span></span> |<span data-ttu-id="835a3-406">1.1.14600.4</span><span class="sxs-lookup"><span data-stu-id="835a3-406">1.1.14600.4</span></span> | <span data-ttu-id="835a3-407">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="835a3-407">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="835a3-408">1709 (RS3)</span><span class="sxs-lookup"><span data-stu-id="835a3-408">1709  (RS3)</span></span> |<span data-ttu-id="835a3-409">4.12.16299.15</span><span class="sxs-lookup"><span data-stu-id="835a3-409">4.12.16299.15</span></span> |<span data-ttu-id="835a3-410">1.1.14104.0</span><span class="sxs-lookup"><span data-stu-id="835a3-410">1.1.14104.0</span></span> | <span data-ttu-id="835a3-411">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="835a3-411">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="835a3-412">1703 (RS2)</span><span class="sxs-lookup"><span data-stu-id="835a3-412">1703  (RS2)</span></span> |<span data-ttu-id="835a3-413">4.11.15603.2</span><span class="sxs-lookup"><span data-stu-id="835a3-413">4.11.15603.2</span></span> |<span data-ttu-id="835a3-414">1.1.13504.0</span><span class="sxs-lookup"><span data-stu-id="835a3-414">1.1.13504.0</span></span> | <span data-ttu-id="835a3-415">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="835a3-415">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="835a3-416">1607 (RS1)</span><span class="sxs-lookup"><span data-stu-id="835a3-416">1607 (RS1)</span></span> |<span data-ttu-id="835a3-417">4.10.14393.3683</span><span class="sxs-lookup"><span data-stu-id="835a3-417">4.10.14393.3683</span></span> |<span data-ttu-id="835a3-418">1.1.12805.0</span><span class="sxs-lookup"><span data-stu-id="835a3-418">1.1.12805.0</span></span> | <span data-ttu-id="835a3-419">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="835a3-419">Technical upgrade support (only)</span></span> |  

<span data-ttu-id="835a3-420">Pour Windows 10 de publication, consultez la [Windows de faits sur](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet)le cycle de vie.</span><span class="sxs-lookup"><span data-stu-id="835a3-420">For Windows 10 release information, see the [Windows lifecycle fact sheet](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet).</span></span>

## <a name="updates-for-deployment-image-servicing-and-management-dism"></a><span data-ttu-id="835a3-421">Mises à jour pour la gestion et la maintenance des images de déploiement (DISM)</span><span class="sxs-lookup"><span data-stu-id="835a3-421">Updates for Deployment Image Servicing and Management (DISM)</span></span>

<span data-ttu-id="835a3-422">Nous vous recommandons de mettre à jour vos images d’installation Windows 10 (éditions Enterprise, Pro et Famille), Windows Server 2019 et Windows Server 2016 OS avec les dernières mises à jour antivirus et anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="835a3-422">We recommend updating your Windows 10 (Enterprise, Pro, and Home editions), Windows Server 2019, and Windows Server 2016 OS installation images with the latest antivirus and antimalware updates.</span></span> <span data-ttu-id="835a3-423">La mise à jour de vos images d’installation du système d’exploitation permet d’éviter un écart de protection.</span><span class="sxs-lookup"><span data-stu-id="835a3-423">Keeping your OS installation images up to date helps avoid a gap in protection.</span></span> 

<span data-ttu-id="835a3-424">Pour plus d’informations, voir mise à [jour de Microsoft Defender pour Windows images d’installation du système d’exploitation.](https://support.microsoft.com/help/4568292/defender-update-for-windows-operating-system-installation-images)</span><span class="sxs-lookup"><span data-stu-id="835a3-424">For more information, see [Microsoft Defender update for Windows operating system installation images](https://support.microsoft.com/help/4568292/defender-update-for-windows-operating-system-installation-images).</span></span>

<details>
<summary><span data-ttu-id="835a3-425">1.1.2106.01</span><span class="sxs-lookup"><span data-stu-id="835a3-425">1.1.2106.01</span></span></summary>

<span data-ttu-id="835a3-426">&ensp;Version du package **: 1.1.2106.01**  </span><span class="sxs-lookup"><span data-stu-id="835a3-426">&ensp;Package version: **1.1.2106.01**  </span></span>  
<span data-ttu-id="835a3-427">&ensp;Version de la plateforme **: 4.18.2104.14** </span><span class="sxs-lookup"><span data-stu-id="835a3-427">&ensp;Platform version: **4.18.2104.14** </span></span>  
<span data-ttu-id="835a3-428">&ensp;Version du moteur **: 1.1.18100.6**</span><span class="sxs-lookup"><span data-stu-id="835a3-428">&ensp;Engine version: **1.1.18100.6**</span></span>  
<span data-ttu-id="835a3-429">&ensp;Version de signature **: 1.339.1923.0**</span><span class="sxs-lookup"><span data-stu-id="835a3-429">&ensp;Signature version: **1.339.1923.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="835a3-430">Correctifs</span><span class="sxs-lookup"><span data-stu-id="835a3-430">Fixes</span></span>
- <span data-ttu-id="835a3-431">Aucun</span><span class="sxs-lookup"><span data-stu-id="835a3-431">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="835a3-432">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="835a3-432">Additional information</span></span>
- <span data-ttu-id="835a3-433">Aucun</span><span class="sxs-lookup"><span data-stu-id="835a3-433">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="835a3-434">1.1.2105.01</span><span class="sxs-lookup"><span data-stu-id="835a3-434">1.1.2105.01</span></span></summary>

<span data-ttu-id="835a3-435">&ensp;Version du package **: 1.1.2105.01**  </span><span class="sxs-lookup"><span data-stu-id="835a3-435">&ensp;Package version: **1.1.2105.01**  </span></span>  
<span data-ttu-id="835a3-436">&ensp;Version de la plateforme **: 4.18.2103.7** </span><span class="sxs-lookup"><span data-stu-id="835a3-436">&ensp;Platform version: **4.18.2103.7** </span></span>  
<span data-ttu-id="835a3-437">&ensp;Version du moteur **: 1.1.18100.6**</span><span class="sxs-lookup"><span data-stu-id="835a3-437">&ensp;Engine version: **1.1.18100.6**</span></span>  
<span data-ttu-id="835a3-438">&ensp;Version de signature **: 1.339.42.0**</span><span class="sxs-lookup"><span data-stu-id="835a3-438">&ensp;Signature version: **1.339.42.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="835a3-439">Correctifs</span><span class="sxs-lookup"><span data-stu-id="835a3-439">Fixes</span></span>
- <span data-ttu-id="835a3-440">Aucun</span><span class="sxs-lookup"><span data-stu-id="835a3-440">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="835a3-441">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="835a3-441">Additional information</span></span>
- <span data-ttu-id="835a3-442">Aucun</span><span class="sxs-lookup"><span data-stu-id="835a3-442">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="835a3-443">1.1.2104.01</span><span class="sxs-lookup"><span data-stu-id="835a3-443">1.1.2104.01</span></span></summary>

<span data-ttu-id="835a3-444">&ensp;Version du package **: 1.1.2104.01**  </span><span class="sxs-lookup"><span data-stu-id="835a3-444">&ensp;Package version: **1.1.2104.01**  </span></span>  
<span data-ttu-id="835a3-445">&ensp;Version de plateforme **: 4.18.2102.4** </span><span class="sxs-lookup"><span data-stu-id="835a3-445">&ensp;Platform version: **4.18.2102.4** </span></span>  
<span data-ttu-id="835a3-446">&ensp;Version du moteur **: 1.1.18000.5**</span><span class="sxs-lookup"><span data-stu-id="835a3-446">&ensp;Engine version: **1.1.18000.5**</span></span>  
<span data-ttu-id="835a3-447">&ensp;Version de signature **: 1.335.232.0**</span><span class="sxs-lookup"><span data-stu-id="835a3-447">&ensp;Signature version: **1.335.232.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="835a3-448">Correctifs</span><span class="sxs-lookup"><span data-stu-id="835a3-448">Fixes</span></span>
- <span data-ttu-id="835a3-449">Aucun</span><span class="sxs-lookup"><span data-stu-id="835a3-449">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="835a3-450">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="835a3-450">Additional information</span></span>
- <span data-ttu-id="835a3-451">Aucun</span><span class="sxs-lookup"><span data-stu-id="835a3-451">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="835a3-452">1.1.2103.01</span><span class="sxs-lookup"><span data-stu-id="835a3-452">1.1.2103.01</span></span></summary>

<span data-ttu-id="835a3-453">&ensp;Version du package **: 1.1.2103.01**  </span><span class="sxs-lookup"><span data-stu-id="835a3-453">&ensp;Package version: **1.1.2103.01**  </span></span>  
<span data-ttu-id="835a3-454">&ensp;Version de plateforme **: 4.18.2101.9** </span><span class="sxs-lookup"><span data-stu-id="835a3-454">&ensp;Platform version: **4.18.2101.9** </span></span>  
<span data-ttu-id="835a3-455">&ensp;Version du moteur **: 1.1.17800.5**</span><span class="sxs-lookup"><span data-stu-id="835a3-455">&ensp;Engine version: **1.1.17800.5**</span></span>  
<span data-ttu-id="835a3-456">&ensp;Version de signature **: 1.331.2302.0**</span><span class="sxs-lookup"><span data-stu-id="835a3-456">&ensp;Signature version: **1.331.2302.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="835a3-457">Correctifs</span><span class="sxs-lookup"><span data-stu-id="835a3-457">Fixes</span></span>
- <span data-ttu-id="835a3-458">Aucun</span><span class="sxs-lookup"><span data-stu-id="835a3-458">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="835a3-459">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="835a3-459">Additional information</span></span>
- <span data-ttu-id="835a3-460">Aucun</span><span class="sxs-lookup"><span data-stu-id="835a3-460">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="835a3-461">1.1.2102.03</span><span class="sxs-lookup"><span data-stu-id="835a3-461">1.1.2102.03</span></span></summary>

<span data-ttu-id="835a3-462">&ensp;Version du package **: 1.1.2102.03**  </span><span class="sxs-lookup"><span data-stu-id="835a3-462">&ensp;Package version: **1.1.2102.03**  </span></span>  
<span data-ttu-id="835a3-463">&ensp;Version de la plateforme **: 4.18.2011.6** </span><span class="sxs-lookup"><span data-stu-id="835a3-463">&ensp;Platform version: **4.18.2011.6** </span></span>  
<span data-ttu-id="835a3-464">&ensp;Version du moteur **: 1.1.17800.5**</span><span class="sxs-lookup"><span data-stu-id="835a3-464">&ensp;Engine version: **1.1.17800.5**</span></span>  
<span data-ttu-id="835a3-465">&ensp;Version de signature **: 1.331.174.0**</span><span class="sxs-lookup"><span data-stu-id="835a3-465">&ensp;Signature version: **1.331.174.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="835a3-466">Correctifs</span><span class="sxs-lookup"><span data-stu-id="835a3-466">Fixes</span></span>
- <span data-ttu-id="835a3-467">Aucun</span><span class="sxs-lookup"><span data-stu-id="835a3-467">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="835a3-468">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="835a3-468">Additional information</span></span>
- <span data-ttu-id="835a3-469">Aucun</span><span class="sxs-lookup"><span data-stu-id="835a3-469">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="835a3-470">1.1.2101.02</span><span class="sxs-lookup"><span data-stu-id="835a3-470">1.1.2101.02</span></span></summary>

<span data-ttu-id="835a3-471">&ensp;Version du package **: 1.1.2101.02**  </span><span class="sxs-lookup"><span data-stu-id="835a3-471">&ensp;Package version: **1.1.2101.02**  </span></span>  
<span data-ttu-id="835a3-472">&ensp;Version de la plateforme **: 4.18.2011.6** </span><span class="sxs-lookup"><span data-stu-id="835a3-472">&ensp;Platform version: **4.18.2011.6** </span></span>  
<span data-ttu-id="835a3-473">&ensp;Version du moteur **: 1.1.17700.4**</span><span class="sxs-lookup"><span data-stu-id="835a3-473">&ensp;Engine version: **1.1.17700.4**</span></span>  
<span data-ttu-id="835a3-474">&ensp;Version de signature **: 1.329.1796.0**</span><span class="sxs-lookup"><span data-stu-id="835a3-474">&ensp;Signature version: **1.329.1796.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="835a3-475">Correctifs</span><span class="sxs-lookup"><span data-stu-id="835a3-475">Fixes</span></span>
- <span data-ttu-id="835a3-476">Aucun</span><span class="sxs-lookup"><span data-stu-id="835a3-476">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="835a3-477">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="835a3-477">Additional information</span></span>
- <span data-ttu-id="835a3-478">Aucun</span><span class="sxs-lookup"><span data-stu-id="835a3-478">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="835a3-479">1.1.2012.01</span><span class="sxs-lookup"><span data-stu-id="835a3-479">1.1.2012.01</span></span></summary>

<span data-ttu-id="835a3-480">&ensp;Version du package **: 1.1.2012.01**  </span><span class="sxs-lookup"><span data-stu-id="835a3-480">&ensp;Package version: **1.1.2012.01**  </span></span>  
<span data-ttu-id="835a3-481">&ensp;Version de plateforme **: 4.18.2010.7** </span><span class="sxs-lookup"><span data-stu-id="835a3-481">&ensp;Platform version: **4.18.2010.7** </span></span>  
<span data-ttu-id="835a3-482">&ensp;Version du moteur **: 1.1.17600.5**</span><span class="sxs-lookup"><span data-stu-id="835a3-482">&ensp;Engine version: **1.1.17600.5**</span></span>  
<span data-ttu-id="835a3-483">&ensp;Version de signature **: 1.327.1991.0**</span><span class="sxs-lookup"><span data-stu-id="835a3-483">&ensp;Signature version: **1.327.1991.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="835a3-484">Correctifs</span><span class="sxs-lookup"><span data-stu-id="835a3-484">Fixes</span></span>
- <span data-ttu-id="835a3-485">Aucun</span><span class="sxs-lookup"><span data-stu-id="835a3-485">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="835a3-486">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="835a3-486">Additional information</span></span>
- <span data-ttu-id="835a3-487">Aucun</span><span class="sxs-lookup"><span data-stu-id="835a3-487">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="835a3-488">1.1.2011.02</span><span class="sxs-lookup"><span data-stu-id="835a3-488">1.1.2011.02</span></span></summary>

<span data-ttu-id="835a3-489">&ensp;Version du package **: 1.1.2011.02**  </span><span class="sxs-lookup"><span data-stu-id="835a3-489">&ensp;Package version: **1.1.2011.02**  </span></span>  
<span data-ttu-id="835a3-490">&ensp;Version de plateforme **: 4.18.2010.7** </span><span class="sxs-lookup"><span data-stu-id="835a3-490">&ensp;Platform version: **4.18.2010.7** </span></span>  
<span data-ttu-id="835a3-491">&ensp;Version du moteur **: 1.1.17600.5**</span><span class="sxs-lookup"><span data-stu-id="835a3-491">&ensp;Engine version: **1.1.17600.5**</span></span>  
<span data-ttu-id="835a3-492">&ensp;Version de signature **: 1.327.658.0**</span><span class="sxs-lookup"><span data-stu-id="835a3-492">&ensp;Signature version: **1.327.658.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="835a3-493">Correctifs</span><span class="sxs-lookup"><span data-stu-id="835a3-493">Fixes</span></span>
- <span data-ttu-id="835a3-494">Aucun</span><span class="sxs-lookup"><span data-stu-id="835a3-494">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="835a3-495">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="835a3-495">Additional information</span></span>
- <span data-ttu-id="835a3-496">Signatures Antivirus Microsoft Defender actualisées</span><span class="sxs-lookup"><span data-stu-id="835a3-496">Refreshed Microsoft Defender Antivirus signatures</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="835a3-497">1.1.2011.01</span><span class="sxs-lookup"><span data-stu-id="835a3-497">1.1.2011.01</span></span></summary>

<span data-ttu-id="835a3-498">&ensp;Version du package **: 1.1.2011.01**  </span><span class="sxs-lookup"><span data-stu-id="835a3-498">&ensp;Package version: **1.1.2011.01**  </span></span>  
<span data-ttu-id="835a3-499">&ensp;Version de la plateforme **: 4.18.2009.7**</span><span class="sxs-lookup"><span data-stu-id="835a3-499">&ensp;Platform version: **4.18.2009.7**</span></span>  
<span data-ttu-id="835a3-500">&ensp;Version du moteur **: 1.1.17600.5**</span><span class="sxs-lookup"><span data-stu-id="835a3-500">&ensp;Engine version: **1.1.17600.5**</span></span>  
<span data-ttu-id="835a3-501">&ensp;Version de signature **: 1.327.344.0**</span><span class="sxs-lookup"><span data-stu-id="835a3-501">&ensp;Signature version: **1.327.344.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="835a3-502">Correctifs</span><span class="sxs-lookup"><span data-stu-id="835a3-502">Fixes</span></span>
- <span data-ttu-id="835a3-503">Aucun</span><span class="sxs-lookup"><span data-stu-id="835a3-503">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="835a3-504">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="835a3-504">Additional information</span></span>
- <span data-ttu-id="835a3-505">Aucun</span><span class="sxs-lookup"><span data-stu-id="835a3-505">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="835a3-506">1.1.2009.10</span><span class="sxs-lookup"><span data-stu-id="835a3-506">1.1.2009.10</span></span></summary>

<span data-ttu-id="835a3-507">&ensp;Version du package **: 1.1.2011.01**  </span><span class="sxs-lookup"><span data-stu-id="835a3-507">&ensp;Package version: **1.1.2011.01**  </span></span>  
<span data-ttu-id="835a3-508">&ensp;Version de la plateforme **: 4.18.2008.9** </span><span class="sxs-lookup"><span data-stu-id="835a3-508">&ensp;Platform version: **4.18.2008.9** </span></span>  
<span data-ttu-id="835a3-509">&ensp;Version du moteur **: 1.1.17400.5**</span><span class="sxs-lookup"><span data-stu-id="835a3-509">&ensp;Engine version: **1.1.17400.5**</span></span>  
<span data-ttu-id="835a3-510">&ensp;Version de signature **: 1.327.2216.0**</span><span class="sxs-lookup"><span data-stu-id="835a3-510">&ensp;Signature version: **1.327.2216.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="835a3-511">Correctifs</span><span class="sxs-lookup"><span data-stu-id="835a3-511">Fixes</span></span>
- <span data-ttu-id="835a3-512">Aucun</span><span class="sxs-lookup"><span data-stu-id="835a3-512">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="835a3-513">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="835a3-513">Additional information</span></span>
- <span data-ttu-id="835a3-514">Ajout de la prise en charge Windows 10 images d’installation du système d’exploitation RS1 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="835a3-514">Added support for Windows 10 RS1 or later OS install images.</span></span>  
<br/>
</details>

## <a name="additional-resources"></a><span data-ttu-id="835a3-515">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="835a3-515">Additional resources</span></span>

| <span data-ttu-id="835a3-516">Article</span><span class="sxs-lookup"><span data-stu-id="835a3-516">Article</span></span> | <span data-ttu-id="835a3-517">Description</span><span class="sxs-lookup"><span data-stu-id="835a3-517">Description</span></span>  |
|:---|:---|
|[<span data-ttu-id="835a3-518">Mise à jour de Microsoft Defender Windows images d’installation du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="835a3-518">Microsoft Defender update for Windows operating system installation images</span></span>](https://support.microsoft.com/help/4568292/defender-update-for-windows-operating-system-installation-images)  | <span data-ttu-id="835a3-519">Passer en revue les packages de mise à jour anti-programme malveillant pour vos images d’installation du système d’exploitation (fichiers WIM et VHD).</span><span class="sxs-lookup"><span data-stu-id="835a3-519">Review antimalware update packages for your OS installation images (WIM and VHD files).</span></span> <span data-ttu-id="835a3-520">Obtenez Antivirus Microsoft Defender mises à jour de Windows 10 (éditions Enterprise, Pro et Famille), Windows Server 2019 et Windows Server 2016 images d’installation.</span><span class="sxs-lookup"><span data-stu-id="835a3-520">Get Microsoft Defender Antivirus updates for Windows 10 (Enterprise, Pro, and Home editions), Windows Server 2019, and Windows Server 2016 installation images.</span></span>  |
|[<span data-ttu-id="835a3-521">Gérer le téléchargement et l’application des mises à jour de protection</span><span class="sxs-lookup"><span data-stu-id="835a3-521">Manage how protection updates are downloaded and applied</span></span>](manage-protection-updates-microsoft-defender-antivirus.md) | <span data-ttu-id="835a3-522">Les mises à jour de protection peuvent être mises à jour via de nombreuses sources.</span><span class="sxs-lookup"><span data-stu-id="835a3-522">Protection updates can be delivered through many sources.</span></span> |
|[<span data-ttu-id="835a3-523">Gérer le moment où les mises à jour de protection doivent être téléchargées et appliquées</span><span class="sxs-lookup"><span data-stu-id="835a3-523">Manage when protection updates should be downloaded and applied</span></span>](manage-protection-update-schedule-microsoft-defender-antivirus.md) | <span data-ttu-id="835a3-524">Vous pouvez planifier le téléchargement des mises à jour de la protection.</span><span class="sxs-lookup"><span data-stu-id="835a3-524">You can schedule when protection updates should be downloaded.</span></span> |
|[<span data-ttu-id="835a3-525">Gérer les mises à jour des points de terminaison qui ne sont plus à jour</span><span class="sxs-lookup"><span data-stu-id="835a3-525">Manage updates for endpoints that are out of date</span></span>](manage-outdated-endpoints-microsoft-defender-antivirus.md) | <span data-ttu-id="835a3-526">Si un point de terminaison manque une mise à jour ou une analyse programmée, vous pouvez forcer une mise à jour ou une analyse la prochaine fois qu’un utilisateur se signe.</span><span class="sxs-lookup"><span data-stu-id="835a3-526">If an endpoint misses an update or scheduled scan, you can force an update or scan the next time a user signs in.</span></span> |
|[<span data-ttu-id="835a3-527">Gérer les mises à jour forcées en fonction des événements</span><span class="sxs-lookup"><span data-stu-id="835a3-527">Manage event-based forced updates</span></span>](manage-event-based-updates-microsoft-defender-antivirus.md) | <span data-ttu-id="835a3-528">Vous pouvez définir des mises à jour de protection à télécharger au démarrage ou après certains événements de protection livrés par le cloud.</span><span class="sxs-lookup"><span data-stu-id="835a3-528">You can set protection updates to be downloaded at startup or after certain cloud-delivered protection events.</span></span> |
|[<span data-ttu-id="835a3-529">Gérer les mises à jour pour les appareils mobiles et les machines virtuelles</span><span class="sxs-lookup"><span data-stu-id="835a3-529">Manage updates for mobile devices and virtual machines (VMs)</span></span>](manage-updates-mobile-devices-vms-microsoft-defender-antivirus.md)| <span data-ttu-id="835a3-530">Vous pouvez spécifier des paramètres, par exemple si des mises à jour doivent être mises à jour sur l’alimentation de la batterie, qui sont particulièrement utiles pour les appareils mobiles et les ordinateurs virtuels.</span><span class="sxs-lookup"><span data-stu-id="835a3-530">You can specify settings, such as whether updates should occur on battery power, that are especially useful for mobile devices and virtual machines.</span></span> |
