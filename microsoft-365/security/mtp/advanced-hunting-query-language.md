---
title: Découvrez le langage de requête de repérage avancé dans la Protection Microsoft contre les menaces
description: Créez votre première requête de repérage de menace et découvrez les opérateurs communs et les autres aspects du langage de requête de repérage avancé
keywords: recherche avancée, recherche de menace, recherche dans les menaces informatiques, protection contre les menaces Microsoft, Microsoft 365, MTP, M365, recherche, requête, langue, apprentissage, première requête, télémétrie, événements, télémétrie, détections personnalisées, schéma, Kusto, opérateurs, types de données, PowerShell exemple de téléchargement, de requête
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
ms.openlocfilehash: 7f2cf7f62060774343354467d27b76456f6581fc
ms.sourcegitcommit: cc3b64a91e16ccdaa9c338b9a9056dbe3963ba9e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2020
ms.locfileid: "42567027"
---
# <a name="learn-the-advanced-hunting-query-language"></a><span data-ttu-id="adc2e-104">Découvrir le langage de requête de repérage avancé</span><span class="sxs-lookup"><span data-stu-id="adc2e-104">Learn the advanced hunting query language</span></span>

<span data-ttu-id="adc2e-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="adc2e-105">**Applies to:**</span></span>
- <span data-ttu-id="adc2e-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="adc2e-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="adc2e-107">Le repérage avancé est basé sur le [langage de requête Kusto](https://docs.microsoft.com/azure/kusto/query/).</span><span class="sxs-lookup"><span data-stu-id="adc2e-107">Advanced hunting is based on the [Kusto query language](https://docs.microsoft.com/azure/kusto/query/).</span></span> <span data-ttu-id="adc2e-108">Vous pouvez utiliser la syntaxe et les opérateurs Kusto pour créer des requêtes qui recherchent des informations dans le [schéma](advanced-hunting-schema-tables.md) spécifiquement structuré pour un repérage avancé.</span><span class="sxs-lookup"><span data-stu-id="adc2e-108">You can use Kusto syntax and operators to construct queries that locate information in the [schema](advanced-hunting-schema-tables.md) specifically structured for advanced hunting.</span></span> <span data-ttu-id="adc2e-109">Pour mieux comprendre ces concepts, exécutez votre première requête.</span><span class="sxs-lookup"><span data-stu-id="adc2e-109">To understand these concepts better, run your first query.</span></span>

## <a name="try-your-first-query"></a><span data-ttu-id="adc2e-110">Essayez votre première requête</span><span class="sxs-lookup"><span data-stu-id="adc2e-110">Try your first query</span></span>

<span data-ttu-id="adc2e-111">Dans le centre de sécurité Microsoft 365, accédez à la **recherche pour exécuter** votre première requête.</span><span class="sxs-lookup"><span data-stu-id="adc2e-111">In Microsoft 365 security center, go to **Hunting** to run your first query.</span></span> <span data-ttu-id="adc2e-112">Consultez l’exemple qui suit :</span><span class="sxs-lookup"><span data-stu-id="adc2e-112">Use the following example:</span></span>

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

<span data-ttu-id="adc2e-113">Voici son futur aspect dans le repérage avancé.</span><span class="sxs-lookup"><span data-stu-id="adc2e-113">This is how it will look like in advanced hunting.</span></span>

![Image de la requête de recherche avancée Microsoft Threat Protection](../../media/advanced-hunting-query-example.png)

<span data-ttu-id="adc2e-115">Un bref commentaire a été ajouté au début de la requête pour décrire sa fonction.</span><span class="sxs-lookup"><span data-stu-id="adc2e-115">A short comment has been added to the beginning of the query to describe what it is for.</span></span> <span data-ttu-id="adc2e-116">Cela vous permet de décider ultérieurement d’enregistrer la requête et de la partager avec d’autres membres de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="adc2e-116">This helps if you later decide to save the query and share it with others in your organization.</span></span> 

```kusto
// Finds PowerShell execution events that could involve a download
```

<span data-ttu-id="adc2e-117">La requête elle-même commence généralement par un nom de table suivi d’une série d’éléments commençant par une barre verticale (`|`).</span><span class="sxs-lookup"><span data-stu-id="adc2e-117">The query itself will typically start with a table name followed by a series of elements started by a pipe (`|`).</span></span> <span data-ttu-id="adc2e-118">Dans cet exemple, nous commençons par créer une Union de deux tables `DeviceProcessEvents` , `DeviceNetworkEvents`et et ajoutons des éléments redirigés selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="adc2e-118">In this example, we start by creating a union of two tables,  `DeviceProcessEvents` and `DeviceNetworkEvents`, and add piped elements as needed.</span></span>

```kusto
union DeviceProcessEvents, DeviceNetworkEvents
```
<span data-ttu-id="adc2e-119">Le premier élément Redirigé est un filtre temporel étendu aux sept jours précédents.</span><span class="sxs-lookup"><span data-stu-id="adc2e-119">The first piped element is a time filter scoped to the previous seven days.</span></span> <span data-ttu-id="adc2e-120">La conservation d’un intervalle de temps le plus étroit possible permet de s’assurer que les requêtes fonctionnent bien, renvoient des résultats gérables et n’expirent pas.</span><span class="sxs-lookup"><span data-stu-id="adc2e-120">Keeping the time range as narrow as possible ensures that queries perform well, return manageable results, and don't time out.</span></span>

```kusto
| where Timestamp > ago(7d)
```

<span data-ttu-id="adc2e-121">La plage horaire est immédiatement suivie d’une recherche de noms de fichiers de processus représentant l’application PowerShell.</span><span class="sxs-lookup"><span data-stu-id="adc2e-121">The time range is immediately followed by a search for process file names representing the PowerShell application.</span></span>

```
// Pivoting on PowerShell processes
| where FileName in~ ("powershell.exe", "powershell_ise.exe")
```

<span data-ttu-id="adc2e-122">Ensuite, la requête recherche des chaînes dans les lignes de commande qui sont généralement utilisées pour télécharger des fichiers à l’aide de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="adc2e-122">Afterwards, the query looks for strings in command lines that are typically used to download files using PowerShell.</span></span>

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
<span data-ttu-id="adc2e-123">Maintenant que votre requête identifie clairement les données que vous recherchez, vous pouvez ajouter des éléments qui définissent l’apparence des résultats.</span><span class="sxs-lookup"><span data-stu-id="adc2e-123">Now that your query clearly identifies the data you want to locate, you can add elements that define what the results look like.</span></span> <span data-ttu-id="adc2e-124">`project`renvoie des colonnes spécifiques `top` et limite le nombre de résultats, ce qui permet de s’assurer que les résultats sont bien formatés et raisonnablement volumineux et faciles à traiter.</span><span class="sxs-lookup"><span data-stu-id="adc2e-124">`project` returns specific columns and `top` limits the number of results, helping ensure the results well-formatted and reasonably large and easy to process.</span></span>

```kusto
| project Timestamp, DeviceName, InitiatingProcessFileName, InitiatingProcessCommandLine, 
FileName, ProcessCommandLine, RemoteIP, RemoteUrl, RemotePort, RemoteIPType
| top 100 by Timestamp
```

<span data-ttu-id="adc2e-125">Cliquez sur **Exécuter la requête** pour afficher les résultats.</span><span class="sxs-lookup"><span data-stu-id="adc2e-125">Click **Run query** to see the results.</span></span> <span data-ttu-id="adc2e-126">Sélectionnez l’icône développer en haut à droite de l’éditeur de requête pour vous concentrer sur votre requête de recherche et les résultats.</span><span class="sxs-lookup"><span data-stu-id="adc2e-126">Select the expand icon at the top right of the query editor to focus on your hunting query and the results.</span></span>

![Image du contrôle Expand dans l’éditeur de requête de recherche avancée](../../media/advanced-hunting-expand.png)

## <a name="learn-common-query-operators-for-advanced-hunting"></a><span data-ttu-id="adc2e-128">Découvrir les opérateurs de requête courants pour le repérage avancé</span><span class="sxs-lookup"><span data-stu-id="adc2e-128">Learn common query operators for advanced hunting</span></span>

<span data-ttu-id="adc2e-129">Maintenant que vous avez exécuté votre première requête et que vous avez une idée générale de ses composants, il est temps de revenir en arrière pour découvrir quelques notions de base.</span><span class="sxs-lookup"><span data-stu-id="adc2e-129">Now that you've run your first query and have a general idea of its components, it's time to backtrack a little bit and learn some basics.</span></span> <span data-ttu-id="adc2e-130">Le langage de requête Kusto utilisé par le repérage avancé prend en charge divers opérateurs, notamment les opérateurs communs suivants.</span><span class="sxs-lookup"><span data-stu-id="adc2e-130">The Kusto query language used by advanced hunting supports a range of operators, including the following common ones.</span></span>

| <span data-ttu-id="adc2e-131">Opérateur</span><span class="sxs-lookup"><span data-stu-id="adc2e-131">Operator</span></span> | <span data-ttu-id="adc2e-132">Description et utilisation</span><span class="sxs-lookup"><span data-stu-id="adc2e-132">Description and usage</span></span> |
|--|--|
| `where` | <span data-ttu-id="adc2e-133">Filtre une table sur le sous-ensemble de lignes qui répondent à un prédicat.</span><span class="sxs-lookup"><span data-stu-id="adc2e-133">Filter a table to the subset of rows that satisfy a predicate.</span></span> |
| `summarize` | <span data-ttu-id="adc2e-134">Produit une table qui agrège le contenu de la table d’entrée.</span><span class="sxs-lookup"><span data-stu-id="adc2e-134">Produce a table that aggregates the content of the input table.</span></span> |
| `join` | <span data-ttu-id="adc2e-135">Fusionne les lignes de deux tables pour former une nouvelle table en faisant correspondre les valeurs des colonnes spécifiées de chaque table.</span><span class="sxs-lookup"><span data-stu-id="adc2e-135">Merge the rows of two tables to form a new table by matching values of the specified column(s) from each table.</span></span> |
| `count` | <span data-ttu-id="adc2e-136">Renvoie le nombre d’enregistrements dans le groupe d’enregistrements d’entrée.</span><span class="sxs-lookup"><span data-stu-id="adc2e-136">Return the number of records in the input record set.</span></span> |
| `top` | <span data-ttu-id="adc2e-137">Renvoie les N premiers enregistrements triés par les colonnes spécifiées.</span><span class="sxs-lookup"><span data-stu-id="adc2e-137">Return the first N records sorted by the specified columns.</span></span> |
| `limit` | <span data-ttu-id="adc2e-138">Renvoie jusqu’au nombre de lignes spécifié.</span><span class="sxs-lookup"><span data-stu-id="adc2e-138">Return up to the specified number of rows.</span></span> |
| `project` | <span data-ttu-id="adc2e-139">Sélectionne les colonnes à inclure, renommer ou déplacer et insère de nouvelles colonnes calculées.</span><span class="sxs-lookup"><span data-stu-id="adc2e-139">Select the columns to include, rename or drop, and insert new computed columns.</span></span> |
| `extend` | <span data-ttu-id="adc2e-140">Crée des colonnes calculées et les ajoute au jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="adc2e-140">Create calculated columns and append them to the result set.</span></span> |
| `makeset` |  <span data-ttu-id="adc2e-141">Renvoie un tableau dynamique (JSON) de l’ensemble de valeurs distinctes prise par Expr dans le groupe.</span><span class="sxs-lookup"><span data-stu-id="adc2e-141">Return a dynamic (JSON) array of the set of distinct values that Expr takes in the group.</span></span> |
| `find` | <span data-ttu-id="adc2e-142">Recherche des lignes qui correspondent à un prédicat dans un ensemble de tables.</span><span class="sxs-lookup"><span data-stu-id="adc2e-142">Find rows that match a predicate across a set of tables.</span></span> |

<span data-ttu-id="adc2e-143">Pour voir un exemple parlant de ces opérateurs, exécutez-les à partir de la section **Prise en main** du repérage avancé.</span><span class="sxs-lookup"><span data-stu-id="adc2e-143">To see a live example of these operators, run them from the **Get started** section in advanced hunting.</span></span>

## <a name="understand-data-types-and-their-query-syntax-implications"></a><span data-ttu-id="adc2e-144">Comprendre les types de données et leurs implications dans la syntaxe de requête</span><span class="sxs-lookup"><span data-stu-id="adc2e-144">Understand data types and their query syntax implications</span></span>

<span data-ttu-id="adc2e-145">Les données des tables de repérage avancé sont généralement classées dans les types de données suivants.</span><span class="sxs-lookup"><span data-stu-id="adc2e-145">Data in advanced hunting tables are generally classified into the following data types.</span></span>

| <span data-ttu-id="adc2e-146">Type de données</span><span class="sxs-lookup"><span data-stu-id="adc2e-146">Data type</span></span> | <span data-ttu-id="adc2e-147">Description et implications dans les requêtes</span><span class="sxs-lookup"><span data-stu-id="adc2e-147">Description and query implications</span></span> |
|--|--|
| `datetime` | <span data-ttu-id="adc2e-148">Informations sur les données et les heures représentant généralement les horodatages d’événement</span><span class="sxs-lookup"><span data-stu-id="adc2e-148">Data and time information typically representing event timestamps</span></span> |
| `string` | <span data-ttu-id="adc2e-149">Chaîne de caractères</span><span class="sxs-lookup"><span data-stu-id="adc2e-149">Character string</span></span> |
| `bool` | <span data-ttu-id="adc2e-150">True ou false</span><span class="sxs-lookup"><span data-stu-id="adc2e-150">True or false</span></span> |
| `int` | <span data-ttu-id="adc2e-151">Valeur numérique de 32 bits</span><span class="sxs-lookup"><span data-stu-id="adc2e-151">32-bit numeric value</span></span>  |
| `long` | <span data-ttu-id="adc2e-152">Valeur numérique de 64 bits</span><span class="sxs-lookup"><span data-stu-id="adc2e-152">64-bit numeric value</span></span> |

## <a name="use-sample-queries"></a><span data-ttu-id="adc2e-153">Utiliser des exemples de requêtes</span><span class="sxs-lookup"><span data-stu-id="adc2e-153">Use sample queries</span></span>

<span data-ttu-id="adc2e-154">La section **Prise en main** fournit quelques requêtes simples utilisant des opérateurs fréquemment utilisés.</span><span class="sxs-lookup"><span data-stu-id="adc2e-154">The **Get started** section provides a few simple queries using commonly used operators.</span></span> <span data-ttu-id="adc2e-155">Essayez d’exécuter ces requêtes et de leur apporter de légères modifications.</span><span class="sxs-lookup"><span data-stu-id="adc2e-155">Try running these queries and making small modifications to them.</span></span>

![Image d’une fenêtre de repérage avancé](../../media/advanced-hunting-get-started.png)

>[!NOTE]
><span data-ttu-id="adc2e-157">Hormis les exemples de requête de base, vous pouvez également accéder à des [requêtes partagées](advanced-hunting-shared-queries.md) pour des scénarios de repérage de menace spécifiques.</span><span class="sxs-lookup"><span data-stu-id="adc2e-157">Apart from the basic query samples, you can also access [shared queries](advanced-hunting-shared-queries.md) for specific threat hunting scenarios.</span></span> <span data-ttu-id="adc2e-158">Explorez les requêtes partagées sur le côté gauche de la page ou le référentiel de requête GitHub.</span><span class="sxs-lookup"><span data-stu-id="adc2e-158">Explore the shared queries on the left side of the page or the GitHub query repository.</span></span>

## <a name="access-query-language-documentation"></a><span data-ttu-id="adc2e-159">Documentation sur le langage de requête Access</span><span class="sxs-lookup"><span data-stu-id="adc2e-159">Access query language documentation</span></span>

<span data-ttu-id="adc2e-160">Pour plus d’informations sur le langage de requête Kusto et les opérateurs pris en charge, voir [documentation sur le langage de requête Kusto](https://docs.microsoft.com/azure/kusto/query/).</span><span class="sxs-lookup"><span data-stu-id="adc2e-160">For more information on Kusto query language and supported operators, see [Kusto query language documentation](https://docs.microsoft.com/azure/kusto/query/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="adc2e-161">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="adc2e-161">Related topics</span></span>
- [<span data-ttu-id="adc2e-162">Repérage proactif des menaces</span><span class="sxs-lookup"><span data-stu-id="adc2e-162">Proactively hunt for threats</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="adc2e-163">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="adc2e-163">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="adc2e-164">Repérer les menaces sur divers appareils et e-mails</span><span class="sxs-lookup"><span data-stu-id="adc2e-164">Hunt for threats across devices and emails</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="adc2e-165">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="adc2e-165">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="adc2e-166">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="adc2e-166">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
