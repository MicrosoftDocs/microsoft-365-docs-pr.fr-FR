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
author: dansimp
ms.author: dansimp
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.openlocfilehash: 7ce652d58be2d9ff28d82c088d5471a7bffdf6dc
ms.sourcegitcommit: 6e5c00f84b5201422aed094f2697016407df8fc2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "51570971"
---
# <a name="test-how-microsoft-defender-for-endpoint-features-work-in-audit-mode"></a><span data-ttu-id="881a8-104">Tester le fonctionnement des fonctionnalités de Microsoft Defender for Endpoint en mode audit</span><span class="sxs-lookup"><span data-stu-id="881a8-104">Test how Microsoft Defender for Endpoint features work in audit mode</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="881a8-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="881a8-105">**Applies to:**</span></span>
- [<span data-ttu-id="881a8-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="881a8-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="881a8-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="881a8-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


<span data-ttu-id="881a8-108">Vous pouvez activer les règles de réduction de la surface d’attaque, Exploit Protection, la protection réseau et l’accès contrôlé aux dossiers en mode audit.</span><span class="sxs-lookup"><span data-stu-id="881a8-108">You can enable attack surface reduction rules, exploit protection, network protection, and controlled folder access in audit mode.</span></span> <span data-ttu-id="881a8-109">Le mode audit vous permet  d’enregistrer ce qui se serait passé si vous aviez activé la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="881a8-109">Audit mode lets you see a record of what *would* have happened if you had enabled the feature.</span></span>

<span data-ttu-id="881a8-110">Vous pouvez activer le mode audit lors du test du fonctionnement des fonctionnalités dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="881a8-110">You may want to enable audit mode when testing how the features will work in your organization.</span></span> <span data-ttu-id="881a8-111">Cela vous permettra de vous assurer que vos applications métier ne sont pas affectées.</span><span class="sxs-lookup"><span data-stu-id="881a8-111">This will help make sure your line-of-business apps aren't affected.</span></span> <span data-ttu-id="881a8-112">Vous pouvez également avoir une idée du nombre de tentatives de modification de fichier suspectes qui se produisent sur une période donnée.</span><span class="sxs-lookup"><span data-stu-id="881a8-112">You can also get an idea of how many suspicious file modification attempts occur over a certain period of time.</span></span>

<span data-ttu-id="881a8-113">Les fonctionnalités ne bloquent pas ou empêchent la modification des applications, des scripts ou des fichiers.</span><span class="sxs-lookup"><span data-stu-id="881a8-113">The features won't block or prevent apps, scripts, or files from being modified.</span></span> <span data-ttu-id="881a8-114">Toutefois, le journal des événements Windows enregistre les événements comme si les fonctionnalités étaient entièrement activées.</span><span class="sxs-lookup"><span data-stu-id="881a8-114">However, the Windows Event Log will record events as if the features were fully enabled.</span></span> <span data-ttu-id="881a8-115">Avec le mode audit, vous pouvez consulter le journal des événements pour voir l’impact que la fonctionnalité aurait eu si elle était activée.</span><span class="sxs-lookup"><span data-stu-id="881a8-115">With audit mode, you can review the event log to see what impact the feature would have had if it was enabled.</span></span>

<span data-ttu-id="881a8-116">Pour rechercher les entrées auditées, go to **Applications and Services**  >  **Microsoft**  >  **Windows**  >  **Windows Defender**  >  **Operational**.</span><span class="sxs-lookup"><span data-stu-id="881a8-116">To find the audited entries, go to **Applications and Services** > **Microsoft** > **Windows** > **Windows Defender** > **Operational**.</span></span>

<span data-ttu-id="881a8-117">Vous pouvez utiliser Defender pour le point de terminaison pour obtenir des détails plus détaillés pour chaque événement, en particulier pour examiner les règles de réduction de la surface d’attaque.</span><span class="sxs-lookup"><span data-stu-id="881a8-117">You can use Defender for Endpoint to get greater details for each event, especially for investigating attack surface reduction rules.</span></span> <span data-ttu-id="881a8-118">L’utilisation de la console Defender for Endpoint vous permet d’examiner les problèmes dans le cadre de la chronologie des alertes et des [scénarios d’enquête.](investigate-alerts.md)</span><span class="sxs-lookup"><span data-stu-id="881a8-118">Using the Defender for Endpoint console lets you [investigate issues as part of the alert timeline and investigation scenarios](investigate-alerts.md).</span></span>

<span data-ttu-id="881a8-119">Vous pouvez utiliser la stratégie de groupe, PowerShell et les fournisseurs de services de configuration (CSP) pour activer le mode audit.</span><span class="sxs-lookup"><span data-stu-id="881a8-119">You can use Group Policy, PowerShell, and configuration service providers (CSPs) to enable audit mode.</span></span>

> [!TIP]
> <span data-ttu-id="881a8-120">Vous pouvez également consulter le site Windows Defender Testground sur [demo.wd.microsoft.com](https://demo.wd.microsoft.com?ocid=cx-wddocs-testground) pour vérifier que les fonctionnalités fonctionnent et voir comment elles fonctionnent.</span><span class="sxs-lookup"><span data-stu-id="881a8-120">You can also visit the Windows Defender Testground website at [demo.wd.microsoft.com](https://demo.wd.microsoft.com?ocid=cx-wddocs-testground) to confirm the features are working and see how they work.</span></span>

 <span data-ttu-id="881a8-121">**Options d’audit**</span><span class="sxs-lookup"><span data-stu-id="881a8-121">**Audit options**</span></span> | <span data-ttu-id="881a8-122">**Comment activer le mode audit**</span><span class="sxs-lookup"><span data-stu-id="881a8-122">**How to enable audit mode**</span></span> | <span data-ttu-id="881a8-123">**Comment afficher les événements**</span><span class="sxs-lookup"><span data-stu-id="881a8-123">**How to view events**</span></span>
|---------|---------|---------|
| <span data-ttu-id="881a8-124">L’audit s’applique à tous les événements</span><span class="sxs-lookup"><span data-stu-id="881a8-124">Audit applies to all events</span></span> | [<span data-ttu-id="881a8-125">Activer l’accès contrôlé aux dossiers</span><span class="sxs-lookup"><span data-stu-id="881a8-125">Enable controlled folder access</span></span>](enable-controlled-folders.md) | [<span data-ttu-id="881a8-126">Événements d’accès contrôlé aux dossiers</span><span class="sxs-lookup"><span data-stu-id="881a8-126">Controlled folder access events</span></span>](evaluate-controlled-folder-access.md#review-controlled-folder-access-events-in-windows-event-viewer)
| <span data-ttu-id="881a8-127">L’audit s’applique à des règles individuelles</span><span class="sxs-lookup"><span data-stu-id="881a8-127">Audit applies to individual rules</span></span> | [<span data-ttu-id="881a8-128">Activer les règles de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="881a8-128">Enable attack surface reduction rules</span></span>](enable-attack-surface-reduction.md) | [<span data-ttu-id="881a8-129">Événements de règle de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="881a8-129">Attack surface reduction rule events</span></span>](evaluate-attack-surface-reduction.md#review-attack-surface-reduction-events-in-windows-event-viewer)
| <span data-ttu-id="881a8-130">L’audit s’applique à tous les événements</span><span class="sxs-lookup"><span data-stu-id="881a8-130">Audit applies to all events</span></span> | [<span data-ttu-id="881a8-131">Activer la protection réseau</span><span class="sxs-lookup"><span data-stu-id="881a8-131">Enable network protection</span></span>](enable-network-protection.md) | [<span data-ttu-id="881a8-132">Événements de protection du réseau</span><span class="sxs-lookup"><span data-stu-id="881a8-132">Network protection events</span></span>](evaluate-network-protection.md#review-network-protection-events-in-windows-event-viewer)
| <span data-ttu-id="881a8-133">L’audit s’applique aux atténuations individuelles</span><span class="sxs-lookup"><span data-stu-id="881a8-133">Audit applies to individual mitigations</span></span> | [<span data-ttu-id="881a8-134">Activer la protection la protection contre les codes malveillants exploitant une faille de sécurité</span><span class="sxs-lookup"><span data-stu-id="881a8-134">Enable exploit protection</span></span>](enable-exploit-protection.md) | [<span data-ttu-id="881a8-135">Événements Exploit Protection</span><span class="sxs-lookup"><span data-stu-id="881a8-135">Exploit protection events</span></span>](exploit-protection.md#review-exploit-protection-events-in-windows-event-viewer)

## <a name="related-topics"></a><span data-ttu-id="881a8-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="881a8-136">Related topics</span></span>

* [<span data-ttu-id="881a8-137">Protéger les appareils contre les codes malveillants exploitant une faille de sécurité</span><span class="sxs-lookup"><span data-stu-id="881a8-137">Protect devices from exploits</span></span>](exploit-protection.md)
* [<span data-ttu-id="881a8-138">Réduire les surfaces d’attaque avec des règles de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="881a8-138">Reduce attack surfaces with attack surface reduction rules</span></span>](attack-surface-reduction.md)
* [<span data-ttu-id="881a8-139">Protéger votre réseau</span><span class="sxs-lookup"><span data-stu-id="881a8-139">Protect your network</span></span>](network-protection.md)
* [<span data-ttu-id="881a8-140">Protéger les dossiers importants</span><span class="sxs-lookup"><span data-stu-id="881a8-140">Protect important folders</span></span>](controlled-folders.md)
