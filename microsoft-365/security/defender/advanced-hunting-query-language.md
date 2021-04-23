---
title: Découvrir le langage de requête de recherche avancée dans Microsoft 365 Defender
description: Créez votre première requête de repérage de menace et découvrez les opérateurs communs et les autres aspects du langage de requête de repérage avancé
keywords: repérage avancé, repérage de menace, repérage de cybermenace, Microsoft 365 Defender, microsoft 365, m365, recherche, requête, langue, apprendre, première requête, télémétrie, événements, télémétrie, détections personnalisées, schéma, kusto, opérateurs, types de données, téléchargement PowerShell, exemple de requête
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
ms.openlocfilehash: 14287fb6dea9dda8accb580246b383f0427c3b3f
ms.sourcegitcommit: 7cc2be0244fcc30049351e35c25369cacaaf4ca9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "51952619"
---
# <a name="learn-the-advanced-hunting-query-language"></a><span data-ttu-id="1d5dd-104">Découvrir le langage de requête de repérage avancé</span><span class="sxs-lookup"><span data-stu-id="1d5dd-104">Learn the advanced hunting query language</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="1d5dd-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="1d5dd-105">**Applies to:**</span></span>
- <span data-ttu-id="1d5dd-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="1d5dd-106">Microsoft 365 Defender</span></span>
- <span data-ttu-id="1d5dd-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="1d5dd-107">Microsoft Defender for Endpoint</span></span>

<span data-ttu-id="1d5dd-108">Le repérage avancé est basé sur le [langage de requête Kusto](/azure/kusto/query/).</span><span class="sxs-lookup"><span data-stu-id="1d5dd-108">Advanced hunting is based on the [Kusto query language](/azure/kusto/query/).</span></span> <span data-ttu-id="1d5dd-109">Vous pouvez utiliser des opérateurs et des instructions Kusto pour créer des requêtes qui recherchent des informations dans un [schéma spécialisé.](advanced-hunting-schema-tables.md)</span><span class="sxs-lookup"><span data-stu-id="1d5dd-109">You can use Kusto operators and statements to construct queries that locate information in a specialized [schema](advanced-hunting-schema-tables.md).</span></span> <span data-ttu-id="1d5dd-110">Pour mieux comprendre ces concepts, exécutez votre première requête.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-110">To understand these concepts better, run your first query.</span></span>

## <a name="try-your-first-query"></a><span data-ttu-id="1d5dd-111">Essayez votre première requête</span><span class="sxs-lookup"><span data-stu-id="1d5dd-111">Try your first query</span></span>

<span data-ttu-id="1d5dd-112">Dans le Centre de sécurité Microsoft 365, go to **Hunting** to run your first query.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-112">In Microsoft 365 security center, go to **Hunting** to run your first query.</span></span> <span data-ttu-id="1d5dd-113">Consultez l’exemple qui suit :</span><span class="sxs-lookup"><span data-stu-id="1d5dd-113">Use the following example:</span></span>

```kusto
// Finds PowerShell execution events that could involve a download
union DeviceProcessEvents, DeviceNetworkEvents
| where Timestamp > ago(7d)
// Pivoting on PowerShell processes
| where FileName in~ ("powershell.exe", "powershell_ise.exe")
// Suspicious commands
| where ProcessCommandLine has_any("WebClient",
 "DownloadFile",
 "DownloadData",
 "DownloadString",
"WebRequest",
"Shellcode",
"http",
"https")
| project Timestamp, DeviceName, InitiatingProcessFileName, InitiatingProcessCommandLine, 
FileName, ProcessCommandLine, RemoteIP, RemoteUrl, RemotePort, RemoteIPType
| top 100 by Timestamp
```

<span data-ttu-id="1d5dd-114">**[Exécuter cette requête dans un recherche avancée](https://security.microsoft.com/hunting?query=H4sIAAAAAAAEAI2TW0sCURSF93PQfxh8Moisp956yYIgQtLoMaYczJpbzkkTpN_et_dcdPQkcpjbmrXXWftyetKTQG5lKqmMpeB9IJksJJKZDOWdZ8wKeP5wvcm3OLgZbMXmXCmIxjnYIfcAVgYvRi8w3TnfsXEDGAG47pCCZXyP5ViO4KeNbt-Up-hEuJmB6lvButnY8XSL-cDl0M2I-GwxVX8Fe2H5zMzHiKjEVB0eEsnBrszfBIWuXOLrxCJ7VqEBfM3DWUYTkNKrv1p5y3X0jwetemzOQ_NSVuuXZ1c6aNTKRaN8VvWhY9n7OS-o6J5r7mYeQypdEKc1m1qfiqpjCSuspsDntt2J61bEvTlXls5AgQfFl5bHM_gr_BhO2RF1rztoBv2tWahrso_TtzkL93KGMGZVr2pe7eWR-xeZl91f_113UOsx3nDR4Y9j5R6kaCq8ajr_YWfFeedsd27L7it-Z6dAZyxsJq1d9-2ZOSzK3y2NVd8-zUPjtZaJnYsIH4Md7AmdeAcd2Cl1XoURc5PzXlfU8U9P54WcswL6t_TW9Q__qX-xygQAAA&runQuery=true&timeRangeId=week)**</span><span class="sxs-lookup"><span data-stu-id="1d5dd-114">**[Run this query in advanced hunting](https://security.microsoft.com/hunting?query=H4sIAAAAAAAEAI2TW0sCURSF93PQfxh8Moisp956yYIgQtLoMaYczJpbzkkTpN_et_dcdPQkcpjbmrXXWftyetKTQG5lKqmMpeB9IJksJJKZDOWdZ8wKeP5wvcm3OLgZbMXmXCmIxjnYIfcAVgYvRi8w3TnfsXEDGAG47pCCZXyP5ViO4KeNbt-Up-hEuJmB6lvButnY8XSL-cDl0M2I-GwxVX8Fe2H5zMzHiKjEVB0eEsnBrszfBIWuXOLrxCJ7VqEBfM3DWUYTkNKrv1p5y3X0jwetemzOQ_NSVuuXZ1c6aNTKRaN8VvWhY9n7OS-o6J5r7mYeQypdEKc1m1qfiqpjCSuspsDntt2J61bEvTlXls5AgQfFl5bHM_gr_BhO2RF1rztoBv2tWahrso_TtzkL93KGMGZVr2pe7eWR-xeZl91f_113UOsx3nDR4Y9j5R6kaCq8ajr_YWfFeedsd27L7it-Z6dAZyxsJq1d9-2ZOSzK3y2NVd8-zUPjtZaJnYsIH4Md7AmdeAcd2Cl1XoURc5PzXlfU8U9P54WcswL6t_TW9Q__qX-xygQAAA&runQuery=true&timeRangeId=week)**</span></span>

### <a name="describe-the-query-and-specify-the-tables-to-search"></a><span data-ttu-id="1d5dd-115">Décrire la requête et spécifier les tables à rechercher</span><span class="sxs-lookup"><span data-stu-id="1d5dd-115">Describe the query and specify the tables to search</span></span>
<span data-ttu-id="1d5dd-116">Un commentaire court a été ajouté au début de la requête pour décrire son objectif.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-116">A short comment has been added to the beginning of the query to describe what it is for.</span></span> <span data-ttu-id="1d5dd-117">Ce commentaire est utile si vous décidez ultérieurement d'enregistrer la requête et de la partager avec d'autres membres de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-117">This comment helps if you later decide to save the query and share it with others in your organization.</span></span> 

```kusto
// Finds PowerShell execution events that could involve a download
```

<span data-ttu-id="1d5dd-118">La requête elle-même commence généralement par un nom de table suivi de plusieurs éléments qui commencent par un canal ( `|` ).</span><span class="sxs-lookup"><span data-stu-id="1d5dd-118">The query itself will typically start with a table name followed by several elements that start with a pipe (`|`).</span></span> <span data-ttu-id="1d5dd-119">Dans cet exemple, nous commençons par créer une union de deux tables et, si nécessaire, nous ajoutons des  `DeviceProcessEvents` `DeviceNetworkEvents` éléments canalés.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-119">In this example, we start by creating a union of two tables,  `DeviceProcessEvents` and `DeviceNetworkEvents`, and add piped elements as needed.</span></span>

```kusto
union DeviceProcessEvents, DeviceNetworkEvents
```
### <a name="set-the-time-range"></a><span data-ttu-id="1d5dd-120">Définir la plage de temps</span><span class="sxs-lookup"><span data-stu-id="1d5dd-120">Set the time range</span></span>
<span data-ttu-id="1d5dd-121">Le premier élément canal est un filtre de temps dont l'étendue est limitée aux sept jours précédents.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-121">The first piped element is a time filter scoped to the previous seven days.</span></span> <span data-ttu-id="1d5dd-122">La limitation de la plage de temps permet de s'assurer que les requêtes s'exécutent bien, retournent des résultats gérables et n'ont pas de délai d'délai.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-122">Limiting the time range helps ensure that queries perform well, return manageable results, and don't time out.</span></span>

```kusto
| where Timestamp > ago(7d)
```

### <a name="check-specific-processes"></a><span data-ttu-id="1d5dd-123">Vérifier des processus spécifiques</span><span class="sxs-lookup"><span data-stu-id="1d5dd-123">Check specific processes</span></span>
<span data-ttu-id="1d5dd-124">La période est immédiatement suivie d'une recherche de noms de fichiers de processus représentant l'application PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-124">The time range is immediately followed by a search for process file names representing the PowerShell application.</span></span>

```kusto
// Pivoting on PowerShell processes
| where FileName in~ ("powershell.exe", "powershell_ise.exe")
```

### <a name="search-for-specific-command-strings"></a><span data-ttu-id="1d5dd-125">Rechercher des chaînes de commandes spécifiques</span><span class="sxs-lookup"><span data-stu-id="1d5dd-125">Search for specific command strings</span></span>
<span data-ttu-id="1d5dd-126">Ensuite, la requête recherche des chaînes dans les lignes de commande qui sont généralement utilisées pour télécharger des fichiers à l'aide de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-126">Afterwards, the query looks for strings in command lines that are typically used to download files using PowerShell.</span></span>

```kusto
// Suspicious commands
| where ProcessCommandLine has_any("WebClient",
    "DownloadFile",
    "DownloadData",
    "DownloadString",
    "WebRequest",
    "Shellcode",
    "http",
    "https")
```

### <a name="customize-result-columns-and-length"></a><span data-ttu-id="1d5dd-127">Personnaliser les colonnes de résultats et la longueur</span><span class="sxs-lookup"><span data-stu-id="1d5dd-127">Customize result columns and length</span></span> 
<span data-ttu-id="1d5dd-128">Maintenant que votre requête identifie clairement les données que vous souhaitez localiser, vous pouvez définir à quoi ressemblent les résultats.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-128">Now that your query clearly identifies the data you want to locate, you can define what the results look like.</span></span> <span data-ttu-id="1d5dd-129">`project` renvoie des `top` colonnes spécifiques et limite le nombre de résultats.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-129">`project` returns specific columns, and `top` limits the number of results.</span></span> <span data-ttu-id="1d5dd-130">Ces opérateurs permettent de s'assurer que les résultats sont bien formatés, raisonnablement grands et faciles à traiter.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-130">These operators help ensure the results are well-formatted and reasonably large and easy to process.</span></span>

```kusto
| project Timestamp, DeviceName, InitiatingProcessFileName, InitiatingProcessCommandLine, 
FileName, ProcessCommandLine, RemoteIP, RemoteUrl, RemotePort, RemoteIPType
| top 100 by Timestamp
```

<span data-ttu-id="1d5dd-131">Sélectionnez **Exécuter la requête** pour voir les résultats.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-131">Select **Run query** to see the results.</span></span> <span data-ttu-id="1d5dd-132">Utilisez l'icône développer en haut à droite de l'éditeur de requête pour vous concentrer sur votre requête de recherche et les résultats.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-132">Use the expand icon at the top right of the query editor to focus on your hunting query and the results.</span></span> 

![Image du contrôle Développer dans l'éditeur de requête de recherche avancée](../../media/advanced-hunting-expand.png)

>[!TIP]
><span data-ttu-id="1d5dd-134">Vous pouvez afficher les résultats de la requête sous la mesure de graphiques et ajuster rapidement les filtres.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-134">You can view query results as charts and quickly adjust filters.</span></span> <span data-ttu-id="1d5dd-135">Pour obtenir des [conseils, voir l'aide sur l'working with query results](advanced-hunting-query-results.md)</span><span class="sxs-lookup"><span data-stu-id="1d5dd-135">For guidance, [read about working with query results](advanced-hunting-query-results.md)</span></span>

## <a name="learn-common-query-operators"></a><span data-ttu-id="1d5dd-136">Découvrir les opérateurs de requête courants</span><span class="sxs-lookup"><span data-stu-id="1d5dd-136">Learn common query operators</span></span>

<span data-ttu-id="1d5dd-137">Vous viennent d'exécuter votre première requête et vous avez une idée générale de ses composants.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-137">You've just run your first query and have a general idea of its components.</span></span> <span data-ttu-id="1d5dd-138">Il est temps de revenir en arrière légèrement et d'apprendre quelques principes de base.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-138">It's time to backtrack slightly and learn some basics.</span></span> <span data-ttu-id="1d5dd-139">Le langage de requête Kusto utilisé par le repérage avancé prend en charge divers opérateurs, notamment les opérateurs communs suivants.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-139">The Kusto query language used by advanced hunting supports a range of operators, including the following common ones.</span></span>

| <span data-ttu-id="1d5dd-140">Opérateur</span><span class="sxs-lookup"><span data-stu-id="1d5dd-140">Operator</span></span> | <span data-ttu-id="1d5dd-141">Description et utilisation</span><span class="sxs-lookup"><span data-stu-id="1d5dd-141">Description and usage</span></span> |
|--|--|
| `where` | <span data-ttu-id="1d5dd-142">Filtre une table sur le sous-ensemble de lignes qui répondent à un prédicat.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-142">Filter a table to the subset of rows that satisfy a predicate.</span></span> |
| `summarize` | <span data-ttu-id="1d5dd-143">Produit une table qui agrège le contenu de la table d’entrée.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-143">Produce a table that aggregates the content of the input table.</span></span> |
| `join` | <span data-ttu-id="1d5dd-144">Fusionne les lignes de deux tables pour former une nouvelle table en faisant correspondre les valeurs des colonnes spécifiées de chaque table.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-144">Merge the rows of two tables to form a new table by matching values of the specified column(s) from each table.</span></span> |
| `count` | <span data-ttu-id="1d5dd-145">Renvoie le nombre d’enregistrements dans le groupe d’enregistrements d’entrée.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-145">Return the number of records in the input record set.</span></span> |
| `top` | <span data-ttu-id="1d5dd-146">Renvoie les N premiers enregistrements triés par les colonnes spécifiées.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-146">Return the first N records sorted by the specified columns.</span></span> |
| `limit` | <span data-ttu-id="1d5dd-147">Renvoie jusqu’au nombre de lignes spécifié.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-147">Return up to the specified number of rows.</span></span> |
| `project` | <span data-ttu-id="1d5dd-148">Sélectionne les colonnes à inclure, renommer ou déplacer et insère de nouvelles colonnes calculées.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-148">Select the columns to include, rename or drop, and insert new computed columns.</span></span> |
| `extend` | <span data-ttu-id="1d5dd-149">Crée des colonnes calculées et les ajoute au jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-149">Create calculated columns and append them to the result set.</span></span> |
| `makeset` |  <span data-ttu-id="1d5dd-150">Renvoie un tableau dynamique (JSON) de l’ensemble de valeurs distinctes prise par Expr dans le groupe.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-150">Return a dynamic (JSON) array of the set of distinct values that Expr takes in the group.</span></span> |
| `find` | <span data-ttu-id="1d5dd-151">Recherche des lignes qui correspondent à un prédicat dans un ensemble de tables.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-151">Find rows that match a predicate across a set of tables.</span></span> |

<span data-ttu-id="1d5dd-152">Pour voir un exemple parlant de ces opérateurs, exécutez-les à partir de la section **Prise en main** du repérage avancé.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-152">To see a live example of these operators, run them from the **Get started** section in advanced hunting.</span></span>

## <a name="understand-data-types"></a><span data-ttu-id="1d5dd-153">Comprendre les types de données</span><span class="sxs-lookup"><span data-stu-id="1d5dd-153">Understand data types</span></span>

<span data-ttu-id="1d5dd-154">Le recherche avancée prend en charge les types de données Kusto, y compris les types courants suivants :</span><span class="sxs-lookup"><span data-stu-id="1d5dd-154">Advanced hunting supports Kusto data types, including the following common types:</span></span>

| <span data-ttu-id="1d5dd-155">Type de données</span><span class="sxs-lookup"><span data-stu-id="1d5dd-155">Data type</span></span> | <span data-ttu-id="1d5dd-156">Description et implications dans les requêtes</span><span class="sxs-lookup"><span data-stu-id="1d5dd-156">Description and query implications</span></span> |
|--|--|
| `datetime` | <span data-ttu-id="1d5dd-157">Les données et les informations d'heure représentent généralement des timestamps d'événement.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-157">Data and time information typically representing event timestamps.</span></span> [<span data-ttu-id="1d5dd-158">Voir les formats de date/heure pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d5dd-158">See supported datetime formats</span></span>](/azure/data-explorer/kusto/query/scalar-data-types/datetime) |
| `string` | <span data-ttu-id="1d5dd-159">Chaîne de caractères en UTF-8 entre guillemets simples ( `'` ) ou guillemets doubles ( `"` ).</span><span class="sxs-lookup"><span data-stu-id="1d5dd-159">Character string in UTF-8 enclosed in single quotes (`'`) or double quotes (`"`).</span></span> [<span data-ttu-id="1d5dd-160">En savoir plus sur les chaînes</span><span class="sxs-lookup"><span data-stu-id="1d5dd-160">Read more about strings</span></span>](/azure/data-explorer/kusto/query/scalar-data-types/string) |
| `bool` | <span data-ttu-id="1d5dd-161">Ce type de données prend en charge `true` ou `false` indique.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-161">This data type supports `true` or `false` states.</span></span> [<span data-ttu-id="1d5dd-162">Voir les opérateurs et les littéraux pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d5dd-162">See supported literals and operators</span></span>](/azure/data-explorer/kusto/query/scalar-data-types/bool) |
| `int` | <span data-ttu-id="1d5dd-163">Integer 32 bits</span><span class="sxs-lookup"><span data-stu-id="1d5dd-163">32-bit integer</span></span>  |
| `long` | <span data-ttu-id="1d5dd-164">Integer 64 bits</span><span class="sxs-lookup"><span data-stu-id="1d5dd-164">64-bit integer</span></span> |

<span data-ttu-id="1d5dd-165">Pour en savoir plus sur ces types de données, consultez les types de données [scalar Kusto.](/azure/data-explorer/kusto/query/scalar-data-types/)</span><span class="sxs-lookup"><span data-stu-id="1d5dd-165">To learn more about these data types, [read about Kusto scalar data types](/azure/data-explorer/kusto/query/scalar-data-types/).</span></span>

## <a name="get-help-as-you-write-queries"></a><span data-ttu-id="1d5dd-166">Obtenez de l’aide lorsque vous rédigez des requêtes</span><span class="sxs-lookup"><span data-stu-id="1d5dd-166">Get help as you write queries</span></span>
<span data-ttu-id="1d5dd-167">Tirez parti des fonctionnalités suivantes pour rédiger des requêtes plus rapidement :</span><span class="sxs-lookup"><span data-stu-id="1d5dd-167">Take advantage of the following functionality to write queries faster:</span></span>
- <span data-ttu-id="1d5dd-168">**Suggestion automatique : lorsque** vous écrivez des requêtes, le recherche avancée fournit des suggestions de IntelliSense.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-168">**Autosuggest**—as you write queries, advanced hunting provides suggestions from IntelliSense.</span></span> 
- <span data-ttu-id="1d5dd-169">**Arborescence de schéma**: une représentation de schéma qui inclut la liste des tableaux et leurs colonnes est fournie en de côté de votre zone de travail.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-169">**Schema tree**—a schema representation that includes the list of tables and their columns is provided next to your working area.</span></span> <span data-ttu-id="1d5dd-170">Si vous souhaitez en savoir plus, veuillez placer le pointeur sur un élément.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-170">For more information, hover over an item.</span></span> <span data-ttu-id="1d5dd-171">Double-cliquez sur un élément pour l’insérer dans l’éditeur de requête.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-171">Double-click an item to insert it to the query editor.</span></span>
- <span data-ttu-id="1d5dd-172">**[Référence de schéma :](advanced-hunting-schema-tables.md#get-schema-information-in-the-security-center)** référence dans le portail avec des descriptions de tableau et de colonne, ainsi que des types d'événements pris en charge (valeurs) et `ActionType` des exemples de requêtes</span><span class="sxs-lookup"><span data-stu-id="1d5dd-172">**[Schema reference](advanced-hunting-schema-tables.md#get-schema-information-in-the-security-center)**—in-portal reference with table and column descriptions as well as supported event types (`ActionType` values) and sample queries</span></span>

## <a name="work-with-multiple-queries-in-the-editor"></a><span data-ttu-id="1d5dd-173">Utilisation de plusieurs requêtes dans l'éditeur</span><span class="sxs-lookup"><span data-stu-id="1d5dd-173">Work with multiple queries in the editor</span></span>
<span data-ttu-id="1d5dd-174">Vous pouvez utiliser l'éditeur de requête pour expérimenter plusieurs requêtes.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-174">You can use the query editor to experiment with multiple queries.</span></span> <span data-ttu-id="1d5dd-175">Pour utiliser plusieurs requêtes :</span><span class="sxs-lookup"><span data-stu-id="1d5dd-175">To use multiple queries:</span></span>

- <span data-ttu-id="1d5dd-176">Séparez chaque requête par une ligne vide.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-176">Separate each query with an empty line.</span></span>
- <span data-ttu-id="1d5dd-177">Placez le curseur sur n'importe quelle partie d'une requête pour sélectionner cette requête avant de l'exécutez.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-177">Place the cursor on any part of a query to select that query before running it.</span></span> <span data-ttu-id="1d5dd-178">Cette requête n'exécutera que la requête sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-178">This will run only the selected query.</span></span> <span data-ttu-id="1d5dd-179">Pour exécuter une autre requête, déplacez le curseur en conséquence et sélectionnez **Exécuter la requête.**</span><span class="sxs-lookup"><span data-stu-id="1d5dd-179">To run another query, move the cursor accordingly and select **Run query**.</span></span>

![Image de l'éditeur de requête avec plusieurs requêtes](../../media/mtp-ah/ah-multi-query.png)

## <a name="use-sample-queries"></a><span data-ttu-id="1d5dd-181">Utiliser des exemples de requêtes</span><span class="sxs-lookup"><span data-stu-id="1d5dd-181">Use sample queries</span></span>

<span data-ttu-id="1d5dd-182">La section **Prise en main** fournit quelques requêtes simples utilisant des opérateurs fréquemment utilisés.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-182">The **Get started** section provides a few simple queries using commonly used operators.</span></span> <span data-ttu-id="1d5dd-183">Essayez d’exécuter ces requêtes et de leur apporter de légères modifications.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-183">Try running these queries and making small modifications to them.</span></span>

![Image d’une fenêtre de repérage avancé](../../media/advanced-hunting-get-started.png)

>[!NOTE]
><span data-ttu-id="1d5dd-185">Hormis les exemples de requête de base, vous pouvez également accéder à des [requêtes partagées](advanced-hunting-shared-queries.md) pour des scénarios de repérage de menace spécifiques.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-185">Apart from the basic query samples, you can also access [shared queries](advanced-hunting-shared-queries.md) for specific threat hunting scenarios.</span></span> <span data-ttu-id="1d5dd-186">Explorez les requêtes partagées sur le côté gauche de la page ou le référentiel de requêtes [GitHub.](https://aka.ms/hunting-queries)</span><span class="sxs-lookup"><span data-stu-id="1d5dd-186">Explore the shared queries on the left side of the page or the [GitHub query repository](https://aka.ms/hunting-queries).</span></span>

## <a name="access-query-language-documentation"></a><span data-ttu-id="1d5dd-187">Documentation sur le langage de requête Access</span><span class="sxs-lookup"><span data-stu-id="1d5dd-187">Access query language documentation</span></span>

<span data-ttu-id="1d5dd-188">Pour plus d’informations sur le langage de requête Kusto et les opérateurs pris en charge, voir [documentation sur le langage de requête Kusto](/azure/kusto/query/).</span><span class="sxs-lookup"><span data-stu-id="1d5dd-188">For more information on Kusto query language and supported operators, see [Kusto query language documentation](/azure/kusto/query/).</span></span>

>[!NOTE]
><span data-ttu-id="1d5dd-189">Certains tableaux de cet article peuvent ne pas être disponibles dans Microsoft Defender pour Endpoint.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-189">Some tables in this article might not be available in Microsoft Defender for Endpoint.</span></span> <span data-ttu-id="1d5dd-190">[Activer Microsoft 365 Defender](m365d-enable.md) pour qu'il recherche les menaces à l'aide de sources de données plus nombreuses.</span><span class="sxs-lookup"><span data-stu-id="1d5dd-190">[Turn on Microsoft 365 Defender](m365d-enable.md) to hunt for threats using more data sources.</span></span> <span data-ttu-id="1d5dd-191">Vous pouvez déplacer vos flux de travail de recherche avancée de Microsoft Defender pour point de terminaison vers Microsoft 365 Defender en suivant les étapes de la procédure de migration des requêtes de recherche avancée à partir de Microsoft Defender pour le point de [terminaison.](advanced-hunting-migrate-from-mde.md)</span><span class="sxs-lookup"><span data-stu-id="1d5dd-191">You can move your advanced hunting workflows from Microsoft Defender for Endpoint to Microsoft 365 Defender by following the steps in [Migrate advanced hunting queries from Microsoft Defender for Endpoint](advanced-hunting-migrate-from-mde.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d5dd-192">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d5dd-192">Related topics</span></span>
- [<span data-ttu-id="1d5dd-193">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="1d5dd-193">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="1d5dd-194">Utiliser les résultats d’une requête</span><span class="sxs-lookup"><span data-stu-id="1d5dd-194">Work with query results</span></span>](advanced-hunting-query-results.md)
- [<span data-ttu-id="1d5dd-195">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="1d5dd-195">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="1d5dd-196">Repérer des menaces sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="1d5dd-196">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="1d5dd-197">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="1d5dd-197">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="1d5dd-198">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="1d5dd-198">Apply query best practices</span></span>](advanced-hunting-best-practices.md)