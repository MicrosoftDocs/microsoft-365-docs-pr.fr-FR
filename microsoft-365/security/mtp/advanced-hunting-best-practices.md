---
title: Meilleures pratiques de repérage avancé dans la Protection Microsoft contre les menaces
description: Découvrez comment créer des requêtes de repérage de menace, efficace et sans erreur dans le cas d’un repérage avancé
keywords: repérage avancé, repérage de menace, repérage de cybermenace, recherche, requête, télémétrie, détections personnalisées, schéma, kusto, éviter les délais d'attente, lignes de commande, ID de processus
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
ms.openlocfilehash: 871f659074c4f8386746e341db4d3500c5e80a31
ms.sourcegitcommit: 0ad0092d9c5cb2d69fc70c990a9b7cc03140611b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2019
ms.locfileid: "40807003"
---
# <a name="advanced-hunting-query-best-practices"></a><span data-ttu-id="72bc6-104">Pratiques recommandées pour la requête de repérage avancé</span><span class="sxs-lookup"><span data-stu-id="72bc6-104">Advanced hunting query best practices</span></span>

<span data-ttu-id="72bc6-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="72bc6-105">**Applies to:**</span></span>
- <span data-ttu-id="72bc6-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="72bc6-106">Microsoft Threat Protection</span></span>

[!INCLUDE [Prerelease information](../includes/prerelease.md)]

## <a name="optimize-query-performance"></a><span data-ttu-id="72bc6-107">Optimiser la performance des requêtes</span><span class="sxs-lookup"><span data-stu-id="72bc6-107">Optimize query performance</span></span>
<span data-ttu-id="72bc6-108">Appliquez ces recommandations pour obtenir des résultats plus rapidement et éviter les délais d’attente lors de l’exécution de requêtes complexes :</span><span class="sxs-lookup"><span data-stu-id="72bc6-108">Apply these recommendations to get results faster and avoid timeouts while running complex queries:</span></span>
- <span data-ttu-id="72bc6-109">Lorsque vous essayez de nouvelles requêtes, utilisez toujours `limit` pour éviter des jeux de résultats très volumineux.</span><span class="sxs-lookup"><span data-stu-id="72bc6-109">When trying new queries, always use `limit` to avoid extremely large result sets.</span></span> <span data-ttu-id="72bc6-110">Vous pouvez également évaluer la taille du jeu de résultats à l’aide de `count`.</span><span class="sxs-lookup"><span data-stu-id="72bc6-110">You can also initially assess the size of the result set using `count`.</span></span>
- <span data-ttu-id="72bc6-111">Utilisez tout d’abord les filtres de temps.</span><span class="sxs-lookup"><span data-stu-id="72bc6-111">Use time filters first.</span></span> <span data-ttu-id="72bc6-112">Idéalement, vous pouvez limiter vos requêtes à quelques jours.</span><span class="sxs-lookup"><span data-stu-id="72bc6-112">Ideally, limit your queries to even days.</span></span>
- <span data-ttu-id="72bc6-113">Placez les filtres qui sont censés supprimer la plupart des données au début de la requête, juste après le filtre de temps.</span><span class="sxs-lookup"><span data-stu-id="72bc6-113">Put filters that are expected to remove most of the data in the beginning of the query, right after the time filter.</span></span>
- <span data-ttu-id="72bc6-114">Utilisez l’opérateur `has` sur `contains` pour rechercher des jetons complets.</span><span class="sxs-lookup"><span data-stu-id="72bc6-114">Use the `has` operator over `contains` when looking for full tokens.</span></span>
- <span data-ttu-id="72bc6-115">Consultez une colonne spécifique plutôt que d’exécuter des recherches de texte complet dans toutes les colonnes.</span><span class="sxs-lookup"><span data-stu-id="72bc6-115">Look in a specific column rather than running full text searches across all columns.</span></span>
- <span data-ttu-id="72bc6-116">Lorsque vous joignez des tableaux, vous devez d’abord spécifier le tableau comportant moins de lignes.</span><span class="sxs-lookup"><span data-stu-id="72bc6-116">When joining tables, specify the table with fewer rows first.</span></span>
- <span data-ttu-id="72bc6-117">`project` uniquement les colonnes nécessaires des tableaux que vous avez jointes.</span><span class="sxs-lookup"><span data-stu-id="72bc6-117">`project` only the necessary columns from tables you've joined.</span></span>

>[!Tip]
><span data-ttu-id="72bc6-118">Si vous souhaitez en savoir plus sur l’amélioration des performances de requête, veuillez consulter [Meilleures pratiques de requête Kusto](https://docs.microsoft.com/azure/kusto/query/best-practices).</span><span class="sxs-lookup"><span data-stu-id="72bc6-118">For more guidance on improving query performance, read [Kusto query best practices](https://docs.microsoft.com/azure/kusto/query/best-practices).</span></span>

## <a name="query-tips-and-pitfalls"></a><span data-ttu-id="72bc6-119">Conseils et pièges de la requête</span><span class="sxs-lookup"><span data-stu-id="72bc6-119">Query tips and pitfalls</span></span>

### <a name="queries-with-process-ids"></a><span data-ttu-id="72bc6-120">Requêtes avec ID de processus</span><span class="sxs-lookup"><span data-stu-id="72bc6-120">Queries with process IDs</span></span>
<span data-ttu-id="72bc6-121">Les ID de processus (PID) sont recyclés dans Windows et réutilisés pour les nouveaux processus.</span><span class="sxs-lookup"><span data-stu-id="72bc6-121">Process IDs (PIDs) are recycled in Windows and reused for new processes.</span></span> <span data-ttu-id="72bc6-122">Ils ne peuvent pas être utilisés comme identificateurs uniques pour des processus spécifiques.</span><span class="sxs-lookup"><span data-stu-id="72bc6-122">On their own, they can't serve as unique identifiers for specific processes.</span></span>

<span data-ttu-id="72bc6-123">Pour obtenir un identificateur unique pour un processus sur un ordinateur spécifique, utilisez l’ID de processus conjointement avec l’heure de création du processus.</span><span class="sxs-lookup"><span data-stu-id="72bc6-123">To get a unique identifier for a process on a specific machine, use the process ID together with the process creation time.</span></span> <span data-ttu-id="72bc6-124">Lorsque vous rejoignez ou résumez des données autour des processus, incluez des colonnes pour l’identificateur de l’ordinateur (`DeviceId` ou `DeviceName`), l’ID de processus (`ProcessId` ou `InitiatingProcessId`) et l’heure de création du processus (`ProcessCreationTime` ou `InitiatingProcessCreationTime`).</span><span class="sxs-lookup"><span data-stu-id="72bc6-124">When you join or summarize data around processes, include columns for the machine identifier (either `DeviceId` or `DeviceName`), the process ID (`ProcessId` or `InitiatingProcessId`), and the process creation time (`ProcessCreationTime` or `InitiatingProcessCreationTime`)</span></span>

<span data-ttu-id="72bc6-125">L’exemple de requête suivant trouve les processus qui accèdent à plus de 10 adresses IP via le port 445 (SMB), qui peut rechercher des partages de fichiers.</span><span class="sxs-lookup"><span data-stu-id="72bc6-125">The following example query finds processes that access more than 10 IP addresses over port 445 (SMB), possibly scanning for file shares.</span></span>

<span data-ttu-id="72bc6-126">Exemples de requête :</span><span class="sxs-lookup"><span data-stu-id="72bc6-126">Example query:</span></span>
```
DeviceNetworkEvents
| where RemotePort == 445 and Timestamp > ago(12h) and InitiatingProcessId !in (0, 4)
| summarize RemoteIPCount=dcount(RemoteIP) by DeviceName, InitiatingProcessId, InitiatingProcessCreationTime, InitiatingProcessFileName
| where RemoteIPCount > 10
```

<span data-ttu-id="72bc6-127">La requête se résume par `InitiatingProcessId` et `InitiatingProcessCreationTime` de sorte qu’elle examine un seul processus, sans mélanger plusieurs processus ayant le même ID de processus.</span><span class="sxs-lookup"><span data-stu-id="72bc6-127">The query summarizes by both `InitiatingProcessId` and `InitiatingProcessCreationTime` so that it looks at a single process, without mixing multiple processes with the same process ID.</span></span>

### <a name="queries-with-command-lines"></a><span data-ttu-id="72bc6-128">Requêtes avec des lignes de commande</span><span class="sxs-lookup"><span data-stu-id="72bc6-128">Queries with command lines</span></span>

<span data-ttu-id="72bc6-129">Les lignes de commande peuvent varier.</span><span class="sxs-lookup"><span data-stu-id="72bc6-129">Command lines can vary.</span></span> <span data-ttu-id="72bc6-130">Le cas échéant, filtrez sur les noms des fichiers et effectuez une correspondance approximative.</span><span class="sxs-lookup"><span data-stu-id="72bc6-130">When applicable, filter on file names and do fuzzy matching.</span></span>

<span data-ttu-id="72bc6-131">Plusieurs méthodes s’offrent à vous pour créer une ligne de commande pour accomplir une tâche.</span><span class="sxs-lookup"><span data-stu-id="72bc6-131">There are numerous ways to construct a command line to accomplish a task.</span></span> <span data-ttu-id="72bc6-132">Par exemple, un attaquant peut référencer un fichier image avec ou sans chemin, sans extension de fichier, à l’aide de variables d’environnement ou de guillemets.</span><span class="sxs-lookup"><span data-stu-id="72bc6-132">For example, an attacker could reference an image file with or without a path, without a file extension, using environment variables, or with quotes.</span></span> <span data-ttu-id="72bc6-133">De plus, l’attaquant peut également modifier l’ordre des paramètres ou ajouter plusieurs guillemets et espaces.</span><span class="sxs-lookup"><span data-stu-id="72bc6-133">In addition, the attacker could also change the order of parameters or add multiple quotes and spaces.</span></span>

<span data-ttu-id="72bc6-134">Pour créer des requêtes plus durables à l’aide de lignes de commande, appliquez les pratiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="72bc6-134">To create more durable queries using command lines, apply the following practices:</span></span>

- <span data-ttu-id="72bc6-135">Identifiez les processus connus (par exemple, *net.exe* ou *psexec.exe*) en faisant correspondre les champs de nom de fichier, au lieu de filtrer sur le champ de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="72bc6-135">Identify the known processes (such as *net.exe* or *psexec.exe*) by matching on the filename fields, instead of filtering on the command-line field.</span></span>
- <span data-ttu-id="72bc6-136">Lors de l’interrogation des arguments de la ligne de commande, ne recherchez pas une correspondance exacte de plusieurs arguments non liés dans un certain ordre.</span><span class="sxs-lookup"><span data-stu-id="72bc6-136">When querying for command-line arguments, don't look for an exact match on multiple unrelated arguments in a certain order.</span></span> <span data-ttu-id="72bc6-137">Au lieu de cela, vous devez utiliser des expressions régulières ou utiliser plusieurs opérateurs de contenu séparés..</span><span class="sxs-lookup"><span data-stu-id="72bc6-137">Instead, use regular expressions or use multiple separate contains operators.</span></span>
- <span data-ttu-id="72bc6-138">Utilisez des correspondances non respectées de casse.</span><span class="sxs-lookup"><span data-stu-id="72bc6-138">Use case insensitive matches.</span></span> <span data-ttu-id="72bc6-139">Par exemple, utilisez `=~`, `in~` et `contains` au lieu de `==`, `in` et `contains_cs`</span><span class="sxs-lookup"><span data-stu-id="72bc6-139">For example, use `=~`, `in~`, and `contains` instead of `==`, `in`, and `contains_cs`</span></span>
- <span data-ttu-id="72bc6-140">Pour atténuer les techniques d’obscurcissement de lignes de commande, vous pouvez supprimer les guillemets, remplacer les virgules par des espaces et remplacer plusieurs espaces consécutifs par un seul espace.</span><span class="sxs-lookup"><span data-stu-id="72bc6-140">To mitigate DOS command-line obfuscation techniques, consider removing quotes, replacing commas with spaces, and replacing multiple consecutive spaces with a single space.</span></span> <span data-ttu-id="72bc6-141">Notez qu'il existe des techniques d'obscurcissement DOS plus complexes qui nécessitent d'autres approches, mais celles-ci peuvent aider à résoudre les problèmes les plus fréquents.</span><span class="sxs-lookup"><span data-stu-id="72bc6-141">Note that there are more complex DOS obfuscation techniques that require other approaches, but these can help address the most common ones.</span></span>

<span data-ttu-id="72bc6-142">Les exemples suivants illustrent différentes manières de créer une requête qui recherche le fichier *net.exe* pour arrêter le service Pare-feu Windows Defender :</span><span class="sxs-lookup"><span data-stu-id="72bc6-142">The following examples show various ways to construct a query that looks for the file *net.exe* to stop the Windows Defender Firewall service:</span></span>

```
// Non-durable query - do not use
DeviceProcessEvents
| where ProcessCommandLine == "net stop MpsSvc"
| limit 10

// Better query - filters on filename, does case-insensitive matches
DeviceProcessEvents
| where Timestamp > ago(7d) and FileName in~ ("net.exe", "net1.exe") and ProcessCommandLine contains "stop" and ProcessCommandLine contains "MpsSvc" 

// Best query also ignores quotes
DeviceProcessEvents
| where Timestamp > ago(7d) and FileName in~ ("net.exe", "net1.exe")
| extend CanonicalCommandLine=replace("\"", "", ProcessCommandLine)
| where CanonicalCommandLine contains "stop" and CanonicalCommandLine contains "MpsSvc" 
```
## <a name="related-topics"></a><span data-ttu-id="72bc6-143">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="72bc6-143">Related topics</span></span>
- [<span data-ttu-id="72bc6-144">Repérage proactif des menaces</span><span class="sxs-lookup"><span data-stu-id="72bc6-144">Proactively hunt for threats</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="72bc6-145">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="72bc6-145">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="72bc6-146">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="72bc6-146">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="72bc6-147">Repérer les menaces sur divers appareils et e-mails</span><span class="sxs-lookup"><span data-stu-id="72bc6-147">Hunt for threats across devices and emails</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="72bc6-148">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="72bc6-148">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
