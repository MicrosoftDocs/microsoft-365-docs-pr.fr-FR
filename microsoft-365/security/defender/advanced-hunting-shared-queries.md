---
title: Utiliser des requêtes partagées dans Microsoft 365 de recherche avancée Defender
description: Commencez immédiatement le repérage des menaces à l’aide de requêtes prédéfinies et partagées. Partagez vos requêtes au public ou au sein de votre organisation.
keywords: repérage avancé, repérage de menace, repérage de cybermenace, Microsoft 365 Defender, microsoft 365, m365, recherche, requête, télémétrie, détections personnalisées, schéma, kusto, référentiel github, mes requêtes, requêtes partagées
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: maccruz
author: schmurky
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
ms.technology: m365d
ms.openlocfilehash: 83c78f9df5560c75e40a171d770e994b86049204
ms.sourcegitcommit: 7cc2be0244fcc30049351e35c25369cacaaf4ca9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "51952583"
---
# <a name="use-shared-queries-in-advanced-hunting"></a><span data-ttu-id="20a4f-105">Utiliser des requêtes partagées dans un repérage avancé</span><span class="sxs-lookup"><span data-stu-id="20a4f-105">Use shared queries in advanced hunting</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="20a4f-106">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="20a4f-106">**Applies to:**</span></span>
- <span data-ttu-id="20a4f-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="20a4f-107">Microsoft 365 Defender</span></span>
- <span data-ttu-id="20a4f-108">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="20a4f-108">Microsoft Defender for Endpoint</span></span>



<span data-ttu-id="20a4f-109">Les requêtes de [repérage avancé](advanced-hunting-overview.md) peuvent être partagées entre les utilisateurs au sein de la même organisation.</span><span class="sxs-lookup"><span data-stu-id="20a4f-109">[Advanced hunting](advanced-hunting-overview.md) queries can be shared among users in the same organization.</span></span> <span data-ttu-id="20a4f-110">Vous pouvez également trouver des requêtes partagées publiquement sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="20a4f-110">You can also find queries shared publicly on GitHub.</span></span> <span data-ttu-id="20a4f-111">Ces requêtes vous permettent d’effectuer rapidement des scénarios de repérage de menace spécifiques sans avoir à créer des requêtes.</span><span class="sxs-lookup"><span data-stu-id="20a4f-111">These queries let you quickly pursue specific threat hunting scenarios without having to write queries from scratch.</span></span>

![Image des requêtes partagées](../../media/advanced-hunting-shared-queries.png)

## <a name="save-modify-and-share-a-query"></a><span data-ttu-id="20a4f-113">Enregistrer, modifier et partager une requête</span><span class="sxs-lookup"><span data-stu-id="20a4f-113">Save, modify, and share a query</span></span>
<span data-ttu-id="20a4f-114">Vous pouvez enregistrer une requête nouvelle ou existante pour qu’elle soit uniquement accessible à vous-même ou partagée avec d’autres utilisateurs au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="20a4f-114">You can save a new or existing query so that it is only accessible to you or shared with other users in your organization.</span></span> 

1. <span data-ttu-id="20a4f-115">Création ou modification d’une requête.</span><span class="sxs-lookup"><span data-stu-id="20a4f-115">Create or modify a query.</span></span> 

2. <span data-ttu-id="20a4f-116">Cliquez sur le bouton déroulant **Enregistrer la requête**, puis sélectionnez **Enregistrer sous**.</span><span class="sxs-lookup"><span data-stu-id="20a4f-116">Click the **Save query** drop-down button and select **Save as**.</span></span>
    
3. <span data-ttu-id="20a4f-117">Entrez un nom pour la requête.</span><span class="sxs-lookup"><span data-stu-id="20a4f-117">Enter a name for the query.</span></span> 

   ![Image de l’enregistrement d’une requête](../../media/advanced-hunting-save-query.png)

4. <span data-ttu-id="20a4f-119">Sélectionnez le dossier dans lequel vous voulez enregistrer la requête.</span><span class="sxs-lookup"><span data-stu-id="20a4f-119">Select the folder where you'd like to save the query.</span></span>
    - <span data-ttu-id="20a4f-120">**Requêtes partagées** : partagées avec tous les utilisateurs de votre organisation</span><span class="sxs-lookup"><span data-stu-id="20a4f-120">**Shared queries** — shared to all users your organization</span></span>
    - <span data-ttu-id="20a4f-121">**Mes requêtes** : accessibles uniquement à vous</span><span class="sxs-lookup"><span data-stu-id="20a4f-121">**My queries** — accessible only to you</span></span>
    
5. <span data-ttu-id="20a4f-122">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="20a4f-122">Select **Save**.</span></span> 

## <a name="delete-or-rename-a-query"></a><span data-ttu-id="20a4f-123">Supprimer ou renommer une requête</span><span class="sxs-lookup"><span data-stu-id="20a4f-123">Delete or rename a query</span></span>
1. <span data-ttu-id="20a4f-124">Cliquez avec le bouton droit de la souris sur une requête que vous voulez renommer ou supprimer.</span><span class="sxs-lookup"><span data-stu-id="20a4f-124">Right-click on a query you want to rename or delete.</span></span>

    ![Image de suppression de la requête](../../media/advanced_hunting_delete_rename.png)

2. <span data-ttu-id="20a4f-126">Sélectionnez **Supprimer** et confirmer la suppression.</span><span class="sxs-lookup"><span data-stu-id="20a4f-126">Select **Delete** and confirm deletion.</span></span> <span data-ttu-id="20a4f-127">Ou sélectionnez **Renommer** et attribuer un nouveau nom à la requête.</span><span class="sxs-lookup"><span data-stu-id="20a4f-127">Or select **Rename** and provide a new name for the query.</span></span>

## <a name="create-a-direct-link-to-a-query"></a><span data-ttu-id="20a4f-128">Créer un lien direct vers une requête</span><span class="sxs-lookup"><span data-stu-id="20a4f-128">Create a direct link to a query</span></span>
<span data-ttu-id="20a4f-129">Pour générer un lien qui ouvre votre requête directement dans l’éditeur de requête de recherche avancée, finalisez votre requête et sélectionnez **Le lien partager.**</span><span class="sxs-lookup"><span data-stu-id="20a4f-129">To generate a link that opens your query directly in the advanced hunting query editor, finalize your query and select **Share link**.</span></span>

## <a name="access-queries-in-the-github-repository"></a><span data-ttu-id="20a4f-130">Accéder aux requêtes dans le référentiel GitHub</span><span class="sxs-lookup"><span data-stu-id="20a4f-130">Access queries in the GitHub repository</span></span>  
<span data-ttu-id="20a4f-131">Les chercheurs en matière de sécurité Microsoft partagent régulièrement des requêtes de repérage avancée dans un [référentiel public désigné sur GitHub](https://aka.ms/hunting-queries).</span><span class="sxs-lookup"><span data-stu-id="20a4f-131">Microsoft security researchers regularly share advanced hunting queries in a [designated public repository on GitHub](https://aka.ms/hunting-queries).</span></span> <span data-ttu-id="20a4f-132">Ce référentiel est ouvert aux contributions.</span><span class="sxs-lookup"><span data-stu-id="20a4f-132">This repository is open to contributions.</span></span> <span data-ttu-id="20a4f-133">Si vous souhaitez contribuer, [ veuillez rejoindre GitHub gratuitement](https://github.com/).</span><span class="sxs-lookup"><span data-stu-id="20a4f-133">To contribute, [join GitHub for free](https://github.com/).</span></span>

>[!tip]
><span data-ttu-id="20a4f-134">Les chercheurs en matière de sécurité Microsoft proposent également des requêtes de repérage avancé que vous pouvez utiliser pour localiser les activités et indicateurs associés aux menaces émergentes.</span><span class="sxs-lookup"><span data-stu-id="20a4f-134">Microsoft security researchers also provide advanced hunting queries that you can use to locate activities and indicators associated with emerging threats.</span></span> <span data-ttu-id="20a4f-135">Ces requêtes sont fournies dans le cadre du rapport de l’[analyse des menaces](/windows/security/threat-protection/microsoft-defender-atp/threat-analytics) dans le Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="20a4f-135">These queries are provided as part of the [threat analytics](/windows/security/threat-protection/microsoft-defender-atp/threat-analytics) reports in Microsoft Defender Security Center.</span></span>

>[!NOTE]
><span data-ttu-id="20a4f-136">Certains tableaux de cet article peuvent ne pas être disponibles dans Microsoft Defender pour Endpoint.</span><span class="sxs-lookup"><span data-stu-id="20a4f-136">Some tables in this article might not be available in Microsoft Defender for Endpoint.</span></span> <span data-ttu-id="20a4f-137">[Activer Microsoft 365 Defender pour qu’il](m365d-enable.md) recherche les menaces à l’aide de sources de données plus nombreuses.</span><span class="sxs-lookup"><span data-stu-id="20a4f-137">[Turn on Microsoft 365 Defender](m365d-enable.md) to hunt for threats using more data sources.</span></span> <span data-ttu-id="20a4f-138">Vous pouvez déplacer vos flux de travail de recherche avancée de Microsoft Defender pour point de terminaison vers Microsoft 365 Defender en suivant les étapes de la procédure de migration des requêtes de recherche avancée à partir de Microsoft Defender pour le point de [terminaison.](advanced-hunting-migrate-from-mde.md)</span><span class="sxs-lookup"><span data-stu-id="20a4f-138">You can move your advanced hunting workflows from Microsoft Defender for Endpoint to Microsoft 365 Defender by following the steps in [Migrate advanced hunting queries from Microsoft Defender for Endpoint](advanced-hunting-migrate-from-mde.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="20a4f-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20a4f-139">Related topics</span></span>
- [<span data-ttu-id="20a4f-140">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="20a4f-140">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="20a4f-141">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="20a4f-141">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="20a4f-142">Utiliser les résultats d’une requête</span><span class="sxs-lookup"><span data-stu-id="20a4f-142">Work with query results</span></span>](advanced-hunting-query-results.md)
- [<span data-ttu-id="20a4f-143">Repérer des menaces sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="20a4f-143">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="20a4f-144">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="20a4f-144">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="20a4f-145">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="20a4f-145">Apply query best practices</span></span>](advanced-hunting-best-practices.md)