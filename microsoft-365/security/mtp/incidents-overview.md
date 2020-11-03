---
title: Présentation des incidents dans Microsoft 365 Defender
description: Enquêter sur les incidents détectés entre les appareils, les utilisateurs et les boîtes aux lettres.
keywords: incidents, alertes, enquêter, corrélation, attaque, machines, appareils, utilisateurs, identités, identité, boîte de réception, e-mail, 365, microsoft, m365
search.product: eADQiWindows 10XVcnh
ms.prod: microsoft-365-enterprise
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
ms.openlocfilehash: e5ac3e9a02c333d3168c328aa6ad5532c48af99e
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48846687"
---
# <a name="incidents-overview-in-microsoft-365-defender"></a><span data-ttu-id="b244a-104">Présentation des incidents dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b244a-104">Incidents overview in Microsoft 365 Defender</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="b244a-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="b244a-105">**Applies to:**</span></span>
- <span data-ttu-id="b244a-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b244a-106">Microsoft 365 Defender</span></span>



<span data-ttu-id="b244a-107">Les incidents sont basés sur les alertes associées.</span><span class="sxs-lookup"><span data-stu-id="b244a-107">Incidents are based on related alerts.</span></span> <span data-ttu-id="b244a-108">Elles sont créées lorsqu’un événement ou une activité malveillante est détecté sur votre réseau.</span><span class="sxs-lookup"><span data-stu-id="b244a-108">Alerts are created when a malicious event or activity is seen on your network.</span></span> <span data-ttu-id="b244a-109">Les alertes individuelles fournissent des indices précieux sur une attaque en cours.</span><span class="sxs-lookup"><span data-stu-id="b244a-109">Individual alerts provide valuable clues about an on-going attack.</span></span> <span data-ttu-id="b244a-110">Toutefois, les attaques utilisent généralement plusieurs vecteurs et techniques pour effectuer une violation.</span><span class="sxs-lookup"><span data-stu-id="b244a-110">However, attacks typically employ various vectors and techniques to carry out a breach.</span></span> <span data-ttu-id="b244a-111">Piecing les indices individuels peuvent être difficiles et longs.</span><span class="sxs-lookup"><span data-stu-id="b244a-111">Piecing individual clues together can be challenging and time-consuming.</span></span>

<span data-ttu-id="b244a-112">Cette courte vidéo donne une vue d’ensemble des incidents dans Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="b244a-112">This short video gives an overview of incidents in Microsoft 365 Defender.</span></span>
<br>

>[!VIDEO https://www.microsoft.com/videoplayer/embed/RE4Bzwz?]

<span data-ttu-id="b244a-113">Un incident est une collection d’alertes corrélées qui composent l’article d’une attaque.</span><span class="sxs-lookup"><span data-stu-id="b244a-113">An incident is a collection of correlated alerts that make up the story of an attack.</span></span> <span data-ttu-id="b244a-114">Les événements malveillants et suspects détectés dans différentes entités d’appareil, d’utilisateur et de boîte aux lettres dans le réseau sont automatiquement regroupés par Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="b244a-114">Malicious and suspicious events that are found in different device, user, and mailbox entities in the network are automatically aggregated by Microsoft 365 Defender.</span></span> <span data-ttu-id="b244a-115">En regroupant les alertes associées en un incident, les défenseurs de sécurité ont une vue complète d’une attaque.</span><span class="sxs-lookup"><span data-stu-id="b244a-115">Grouping related alerts into an incident gives security defenders a comprehensive view of an attack.</span></span> 

<span data-ttu-id="b244a-116">Par exemple, les défenseurs de sécurité peuvent identifier l’endroit où l’attaque a commencé, les tactiques utilisées et la durée de l’attaque sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="b244a-116">For instance, security defenders can see where the attack started, what tactics were used, and how far the attack has gone into the network.</span></span> <span data-ttu-id="b244a-117">Ils peuvent également voir l’étendue de l’attaque, comme le nombre d’appareils, d’utilisateurs et de boîtes aux lettres ayant été affectés, la gravité de l’impact et d’autres détails sur les entités affectées.</span><span class="sxs-lookup"><span data-stu-id="b244a-117">They can also see the scope of the attack, like how many devices, users, and mailboxes were impacted, how severe the impact was, and other details about affected entities.</span></span>

<span data-ttu-id="b244a-118">Si ce n’est pas le cas, Microsoft 365 Defender peut rechercher et résoudre automatiquement les alertes individuelles par le biais de l’intelligence artificielle et de l’intelligence.</span><span class="sxs-lookup"><span data-stu-id="b244a-118">If enabled, Microsoft 365 Defender can automatically investigate and resolve the individual alerts through automation and artificial intelligence.</span></span> <span data-ttu-id="b244a-119">Les défenseurs de sécurité peuvent également exécuter des étapes de correction supplémentaires pour résoudre l’attaque, directement à partir de la vue incidents.</span><span class="sxs-lookup"><span data-stu-id="b244a-119">Security defenders can also perform additional remediation steps to resolve the attack straight from the incidents view.</span></span> 

<span data-ttu-id="b244a-120">Les incidents des 30 derniers jours sont affichés dans la file d’attente des incidents.</span><span class="sxs-lookup"><span data-stu-id="b244a-120">Incidents from the last 30 days are shown in the incident queue.</span></span> <span data-ttu-id="b244a-121">À partir de là, les défenseurs de sécurité peuvent voir quels incidents doivent être classés par ordre de priorité en fonction du niveau de risque et d’autres facteurs.</span><span class="sxs-lookup"><span data-stu-id="b244a-121">From here, security defenders can see which incidents should be prioritized based on risk level and other factors.</span></span> 

<span data-ttu-id="b244a-122">Les défenseurs de sécurité peuvent également renommer les incidents, les affecter à des analystes individuels, classer et ajouter des balises aux incidents pour une expérience de gestion des incidents plus personnalisée et plus personnalisée.</span><span class="sxs-lookup"><span data-stu-id="b244a-122">Security defenders can also rename incidents, assign them to individual analysts, classify, and add tags to incidents for a better and more customized incident management experience.</span></span>



## <a name="see-also"></a><span data-ttu-id="b244a-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b244a-123">See also</span></span>
- [<span data-ttu-id="b244a-124">Hiérarchiser les incidents</span><span class="sxs-lookup"><span data-stu-id="b244a-124">Prioritize incidents</span></span>](incident-queue.md)
- [<span data-ttu-id="b244a-125">Enquêter sur des incidents</span><span class="sxs-lookup"><span data-stu-id="b244a-125">Investigate incidents</span></span>](investigate-incidents.md)
- [<span data-ttu-id="b244a-126">Gérer les incidents</span><span class="sxs-lookup"><span data-stu-id="b244a-126">Manage incidents</span></span>](manage-incidents.md)
