---
title: Tester le fonctionnement des fonctionnalités de Microsoft Defender for Endpoint en mode audit
description: Le mode audit vous permet de voir comment Microsoft Defender pour point de terminaison protégerait vos appareils s’il était activé.
keywords: exploit guard, audit, audit, mode, activé, désactivé, test, démonstration, évaluer, atelier
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: Normal
audience: ITPro
author: denisebmsft
ms.author: deniseb
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.date: 06/02/2021
ms.topic: article
ms.openlocfilehash: e78b21b751aa398ed4449fb398f12b60f1929873
ms.sourcegitcommit: 2cf7293d610a676726ac891b89366e23810d9142
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/10/2021
ms.locfileid: "52866678"
---
# <a name="test-attack-surface-reduction-in-microsoft-defender-for-endpoint"></a><span data-ttu-id="2e0a5-104">Tester la réduction de la surface d’attaque dans Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="2e0a5-104">Test attack surface reduction in Microsoft Defender for Endpoint</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="2e0a5-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="2e0a5-105">**Applies to:**</span></span>
- [<span data-ttu-id="2e0a5-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="2e0a5-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="2e0a5-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="2e0a5-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

<span data-ttu-id="2e0a5-108">Si vous faites partie de l’équipe de sécurité de votre organisation, vous pouvez configurer les fonctionnalités de réduction de la surface d’attaque pour qu’elles s’exécutent en mode audit pour voir comment elles fonctionneront dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="2e0a5-108">If you're part of your organization's security team, you can configure attack surface reduction capabilities to run in audit mode to see how they'll work in your organization.</span></span> <span data-ttu-id="2e0a5-109">En particulier, vous pouvez activer les règles de réduction de la surface d’attaque, exploit protection, protection du réseau et accès contrôlé aux dossiers en mode audit.</span><span class="sxs-lookup"><span data-stu-id="2e0a5-109">In particular, you can enable attack surface reduction rules, exploit protection, network protection, and controlled folder access in audit mode.</span></span> <span data-ttu-id="2e0a5-110">Le mode audit vous permet  d’enregistrer ce qui se serait passé si vous aviez activé la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="2e0a5-110">Audit mode lets you see a record of what *would* have happened if you had enabled the feature.</span></span>

<span data-ttu-id="2e0a5-111">Vous pouvez activer le mode audit lors du test du fonctionnement des fonctionnalités dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="2e0a5-111">You may want to enable audit mode when testing how the features will work in your organization.</span></span> <span data-ttu-id="2e0a5-112">Cela vous permettra de vous assurer que vos applications métier ne sont pas affectées.</span><span class="sxs-lookup"><span data-stu-id="2e0a5-112">This will help make sure your line-of-business apps aren't affected.</span></span> <span data-ttu-id="2e0a5-113">Vous pouvez également avoir une idée du nombre de tentatives de modification de fichier suspectes qui se produisent sur une certaine période de temps.</span><span class="sxs-lookup"><span data-stu-id="2e0a5-113">You can also get an idea of how many suspicious file modification attempts occur over a certain period of time.</span></span>

<span data-ttu-id="2e0a5-114">Les fonctionnalités ne bloquent pas ou n’empêchent pas les applications, les scripts ou les fichiers d’être modifiés.</span><span class="sxs-lookup"><span data-stu-id="2e0a5-114">The features won't block or prevent apps, scripts, or files from being modified.</span></span> <span data-ttu-id="2e0a5-115">Toutefois, le Windows journal des événements enregistre les événements comme si les fonctionnalités étaient entièrement activées.</span><span class="sxs-lookup"><span data-stu-id="2e0a5-115">However, the Windows Event Log will record events as if the features were fully enabled.</span></span> <span data-ttu-id="2e0a5-116">Avec le mode audit, vous pouvez consulter le journal des événements pour voir l’impact que la fonctionnalité aurait eu si elle était activée.</span><span class="sxs-lookup"><span data-stu-id="2e0a5-116">With audit mode, you can review the event log to see what impact the feature would have had if it was enabled.</span></span>

<span data-ttu-id="2e0a5-117">Pour rechercher les entrées auditées, allez à **Applications et services**  >  **Microsoft**  >  **Windows**  >  **Windows Defender**  >  **Opérationnel**.</span><span class="sxs-lookup"><span data-stu-id="2e0a5-117">To find the audited entries, go to **Applications and Services** > **Microsoft** > **Windows** > **Windows Defender** > **Operational**.</span></span>

<span data-ttu-id="2e0a5-118">Vous pouvez utiliser Defender pour le point de terminaison pour obtenir des détails plus détaillés pour chaque événement, en particulier pour examiner les règles de réduction de la surface d’attaque.</span><span class="sxs-lookup"><span data-stu-id="2e0a5-118">You can use Defender for Endpoint to get greater details for each event, especially for investigating attack surface reduction rules.</span></span> <span data-ttu-id="2e0a5-119">L’utilisation de la console Defender for Endpoint vous permet d’examiner les problèmes dans le cadre de la chronologie des alertes et des [scénarios d’enquête.](investigate-alerts.md)</span><span class="sxs-lookup"><span data-stu-id="2e0a5-119">Using the Defender for Endpoint console lets you [investigate issues as part of the alert timeline and investigation scenarios](investigate-alerts.md).</span></span>

<span data-ttu-id="2e0a5-120">Vous pouvez utiliser la stratégie de groupe, PowerShell et les fournisseurs de services de configuration (CSP) pour activer le mode audit.</span><span class="sxs-lookup"><span data-stu-id="2e0a5-120">You can use Group Policy, PowerShell, and configuration service providers (CSPs) to enable audit mode.</span></span>

> [!TIP]
> <span data-ttu-id="2e0a5-121">Vous pouvez également consulter le site web Windows Defender Testground sur [demo.wd.microsoft.com](https://demo.wd.microsoft.com?ocid=cx-wddocs-testground) pour vérifier que les fonctionnalités fonctionnent et voir comment elles fonctionnent.</span><span class="sxs-lookup"><span data-stu-id="2e0a5-121">You can also visit the Windows Defender Testground website at [demo.wd.microsoft.com](https://demo.wd.microsoft.com?ocid=cx-wddocs-testground) to confirm the features are working and see how they work.</span></span>

| <span data-ttu-id="2e0a5-122">Options d’audit</span><span class="sxs-lookup"><span data-stu-id="2e0a5-122">Audit options</span></span> | <span data-ttu-id="2e0a5-123">Comment activer le mode audit</span><span class="sxs-lookup"><span data-stu-id="2e0a5-123">How to enable audit mode</span></span> | <span data-ttu-id="2e0a5-124">Comment afficher les événements</span><span class="sxs-lookup"><span data-stu-id="2e0a5-124">How to view events</span></span> |
|---------|---------|---------|
| <span data-ttu-id="2e0a5-125">L’audit s’applique à tous les événements</span><span class="sxs-lookup"><span data-stu-id="2e0a5-125">Audit applies to all events</span></span> | [<span data-ttu-id="2e0a5-126">Activer l’accès contrôlé aux dossiers</span><span class="sxs-lookup"><span data-stu-id="2e0a5-126">Enable controlled folder access</span></span>](enable-controlled-folders.md) | [<span data-ttu-id="2e0a5-127">Événements d’accès contrôlé aux dossiers</span><span class="sxs-lookup"><span data-stu-id="2e0a5-127">Controlled folder access events</span></span>](evaluate-controlled-folder-access.md#review-controlled-folder-access-events-in-windows-event-viewer)
| <span data-ttu-id="2e0a5-128">L’audit s’applique à des règles individuelles</span><span class="sxs-lookup"><span data-stu-id="2e0a5-128">Audit applies to individual rules</span></span> | [<span data-ttu-id="2e0a5-129">Activer les règles de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="2e0a5-129">Enable attack surface reduction rules</span></span>](enable-attack-surface-reduction.md) | [<span data-ttu-id="2e0a5-130">Événements de règle de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="2e0a5-130">Attack surface reduction rule events</span></span>](evaluate-attack-surface-reduction.md#review-attack-surface-reduction-events-in-windows-event-viewer)
| <span data-ttu-id="2e0a5-131">L’audit s’applique à tous les événements</span><span class="sxs-lookup"><span data-stu-id="2e0a5-131">Audit applies to all events</span></span> | [<span data-ttu-id="2e0a5-132">Activer la protection réseau</span><span class="sxs-lookup"><span data-stu-id="2e0a5-132">Enable network protection</span></span>](enable-network-protection.md) | [<span data-ttu-id="2e0a5-133">Événements de protection du réseau</span><span class="sxs-lookup"><span data-stu-id="2e0a5-133">Network protection events</span></span>](evaluate-network-protection.md#review-network-protection-events-in-windows-event-viewer)
| <span data-ttu-id="2e0a5-134">L’audit s’applique aux atténuations individuelles</span><span class="sxs-lookup"><span data-stu-id="2e0a5-134">Audit applies to individual mitigations</span></span> | [<span data-ttu-id="2e0a5-135">Activer la protection la protection contre les codes malveillants exploitant une faille de sécurité</span><span class="sxs-lookup"><span data-stu-id="2e0a5-135">Enable exploit protection</span></span>](enable-exploit-protection.md) | [<span data-ttu-id="2e0a5-136">Événements Exploit Protection</span><span class="sxs-lookup"><span data-stu-id="2e0a5-136">Exploit protection events</span></span>](exploit-protection.md#review-exploit-protection-events-in-windows-event-viewer)


