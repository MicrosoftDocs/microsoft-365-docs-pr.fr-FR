---
title: Configurer les fonctionnalités antivirus Microsoft Defender
description: Vous pouvez configurer les Antivirus Microsoft Defender avec Intune, Microsoft Endpoint Configuration Manager, la stratégie de groupe et PowerShell.
keywords: Antivirus Microsoft Defender, anti-programme malveillant, sécurité, defender, configurer, configuration, Gestionnaire de configuration, Microsoft Endpoint Configuration Manager, SCCM, Intune, GDM, gestion des appareils mobiles, GP, stratégie de groupe, PowerShell
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.technology: mde
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: Normal
author: denisebmsft
ms.author: deniseb
ms.topic: article
ms.custom: nextgen
ms.date: 06/04/2021
ms.reviewer: ''
manager: dansimp
ms.openlocfilehash: 7fa5959ede9f0c71c75cefafc0fcb0d4376a1a4f
ms.sourcegitcommit: be929f79751c0c52dfa6bd98a854432a0c63faf0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "52925394"
---
# <a name="configure-microsoft-defender-antivirus-features"></a><span data-ttu-id="12ff5-104">Configurer les fonctionnalités antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="12ff5-104">Configure Microsoft Defender Antivirus features</span></span>


<span data-ttu-id="12ff5-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="12ff5-105">**Applies to:**</span></span>

- [<span data-ttu-id="12ff5-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="12ff5-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="12ff5-107">Vous pouvez configurer Antivirus Microsoft Defender avec un certain nombre d’outils, tels que :</span><span class="sxs-lookup"><span data-stu-id="12ff5-107">You can configure Microsoft Defender Antivirus with a number of tools, such as:</span></span>

- <span data-ttu-id="12ff5-108">Microsoft Endpoint Manager (qui inclut les Microsoft Intune et Microsoft Endpoint Configuration Manager)</span><span class="sxs-lookup"><span data-stu-id="12ff5-108">Microsoft Endpoint Manager (which includes Microsoft Intune and Microsoft Endpoint Configuration Manager)</span></span>
- <span data-ttu-id="12ff5-109">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="12ff5-109">Group Policy</span></span>
- <span data-ttu-id="12ff5-110">Cmdlets PowerShell</span><span class="sxs-lookup"><span data-stu-id="12ff5-110">PowerShell cmdlets</span></span>
- <span data-ttu-id="12ff5-111">WMI (Windows Management Instrumentation)</span><span class="sxs-lookup"><span data-stu-id="12ff5-111">Windows Management Instrumentation (WMI)</span></span>

<span data-ttu-id="12ff5-112">Les grandes catégories de fonctionnalités suivantes peuvent être configurées :</span><span class="sxs-lookup"><span data-stu-id="12ff5-112">The following broad categories of features can be configured:</span></span>

- <span data-ttu-id="12ff5-113">Protection cloud.</span><span class="sxs-lookup"><span data-stu-id="12ff5-113">Cloud-delivered protection.</span></span> <span data-ttu-id="12ff5-114">Voir protection et protection des services [cloud Antivirus Microsoft Defender](cloud-protection-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="12ff5-114">See [Cloud-delivered protection and Microsoft Defender Antivirus](cloud-protection-microsoft-defender-antivirus.md)</span></span>
 
- <span data-ttu-id="12ff5-115">Protection en temps réel toujours continue, y compris la protection comportementale, heuristique et basée sur l’apprentissage automatique.</span><span class="sxs-lookup"><span data-stu-id="12ff5-115">Always-on real-time protection, including behavioral, heuristic, and machine-learning-based protection.</span></span> <span data-ttu-id="12ff5-116">Voir [Configurer la protection comportementale, heuristique et en temps réel.](configure-protection-features-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="12ff5-116">See [Configure behavioral, heuristic, and real-time protection](configure-protection-features-microsoft-defender-antivirus.md).</span></span>

- <span data-ttu-id="12ff5-117">Interaction des utilisateurs finaux avec le client sur des points de terminaison individuels.</span><span class="sxs-lookup"><span data-stu-id="12ff5-117">How end users interact with the client on individual endpoints.</span></span> <span data-ttu-id="12ff5-118">Consultez les ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="12ff5-118">See the following resources:</span></span>
   
   - [<span data-ttu-id="12ff5-119">Empêcher les utilisateurs de voir ou d’interagir avec l Antivirus Microsoft Defender’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="12ff5-119">Prevent users from seeing or interacting with the Microsoft Defender Antivirus user interface</span></span>](prevent-end-user-interaction-microsoft-defender-antivirus.md)

   - [<span data-ttu-id="12ff5-120">Empêcher ou autoriser les utilisateurs à modifier localement les paramètres Antivirus Microsoft Defender stratégie</span><span class="sxs-lookup"><span data-stu-id="12ff5-120">Prevent or allow users to locally modify Microsoft Defender Antivirus policy settings</span></span>](configure-local-policy-overrides-microsoft-defender-antivirus.md) 

> [!TIP]
> <span data-ttu-id="12ff5-121">Consulter les [rubriques de référence pour les outils de gestion et de configuration.](configuration-management-reference-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="12ff5-121">Review [Reference topics for management and configuration tools](configuration-management-reference-microsoft-defender-antivirus.md).</span></span>
