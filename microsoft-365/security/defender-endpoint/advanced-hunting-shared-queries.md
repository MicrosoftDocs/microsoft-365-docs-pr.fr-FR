---
title: Utiliser des requêtes partagées dans un repérage avancé
description: Commencez immédiatement le repérage des menaces à l’aide de requêtes prédéfinies et partagées. Partagez vos requêtes au public ou au sein de votre organisation.
keywords: repérage avancé, repérage de menace, repérage de cybermenace, mdatp, microsoft defender atp, recherche wdatp, requête, télémétrie, détections personnalisées, schéma, kusto, référentiel github, mes requêtes, requêtes partagées
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
ms.openlocfilehash: 78a532167e4256e3453803f1a0b4a9e4875771cf
ms.sourcegitcommit: 582555d2b4ef5f2e2494ffdeab2c1d49e5d6b724
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51499423"
---
# <a name="use-shared-queries-in-advanced-hunting"></a><span data-ttu-id="1cc06-105">Utiliser des requêtes partagées dans un repérage avancé</span><span class="sxs-lookup"><span data-stu-id="1cc06-105">Use shared queries in advanced hunting</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="1cc06-106">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="1cc06-106">**Applies to:**</span></span>
- [<span data-ttu-id="1cc06-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="1cc06-107">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)

><span data-ttu-id="1cc06-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="1cc06-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="1cc06-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="1cc06-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-advancedhunting-abovefoldlink)

<span data-ttu-id="1cc06-110">Les requêtes de [repérage avancé](advanced-hunting-overview.md) peuvent être partagées entre les utilisateurs au sein de la même organisation.</span><span class="sxs-lookup"><span data-stu-id="1cc06-110">[Advanced hunting](advanced-hunting-overview.md) queries can be shared among users in the same organization.</span></span> <span data-ttu-id="1cc06-111">Vous pouvez également trouver des requêtes partagées publiquement sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="1cc06-111">You can also find queries shared publicly on GitHub.</span></span> <span data-ttu-id="1cc06-112">Ces requêtes vous permettent d’effectuer rapidement des scénarios de repérage de menace spécifiques sans avoir à créer des requêtes.</span><span class="sxs-lookup"><span data-stu-id="1cc06-112">These queries let you quickly pursue specific threat hunting scenarios without having to write queries from scratch.</span></span>

![Image des requêtes partagées](images/atp-advanced-hunting-shared-queries.png)

## <a name="save-modify-and-share-a-query"></a><span data-ttu-id="1cc06-114">Enregistrer, modifier et partager une requête</span><span class="sxs-lookup"><span data-stu-id="1cc06-114">Save, modify, and share a query</span></span>
<span data-ttu-id="1cc06-115">Vous pouvez enregistrer une requête nouvelle ou existante pour qu’elle soit uniquement accessible à vous-même ou partagée avec d’autres utilisateurs au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1cc06-115">You can save a new or existing query so that it is only accessible to you or shared with other users in your organization.</span></span>

1. <span data-ttu-id="1cc06-116">Tapez une nouvelle requête ou chargez une requête existante sous Requêtes **partagées** ou **Mes requêtes.**</span><span class="sxs-lookup"><span data-stu-id="1cc06-116">Type a new query or load an existing one from under **Shared queries** or **My queries**.</span></span>

2. <span data-ttu-id="1cc06-117">Sélectionnez **Enregistrer** ou **Enregistrer en tant que dans** les options d’enregistrer.</span><span class="sxs-lookup"><span data-stu-id="1cc06-117">Select **Save** or **Save as** from the save options.</span></span> <span data-ttu-id="1cc06-118">Pour éviter l’écriture d’une requête existante, choisissez **Enregistrer sous**.</span><span class="sxs-lookup"><span data-stu-id="1cc06-118">To avoid overwriting an existing query, choose **Save as**.</span></span>

3. <span data-ttu-id="1cc06-119">Entrez un nom pour la requête.</span><span class="sxs-lookup"><span data-stu-id="1cc06-119">Enter a name for the query.</span></span>

   ![Image de l’enregistrement d’une requête](images/advanced-hunting-save-query.png)

4. <span data-ttu-id="1cc06-121">Sélectionnez le dossier dans lequel vous voulez enregistrer la requête.</span><span class="sxs-lookup"><span data-stu-id="1cc06-121">Select the folder where you'd like to save the query.</span></span>
    - <span data-ttu-id="1cc06-122">**Requêtes partagées** : partagées avec tous les utilisateurs de votre organisation</span><span class="sxs-lookup"><span data-stu-id="1cc06-122">**Shared queries** — shared to all users in your organization</span></span>
    - <span data-ttu-id="1cc06-123">**Mes requêtes** : accessibles uniquement à vous</span><span class="sxs-lookup"><span data-stu-id="1cc06-123">**My queries** — accessible only to you</span></span>
    
5. <span data-ttu-id="1cc06-124">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="1cc06-124">Select **Save**.</span></span>

## <a name="delete-or-rename-a-query"></a><span data-ttu-id="1cc06-125">Supprimer ou renommer une requête</span><span class="sxs-lookup"><span data-stu-id="1cc06-125">Delete or rename a query</span></span>
1. <span data-ttu-id="1cc06-126">Cliquez avec le bouton droit de la souris sur une requête que vous voulez renommer ou supprimer.</span><span class="sxs-lookup"><span data-stu-id="1cc06-126">Right-click on a query you want to rename or delete.</span></span>

    ![Image de suppression de la requête](images/atp_advanced_hunting_delete_rename.png)

2. <span data-ttu-id="1cc06-128">Sélectionnez **Supprimer** et confirmer la suppression.</span><span class="sxs-lookup"><span data-stu-id="1cc06-128">Select **Delete** and confirm deletion.</span></span> <span data-ttu-id="1cc06-129">Ou sélectionnez **Renommer** et attribuer un nouveau nom à la requête.</span><span class="sxs-lookup"><span data-stu-id="1cc06-129">Or select **Rename** and provide a new name for the query.</span></span>

## <a name="create-a-direct-link-to-a-query"></a><span data-ttu-id="1cc06-130">Créer un lien direct vers une requête</span><span class="sxs-lookup"><span data-stu-id="1cc06-130">Create a direct link to a query</span></span>
<span data-ttu-id="1cc06-131">Pour générer un lien qui ouvre votre requête directement dans l’éditeur de requête de recherche avancée, finalisez votre requête et sélectionnez **Le lien partager.**</span><span class="sxs-lookup"><span data-stu-id="1cc06-131">To generate a link that opens your query directly in the advanced hunting query editor, finalize your query and select **Share link**.</span></span>

## <a name="access-queries-in-the-github-repository"></a><span data-ttu-id="1cc06-132">Accéder aux requêtes dans le référentiel GitHub</span><span class="sxs-lookup"><span data-stu-id="1cc06-132">Access queries in the GitHub repository</span></span>  
<span data-ttu-id="1cc06-133">Les chercheurs en matière de sécurité Microsoft partagent régulièrement des requêtes de repérage avancée dans un [référentiel public désigné sur GitHub](https://github.com/Microsoft/WindowsDefenderATP-Hunting-Queries).</span><span class="sxs-lookup"><span data-stu-id="1cc06-133">Microsoft security researchers regularly share advanced hunting queries in a [designated public repository on GitHub](https://github.com/Microsoft/WindowsDefenderATP-Hunting-Queries).</span></span> <span data-ttu-id="1cc06-134">Ce référentiel est ouvert aux contributions.</span><span class="sxs-lookup"><span data-stu-id="1cc06-134">This repository is open to contributions.</span></span> <span data-ttu-id="1cc06-135">Si vous souhaitez contribuer, [ veuillez rejoindre GitHub gratuitement](https://github.com/).</span><span class="sxs-lookup"><span data-stu-id="1cc06-135">To contribute, [join GitHub for free](https://github.com/).</span></span> 

>[!TIP]
><span data-ttu-id="1cc06-136">Les chercheurs en matière de sécurité Microsoft proposent également des requêtes de repérage avancé que vous pouvez utiliser pour localiser les activités et indicateurs associés aux menaces émergentes.</span><span class="sxs-lookup"><span data-stu-id="1cc06-136">Microsoft security researchers also provide advanced hunting queries that you can use to locate activities and indicators associated with emerging threats.</span></span> <span data-ttu-id="1cc06-137">Ces requêtes sont fournies dans le cadre du rapport de l’[analyse des menaces](threat-analytics.md) dans le Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="1cc06-137">These queries are provided as part of the [threat analytics](threat-analytics.md) reports in Microsoft Defender Security Center.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1cc06-138">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="1cc06-138">Related topics</span></span>
- [<span data-ttu-id="1cc06-139">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="1cc06-139">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="1cc06-140">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="1cc06-140">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="1cc06-141">Utiliser les résultats d’une requête</span><span class="sxs-lookup"><span data-stu-id="1cc06-141">Work with query results</span></span>](advanced-hunting-query-results.md)
- [<span data-ttu-id="1cc06-142">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="1cc06-142">Understand the schema</span></span>](advanced-hunting-schema-reference.md)
- [<span data-ttu-id="1cc06-143">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="1cc06-143">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
- [<span data-ttu-id="1cc06-144">Vue d’ensemble des détections personnalisées</span><span class="sxs-lookup"><span data-stu-id="1cc06-144">Custom detections overview</span></span>](overview-custom-detections.md)
