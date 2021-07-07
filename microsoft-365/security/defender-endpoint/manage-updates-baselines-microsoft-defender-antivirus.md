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
ms.reviewer: pahuijbr, mkaminska
manager: dansimp
ms.technology: mde
ms.date: 07/06/2021
ms.openlocfilehash: f64c71501a550aabdf16b9de2d7a5db93e48caef
ms.sourcegitcommit: 8b0718f5607ab509092cb80bda854010d885c54f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2021
ms.locfileid: "53314463"
---
# <a name="manage-microsoft-defender-antivirus-updates-and-apply-baselines"></a><span data-ttu-id="aeeef-104">Gérer les mises Antivirus Microsoft Defender jour et appliquer les lignes de base</span><span class="sxs-lookup"><span data-stu-id="aeeef-104">Manage Microsoft Defender Antivirus updates and apply baselines</span></span>

<span data-ttu-id="aeeef-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="aeeef-105">**Applies to:**</span></span>

- [<span data-ttu-id="aeeef-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="aeeef-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)
- <span data-ttu-id="aeeef-107">Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="aeeef-107">Microsoft Defender Antivirus</span></span>

<span data-ttu-id="aeeef-108">Le Antivirus Microsoft Defender à jour est essentiel pour garantir que vos appareils disposent des dernières technologies et fonctionnalités nécessaires pour se protéger contre les nouveaux programmes malveillants et les nouvelles techniques d’attaque.</span><span class="sxs-lookup"><span data-stu-id="aeeef-108">Keeping Microsoft Defender Antivirus up to date is critical to assure your devices have the latest technology and features needed to protect against new malware and attack techniques.</span></span> <span data-ttu-id="aeeef-109">Veillez à mettre à jour votre protection antivirus, même si Antivirus Microsoft Defender est en cours d’exécution en [mode passif.](microsoft-defender-antivirus-compatibility.md)</span><span class="sxs-lookup"><span data-stu-id="aeeef-109">Make sure to update your antivirus protection, even if Microsoft Defender Antivirus is running in [passive mode](microsoft-defender-antivirus-compatibility.md).</span></span> <span data-ttu-id="aeeef-110">Il existe deux types de mises à jour liées à la mise Antivirus Microsoft Defender jour :</span><span class="sxs-lookup"><span data-stu-id="aeeef-110">There are two types of updates related to keeping Microsoft Defender Antivirus up to date:</span></span>

- <span data-ttu-id="aeeef-111">Mises à jour de l’intelligence de la sécurité</span><span class="sxs-lookup"><span data-stu-id="aeeef-111">Security intelligence updates</span></span>
- <span data-ttu-id="aeeef-112">Mises à jour de produit</span><span class="sxs-lookup"><span data-stu-id="aeeef-112">Product updates</span></span>

> [!TIP]
> <span data-ttu-id="aeeef-113">Pour voir le moteur, la plateforme et la date de signature les plus à jour, consultez les mises à jour de l’intelligence de sécurité pour Antivirus Microsoft Defender logiciel [anti-programme malveillant Microsoft](https://www.microsoft.com/en-us/wdsi/defenderupdates)</span><span class="sxs-lookup"><span data-stu-id="aeeef-113">To see the most current engine, platform, and signature date, visit the [Security intelligence updates for Microsoft Defender Antivirus and other Microsoft antimalware](https://www.microsoft.com/en-us/wdsi/defenderupdates)</span></span>

## <a name="security-intelligence-updates"></a><span data-ttu-id="aeeef-114">Mises à jour de l’intelligence de la sécurité</span><span class="sxs-lookup"><span data-stu-id="aeeef-114">Security intelligence updates</span></span>

<span data-ttu-id="aeeef-115">Antivirus Microsoft Defender utilise la protection fournie par le [cloud](cloud-protection-microsoft-defender-antivirus.md) (également appelée Microsoft Advanced Protection Service ou MAPS) et télécharge régulièrement les mises à jour de l’intelligence de sécurité pour fournir une protection.</span><span class="sxs-lookup"><span data-stu-id="aeeef-115">Microsoft Defender Antivirus uses [cloud-delivered protection](cloud-protection-microsoft-defender-antivirus.md) (also called the Microsoft Advanced Protection Service or MAPS) and periodically downloads security intelligence updates to provide protection.</span></span>

> [!NOTE]
> <span data-ttu-id="aeeef-116">Les mises à jour sont publiées sous les numéros de la Ko ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="aeeef-116">Updates are released under the below KB numbers:</span></span>  
> - <span data-ttu-id="aeeef-117">Antivirus Microsoft Defender : KB2267602</span><span class="sxs-lookup"><span data-stu-id="aeeef-117">Microsoft Defender Antivirus: KB2267602</span></span>  
> - <span data-ttu-id="aeeef-118">System Center Endpoint Protection : KB2461484</span><span class="sxs-lookup"><span data-stu-id="aeeef-118">System Center Endpoint Protection: KB2461484</span></span>

<span data-ttu-id="aeeef-119">La protection cloud est toujours active et nécessite une connexion active à Internet pour fonctionner.</span><span class="sxs-lookup"><span data-stu-id="aeeef-119">Cloud-delivered protection is always on and requires an active connection to the Internet to function.</span></span> <span data-ttu-id="aeeef-120">Les mises à jour des informations de sécurité se produisent à une cadence programmée (configurable via une stratégie).</span><span class="sxs-lookup"><span data-stu-id="aeeef-120">Security intelligence updates occur on a scheduled cadence (configurable via policy).</span></span> <span data-ttu-id="aeeef-121">Pour plus d’informations, voir Utiliser la protection fournie par le [cloud microsoft dans Antivirus Microsoft Defender](cloud-protection-microsoft-defender-antivirus.md).</span><span class="sxs-lookup"><span data-stu-id="aeeef-121">For more information, see [Use Microsoft cloud-provided protection in Microsoft Defender Antivirus](cloud-protection-microsoft-defender-antivirus.md).</span></span> 

<span data-ttu-id="aeeef-122">Pour obtenir la liste des mises à jour récentes de l’intelligence de sécurité, voir Les mises à jour de l’intelligence de sécurité pour Antivirus Microsoft Defender logiciel [anti-programme](https://www.microsoft.com/en-us/wdsi/defenderupdates)malveillant Microsoft.</span><span class="sxs-lookup"><span data-stu-id="aeeef-122">For a list of recent security intelligence updates, see [Security intelligence updates for Microsoft Defender Antivirus and other Microsoft antimalware](https://www.microsoft.com/en-us/wdsi/defenderupdates).</span></span>

<span data-ttu-id="aeeef-123">Les mises à jour du moteur sont incluses dans les mises à jour de l’intelligence de sécurité et sont publiées à une cadence mensuelle.</span><span class="sxs-lookup"><span data-stu-id="aeeef-123">Engine updates are included with security intelligence updates and are released on a monthly cadence.</span></span>

## <a name="product-updates"></a><span data-ttu-id="aeeef-124">Mises à jour de produit</span><span class="sxs-lookup"><span data-stu-id="aeeef-124">Product updates</span></span>

<span data-ttu-id="aeeef-125">Antivirus Microsoft Defender nécessite des mises à jour [mensuelles (KB4052623)](https://support.microsoft.com/help/4052623/update-for-windows-defender-antimalware-platform) appelées mises à jour *de plateforme.*</span><span class="sxs-lookup"><span data-stu-id="aeeef-125">Microsoft Defender Antivirus requires [monthly updates (KB4052623)](https://support.microsoft.com/help/4052623/update-for-windows-defender-antimalware-platform) known as *platform updates*.</span></span>

<span data-ttu-id="aeeef-126">Vous pouvez gérer la distribution des mises à jour via l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="aeeef-126">You can manage the distribution of updates through one of the following methods:</span></span> 

- [<span data-ttu-id="aeeef-127">Windows Server Update Service (WSUS)</span><span class="sxs-lookup"><span data-stu-id="aeeef-127">Windows Server Update Service (WSUS)</span></span>](/mem/configmgr/protect/deploy-use/endpoint-definitions-wsus#to-synchronize-endpoint-protection-definition-updates-in-standalone-wsus)
- [<span data-ttu-id="aeeef-128">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="aeeef-128">Microsoft Endpoint Configuration Manager</span></span>](/configmgr/sum/understand/software-updates-introduction)
- <span data-ttu-id="aeeef-129">La méthode habituelle que vous utilisez pour déployer Microsoft et Windows mises à jour aux points de terminaison de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="aeeef-129">The usual method you use to deploy Microsoft and Windows updates to endpoints in your network.</span></span>

<span data-ttu-id="aeeef-130">Pour plus d’informations, [voir Gérer les sources pour les mises à jour Antivirus Microsoft Defender protection des données.](/mem/configmgr/protect/deploy-use/endpoint-definitions-wsus#to-synchronize-endpoint-protection-definition-updates-in-standalone-wsus)</span><span class="sxs-lookup"><span data-stu-id="aeeef-130">For more information, see [Manage the sources for Microsoft Defender Antivirus protection updates](/mem/configmgr/protect/deploy-use/endpoint-definitions-wsus#to-synchronize-endpoint-protection-definition-updates-in-standalone-wsus).</span></span>

> [!NOTE]
> - <span data-ttu-id="aeeef-131">Les mises à jour mensuelles sont publiées par phases, ce qui entraîne la mise à jour de plusieurs packages dans vos services de mise à jour [de serveur Window.](/windows-server/administration/windows-server-update-services/get-started/windows-server-update-services-wsus)</span><span class="sxs-lookup"><span data-stu-id="aeeef-131">Monthly updates are released in phases, resulting in multiple packages visible in your [Window Server Update Services](/windows-server/administration/windows-server-update-services/get-started/windows-server-update-services-wsus).</span></span>
> - <span data-ttu-id="aeeef-132">Cet article répertorie les modifications incluses dans le canal de publication étendu.</span><span class="sxs-lookup"><span data-stu-id="aeeef-132">This article lists changes that are included in the broad release channel.</span></span> <span data-ttu-id="aeeef-133">[Consultez la dernière version de canal étendu ici.](https://www.microsoft.com/security/encyclopedia/adlpackages.aspx?action=info)</span><span class="sxs-lookup"><span data-stu-id="aeeef-133">[See the latest broad channel release here](https://www.microsoft.com/security/encyclopedia/adlpackages.aspx?action=info).</span></span> 
> - <span data-ttu-id="aeeef-134">Pour en savoir plus sur le processus de déploiement progressif et pour plus d’informations sur la prochaine version, voir Gérer le processus de déploiement progressif pour les mises à jour [de Microsoft Defender.](manage-gradual-rollout.md)</span><span class="sxs-lookup"><span data-stu-id="aeeef-134">To learn more about the gradual rollout process, and to see more information about the next release, see [Manage the gradual rollout process for Microsoft Defender updates](manage-gradual-rollout.md).</span></span>
> - <span data-ttu-id="aeeef-135">Pour en savoir plus sur les mises à jour de l’intelligence de sécurité, consultez les mises à jour de l’intelligence de sécurité pour Antivirus Microsoft Defender logiciel [anti-programme](https://www.microsoft.com/wdsi/defenderupdates)malveillant Microsoft.</span><span class="sxs-lookup"><span data-stu-id="aeeef-135">To learn more about security intelligence updates, see [Security intelligence updates for Microsoft Defender Antivirus and other Microsoft antimalware](https://www.microsoft.com/wdsi/defenderupdates).</span></span> 

## <a name="monthly-platform-and-engine-versions"></a><span data-ttu-id="aeeef-136">Versions mensuelles de la plateforme et du moteur</span><span class="sxs-lookup"><span data-stu-id="aeeef-136">Monthly platform and engine versions</span></span>

<span data-ttu-id="aeeef-137">Pour plus d’informations sur la mise à jour ou l’installation de la mise à jour de la plateforme, voir [Update for Windows Defender antimalware platform](https://support.microsoft.com/help/4052623/update-for-windows-defender-antimalware-platform).</span><span class="sxs-lookup"><span data-stu-id="aeeef-137">For information how to update or install the platform update, see [Update for Windows Defender antimalware platform](https://support.microsoft.com/help/4052623/update-for-windows-defender-antimalware-platform).</span></span>

<span data-ttu-id="aeeef-138">Toutes nos mises à jour contiennent</span><span class="sxs-lookup"><span data-stu-id="aeeef-138">All our updates contain</span></span> 
- <span data-ttu-id="aeeef-139">améliorations des performances ;</span><span class="sxs-lookup"><span data-stu-id="aeeef-139">performance improvements;</span></span>
- <span data-ttu-id="aeeef-140">améliorations de la serviceabilité ; et</span><span class="sxs-lookup"><span data-stu-id="aeeef-140">serviceability improvements; and</span></span> 
- <span data-ttu-id="aeeef-141">améliorations de l’intégration (Cloud, [Microsoft 365 Defender](/microsoft-365/security/defender/microsoft-365-defender)).</span><span class="sxs-lookup"><span data-stu-id="aeeef-141">integration improvements (Cloud, [Microsoft 365 Defender](/microsoft-365/security/defender/microsoft-365-defender)).</span></span>
<br/>
<details>
<summary> <span data-ttu-id="aeeef-142">Juin-2021 (plateforme : 4.18.2106.5 | Moteur : 1.1.18300.4)</span><span class="sxs-lookup"><span data-stu-id="aeeef-142">June-2021 (Platform: 4.18.2106.5 | Engine: 1.1.18300.4)</span></span></summary>

<span data-ttu-id="aeeef-143">&ensp;Version de mise à jour des informations de sécurité **: 1.343.17.0**</span><span class="sxs-lookup"><span data-stu-id="aeeef-143">&ensp;Security intelligence update version: **1.343.17.0**</span></span>  
<span data-ttu-id="aeeef-144">&ensp;Publication : **28 juin 2021**</span><span class="sxs-lookup"><span data-stu-id="aeeef-144">&ensp;Released: **June 28, 2021**</span></span>  
<span data-ttu-id="aeeef-145">&ensp;Plateforme : **4.18.2106.5**</span><span class="sxs-lookup"><span data-stu-id="aeeef-145">&ensp;Platform: **4.18.2106.5**</span></span>  
<span data-ttu-id="aeeef-146">&ensp;Moteur : **1.1.18300.4**</span><span class="sxs-lookup"><span data-stu-id="aeeef-146">&ensp;Engine: **1.1.18300.4**</span></span>  
<span data-ttu-id="aeeef-147">&ensp;Phase de prise en charge **: Mises à jour critiques et de sécurité**</span><span class="sxs-lookup"><span data-stu-id="aeeef-147">&ensp;Support phase: **Security and Critical Updates**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="aeeef-148">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="aeeef-148">What's new</span></span>
- <span data-ttu-id="aeeef-149">Nouveaux contrôles pour la gestion du processus de déploiement progressif des mises à jour De Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="aeeef-149">New controls for managing the gradual rollout process of Microsoft Defender updates.</span></span> <span data-ttu-id="aeeef-150">Voir [Gérer le processus de déploiement progressif pour les mises à jour de Microsoft Defender.](manage-gradual-rollout.md)</span><span class="sxs-lookup"><span data-stu-id="aeeef-150">See [Manage the gradual rollout process for Microsoft Defender updates](manage-gradual-rollout.md).</span></span>
- <span data-ttu-id="aeeef-151">Amélioration du moteur d’analyse du comportement</span><span class="sxs-lookup"><span data-stu-id="aeeef-151">Improvement to the behavior monitoring engine</span></span>
- <span data-ttu-id="aeeef-152">Améliorations apportées au déploiement des définitions de logiciels anti-programme malveillant</span><span class="sxs-lookup"><span data-stu-id="aeeef-152">Improvements to the rollout of antimalware definitions</span></span>
- <span data-ttu-id="aeeef-153">Inspections des événements réseau Edge étendus</span><span class="sxs-lookup"><span data-stu-id="aeeef-153">Extended Edge network event inspections</span></span>

### <a name="known-issues"></a><span data-ttu-id="aeeef-154">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="aeeef-154">Known Issues</span></span>
<span data-ttu-id="aeeef-155">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="aeeef-155">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="aeeef-156">Mai-2021 (plateforme : 4.18.2105.4 | Moteur : 1.1.18200.4)</span><span class="sxs-lookup"><span data-stu-id="aeeef-156">May-2021 (Platform: 4.18.2105.4 | Engine: 1.1.18200.4)</span></span></summary>

<span data-ttu-id="aeeef-157">&ensp;Version de mise à jour des informations de sécurité **: 1.341.8.0**</span><span class="sxs-lookup"><span data-stu-id="aeeef-157">&ensp;Security intelligence update version: **1.341.8.0**</span></span>  
<span data-ttu-id="aeeef-158">&ensp;Publication : **3 juin 2021**</span><span class="sxs-lookup"><span data-stu-id="aeeef-158">&ensp;Released: **June 3, 2021**</span></span>  
<span data-ttu-id="aeeef-159">&ensp;Plateforme : **4.18.2105.4**</span><span class="sxs-lookup"><span data-stu-id="aeeef-159">&ensp;Platform: **4.18.2105.4**</span></span>  
<span data-ttu-id="aeeef-160">&ensp;Moteur : **1.1.18200.4**</span><span class="sxs-lookup"><span data-stu-id="aeeef-160">&ensp;Engine: **1.1.18200.4**</span></span>  
<span data-ttu-id="aeeef-161">&ensp;Phase de prise en charge **: Mises à jour critiques et de sécurité**</span><span class="sxs-lookup"><span data-stu-id="aeeef-161">&ensp;Support phase: **Security and Critical Updates**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="aeeef-162">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="aeeef-162">What's new</span></span>
- <span data-ttu-id="aeeef-163">Améliorations apportées à la [surveillance du comportement](client-behavioral-blocking.md)</span><span class="sxs-lookup"><span data-stu-id="aeeef-163">Improvements to [behavior monitoring](client-behavioral-blocking.md)</span></span> 
- <span data-ttu-id="aeeef-164">Fonctionnalité de [filtrage des](network-protection.md) notifications de protection réseau fixe</span><span class="sxs-lookup"><span data-stu-id="aeeef-164">Fixed [network protection](network-protection.md) notification filtering feature</span></span>

### <a name="known-issues"></a><span data-ttu-id="aeeef-165">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="aeeef-165">Known Issues</span></span>
<span data-ttu-id="aeeef-166">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="aeeef-166">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="aeeef-167">Avril-2021 (plateforme : 4.18.2104.14 | Moteur : 1.1.18100.5)</span><span class="sxs-lookup"><span data-stu-id="aeeef-167">April-2021 (Platform: 4.18.2104.14 | Engine: 1.1.18100.5)</span></span></summary>

<span data-ttu-id="aeeef-168">&ensp;Version de mise à jour des informations de sécurité **: 1.337.2.0**</span><span class="sxs-lookup"><span data-stu-id="aeeef-168">&ensp;Security intelligence update version: **1.337.2.0**</span></span>  
<span data-ttu-id="aeeef-169">&ensp;Publication : **26 avril 2021**  (moteur : 1.1.18100.6 publié le 5 mai 2021) Plateforme : &ensp; **4.18.2104.14**</span><span class="sxs-lookup"><span data-stu-id="aeeef-169">&ensp;Released: **April 26, 2021**  (Engine: 1.1.18100.6 released May 5, 2021) &ensp;Platform: **4.18.2104.14**</span></span>  
<span data-ttu-id="aeeef-170">&ensp;Moteur : **1.1.18100.5**</span><span class="sxs-lookup"><span data-stu-id="aeeef-170">&ensp;Engine: **1.1.18100.5**</span></span>  
<span data-ttu-id="aeeef-171">&ensp;Phase de prise en charge **: Mises à jour critiques et de sécurité**</span><span class="sxs-lookup"><span data-stu-id="aeeef-171">&ensp;Support phase: **Security and Critical Updates**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="aeeef-172">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="aeeef-172">What's new</span></span>
- <span data-ttu-id="aeeef-173">Logique d’analyse de comportement supplémentaire</span><span class="sxs-lookup"><span data-stu-id="aeeef-173">Additional behavior monitoring logic</span></span>
- <span data-ttu-id="aeeef-174">Détection améliorée de l’enregistreur de clés en mode noyau</span><span class="sxs-lookup"><span data-stu-id="aeeef-174">Improved kernel mode key logger detection</span></span>
- <span data-ttu-id="aeeef-175">Ajout de nouveaux contrôles pour gérer le processus de déploiement progressif pour [les mises à jour De Microsoft Defender](manage-gradual-rollout.md)</span><span class="sxs-lookup"><span data-stu-id="aeeef-175">Added new controls to manage the gradual rollout process for [Microsoft Defender updates](manage-gradual-rollout.md)</span></span>


### <a name="known-issues"></a><span data-ttu-id="aeeef-176">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="aeeef-176">Known Issues</span></span>
<span data-ttu-id="aeeef-177">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="aeeef-177">No known issues</span></span>  
<br/>
</details>

### <a name="previous-version-updates-technical-upgrade-support-only"></a><span data-ttu-id="aeeef-178">Mises à jour de version précédente : prise en charge de la mise à niveau technique uniquement</span><span class="sxs-lookup"><span data-stu-id="aeeef-178">Previous version updates: Technical upgrade support only</span></span>

<span data-ttu-id="aeeef-179">Après la publication d’une nouvelle version de package, la prise en charge des deux versions précédentes est réduite au support technique uniquement.</span><span class="sxs-lookup"><span data-stu-id="aeeef-179">After a new package version is released, support for the previous two versions is reduced to technical support only.</span></span> <span data-ttu-id="aeeef-180">Les versions antérieures à celles répertoriées dans cette section sont fournies uniquement pour la prise en charge de la mise à niveau technique.</span><span class="sxs-lookup"><span data-stu-id="aeeef-180">Versions older than that are listed in this section, and are provided for technical upgrade support only.</span></span> 
<details>
<summary> <span data-ttu-id="aeeef-181">Mars-2021 (plateforme : 4.18.2103.7 | Moteur : 1.1.18000.5)</span><span class="sxs-lookup"><span data-stu-id="aeeef-181">March-2021 (Platform: 4.18.2103.7 | Engine: 1.1.18000.5)</span></span></summary>

<span data-ttu-id="aeeef-182">&ensp;Version de mise à jour des informations de sécurité **: 1.335.36.0**</span><span class="sxs-lookup"><span data-stu-id="aeeef-182">&ensp;Security intelligence update version: **1.335.36.0**</span></span>  
<span data-ttu-id="aeeef-183">&ensp;Publication : **2 avril 2021**</span><span class="sxs-lookup"><span data-stu-id="aeeef-183">&ensp;Released: **April 2, 2021**</span></span>  
<span data-ttu-id="aeeef-184">&ensp;Plateforme : **4.18.2103.7**</span><span class="sxs-lookup"><span data-stu-id="aeeef-184">&ensp;Platform: **4.18.2103.7**</span></span>  
<span data-ttu-id="aeeef-185">&ensp;Moteur : **1.1.18000.5**</span><span class="sxs-lookup"><span data-stu-id="aeeef-185">&ensp;Engine: **1.1.18000.5**</span></span>  
<span data-ttu-id="aeeef-186">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="aeeef-186">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="aeeef-187">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="aeeef-187">What's new</span></span>

- <span data-ttu-id="aeeef-188">Amélioration du moteur d’analyse du comportement</span><span class="sxs-lookup"><span data-stu-id="aeeef-188">Improvement to the Behavior Monitoring engine</span></span> 
- <span data-ttu-id="aeeef-189">Préventions d’attaques par force brute du réseau étendu</span><span class="sxs-lookup"><span data-stu-id="aeeef-189">Expanded network brute-force-attack mitigations</span></span> 
- <span data-ttu-id="aeeef-190">Génération d’événements de tentative de falsification en échec supplémentaires lorsque la [protection](prevent-changes-to-security-settings-with-tamper-protection.md) contre la falsification est activée</span><span class="sxs-lookup"><span data-stu-id="aeeef-190">Additional failed tampering attempt event generation when [Tamper Protection](prevent-changes-to-security-settings-with-tamper-protection.md) is enabled</span></span>

### <a name="known-issues"></a><span data-ttu-id="aeeef-191">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="aeeef-191">Known Issues</span></span>
<span data-ttu-id="aeeef-192">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="aeeef-192">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="aeeef-193">Février-2021 (plateforme : 4.18.2102.3 | Moteur : 1.1.17900.7)</span><span class="sxs-lookup"><span data-stu-id="aeeef-193">February-2021 (Platform: 4.18.2102.3 | Engine: 1.1.17900.7)</span></span></summary>

<span data-ttu-id="aeeef-194">&ensp;Version de mise à jour des informations de sécurité **: 1.333.7.0**</span><span class="sxs-lookup"><span data-stu-id="aeeef-194">&ensp;Security intelligence update version: **1.333.7.0**</span></span>  
<span data-ttu-id="aeeef-195">&ensp;Publication : **9 mars 2021**</span><span class="sxs-lookup"><span data-stu-id="aeeef-195">&ensp;Released: **March 9, 2021**</span></span>  
<span data-ttu-id="aeeef-196">&ensp;Plateforme : **4.18.2102.3**</span><span class="sxs-lookup"><span data-stu-id="aeeef-196">&ensp;Platform: **4.18.2102.3**</span></span>  
<span data-ttu-id="aeeef-197">&ensp;Moteur : **1.1.17900.7**</span><span class="sxs-lookup"><span data-stu-id="aeeef-197">&ensp;Engine: **1.1.17900.7**</span></span>  
<span data-ttu-id="aeeef-198">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="aeeef-198">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="aeeef-199">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="aeeef-199">What's new</span></span>

- <span data-ttu-id="aeeef-200">Amélioration de la récupération du service par le biais [de la protection contre la falsification](prevent-changes-to-security-settings-with-tamper-protection.md)</span><span class="sxs-lookup"><span data-stu-id="aeeef-200">Improved service recovery through [tamper protection](prevent-changes-to-security-settings-with-tamper-protection.md)</span></span>
- <span data-ttu-id="aeeef-201">Étendre l’étendue de la protection contre la falsification</span><span class="sxs-lookup"><span data-stu-id="aeeef-201">Extend tamper protection scope</span></span>

### <a name="known-issues"></a><span data-ttu-id="aeeef-202">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="aeeef-202">Known Issues</span></span>
<span data-ttu-id="aeeef-203">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="aeeef-203">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="aeeef-204">Janvier-2021 (plateforme : 4.18.2101.9 | Moteur : 1.1.17800.5)</span><span class="sxs-lookup"><span data-stu-id="aeeef-204">January-2021 (Platform: 4.18.2101.9 | Engine: 1.1.17800.5)</span></span></summary>

<span data-ttu-id="aeeef-205">&ensp;Version de mise à jour des informations de sécurité **: 1.327.1854.0**</span><span class="sxs-lookup"><span data-stu-id="aeeef-205">&ensp;Security intelligence update version: **1.327.1854.0**</span></span>  
<span data-ttu-id="aeeef-206">&ensp;Publication : **2 février 2021**</span><span class="sxs-lookup"><span data-stu-id="aeeef-206">&ensp;Released: **February 2, 2021**</span></span>  
<span data-ttu-id="aeeef-207">&ensp;Plateforme : **4.18.2101.9**</span><span class="sxs-lookup"><span data-stu-id="aeeef-207">&ensp;Platform: **4.18.2101.9**</span></span>  
<span data-ttu-id="aeeef-208">&ensp;Moteur : **1.1.17800.5**</span><span class="sxs-lookup"><span data-stu-id="aeeef-208">&ensp;Engine: **1.1.17800.5**</span></span>  
<span data-ttu-id="aeeef-209">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="aeeef-209">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="aeeef-210">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="aeeef-210">What's new</span></span>

- <span data-ttu-id="aeeef-211">Améliorations de la détection d’exploits shellcode</span><span class="sxs-lookup"><span data-stu-id="aeeef-211">Shellcode exploit detection improvements</span></span>
- <span data-ttu-id="aeeef-212">Visibilité accrue des tentatives de vol d’informations d’identification</span><span class="sxs-lookup"><span data-stu-id="aeeef-212">Increased visibility for credential stealing attempts</span></span>
- <span data-ttu-id="aeeef-213">Améliorations des fonctionnalités antitampering dans Antivirus Microsoft Defender services</span><span class="sxs-lookup"><span data-stu-id="aeeef-213">Improvements in antitampering features in Microsoft Defender Antivirus services</span></span>
- <span data-ttu-id="aeeef-214">Prise en charge améliorée de l ARM éulation x64</span><span class="sxs-lookup"><span data-stu-id="aeeef-214">Improved support for ARM x64 emulation</span></span>
- <span data-ttu-id="aeeef-215">Correctif : PEPT notification de blocage reste dans l’historique des menaces après la détection initiale de la protection en temps réel</span><span class="sxs-lookup"><span data-stu-id="aeeef-215">Fix: EDR Block notification remains in threat history after real-time protection performed initial detection</span></span>

### <a name="known-issues"></a><span data-ttu-id="aeeef-216">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="aeeef-216">Known Issues</span></span>
<span data-ttu-id="aeeef-217">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="aeeef-217">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="aeeef-218">Novembre-2020 (plateforme : 4.18.2011.6 | Moteur : 1.1.17700.4)</span><span class="sxs-lookup"><span data-stu-id="aeeef-218">November-2020 (Platform: 4.18.2011.6 | Engine: 1.1.17700.4)</span></span></summary>

<span data-ttu-id="aeeef-219">&ensp;Version de mise à jour des informations de sécurité **: 1.327.1854.0**</span><span class="sxs-lookup"><span data-stu-id="aeeef-219">&ensp;Security intelligence update version: **1.327.1854.0**</span></span>  
<span data-ttu-id="aeeef-220">&ensp;Publication : **03 décembre 2020**</span><span class="sxs-lookup"><span data-stu-id="aeeef-220">&ensp;Released: **December 03, 2020**</span></span>  
<span data-ttu-id="aeeef-221">&ensp;Plateforme : **4.18.2011.6**</span><span class="sxs-lookup"><span data-stu-id="aeeef-221">&ensp;Platform: **4.18.2011.6**</span></span>  
<span data-ttu-id="aeeef-222">&ensp;Moteur : **1.1.17700.4**</span><span class="sxs-lookup"><span data-stu-id="aeeef-222">&ensp;Engine: **1.1.17700.4**</span></span>  
<span data-ttu-id="aeeef-223">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="aeeef-223">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="aeeef-224">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="aeeef-224">What's new</span></span>

- <span data-ttu-id="aeeef-225">Amélioration de la [journalisation de la prise en](/windows/security/threat-protection/microsoft-defender-smartscreen/microsoft-defender-smartscreen-overview) charge de l’état SmartScreen</span><span class="sxs-lookup"><span data-stu-id="aeeef-225">Improved [SmartScreen](/windows/security/threat-protection/microsoft-defender-smartscreen/microsoft-defender-smartscreen-overview) status support logging</span></span>

### <a name="known-issues"></a><span data-ttu-id="aeeef-226">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="aeeef-226">Known Issues</span></span>
<span data-ttu-id="aeeef-227">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="aeeef-227">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="aeeef-228">Octobre-2020 (plateforme : 4.18.2010.7 | Moteur : 1.1.17600.5)</span><span class="sxs-lookup"><span data-stu-id="aeeef-228">October-2020 (Platform: 4.18.2010.7 | Engine: 1.1.17600.5)</span></span></summary>

<span data-ttu-id="aeeef-229">&ensp;Version de mise à jour des informations de sécurité **: 1.327.7.0**</span><span class="sxs-lookup"><span data-stu-id="aeeef-229">&ensp;Security intelligence update version: **1.327.7.0**</span></span>  
<span data-ttu-id="aeeef-230">&ensp;Publication : **29 octobre 2020**</span><span class="sxs-lookup"><span data-stu-id="aeeef-230">&ensp;Released: **October 29, 2020**</span></span>  
<span data-ttu-id="aeeef-231">&ensp;Plateforme : **4.18.2010.7**</span><span class="sxs-lookup"><span data-stu-id="aeeef-231">&ensp;Platform: **4.18.2010.7**</span></span>  
<span data-ttu-id="aeeef-232">&ensp;Moteur : **1.1.17600.5**</span><span class="sxs-lookup"><span data-stu-id="aeeef-232">&ensp;Engine: **1.1.17600.5**</span></span>  
<span data-ttu-id="aeeef-233">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="aeeef-233">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="aeeef-234">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="aeeef-234">What's new</span></span>

- <span data-ttu-id="aeeef-235">Nouvelles descriptions pour les catégories de menaces spéciales</span><span class="sxs-lookup"><span data-stu-id="aeeef-235">New descriptions for special threat categories</span></span>
- <span data-ttu-id="aeeef-236">Fonctionnalités d’émulation améliorées</span><span class="sxs-lookup"><span data-stu-id="aeeef-236">Improved emulation capabilities</span></span>
- <span data-ttu-id="aeeef-237">Fonctionnalités améliorées d’autoriser/de bloquer l’adresse hôte</span><span class="sxs-lookup"><span data-stu-id="aeeef-237">Improved host address allow/block capabilities</span></span>
- <span data-ttu-id="aeeef-238">Nouvelle option dans le programme CSP Defender pour ignorer la fusion des exclusions des utilisateurs locaux</span><span class="sxs-lookup"><span data-stu-id="aeeef-238">New option in Defender CSP to Ignore merging of local user exclusions</span></span>

### <a name="known-issues"></a><span data-ttu-id="aeeef-239">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="aeeef-239">Known Issues</span></span>

<span data-ttu-id="aeeef-240">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="aeeef-240">No known issues</span></span>  
<br/>
</details><details>
<summary> <span data-ttu-id="aeeef-241">Septembre-2020 (plateforme : 4.18.2009.7 | Moteur : 1.1.17500.4)</span><span class="sxs-lookup"><span data-stu-id="aeeef-241">September-2020 (Platform: 4.18.2009.7 | Engine: 1.1.17500.4)</span></span></summary>

<span data-ttu-id="aeeef-242">&ensp;Version de mise à jour des informations de sécurité **: 1.325.10.0**</span><span class="sxs-lookup"><span data-stu-id="aeeef-242">&ensp;Security intelligence update version: **1.325.10.0**</span></span>  
<span data-ttu-id="aeeef-243">&ensp;Publication : **01 octobre 2020**</span><span class="sxs-lookup"><span data-stu-id="aeeef-243">&ensp;Released: **October 01, 2020**</span></span>  
<span data-ttu-id="aeeef-244">&ensp;Plateforme : **4.18.2009.7**</span><span class="sxs-lookup"><span data-stu-id="aeeef-244">&ensp;Platform: **4.18.2009.7**</span></span>  
<span data-ttu-id="aeeef-245">&ensp;Moteur : **1.1.17500.4**</span><span class="sxs-lookup"><span data-stu-id="aeeef-245">&ensp;Engine: **1.1.17500.4**</span></span>  
<span data-ttu-id="aeeef-246">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="aeeef-246">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="aeeef-247">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="aeeef-247">What's new</span></span>

- <span data-ttu-id="aeeef-248">Des autorisations d’administrateur sont requises pour restaurer les fichiers en quarantaine</span><span class="sxs-lookup"><span data-stu-id="aeeef-248">Admin permissions are required to restore files in quarantine</span></span>
- <span data-ttu-id="aeeef-249">Les événements au format XML sont désormais pris en charge</span><span class="sxs-lookup"><span data-stu-id="aeeef-249">XML formatted events are now supported</span></span>
- <span data-ttu-id="aeeef-250">Prise en charge du programme CSP pour ignorer les fusions d’exclusions</span><span class="sxs-lookup"><span data-stu-id="aeeef-250">CSP support for ignoring exclusion merges</span></span>
- <span data-ttu-id="aeeef-251">Nouvelles interfaces de gestion pour :</span><span class="sxs-lookup"><span data-stu-id="aeeef-251">New management interfaces for:</span></span>
   - <span data-ttu-id="aeeef-252">UDP Inspection</span><span class="sxs-lookup"><span data-stu-id="aeeef-252">UDP Inspection</span></span>
   - <span data-ttu-id="aeeef-253">Protection du réseau sur Server 2019</span><span class="sxs-lookup"><span data-stu-id="aeeef-253">Network Protection on Server 2019</span></span>
   - <span data-ttu-id="aeeef-254">Exclusions d’adresses IP pour la protection du réseau</span><span class="sxs-lookup"><span data-stu-id="aeeef-254">IP Address exclusions for Network Protection</span></span>
- <span data-ttu-id="aeeef-255">Meilleure visibilité des mesures du TPM</span><span class="sxs-lookup"><span data-stu-id="aeeef-255">Improved visibility into TPM measurements</span></span>
- <span data-ttu-id="aeeef-256">Amélioration de l Office de module VBA</span><span class="sxs-lookup"><span data-stu-id="aeeef-256">Improved Office VBA module scanning</span></span>

### <a name="known-issues"></a><span data-ttu-id="aeeef-257">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="aeeef-257">Known Issues</span></span>

<span data-ttu-id="aeeef-258">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="aeeef-258">No known issues</span></span>  
<br/>
</details>
<details>
<summary> <span data-ttu-id="aeeef-259">Août-2020 (plateforme : 4.18.2008.9 | Moteur : 1.1.17400.5)</span><span class="sxs-lookup"><span data-stu-id="aeeef-259">August-2020 (Platform: 4.18.2008.9 | Engine: 1.1.17400.5)</span></span></summary>

<span data-ttu-id="aeeef-260">&ensp;Version de mise à jour des informations de sécurité **: 1.323.9.0**</span><span class="sxs-lookup"><span data-stu-id="aeeef-260">&ensp;Security intelligence update version: **1.323.9.0**</span></span>  
<span data-ttu-id="aeeef-261">&ensp;Publication : **27 août 2020**</span><span class="sxs-lookup"><span data-stu-id="aeeef-261">&ensp;Released: **August 27, 2020**</span></span>  
<span data-ttu-id="aeeef-262">&ensp;Plateforme : **4.18.2008.9**</span><span class="sxs-lookup"><span data-stu-id="aeeef-262">&ensp;Platform: **4.18.2008.9**</span></span>  
<span data-ttu-id="aeeef-263">&ensp;Moteur : **1.1.17400.5**</span><span class="sxs-lookup"><span data-stu-id="aeeef-263">&ensp;Engine: **1.1.17400.5**</span></span>  
<span data-ttu-id="aeeef-264">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="aeeef-264">&ensp;Support phase: **Technical upgrade support (only)**</span></span>

### <a name="whats-new"></a><span data-ttu-id="aeeef-265">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="aeeef-265">What's new</span></span>

- <span data-ttu-id="aeeef-266">Ajouter d’autres événements de télémétrie</span><span class="sxs-lookup"><span data-stu-id="aeeef-266">Add more telemetry events</span></span>
- <span data-ttu-id="aeeef-267">Télémétrie améliorée des événements d’analyse</span><span class="sxs-lookup"><span data-stu-id="aeeef-267">Improved scan event telemetry</span></span>
- <span data-ttu-id="aeeef-268">Amélioration de la surveillance du comportement pour les analyses de mémoire</span><span class="sxs-lookup"><span data-stu-id="aeeef-268">Improved behavior monitoring for memory scans</span></span>
- <span data-ttu-id="aeeef-269">Amélioration de l’analyse des flux de macros</span><span class="sxs-lookup"><span data-stu-id="aeeef-269">Improved macro streams scanning</span></span>
- <span data-ttu-id="aeeef-270">Ajouté à `AMRunningMode` la Get-MpComputerStatus cmdlet PowerShell</span><span class="sxs-lookup"><span data-stu-id="aeeef-270">Added `AMRunningMode` to Get-MpComputerStatus PowerShell cmdlet</span></span>
- <span data-ttu-id="aeeef-271">[DisableAntiSpyware](/windows-hardware/customize/desktop/unattend/security-malware-windows-defender-disableantispyware) est ignoré.</span><span class="sxs-lookup"><span data-stu-id="aeeef-271">[DisableAntiSpyware](/windows-hardware/customize/desktop/unattend/security-malware-windows-defender-disableantispyware) is ignored.</span></span> <span data-ttu-id="aeeef-272">Antivirus Microsoft Defender s’arrête automatiquement lorsqu’il détecte un autre programme antivirus.</span><span class="sxs-lookup"><span data-stu-id="aeeef-272">Microsoft Defender Antivirus automatically turns itself off when it detects another antivirus program.</span></span>


### <a name="known-issues"></a><span data-ttu-id="aeeef-273">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="aeeef-273">Known Issues</span></span>
<span data-ttu-id="aeeef-274">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="aeeef-274">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="aeeef-275">Juillet-2020 (plateforme : 4.18.2007.8 | Moteur : 1.1.17300.4)</span><span class="sxs-lookup"><span data-stu-id="aeeef-275">July-2020 (Platform: 4.18.2007.8 | Engine: 1.1.17300.4)</span></span></summary>

<span data-ttu-id="aeeef-276">&ensp;Version de mise à jour des informations de sécurité **: 1.321.30.0**</span><span class="sxs-lookup"><span data-stu-id="aeeef-276">&ensp;Security intelligence update version: **1.321.30.0**</span></span>  
<span data-ttu-id="aeeef-277">&ensp;Publication : **28 juillet 2020**</span><span class="sxs-lookup"><span data-stu-id="aeeef-277">&ensp;Released: **July 28, 2020**</span></span>  
<span data-ttu-id="aeeef-278">&ensp;Plateforme : **4.18.2007.8**</span><span class="sxs-lookup"><span data-stu-id="aeeef-278">&ensp;Platform: **4.18.2007.8**</span></span>  
<span data-ttu-id="aeeef-279">&ensp;Moteur : **1.1.17300.4**</span><span class="sxs-lookup"><span data-stu-id="aeeef-279">&ensp;Engine: **1.1.17300.4**</span></span>  
<span data-ttu-id="aeeef-280">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="aeeef-280">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="aeeef-281">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="aeeef-281">What's new</span></span>

- <span data-ttu-id="aeeef-282">Télémétrie améliorée pour BITS</span><span class="sxs-lookup"><span data-stu-id="aeeef-282">Improved telemetry for BITS</span></span>
- <span data-ttu-id="aeeef-283">Validation améliorée du certificat de signature de code Authenticode</span><span class="sxs-lookup"><span data-stu-id="aeeef-283">Improved Authenticode code signing certificate validation</span></span>

### <a name="known-issues"></a><span data-ttu-id="aeeef-284">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="aeeef-284">Known Issues</span></span>
<span data-ttu-id="aeeef-285">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="aeeef-285">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="aeeef-286">Juin-2020 (plateforme : 4.18.2006.10 | Moteur : 1.1.17200.2)</span><span class="sxs-lookup"><span data-stu-id="aeeef-286">June-2020 (Platform: 4.18.2006.10 | Engine: 1.1.17200.2)</span></span></summary>

<span data-ttu-id="aeeef-287">&ensp;Version de mise à jour des informations de sécurité **: 1.319.20.0**</span><span class="sxs-lookup"><span data-stu-id="aeeef-287">&ensp;Security intelligence update version: **1.319.20.0**</span></span>  
<span data-ttu-id="aeeef-288">&ensp;Publication : **22 juin 2020**</span><span class="sxs-lookup"><span data-stu-id="aeeef-288">&ensp;Released: **June 22, 2020**</span></span>  
<span data-ttu-id="aeeef-289">&ensp;Plateforme : **4.18.2006.10**</span><span class="sxs-lookup"><span data-stu-id="aeeef-289">&ensp;Platform: **4.18.2006.10**</span></span>  
<span data-ttu-id="aeeef-290">&ensp;Moteur : **1.1.17200.2**</span><span class="sxs-lookup"><span data-stu-id="aeeef-290">&ensp;Engine: **1.1.17200.2**</span></span>  
<span data-ttu-id="aeeef-291">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="aeeef-291">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="aeeef-292">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="aeeef-292">What's new</span></span>

- <span data-ttu-id="aeeef-293">Possibilité de spécifier [l’emplacement des journaux de support](./collect-diagnostic-data.md)</span><span class="sxs-lookup"><span data-stu-id="aeeef-293">Possibility to specify the [location of the support logs](./collect-diagnostic-data.md)</span></span>
- <span data-ttu-id="aeeef-294">Ignorer l’analyse de rattrapage agressive en mode passif.</span><span class="sxs-lookup"><span data-stu-id="aeeef-294">Skipping aggressive catchup scan in Passive mode.</span></span>
- <span data-ttu-id="aeeef-295">Autoriser Defender à se mettre à jour sur les connexions à connexions avec des compteurs</span><span class="sxs-lookup"><span data-stu-id="aeeef-295">Allow Defender to update on metered connections</span></span>
- <span data-ttu-id="aeeef-296">Réglage des performances fixes lorsque la mise en cache est désactivée</span><span class="sxs-lookup"><span data-stu-id="aeeef-296">Fixed performance tuning when caching is disabled</span></span> 
- <span data-ttu-id="aeeef-297">Requête de Registre fixe</span><span class="sxs-lookup"><span data-stu-id="aeeef-297">Fixed registry query</span></span> 
- <span data-ttu-id="aeeef-298">Randomisation du scantime fixe dans ADMX</span><span class="sxs-lookup"><span data-stu-id="aeeef-298">Fixed scantime randomization in ADMX</span></span>

### <a name="known-issues"></a><span data-ttu-id="aeeef-299">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="aeeef-299">Known Issues</span></span>
<span data-ttu-id="aeeef-300">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="aeeef-300">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="aeeef-301">Mai-2020 (plateforme : 4.18.2005.4 | Moteur : 1.1.17100.2)</span><span class="sxs-lookup"><span data-stu-id="aeeef-301">May-2020 (Platform: 4.18.2005.4 | Engine: 1.1.17100.2)</span></span></summary>

<span data-ttu-id="aeeef-302">&ensp;Version de mise à jour des informations de sécurité **: 1.317.20.0**</span><span class="sxs-lookup"><span data-stu-id="aeeef-302">&ensp;Security intelligence update version: **1.317.20.0**</span></span>  
<span data-ttu-id="aeeef-303">&ensp;Publication : **26 mai 2020**</span><span class="sxs-lookup"><span data-stu-id="aeeef-303">&ensp;Released: **May 26, 2020**</span></span>  
<span data-ttu-id="aeeef-304">&ensp;Plateforme : **4.18.2005.4**</span><span class="sxs-lookup"><span data-stu-id="aeeef-304">&ensp;Platform: **4.18.2005.4**</span></span>  
<span data-ttu-id="aeeef-305">&ensp;Moteur : **1.1.17100.2**</span><span class="sxs-lookup"><span data-stu-id="aeeef-305">&ensp;Engine: **1.1.17100.2**</span></span>  
<span data-ttu-id="aeeef-306">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="aeeef-306">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="aeeef-307">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="aeeef-307">What's new</span></span>

- <span data-ttu-id="aeeef-308">Enregistrement amélioré pour les événements d’analyse</span><span class="sxs-lookup"><span data-stu-id="aeeef-308">Improved logging for scan events</span></span>
- <span data-ttu-id="aeeef-309">Amélioration de la gestion des incidents en mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="aeeef-309">Improved user mode crash handling.</span></span>
- <span data-ttu-id="aeeef-310">Suivi des événements ajouté pour la protection contre la falsification</span><span class="sxs-lookup"><span data-stu-id="aeeef-310">Added event tracing for Tamper protection</span></span>
- <span data-ttu-id="aeeef-311">Envoi d’exemples AMSI fixes</span><span class="sxs-lookup"><span data-stu-id="aeeef-311">Fixed AMSI Sample submission</span></span>
- <span data-ttu-id="aeeef-312">Blocage du cloud AMSI fixe</span><span class="sxs-lookup"><span data-stu-id="aeeef-312">Fixed AMSI Cloud blocking</span></span>
- <span data-ttu-id="aeeef-313">Journal d’installation des mises à jour de sécurité fixes</span><span class="sxs-lookup"><span data-stu-id="aeeef-313">Fixed Security update install log</span></span>

### <a name="known-issues"></a><span data-ttu-id="aeeef-314">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="aeeef-314">Known Issues</span></span>
<span data-ttu-id="aeeef-315">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="aeeef-315">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="aeeef-316">Avril-2020 (plateforme : 4.18.2004.6 | Moteur : 1.1.17000.2)</span><span class="sxs-lookup"><span data-stu-id="aeeef-316">April-2020 (Platform: 4.18.2004.6 | Engine: 1.1.17000.2)</span></span></summary>

<span data-ttu-id="aeeef-317">&ensp;Version de mise à jour des informations de sécurité **: 1.315.12.0**</span><span class="sxs-lookup"><span data-stu-id="aeeef-317">&ensp;Security intelligence update version: **1.315.12.0**</span></span>  
<span data-ttu-id="aeeef-318">&ensp;Publication : **30 avril 2020**</span><span class="sxs-lookup"><span data-stu-id="aeeef-318">&ensp;Released: **April 30, 2020**</span></span>  
<span data-ttu-id="aeeef-319">&ensp;Plateforme : **4.18.2004.6**</span><span class="sxs-lookup"><span data-stu-id="aeeef-319">&ensp;Platform: **4.18.2004.6**</span></span>  
<span data-ttu-id="aeeef-320">&ensp;Moteur : **1.1.17000.2**</span><span class="sxs-lookup"><span data-stu-id="aeeef-320">&ensp;Engine: **1.1.17000.2**</span></span>  
<span data-ttu-id="aeeef-321">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="aeeef-321">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="aeeef-322">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="aeeef-322">What's new</span></span>
- <span data-ttu-id="aeeef-323">Améliorations apportées aux filtres WDfilter</span><span class="sxs-lookup"><span data-stu-id="aeeef-323">WDfilter improvements</span></span>
- <span data-ttu-id="aeeef-324">Ajouter des données d’événements actionnables à des événements de détection de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="aeeef-324">Add more actionable event data to attack surface reduction detection events</span></span>
- <span data-ttu-id="aeeef-325">Informations de version fixes dans les données de diagnostic et WMI</span><span class="sxs-lookup"><span data-stu-id="aeeef-325">Fixed version information in diagnostic data and WMI</span></span>
- <span data-ttu-id="aeeef-326">Version de plateforme incorrecte corrigée dans l’interface utilisateur après la mise à jour de la plateforme</span><span class="sxs-lookup"><span data-stu-id="aeeef-326">Fixed incorrect platform version in UI after platform update</span></span>
- <span data-ttu-id="aeeef-327">Intel d’URL dynamique pour la protection contre les menaces sans fichier</span><span class="sxs-lookup"><span data-stu-id="aeeef-327">Dynamic URL intel for Fileless threat protection</span></span>
- <span data-ttu-id="aeeef-328">Fonctionnalité d’analyse UEFI</span><span class="sxs-lookup"><span data-stu-id="aeeef-328">UEFI scan capability</span></span>
- <span data-ttu-id="aeeef-329">Étendre la journalisation pour les mises à jour</span><span class="sxs-lookup"><span data-stu-id="aeeef-329">Extend logging for updates</span></span>

### <a name="known-issues"></a><span data-ttu-id="aeeef-330">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="aeeef-330">Known Issues</span></span>
<span data-ttu-id="aeeef-331">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="aeeef-331">No known issues</span></span>  
<br/>
</details>

<details>
<summary> <span data-ttu-id="aeeef-332">Mars-2020 (plateforme : 4.18.2003.8 | Moteur : 1.1.16900.2)</span><span class="sxs-lookup"><span data-stu-id="aeeef-332">March-2020 (Platform: 4.18.2003.8 | Engine: 1.1.16900.2)</span></span></summary>

<span data-ttu-id="aeeef-333">&ensp;Version de mise à jour des informations de sécurité **: 1.313.8.0**</span><span class="sxs-lookup"><span data-stu-id="aeeef-333">&ensp;Security intelligence update version: **1.313.8.0**</span></span>  
<span data-ttu-id="aeeef-334">&ensp;Publication : **24 mars 2020**</span><span class="sxs-lookup"><span data-stu-id="aeeef-334">&ensp;Released: **March 24, 2020**</span></span>  
<span data-ttu-id="aeeef-335">&ensp;Plateforme : **4.18.2003.8**</span><span class="sxs-lookup"><span data-stu-id="aeeef-335">&ensp;Platform: **4.18.2003.8**</span></span>  
<span data-ttu-id="aeeef-336">&ensp;Moteur : **1.1.16900.4**</span><span class="sxs-lookup"><span data-stu-id="aeeef-336">&ensp;Engine: **1.1.16900.4**</span></span>  
<span data-ttu-id="aeeef-337">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="aeeef-337">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
    
### <a name="whats-new"></a><span data-ttu-id="aeeef-338">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="aeeef-338">What's new</span></span>

- <span data-ttu-id="aeeef-339">Option limitation du processeur ajoutée à [MpCmdRun](./command-line-arguments-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="aeeef-339">CPU Throttling option added to [MpCmdRun](./command-line-arguments-microsoft-defender-antivirus.md)</span></span>
- <span data-ttu-id="aeeef-340">Améliorer les fonctionnalités de diagnostic</span><span class="sxs-lookup"><span data-stu-id="aeeef-340">Improve diagnostic capability</span></span>
- <span data-ttu-id="aeeef-341">réduire le délai d’out des informations de sécurité (5 min)</span><span class="sxs-lookup"><span data-stu-id="aeeef-341">reduce Security intelligence timeout (5 min)</span></span>
- <span data-ttu-id="aeeef-342">Étendre la fonctionnalité de journal interne du moteur AMSI</span><span class="sxs-lookup"><span data-stu-id="aeeef-342">Extend AMSI engine internal log capability</span></span>
- <span data-ttu-id="aeeef-343">Améliorer la notification pour le blocage des processus</span><span class="sxs-lookup"><span data-stu-id="aeeef-343">Improve notification for process blocking</span></span>
   
### <a name="known-issues"></a><span data-ttu-id="aeeef-344">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="aeeef-344">Known Issues</span></span>
<span data-ttu-id="aeeef-345">[**Fixe**] Antivirus Microsoft Defender ignorer les fichiers lors de l’exécution d’une analyse.</span><span class="sxs-lookup"><span data-stu-id="aeeef-345">[**Fixed**] Microsoft Defender Antivirus is skipping files when running a scan.</span></span>

<br/>
</details>

<details>

<summary> <span data-ttu-id="aeeef-346">Février-2020 (plateforme : - | Moteur : 1.1.16800.2)</span><span class="sxs-lookup"><span data-stu-id="aeeef-346">February-2020 (Platform: - | Engine: 1.1.16800.2)</span></span></summary>
  

<span data-ttu-id="aeeef-347">&ensp;Version de mise à jour des informations de sécurité **: 1.311.4.0** </span><span class="sxs-lookup"><span data-stu-id="aeeef-347">&ensp;Security intelligence update version: **1.311.4.0** </span></span>  
<span data-ttu-id="aeeef-348">&ensp;Publication : **25 février 2020**</span><span class="sxs-lookup"><span data-stu-id="aeeef-348">&ensp;Released: **February 25, 2020**</span></span>  
<span data-ttu-id="aeeef-349">&ensp;Plateforme/client : **-**</span><span class="sxs-lookup"><span data-stu-id="aeeef-349">&ensp;Platform/Client: **-**</span></span>  
<span data-ttu-id="aeeef-350">&ensp;Moteur : **1.1.16800.2**</span><span class="sxs-lookup"><span data-stu-id="aeeef-350">&ensp;Engine: **1.1.16800.2**</span></span>  
<span data-ttu-id="aeeef-351">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="aeeef-351">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
     
### <a name="whats-new"></a><span data-ttu-id="aeeef-352">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="aeeef-352">What's new</span></span>

  
### <a name="known-issues"></a><span data-ttu-id="aeeef-353">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="aeeef-353">Known Issues</span></span>
<span data-ttu-id="aeeef-354">Aucun problème connu</span><span class="sxs-lookup"><span data-stu-id="aeeef-354">No known issues</span></span>
<br/>
</details>

<details>
<summary> <span data-ttu-id="aeeef-355">Janvier-2020 (plateforme : 4.18.2001.10 | Moteur : 1.1.16700.2)</span><span class="sxs-lookup"><span data-stu-id="aeeef-355">January-2020 (Platform: 4.18.2001.10 | Engine: 1.1.16700.2)</span></span></summary>
  

<span data-ttu-id="aeeef-356">Version de mise à jour des informations de sécurité **: 1.309.32.0**</span><span class="sxs-lookup"><span data-stu-id="aeeef-356">Security intelligence update version: **1.309.32.0**</span></span>  
<span data-ttu-id="aeeef-357">Publication : **30 janvier 2020**</span><span class="sxs-lookup"><span data-stu-id="aeeef-357">Released: **January 30, 2020**</span></span>  
<span data-ttu-id="aeeef-358">Plateforme/Client : **4.18.2001.10**</span><span class="sxs-lookup"><span data-stu-id="aeeef-358">Platform/Client: **4.18.2001.10**</span></span>  
<span data-ttu-id="aeeef-359">Moteur : **1.1.16700.2**</span><span class="sxs-lookup"><span data-stu-id="aeeef-359">Engine: **1.1.16700.2**</span></span>  
<span data-ttu-id="aeeef-360">&ensp;Phase de support : **prise en charge de la mise à niveau technique (uniquement)**</span><span class="sxs-lookup"><span data-stu-id="aeeef-360">&ensp;Support phase: **Technical upgrade support (only)**</span></span>
     
### <a name="whats-new"></a><span data-ttu-id="aeeef-361">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="aeeef-361">What's new</span></span>

- <span data-ttu-id="aeeef-362">Correction du BSOD sur WS2016 avec Exchange</span><span class="sxs-lookup"><span data-stu-id="aeeef-362">Fixed BSOD on WS2016 with Exchange</span></span>
- <span data-ttu-id="aeeef-363">Prise en charge des mises à jour de plateforme lorsque le TMP est redirigé vers le chemin d’accès réseau</span><span class="sxs-lookup"><span data-stu-id="aeeef-363">Support platform updates when TMP is redirected to network path</span></span>
- <span data-ttu-id="aeeef-364">Les versions de plateforme et de moteur sont [ajoutées à WDSI](https://www.microsoft.com/en-us/wdsi/defenderupdates)</span><span class="sxs-lookup"><span data-stu-id="aeeef-364">Platform and engine versions are added to [WDSI](https://www.microsoft.com/en-us/wdsi/defenderupdates)</span></span> <!-- The preceding URL must include "/en-us" -->
- <span data-ttu-id="aeeef-365">étendre la mise à jour des signatures d’urgence [en mode passif](./microsoft-defender-antivirus-compatibility.md)</span><span class="sxs-lookup"><span data-stu-id="aeeef-365">extend Emergency signature update to [passive mode](./microsoft-defender-antivirus-compatibility.md)</span></span>
- <span data-ttu-id="aeeef-366">Correction du problème de 4.18.1911.3</span><span class="sxs-lookup"><span data-stu-id="aeeef-366">Fix 4.18.1911.3 hang</span></span>
   
### <a name="known-issues"></a><span data-ttu-id="aeeef-367">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="aeeef-367">Known Issues</span></span>

<span data-ttu-id="aeeef-368">[**Fixed**] Devices using [modern standby mode](/windows-hardware/design/device-experiences/modern-standby) may experience a hang with the Windows Defender filter driver that results in a gap of protection.</span><span class="sxs-lookup"><span data-stu-id="aeeef-368">[**Fixed**] devices utilizing [modern standby mode](/windows-hardware/design/device-experiences/modern-standby) may experience a hang with the Windows Defender filter driver that results in a gap of protection.</span></span>  <span data-ttu-id="aeeef-369">Les ordinateurs concernés semblent ne pas avoir été mis à jour vers la dernière plateforme anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="aeeef-369">Affected machines appear to the customer as having not updated to the latest antimalware platform.</span></span>  
<br/>
> [!IMPORTANT]
> <span data-ttu-id="aeeef-370">Cette mise à jour est :</span><span class="sxs-lookup"><span data-stu-id="aeeef-370">This update is:</span></span>
> - <span data-ttu-id="aeeef-371">nécessaire aux appareils RS1 exécutant une version inférieure de la plateforme pour prendre en charge SHA2 ;</span><span class="sxs-lookup"><span data-stu-id="aeeef-371">needed by RS1 devices running lower version of the platform to support SHA2;</span></span>
> - <span data-ttu-id="aeeef-372">a un indicateur de redémarrage pour les systèmes qui ont des problèmes en suspension ;</span><span class="sxs-lookup"><span data-stu-id="aeeef-372">has a reboot flag for systems that have hanging issues;</span></span>
> - <span data-ttu-id="aeeef-373">est re-publiée en avril 2020 et ne sera pas recalée par les mises à jour plus nouvelles pour conserver la disponibilité future ;</span><span class="sxs-lookup"><span data-stu-id="aeeef-373">is re-released in April 2020 and will not be superseded by newer updates to keep future availability;</span></span>  
> - <span data-ttu-id="aeeef-374">est classée en tant que mise à jour en raison de l’exigence de redémarrage ; et</span><span class="sxs-lookup"><span data-stu-id="aeeef-374">is categorized as an update due to the reboot requirement; and</span></span>
> - <span data-ttu-id="aeeef-375">est uniquement proposée avec [Windows Update](https://support.microsoft.com/help/4027667/windows-10-update).</span><span class="sxs-lookup"><span data-stu-id="aeeef-375">is only be offered with [Windows Update](https://support.microsoft.com/help/4027667/windows-10-update).</span></span>
<br/>
</details>

<details>
<summary> <span data-ttu-id="aeeef-376">Novembre-2019 (plateforme : 4.18.1911.3 | Moteur : 1.1.16600.7)</span><span class="sxs-lookup"><span data-stu-id="aeeef-376">November-2019 (Platform: 4.18.1911.3 | Engine: 1.1.16600.7)</span></span></summary>

<span data-ttu-id="aeeef-377">Version de mise à jour des informations de sécurité **: 1.307.13.0**</span><span class="sxs-lookup"><span data-stu-id="aeeef-377">Security intelligence update version: **1.307.13.0**</span></span>  
<span data-ttu-id="aeeef-378">Publication : **7 décembre 2019**</span><span class="sxs-lookup"><span data-stu-id="aeeef-378">Released: **December 7, 2019**</span></span>  
<span data-ttu-id="aeeef-379">Plateforme : **4.18.1911.3**</span><span class="sxs-lookup"><span data-stu-id="aeeef-379">Platform: **4.18.1911.3**</span></span>  
<span data-ttu-id="aeeef-380">Moteur : **1.1.17000.7**</span><span class="sxs-lookup"><span data-stu-id="aeeef-380">Engine: **1.1.17000.7**</span></span>  
<span data-ttu-id="aeeef-381">Phase de support : **aucune prise en charge**</span><span class="sxs-lookup"><span data-stu-id="aeeef-381">Support phase: **No support**</span></span>  
     
### <a name="whats-new"></a><span data-ttu-id="aeeef-382">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="aeeef-382">What's new</span></span>

- <span data-ttu-id="aeeef-383">Niveau de suivi MpCmdRun fixe</span><span class="sxs-lookup"><span data-stu-id="aeeef-383">Fixed MpCmdRun tracing level</span></span>
- <span data-ttu-id="aeeef-384">Informations de version de WDFilter fixes</span><span class="sxs-lookup"><span data-stu-id="aeeef-384">Fixed WDFilter version info</span></span>
- <span data-ttu-id="aeeef-385">Améliorer les notifications (PUA)</span><span class="sxs-lookup"><span data-stu-id="aeeef-385">Improve notifications (PUA)</span></span>
- <span data-ttu-id="aeeef-386">ajouter des journaux MRT pour prendre en charge les fichiers</span><span class="sxs-lookup"><span data-stu-id="aeeef-386">add MRT logs to support files</span></span>
   
### <a name="known-issues"></a><span data-ttu-id="aeeef-387">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="aeeef-387">Known Issues</span></span>
<span data-ttu-id="aeeef-388">Lorsque cette mise à jour est installée, l’appareil a besoin du package de saut 4.18.2001.10 pour pouvoir se mettre à jour vers la dernière version de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="aeeef-388">When this update is installed, the device needs the jump package 4.18.2001.10 to be able to update to the latest platform version.</span></span>
<br/>
</details>


## <a name="microsoft-defender-antivirus-platform-support"></a><span data-ttu-id="aeeef-389">Antivirus Microsoft Defender prise en charge de la plateforme</span><span class="sxs-lookup"><span data-stu-id="aeeef-389">Microsoft Defender Antivirus platform support</span></span>
<span data-ttu-id="aeeef-390">Les mises à jour de la plateforme et du moteur sont fournies à une cadence mensuelle.</span><span class="sxs-lookup"><span data-stu-id="aeeef-390">Platform and engine updates are provided on a monthly cadence.</span></span> <span data-ttu-id="aeeef-391">Pour être entièrement pris en charge, tenez à jour les dernières mises à jour de plateforme.</span><span class="sxs-lookup"><span data-stu-id="aeeef-391">To be fully supported, keep current with the latest platform updates.</span></span> <span data-ttu-id="aeeef-392">Notre structure de support est dynamique et évolue en deux phases en fonction de la disponibilité de la dernière version de plateforme :</span><span class="sxs-lookup"><span data-stu-id="aeeef-392">Our support structure is dynamic, evolving into two phases depending on the availability of the latest platform version:</span></span>

- <span data-ttu-id="aeeef-393">Phase de maintenance des mises à jour **critiques** et de sécurité : lors de l’exécution de la dernière version de la plateforme, vous serez éligible à la réception des mises à jour de sécurité et critiques sur la plateforme anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="aeeef-393">**Security and Critical Updates servicing phase** - When running the latest platform version, you will be eligible to receive both Security and Critical updates to the anti-malware platform.</span></span>
 
- <span data-ttu-id="aeeef-394">**Phase de support technique (uniquement)** : après la publication d’une nouvelle version de plateforme, la prise en charge des versions antérieures (N-2) sera réduit au support technique uniquement.</span><span class="sxs-lookup"><span data-stu-id="aeeef-394">**Technical Support (Only) phase** - After a new platform version is released, support for older versions (N-2) will reduce to technical support only.</span></span> <span data-ttu-id="aeeef-395">Les versions de plateforme antérieures à N-2 ne seront plus pris en charge.\*</span><span class="sxs-lookup"><span data-stu-id="aeeef-395">Platform versions older than N-2 will no longer be supported.\*</span></span>

<span data-ttu-id="aeeef-396">\*Le support technique continuera d’être fourni pour les mises à niveau de la version Windows 10 (voir la version de plateforme incluse avec [les](#platform-version-included-with-windows-10-releases)versions Windows 10 ) vers la dernière version de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="aeeef-396">\* Technical support will continue to be provided for upgrades from the Windows 10 release version (see [Platform version included with Windows 10 releases](#platform-version-included-with-windows-10-releases)) to the latest platform version.</span></span>

<span data-ttu-id="aeeef-397">Pendant la phase de support technique (uniquement), les incidents de support commercialement raisonnables sont fournis par le biais du support technique du service clientèle Microsoft & et des offres de support géré de Microsoft (telles que le support Premier).</span><span class="sxs-lookup"><span data-stu-id="aeeef-397">During the technical support (only) phase, commercially reasonable support incidents will be provided through Microsoft Customer Service & Support and Microsoft’s managed support offerings (such as Premier Support).</span></span> <span data-ttu-id="aeeef-398">Si un incident de support nécessite une escalade vers le développement pour obtenir des conseils supplémentaires, nécessite une mise à jour non de sécurité ou nécessite une mise à jour de sécurité, les clients sont invités à mettre à niveau vers la dernière version de plateforme ou une mise à jour intermédiaire (\*).</span><span class="sxs-lookup"><span data-stu-id="aeeef-398">If a support incident requires escalation to development for further guidance, requires a non-security update, or requires a security update, customers will be asked to upgrade to the latest platform version or an intermediate update (\*).</span></span>

### <a name="platform-version-included-with-windows-10-releases"></a><span data-ttu-id="aeeef-399">Version de plateforme incluse dans Windows 10 versions</span><span class="sxs-lookup"><span data-stu-id="aeeef-399">Platform version included with Windows 10 releases</span></span>
<span data-ttu-id="aeeef-400">Le tableau ci-dessous fournit les versions Antivirus Microsoft Defender de plateforme et de moteur qui sont livrées avec les versions les Windows 10 les plus récentes :</span><span class="sxs-lookup"><span data-stu-id="aeeef-400">The below table provides the Microsoft Defender Antivirus platform and engine versions that are shipped with the latest Windows 10 releases:</span></span>    

|<span data-ttu-id="aeeef-401">Windows 10 version</span><span class="sxs-lookup"><span data-stu-id="aeeef-401">Windows 10 release</span></span>  |<span data-ttu-id="aeeef-402">Version de la plateforme</span><span class="sxs-lookup"><span data-stu-id="aeeef-402">Platform version</span></span>  |<span data-ttu-id="aeeef-403">Version du moteur</span><span class="sxs-lookup"><span data-stu-id="aeeef-403">Engine version</span></span> |<span data-ttu-id="aeeef-404">Phase de prise en charge</span><span class="sxs-lookup"><span data-stu-id="aeeef-404">Support phase</span></span> |
|:---|:---|:---|:---|
|<span data-ttu-id="aeeef-405">2004 (20H1/20H2)</span><span class="sxs-lookup"><span data-stu-id="aeeef-405">2004  (20H1/20H2)</span></span> |<span data-ttu-id="aeeef-406">4.18.1909.6</span><span class="sxs-lookup"><span data-stu-id="aeeef-406">4.18.1909.6</span></span> |<span data-ttu-id="aeeef-407">1.1.17000.2</span><span class="sxs-lookup"><span data-stu-id="aeeef-407">1.1.17000.2</span></span> | <span data-ttu-id="aeeef-408">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="aeeef-408">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="aeeef-409">1909 (19H2)</span><span class="sxs-lookup"><span data-stu-id="aeeef-409">1909  (19H2)</span></span> |<span data-ttu-id="aeeef-410">4.18.1902.5</span><span class="sxs-lookup"><span data-stu-id="aeeef-410">4.18.1902.5</span></span> |<span data-ttu-id="aeeef-411">1.1.16700.3</span><span class="sxs-lookup"><span data-stu-id="aeeef-411">1.1.16700.3</span></span> | <span data-ttu-id="aeeef-412">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="aeeef-412">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="aeeef-413">1903 (19H1)</span><span class="sxs-lookup"><span data-stu-id="aeeef-413">1903  (19H1)</span></span> |<span data-ttu-id="aeeef-414">4.18.1902.5</span><span class="sxs-lookup"><span data-stu-id="aeeef-414">4.18.1902.5</span></span> |<span data-ttu-id="aeeef-415">1.1.15600.4</span><span class="sxs-lookup"><span data-stu-id="aeeef-415">1.1.15600.4</span></span> | <span data-ttu-id="aeeef-416">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="aeeef-416">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="aeeef-417">1809 (RS5)</span><span class="sxs-lookup"><span data-stu-id="aeeef-417">1809  (RS5)</span></span> |<span data-ttu-id="aeeef-418">4.18.1807.18075</span><span class="sxs-lookup"><span data-stu-id="aeeef-418">4.18.1807.18075</span></span> |<span data-ttu-id="aeeef-419">1.1.15000.2</span><span class="sxs-lookup"><span data-stu-id="aeeef-419">1.1.15000.2</span></span> | <span data-ttu-id="aeeef-420">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="aeeef-420">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="aeeef-421">1803 (RS4)</span><span class="sxs-lookup"><span data-stu-id="aeeef-421">1803  (RS4)</span></span> |<span data-ttu-id="aeeef-422">4.13.17134.1</span><span class="sxs-lookup"><span data-stu-id="aeeef-422">4.13.17134.1</span></span> |<span data-ttu-id="aeeef-423">1.1.14600.4</span><span class="sxs-lookup"><span data-stu-id="aeeef-423">1.1.14600.4</span></span> | <span data-ttu-id="aeeef-424">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="aeeef-424">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="aeeef-425">1709 (RS3)</span><span class="sxs-lookup"><span data-stu-id="aeeef-425">1709  (RS3)</span></span> |<span data-ttu-id="aeeef-426">4.12.16299.15</span><span class="sxs-lookup"><span data-stu-id="aeeef-426">4.12.16299.15</span></span> |<span data-ttu-id="aeeef-427">1.1.14104.0</span><span class="sxs-lookup"><span data-stu-id="aeeef-427">1.1.14104.0</span></span> | <span data-ttu-id="aeeef-428">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="aeeef-428">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="aeeef-429">1703 (RS2)</span><span class="sxs-lookup"><span data-stu-id="aeeef-429">1703  (RS2)</span></span> |<span data-ttu-id="aeeef-430">4.11.15603.2</span><span class="sxs-lookup"><span data-stu-id="aeeef-430">4.11.15603.2</span></span> |<span data-ttu-id="aeeef-431">1.1.13504.0</span><span class="sxs-lookup"><span data-stu-id="aeeef-431">1.1.13504.0</span></span> | <span data-ttu-id="aeeef-432">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="aeeef-432">Technical upgrade support (only)</span></span> |
|<span data-ttu-id="aeeef-433">1607 (RS1)</span><span class="sxs-lookup"><span data-stu-id="aeeef-433">1607 (RS1)</span></span> |<span data-ttu-id="aeeef-434">4.10.14393.3683</span><span class="sxs-lookup"><span data-stu-id="aeeef-434">4.10.14393.3683</span></span> |<span data-ttu-id="aeeef-435">1.1.12805.0</span><span class="sxs-lookup"><span data-stu-id="aeeef-435">1.1.12805.0</span></span> | <span data-ttu-id="aeeef-436">Prise en charge de la mise à niveau technique (uniquement)</span><span class="sxs-lookup"><span data-stu-id="aeeef-436">Technical upgrade support (only)</span></span> |  

<span data-ttu-id="aeeef-437">Pour Windows 10 de publication, consultez la [Windows de faits sur le cycle de vie.](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet)</span><span class="sxs-lookup"><span data-stu-id="aeeef-437">For Windows 10 release information, see the [Windows lifecycle fact sheet](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet).</span></span>

## <a name="updates-for-deployment-image-servicing-and-management-dism"></a><span data-ttu-id="aeeef-438">Mises à jour pour la gestion et la maintenance des images de déploiement (DISM)</span><span class="sxs-lookup"><span data-stu-id="aeeef-438">Updates for Deployment Image Servicing and Management (DISM)</span></span>

<span data-ttu-id="aeeef-439">Nous vous recommandons de mettre à jour vos images d’installation Windows 10 (Enterprise, Pro et Éditions Famille), Windows Server 2019 et Windows Server 2016 OS avec les dernières mises à jour antivirus et anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="aeeef-439">We recommend updating your Windows 10 (Enterprise, Pro, and Home editions), Windows Server 2019, and Windows Server 2016 OS installation images with the latest antivirus and antimalware updates.</span></span> <span data-ttu-id="aeeef-440">La mise à jour de vos images d’installation du système d’exploitation permet d’éviter un écart de protection.</span><span class="sxs-lookup"><span data-stu-id="aeeef-440">Keeping your OS installation images up to date helps avoid a gap in protection.</span></span> 

<span data-ttu-id="aeeef-441">Pour plus d’informations, voir Mise à [jour de Microsoft Defender pour Windows images d’installation du système d’exploitation.](https://support.microsoft.com/help/4568292/defender-update-for-windows-operating-system-installation-images)</span><span class="sxs-lookup"><span data-stu-id="aeeef-441">For more information, see [Microsoft Defender update for Windows operating system installation images](https://support.microsoft.com/help/4568292/defender-update-for-windows-operating-system-installation-images).</span></span>

<details>
<summary><span data-ttu-id="aeeef-442">1.1.2106.01</span><span class="sxs-lookup"><span data-stu-id="aeeef-442">1.1.2106.01</span></span></summary>

<span data-ttu-id="aeeef-443">&ensp;Version du package **: 1.1.2106.01**  </span><span class="sxs-lookup"><span data-stu-id="aeeef-443">&ensp;Package version: **1.1.2106.01**  </span></span>  
<span data-ttu-id="aeeef-444">&ensp;Version de la plateforme **: 4.18.2104.14** </span><span class="sxs-lookup"><span data-stu-id="aeeef-444">&ensp;Platform version: **4.18.2104.14** </span></span>  
<span data-ttu-id="aeeef-445">&ensp;Version du moteur **: 1.1.18100.6**</span><span class="sxs-lookup"><span data-stu-id="aeeef-445">&ensp;Engine version: **1.1.18100.6**</span></span>  
<span data-ttu-id="aeeef-446">&ensp;Version de signature **: 1.339.1923.0**</span><span class="sxs-lookup"><span data-stu-id="aeeef-446">&ensp;Signature version: **1.339.1923.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="aeeef-447">Correctifs</span><span class="sxs-lookup"><span data-stu-id="aeeef-447">Fixes</span></span>
- <span data-ttu-id="aeeef-448">Aucun</span><span class="sxs-lookup"><span data-stu-id="aeeef-448">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="aeeef-449">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="aeeef-449">Additional information</span></span>
- <span data-ttu-id="aeeef-450">Aucun</span><span class="sxs-lookup"><span data-stu-id="aeeef-450">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="aeeef-451">1.1.2105.01</span><span class="sxs-lookup"><span data-stu-id="aeeef-451">1.1.2105.01</span></span></summary>

<span data-ttu-id="aeeef-452">&ensp;Version du package **: 1.1.2105.01**  </span><span class="sxs-lookup"><span data-stu-id="aeeef-452">&ensp;Package version: **1.1.2105.01**  </span></span>  
<span data-ttu-id="aeeef-453">&ensp;Version de la plateforme **: 4.18.2103.7** </span><span class="sxs-lookup"><span data-stu-id="aeeef-453">&ensp;Platform version: **4.18.2103.7** </span></span>  
<span data-ttu-id="aeeef-454">&ensp;Version du moteur **: 1.1.18100.6**</span><span class="sxs-lookup"><span data-stu-id="aeeef-454">&ensp;Engine version: **1.1.18100.6**</span></span>  
<span data-ttu-id="aeeef-455">&ensp;Version de signature **: 1.339.42.0**</span><span class="sxs-lookup"><span data-stu-id="aeeef-455">&ensp;Signature version: **1.339.42.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="aeeef-456">Correctifs</span><span class="sxs-lookup"><span data-stu-id="aeeef-456">Fixes</span></span>
- <span data-ttu-id="aeeef-457">Aucun</span><span class="sxs-lookup"><span data-stu-id="aeeef-457">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="aeeef-458">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="aeeef-458">Additional information</span></span>
- <span data-ttu-id="aeeef-459">Aucun</span><span class="sxs-lookup"><span data-stu-id="aeeef-459">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="aeeef-460">1.1.2104.01</span><span class="sxs-lookup"><span data-stu-id="aeeef-460">1.1.2104.01</span></span></summary>

<span data-ttu-id="aeeef-461">&ensp;Version du package **: 1.1.2104.01**  </span><span class="sxs-lookup"><span data-stu-id="aeeef-461">&ensp;Package version: **1.1.2104.01**  </span></span>  
<span data-ttu-id="aeeef-462">&ensp;Version de la plateforme **: 4.18.2102.4** </span><span class="sxs-lookup"><span data-stu-id="aeeef-462">&ensp;Platform version: **4.18.2102.4** </span></span>  
<span data-ttu-id="aeeef-463">&ensp;Version du moteur **: 1.1.18000.5**</span><span class="sxs-lookup"><span data-stu-id="aeeef-463">&ensp;Engine version: **1.1.18000.5**</span></span>  
<span data-ttu-id="aeeef-464">&ensp;Version de signature **: 1.335.232.0**</span><span class="sxs-lookup"><span data-stu-id="aeeef-464">&ensp;Signature version: **1.335.232.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="aeeef-465">Correctifs</span><span class="sxs-lookup"><span data-stu-id="aeeef-465">Fixes</span></span>
- <span data-ttu-id="aeeef-466">Aucun</span><span class="sxs-lookup"><span data-stu-id="aeeef-466">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="aeeef-467">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="aeeef-467">Additional information</span></span>
- <span data-ttu-id="aeeef-468">Aucun</span><span class="sxs-lookup"><span data-stu-id="aeeef-468">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="aeeef-469">1.1.2103.01</span><span class="sxs-lookup"><span data-stu-id="aeeef-469">1.1.2103.01</span></span></summary>

<span data-ttu-id="aeeef-470">&ensp;Version du package **: 1.1.2103.01**  </span><span class="sxs-lookup"><span data-stu-id="aeeef-470">&ensp;Package version: **1.1.2103.01**  </span></span>  
<span data-ttu-id="aeeef-471">&ensp;Version de la plateforme **: 4.18.2101.9** </span><span class="sxs-lookup"><span data-stu-id="aeeef-471">&ensp;Platform version: **4.18.2101.9** </span></span>  
<span data-ttu-id="aeeef-472">&ensp;Version du moteur **: 1.1.17800.5**</span><span class="sxs-lookup"><span data-stu-id="aeeef-472">&ensp;Engine version: **1.1.17800.5**</span></span>  
<span data-ttu-id="aeeef-473">&ensp;Version de signature **: 1.331.2302.0**</span><span class="sxs-lookup"><span data-stu-id="aeeef-473">&ensp;Signature version: **1.331.2302.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="aeeef-474">Correctifs</span><span class="sxs-lookup"><span data-stu-id="aeeef-474">Fixes</span></span>
- <span data-ttu-id="aeeef-475">Aucun</span><span class="sxs-lookup"><span data-stu-id="aeeef-475">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="aeeef-476">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="aeeef-476">Additional information</span></span>
- <span data-ttu-id="aeeef-477">Aucun</span><span class="sxs-lookup"><span data-stu-id="aeeef-477">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="aeeef-478">1.1.2102.03</span><span class="sxs-lookup"><span data-stu-id="aeeef-478">1.1.2102.03</span></span></summary>

<span data-ttu-id="aeeef-479">&ensp;Version du package **: 1.1.2102.03**  </span><span class="sxs-lookup"><span data-stu-id="aeeef-479">&ensp;Package version: **1.1.2102.03**  </span></span>  
<span data-ttu-id="aeeef-480">&ensp;Version de la plateforme **: 4.18.2011.6** </span><span class="sxs-lookup"><span data-stu-id="aeeef-480">&ensp;Platform version: **4.18.2011.6** </span></span>  
<span data-ttu-id="aeeef-481">&ensp;Version du moteur **: 1.1.17800.5**</span><span class="sxs-lookup"><span data-stu-id="aeeef-481">&ensp;Engine version: **1.1.17800.5**</span></span>  
<span data-ttu-id="aeeef-482">&ensp;Version de signature **: 1.331.174.0**</span><span class="sxs-lookup"><span data-stu-id="aeeef-482">&ensp;Signature version: **1.331.174.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="aeeef-483">Correctifs</span><span class="sxs-lookup"><span data-stu-id="aeeef-483">Fixes</span></span>
- <span data-ttu-id="aeeef-484">Aucun</span><span class="sxs-lookup"><span data-stu-id="aeeef-484">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="aeeef-485">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="aeeef-485">Additional information</span></span>
- <span data-ttu-id="aeeef-486">Aucun</span><span class="sxs-lookup"><span data-stu-id="aeeef-486">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="aeeef-487">1.1.2101.02</span><span class="sxs-lookup"><span data-stu-id="aeeef-487">1.1.2101.02</span></span></summary>

<span data-ttu-id="aeeef-488">&ensp;Version du package **: 1.1.2101.02**  </span><span class="sxs-lookup"><span data-stu-id="aeeef-488">&ensp;Package version: **1.1.2101.02**  </span></span>  
<span data-ttu-id="aeeef-489">&ensp;Version de la plateforme **: 4.18.2011.6** </span><span class="sxs-lookup"><span data-stu-id="aeeef-489">&ensp;Platform version: **4.18.2011.6** </span></span>  
<span data-ttu-id="aeeef-490">&ensp;Version du moteur **: 1.1.17700.4**</span><span class="sxs-lookup"><span data-stu-id="aeeef-490">&ensp;Engine version: **1.1.17700.4**</span></span>  
<span data-ttu-id="aeeef-491">&ensp;Version de signature **: 1.329.1796.0**</span><span class="sxs-lookup"><span data-stu-id="aeeef-491">&ensp;Signature version: **1.329.1796.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="aeeef-492">Correctifs</span><span class="sxs-lookup"><span data-stu-id="aeeef-492">Fixes</span></span>
- <span data-ttu-id="aeeef-493">Aucun</span><span class="sxs-lookup"><span data-stu-id="aeeef-493">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="aeeef-494">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="aeeef-494">Additional information</span></span>
- <span data-ttu-id="aeeef-495">Aucun</span><span class="sxs-lookup"><span data-stu-id="aeeef-495">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="aeeef-496">1.1.2012.01</span><span class="sxs-lookup"><span data-stu-id="aeeef-496">1.1.2012.01</span></span></summary>

<span data-ttu-id="aeeef-497">&ensp;Version du package **: 1.1.2012.01**  </span><span class="sxs-lookup"><span data-stu-id="aeeef-497">&ensp;Package version: **1.1.2012.01**  </span></span>  
<span data-ttu-id="aeeef-498">&ensp;Version de la plateforme **: 4.18.2010.7** </span><span class="sxs-lookup"><span data-stu-id="aeeef-498">&ensp;Platform version: **4.18.2010.7** </span></span>  
<span data-ttu-id="aeeef-499">&ensp;Version du moteur **: 1.1.17600.5**</span><span class="sxs-lookup"><span data-stu-id="aeeef-499">&ensp;Engine version: **1.1.17600.5**</span></span>  
<span data-ttu-id="aeeef-500">&ensp;Version de signature **: 1.327.1991.0**</span><span class="sxs-lookup"><span data-stu-id="aeeef-500">&ensp;Signature version: **1.327.1991.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="aeeef-501">Correctifs</span><span class="sxs-lookup"><span data-stu-id="aeeef-501">Fixes</span></span>
- <span data-ttu-id="aeeef-502">Aucun</span><span class="sxs-lookup"><span data-stu-id="aeeef-502">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="aeeef-503">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="aeeef-503">Additional information</span></span>
- <span data-ttu-id="aeeef-504">Aucun</span><span class="sxs-lookup"><span data-stu-id="aeeef-504">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="aeeef-505">1.1.2011.02</span><span class="sxs-lookup"><span data-stu-id="aeeef-505">1.1.2011.02</span></span></summary>

<span data-ttu-id="aeeef-506">&ensp;Version du package **: 1.1.2011.02**  </span><span class="sxs-lookup"><span data-stu-id="aeeef-506">&ensp;Package version: **1.1.2011.02**  </span></span>  
<span data-ttu-id="aeeef-507">&ensp;Version de la plateforme **: 4.18.2010.7** </span><span class="sxs-lookup"><span data-stu-id="aeeef-507">&ensp;Platform version: **4.18.2010.7** </span></span>  
<span data-ttu-id="aeeef-508">&ensp;Version du moteur **: 1.1.17600.5**</span><span class="sxs-lookup"><span data-stu-id="aeeef-508">&ensp;Engine version: **1.1.17600.5**</span></span>  
<span data-ttu-id="aeeef-509">&ensp;Version de signature **: 1.327.658.0**</span><span class="sxs-lookup"><span data-stu-id="aeeef-509">&ensp;Signature version: **1.327.658.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="aeeef-510">Correctifs</span><span class="sxs-lookup"><span data-stu-id="aeeef-510">Fixes</span></span>
- <span data-ttu-id="aeeef-511">Aucun</span><span class="sxs-lookup"><span data-stu-id="aeeef-511">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="aeeef-512">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="aeeef-512">Additional information</span></span>
- <span data-ttu-id="aeeef-513">Signatures Antivirus Microsoft Defender actualisées</span><span class="sxs-lookup"><span data-stu-id="aeeef-513">Refreshed Microsoft Defender Antivirus signatures</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="aeeef-514">1.1.2011.01</span><span class="sxs-lookup"><span data-stu-id="aeeef-514">1.1.2011.01</span></span></summary>

<span data-ttu-id="aeeef-515">&ensp;Version du package **: 1.1.2011.01**  </span><span class="sxs-lookup"><span data-stu-id="aeeef-515">&ensp;Package version: **1.1.2011.01**  </span></span>  
<span data-ttu-id="aeeef-516">&ensp;Version de la plateforme **: 4.18.2009.7**</span><span class="sxs-lookup"><span data-stu-id="aeeef-516">&ensp;Platform version: **4.18.2009.7**</span></span>  
<span data-ttu-id="aeeef-517">&ensp;Version du moteur **: 1.1.17600.5**</span><span class="sxs-lookup"><span data-stu-id="aeeef-517">&ensp;Engine version: **1.1.17600.5**</span></span>  
<span data-ttu-id="aeeef-518">&ensp;Version de signature **: 1.327.344.0**</span><span class="sxs-lookup"><span data-stu-id="aeeef-518">&ensp;Signature version: **1.327.344.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="aeeef-519">Correctifs</span><span class="sxs-lookup"><span data-stu-id="aeeef-519">Fixes</span></span>
- <span data-ttu-id="aeeef-520">Aucun</span><span class="sxs-lookup"><span data-stu-id="aeeef-520">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="aeeef-521">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="aeeef-521">Additional information</span></span>
- <span data-ttu-id="aeeef-522">Aucun</span><span class="sxs-lookup"><span data-stu-id="aeeef-522">None</span></span>  
<br/>
</details><details>
<summary><span data-ttu-id="aeeef-523">1.1.2009.10</span><span class="sxs-lookup"><span data-stu-id="aeeef-523">1.1.2009.10</span></span></summary>

<span data-ttu-id="aeeef-524">&ensp;Version du package **: 1.1.2011.01**  </span><span class="sxs-lookup"><span data-stu-id="aeeef-524">&ensp;Package version: **1.1.2011.01**  </span></span>  
<span data-ttu-id="aeeef-525">&ensp;Version de la plateforme **: 4.18.2008.9** </span><span class="sxs-lookup"><span data-stu-id="aeeef-525">&ensp;Platform version: **4.18.2008.9** </span></span>  
<span data-ttu-id="aeeef-526">&ensp;Version du moteur **: 1.1.17400.5**</span><span class="sxs-lookup"><span data-stu-id="aeeef-526">&ensp;Engine version: **1.1.17400.5**</span></span>  
<span data-ttu-id="aeeef-527">&ensp;Version de signature **: 1.327.2216.0**</span><span class="sxs-lookup"><span data-stu-id="aeeef-527">&ensp;Signature version: **1.327.2216.0**</span></span>    
    
### <a name="fixes"></a><span data-ttu-id="aeeef-528">Correctifs</span><span class="sxs-lookup"><span data-stu-id="aeeef-528">Fixes</span></span>
- <span data-ttu-id="aeeef-529">Aucun</span><span class="sxs-lookup"><span data-stu-id="aeeef-529">None</span></span>

### <a name="additional-information"></a><span data-ttu-id="aeeef-530">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="aeeef-530">Additional information</span></span>
- <span data-ttu-id="aeeef-531">Ajout de la prise en charge Windows 10 images d’installation du système d’exploitation RS1 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="aeeef-531">Added support for Windows 10 RS1 or later OS install images.</span></span>  
<br/>
</details>

## <a name="additional-resources"></a><span data-ttu-id="aeeef-532">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="aeeef-532">Additional resources</span></span>

| <span data-ttu-id="aeeef-533">Article</span><span class="sxs-lookup"><span data-stu-id="aeeef-533">Article</span></span> | <span data-ttu-id="aeeef-534">Description</span><span class="sxs-lookup"><span data-stu-id="aeeef-534">Description</span></span>  |
|:---|:---|
|[<span data-ttu-id="aeeef-535">Mise à jour de Microsoft Defender Windows images d’installation du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="aeeef-535">Microsoft Defender update for Windows operating system installation images</span></span>](https://support.microsoft.com/help/4568292/defender-update-for-windows-operating-system-installation-images)  | <span data-ttu-id="aeeef-536">Passer en revue les packages de mise à jour anti-programme malveillant pour vos images d’installation du système d’exploitation (fichiers WIM et VHD).</span><span class="sxs-lookup"><span data-stu-id="aeeef-536">Review antimalware update packages for your OS installation images (WIM and VHD files).</span></span> <span data-ttu-id="aeeef-537">Obtenez Antivirus Microsoft Defender mises à jour pour Windows 10 (éditions Enterprise, Pro et Famille), Windows Server 2019 et Windows Server 2016 images d’installation.</span><span class="sxs-lookup"><span data-stu-id="aeeef-537">Get Microsoft Defender Antivirus updates for Windows 10 (Enterprise, Pro, and Home editions), Windows Server 2019, and Windows Server 2016 installation images.</span></span>  |
|[<span data-ttu-id="aeeef-538">Gérer le téléchargement et l’application des mises à jour de protection</span><span class="sxs-lookup"><span data-stu-id="aeeef-538">Manage how protection updates are downloaded and applied</span></span>](manage-protection-updates-microsoft-defender-antivirus.md) | <span data-ttu-id="aeeef-539">Les mises à jour de la protection peuvent être livrées via de nombreuses sources.</span><span class="sxs-lookup"><span data-stu-id="aeeef-539">Protection updates can be delivered through many sources.</span></span> |
|[<span data-ttu-id="aeeef-540">Gérer le moment où les mises à jour de la protection doivent être téléchargées et appliquées</span><span class="sxs-lookup"><span data-stu-id="aeeef-540">Manage when protection updates should be downloaded and applied</span></span>](manage-protection-update-schedule-microsoft-defender-antivirus.md) | <span data-ttu-id="aeeef-541">Vous pouvez planifier le téléchargement des mises à jour de la protection.</span><span class="sxs-lookup"><span data-stu-id="aeeef-541">You can schedule when protection updates should be downloaded.</span></span> |
|[<span data-ttu-id="aeeef-542">Gérer les mises à jour des points de terminaison qui ne sont plus à jour</span><span class="sxs-lookup"><span data-stu-id="aeeef-542">Manage updates for endpoints that are out of date</span></span>](manage-outdated-endpoints-microsoft-defender-antivirus.md) | <span data-ttu-id="aeeef-543">Si un point de terminaison manque une mise à jour ou une analyse programmée, vous pouvez forcer une mise à jour ou une analyse la prochaine fois qu’un utilisateur se signe.</span><span class="sxs-lookup"><span data-stu-id="aeeef-543">If an endpoint misses an update or scheduled scan, you can force an update or scan the next time a user signs in.</span></span> |
|[<span data-ttu-id="aeeef-544">Gérer les mises à jour forcées en fonction des événements</span><span class="sxs-lookup"><span data-stu-id="aeeef-544">Manage event-based forced updates</span></span>](manage-event-based-updates-microsoft-defender-antivirus.md) | <span data-ttu-id="aeeef-545">Vous pouvez définir des mises à jour de protection à télécharger au démarrage ou après certains événements de protection livrés par le cloud.</span><span class="sxs-lookup"><span data-stu-id="aeeef-545">You can set protection updates to be downloaded at startup or after certain cloud-delivered protection events.</span></span> |
|[<span data-ttu-id="aeeef-546">Gérer les mises à jour pour les appareils mobiles et les machines virtuelles</span><span class="sxs-lookup"><span data-stu-id="aeeef-546">Manage updates for mobile devices and virtual machines (VMs)</span></span>](manage-updates-mobile-devices-vms-microsoft-defender-antivirus.md)| <span data-ttu-id="aeeef-547">Vous pouvez spécifier des paramètres, par exemple si des mises à jour doivent être mises à jour sur l’alimentation de la batterie, qui sont particulièrement utiles pour les appareils mobiles et les ordinateurs virtuels.</span><span class="sxs-lookup"><span data-stu-id="aeeef-547">You can specify settings, such as whether updates should occur on battery power, that are especially useful for mobile devices and virtual machines.</span></span> |
