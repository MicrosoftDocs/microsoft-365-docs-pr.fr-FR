---
title: Découvrez le langage de requête de repérage avancé dans la Protection Microsoft contre les menaces
description: Créez votre première requête de repérage de menace et découvrez les opérateurs communs et les autres aspects du langage de requête de repérage avancé
keywords: chasse de menace, recherche de menace, recherche de menace informatique, protection contre les menaces Microsoft, Microsoft 365, MTP, M365, recherche, requête, langue, apprentissage, première requête, télémétrie, événements, télémétrie, détections personnalisées, schéma, Kusto, opérateurs, types de données, téléchargement PowerShell, exemple de requête
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
ms.openlocfilehash: 8c66ee39d9c7f90142a564c61b13f68e6b4b481e
ms.sourcegitcommit: c083602dda3cdcb5b58cb8aa070d77019075f765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2020
ms.locfileid: "48197772"
---
# <a name="learn-the-advanced-hunting-query-language"></a><span data-ttu-id="0d568-104">Découvrir le langage de requête de repérage avancé</span><span class="sxs-lookup"><span data-stu-id="0d568-104">Learn the advanced hunting query language</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="0d568-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="0d568-105">**Applies to:**</span></span>
- <span data-ttu-id="0d568-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="0d568-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="0d568-107">Le repérage avancé est basé sur le [langage de requête Kusto](https://docs.microsoft.com/azure/kusto/query/).</span><span class="sxs-lookup"><span data-stu-id="0d568-107">Advanced hunting is based on the [Kusto query language](https://docs.microsoft.com/azure/kusto/query/).</span></span> <span data-ttu-id="0d568-108">Vous pouvez utiliser la syntaxe et les opérateurs Kusto pour créer des requêtes qui recherchent des informations dans le [schéma](advanced-hunting-schema-tables.md) spécifiquement structuré pour un repérage avancé.</span><span class="sxs-lookup"><span data-stu-id="0d568-108">You can use Kusto syntax and operators to construct queries that locate information in the [schema](advanced-hunting-schema-tables.md) specifically structured for advanced hunting.</span></span> <span data-ttu-id="0d568-109">Pour mieux comprendre ces concepts, exécutez votre première requête.</span><span class="sxs-lookup"><span data-stu-id="0d568-109">To understand these concepts better, run your first query.</span></span>

## <a name="try-your-first-query"></a><span data-ttu-id="0d568-110">Essayez votre première requête</span><span class="sxs-lookup"><span data-stu-id="0d568-110">Try your first query</span></span>

<span data-ttu-id="0d568-111">Dans le centre de sécurité Microsoft 365, accédez à la **recherche pour exécuter** votre première requête.</span><span class="sxs-lookup"><span data-stu-id="0d568-111">In Microsoft 365 security center, go to **Hunting** to run your first query.</span></span> <span data-ttu-id="0d568-112">Consultez l’exemple qui suit :</span><span class="sxs-lookup"><span data-stu-id="0d568-112">Use the following example:</span></span>

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

<span data-ttu-id="0d568-113">Voici son futur aspect dans le repérage avancé.</span><span class="sxs-lookup"><span data-stu-id="0d568-113">This is how it will look like in advanced hunting.</span></span>

![Image de la requête de recherche avancée Microsoft Threat Protection](../../media/advanced-hunting-query-example-2.png)

### <a name="describe-the-query-and-specify-the-tables-to-search"></a><span data-ttu-id="0d568-115">Décrire la requête et spécifier les tables à rechercher</span><span class="sxs-lookup"><span data-stu-id="0d568-115">Describe the query and specify the tables to search</span></span>
<span data-ttu-id="0d568-116">Un bref commentaire a été ajouté au début de la requête pour décrire sa fonction.</span><span class="sxs-lookup"><span data-stu-id="0d568-116">A short comment has been added to the beginning of the query to describe what it is for.</span></span> <span data-ttu-id="0d568-117">Cela vous permet de décider ultérieurement d’enregistrer la requête et de la partager avec d’autres membres de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0d568-117">This helps if you later decide to save the query and share it with others in your organization.</span></span> 

```kusto
// Finds PowerShell execution events that could involve a download
```

<span data-ttu-id="0d568-118">La requête elle-même commence généralement par un nom de table suivi d’une série d’éléments commençant par une barre verticale (`|`).</span><span class="sxs-lookup"><span data-stu-id="0d568-118">The query itself will typically start with a table name followed by a series of elements started by a pipe (`|`).</span></span> <span data-ttu-id="0d568-119">Dans cet exemple, nous commençons par créer une Union de deux tables,  `DeviceProcessEvents` et `DeviceNetworkEvents` et ajoutons des éléments redirigés selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="0d568-119">In this example, we start by creating a union of two tables,  `DeviceProcessEvents` and `DeviceNetworkEvents`, and add piped elements as needed.</span></span>

```kusto
union DeviceProcessEvents, DeviceNetworkEvents
```
### <a name="set-the-time-range"></a><span data-ttu-id="0d568-120">Définir la plage horaire</span><span class="sxs-lookup"><span data-stu-id="0d568-120">Set the time range</span></span>
<span data-ttu-id="0d568-121">Le premier élément Redirigé est un filtre temporel étendu aux sept jours précédents.</span><span class="sxs-lookup"><span data-stu-id="0d568-121">The first piped element is a time filter scoped to the previous seven days.</span></span> <span data-ttu-id="0d568-122">La conservation d’un intervalle de temps le plus étroit possible permet de s’assurer que les requêtes fonctionnent bien, renvoient des résultats gérables et n’expirent pas.</span><span class="sxs-lookup"><span data-stu-id="0d568-122">Keeping the time range as narrow as possible ensures that queries perform well, return manageable results, and don't time out.</span></span>

```kusto
| where Timestamp > ago(7d)
```

### <a name="check-specific-processes"></a><span data-ttu-id="0d568-123">Vérifier des processus spécifiques</span><span class="sxs-lookup"><span data-stu-id="0d568-123">Check specific processes</span></span>
<span data-ttu-id="0d568-124">La plage horaire est immédiatement suivie d’une recherche de noms de fichiers de processus représentant l’application PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0d568-124">The time range is immediately followed by a search for process file names representing the PowerShell application.</span></span>

```kusto
// Pivoting on PowerShell processes
| where FileName in~ ("powershell.exe", "powershell_ise.exe")
```

### <a name="search-for-specific-command-strings"></a><span data-ttu-id="0d568-125">Rechercher des chaînes de commande spécifiques</span><span class="sxs-lookup"><span data-stu-id="0d568-125">Search for specific command strings</span></span>
<span data-ttu-id="0d568-126">Ensuite, la requête recherche des chaînes dans les lignes de commande qui sont généralement utilisées pour télécharger des fichiers à l’aide de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0d568-126">Afterwards, the query looks for strings in command lines that are typically used to download files using PowerShell.</span></span>

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

### <a name="customize-result-columns-and-length"></a><span data-ttu-id="0d568-127">Personnaliser les colonnes de résultats et la longueur</span><span class="sxs-lookup"><span data-stu-id="0d568-127">Customize result columns and length</span></span> 
<span data-ttu-id="0d568-128">Maintenant que votre requête identifie clairement les données que vous recherchez, vous pouvez ajouter des éléments qui définissent l’apparence des résultats.</span><span class="sxs-lookup"><span data-stu-id="0d568-128">Now that your query clearly identifies the data you want to locate, you can add elements that define what the results look like.</span></span> <span data-ttu-id="0d568-129">`project` renvoie des colonnes spécifiques et `top` limite le nombre de résultats.</span><span class="sxs-lookup"><span data-stu-id="0d568-129">`project` returns specific columns, and `top` limits the number of results.</span></span> <span data-ttu-id="0d568-130">Ces opérateurs permettent de s’assurer que les résultats sont bien formatés et raisonnablement volumineux et faciles à traiter.</span><span class="sxs-lookup"><span data-stu-id="0d568-130">These operators help ensure the results are well-formatted and reasonably large and easy to process.</span></span>

```kusto
| project Timestamp, DeviceName, InitiatingProcessFileName, InitiatingProcessCommandLine, 
FileName, ProcessCommandLine, RemoteIP, RemoteUrl, RemotePort, RemoteIPType
| top 100 by Timestamp
```

<span data-ttu-id="0d568-131">Cliquez sur **Exécuter la requête** pour afficher les résultats.</span><span class="sxs-lookup"><span data-stu-id="0d568-131">Click **Run query** to see the results.</span></span> <span data-ttu-id="0d568-132">Sélectionnez l’icône développer en haut à droite de l’éditeur de requête pour vous concentrer sur votre requête de recherche et les résultats.</span><span class="sxs-lookup"><span data-stu-id="0d568-132">Select the expand icon at the top right of the query editor to focus on your hunting query and the results.</span></span> 

![Image du contrôle Expand dans l’éditeur de requête de recherche avancée](../../media/advanced-hunting-expand.png)

>[!TIP]
><span data-ttu-id="0d568-134">Vous pouvez afficher les résultats de la requête sous forme de graphiques et ajuster rapidement les filtres.</span><span class="sxs-lookup"><span data-stu-id="0d568-134">You can view query results as charts and quickly adjust filters.</span></span> <span data-ttu-id="0d568-135">Pour obtenir des instructions, consultez la rubrique [utilisation des résultats de requête](advanced-hunting-query-results.md)</span><span class="sxs-lookup"><span data-stu-id="0d568-135">For guidance, [read about working with query results](advanced-hunting-query-results.md)</span></span>

## <a name="learn-common-query-operators"></a><span data-ttu-id="0d568-136">Apprentissage des opérateurs de requête courants</span><span class="sxs-lookup"><span data-stu-id="0d568-136">Learn common query operators</span></span>

<span data-ttu-id="0d568-137">Maintenant que vous avez exécuté votre première requête et que vous avez une idée générale de ses composants, il est temps de revenir en arrière pour découvrir quelques notions de base.</span><span class="sxs-lookup"><span data-stu-id="0d568-137">Now that you've run your first query and have a general idea of its components, it's time to backtrack a little bit and learn some basics.</span></span> <span data-ttu-id="0d568-138">Le langage de requête Kusto utilisé par le repérage avancé prend en charge divers opérateurs, notamment les opérateurs communs suivants.</span><span class="sxs-lookup"><span data-stu-id="0d568-138">The Kusto query language used by advanced hunting supports a range of operators, including the following common ones.</span></span>

| <span data-ttu-id="0d568-139">Opérateur</span><span class="sxs-lookup"><span data-stu-id="0d568-139">Operator</span></span> | <span data-ttu-id="0d568-140">Description et utilisation</span><span class="sxs-lookup"><span data-stu-id="0d568-140">Description and usage</span></span> |
|--|--|
| `where` | <span data-ttu-id="0d568-141">Filtre une table sur le sous-ensemble de lignes qui répondent à un prédicat.</span><span class="sxs-lookup"><span data-stu-id="0d568-141">Filter a table to the subset of rows that satisfy a predicate.</span></span> |
| `summarize` | <span data-ttu-id="0d568-142">Produit une table qui agrège le contenu de la table d’entrée.</span><span class="sxs-lookup"><span data-stu-id="0d568-142">Produce a table that aggregates the content of the input table.</span></span> |
| `join` | <span data-ttu-id="0d568-143">Fusionne les lignes de deux tables pour former une nouvelle table en faisant correspondre les valeurs des colonnes spécifiées de chaque table.</span><span class="sxs-lookup"><span data-stu-id="0d568-143">Merge the rows of two tables to form a new table by matching values of the specified column(s) from each table.</span></span> |
| `count` | <span data-ttu-id="0d568-144">Renvoie le nombre d’enregistrements dans le groupe d’enregistrements d’entrée.</span><span class="sxs-lookup"><span data-stu-id="0d568-144">Return the number of records in the input record set.</span></span> |
| `top` | <span data-ttu-id="0d568-145">Renvoie les N premiers enregistrements triés par les colonnes spécifiées.</span><span class="sxs-lookup"><span data-stu-id="0d568-145">Return the first N records sorted by the specified columns.</span></span> |
| `limit` | <span data-ttu-id="0d568-146">Renvoie jusqu’au nombre de lignes spécifié.</span><span class="sxs-lookup"><span data-stu-id="0d568-146">Return up to the specified number of rows.</span></span> |
| `project` | <span data-ttu-id="0d568-147">Sélectionne les colonnes à inclure, renommer ou déplacer et insère de nouvelles colonnes calculées.</span><span class="sxs-lookup"><span data-stu-id="0d568-147">Select the columns to include, rename or drop, and insert new computed columns.</span></span> |
| `extend` | <span data-ttu-id="0d568-148">Crée des colonnes calculées et les ajoute au jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="0d568-148">Create calculated columns and append them to the result set.</span></span> |
| `makeset` |  <span data-ttu-id="0d568-149">Renvoie un tableau dynamique (JSON) de l’ensemble de valeurs distinctes prise par Expr dans le groupe.</span><span class="sxs-lookup"><span data-stu-id="0d568-149">Return a dynamic (JSON) array of the set of distinct values that Expr takes in the group.</span></span> |
| `find` | <span data-ttu-id="0d568-150">Recherche des lignes qui correspondent à un prédicat dans un ensemble de tables.</span><span class="sxs-lookup"><span data-stu-id="0d568-150">Find rows that match a predicate across a set of tables.</span></span> |

<span data-ttu-id="0d568-151">Pour voir un exemple parlant de ces opérateurs, exécutez-les à partir de la section **Prise en main** du repérage avancé.</span><span class="sxs-lookup"><span data-stu-id="0d568-151">To see a live example of these operators, run them from the **Get started** section in advanced hunting.</span></span>

## <a name="understand-data-types"></a><span data-ttu-id="0d568-152">Comprendre les types de données</span><span class="sxs-lookup"><span data-stu-id="0d568-152">Understand data types</span></span>

<span data-ttu-id="0d568-153">Les données des tables de repérage avancé sont généralement classées dans les types de données suivants.</span><span class="sxs-lookup"><span data-stu-id="0d568-153">Data in advanced hunting tables are generally classified into the following data types.</span></span>

| <span data-ttu-id="0d568-154">Type de données</span><span class="sxs-lookup"><span data-stu-id="0d568-154">Data type</span></span> | <span data-ttu-id="0d568-155">Description et implications dans les requêtes</span><span class="sxs-lookup"><span data-stu-id="0d568-155">Description and query implications</span></span> |
|--|--|
| `datetime` | <span data-ttu-id="0d568-156">Informations sur les données et les heures représentant généralement les horodatages d’événement</span><span class="sxs-lookup"><span data-stu-id="0d568-156">Data and time information typically representing event timestamps</span></span> |
| `string` | <span data-ttu-id="0d568-157">Chaîne de caractères</span><span class="sxs-lookup"><span data-stu-id="0d568-157">Character string</span></span> |
| `bool` | <span data-ttu-id="0d568-158">True ou false</span><span class="sxs-lookup"><span data-stu-id="0d568-158">True or false</span></span> |
| `int` | <span data-ttu-id="0d568-159">Valeur numérique de 32 bits</span><span class="sxs-lookup"><span data-stu-id="0d568-159">32-bit numeric value</span></span>  |
| `long` | <span data-ttu-id="0d568-160">Valeur numérique de 64 bits</span><span class="sxs-lookup"><span data-stu-id="0d568-160">64-bit numeric value</span></span> |

<span data-ttu-id="0d568-161">Pour en savoir plus sur ces types de données et leurs implications, consultez la rubrique [relative aux types de données scalaires Kusto](https://docs.microsoft.com/azure/data-explorer/kusto/query/scalar-data-types/).</span><span class="sxs-lookup"><span data-stu-id="0d568-161">To learn more about these data types and their implications, [read about Kusto scalar data types](https://docs.microsoft.com/azure/data-explorer/kusto/query/scalar-data-types/).</span></span>

## <a name="get-help-as-you-write-queries"></a><span data-ttu-id="0d568-162">Obtenez de l’aide lorsque vous rédigez des requêtes</span><span class="sxs-lookup"><span data-stu-id="0d568-162">Get help as you write queries</span></span>
<span data-ttu-id="0d568-163">Tirez parti des fonctionnalités suivantes pour rédiger des requêtes plus rapidement :</span><span class="sxs-lookup"><span data-stu-id="0d568-163">Take advantage of the following functionality to write queries faster:</span></span>
- <span data-ttu-id="0d568-164">**Suggestion** automatique : lors de l’écriture de requêtes, la recherche avancée fournit des suggestions d’IntelliSense.</span><span class="sxs-lookup"><span data-stu-id="0d568-164">**Autosuggest** — as you write queries, advanced hunting provides suggestions from IntelliSense.</span></span> 
- <span data-ttu-id="0d568-165">**Arborescence de schéma** : représentation de schéma qui inclut la liste des tables et leurs colonnes sont fournies en regard de votre zone de travail.</span><span class="sxs-lookup"><span data-stu-id="0d568-165">**Schema tree** — a schema representation that includes the list of tables and their columns is provided next to your working area.</span></span> <span data-ttu-id="0d568-166">Si vous souhaitez en savoir plus, veuillez placer le pointeur sur un élément.</span><span class="sxs-lookup"><span data-stu-id="0d568-166">For more information, hover over an item.</span></span> <span data-ttu-id="0d568-167">Double-cliquez sur un élément pour l’insérer dans l’éditeur de requête.</span><span class="sxs-lookup"><span data-stu-id="0d568-167">Double-click an item to insert it to the query editor.</span></span>
- <span data-ttu-id="0d568-168">**[Référence de schéma](advanced-hunting-schema-tables.md#get-schema-information-in-the-security-center)** : référence dans le portail avec descriptions des tables et des colonnes, ainsi que des types d’événements pris en charge ( `ActionType` valeurs) et des exemples de requêtes</span><span class="sxs-lookup"><span data-stu-id="0d568-168">**[Schema reference](advanced-hunting-schema-tables.md#get-schema-information-in-the-security-center)** — in-portal reference with table and column descriptions as well as supported event types (`ActionType` values) and sample queries</span></span>

## <a name="work-with-multiple-queries-in-the-editor"></a><span data-ttu-id="0d568-169">Utiliser plusieurs requêtes dans l’éditeur</span><span class="sxs-lookup"><span data-stu-id="0d568-169">Work with multiple queries in the editor</span></span>
<span data-ttu-id="0d568-170">L’éditeur de requête peut servir de bloc de montage pour tester plusieurs requêtes.</span><span class="sxs-lookup"><span data-stu-id="0d568-170">The query editor can serve as your scratch pad for experimenting with multiple queries.</span></span> <span data-ttu-id="0d568-171">Pour utiliser plusieurs requêtes :</span><span class="sxs-lookup"><span data-stu-id="0d568-171">To use multiple queries:</span></span>

- <span data-ttu-id="0d568-172">Séparez chaque requête par une ligne vide.</span><span class="sxs-lookup"><span data-stu-id="0d568-172">Separate each query with an empty line.</span></span>
- <span data-ttu-id="0d568-173">Placez le curseur sur une partie quelconque d’une requête pour sélectionner cette requête avant de l’exécuter.</span><span class="sxs-lookup"><span data-stu-id="0d568-173">Place the cursor on any part of a query to select that query before running it.</span></span> <span data-ttu-id="0d568-174">Cette opération n’exécutera que la requête sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="0d568-174">This will run only the selected query.</span></span> <span data-ttu-id="0d568-175">Pour exécuter une autre requête, déplacez le curseur en conséquence et sélectionnez **exécuter la requête**.</span><span class="sxs-lookup"><span data-stu-id="0d568-175">To run another query, move the cursor accordingly and select **Run query**.</span></span>

![Image de l’éditeur de requête avec plusieurs requêtes](../../media/mtp-ah/ah-multi-query.png)

## <a name="use-sample-queries"></a><span data-ttu-id="0d568-177">Utiliser des exemples de requêtes</span><span class="sxs-lookup"><span data-stu-id="0d568-177">Use sample queries</span></span>

<span data-ttu-id="0d568-178">La section **Prise en main** fournit quelques requêtes simples utilisant des opérateurs fréquemment utilisés.</span><span class="sxs-lookup"><span data-stu-id="0d568-178">The **Get started** section provides a few simple queries using commonly used operators.</span></span> <span data-ttu-id="0d568-179">Essayez d’exécuter ces requêtes et de leur apporter de légères modifications.</span><span class="sxs-lookup"><span data-stu-id="0d568-179">Try running these queries and making small modifications to them.</span></span>

![Image d’une fenêtre de repérage avancé](../../media/advanced-hunting-get-started.png)

>[!NOTE]
><span data-ttu-id="0d568-181">Hormis les exemples de requête de base, vous pouvez également accéder à des [requêtes partagées](advanced-hunting-shared-queries.md) pour des scénarios de repérage de menace spécifiques.</span><span class="sxs-lookup"><span data-stu-id="0d568-181">Apart from the basic query samples, you can also access [shared queries](advanced-hunting-shared-queries.md) for specific threat hunting scenarios.</span></span> <span data-ttu-id="0d568-182">Explorez les requêtes partagées sur le côté gauche de la page ou le référentiel de requête GitHub.</span><span class="sxs-lookup"><span data-stu-id="0d568-182">Explore the shared queries on the left side of the page or the GitHub query repository.</span></span>

## <a name="access-query-language-documentation"></a><span data-ttu-id="0d568-183">Documentation sur le langage de requête Access</span><span class="sxs-lookup"><span data-stu-id="0d568-183">Access query language documentation</span></span>

<span data-ttu-id="0d568-184">Pour plus d’informations sur le langage de requête Kusto et les opérateurs pris en charge, voir [documentation sur le langage de requête Kusto](https://docs.microsoft.com/azure/kusto/query/).</span><span class="sxs-lookup"><span data-stu-id="0d568-184">For more information on Kusto query language and supported operators, see [Kusto query language documentation](https://docs.microsoft.com/azure/kusto/query/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d568-185">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="0d568-185">Related topics</span></span>
- [<span data-ttu-id="0d568-186">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="0d568-186">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="0d568-187">Travailler avec les résultats de la requête</span><span class="sxs-lookup"><span data-stu-id="0d568-187">Work with query results</span></span>](advanced-hunting-query-results.md)
- [<span data-ttu-id="0d568-188">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="0d568-188">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="0d568-189">Rechercher sur les appareils, les emails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="0d568-189">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="0d568-190">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="0d568-190">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="0d568-191">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="0d568-191">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
