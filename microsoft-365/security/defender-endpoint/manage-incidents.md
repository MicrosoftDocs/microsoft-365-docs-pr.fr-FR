---
title: Gérer Microsoft Defender pour les incidents de point de terminaison
description: Gérez les incidents en l’attribuant, en mettant à jour son état ou en attribuant sa classification.
keywords: incidents, gérer, affecter, état, classification, alerte vraie, alerte false
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
ms.technology: mde
ms.openlocfilehash: c86b53abf54788740c8c78cb0ecf9251b10ea8f7
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52842337"
---
# <a name="manage-microsoft-defender-for-endpoint-incidents"></a><span data-ttu-id="3e52c-104">Gérer Microsoft Defender pour les incidents de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="3e52c-104">Manage Microsoft Defender for Endpoint incidents</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="3e52c-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="3e52c-105">**Applies to:**</span></span>
- [<span data-ttu-id="3e52c-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="3e52c-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="3e52c-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="3e52c-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="3e52c-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="3e52c-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="3e52c-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="3e52c-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="3e52c-110">La gestion des incidents est une partie importante de chaque opération de cybersécurité.</span><span class="sxs-lookup"><span data-stu-id="3e52c-110">Managing incidents is an important part of every cybersecurity operation.</span></span> <span data-ttu-id="3e52c-111">Vous pouvez gérer les incidents en sélectionnant un incident dans la file **d’attente Incidents** ou dans le volet de **gestion Incidents.**</span><span class="sxs-lookup"><span data-stu-id="3e52c-111">You can manage incidents by selecting an incident from the **Incidents queue** or the **Incidents management pane**.</span></span> 


<span data-ttu-id="3e52c-112">La sélection d’un incident dans la  file **d’attente Incidents** ouvre le volet Gestion des incidents dans lequel vous pouvez ouvrir la page incident pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="3e52c-112">Selecting an incident from the **Incidents queue** brings up the **Incident management pane** where you can open the incident page for details.</span></span>


![Image du volet de gestion des incidents](images/atp-incidents-mgt-pane-updated.png)

<span data-ttu-id="3e52c-114">Vous pouvez affecter des incidents à vous-même, modifier l’état et la classification, les renommer ou commenter pour suivre leur progression.</span><span class="sxs-lookup"><span data-stu-id="3e52c-114">You can assign incidents to yourself, change the status and classification, rename, or comment on them to keep track of their progress.</span></span>

> [!TIP]
> <span data-ttu-id="3e52c-115">Pour une visibilité supplémentaire en un coup d’œil, les noms des incidents sont générés automatiquement en fonction des attributs d’alerte tels que le nombre de points de terminaison affectés, les utilisateurs affectés, les sources de détection ou les catégories.</span><span class="sxs-lookup"><span data-stu-id="3e52c-115">For additional visibility at a glance, incident names are automatically generated based on alert attributes such as the number of endpoints affected, users affected, detection sources or categories.</span></span> <span data-ttu-id="3e52c-116">Cela vous permet de comprendre rapidement l’étendue de l’incident.</span><span class="sxs-lookup"><span data-stu-id="3e52c-116">This allows you to quickly understand the scope of the incident.</span></span>
>
> <span data-ttu-id="3e52c-117">Par exemple : *incident en plusieurs étapes sur plusieurs points de terminaison signalés par plusieurs sources.*</span><span class="sxs-lookup"><span data-stu-id="3e52c-117">For example: *Multi-stage incident on multiple endpoints reported by multiple sources.*</span></span>
>
> <span data-ttu-id="3e52c-118">Les incidents qui existaient avant le déploiement de la dénomination automatique des incidents conserveront leurs noms.</span><span class="sxs-lookup"><span data-stu-id="3e52c-118">Incidents that existed prior the rollout of automatic incident naming will retain their names.</span></span>
>


![Image de la page de détails de l’incident](images/atp-incident-details-updated.png)

## <a name="assign-incidents"></a><span data-ttu-id="3e52c-120">Attribuer des incidents</span><span class="sxs-lookup"><span data-stu-id="3e52c-120">Assign incidents</span></span>
<span data-ttu-id="3e52c-121">Si aucun incident n’a encore  été affecté, vous pouvez sélectionner Affecter à moi pour vous attribuer l’incident.</span><span class="sxs-lookup"><span data-stu-id="3e52c-121">If an incident has not been assigned yet, you can select **Assign to me** to assign the incident to yourself.</span></span> <span data-ttu-id="3e52c-122">Cette action suppose l’appropriation non seulement de l’incident, mais aussi de toutes les alertes associées.</span><span class="sxs-lookup"><span data-stu-id="3e52c-122">Doing so assumes ownership of not just the incident, but also all the alerts associated with it.</span></span>

## <a name="set-status-and-classification"></a><span data-ttu-id="3e52c-123">Définir l’état et la classification</span><span class="sxs-lookup"><span data-stu-id="3e52c-123">Set status and classification</span></span>
### <a name="incident-status"></a><span data-ttu-id="3e52c-124">État de l’incident</span><span class="sxs-lookup"><span data-stu-id="3e52c-124">Incident status</span></span>
<span data-ttu-id="3e52c-125">Vous pouvez classer les incidents (comme **actifs** ou **résolus**) en modifiant leur état au fur et à mesure de l’avancement de votre enquête.</span><span class="sxs-lookup"><span data-stu-id="3e52c-125">You can categorize incidents (as **Active**, or **Resolved**) by changing their status as your investigation progresses.</span></span> <span data-ttu-id="3e52c-126">Cela vous permet d’organiser et de gérer la manière dont votre équipe peut réagir aux incidents.</span><span class="sxs-lookup"><span data-stu-id="3e52c-126">This helps you organize and manage how your team can respond to incidents.</span></span>

<span data-ttu-id="3e52c-127">Par exemple, votre analyste SoC peut examiner les incidents **actifs** urgents de la journée et décider de les affecter à lui-même pour examen.</span><span class="sxs-lookup"><span data-stu-id="3e52c-127">For example, your SoC analyst can review the urgent **Active** incidents for the day, and decide to assign them to himself for investigation.</span></span>

<span data-ttu-id="3e52c-128">Sinon, votre analyste SoC peut  définir l’incident comme résolu si l’incident a été corrigé.</span><span class="sxs-lookup"><span data-stu-id="3e52c-128">Alternatively, your SoC analyst might set the incident as **Resolved** if the incident has been remediated.</span></span> 

### <a name="classification"></a><span data-ttu-id="3e52c-129">Classification</span><span class="sxs-lookup"><span data-stu-id="3e52c-129">Classification</span></span>
<span data-ttu-id="3e52c-130">Vous pouvez choisir de ne pas définir de classification ou décider de spécifier si un incident est vrai ou faux.</span><span class="sxs-lookup"><span data-stu-id="3e52c-130">You can choose not to set a classification, or decide to specify whether an incident is true or false.</span></span> <span data-ttu-id="3e52c-131">Cette opération permet à l’équipe de voir les modèles et d’en apprendre davantage.</span><span class="sxs-lookup"><span data-stu-id="3e52c-131">Doing so helps the team see patterns and learn from them.</span></span>

### <a name="add-comments"></a><span data-ttu-id="3e52c-132">Ajouter des commentaires</span><span class="sxs-lookup"><span data-stu-id="3e52c-132">Add comments</span></span>
<span data-ttu-id="3e52c-133">Vous pouvez ajouter des commentaires et afficher les événements historiques relatifs à un incident afin de voir les modifications précédentes apportées à ce dernier.</span><span class="sxs-lookup"><span data-stu-id="3e52c-133">You can add comments and view historical events about an incident to see previous changes made to it.</span></span>

<span data-ttu-id="3e52c-134">Chaque fois qu’une modification ou un commentaire est apporté à une alerte, cet élément est enregistré dans la section Commentaires et historique.</span><span class="sxs-lookup"><span data-stu-id="3e52c-134">Whenever a change or comment is made to an alert, it is recorded in the Comments and history section.</span></span>

<span data-ttu-id="3e52c-135">Les commentaires ajoutés apparaissent instantanément dans le volet.</span><span class="sxs-lookup"><span data-stu-id="3e52c-135">Added comments instantly appear on the pane.</span></span>



## <a name="related-topics"></a><span data-ttu-id="3e52c-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e52c-136">Related topics</span></span>
- [<span data-ttu-id="3e52c-137">File d’attente des incidents</span><span class="sxs-lookup"><span data-stu-id="3e52c-137">Incidents queue</span></span>](/microsoft-365/security/defender-endpoint/view-incidents-queue)
- [<span data-ttu-id="3e52c-138">Afficher et organiser la file d’attente des incidents</span><span class="sxs-lookup"><span data-stu-id="3e52c-138">View and organize the Incidents queue</span></span>](view-incidents-queue.md)
- [<span data-ttu-id="3e52c-139">Examiner des incidents</span><span class="sxs-lookup"><span data-stu-id="3e52c-139">Investigate incidents</span></span>](investigate-incidents.md)
