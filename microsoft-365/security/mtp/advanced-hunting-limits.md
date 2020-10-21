---
title: Quotas de chasse et paramètres d’utilisation avancés dans Microsoft Threat Protection
description: Comprendre les différents quotas et paramètres d’utilisation (limites de service) qui assurent la réactivité avancée du service de chasse
keywords: chasse aux menaces, recherche de menace, recherche de menace, protection contre les menaces Microsoft 365, MTP, M365, recherche, requête, télémétrie, schéma, Kusto, limite du processeur, limite de requête, ressources, résultats maximaux, quota, paramètres, allocation
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
ms.openlocfilehash: 192fb47aafdd20bd5e1f0774a64ec3215f1203d1
ms.sourcegitcommit: 628f195cbe3c00910f7350d8b09997a675dde989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2020
ms.locfileid: "48636904"
---
# <a name="advanced-hunting-quotas-and-usage-parameters"></a><span data-ttu-id="a36d6-104">Quotas de chasse et paramètres d’utilisation avancés</span><span class="sxs-lookup"><span data-stu-id="a36d6-104">Advanced hunting quotas and usage parameters</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="a36d6-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="a36d6-105">**Applies to:**</span></span>
- <span data-ttu-id="a36d6-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="a36d6-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="a36d6-107">Pour maintenir le service de manière efficace et réactive, la chasse avancée définit différents quotas et paramètres d’utilisation (également appelés « limites de service »).</span><span class="sxs-lookup"><span data-stu-id="a36d6-107">To keep the service performant and responsive, advanced hunting sets various quotas and usage parameters (also known as "service limits").</span></span> <span data-ttu-id="a36d6-108">Ces quotas et paramètres s’appliquent aux requêtes exécutées manuellement et par les [règles de détection personnalisées](custom-detection-rules.md).</span><span class="sxs-lookup"><span data-stu-id="a36d6-108">These quotas and parameters apply to queries run manually and by [custom detection rules](custom-detection-rules.md).</span></span> <span data-ttu-id="a36d6-109">Les clients qui exécutent régulièrement plusieurs requêtes doivent suivre la consommation et [appliquer les meilleures pratiques en matière d’optimisation](advanced-hunting-best-practices.md) afin de minimiser les interruptions.</span><span class="sxs-lookup"><span data-stu-id="a36d6-109">Customers who run multiple queries regularly should track consumption and [apply optimization best practices](advanced-hunting-best-practices.md) to minimize disruptions.</span></span>

<span data-ttu-id="a36d6-110">Reportez-vous au tableau suivant pour comprendre les quotas et les paramètres d’utilisation existants.</span><span class="sxs-lookup"><span data-stu-id="a36d6-110">Refer to the following table to understand existing quotas and usage parameters.</span></span>

| <span data-ttu-id="a36d6-111">Quota ou paramètre</span><span class="sxs-lookup"><span data-stu-id="a36d6-111">Quota or parameter</span></span> | <span data-ttu-id="a36d6-112">Size</span><span class="sxs-lookup"><span data-stu-id="a36d6-112">Size</span></span> | <span data-ttu-id="a36d6-113">Cycle d’actualisation</span><span class="sxs-lookup"><span data-stu-id="a36d6-113">Refresh cycle</span></span> | <span data-ttu-id="a36d6-114">Description</span><span class="sxs-lookup"><span data-stu-id="a36d6-114">Description</span></span> |
|--|--|--|--|
| <span data-ttu-id="a36d6-115">Plage de données</span><span class="sxs-lookup"><span data-stu-id="a36d6-115">Data range</span></span> | <span data-ttu-id="a36d6-116">30 jours</span><span class="sxs-lookup"><span data-stu-id="a36d6-116">30 days</span></span> | <span data-ttu-id="a36d6-117">Chaque requête</span><span class="sxs-lookup"><span data-stu-id="a36d6-117">Every query</span></span> | <span data-ttu-id="a36d6-118">Chaque requête peut rechercher des données depuis au cours des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="a36d6-118">Each query can look up data from up to the past 30 days.</span></span> |
| <span data-ttu-id="a36d6-119">Jeu de résultats</span><span class="sxs-lookup"><span data-stu-id="a36d6-119">Result set</span></span> | <span data-ttu-id="a36d6-120">10 000 lignes</span><span class="sxs-lookup"><span data-stu-id="a36d6-120">10,000 rows</span></span> | <span data-ttu-id="a36d6-121">Chaque requête</span><span class="sxs-lookup"><span data-stu-id="a36d6-121">Every query</span></span> | <span data-ttu-id="a36d6-122">Chaque requête peut renvoyer jusqu’à 10 000 enregistrements.</span><span class="sxs-lookup"><span data-stu-id="a36d6-122">Each query can return up to 10,000 records.</span></span> |
| <span data-ttu-id="a36d6-123">Timeout</span><span class="sxs-lookup"><span data-stu-id="a36d6-123">Timeout</span></span> | <span data-ttu-id="a36d6-124">10 minutes</span><span class="sxs-lookup"><span data-stu-id="a36d6-124">10 minutes</span></span> | <span data-ttu-id="a36d6-125">Chaque requête</span><span class="sxs-lookup"><span data-stu-id="a36d6-125">Every query</span></span> | <span data-ttu-id="a36d6-126">Chaque requête peut être exécutée pendant 10 minutes maximum.</span><span class="sxs-lookup"><span data-stu-id="a36d6-126">Each query can run for up to 10 minutes.</span></span> <span data-ttu-id="a36d6-127">Si elle ne se termine pas dans les 10 minutes, le service affiche une erreur.</span><span class="sxs-lookup"><span data-stu-id="a36d6-127">If it does not complete within 10 minutes, the service displays an error.</span></span>
| <span data-ttu-id="a36d6-128">Ressources du processeur</span><span class="sxs-lookup"><span data-stu-id="a36d6-128">CPU resources</span></span> | <span data-ttu-id="a36d6-129">En fonction de la taille du client</span><span class="sxs-lookup"><span data-stu-id="a36d6-129">Based on tenant size</span></span> | <span data-ttu-id="a36d6-130">-Sur l’heure, puis toutes les 15 minutes</span><span class="sxs-lookup"><span data-stu-id="a36d6-130">- On the hour and then every 15 minutes</span></span><br><span data-ttu-id="a36d6-131">-Tous les jours à 12 minuit</span><span class="sxs-lookup"><span data-stu-id="a36d6-131">- Daily at 12 midnight</span></span> | <span data-ttu-id="a36d6-132">Le service applique le quota quotidien et 15 minutes séparément.</span><span class="sxs-lookup"><span data-stu-id="a36d6-132">The service enforces the daily and the 15-minute quota separately.</span></span> <span data-ttu-id="a36d6-133">Pour chaque quota, le [portail affiche une erreur](advanced-hunting-errors.md) chaque fois qu’une requête s’exécute et que le client a consommé plus de 10% des ressources allouées.</span><span class="sxs-lookup"><span data-stu-id="a36d6-133">For each quota, the [portal displays an error](advanced-hunting-errors.md) whenever a query runs and the tenant has consumed over 10% of allocated resources.</span></span> <span data-ttu-id="a36d6-134">Les requêtes sont bloquées si le client a atteint 100% jusqu’au prochain cycle quotidien ou 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="a36d6-134">Queries are blocked if the tenant has reached 100% until after the next daily or 15-minute cycle.</span></span> |

>[!NOTE] 
><span data-ttu-id="a36d6-135">Un ensemble distinct de quotas et de paramètres s’applique aux requêtes de chasse avancée effectuées via l’API.</span><span class="sxs-lookup"><span data-stu-id="a36d6-135">A separate set of quotas and parameters apply to advanced hunting queries performed through the API.</span></span> [<span data-ttu-id="a36d6-136">En savoir plus sur les API de chasse avancées</span><span class="sxs-lookup"><span data-stu-id="a36d6-136">Read about advanced hunting APIs</span></span>](https://docs.microsoft.com/microsoft-365/security/mtp/api-advanced-hunting)

## <a name="related-topics"></a><span data-ttu-id="a36d6-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a36d6-137">Related topics</span></span>

- [<span data-ttu-id="a36d6-138">Meilleures pratiques pour la chasse avancée</span><span class="sxs-lookup"><span data-stu-id="a36d6-138">Advanced hunting best practices</span></span>](advanced-hunting-best-practices.md)
- [<span data-ttu-id="a36d6-139">Gérer les erreurs de chasse avancées</span><span class="sxs-lookup"><span data-stu-id="a36d6-139">Handle advanced hunting errors</span></span>](advanced-hunting-errors.md)
- [<span data-ttu-id="a36d6-140">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="a36d6-140">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="a36d6-141">Vue d’ensemble des détections personnalisées</span><span class="sxs-lookup"><span data-stu-id="a36d6-141">Custom detections overview</span></span>](custom-detections-overview.md)