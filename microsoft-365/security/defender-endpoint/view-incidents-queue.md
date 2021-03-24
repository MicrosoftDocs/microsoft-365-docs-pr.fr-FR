---
title: Afficher et organiser la file d’attente Incidents
ms.reviewer: ''
description: Consultez la liste des incidents et découvrez comment appliquer des filtres pour limiter la liste et obtenir une vue plus centrée.
keywords: afficher, organiser, incidents, agrégation, enquêtes, file d’attente, ttp
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: ellevin
author: levinec
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: f25189ac6550d9c3349e08f7e7ac685d4b8031fc
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51063734"
---
# <a name="view-and-organize-the-microsoft-defender-for-endpoint-incidents-queue"></a><span data-ttu-id="d1810-104">Afficher et organiser la file d’attente Microsoft Defender pour les incidents de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="d1810-104">View and organize the Microsoft Defender for Endpoint Incidents queue</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="d1810-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="d1810-105">**Applies to:**</span></span>
- [<span data-ttu-id="d1810-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="d1810-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="d1810-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="d1810-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="d1810-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="d1810-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="d1810-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="d1810-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-pullalerts-abovefoldlink) 

<span data-ttu-id="d1810-110">La **file d’attente Incidents** affiche un ensemble d’incidents qui ont été signalés à partir d’appareils de votre réseau.</span><span class="sxs-lookup"><span data-stu-id="d1810-110">The **Incidents queue** shows a collection of incidents that were flagged from devices in your network.</span></span> <span data-ttu-id="d1810-111">Elle vous aide à trier les incidents afin de hiérarchiser et de créer une décision de réponse cyber-sécurité.</span><span class="sxs-lookup"><span data-stu-id="d1810-111">It helps you sort through incidents to prioritize and create an informed cybersecurity response decision.</span></span>

<span data-ttu-id="d1810-112">Par défaut, la file d’attente affiche les incidents observés au cours des 30 derniers jours, le plus récent s’affichant en haut de la liste, ce qui vous aide à voir les incidents les plus récents en premier.</span><span class="sxs-lookup"><span data-stu-id="d1810-112">By default, the queue displays incidents seen in the last 30 days, with the most recent incident showing at the top of the list, helping you see the most recent incidents first.</span></span>

<span data-ttu-id="d1810-113">Vous pouvez choisir parmi plusieurs options pour personnaliser l’affichage de file d’attente Incidents.</span><span class="sxs-lookup"><span data-stu-id="d1810-113">There are several options you can choose from to customize the Incidents queue view.</span></span> 

<span data-ttu-id="d1810-114">Dans la barre de navigation supérieure, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="d1810-114">On the top navigation you can:</span></span>
- <span data-ttu-id="d1810-115">Personnaliser des colonnes pour ajouter ou supprimer des colonnes</span><span class="sxs-lookup"><span data-stu-id="d1810-115">Customize columns to add or remove columns</span></span> 
- <span data-ttu-id="d1810-116">Modifier le nombre d’éléments à afficher par page</span><span class="sxs-lookup"><span data-stu-id="d1810-116">Modify the number of items to view per page</span></span>
- <span data-ttu-id="d1810-117">Sélectionner les éléments à afficher par page</span><span class="sxs-lookup"><span data-stu-id="d1810-117">Select the items to show per page</span></span>
- <span data-ttu-id="d1810-118">Sélectionner par lot les incidents à affecter</span><span class="sxs-lookup"><span data-stu-id="d1810-118">Batch-select the incidents to assign</span></span> 
- <span data-ttu-id="d1810-119">Naviguer entre les pages</span><span class="sxs-lookup"><span data-stu-id="d1810-119">Navigate between pages</span></span>
- <span data-ttu-id="d1810-120">Appliquer des filtres</span><span class="sxs-lookup"><span data-stu-id="d1810-120">Apply filters</span></span>

![Image de la file d’attente des incidents](images/atp-incident-queue.png)

## <a name="sort-and-filter-the-incidents-queue"></a><span data-ttu-id="d1810-122">Trier et filtrer la file d’attente des incidents</span><span class="sxs-lookup"><span data-stu-id="d1810-122">Sort and filter the incidents queue</span></span>
<span data-ttu-id="d1810-123">Vous pouvez appliquer les filtres suivants pour limiter la liste des incidents et obtenir une vue plus centrée.</span><span class="sxs-lookup"><span data-stu-id="d1810-123">You can apply the following filters to limit the list of incidents and get a more focused view.</span></span>

### <a name="severity"></a><span data-ttu-id="d1810-124">Severity</span><span class="sxs-lookup"><span data-stu-id="d1810-124">Severity</span></span>

<span data-ttu-id="d1810-125">Gravité de l’incident</span><span class="sxs-lookup"><span data-stu-id="d1810-125">Incident severity</span></span> | <span data-ttu-id="d1810-126">Description</span><span class="sxs-lookup"><span data-stu-id="d1810-126">Description</span></span>
:---|:---
<span data-ttu-id="d1810-127">Élevé</span><span class="sxs-lookup"><span data-stu-id="d1810-127">High</span></span> </br><span data-ttu-id="d1810-128">(Rouge)</span><span class="sxs-lookup"><span data-stu-id="d1810-128">(Red)</span></span> | <span data-ttu-id="d1810-129">Menaces souvent associées à des menaces avancées persistantes (APT).</span><span class="sxs-lookup"><span data-stu-id="d1810-129">Threats often associated with advanced persistent threats (APT).</span></span> <span data-ttu-id="d1810-130">Ces incidents indiquent un risque élevé en raison de la gravité des dommages qu’ils peuvent causer sur les appareils.</span><span class="sxs-lookup"><span data-stu-id="d1810-130">These incidents indicate a high risk due to the severity of damage they can inflict on devices.</span></span>
<span data-ttu-id="d1810-131">Moyen</span><span class="sxs-lookup"><span data-stu-id="d1810-131">Medium</span></span> </br><span data-ttu-id="d1810-132">(Orange)</span><span class="sxs-lookup"><span data-stu-id="d1810-132">(Orange)</span></span> | <span data-ttu-id="d1810-133">Menaces rarement observées dans l’organisation, telles que la modification anormale du Registre, l’exécution de fichiers suspects et les comportements observés typiques des phases d’attaque.</span><span class="sxs-lookup"><span data-stu-id="d1810-133">Threats rarely observed in the organization, such as anomalous registry change, execution of suspicious files, and observed behaviors typical of attack stages.</span></span>
<span data-ttu-id="d1810-134">Faible</span><span class="sxs-lookup"><span data-stu-id="d1810-134">Low</span></span> </br><span data-ttu-id="d1810-135">(Jaune)</span><span class="sxs-lookup"><span data-stu-id="d1810-135">(Yellow)</span></span> | <span data-ttu-id="d1810-136">Menaces associées à des programmes malveillants et à des outils de piratage répandus qui n’indiquent pas nécessairement une menace avancée ciblant l’organisation.</span><span class="sxs-lookup"><span data-stu-id="d1810-136">Threats associated with prevalent malware and hack-tools that do not necessarily indicate an advanced threat targeting the organization.</span></span>
<span data-ttu-id="d1810-137">Informationnel</span><span class="sxs-lookup"><span data-stu-id="d1810-137">Informational</span></span> </br><span data-ttu-id="d1810-138">(Gris)</span><span class="sxs-lookup"><span data-stu-id="d1810-138">(Grey)</span></span> | <span data-ttu-id="d1810-139">Les incidents d’information peuvent ne pas être considérés comme dangereux pour le réseau, mais ils peuvent être utiles pour assurer le suivi.</span><span class="sxs-lookup"><span data-stu-id="d1810-139">Informational incidents might not be considered harmful to the network but might be good to keep track of.</span></span>

## <a name="assigned-to"></a><span data-ttu-id="d1810-140">Affectée à</span><span class="sxs-lookup"><span data-stu-id="d1810-140">Assigned to</span></span>
<span data-ttu-id="d1810-141">Vous pouvez choisir de filtrer la liste en sélectionnant ceux qui vous sont affectés ou ceux qui vous sont affectés.</span><span class="sxs-lookup"><span data-stu-id="d1810-141">You can choose to filter the list by selecting assigned to anyone or ones that are assigned to you.</span></span>

### <a name="category"></a><span data-ttu-id="d1810-142">Catégorie</span><span class="sxs-lookup"><span data-stu-id="d1810-142">Category</span></span>
<span data-ttu-id="d1810-143">Les incidents sont classés en fonction de la description de l’étape à laquelle se trouve la chaîne de fin de la cybersécurité.</span><span class="sxs-lookup"><span data-stu-id="d1810-143">Incidents are categorized based on the description of the stage by which the cybersecurity kill chain is in.</span></span> <span data-ttu-id="d1810-144">Cette vue permet à l’analyste de menaces de déterminer la priorité, l’urgence et la stratégie de réponse correspondante à déployer en fonction du contexte.</span><span class="sxs-lookup"><span data-stu-id="d1810-144">This view helps the threat analyst to determine priority, urgency, and corresponding response strategy to deploy based on context.</span></span>

### <a name="status"></a><span data-ttu-id="d1810-145">Statut</span><span class="sxs-lookup"><span data-stu-id="d1810-145">Status</span></span>
<span data-ttu-id="d1810-146">Vous pouvez choisir de limiter la liste des incidents affichés en fonction de leur état pour identifier ceux qui sont actifs ou résolus.</span><span class="sxs-lookup"><span data-stu-id="d1810-146">You can choose to limit the list of incidents shown based on their status to see which ones are active or resolved.</span></span>

### <a name="data-sensitivity"></a><span data-ttu-id="d1810-147">Confidentialité des données</span><span class="sxs-lookup"><span data-stu-id="d1810-147">Data sensitivity</span></span>
<span data-ttu-id="d1810-148">Utilisez ce filtre pour afficher les incidents qui contiennent des étiquettes de sensibilité.</span><span class="sxs-lookup"><span data-stu-id="d1810-148">Use this filter to show incidents that contain sensitivity labels.</span></span>

## <a name="incident-naming"></a><span data-ttu-id="d1810-149">Nommage d’incident</span><span class="sxs-lookup"><span data-stu-id="d1810-149">Incident naming</span></span>

<span data-ttu-id="d1810-150">Pour comprendre l’étendue de l’incident en un coup d’œil, les noms des incidents sont générés automatiquement en fonction des attributs d’alerte tels que le nombre de points de terminaison affectés, les utilisateurs affectés, les sources de détection ou les catégories.</span><span class="sxs-lookup"><span data-stu-id="d1810-150">To understand the incident's scope at a glance, incident names are automatically generated based on alert attributes such as the number of endpoints affected, users affected, detection sources or categories.</span></span>

<span data-ttu-id="d1810-151">Par exemple : *incident en plusieurs étapes sur plusieurs points de terminaison signalés par plusieurs sources.*</span><span class="sxs-lookup"><span data-stu-id="d1810-151">For example: *Multi-stage incident on multiple endpoints reported by multiple sources.*</span></span>

> [!NOTE]
> <span data-ttu-id="d1810-152">Les incidents qui existaient avant le déploiement de la dénomination automatique des incidents conserveront leur nom.</span><span class="sxs-lookup"><span data-stu-id="d1810-152">Incidents that existed prior the rollout of automatic incident naming will retain their name.</span></span>


## <a name="see-also"></a><span data-ttu-id="d1810-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1810-153">See also</span></span>
- [<span data-ttu-id="d1810-154">File d’attente des incidents</span><span class="sxs-lookup"><span data-stu-id="d1810-154">Incidents queue</span></span>](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/view-incidents-queue)
- [<span data-ttu-id="d1810-155">Gérer les incidents</span><span class="sxs-lookup"><span data-stu-id="d1810-155">Manage incidents</span></span>](manage-incidents.md)
- [<span data-ttu-id="d1810-156">Enquêter sur des incidents</span><span class="sxs-lookup"><span data-stu-id="d1810-156">Investigate incidents</span></span>](investigate-incidents.md)
