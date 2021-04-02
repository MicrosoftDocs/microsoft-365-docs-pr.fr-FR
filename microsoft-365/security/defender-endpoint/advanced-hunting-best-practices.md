---
title: Meilleures pratiques de requête pour le recherche avancée
description: Découvrez comment créer des requêtes de repérage de menace, efficace et sans erreur dans le cas d’un repérage avancé
keywords: repérage avancé, repérage de menace, repérage de cybermenace, mdatp, microsoft defender atp, recherche wdatp, requête, télémétrie, détections personnalisées, schéma, kusto, éviter le délai d’attente, lignes de commande, ID de processus
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
ms.collection: m365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: b65adbc968e095a6845f27ae1ae859830e4065c4
ms.sourcegitcommit: 582555d2b4ef5f2e2494ffdeab2c1d49e5d6b724
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51499259"
---
# <a name="advanced-hunting-query-best-practices"></a><span data-ttu-id="c57a1-104">Pratiques recommandées pour la requête de repérage avancé</span><span class="sxs-lookup"><span data-stu-id="c57a1-104">Advanced hunting query best practices</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="c57a1-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="c57a1-105">**Applies to:**</span></span>
- [<span data-ttu-id="c57a1-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="c57a1-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)


><span data-ttu-id="c57a1-107">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="c57a1-107">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="c57a1-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="c57a1-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-bestpractices-abovefoldlink)

## <a name="optimize-query-performance"></a><span data-ttu-id="c57a1-109">Optimiser la performance des requêtes</span><span class="sxs-lookup"><span data-stu-id="c57a1-109">Optimize query performance</span></span>

<span data-ttu-id="c57a1-110">Appliquez ces recommandations pour obtenir des résultats plus rapidement et éviter les délai d’accès lors de l’exécution de requêtes complexes.</span><span class="sxs-lookup"><span data-stu-id="c57a1-110">Apply these recommendations to get results faster and avoid timeouts while running complex queries.</span></span>

- <span data-ttu-id="c57a1-111">Lorsque vous essayez de nouvelles requêtes, utilisez toujours `limit` pour éviter des jeux de résultats très volumineux.</span><span class="sxs-lookup"><span data-stu-id="c57a1-111">When trying new queries, always use `limit` to avoid extremely large result sets.</span></span> <span data-ttu-id="c57a1-112">Vous pouvez également évaluer la taille du jeu de résultats à l’aide de `count`.</span><span class="sxs-lookup"><span data-stu-id="c57a1-112">You can also initially assess the size of the result set using `count`.</span></span>
- <span data-ttu-id="c57a1-113">Utilisez tout d’abord les filtres de temps.</span><span class="sxs-lookup"><span data-stu-id="c57a1-113">Use time filters first.</span></span> <span data-ttu-id="c57a1-114">Dans l’idéal, limitez vos requêtes à sept jours.</span><span class="sxs-lookup"><span data-stu-id="c57a1-114">Ideally, limit your queries to seven days.</span></span>
- <span data-ttu-id="c57a1-115">Placez les filtres qui sont censés supprimer la plupart des données au début de la requête, juste après le filtre de temps.</span><span class="sxs-lookup"><span data-stu-id="c57a1-115">Put filters that are expected to remove most of the data in the beginning of the query, right after the time filter.</span></span>
- <span data-ttu-id="c57a1-116">Utilisez l’opérateur `has` sur `contains` pour rechercher des jetons complets.</span><span class="sxs-lookup"><span data-stu-id="c57a1-116">Use the `has` operator over `contains` when looking for full tokens.</span></span>
- <span data-ttu-id="c57a1-117">Consultez une colonne spécifique plutôt que d’exécuter des recherches de texte complet dans toutes les colonnes.</span><span class="sxs-lookup"><span data-stu-id="c57a1-117">Look in a specific column rather than running full text searches across all columns.</span></span>
- <span data-ttu-id="c57a1-118">Lorsque vous joignez des tableaux, vous devez d’abord spécifier le tableau comportant moins de lignes.</span><span class="sxs-lookup"><span data-stu-id="c57a1-118">When joining tables, specify the table with fewer rows first.</span></span>
- <span data-ttu-id="c57a1-119">`project` uniquement les colonnes nécessaires des tableaux que vous avez jointes.</span><span class="sxs-lookup"><span data-stu-id="c57a1-119">`project` only the necessary columns from tables you've joined.</span></span>

>[!TIP]
><span data-ttu-id="c57a1-120">Si vous souhaitez en savoir plus sur l’amélioration des performances de requête, veuillez consulter [Meilleures pratiques de requête Kusto](https://docs.microsoft.com/azure/kusto/query/best-practices).</span><span class="sxs-lookup"><span data-stu-id="c57a1-120">For more guidance on improving query performance, read [Kusto query best practices](https://docs.microsoft.com/azure/kusto/query/best-practices).</span></span>

## <a name="query-tips-and-pitfalls"></a><span data-ttu-id="c57a1-121">Conseils et pièges de la requête</span><span class="sxs-lookup"><span data-stu-id="c57a1-121">Query tips and pitfalls</span></span>

### <a name="queries-with-process-ids"></a><span data-ttu-id="c57a1-122">Requêtes avec ID de processus</span><span class="sxs-lookup"><span data-stu-id="c57a1-122">Queries with process IDs</span></span>

<span data-ttu-id="c57a1-123">Les ID de processus (PID) sont recyclés dans Windows et réutilisés pour les nouveaux processus.</span><span class="sxs-lookup"><span data-stu-id="c57a1-123">Process IDs (PIDs) are recycled in Windows and reused for new processes.</span></span> <span data-ttu-id="c57a1-124">Ils ne peuvent pas être utilisés comme identificateurs uniques pour des processus spécifiques.</span><span class="sxs-lookup"><span data-stu-id="c57a1-124">On their own, they can't serve as unique identifiers for specific processes.</span></span> <span data-ttu-id="c57a1-125">Pour obtenir un identificateur unique pour un processus sur un appareil spécifique, utilisez l’ID de processus avec l’heure de création du processus.</span><span class="sxs-lookup"><span data-stu-id="c57a1-125">To get a unique identifier for a process on a specific device, use the process ID together with the process creation time.</span></span> <span data-ttu-id="c57a1-126">Lorsque vous joignez ou synthétiser des données autour des processus, incluez des colonnes pour l’identificateur de l’appareil (ou ), l’ID de processus ( ou ), et l’heure de création `DeviceId` du processus ( ou `DeviceName` `ProcessId` `InitiatingProcessId` `ProcessCreationTime` `InitiatingProcessCreationTime` ).</span><span class="sxs-lookup"><span data-stu-id="c57a1-126">When you join or summarize data around processes, include columns for the device identifier (either `DeviceId` or `DeviceName`), the process ID (`ProcessId` or `InitiatingProcessId`), and the process creation time (`ProcessCreationTime` or `InitiatingProcessCreationTime`).</span></span>

<span data-ttu-id="c57a1-127">L’exemple de requête suivant trouve les processus qui accèdent à plus de 10 adresses IP via le port 445 (SMB), qui peut rechercher des partages de fichiers.</span><span class="sxs-lookup"><span data-stu-id="c57a1-127">The following example query finds processes that access more than 10 IP addresses over port 445 (SMB), possibly scanning for file shares.</span></span>

```kusto
DeviceNetworkEvents
| where RemotePort == 445 and Timestamp > ago(12h) and InitiatingProcessId !in (0, 4)
| summarize RemoteIPCount=dcount(RemoteIP) by DeviceName, InitiatingProcessId, InitiatingProcessCreationTime, InitiatingProcessFileName
| where RemoteIPCount > 10
```

<span data-ttu-id="c57a1-128">La requête se résume par `InitiatingProcessId` et `InitiatingProcessCreationTime` de sorte qu’elle examine un seul processus, sans mélanger plusieurs processus ayant le même ID de processus.</span><span class="sxs-lookup"><span data-stu-id="c57a1-128">The query summarizes by both `InitiatingProcessId` and `InitiatingProcessCreationTime` so that it looks at a single process, without mixing multiple processes with the same process ID.</span></span>

### <a name="queries-with-command-lines"></a><span data-ttu-id="c57a1-129">Requêtes avec des lignes de commande</span><span class="sxs-lookup"><span data-stu-id="c57a1-129">Queries with command lines</span></span>

<span data-ttu-id="c57a1-130">Les lignes de commande peuvent varier.</span><span class="sxs-lookup"><span data-stu-id="c57a1-130">Command lines can vary.</span></span> <span data-ttu-id="c57a1-131">Le cas échéant, filtrez sur les noms des fichiers et effectuez une correspondance approximative.</span><span class="sxs-lookup"><span data-stu-id="c57a1-131">When applicable, filter on file names and do fuzzy matching.</span></span>

<span data-ttu-id="c57a1-132">Plusieurs méthodes s’offrent à vous pour créer une ligne de commande pour accomplir une tâche.</span><span class="sxs-lookup"><span data-stu-id="c57a1-132">There are numerous ways to construct a command line to accomplish a task.</span></span> <span data-ttu-id="c57a1-133">Par exemple, un attaquant peut référencer un fichier image avec ou sans chemin, sans extension de fichier, à l’aide de variables d’environnement ou de guillemets.</span><span class="sxs-lookup"><span data-stu-id="c57a1-133">For example, an attacker could reference an image file with or without a path, without a file extension, using environment variables, or with quotes.</span></span> <span data-ttu-id="c57a1-134">De plus, l’attaquant peut également modifier l’ordre des paramètres ou ajouter plusieurs guillemets et espaces.</span><span class="sxs-lookup"><span data-stu-id="c57a1-134">In addition, the attacker could also change the order of parameters or add multiple quotes and spaces.</span></span>

<span data-ttu-id="c57a1-135">Pour créer des requêtes plus durables à l’aide de lignes de commande, appliquez les pratiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="c57a1-135">To create more durable queries using command lines, apply the following practices:</span></span>

- <span data-ttu-id="c57a1-136">Identifiez les processus connus (par exemple, *net.exe* ou *psexec.exe*) en faisant correspondre les champs de nom de fichier, au lieu de filtrer sur le champ de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="c57a1-136">Identify the known processes (such as *net.exe* or *psexec.exe*) by matching on the filename fields, instead of filtering on the command-line field.</span></span>
- <span data-ttu-id="c57a1-137">Lors de l’interrogation des arguments de la ligne de commande, ne recherchez pas une correspondance exacte de plusieurs arguments non liés dans un certain ordre.</span><span class="sxs-lookup"><span data-stu-id="c57a1-137">When querying for command-line arguments, don't look for an exact match on multiple unrelated arguments in a certain order.</span></span> <span data-ttu-id="c57a1-138">Au lieu de cela, vous devez utiliser des expressions régulières ou utiliser plusieurs opérateurs de contenu séparés..</span><span class="sxs-lookup"><span data-stu-id="c57a1-138">Instead, use regular expressions or use multiple separate contains operators.</span></span>
- <span data-ttu-id="c57a1-139">Utilisez des correspondances non respectées de casse.</span><span class="sxs-lookup"><span data-stu-id="c57a1-139">Use case insensitive matches.</span></span> <span data-ttu-id="c57a1-140">Par exemple, utilisez `=~` , et au lieu de , `in~` `contains` `==` `in` et `contains_cs`</span><span class="sxs-lookup"><span data-stu-id="c57a1-140">For example, use `=~`, `in~`, and `contains` instead of `==`, `in` and `contains_cs`</span></span>
- <span data-ttu-id="c57a1-141">Pour atténuer les techniques d’obscurcissement de lignes de commande, vous pouvez supprimer les guillemets, remplacer les virgules par des espaces et remplacer plusieurs espaces consécutifs par un seul espace.</span><span class="sxs-lookup"><span data-stu-id="c57a1-141">To mitigate DOS command-line obfuscation techniques, consider removing quotes, replacing commas with spaces, and replacing multiple consecutive spaces with a single space.</span></span> <span data-ttu-id="c57a1-142">Notez qu'il existe des techniques d'obscurcissement DOS plus complexes qui nécessitent d'autres approches, mais celles-ci peuvent aider à résoudre les problèmes les plus fréquents.</span><span class="sxs-lookup"><span data-stu-id="c57a1-142">Note that there are more complex DOS obfuscation techniques that require other approaches, but these can help address the most common ones.</span></span>

<span data-ttu-id="c57a1-143">Les exemples suivants illustrent différentes manières de créer une requête qui recherche le fichier *net.exe* pour arrêter le service Pare-feu Windows Defender :</span><span class="sxs-lookup"><span data-stu-id="c57a1-143">The following examples show various ways to construct a query that looks for the file *net.exe* to stop the Windows Defender Firewall service:</span></span>

```kusto
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

> <span data-ttu-id="c57a1-144">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="c57a1-144">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="c57a1-145">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="c57a1-145">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-bestpractices-belowfoldlink)

## <a name="related-topics"></a><span data-ttu-id="c57a1-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c57a1-146">Related topics</span></span>

- [<span data-ttu-id="c57a1-147">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="c57a1-147">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="c57a1-148">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="c57a1-148">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="c57a1-149">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="c57a1-149">Understand the schema</span></span>](advanced-hunting-schema-reference.md)
- [<span data-ttu-id="c57a1-150">Utiliser les résultats d’une requête</span><span class="sxs-lookup"><span data-stu-id="c57a1-150">Work with query results</span></span>](advanced-hunting-query-results.md)
- [<span data-ttu-id="c57a1-151">Vue d’ensemble des détections personnalisées</span><span class="sxs-lookup"><span data-stu-id="c57a1-151">Custom detections overview</span></span>](overview-custom-detections.md)
