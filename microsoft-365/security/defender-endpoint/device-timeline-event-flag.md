---
title: Indicateurs d’événement de chronologie d’appareil Microsoft Defender pour point de terminaison
description: Utiliser microsoft Defender pour les indicateurs d’événement de chronologie d’appareil de point de terminaison pour
keywords: Chronologie de l’appareil defender pour le point de terminaison, indicateurs d’événement
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: dansimp
author: dansimp
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: a34efc171d3bb3aa1fcf33e0f56700149885ac2e
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51165152"
---
# <a name="microsoft-defender-for-endpoint-device-timeline-event-flags"></a><span data-ttu-id="55562-104">Indicateurs d’événement de chronologie d’appareil Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="55562-104">Microsoft Defender for Endpoint device timeline event flags</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="55562-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="55562-105">**Applies to:**</span></span>
- [<span data-ttu-id="55562-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="55562-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="55562-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="55562-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="55562-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="55562-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="55562-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="55562-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-assignaccess-abovefoldlink)

<span data-ttu-id="55562-110">Les indicateurs d’événements dans la chronologie de l’appareil Defender for Endpoint vous aident à filtrer et à organiser des événements spécifiques lorsque vous examinez des attaques potentielles.</span><span class="sxs-lookup"><span data-stu-id="55562-110">Event flags in the Defender for Endpoint device timeline help you filter and organize specific events when you're  investigate potential attacks.</span></span>

<span data-ttu-id="55562-111">La chronologie de l’appareil Defender pour point de terminaison fournit une vue chronologique des événements et des alertes associées observés sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="55562-111">The Defender for Endpoint device timeline provides a chronological view of the events and associated alerts observed on a device.</span></span> <span data-ttu-id="55562-112">Cette liste d’événements offre une visibilité totale sur les événements, fichiers et adresses IP observés sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="55562-112">This list of events provides full visibility into any events, files, and IP addresses observed on the device.</span></span> <span data-ttu-id="55562-113">La liste peut parfois être longue.</span><span class="sxs-lookup"><span data-stu-id="55562-113">The list can sometimes be lengthy.</span></span> <span data-ttu-id="55562-114">Les indicateurs d’événement de chronologie de l’appareil vous aident à suivre les événements qui peuvent être liés.</span><span class="sxs-lookup"><span data-stu-id="55562-114">Device timeline event flags help you track events that could be related.</span></span> 

<span data-ttu-id="55562-115">Une fois la chronologie de l’appareil passée, vous pouvez trier, filtrer et exporter les événements spécifiques que vous avez signalés.</span><span class="sxs-lookup"><span data-stu-id="55562-115">After you've gone through a device timeline, you can sort, filter, and export the specific events that you flagged.</span></span>

<span data-ttu-id="55562-116">Lors de la navigation dans la chronologie de l’appareil, vous pouvez rechercher et filtrer des événements spécifiques.</span><span class="sxs-lookup"><span data-stu-id="55562-116">While navigating the device timeline, you can search and filter for specific events.</span></span> <span data-ttu-id="55562-117">Vous pouvez définir des indicateurs d’événement en :</span><span class="sxs-lookup"><span data-stu-id="55562-117">You can set event flags by:</span></span> 

- <span data-ttu-id="55562-118">Mise en surbrillance des événements les plus importants</span><span class="sxs-lookup"><span data-stu-id="55562-118">Highlighting the most important events</span></span> 
- <span data-ttu-id="55562-119">Marquage d’événements nécessitant une profondeur</span><span class="sxs-lookup"><span data-stu-id="55562-119">Marking events that requires deep dive</span></span> 
- <span data-ttu-id="55562-120">Création d’une nouvelle chronologie des violations</span><span class="sxs-lookup"><span data-stu-id="55562-120">Building a clean breach timeline</span></span>



## <a name="flag-an-event"></a><span data-ttu-id="55562-121">Indicateur d’un événement</span><span class="sxs-lookup"><span data-stu-id="55562-121">Flag an event</span></span>
1. <span data-ttu-id="55562-122">Rechercher l’événement que vous souhaitez indicateur</span><span class="sxs-lookup"><span data-stu-id="55562-122">Find the event that you want to flag</span></span>
2. <span data-ttu-id="55562-123">Cliquez sur l’icône d’indicateur dans la colonne Indicateur.</span><span class="sxs-lookup"><span data-stu-id="55562-123">Click the flag icon in the Flag column.</span></span> 
<span data-ttu-id="55562-124">![Image de l’indicateur de chronologie de l’appareil](images/device-flags.png)</span><span class="sxs-lookup"><span data-stu-id="55562-124">![Image of device timeline flag](images/device-flags.png)</span></span>

## <a name="view-flagged-events"></a><span data-ttu-id="55562-125">Afficher les événements marqués</span><span class="sxs-lookup"><span data-stu-id="55562-125">View flagged events</span></span>  
1. <span data-ttu-id="55562-126">Dans la section **Filtres de** chronologie, activez **les événements marqués.**</span><span class="sxs-lookup"><span data-stu-id="55562-126">In the timeline **Filters** section, enable **Flagged events**.</span></span>
2. <span data-ttu-id="55562-127">Cliquez sur **Appliquer**.</span><span class="sxs-lookup"><span data-stu-id="55562-127">Click **Apply**.</span></span> <span data-ttu-id="55562-128">Seuls les événements marqués sont affichés.</span><span class="sxs-lookup"><span data-stu-id="55562-128">Only flagged events are displayed.</span></span>
<span data-ttu-id="55562-129">Vous pouvez appliquer des filtres supplémentaires en cliquant sur la barre d’heure.</span><span class="sxs-lookup"><span data-stu-id="55562-129">You can apply additional filters by clicking on the time bar.</span></span> <span data-ttu-id="55562-130">Cela affiche uniquement les événements antérieurs à l’événement marqué.</span><span class="sxs-lookup"><span data-stu-id="55562-130">This will only show events prior to the flagged event.</span></span>  
<span data-ttu-id="55562-131">![Image de l’indicateur de chronologie de l’appareil avec le filtre sur](images/device-flag-filter.png)</span><span class="sxs-lookup"><span data-stu-id="55562-131">![Image of device timeline flag with filter on](images/device-flag-filter.png)</span></span>
