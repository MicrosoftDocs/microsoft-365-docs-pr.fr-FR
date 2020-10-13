---
title: Limites de chasse avancée dans la protection contre les menaces Microsoft
description: Comprendre les différentes limites de service qui maintiennent le service de chasse dynamique
keywords: chasse de menace, recherche de menace, recherche de menace informatique, protection contre les menaces Microsoft, Microsoft 365, MTP, M365, recherche, requête, télémétrie, schéma, Kusto, limite d’UC, limite de requête, ressources, résultats maximaux
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: lomayor
author: lomayor
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
ms.openlocfilehash: ab19c86bbdec243dd4abb8b6c9fab9b5ec6f2228
ms.sourcegitcommit: de600339b08951d6dd3933288a8da2327a4b6ef3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/13/2020
ms.locfileid: "48430454"
---
# <a name="advanced-hunting-service-limits"></a><span data-ttu-id="e4e2e-104">Limites de service de la chasse avancée</span><span class="sxs-lookup"><span data-stu-id="e4e2e-104">Advanced hunting service limits</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="e4e2e-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="e4e2e-105">**Applies to:**</span></span>
- <span data-ttu-id="e4e2e-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="e4e2e-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="e4e2e-107">Pour maintenir le service de façon efficace et réactive, la chasse avancée définit différentes limites pour les requêtes exécutées manuellement et par les [règles de détection personnalisées](custom-detection-rules.md).</span><span class="sxs-lookup"><span data-stu-id="e4e2e-107">To keep the service performant and responsive, advanced hunting sets various limits for queries run manually and by [custom detection rules](custom-detection-rules.md).</span></span> <span data-ttu-id="e4e2e-108">Reportez-vous au tableau suivant pour comprendre ces limites.</span><span class="sxs-lookup"><span data-stu-id="e4e2e-108">Refer to the following table to understand these limits.</span></span>

| <span data-ttu-id="e4e2e-109">Limite</span><span class="sxs-lookup"><span data-stu-id="e4e2e-109">Limit</span></span> | <span data-ttu-id="e4e2e-110">Size</span><span class="sxs-lookup"><span data-stu-id="e4e2e-110">Size</span></span> | <span data-ttu-id="e4e2e-111">Cycle d’actualisation</span><span class="sxs-lookup"><span data-stu-id="e4e2e-111">Refresh cycle</span></span> | <span data-ttu-id="e4e2e-112">Description</span><span class="sxs-lookup"><span data-stu-id="e4e2e-112">Description</span></span> |
|--|--|--|--|
| <span data-ttu-id="e4e2e-113">Plage de données</span><span class="sxs-lookup"><span data-stu-id="e4e2e-113">Data range</span></span> | <span data-ttu-id="e4e2e-114">30 jours</span><span class="sxs-lookup"><span data-stu-id="e4e2e-114">30 days</span></span> | <span data-ttu-id="e4e2e-115">Chaque requête</span><span class="sxs-lookup"><span data-stu-id="e4e2e-115">Every query</span></span> | <span data-ttu-id="e4e2e-116">Chaque requête peut rechercher des données depuis au cours des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="e4e2e-116">Each query can look up data from up to the past 30 days.</span></span> |
| <span data-ttu-id="e4e2e-117">Jeu de résultats</span><span class="sxs-lookup"><span data-stu-id="e4e2e-117">Result set</span></span> | <span data-ttu-id="e4e2e-118">10 000 lignes</span><span class="sxs-lookup"><span data-stu-id="e4e2e-118">10,000 rows</span></span> | <span data-ttu-id="e4e2e-119">Chaque requête</span><span class="sxs-lookup"><span data-stu-id="e4e2e-119">Every query</span></span> | <span data-ttu-id="e4e2e-120">Chaque requête peut renvoyer jusqu’à 10 000 enregistrements.</span><span class="sxs-lookup"><span data-stu-id="e4e2e-120">Each query can return up to 10,000 records.</span></span> |
| <span data-ttu-id="e4e2e-121">Timeout</span><span class="sxs-lookup"><span data-stu-id="e4e2e-121">Timeout</span></span> | <span data-ttu-id="e4e2e-122">10 minutes</span><span class="sxs-lookup"><span data-stu-id="e4e2e-122">10 minutes</span></span> | <span data-ttu-id="e4e2e-123">Chaque requête</span><span class="sxs-lookup"><span data-stu-id="e4e2e-123">Every query</span></span> | <span data-ttu-id="e4e2e-124">Chaque requête peut être exécutée pendant 10 minutes maximum.</span><span class="sxs-lookup"><span data-stu-id="e4e2e-124">Each query can run for up to 10 minutes.</span></span> <span data-ttu-id="e4e2e-125">Si elle ne se termine pas dans les 10 minutes, le service affiche une erreur.</span><span class="sxs-lookup"><span data-stu-id="e4e2e-125">If it does not complete within 10 minutes, the service displays an error.</span></span>
| <span data-ttu-id="e4e2e-126">Ressources du processeur</span><span class="sxs-lookup"><span data-stu-id="e4e2e-126">CPU resources</span></span> | <span data-ttu-id="e4e2e-127">En fonction de la taille du client</span><span class="sxs-lookup"><span data-stu-id="e4e2e-127">Based on tenant size</span></span> | <span data-ttu-id="e4e2e-128">-Sur l’heure, puis toutes les 15 minutes</span><span class="sxs-lookup"><span data-stu-id="e4e2e-128">- On the hour and then every 15 minutes</span></span><br><span data-ttu-id="e4e2e-129">-Tous les jours à 12 minuit</span><span class="sxs-lookup"><span data-stu-id="e4e2e-129">- Daily at 12 midnight</span></span> | <span data-ttu-id="e4e2e-130">Le service applique la limite quotidienne et la limite de 15 minutes séparément.</span><span class="sxs-lookup"><span data-stu-id="e4e2e-130">The service enforces the daily and the 15-minute limit separately.</span></span> <span data-ttu-id="e4e2e-131">Pour chaque limite, le [portail affiche une erreur](advanced-hunting-errors.md) chaque fois qu’une requête s’exécute et que le client a consommé plus de 10% des ressources allouées.</span><span class="sxs-lookup"><span data-stu-id="e4e2e-131">For each limit, the [portal displays an error](advanced-hunting-errors.md) whenever a query runs and the tenant has consumed over 10% of allocated resources.</span></span> <span data-ttu-id="e4e2e-132">Les requêtes sont bloquées si le client a atteint 100% jusqu’au prochain cycle quotidien ou 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="e4e2e-132">Queries are blocked if the tenant has reached 100% until after the next daily or 15-minute cycle.</span></span> |

>[!NOTE] 
><span data-ttu-id="e4e2e-133">Un ensemble distinct de limites s’applique aux requêtes de chasse avancée effectuées via l’API.</span><span class="sxs-lookup"><span data-stu-id="e4e2e-133">A separate set of limits apply to advanced hunting queries performed through the API.</span></span> [<span data-ttu-id="e4e2e-134">En savoir plus sur les API de chasse avancées</span><span class="sxs-lookup"><span data-stu-id="e4e2e-134">Read about advanced hunting APIs</span></span>](https://docs.microsoft.com/microsoft-365/security/mtp/api-advanced-hunting)

<span data-ttu-id="e4e2e-135">Les clients qui exécutent régulièrement plusieurs requêtes doivent suivre la consommation et [appliquer les meilleures pratiques en matière d’optimisation](advanced-hunting-best-practices.md) afin de minimiser la perturbation résultant du dépassement de ces limites.</span><span class="sxs-lookup"><span data-stu-id="e4e2e-135">Customers who run multiple queries regularly should track consumption and [apply optimization best practices](advanced-hunting-best-practices.md) to minimize disruption resulting from exceeding these limits.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4e2e-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4e2e-136">Related topics</span></span>

- [<span data-ttu-id="e4e2e-137">Meilleures pratiques pour la chasse avancée</span><span class="sxs-lookup"><span data-stu-id="e4e2e-137">Advanced hunting best practices</span></span>](advanced-hunting-best-practices.md)
- [<span data-ttu-id="e4e2e-138">Gérer les erreurs de chasse avancées</span><span class="sxs-lookup"><span data-stu-id="e4e2e-138">Handle advanced hunting errors</span></span>](advanced-hunting-errors.md)
- [<span data-ttu-id="e4e2e-139">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="e4e2e-139">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="e4e2e-140">Vue d’ensemble des détections personnalisées</span><span class="sxs-lookup"><span data-stu-id="e4e2e-140">Custom detections overview</span></span>](custom-detections-overview.md)
