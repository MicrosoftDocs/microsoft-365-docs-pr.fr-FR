---
title: Spécialistes des menaces Microsoft
ms.reviewer: ''
description: Les experts microsoft en matière de menaces fournissent une couche supplémentaire d’expertise à Microsoft Defender for Endpoint.
keywords: service de repérage de menace gérée, repérage de menace gérée, service de détection et réponse gérée (MDR), MTE, Experts microsoft en matière de menaces, MTE-TAN, notification d’attaque ciblée, notification d’attaque ciblée
search.product: Windows 10
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 4c61fcdfb452fb075498dcc2858bb7a9b4b81a2f
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51165944"
---
# <a name="microsoft-threat-experts"></a><span data-ttu-id="f4f0e-104">Spécialistes des menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="f4f0e-104">Microsoft Threat Experts</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="f4f0e-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="f4f0e-105">**Applies to:**</span></span>
- [<span data-ttu-id="f4f0e-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f4f0e-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2146631)
- [<span data-ttu-id="f4f0e-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="f4f0e-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="f4f0e-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="f4f0e-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="f4f0e-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="f4f0e-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)


<span data-ttu-id="f4f0e-110">Microsoft Threat Experts est un service de recherche de menace géré qui fournit à vos centres d’opérations de sécurité (SOC) une analyse et une surveillance de niveau expert pour les aider à s’assurer que les menaces critiques dans vos environnements uniques ne sont pas manquées.</span><span class="sxs-lookup"><span data-stu-id="f4f0e-110">Microsoft Threat Experts is a managed threat hunting service that provides your Security Operation Centers (SOCs) with expert level monitoring and analysis to help them ensure that critical threats in your unique environments don’t get missed.</span></span>
  
<span data-ttu-id="f4f0e-111">Ce service de recherche de menace gérée fournit des informations et des données pilotées par des experts par le biais de ces deux fonctionnalités : la notification d’attaque ciblée et l’accès aux experts à la demande.</span><span class="sxs-lookup"><span data-stu-id="f4f0e-111">This managed threat hunting service provides expert-driven insights and data through these two capabilities: targeted attack notification and access to experts on demand.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="f4f0e-112">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="f4f0e-112">Before you begin</span></span> 
> [!NOTE]
> <span data-ttu-id="f4f0e-113">Discutez des conditions d’éligibilité avec votre fournisseur de services techniques Microsoft et votre équipe de compte avant de vous appliquer au service de recherche de menaces gérées.</span><span class="sxs-lookup"><span data-stu-id="f4f0e-113">Discuss the eligibility requirements with your Microsoft Technical Service provider and account team before you apply to the managed threat hunting service.</span></span>

<span data-ttu-id="f4f0e-114">Si vous êtes un client Microsoft Defender pour points de terminaison, vous devez demander des experts microsoft en matière de **menaces - Notifications** d’attaque ciblées pour obtenir des informations et une analyse spéciales qui vous aident à identifier les menaces les plus critiques dans votre environnement afin de pouvoir y répondre rapidement.</span><span class="sxs-lookup"><span data-stu-id="f4f0e-114">If you're a Microsoft Defender for Endpoint customer, you need to apply for **Microsoft Threat Experts - Targeted Attack Notifications** to get special insights and analysis that help identify the most critical threats in your environment so you can respond to them quickly</span></span>

<span data-ttu-id="f4f0e-115">Pour vous inscrire à Microsoft Threat Experts - Avantages des notifications d’attaques **ciblées,** voir Paramètres généraux Avancés fonctionnalités  >    >    >  **Microsoft Threat Experts - Notifications** d’attaque ciblée à appliquer.</span><span class="sxs-lookup"><span data-stu-id="f4f0e-115">To enroll to Microsoft Threat Experts - Targeted Attack Notifications benefits, go to **Settings** > **General** > **Advanced features** > **Microsoft Threat Experts - Targeted Attack Notifications** to apply.</span></span> <span data-ttu-id="f4f0e-116">Une fois accepté, vous bénéficiez des avantages des notifications d’attaque ciblée.</span><span class="sxs-lookup"><span data-stu-id="f4f0e-116">Once accepted, you will get the benefits of Targeted Attack Notifications.</span></span>

<span data-ttu-id="f4f0e-117">Contactez votre équipe de compte ou votre représentant Microsoft pour vous abonner à **Microsoft Threat Experts - Experts** à la demande pour consulter nos experts en matière de menaces sur les détections et les adversaires pertinents auxquels votre organisation est confrontée.</span><span class="sxs-lookup"><span data-stu-id="f4f0e-117">Contact your account team or Microsoft representative to subscribe to **Microsoft Threat Experts - Experts on Demand** to consult with our threat experts on relevant detections and adversaries that your organization is facing.</span></span>

<span data-ttu-id="f4f0e-118">Pour plus [d’informations, voir](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/configure-microsoft-threat-experts#before-you-begin) Configurer les fonctionnalités des experts microsoft en matière de menaces.</span><span class="sxs-lookup"><span data-stu-id="f4f0e-118">See [Configure Microsoft Threat Experts capabilities](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/configure-microsoft-threat-experts#before-you-begin) for details.</span></span> 

## <a name="microsoft-threat-experts---targeted-attack-notification"></a><span data-ttu-id="f4f0e-119">Spécialistes des menaces Microsoft - Notification d’attaque ciblée</span><span class="sxs-lookup"><span data-stu-id="f4f0e-119">Microsoft Threat Experts - Targeted attack notification</span></span> 
<span data-ttu-id="f4f0e-120">Experts microsoft en matière de menaces : la notification d’attaque ciblée permet de cibler de manière proactive les menaces les plus importantes pour votre réseau, notamment les intrusions de l’adversaire humain, les attaques par clavier ou les attaques avancées telles que le cyber-espionnage.</span><span class="sxs-lookup"><span data-stu-id="f4f0e-120">Microsoft Threat Experts - Targeted attack notification provides proactive hunting for the most important threats to your network, including human adversary intrusions, hands-on-keyboard attacks, or advanced attacks like cyber-espionage.</span></span> <span data-ttu-id="f4f0e-121">Ces notifications s’affiche sous la forme d’une nouvelle alerte.</span><span class="sxs-lookup"><span data-stu-id="f4f0e-121">These notifications shows up as a new alert.</span></span> <span data-ttu-id="f4f0e-122">Le service de recherche géré inclut :</span><span class="sxs-lookup"><span data-stu-id="f4f0e-122">The managed hunting service includes:</span></span>  
- <span data-ttu-id="f4f0e-123">Analyse et analyse des menaces, ce qui réduit le temps d’activité et les risques pour l’entreprise</span><span class="sxs-lookup"><span data-stu-id="f4f0e-123">Threat monitoring and analysis, reducing dwell time and risk to the business</span></span> 
- <span data-ttu-id="f4f0e-124">Intelligence artificielle entraînée pour découvrir et hiérarchiser les attaques connues et inconnues</span><span class="sxs-lookup"><span data-stu-id="f4f0e-124">Hunter-trained artificial intelligence to discover and prioritize both known and unknown attacks</span></span>  
- <span data-ttu-id="f4f0e-125">Identification des risques les plus importants, aider les SOC à optimiser le temps et l’énergie</span><span class="sxs-lookup"><span data-stu-id="f4f0e-125">Identifying the most important risks, helping SOCs maximize time and energy</span></span> 
- <span data-ttu-id="f4f0e-126">Étendue de compromission et autant de contexte qu’il est possible de fournir rapidement pour permettre une réponse SOC rapide.</span><span class="sxs-lookup"><span data-stu-id="f4f0e-126">Scope of compromise and as much context as can be quickly delivered to enable fast SOC response.</span></span> 
 
## <a name="microsoft-threat-experts---experts-on-demand"></a><span data-ttu-id="f4f0e-127">Experts microsoft en matière de menaces : experts à la demande</span><span class="sxs-lookup"><span data-stu-id="f4f0e-127">Microsoft Threat Experts - Experts on Demand</span></span>
<span data-ttu-id="f4f0e-128">Les clients peuvent faire appel à nos experts en matière de sécurité directement à partir du Centre de sécurité Microsoft Defender pour obtenir une réponse précise et opportune.</span><span class="sxs-lookup"><span data-stu-id="f4f0e-128">Customers can engage our security experts directly from within Microsoft Defender Security Center for timely and accurate response.</span></span> <span data-ttu-id="f4f0e-129">Les experts fournissent des informations nécessaires pour mieux comprendre les menaces complexes qui affectent votre organisation, depuis les demandes d’alerte, les appareils potentiellement compromis, la cause première d’une connexion réseau suspecte, jusqu’à des informations supplémentaires sur les menaces concernant les campagnes avancées de menaces persistantes en cours.</span><span class="sxs-lookup"><span data-stu-id="f4f0e-129">Experts provide insights needed to better understand the complex threats affecting your organization, from alert inquiries, potentially compromised devices, root cause of a suspicious network connection, to additional threat intelligence regarding ongoing advanced persistent threat campaigns.</span></span> <span data-ttu-id="f4f0e-130">Avec cette fonctionnalité, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="f4f0e-130">With this capability, you can:</span></span>
- <span data-ttu-id="f4f0e-131">Obtenir une clarification supplémentaire sur les alertes, y compris la cause racine ou l’étendue de l’incident</span><span class="sxs-lookup"><span data-stu-id="f4f0e-131">Get additional clarification on alerts including root cause or scope of the incident</span></span> 
- <span data-ttu-id="f4f0e-132">Clarifier le comportement suspect de l’appareil et les étapes suivantes en cas d’attaque avancée</span><span class="sxs-lookup"><span data-stu-id="f4f0e-132">Gain clarity into suspicious device behavior and next steps if faced with an advanced attacker</span></span>  
- <span data-ttu-id="f4f0e-133">Déterminer les risques et la protection concernant les acteurs des menaces, les campagnes ou les techniques malveillantes émergentes</span><span class="sxs-lookup"><span data-stu-id="f4f0e-133">Determine risk and protection regarding threat actors, campaigns, or emerging attacker techniques</span></span> 

<span data-ttu-id="f4f0e-134">L’option de **consulter un expert en** menaces est disponible à plusieurs endroits dans le portail afin que vous pouvez interagir avec des experts dans le cadre de votre enquête :</span><span class="sxs-lookup"><span data-stu-id="f4f0e-134">The option to **Consult a threat expert** is available in several places in the portal so you can engage with experts in the context of your investigation:</span></span>

- <span data-ttu-id="f4f0e-135"><i>**Menu Aide et support**</i></span><span class="sxs-lookup"><span data-stu-id="f4f0e-135"><i>**Help and support menu**</i></span></span><BR>
<span data-ttu-id="f4f0e-136">![Capture d’écran de l’option de menu MTE-EOD](images/mte-eod-menu.png)</span><span class="sxs-lookup"><span data-stu-id="f4f0e-136">![Screenshot of MTE-EOD menu option](images/mte-eod-menu.png)</span></span>

- <span data-ttu-id="f4f0e-137"><i>**Menu Actions de page d’appareil**</i></span><span class="sxs-lookup"><span data-stu-id="f4f0e-137"><i>**Device page actions menu**</i></span></span><BR>
<span data-ttu-id="f4f0e-138">![Capture d’écran de l’option de menu Action de page d’appareil MTE-EOD](images/mte-eod-machines.png)</span><span class="sxs-lookup"><span data-stu-id="f4f0e-138">![Screenshot of MTE-EOD device page action menu option](images/mte-eod-machines.png)</span></span>

- <span data-ttu-id="f4f0e-139"><i>**Menu Actions de la page Alertes**</i></span><span class="sxs-lookup"><span data-stu-id="f4f0e-139"><i>**Alerts page actions menu**</i></span></span><BR>
<span data-ttu-id="f4f0e-140">![Capture d’écran de l’option de menu Action de la page d’alerte MTE-EOD](images/mte-eod-alerts.png)</span><span class="sxs-lookup"><span data-stu-id="f4f0e-140">![Screenshot of MTE-EOD alert page action menu option](images/mte-eod-alerts.png)</span></span>

- <span data-ttu-id="f4f0e-141"><i>**Menu Actions de la page de fichiers**</i></span><span class="sxs-lookup"><span data-stu-id="f4f0e-141"><i>**File page actions menu**</i></span></span><BR>
<span data-ttu-id="f4f0e-142">![Capture d’écran de l’option de menu Action de la page de fichiers MTE-EOD](images/mte-eod-file.png)</span><span class="sxs-lookup"><span data-stu-id="f4f0e-142">![Screenshot of MTE-EOD file page action menu option](images/mte-eod-file.png)</span></span>

> [!NOTE]
> <span data-ttu-id="f4f0e-143">Si vous souhaitez suivre l’état de vos cas d’experts à la demande via le Microsoft Services Hub, faites-en le suivi.</span><span class="sxs-lookup"><span data-stu-id="f4f0e-143">If you would like to track the status of your Experts on Demand cases through Microsoft Services Hub, reach out to your Technical Account Manager.</span></span> 

<span data-ttu-id="f4f0e-144">Regardez cette vidéo pour obtenir une vue d’ensemble rapide du Microsoft Services Hub.</span><span class="sxs-lookup"><span data-stu-id="f4f0e-144">Watch this video for a quick overview of the Microsoft Services Hub.</span></span>

>[!VIDEO https://www.microsoft.com/videoplayer/embed/RE4pk9f] 

   
## <a name="related-topic"></a><span data-ttu-id="f4f0e-145">Rubrique connexe</span><span class="sxs-lookup"><span data-stu-id="f4f0e-145">Related topic</span></span>
- [<span data-ttu-id="f4f0e-146">Configurer les fonctionnalités des experts microsoft en matière de menaces</span><span class="sxs-lookup"><span data-stu-id="f4f0e-146">Configure Microsoft Threat Experts capabilities</span></span>](configure-microsoft-threat-experts.md)
