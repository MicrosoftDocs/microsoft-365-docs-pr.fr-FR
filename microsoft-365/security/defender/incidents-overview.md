---
title: Incidents dans Microsoft 365 Defender
description: Enquêter sur les incidents détectés entre les appareils, les utilisateurs et les boîtes aux lettres.
keywords: incidents, alertes, enquêter, corrélation, attaque, machines, appareils, utilisateurs, identités, identité, boîte de réception, e-mail, 365, microsoft, m365
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
localization_priority: Normal
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
ms.openlocfilehash: e1e028f7b58df07eccf945b3a79012b4ea12366d
ms.sourcegitcommit: 22505ce322f68a2d0ce70d71caf3b0a657fa838a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2021
ms.locfileid: "51861622"
---
# <a name="incidents-in-microsoft-365-defender"></a><span data-ttu-id="9dc6b-104">Incidents dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="9dc6b-104">Incidents in Microsoft 365 Defender</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="9dc6b-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="9dc6b-105">**Applies to:**</span></span>
- <span data-ttu-id="9dc6b-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="9dc6b-106">Microsoft 365 Defender</span></span>

> <span data-ttu-id="9dc6b-107">Vous voulez essayer Microsoft 365 Defender ?</span><span class="sxs-lookup"><span data-stu-id="9dc6b-107">Want to experience Microsoft 365 Defender?</span></span> <span data-ttu-id="9dc6b-108">Vous pouvez [l’évaluer dans un environnement de laboratoire](m365d-evaluation.md?ocid=cx-docs-MTPtriallab) ou [exécuter votre projet pilote en production](m365d-pilot.md?ocid=cx-evalpilot).</span><span class="sxs-lookup"><span data-stu-id="9dc6b-108">You can [evaluate it in a lab environment](m365d-evaluation.md?ocid=cx-docs-MTPtriallab) or [run your pilot project in production](m365d-pilot.md?ocid=cx-evalpilot).</span></span>
>

<span data-ttu-id="9dc6b-109">Un incident dans Microsoft 365 Defender est une collection d'alertes corrélées et de données associées qui constitue l'histoire d'une attaque.</span><span class="sxs-lookup"><span data-stu-id="9dc6b-109">An incident in Microsoft 365 Defender is a collection of correlated alerts and associated data that make up the story of an attack.</span></span> 

<span data-ttu-id="9dc6b-110">Les applications et services Microsoft 365 créent des alertes lorsqu'ils détectent un événement ou une activité suspect ou malveillant.</span><span class="sxs-lookup"><span data-stu-id="9dc6b-110">Microsoft 365 services and apps create alerts when they detect a suspicious or malicious event or activity.</span></span> <span data-ttu-id="9dc6b-111">Les alertes individuelles fournissent des indices précieux sur une attaque terminée ou en cours.</span><span class="sxs-lookup"><span data-stu-id="9dc6b-111">Individual alerts provide valuable clues about a completed or ongoing attack.</span></span> <span data-ttu-id="9dc6b-112">Toutefois, les attaques utilisent généralement différentes techniques pour différents types d'entités, telles que les appareils, les utilisateurs et les boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="9dc6b-112">However, attacks typically employ various techniques against different types of entities, such as devices, users, and mailboxes.</span></span> <span data-ttu-id="9dc6b-113">Le résultat est plusieurs alertes pour plusieurs entités dans votre client.</span><span class="sxs-lookup"><span data-stu-id="9dc6b-113">The result is multiple alerts for multiple entities in your tenant.</span></span> 

<span data-ttu-id="9dc6b-114">Étant donné que l'agrégation des alertes individuelles pour obtenir des informations sur une attaque peut être difficile et chronophage, Microsoft 365 Defender regroupe automatiquement les alertes et leurs informations associées dans un incident.</span><span class="sxs-lookup"><span data-stu-id="9dc6b-114">Because piecing the individual alerts together to gain insight into an attack can be challenging and time-consuming, Microsoft 365 Defender automatically aggregates the alerts and their associated information into an incident.</span></span>

:::image type="content" source="../../media/incidents-overview/incidents.png" alt-text="Comment Microsoft 365 Defender met en corrélation les événements des entités avec un incident":::

<span data-ttu-id="9dc6b-116">Regardez cette courte présentation des incidents dans Microsoft 365 Defender (4 minutes).</span><span class="sxs-lookup"><span data-stu-id="9dc6b-116">Watch this short overview of incidents in Microsoft 365 Defender (4 minutes).</span></span>

<br>

>[!VIDEO https://www.microsoft.com/videoplayer/embed/RE4Bzwz?]

<span data-ttu-id="9dc6b-117">Le regroupement d'alertes associées dans un incident vous offre une vue complète d'une attaque.</span><span class="sxs-lookup"><span data-stu-id="9dc6b-117">Grouping related alerts into an incident gives you a comprehensive view of an attack.</span></span> <span data-ttu-id="9dc6b-118">Par exemple, vous pouvez voir :</span><span class="sxs-lookup"><span data-stu-id="9dc6b-118">For example, you can see:</span></span>

- <span data-ttu-id="9dc6b-119">L'endroit où l'attaque a commencé.</span><span class="sxs-lookup"><span data-stu-id="9dc6b-119">Where the attack started.</span></span>
- <span data-ttu-id="9dc6b-120">Quelles tactiques ont été utilisées .</span><span class="sxs-lookup"><span data-stu-id="9dc6b-120">What tactics were used.</span></span>
- <span data-ttu-id="9dc6b-121">Jusqu'où l'attaque est passée dans votre client.</span><span class="sxs-lookup"><span data-stu-id="9dc6b-121">How far the attack has gone into your tenant.</span></span>
- <span data-ttu-id="9dc6b-122">Étendue de l'attaque, telle que le nombre d'appareils, d'utilisateurs et de boîtes aux lettres touchés.</span><span class="sxs-lookup"><span data-stu-id="9dc6b-122">The scope of the attack, such as how many devices, users, and mailboxes were impacted.</span></span> 
- <span data-ttu-id="9dc6b-123">Toutes les données associées à l'attaque.</span><span class="sxs-lookup"><span data-stu-id="9dc6b-123">All of the data associated with the attack.</span></span>

<span data-ttu-id="9dc6b-124">[S'il est](m365d-enable.md)activé, Microsoft 365 Defender peut automatiquement examiner et résoudre les alertes par le biais de l'automatisation et de l'intelligence artificielle.</span><span class="sxs-lookup"><span data-stu-id="9dc6b-124">If [enabled](m365d-enable.md), Microsoft 365 Defender can automatically investigate and resolve alerts through automation and artificial intelligence.</span></span> <span data-ttu-id="9dc6b-125">Vous pouvez également effectuer des étapes de correction supplémentaires pour résoudre l'attaque.</span><span class="sxs-lookup"><span data-stu-id="9dc6b-125">You can also perform additional remediation steps to resolve the attack.</span></span> 

## <a name="incidents-and-alerts-in-the-microsoft-365-security-center"></a><span data-ttu-id="9dc6b-126">Incidents et alertes dans le Centre de sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="9dc6b-126">Incidents and alerts in the Microsoft 365 security center</span></span>

<span data-ttu-id="9dc6b-127">Vous gérez les incidents à partir **d'incidents & alertes** > Incidents dans le lancement rapide du Centre de sécurité Microsoft 365 ([security.microsoft.com](https://security.microsoft.com)).</span><span class="sxs-lookup"><span data-stu-id="9dc6b-127">You manage incidents from **Incidents & alerts > Incidents** on the quick launch of the Microsoft 365 security center ([security.microsoft.com](https://security.microsoft.com)).</span></span> <span data-ttu-id="9dc6b-128">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="9dc6b-128">Here's an example.</span></span>

:::image type="content" source="../../media/incidents-queue/incidents-ss-incidents.png" alt-text="Page Incidents dans le Centre de sécurité Microsoft 365":::

<span data-ttu-id="9dc6b-130">La sélection d'un nom d'incident affiche un résumé de l'incident et donne accès aux onglets avec des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="9dc6b-130">Selecting an incident name displays a summary of the incident and provides access to tabs with additional information.</span></span>

:::image type="content" source="../../media/incidents-overview/incidents-ss-incident-summary.png" alt-text="Exemple de page Résumé d'un incident dans le Centre de sécurité Microsoft 365":::

<span data-ttu-id="9dc6b-132">Les onglets supplémentaires pour un incident sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="9dc6b-132">The additional tabs for an incident are:</span></span>

- <span data-ttu-id="9dc6b-133">Alertes</span><span class="sxs-lookup"><span data-stu-id="9dc6b-133">Alerts</span></span> 

  <span data-ttu-id="9dc6b-134">Toutes les alertes liées à l'incident et leurs informations.</span><span class="sxs-lookup"><span data-stu-id="9dc6b-134">All the alerts related to the incident and their information.</span></span>

- <span data-ttu-id="9dc6b-135">Appareils</span><span class="sxs-lookup"><span data-stu-id="9dc6b-135">Devices</span></span>

  <span data-ttu-id="9dc6b-136">Tous les appareils identifiés comme faisant partie ou liés à l'incident.</span><span class="sxs-lookup"><span data-stu-id="9dc6b-136">All the devices that have been identified to be part of or related to the incident.</span></span>

- <span data-ttu-id="9dc6b-137">Utilisateurs</span><span class="sxs-lookup"><span data-stu-id="9dc6b-137">Users</span></span>

  <span data-ttu-id="9dc6b-138">Tous les utilisateurs identifiés comme faisant partie ou associés à l'incident.</span><span class="sxs-lookup"><span data-stu-id="9dc6b-138">All the users that have been identified to be part of or related to the incident.</span></span>

- <span data-ttu-id="9dc6b-139">Boîtes aux lettres</span><span class="sxs-lookup"><span data-stu-id="9dc6b-139">Mailboxes</span></span>

  <span data-ttu-id="9dc6b-140">Toutes les boîtes aux lettres identifiées comme faisant partie ou liées à l'incident.</span><span class="sxs-lookup"><span data-stu-id="9dc6b-140">All the mailboxes that have been identified to be part of or related to the incident.</span></span>

- <span data-ttu-id="9dc6b-141">Examens</span><span class="sxs-lookup"><span data-stu-id="9dc6b-141">Investigations</span></span>

  <span data-ttu-id="9dc6b-142">Toutes les enquêtes automatisées déclenchées par des alertes dans l'incident.</span><span class="sxs-lookup"><span data-stu-id="9dc6b-142">All the automated investigations triggered by alerts in the incident.</span></span>

- <span data-ttu-id="9dc6b-143">Preuve et réponse</span><span class="sxs-lookup"><span data-stu-id="9dc6b-143">Evidence and Response</span></span>

  <span data-ttu-id="9dc6b-144">Tous les événements pris en charge et entités suspectes dans les alertes dans l'incident.</span><span class="sxs-lookup"><span data-stu-id="9dc6b-144">All the supported events and suspicious entities in the alerts in the incident.</span></span>

<span data-ttu-id="9dc6b-145">Voici la relation entre un incident et ses données et les onglets d'un incident dans le Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="9dc6b-145">Here's the relationship between an incident and its data and the tabs of an incident in the Microsoft 365 security center.</span></span>

:::image type="content" source="../../media/incidents-overview/incidents-security-center.png" alt-text="Relation d'un incident et de ses données avec les onglets d'un incident dans le Centre de sécurité Microsoft 365":::

## <a name="next-step"></a><span data-ttu-id="9dc6b-147">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="9dc6b-147">Next step</span></span>

<span data-ttu-id="9dc6b-148">La file d'attente des incidents de la page **Incidents** répertorie les incidents les plus récents.</span><span class="sxs-lookup"><span data-stu-id="9dc6b-148">The incident queue from the **Incidents** page lists the most recent incidents.</span></span> <span data-ttu-id="9dc6b-149">À partir de là, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="9dc6b-149">From here, you can:</span></span>

- <span data-ttu-id="9dc6b-150">Voir quels incidents doivent [être](incident-queue.md) hiérarchisés en fonction de la gravité et d'autres facteurs.</span><span class="sxs-lookup"><span data-stu-id="9dc6b-150">See which incidents should be [prioritized](incident-queue.md) based on severity and other factors.</span></span> 
- <span data-ttu-id="9dc6b-151">Effectuer une [investigation d'un](investigate-incidents.md) incident.</span><span class="sxs-lookup"><span data-stu-id="9dc6b-151">Perform an [investigation](investigate-incidents.md) of an incident.</span></span>
- <span data-ttu-id="9dc6b-152">[Gérer les incidents,](manage-incidents.md)ce qui inclut le changement de nom, leur affectation, la classification et l'ajout de balises pour votre flux de travail de gestion des incidents.</span><span class="sxs-lookup"><span data-stu-id="9dc6b-152">[Manage incidents](manage-incidents.md), which includes renaming, assigning them, classifying, and adding tags for your incident management workflow.</span></span>
