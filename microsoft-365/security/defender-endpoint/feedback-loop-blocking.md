---
title: Blocage de la boucle de commentaires
description: Le blocage de boucle de commentaires, également appelé protection rapide, fait partie des fonctionnalités de blocage du comportement et de blocage de contenu dans Microsoft Defender pour point de terminaison
keywords: blocage comportemental, protection rapide, blocage des commentaires, Microsoft Defender pour point de terminaison
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
ms.collection: ''
ms.technology: mde
ms.openlocfilehash: 7319ff5a89a20529eed7d36aa0d0b1522013abd4
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52842457"
---
# <a name="feedback-loop-blocking"></a><span data-ttu-id="ce117-104">Blocage de la boucle de commentaires</span><span class="sxs-lookup"><span data-stu-id="ce117-104">Feedback-loop blocking</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="ce117-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="ce117-105">**Applies to:**</span></span>
- [<span data-ttu-id="ce117-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="ce117-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)

## <a name="overview"></a><span data-ttu-id="ce117-107">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="ce117-107">Overview</span></span>

<span data-ttu-id="ce117-108">Le blocage de boucle de commentaires, également appelé [](/microsoft-365/security/defender-endpoint/behavioral-blocking-containment) protection rapide, est un composant des fonctionnalités de blocage du comportement et de contenu dans [Microsoft Defender pour point de terminaison.](/windows/security/threat-protection/)</span><span class="sxs-lookup"><span data-stu-id="ce117-108">Feedback-loop blocking, also referred to as rapid protection, is a component of [behavioral blocking and containment capabilities](/microsoft-365/security/defender-endpoint/behavioral-blocking-containment) in [Microsoft Defender for Endpoint](/windows/security/threat-protection/).</span></span> <span data-ttu-id="ce117-109">Avec le blocage de la boucle de commentaires, les appareils au sein de votre organisation sont mieux protégés contre les attaques.</span><span class="sxs-lookup"><span data-stu-id="ce117-109">With feedback-loop blocking, devices across your organization are better protected from attacks.</span></span> 

## <a name="how-feedback-loop-blocking-works"></a><span data-ttu-id="ce117-110">Fonctionnement du blocage de la boucle de commentaires</span><span class="sxs-lookup"><span data-stu-id="ce117-110">How feedback-loop blocking works</span></span>

<span data-ttu-id="ce117-111">Lorsqu’un comportement ou un fichier suspect est détecté, par exemple par [Antivirus Microsoft Defender](/windows/security/threat-protection/microsoft-defender-antivirus/microsoft-defender-antivirus-in-windows-10), les informations sur cet artefact sont envoyées à plusieurs classifieurs.</span><span class="sxs-lookup"><span data-stu-id="ce117-111">When a suspicious behavior or file is detected, such as by [Microsoft Defender Antivirus](/windows/security/threat-protection/microsoft-defender-antivirus/microsoft-defender-antivirus-in-windows-10), information about that artifact is sent to multiple classifiers.</span></span> <span data-ttu-id="ce117-112">Le moteur de boucle de protection rapide inspecte et met en corrélation les informations avec d’autres signaux pour déterminer s’il faut bloquer un fichier.</span><span class="sxs-lookup"><span data-stu-id="ce117-112">The rapid protection loop engine inspects and correlates the information with other signals to arrive at a decision as to whether to block a file.</span></span> <span data-ttu-id="ce117-113">La vérification et la classification des artefacts se produisent rapidement.</span><span class="sxs-lookup"><span data-stu-id="ce117-113">Checking and classifying artifacts happens quickly.</span></span> <span data-ttu-id="ce117-114">Cela entraîne un blocage rapide des programmes malveillants confirmés et entraîne la protection dans l’ensemble de l’écosystème.</span><span class="sxs-lookup"><span data-stu-id="ce117-114">It results in rapid blocking of confirmed malware, and drives protection across the entire ecosystem.</span></span> 

<span data-ttu-id="ce117-115">Grâce à une protection rapide, une attaque peut être arrêtée sur un appareil, d’autres appareils de l’organisation et des appareils d’autres organisations, à mesure qu’une attaque tente d’élargir sa position.</span><span class="sxs-lookup"><span data-stu-id="ce117-115">With rapid protection in place, an attack can be stopped on a device, other devices in the organization, and devices in other organizations, as an attack attempts to broaden its foothold.</span></span>


## <a name="configuring-feedback-loop-blocking"></a><span data-ttu-id="ce117-116">Configuration du blocage de boucle de commentaires</span><span class="sxs-lookup"><span data-stu-id="ce117-116">Configuring feedback-loop blocking</span></span>

<span data-ttu-id="ce117-117">Si votre organisation utilise Defender pour endpoint, le blocage de la boucle de commentaires est activé par défaut.</span><span class="sxs-lookup"><span data-stu-id="ce117-117">If your organization is using Defender for Endpoint, feedback-loop blocking is enabled by default.</span></span> <span data-ttu-id="ce117-118">Toutefois, une protection rapide se produit par le biais d’une combinaison des fonctionnalités de Defender for Endpoint, des fonctionnalités de protection de l’apprentissage automatique et du partage de signal entre les services de sécurité Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ce117-118">However, rapid protection occurs through a combination of Defender for Endpoint capabilities, machine learning protection features, and signal-sharing across Microsoft security services.</span></span> <span data-ttu-id="ce117-119">Assurez-vous que les fonctionnalités suivantes de Defender for Endpoint sont activées et configurées :</span><span class="sxs-lookup"><span data-stu-id="ce117-119">Make sure the following features and capabilities of Defender for Endpoint are enabled and configured:</span></span>

- [<span data-ttu-id="ce117-120">Lignes de base de Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="ce117-120">Microsoft Defender for Endpoint baselines</span></span>](/microsoft-365/security/defender-endpoint/configure-machines-security-baseline)

- [<span data-ttu-id="ce117-121">Appareils intégrés à Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="ce117-121">Devices onboarded to Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/onboard-configure)

- [<span data-ttu-id="ce117-122">PEPT en mode blocage</span><span class="sxs-lookup"><span data-stu-id="ce117-122">EDR in block mode</span></span>](/microsoft-365/security/defender-endpoint/edr-in-block-mode)

- [<span data-ttu-id="ce117-123">Réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="ce117-123">Attack surface reduction</span></span>](/microsoft-365/security/defender-endpoint/attack-surface-reduction)

- <span data-ttu-id="ce117-124">[Protection nouvelle génération](/windows/security/threat-protection/microsoft-defender-antivirus/configure-microsoft-defender-antivirus-features) (antivirus)</span><span class="sxs-lookup"><span data-stu-id="ce117-124">[Next-generation protection](/windows/security/threat-protection/microsoft-defender-antivirus/configure-microsoft-defender-antivirus-features) (antivirus)</span></span>

## <a name="related-articles"></a><span data-ttu-id="ce117-125">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="ce117-125">Related articles</span></span>

- [<span data-ttu-id="ce117-126">Blocage et confinement comportementaux</span><span class="sxs-lookup"><span data-stu-id="ce117-126">Behavioral blocking and containment</span></span>](behavioral-blocking-containment.md)

- [<span data-ttu-id="ce117-127">(Blog) Blocage et contenu comportementaux : transformation de l’optique en protection</span><span class="sxs-lookup"><span data-stu-id="ce117-127">(Blog) Behavioral blocking and containment: Transforming optics into protection</span></span>](https://www.microsoft.com/security/blog/2020/03/09/behavioral-blocking-and-containment-transforming-optics-into-protection/)

- [<span data-ttu-id="ce117-128">Ressources Utiles de Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="ce117-128">Helpful Microsoft Defender for Endpoint resources</span></span>](/microsoft-365/security/defender-endpoint/helpful-resources)
