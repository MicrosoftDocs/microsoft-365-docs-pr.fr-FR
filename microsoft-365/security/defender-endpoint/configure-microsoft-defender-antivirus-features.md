---
title: Configurer les fonctionnalités antivirus Microsoft Defender
description: Vous pouvez configurer les Antivirus Microsoft Defender avec Intune, Microsoft Endpoint Configuration Manager, la stratégie de groupe et PowerShell.
keywords: Antivirus Microsoft Defender, anti-programme malveillant, sécurité, defender, configurer, configuration, Gestionnaire de configuration, Microsoft Endpoint Configuration Manager, SCCM, Intune, GDM, gestion des appareils mobiles, GP, stratégie de groupe, PowerShell
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: Normal
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.date: 06/04/2021
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.topic: article
ms.openlocfilehash: 6ef9a2c34a88d7c9f5506c681088db9dc84cb0cc
ms.sourcegitcommit: b09aee96a1e2266b33ba81dfe497f24c5300bb56
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/06/2021
ms.locfileid: "52789026"
---
# <a name="configure-microsoft-defender-antivirus-features"></a><span data-ttu-id="9fef3-104">Configurer les fonctionnalités antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="9fef3-104">Configure Microsoft Defender Antivirus features</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="9fef3-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="9fef3-105">**Applies to:**</span></span>

- [<span data-ttu-id="9fef3-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="9fef3-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="9fef3-107">Vous pouvez configurer Antivirus Microsoft Defender avec un certain nombre d’outils, tels que :</span><span class="sxs-lookup"><span data-stu-id="9fef3-107">You can configure Microsoft Defender Antivirus with a number of tools, such as:</span></span>

- <span data-ttu-id="9fef3-108">Microsoft Endpoint Manager (qui inclut les Microsoft Intune et Microsoft Endpoint Configuration Manager)</span><span class="sxs-lookup"><span data-stu-id="9fef3-108">Microsoft Endpoint Manager (which includes Microsoft Intune and Microsoft Endpoint Configuration Manager)</span></span>
- <span data-ttu-id="9fef3-109">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="9fef3-109">Group Policy</span></span>
- <span data-ttu-id="9fef3-110">Cmdlets PowerShell</span><span class="sxs-lookup"><span data-stu-id="9fef3-110">PowerShell cmdlets</span></span>
- <span data-ttu-id="9fef3-111">WMI (Windows Management Instrumentation)</span><span class="sxs-lookup"><span data-stu-id="9fef3-111">Windows Management Instrumentation (WMI)</span></span>

<span data-ttu-id="9fef3-112">Les grandes catégories de fonctionnalités suivantes peuvent être configurées :</span><span class="sxs-lookup"><span data-stu-id="9fef3-112">The following broad categories of features can be configured:</span></span>

- <span data-ttu-id="9fef3-113">Protection cloud.</span><span class="sxs-lookup"><span data-stu-id="9fef3-113">Cloud-delivered protection.</span></span> <span data-ttu-id="9fef3-114">Voir protection et protection des services [cloud Antivirus Microsoft Defender](cloud-protection-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="9fef3-114">See [Cloud-delivered protection and Microsoft Defender Antivirus](cloud-protection-microsoft-defender-antivirus.md)</span></span>
 
- <span data-ttu-id="9fef3-115">Protection en temps réel toujours continue, y compris la protection comportementale, heuristique et basée sur l’apprentissage automatique.</span><span class="sxs-lookup"><span data-stu-id="9fef3-115">Always-on real-time protection, including behavioral, heuristic, and machine-learning-based protection.</span></span> <span data-ttu-id="9fef3-116">Voir [Configurer la protection comportementale, heuristique et en temps réel.](configure-protection-features-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="9fef3-116">See [Configure behavioral, heuristic, and real-time protection](configure-protection-features-microsoft-defender-antivirus.md).</span></span>

- <span data-ttu-id="9fef3-117">Interaction des utilisateurs finaux avec le client sur des points de terminaison individuels.</span><span class="sxs-lookup"><span data-stu-id="9fef3-117">How end users interact with the client on individual endpoints.</span></span> <span data-ttu-id="9fef3-118">Consultez les ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="9fef3-118">See the following resources:</span></span>
   
   - [<span data-ttu-id="9fef3-119">Empêcher les utilisateurs de voir ou d’interagir avec l Antivirus Microsoft Defender’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="9fef3-119">Prevent users from seeing or interacting with the Microsoft Defender Antivirus user interface</span></span>](prevent-end-user-interaction-microsoft-defender-antivirus.md)

   - [<span data-ttu-id="9fef3-120">Empêcher ou autoriser les utilisateurs à modifier localement les paramètres Antivirus Microsoft Defender stratégie</span><span class="sxs-lookup"><span data-stu-id="9fef3-120">Prevent or allow users to locally modify Microsoft Defender Antivirus policy settings</span></span>](configure-local-policy-overrides-microsoft-defender-antivirus.md) 

> [!TIP]
> <span data-ttu-id="9fef3-121">Consulter les [rubriques de référence pour les outils de gestion et de configuration.](configuration-management-reference-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="9fef3-121">Review [Reference topics for management and configuration tools](configuration-management-reference-microsoft-defender-antivirus.md).</span></span>