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
ms.openlocfilehash: c58c81cd4623ec03850c167cad285e052413174c
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51933420"
---
# <a name="client-behavioral-blocking"></a><span data-ttu-id="74069-104">Blocage comportemental du client</span><span class="sxs-lookup"><span data-stu-id="74069-104">Client behavioral blocking</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="74069-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="74069-105">**Applies to:**</span></span>
- [<span data-ttu-id="74069-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="74069-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="74069-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="74069-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="74069-108">Vous souhaitez faire l'expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="74069-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="74069-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="74069-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-assignaccess-abovefoldlink)

## <a name="overview"></a><span data-ttu-id="74069-110">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="74069-110">Overview</span></span>

<span data-ttu-id="74069-111">Le blocage du comportement client est un composant des fonctionnalités de blocage du comportement et de blocage [de](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/behavioral-blocking-containment) contenu dans Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="74069-111">Client behavioral blocking is a component of [behavioral blocking and containment capabilities](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/behavioral-blocking-containment) in Defender for Endpoint.</span></span> <span data-ttu-id="74069-112">Lorsque des comportements suspects sont détectés sur des appareils (également appelés clients ou points de terminaison), les artefacts (tels que les fichiers ou applications) sont bloqués, vérifiés et corrigés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="74069-112">As suspicious behaviors are detected on devices (also referred to as clients or endpoints), artifacts (such as files or applications) are blocked, checked, and remediated automatically.</span></span> 

:::image type="content" source="images/pre-execution-and-post-execution-detection-engines.png" alt-text="Protection du cloud et du client":::

<span data-ttu-id="74069-114">La protection antivirus fonctionne mieux lorsqu'elle est couplée à la protection cloud.</span><span class="sxs-lookup"><span data-stu-id="74069-114">Antivirus protection works best when paired with cloud protection.</span></span>

## <a name="how-client-behavioral-blocking-works"></a><span data-ttu-id="74069-115">Fonctionnement du blocage du comportement client</span><span class="sxs-lookup"><span data-stu-id="74069-115">How client behavioral blocking works</span></span>

<span data-ttu-id="74069-116">[L'Antivirus Microsoft Defender](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/microsoft-defender-antivirus-in-windows-10) peut détecter des comportements suspects, du code malveillant, des attaques sans fichier et en mémoire, et bien plus encore sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="74069-116">[Microsoft Defender Antivirus](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/microsoft-defender-antivirus-in-windows-10) can detect suspicious behavior, malicious code, fileless and in-memory attacks, and more on a device.</span></span> <span data-ttu-id="74069-117">Lorsque des comportements suspects sont détectés, l'Antivirus Microsoft Defender surveille et envoie ces comportements suspects et leurs arbre de processus au service de protection cloud.</span><span class="sxs-lookup"><span data-stu-id="74069-117">When suspicious behaviors are detected, Microsoft Defender Antivirus monitors and sends those suspicious behaviors and their process trees to the cloud protection service.</span></span> <span data-ttu-id="74069-118">L'apprentissage automatique différencie les applications malveillantes et les comportements de qualité en millisecondes et classifie chaque artefact.</span><span class="sxs-lookup"><span data-stu-id="74069-118">Machine learning differentiates between malicious applications and good behaviors within milliseconds, and classifies each artifact.</span></span> <span data-ttu-id="74069-119">En temps quasi réel, dès qu'un artefact est trouvé malveillant, il est bloqué sur l'appareil.</span><span class="sxs-lookup"><span data-stu-id="74069-119">In almost real time, as soon as an artifact is found to be malicious, it's blocked on the device.</span></span> 

<span data-ttu-id="74069-120">Chaque fois qu'un comportement suspect est détecté, [une](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/alerts-queue) alerte est générée et visible dans le Centre de sécurité Microsoft Defender ( [https://securitycenter.windows.com](https://securitycenter.windows.com) ).</span><span class="sxs-lookup"><span data-stu-id="74069-120">Whenever a suspicious behavior is detected, an [alert](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/alerts-queue) is generated, and is visible in the Microsoft Defender Security Center ([https://securitycenter.windows.com](https://securitycenter.windows.com)).</span></span>

<span data-ttu-id="74069-121">Le blocage du comportement client est efficace, car il permet non seulement d'empêcher le démarrage d'une attaque, mais également d'arrêter une attaque qui a commencé à s'exécuter.</span><span class="sxs-lookup"><span data-stu-id="74069-121">Client behavioral blocking is effective because it not only helps prevent an attack from starting, it can help stop an attack that has begun executing.</span></span> <span data-ttu-id="74069-122">En outre, avec [le blocage de boucle de](feedback-loop-blocking.md) commentaires (autre fonctionnalité de blocage et de blocage du comportement), les attaques sont empêchées sur d'autres appareils de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="74069-122">And, with [feedback-loop blocking](feedback-loop-blocking.md) (another capability of behavioral blocking and containment), attacks are prevented on other devices in your organization.</span></span>

## <a name="behavior-based-detections"></a><span data-ttu-id="74069-123">Détections basées sur le comportement</span><span class="sxs-lookup"><span data-stu-id="74069-123">Behavior-based detections</span></span>

<span data-ttu-id="74069-124">Les détections basées sur le comportement sont nommées en fonction de la matrice CK&[MITRE ATT pour Entreprise.](https://attack.mitre.org/matrices/enterprise)</span><span class="sxs-lookup"><span data-stu-id="74069-124">Behavior-based detections are named according to the [MITRE ATT&CK Matrix for Enterprise](https://attack.mitre.org/matrices/enterprise).</span></span> <span data-ttu-id="74069-125">La convention d'attribution de noms permet d'identifier la phase d'attaque où le comportement malveillant a été observé :</span><span class="sxs-lookup"><span data-stu-id="74069-125">The naming convention helps identify the attack stage where the malicious behavior was observed:</span></span>


|<span data-ttu-id="74069-126">Tactique</span><span class="sxs-lookup"><span data-stu-id="74069-126">Tactic</span></span> |   <span data-ttu-id="74069-127">Nom de la menace de détection</span><span class="sxs-lookup"><span data-stu-id="74069-127">Detection threat name</span></span> |
|----|----|
|<span data-ttu-id="74069-128">Accès initial</span><span class="sxs-lookup"><span data-stu-id="74069-128">Initial Access</span></span> | <span data-ttu-id="74069-129">Behavior:Win32/InitialAccess.\*!ml</span><span class="sxs-lookup"><span data-stu-id="74069-129">Behavior:Win32/InitialAccess.\*!ml</span></span> |
|<span data-ttu-id="74069-130">Exécution</span><span class="sxs-lookup"><span data-stu-id="74069-130">Execution</span></span>  | <span data-ttu-id="74069-131">Behavior:Win32/Execution.\*!ml</span><span class="sxs-lookup"><span data-stu-id="74069-131">Behavior:Win32/Execution.\*!ml</span></span> |
|<span data-ttu-id="74069-132">Persistance</span><span class="sxs-lookup"><span data-stu-id="74069-132">Persistence</span></span>    | <span data-ttu-id="74069-133">Behavior:Win32/Persistence.\*!ml</span><span class="sxs-lookup"><span data-stu-id="74069-133">Behavior:Win32/Persistence.\*!ml</span></span> |
|<span data-ttu-id="74069-134">Escalade de privilèges</span><span class="sxs-lookup"><span data-stu-id="74069-134">Privilege Escalation</span></span>   | <span data-ttu-id="74069-135">Behavior:Win32/PrivilegeEscalation.\*!ml</span><span class="sxs-lookup"><span data-stu-id="74069-135">Behavior:Win32/PrivilegeEscalation.\*!ml</span></span> |
|<span data-ttu-id="74069-136">Défense</span><span class="sxs-lookup"><span data-stu-id="74069-136">Defense Evasion</span></span>    | <span data-ttu-id="74069-137">Behavior:Win32/DefenseEvasion.\*!ml</span><span class="sxs-lookup"><span data-stu-id="74069-137">Behavior:Win32/DefenseEvasion.\*!ml</span></span> |
|<span data-ttu-id="74069-138">Accès aux informations d’identification</span><span class="sxs-lookup"><span data-stu-id="74069-138">Credential Access</span></span>  | <span data-ttu-id="74069-139">Behavior:Win32/CredentialAccess.\*!ml</span><span class="sxs-lookup"><span data-stu-id="74069-139">Behavior:Win32/CredentialAccess.\*!ml</span></span> |
|<span data-ttu-id="74069-140">Discovery</span><span class="sxs-lookup"><span data-stu-id="74069-140">Discovery</span></span>  | <span data-ttu-id="74069-141">Behavior:Win32/Discovery.\*!ml</span><span class="sxs-lookup"><span data-stu-id="74069-141">Behavior:Win32/Discovery.\*!ml</span></span> |
|<span data-ttu-id="74069-142">Mouvement latéral</span><span class="sxs-lookup"><span data-stu-id="74069-142">Lateral Movement</span></span> | <span data-ttu-id="74069-143">Behavior:Win32/LateralMovement.\*!ml</span><span class="sxs-lookup"><span data-stu-id="74069-143">Behavior:Win32/LateralMovement.\*!ml</span></span> |
|<span data-ttu-id="74069-144">Collection</span><span class="sxs-lookup"><span data-stu-id="74069-144">Collection</span></span> |   <span data-ttu-id="74069-145">Behavior:Win32/Collection.\*!ml</span><span class="sxs-lookup"><span data-stu-id="74069-145">Behavior:Win32/Collection.\*!ml</span></span> |
|<span data-ttu-id="74069-146">Commande et contrôle</span><span class="sxs-lookup"><span data-stu-id="74069-146">Command and Control</span></span> | <span data-ttu-id="74069-147">Behavior:Win32/CommandAndControl.\*!ml</span><span class="sxs-lookup"><span data-stu-id="74069-147">Behavior:Win32/CommandAndControl.\*!ml</span></span> |
|<span data-ttu-id="74069-148">Exfiltration</span><span class="sxs-lookup"><span data-stu-id="74069-148">Exfiltration</span></span>   | <span data-ttu-id="74069-149">Behavior:Win32/Exfiltration.\*!ml</span><span class="sxs-lookup"><span data-stu-id="74069-149">Behavior:Win32/Exfiltration.\*!ml</span></span> |
|<span data-ttu-id="74069-150">Impact</span><span class="sxs-lookup"><span data-stu-id="74069-150">Impact</span></span> | <span data-ttu-id="74069-151">Behavior:Win32/Impact.\*!ml</span><span class="sxs-lookup"><span data-stu-id="74069-151">Behavior:Win32/Impact.\*!ml</span></span> |
|<span data-ttu-id="74069-152">Non catégorisé</span><span class="sxs-lookup"><span data-stu-id="74069-152">Uncategorized</span></span>  | <span data-ttu-id="74069-153">Behavior:Win32/Generic.\*!ml</span><span class="sxs-lookup"><span data-stu-id="74069-153">Behavior:Win32/Generic.\*!ml</span></span> |

> [!TIP]
> <span data-ttu-id="74069-154">Pour en savoir plus sur les menaces spécifiques, consultez **[l'activité récente des menaces globales.](https://www.microsoft.com/wdsi/threats)**</span><span class="sxs-lookup"><span data-stu-id="74069-154">To learn more about specific threats, see **[recent global threat activity](https://www.microsoft.com/wdsi/threats)**.</span></span>


## <a name="configuring-client-behavioral-blocking"></a><span data-ttu-id="74069-155">Configuration du blocage du comportement client</span><span class="sxs-lookup"><span data-stu-id="74069-155">Configuring client behavioral blocking</span></span>

<span data-ttu-id="74069-156">Si votre organisation utilise Defender pour endpoint, le blocage du comportement client est activé par défaut.</span><span class="sxs-lookup"><span data-stu-id="74069-156">If your organization is using Defender for Endpoint, client behavioral blocking is enabled by default.</span></span> <span data-ttu-id="74069-157">Toutefois, pour bénéficier de toutes les fonctionnalités de Defender pour point de terminaison, y compris le blocage du comportement et le [contenu,](behavioral-blocking-containment.md)assurez-vous que les fonctionnalités et fonctionnalités suivantes de Defender pour point de terminaison sont activées et configurées :</span><span class="sxs-lookup"><span data-stu-id="74069-157">However, to benefit from all Defender for Endpoint capabilities, including [behavioral blocking and containment](behavioral-blocking-containment.md), make sure the following features and capabilities of Defender for Endpoint are enabled and configured:</span></span>

- [<span data-ttu-id="74069-158">Lignes de base de Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="74069-158">Defender for Endpoint baselines</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/configure-machines-security-baseline)

- [<span data-ttu-id="74069-159">Appareils intégrés à Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="74069-159">Devices onboarded to Defender for Endpoint</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/onboard-configure)

- [<span data-ttu-id="74069-160">PEPT en mode blocage</span><span class="sxs-lookup"><span data-stu-id="74069-160">EDR in block mode</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/edr-in-block-mode)

- [<span data-ttu-id="74069-161">Réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="74069-161">Attack surface reduction</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/attack-surface-reduction)

- <span data-ttu-id="74069-162">[Protection nouvelle génération](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/configure-microsoft-defender-antivirus-features) (antivirus)</span><span class="sxs-lookup"><span data-stu-id="74069-162">[Next-generation protection](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-antivirus/configure-microsoft-defender-antivirus-features) (antivirus)</span></span>

## <a name="related-articles"></a><span data-ttu-id="74069-163">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="74069-163">Related articles</span></span>

- [<span data-ttu-id="74069-164">Blocage et confinement comportementaux</span><span class="sxs-lookup"><span data-stu-id="74069-164">Behavioral blocking and containment</span></span>](behavioral-blocking-containment.md)

- [<span data-ttu-id="74069-165">Blocage de la boucle de commentaires</span><span class="sxs-lookup"><span data-stu-id="74069-165">Feedback-loop blocking</span></span>](feedback-loop-blocking.md)

- [<span data-ttu-id="74069-166">(Blog) Blocage et contenu comportementaux : transformation de l'optique en protection</span><span class="sxs-lookup"><span data-stu-id="74069-166">(Blog) Behavioral blocking and containment: Transforming optics into protection</span></span>](https://www.microsoft.com/security/blog/2020/03/09/behavioral-blocking-and-containment-transforming-optics-into-protection/)

- [<span data-ttu-id="74069-167">Helpful Defender pour les ressources de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="74069-167">Helpful Defender for Endpoint resources</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/helpful-resources)
