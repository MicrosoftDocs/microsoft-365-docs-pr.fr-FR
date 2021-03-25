---
title: Examiner microsoft Defender pour les alertes de point de terminaison
description: Utilisez les options d’examen pour obtenir des détails sur les alertes qui affectent votre réseau, ce qu’elles signifient et comment les résoudre.
keywords: examiner, examen, appareils, périphérique, file d’attente des alertes, tableau de bord, adresse IP, fichier, soumettre, envois, analyse approfondie, chronologie, recherche, domaine, URL, IP
search.product: eADQiWindows 10XVcnh
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
ms.topic: article
ms.date: 04/24/2018
ms.technology: mde
ms.openlocfilehash: 8b3b864e716957c24893d2097249440b0a90f10a
ms.sourcegitcommit: 6f2288e0c863496dfd0ee38de754bd43096ab3e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51186100"
---
# <a name="investigate-alerts-in-microsoft-defender-for-endpoint"></a><span data-ttu-id="78a2b-104">Examiner les alertes dans Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="78a2b-104">Investigate alerts in Microsoft Defender for Endpoint</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="78a2b-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="78a2b-105">**Applies to:**</span></span>
- [<span data-ttu-id="78a2b-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="78a2b-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="78a2b-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="78a2b-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="78a2b-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="78a2b-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="78a2b-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="78a2b-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigatealerts-abovefoldlink) 

<span data-ttu-id="78a2b-110">Examinez les alertes qui affectent votre réseau, comprenez ce qu’elles signifient et comment les résoudre.</span><span class="sxs-lookup"><span data-stu-id="78a2b-110">Investigate alerts that are affecting your network, understand what they mean, and how to resolve them.</span></span>

<span data-ttu-id="78a2b-111">Sélectionnez une alerte dans la file d’attente des alertes pour aller à la page d’alerte.</span><span class="sxs-lookup"><span data-stu-id="78a2b-111">Select an alert from the alerts queue to go to alert page.</span></span> <span data-ttu-id="78a2b-112">Cet affichage contient le titre de l’alerte, les ressources affectées, le volet latéral détails et l’article sur l’alerte.</span><span class="sxs-lookup"><span data-stu-id="78a2b-112">This view contains the alert title, the affected assets, the details side pane, and the alert story.</span></span>

<span data-ttu-id="78a2b-113">Dans la page d’alerte, commencez votre enquête en sélectionnant les biens affectés ou l’une des entités sous l’arborescence de l’article de l’alerte.</span><span class="sxs-lookup"><span data-stu-id="78a2b-113">From the alert page, begin your investigation by selecting the affected assets or any of the entities under the alert story tree view.</span></span> <span data-ttu-id="78a2b-114">Le volet d’informations se remplit automatiquement avec d’autres informations sur ce que vous avez sélectionné.</span><span class="sxs-lookup"><span data-stu-id="78a2b-114">The details pane automatically populates with further information about what you selected.</span></span> <span data-ttu-id="78a2b-115">Pour voir le type d’informations que vous pouvez afficher ici, lisez Les alertes de [révision dans Microsoft Defender pour le point de terminaison.](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/review-alerts)</span><span class="sxs-lookup"><span data-stu-id="78a2b-115">To see what kind of information you can view here, read [Review alerts in Microsoft Defender for Endpoint](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/review-alerts).</span></span>

## <a name="investigate-using-the-alert-story"></a><span data-ttu-id="78a2b-116">Examiner l’utilisation de l’article d’alerte</span><span class="sxs-lookup"><span data-stu-id="78a2b-116">Investigate using the alert story</span></span>

<span data-ttu-id="78a2b-117">L’article d’alerte explique pourquoi l’alerte a été déclenchée, les événements connexes qui se sont produits avant et après, ainsi que d’autres entités associées.</span><span class="sxs-lookup"><span data-stu-id="78a2b-117">The alert story details why the alert was triggered, related events that happened before and after, as well as other related entities.</span></span>

<span data-ttu-id="78a2b-118">Les entités sont cliquables et chaque entité qui n’est pas une alerte peut être étendue à l’aide de l’icône développer sur le côté droit de la carte de cette entité.</span><span class="sxs-lookup"><span data-stu-id="78a2b-118">Entities are clickable and every entity that isn't an alert is expandable using the expand icon on the right side of that entity's card.</span></span> <span data-ttu-id="78a2b-119">L’entité en cours d’utilisation est indiquée par une bande bleue sur le côté gauche de la carte de cette entité, avec l’alerte dans le titre en cours de mise au point au premier abord.</span><span class="sxs-lookup"><span data-stu-id="78a2b-119">The entity in focus will be indicated by a blue stripe to the left side of that entity's card, with the alert in the title being in focus at first.</span></span>

<span data-ttu-id="78a2b-120">Développez les entités pour afficher les détails en un coup d’œil.</span><span class="sxs-lookup"><span data-stu-id="78a2b-120">Expand entities to view details at a glance.</span></span> <span data-ttu-id="78a2b-121">La sélection d’une entité basculera le contexte du volet d’informations sur cette entité et vous permettra de passer en revue d’autres informations, ainsi que de gérer cette entité.</span><span class="sxs-lookup"><span data-stu-id="78a2b-121">Selecting an entity will switch the context of the details pane to this entity, and will allow you to review further information, as well as manage that entity.</span></span> <span data-ttu-id="78a2b-122">La sélection *de...* à droite de la carte d’entité révélera toutes les actions disponibles pour cette entité.</span><span class="sxs-lookup"><span data-stu-id="78a2b-122">Selecting *...* to the right of the entity card will reveal all actions available for that entity.</span></span> <span data-ttu-id="78a2b-123">Ces mêmes actions apparaissent dans le volet d’informations lorsque cette entité est en focus.</span><span class="sxs-lookup"><span data-stu-id="78a2b-123">These same actions appear in the details pane when that entity is in focus.</span></span>

> [!NOTE]
> <span data-ttu-id="78a2b-124">La section de l’article sur l’alerte peut contenir plusieurs alertes, avec des alertes supplémentaires liées à la même arborescence d’exécution apparaissant avant ou après l’alerte que vous avez sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="78a2b-124">The alert story section may contain more than one alert, with additional alerts related to the same execution tree appearing before or after the alert you've selected.</span></span>

![Exemple d’un article d’alerte avec une alerte en focus et des cartes étendues](images/alert-story-tree.png)

## <a name="take-action-from-the-details-pane"></a><span data-ttu-id="78a2b-126">Action à partir du volet d’informations</span><span class="sxs-lookup"><span data-stu-id="78a2b-126">Take action from the details pane</span></span>

<span data-ttu-id="78a2b-127">Une fois que vous avez sélectionné une entité d’intérêt, le volet d’informations change pour afficher les informations sur le  type d’entité sélectionné, les informations historiques lorsqu’elle est disponible et propose aux contrôles d’agir sur cette entité directement à partir de la page d’alerte.</span><span class="sxs-lookup"><span data-stu-id="78a2b-127">Once you've selected an entity of interest, the details pane will change to display information about the selected entity type, historic information when it's available, and offer controls to **take action** on this entity directly from the alert page.</span></span>

<span data-ttu-id="78a2b-128">Une fois que vous avez terminé d’examiner, revenir à l’alerte que vous avez commencée, marquez l’état de l’alerte comme résolu et classez-le comme alerte **False** ou **Alerte True**. </span><span class="sxs-lookup"><span data-stu-id="78a2b-128">Once you're done investigating, go back to the alert you started with, mark the alert's status as **Resolved** and classify it as either **False alert** or **True alert**.</span></span> <span data-ttu-id="78a2b-129">La classification des alertes permet d’affiner cette fonctionnalité pour fournir plus d’alertes vraies et moins de fausses alertes.</span><span class="sxs-lookup"><span data-stu-id="78a2b-129">Classifying alerts helps tune this capability to provide more true alerts and less false alerts.</span></span>

<span data-ttu-id="78a2b-130">Si vous la classez comme une alerte réelle, vous pouvez également sélectionner une détermination, comme illustré dans l’image ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="78a2b-130">If you classify it as a true alert, you can also select a determination, as shown in the image below.</span></span>

![Extrait du volet d’informations avec une alerte résolue et la liste de détermination étendue](images/alert-details-resolved-true.png)

<span data-ttu-id="78a2b-132">Si vous rencontrez une fausse alerte avec une application métier, créez une règle de suppression pour éviter ce type d’alerte à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="78a2b-132">If you are experiencing a false alert with a line-of-business application, create a suppression rule to avoid this type of alert in the future.</span></span>

![actions et classification dans le volet d’informations avec la règle de suppression mise en évidence](images/alert-false-suppression-rule.png)

> [!TIP]
> <span data-ttu-id="78a2b-134">Si vous rencontrez des problèmes non décrits ci-dessus, utilisez le bouton pour fournir des commentaires ou 🙂 ouvrir un ticket de support.</span><span class="sxs-lookup"><span data-stu-id="78a2b-134">If you're experiencing any issues not described above, use the 🙂 button to provide feedback or open a support ticket.</span></span>


## <a name="related-topics"></a><span data-ttu-id="78a2b-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78a2b-135">Related topics</span></span>
- [<span data-ttu-id="78a2b-136">Afficher et organiser la file d’attente des alertes de Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="78a2b-136">View and organize the Microsoft Defender for Endpoint Alerts queue</span></span>](alerts-queue.md)
- [<span data-ttu-id="78a2b-137">Gérer les alertes microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="78a2b-137">Manage Microsoft Defender for Endpoint alerts</span></span>](manage-alerts.md)
- [<span data-ttu-id="78a2b-138">Examiner un fichier associé à une alerte Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="78a2b-138">Investigate a file associated with a Defender for Endpoint alert</span></span>](investigate-files.md)
- [<span data-ttu-id="78a2b-139">Examiner les appareils dans la liste Defender pour les appareils de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="78a2b-139">Investigate devices in the Defender for Endpoint Devices list</span></span>](investigate-machines.md)
- [<span data-ttu-id="78a2b-140">Examiner une adresse IP associée à une alerte Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="78a2b-140">Investigate an IP address associated with a Defender for Endpoint alert</span></span>](investigate-ip.md)
- [<span data-ttu-id="78a2b-141">Examiner un domaine associé à une alerte Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="78a2b-141">Investigate a domain associated with a Defender for Endpoint alert</span></span>](investigate-domain.md)
- [<span data-ttu-id="78a2b-142">Examiner un compte d’utilisateur dans Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="78a2b-142">Investigate a user account in Defender for Endpoint</span></span>](investigate-user.md)


