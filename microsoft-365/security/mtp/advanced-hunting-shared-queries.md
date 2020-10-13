---
title: Utiliser des requêtes partagées dans le repérage avancé de la Protection Microsoft contre les menaces
description: Commencez immédiatement le repérage des menaces à l’aide de requêtes prédéfinies et partagées. Partagez vos requêtes au public ou au sein de votre organisation.
keywords: chasse de menace, recherche de menace, recherche de menace informatique, protection contre les menaces Microsoft, Microsoft 365, MTP, M365, recherche, requête, télémétrie, détections personnalisées, schéma, Kusto, GitHub référentiel, mes requêtes, requêtes partagées
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
ms.openlocfilehash: 7cdb15be274c89bd92995b9e947489c62521c6bb
ms.sourcegitcommit: de600339b08951d6dd3933288a8da2327a4b6ef3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/13/2020
ms.locfileid: "48429682"
---
# <a name="use-shared-queries-in-advanced-hunting"></a><span data-ttu-id="82c1f-105">Utiliser des requêtes partagées dans un repérage avancé</span><span class="sxs-lookup"><span data-stu-id="82c1f-105">Use shared queries in advanced hunting</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="82c1f-106">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="82c1f-106">**Applies to:**</span></span>
- <span data-ttu-id="82c1f-107">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="82c1f-107">Microsoft Threat Protection</span></span>



<span data-ttu-id="82c1f-108">Les requêtes de [repérage avancé](advanced-hunting-overview.md) peuvent être partagées entre les utilisateurs au sein de la même organisation.</span><span class="sxs-lookup"><span data-stu-id="82c1f-108">[Advanced hunting](advanced-hunting-overview.md) queries can be shared among users in the same organization.</span></span> <span data-ttu-id="82c1f-109">Vous pouvez également trouver des requêtes partagées publiquement sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="82c1f-109">You can also find queries shared publicly on GitHub.</span></span> <span data-ttu-id="82c1f-110">Ces requêtes vous permettent d’effectuer rapidement des scénarios de repérage de menace spécifiques sans avoir à créer des requêtes.</span><span class="sxs-lookup"><span data-stu-id="82c1f-110">These queries let you quickly pursue specific threat hunting scenarios without having to write queries from scratch.</span></span>

![Image des requêtes partagées](../../media/advanced-hunting-shared-queries.png)

## <a name="save-modify-and-share-a-query"></a><span data-ttu-id="82c1f-112">Enregistrer, modifier et partager une requête</span><span class="sxs-lookup"><span data-stu-id="82c1f-112">Save, modify, and share a query</span></span>
<span data-ttu-id="82c1f-113">Vous pouvez enregistrer une requête nouvelle ou existante pour qu’elle soit uniquement accessible à vous-même ou partagée avec d’autres utilisateurs au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="82c1f-113">You can save a new or existing query so that it is only accessible to you or shared with other users in your organization.</span></span> 

1. <span data-ttu-id="82c1f-114">Création ou modification d’une requête.</span><span class="sxs-lookup"><span data-stu-id="82c1f-114">Create or modify a query.</span></span> 

2. <span data-ttu-id="82c1f-115">Cliquez sur le bouton déroulant **Enregistrer la requête**, puis sélectionnez **Enregistrer sous**.</span><span class="sxs-lookup"><span data-stu-id="82c1f-115">Click the **Save query** drop-down button and select **Save as**.</span></span>
    
3. <span data-ttu-id="82c1f-116">Entrez un nom pour la requête.</span><span class="sxs-lookup"><span data-stu-id="82c1f-116">Enter a name for the query.</span></span> 

   ![Image de l’enregistrement d’une requête](../../media/advanced-hunting-save-query.png)

4. <span data-ttu-id="82c1f-118">Sélectionnez le dossier dans lequel vous voulez enregistrer la requête.</span><span class="sxs-lookup"><span data-stu-id="82c1f-118">Select the folder where you'd like to save the query.</span></span>
    - <span data-ttu-id="82c1f-119">**Requêtes partagées** : partagées avec tous les utilisateurs de votre organisation</span><span class="sxs-lookup"><span data-stu-id="82c1f-119">**Shared queries** — shared to all users your organization</span></span>
    - <span data-ttu-id="82c1f-120">**Mes requêtes** : accessibles uniquement à vous</span><span class="sxs-lookup"><span data-stu-id="82c1f-120">**My queries** — accessible only to you</span></span>
    
5. <span data-ttu-id="82c1f-121">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="82c1f-121">Select **Save**.</span></span> 

## <a name="delete-or-rename-a-query"></a><span data-ttu-id="82c1f-122">Supprimer ou renommer une requête</span><span class="sxs-lookup"><span data-stu-id="82c1f-122">Delete or rename a query</span></span>
1. <span data-ttu-id="82c1f-123">Cliquez avec le bouton droit de la souris sur une requête que vous voulez renommer ou supprimer.</span><span class="sxs-lookup"><span data-stu-id="82c1f-123">Right-click on a query you want to rename or delete.</span></span>

    ![Image de suppression de la requête](../../media/advanced_hunting_delete_rename.png)

2. <span data-ttu-id="82c1f-125">Sélectionnez **Supprimer** et confirmer la suppression.</span><span class="sxs-lookup"><span data-stu-id="82c1f-125">Select **Delete** and confirm deletion.</span></span> <span data-ttu-id="82c1f-126">Ou sélectionnez **Renommer** et attribuer un nouveau nom à la requête.</span><span class="sxs-lookup"><span data-stu-id="82c1f-126">Or select **Rename** and provide a new name for the query.</span></span>

## <a name="create-a-direct-link-to-a-query"></a><span data-ttu-id="82c1f-127">Créer un lien direct vers une requête</span><span class="sxs-lookup"><span data-stu-id="82c1f-127">Create a direct link to a query</span></span>
<span data-ttu-id="82c1f-128">Pour générer un lien qui ouvre votre requête directement dans l’éditeur de requête de recherche avancée, finalisez votre requête et sélectionnez **partager le lien**.</span><span class="sxs-lookup"><span data-stu-id="82c1f-128">To generate a link that opens your query directly in the advanced hunting query editor, finalize your query and select **Share link**.</span></span>

## <a name="access-queries-in-the-github-repository"></a><span data-ttu-id="82c1f-129">Accéder aux requêtes dans le référentiel GitHub</span><span class="sxs-lookup"><span data-stu-id="82c1f-129">Access queries in the GitHub repository</span></span>  
<span data-ttu-id="82c1f-130">Les chercheurs en matière de sécurité Microsoft partagent régulièrement des requêtes de repérage avancée dans un [référentiel public désigné sur GitHub](https://aka.ms/hunting-queries).</span><span class="sxs-lookup"><span data-stu-id="82c1f-130">Microsoft security researchers regularly share advanced hunting queries in a [designated public repository on GitHub](https://aka.ms/hunting-queries).</span></span> <span data-ttu-id="82c1f-131">Ce référentiel est ouvert aux contributions.</span><span class="sxs-lookup"><span data-stu-id="82c1f-131">This repository is open to contributions.</span></span> <span data-ttu-id="82c1f-132">Si vous souhaitez contribuer, [ veuillez rejoindre GitHub gratuitement](https://github.com/).</span><span class="sxs-lookup"><span data-stu-id="82c1f-132">To contribute, [join GitHub for free](https://github.com/).</span></span>

>[!tip]
><span data-ttu-id="82c1f-133">Les chercheurs en matière de sécurité Microsoft proposent également des requêtes de repérage avancé que vous pouvez utiliser pour localiser les activités et indicateurs associés aux menaces émergentes.</span><span class="sxs-lookup"><span data-stu-id="82c1f-133">Microsoft security researchers also provide advanced hunting queries that you can use to locate activities and indicators associated with emerging threats.</span></span> <span data-ttu-id="82c1f-134">Ces requêtes sont fournies dans le cadre du rapport de l’[analyse des menaces](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/threat-analytics) dans le Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="82c1f-134">These queries are provided as part of the [threat analytics](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/threat-analytics) reports in Microsoft Defender Security Center.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82c1f-135">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="82c1f-135">Related topics</span></span>
- [<span data-ttu-id="82c1f-136">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="82c1f-136">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="82c1f-137">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="82c1f-137">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="82c1f-138">Travailler avec les résultats de la requête</span><span class="sxs-lookup"><span data-stu-id="82c1f-138">Work with query results</span></span>](advanced-hunting-query-results.md)
- [<span data-ttu-id="82c1f-139">Rechercher sur les appareils, les emails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="82c1f-139">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="82c1f-140">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="82c1f-140">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="82c1f-141">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="82c1f-141">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
