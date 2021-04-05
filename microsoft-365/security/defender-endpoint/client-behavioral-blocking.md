---
title: Blocage comportemental du client
description: Le blocage du comportement client fait partie des fonctionnalités de blocage et de blocage du comportement dans Microsoft Defender pour point de terminaison
keywords: blocage comportemental, protection rapide, comportement du client, Microsoft Defender ATP
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
ms.openlocfilehash: 9fcff96b2583c6ef6bec05429ec50a71f3872e43
ms.sourcegitcommit: 987f70e44e406ab6b1dd35f336a9d0c228032794
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/05/2021
ms.locfileid: "51587106"
---
# <a name="client-behavioral-blocking"></a><span data-ttu-id="c9811-104">Blocage comportemental du client</span><span class="sxs-lookup"><span data-stu-id="c9811-104">Client behavioral blocking</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="c9811-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="c9811-105">**Applies to:**</span></span>
- [<span data-ttu-id="c9811-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="c9811-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="c9811-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="c9811-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="c9811-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="c9811-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="c9811-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="c9811-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-assignaccess-abovefoldlink)

## <a name="overview"></a><span data-ttu-id="c9811-110">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="c9811-110">Overview</span></span>

<span data-ttu-id="c9811-111">Le blocage du comportement client est un composant [des](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/behavioral-blocking-containment) fonctionnalités de blocage et de blocage du comportement dans Defender pour point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="c9811-111">Client behavioral blocking is a component of [behavioral blocking and containment capabilities](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/behavioral-blocking-containment) in Defender for Endpoint.</span></span> <span data-ttu-id="c9811-112">Lorsque des comportements suspects sont détectés sur des appareils (également appelés clients ou points de terminaison), les artefacts (tels que les fichiers ou applications) sont bloqués, vérifiés et corrigés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="c9811-112">As suspicious behaviors are detected on devices (also referred to as clients or endpoints), artifacts (such as files or applications) are blocked, checked, and remediated automatically.</span></span> 

:::image type="content" source="images/pre-execution-and-post-execution-detection-engines.png" alt-text="Protection du cloud et du client":::

<span data-ttu-id="c9811-114">La protection antivirus fonctionne mieux lorsqu’elle est couplée à la protection cloud.</span><span class="sxs-lookup"><span data-stu-id="c9811-114">Antivirus protection works best when paired with cloud protection.</span></span>

## <a name="how-client-behavioral-blocking-works"></a><span data-ttu-id="c9811-115">Fonctionnement du blocage du comportement client</span><span class="sxs-lookup"><span data-stu-id="c9811-115">How client behavioral blocking works</span></span>

<span data-ttu-id="c9811-116">[L’Antivirus Microsoft Defender](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/microsoft-defender-antivirus-in-windows-10) peut détecter des comportements suspects, du code malveillant, des attaques sans fichier et en mémoire, et bien plus encore sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="c9811-116">[Microsoft Defender Antivirus](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/microsoft-defender-antivirus-in-windows-10) can detect suspicious behavior, malicious code, fileless and in-memory attacks, and more on a device.</span></span> <span data-ttu-id="c9811-117">Lorsque des comportements suspects sont détectés, l’Antivirus Microsoft Defender surveille et envoie ces comportements suspects et leurs arbre de processus au service de protection cloud.</span><span class="sxs-lookup"><span data-stu-id="c9811-117">When suspicious behaviors are detected, Microsoft Defender Antivirus monitors and sends those suspicious behaviors and their process trees to the cloud protection service.</span></span> <span data-ttu-id="c9811-118">L’apprentissage automatique différencie les applications malveillantes et les comportements de qualité en millisecondes et classifie chaque artefact.</span><span class="sxs-lookup"><span data-stu-id="c9811-118">Machine learning differentiates between malicious applications and good behaviors within milliseconds, and classifies each artifact.</span></span> <span data-ttu-id="c9811-119">En temps quasi réel, dès qu’un artefact est trouvé malveillant, il est bloqué sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c9811-119">In almost real time, as soon as an artifact is found to be malicious, it's blocked on the device.</span></span> 

<span data-ttu-id="c9811-120">Chaque fois qu’un comportement suspect est détecté, [une](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/alerts-queue) alerte est générée et visible dans le Centre de sécurité Microsoft Defender ( [https://securitycenter.windows.com](https://securitycenter.windows.com) ).</span><span class="sxs-lookup"><span data-stu-id="c9811-120">Whenever a suspicious behavior is detected, an [alert](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/alerts-queue) is generated, and is visible in the Microsoft Defender Security Center ([https://securitycenter.windows.com](https://securitycenter.windows.com)).</span></span>

<span data-ttu-id="c9811-121">Le blocage du comportement client est efficace, car il permet non seulement d’empêcher le démarrage d’une attaque, mais également d’arrêter une attaque qui a commencé à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="c9811-121">Client behavioral blocking is effective because it not only helps prevent an attack from starting, it can help stop an attack that has begun executing.</span></span> <span data-ttu-id="c9811-122">En outre, avec [le blocage de boucle de](feedback-loop-blocking.md) commentaires (autre fonctionnalité de blocage et de blocage du comportement), les attaques sont empêchées sur d’autres appareils de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c9811-122">And, with [feedback-loop blocking](feedback-loop-blocking.md) (another capability of behavioral blocking and containment), attacks are prevented on other devices in your organization.</span></span>

## <a name="behavior-based-detections"></a><span data-ttu-id="c9811-123">Détections basées sur le comportement</span><span class="sxs-lookup"><span data-stu-id="c9811-123">Behavior-based detections</span></span>

<span data-ttu-id="c9811-124">Les détections basées sur le comportement sont nommées en fonction de la matrice CK&[MITRE ATT pour Entreprise.](https://attack.mitre.org/matrices/enterprise)</span><span class="sxs-lookup"><span data-stu-id="c9811-124">Behavior-based detections are named according to the [MITRE ATT&CK Matrix for Enterprise](https://attack.mitre.org/matrices/enterprise).</span></span> <span data-ttu-id="c9811-125">La convention d’attribution de noms permet d’identifier la phase d’attaque où le comportement malveillant a été observé :</span><span class="sxs-lookup"><span data-stu-id="c9811-125">The naming convention helps identify the attack stage where the malicious behavior was observed:</span></span>


|<span data-ttu-id="c9811-126">Tactique</span><span class="sxs-lookup"><span data-stu-id="c9811-126">Tactic</span></span> |   <span data-ttu-id="c9811-127">Nom de la menace de détection</span><span class="sxs-lookup"><span data-stu-id="c9811-127">Detection threat name</span></span> |
|----|----|
|<span data-ttu-id="c9811-128">Accès initial</span><span class="sxs-lookup"><span data-stu-id="c9811-128">Initial Access</span></span> | <span data-ttu-id="c9811-129">Behavior:Win32/InitialAccess.\*!ml</span><span class="sxs-lookup"><span data-stu-id="c9811-129">Behavior:Win32/InitialAccess.\*!ml</span></span> |
|<span data-ttu-id="c9811-130">Exécution</span><span class="sxs-lookup"><span data-stu-id="c9811-130">Execution</span></span>  | <span data-ttu-id="c9811-131">Behavior:Win32/Execution.\*!ml</span><span class="sxs-lookup"><span data-stu-id="c9811-131">Behavior:Win32/Execution.\*!ml</span></span> |
|<span data-ttu-id="c9811-132">Persistance</span><span class="sxs-lookup"><span data-stu-id="c9811-132">Persistence</span></span>    | <span data-ttu-id="c9811-133">Behavior:Win32/Persistence.\*!ml</span><span class="sxs-lookup"><span data-stu-id="c9811-133">Behavior:Win32/Persistence.\*!ml</span></span> |
|<span data-ttu-id="c9811-134">Escalade de privilèges</span><span class="sxs-lookup"><span data-stu-id="c9811-134">Privilege Escalation</span></span>   | <span data-ttu-id="c9811-135">Behavior:Win32/PrivilegeEscalation.\*!ml</span><span class="sxs-lookup"><span data-stu-id="c9811-135">Behavior:Win32/PrivilegeEscalation.\*!ml</span></span> |
|<span data-ttu-id="c9811-136">Défense</span><span class="sxs-lookup"><span data-stu-id="c9811-136">Defense Evasion</span></span>    | <span data-ttu-id="c9811-137">Behavior:Win32/DefenseEvasion.\*!ml</span><span class="sxs-lookup"><span data-stu-id="c9811-137">Behavior:Win32/DefenseEvasion.\*!ml</span></span> |
|<span data-ttu-id="c9811-138">Accès aux informations d’identification</span><span class="sxs-lookup"><span data-stu-id="c9811-138">Credential Access</span></span>  | <span data-ttu-id="c9811-139">Behavior:Win32/CredentialAccess.\*!ml</span><span class="sxs-lookup"><span data-stu-id="c9811-139">Behavior:Win32/CredentialAccess.\*!ml</span></span> |
|<span data-ttu-id="c9811-140">Découverte</span><span class="sxs-lookup"><span data-stu-id="c9811-140">Discovery</span></span>  | <span data-ttu-id="c9811-141">Behavior:Win32/Discovery.\*!ml</span><span class="sxs-lookup"><span data-stu-id="c9811-141">Behavior:Win32/Discovery.\*!ml</span></span> |
|<span data-ttu-id="c9811-142">Mouvement latéral</span><span class="sxs-lookup"><span data-stu-id="c9811-142">Lateral Movement</span></span> | <span data-ttu-id="c9811-143">Behavior:Win32/LateralMovement.\*!ml</span><span class="sxs-lookup"><span data-stu-id="c9811-143">Behavior:Win32/LateralMovement.\*!ml</span></span> |
|<span data-ttu-id="c9811-144">Collection</span><span class="sxs-lookup"><span data-stu-id="c9811-144">Collection</span></span> |   <span data-ttu-id="c9811-145">Behavior:Win32/Collection.\*!ml</span><span class="sxs-lookup"><span data-stu-id="c9811-145">Behavior:Win32/Collection.\*!ml</span></span> |
|<span data-ttu-id="c9811-146">Commande et contrôle</span><span class="sxs-lookup"><span data-stu-id="c9811-146">Command and Control</span></span> | <span data-ttu-id="c9811-147">Behavior:Win32/CommandAndControl.\*!ml</span><span class="sxs-lookup"><span data-stu-id="c9811-147">Behavior:Win32/CommandAndControl.\*!ml</span></span> |
|<span data-ttu-id="c9811-148">Exfiltration</span><span class="sxs-lookup"><span data-stu-id="c9811-148">Exfiltration</span></span>   | <span data-ttu-id="c9811-149">Behavior:Win32/Exfiltration.\*!ml</span><span class="sxs-lookup"><span data-stu-id="c9811-149">Behavior:Win32/Exfiltration.\*!ml</span></span> |
|<span data-ttu-id="c9811-150">Impact</span><span class="sxs-lookup"><span data-stu-id="c9811-150">Impact</span></span> | <span data-ttu-id="c9811-151">Behavior:Win32/Impact.\*!ml</span><span class="sxs-lookup"><span data-stu-id="c9811-151">Behavior:Win32/Impact.\*!ml</span></span> |
|<span data-ttu-id="c9811-152">Non catégorisé</span><span class="sxs-lookup"><span data-stu-id="c9811-152">Uncategorized</span></span>  | <span data-ttu-id="c9811-153">Behavior:Win32/Generic.\*!ml</span><span class="sxs-lookup"><span data-stu-id="c9811-153">Behavior:Win32/Generic.\*!ml</span></span> |

> [!TIP]
> <span data-ttu-id="c9811-154">Pour en savoir plus sur les menaces spécifiques, consultez **[l’activité récente des menaces globales.](https://www.microsoft.com/wdsi/threats)**</span><span class="sxs-lookup"><span data-stu-id="c9811-154">To learn more about specific threats, see **[recent global threat activity](https://www.microsoft.com/wdsi/threats)**.</span></span>


## <a name="configuring-client-behavioral-blocking"></a><span data-ttu-id="c9811-155">Configuration du blocage du comportement client</span><span class="sxs-lookup"><span data-stu-id="c9811-155">Configuring client behavioral blocking</span></span>

<span data-ttu-id="c9811-156">Si votre organisation utilise Defender pour endpoint, le blocage du comportement client est activé par défaut.</span><span class="sxs-lookup"><span data-stu-id="c9811-156">If your organization is using Defender for Endpoint, client behavioral blocking is enabled by default.</span></span> <span data-ttu-id="c9811-157">Toutefois, pour bénéficier de toutes les fonctionnalités de Defender pour point de terminaison, y compris le blocage du comportement et le [contenu,](behavioral-blocking-containment.md)assurez-vous que les fonctionnalités et fonctionnalités suivantes de Defender pour point de terminaison sont activées et configurées :</span><span class="sxs-lookup"><span data-stu-id="c9811-157">However, to benefit from all Defender for Endpoint capabilities, including [behavioral blocking and containment](behavioral-blocking-containment.md), make sure the following features and capabilities of Defender for Endpoint are enabled and configured:</span></span>

- [<span data-ttu-id="c9811-158">Lignes de base de Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="c9811-158">Defender for Endpoint baselines</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/configure-machines-security-baseline)

- [<span data-ttu-id="c9811-159">Appareils intégrés à Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="c9811-159">Devices onboarded to Defender for Endpoint</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/onboard-configure)

- [<span data-ttu-id="c9811-160">PEPT en mode blocage</span><span class="sxs-lookup"><span data-stu-id="c9811-160">EDR in block mode</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/edr-in-block-mode)

- [<span data-ttu-id="c9811-161">Réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="c9811-161">Attack surface reduction</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/attack-surface-reduction)

- <span data-ttu-id="c9811-162">[Protection nouvelle génération](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/configure-microsoft-defender-antivirus-features) (antivirus)</span><span class="sxs-lookup"><span data-stu-id="c9811-162">[Next-generation protection](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/configure-microsoft-defender-antivirus-features) (antivirus)</span></span>

## <a name="related-articles"></a><span data-ttu-id="c9811-163">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="c9811-163">Related articles</span></span>

- [<span data-ttu-id="c9811-164">Blocage et confinement comportementaux</span><span class="sxs-lookup"><span data-stu-id="c9811-164">Behavioral blocking and containment</span></span>](behavioral-blocking-containment.md)

- [<span data-ttu-id="c9811-165">Blocage de la boucle de commentaires</span><span class="sxs-lookup"><span data-stu-id="c9811-165">Feedback-loop blocking</span></span>](feedback-loop-blocking.md)

- [<span data-ttu-id="c9811-166">(Blog) Blocage et contenu comportementaux : transformation de l’optique en protection</span><span class="sxs-lookup"><span data-stu-id="c9811-166">(Blog) Behavioral blocking and containment: Transforming optics into protection</span></span>](https://www.microsoft.com/security/blog/2020/03/09/behavioral-blocking-and-containment-transforming-optics-into-protection/)

- [<span data-ttu-id="c9811-167">Helpful Defender pour les ressources de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="c9811-167">Helpful Defender for Endpoint resources</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/helpful-resources)
