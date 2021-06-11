---
title: Blocage comportemental du client
description: Le blocage du comportement client fait partie des fonctionnalités de blocage et de blocage du comportement dans Microsoft Defender pour point de terminaison
keywords: blocage comportemental, protection rapide, comportement du client, Microsoft Defender pour point de terminaison
search.product: eADQiWindows 10XVcnh
ms.pagetype: security
author: denisebmsft
ms.author: deniseb
manager: dansimp
ms.reviewer: shwetaj
audience: ITPro
ms.topic: article
ms.prod: m365-security
localization_priority: Normal
ms.custom:
- next-gen
- edr
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.technology: mde
ms.openlocfilehash: 4e416aa9484f251280649035247a59dcc82ce750
ms.sourcegitcommit: bce733c1152dfbca782e716579074261e3c2ef65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/07/2021
ms.locfileid: "52795957"
---
# <a name="client-behavioral-blocking"></a><span data-ttu-id="85c9b-104">Blocage comportemental du client</span><span class="sxs-lookup"><span data-stu-id="85c9b-104">Client behavioral blocking</span></span>

<span data-ttu-id="85c9b-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="85c9b-105">**Applies to:**</span></span>
- [<span data-ttu-id="85c9b-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="85c9b-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="85c9b-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="85c9b-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="85c9b-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="85c9b-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="85c9b-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="85c9b-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-assignaccess-abovefoldlink)

## <a name="overview"></a><span data-ttu-id="85c9b-110">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="85c9b-110">Overview</span></span>

<span data-ttu-id="85c9b-111">Le blocage du comportement client est un composant [des](behavioral-blocking-containment.md) fonctionnalités de blocage et de blocage du comportement dans Defender pour point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="85c9b-111">Client behavioral blocking is a component of [behavioral blocking and containment capabilities](behavioral-blocking-containment.md) in Defender for Endpoint.</span></span> <span data-ttu-id="85c9b-112">Lorsque des comportements suspects sont détectés sur des appareils (également appelés clients ou points de terminaison), les artefacts (tels que les fichiers ou applications) sont bloqués, vérifiés et corrigés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="85c9b-112">As suspicious behaviors are detected on devices (also referred to as clients or endpoints), artifacts (such as files or applications) are blocked, checked, and remediated automatically.</span></span> 

:::image type="content" source="images/pre-execution-and-post-execution-detection-engines.png" alt-text="Protection du cloud et du client":::

<span data-ttu-id="85c9b-114">La protection antivirus fonctionne mieux lorsqu’elle est couplée à la protection cloud.</span><span class="sxs-lookup"><span data-stu-id="85c9b-114">Antivirus protection works best when paired with cloud protection.</span></span>

## <a name="how-client-behavioral-blocking-works"></a><span data-ttu-id="85c9b-115">Fonctionnement du blocage du comportement client</span><span class="sxs-lookup"><span data-stu-id="85c9b-115">How client behavioral blocking works</span></span>

<span data-ttu-id="85c9b-116">[Antivirus Microsoft Defender](microsoft-defender-antivirus-in-windows-10.md) détecter des comportements suspects, du code malveillant, des attaques sans fichier et en mémoire, et bien plus encore sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="85c9b-116">[Microsoft Defender Antivirus](microsoft-defender-antivirus-in-windows-10.md) can detect suspicious behavior, malicious code, fileless and in-memory attacks, and more on a device.</span></span> <span data-ttu-id="85c9b-117">Lorsque des comportements suspects sont détectés, Antivirus Microsoft Defender surveille et envoie ces comportements suspects et leurs arbre de processus au service de protection cloud.</span><span class="sxs-lookup"><span data-stu-id="85c9b-117">When suspicious behaviors are detected, Microsoft Defender Antivirus monitors and sends those suspicious behaviors and their process trees to the cloud protection service.</span></span> <span data-ttu-id="85c9b-118">L’apprentissage automatique différencie les applications malveillantes et les comportements de qualité en millisecondes et classifie chaque artefact.</span><span class="sxs-lookup"><span data-stu-id="85c9b-118">Machine learning differentiates between malicious applications and good behaviors within milliseconds, and classifies each artifact.</span></span> <span data-ttu-id="85c9b-119">En temps quasi réel, dès qu’un artefact est trouvé malveillant, il est bloqué sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="85c9b-119">In almost real time, as soon as an artifact is found to be malicious, it's blocked on the device.</span></span> 

<span data-ttu-id="85c9b-120">Chaque fois qu’un comportement suspect est détecté, [une](alerts-queue.md) alerte est générée et visible dans le Centre de sécurité Microsoft Defender ( [https://securitycenter.windows.com](https://securitycenter.windows.com) ).</span><span class="sxs-lookup"><span data-stu-id="85c9b-120">Whenever a suspicious behavior is detected, an [alert](alerts-queue.md) is generated, and is visible in the Microsoft Defender Security Center ([https://securitycenter.windows.com](https://securitycenter.windows.com)).</span></span>

<span data-ttu-id="85c9b-121">Le blocage du comportement client est efficace, car il permet non seulement d’empêcher le démarrage d’une attaque, mais également d’arrêter une attaque qui a commencé à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="85c9b-121">Client behavioral blocking is effective because it not only helps prevent an attack from starting, it can help stop an attack that has begun executing.</span></span> <span data-ttu-id="85c9b-122">En outre, avec [le blocage de boucle de](feedback-loop-blocking.md) commentaires (autre fonctionnalité de blocage et de blocage du comportement), les attaques sont empêchées sur d’autres appareils de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="85c9b-122">And, with [feedback-loop blocking](feedback-loop-blocking.md) (another capability of behavioral blocking and containment), attacks are prevented on other devices in your organization.</span></span>

## <a name="behavior-based-detections"></a><span data-ttu-id="85c9b-123">Détections basées sur le comportement</span><span class="sxs-lookup"><span data-stu-id="85c9b-123">Behavior-based detections</span></span>

<span data-ttu-id="85c9b-124">Les détections basées sur le comportement sont nommées en fonction de la matrice [MITRE ATT&CK pour Enterprise](https://attack.mitre.org/matrices/enterprise).</span><span class="sxs-lookup"><span data-stu-id="85c9b-124">Behavior-based detections are named according to the [MITRE ATT&CK Matrix for Enterprise](https://attack.mitre.org/matrices/enterprise).</span></span> <span data-ttu-id="85c9b-125">La convention d’attribution de noms permet d’identifier la phase d’attaque où le comportement malveillant a été observé :</span><span class="sxs-lookup"><span data-stu-id="85c9b-125">The naming convention helps identify the attack stage where the malicious behavior was observed:</span></span>


|<span data-ttu-id="85c9b-126">Tactique</span><span class="sxs-lookup"><span data-stu-id="85c9b-126">Tactic</span></span> |   <span data-ttu-id="85c9b-127">Nom de la menace de détection</span><span class="sxs-lookup"><span data-stu-id="85c9b-127">Detection threat name</span></span> |
|----|----|
|<span data-ttu-id="85c9b-128">Accès initial</span><span class="sxs-lookup"><span data-stu-id="85c9b-128">Initial Access</span></span> | `Behavior:Win32/InitialAccess.*!ml` |
|<span data-ttu-id="85c9b-129">Exécution</span><span class="sxs-lookup"><span data-stu-id="85c9b-129">Execution</span></span>  | `Behavior:Win32/Execution.*!ml` |
|<span data-ttu-id="85c9b-130">Persistance</span><span class="sxs-lookup"><span data-stu-id="85c9b-130">Persistence</span></span>    | `Behavior:Win32/Persistence.*!ml` |
|<span data-ttu-id="85c9b-131">Escalade de privilèges</span><span class="sxs-lookup"><span data-stu-id="85c9b-131">Privilege Escalation</span></span>   | `Behavior:Win32/PrivilegeEscalation.*!ml` |
|<span data-ttu-id="85c9b-132">Défense</span><span class="sxs-lookup"><span data-stu-id="85c9b-132">Defense Evasion</span></span>    | `Behavior:Win32/DefenseEvasion.*!ml` |
|<span data-ttu-id="85c9b-133">Accès aux informations d’identification</span><span class="sxs-lookup"><span data-stu-id="85c9b-133">Credential Access</span></span>  | `Behavior:Win32/CredentialAccess.*!ml` |
|<span data-ttu-id="85c9b-134">Discovery</span><span class="sxs-lookup"><span data-stu-id="85c9b-134">Discovery</span></span>  | `Behavior:Win32/Discovery.*!ml` |
|<span data-ttu-id="85c9b-135">Mouvement latéral</span><span class="sxs-lookup"><span data-stu-id="85c9b-135">Lateral Movement</span></span> | `Behavior:Win32/LateralMovement.*!ml` |
|<span data-ttu-id="85c9b-136">Collection</span><span class="sxs-lookup"><span data-stu-id="85c9b-136">Collection</span></span> |   `Behavior:Win32/Collection.*!ml` |
|<span data-ttu-id="85c9b-137">Commande et contrôle</span><span class="sxs-lookup"><span data-stu-id="85c9b-137">Command and Control</span></span> | `Behavior:Win32/CommandAndControl.*!ml` |
|<span data-ttu-id="85c9b-138">Exfiltration</span><span class="sxs-lookup"><span data-stu-id="85c9b-138">Exfiltration</span></span>   | `Behavior:Win32/Exfiltration.*!ml` |
|<span data-ttu-id="85c9b-139">Impact</span><span class="sxs-lookup"><span data-stu-id="85c9b-139">Impact</span></span> | `Behavior:Win32/Impact.*!ml` |
|<span data-ttu-id="85c9b-140">Non catégorisé</span><span class="sxs-lookup"><span data-stu-id="85c9b-140">Uncategorized</span></span>  | `Behavior:Win32/Generic.*!ml` |

> [!TIP]
> <span data-ttu-id="85c9b-141">Pour en savoir plus sur les menaces spécifiques, consultez **[l’activité récente des menaces globales.](https://www.microsoft.com/wdsi/threats)**</span><span class="sxs-lookup"><span data-stu-id="85c9b-141">To learn more about specific threats, see **[recent global threat activity](https://www.microsoft.com/wdsi/threats)**.</span></span>


## <a name="configuring-client-behavioral-blocking"></a><span data-ttu-id="85c9b-142">Configuration du blocage du comportement client</span><span class="sxs-lookup"><span data-stu-id="85c9b-142">Configuring client behavioral blocking</span></span>

<span data-ttu-id="85c9b-143">Si votre organisation utilise Defender pour endpoint, le blocage du comportement client est activé par défaut.</span><span class="sxs-lookup"><span data-stu-id="85c9b-143">If your organization is using Defender for Endpoint, client behavioral blocking is enabled by default.</span></span> <span data-ttu-id="85c9b-144">Toutefois, pour bénéficier de toutes les fonctionnalités de Defender pour point de terminaison, y compris le blocage du comportement et le [contenu,](behavioral-blocking-containment.md)assurez-vous que les fonctionnalités et fonctionnalités suivantes de Defender pour point de terminaison sont activées et configurées :</span><span class="sxs-lookup"><span data-stu-id="85c9b-144">However, to benefit from all Defender for Endpoint capabilities, including [behavioral blocking and containment](behavioral-blocking-containment.md), make sure the following features and capabilities of Defender for Endpoint are enabled and configured:</span></span>

- [<span data-ttu-id="85c9b-145">Lignes de base de Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="85c9b-145">Defender for Endpoint baselines</span></span>](configure-machines-security-baseline.md)

- [<span data-ttu-id="85c9b-146">Appareils intégrés à Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="85c9b-146">Devices onboarded to Defender for Endpoint</span></span>](onboard-configure.md)

- [<span data-ttu-id="85c9b-147">PEPT en mode blocage</span><span class="sxs-lookup"><span data-stu-id="85c9b-147">EDR in block mode</span></span>](edr-in-block-mode.md)

- [<span data-ttu-id="85c9b-148">Réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="85c9b-148">Attack surface reduction</span></span>](attack-surface-reduction.md)

- <span data-ttu-id="85c9b-149">[Protection nouvelle génération](configure-microsoft-defender-antivirus-features.md) (antivirus, logiciel anti-programme malveillant et autres fonctionnalités de protection contre les menaces)</span><span class="sxs-lookup"><span data-stu-id="85c9b-149">[Next-generation protection](configure-microsoft-defender-antivirus-features.md) (antivirus, antimalware, and other threat protection capabilities)</span></span>

