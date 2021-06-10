---
title: Évaluer les règles de réduction de la surface d’attaque
description: Découvrez comment la réduction de la surface d’attaque bloquerait et empêcherait les attaques à l’aide de l’outil de démonstration personnalisé.
keywords: Réduction de la surface d’attaque, système de prévention des intrusions hôtes, règles de protection, anti-attaque, attaque, prévention des infections, évaluer, tester, démonstration
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.topic: article
localization_priority: Normal
audience: ITPro
author: denisebmsft
ms.author: deniseb
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.openlocfilehash: c2dea22cc8a0ebb875f83ebd5a3e42f723e5f254
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52771320"
---
# <a name="evaluate-attack-surface-reduction-rules"></a><span data-ttu-id="6e29d-104">Évaluer les règles de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="6e29d-104">Evaluate attack surface reduction rules</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="6e29d-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="6e29d-105">**Applies to:**</span></span>

- [<span data-ttu-id="6e29d-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="6e29d-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="6e29d-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6e29d-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="6e29d-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="6e29d-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="6e29d-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="6e29d-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-enablesiem-abovefoldlink)

<span data-ttu-id="6e29d-110">Les règles de réduction de la surface d’attaque permettent d’empêcher les actions généralement utilisées par les programmes malveillants pour compromettre les appareils ou les réseaux.</span><span class="sxs-lookup"><span data-stu-id="6e29d-110">Attack surface reduction rules help prevent actions typically used by malware to compromise devices or networks.</span></span> <span data-ttu-id="6e29d-111">Les règles de réduction de la surface d’attaque permettent de fermer la plupart des points d’entrée courants utilisés par les programmes malveillants et les ransomware.</span><span class="sxs-lookup"><span data-stu-id="6e29d-111">Attack surface reduction rules help close off many of the common entry points used by malware and ransomware.</span></span> 

<span data-ttu-id="6e29d-112">Définissez des règles de réduction de la surface d’attaque pour les appareils exécutant l’une des éditions et versions de Windows :</span><span class="sxs-lookup"><span data-stu-id="6e29d-112">Set attack surface reduction rules for devices running any of the following editions and versions of Windows:</span></span>

- <span data-ttu-id="6e29d-113">Windows 10 Professionnel, [version 1709 ou](/windows/whats-new/whats-new-windows-10-version-1709) ultérieure</span><span class="sxs-lookup"><span data-stu-id="6e29d-113">Windows 10 Pro, [version 1709](/windows/whats-new/whats-new-windows-10-version-1709) or later</span></span>
- <span data-ttu-id="6e29d-114">Windows 10 Entreprise, [version 1709 ou](/windows/whats-new/whats-new-windows-10-version-1709) ultérieure</span><span class="sxs-lookup"><span data-stu-id="6e29d-114">Windows 10 Enterprise, [version 1709](/windows/whats-new/whats-new-windows-10-version-1709) or later</span></span>
- <span data-ttu-id="6e29d-115">Windows Serveur, [version 1803 (canal semi-annuel)](/windows-server/get-started/whats-new-in-windows-server-1803) ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="6e29d-115">Windows Server, [version 1803 (Semi-Annual Channel)](/windows-server/get-started/whats-new-in-windows-server-1803) or later</span></span>
- [<span data-ttu-id="6e29d-116">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="6e29d-116">Windows Server 2019</span></span>](/windows-server/get-started-19/whats-new-19)

<span data-ttu-id="6e29d-117">Découvrez comment évaluer les règles de réduction de la surface d’attaque en activant le mode audit pour tester la fonctionnalité directement dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6e29d-117">Learn how to evaluate attack surface reduction rules by enabling audit mode to test the feature directly in your organization.</span></span>

> [!TIP]
> <span data-ttu-id="6e29d-118">Vous pouvez également consulter le site web du scénario de démonstration microsoft Defender pour point de terminaison [sur demo.wd.microsoft.com](https://demo.wd.microsoft.com?ocid=cx-wddocs-testground) pour vérifier que la fonctionnalité fonctionne et voir comment elle fonctionne.</span><span class="sxs-lookup"><span data-stu-id="6e29d-118">You can also visit the Microsoft Defender for Endpoint demo scenario website at [demo.wd.microsoft.com](https://demo.wd.microsoft.com?ocid=cx-wddocs-testground) to confirm the feature is working and see how it works.</span></span>

## <a name="use-audit-mode-to-measure-impact"></a><span data-ttu-id="6e29d-119">Utiliser le mode audit pour mesurer l’impact</span><span class="sxs-lookup"><span data-stu-id="6e29d-119">Use audit mode to measure impact</span></span>

<span data-ttu-id="6e29d-120">Activez les règles de réduction de la surface d’attaque en mode audit pour afficher un enregistrement des applications qui auraient été bloquées si la fonctionnalité était entièrement activée.</span><span class="sxs-lookup"><span data-stu-id="6e29d-120">Enable attack surface reduction rules in audit mode to view a record of apps that would have been blocked if the feature was fully enabled.</span></span> <span data-ttu-id="6e29d-121">Testez le fonctionnement de la fonctionnalité dans votre organisation pour vous assurer qu’elle n’affecte pas vos applications métier.</span><span class="sxs-lookup"><span data-stu-id="6e29d-121">Test how the feature will work in your organization to ensure it doesn't affect your line-of-business apps.</span></span> <span data-ttu-id="6e29d-122">Vous pouvez également avoir une idée de la fréquence de tir des règles lors d’une utilisation normale.</span><span class="sxs-lookup"><span data-stu-id="6e29d-122">You can also get an idea of how often the rules will fire during normal use.</span></span>

<span data-ttu-id="6e29d-123">Pour activer une règle de réduction de la surface d’attaque en mode audit, utilisez l’cmdlet PowerShell suivante :</span><span class="sxs-lookup"><span data-stu-id="6e29d-123">To enable an attack surface reduction rule in audit mode, use the following PowerShell cmdlet:</span></span>

```PowerShell
Add-MpPreference -AttackSurfaceReductionRules_Ids <rule ID> -AttackSurfaceReductionRules_Actions AuditMode
```

<span data-ttu-id="6e29d-124">Où `<rule ID>` se trouve une valeur GUID de la règle de réduction de la surface [d’attaque](attack-surface-reduction.md#attack-surface-reduction-rules).</span><span class="sxs-lookup"><span data-stu-id="6e29d-124">Where `<rule ID>` is a [GUID value of the attack surface reduction rule](attack-surface-reduction.md#attack-surface-reduction-rules).</span></span>

<span data-ttu-id="6e29d-125">Pour activer toutes les règles de réduction de la surface d’attaque ajoutées en mode audit, utilisez l’cmdlet PowerShell suivante :</span><span class="sxs-lookup"><span data-stu-id="6e29d-125">To enable all the added attack surface reduction rules in audit mode, use the following PowerShell cmdlet:</span></span>

```PowerShell
(Get-MpPreference).AttackSurfaceReductionRules_Ids | Foreach {Add-MpPreference -AttackSurfaceReductionRules_Ids $_ -AttackSurfaceReductionRules_Actions AuditMode}
```

> [!TIP]
> <span data-ttu-id="6e29d-126">Si vous souhaitez auditer entièrement le fonctionnement des règles de réduction de la surface d’attaque dans votre organisation, vous devez utiliser un outil de gestion pour déployer ce paramètre sur les appareils de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="6e29d-126">If you want to fully audit how attack surface reduction rules will work in your organization, you'll need to use a management tool to deploy this setting to devices in your network(s).</span></span>

<span data-ttu-id="6e29d-127">Vous pouvez également utiliser une stratégie de groupe, Intune ou des fournisseurs de services de configuration (CSP) de gestion des périphériques mobiles (CSP) pour configurer et déployer le paramètre.</span><span class="sxs-lookup"><span data-stu-id="6e29d-127">You can also use Group Policy, Intune, or mobile device management (MDM) configuration service providers (CSPs) to configure and deploy the setting.</span></span> <span data-ttu-id="6e29d-128">En savoir plus dans l’article principal des règles de [réduction de la surface d’attaque.](attack-surface-reduction.md)</span><span class="sxs-lookup"><span data-stu-id="6e29d-128">Learn more in the main [Attack surface reduction rules](attack-surface-reduction.md) article.</span></span>

## <a name="review-attack-surface-reduction-events-in-windows-event-viewer"></a><span data-ttu-id="6e29d-129">Passer en revue les événements de réduction de la surface d’Windows l’Observateur d’événements</span><span class="sxs-lookup"><span data-stu-id="6e29d-129">Review attack surface reduction events in Windows Event Viewer</span></span>

<span data-ttu-id="6e29d-130">Pour passer en revue les applications qui auraient été bloquées, ouvrez l’Observateur d’événements et filtrez l’ID d’événement 1121 dans le journal microsoft-Windows-Windows Defender/opérationnel.</span><span class="sxs-lookup"><span data-stu-id="6e29d-130">To review apps that would have been blocked, open Event Viewer and filter for Event ID 1121 in the Microsoft-Windows-Windows Defender/Operational log.</span></span> <span data-ttu-id="6e29d-131">Le tableau suivant répertorie tous les événements de protection réseau.</span><span class="sxs-lookup"><span data-stu-id="6e29d-131">The following table lists all network protection events.</span></span>

<span data-ttu-id="6e29d-132">ID de l'événement</span><span class="sxs-lookup"><span data-stu-id="6e29d-132">Event ID</span></span> | <span data-ttu-id="6e29d-133">Description</span><span class="sxs-lookup"><span data-stu-id="6e29d-133">Description</span></span>
-|-
 <span data-ttu-id="6e29d-134">5007</span><span class="sxs-lookup"><span data-stu-id="6e29d-134">5007</span></span> | <span data-ttu-id="6e29d-135">Événement lorsque les paramètres sont modifiés</span><span class="sxs-lookup"><span data-stu-id="6e29d-135">Event when settings are changed</span></span>
 <span data-ttu-id="6e29d-136">1121</span><span class="sxs-lookup"><span data-stu-id="6e29d-136">1121</span></span> | <span data-ttu-id="6e29d-137">Événement lorsqu’une règle de réduction de la surface d’attaque se déclenche en mode blocage</span><span class="sxs-lookup"><span data-stu-id="6e29d-137">Event when an attack surface reduction rule fires in block mode</span></span>
 <span data-ttu-id="6e29d-138">1122</span><span class="sxs-lookup"><span data-stu-id="6e29d-138">1122</span></span> | <span data-ttu-id="6e29d-139">Événement lorsqu’une règle de réduction de la surface d’attaque se déclenche en mode audit</span><span class="sxs-lookup"><span data-stu-id="6e29d-139">Event when an attack surface reduction rule fires in audit mode</span></span>

## <a name="customize-attack-surface-reduction-rules"></a><span data-ttu-id="6e29d-140">Personnaliser les règles de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="6e29d-140">Customize attack surface reduction rules</span></span>

<span data-ttu-id="6e29d-141">Au cours de votre évaluation, vous pouvez configurer chaque règle individuellement ou exclure certains fichiers et processus de l’évaluation par la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="6e29d-141">During your evaluation, you may wish to configure each rule individually or exclude certain files and processes from being evaluated by the feature.</span></span>

<span data-ttu-id="6e29d-142">Voir [Personnaliser les règles de réduction de la surface](customize-attack-surface-reduction.md) d’attaque pour plus d’informations sur la configuration de la fonctionnalité à l’aide des outils de gestion, y compris la stratégie de groupe et les stratégies CSP mdM.</span><span class="sxs-lookup"><span data-stu-id="6e29d-142">See [Customize attack surface reduction rules](customize-attack-surface-reduction.md) for information on configuring the feature with management tools, including Group Policy and MDM CSP policies.</span></span>

## <a name="see-also"></a><span data-ttu-id="6e29d-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e29d-143">See also</span></span>

* [<span data-ttu-id="6e29d-144">Réduire les surfaces d’attaque avec des règles de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="6e29d-144">Reduce attack surfaces with attack surface reduction rules</span></span>](attack-surface-reduction.md)
* [<span data-ttu-id="6e29d-145">Utiliser le mode audit pour évaluer les Windows Defender</span><span class="sxs-lookup"><span data-stu-id="6e29d-145">Use audit mode to evaluate Windows Defender</span></span>](audit-windows-defender.md)
* [<span data-ttu-id="6e29d-146">FAQ sur la réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="6e29d-146">Attack surface reduction FAQ</span></span>](attack-surface-reduction.md)
