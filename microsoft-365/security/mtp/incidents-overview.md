---
title: Vue d’ensemble des incidents dans Microsoft 365 Defender
description: Enquêter sur les incidents détectés entre les appareils, les utilisateurs et les boîtes aux lettres.
keywords: incidents, alertes, enquêter, corrélation, attaque, machines, appareils, utilisateurs, identités, identité, boîte de réception, e-mail, 365, microsoft, m365
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: macapara
author: mjcaparas
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: conceptual
search.appverid:
- MOE150
- MET150
ms.technology: m365d
ms.openlocfilehash: de3fba2692f5b6df7c7192c328a3911287cd7ce2
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50928723"
---
# <a name="incidents-overview-in-microsoft-365-defender"></a><span data-ttu-id="fcc86-104">Vue d’ensemble des incidents dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="fcc86-104">Incidents overview in Microsoft 365 Defender</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="fcc86-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="fcc86-105">**Applies to:**</span></span>
- <span data-ttu-id="fcc86-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="fcc86-106">Microsoft 365 Defender</span></span>

> <span data-ttu-id="fcc86-107">Vous souhaitez découvrir Microsoft 365 Defender ?</span><span class="sxs-lookup"><span data-stu-id="fcc86-107">Want to experience Microsoft 365 Defender?</span></span> <span data-ttu-id="fcc86-108">Vous pouvez [l’évaluer dans un environnement de laboratoire](./mtp-evaluation.md?ocid=cx-docs-MTPtriallab) ou exécuter votre projet pilote en [production.](./mtp-pilot.md?ocid=cx-evalpilot)</span><span class="sxs-lookup"><span data-stu-id="fcc86-108">You can [evaluate it in a lab environment](./mtp-evaluation.md?ocid=cx-docs-MTPtriallab) or [run your pilot project in production](./mtp-pilot.md?ocid=cx-evalpilot).</span></span>
>


<span data-ttu-id="fcc86-109">Les incidents sont basés sur des alertes connexes.</span><span class="sxs-lookup"><span data-stu-id="fcc86-109">Incidents are based on related alerts.</span></span> <span data-ttu-id="fcc86-110">Elles sont créées lorsqu’un événement ou une activité malveillante est détecté sur votre réseau.</span><span class="sxs-lookup"><span data-stu-id="fcc86-110">Alerts are created when a malicious event or activity is seen on your network.</span></span> <span data-ttu-id="fcc86-111">Les alertes individuelles fournissent des indices précieux sur une attaque en cours.</span><span class="sxs-lookup"><span data-stu-id="fcc86-111">Individual alerts provide valuable clues about an on-going attack.</span></span> <span data-ttu-id="fcc86-112">Toutefois, les attaques utilisent généralement différents vecteurs et techniques pour effectuer une violation.</span><span class="sxs-lookup"><span data-stu-id="fcc86-112">However, attacks typically employ various vectors and techniques to carry out a breach.</span></span> <span data-ttu-id="fcc86-113">Rassembler des indices individuels peut être difficile et chronophage.</span><span class="sxs-lookup"><span data-stu-id="fcc86-113">Piecing individual clues together can be challenging and time-consuming.</span></span>

<span data-ttu-id="fcc86-114">Cette courte vidéo donne une vue d’ensemble des incidents dans Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="fcc86-114">This short video gives an overview of incidents in Microsoft 365 Defender.</span></span>
<br>

>[!VIDEO https://www.microsoft.com/videoplayer/embed/RE4Bzwz?]

<span data-ttu-id="fcc86-115">Un incident est un ensemble d’alertes corrélées qui constitue l’histoire d’une attaque.</span><span class="sxs-lookup"><span data-stu-id="fcc86-115">An incident is a collection of correlated alerts that make up the story of an attack.</span></span> <span data-ttu-id="fcc86-116">Les événements malveillants et suspects qui se trouvent dans différentes entités d’appareil, d’utilisateur et de boîte aux lettres dans le réseau sont automatiquement regroupés par Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="fcc86-116">Malicious and suspicious events that are found in different device, user, and mailbox entities in the network are automatically aggregated by Microsoft 365 Defender.</span></span> <span data-ttu-id="fcc86-117">Le regroupement d’alertes associées dans un incident offre aux défenseurs de la sécurité une vue complète d’une attaque.</span><span class="sxs-lookup"><span data-stu-id="fcc86-117">Grouping related alerts into an incident gives security defenders a comprehensive view of an attack.</span></span> 

<span data-ttu-id="fcc86-118">Par exemple, les défenseurs de la sécurité peuvent voir où l’attaque a commencé, quelles tactiques ont été utilisées et jusqu’où l’attaque est passée dans le réseau.</span><span class="sxs-lookup"><span data-stu-id="fcc86-118">For instance, security defenders can see where the attack started, what tactics were used, and how far the attack has gone into the network.</span></span> <span data-ttu-id="fcc86-119">Ils peuvent également voir l’étendue de l’attaque, telle que le nombre d’appareils, d’utilisateurs et de boîtes aux lettres concernés, la portée de l’impact et d’autres détails sur les entités affectées.</span><span class="sxs-lookup"><span data-stu-id="fcc86-119">They can also see the scope of the attack, like how many devices, users, and mailboxes were impacted, how severe the impact was, and other details about affected entities.</span></span>

<span data-ttu-id="fcc86-120">S’il est activé, Microsoft 365 Defender peut automatiquement examiner et résoudre les alertes individuelles par le biais de l’automatisation et de l’intelligence artificielle.</span><span class="sxs-lookup"><span data-stu-id="fcc86-120">If enabled, Microsoft 365 Defender can automatically investigate and resolve the individual alerts through automation and artificial intelligence.</span></span> <span data-ttu-id="fcc86-121">Les défenseurs de la sécurité peuvent également effectuer des étapes de correction supplémentaires pour résoudre l’attaque directement à partir de l’affichage Incidents.</span><span class="sxs-lookup"><span data-stu-id="fcc86-121">Security defenders can also perform additional remediation steps to resolve the attack straight from the incidents view.</span></span> 

<span data-ttu-id="fcc86-122">Les incidents des 30 derniers jours sont affichés dans la file d’attente des incidents.</span><span class="sxs-lookup"><span data-stu-id="fcc86-122">Incidents from the last 30 days are shown in the incident queue.</span></span> <span data-ttu-id="fcc86-123">À partir de là, les défenseurs de la sécurité peuvent voir quels incidents doivent être hiérarchisés en fonction du niveau de risque et d’autres facteurs.</span><span class="sxs-lookup"><span data-stu-id="fcc86-123">From here, security defenders can see which incidents should be prioritized based on risk level and other factors.</span></span> 

<span data-ttu-id="fcc86-124">Les défenseurs de la sécurité peuvent également renommer les incidents, les affecter à des analystes individuels, classer et ajouter des balises aux incidents pour une expérience de gestion des incidents meilleure et plus personnalisée.</span><span class="sxs-lookup"><span data-stu-id="fcc86-124">Security defenders can also rename incidents, assign them to individual analysts, classify, and add tags to incidents for a better and more customized incident management experience.</span></span>



## <a name="see-also"></a><span data-ttu-id="fcc86-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fcc86-125">See also</span></span>
- [<span data-ttu-id="fcc86-126">Hiérarchiser les incidents</span><span class="sxs-lookup"><span data-stu-id="fcc86-126">Prioritize incidents</span></span>](incident-queue.md)
- [<span data-ttu-id="fcc86-127">Enquêter sur des incidents</span><span class="sxs-lookup"><span data-stu-id="fcc86-127">Investigate incidents</span></span>](investigate-incidents.md)
- [<span data-ttu-id="fcc86-128">Gérer les incidents</span><span class="sxs-lookup"><span data-stu-id="fcc86-128">Manage incidents</span></span>](manage-incidents.md)