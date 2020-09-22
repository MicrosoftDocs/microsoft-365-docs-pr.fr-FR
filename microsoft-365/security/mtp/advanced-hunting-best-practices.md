---
title: Meilleures pratiques de recherche avancée de la recherche dans Microsoft Threat Protection
description: Découvrez comment créer des requêtes de recherche rapide, efficace et sans erreur avec la chasse avancée
keywords: chasse aux menaces, recherche de menace, recherche sur les menaces informatiques, protection contre les menaces Microsoft, Microsoft 365, MTP, M365, recherche, requête, télémétrie, schéma, Kusto, éviter le délai d’attente, lignes de commande, ID de processus, optimiser, meilleures pratiques, analyser, joindre, Résumé
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
ms.openlocfilehash: af9579b94314375aa786782ea477bb11b0cd9c0b
ms.sourcegitcommit: c083602dda3cdcb5b58cb8aa070d77019075f765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2020
ms.locfileid: "48198210"
---
# <a name="advanced-hunting-query-best-practices"></a><span data-ttu-id="634a5-104">Pratiques recommandées pour la requête de repérage avancé</span><span class="sxs-lookup"><span data-stu-id="634a5-104">Advanced hunting query best practices</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="634a5-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="634a5-105">**Applies to:**</span></span>
- <span data-ttu-id="634a5-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="634a5-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="634a5-107">Appliquez ces recommandations pour obtenir des résultats plus rapidement et éviter les délais d’attente lors de l’exécution de requêtes complexes.</span><span class="sxs-lookup"><span data-stu-id="634a5-107">Apply these recommendations to get results faster and avoid timeouts while running complex queries.</span></span> <span data-ttu-id="634a5-108">Si vous souhaitez en savoir plus sur l’amélioration des performances de requête, veuillez consulter [Meilleures pratiques de requête Kusto](https://docs.microsoft.com/azure/kusto/query/best-practices).</span><span class="sxs-lookup"><span data-stu-id="634a5-108">For more guidance on improving query performance, read [Kusto query best practices](https://docs.microsoft.com/azure/kusto/query/best-practices).</span></span>

## <a name="understand-cpu-resource-limits"></a><span data-ttu-id="634a5-109">Comprendre les limites de ressources d’UC</span><span class="sxs-lookup"><span data-stu-id="634a5-109">Understand CPU resource limits</span></span>
<span data-ttu-id="634a5-110">En fonction de sa taille, chaque client a accès à un nombre défini de ressources CPU allouées à l’exécution de requêtes de chasse avancées.</span><span class="sxs-lookup"><span data-stu-id="634a5-110">Depending on its size, each tenant has access to a set amount of CPU resources allocated for running advanced hunting queries.</span></span> <span data-ttu-id="634a5-111">Pour plus d’informations sur les différentes limites de service, consultez la rubrique [relative aux limites de chasse avancée](advanced-hunting-limits.md).</span><span class="sxs-lookup"><span data-stu-id="634a5-111">For detailed information about various service limits, [read about advanced hunting limits](advanced-hunting-limits.md).</span></span>

<span data-ttu-id="634a5-112">Les clients qui exécutent régulièrement plusieurs requêtes doivent suivre la consommation et appliquer les conseils d’optimisation de cet article pour minimiser les interruptions résultant du dépassement des limites.</span><span class="sxs-lookup"><span data-stu-id="634a5-112">Customers who run multiple queries regularly should track consumption and apply the optimization guidance in this article to minimize disruption resulting from exceeding the limits.</span></span>

## <a name="general-optimization-tips"></a><span data-ttu-id="634a5-113">Conseils généraux pour l’optimisation</span><span class="sxs-lookup"><span data-stu-id="634a5-113">General optimization tips</span></span>

- <span data-ttu-id="634a5-114">**Taille des nouvelles requêtes**: Si vous pensez qu’une requête renverra un jeu de résultats volumineux, évaluez-la d’abord à l’aide de l' [opérateur Count](https://docs.microsoft.com/azure/data-explorer/kusto/query/countoperator).</span><span class="sxs-lookup"><span data-stu-id="634a5-114">**Size new queries**—If you suspect that a query will return a large result set, assess it first using the [count operator](https://docs.microsoft.com/azure/data-explorer/kusto/query/countoperator).</span></span> <span data-ttu-id="634a5-115">Utilisez la [limite](https://docs.microsoft.com/azure/data-explorer/kusto/query/limitoperator) ou son synonyme `take` pour éviter les jeux de résultats volumineux.</span><span class="sxs-lookup"><span data-stu-id="634a5-115">Use [limit](https://docs.microsoft.com/azure/data-explorer/kusto/query/limitoperator) or its synonym `take` to avoid large result sets.</span></span>
- <span data-ttu-id="634a5-116">**Appliquer des filtres plus tôt**: appliquer des filtres de temps et d’autres filtres pour réduire le jeu de données, en particulier avant d’utiliser les fonctions de transformation et d’analyse, telles que [Substring ()](https://docs.microsoft.com/azure/data-explorer/kusto/query/substringfunction), [Replace (](https://docs.microsoft.com/azure/data-explorer/kusto/query/replacefunction)), [Trim ()](https://docs.microsoft.com/azure/data-explorer/kusto/query/trimfunction), [ToUpper ()](https://docs.microsoft.com/azure/data-explorer/kusto/query/toupperfunction)ou [parse_json ()](https://docs.microsoft.com/azure/data-explorer/kusto/query/parsejsonfunction).</span><span class="sxs-lookup"><span data-stu-id="634a5-116">**Apply filters early**—Apply time filters and other filters to reduce the data set, especially before using transformation and parsing functions, such as [substring()](https://docs.microsoft.com/azure/data-explorer/kusto/query/substringfunction), [replace()](https://docs.microsoft.com/azure/data-explorer/kusto/query/replacefunction), [trim()](https://docs.microsoft.com/azure/data-explorer/kusto/query/trimfunction), [toupper()](https://docs.microsoft.com/azure/data-explorer/kusto/query/toupperfunction), or [parse_json()](https://docs.microsoft.com/azure/data-explorer/kusto/query/parsejsonfunction).</span></span> <span data-ttu-id="634a5-117">Dans l’exemple ci-dessous, la fonction d’analyse [extractjson ()](https://docs.microsoft.com/azure/data-explorer/kusto/query/extractjsonfunction) est utilisée après que les opérateurs de filtrage ont réduit le nombre d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="634a5-117">In the example below, the parsing function [extractjson()](https://docs.microsoft.com/azure/data-explorer/kusto/query/extractjsonfunction) is used after filtering operators have reduced the number of records.</span></span>

    ```kusto
    DeviceEvents
    | where Timestamp > ago(1d)
    | where ActionType == "UsbDriveMount" 
    | where DeviceName == "user-desktop.domain.com"
    | extend DriveLetter = extractjson("$.DriveLetter", AdditionalFields)
     ```

- <span data-ttu-id="634a5-118">**Contenant les temps contient**— pour éviter de Rechercher inutilement des sous-chaînes dans des mots, utilisez l' `has` opérateur au lieu de `contains` .</span><span class="sxs-lookup"><span data-stu-id="634a5-118">**Has beats contains**—To avoid searching substrings within words unnecessarily, use the `has` operator instead of `contains`.</span></span> [<span data-ttu-id="634a5-119">En savoir plus sur les opérateurs de chaîne</span><span class="sxs-lookup"><span data-stu-id="634a5-119">Learn about string operators</span></span>](https://docs.microsoft.com/azure/data-explorer/kusto/query/datatypes-string-operators)
- <span data-ttu-id="634a5-120">**Rechercher dans des colonnes spécifiques**: recherchez une colonne spécifique au lieu d’exécuter des recherches de texte intégral dans toutes les colonnes.</span><span class="sxs-lookup"><span data-stu-id="634a5-120">**Look in specific columns**—Look in a specific column rather than running full text searches across all columns.</span></span> <span data-ttu-id="634a5-121">N’utilisez pas `*` pour vérifier toutes les colonnes.</span><span class="sxs-lookup"><span data-stu-id="634a5-121">Don't use `*` to check all columns.</span></span>
- <span data-ttu-id="634a5-122">Respect **de la casse pour la vitesse**— les recherches sensibles à la casse sont plus spécifiques et généralement plus performantes.</span><span class="sxs-lookup"><span data-stu-id="634a5-122">**Case-sensitive for speed**—Case-sensitive searches are more specific and generally more performant.</span></span> <span data-ttu-id="634a5-123">Les noms des opérateurs de [chaîne](https://docs.microsoft.com/azure/data-explorer/kusto/query/datatypes-string-operators)respectant la casse, tels que `has_cs` et `contains_cs` , se terminent généralement par `_cs` .</span><span class="sxs-lookup"><span data-stu-id="634a5-123">Names of case-sensitive [string operators](https://docs.microsoft.com/azure/data-explorer/kusto/query/datatypes-string-operators), such as `has_cs` and `contains_cs`, generally end with `_cs`.</span></span> <span data-ttu-id="634a5-124">Vous pouvez également utiliser l’opérateur Equals avec respect de la casse `==` et non `~=` .</span><span class="sxs-lookup"><span data-stu-id="634a5-124">You can also use the case-sensitive equals operator `==` instead of `~=`.</span></span>
- <span data-ttu-id="634a5-125">**Parse, ne pas extraire**: dans la mesure du possible, utilisez l' [opérateur d’analyse](https://docs.microsoft.com/azure/data-explorer/kusto/query/parseoperator) ou une fonction d’analyse telle que [parse_json ()](https://docs.microsoft.com/azure/data-explorer/kusto/query/parsejsonfunction).</span><span class="sxs-lookup"><span data-stu-id="634a5-125">**Parse, don't extract**—Whenever possible, use the [parse operator](https://docs.microsoft.com/azure/data-explorer/kusto/query/parseoperator) or a parsing function like [parse_json()](https://docs.microsoft.com/azure/data-explorer/kusto/query/parsejsonfunction).</span></span> <span data-ttu-id="634a5-126">Évitez l' `matches regex` opérateur String ou la [fonction Extract ()](https://docs.microsoft.com/azure/data-explorer/kusto/query/extractfunction), qui utilisent les deux l’expression régulière.</span><span class="sxs-lookup"><span data-stu-id="634a5-126">Avoid the `matches regex` string operator or the [extract() function](https://docs.microsoft.com/azure/data-explorer/kusto/query/extractfunction), both of which use regular expression.</span></span> <span data-ttu-id="634a5-127">Réservez l’utilisation de l’expression régulière pour des scénarios plus complexes.</span><span class="sxs-lookup"><span data-stu-id="634a5-127">Reserve the use of regular expression for more complex scenarios.</span></span> [<span data-ttu-id="634a5-128">En savoir plus sur les fonctions d’analyse</span><span class="sxs-lookup"><span data-stu-id="634a5-128">Read more about parsing functions</span></span>](#parse-strings)
- <span data-ttu-id="634a5-129">**Filtrer les tables et non les expressions**: ne filtrez pas une colonne calculée si vous pouvez filtrer une colonne de table.</span><span class="sxs-lookup"><span data-stu-id="634a5-129">**Filter tables not expressions**—Don't filter on a calculated column if you can filter on a table column.</span></span>
- <span data-ttu-id="634a5-130">**Aucun caractère de trois caractères**— Évitez de comparer ou de filtrer à l’aide de termes de trois caractères maximum.</span><span class="sxs-lookup"><span data-stu-id="634a5-130">**No three-character terms**—Avoid comparing or filtering using terms with three characters or fewer.</span></span> <span data-ttu-id="634a5-131">Ces termes ne sont pas indexés et leur correspondance nécessitera davantage de ressources.</span><span class="sxs-lookup"><span data-stu-id="634a5-131">These terms are not indexed and matching them will require more resources.</span></span>
- <span data-ttu-id="634a5-132">**Project de manière sélective**: Rendez vos résultats plus faciles à comprendre en ne projetant que les colonnes dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="634a5-132">**Project selectively**—Make your results easier to understand by projecting only the columns you need.</span></span> <span data-ttu-id="634a5-133">La projection de colonnes spécifiques avant l’exécution d’opérations [join](https://docs.microsoft.com/azure/data-explorer/kusto/query/joinoperator) ou similaires permet également d’améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="634a5-133">Projecting specific columns prior to running [join](https://docs.microsoft.com/azure/data-explorer/kusto/query/joinoperator) or similar operations also helps improve performance.</span></span>

## <a name="optimize-the-join-operator"></a><span data-ttu-id="634a5-134">Optimiser l' `join` opérateur</span><span class="sxs-lookup"><span data-stu-id="634a5-134">Optimize the `join` operator</span></span>
<span data-ttu-id="634a5-135">L' [opérateur Join](https://docs.microsoft.com/azure/data-explorer/kusto/query/joinoperator) fusionne les lignes de deux tables en faisant correspondre les valeurs dans les colonnes spécifiées.</span><span class="sxs-lookup"><span data-stu-id="634a5-135">The [join operator](https://docs.microsoft.com/azure/data-explorer/kusto/query/joinoperator) merges rows from two tables by matching values in specified columns.</span></span> <span data-ttu-id="634a5-136">Appliquez ces conseils pour optimiser les requêtes qui utilisent cet opérateur.</span><span class="sxs-lookup"><span data-stu-id="634a5-136">Apply these tips to optimize queries that use this operator.</span></span>

- <span data-ttu-id="634a5-137">**Petit tableau à gauche**: l' `join` opérateur fait correspondre les enregistrements de la table à gauche de votre instruction JOIN aux enregistrements à droite.</span><span class="sxs-lookup"><span data-stu-id="634a5-137">**Smaller table to your left**—The `join` operator matches records in the table on the left side of your join statement to records on the right.</span></span> <span data-ttu-id="634a5-138">En faisant en sorte que le tableau est plus petit sur la gauche, moins d’enregistrements doivent être mis en correspondance, ce qui accélère la requête.</span><span class="sxs-lookup"><span data-stu-id="634a5-138">By having the smaller table on the left, fewer records will need to be matched, thus speeding up the query.</span></span> 

    <span data-ttu-id="634a5-139">Dans le tableau ci-dessous, nous allons réduire le tableau `DeviceLogonEvents` de gauche pour ne traiter que trois appareils spécifiques avant de les joindre à des `IdentityLogonEvents` SID de compte.</span><span class="sxs-lookup"><span data-stu-id="634a5-139">In the table below, we reduce the left table `DeviceLogonEvents` to cover only three specific devices before joining it with `IdentityLogonEvents` by account SIDs.</span></span>
 
    ```kusto
    DeviceLogonEvents 
    | where DeviceName in ("device-1.domain.com", "device-2.domain.com", "device-3.domain.com")
    | where ActionType == "LogonFailed"
    | join
        (IdentityLogonEvents
        | where ActionType == "LogonFailed"
        | where Protocol == "Kerberos")
    on AccountSid
    ```

- <span data-ttu-id="634a5-140">**Utilisez la version INNER JOIN**: la version de [jointure](https://docs.microsoft.com/azure/data-explorer/kusto/query/joinoperator#join-flavors) par défaut ou la [innerunique-Join](https://docs.microsoft.com/azure/data-explorer/kusto/query/joinoperator?pivots=azuredataexplorer#innerunique-join-flavor) déduplique les lignes du tableau de gauche en fonction de la clé de jointure avant de renvoyer une ligne pour chaque correspondance à la table de droite.</span><span class="sxs-lookup"><span data-stu-id="634a5-140">**Use the inner-join flavor**—The default [join flavor](https://docs.microsoft.com/azure/data-explorer/kusto/query/joinoperator#join-flavors) or the [innerunique-join](https://docs.microsoft.com/azure/data-explorer/kusto/query/joinoperator?pivots=azuredataexplorer#innerunique-join-flavor) deduplicates rows in the left table by the join key before returning a row for each match to the right table.</span></span> <span data-ttu-id="634a5-141">Si la table de gauche comporte plusieurs lignes avec la même valeur pour la `join` clé, ces lignes seront dédoublées afin de laisser une seule ligne aléatoire pour chaque valeur unique.</span><span class="sxs-lookup"><span data-stu-id="634a5-141">If the left table has multiple rows with the same value for the `join` key, those rows will be deduplicated to leave a single random row for each unique value.</span></span>

    <span data-ttu-id="634a5-142">Ce comportement par défaut peut ignorer des informations importantes de la table de gauche qui peuvent fournir des informations utiles.</span><span class="sxs-lookup"><span data-stu-id="634a5-142">This default behavior can leave out important information from the left table that can provide useful insight.</span></span> <span data-ttu-id="634a5-143">Par exemple, la requête ci-dessous n’affiche qu’un seul e-mail contenant une pièce jointe particulière, même si la même pièce jointe a été envoyée à l’aide de plusieurs messages électroniques :</span><span class="sxs-lookup"><span data-stu-id="634a5-143">For example, the query below will only show one email containing a particular attachment, even if that same attachment was sent using multiple emails messages:</span></span>

    ```kusto
    EmailAttachmentInfo
    | where Timestamp > ago(1h)
    | where Subject == "Document Attachment" and FileName == "Document.pdf"
    | join (DeviceFileEvents | where Timestamp > ago(1h)) on SHA256 
    ```

    <span data-ttu-id="634a5-144">Pour résoudre cette limitation, nous appliquons la saveur [INNER-JOIN](https://docs.microsoft.com/azure/data-explorer/kusto/query/joinoperator?pivots=azuredataexplorer#inner-join-flavor) en spécifiant `kind=inner` d’afficher toutes les lignes de la table de gauche avec des valeurs correspondantes à droite :</span><span class="sxs-lookup"><span data-stu-id="634a5-144">To address this limitation, we apply the [inner-join](https://docs.microsoft.com/azure/data-explorer/kusto/query/joinoperator?pivots=azuredataexplorer#inner-join-flavor) flavor by specifying `kind=inner` to show all rows in the left table with matching values in the right:</span></span>
    
    ```kusto
    EmailAttachmentInfo
    | where Timestamp > ago(1h)
    | where Subject == "Document Attachment" and FileName == "Document.pdf"
    | join kind=inner (DeviceFileEvents | where Timestamp > ago(1h)) on SHA256 
    ```
- <span data-ttu-id="634a5-145">**Joindre des enregistrements à partir d’une fenêtre temporelle**: lors de l’examen des événements de sécurité, les analystes recherchent des événements associés qui se produisent sur la même période.</span><span class="sxs-lookup"><span data-stu-id="634a5-145">**Join records from a time window**—When investigating security events, analysts look for related events that occur around the same time period.</span></span> <span data-ttu-id="634a5-146">Appliquer la même approche lorsque `join` vous utilisez également les performances en réduisant le nombre d’enregistrements à vérifier.</span><span class="sxs-lookup"><span data-stu-id="634a5-146">Applying the same approach when using `join` also benefits performance by reducing the number of records to check.</span></span>
    
    <span data-ttu-id="634a5-147">La requête ci-dessous vérifie les événements de connexion dans les 30 minutes suivant la réception d’un fichier malveillant :</span><span class="sxs-lookup"><span data-stu-id="634a5-147">The query below checks for logon events within 30 minutes of receiving a malicious file:</span></span>

    ```kusto
    EmailEvents
    | where Timestamp > ago(7d)
    | where MalwareFilterVerdict == "Malware" 
    | project EmailReceivedTime = Timestamp, Subject, SenderFromAddress, AccountName = tostring(split(RecipientEmailAddress, "@")[0])
    | join (
    DeviceLogonEvents 
    | where Timestamp > ago(7d)
    | project LogonTime = Timestamp, AccountName, DeviceName
    ) on AccountName 
    | where (LogonTime - EmailReceivedTime) between (0min .. 30min)
    ```
- <span data-ttu-id="634a5-148">**Appliquer des filtres de temps sur les deux côtés**— même si vous n’examinez pas une fenêtre de temps spécifique, l’application de filtres de temps sur les tables gauche et droite peut réduire le nombre d’enregistrements à vérifier et améliorer les `join` performances.</span><span class="sxs-lookup"><span data-stu-id="634a5-148">**Apply time filters on both sides**—Even if you're not investigating a specific time window, applying time filters on both the left and right tables can reduce the number of records to check and improve `join` performance.</span></span> <span data-ttu-id="634a5-149">La requête ci-dessous s’applique `Timestamp > ago(1h)` aux deux tables afin qu’elle ne rejoigne que les enregistrements de la dernière heure :</span><span class="sxs-lookup"><span data-stu-id="634a5-149">The query below applies `Timestamp > ago(1h)` to both tables so that it joins only records from the past hour:</span></span>

    ```kusto
    EmailAttachmentInfo
    | where Timestamp > ago(1h)
    | where Subject == "Document Attachment" and FileName == "Document.pdf"
    | join kind=inner (DeviceFileEvents | where Timestamp > ago(1h)) on SHA256 
    ```  

- <span data-ttu-id="634a5-150">**Utiliser des conseils pour les performances**: utilisez des conseils avec l' `join` opérateur pour indiquer au serveur principal de distribuer la charge lors de l’exécution d’opérations gourmandes en ressources.</span><span class="sxs-lookup"><span data-stu-id="634a5-150">**Use hints for performance**—Use hints with the `join` operator to instruct the backend to distribute load when running resource-intensive operations.</span></span> [<span data-ttu-id="634a5-151">En savoir plus sur les conseils de jointure</span><span class="sxs-lookup"><span data-stu-id="634a5-151">Learn more about join hints</span></span>](https://docs.microsoft.com/azure/data-explorer/kusto/query/joinoperator#join-hints)

    <span data-ttu-id="634a5-152">Par exemple, l' **[indicateur de lecture aléatoire](https://docs.microsoft.com/azure/data-explorer/kusto/query/shufflequery)** permet d’améliorer les performances des requêtes lors de la jointure de tables à l’aide d’une clé à haute cardinalité, une clé avec de nombreuses valeurs uniques, telles que la `AccountObjectId` requête ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="634a5-152">For example, the **[shuffle hint](https://docs.microsoft.com/azure/data-explorer/kusto/query/shufflequery)** helps improve query performance when joining tables using a key with high cardinality—a key with many unique values—such as the `AccountObjectId` in the query below:</span></span>

    ```kusto
    IdentityInfo
    | where JobTitle == "CONSULTANT"
    | join hint.shufflekey = AccountObjectId 
    (IdentityDirectoryEvents
        | where Application == "Active Directory"
        | where ActionType == "Private data retrieval")
    on AccountObjectId 
    ```
    
    <span data-ttu-id="634a5-153">L' **[indication de diffusion](https://docs.microsoft.com/azure/data-explorer/kusto/query/broadcastjoin)** est utile lorsque le tableau de gauche est de petite taille (jusqu’à 100 000 enregistrements) et que la table de droite est extrêmement volumineuse.</span><span class="sxs-lookup"><span data-stu-id="634a5-153">The **[broadcast hint](https://docs.microsoft.com/azure/data-explorer/kusto/query/broadcastjoin)** helps when the left table is small (up to 100,000 records) and the right table is extremely large.</span></span> <span data-ttu-id="634a5-154">Par exemple, la requête ci-dessous tente de joindre quelques e-mails contenant des objets spécifiques avec _tous les_ messages contenant des liens dans la `EmailUrlInfo` table :</span><span class="sxs-lookup"><span data-stu-id="634a5-154">For example, the query below is trying to join a few emails that have specific subjects with _all_ messages containing links in the `EmailUrlInfo` table:</span></span>

    ```kusto
    EmailEvents 
    | where Subject in ("Warning: Update your credentials now", "Action required: Update your credentials now")
    | join hint.strategy = broadcast EmailUrlInfo on NetworkMessageId 
    ```

## <a name="optimize-the-summarize-operator"></a><span data-ttu-id="634a5-155">Optimiser l' `summarize` opérateur</span><span class="sxs-lookup"><span data-stu-id="634a5-155">Optimize the `summarize` operator</span></span>
<span data-ttu-id="634a5-156">L' [opérateur de synthèse](https://docs.microsoft.com/azure/data-explorer/kusto/query/summarizeoperator) agrège le contenu d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="634a5-156">The [summarize operator](https://docs.microsoft.com/azure/data-explorer/kusto/query/summarizeoperator) aggregates the contents of a table.</span></span> <span data-ttu-id="634a5-157">Appliquez ces conseils pour optimiser les requêtes qui utilisent cet opérateur.</span><span class="sxs-lookup"><span data-stu-id="634a5-157">Apply these tips to optimize queries that use this operator.</span></span>

- <span data-ttu-id="634a5-158">**Rechercher des valeurs distinctes**: en règle générale, utilisez `summarize` pour rechercher des valeurs distinctes pouvant être répétitives.</span><span class="sxs-lookup"><span data-stu-id="634a5-158">**Find distinct values**—In general, use `summarize` to find distinct values that can be repetitive.</span></span> <span data-ttu-id="634a5-159">Il peut s’avérer inutile de l’utiliser pour agréger des colonnes qui n’ont pas de valeurs répétitives.</span><span class="sxs-lookup"><span data-stu-id="634a5-159">It can be unnecessary to use it to aggregate columns that don't have repetitive values.</span></span>

    <span data-ttu-id="634a5-160">Bien qu’un seul courrier électronique puisse faire partie de plusieurs événements, l’exemple ci-dessous n’est _pas_ une utilisation efficace de, `summarize` car un ID de message réseau pour un e-mail individuel est toujours fourni avec une adresse d’expéditeur unique.</span><span class="sxs-lookup"><span data-stu-id="634a5-160">While a single email can be part of multiple events, the example below is _not_ an efficient use of `summarize` because a network message ID for an individual email always comes with a unique sender address.</span></span>
 
    ```kusto
    EmailEvents  
    | where Timestamp > ago(1h)
    | summarize by NetworkMessageId, SenderFromAddress   
    ```
    <span data-ttu-id="634a5-161">L' `summarize` opérateur peut être facilement remplacé par, ce qui peut `project` produire des résultats identiques tout en consommant moins de ressources :</span><span class="sxs-lookup"><span data-stu-id="634a5-161">The `summarize` operator can be easily replaced with `project`, yielding potentially the same results while consuming fewer resources:</span></span>

    ```kusto
    EmailEvents  
    | where Timestamp > ago(1h)
    | project NetworkMessageId, SenderFromAddress   
    ```
    <span data-ttu-id="634a5-162">L’exemple suivant est une utilisation plus efficace de `summarize` , car il peut y avoir plusieurs instances distinctes d’une adresse d’expéditeur qui envoient des messages électroniques à la même adresse de destinataire.</span><span class="sxs-lookup"><span data-stu-id="634a5-162">The following example is a more efficient use of `summarize` because there can be multiple distinct instances of a sender address sending email to the same recipient address.</span></span> <span data-ttu-id="634a5-163">Ces combinaisons sont moins distinctes et sont susceptibles d’avoir des doublons.</span><span class="sxs-lookup"><span data-stu-id="634a5-163">Such combinations are less distinct and are likely to have duplicates.</span></span>

    ```kusto
    EmailEvents  
    | where Timestamp > ago(1h)
    | summarize by SenderFromAddress, RecipientEmailAddress   
    ```

- <span data-ttu-id="634a5-164">**Lecture aléatoire de la requête**, bien qu' `summarize` il soit préférable de l’utiliser dans des colonnes avec des valeurs répétitives, les mêmes colonnes peuvent également avoir _une haute cardinalité_ ou un grand nombre de valeurs uniques.</span><span class="sxs-lookup"><span data-stu-id="634a5-164">**Shuffle the query**—While `summarize` is best used in columns with repetitive values, the same columns can also have _high cardinality_ or large numbers of unique values.</span></span> <span data-ttu-id="634a5-165">Comme l' `join` opérateur, vous pouvez également appliquer l' [indicateur de lecture aléatoire](https://docs.microsoft.com/azure/data-explorer/kusto/query/shufflequery) `summarize` pour répartir la charge de traitement et éventuellement améliorer les performances lors de l’utilisation de colonnes à haute cardinalité.</span><span class="sxs-lookup"><span data-stu-id="634a5-165">Like the `join` operator, you can also apply the [shuffle hint](https://docs.microsoft.com/azure/data-explorer/kusto/query/shufflequery) with `summarize` to distribute processing load and potentially improve performance when operating on columns with high cardinality.</span></span>

    <span data-ttu-id="634a5-166">La requête ci-dessous utilise `summarize` pour compter le nombre d’adresses de messagerie de destinataires distinctes, qui peut s’exécuter dans des centaines de milliers dans les grandes organisations.</span><span class="sxs-lookup"><span data-stu-id="634a5-166">The query below uses `summarize` to count distinct recipient email address, which can run in the hundreds of thousands in large organizations.</span></span> <span data-ttu-id="634a5-167">Pour améliorer les performances, il intègre les `hint.shufflekey` éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="634a5-167">To improve performance, it incorporates `hint.shufflekey`:</span></span>

    ```kusto
    EmailEvents  
    | where Timestamp > ago(1h)
    | summarize hint.shufflekey = RecipientEmailAddress count() by Subject, RecipientEmailAddress
    ```

## <a name="query-scenarios"></a><span data-ttu-id="634a5-168">Scénarios de requête</span><span class="sxs-lookup"><span data-stu-id="634a5-168">Query scenarios</span></span>

### <a name="identify-unique-processes-with-process-ids"></a><span data-ttu-id="634a5-169">Identifier les processus uniques avec des ID de processus</span><span class="sxs-lookup"><span data-stu-id="634a5-169">Identify unique processes with process IDs</span></span>
<span data-ttu-id="634a5-170">Les ID de processus (PID) sont recyclés dans Windows et réutilisés pour les nouveaux processus.</span><span class="sxs-lookup"><span data-stu-id="634a5-170">Process IDs (PIDs) are recycled in Windows and reused for new processes.</span></span> <span data-ttu-id="634a5-171">Ils ne peuvent pas être utilisés comme identificateurs uniques pour des processus spécifiques.</span><span class="sxs-lookup"><span data-stu-id="634a5-171">On their own, they can't serve as unique identifiers for specific processes.</span></span>

<span data-ttu-id="634a5-172">Pour obtenir un identificateur unique pour un processus sur un ordinateur spécifique, utilisez l’ID de processus conjointement avec l’heure de création du processus.</span><span class="sxs-lookup"><span data-stu-id="634a5-172">To get a unique identifier for a process on a specific machine, use the process ID together with the process creation time.</span></span> <span data-ttu-id="634a5-173">Lorsque vous rejoignez ou résumez des données autour des processus, incluez des colonnes pour l’identificateur de l’ordinateur (`DeviceId` ou `DeviceName`), l’ID de processus (`ProcessId` ou `InitiatingProcessId`) et l’heure de création du processus (`ProcessCreationTime` ou `InitiatingProcessCreationTime`).</span><span class="sxs-lookup"><span data-stu-id="634a5-173">When you join or summarize data around processes, include columns for the machine identifier (either `DeviceId` or `DeviceName`), the process ID (`ProcessId` or `InitiatingProcessId`), and the process creation time (`ProcessCreationTime` or `InitiatingProcessCreationTime`)</span></span>

<span data-ttu-id="634a5-174">L’exemple de requête suivant trouve les processus qui accèdent à plus de 10 adresses IP via le port 445 (SMB), qui peut rechercher des partages de fichiers.</span><span class="sxs-lookup"><span data-stu-id="634a5-174">The following example query finds processes that access more than 10 IP addresses over port 445 (SMB), possibly scanning for file shares.</span></span>

<span data-ttu-id="634a5-175">Exemples de requête :</span><span class="sxs-lookup"><span data-stu-id="634a5-175">Example query:</span></span>
```kusto
DeviceNetworkEvents
| where RemotePort == 445 and Timestamp > ago(12h) and InitiatingProcessId !in (0, 4)
| summarize RemoteIPCount=dcount(RemoteIP) by DeviceName, InitiatingProcessId
InitiatingProcessCreationTime, InitiatingProcessFileName
| where RemoteIPCount > 10
```

<span data-ttu-id="634a5-176">La requête se résume par `InitiatingProcessId` et `InitiatingProcessCreationTime` de sorte qu’elle examine un seul processus, sans mélanger plusieurs processus ayant le même ID de processus.</span><span class="sxs-lookup"><span data-stu-id="634a5-176">The query summarizes by both `InitiatingProcessId` and `InitiatingProcessCreationTime` so that it looks at a single process, without mixing multiple processes with the same process ID.</span></span>

### <a name="query-command-lines"></a><span data-ttu-id="634a5-177">Lignes de commande de requête</span><span class="sxs-lookup"><span data-stu-id="634a5-177">Query command lines</span></span>
<span data-ttu-id="634a5-178">Plusieurs méthodes s’offrent à vous pour créer une ligne de commande pour accomplir une tâche.</span><span class="sxs-lookup"><span data-stu-id="634a5-178">There are numerous ways to construct a command line to accomplish a task.</span></span> <span data-ttu-id="634a5-179">Par exemple, un agresseur peut faire référence à un fichier image sans chemin d’accès, sans extension de fichier, à l’aide de variables d’environnement ou de guillemets.</span><span class="sxs-lookup"><span data-stu-id="634a5-179">For example, an attacker could reference an image file without a path, without a file extension, using environment variables, or with quotes.</span></span> <span data-ttu-id="634a5-180">L’agresseur peut également modifier l’ordre des paramètres ou ajouter plusieurs guillemets et espaces.</span><span class="sxs-lookup"><span data-stu-id="634a5-180">The attacker could also change the order of parameters or add multiple quotes and spaces.</span></span>

<span data-ttu-id="634a5-181">Pour créer des requêtes plus durables sur les lignes de commande, appliquez les pratiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="634a5-181">To create more durable queries around command lines, apply the following practices:</span></span>

- <span data-ttu-id="634a5-182">Identifiez les processus connus (par exemple, *net.exe* ou *psexec.exe*) en faisant correspondre les champs de nom de fichier au lieu de filtrer sur la ligne de commande proprement dite.</span><span class="sxs-lookup"><span data-stu-id="634a5-182">Identify the known processes (such as *net.exe* or *psexec.exe*) by matching on the file name fields, instead of filtering on the command-line itself.</span></span>
- <span data-ttu-id="634a5-183">Analyser les sections de ligne de commande à l’aide de la [fonction parse_command_line ()](https://docs.microsoft.com/azure/data-explorer/kusto/query/parse-command-line)</span><span class="sxs-lookup"><span data-stu-id="634a5-183">Parse command-line sections using the [parse_command_line() function](https://docs.microsoft.com/azure/data-explorer/kusto/query/parse-command-line)</span></span> 
- <span data-ttu-id="634a5-184">Lors de l’interrogation des arguments de la ligne de commande, ne recherchez pas une correspondance exacte de plusieurs arguments non liés dans un certain ordre.</span><span class="sxs-lookup"><span data-stu-id="634a5-184">When querying for command-line arguments, don't look for an exact match on multiple unrelated arguments in a certain order.</span></span> <span data-ttu-id="634a5-185">Au lieu de cela, vous devez utiliser des expressions régulières ou utiliser plusieurs opérateurs de contenu séparés..</span><span class="sxs-lookup"><span data-stu-id="634a5-185">Instead, use regular expressions or use multiple separate contains operators.</span></span>
- <span data-ttu-id="634a5-186">Utilisez des correspondances non respectées de casse.</span><span class="sxs-lookup"><span data-stu-id="634a5-186">Use case insensitive matches.</span></span> <span data-ttu-id="634a5-187">Par exemple, utilisez `=~` ,, `in~` et `contains` au lieu de `==` , `in` , et `contains_cs` .</span><span class="sxs-lookup"><span data-stu-id="634a5-187">For example, use `=~`, `in~`, and `contains` instead of `==`, `in`, and `contains_cs`.</span></span>
- <span data-ttu-id="634a5-188">Pour atténuer les techniques d’obscurcissement de ligne de commande, envisagez de supprimer des guillemets, de remplacer des virgules par des espaces et de remplacer plusieurs espaces consécutifs par un seul espace.</span><span class="sxs-lookup"><span data-stu-id="634a5-188">To mitigate command-line obfuscation techniques, consider removing quotes, replacing commas with spaces, and replacing multiple consecutive spaces with a single space.</span></span> <span data-ttu-id="634a5-189">Il existe des techniques d’obscurcissement plus complexes qui nécessitent d’autres approches, mais ces ajustements peuvent aider à résoudre les problèmes courants.</span><span class="sxs-lookup"><span data-stu-id="634a5-189">There are more complex obfuscation techniques that require other approaches, but these tweaks can help address common ones.</span></span>

<span data-ttu-id="634a5-190">Les exemples suivants illustrent différentes façons de créer une requête qui recherche le fichier *net.exe* pour arrêter le service pare-feu « mpssvc » :</span><span class="sxs-lookup"><span data-stu-id="634a5-190">The following examples show various ways to construct a query that looks for the file *net.exe* to stop the firewall service "MpsSvc":</span></span>

```kusto
// Non-durable query - do not use
DeviceProcessEvents
| where ProcessCommandLine == "net stop MpsSvc"
| limit 10

// Better query - filters on file name, does case-insensitive matches
DeviceProcessEvents
| where Timestamp > ago(7d) and FileName in~ ("net.exe", "net1.exe") and ProcessCommandLine contains "stop" and ProcessCommandLine contains "MpsSvc" 

// Best query also ignores quotes
DeviceProcessEvents
| where Timestamp > ago(7d) and FileName in~ ("net.exe", "net1.exe")
| extend CanonicalCommandLine=replace("\"", "", ProcessCommandLine)
| where CanonicalCommandLine contains "stop" and CanonicalCommandLine contains "MpsSvc" 
```

### <a name="ingest-data-from-external-sources"></a><span data-ttu-id="634a5-191">Données ingérées provenant de sources externes</span><span class="sxs-lookup"><span data-stu-id="634a5-191">Ingest data from external sources</span></span>
<span data-ttu-id="634a5-192">Pour incorporer des listes longues ou des tables volumineuses dans votre requête, utilisez l' [opérateur ExternalData](https://docs.microsoft.com/azure/data-explorer/kusto/query/externaldata-operator) pour les données à partir d’un URI spécifié.</span><span class="sxs-lookup"><span data-stu-id="634a5-192">To incorporate long lists or large tables into your query, use the [externaldata operator](https://docs.microsoft.com/azure/data-explorer/kusto/query/externaldata-operator) to ingest data from a specified URI.</span></span> <span data-ttu-id="634a5-193">Vous pouvez obtenir des données à partir de fichiers TXT, CSV, JSON ou d' [autres formats](https://docs.microsoft.com/azure/data-explorer/ingestion-supported-formats).</span><span class="sxs-lookup"><span data-stu-id="634a5-193">You can get data from files in TXT, CSV, JSON, or [other formats](https://docs.microsoft.com/azure/data-explorer/ingestion-supported-formats).</span></span> <span data-ttu-id="634a5-194">L’exemple ci-dessous montre comment vous pouvez utiliser la liste exhaustive des hachages SHA-256 fournis par MalwareBazaar (abuse.ch) pour vérifier les pièces jointes dans les e-mails :</span><span class="sxs-lookup"><span data-stu-id="634a5-194">The example below shows how you can utilize the extensive list of malware SHA-256  hashes provided by MalwareBazaar (abuse.ch) to check attachments on emails:</span></span>

```kusto
let abuse_sha256 = (externaldata(sha256_hash: string )
[@"https://bazaar.abuse.ch/export/txt/sha256/recent/"]
with (format="txt"))
| where sha256_hash !startswith "#"
| project sha256_hash;
abuse_sha256
| join (EmailAttachmentInfo 
| where Timestamp > ago(1d) 
) on $left.sha256_hash == $right.SHA256
| project Timestamp,SenderFromAddress,RecipientEmailAddress,FileName,FileType,
SHA256,MalwareFilterVerdict,MalwareDetectionMethod
```

### <a name="parse-strings"></a><span data-ttu-id="634a5-195">Analyser des chaînes</span><span class="sxs-lookup"><span data-stu-id="634a5-195">Parse strings</span></span>
<span data-ttu-id="634a5-196">Il existe différentes fonctions que vous pouvez utiliser pour gérer efficacement les chaînes qui nécessitent une analyse ou une conversion.</span><span class="sxs-lookup"><span data-stu-id="634a5-196">There are various functions you can use to efficiently handle strings that need parsing or conversion.</span></span> 

| <span data-ttu-id="634a5-197">String</span><span class="sxs-lookup"><span data-stu-id="634a5-197">String</span></span> | <span data-ttu-id="634a5-198">Fonction</span><span class="sxs-lookup"><span data-stu-id="634a5-198">Function</span></span> | <span data-ttu-id="634a5-199">Exemple d'utilisation</span><span class="sxs-lookup"><span data-stu-id="634a5-199">Usage example</span></span> |
|--|--|--|
| <span data-ttu-id="634a5-200">Lignes de commande</span><span class="sxs-lookup"><span data-stu-id="634a5-200">Command-lines</span></span> | [<span data-ttu-id="634a5-201">parse_command_line ()</span><span class="sxs-lookup"><span data-stu-id="634a5-201">parse_command_line()</span></span>](https://docs.microsoft.com/azure/data-explorer/kusto/query/parse-command-line) | <span data-ttu-id="634a5-202">Extrayez la commande et tous les arguments.</span><span class="sxs-lookup"><span data-stu-id="634a5-202">Extract the command and all arguments.</span></span> | 
| <span data-ttu-id="634a5-203">Paths</span><span class="sxs-lookup"><span data-stu-id="634a5-203">Paths</span></span> | [<span data-ttu-id="634a5-204">parse_path ()</span><span class="sxs-lookup"><span data-stu-id="634a5-204">parse_path()</span></span>](https://docs.microsoft.com/azure/data-explorer/kusto/query/parsepathfunction) | <span data-ttu-id="634a5-205">Extraire les sections d’un fichier ou d’un chemin d’accès de dossier.</span><span class="sxs-lookup"><span data-stu-id="634a5-205">Extract the sections of a file or folder path.</span></span> |
| <span data-ttu-id="634a5-206">Numéros de version</span><span class="sxs-lookup"><span data-stu-id="634a5-206">Version numbers</span></span> | [<span data-ttu-id="634a5-207">parse_version ()</span><span class="sxs-lookup"><span data-stu-id="634a5-207">parse_version()</span></span>](https://docs.microsoft.com/azure/data-explorer/kusto/query/parse-versionfunction) | <span data-ttu-id="634a5-208">Déconstruisez un numéro de version avec un maximum de quatre sections et jusqu’à huit caractères par section.</span><span class="sxs-lookup"><span data-stu-id="634a5-208">Deconstruct a version number with up to four sections and up to eight characters per section.</span></span> <span data-ttu-id="634a5-209">Utilisez les données analysées pour comparer l’âge de la version.</span><span class="sxs-lookup"><span data-stu-id="634a5-209">Use the parsed data to compare version age.</span></span> |
| <span data-ttu-id="634a5-210">Adresses IPv4</span><span class="sxs-lookup"><span data-stu-id="634a5-210">IPv4 addresses</span></span> | [<span data-ttu-id="634a5-211">parse_ipv4 ()</span><span class="sxs-lookup"><span data-stu-id="634a5-211">parse_ipv4()</span></span>](https://docs.microsoft.com/azure/data-explorer/kusto/query/parse-ipv4function) | <span data-ttu-id="634a5-212">Convertissez une adresse IPv4 en entier long.</span><span class="sxs-lookup"><span data-stu-id="634a5-212">Convert an IPv4 address to a long integer.</span></span> <span data-ttu-id="634a5-213">Pour comparer des adresses IPv4 sans les convertir, utilisez [ipv4_compare ()](https://docs.microsoft.com/azure/data-explorer/kusto/query/ipv4-comparefunction).</span><span class="sxs-lookup"><span data-stu-id="634a5-213">To compare IPv4 addresses without converting them, use [ipv4_compare()](https://docs.microsoft.com/azure/data-explorer/kusto/query/ipv4-comparefunction).</span></span> |
| <span data-ttu-id="634a5-214">Adresses IPv6</span><span class="sxs-lookup"><span data-stu-id="634a5-214">IPv6 addresses</span></span> | [<span data-ttu-id="634a5-215">parse_ipv6 ()</span><span class="sxs-lookup"><span data-stu-id="634a5-215">parse_ipv6()</span></span>](https://docs.microsoft.com/azure/data-explorer/kusto/query/parse-ipv6function)  | <span data-ttu-id="634a5-216">Convertissez une adresse IPv4 ou IPv6 en notation IPv6 canonique.</span><span class="sxs-lookup"><span data-stu-id="634a5-216">Convert an IPv4 or IPv6 address to the canonical IPv6 notation.</span></span> <span data-ttu-id="634a5-217">Pour comparer des adresses IPv6, utilisez [ipv6_compare ()](https://docs.microsoft.com/azure/data-explorer/kusto/query/ipv6-comparefunction).</span><span class="sxs-lookup"><span data-stu-id="634a5-217">To compare IPv6 addresses, use [ipv6_compare()](https://docs.microsoft.com/azure/data-explorer/kusto/query/ipv6-comparefunction).</span></span> |

<span data-ttu-id="634a5-218">Pour en savoir plus sur toutes les fonctions d’analyse prises en charge, consultez la rubrique [about Kusto String Functions](https://docs.microsoft.com/azure/data-explorer/kusto/query/scalarfunctions#string-functions).</span><span class="sxs-lookup"><span data-stu-id="634a5-218">To learn about all supported parsing functions, [read about Kusto string functions](https://docs.microsoft.com/azure/data-explorer/kusto/query/scalarfunctions#string-functions).</span></span> 

## <a name="related-topics"></a><span data-ttu-id="634a5-219">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="634a5-219">Related topics</span></span>
- [<span data-ttu-id="634a5-220">Documentation du langage de requête Kusto</span><span class="sxs-lookup"><span data-stu-id="634a5-220">Kusto query language documentation</span></span>](https://docs.microsoft.com/azure/data-explorer/kusto/query/)
- [<span data-ttu-id="634a5-221">Limites de service</span><span class="sxs-lookup"><span data-stu-id="634a5-221">Service limits</span></span>](advanced-hunting-limits.md)
- [<span data-ttu-id="634a5-222">Gérer les erreurs de chasse avancées</span><span class="sxs-lookup"><span data-stu-id="634a5-222">Handle advanced hunting errors</span></span>](advanced-hunting-errors.md)
- [<span data-ttu-id="634a5-223">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="634a5-223">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="634a5-224">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="634a5-224">Learn the query language</span></span>](advanced-hunting-query-language.md)
