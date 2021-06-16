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
ms.date: 06/14/2021
ms.openlocfilehash: 1c7ff52398e048aa34fd9c5ab3d8edd1004ea5ec
ms.sourcegitcommit: 3d30ec03628870a22c54b6ec5d865cbe94f34245
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "52929442"
---
# <a name="manage-microsoft-defender-antivirus-updates-and-apply-baselines"></a><span data-ttu-id="f8aaa-104">Gérer les mises Antivirus Microsoft Defender jour et appliquer les lignes de base</span><span class="sxs-lookup"><span data-stu-id="f8aaa-104">Manage Microsoft Defender Antivirus updates and apply baselines</span></span>

<span data-ttu-id="f8aaa-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-105">**Applies to:**</span></span>

- [<span data-ttu-id="f8aaa-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f8aaa-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)
- <span data-ttu-id="f8aaa-107">Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="f8aaa-107">Microsoft Defender Antivirus</span></span>

<span data-ttu-id="f8aaa-108">Le Antivirus Microsoft Defender à jour est essentiel pour garantir que vos appareils disposent des dernières technologies et fonctionnalités nécessaires pour se protéger contre les nouveaux programmes malveillants et les nouvelles techniques d’attaque.</span><span class="sxs-lookup"><span data-stu-id="f8aaa-108">Keeping Microsoft Defender Antivirus up to date is critical to assure your devices have the latest technology and features needed to protect against new malware and attack techniques.</span></span> <span data-ttu-id="f8aaa-109">Veillez à mettre à jour votre protection antivirus, même si Antivirus Microsoft Defender est en cours d’exécution en [mode passif.](microsoft-defender-antivirus-compatibility.md)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-109">Make sure to update your antivirus protection, even if Microsoft Defender Antivirus is running in [passive mode](microsoft-defender-antivirus-compatibility.md).</span></span> <span data-ttu-id="f8aaa-110">Il existe deux types de mises à jour liées au Antivirus Microsoft Defender à jour :</span><span class="sxs-lookup"><span data-stu-id="f8aaa-110">There are two types of updates related to keeping Microsoft Defender Antivirus up to date:</span></span>

- <span data-ttu-id="f8aaa-111">Mises à jour de l’intelligence de la sécurité</span><span class="sxs-lookup"><span data-stu-id="f8aaa-111">Security intelligence updates</span></span>
- <span data-ttu-id="f8aaa-112">Mises à jour de produit</span><span class="sxs-lookup"><span data-stu-id="f8aaa-112">Product updates</span></span>

> [!TIP]
> <span data-ttu-id="f8aaa-113">Pour voir le moteur, la plateforme et la date de signature les plus à jour, consultez les mises à jour de l’intelligence de sécurité pour Antivirus Microsoft Defender logiciel [anti-programme malveillant Microsoft](https://www.microsoft.com/en-us/wdsi/defenderupdates)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-113">To see the most current engine, platform, and signature date, visit the [Security intelligence updates for Microsoft Defender Antivirus and other Microsoft antimalware](https://www.microsoft.com/en-us/wdsi/defenderupdates)</span></span>

## <a name="security-intelligence-updates"></a><span data-ttu-id="f8aaa-114">Mises à jour de l’intelligence de la sécurité</span><span class="sxs-lookup"><span data-stu-id="f8aaa-114">Security intelligence updates</span></span>

<span data-ttu-id="f8aaa-115">Antivirus Microsoft Defender utilise la protection fournie par le [cloud](cloud-protection-microsoft-defender-antivirus.md) (également appelée Microsoft Advanced Protection Service ou MAPS) et télécharge régulièrement les mises à jour de l’intelligence de sécurité pour fournir une protection.</span><span class="sxs-lookup"><span data-stu-id="f8aaa-115">Microsoft Defender Antivirus uses [cloud-delivered protection](cloud-protection-microsoft-defender-antivirus.md) (also called the Microsoft Advanced Protection Service or MAPS) and periodically downloads security intelligence updates to provide protection.</span></span>

> [!NOTE]
> <span data-ttu-id="f8aaa-116">Les mises à jour sont publiées sous les numéros de la Ko ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="f8aaa-116">Updates are released under the below KB numbers:</span></span>  
> - <span data-ttu-id="f8aaa-117">Antivirus Microsoft Defender : KB2267602</span><span class="sxs-lookup"><span data-stu-id="f8aaa-117">Microsoft Defender Antivirus: KB2267602</span></span>  
> - <span data-ttu-id="f8aaa-118">System Center Endpoint Protection : KB2461484</span><span class="sxs-lookup"><span data-stu-id="f8aaa-118">System Center Endpoint Protection: KB2461484</span></span>

<span data-ttu-id="f8aaa-119">La protection cloud est toujours active et nécessite une connexion active à Internet pour fonctionner.</span><span class="sxs-lookup"><span data-stu-id="f8aaa-119">Cloud-delivered protection is always on and requires an active connection to the Internet to function.</span></span> <span data-ttu-id="f8aaa-120">Les mises à jour des informations de sécurité se produisent à une cadence programmée (configurable via une stratégie).</span><span class="sxs-lookup"><span data-stu-id="f8aaa-120">Security intelligence updates occur on a scheduled cadence (configurable via policy).</span></span> <span data-ttu-id="f8aaa-121">Pour plus d’informations, voir Utiliser la protection fournie par le [cloud microsoft dans Antivirus Microsoft Defender](cloud-protection-microsoft-defender-antivirus.md).</span><span class="sxs-lookup"><span data-stu-id="f8aaa-121">For more information, see [Use Microsoft cloud-provided protection in Microsoft Defender Antivirus](cloud-protection-microsoft-defender-antivirus.md).</span></span> 

<span data-ttu-id="f8aaa-122">Pour obtenir la liste des mises à jour récentes de l’intelligence de sécurité, voir Les mises à jour d’intelligence de sécurité pour Antivirus Microsoft Defender logiciel [anti-programme](https://www.microsoft.com/en-us/wdsi/defenderupdates)malveillant Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f8aaa-122">For a list of recent security intelligence updates, see [Security intelligence updates for Microsoft Defender Antivirus and other Microsoft antimalware](https://www.microsoft.com/en-us/wdsi/defenderupdates).</span></span>

<span data-ttu-id="f8aaa-123">Les mises à jour du moteur sont incluses dans les mises à jour de l’intelligence de sécurité et sont publiées à une cadence mensuelle.</span><span class="sxs-lookup"><span data-stu-id="f8aaa-123">Engine updates are included with security intelligence updates and are released on a monthly cadence.</span></span>

## <a name="product-updates"></a><span data-ttu-id="f8aaa-124">Mises à jour de produit</span><span class="sxs-lookup"><span data-stu-id="f8aaa-124">Product updates</span></span>

<span data-ttu-id="f8aaa-125">Antivirus Microsoft Defender nécessite des mises à jour [mensuelles (KB4052623)](https://support.microsoft.com/help/4052623/update-for-windows-defender-antimalware-platform) *(connues* sous le nom de mises à jour de plateforme) et recevra des mises à jour de fonctionnalités majeures avec Windows 10 de publication.</span><span class="sxs-lookup"><span data-stu-id="f8aaa-125">Microsoft Defender Antivirus requires [monthly updates (KB4052623)](https://support.microsoft.com/help/4052623/update-for-windows-defender-antimalware-platform) (known as *platform updates*), and will receive major feature updates alongside Windows 10 releases.</span></span>

<span data-ttu-id="f8aaa-126">Vous pouvez gérer la distribution des mises à jour via l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="f8aaa-126">You can manage the distribution of updates through one of the following methods:</span></span> 

- [<span data-ttu-id="f8aaa-127">Windows Server Update Service (WSUS)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-127">Windows Server Update Service (WSUS)</span></span>](/mem/configmgr/protect/deploy-use/endpoint-definitions-wsus#to-synchronize-endpoint-protection-definition-updates-in-standalone-wsus)
- [<span data-ttu-id="f8aaa-128">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="f8aaa-128">Microsoft Endpoint Configuration Manager</span></span>](/configmgr/sum/understand/software-updates-introduction)
- <span data-ttu-id="f8aaa-129">La méthode habituelle que vous utilisez pour déployer Microsoft et Windows mises à jour aux points de terminaison de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="f8aaa-129">The usual method you use to deploy Microsoft and Windows updates to endpoints in your network.</span></span>

<span data-ttu-id="f8aaa-130">Pour plus d’informations, [voir Gérer les sources pour les mises à jour Antivirus Microsoft Defender protection des données.](/mem/configmgr/protect/deploy-use/endpoint-definitions-wsus#to-synchronize-endpoint-protection-definition-updates-in-standalone-wsus)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-130">For more information, see [Manage the sources for Microsoft Defender Antivirus protection updates](/mem/configmgr/protect/deploy-use/endpoint-definitions-wsus#to-synchronize-endpoint-protection-definition-updates-in-standalone-wsus).</span></span>

> [!NOTE]
> <span data-ttu-id="f8aaa-131">Les mises à jour mensuelles sont publiées par phases, ce qui entraîne la mise à jour de plusieurs packages dans vos services de mise à jour [de serveur Window.](/windows-server/administration/windows-server-update-services/get-started/windows-server-update-services-wsus)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-131">Monthly updates are released in phases, resulting in multiple packages visible in your [Window Server Update Services](/windows-server/administration/windows-server-update-services/get-started/windows-server-update-services-wsus).</span></span>

## <a name="monthly-platform-and-engine-versions"></a><span data-ttu-id="f8aaa-132">Versions mensuelles de la plateforme et du moteur</span><span class="sxs-lookup"><span data-stu-id="f8aaa-132">Monthly platform and engine versions</span></span>

<span data-ttu-id="f8aaa-133">Pour plus d’informations sur la mise à jour ou l’installation de la mise à jour de plateforme, voir Mise à [jour Windows Defender plateforme anti-programme malveillant.](https://support.microsoft.com/help/4052623/update-for-windows-defender-antimalware-platform)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-133">For information how to update or install the platform update, see [Update for Windows Defender antimalware platform](https://support.microsoft.com/help/4052623/update-for-windows-defender-antimalware-platform).</span></span>

<span data-ttu-id="f8aaa-134">Toutes nos mises à jour contiennent</span><span class="sxs-lookup"><span data-stu-id="f8aaa-134">All our updates contain</span></span> 
- <span data-ttu-id="f8aaa-135">améliorations des performances ;</span><span class="sxs-lookup"><span data-stu-id="f8aaa-135">performance improvements;</span></span>
- <span data-ttu-id="f8aaa-136">améliorations en matière de serviceabilité ; et</span><span class="sxs-lookup"><span data-stu-id="f8aaa-136">serviceability improvements; and</span></span> 
- <span data-ttu-id="f8aaa-137">améliorations de l’intégration (Cloud, [Microsoft 365 Defender](/microsoft-365/security/defender/microsoft-365-defender)).</span><span class="sxs-lookup"><span data-stu-id="f8aaa-137">integration improvements (Cloud, [Microsoft 365 Defender](/microsoft-365/security/defender/microsoft-365-defender)).</span></span>
<br/><br/>
<details>
<summary> <span data-ttu-id="f8aaa-138">Mai-2021 (plateforme : 4.18.2105.4 | Moteur : 1.1.18200.4)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-138">May-2021 (Platform: 4.18.2105.4 | Engine: 1.1.18200.4)</span></span></summary>

<span data-ttu-id="f8aaa-139">&ensp;Version de mise à jour des informations de sécurité **: 1.341.8.0**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-139">&ensp;Security intelligence update version: **1.341.8.0**</span></span>  
<span data-ttu-id="f8aaa-140">&ensp;Publication : **3 juin 2021**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-140">&ensp;Released: **June 3, 2021**</span></span>  
<span data-ttu-id="f8aaa-141">&ensp;Plateforme : **4.18.2105.4**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-141">&ensp;Platform: **4.18.2105.4**</span></span>  
<span data-ttu-id="f8aaa-142">&ensp;Moteur : **1.1.18200.4**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-142">&ensp;Engine: **1.1.18200.4**</span></span>  
<span data-ttu-id="f8aaa-143">&ensp;Phase de prise en charge **: Mises à jour critiques et de sécurité**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-143">&ensp;Support phase: **Security and Critical Updates**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="f8aaa-144">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="f8aaa-144">What's new</span></span>
- <span data-ttu-id="f8aaa-145">Améliorations apportées à la [surveillance du comportement](client-behavioral-blocking.md)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-145">Improvements to [behavior monitoring](client-behavioral-blocking.md)</span></span> 
- <span data-ttu-id="f8aaa-146">Fonctionnalité de [filtrage des](network-protection.md) notifications de protection réseau fixe</span><span class="sxs-lookup"><span data-stu-id="f8aaa-146">Fixed [network protection](network-protection.md) notification filtering feature</span></span>

### <a name="known-issues"></a><span data-ttu-id="f8aaa-147">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="f8aaa-147">Known Issues</span></span>
<span data-ttu-id="f8aaa-148">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="f8aaa-148">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="f8aaa-149">Avril-2021 (plateforme : 4.18.2104.14 | Moteur : 1.1.18100.5)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-149">April-2021 (Platform: 4.18.2104.14 | Engine: 1.1.18100.5)</span></span></summary>

<span data-ttu-id="f8aaa-150">&ensp;Version de mise à jour des informations de sécurité **: 1.337.2.0**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-150">&ensp;Security intelligence update version: **1.337.2.0**</span></span>  
<span data-ttu-id="f8aaa-151">&ensp;Publication : **26 avril 2021**  (moteur : 1.1.18100.6 publié le 5 mai 2021) Plateforme : &ensp; **4.18.2104.14**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-151">&ensp;Released: **April 26, 2021**  (Engine: 1.1.18100.6 released May 5, 2021) &ensp;Platform: **4.18.2104.14**</span></span>  
<span data-ttu-id="f8aaa-152">&ensp;Moteur : **1.1.18100.5**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-152">&ensp;Engine: **1.1.18100.5**</span></span>  
<span data-ttu-id="f8aaa-153">&ensp;Phase de prise en charge **: Mises à jour critiques et de sécurité**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-153">&ensp;Support phase: **Security and Critical Updates**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="f8aaa-154">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="f8aaa-154">What's new</span></span>
- <span data-ttu-id="f8aaa-155">Logique de surveillance du comportement supplémentaire</span><span class="sxs-lookup"><span data-stu-id="f8aaa-155">Additional behavior monitoring logic</span></span>
- <span data-ttu-id="f8aaa-156">Détection améliorée du keylogger en mode noyau</span><span class="sxs-lookup"><span data-stu-id="f8aaa-156">Improved kernel mode keylogger detection</span></span>

### <a name="known-issues"></a><span data-ttu-id="f8aaa-157">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="f8aaa-157">Known Issues</span></span>
<span data-ttu-id="f8aaa-158">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="f8aaa-158">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="f8aaa-159">Mars-2021 (plateforme : 4.18.2103.7 | Moteur : 1.1.18000.5)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-159">March-2021 (Platform: 4.18.2103.7 | Engine: 1.1.18000.5)</span></span></summary>

<span data-ttu-id="f8aaa-160">&ensp;Version de mise à jour des informations de sécurité **: 1.335.36.0**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-160">&ensp;Security intelligence update version: **1.335.36.0**</span></span>  
<span data-ttu-id="f8aaa-161">&ensp;Publication : **2 avril 2021**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-161">&ensp;Released: **April 2, 2021**</span></span>  
<span data-ttu-id="f8aaa-162">&ensp;Plateforme : **4.18.2103.7**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-162">&ensp;Platform: **4.18.2103.7**</span></span>  
<span data-ttu-id="f8aaa-163">&ensp;Moteur : **1.1.18000.5**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-163">&ensp;Engine: **1.1.18000.5**</span></span>  
<span data-ttu-id="f8aaa-164">&ensp;Phase de prise en charge **: Mises à jour critiques et de sécurité**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-164">&ensp;Support phase: **Security and Critical Updates**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="f8aaa-165">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="f8aaa-165">What's new</span></span>

- <span data-ttu-id="f8aaa-166">Amélioration du moteur d’analyse du comportement</span><span class="sxs-lookup"><span data-stu-id="f8aaa-166">Improvement to the Behavior Monitoring engine</span></span> 
- <span data-ttu-id="f8aaa-167">Préventions d’attaques par force brute du réseau étendu</span><span class="sxs-lookup"><span data-stu-id="f8aaa-167">Expanded network brute-force-attack mitigations</span></span> 
- <span data-ttu-id="f8aaa-168">Génération d’événements de tentative de falsification en échec supplémentaires lorsque la [protection](prevent-changes-to-security-settings-with-tamper-protection.md) contre la falsification est activée</span><span class="sxs-lookup"><span data-stu-id="f8aaa-168">Additional failed tampering attempt event generation when [Tamper Protection](prevent-changes-to-security-settings-with-tamper-protection.md) is enabled</span></span>

### <a name="known-issues"></a><span data-ttu-id="f8aaa-169">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="f8aaa-169">Known Issues</span></span>
<span data-ttu-id="f8aaa-170">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="f8aaa-170">No known issues</span></span>  
<br/>
</details>

### <a name="previous-version-updates-technical-upgrade-support-only"></a><span data-ttu-id="f8aaa-171">Mises à jour de version précédente : prise en charge de la mise à niveau technique uniquement</span><span class="sxs-lookup"><span data-stu-id="f8aaa-171">Previous version updates: Technical upgrade support only</span></span>

<span data-ttu-id="f8aaa-172">Après la publication d’une nouvelle version de package, la prise en charge des deux versions précédentes est réduite au support technique uniquement.</span><span class="sxs-lookup"><span data-stu-id="f8aaa-172">After a new package version is released, support for the previous two versions is reduced to technical support only.</span></span> <span data-ttu-id="f8aaa-173">Les versions antérieures à celles répertoriées dans cette section sont fournies uniquement pour la prise en charge de la mise à niveau technique.</span><span class="sxs-lookup"><span data-stu-id="f8aaa-173">Versions older than that are listed in this section, and are provided for technical upgrade support only.</span></span> 
<br/><br/>
<details>
<summary> <span data-ttu-id="f8aaa-174">Février-2021 (plateforme : 4.18.2102.3 | Moteur : 1.1.17900.7)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-174">February-2021 (Platform: 4.18.2102.3 | Engine: 1.1.17900.7)</span></span></summary>

<span data-ttu-id="f8aaa-175">&ensp;Version de mise à jour des informations de sécurité **: 1.333.7.0**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-175">&ensp;Security intelligence update version: **1.333.7.0**</span></span>  
<span data-ttu-id="f8aaa-176">&ensp;Publication : **9 mars 2021**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-176">&ensp;Released: **March 9, 2021**</span></span>  
<span data-ttu-id="f8aaa-177">&ensp;Plateforme : **4.18.2102.3**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-177">&ensp;Platform: **4.18.2102.3**</span></span>  
<span data-ttu-id="f8aaa-178">&ensp;Moteur : **1.1.17900.7**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-178">&ensp;Engine: **1.1.17900.7**</span></span>  
<span data-ttu-id="f8aaa-179">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-179">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="f8aaa-180">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="f8aaa-180">What's new</span></span>

- <span data-ttu-id="f8aaa-181">Amélioration de la récupération du service par le biais [de la protection contre la falsification](prevent-changes-to-security-settings-with-tamper-protection.md)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-181">Improved service recovery through [tamper protection](prevent-changes-to-security-settings-with-tamper-protection.md)</span></span>
- <span data-ttu-id="f8aaa-182">Étendre l’étendue de la protection contre la falsification</span><span class="sxs-lookup"><span data-stu-id="f8aaa-182">Extend tamper protection scope</span></span>

### <a name="known-issues"></a><span data-ttu-id="f8aaa-183">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="f8aaa-183">Known Issues</span></span>
<span data-ttu-id="f8aaa-184">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="f8aaa-184">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="f8aaa-185">Janvier-2021 (plateforme : 4.18.2101.9 | Moteur : 1.1.17800.5)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-185">January-2021 (Platform: 4.18.2101.9 | Engine: 1.1.17800.5)</span></span></summary>

<span data-ttu-id="f8aaa-186">&ensp;Version de mise à jour des informations de sécurité **: 1.327.1854.0**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-186">&ensp;Security intelligence update version: **1.327.1854.0**</span></span>  
<span data-ttu-id="f8aaa-187">&ensp;Publication : **2 février 2021**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-187">&ensp;Released: **February 2, 2021**</span></span>  
<span data-ttu-id="f8aaa-188">&ensp;Plateforme : **4.18.2101.9**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-188">&ensp;Platform: **4.18.2101.9**</span></span>  
<span data-ttu-id="f8aaa-189">&ensp;Moteur : **1.1.17800.5**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-189">&ensp;Engine: **1.1.17800.5**</span></span>  
<span data-ttu-id="f8aaa-190">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-190">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="f8aaa-191">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="f8aaa-191">What's new</span></span>

- <span data-ttu-id="f8aaa-192">Améliorations de la détection d’exploits shellcode</span><span class="sxs-lookup"><span data-stu-id="f8aaa-192">Shellcode exploit detection improvements</span></span>
- <span data-ttu-id="f8aaa-193">Visibilité accrue des tentatives de vol d’informations d’identification</span><span class="sxs-lookup"><span data-stu-id="f8aaa-193">Increased visibility for credential stealing attempts</span></span>
- <span data-ttu-id="f8aaa-194">Améliorations des fonctionnalités antitampering dans Antivirus Microsoft Defender services</span><span class="sxs-lookup"><span data-stu-id="f8aaa-194">Improvements in antitampering features in Microsoft Defender Antivirus services</span></span>
- <span data-ttu-id="f8aaa-195">Prise en charge améliorée de l ARM éulation x64</span><span class="sxs-lookup"><span data-stu-id="f8aaa-195">Improved support for ARM x64 emulation</span></span>
- <span data-ttu-id="f8aaa-196">Correctif : PEPT notification de blocage reste dans l’historique des menaces après la détection initiale de la protection en temps réel</span><span class="sxs-lookup"><span data-stu-id="f8aaa-196">Fix: EDR Block notification remains in threat history after real-time protection performed initial detection</span></span>

### <a name="known-issues"></a><span data-ttu-id="f8aaa-197">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="f8aaa-197">Known Issues</span></span>
<span data-ttu-id="f8aaa-198">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="f8aaa-198">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="f8aaa-199">Novembre-2020 (plateforme : 4.18.2011.6 | Moteur : 1.1.17700.4)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-199">November-2020 (Platform: 4.18.2011.6 | Engine: 1.1.17700.4)</span></span></summary>

<span data-ttu-id="f8aaa-200">&ensp;Version de mise à jour des informations de sécurité **: 1.327.1854.0**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-200">&ensp;Security intelligence update version: **1.327.1854.0**</span></span>  
<span data-ttu-id="f8aaa-201">&ensp;Publication : **03 décembre 2020**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-201">&ensp;Released: **December 03, 2020**</span></span>  
<span data-ttu-id="f8aaa-202">&ensp;Plateforme : **4.18.2011.6**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-202">&ensp;Platform: **4.18.2011.6**</span></span>  
<span data-ttu-id="f8aaa-203">&ensp;Moteur : **1.1.17700.4**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-203">&ensp;Engine: **1.1.17700.4**</span></span>  
<span data-ttu-id="f8aaa-204">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-204">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="f8aaa-205">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="f8aaa-205">What's new</span></span>

- <span data-ttu-id="f8aaa-206">Amélioration de la [journalisation de la prise en](/windows/security/threat-protection/microsoft-defender-smartscreen/microsoft-defender-smartscreen-overview) charge de l’état SmartScreen</span><span class="sxs-lookup"><span data-stu-id="f8aaa-206">Improved [SmartScreen](/windows/security/threat-protection/microsoft-defender-smartscreen/microsoft-defender-smartscreen-overview) status support logging</span></span>

### <a name="known-issues"></a><span data-ttu-id="f8aaa-207">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="f8aaa-207">Known Issues</span></span>
<span data-ttu-id="f8aaa-208">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="f8aaa-208">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="f8aaa-209">Octobre-2020 (plateforme : 4.18.2010.7 | Moteur : 1.1.17600.5)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-209">October-2020 (Platform: 4.18.2010.7 | Engine: 1.1.17600.5)</span></span></summary>

<span data-ttu-id="f8aaa-210">&ensp;Version de mise à jour des informations de sécurité **: 1.327.7.0**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-210">&ensp;Security intelligence update version: **1.327.7.0**</span></span>  
<span data-ttu-id="f8aaa-211">&ensp;Publication : **29 octobre 2020**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-211">&ensp;Released: **October 29, 2020**</span></span>  
<span data-ttu-id="f8aaa-212">&ensp;Plateforme : **4.18.2010.7**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-212">&ensp;Platform: **4.18.2010.7**</span></span>  
<span data-ttu-id="f8aaa-213">&ensp;Moteur : **1.1.17600.5**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-213">&ensp;Engine: **1.1.17600.5**</span></span>  
<span data-ttu-id="f8aaa-214">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-214">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="f8aaa-215">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="f8aaa-215">What's new</span></span>

- <span data-ttu-id="f8aaa-216">Nouvelles descriptions pour les catégories de menaces spéciales</span><span class="sxs-lookup"><span data-stu-id="f8aaa-216">New descriptions for special threat categories</span></span>
- <span data-ttu-id="f8aaa-217">Fonctionnalités d’émulation améliorées</span><span class="sxs-lookup"><span data-stu-id="f8aaa-217">Improved emulation capabilities</span></span>
- <span data-ttu-id="f8aaa-218">Fonctionnalités améliorées d’autoriser/de bloquer l’adresse hôte</span><span class="sxs-lookup"><span data-stu-id="f8aaa-218">Improved host address allow/block capabilities</span></span>
- <span data-ttu-id="f8aaa-219">Nouvelle option dans le programme CSP Defender pour ignorer la fusion des exclusions des utilisateurs locaux</span><span class="sxs-lookup"><span data-stu-id="f8aaa-219">New option in Defender CSP to Ignore merging of local user exclusions</span></span>

### <a name="known-issues"></a><span data-ttu-id="f8aaa-220">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="f8aaa-220">Known Issues</span></span>

<span data-ttu-id="f8aaa-221">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="f8aaa-221">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="f8aaa-222">Septembre-2020 (plateforme : 4.18.2009.7 | Moteur : 1.1.17500.4)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-222">September-2020 (Platform: 4.18.2009.7 | Engine: 1.1.17500.4)</span></span></summary>

<span data-ttu-id="f8aaa-223">&ensp;Version de mise à jour des informations de sécurité **: 1.325.10.0**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-223">&ensp;Security intelligence update version: **1.325.10.0**</span></span>  
<span data-ttu-id="f8aaa-224">&ensp;Publication : **01 octobre 2020**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-224">&ensp;Released: **October 01, 2020**</span></span>  
<span data-ttu-id="f8aaa-225">&ensp;Plateforme : **4.18.2009.7**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-225">&ensp;Platform: **4.18.2009.7**</span></span>  
<span data-ttu-id="f8aaa-226">&ensp;Moteur : **1.1.17500.4**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-226">&ensp;Engine: **1.1.17500.4**</span></span>  
<span data-ttu-id="f8aaa-227">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-227">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="f8aaa-228">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="f8aaa-228">What's new</span></span>

- <span data-ttu-id="f8aaa-229">Des autorisations d’administrateur sont requises pour restaurer les fichiers en quarantaine</span><span class="sxs-lookup"><span data-stu-id="f8aaa-229">Admin permissions are required to restore files in quarantine</span></span>
- <span data-ttu-id="f8aaa-230">Les événements au format XML sont désormais pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8aaa-230">XML formatted events are now supported</span></span>
- <span data-ttu-id="f8aaa-231">Prise en charge du programme CSP pour ignorer les fusions d’exclusions</span><span class="sxs-lookup"><span data-stu-id="f8aaa-231">CSP support for ignoring exclusion merges</span></span>
- <span data-ttu-id="f8aaa-232">Nouvelles interfaces de gestion pour :</span><span class="sxs-lookup"><span data-stu-id="f8aaa-232">New management interfaces for:</span></span>
   - <span data-ttu-id="f8aaa-233">UDP Inspection</span><span class="sxs-lookup"><span data-stu-id="f8aaa-233">UDP Inspection</span></span>
   - <span data-ttu-id="f8aaa-234">Protection du réseau sur Server 2019</span><span class="sxs-lookup"><span data-stu-id="f8aaa-234">Network Protection on Server 2019</span></span>
   - <span data-ttu-id="f8aaa-235">Exclusions d’adresses IP pour la protection du réseau</span><span class="sxs-lookup"><span data-stu-id="f8aaa-235">IP Address exclusions for Network Protection</span></span>
- <span data-ttu-id="f8aaa-236">Meilleure visibilité des mesures du TPM</span><span class="sxs-lookup"><span data-stu-id="f8aaa-236">Improved visibility into TPM measurements</span></span>
- <span data-ttu-id="f8aaa-237">Amélioration de l Office de module VBA</span><span class="sxs-lookup"><span data-stu-id="f8aaa-237">Improved Office VBA module scanning</span></span>

### <a name="known-issues"></a><span data-ttu-id="f8aaa-238">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="f8aaa-238">Known Issues</span></span>

<span data-ttu-id="f8aaa-239">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="f8aaa-239">No known issues</span></span>  
<br/>
</details>
<details>
<summary> <span data-ttu-id="f8aaa-240">Août-2020 (plateforme : 4.18.2008.9 | Moteur : 1.1.17400.5)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-240">August-2020 (Platform: 4.18.2008.9 | Engine: 1.1.17400.5)</span></span></summary>

<span data-ttu-id="f8aaa-241">&ensp;Version de mise à jour des informations de sécurité **: 1.323.9.0**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-241">&ensp;Security intelligence update version: **1.323.9.0**</span></span>  
<span data-ttu-id="f8aaa-242">&ensp;Publication : **27 août 2020**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-242">&ensp;Released: **August 27, 2020**</span></span>  
<span data-ttu-id="f8aaa-243">&ensp;Plateforme : **4.18.2008.9**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-243">&ensp;Platform: **4.18.2008.9**</span></span>  
<span data-ttu-id="f8aaa-244">&ensp;Moteur : **1.1.17400.5**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-244">&ensp;Engine: **1.1.17400.5**</span></span>  
<span data-ttu-id="f8aaa-245">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-245">&ensp;Support phase: **Technical upgrade support (only)**</span></span>

### <a name="whats-new"></a><span data-ttu-id="f8aaa-246">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="f8aaa-246">What's new</span></span>

- <span data-ttu-id="f8aaa-247">Ajouter d’autres événements de télémétrie</span><span class="sxs-lookup"><span data-stu-id="f8aaa-247">Add more telemetry events</span></span>
- <span data-ttu-id="f8aaa-248">Télémétrie améliorée des événements d’analyse</span><span class="sxs-lookup"><span data-stu-id="f8aaa-248">Improved scan event telemetry</span></span>
- <span data-ttu-id="f8aaa-249">Amélioration de la surveillance du comportement pour les analyses de mémoire</span><span class="sxs-lookup"><span data-stu-id="f8aaa-249">Improved behavior monitoring for memory scans</span></span>
- <span data-ttu-id="f8aaa-250">Amélioration de l’analyse des flux de macros</span><span class="sxs-lookup"><span data-stu-id="f8aaa-250">Improved macro streams scanning</span></span>
- <span data-ttu-id="f8aaa-251">Ajouté à `AMRunningMode` la Get-MpComputerStatus cmdlet PowerShell</span><span class="sxs-lookup"><span data-stu-id="f8aaa-251">Added `AMRunningMode` to Get-MpComputerStatus PowerShell cmdlet</span></span>
- <span data-ttu-id="f8aaa-252">[DisableAntiSpyware](/windows-hardware/customize/desktop/unattend/security-malware-windows-defender-disableantispyware) est ignoré.</span><span class="sxs-lookup"><span data-stu-id="f8aaa-252">[DisableAntiSpyware](/windows-hardware/customize/desktop/unattend/security-malware-windows-defender-disableantispyware) is ignored.</span></span> <span data-ttu-id="f8aaa-253">Antivirus Microsoft Defender s’arrête automatiquement lorsqu’il détecte un autre programme antivirus.</span><span class="sxs-lookup"><span data-stu-id="f8aaa-253">Microsoft Defender Antivirus automatically turns itself off when it detects another antivirus program.</span></span>


### <a name="known-issues"></a><span data-ttu-id="f8aaa-254">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="f8aaa-254">Known Issues</span></span>
<span data-ttu-id="f8aaa-255">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="f8aaa-255">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="f8aaa-256">Juillet-2020 (plateforme : 4.18.2007.8 | Moteur : 1.1.17300.4)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-256">July-2020 (Platform: 4.18.2007.8 | Engine: 1.1.17300.4)</span></span></summary>

<span data-ttu-id="f8aaa-257">&ensp;Version de mise à jour des informations de sécurité **: 1.321.30.0**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-257">&ensp;Security intelligence update version: **1.321.30.0**</span></span>  
<span data-ttu-id="f8aaa-258">&ensp;Publication : **28 juillet 2020**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-258">&ensp;Released: **July 28, 2020**</span></span>  
<span data-ttu-id="f8aaa-259">&ensp;Plateforme : **4.18.2007.8**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-259">&ensp;Platform: **4.18.2007.8**</span></span>  
<span data-ttu-id="f8aaa-260">&ensp;Moteur : **1.1.17300.4**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-260">&ensp;Engine: **1.1.17300.4**</span></span>  
<span data-ttu-id="f8aaa-261">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-261">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="f8aaa-262">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="f8aaa-262">What's new</span></span>

- <span data-ttu-id="f8aaa-263">Télémétrie améliorée pour BITS</span><span class="sxs-lookup"><span data-stu-id="f8aaa-263">Improved telemetry for BITS</span></span>
- <span data-ttu-id="f8aaa-264">Validation améliorée du certificat de signature de code Authenticode</span><span class="sxs-lookup"><span data-stu-id="f8aaa-264">Improved Authenticode code signing certificate validation</span></span>

### <a name="known-issues"></a><span data-ttu-id="f8aaa-265">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="f8aaa-265">Known Issues</span></span>
<span data-ttu-id="f8aaa-266">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="f8aaa-266">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="f8aaa-267">Juin-2020 (plateforme : 4.18.2006.10 | Moteur : 1.1.17200.2)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-267">June-2020 (Platform: 4.18.2006.10 | Engine: 1.1.17200.2)</span></span></summary>

<span data-ttu-id="f8aaa-268">&ensp;Version de mise à jour des informations de sécurité **: 1.319.20.0**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-268">&ensp;Security intelligence update version: **1.319.20.0**</span></span>  
<span data-ttu-id="f8aaa-269">&ensp;Publication : **22 juin 2020**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-269">&ensp;Released: **June 22, 2020**</span></span>  
<span data-ttu-id="f8aaa-270">&ensp;Plateforme : **4.18.2006.10**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-270">&ensp;Platform: **4.18.2006.10**</span></span>  
<span data-ttu-id="f8aaa-271">&ensp;Moteur : **1.1.17200.2**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-271">&ensp;Engine: **1.1.17200.2**</span></span>  
<span data-ttu-id="f8aaa-272">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-272">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="f8aaa-273">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="f8aaa-273">What's new</span></span>

- <span data-ttu-id="f8aaa-274">Possibilité de spécifier [l’emplacement des journaux de support](./collect-diagnostic-data.md)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-274">Possibility to specify the [location of the support logs](./collect-diagnostic-data.md)</span></span>
- <span data-ttu-id="f8aaa-275">Ignorer l’analyse de rattrapage agressive en mode passif.</span><span class="sxs-lookup"><span data-stu-id="f8aaa-275">Skipping aggressive catchup scan in Passive mode.</span></span>
- <span data-ttu-id="f8aaa-276">Autoriser Defender à mettre à jour les connexions avec des compteurs</span><span class="sxs-lookup"><span data-stu-id="f8aaa-276">Allow Defender to update on metered connections</span></span>
- <span data-ttu-id="f8aaa-277">Réglage des performances fixes lorsque la mise en cache est désactivée</span><span class="sxs-lookup"><span data-stu-id="f8aaa-277">Fixed performance tuning when caching is disabled</span></span> 
- <span data-ttu-id="f8aaa-278">Requête de Registre fixe</span><span class="sxs-lookup"><span data-stu-id="f8aaa-278">Fixed registry query</span></span> 
- <span data-ttu-id="f8aaa-279">Randomisation du scantime fixe dans ADMX</span><span class="sxs-lookup"><span data-stu-id="f8aaa-279">Fixed scantime randomization in ADMX</span></span>

### <a name="known-issues"></a><span data-ttu-id="f8aaa-280">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="f8aaa-280">Known Issues</span></span>
<span data-ttu-id="f8aaa-281">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="f8aaa-281">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="f8aaa-282">Mai-2020 (plateforme : 4.18.2005.4 | Moteur : 1.1.17100.2)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-282">May-2020 (Platform: 4.18.2005.4 | Engine: 1.1.17100.2)</span></span></summary>

<span data-ttu-id="f8aaa-283">&ensp;Version de mise à jour des informations de sécurité **: 1.317.20.0**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-283">&ensp;Security intelligence update version: **1.317.20.0**</span></span>  
<span data-ttu-id="f8aaa-284">&ensp;Publication : **26 mai 2020**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-284">&ensp;Released: **May 26, 2020**</span></span>  
<span data-ttu-id="f8aaa-285">&ensp;Plateforme : **4.18.2005.4**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-285">&ensp;Platform: **4.18.2005.4**</span></span>  
<span data-ttu-id="f8aaa-286">&ensp;Moteur : **1.1.17100.2**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-286">&ensp;Engine: **1.1.17100.2**</span></span>  
<span data-ttu-id="f8aaa-287">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-287">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="f8aaa-288">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="f8aaa-288">What's new</span></span>

- <span data-ttu-id="f8aaa-289">Enregistrement amélioré pour les événements d’analyse</span><span class="sxs-lookup"><span data-stu-id="f8aaa-289">Improved logging for scan events</span></span>
- <span data-ttu-id="f8aaa-290">Amélioration de la gestion des incidents en mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f8aaa-290">Improved user mode crash handling.</span></span>
- <span data-ttu-id="f8aaa-291">Suivi des événements ajouté pour la protection contre la falsification</span><span class="sxs-lookup"><span data-stu-id="f8aaa-291">Added event tracing for Tamper protection</span></span>
- <span data-ttu-id="f8aaa-292">Envoi d’exemples AMSI fixes</span><span class="sxs-lookup"><span data-stu-id="f8aaa-292">Fixed AMSI Sample submission</span></span>
- <span data-ttu-id="f8aaa-293">Blocage du cloud AMSI fixe</span><span class="sxs-lookup"><span data-stu-id="f8aaa-293">Fixed AMSI Cloud blocking</span></span>
- <span data-ttu-id="f8aaa-294">Journal d’installation des mises à jour de sécurité fixes</span><span class="sxs-lookup"><span data-stu-id="f8aaa-294">Fixed Security update install log</span></span>

### <a name="known-issues"></a><span data-ttu-id="f8aaa-295">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="f8aaa-295">Known Issues</span></span>
<span data-ttu-id="f8aaa-296">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="f8aaa-296">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="f8aaa-297">Avril-2020 (plateforme : 4.18.2004.6 | Moteur : 1.1.17000.2)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-297">April-2020 (Platform: 4.18.2004.6 | Engine: 1.1.17000.2)</span></span></summary>

<span data-ttu-id="f8aaa-298">&ensp;Version de mise à jour des informations de sécurité **: 1.315.12.0**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-298">&ensp;Security intelligence update version: **1.315.12.0**</span></span>  
<span data-ttu-id="f8aaa-299">&ensp;Publication : **30 avril 2020**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-299">&ensp;Released: **April 30, 2020**</span></span>  
<span data-ttu-id="f8aaa-300">&ensp;Plateforme : **4.18.2004.6**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-300">&ensp;Platform: **4.18.2004.6**</span></span>  
<span data-ttu-id="f8aaa-301">&ensp;Moteur : **1.1.17000.2**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-301">&ensp;Engine: **1.1.17000.2**</span></span>  
<span data-ttu-id="f8aaa-302">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-302">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="f8aaa-303">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="f8aaa-303">What's new</span></span>
- <span data-ttu-id="f8aaa-304">Améliorations apportées aux filtres WDfilter</span><span class="sxs-lookup"><span data-stu-id="f8aaa-304">WDfilter improvements</span></span>
- <span data-ttu-id="f8aaa-305">Ajouter des données d’événements actionnables à des événements de détection de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="f8aaa-305">Add more actionable event data to attack surface reduction detection events</span></span>
- <span data-ttu-id="f8aaa-306">Informations de version fixes dans les données de diagnostic et WMI</span><span class="sxs-lookup"><span data-stu-id="f8aaa-306">Fixed version information in diagnostic data and WMI</span></span>
- <span data-ttu-id="f8aaa-307">Version de plateforme incorrecte corrigée dans l’interface utilisateur après la mise à jour de la plateforme</span><span class="sxs-lookup"><span data-stu-id="f8aaa-307">Fixed incorrect platform version in UI after platform update</span></span>
- <span data-ttu-id="f8aaa-308">Intel d’URL dynamique pour la protection contre les menaces sans fichier</span><span class="sxs-lookup"><span data-stu-id="f8aaa-308">Dynamic URL intel for Fileless threat protection</span></span>
- <span data-ttu-id="f8aaa-309">Fonctionnalité d’analyse UEFI</span><span class="sxs-lookup"><span data-stu-id="f8aaa-309">UEFI scan capability</span></span>
- <span data-ttu-id="f8aaa-310">Étendre la journalisation pour les mises à jour</span><span class="sxs-lookup"><span data-stu-id="f8aaa-310">Extend logging for updates</span></span>

### <a name="known-issues"></a><span data-ttu-id="f8aaa-311">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="f8aaa-311">Known Issues</span></span>
<span data-ttu-id="f8aaa-312">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="f8aaa-312">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="f8aaa-313">Mars-2020 (plateforme : 4.18.2003.8 | Moteur : 1.1.16900.2)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-313">March-2020 (Platform: 4.18.2003.8 | Engine: 1.1.16900.2)</span></span></summary>

<span data-ttu-id="f8aaa-314">&ensp;Version de mise à jour des informations de sécurité **: 1.313.8.0**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-314">&ensp;Security intelligence update version: **1.313.8.0**</span></span>  
<span data-ttu-id="f8aaa-315">&ensp;Publication : **24 mars 2020**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-315">&ensp;Released: **March 24, 2020**</span></span>  
<span data-ttu-id="f8aaa-316">&ensp;Plateforme : **4.18.2003.8**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-316">&ensp;Platform: **4.18.2003.8**</span></span>  
<span data-ttu-id="f8aaa-317">&ensp;Moteur : **1.1.16900.4**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-317">&ensp;Engine: **1.1.16900.4**</span></span>  
<span data-ttu-id="f8aaa-318">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-318">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="f8aaa-319">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="f8aaa-319">What's new</span></span>

- <span data-ttu-id="f8aaa-320">Option de limitation du processeur ajoutée à [MpCmdRun](./command-line-arguments-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-320">CPU Throttling option added to [MpCmdRun](./command-line-arguments-microsoft-defender-antivirus.md)</span></span>
- <span data-ttu-id="f8aaa-321">Améliorer les fonctionnalités de diagnostic</span><span class="sxs-lookup"><span data-stu-id="f8aaa-321">Improve diagnostic capability</span></span>
- <span data-ttu-id="f8aaa-322">réduire le délai d’out des informations de sécurité (5 min)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-322">reduce Security intelligence timeout (5 min)</span></span>
- <span data-ttu-id="f8aaa-323">Étendre la fonctionnalité de journal interne du moteur AMSI</span><span class="sxs-lookup"><span data-stu-id="f8aaa-323">Extend AMSI engine internal log capability</span></span>
- <span data-ttu-id="f8aaa-324">Améliorer la notification pour le blocage des processus</span><span class="sxs-lookup"><span data-stu-id="f8aaa-324">Improve notification for process blocking</span></span>
   
### <a name="known-issues"></a><span data-ttu-id="f8aaa-325">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="f8aaa-325">Known Issues</span></span>
<span data-ttu-id="f8aaa-326">[**Fixe**] Antivirus Microsoft Defender ignorer les fichiers lors de l’exécution d’une analyse.</span><span class="sxs-lookup"><span data-stu-id="f8aaa-326">[**Fixed**] Microsoft Defender Antivirus is skipping files when running a scan.</span></span>

<br/>
</details>

<details>

<summary> <span data-ttu-id="f8aaa-327">Février-2020 (plateforme : - | Moteur : 1.1.16800.2)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-327">February-2020 (Platform: - | Engine: 1.1.16800.2)</span></span></summary>
  

<span data-ttu-id="f8aaa-328">&ensp;Version de mise à jour des informations de sécurité **: 1.311.4.0** </span><span class="sxs-lookup"><span data-stu-id="f8aaa-328">&ensp;Security intelligence update version: **1.311.4.0** </span></span>  
<span data-ttu-id="f8aaa-329">&ensp;Publication : **25 février 2020**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-329">&ensp;Released: **February 25, 2020**</span></span>  
<span data-ttu-id="f8aaa-330">&ensp;Plateforme/client : **-**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-330">&ensp;Platform/Client: **-**</span></span>  
<span data-ttu-id="f8aaa-331">&ensp;Moteur : **1.1.16800.2**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-331">&ensp;Engine: **1.1.16800.2**</span></span>  
<span data-ttu-id="f8aaa-332">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-332">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
     
### <a name="whats-new"></a><span data-ttu-id="f8aaa-333">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="f8aaa-333">What's new</span></span>

  
### <a name="known-issues"></a><span data-ttu-id="f8aaa-334">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="f8aaa-334">Known Issues</span></span>
<span data-ttu-id="f8aaa-335">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="f8aaa-335">No known issues</span></span>
<br/>
</details>

<details>
<summary> <span data-ttu-id="f8aaa-336">Janvier-2020 (plateforme : 4.18.2001.10 | Moteur : 1.1.16700.2)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-336">January-2020 (Platform: 4.18.2001.10 | Engine: 1.1.16700.2)</span></span></summary>
  

<span data-ttu-id="f8aaa-337">Version de mise à jour des informations de sécurité **: 1.309.32.0**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-337">Security intelligence update version: **1.309.32.0**</span></span>  
<span data-ttu-id="f8aaa-338">Publication : **30 janvier 2020**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-338">Released: **January 30, 2020**</span></span>  
<span data-ttu-id="f8aaa-339">Plateforme/Client : **4.18.2001.10**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-339">Platform/Client: **4.18.2001.10**</span></span>  
<span data-ttu-id="f8aaa-340">Moteur : **1.1.16700.2**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-340">Engine: **1.1.16700.2**</span></span>  
<span data-ttu-id="f8aaa-341">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-341">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
     
### <a name="whats-new"></a><span data-ttu-id="f8aaa-342">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="f8aaa-342">What's new</span></span>

- <span data-ttu-id="f8aaa-343">Correction du BSOD sur WS2016 avec Exchange</span><span class="sxs-lookup"><span data-stu-id="f8aaa-343">Fixed BSOD on WS2016 with Exchange</span></span>
- <span data-ttu-id="f8aaa-344">Prise en charge des mises à jour de plateforme lorsque le TMP est redirigé vers le chemin d’accès réseau</span><span class="sxs-lookup"><span data-stu-id="f8aaa-344">Support platform updates when TMP is redirected to network path</span></span>
- <span data-ttu-id="f8aaa-345">Les versions de plateforme et de moteur sont [ajoutées à WDSI](https://www.microsoft.com/en-us/wdsi/defenderupdates)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-345">Platform and engine versions are added to [WDSI](https://www.microsoft.com/en-us/wdsi/defenderupdates)</span></span> <!-- The preceding URL must include "/en-us" -->
- <span data-ttu-id="f8aaa-346">étendre la mise à jour des signatures d’urgence [en mode passif](./microsoft-defender-antivirus-compatibility.md)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-346">extend Emergency signature update to [passive mode](./microsoft-defender-antivirus-compatibility.md)</span></span>
- <span data-ttu-id="f8aaa-347">Correction du problème de 4.18.1911.3</span><span class="sxs-lookup"><span data-stu-id="f8aaa-347">Fix 4.18.1911.3 hang</span></span>
   
### <a name="known-issues"></a><span data-ttu-id="f8aaa-348">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="f8aaa-348">Known Issues</span></span>

<span data-ttu-id="f8aaa-349">[**Fixe**] Les appareils utilisant le [mode](/windows-hardware/design/device-experiences/modern-standby) de veille moderne peuvent se bloquer avec le pilote de filtre Windows Defender, ce qui se traduit par un manque de protection.</span><span class="sxs-lookup"><span data-stu-id="f8aaa-349">[**Fixed**] devices utilizing [modern standby mode](/windows-hardware/design/device-experiences/modern-standby) may experience a hang with the Windows Defender filter driver that results in a gap of protection.</span></span>  <span data-ttu-id="f8aaa-350">Les ordinateurs concernés semblent ne pas avoir été mis à jour vers la dernière plateforme anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="f8aaa-350">Affected machines appear to the customer as having not updated to the latest antimalware platform.</span></span>  
<br/>
> [!IMPORTANT]
> <span data-ttu-id="f8aaa-351">Cette mise à jour est :</span><span class="sxs-lookup"><span data-stu-id="f8aaa-351">This update is:</span></span>
> - <span data-ttu-id="f8aaa-352">nécessaire aux appareils RS1 exécutant une version inférieure de la plateforme pour prendre en charge SHA2 ;</span><span class="sxs-lookup"><span data-stu-id="f8aaa-352">needed by RS1 devices running lower version of the platform to support SHA2;</span></span>
> - <span data-ttu-id="f8aaa-353">a un indicateur de redémarrage pour les systèmes qui ont des problèmes en suspension ;</span><span class="sxs-lookup"><span data-stu-id="f8aaa-353">has a reboot flag for systems that have hanging issues;</span></span>
> - <span data-ttu-id="f8aaa-354">est re-publiée en avril 2020 et ne sera pas recalée par les mises à jour plus nouvelles pour conserver la disponibilité future ;</span><span class="sxs-lookup"><span data-stu-id="f8aaa-354">is re-released in April 2020 and will not be superseded by newer updates to keep future availability;</span></span>  
> - <span data-ttu-id="f8aaa-355">est classée en tant que mise à jour en raison de l’exigence de redémarrage ; et</span><span class="sxs-lookup"><span data-stu-id="f8aaa-355">is categorized as an update due to the reboot requirement; and</span></span>
> - <span data-ttu-id="f8aaa-356">est uniquement proposé avec [la mise à jour Windows.](https://support.microsoft.com/help/4027667/windows-10-update)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-356">is only be offered with [Windows Update](https://support.microsoft.com/help/4027667/windows-10-update).</span></span>
<br/>
</details>

<details>
<summary> <span data-ttu-id="f8aaa-357">Novembre-2019 (plateforme : 4.18.1911.3 | Moteur : 1.1.16600.7)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-357">November-2019 (Platform: 4.18.1911.3 | Engine: 1.1.16600.7)</span></span></summary>

<span data-ttu-id="f8aaa-358">Version de mise à jour des informations de sécurité **: 1.307.13.0**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-358">Security intelligence update version: **1.307.13.0**</span></span>  
<span data-ttu-id="f8aaa-359">Publication : **7 décembre 2019**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-359">Released: **December 7, 2019**</span></span>  
<span data-ttu-id="f8aaa-360">Plateforme : **4.18.1911.3**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-360">Platform: **4.18.1911.3**</span></span>  
<span data-ttu-id="f8aaa-361">Moteur : **1.1.17000.7**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-361">Engine: **1.1.17000.7**</span></span>  
<span data-ttu-id="f8aaa-362">Phase de support : **aucune prise en charge**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-362">Support phase: **No support**</span></span>  
     
### <a name="whats-new"></a><span data-ttu-id="f8aaa-363">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="f8aaa-363">What's new</span></span>

- <span data-ttu-id="f8aaa-364">Niveau de suivi MpCmdRun fixe</span><span class="sxs-lookup"><span data-stu-id="f8aaa-364">Fixed MpCmdRun tracing level</span></span>
- <span data-ttu-id="f8aaa-365">Informations de version de WDFilter fixes</span><span class="sxs-lookup"><span data-stu-id="f8aaa-365">Fixed WDFilter version info</span></span>
- <span data-ttu-id="f8aaa-366">Améliorer les notifications (PUA)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-366">Improve notifications (PUA)</span></span>
- <span data-ttu-id="f8aaa-367">ajouter des journaux MRT pour prendre en charge les fichiers</span><span class="sxs-lookup"><span data-stu-id="f8aaa-367">add MRT logs to support files</span></span>
   
### <a name="known-issues"></a><span data-ttu-id="f8aaa-368">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="f8aaa-368">Known Issues</span></span>
<span data-ttu-id="f8aaa-369">Lorsque cette mise à jour est installée, l’appareil a besoin du package de saut 4.18.2001.10 pour pouvoir se mettre à jour vers la dernière version de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="f8aaa-369">When this update is installed, the device needs the jump package 4.18.2001.10 to be able to update to the latest platform version.</span></span>
<br/>
</details>


## <a name="microsoft-defender-antivirus-platform-support"></a><span data-ttu-id="f8aaa-370">Antivirus Microsoft Defender prise en charge de la plateforme</span><span class="sxs-lookup"><span data-stu-id="f8aaa-370">Microsoft Defender Antivirus platform support</span></span>
<span data-ttu-id="f8aaa-371">Les mises à jour de la plateforme et du moteur sont fournies à une cadence mensuelle.</span><span class="sxs-lookup"><span data-stu-id="f8aaa-371">Platform and engine updates are provided on a monthly cadence.</span></span> <span data-ttu-id="f8aaa-372">Pour être entièrement pris en charge, tenez à jour les dernières mises à jour de plateforme.</span><span class="sxs-lookup"><span data-stu-id="f8aaa-372">To be fully supported, keep current with the latest platform updates.</span></span> <span data-ttu-id="f8aaa-373">Notre structure de support est dynamique et évolue en deux phases en fonction de la disponibilité de la dernière version de plateforme :</span><span class="sxs-lookup"><span data-stu-id="f8aaa-373">Our support structure is dynamic, evolving into two phases depending on the availability of the latest platform version:</span></span>

- <span data-ttu-id="f8aaa-374">Phase de maintenance des mises à jour **critiques** et de sécurité : lors de l’exécution de la dernière version de la plateforme, vous serez éligible à la réception des mises à jour de sécurité et critiques sur la plateforme anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="f8aaa-374">**Security and Critical Updates servicing phase** - When running the latest platform version, you will be eligible to receive both Security and Critical updates to the anti-malware platform.</span></span>
 
- <span data-ttu-id="f8aaa-375">**Phase de support technique (uniquement)** : après la publication d’une nouvelle version de plateforme, la prise en charge des versions antérieures (N-2) sera réduit au support technique uniquement.</span><span class="sxs-lookup"><span data-stu-id="f8aaa-375">**Technical Support (Only) phase** - After a new platform version is released, support for older versions (N-2) will reduce to technical support only.</span></span> <span data-ttu-id="f8aaa-376">Les versions de plateforme antérieures à N-2 ne seront plus pris en charge.\*</span><span class="sxs-lookup"><span data-stu-id="f8aaa-376">Platform versions older than N-2 will no longer be supported.\*</span></span>

<span data-ttu-id="f8aaa-377">\*Le support technique continuera d’être fourni pour les mises à niveau de la version Windows 10 (voir la version de plateforme incluse avec [les](#platform-version-included-with-windows-10-releases)versions Windows 10 ) vers la dernière version de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="f8aaa-377">\* Technical support will continue to be provided for upgrades from the Windows 10 release version (see [Platform version included with Windows 10 releases](#platform-version-included-with-windows-10-releases)) to the latest platform version.</span></span>

<span data-ttu-id="f8aaa-378">Pendant la phase de support technique (uniquement), les incidents de support commercialement raisonnables sont fournis par le biais du support technique du service clientèle Microsoft & et des offres de support géré de Microsoft (telles que le support Premier).</span><span class="sxs-lookup"><span data-stu-id="f8aaa-378">During the technical support (only) phase, commercially reasonable support incidents will be provided through Microsoft Customer Service & Support and Microsoft’s managed support offerings (such as Premier Support).</span></span> <span data-ttu-id="f8aaa-379">Si un incident de support nécessite une escalade vers le développement pour obtenir des conseils supplémentaires, nécessite une mise à jour non de sécurité ou nécessite une mise à jour de sécurité, les clients sont invités à mettre à niveau vers la dernière version de plateforme ou une mise à jour intermédiaire (\*).</span><span class="sxs-lookup"><span data-stu-id="f8aaa-379">If a support incident requires escalation to development for further guidance, requires a non-security update, or requires a security update, customers will be asked to upgrade to the latest platform version or an intermediate update (\*).</span></span>

### <a name="platform-version-included-with-windows-10-releases"></a><span data-ttu-id="f8aaa-380">Version de plateforme incluse dans Windows 10 versions</span><span class="sxs-lookup"><span data-stu-id="f8aaa-380">Platform version included with Windows 10 releases</span></span>
<span data-ttu-id="f8aaa-381">Le tableau ci-dessous fournit les versions Antivirus Microsoft Defender de plateforme et de moteur qui sont livrées avec les versions les Windows 10 les plus récentes :</span><span class="sxs-lookup"><span data-stu-id="f8aaa-381">The below table provides the Microsoft Defender Antivirus platform and engine versions that are shipped with the latest Windows 10 releases:</span></span>    

|<span data-ttu-id="f8aaa-382">Windows 10 version</span><span class="sxs-lookup"><span data-stu-id="f8aaa-382">Windows 10 release</span></span>  |<span data-ttu-id="f8aaa-383">Version de la plateforme</span><span class="sxs-lookup"><span data-stu-id="f8aaa-383">Platform version</span></span>  |<span data-ttu-id="f8aaa-384">Version du moteur</span><span class="sxs-lookup"><span data-stu-id="f8aaa-384">Engine version</span></span> |<span data-ttu-id="f8aaa-385">Phase de prise en charge</span><span class="sxs-lookup"><span data-stu-id="f8aaa-385">Support phase</span></span> |
|:---|:---|:---|:---|
|<span data-ttu-id="f8aaa-386">2004 (20H1/20H2)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-386">2004  (20H1/20H2)</span></span> |<span data-ttu-id="f8aaa-387">4.18.1909.6</span><span class="sxs-lookup"><span data-stu-id="f8aaa-387">4.18.1909.6</span></span> |<span data-ttu-id="f8aaa-388">1.1.17000.2</span><span class="sxs-lookup"><span data-stu-id="f8aaa-388">1.1.17000.2</span></span> | <span data-ttu-id="f8aaa-389">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-389">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="f8aaa-390">1909 (19H2)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-390">1909  (19H2)</span></span> |<span data-ttu-id="f8aaa-391">4.18.1902.5</span><span class="sxs-lookup"><span data-stu-id="f8aaa-391">4.18.1902.5</span></span> |<span data-ttu-id="f8aaa-392">1.1.16700.3</span><span class="sxs-lookup"><span data-stu-id="f8aaa-392">1.1.16700.3</span></span> | <span data-ttu-id="f8aaa-393">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-393">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="f8aaa-394">1903 (19H1)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-394">1903  (19H1)</span></span> |<span data-ttu-id="f8aaa-395">4.18.1902.5</span><span class="sxs-lookup"><span data-stu-id="f8aaa-395">4.18.1902.5</span></span> |<span data-ttu-id="f8aaa-396">1.1.15600.4</span><span class="sxs-lookup"><span data-stu-id="f8aaa-396">1.1.15600.4</span></span> | <span data-ttu-id="f8aaa-397">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-397">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="f8aaa-398">1809 (RS5)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-398">1809  (RS5)</span></span> |<span data-ttu-id="f8aaa-399">4.18.1807.18075</span><span class="sxs-lookup"><span data-stu-id="f8aaa-399">4.18.1807.18075</span></span> |<span data-ttu-id="f8aaa-400">1.1.15000.2</span><span class="sxs-lookup"><span data-stu-id="f8aaa-400">1.1.15000.2</span></span> | <span data-ttu-id="f8aaa-401">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-401">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="f8aaa-402">1803 (RS4)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-402">1803  (RS4)</span></span> |<span data-ttu-id="f8aaa-403">4.13.17134.1</span><span class="sxs-lookup"><span data-stu-id="f8aaa-403">4.13.17134.1</span></span> |<span data-ttu-id="f8aaa-404">1.1.14600.4</span><span class="sxs-lookup"><span data-stu-id="f8aaa-404">1.1.14600.4</span></span> | <span data-ttu-id="f8aaa-405">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-405">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="f8aaa-406">1709 (RS3)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-406">1709  (RS3)</span></span> |<span data-ttu-id="f8aaa-407">4.12.16299.15</span><span class="sxs-lookup"><span data-stu-id="f8aaa-407">4.12.16299.15</span></span> |<span data-ttu-id="f8aaa-408">1.1.14104.0</span><span class="sxs-lookup"><span data-stu-id="f8aaa-408">1.1.14104.0</span></span> | <span data-ttu-id="f8aaa-409">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-409">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="f8aaa-410">1703 (RS2)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-410">1703  (RS2)</span></span> |<span data-ttu-id="f8aaa-411">4.11.15603.2</span><span class="sxs-lookup"><span data-stu-id="f8aaa-411">4.11.15603.2</span></span> |<span data-ttu-id="f8aaa-412">1.1.13504.0</span><span class="sxs-lookup"><span data-stu-id="f8aaa-412">1.1.13504.0</span></span> | <span data-ttu-id="f8aaa-413">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-413">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="f8aaa-414">1607 (RS1)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-414">1607 (RS1)</span></span> |<span data-ttu-id="f8aaa-415">4.10.14393.3683</span><span class="sxs-lookup"><span data-stu-id="f8aaa-415">4.10.14393.3683</span></span> |<span data-ttu-id="f8aaa-416">1.1.12805.0</span><span class="sxs-lookup"><span data-stu-id="f8aaa-416">1.1.12805.0</span></span> | <span data-ttu-id="f8aaa-417">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-417">Technical upgrade support (only)</span></span> |  

<span data-ttu-id="f8aaa-418">Pour Windows 10 de publication, consultez la [Windows de faits sur](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet)le cycle de vie.</span><span class="sxs-lookup"><span data-stu-id="f8aaa-418">For Windows 10 release information, see the [Windows lifecycle fact sheet](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet).</span></span>

## <a name="updates-for-deployment-image-servicing-and-management-dism"></a><span data-ttu-id="f8aaa-419">Mises à jour pour la gestion et la maintenance des images de déploiement (DISM)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-419">Updates for Deployment Image Servicing and Management (DISM)</span></span>

<span data-ttu-id="f8aaa-420">Nous vous recommandons de mettre à jour vos images d’installation Windows 10 (éditions Enterprise, Pro et Famille), Windows Server 2019 et Windows Server 2016 OS avec les dernières mises à jour antivirus et anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="f8aaa-420">We recommend updating your Windows 10 (Enterprise, Pro, and Home editions), Windows Server 2019, and Windows Server 2016 OS installation images with the latest antivirus and antimalware updates.</span></span> <span data-ttu-id="f8aaa-421">La mise à jour de vos images d’installation du système d’exploitation permet d’éviter un écart de protection.</span><span class="sxs-lookup"><span data-stu-id="f8aaa-421">Keeping your OS installation images up to date helps avoid a gap in protection.</span></span> 

<span data-ttu-id="f8aaa-422">Pour plus d’informations, voir mise à [jour de Microsoft Defender pour Windows images d’installation du système d’exploitation.](https://support.microsoft.com/help/4568292/defender-update-for-windows-operating-system-installation-images)</span><span class="sxs-lookup"><span data-stu-id="f8aaa-422">For more information, see [Microsoft Defender update for Windows operating system installation images](https://support.microsoft.com/help/4568292/defender-update-for-windows-operating-system-installation-images).</span></span>

<details>
<summary><span data-ttu-id="f8aaa-423">1.1.2106.01</span><span class="sxs-lookup"><span data-stu-id="f8aaa-423">1.1.2106.01</span></span></summary>

<span data-ttu-id="f8aaa-424">&ensp;Version du package **: 1.1.2106.01**  </span><span class="sxs-lookup"><span data-stu-id="f8aaa-424">&ensp;Package version: **1.1.2106.01**  </span></span>  
<span data-ttu-id="f8aaa-425">&ensp;Version de la plateforme **: 4.18.2104.14** </span><span class="sxs-lookup"><span data-stu-id="f8aaa-425">&ensp;Platform version: **4.18.2104.14** </span></span>  
<span data-ttu-id="f8aaa-426">&ensp;Version du moteur **: 1.1.18100.6**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-426">&ensp;Engine version: **1.1.18100.6**</span></span>  
<span data-ttu-id="f8aaa-427">&ensp;Version de signature **: 1.339.1923.0**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-427">&ensp;Signature version: **1.339.1923.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="f8aaa-428">Correctifs</span><span class="sxs-lookup"><span data-stu-id="f8aaa-428">Fixes</span></span>
- <span data-ttu-id="f8aaa-429">Aucun</span><span class="sxs-lookup"><span data-stu-id="f8aaa-429">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="f8aaa-430">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="f8aaa-430">Additional information</span></span>
- <span data-ttu-id="f8aaa-431">Aucun</span><span class="sxs-lookup"><span data-stu-id="f8aaa-431">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="f8aaa-432">1.1.2105.01</span><span class="sxs-lookup"><span data-stu-id="f8aaa-432">1.1.2105.01</span></span></summary>

<span data-ttu-id="f8aaa-433">&ensp;Version du package **: 1.1.2105.01**  </span><span class="sxs-lookup"><span data-stu-id="f8aaa-433">&ensp;Package version: **1.1.2105.01**  </span></span>  
<span data-ttu-id="f8aaa-434">&ensp;Version de la plateforme **: 4.18.2103.7** </span><span class="sxs-lookup"><span data-stu-id="f8aaa-434">&ensp;Platform version: **4.18.2103.7** </span></span>  
<span data-ttu-id="f8aaa-435">&ensp;Version du moteur **: 1.1.18100.6**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-435">&ensp;Engine version: **1.1.18100.6**</span></span>  
<span data-ttu-id="f8aaa-436">&ensp;Version de signature **: 1.339.42.0**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-436">&ensp;Signature version: **1.339.42.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="f8aaa-437">Correctifs</span><span class="sxs-lookup"><span data-stu-id="f8aaa-437">Fixes</span></span>
- <span data-ttu-id="f8aaa-438">Aucun</span><span class="sxs-lookup"><span data-stu-id="f8aaa-438">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="f8aaa-439">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="f8aaa-439">Additional information</span></span>
- <span data-ttu-id="f8aaa-440">Aucun</span><span class="sxs-lookup"><span data-stu-id="f8aaa-440">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="f8aaa-441">1.1.2104.01</span><span class="sxs-lookup"><span data-stu-id="f8aaa-441">1.1.2104.01</span></span></summary>

<span data-ttu-id="f8aaa-442">&ensp;Version du package **: 1.1.2104.01**  </span><span class="sxs-lookup"><span data-stu-id="f8aaa-442">&ensp;Package version: **1.1.2104.01**  </span></span>  
<span data-ttu-id="f8aaa-443">&ensp;Version de plateforme **: 4.18.2102.4** </span><span class="sxs-lookup"><span data-stu-id="f8aaa-443">&ensp;Platform version: **4.18.2102.4** </span></span>  
<span data-ttu-id="f8aaa-444">&ensp;Version du moteur **: 1.1.18000.5**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-444">&ensp;Engine version: **1.1.18000.5**</span></span>  
<span data-ttu-id="f8aaa-445">&ensp;Version de signature **: 1.335.232.0**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-445">&ensp;Signature version: **1.335.232.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="f8aaa-446">Correctifs</span><span class="sxs-lookup"><span data-stu-id="f8aaa-446">Fixes</span></span>
- <span data-ttu-id="f8aaa-447">Aucun</span><span class="sxs-lookup"><span data-stu-id="f8aaa-447">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="f8aaa-448">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="f8aaa-448">Additional information</span></span>
- <span data-ttu-id="f8aaa-449">Aucun</span><span class="sxs-lookup"><span data-stu-id="f8aaa-449">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="f8aaa-450">1.1.2103.01</span><span class="sxs-lookup"><span data-stu-id="f8aaa-450">1.1.2103.01</span></span></summary>

<span data-ttu-id="f8aaa-451">&ensp;Version du package **: 1.1.2103.01**  </span><span class="sxs-lookup"><span data-stu-id="f8aaa-451">&ensp;Package version: **1.1.2103.01**  </span></span>  
<span data-ttu-id="f8aaa-452">&ensp;Version de plateforme **: 4.18.2101.9** </span><span class="sxs-lookup"><span data-stu-id="f8aaa-452">&ensp;Platform version: **4.18.2101.9** </span></span>  
<span data-ttu-id="f8aaa-453">&ensp;Version du moteur **: 1.1.17800.5**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-453">&ensp;Engine version: **1.1.17800.5**</span></span>  
<span data-ttu-id="f8aaa-454">&ensp;Version de signature **: 1.331.2302.0**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-454">&ensp;Signature version: **1.331.2302.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="f8aaa-455">Correctifs</span><span class="sxs-lookup"><span data-stu-id="f8aaa-455">Fixes</span></span>
- <span data-ttu-id="f8aaa-456">Aucun</span><span class="sxs-lookup"><span data-stu-id="f8aaa-456">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="f8aaa-457">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="f8aaa-457">Additional information</span></span>
- <span data-ttu-id="f8aaa-458">Aucun</span><span class="sxs-lookup"><span data-stu-id="f8aaa-458">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="f8aaa-459">1.1.2102.03</span><span class="sxs-lookup"><span data-stu-id="f8aaa-459">1.1.2102.03</span></span></summary>

<span data-ttu-id="f8aaa-460">&ensp;Version du package **: 1.1.2102.03**  </span><span class="sxs-lookup"><span data-stu-id="f8aaa-460">&ensp;Package version: **1.1.2102.03**  </span></span>  
<span data-ttu-id="f8aaa-461">&ensp;Version de la plateforme **: 4.18.2011.6** </span><span class="sxs-lookup"><span data-stu-id="f8aaa-461">&ensp;Platform version: **4.18.2011.6** </span></span>  
<span data-ttu-id="f8aaa-462">&ensp;Version du moteur **: 1.1.17800.5**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-462">&ensp;Engine version: **1.1.17800.5**</span></span>  
<span data-ttu-id="f8aaa-463">&ensp;Version de signature **: 1.331.174.0**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-463">&ensp;Signature version: **1.331.174.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="f8aaa-464">Correctifs</span><span class="sxs-lookup"><span data-stu-id="f8aaa-464">Fixes</span></span>
- <span data-ttu-id="f8aaa-465">Aucun</span><span class="sxs-lookup"><span data-stu-id="f8aaa-465">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="f8aaa-466">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="f8aaa-466">Additional information</span></span>
- <span data-ttu-id="f8aaa-467">Aucun</span><span class="sxs-lookup"><span data-stu-id="f8aaa-467">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="f8aaa-468">1.1.2101.02</span><span class="sxs-lookup"><span data-stu-id="f8aaa-468">1.1.2101.02</span></span></summary>

<span data-ttu-id="f8aaa-469">&ensp;Version du package **: 1.1.2101.02**  </span><span class="sxs-lookup"><span data-stu-id="f8aaa-469">&ensp;Package version: **1.1.2101.02**  </span></span>  
<span data-ttu-id="f8aaa-470">&ensp;Version de la plateforme **: 4.18.2011.6** </span><span class="sxs-lookup"><span data-stu-id="f8aaa-470">&ensp;Platform version: **4.18.2011.6** </span></span>  
<span data-ttu-id="f8aaa-471">&ensp;Version du moteur **: 1.1.17700.4**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-471">&ensp;Engine version: **1.1.17700.4**</span></span>  
<span data-ttu-id="f8aaa-472">&ensp;Version de signature **: 1.329.1796.0**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-472">&ensp;Signature version: **1.329.1796.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="f8aaa-473">Correctifs</span><span class="sxs-lookup"><span data-stu-id="f8aaa-473">Fixes</span></span>
- <span data-ttu-id="f8aaa-474">Aucun</span><span class="sxs-lookup"><span data-stu-id="f8aaa-474">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="f8aaa-475">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="f8aaa-475">Additional information</span></span>
- <span data-ttu-id="f8aaa-476">Aucun</span><span class="sxs-lookup"><span data-stu-id="f8aaa-476">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="f8aaa-477">1.1.2012.01</span><span class="sxs-lookup"><span data-stu-id="f8aaa-477">1.1.2012.01</span></span></summary>

<span data-ttu-id="f8aaa-478">&ensp;Version du package **: 1.1.2012.01**  </span><span class="sxs-lookup"><span data-stu-id="f8aaa-478">&ensp;Package version: **1.1.2012.01**  </span></span>  
<span data-ttu-id="f8aaa-479">&ensp;Version de plateforme **: 4.18.2010.7** </span><span class="sxs-lookup"><span data-stu-id="f8aaa-479">&ensp;Platform version: **4.18.2010.7** </span></span>  
<span data-ttu-id="f8aaa-480">&ensp;Version du moteur **: 1.1.17600.5**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-480">&ensp;Engine version: **1.1.17600.5**</span></span>  
<span data-ttu-id="f8aaa-481">&ensp;Version de signature **: 1.327.1991.0**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-481">&ensp;Signature version: **1.327.1991.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="f8aaa-482">Correctifs</span><span class="sxs-lookup"><span data-stu-id="f8aaa-482">Fixes</span></span>
- <span data-ttu-id="f8aaa-483">Aucun</span><span class="sxs-lookup"><span data-stu-id="f8aaa-483">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="f8aaa-484">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="f8aaa-484">Additional information</span></span>
- <span data-ttu-id="f8aaa-485">Aucun</span><span class="sxs-lookup"><span data-stu-id="f8aaa-485">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="f8aaa-486">1.1.2011.02</span><span class="sxs-lookup"><span data-stu-id="f8aaa-486">1.1.2011.02</span></span></summary>

<span data-ttu-id="f8aaa-487">&ensp;Version du package **: 1.1.2011.02**  </span><span class="sxs-lookup"><span data-stu-id="f8aaa-487">&ensp;Package version: **1.1.2011.02**  </span></span>  
<span data-ttu-id="f8aaa-488">&ensp;Version de plateforme **: 4.18.2010.7** </span><span class="sxs-lookup"><span data-stu-id="f8aaa-488">&ensp;Platform version: **4.18.2010.7** </span></span>  
<span data-ttu-id="f8aaa-489">&ensp;Version du moteur **: 1.1.17600.5**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-489">&ensp;Engine version: **1.1.17600.5**</span></span>  
<span data-ttu-id="f8aaa-490">&ensp;Version de signature **: 1.327.658.0**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-490">&ensp;Signature version: **1.327.658.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="f8aaa-491">Correctifs</span><span class="sxs-lookup"><span data-stu-id="f8aaa-491">Fixes</span></span>
- <span data-ttu-id="f8aaa-492">Aucun</span><span class="sxs-lookup"><span data-stu-id="f8aaa-492">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="f8aaa-493">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="f8aaa-493">Additional information</span></span>
- <span data-ttu-id="f8aaa-494">Signatures Antivirus Microsoft Defender actualisées</span><span class="sxs-lookup"><span data-stu-id="f8aaa-494">Refreshed Microsoft Defender Antivirus signatures</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="f8aaa-495">1.1.2011.01</span><span class="sxs-lookup"><span data-stu-id="f8aaa-495">1.1.2011.01</span></span></summary>

<span data-ttu-id="f8aaa-496">&ensp;Version du package **: 1.1.2011.01**  </span><span class="sxs-lookup"><span data-stu-id="f8aaa-496">&ensp;Package version: **1.1.2011.01**  </span></span>  
<span data-ttu-id="f8aaa-497">&ensp;Version de la plateforme **: 4.18.2009.7**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-497">&ensp;Platform version: **4.18.2009.7**</span></span>  
<span data-ttu-id="f8aaa-498">&ensp;Version du moteur **: 1.1.17600.5**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-498">&ensp;Engine version: **1.1.17600.5**</span></span>  
<span data-ttu-id="f8aaa-499">&ensp;Version de signature **: 1.327.344.0**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-499">&ensp;Signature version: **1.327.344.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="f8aaa-500">Correctifs</span><span class="sxs-lookup"><span data-stu-id="f8aaa-500">Fixes</span></span>
- <span data-ttu-id="f8aaa-501">Aucun</span><span class="sxs-lookup"><span data-stu-id="f8aaa-501">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="f8aaa-502">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="f8aaa-502">Additional information</span></span>
- <span data-ttu-id="f8aaa-503">Aucun</span><span class="sxs-lookup"><span data-stu-id="f8aaa-503">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="f8aaa-504">1.1.2009.10</span><span class="sxs-lookup"><span data-stu-id="f8aaa-504">1.1.2009.10</span></span></summary>

<span data-ttu-id="f8aaa-505">&ensp;Version du package **: 1.1.2011.01**  </span><span class="sxs-lookup"><span data-stu-id="f8aaa-505">&ensp;Package version: **1.1.2011.01**  </span></span>  
<span data-ttu-id="f8aaa-506">&ensp;Version de plateforme **: 4.18.2008.9** </span><span class="sxs-lookup"><span data-stu-id="f8aaa-506">&ensp;Platform version: **4.18.2008.9** </span></span>  
<span data-ttu-id="f8aaa-507">&ensp;Version du moteur **: 1.1.17400.5**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-507">&ensp;Engine version: **1.1.17400.5**</span></span>  
<span data-ttu-id="f8aaa-508">&ensp;Version de signature **: 1.327.2216.0**</span><span class="sxs-lookup"><span data-stu-id="f8aaa-508">&ensp;Signature version: **1.327.2216.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="f8aaa-509">Correctifs</span><span class="sxs-lookup"><span data-stu-id="f8aaa-509">Fixes</span></span>
- <span data-ttu-id="f8aaa-510">Aucun</span><span class="sxs-lookup"><span data-stu-id="f8aaa-510">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="f8aaa-511">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="f8aaa-511">Additional information</span></span>
- <span data-ttu-id="f8aaa-512">Ajout de la prise en charge Windows 10 images d’installation du système d’exploitation RS1 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f8aaa-512">Added support for Windows 10 RS1 or later OS install images.</span></span>  
<br/>
</details>

## <a name="additional-resources"></a><span data-ttu-id="f8aaa-513">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="f8aaa-513">Additional resources</span></span>

| <span data-ttu-id="f8aaa-514">Article</span><span class="sxs-lookup"><span data-stu-id="f8aaa-514">Article</span></span> | <span data-ttu-id="f8aaa-515">Description</span><span class="sxs-lookup"><span data-stu-id="f8aaa-515">Description</span></span>  |
|:---|:---|
|[<span data-ttu-id="f8aaa-516">Mise à jour de Microsoft Defender Windows images d’installation du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="f8aaa-516">Microsoft Defender update for Windows operating system installation images</span></span>](https://support.microsoft.com/help/4568292/defender-update-for-windows-operating-system-installation-images)  | <span data-ttu-id="f8aaa-517">Passer en revue les packages de mise à jour anti-programme malveillant pour vos images d’installation du système d’exploitation (fichiers WIM et VHD).</span><span class="sxs-lookup"><span data-stu-id="f8aaa-517">Review antimalware update packages for your OS installation images (WIM and VHD files).</span></span> <span data-ttu-id="f8aaa-518">Obtenez Antivirus Microsoft Defender mises à jour pour Windows 10 (éditions Enterprise, Pro et Famille), Windows Server 2019 et Windows Server 2016 images d’installation.</span><span class="sxs-lookup"><span data-stu-id="f8aaa-518">Get Microsoft Defender Antivirus updates for Windows 10 (Enterprise, Pro, and Home editions), Windows Server 2019, and Windows Server 2016 installation images.</span></span>  |
|[<span data-ttu-id="f8aaa-519">Gérer le téléchargement et l’application des mises à jour de protection</span><span class="sxs-lookup"><span data-stu-id="f8aaa-519">Manage how protection updates are downloaded and applied</span></span>](manage-protection-updates-microsoft-defender-antivirus.md) | <span data-ttu-id="f8aaa-520">Les mises à jour de la protection peuvent être livrées via de nombreuses sources.</span><span class="sxs-lookup"><span data-stu-id="f8aaa-520">Protection updates can be delivered through many sources.</span></span> |
|[<span data-ttu-id="f8aaa-521">Gérer le moment où les mises à jour de la protection doivent être téléchargées et appliquées</span><span class="sxs-lookup"><span data-stu-id="f8aaa-521">Manage when protection updates should be downloaded and applied</span></span>](manage-protection-update-schedule-microsoft-defender-antivirus.md) | <span data-ttu-id="f8aaa-522">Vous pouvez planifier le téléchargement des mises à jour de la protection.</span><span class="sxs-lookup"><span data-stu-id="f8aaa-522">You can schedule when protection updates should be downloaded.</span></span> |
|[<span data-ttu-id="f8aaa-523">Gérer les mises à jour des points de terminaison qui ne sont pas à jour</span><span class="sxs-lookup"><span data-stu-id="f8aaa-523">Manage updates for endpoints that are out of date</span></span>](manage-outdated-endpoints-microsoft-defender-antivirus.md) | <span data-ttu-id="f8aaa-524">Si un point de terminaison manque une mise à jour ou une analyse programmée, vous pouvez forcer une mise à jour ou une analyse la prochaine fois qu’un utilisateur se signe.</span><span class="sxs-lookup"><span data-stu-id="f8aaa-524">If an endpoint misses an update or scheduled scan, you can force an update or scan the next time a user signs in.</span></span> |
|[<span data-ttu-id="f8aaa-525">Gérer les mises à jour forcées en fonction des événements</span><span class="sxs-lookup"><span data-stu-id="f8aaa-525">Manage event-based forced updates</span></span>](manage-event-based-updates-microsoft-defender-antivirus.md) | <span data-ttu-id="f8aaa-526">Vous pouvez définir des mises à jour de protection à télécharger au démarrage ou après certains événements de protection livrés par le cloud.</span><span class="sxs-lookup"><span data-stu-id="f8aaa-526">You can set protection updates to be downloaded at startup or after certain cloud-delivered protection events.</span></span> |
|[<span data-ttu-id="f8aaa-527">Gérer les mises à jour pour les appareils mobiles et les machines virtuelles</span><span class="sxs-lookup"><span data-stu-id="f8aaa-527">Manage updates for mobile devices and virtual machines (VMs)</span></span>](manage-updates-mobile-devices-vms-microsoft-defender-antivirus.md)| <span data-ttu-id="f8aaa-528">Vous pouvez spécifier des paramètres, par exemple si des mises à jour doivent être mises à jour sur l’alimentation de la batterie, qui sont particulièrement utiles pour les appareils mobiles et les ordinateurs virtuels.</span><span class="sxs-lookup"><span data-stu-id="f8aaa-528">You can specify settings, such as whether updates should occur on battery power, that are especially useful for mobile devices and virtual machines.</span></span> |
