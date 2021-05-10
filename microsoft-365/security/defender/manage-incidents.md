---
title: Gérer les incidents dans Microsoft 365 Defender
description: Découvrez comment attribuer, mettre à jour l’état,
keywords: incident, incidents, analyse, réponse, alertes, alertes corrélées, affecter, mettre à jour, état, gérer, classification, microsoft, 365, m365
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
ms.openlocfilehash: 09c391d6b02e1273f55070283a6e11454f677114
ms.sourcegitcommit: de5fce90de22ba588e75e1a1d2e87e03b9e25ec7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "52300000"
---
# <a name="manage-incidents-in-microsoft-365-defender"></a><span data-ttu-id="621bc-104">Gérer les incidents dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="621bc-104">Manage incidents in Microsoft 365 Defender</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="621bc-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="621bc-105">**Applies to:**</span></span>
- <span data-ttu-id="621bc-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="621bc-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="621bc-107">La gestion des incidents est essentielle pour s’assurer que les menaces sont contenues et traitées.</span><span class="sxs-lookup"><span data-stu-id="621bc-107">Incident management is critical in ensuring that threats are contained and addressed.</span></span>

<span data-ttu-id="621bc-108">Vous gérez les incidents à partir **d’incidents & alertes** > incidents dans le lancement rapide du centre de sécurité Microsoft 365 ([security.microsoft.com](https://security.microsoft.com)).</span><span class="sxs-lookup"><span data-stu-id="621bc-108">You manage incidents from **Incidents & alerts > Incidents** on the quick launch of the Microsoft 365 security center ([security.microsoft.com](https://security.microsoft.com)).</span></span> <span data-ttu-id="621bc-109">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="621bc-109">Here's an example.</span></span>

:::image type="content" source="../../media/incidents-queue/incidents-ss-incidents.png" alt-text="Exemple de file d’attente d’incident":::

<span data-ttu-id="621bc-111">Voici comment gérer vos incidents :</span><span class="sxs-lookup"><span data-stu-id="621bc-111">Here are the ways you can manage your incidents:</span></span>

- <span data-ttu-id="621bc-112">Modifier le nom de l’incident</span><span class="sxs-lookup"><span data-stu-id="621bc-112">Change the incident name</span></span>
- <span data-ttu-id="621bc-113">Ajoutez des balises d’incident.</span><span class="sxs-lookup"><span data-stu-id="621bc-113">Add incident tags.</span></span>
- <span data-ttu-id="621bc-114">Affecter l’incident à un compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="621bc-114">Assign the incident to a user account</span></span>
- <span data-ttu-id="621bc-115">Résoudre les problèmes</span><span class="sxs-lookup"><span data-stu-id="621bc-115">Resolve them</span></span> 
- <span data-ttu-id="621bc-116">Définir sa classification et sa détermination</span><span class="sxs-lookup"><span data-stu-id="621bc-116">Set its classification and determination</span></span>
- <span data-ttu-id="621bc-117">Ajoutez des commentaires.</span><span class="sxs-lookup"><span data-stu-id="621bc-117">Add comments.</span></span>

<span data-ttu-id="621bc-118">Vous pouvez gérer les incidents à partir du **volet Gérer les incidents** pour un incident.</span><span class="sxs-lookup"><span data-stu-id="621bc-118">You can manage incidents from the **Manage incident** pane for an incident.</span></span> <span data-ttu-id="621bc-119">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="621bc-119">Here's an example.</span></span>

:::image type="content" source="../../media/incidents-queue/incidents-ss-incidents-manage.png" alt-text="Exemple du volet Gérer les incidents d’un incident":::

<span data-ttu-id="621bc-121">Vous pouvez afficher ce volet à partir du lien **Gérer l’incident** sur :</span><span class="sxs-lookup"><span data-stu-id="621bc-121">You can display this pane from the **Manage incident** link on the:</span></span>

- <span data-ttu-id="621bc-122">Volet des propriétés d’un incident dans la file d’attente des incidents.</span><span class="sxs-lookup"><span data-stu-id="621bc-122">Properties pane of an incident in the incident queue.</span></span>
- <span data-ttu-id="621bc-123">**Page récapitulatif** d’un incident.</span><span class="sxs-lookup"><span data-stu-id="621bc-123">**Summary** page of an incident.</span></span>

<span data-ttu-id="621bc-124">Dans les cas où, lors de l’analyse, vous souhaitez déplacer des alertes d’un incident à un autre, vous pouvez également le faire à partir de l’onglet **Alertes,** créant ainsi un incident plus ou moins volumineux qui inclut toutes les alertes pertinentes.</span><span class="sxs-lookup"><span data-stu-id="621bc-124">In cases where, while analyzing you would like to move alerts from one incident to another, you can also do so from the **Alerts** tab, thus creating a larger or smaller incident that includes all relevant alerts.</span></span>

## <a name="edit-the-incident-name"></a><span data-ttu-id="621bc-125">Modifier le nom de l’incident</span><span class="sxs-lookup"><span data-stu-id="621bc-125">Edit the incident name</span></span>

<span data-ttu-id="621bc-126">Microsoft 365 Defender attribue automatiquement un nom basé sur les attributs d’alerte tels que le nombre de points de terminaison affectés, les utilisateurs affectés, les sources de détection ou les catégories.</span><span class="sxs-lookup"><span data-stu-id="621bc-126">Microsoft 365 Defender automatically assigns a name based on alert attributes such as the number of endpoints affected, users affected, detection sources or categories.</span></span> <span data-ttu-id="621bc-127">Cela vous permet de comprendre rapidement l’étendue de l’incident.</span><span class="sxs-lookup"><span data-stu-id="621bc-127">This allows you to quickly understand the scope of the incident.</span></span> <span data-ttu-id="621bc-128">Par exemple : *incident en plusieurs étapes sur plusieurs points de terminaison signalés par plusieurs sources.*</span><span class="sxs-lookup"><span data-stu-id="621bc-128">For example: *Multi-stage incident on multiple endpoints reported by multiple sources.*</span></span>

<span data-ttu-id="621bc-129">Vous pouvez modifier le nom de l’incident à partir du **champ Nom de l’incident** dans le volet Gérer **l’incident.**</span><span class="sxs-lookup"><span data-stu-id="621bc-129">You can edit the incident name from the **Incident name** field on the **Manage incident** pane.</span></span>

> [!NOTE]
> <span data-ttu-id="621bc-130">Les incidents qui existaient avant le déploiement de la fonctionnalité de nommage automatique des incidents conserveront leur nom.</span><span class="sxs-lookup"><span data-stu-id="621bc-130">Incidents that existed before the rollout of the automatic incident naming feature will retain their name.</span></span>

## <a name="add-incident-tags"></a><span data-ttu-id="621bc-131">Ajouter des balises d’incident</span><span class="sxs-lookup"><span data-stu-id="621bc-131">Add incident tags</span></span>

<span data-ttu-id="621bc-132">Vous pouvez ajouter des balises personnalisées à un incident, par exemple pour baliser un groupe d’incidents avec une caractéristique commune.</span><span class="sxs-lookup"><span data-stu-id="621bc-132">You can add custom tags to an incident, for example to flag a group of incidents with a common characteristic.</span></span> <span data-ttu-id="621bc-133">Vous pouvez ensuite filtrer la file d’attente des incidents pour tous les incidents qui contiennent une balise spécifique.</span><span class="sxs-lookup"><span data-stu-id="621bc-133">You can later filter the incident queue for all incidents that contain a specific tag.</span></span>

<span data-ttu-id="621bc-134">Lorsque vous commencez à taper, vous avez la possibilité de sélectionner des balises dans une liste de balises sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="621bc-134">When you start typing, you have the option to select from a list of selected tags.</span></span>

## <a name="assign-incidents"></a><span data-ttu-id="621bc-135">Attribuer des incidents</span><span class="sxs-lookup"><span data-stu-id="621bc-135">Assign incidents</span></span>

<span data-ttu-id="621bc-136">Si aucun incident n’a encore été affecté, vous pouvez sélectionner **Affecter** à et spécifier le compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="621bc-136">If an incident has not yet been assigned, you can select **Assign to** and specify the user account.</span></span> <span data-ttu-id="621bc-137">Cette action affecte la propriété de l’incident et toutes les alertes qui lui sont associées.</span><span class="sxs-lookup"><span data-stu-id="621bc-137">Doing so assigns ownership of the incident and all the alerts associated with it.</span></span>

## <a name="resolve-incident"></a><span data-ttu-id="621bc-138">Résoudre l’incident</span><span class="sxs-lookup"><span data-stu-id="621bc-138">Resolve incident</span></span>

<span data-ttu-id="621bc-139">Si l’incident a été corrigé, sélectionnez **Résoudre l’incident** pour déplacer le basculement vers la droite.</span><span class="sxs-lookup"><span data-stu-id="621bc-139">If the incident has been remediated, select **Resolve incident** to move the toggle to the right.</span></span> <span data-ttu-id="621bc-140">Notez que la résolution d’un incident résout également toutes les alertes liées et actives liées à l’incident.</span><span class="sxs-lookup"><span data-stu-id="621bc-140">Note that resolving an incident also resolves all the linked and active alerts related to the incident.</span></span>

<span data-ttu-id="621bc-141">Un incident qui n’est pas résolu s’affiche comme **étant actif.**</span><span class="sxs-lookup"><span data-stu-id="621bc-141">An incident that is not resolved displays as **Active**.</span></span>

## <a name="set-the-classification-and-determination"></a><span data-ttu-id="621bc-142">Définir la classification et la détermination</span><span class="sxs-lookup"><span data-stu-id="621bc-142">Set the classification and determination</span></span>

<span data-ttu-id="621bc-143">La classification des incidents est la question de savoir s’il s’agit d’une alerte vraie ou d’une fausse alerte, que vous configurez à partir du champ **Classification.**</span><span class="sxs-lookup"><span data-stu-id="621bc-143">The incident classification is whether it was a true alert or a false alert, which you configure from the **Classification** field.</span></span> 

<span data-ttu-id="621bc-144">S’il s’agissait d’une alerte réelle, vous devez également spécifier le type de menace qu’il s’agissait avec le **champ Détermination.**</span><span class="sxs-lookup"><span data-stu-id="621bc-144">If it was a true alert, you should also specify what type of threat it was with the **Determination** field.</span></span> <span data-ttu-id="621bc-145">La spécification du type de menace permet à votre équipe de sécurité de voir les modèles de menace et d’agir pour défendre votre organisation contre ces modèles.</span><span class="sxs-lookup"><span data-stu-id="621bc-145">Specifying the threat type helps your security team see threat patterns and act to defend your organization from them.</span></span> 

## <a name="add-comments"></a><span data-ttu-id="621bc-146">Ajouter des commentaires</span><span class="sxs-lookup"><span data-stu-id="621bc-146">Add comments</span></span>

<span data-ttu-id="621bc-147">Vous pouvez ajouter plusieurs commentaires à un incident avec le **champ** Commentaire.</span><span class="sxs-lookup"><span data-stu-id="621bc-147">You can add multiple comments to an incident with the **Comment** field.</span></span> <span data-ttu-id="621bc-148">Chaque commentaire est ajouté aux événements historiques de l’incident.</span><span class="sxs-lookup"><span data-stu-id="621bc-148">Each comment gets added to the historical events of the incident.</span></span> <span data-ttu-id="621bc-149">Vous pouvez voir les commentaires et l’historique d’un incident à partir du lien Commentaires et historique dans la page **Résumé.** </span><span class="sxs-lookup"><span data-stu-id="621bc-149">You can see the comments and history of an incident from the **Comments and history** link on the **Summary** page.</span></span>

## <a name="next-steps"></a><span data-ttu-id="621bc-150">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="621bc-150">Next steps</span></span>

<span data-ttu-id="621bc-151">Pour les nouveaux incidents, commencez votre [enquête.](investigate-incidents.md)</span><span class="sxs-lookup"><span data-stu-id="621bc-151">For new incidents, begin your [investigation](investigate-incidents.md).</span></span>

<span data-ttu-id="621bc-152">Pour les incidents in-process, poursuivez votre [enquête.](investigate-incidents.md)</span><span class="sxs-lookup"><span data-stu-id="621bc-152">For in-process incidents, continue your [investigation](investigate-incidents.md).</span></span>

<span data-ttu-id="621bc-153">Pour les incidents résolus, effectuez une révision [post-incident.](first-incident-post.md)</span><span class="sxs-lookup"><span data-stu-id="621bc-153">For resolved incidents, perform a [post-incident review](first-incident-post.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="621bc-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="621bc-154">See also</span></span>

- [<span data-ttu-id="621bc-155">Vue d’ensemble des incidents</span><span class="sxs-lookup"><span data-stu-id="621bc-155">Incidents overview</span></span>](incidents-overview.md)
- [<span data-ttu-id="621bc-156">Hiérarchiser les incidents</span><span class="sxs-lookup"><span data-stu-id="621bc-156">Prioritize incidents</span></span>](incident-queue.md)
- [<span data-ttu-id="621bc-157">Enquêter sur des incidents</span><span class="sxs-lookup"><span data-stu-id="621bc-157">Investigate incidents</span></span>](investigate-incidents.md)
