---
title: Vue d’ensemble du repérage avancé dans la Protection Microsoft contre les menaces
description: En savoir plus sur les requêtes de repérage avancés dans Microsoft 365 et leur utilisation pour rechercher de manière proactive les menaces et faiblesses de votre réseau
keywords: chasse de menace, recherche de menace, recherche de menace informatique, protection contre les menaces Microsoft, Microsoft 365, MTP, M365, recherche, requête, télémétrie, détections personnalisées, schéma, Kusto, Microsoft 365, protection contre les menaces Microsoft
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
ms.openlocfilehash: 598ef669e95081ef098dfa9cfdb5473b21b28306
ms.sourcegitcommit: 74bf600424d0cb7b9d16b4f391aeda7875058be1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42234753"
---
# <a name="proactively-hunt-for-threats-with-advanced-hunting-in-microsoft-threat-protection"></a><span data-ttu-id="cffce-104">Repérage proactive de menaces avec repérage avancé dans la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="cffce-104">Proactively hunt for threats with advanced hunting in Microsoft Threat Protection</span></span>

<span data-ttu-id="cffce-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="cffce-105">**Applies to:**</span></span>
- <span data-ttu-id="cffce-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="cffce-106">Microsoft Threat Protection</span></span>



<span data-ttu-id="cffce-107">Le repérage avancé est un outil de repérage de menaces basé sur des requêtes qui vous permet d’explorer jusqu’à 30 jours de données brutes.</span><span class="sxs-lookup"><span data-stu-id="cffce-107">Advanced hunting is a query-based threat-hunting tool that lets you explore up to 30 days of raw data.</span></span> <span data-ttu-id="cffce-108">Vous pouvez inspecter de manière proactive les événements de votre réseau pour localiser les indicateurs et entités intéressants.</span><span class="sxs-lookup"><span data-stu-id="cffce-108">You can proactively inspect events in your network to locate interesting indicators and entities.</span></span> <span data-ttu-id="cffce-109">L’accès flexible aux données facilite le repérage sans contrainte pour les menaces connues et potentielles.</span><span class="sxs-lookup"><span data-stu-id="cffce-109">The flexible access to data facilitates unconstrained hunting for both known and potential threats.</span></span>

<span data-ttu-id="cffce-110">Dans le centre de sécurité Microsoft 365, la recherche avancée prend en charge les requêtes qui examinent les données issues de Microsoft Defender ATP, qui couvrent les données des appareils intégrés et Office 365 ATP, qui fournissent des données à partir de courriers électroniques.</span><span class="sxs-lookup"><span data-stu-id="cffce-110">In the Microsoft 365 security center, advanced hunting supports queries that look into data from both Microsoft Defender ATP, covering data from onboarded devices, and Office 365 ATP, providing data from emails.</span></span> <span data-ttu-id="cffce-111">Pour utiliser le repérage avancé, [activez Protection Microsoft contre les menaces](mtp-enable.md).</span><span class="sxs-lookup"><span data-stu-id="cffce-111">To use advanced hunting, [turn on Microsoft Threat Protection](mtp-enable.md).</span></span>

## <a name="get-started-with-advanced-hunting"></a><span data-ttu-id="cffce-112">Prise en main du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="cffce-112">Get started with advanced hunting</span></span>

<span data-ttu-id="cffce-113">Nous vous recommandons de suivre plusieurs étapes pour devenir rapidement opérationnel avec le repérage avancé.</span><span class="sxs-lookup"><span data-stu-id="cffce-113">We recommend going through several steps to quickly get up and running with advanced hunting.</span></span>

| <span data-ttu-id="cffce-114">Objectif d’apprentissage</span><span class="sxs-lookup"><span data-stu-id="cffce-114">Learning goal</span></span> | <span data-ttu-id="cffce-115">Description</span><span class="sxs-lookup"><span data-stu-id="cffce-115">Description</span></span> | <span data-ttu-id="cffce-116">Ressource</span><span class="sxs-lookup"><span data-stu-id="cffce-116">Resource</span></span> |
|--|--|--|
| <span data-ttu-id="cffce-117">**Prise en main du langage**</span><span class="sxs-lookup"><span data-stu-id="cffce-117">**Get a feel for the language**</span></span> | <span data-ttu-id="cffce-118">La fonction de repérage avancé est basée sur le [langage de requête Kusto](https://docs.microsoft.com/azure/kusto/query/), prenant en charge les mêmes syntaxe et opérateurs.</span><span class="sxs-lookup"><span data-stu-id="cffce-118">Advanced hunting is based on the [Kusto query language](https://docs.microsoft.com/azure/kusto/query/), supporting the same syntax and operators.</span></span> <span data-ttu-id="cffce-119">Commencez à découvrir le langage de requête en exécutant votre première requête.</span><span class="sxs-lookup"><span data-stu-id="cffce-119">Start learning the query language by running your first query.</span></span> | [<span data-ttu-id="cffce-120">Vue d'ensemble du language de requête</span><span class="sxs-lookup"><span data-stu-id="cffce-120">Query language overview</span></span>](advanced-hunting-query-language.md) |
| <span data-ttu-id="cffce-121">**Comprendre le schéma**</span><span class="sxs-lookup"><span data-stu-id="cffce-121">**Understand the schema**</span></span> | <span data-ttu-id="cffce-122">Obtenez une compréhension optimale des tableaux du schéma et de leurs colonnes.</span><span class="sxs-lookup"><span data-stu-id="cffce-122">Get a good, high-level understanding of the tables in the schema and their columns.</span></span> <span data-ttu-id="cffce-123">Cela vous permet de déterminer où rechercher des données et comment construire vos requêtes.</span><span class="sxs-lookup"><span data-stu-id="cffce-123">This will help you determine where to look for data and how to construct your queries.</span></span> | [<span data-ttu-id="cffce-124">Référence de schéma</span><span class="sxs-lookup"><span data-stu-id="cffce-124">Schema reference</span></span>](advanced-hunting-schema-tables.md) |
| <span data-ttu-id="cffce-125">**Utiliser des requêtes prédéfinies**</span><span class="sxs-lookup"><span data-stu-id="cffce-125">**Use predefined queries**</span></span> | <span data-ttu-id="cffce-126">Explorez les collections de requêtes prédéfinies couvrant différents scénarios de repérage de menaces.</span><span class="sxs-lookup"><span data-stu-id="cffce-126">Explore collections of predefined queries covering different threat hunting scenarios.</span></span> | [<span data-ttu-id="cffce-127">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="cffce-127">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
| <span data-ttu-id="cffce-128">**Optimiser les requêtes**</span><span class="sxs-lookup"><span data-stu-id="cffce-128">**Optimize queries**</span></span> | <span data-ttu-id="cffce-129">Découvrez comment créer des requêtes et des requêtes efficaces qui combinent des données provenant des e-mails et d’appareils.</span><span class="sxs-lookup"><span data-stu-id="cffce-129">Understand how to create efficient queries and queries that combine data from emails and devices.</span></span> | <span data-ttu-id="cffce-130">[Meilleures pratiques en matière de](advanced-hunting-shared-queries.md), [repérage sur différents appareils et e-mails](advanced-hunting-best-practices.md)</span><span class="sxs-lookup"><span data-stu-id="cffce-130">[Query best practices](advanced-hunting-shared-queries.md), [Hunt across devices and emails](advanced-hunting-best-practices.md)</span></span>

## <a name="get-help-as-you-write-queries"></a><span data-ttu-id="cffce-131">Obtenez de l’aide lorsque vous rédigez des requêtes</span><span class="sxs-lookup"><span data-stu-id="cffce-131">Get help as you write queries</span></span>
<span data-ttu-id="cffce-132">Tirez parti des fonctionnalités suivantes pour rédiger des requêtes plus rapidement :</span><span class="sxs-lookup"><span data-stu-id="cffce-132">Take advantage of the following functionality to write queries faster:</span></span>
- <span data-ttu-id="cffce-133">**Suggérer automatiquement** : lorsque vous rédigez des requêtes, la recherche avancée fournit des suggestions.</span><span class="sxs-lookup"><span data-stu-id="cffce-133">**Autosuggest** — as you write queries, advanced hunting provides suggestions.</span></span> 
- <span data-ttu-id="cffce-134">**Référence de schéma** : une référence de schéma qui inclut la liste des tableaux et leurs colonnes est fournie à côté de votre espace de travail.</span><span class="sxs-lookup"><span data-stu-id="cffce-134">**Schema reference** — a schema reference that includes the list of tables and their columns is provided next to your working area.</span></span> <span data-ttu-id="cffce-135">Si vous souhaitez en savoir plus, veuillez placer le pointeur sur un élément.</span><span class="sxs-lookup"><span data-stu-id="cffce-135">For more information, hover over an item.</span></span> <span data-ttu-id="cffce-136">Double-cliquez sur un élément pour l’insérer dans l’éditeur de requête.</span><span class="sxs-lookup"><span data-stu-id="cffce-136">Double-click an item to insert it to the query editor.</span></span>

## <a name="drilldown-from-query-results"></a><span data-ttu-id="cffce-137">Détails des résultats de la requête</span><span class="sxs-lookup"><span data-stu-id="cffce-137">Drilldown from query results</span></span>
<span data-ttu-id="cffce-138">Pour afficher plus d’informations sur les entités, telles que des ordinateurs, fichiers, utilisateurs, adresses IP et URL, dans les résultats de votre requête, cliquez simplement sur l’identificateur d’entité.</span><span class="sxs-lookup"><span data-stu-id="cffce-138">To view more information about entities, such as machines, files, users, IP addresses, and URLs, in your query results, simply click the entity identifier.</span></span> <span data-ttu-id="cffce-139">Une page de profil détaillée s’ouvre pour l’entité sélectionnée dans le Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="cffce-139">This opens a detailed profile page for the selected entity in Microsoft Defender Security Center.</span></span>

## <a name="tweak-your-queries-from-the-results"></a><span data-ttu-id="cffce-140">Adaptez vos requêtes à partir des résultats</span><span class="sxs-lookup"><span data-stu-id="cffce-140">Tweak your queries from the results</span></span>
<span data-ttu-id="cffce-141">Cliquez avec le bouton droit de la souris sur une valeur du jeu de résultats pour améliorer rapidement votre requête.</span><span class="sxs-lookup"><span data-stu-id="cffce-141">Right-click a value in the result set to quickly enhance your query.</span></span> <span data-ttu-id="cffce-142">Vous pouvez utiliser les options suivantes pour :</span><span class="sxs-lookup"><span data-stu-id="cffce-142">You can use the options to:</span></span>

- <span data-ttu-id="cffce-143">Rechercher explicitement la valeur sélectionnée (`==`)</span><span class="sxs-lookup"><span data-stu-id="cffce-143">Explicitly look for the selected value (`==`)</span></span>
- <span data-ttu-id="cffce-144">Exclure la valeur sélectionnée de la requête (`!=`)</span><span class="sxs-lookup"><span data-stu-id="cffce-144">Exclude the selected value from the query (`!=`)</span></span>
- <span data-ttu-id="cffce-145">Obtenez des opérateurs plus avancés pour ajouter la valeur à votre requête (par exemple, `contains`, `starts with` et `ends with`)</span><span class="sxs-lookup"><span data-stu-id="cffce-145">Get more advanced operators for adding the value to your query, such as `contains`, `starts with` and `ends with`</span></span> 

![Image du jeu de résultats de repérage avancé Microsoft Defender - Protection avancée contre les menaces](../../media/advanced-hunting-results-filter.png)

## <a name="filter-the-query-results"></a><span data-ttu-id="cffce-147">Filtrer les résultats de la requête</span><span class="sxs-lookup"><span data-stu-id="cffce-147">Filter the query results</span></span>
<span data-ttu-id="cffce-148">Les filtres de droite fournissent un résumé du jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="cffce-148">The filters displayed to the right provide a summary of the result set.</span></span> <span data-ttu-id="cffce-149">Chaque colonne possède sa propre section qui répertorie les valeurs distinctes trouvées pour cette colonne et le nombre d’instances.</span><span class="sxs-lookup"><span data-stu-id="cffce-149">Each column has its own section that lists the distinct values found for that column and the number of instances.</span></span>

<span data-ttu-id="cffce-150">Affinez votre requête en sélectionnant les boutons « + » ou « - » sur les valeurs que vous voulez inclure ou exclure, puis sélectionnez **exécuter la requête**.</span><span class="sxs-lookup"><span data-stu-id="cffce-150">Refine your query by selecting the "+" or "-" buttons on the values that you want to include or exclude and then selecting **Run query**.</span></span>

![Image du filtre de repérage avancé](../../media/advanced-hunting-filter.png)

<span data-ttu-id="cffce-152">Une fois le filtre appliqué pour modifier la requête, puis exécuter la requête, les résultats sont mis à jour en conséquence.</span><span class="sxs-lookup"><span data-stu-id="cffce-152">Once you apply the filter to modify the query and then run the query, the results are updated accordingly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cffce-153">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="cffce-153">Related topics</span></span>
- [<span data-ttu-id="cffce-154">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="cffce-154">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="cffce-155">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="cffce-155">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="cffce-156">Repérer les menaces sur divers appareils et e-mails</span><span class="sxs-lookup"><span data-stu-id="cffce-156">Hunt for threats across devices and emails</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="cffce-157">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="cffce-157">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="cffce-158">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="cffce-158">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
