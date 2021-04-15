---
title: Gérer les incidents dans Microsoft 365 Defender
description: Découvrez comment attribuer, mettre à jour l’état,
keywords: incident, incidents, alertes, alertes corrélées, attribuer, mettre à jour, état, gérer, classification, microsoft, 365, m365
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
ms.openlocfilehash: 2d2bf18c6cacb377e710f34b74ec8f83bb77d3b1
ms.sourcegitcommit: 223a36a86753fe9cebee96f05ab4c9a144133677
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "51760063"
---
# <a name="manage-incidents-in-microsoft-365-defender"></a><span data-ttu-id="21d08-104">Gérer les incidents dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="21d08-104">Manage incidents in Microsoft 365 Defender</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="21d08-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="21d08-105">**Applies to:**</span></span>
- <span data-ttu-id="21d08-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="21d08-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="21d08-107">La gestion des incidents est essentielle pour s'assurer que les menaces sont contenues et traitées.</span><span class="sxs-lookup"><span data-stu-id="21d08-107">Incident management is critical in ensuring that threats are contained and addressed.</span></span>

<span data-ttu-id="21d08-108">Vous gérez les incidents à partir **d'incidents & alertes** > Incidents dans le lancement rapide du Centre de sécurité Microsoft 365 ([security.microsoft.com](https://security.microsoft.com)).</span><span class="sxs-lookup"><span data-stu-id="21d08-108">You manage incidents from **Incidents & alerts > Incidents** on the quick launch of the Microsoft 365 security center ([security.microsoft.com](https://security.microsoft.com)).</span></span> <span data-ttu-id="21d08-109">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="21d08-109">Here's an example.</span></span>

:::image type="content" source="../../media/incidents-queue/incidents-ss-incidents.png" alt-text="Exemple de file d'attente d'incident":::

<span data-ttu-id="21d08-111">Voici comment gérer vos incidents :</span><span class="sxs-lookup"><span data-stu-id="21d08-111">Here are the ways you can manage your incidents:</span></span>

- <span data-ttu-id="21d08-112">Modifier le nom de l'incident</span><span class="sxs-lookup"><span data-stu-id="21d08-112">Change the incident name</span></span>
- <span data-ttu-id="21d08-113">Ajoutez des balises d'incident.</span><span class="sxs-lookup"><span data-stu-id="21d08-113">Add incident tags.</span></span>
- <span data-ttu-id="21d08-114">Affecter l'incident à un compte d'utilisateur</span><span class="sxs-lookup"><span data-stu-id="21d08-114">Assign the incident to a user account</span></span>
- <span data-ttu-id="21d08-115">Résoudre les problèmes</span><span class="sxs-lookup"><span data-stu-id="21d08-115">Resolve them</span></span> 
- <span data-ttu-id="21d08-116">Définir sa classification et sa détermination</span><span class="sxs-lookup"><span data-stu-id="21d08-116">Set its classification and determination</span></span>
- <span data-ttu-id="21d08-117">Ajoutez des commentaires.</span><span class="sxs-lookup"><span data-stu-id="21d08-117">Add comments.</span></span>

<span data-ttu-id="21d08-118">Vous pouvez gérer les incidents à partir du volet Gérer **les incidents** pour un incident.</span><span class="sxs-lookup"><span data-stu-id="21d08-118">You can manage incidents from the **Manage incident** pane for an incident.</span></span> <span data-ttu-id="21d08-119">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="21d08-119">Here's an example.</span></span>

:::image type="content" source="../../media/incidents-queue/incidents-ss-incidents-manage.png" alt-text="Exemple du volet Gérer les incidents d'un incident":::

<span data-ttu-id="21d08-121">Vous pouvez afficher ce volet à partir du lien **Gérer l'incident** sur :</span><span class="sxs-lookup"><span data-stu-id="21d08-121">You can display this pane from the **Manage incident** link on the:</span></span>

- <span data-ttu-id="21d08-122">Volet des propriétés d'un incident dans la file d'attente des incidents.</span><span class="sxs-lookup"><span data-stu-id="21d08-122">Properties pane of an incident in the incident queue.</span></span>
- <span data-ttu-id="21d08-123">**Page récapitulatif** d'un incident.</span><span class="sxs-lookup"><span data-stu-id="21d08-123">**Summary** page of an incident.</span></span>

<span data-ttu-id="21d08-124">Dans les cas où, lors de l'enquête, vous souhaitez déplacer des alertes d'un incident à un autre, vous pouvez également le faire à partir de l'onglet **Alertes,** créant ainsi un incident plus ou moins volumineux qui inclut toutes les alertes pertinentes.</span><span class="sxs-lookup"><span data-stu-id="21d08-124">In cases where, while investigating you would like to move alerts from one incident to another, you can also do so from the **Alerts** tab, thus creating a larger or smaller incident that includes all relevant alerts.</span></span>

## <a name="edit-the-incident-name"></a><span data-ttu-id="21d08-125">Modifier le nom de l'incident</span><span class="sxs-lookup"><span data-stu-id="21d08-125">Edit the incident name</span></span>

<span data-ttu-id="21d08-126">Un nom est automatiquement attribué aux incidents en fonction des attributs d'alerte tels que le nombre de points de terminaison affectés, les utilisateurs affectés, les sources de détection ou les catégories.</span><span class="sxs-lookup"><span data-stu-id="21d08-126">Incidents are automatically assigned a name based on alert attributes such as the number of endpoints affected, users affected, detection sources or categories.</span></span> <span data-ttu-id="21d08-127">Cela vous permet de comprendre rapidement l'étendue de l'incident.</span><span class="sxs-lookup"><span data-stu-id="21d08-127">This allows you to quickly understand the scope of the incident.</span></span> <span data-ttu-id="21d08-128">Par exemple : incident en plusieurs étapes sur plusieurs points de *terminaison signalés par plusieurs sources.*</span><span class="sxs-lookup"><span data-stu-id="21d08-128">For example: *Multi-stage incident on multiple endpoints reported by multiple sources.*</span></span>

<span data-ttu-id="21d08-129">Vous pouvez modifier le nom de l'incident à partir du **champ Nom de l'incident** dans le volet Gérer **l'incident.**</span><span class="sxs-lookup"><span data-stu-id="21d08-129">You can edit the incident name from the **Incident name** field on the **Manage incident** pane.</span></span>

> [!NOTE]
> <span data-ttu-id="21d08-130">Les incidents qui existaient avant le déploiement de la fonctionnalité de nommage automatique des incidents conserveront leur nom.</span><span class="sxs-lookup"><span data-stu-id="21d08-130">Incidents that existed prior the rollout of the automatic incident naming feature will retain their name.</span></span>

## <a name="add-incident-tags"></a><span data-ttu-id="21d08-131">Ajouter des balises d’incident</span><span class="sxs-lookup"><span data-stu-id="21d08-131">Add incident tags</span></span>

<span data-ttu-id="21d08-132">Vous pouvez ajouter des balises personnalisées à un incident, par exemple pour baliser un groupe d'incidents avec une caractéristique commune.</span><span class="sxs-lookup"><span data-stu-id="21d08-132">You can add custom tags to an incident, for example to flag a group of incidents with a common characteristic.</span></span> <span data-ttu-id="21d08-133">Vous pouvez ensuite filtrer la file d'attente des incidents pour tous les incidents qui contiennent une balise spécifique.</span><span class="sxs-lookup"><span data-stu-id="21d08-133">You can later filter the incident queue for all incidents that contain a specific tag.</span></span>

<span data-ttu-id="21d08-134">Lorsque vous commencez à taper, vous avez la possibilité de sélectionner des balises dans une liste de balises sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="21d08-134">When you start typing, you have the option to select from a list of selected tags.</span></span>

## <a name="assign-incidents"></a><span data-ttu-id="21d08-135">Attribuer des incidents</span><span class="sxs-lookup"><span data-stu-id="21d08-135">Assign incidents</span></span>

<span data-ttu-id="21d08-136">Si aucun incident n'a encore été affecté, vous pouvez sélectionner **Affecter** à et spécifier le compte d'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="21d08-136">If an incident has not yet been assigned, you can select **Assign to** and specify the user account.</span></span> <span data-ttu-id="21d08-137">Cette action affecte la propriété de l'incident et toutes les alertes qui lui sont associées.</span><span class="sxs-lookup"><span data-stu-id="21d08-137">Doing so assigns ownership of the incident and all the alerts associated with it.</span></span>

## <a name="resolve-incident"></a><span data-ttu-id="21d08-138">Résoudre l'incident</span><span class="sxs-lookup"><span data-stu-id="21d08-138">Resolve incident</span></span>

<span data-ttu-id="21d08-139">Si l'incident a été corrigé, sélectionnez **Résoudre l'incident** pour déplacer le basculement vers la droite.</span><span class="sxs-lookup"><span data-stu-id="21d08-139">If the incident has been remediated, select **Resolve incident** to move the toggle to the right.</span></span> <span data-ttu-id="21d08-140">Notez que la résolution d'un incident résout également toutes les alertes liées et actives liées à l'incident.</span><span class="sxs-lookup"><span data-stu-id="21d08-140">Note that resolving an incident also resolves all the linked and active alerts related to the incident.</span></span>

<span data-ttu-id="21d08-141">Un incident qui n'est pas résolu s'affiche comme **étant actif.**</span><span class="sxs-lookup"><span data-stu-id="21d08-141">An incident that is not resolved displays as **Active**.</span></span>

## <a name="set-the-classification-and-determination"></a><span data-ttu-id="21d08-142">Définir la classification et la détermination</span><span class="sxs-lookup"><span data-stu-id="21d08-142">Set the classification and determination</span></span>

<span data-ttu-id="21d08-143">La classification des incidents est de savoir s'il s'agit d'une alerte vraie ou d'une fausse alerte, que vous configurez à partir du champ **Classification.**</span><span class="sxs-lookup"><span data-stu-id="21d08-143">The incident classification is whether it was a true alert or a false alert, which you configure from the **Classification** field.</span></span> 

<span data-ttu-id="21d08-144">S'il s'agissait d'une alerte réelle, vous devez également spécifier le type de menace qu'il s'agissait du **champ Détermination.**</span><span class="sxs-lookup"><span data-stu-id="21d08-144">If it was a true alert, you should also specify what type of threat it was with the **Determination** field.</span></span> <span data-ttu-id="21d08-145">La spécification du type de menace permet à votre équipe de sécurité de voir les modèles de menace et d'agir pour défendre votre organisation contre ces modèles.</span><span class="sxs-lookup"><span data-stu-id="21d08-145">Specifying the threat type helps your security team see threat patterns and act to defend your organization from them.</span></span> 

## <a name="add-comments"></a><span data-ttu-id="21d08-146">Ajouter des commentaires</span><span class="sxs-lookup"><span data-stu-id="21d08-146">Add comments</span></span>

<span data-ttu-id="21d08-147">Vous pouvez ajouter plusieurs commentaires à un incident avec le **champ** Commentaire.</span><span class="sxs-lookup"><span data-stu-id="21d08-147">You can add multiple comments to an incident with the **Comment** field.</span></span> <span data-ttu-id="21d08-148">Chaque commentaire est ajouté aux événements historiques de l'incident.</span><span class="sxs-lookup"><span data-stu-id="21d08-148">Each comment is added to the historical events of the incident.</span></span> <span data-ttu-id="21d08-149">Vous pouvez voir les commentaires et l'historique d'un incident à partir du lien Commentaires et historique dans la page **Résumé.** </span><span class="sxs-lookup"><span data-stu-id="21d08-149">You can see the comments and history of an incident from the **Comments and history** link on the **Summary** page.</span></span>
