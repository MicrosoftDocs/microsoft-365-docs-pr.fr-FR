---
title: Évaluer les règles de réduction de la surface d’attaque
description: Découvrez comment la réduction de la surface d’attaque bloquerait et empêcherait les attaques à l’aide de l’outil de démonstration personnalisé.
keywords: Réduction de la surface d’attaque, système de prévention des intrusions hôtes, règles de protection, anti-attaque, attaque, prévention des infections, évaluer, tester, démonstration
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
localization_priority: Normal
audience: ITPro
author: dansimp
ms.author: dansimp
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.openlocfilehash: 07573fd92643ce5fdf3e9140031bf5f15ae8f7aa
ms.sourcegitcommit: 6e5c00f84b5201422aed094f2697016407df8fc2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "51570338"
---
# <a name="evaluate-attack-surface-reduction-rules"></a><span data-ttu-id="1ac38-104">Évaluer les règles de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="1ac38-104">Evaluate attack surface reduction rules</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="1ac38-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="1ac38-105">**Applies to:**</span></span>
- [<span data-ttu-id="1ac38-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="1ac38-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="1ac38-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="1ac38-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="1ac38-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="1ac38-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="1ac38-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="1ac38-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-enablesiem-abovefoldlink)

<span data-ttu-id="1ac38-110">Les règles de réduction de la surface d’attaque permettent d’empêcher les actions généralement utilisées par les programmes malveillants pour compromettre les appareils ou les réseaux.</span><span class="sxs-lookup"><span data-stu-id="1ac38-110">Attack surface reduction rules help prevent actions typically used by malware to compromise devices or networks.</span></span> <span data-ttu-id="1ac38-111">Définissez des règles de réduction de la surface d’attaque pour les appareils exécutant l’une des éditions et versions suivantes de Windows :</span><span class="sxs-lookup"><span data-stu-id="1ac38-111">Set attack surface reduction rules for devices running any of the following editions and versions of Windows:</span></span>

- <span data-ttu-id="1ac38-112">Windows 10 Professionnel, [version 1709 ou](https://docs.microsoft.com/windows/whats-new/whats-new-windows-10-version-1709) ultérieure</span><span class="sxs-lookup"><span data-stu-id="1ac38-112">Windows 10 Pro, [version 1709](https://docs.microsoft.com/windows/whats-new/whats-new-windows-10-version-1709) or later</span></span>
- <span data-ttu-id="1ac38-113">Windows 10 Entreprise, [version 1709 ou](https://docs.microsoft.com/windows/whats-new/whats-new-windows-10-version-1709) ultérieure</span><span class="sxs-lookup"><span data-stu-id="1ac38-113">Windows 10 Enterprise, [version 1709](https://docs.microsoft.com/windows/whats-new/whats-new-windows-10-version-1709) or later</span></span>
- <span data-ttu-id="1ac38-114">Windows Server, [version 1803 (canal semi-annuel)](https://docs.microsoft.com/windows-server/get-started/whats-new-in-windows-server-1803) ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="1ac38-114">Windows Server, [version 1803 (Semi-Annual Channel)](https://docs.microsoft.com/windows-server/get-started/whats-new-in-windows-server-1803) or later</span></span>
- [<span data-ttu-id="1ac38-115">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="1ac38-115">Windows Server 2019</span></span>](https://docs.microsoft.com/windows-server/get-started-19/whats-new-19)

<span data-ttu-id="1ac38-116">Découvrez comment évaluer les règles de réduction de la surface d’attaque en activant le mode audit pour tester la fonctionnalité directement dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1ac38-116">Learn how to evaluate attack surface reduction rules by enabling audit mode to test the feature directly in your organization.</span></span>

> [!TIP]
> <span data-ttu-id="1ac38-117">Vous pouvez également consulter le site web du scénario de démonstration microsoft Defender pour point de terminaison [sur demo.wd.microsoft.com](https://demo.wd.microsoft.com?ocid=cx-wddocs-testground) pour vérifier que la fonctionnalité fonctionne et voir comment elle fonctionne.</span><span class="sxs-lookup"><span data-stu-id="1ac38-117">You can also visit the Microsoft Defender for Endpoint demo scenario website at [demo.wd.microsoft.com](https://demo.wd.microsoft.com?ocid=cx-wddocs-testground) to confirm the feature is working and see how it works.</span></span>

## <a name="use-audit-mode-to-measure-impact"></a><span data-ttu-id="1ac38-118">Utiliser le mode audit pour mesurer l’impact</span><span class="sxs-lookup"><span data-stu-id="1ac38-118">Use audit mode to measure impact</span></span>

<span data-ttu-id="1ac38-119">Activez les règles de réduction de la surface d’attaque en mode audit pour afficher un enregistrement des applications qui auraient été bloquées si la fonctionnalité était entièrement activée.</span><span class="sxs-lookup"><span data-stu-id="1ac38-119">Enable attack surface reduction rules in audit mode to view a record of apps that would have been blocked if the feature was fully enabled.</span></span> <span data-ttu-id="1ac38-120">Testez le fonctionnement de la fonctionnalité dans votre organisation pour vous assurer qu’elle n’affecte pas vos applications métier.</span><span class="sxs-lookup"><span data-stu-id="1ac38-120">Test how the feature will work in your organization to ensure it doesn't affect your line-of-business apps.</span></span> <span data-ttu-id="1ac38-121">Vous pouvez également avoir une idée de la fréquence de tir des règles lors d’une utilisation normale.</span><span class="sxs-lookup"><span data-stu-id="1ac38-121">You can also get an idea of how often the rules will fire during normal use.</span></span>

<span data-ttu-id="1ac38-122">Pour activer une règle de réduction de la surface d’attaque en mode audit, utilisez l’cmdlet PowerShell suivante :</span><span class="sxs-lookup"><span data-stu-id="1ac38-122">To enable an attack surface reduction rule in audit mode, use the following PowerShell cmdlet:</span></span>

```PowerShell
Add-MpPreference -AttackSurfaceReductionRules_Ids <rule ID> -AttackSurfaceReductionRules_Actions AuditMode
```

<span data-ttu-id="1ac38-123">Où `<rule ID>` se trouve une valeur GUID de la règle de réduction de la surface [d’attaque](attack-surface-reduction.md#attack-surface-reduction-rules).</span><span class="sxs-lookup"><span data-stu-id="1ac38-123">Where `<rule ID>` is a [GUID value of the attack surface reduction rule](attack-surface-reduction.md#attack-surface-reduction-rules).</span></span>

<span data-ttu-id="1ac38-124">Pour activer toutes les règles de réduction de la surface d’attaque ajoutées en mode audit, utilisez l’cmdlet PowerShell suivante :</span><span class="sxs-lookup"><span data-stu-id="1ac38-124">To enable all the added attack surface reduction rules in audit mode, use the following PowerShell cmdlet:</span></span>

```PowerShell
(Get-MpPreference).AttackSurfaceReductionRules_Ids | Foreach {Add-MpPreference -AttackSurfaceReductionRules_Ids $_ -AttackSurfaceReductionRules_Actions AuditMode}
```

> [!TIP]
> <span data-ttu-id="1ac38-125">Si vous souhaitez auditer complètement le fonctionnement des règles de réduction de la surface d’attaque dans votre organisation, vous devez utiliser un outil de gestion pour déployer ce paramètre sur les appareils de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="1ac38-125">If you want to fully audit how attack surface reduction rules will work in your organization, you'll need to use a management tool to deploy this setting to devices in your network(s).</span></span>

<span data-ttu-id="1ac38-126">Vous pouvez également utiliser une stratégie de groupe, Intune ou des fournisseurs de services de configuration (CSP) de gestion des périphériques mobiles (CSP) pour configurer et déployer le paramètre.</span><span class="sxs-lookup"><span data-stu-id="1ac38-126">You can also use Group Policy, Intune, or mobile device management (MDM) configuration service providers (CSPs) to configure and deploy the setting.</span></span> <span data-ttu-id="1ac38-127">En savoir plus dans l’article principal des règles de [réduction de la surface d’attaque.](attack-surface-reduction.md)</span><span class="sxs-lookup"><span data-stu-id="1ac38-127">Learn more in the main [Attack surface reduction rules](attack-surface-reduction.md) article.</span></span>

## <a name="review-attack-surface-reduction-events-in-windows-event-viewer"></a><span data-ttu-id="1ac38-128">Passer en revue les événements de réduction de la surface d’attaque dans l’Observateur d’événements Windows</span><span class="sxs-lookup"><span data-stu-id="1ac38-128">Review attack surface reduction events in Windows Event Viewer</span></span>

<span data-ttu-id="1ac38-129">Pour passer en revue les applications qui auraient été bloquées, ouvrez l’Observateur d’événements et filtrez l’ID d’événement 1121 dans le journal microsoft-windows-Windows Defender/opérationnel.</span><span class="sxs-lookup"><span data-stu-id="1ac38-129">To review apps that would have been blocked, open Event Viewer and filter for Event ID 1121 in the Microsoft-Windows-Windows Defender/Operational log.</span></span> <span data-ttu-id="1ac38-130">Le tableau suivant répertorie tous les événements de protection réseau.</span><span class="sxs-lookup"><span data-stu-id="1ac38-130">The following table lists all network protection events.</span></span>

<span data-ttu-id="1ac38-131">ID de l'événement</span><span class="sxs-lookup"><span data-stu-id="1ac38-131">Event ID</span></span> | <span data-ttu-id="1ac38-132">Description</span><span class="sxs-lookup"><span data-stu-id="1ac38-132">Description</span></span>
-|-
 <span data-ttu-id="1ac38-133">5007</span><span class="sxs-lookup"><span data-stu-id="1ac38-133">5007</span></span> | <span data-ttu-id="1ac38-134">Événement lorsque les paramètres sont modifiés</span><span class="sxs-lookup"><span data-stu-id="1ac38-134">Event when settings are changed</span></span>
 <span data-ttu-id="1ac38-135">1121</span><span class="sxs-lookup"><span data-stu-id="1ac38-135">1121</span></span> | <span data-ttu-id="1ac38-136">Événement lorsqu’une règle de réduction de la surface d’attaque se déclenche en mode blocage</span><span class="sxs-lookup"><span data-stu-id="1ac38-136">Event when an attack surface reduction rule fires in block mode</span></span>
 <span data-ttu-id="1ac38-137">1122</span><span class="sxs-lookup"><span data-stu-id="1ac38-137">1122</span></span> | <span data-ttu-id="1ac38-138">Événement lorsqu’une règle de réduction de la surface d’attaque se déclenche en mode audit</span><span class="sxs-lookup"><span data-stu-id="1ac38-138">Event when an attack surface reduction rule fires in audit mode</span></span>

## <a name="customize-attack-surface-reduction-rules"></a><span data-ttu-id="1ac38-139">Personnaliser les règles de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="1ac38-139">Customize attack surface reduction rules</span></span>

<span data-ttu-id="1ac38-140">Au cours de votre évaluation, vous pouvez configurer chaque règle individuellement ou exclure certains fichiers et processus de l’évaluation par la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="1ac38-140">During your evaluation, you may wish to configure each rule individually or exclude certain files and processes from being evaluated by the feature.</span></span>

<span data-ttu-id="1ac38-141">Voir [Personnaliser les règles de réduction de la surface](customize-attack-surface-reduction.md) d’attaque pour plus d’informations sur la configuration de la fonctionnalité avec les outils de gestion, y compris la stratégie de groupe et les stratégies CSP mdM.</span><span class="sxs-lookup"><span data-stu-id="1ac38-141">See [Customize attack surface reduction rules](customize-attack-surface-reduction.md) for information on configuring the feature with management tools, including Group Policy and MDM CSP policies.</span></span>

## <a name="see-also"></a><span data-ttu-id="1ac38-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ac38-142">See also</span></span>

* [<span data-ttu-id="1ac38-143">Réduire les surfaces d’attaque avec des règles de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="1ac38-143">Reduce attack surfaces with attack surface reduction rules</span></span>](attack-surface-reduction.md)
* [<span data-ttu-id="1ac38-144">Utiliser le mode audit pour évaluer les Windows Defender</span><span class="sxs-lookup"><span data-stu-id="1ac38-144">Use audit mode to evaluate Windows Defender</span></span>](audit-windows-defender.md)
* <span data-ttu-id="1ac38-145">[FAQ sur la réduction de la surface d’attaque](attack-surface-reduction.md).</span><span class="sxs-lookup"><span data-stu-id="1ac38-145">[Attack surface reduction FAQ](attack-surface-reduction.md)</span></span>
