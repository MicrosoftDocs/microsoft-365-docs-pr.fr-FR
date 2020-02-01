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
ms.collection: M365-security-compliance
ms.topic: article
ms.openlocfilehash: 6e5dd8d1d80d08ed808bc607fcc7aba8a390a9ca
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41600311"
---
# <a name="use-shared-queries-in-advanced-hunting"></a><span data-ttu-id="69b67-105">Utiliser des requêtes partagées dans un repérage avancé</span><span class="sxs-lookup"><span data-stu-id="69b67-105">Use shared queries in advanced hunting</span></span>

<span data-ttu-id="69b67-106">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="69b67-106">**Applies to:**</span></span>
- <span data-ttu-id="69b67-107">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="69b67-107">Microsoft Threat Protection</span></span>

[!INCLUDE [Prerelease information](../includes/prerelease.md)]

<span data-ttu-id="69b67-108">Les requêtes de [repérage avancé](advanced-hunting-overview.md) peuvent être partagées entre les utilisateurs au sein de la même organisation.</span><span class="sxs-lookup"><span data-stu-id="69b67-108">[Advanced hunting](advanced-hunting-overview.md) queries can be shared among users in the same organization.</span></span> <span data-ttu-id="69b67-109">Vous pouvez également trouver des requêtes partagées publiquement sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="69b67-109">You can also find queries shared publicly on GitHub.</span></span> <span data-ttu-id="69b67-110">Ces requêtes vous permettent d’effectuer rapidement des scénarios de repérage de menace spécifiques sans avoir à créer des requêtes.</span><span class="sxs-lookup"><span data-stu-id="69b67-110">These queries let you quickly pursue specific threat hunting scenarios without having to write queries from scratch.</span></span>

![Image des requêtes partagées](../images/advanced-hunting-shared-queries.png)

## <a name="save-modify-and-share-a-query"></a><span data-ttu-id="69b67-112">Enregistrer, modifier et partager une requête</span><span class="sxs-lookup"><span data-stu-id="69b67-112">Save, modify, and share a query</span></span>
<span data-ttu-id="69b67-113">Vous pouvez enregistrer une requête nouvelle ou existante pour qu’elle soit uniquement accessible à vous-même ou partagée avec d’autres utilisateurs au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="69b67-113">You can save a new or existing query so that it is only accessible to you or shared with other users in your organization.</span></span> 

1. <span data-ttu-id="69b67-114">Création ou modification d’une requête.</span><span class="sxs-lookup"><span data-stu-id="69b67-114">Create or modify a query.</span></span> 

2. <span data-ttu-id="69b67-115">Cliquez sur le bouton déroulant **Enregistrer la requête**, puis sélectionnez **Enregistrer sous**.</span><span class="sxs-lookup"><span data-stu-id="69b67-115">Click the **Save query** drop-down button and select **Save as**.</span></span>
    
3. <span data-ttu-id="69b67-116">Entrez un nom pour la requête.</span><span class="sxs-lookup"><span data-stu-id="69b67-116">Enter a name for the query.</span></span> 

   ![Image de l’enregistrement d’une requête](../images/advanced-hunting-save-query.png)

4. <span data-ttu-id="69b67-118">Sélectionnez le dossier dans lequel vous voulez enregistrer la requête.</span><span class="sxs-lookup"><span data-stu-id="69b67-118">Select the folder where you'd like to save the query.</span></span>
    - <span data-ttu-id="69b67-119">**Requêtes partagées** : partagées avec tous les utilisateurs de votre organisation</span><span class="sxs-lookup"><span data-stu-id="69b67-119">**Shared queries** — shared to all users your organization</span></span>
    - <span data-ttu-id="69b67-120">**Mes requêtes** : accessibles uniquement à vous</span><span class="sxs-lookup"><span data-stu-id="69b67-120">**My queries** — accessible only to you</span></span>
    
5. <span data-ttu-id="69b67-121">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="69b67-121">Select **Save**.</span></span> 

## <a name="delete-or-rename-a-query"></a><span data-ttu-id="69b67-122">Supprimer ou renommer une requête</span><span class="sxs-lookup"><span data-stu-id="69b67-122">Delete or rename a query</span></span>
1. <span data-ttu-id="69b67-123">Cliquez avec le bouton droit de la souris sur une requête que vous voulez renommer ou supprimer.</span><span class="sxs-lookup"><span data-stu-id="69b67-123">Right-click on a query you want to rename or delete.</span></span>

    ![Image de suppression de la requête](../images/advanced_hunting_delete_rename.png)

2. <span data-ttu-id="69b67-125">Sélectionnez **Supprimer** et confirmer la suppression.</span><span class="sxs-lookup"><span data-stu-id="69b67-125">Select **Delete** and confirm deletion.</span></span> <span data-ttu-id="69b67-126">Ou sélectionnez **Renommer** et attribuer un nouveau nom à la requête.</span><span class="sxs-lookup"><span data-stu-id="69b67-126">Or select **Rename** and provide a new name for the query.</span></span>

## <a name="access-queries-in-the-github-repository"></a><span data-ttu-id="69b67-127">Accéder aux requêtes dans le référentiel GitHub</span><span class="sxs-lookup"><span data-stu-id="69b67-127">Access queries in the GitHub repository</span></span>  
<span data-ttu-id="69b67-128">Les chercheurs en matière de sécurité Microsoft partagent régulièrement des requêtes de repérage avancée dans un [référentiel public désigné sur GitHub](https://github.com/microsoft/MTP-AHQ).</span><span class="sxs-lookup"><span data-stu-id="69b67-128">Microsoft security researchers regularly share advanced hunting queries in a [designated public repository on GitHub](https://github.com/microsoft/MTP-AHQ).</span></span> <span data-ttu-id="69b67-129">Ce référentiel est ouvert aux contributions.</span><span class="sxs-lookup"><span data-stu-id="69b67-129">This repository is open to contributions.</span></span> <span data-ttu-id="69b67-130">Si vous souhaitez contribuer, [ veuillez rejoindre GitHub gratuitement](https://github.com/).</span><span class="sxs-lookup"><span data-stu-id="69b67-130">To contribute, [join GitHub for free](https://github.com/).</span></span>

>[!tip]
><span data-ttu-id="69b67-131">Les chercheurs en matière de sécurité Microsoft proposent également des requêtes de repérage avancé que vous pouvez utiliser pour localiser les activités et indicateurs associés aux menaces émergentes.</span><span class="sxs-lookup"><span data-stu-id="69b67-131">Microsoft security researchers also provide advanced hunting queries that you can use to locate activities and indicators associated with emerging threats.</span></span> <span data-ttu-id="69b67-132">Ces requêtes sont fournies dans le cadre du rapport de l’[analyse des menaces](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/threat-analytics) dans le Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="69b67-132">These queries are provided as part of the [threat analytics](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/threat-analytics) reports in Microsoft Defender Security Center.</span></span>

## <a name="related-topics"></a><span data-ttu-id="69b67-133">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="69b67-133">Related topics</span></span>
- [<span data-ttu-id="69b67-134">Repérage proactif des menaces</span><span class="sxs-lookup"><span data-stu-id="69b67-134">Proactively hunt for threats</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="69b67-135">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="69b67-135">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="69b67-136">Repérer les menaces sur divers appareils et e-mails</span><span class="sxs-lookup"><span data-stu-id="69b67-136">Hunt for threats across devices and emails</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="69b67-137">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="69b67-137">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="69b67-138">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="69b67-138">Apply query best practices</span></span>](advanced-hunting-best-practices.md)