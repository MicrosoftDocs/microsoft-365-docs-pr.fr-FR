---
title: Activer et configurer les fonctionnalités de protection de l'Antivirus Microsoft Defender
description: Activez la protection en temps réel, heuristique et basée sur le comportement dans Microsoft Defender AV.
keywords: heuristique, machine learning, moniteur de comportement, protection en temps réel, toujours en action, Antivirus Microsoft Defender, logiciel anti-programme malveillant, sécurité, defender
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: normal
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.openlocfilehash: 9fc51682b659670a21c3c293ea8996beb228802a
ms.sourcegitcommit: 7a339c9f7039825d131b39481ddf54c57b021b11
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "51765070"
---
# <a name="configure-behavioral-heuristic-and-real-time-protection"></a><span data-ttu-id="3ed4b-104">Configurer la protection comportementale, heuristique et en temps réel</span><span class="sxs-lookup"><span data-stu-id="3ed4b-104">Configure behavioral, heuristic, and real-time protection</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="3ed4b-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="3ed4b-105">**Applies to:**</span></span>

- [<span data-ttu-id="3ed4b-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="3ed4b-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="3ed4b-107">L'Antivirus Microsoft Defender utilise plusieurs méthodes pour fournir une protection contre les menaces :</span><span class="sxs-lookup"><span data-stu-id="3ed4b-107">Microsoft Defender Antivirus uses several methods to provide threat protection:</span></span>

- <span data-ttu-id="3ed4b-108">Protection cloud pour la détection et le blocage quasi instantanés des menaces nouvelles et émergentes</span><span class="sxs-lookup"><span data-stu-id="3ed4b-108">Cloud-delivered protection for near-instant detection and blocking of new and emerging threats</span></span>
- <span data-ttu-id="3ed4b-109">Analyse toujours continue, à l'aide de la surveillance du comportement des fichiers et des processus et d'autres heuristiques (également appelée « protection en temps réel »)</span><span class="sxs-lookup"><span data-stu-id="3ed4b-109">Always-on scanning, using file and process behavior monitoring and other heuristics (also known as "real-time protection")</span></span>
- <span data-ttu-id="3ed4b-110">Mises à jour de la protection dédiées, fondées sur l’apprentissage automatique, l’analyse humaine et automatisée du Big Data, et des recherches approfondies sur la résistance aux menaces</span><span class="sxs-lookup"><span data-stu-id="3ed4b-110">Dedicated protection updates based on machine-learning, human and automated big-data analysis, and in-depth threat resistance research</span></span>

<span data-ttu-id="3ed4b-111">Vous pouvez configurer la façon dont l'Antivirus Microsoft Defender utilise ces méthodes avec la stratégie de groupe, System Center Configuration Manage, les cmdlets PowerShell et Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="3ed4b-111">You can configure how Microsoft Defender Antivirus uses these methods with Group Policy, System Center Configuration Manage, PowerShell cmdlets, and Windows Management Instrumentation (WMI).</span></span>

<span data-ttu-id="3ed4b-112">Cette section couvre la configuration de l'analyse toujours en ligne, notamment la détection et le blocage des applications qui sont considérées comme non sûres, mais qui peuvent ne pas être détectées comme des programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="3ed4b-112">This section covers configuration for always-on scanning, including how to detect and block apps that are deemed unsafe, but may not be detected as malware.</span></span>

<span data-ttu-id="3ed4b-113">Voir [Utiliser les technologies de l'Antivirus Microsoft Defender](cloud-protection-microsoft-defender-antivirus.md) de nouvelle génération via la protection cloud pour savoir comment activer et configurer la protection de l'antivirus Microsoft Defender dans le cloud.</span><span class="sxs-lookup"><span data-stu-id="3ed4b-113">See [Use next-gen Microsoft Defender Antivirus technologies through cloud-delivered protection](cloud-protection-microsoft-defender-antivirus.md) for how to enable and configure Microsoft Defender Antivirus cloud-delivered protection.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3ed4b-114">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="3ed4b-114">In this section</span></span>

 <span data-ttu-id="3ed4b-115">Rubrique</span><span class="sxs-lookup"><span data-stu-id="3ed4b-115">Topic</span></span> | <span data-ttu-id="3ed4b-116">Description</span><span class="sxs-lookup"><span data-stu-id="3ed4b-116">Description</span></span>
---|---
[<span data-ttu-id="3ed4b-117">Détecter et bloquer les applications potentiellement indésirables</span><span class="sxs-lookup"><span data-stu-id="3ed4b-117">Detect and block potentially unwanted applications</span></span>](detect-block-potentially-unwanted-apps-microsoft-defender-antivirus.md) | <span data-ttu-id="3ed4b-118">Détecter et bloquer les applications qui peuvent être indésirables sur votre réseau, telles que les logiciels publicitaires, les modificateurs de navigateur et les barres d'outils, ainsi que les applications antivirus malveillantes ou factices</span><span class="sxs-lookup"><span data-stu-id="3ed4b-118">Detect and block apps that may be unwanted in your network, such as adware, browser modifiers and toolbars, and rogue or fake antivirus apps</span></span>
[<span data-ttu-id="3ed4b-119">Activer et configurer les fonctionnalités de protection de l'Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="3ed4b-119">Enable and configure Microsoft Defender Antivirus protection capabilities</span></span>](configure-real-time-protection-microsoft-defender-antivirus.md) | <span data-ttu-id="3ed4b-120">Activer et configurer la protection en temps réel, l'heuristique et d'autres fonctionnalités de surveillance de l'Antivirus Microsoft Defender toujours actives</span><span class="sxs-lookup"><span data-stu-id="3ed4b-120">Enable and configure real-time protection, heuristics, and other always-on Microsoft Defender Antivirus monitoring features</span></span>