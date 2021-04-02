---
title: Découvrir le langage de requête de repérage avancé
description: Créez votre première requête de repérage de menace et découvrez les opérateurs communs et les autres aspects du langage de requête de repérage avancé
keywords: repérage avancé, repérage de menace, repérage de cybermenace, mdatp, microsoft defender atp, recherche wdatp, requête, langue, apprendre, première requête, télémétrie, événements, télémétrie, détections personnalisées, schéma, kusto, opérateurs, types de données
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
ms.openlocfilehash: af612a051f133e4846e04033ab35ea39769d0193
ms.sourcegitcommit: 582555d2b4ef5f2e2494ffdeab2c1d49e5d6b724
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51499545"
---
# <a name="learn-the-advanced-hunting-query-language"></a><span data-ttu-id="58256-104">Découvrir le langage de requête de repérage avancé</span><span class="sxs-lookup"><span data-stu-id="58256-104">Learn the advanced hunting query language</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="58256-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="58256-105">**Applies to:**</span></span>
- [<span data-ttu-id="58256-106">Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="58256-106">Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)

> <span data-ttu-id="58256-107">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="58256-107">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="58256-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="58256-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-advancedhunting-abovefoldlink)

<span data-ttu-id="58256-109">Le repérage avancé est basé sur le [langage de requête Kusto](https://docs.microsoft.com/azure/kusto/query/).</span><span class="sxs-lookup"><span data-stu-id="58256-109">Advanced hunting is based on the [Kusto query language](https://docs.microsoft.com/azure/kusto/query/).</span></span> <span data-ttu-id="58256-110">Vous pouvez utiliser des opérateurs et des instructions Kusto pour créer des requêtes qui recherchent des informations dans un [schéma spécialisé.](advanced-hunting-schema-reference.md)</span><span class="sxs-lookup"><span data-stu-id="58256-110">You can use Kusto operators and statements to construct queries that locate information in a specialized [schema](advanced-hunting-schema-reference.md).</span></span> <span data-ttu-id="58256-111">Pour mieux comprendre ces concepts, exécutez votre première requête.</span><span class="sxs-lookup"><span data-stu-id="58256-111">To understand these concepts better, run your first query.</span></span>

## <a name="try-your-first-query"></a><span data-ttu-id="58256-112">Essayez votre première requête</span><span class="sxs-lookup"><span data-stu-id="58256-112">Try your first query</span></span>

<span data-ttu-id="58256-113">Dans le Centre de sécurité Microsoft Defender, allez à la recherche **avancée** pour exécuter votre première requête.</span><span class="sxs-lookup"><span data-stu-id="58256-113">In Microsoft Defender Security Center, go to **Advanced hunting** to run your first query.</span></span> <span data-ttu-id="58256-114">Consultez l’exemple qui suit :</span><span class="sxs-lookup"><span data-stu-id="58256-114">Use the following example:</span></span>

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
<span data-ttu-id="58256-115">**[Exécuter cette requête dans un recherche avancée](https://securitycenter.windows.com/hunting?query=H4sIAAAAAAAEAI2TT0vDQBDF5yz4HUJPFcTqyZsXqyCIBFvxKNGWtpo_NVlbC8XP7m8mado0K5Zls8nkzdu3b2Z70pNAbmUmqYyk4D2UTJYyllwGMmWNGQHrN_NNvsSBzUBrbMFMiWieAx3xDEBl4GL4AuNd8B0bNgARENcdUmIZ3yM5liPwac3bN-YZPGPU5ET1rWDc7Ox4uod8YDp4MzI-GkjlX4Ne2nly0zEkKzFWh4ZE5sSuTN8Ehq5couvEMnvmUAhez-HsRBMipVa_W_OG6vEfGtT12JRHpqV064e1Kx04NsxFzXxW1aFjp_djXmDRPbfY3XMMcLogTz2bWZ2KqmIJI6q6wKe2WYnrRsa9KVeU9kCBBo2v7BzPxF_Bx2DKiqh63SGoRoc6Njti48z_yL71XHQAcgAur6rXRpcqH3l-4knZF23Utsbq2MircEqmw-G__xR1TdZ1r7zb7XLezmx3etkvGr-ze6NdGdW92azUfpcdluWvr-aqbh_nofnqcWI3aYyOsBV7giduRUO7187LMKTT5rxvHHX80_t8IeeMgLquvL7-Ak3q-kz8BAAA&runQuery=true&timeRangeId=week)**</span><span class="sxs-lookup"><span data-stu-id="58256-115">**[Run this query in advanced hunting](https://securitycenter.windows.com/hunting?query=H4sIAAAAAAAEAI2TT0vDQBDF5yz4HUJPFcTqyZsXqyCIBFvxKNGWtpo_NVlbC8XP7m8mado0K5Zls8nkzdu3b2Z70pNAbmUmqYyk4D2UTJYyllwGMmWNGQHrN_NNvsSBzUBrbMFMiWieAx3xDEBl4GL4AuNd8B0bNgARENcdUmIZ3yM5liPwac3bN-YZPGPU5ET1rWDc7Ox4uod8YDp4MzI-GkjlX4Ne2nly0zEkKzFWh4ZE5sSuTN8Ehq5couvEMnvmUAhez-HsRBMipVa_W_OG6vEfGtT12JRHpqV064e1Kx04NsxFzXxW1aFjp_djXmDRPbfY3XMMcLogTz2bWZ2KqmIJI6q6wKe2WYnrRsa9KVeU9kCBBo2v7BzPxF_Bx2DKiqh63SGoRoc6Njti48z_yL71XHQAcgAur6rXRpcqH3l-4knZF23Utsbq2MircEqmw-G__xR1TdZ1r7zb7XLezmx3etkvGr-ze6NdGdW92azUfpcdluWvr-aqbh_nofnqcWI3aYyOsBV7giduRUO7187LMKTT5rxvHHX80_t8IeeMgLquvL7-Ak3q-kz8BAAA&runQuery=true&timeRangeId=week)**</span></span>

### <a name="describe-the-query-and-specify-the-tables-to-search"></a><span data-ttu-id="58256-116">Décrire la requête et spécifier les tables à rechercher</span><span class="sxs-lookup"><span data-stu-id="58256-116">Describe the query and specify the tables to search</span></span>
<span data-ttu-id="58256-117">Un commentaire court a été ajouté au début de la requête pour décrire son objectif.</span><span class="sxs-lookup"><span data-stu-id="58256-117">A short comment has been added to the beginning of the query to describe what it is for.</span></span> <span data-ttu-id="58256-118">Ce commentaire est utile si vous décidez ultérieurement d’enregistrer la requête et de la partager avec d’autres membres de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="58256-118">This comment helps if you later decide to save the query and share it with others in your organization.</span></span>

```kusto
// Finds PowerShell execution events that could involve a download
```
<span data-ttu-id="58256-119">La requête elle-même commence généralement par un nom de table suivi de plusieurs éléments qui commencent par un canal ( `|` ).</span><span class="sxs-lookup"><span data-stu-id="58256-119">The query itself will typically start with a table name followed by several elements that start with a pipe (`|`).</span></span> <span data-ttu-id="58256-120">Dans cet exemple, nous commençons par créer une union de deux tables et, si nécessaire, nous ajoutons des  `DeviceProcessEvents` `DeviceNetworkEvents` éléments canalés.</span><span class="sxs-lookup"><span data-stu-id="58256-120">In this example, we start by creating a union of two tables,  `DeviceProcessEvents` and `DeviceNetworkEvents`, and add piped elements as needed.</span></span>

```kusto
union DeviceProcessEvents, DeviceNetworkEvents
```
### <a name="set-the-time-range"></a><span data-ttu-id="58256-121">Définir la plage de temps</span><span class="sxs-lookup"><span data-stu-id="58256-121">Set the time range</span></span>
<span data-ttu-id="58256-122">Le premier élément canal est un filtre de temps dont l’étendue est limitée aux sept jours précédents.</span><span class="sxs-lookup"><span data-stu-id="58256-122">The first piped element is a time filter scoped to the previous seven days.</span></span> <span data-ttu-id="58256-123">La limitation de la plage de temps permet de s’assurer que les requêtes s’exécutent bien, retournent des résultats gérables et n’ont pas de délai d’délai.</span><span class="sxs-lookup"><span data-stu-id="58256-123">Limiting the time range helps ensure that queries perform well, return manageable results, and don't time out.</span></span>

```kusto
| where Timestamp > ago(7d)
```

### <a name="check-specific-processes"></a><span data-ttu-id="58256-124">Vérifier des processus spécifiques</span><span class="sxs-lookup"><span data-stu-id="58256-124">Check specific processes</span></span>
<span data-ttu-id="58256-125">La période est immédiatement suivie d’une recherche de noms de fichiers de processus représentant l’application PowerShell.</span><span class="sxs-lookup"><span data-stu-id="58256-125">The time range is immediately followed by a search for process file names representing the PowerShell application.</span></span>

```kusto
// Pivoting on PowerShell processes
| where FileName in~ ("powershell.exe", "powershell_ise.exe")
```

### <a name="search-for-specific-command-strings"></a><span data-ttu-id="58256-126">Rechercher des chaînes de commandes spécifiques</span><span class="sxs-lookup"><span data-stu-id="58256-126">Search for specific command strings</span></span>
<span data-ttu-id="58256-127">Ensuite, la requête recherche des chaînes dans les lignes de commande qui sont généralement utilisées pour télécharger des fichiers à l’aide de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="58256-127">Afterwards, the query looks for strings in command lines that are typically used to download files using PowerShell.</span></span>

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

### <a name="customize-result-columns-and-length"></a><span data-ttu-id="58256-128">Personnaliser les colonnes de résultats et la longueur</span><span class="sxs-lookup"><span data-stu-id="58256-128">Customize result columns and length</span></span> 
<span data-ttu-id="58256-129">Maintenant que votre requête identifie clairement les données que vous souhaitez localiser, vous pouvez définir à quoi ressemblent les résultats.</span><span class="sxs-lookup"><span data-stu-id="58256-129">Now that your query clearly identifies the data you want to locate, you can define what the results look like.</span></span> <span data-ttu-id="58256-130">`project` renvoie des `top` colonnes spécifiques et limite le nombre de résultats.</span><span class="sxs-lookup"><span data-stu-id="58256-130">`project` returns specific columns, and `top` limits the number of results.</span></span> <span data-ttu-id="58256-131">Ces opérateurs permettent de s’assurer que les résultats sont bien formatés, raisonnablement grands et faciles à traiter.</span><span class="sxs-lookup"><span data-stu-id="58256-131">These operators help ensure the results are well-formatted and reasonably large and easy to process.</span></span>

```kusto
| project Timestamp, DeviceName, InitiatingProcessFileName, InitiatingProcessCommandLine, 
FileName, ProcessCommandLine, RemoteIP, RemoteUrl, RemotePort, RemoteIPType
| top 100 by Timestamp
```

<span data-ttu-id="58256-132">Sélectionnez **Exécuter la requête** pour voir les résultats.</span><span class="sxs-lookup"><span data-stu-id="58256-132">Select **Run query** to see the results.</span></span> <span data-ttu-id="58256-133">Utilisez l’icône développer en haut à droite de l’éditeur de requête pour vous concentrer sur votre requête de recherche et les résultats.</span><span class="sxs-lookup"><span data-stu-id="58256-133">Use the expand icon at the top right of the query editor to focus on your hunting query and the results.</span></span> 

![Image du contrôle Développer dans l’éditeur de requête de recherche avancée](images/advanced-hunting-expand.png)

>[!TIP]
><span data-ttu-id="58256-135">Vous pouvez afficher les résultats de la requête sous la mesure de graphiques et ajuster rapidement les filtres.</span><span class="sxs-lookup"><span data-stu-id="58256-135">You can view query results as charts and quickly adjust filters.</span></span> <span data-ttu-id="58256-136">Pour obtenir des [conseils, voir l’aide sur l’working with query results](advanced-hunting-query-results.md)</span><span class="sxs-lookup"><span data-stu-id="58256-136">For guidance, [read about working with query results](advanced-hunting-query-results.md)</span></span>

## <a name="learn-common-query-operators-for-advanced-hunting"></a><span data-ttu-id="58256-137">Découvrir les opérateurs de requête courants pour le repérage avancé</span><span class="sxs-lookup"><span data-stu-id="58256-137">Learn common query operators for advanced hunting</span></span>

<span data-ttu-id="58256-138">Vous viennent d’exécuter votre première requête et vous avez une idée générale de ses composants.</span><span class="sxs-lookup"><span data-stu-id="58256-138">You've just run your first query and have a general idea of its components.</span></span> <span data-ttu-id="58256-139">Il est temps de revenir en arrière légèrement et d’apprendre quelques principes de base.</span><span class="sxs-lookup"><span data-stu-id="58256-139">It's time to backtrack slightly and learn some basics.</span></span> <span data-ttu-id="58256-140">Le langage de requête Kusto utilisé par le repérage avancé prend en charge divers opérateurs, notamment les opérateurs communs suivants.</span><span class="sxs-lookup"><span data-stu-id="58256-140">The Kusto query language used by advanced hunting supports a range of operators, including the following common ones.</span></span>

| <span data-ttu-id="58256-141">Opérateur</span><span class="sxs-lookup"><span data-stu-id="58256-141">Operator</span></span> | <span data-ttu-id="58256-142">Description et utilisation</span><span class="sxs-lookup"><span data-stu-id="58256-142">Description and usage</span></span> |
|--|--|
| `where` | <span data-ttu-id="58256-143">Filtre une table sur le sous-ensemble de lignes qui répondent à un prédicat.</span><span class="sxs-lookup"><span data-stu-id="58256-143">Filter a table to the subset of rows that satisfy a predicate.</span></span> |
| `summarize` | <span data-ttu-id="58256-144">Produit une table qui agrège le contenu de la table d’entrée.</span><span class="sxs-lookup"><span data-stu-id="58256-144">Produce a table that aggregates the content of the input table.</span></span> |
| `join` | <span data-ttu-id="58256-145">Fusionne les lignes de deux tables pour former une nouvelle table en faisant correspondre les valeurs des colonnes spécifiées de chaque table.</span><span class="sxs-lookup"><span data-stu-id="58256-145">Merge the rows of two tables to form a new table by matching values of the specified column(s) from each table.</span></span> |
| `count` | <span data-ttu-id="58256-146">Renvoie le nombre d’enregistrements dans le groupe d’enregistrements d’entrée.</span><span class="sxs-lookup"><span data-stu-id="58256-146">Return the number of records in the input record set.</span></span> |
| `top` | <span data-ttu-id="58256-147">Renvoie les N premiers enregistrements triés par les colonnes spécifiées.</span><span class="sxs-lookup"><span data-stu-id="58256-147">Return the first N records sorted by the specified columns.</span></span> |
| `limit` | <span data-ttu-id="58256-148">Renvoie jusqu’au nombre de lignes spécifié.</span><span class="sxs-lookup"><span data-stu-id="58256-148">Return up to the specified number of rows.</span></span> |
| `project` | <span data-ttu-id="58256-149">Sélectionne les colonnes à inclure, renommer ou déplacer et insère de nouvelles colonnes calculées.</span><span class="sxs-lookup"><span data-stu-id="58256-149">Select the columns to include, rename or drop, and insert new computed columns.</span></span> |
| `extend` | <span data-ttu-id="58256-150">Crée des colonnes calculées et les ajoute au jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="58256-150">Create calculated columns and append them to the result set.</span></span> |
| `makeset` |  <span data-ttu-id="58256-151">Renvoie un tableau dynamique (JSON) de l’ensemble de valeurs distinctes prise par Expr dans le groupe.</span><span class="sxs-lookup"><span data-stu-id="58256-151">Return a dynamic (JSON) array of the set of distinct values that Expr takes in the group.</span></span> |
| `find` | <span data-ttu-id="58256-152">Recherche des lignes qui correspondent à un prédicat dans un ensemble de tables.</span><span class="sxs-lookup"><span data-stu-id="58256-152">Find rows that match a predicate across a set of tables.</span></span> |

<span data-ttu-id="58256-153">Pour voir un exemple en direct de ces opérateurs, exécutez-les à partir de la **section** Commencer de la page de recherche avancée.</span><span class="sxs-lookup"><span data-stu-id="58256-153">To see a live example of these operators, run them from the **Get started** section of the advanced hunting page.</span></span>

## <a name="understand-data-types"></a><span data-ttu-id="58256-154">Comprendre les types de données</span><span class="sxs-lookup"><span data-stu-id="58256-154">Understand data types</span></span>

<span data-ttu-id="58256-155">Le recherche avancée prend en charge les types de données Kusto, y compris les types courants suivants :</span><span class="sxs-lookup"><span data-stu-id="58256-155">Advanced hunting supports Kusto data types, including the following common types:</span></span>

| <span data-ttu-id="58256-156">Type de données</span><span class="sxs-lookup"><span data-stu-id="58256-156">Data type</span></span> | <span data-ttu-id="58256-157">Description et implications dans les requêtes</span><span class="sxs-lookup"><span data-stu-id="58256-157">Description and query implications</span></span> |
|--|--|
| `datetime` | <span data-ttu-id="58256-158">Les données et les informations d’heure représentent généralement des timestamps d’événement.</span><span class="sxs-lookup"><span data-stu-id="58256-158">Data and time information typically representing event timestamps.</span></span> [<span data-ttu-id="58256-159">Voir les formats de date/heure pris en charge</span><span class="sxs-lookup"><span data-stu-id="58256-159">See supported datetime formats</span></span>](https://docs.microsoft.com/azure/data-explorer/kusto/query/scalar-data-types/datetime) |
| `string` | <span data-ttu-id="58256-160">Chaîne de caractères en UTF-8 entre guillemets simples ( `'` ) ou guillemets doubles ( `"` ).</span><span class="sxs-lookup"><span data-stu-id="58256-160">Character string in UTF-8 enclosed in single quotes (`'`) or double quotes (`"`).</span></span> [<span data-ttu-id="58256-161">En savoir plus sur les chaînes</span><span class="sxs-lookup"><span data-stu-id="58256-161">Read more about strings</span></span>](https://docs.microsoft.com/azure/data-explorer/kusto/query/scalar-data-types/string) |
| `bool` | <span data-ttu-id="58256-162">Ce type de données prend en charge `true` ou `false` indique.</span><span class="sxs-lookup"><span data-stu-id="58256-162">This data type supports `true` or `false` states.</span></span> [<span data-ttu-id="58256-163">Voir les opérateurs et les littéraux pris en charge</span><span class="sxs-lookup"><span data-stu-id="58256-163">See supported literals and operators</span></span>](https://docs.microsoft.com/azure/data-explorer/kusto/query/scalar-data-types/bool) |
| `int` | <span data-ttu-id="58256-164">Integer 32 bits</span><span class="sxs-lookup"><span data-stu-id="58256-164">32-bit integer</span></span>  |
| `long` | <span data-ttu-id="58256-165">Integer 64 bits</span><span class="sxs-lookup"><span data-stu-id="58256-165">64-bit integer</span></span> |

<span data-ttu-id="58256-166">Pour en savoir plus sur ces types de données, consultez les types de données [scalar Kusto.](https://docs.microsoft.com/azure/data-explorer/kusto/query/scalar-data-types/)</span><span class="sxs-lookup"><span data-stu-id="58256-166">To learn more about these data types, [read about Kusto scalar data types](https://docs.microsoft.com/azure/data-explorer/kusto/query/scalar-data-types/).</span></span>

## <a name="get-help-as-you-write-queries"></a><span data-ttu-id="58256-167">Obtenez de l’aide lorsque vous rédigez des requêtes</span><span class="sxs-lookup"><span data-stu-id="58256-167">Get help as you write queries</span></span>
<span data-ttu-id="58256-168">Tirez parti des fonctionnalités suivantes pour rédiger des requêtes plus rapidement :</span><span class="sxs-lookup"><span data-stu-id="58256-168">Take advantage of the following functionality to write queries faster:</span></span>

- <span data-ttu-id="58256-169">**Suggestion automatique : lorsque** vous écrivez des requêtes, le recherche avancée fournit des suggestions de IntelliSense.</span><span class="sxs-lookup"><span data-stu-id="58256-169">**Autosuggest**—as you write queries, advanced hunting provides suggestions from IntelliSense.</span></span>
- <span data-ttu-id="58256-170">**Arborescence de schéma**: une représentation de schéma qui inclut la liste des tableaux et leurs colonnes est fournie en de côté de votre zone de travail.</span><span class="sxs-lookup"><span data-stu-id="58256-170">**Schema tree**—a schema representation that includes the list of tables and their columns is provided next to your working area.</span></span> <span data-ttu-id="58256-171">Si vous souhaitez en savoir plus, veuillez placer le pointeur sur un élément.</span><span class="sxs-lookup"><span data-stu-id="58256-171">For more information, hover over an item.</span></span> <span data-ttu-id="58256-172">Double-cliquez sur un élément pour l’insérer dans l’éditeur de requête.</span><span class="sxs-lookup"><span data-stu-id="58256-172">Double-click an item to insert it to the query editor.</span></span>
- <span data-ttu-id="58256-173">**[Référence de schéma :](advanced-hunting-schema-reference.md#get-schema-information-in-the-security-center)** référence dans le portail avec des descriptions de tableau et de colonne, ainsi que des types d’événements pris en charge (valeurs) et `ActionType` des exemples de requêtes</span><span class="sxs-lookup"><span data-stu-id="58256-173">**[Schema reference](advanced-hunting-schema-reference.md#get-schema-information-in-the-security-center)**—in-portal reference with table and column descriptions as well as supported event types (`ActionType` values) and sample queries</span></span>

## <a name="work-with-multiple-queries-in-the-editor"></a><span data-ttu-id="58256-174">Utilisation de plusieurs requêtes dans l’éditeur</span><span class="sxs-lookup"><span data-stu-id="58256-174">Work with multiple queries in the editor</span></span>
<span data-ttu-id="58256-175">Vous pouvez utiliser l’éditeur de requête pour expérimenter plusieurs requêtes.</span><span class="sxs-lookup"><span data-stu-id="58256-175">You can use the query editor to experiment with multiple queries.</span></span> <span data-ttu-id="58256-176">Pour utiliser plusieurs requêtes :</span><span class="sxs-lookup"><span data-stu-id="58256-176">To use multiple queries:</span></span>

- <span data-ttu-id="58256-177">Séparez chaque requête par une ligne vide.</span><span class="sxs-lookup"><span data-stu-id="58256-177">Separate each query with an empty line.</span></span>
- <span data-ttu-id="58256-178">Placez le curseur sur n’importe quelle partie d’une requête pour sélectionner cette requête avant de l’exécutez.</span><span class="sxs-lookup"><span data-stu-id="58256-178">Place the cursor on any part of a query to select that query before running it.</span></span> <span data-ttu-id="58256-179">Cette requête n’exécutera que la requête sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="58256-179">This will run only the selected query.</span></span> <span data-ttu-id="58256-180">Pour exécuter une autre requête, déplacez le curseur en conséquence et sélectionnez **Exécuter la requête.**</span><span class="sxs-lookup"><span data-stu-id="58256-180">To run another query, move the cursor accordingly and select **Run query**.</span></span>

<span data-ttu-id="58256-181">![Image de l’éditeur de requête de recherche avancée avec l’éditeur de requêtes multiples avec ](images/ah-multi-query.png)
 _plusieurs requêtes_</span><span class="sxs-lookup"><span data-stu-id="58256-181">![Image of the advanced hunting query editor with multiple queries](images/ah-multi-query.png)
_Query editor with multiple queries_</span></span>

## <a name="use-sample-queries"></a><span data-ttu-id="58256-182">Utiliser des exemples de requêtes</span><span class="sxs-lookup"><span data-stu-id="58256-182">Use sample queries</span></span>

<span data-ttu-id="58256-183">La section **Prise en main** fournit quelques requêtes simples utilisant des opérateurs fréquemment utilisés.</span><span class="sxs-lookup"><span data-stu-id="58256-183">The **Get started** section provides a few simple queries using commonly used operators.</span></span> <span data-ttu-id="58256-184">Essayez d’exécuter ces requêtes et de leur apporter de légères modifications.</span><span class="sxs-lookup"><span data-stu-id="58256-184">Try running these queries and making small modifications to them.</span></span>

![Image de l’onglet De mise en place du recherche avancée](images/atp-advanced-hunting.png)

> [!NOTE]
> <span data-ttu-id="58256-186">Hormis les exemples de requête de base, vous pouvez également accéder à des [requêtes partagées](advanced-hunting-shared-queries.md) pour des scénarios de repérage de menace spécifiques.</span><span class="sxs-lookup"><span data-stu-id="58256-186">Apart from the basic query samples, you can also access [shared queries](advanced-hunting-shared-queries.md) for specific threat hunting scenarios.</span></span> <span data-ttu-id="58256-187">Explorez les requêtes partagées sur le côté gauche de la page ou le référentiel de requêtes [GitHub.](https://aka.ms/hunting-queries)</span><span class="sxs-lookup"><span data-stu-id="58256-187">Explore the shared queries on the left side of the page or the [GitHub query repository](https://aka.ms/hunting-queries).</span></span>

## <a name="access-comprehensive-query-language-reference"></a><span data-ttu-id="58256-188">Accéder à une référence de langage de requête complète</span><span class="sxs-lookup"><span data-stu-id="58256-188">Access comprehensive query language reference</span></span>

<span data-ttu-id="58256-189">Pour plus d’informations sur le langage de requête, voir la documentation du langage de requête [Kusto.](https://docs.microsoft.com/azure/kusto/query/)</span><span class="sxs-lookup"><span data-stu-id="58256-189">For detailed information about the query language, see [Kusto query language documentation](https://docs.microsoft.com/azure/kusto/query/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="58256-190">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58256-190">Related topics</span></span>
- [<span data-ttu-id="58256-191">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="58256-191">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="58256-192">Utiliser les résultats d’une requête</span><span class="sxs-lookup"><span data-stu-id="58256-192">Work with query results</span></span>](advanced-hunting-query-results.md)
- [<span data-ttu-id="58256-193">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="58256-193">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="58256-194">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="58256-194">Understand the schema</span></span>](advanced-hunting-schema-reference.md)
- [<span data-ttu-id="58256-195">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="58256-195">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
