---
title: Découvrez le langage de requête de repérage avancé dans la Protection Microsoft contre les menaces
description: Créez votre première requête de repérage de menace et découvrez les opérateurs communs et les autres aspects du langage de requête de repérage avancé
keywords: chasse de menace, recherche de menace, recherche de menace informatique, protection contre les menaces Microsoft, Microsoft 365, MTP, M365, recherche, requête, langue, apprentissage, première requête, télémétrie, événements, télémétrie, détections personnalisées, schéma, Kusto, opérateurs, types de données
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: lomayor
author: lomayor
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.openlocfilehash: 36f2efb733e8403b30e0ecc406bb1ea2d6a6248e
ms.sourcegitcommit: 5b8e9935fe7bfcb96b8f8356119ce23152bd16a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2020
ms.locfileid: "41210339"
---
# <a name="learn-the-advanced-hunting-query-language"></a><span data-ttu-id="60223-104">Découvrir le langage de requête de repérage avancé</span><span class="sxs-lookup"><span data-stu-id="60223-104">Learn the advanced hunting query language</span></span>

<span data-ttu-id="60223-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="60223-105">**Applies to:**</span></span>
- <span data-ttu-id="60223-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="60223-106">Microsoft Threat Protection</span></span>

[!INCLUDE [Prerelease information](../includes/prerelease.md)]

<span data-ttu-id="60223-107">Le repérage avancé est basé sur le [langage de requête Kusto](https://docs.microsoft.com/azure/kusto/query/).</span><span class="sxs-lookup"><span data-stu-id="60223-107">Advanced hunting is based on the [Kusto query language](https://docs.microsoft.com/azure/kusto/query/).</span></span> <span data-ttu-id="60223-108">Vous pouvez utiliser la syntaxe et les opérateurs Kusto pour créer des requêtes qui recherchent des informations dans le [schéma](advanced-hunting-schema-tables.md) spécifiquement structuré pour un repérage avancé.</span><span class="sxs-lookup"><span data-stu-id="60223-108">You can use Kusto syntax and operators to construct queries that locate information in the [schema](advanced-hunting-schema-tables.md) specifically structured for advanced hunting.</span></span> <span data-ttu-id="60223-109">Pour mieux comprendre ces concepts, exécutez votre première requête.</span><span class="sxs-lookup"><span data-stu-id="60223-109">To understand these concepts better, run your first query.</span></span>

## <a name="try-your-first-query"></a><span data-ttu-id="60223-110">Essayez votre première requête</span><span class="sxs-lookup"><span data-stu-id="60223-110">Try your first query</span></span>

<span data-ttu-id="60223-111">dans le Centre de sécurité Microsoft 365, placez-vous dans **Repérage** pour exécuter votre première requête.</span><span class="sxs-lookup"><span data-stu-id="60223-111">in the Microsoft 365 security center, go to **Hunting** to run your first query.</span></span> <span data-ttu-id="60223-112">Consultez l’exemple qui suit :</span><span class="sxs-lookup"><span data-stu-id="60223-112">Use the following example:</span></span>

```kusto
// Finds PowerShell execution events that could involve a download.
DeviceProcessEvents 
| where Timestamp > ago(7d)
| where FileName in ("powershell.exe", "POWERSHELL.EXE", "powershell_ise.exe", "POWERSHELL_ISE.EXE") 
| where ProcessCommandLine has "Net.WebClient"
        or ProcessCommandLine has "DownloadFile"
        or ProcessCommandLine has "Invoke-WebRequest"
        or ProcessCommandLine has "Invoke-Shellcode"
        or ProcessCommandLine contains "http:"
| project Timestamp, DeviceName, InitiatingProcessFileName, FileName, ProcessCommandLine
| top 100 by Timestamp
```

<span data-ttu-id="60223-113">Voici son futur aspect dans le repérage avancé.</span><span class="sxs-lookup"><span data-stu-id="60223-113">This is how it will look like in advanced hunting.</span></span>

![Image de la requête de repérage avancé Microsoft Defender – Protection avancée contre les menaces](../images/advanced-hunting-query-example.png)

<span data-ttu-id="60223-115">La requête commence par un bref commentaire décrivant sa fonction.</span><span class="sxs-lookup"><span data-stu-id="60223-115">The query starts with a short comment describing what it is for.</span></span> <span data-ttu-id="60223-116">Cela vous permet de choisir ultérieurement d’enregistrer votre requête et de la partager avec d’autres dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="60223-116">This helps if you later decide to save your query and share it with others in your organization.</span></span>

```kusto
// Finds PowerShell execution events that could involve a download.
DeviceProcessEvents
```

<span data-ttu-id="60223-117">La requête elle-même commence généralement par un nom de table suivi d’une série d’éléments commençant par une barre verticale (`|`).</span><span class="sxs-lookup"><span data-stu-id="60223-117">The query itself will typically start with a table name followed by a series of elements started by a pipe (`|`).</span></span> <span data-ttu-id="60223-118">Dans cet exemple, nous commençons par ajouter avec le nom de la table `DeviceProcessEvents` et ajoutons des éléments redirigés le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="60223-118">In this example, we start by adding  with the table name `DeviceProcessEvents` and add piped elements as needed.</span></span>

<span data-ttu-id="60223-119">Le premier élément redirigé est un filtre de temps étendu dans les sept jours précédents.</span><span class="sxs-lookup"><span data-stu-id="60223-119">The first piped element is a time filter scoped within the previous seven days.</span></span> <span data-ttu-id="60223-120">La conservation d’un intervalle de temps le plus étroit possible permet de s’assurer que les requêtes fonctionnent bien, renvoient des résultats gérables et n’expirent pas.</span><span class="sxs-lookup"><span data-stu-id="60223-120">Keeping the time range as narrow as possible ensures that queries perform well, return manageable results, and don't time out.</span></span>

```kusto
| where Timestamp > ago(7d)
```

<span data-ttu-id="60223-121">L’intervalle de temps est immédiatement suivi d’une recherche de fichiers représentant l’application PowerShell.</span><span class="sxs-lookup"><span data-stu-id="60223-121">The time range is immediately followed by a search for files representing the PowerShell application.</span></span>

```kusto
| where FileName in ("powershell.exe", "POWERSHELL.EXE", "powershell_ise.exe", "POWERSHELL_ISE.EXE")
```

<span data-ttu-id="60223-122">Par la suite, la requête recherche les lignes de commande généralement utilisées avec PowerShell pour télécharger les fichiers.</span><span class="sxs-lookup"><span data-stu-id="60223-122">Afterwards, the query looks for command lines that are typically used with PowerShell to download files.</span></span>

```kusto
| where ProcessCommandLine has "Net.WebClient"
        or ProcessCommandLine has "DownloadFile"
        or ProcessCommandLine has "Invoke-WebRequest"
        or ProcessCommandLine has "Invoke-Shellcode"
        or ProcessCommandLine contains "http:"
```

<span data-ttu-id="60223-123">Maintenant que votre requête identifie clairement les données que vous recherchez, vous pouvez ajouter des éléments qui définissent l’apparence des résultats.</span><span class="sxs-lookup"><span data-stu-id="60223-123">Now that your query clearly identifies the data you want to locate, you can add elements that define what the results look like.</span></span> <span data-ttu-id="60223-124">`project` renvoie des colonnes spécifiques et `top` limite le nombre de résultats. De ce fait, les résultats sont bien mis en forme et raisonnablement volumineux et faciles à traiter.</span><span class="sxs-lookup"><span data-stu-id="60223-124">`project` returns specific columns and `top` limits the number of results, making the results well-formatted and reasonably large and easy to process.</span></span>

```kusto
| project Timestamp, DeviceName, InitiatingProcessFileName, FileName, ProcessCommandLine
| top 100 by Timestamp
```

<span data-ttu-id="60223-125">Cliquez sur **Exécuter la requête** pour afficher les résultats.</span><span class="sxs-lookup"><span data-stu-id="60223-125">Click **Run query** to see the results.</span></span> <span data-ttu-id="60223-126">Vous pouvez développer l’affichage à l’écran pour pouvoir vous concentrer sur votre requête de repérage et sur les résultats.</span><span class="sxs-lookup"><span data-stu-id="60223-126">You can expand the screen view so you can focus on your hunting query and the results.</span></span>

## <a name="learn-common-query-operators-for-advanced-hunting"></a><span data-ttu-id="60223-127">Découvrir les opérateurs de requête courants pour le repérage avancé</span><span class="sxs-lookup"><span data-stu-id="60223-127">Learn common query operators for advanced hunting</span></span>

<span data-ttu-id="60223-128">Maintenant que vous avez exécuté votre première requête et que vous avez une idée générale de ses composants, il est temps de revenir en arrière pour découvrir quelques notions de base.</span><span class="sxs-lookup"><span data-stu-id="60223-128">Now that you've run your first query and have a general idea of its components, it's time to backtrack a little bit and learn some basics.</span></span> <span data-ttu-id="60223-129">Le langage de requête Kusto utilisé par le repérage avancé prend en charge divers opérateurs, notamment les opérateurs communs suivants.</span><span class="sxs-lookup"><span data-stu-id="60223-129">The Kusto query language used by advanced hunting supports a range of operators, including the following common ones.</span></span>

| <span data-ttu-id="60223-130">Opérateur</span><span class="sxs-lookup"><span data-stu-id="60223-130">Operator</span></span> | <span data-ttu-id="60223-131">Description et utilisation</span><span class="sxs-lookup"><span data-stu-id="60223-131">Description and usage</span></span> |
|--|--|
| `where` | <span data-ttu-id="60223-132">Filtre une table sur le sous-ensemble de lignes qui répondent à un prédicat.</span><span class="sxs-lookup"><span data-stu-id="60223-132">Filter a table to the subset of rows that satisfy a predicate.</span></span> |
| `summarize` | <span data-ttu-id="60223-133">Produit une table qui agrège le contenu de la table d’entrée.</span><span class="sxs-lookup"><span data-stu-id="60223-133">Produce a table that aggregates the content of the input table.</span></span> |
| `join` | <span data-ttu-id="60223-134">Fusionne les lignes de deux tables pour former une nouvelle table en faisant correspondre les valeurs des colonnes spécifiées de chaque table.</span><span class="sxs-lookup"><span data-stu-id="60223-134">Merge the rows of two tables to form a new table by matching values of the specified column(s) from each table.</span></span> |
| `count` | <span data-ttu-id="60223-135">Renvoie le nombre d’enregistrements dans le groupe d’enregistrements d’entrée.</span><span class="sxs-lookup"><span data-stu-id="60223-135">Return the number of records in the input record set.</span></span> |
| `top` | <span data-ttu-id="60223-136">Renvoie les N premiers enregistrements triés par les colonnes spécifiées.</span><span class="sxs-lookup"><span data-stu-id="60223-136">Return the first N records sorted by the specified columns.</span></span> |
| `limit` | <span data-ttu-id="60223-137">Renvoie jusqu’au nombre de lignes spécifié.</span><span class="sxs-lookup"><span data-stu-id="60223-137">Return up to the specified number of rows.</span></span> |
| `project` | <span data-ttu-id="60223-138">Sélectionne les colonnes à inclure, renommer ou déplacer et insère de nouvelles colonnes calculées.</span><span class="sxs-lookup"><span data-stu-id="60223-138">Select the columns to include, rename or drop, and insert new computed columns.</span></span> |
| `extend` | <span data-ttu-id="60223-139">Crée des colonnes calculées et les ajoute au jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="60223-139">Create calculated columns and append them to the result set.</span></span> |
| `makeset` |  <span data-ttu-id="60223-140">Renvoie un tableau dynamique (JSON) de l’ensemble de valeurs distinctes prise par Expr dans le groupe.</span><span class="sxs-lookup"><span data-stu-id="60223-140">Return a dynamic (JSON) array of the set of distinct values that Expr takes in the group.</span></span> |
| `find` | <span data-ttu-id="60223-141">Recherche des lignes qui correspondent à un prédicat dans un ensemble de tables.</span><span class="sxs-lookup"><span data-stu-id="60223-141">Find rows that match a predicate across a set of tables.</span></span> |

<span data-ttu-id="60223-142">Pour voir un exemple parlant de ces opérateurs, exécutez-les à partir de la section **Prise en main** du repérage avancé.</span><span class="sxs-lookup"><span data-stu-id="60223-142">To see a live example of these operators, run them from the **Get started** section in advanced hunting.</span></span>

## <a name="understand-data-types-and-their-query-syntax-implications"></a><span data-ttu-id="60223-143">Comprendre les types de données et leurs implications dans la syntaxe de requête</span><span class="sxs-lookup"><span data-stu-id="60223-143">Understand data types and their query syntax implications</span></span>

<span data-ttu-id="60223-144">Les données des tables de repérage avancé sont généralement classées dans les types de données suivants.</span><span class="sxs-lookup"><span data-stu-id="60223-144">Data in advanced hunting tables are generally classified into the following data types.</span></span>

| <span data-ttu-id="60223-145">Type de données</span><span class="sxs-lookup"><span data-stu-id="60223-145">Data type</span></span> | <span data-ttu-id="60223-146">Description et implications dans les requêtes</span><span class="sxs-lookup"><span data-stu-id="60223-146">Description and query implications</span></span> |
|--|--|
| `datetime` | <span data-ttu-id="60223-147">Informations sur les données et les heures représentant généralement les horodatages d’événement</span><span class="sxs-lookup"><span data-stu-id="60223-147">Data and time information typically representing event timestamps</span></span> |
| `string` | <span data-ttu-id="60223-148">Chaîne de caractères</span><span class="sxs-lookup"><span data-stu-id="60223-148">Character string</span></span> |
| `bool` | <span data-ttu-id="60223-149">True ou false</span><span class="sxs-lookup"><span data-stu-id="60223-149">True or false</span></span> |
| `int` | <span data-ttu-id="60223-150">Valeur numérique de 32 bits</span><span class="sxs-lookup"><span data-stu-id="60223-150">32-bit numeric value</span></span>  |
| `long` | <span data-ttu-id="60223-151">Valeur numérique de 64 bits</span><span class="sxs-lookup"><span data-stu-id="60223-151">64-bit numeric value</span></span> |

## <a name="use-sample-queries"></a><span data-ttu-id="60223-152">Utiliser des exemples de requêtes</span><span class="sxs-lookup"><span data-stu-id="60223-152">Use sample queries</span></span>

<span data-ttu-id="60223-153">La section **Prise en main** fournit quelques requêtes simples utilisant des opérateurs fréquemment utilisés.</span><span class="sxs-lookup"><span data-stu-id="60223-153">The **Get started** section provides a few simple queries using commonly used operators.</span></span> <span data-ttu-id="60223-154">Essayez d’exécuter ces requêtes et de leur apporter de légères modifications.</span><span class="sxs-lookup"><span data-stu-id="60223-154">Try running these queries and making small modifications to them.</span></span>

![Image d’une fenêtre de repérage avancé](../images/advanced-hunting-get-started.png)

>[!NOTE]
><span data-ttu-id="60223-156">Hormis les exemples de requête de base, vous pouvez également accéder à des [requêtes partagées](advanced-hunting-shared-queries.md) pour des scénarios de repérage de menace spécifiques.</span><span class="sxs-lookup"><span data-stu-id="60223-156">Apart from the basic query samples, you can also access [shared queries](advanced-hunting-shared-queries.md) for specific threat hunting scenarios.</span></span> <span data-ttu-id="60223-157">Explorez les requêtes partagées sur le côté gauche de la page ou le référentiel de requête GitHub.</span><span class="sxs-lookup"><span data-stu-id="60223-157">Explore the shared queries on the left side of the page or the GitHub query repository.</span></span>

## <a name="access-query-language-documentation"></a><span data-ttu-id="60223-158">Documentation sur le langage de requête Access</span><span class="sxs-lookup"><span data-stu-id="60223-158">Access query language documentation</span></span>

<span data-ttu-id="60223-159">Pour plus d’informations sur le langage de requête Kusto et les opérateurs pris en charge, voir [documentation sur le langage de requête Kusto](https://docs.microsoft.com/azure/kusto/query/).</span><span class="sxs-lookup"><span data-stu-id="60223-159">For more information on Kusto query language and supported operators, see [Kusto query language documentation](https://docs.microsoft.com/azure/kusto/query/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="60223-160">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="60223-160">Related topics</span></span>
- [<span data-ttu-id="60223-161">Repérage proactif des menaces</span><span class="sxs-lookup"><span data-stu-id="60223-161">Proactively hunt for threats</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="60223-162">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="60223-162">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="60223-163">Repérer les menaces sur divers appareils et e-mails</span><span class="sxs-lookup"><span data-stu-id="60223-163">Hunt for threats across devices and emails</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="60223-164">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="60223-164">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="60223-165">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="60223-165">Apply query best practices</span></span>](advanced-hunting-best-practices.md)