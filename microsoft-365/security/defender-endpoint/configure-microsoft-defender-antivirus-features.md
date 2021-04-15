---
title: Configurer les fonctionnalités de l'Antivirus Microsoft Defender
description: Vous pouvez configurer les fonctionnalités de l'Antivirus Microsoft Defender avec Intune, Microsoft Endpoint Configuration Manager, la stratégie de groupe et PowerShell.
keywords: Antivirus Microsoft Defender, anti-programme malveillant, sécurité, defender, configurer, configuration, Gestionnaire de configuration, Microsoft Endpoint Configuration Manager, SCCM, Intune, GDM, gestion des appareils mobiles, GP, stratégie de groupe, PowerShell
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: normal
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.date: 11/18/2020
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.openlocfilehash: 8503bb5bdd6337ec60390ef1d8e59f6f506fbce2
ms.sourcegitcommit: 7a339c9f7039825d131b39481ddf54c57b021b11
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "51765166"
---
# <a name="configure-microsoft-defender-antivirus-features"></a><span data-ttu-id="ae944-104">Configurer les fonctionnalités de l'Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="ae944-104">Configure Microsoft Defender Antivirus features</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="ae944-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="ae944-105">**Applies to:**</span></span>

- [<span data-ttu-id="ae944-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="ae944-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="ae944-107">Vous pouvez configurer l'Antivirus Microsoft Defender avec un certain nombre d'outils, notamment :</span><span class="sxs-lookup"><span data-stu-id="ae944-107">You can configure Microsoft Defender Antivirus with a number of tools, including:</span></span>

- <span data-ttu-id="ae944-108">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="ae944-108">Microsoft Intune</span></span>
- <span data-ttu-id="ae944-109">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ae944-109">Microsoft Endpoint Configuration Manager</span></span>
- <span data-ttu-id="ae944-110">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="ae944-110">Group Policy</span></span>
- <span data-ttu-id="ae944-111">Cmdlets PowerShell</span><span class="sxs-lookup"><span data-stu-id="ae944-111">PowerShell cmdlets</span></span>
- <span data-ttu-id="ae944-112">WMI (Windows Management Instrumentation)</span><span class="sxs-lookup"><span data-stu-id="ae944-112">Windows Management Instrumentation (WMI)</span></span>

<span data-ttu-id="ae944-113">Les grandes catégories de fonctionnalités suivantes peuvent être configurées :</span><span class="sxs-lookup"><span data-stu-id="ae944-113">The following broad categories of features can be configured:</span></span>

- <span data-ttu-id="ae944-114">Protection cloud</span><span class="sxs-lookup"><span data-stu-id="ae944-114">Cloud-delivered protection</span></span>
- <span data-ttu-id="ae944-115">Protection en temps réel toujours continue, y compris la protection comportementale, heuristique et basée sur l'apprentissage automatique</span><span class="sxs-lookup"><span data-stu-id="ae944-115">Always-on real-time protection, including behavioral, heuristic, and machine-learning-based protection</span></span>
- <span data-ttu-id="ae944-116">Interaction des utilisateurs finaux avec le client sur des points de terminaison individuels</span><span class="sxs-lookup"><span data-stu-id="ae944-116">How end users interact with the client on individual endpoints</span></span>

<span data-ttu-id="ae944-117">Les articles suivants décrivent comment effectuer des tâches clés lors de la configuration de l'Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="ae944-117">The following articles describe how to perform key tasks when configuring Microsoft Defender Antivirus.</span></span> <span data-ttu-id="ae944-118">Chaque article contient des instructions pour l'outil de configuration applicable (ou les outils).</span><span class="sxs-lookup"><span data-stu-id="ae944-118">Each article includes instructions for the applicable configuration tool (or tools).</span></span>

|<span data-ttu-id="ae944-119">Article</span><span class="sxs-lookup"><span data-stu-id="ae944-119">Article</span></span>  |<span data-ttu-id="ae944-120">Description</span><span class="sxs-lookup"><span data-stu-id="ae944-120">Description</span></span>  |
|---------|---------|
|[<span data-ttu-id="ae944-121">Utiliser la protection de l'Antivirus Microsoft Defender fournie par le cloud</span><span class="sxs-lookup"><span data-stu-id="ae944-121">Utilize Microsoft cloud-provided Microsoft Defender Antivirus protection</span></span>](cloud-protection-microsoft-defender-antivirus.md)     | <span data-ttu-id="ae944-122">Utilisez la protection cloud pour une détection avancée, rapide et robuste de l'antivirus.</span><span class="sxs-lookup"><span data-stu-id="ae944-122">Use cloud-delivered protection for advanced, fast, robust antivirus detection.</span></span>        |
|[<span data-ttu-id="ae944-123">Configurer la protection comportementale, heuristique et en temps réel</span><span class="sxs-lookup"><span data-stu-id="ae944-123">Configure behavioral, heuristic, and real-time protection</span></span>](configure-protection-features-microsoft-defender-antivirus.md)     |<span data-ttu-id="ae944-124">Activez la protection antivirus en temps réel, heuristique et basée sur le comportement.</span><span class="sxs-lookup"><span data-stu-id="ae944-124">Enable behavior-based, heuristic, and real-time antivirus protection.</span></span>         |
|[<span data-ttu-id="ae944-125">Configurer l'interaction de l'utilisateur final avec l'Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="ae944-125">Configure end-user interaction with Microsoft Defender Antivirus</span></span>](configure-end-user-interaction-microsoft-defender-antivirus.md) | <span data-ttu-id="ae944-126">Configurez la façon dont les utilisateurs finaux de votre organisation interagissent avec l'Antivirus Microsoft Defender, les notifications qu'ils voient et s'ils peuvent remplacer les paramètres.</span><span class="sxs-lookup"><span data-stu-id="ae944-126">Configure how end users in your organization interact with Microsoft Defender Antivirus, what notifications they see, and whether they can override settings.</span></span> |

> [!TIP]
> <span data-ttu-id="ae944-127">Vous pouvez également consulter les rubriques de référence pour les [outils](configuration-management-reference-microsoft-defender-antivirus.md) de gestion et de configuration pour obtenir une vue d'ensemble de chaque outil et des liens pour obtenir de l'aide supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="ae944-127">You can also review the [Reference topics for management and configuration tools](configuration-management-reference-microsoft-defender-antivirus.md) topic for an overview of each tool and links to further help.</span></span>