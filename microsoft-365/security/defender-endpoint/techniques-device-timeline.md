---
title: Techniques dans la chronologie de l’appareil
description: Présentation de la chronologie de l’appareil dans Microsoft Defender pour le point de terminaison
keywords: chronologie de périphérique, point de terminaison, MITRE, MITRE ATT&CK, techniques, tactiques
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: maccruz
author: schmurky
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 6b080c209292c8cac1aa64d748926734f4be964c
ms.sourcegitcommit: 6f2288e0c863496dfd0ee38de754bd43096ab3e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51185466"
---
# <a name="techniques-in-the-device-timeline"></a><span data-ttu-id="40fd3-104">Techniques dans la chronologie de l’appareil</span><span class="sxs-lookup"><span data-stu-id="40fd3-104">Techniques in the device timeline</span></span>


<span data-ttu-id="40fd3-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="40fd3-105">**Applies to:**</span></span>
- [<span data-ttu-id="40fd3-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="40fd3-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)


<span data-ttu-id="40fd3-107">Vous pouvez obtenir plus d’informations dans une enquête en analysant les événements qui se sont produit sur un appareil spécifique.</span><span class="sxs-lookup"><span data-stu-id="40fd3-107">You can gain more insight in an investigation by analyzing the events that happened on a specific device.</span></span> <span data-ttu-id="40fd3-108">Tout d’abord, sélectionnez l’appareil qui vous intéresse dans la [liste Appareils.](machines-view-overview.md)</span><span class="sxs-lookup"><span data-stu-id="40fd3-108">First, select the device of interest from the [Devices list](machines-view-overview.md).</span></span> <span data-ttu-id="40fd3-109">Dans la page Appareil,  vous pouvez sélectionner l’onglet Chronologie pour afficher tous les événements qui se sont produits sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="40fd3-109">On the device page, you can select the **Timeline** tab to view all the events that occurred on the device.</span></span>

## <a name="understand-techniques-in-the-timeline"></a><span data-ttu-id="40fd3-110">Comprendre les techniques dans la chronologie</span><span class="sxs-lookup"><span data-stu-id="40fd3-110">Understand techniques in the timeline</span></span>

>[!IMPORTANT]
><span data-ttu-id="40fd3-111">Certaines informations concernent une fonctionnalité de produit pré-publiée en prévisualisation publique, qui peut être considérablement modifiée avant sa publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="40fd3-111">Some information relates to a prereleased product feature in public preview which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="40fd3-112">Microsoft n’offre aucune garantie, explicite ou implicite, concernant les informations fournies ici.</span><span class="sxs-lookup"><span data-stu-id="40fd3-112">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

<span data-ttu-id="40fd3-113">Dans Microsoft Defender pour point de terminaison, **les techniques** sont un type de données supplémentaire dans la chronologie des événements.</span><span class="sxs-lookup"><span data-stu-id="40fd3-113">In Microsoft Defender for Endpoint, **Techniques** are an additional data type in the event timeline.</span></span> <span data-ttu-id="40fd3-114">Les techniques fournissent plus d’informations sur les activités associées à [MITRE ATT&](https://attack.mitre.org/) techniques ou sous-techniques CK.</span><span class="sxs-lookup"><span data-stu-id="40fd3-114">Techniques provide more insight on activities associated with [MITRE ATT&CK](https://attack.mitre.org/) techniques or sub-techniques.</span></span> 

<span data-ttu-id="40fd3-115">Cette fonctionnalité simplifie l’examen en aidant les analystes à comprendre les activités observées sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="40fd3-115">This feature simplifies the investigation experience by helping analysts understand the activities that were observed on a device.</span></span> <span data-ttu-id="40fd3-116">Les analystes peuvent ensuite décider d’examiner plus en détail.</span><span class="sxs-lookup"><span data-stu-id="40fd3-116">Analysts can then decide to investigate further.</span></span>

<span data-ttu-id="40fd3-117">Pour la prévisualisation publique, les techniques sont disponibles par défaut et affichées avec les événements lorsque la chronologie d’un appareil est affichée.</span><span class="sxs-lookup"><span data-stu-id="40fd3-117">For public preview, Techniques are available by default and shown together with events when a device's timeline is viewed.</span></span> 

![Techniques dans la capture d’écran de la chronologie de l’appareil](images/device-timeline-2.png)

<span data-ttu-id="40fd3-119">Les techniques sont mises en évidence en gras et apparaissent avec une icône bleue à gauche.</span><span class="sxs-lookup"><span data-stu-id="40fd3-119">Techniques are highlighted in bold text and appear with a blue icon on the left.</span></span> <span data-ttu-id="40fd3-120">L’ID MITRE ATT&et le nom de technique CK correspondants apparaissent également en tant que balises sous Informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="40fd3-120">The corresponding MITRE ATT&CK ID and technique name also appear as tags under Additional information.</span></span> 

<span data-ttu-id="40fd3-121">Les options de recherche et d’exportation sont également disponibles pour les techniques.</span><span class="sxs-lookup"><span data-stu-id="40fd3-121">Search and Export options are also available for Techniques.</span></span>

## <a name="investigate-using-the-side-pane"></a><span data-ttu-id="40fd3-122">Examiner l’utilisation du volet latéral</span><span class="sxs-lookup"><span data-stu-id="40fd3-122">Investigate using the side pane</span></span>

<span data-ttu-id="40fd3-123">Sélectionnez une technique pour ouvrir son volet latéral correspondant.</span><span class="sxs-lookup"><span data-stu-id="40fd3-123">Select a Technique to open its corresponding side pane.</span></span> <span data-ttu-id="40fd3-124">Vous y verrez des informations et des informations supplémentaires, telles que des techniques, des tactiques et des descriptions att&CK associées.</span><span class="sxs-lookup"><span data-stu-id="40fd3-124">Here you can see additional information and insights like related ATT&CK techniques, tactics, and descriptions.</span></span> 

<span data-ttu-id="40fd3-125">Sélectionnez la *technique d’attaque* spécifique pour ouvrir la page de technique att&CK associée dans laquelle vous trouverez plus d’informations à ce sujet.</span><span class="sxs-lookup"><span data-stu-id="40fd3-125">Select the specific *Attack technique* to open the related ATT&CK technique page where you can find more information about it.</span></span>

<span data-ttu-id="40fd3-126">Vous pouvez copier les détails d’une entité lorsque vous voyez une icône bleue à droite.</span><span class="sxs-lookup"><span data-stu-id="40fd3-126">You can copy an entity's details when you see a blue icon on the right.</span></span> <span data-ttu-id="40fd3-127">Par exemple, pour copier le sha1 d’un fichier associé, sélectionnez l’icône de page bleue.</span><span class="sxs-lookup"><span data-stu-id="40fd3-127">For instance, to copy a related file's SHA1, select the blue page icon.</span></span>

![Copier les détails de l’entité](images/techniques-side-pane-clickable.png)

<span data-ttu-id="40fd3-129">Vous pouvez faire de même pour les lignes de commande.</span><span class="sxs-lookup"><span data-stu-id="40fd3-129">You can do the same for command lines.</span></span>

![Copier la ligne de commande](images/techniques-side-pane-command.png)


## <a name="investigate-related-events"></a><span data-ttu-id="40fd3-131">Examiner les événements connexes</span><span class="sxs-lookup"><span data-stu-id="40fd3-131">Investigate related events</span></span>

<span data-ttu-id="40fd3-132">Pour utiliser la [recherche avancée pour](advanced-hunting-overview.md) rechercher des événements liés à la technique sélectionnée, sélectionnez Rechercher les **événements connexes.**</span><span class="sxs-lookup"><span data-stu-id="40fd3-132">To use [advanced hunting](advanced-hunting-overview.md) to find events related to the selected Technique, select **Hunt for related events**.</span></span> <span data-ttu-id="40fd3-133">Cela conduit à la page de recherche avancée avec une requête pour rechercher les événements liés à la technique.</span><span class="sxs-lookup"><span data-stu-id="40fd3-133">This leads to the advanced hunting page with a query to find events related to the Technique.</span></span>

![Recherche des événements connexes](images/techniques-hunt-for-related-events.png)

>[!NOTE]
><span data-ttu-id="40fd3-135">L’interrogation à  l’aide du bouton Recherche d’événements connexes à partir d’un volet latéral Technique affiche tous les événements liés à la technique identifiée, mais n’inclut pas la technique elle-même dans les résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="40fd3-135">Querying using the **Hunt for related events** button from a Technique side pane displays all the events related to the identified technique but does not include the Technique itself in the query results.</span></span>


## <a name="customize-your-device-timeline"></a><span data-ttu-id="40fd3-136">Personnaliser la chronologie de votre appareil</span><span class="sxs-lookup"><span data-stu-id="40fd3-136">Customize your device timeline</span></span>

<span data-ttu-id="40fd3-137">Dans la partie supérieure droite de la chronologie de l’appareil, vous pouvez choisir une plage de dates pour limiter le nombre d’événements et de techniques dans la chronologie.</span><span class="sxs-lookup"><span data-stu-id="40fd3-137">On the upper right-hand side of the device timeline, you can choose a date range to limit the number of events and techniques in the timeline.</span></span> 

<span data-ttu-id="40fd3-138">Vous pouvez personnaliser les colonnes à exposer.</span><span class="sxs-lookup"><span data-stu-id="40fd3-138">You can customize which columns to expose.</span></span> <span data-ttu-id="40fd3-139">Vous pouvez également filtrer les événements marqués par type de données ou par groupe d’événements.</span><span class="sxs-lookup"><span data-stu-id="40fd3-139">You can also filter for flagged events by data type or by event group.</span></span>

### <a name="choose-columns-to-expose"></a><span data-ttu-id="40fd3-140">Choisir les colonnes à exposer</span><span class="sxs-lookup"><span data-stu-id="40fd3-140">Choose columns to expose</span></span>
<span data-ttu-id="40fd3-141">Vous pouvez choisir les colonnes à exposer dans la chronologie en sélectionnant le bouton Choisir **les colonnes.**</span><span class="sxs-lookup"><span data-stu-id="40fd3-141">You can choose which columns to expose in the timeline by selecting the **Choose columns** button.</span></span>

![Personnaliser les colonnes](images/filter-customize-columns.png)

<span data-ttu-id="40fd3-143">À partir de là, vous pouvez sélectionner l’ensemble d’informations à inclure.</span><span class="sxs-lookup"><span data-stu-id="40fd3-143">From there you can select which information set to include.</span></span>

### <a name="filter-to-view-techniques-or-events-only"></a><span data-ttu-id="40fd3-144">Filtre pour afficher les techniques ou les événements uniquement</span><span class="sxs-lookup"><span data-stu-id="40fd3-144">Filter to view techniques or events only</span></span>

<span data-ttu-id="40fd3-145">Pour afficher uniquement les événements ou les techniques, sélectionnez **Filtres** dans la chronologie de l’appareil et choisissez votre type de données préféré à afficher.</span><span class="sxs-lookup"><span data-stu-id="40fd3-145">To view only either events or techniques, select **Filters** from the device timeline and choose your preferred Data type to view.</span></span>

![Capture d’écran des filtres](images/device-timeline-filters.png)



## <a name="see-also"></a><span data-ttu-id="40fd3-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40fd3-147">See also</span></span>
- [<span data-ttu-id="40fd3-148">Afficher et organiser la liste des appareils</span><span class="sxs-lookup"><span data-stu-id="40fd3-148">View and organize the Devices list</span></span>](machines-view-overview.md)
- [<span data-ttu-id="40fd3-149">Indicateurs d’événement de chronologie d’appareil Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="40fd3-149">Microsoft Defender for Endpoint device timeline event flags</span></span>](device-timeline-event-flag.md) 


 
