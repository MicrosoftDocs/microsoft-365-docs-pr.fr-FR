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
ms.openlocfilehash: 14de9d84ef19be3dcf1e630b2814a6060bfe7f27
ms.sourcegitcommit: a45cf8b887587a1810caf9afa354638e68ec5243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/05/2020
ms.locfileid: "44036498"
---
# <a name="learn-the-advanced-hunting-query-language"></a><span data-ttu-id="5657d-104">Découvrir le langage de requête de repérage avancé</span><span class="sxs-lookup"><span data-stu-id="5657d-104">Learn the advanced hunting query language</span></span>

<span data-ttu-id="5657d-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="5657d-105">**Applies to:**</span></span>
- <span data-ttu-id="5657d-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="5657d-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="5657d-107">Le repérage avancé est basé sur le [langage de requête Kusto](https://docs.microsoft.com/azure/kusto/query/).</span><span class="sxs-lookup"><span data-stu-id="5657d-107">Advanced hunting is based on the [Kusto query language](https://docs.microsoft.com/azure/kusto/query/).</span></span> <span data-ttu-id="5657d-108">Vous pouvez utiliser la syntaxe et les opérateurs Kusto pour créer des requêtes qui recherchent des informations dans le [schéma](advanced-hunting-schema-tables.md) spécifiquement structuré pour un repérage avancé.</span><span class="sxs-lookup"><span data-stu-id="5657d-108">You can use Kusto syntax and operators to construct queries that locate information in the [schema](advanced-hunting-schema-tables.md) specifically structured for advanced hunting.</span></span> <span data-ttu-id="5657d-109">Pour mieux comprendre ces concepts, exécutez votre première requête.</span><span class="sxs-lookup"><span data-stu-id="5657d-109">To understand these concepts better, run your first query.</span></span>

## <a name="try-your-first-query"></a><span data-ttu-id="5657d-110">Essayez votre première requête</span><span class="sxs-lookup"><span data-stu-id="5657d-110">Try your first query</span></span>

<span data-ttu-id="5657d-111">Dans le centre de sécurité Microsoft 365, accédez à la **recherche pour exécuter** votre première requête.</span><span class="sxs-lookup"><span data-stu-id="5657d-111">In Microsoft 365 security center, go to **Hunting** to run your first query.</span></span> <span data-ttu-id="5657d-112">Consultez l’exemple qui suit :</span><span class="sxs-lookup"><span data-stu-id="5657d-112">Use the following example:</span></span>

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

<span data-ttu-id="5657d-113">Voici son futur aspect dans le repérage avancé.</span><span class="sxs-lookup"><span data-stu-id="5657d-113">This is how it will look like in advanced hunting.</span></span>

![Image de la requête de recherche avancée Microsoft Threat Protection](../../media/advanced-hunting-query-example-2.png)

### <a name="describe-the-query-and-specify-the-tables-to-search"></a><span data-ttu-id="5657d-115">Décrire la requête et spécifier les tables à rechercher</span><span class="sxs-lookup"><span data-stu-id="5657d-115">Describe the query and specify the tables to search</span></span>
<span data-ttu-id="5657d-116">Un bref commentaire a été ajouté au début de la requête pour décrire sa fonction.</span><span class="sxs-lookup"><span data-stu-id="5657d-116">A short comment has been added to the beginning of the query to describe what it is for.</span></span> <span data-ttu-id="5657d-117">Cela vous permet de décider ultérieurement d’enregistrer la requête et de la partager avec d’autres membres de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="5657d-117">This helps if you later decide to save the query and share it with others in your organization.</span></span> 

```kusto
// Finds PowerShell execution events that could involve a download
```

<span data-ttu-id="5657d-118">La requête elle-même commence généralement par un nom de table suivi d’une série d’éléments commençant par une barre verticale (`|`).</span><span class="sxs-lookup"><span data-stu-id="5657d-118">The query itself will typically start with a table name followed by a series of elements started by a pipe (`|`).</span></span> <span data-ttu-id="5657d-119">Dans cet exemple, nous commençons par créer une Union de deux tables `DeviceProcessEvents` , `DeviceNetworkEvents`et et ajoutons des éléments redirigés selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="5657d-119">In this example, we start by creating a union of two tables,  `DeviceProcessEvents` and `DeviceNetworkEvents`, and add piped elements as needed.</span></span>

```kusto
union DeviceProcessEvents, DeviceNetworkEvents
```
### <a name="set-the-time-range"></a><span data-ttu-id="5657d-120">Définir la plage horaire</span><span class="sxs-lookup"><span data-stu-id="5657d-120">Set the time range</span></span>
<span data-ttu-id="5657d-121">Le premier élément Redirigé est un filtre temporel étendu aux sept jours précédents.</span><span class="sxs-lookup"><span data-stu-id="5657d-121">The first piped element is a time filter scoped to the previous seven days.</span></span> <span data-ttu-id="5657d-122">La conservation d’un intervalle de temps le plus étroit possible permet de s’assurer que les requêtes fonctionnent bien, renvoient des résultats gérables et n’expirent pas.</span><span class="sxs-lookup"><span data-stu-id="5657d-122">Keeping the time range as narrow as possible ensures that queries perform well, return manageable results, and don't time out.</span></span>

```kusto
| where Timestamp > ago(7d)
```

### <a name="check-specific-processes"></a><span data-ttu-id="5657d-123">Vérifier des processus spécifiques</span><span class="sxs-lookup"><span data-stu-id="5657d-123">Check specific processes</span></span>
<span data-ttu-id="5657d-124">La plage horaire est immédiatement suivie d’une recherche de noms de fichiers de processus représentant l’application PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5657d-124">The time range is immediately followed by a search for process file names representing the PowerShell application.</span></span>

```
// Pivoting on PowerShell processes
| where FileName in~ ("powershell.exe", "powershell_ise.exe")
```

### <a name="search-for-specific-command-strings"></a><span data-ttu-id="5657d-125">Rechercher des chaînes de commande spécifiques</span><span class="sxs-lookup"><span data-stu-id="5657d-125">Search for specific command strings</span></span>
<span data-ttu-id="5657d-126">Ensuite, la requête recherche des chaînes dans les lignes de commande qui sont généralement utilisées pour télécharger des fichiers à l’aide de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5657d-126">Afterwards, the query looks for strings in command lines that are typically used to download files using PowerShell.</span></span>

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

### <a name="customize-result-columns-and-length"></a><span data-ttu-id="5657d-127">Personnaliser les colonnes de résultats et la longueur</span><span class="sxs-lookup"><span data-stu-id="5657d-127">Customize result columns and length</span></span> 
<span data-ttu-id="5657d-128">Maintenant que votre requête identifie clairement les données que vous recherchez, vous pouvez ajouter des éléments qui définissent l’apparence des résultats.</span><span class="sxs-lookup"><span data-stu-id="5657d-128">Now that your query clearly identifies the data you want to locate, you can add elements that define what the results look like.</span></span> <span data-ttu-id="5657d-129">`project`renvoie des colonnes spécifiques et `top` limite le nombre de résultats.</span><span class="sxs-lookup"><span data-stu-id="5657d-129">`project` returns specific columns, and `top` limits the number of results.</span></span> <span data-ttu-id="5657d-130">Ces opérateurs permettent de s’assurer que les résultats sont bien formatés et raisonnablement volumineux et faciles à traiter.</span><span class="sxs-lookup"><span data-stu-id="5657d-130">These operators help ensure the results are well-formatted and reasonably large and easy to process.</span></span>

```kusto
| project Timestamp, DeviceName, InitiatingProcessFileName, InitiatingProcessCommandLine, 
FileName, ProcessCommandLine, RemoteIP, RemoteUrl, RemotePort, RemoteIPType
| top 100 by Timestamp
```

<span data-ttu-id="5657d-131">Cliquez sur **Exécuter la requête** pour afficher les résultats.</span><span class="sxs-lookup"><span data-stu-id="5657d-131">Click **Run query** to see the results.</span></span> <span data-ttu-id="5657d-132">Sélectionnez l’icône développer en haut à droite de l’éditeur de requête pour vous concentrer sur votre requête de recherche et les résultats.</span><span class="sxs-lookup"><span data-stu-id="5657d-132">Select the expand icon at the top right of the query editor to focus on your hunting query and the results.</span></span> 

![Image du contrôle Expand dans l’éditeur de requête de recherche avancée](../../media/advanced-hunting-expand.png)

>[!TIP]
><span data-ttu-id="5657d-134">Vous pouvez afficher les résultats de la requête sous forme de graphiques et ajuster rapidement les filtres.</span><span class="sxs-lookup"><span data-stu-id="5657d-134">You can view query results as charts and quickly adjust filters.</span></span> <span data-ttu-id="5657d-135">Pour obtenir des instructions, consultez la rubrique [utilisation des résultats de requête](advanced-hunting-query-results.md)</span><span class="sxs-lookup"><span data-stu-id="5657d-135">For guidance, [read about working with query results](advanced-hunting-query-results.md)</span></span>

## <a name="learn-common-query-operators-for-advanced-hunting"></a><span data-ttu-id="5657d-136">Découvrir les opérateurs de requête courants pour le repérage avancé</span><span class="sxs-lookup"><span data-stu-id="5657d-136">Learn common query operators for advanced hunting</span></span>

<span data-ttu-id="5657d-137">Maintenant que vous avez exécuté votre première requête et que vous avez une idée générale de ses composants, il est temps de revenir en arrière pour découvrir quelques notions de base.</span><span class="sxs-lookup"><span data-stu-id="5657d-137">Now that you've run your first query and have a general idea of its components, it's time to backtrack a little bit and learn some basics.</span></span> <span data-ttu-id="5657d-138">Le langage de requête Kusto utilisé par le repérage avancé prend en charge divers opérateurs, notamment les opérateurs communs suivants.</span><span class="sxs-lookup"><span data-stu-id="5657d-138">The Kusto query language used by advanced hunting supports a range of operators, including the following common ones.</span></span>

| <span data-ttu-id="5657d-139">Opérateur</span><span class="sxs-lookup"><span data-stu-id="5657d-139">Operator</span></span> | <span data-ttu-id="5657d-140">Description et utilisation</span><span class="sxs-lookup"><span data-stu-id="5657d-140">Description and usage</span></span> |
|--|--|
| `where` | <span data-ttu-id="5657d-141">Filtre une table sur le sous-ensemble de lignes qui répondent à un prédicat.</span><span class="sxs-lookup"><span data-stu-id="5657d-141">Filter a table to the subset of rows that satisfy a predicate.</span></span> |
| `summarize` | <span data-ttu-id="5657d-142">Produit une table qui agrège le contenu de la table d’entrée.</span><span class="sxs-lookup"><span data-stu-id="5657d-142">Produce a table that aggregates the content of the input table.</span></span> |
| `join` | <span data-ttu-id="5657d-143">Fusionne les lignes de deux tables pour former une nouvelle table en faisant correspondre les valeurs des colonnes spécifiées de chaque table.</span><span class="sxs-lookup"><span data-stu-id="5657d-143">Merge the rows of two tables to form a new table by matching values of the specified column(s) from each table.</span></span> |
| `count` | <span data-ttu-id="5657d-144">Renvoie le nombre d’enregistrements dans le groupe d’enregistrements d’entrée.</span><span class="sxs-lookup"><span data-stu-id="5657d-144">Return the number of records in the input record set.</span></span> |
| `top` | <span data-ttu-id="5657d-145">Renvoie les N premiers enregistrements triés par les colonnes spécifiées.</span><span class="sxs-lookup"><span data-stu-id="5657d-145">Return the first N records sorted by the specified columns.</span></span> |
| `limit` | <span data-ttu-id="5657d-146">Renvoie jusqu’au nombre de lignes spécifié.</span><span class="sxs-lookup"><span data-stu-id="5657d-146">Return up to the specified number of rows.</span></span> |
| `project` | <span data-ttu-id="5657d-147">Sélectionne les colonnes à inclure, renommer ou déplacer et insère de nouvelles colonnes calculées.</span><span class="sxs-lookup"><span data-stu-id="5657d-147">Select the columns to include, rename or drop, and insert new computed columns.</span></span> |
| `extend` | <span data-ttu-id="5657d-148">Crée des colonnes calculées et les ajoute au jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="5657d-148">Create calculated columns and append them to the result set.</span></span> |
| `makeset` |  <span data-ttu-id="5657d-149">Renvoie un tableau dynamique (JSON) de l’ensemble de valeurs distinctes prise par Expr dans le groupe.</span><span class="sxs-lookup"><span data-stu-id="5657d-149">Return a dynamic (JSON) array of the set of distinct values that Expr takes in the group.</span></span> |
| `find` | <span data-ttu-id="5657d-150">Recherche des lignes qui correspondent à un prédicat dans un ensemble de tables.</span><span class="sxs-lookup"><span data-stu-id="5657d-150">Find rows that match a predicate across a set of tables.</span></span> |

<span data-ttu-id="5657d-151">Pour voir un exemple parlant de ces opérateurs, exécutez-les à partir de la section **Prise en main** du repérage avancé.</span><span class="sxs-lookup"><span data-stu-id="5657d-151">To see a live example of these operators, run them from the **Get started** section in advanced hunting.</span></span>

## <a name="understand-data-types-and-their-query-syntax-implications"></a><span data-ttu-id="5657d-152">Comprendre les types de données et leurs implications dans la syntaxe de requête</span><span class="sxs-lookup"><span data-stu-id="5657d-152">Understand data types and their query syntax implications</span></span>

<span data-ttu-id="5657d-153">Les données des tables de repérage avancé sont généralement classées dans les types de données suivants.</span><span class="sxs-lookup"><span data-stu-id="5657d-153">Data in advanced hunting tables are generally classified into the following data types.</span></span>

| <span data-ttu-id="5657d-154">Type de données</span><span class="sxs-lookup"><span data-stu-id="5657d-154">Data type</span></span> | <span data-ttu-id="5657d-155">Description et implications dans les requêtes</span><span class="sxs-lookup"><span data-stu-id="5657d-155">Description and query implications</span></span> |
|--|--|
| `datetime` | <span data-ttu-id="5657d-156">Informations sur les données et les heures représentant généralement les horodatages d’événement</span><span class="sxs-lookup"><span data-stu-id="5657d-156">Data and time information typically representing event timestamps</span></span> |
| `string` | <span data-ttu-id="5657d-157">Chaîne de caractères</span><span class="sxs-lookup"><span data-stu-id="5657d-157">Character string</span></span> |
| `bool` | <span data-ttu-id="5657d-158">True ou false</span><span class="sxs-lookup"><span data-stu-id="5657d-158">True or false</span></span> |
| `int` | <span data-ttu-id="5657d-159">Valeur numérique de 32 bits</span><span class="sxs-lookup"><span data-stu-id="5657d-159">32-bit numeric value</span></span>  |
| `long` | <span data-ttu-id="5657d-160">Valeur numérique de 64 bits</span><span class="sxs-lookup"><span data-stu-id="5657d-160">64-bit numeric value</span></span> |

## <a name="get-help-as-you-write-queries"></a><span data-ttu-id="5657d-161">Obtenez de l’aide lorsque vous rédigez des requêtes</span><span class="sxs-lookup"><span data-stu-id="5657d-161">Get help as you write queries</span></span>
<span data-ttu-id="5657d-162">Tirez parti des fonctionnalités suivantes pour rédiger des requêtes plus rapidement :</span><span class="sxs-lookup"><span data-stu-id="5657d-162">Take advantage of the following functionality to write queries faster:</span></span>
- <span data-ttu-id="5657d-163">**Suggestion** automatique : lors de l’écriture de requêtes, la recherche avancée fournit des suggestions d’IntelliSense.</span><span class="sxs-lookup"><span data-stu-id="5657d-163">**Autosuggest** — as you write queries, advanced hunting provides suggestions from IntelliSense.</span></span> 
- <span data-ttu-id="5657d-164">**Référence de schéma** : une référence de schéma qui inclut la liste des tableaux et leurs colonnes est fournie à côté de votre espace de travail.</span><span class="sxs-lookup"><span data-stu-id="5657d-164">**Schema reference** — a schema reference that includes the list of tables and their columns is provided next to your working area.</span></span> <span data-ttu-id="5657d-165">Si vous souhaitez en savoir plus, veuillez placer le pointeur sur un élément.</span><span class="sxs-lookup"><span data-stu-id="5657d-165">For more information, hover over an item.</span></span> <span data-ttu-id="5657d-166">Double-cliquez sur un élément pour l’insérer dans l’éditeur de requête.</span><span class="sxs-lookup"><span data-stu-id="5657d-166">Double-click an item to insert it to the query editor.</span></span>

## <a name="use-sample-queries"></a><span data-ttu-id="5657d-167">Utiliser des exemples de requêtes</span><span class="sxs-lookup"><span data-stu-id="5657d-167">Use sample queries</span></span>

<span data-ttu-id="5657d-168">La section **Prise en main** fournit quelques requêtes simples utilisant des opérateurs fréquemment utilisés.</span><span class="sxs-lookup"><span data-stu-id="5657d-168">The **Get started** section provides a few simple queries using commonly used operators.</span></span> <span data-ttu-id="5657d-169">Essayez d’exécuter ces requêtes et de leur apporter de légères modifications.</span><span class="sxs-lookup"><span data-stu-id="5657d-169">Try running these queries and making small modifications to them.</span></span>

![Image d’une fenêtre de repérage avancé](../../media/advanced-hunting-get-started.png)

>[!NOTE]
><span data-ttu-id="5657d-171">Hormis les exemples de requête de base, vous pouvez également accéder à des [requêtes partagées](advanced-hunting-shared-queries.md) pour des scénarios de repérage de menace spécifiques.</span><span class="sxs-lookup"><span data-stu-id="5657d-171">Apart from the basic query samples, you can also access [shared queries](advanced-hunting-shared-queries.md) for specific threat hunting scenarios.</span></span> <span data-ttu-id="5657d-172">Explorez les requêtes partagées sur le côté gauche de la page ou le référentiel de requête GitHub.</span><span class="sxs-lookup"><span data-stu-id="5657d-172">Explore the shared queries on the left side of the page or the GitHub query repository.</span></span>

## <a name="access-query-language-documentation"></a><span data-ttu-id="5657d-173">Documentation sur le langage de requête Access</span><span class="sxs-lookup"><span data-stu-id="5657d-173">Access query language documentation</span></span>

<span data-ttu-id="5657d-174">Pour plus d’informations sur le langage de requête Kusto et les opérateurs pris en charge, voir [documentation sur le langage de requête Kusto](https://docs.microsoft.com/azure/kusto/query/).</span><span class="sxs-lookup"><span data-stu-id="5657d-174">For more information on Kusto query language and supported operators, see [Kusto query language documentation](https://docs.microsoft.com/azure/kusto/query/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5657d-175">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="5657d-175">Related topics</span></span>
- [<span data-ttu-id="5657d-176">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="5657d-176">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="5657d-177">Travailler avec les résultats de la requête</span><span class="sxs-lookup"><span data-stu-id="5657d-177">Work with query results</span></span>](advanced-hunting-query-results.md)
- [<span data-ttu-id="5657d-178">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="5657d-178">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="5657d-179">Repérer les menaces sur divers appareils et e-mails</span><span class="sxs-lookup"><span data-stu-id="5657d-179">Hunt for threats across devices and emails</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="5657d-180">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="5657d-180">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="5657d-181">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="5657d-181">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
