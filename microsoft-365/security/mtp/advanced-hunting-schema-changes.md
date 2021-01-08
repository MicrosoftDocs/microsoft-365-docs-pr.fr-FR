---
title: Changements d’appellation dans le schéma de recherche avancée Microsoft 365 Defender
description: Suivre et passer en revue les tables et les colonnes des modifications d’attribution de noms dans le schéma de recherche avancé
keywords: advanced hunting, threat hunting, cyber threat hunting, microsoft threat protection, microsoft 365, mtp, m365, search, query, telemetry, schema reference, kusto, table, data, naming changes, rename, Microsoft Threat Protection
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
ms.openlocfilehash: 0bef5f4abcaf0d57af9c160ff31f859c2536ccd2
ms.sourcegitcommit: ec293978e951b09903b79e6642aa587824935e0c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "49780785"
---
# <a name="advanced-hunting-schema---naming-changes"></a><span data-ttu-id="012a1-104">Schéma de recherche avancé : modifications d’attribution de noms</span><span class="sxs-lookup"><span data-stu-id="012a1-104">Advanced hunting schema - Naming changes</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="012a1-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="012a1-105">**Applies to:**</span></span>
- <span data-ttu-id="012a1-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="012a1-106">Microsoft 365 Defender</span></span>

[!INCLUDE [Prerelease information](../includes/prerelease.md)]

<span data-ttu-id="012a1-107">Le [schéma de recherche avancée est mis à jour](advanced-hunting-schema-tables.md) régulièrement pour ajouter de nouvelles tables et colonnes.</span><span class="sxs-lookup"><span data-stu-id="012a1-107">The [advanced hunting schema](advanced-hunting-schema-tables.md) is updated regularly to add new tables and columns.</span></span> <span data-ttu-id="012a1-108">Dans certains cas, les noms des colonnes existantes sont renommés ou remplacés pour améliorer l’expérience utilisateur.</span><span class="sxs-lookup"><span data-stu-id="012a1-108">In some cases, existing columns names are renamed or replaced to improve the user experience.</span></span> <span data-ttu-id="012a1-109">Reportez-vous à cet article pour passer en revue les modifications d’attribution de noms qui peuvent avoir un impact sur vos requêtes.</span><span class="sxs-lookup"><span data-stu-id="012a1-109">Refer to this article to review naming changes that could impact your queries.</span></span>

<span data-ttu-id="012a1-110">Les modifications d’attribution de noms sont automatiquement appliquées aux requêtes enregistrées dans le centre de sécurité, y compris les requêtes utilisées par les règles de détection personnalisées.</span><span class="sxs-lookup"><span data-stu-id="012a1-110">Naming changes are automatically applied to queries that are saved in the security center, including queries used by custom detection rules.</span></span> <span data-ttu-id="012a1-111">Vous n’avez pas besoin de mettre à jour ces requêtes manuellement.</span><span class="sxs-lookup"><span data-stu-id="012a1-111">You don't need to update these queries manually.</span></span> <span data-ttu-id="012a1-112">Toutefois, vous devrez mettre à jour les requêtes suivantes :</span><span class="sxs-lookup"><span data-stu-id="012a1-112">However, you will need to update the following queries:</span></span>
- <span data-ttu-id="012a1-113">Requêtes qui sont exécutés à l’aide de l’API</span><span class="sxs-lookup"><span data-stu-id="012a1-113">Queries that are run using the API</span></span>
- <span data-ttu-id="012a1-114">Requêtes enregistrées ailleurs en dehors du centre de sécurité</span><span class="sxs-lookup"><span data-stu-id="012a1-114">Queries that are saved elsewhere outside the security center</span></span>

## <a name="december-2020"></a><span data-ttu-id="012a1-115">Décembre 2020</span><span class="sxs-lookup"><span data-stu-id="012a1-115">December 2020</span></span>

| <span data-ttu-id="012a1-116">Nom du tableau</span><span class="sxs-lookup"><span data-stu-id="012a1-116">Table name</span></span> | <span data-ttu-id="012a1-117">Nom de colonne d’origine</span><span class="sxs-lookup"><span data-stu-id="012a1-117">Original column name</span></span> | <span data-ttu-id="012a1-118">Nouveau nom de colonne</span><span class="sxs-lookup"><span data-stu-id="012a1-118">New column name</span></span> | <span data-ttu-id="012a1-119">Raison du changement</span><span class="sxs-lookup"><span data-stu-id="012a1-119">Reason for change</span></span>
|--|--|--|--|
| [<span data-ttu-id="012a1-120">EmailEvents</span><span class="sxs-lookup"><span data-stu-id="012a1-120">EmailEvents</span></span>](advanced-hunting-emailevents-table.md) | <span data-ttu-id="012a1-121">FinalEmailAction</span><span class="sxs-lookup"><span data-stu-id="012a1-121">FinalEmailAction</span></span> | <span data-ttu-id="012a1-122">EmailAction</span><span class="sxs-lookup"><span data-stu-id="012a1-122">EmailAction</span></span> | <span data-ttu-id="012a1-123">Commentaires des clients.</span><span class="sxs-lookup"><span data-stu-id="012a1-123">Customer feedback</span></span> |
| [<span data-ttu-id="012a1-124">EmailEvents</span><span class="sxs-lookup"><span data-stu-id="012a1-124">EmailEvents</span></span>](advanced-hunting-emailevents-table.md) | <span data-ttu-id="012a1-125">FinalEmailActionPolicy</span><span class="sxs-lookup"><span data-stu-id="012a1-125">FinalEmailActionPolicy</span></span> | <span data-ttu-id="012a1-126">EmailActionPolicy</span><span class="sxs-lookup"><span data-stu-id="012a1-126">EmailActionPolicy</span></span> | <span data-ttu-id="012a1-127">Commentaires des clients.</span><span class="sxs-lookup"><span data-stu-id="012a1-127">Customer feedback</span></span> |
| [<span data-ttu-id="012a1-128">EmailEvents</span><span class="sxs-lookup"><span data-stu-id="012a1-128">EmailEvents</span></span>](advanced-hunting-emailevents-table.md) | <span data-ttu-id="012a1-129">FinalEmailActionPolicyGuid</span><span class="sxs-lookup"><span data-stu-id="012a1-129">FinalEmailActionPolicyGuid</span></span> | <span data-ttu-id="012a1-130">EmailActionPolicyGuid</span><span class="sxs-lookup"><span data-stu-id="012a1-130">EmailActionPolicyGuid</span></span> | <span data-ttu-id="012a1-131">Commentaires des clients.</span><span class="sxs-lookup"><span data-stu-id="012a1-131">Customer feedback</span></span> |

## <a name="related-topics"></a><span data-ttu-id="012a1-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="012a1-132">Related topics</span></span>
- [<span data-ttu-id="012a1-133">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="012a1-133">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="012a1-134">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="012a1-134">Understand the schema</span></span>](advanced-hunting-schema-tables.md)