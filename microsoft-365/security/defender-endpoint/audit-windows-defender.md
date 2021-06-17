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
ms.topic: article
ms.technology: mde
ms.date: 06/02/2021
ms.openlocfilehash: 23de13e9a2b0fb02b95c9bb367c3fd99e11e89c8
ms.sourcegitcommit: 34c06715e036255faa75c66ebf95c12a85f8ef42
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2021
ms.locfileid: "52985095"
---
# <a name="test-attack-surface-reduction-in-microsoft-defender-for-endpoint"></a><span data-ttu-id="02c94-104">Tester la réduction de la surface d’attaque dans Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="02c94-104">Test attack surface reduction in Microsoft Defender for Endpoint</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="02c94-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="02c94-105">**Applies to:**</span></span>

- [<span data-ttu-id="02c94-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="02c94-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="02c94-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="02c94-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

<span data-ttu-id="02c94-108">Dans le cadre de l’équipe de sécurité de votre organisation, vous pouvez configurer les fonctionnalités de réduction de la surface d’attaque pour qu’elles s’exécutent en mode audit pour voir comment elles fonctionneront.</span><span class="sxs-lookup"><span data-stu-id="02c94-108">As part of your organization's security team, you can configure attack surface reduction capabilities to run in audit mode to see how they'll work.</span></span> <span data-ttu-id="02c94-109">En mode audit, vous pouvez activer :</span><span class="sxs-lookup"><span data-stu-id="02c94-109">In audit mode, you can enable:</span></span>

- <span data-ttu-id="02c94-110">Règles de réduction des surfaces d'attaque</span><span class="sxs-lookup"><span data-stu-id="02c94-110">Attack surface reduction rules</span></span>
- <span data-ttu-id="02c94-111">Exploit Protection</span><span class="sxs-lookup"><span data-stu-id="02c94-111">Exploit protection</span></span>
- <span data-ttu-id="02c94-112">Protection du réseau</span><span class="sxs-lookup"><span data-stu-id="02c94-112">Network protection</span></span>
- <span data-ttu-id="02c94-113">Accès contrôlé aux dossiers en mode audit</span><span class="sxs-lookup"><span data-stu-id="02c94-113">And controlled folder access in audit mode</span></span>

<span data-ttu-id="02c94-114">Le mode audit vous permet  d’enregistrer ce qui se serait passé si vous aviez activé la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="02c94-114">Audit mode lets you see a record of what *would* have happened if you had enabled the feature.</span></span>

<span data-ttu-id="02c94-115">Vous pouvez activer le mode audit lors du test du fonctionnement des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="02c94-115">You can enable audit mode when testing how the features will work.</span></span> <span data-ttu-id="02c94-116">Cela vous permettra de vous assurer que vos applications métier ne sont pas affectées.</span><span class="sxs-lookup"><span data-stu-id="02c94-116">This will help make sure your line-of-business apps aren't affected.</span></span> <span data-ttu-id="02c94-117">Vous pouvez également avoir une idée du nombre de tentatives de modification de fichier suspectes qui se produisent sur une période donnée.</span><span class="sxs-lookup"><span data-stu-id="02c94-117">You can also get an idea of how many suspicious file modification attempts occur over a certain period of time.</span></span>

<span data-ttu-id="02c94-118">Les fonctionnalités ne bloquent pas ou empêchent la modification des applications, des scripts ou des fichiers.</span><span class="sxs-lookup"><span data-stu-id="02c94-118">The features won't block or prevent apps, scripts, or files from being modified.</span></span> <span data-ttu-id="02c94-119">Toutefois, le Windows journal des événements enregistre les événements comme si les fonctionnalités étaient entièrement activées.</span><span class="sxs-lookup"><span data-stu-id="02c94-119">However, the Windows Event Log will record events as if the features were fully enabled.</span></span> <span data-ttu-id="02c94-120">Avec le mode audit, vous pouvez consulter le journal des événements pour voir l’impact que la fonctionnalité aurait eu si elle avait été activée.</span><span class="sxs-lookup"><span data-stu-id="02c94-120">With audit mode, you can review the event log to see what affect the feature would have had if it was enabled.</span></span>

<span data-ttu-id="02c94-121">Pour rechercher les entrées auditées, allez à **Applications et services**  >  **Microsoft**  >  **Windows**  >  **Windows Defender**  >  **Opérationnel**.</span><span class="sxs-lookup"><span data-stu-id="02c94-121">To find the audited entries, go to **Applications and Services** > **Microsoft** > **Windows** > **Windows Defender** > **Operational**.</span></span>

<span data-ttu-id="02c94-122">Utilisez Defender pour point de terminaison pour obtenir plus de détails pour chaque événement, en particulier pour examiner les règles de réduction de la surface d’attaque.</span><span class="sxs-lookup"><span data-stu-id="02c94-122">Use Defender for Endpoint to get greater details for each event, especially for investigating attack surface reduction rules.</span></span> <span data-ttu-id="02c94-123">L’utilisation de la console Defender for Endpoint vous permet d’examiner les problèmes dans le cadre de la chronologie des alertes et des [scénarios d’enquête.](investigate-alerts.md)</span><span class="sxs-lookup"><span data-stu-id="02c94-123">Using the Defender for Endpoint console lets you [investigate issues as part of the alert timeline and investigation scenarios](investigate-alerts.md).</span></span>

<span data-ttu-id="02c94-124">Vous pouvez activer le mode audit à l’aide de la stratégie de groupe, de PowerShell et des fournisseurs de services de configuration (CSP).</span><span class="sxs-lookup"><span data-stu-id="02c94-124">You can enable audit mode using Group Policy, PowerShell, and configuration service providers (CSPs).</span></span>

> [!TIP]
> <span data-ttu-id="02c94-125">Vous pouvez également consulter le site web Windows Defender Testground sur [demo.wd.microsoft.com](https://demo.wd.microsoft.com?ocid=cx-wddocs-testground) pour vérifier que les fonctionnalités fonctionnent et voir comment elles fonctionnent.</span><span class="sxs-lookup"><span data-stu-id="02c94-125">You can also visit the Windows Defender Testground website at [demo.wd.microsoft.com](https://demo.wd.microsoft.com?ocid=cx-wddocs-testground) to confirm the features are working and see how they work.</span></span>

| <span data-ttu-id="02c94-126">Options d’audit</span><span class="sxs-lookup"><span data-stu-id="02c94-126">Audit options</span></span> | <span data-ttu-id="02c94-127">Comment activer le mode audit</span><span class="sxs-lookup"><span data-stu-id="02c94-127">How to enable audit mode</span></span> | <span data-ttu-id="02c94-128">Comment afficher les événements</span><span class="sxs-lookup"><span data-stu-id="02c94-128">How to view events</span></span> |
|---------|---------|---------|
| <span data-ttu-id="02c94-129">L’audit s’applique à tous les événements</span><span class="sxs-lookup"><span data-stu-id="02c94-129">Audit applies to all events</span></span> | [<span data-ttu-id="02c94-130">Activer l’accès contrôlé aux dossiers</span><span class="sxs-lookup"><span data-stu-id="02c94-130">Enable controlled folder access</span></span>](enable-controlled-folders.md) | [<span data-ttu-id="02c94-131">Événements d’accès contrôlé aux dossiers</span><span class="sxs-lookup"><span data-stu-id="02c94-131">Controlled folder access events</span></span>](evaluate-controlled-folder-access.md#review-controlled-folder-access-events-in-windows-event-viewer)
| <span data-ttu-id="02c94-132">L’audit s’applique à des règles individuelles</span><span class="sxs-lookup"><span data-stu-id="02c94-132">Audit applies to individual rules</span></span> | [<span data-ttu-id="02c94-133">Activer les règles de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="02c94-133">Enable attack surface reduction rules</span></span>](enable-attack-surface-reduction.md) | [<span data-ttu-id="02c94-134">Événements de règle de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="02c94-134">Attack surface reduction rule events</span></span>](evaluate-attack-surface-reduction.md#review-attack-surface-reduction-events-in-windows-event-viewer)
| <span data-ttu-id="02c94-135">L’audit s’applique à tous les événements</span><span class="sxs-lookup"><span data-stu-id="02c94-135">Audit applies to all events</span></span> | [<span data-ttu-id="02c94-136">Activer la protection réseau</span><span class="sxs-lookup"><span data-stu-id="02c94-136">Enable network protection</span></span>](enable-network-protection.md) | [<span data-ttu-id="02c94-137">Événements de protection du réseau</span><span class="sxs-lookup"><span data-stu-id="02c94-137">Network protection events</span></span>](evaluate-network-protection.md#review-network-protection-events-in-windows-event-viewer)
| <span data-ttu-id="02c94-138">L’audit s’applique aux atténuations individuelles</span><span class="sxs-lookup"><span data-stu-id="02c94-138">Audit applies to individual mitigations</span></span> | [<span data-ttu-id="02c94-139">Activer la protection la protection contre les codes malveillants exploitant une faille de sécurité</span><span class="sxs-lookup"><span data-stu-id="02c94-139">Enable exploit protection</span></span>](enable-exploit-protection.md) | [<span data-ttu-id="02c94-140">Événements Exploit Protection</span><span class="sxs-lookup"><span data-stu-id="02c94-140">Exploit protection events</span></span>](exploit-protection.md#review-exploit-protection-events-in-windows-event-viewer)
