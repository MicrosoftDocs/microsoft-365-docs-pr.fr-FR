---
title: Meilleures pratiques de requête de recherche avancée dans Microsoft 365 Defender
description: Découvrez comment créer des requêtes de recherche de menaces rapides, efficaces et sans erreur avec le hunting avancé
keywords: advanced hunting, threat hunting, cyber threat hunting, microsoft threat protection, microsoft 365, mtp, m365, search, query, telemetry, schema, kusto, avoid timeout, command lines, process id, optimize, best practice, parse, join, summarize
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
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
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
ms.technology: m365d
ms.openlocfilehash: e838ce873a1c3ecc0f437f96e75cc2a40d3af79d
ms.sourcegitcommit: 3d48e198e706f22ac903b346cadda06b2368dd1e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/11/2021
ms.locfileid: "50727270"
---
# <a name="advanced-hunting-query-best-practices"></a><span data-ttu-id="a5c5e-104">Pratiques recommandées pour la requête de repérage avancé</span><span class="sxs-lookup"><span data-stu-id="a5c5e-104">Advanced hunting query best practices</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="a5c5e-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="a5c5e-105">**Applies to:**</span></span>
- <span data-ttu-id="a5c5e-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a5c5e-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="a5c5e-107">Appliquez ces recommandations pour obtenir des résultats plus rapidement et éviter les délai d’accès lors de l’exécution de requêtes complexes.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-107">Apply these recommendations to get results faster and avoid timeouts while running complex queries.</span></span> <span data-ttu-id="a5c5e-108">Si vous souhaitez en savoir plus sur l’amélioration des performances de requête, veuillez consulter [Meilleures pratiques de requête Kusto](https://docs.microsoft.com/azure/kusto/query/best-practices).</span><span class="sxs-lookup"><span data-stu-id="a5c5e-108">For more guidance on improving query performance, read [Kusto query best practices](https://docs.microsoft.com/azure/kusto/query/best-practices).</span></span>

## <a name="understand-cpu-resource-quotas"></a><span data-ttu-id="a5c5e-109">Comprendre les quotas de ressources de l’UC</span><span class="sxs-lookup"><span data-stu-id="a5c5e-109">Understand CPU resource quotas</span></span>
<span data-ttu-id="a5c5e-110">En fonction de sa taille, chaque client a accès à une quantité définie de ressources processeur allouées pour l’exécution de requêtes de recherche avancées.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-110">Depending on its size, each tenant has access to a set amount of CPU resources allocated for running advanced hunting queries.</span></span> <span data-ttu-id="a5c5e-111">Pour plus d’informations sur les différentes limites de service, voir les quotas de recherche avancés et [les paramètres d’utilisation.](advanced-hunting-limits.md)</span><span class="sxs-lookup"><span data-stu-id="a5c5e-111">For detailed information about various service limits, [read about advanced hunting quotas and usage parameters](advanced-hunting-limits.md).</span></span>

<span data-ttu-id="a5c5e-112">Les clients qui exécutent plusieurs requêtes régulièrement doivent suivre la consommation et appliquer les recommandations d’optimisation de cet article afin de minimiser les perturbations résultant du dépassement des quotas ou des paramètres d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-112">Customers who run multiple queries regularly should track consumption and apply the optimization guidance in this article to minimize disruption resulting from exceeding quotas or usage parameters.</span></span>

## <a name="general-optimization-tips"></a><span data-ttu-id="a5c5e-113">Conseils généraux d’optimisation</span><span class="sxs-lookup"><span data-stu-id="a5c5e-113">General optimization tips</span></span>

- <span data-ttu-id="a5c5e-114">**Dimensioniser les nouvelles requêtes**— Si vous pensez qu’une requête retournera un jeu de résultats important, évaluez-la d’abord à l’aide de [l’opérateur de nombre.](https://docs.microsoft.com/azure/data-explorer/kusto/query/countoperator)</span><span class="sxs-lookup"><span data-stu-id="a5c5e-114">**Size new queries**—If you suspect that a query will return a large result set, assess it first using the [count operator](https://docs.microsoft.com/azure/data-explorer/kusto/query/countoperator).</span></span> <span data-ttu-id="a5c5e-115">Utilisez [limit ou](https://docs.microsoft.com/azure/data-explorer/kusto/query/limitoperator) son synonyme pour éviter les jeux de résultats `take` importants.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-115">Use [limit](https://docs.microsoft.com/azure/data-explorer/kusto/query/limitoperator) or its synonym `take` to avoid large result sets.</span></span>
- <span data-ttu-id="a5c5e-116">Appliquer des filtres tôt — Appliquer des filtres de temps et d’autres filtres pour réduire le jeu de données, en particulier avant d’utiliser des fonctions de transformation et d’analyse, telles que sous-string() , [replace()](https://docs.microsoft.com/azure/data-explorer/kusto/query/replacefunction), [](https://docs.microsoft.com/azure/data-explorer/kusto/query/substringfunction) [trim()](https://docs.microsoft.com/azure/data-explorer/kusto/query/trimfunction), [toupper()](https://docs.microsoft.com/azure/data-explorer/kusto/query/toupperfunction)ou [parse_json()](https://docs.microsoft.com/azure/data-explorer/kusto/query/parsejsonfunction).</span><span class="sxs-lookup"><span data-stu-id="a5c5e-116">**Apply filters early**—Apply time filters and other filters to reduce the data set, especially before using transformation and parsing functions, such as [substring()](https://docs.microsoft.com/azure/data-explorer/kusto/query/substringfunction), [replace()](https://docs.microsoft.com/azure/data-explorer/kusto/query/replacefunction), [trim()](https://docs.microsoft.com/azure/data-explorer/kusto/query/trimfunction), [toupper()](https://docs.microsoft.com/azure/data-explorer/kusto/query/toupperfunction), or [parse_json()](https://docs.microsoft.com/azure/data-explorer/kusto/query/parsejsonfunction).</span></span> <span data-ttu-id="a5c5e-117">Dans l’exemple ci-dessous, la fonction d’recherche [extractjson()](https://docs.microsoft.com/azure/data-explorer/kusto/query/extractjsonfunction) est utilisée après que les opérateurs de filtrage ont réduit le nombre d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-117">In the example below, the parsing function [extractjson()](https://docs.microsoft.com/azure/data-explorer/kusto/query/extractjsonfunction) is used after filtering operators have reduced the number of records.</span></span>

    ```kusto
    DeviceEvents
    | where Timestamp > ago(1d)
    | where ActionType == "UsbDriveMount" 
    | where DeviceName == "user-desktop.domain.com"
    | extend DriveLetter = extractjson("$.DriveLetter", AdditionalFields)
     ```

- <span data-ttu-id="a5c5e-118">**A des frappes contient**— Pour éviter inutilement de rechercher des sous-strations dans des mots, utilisez l’opérateur `has` au lieu de `contains` .</span><span class="sxs-lookup"><span data-stu-id="a5c5e-118">**Has beats contains**—To avoid searching substrings within words unnecessarily, use the `has` operator instead of `contains`.</span></span> [<span data-ttu-id="a5c5e-119">En savoir plus sur les opérateurs de chaîne</span><span class="sxs-lookup"><span data-stu-id="a5c5e-119">Learn about string operators</span></span>](https://docs.microsoft.com/azure/data-explorer/kusto/query/datatypes-string-operators)
- <span data-ttu-id="a5c5e-120">**Rechercher dans des colonnes spécifiques**: recherchez dans une colonne spécifique plutôt que d’effectuer des recherches en texte intégral dans toutes les colonnes.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-120">**Look in specific columns**—Look in a specific column rather than running full text searches across all columns.</span></span> <span data-ttu-id="a5c5e-121">Ne pas utiliser pour `*` vérifier toutes les colonnes.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-121">Don't use `*` to check all columns.</span></span>
- <span data-ttu-id="a5c5e-122">**En ce qui concerne la vitesse, les** recherches sensibles à la cas sont plus spécifiques et généralement plus performantes.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-122">**Case-sensitive for speed**—Case-sensitive searches are more specific and generally more performant.</span></span> <span data-ttu-id="a5c5e-123">Les noms des opérateurs de chaîne [sensibles](https://docs.microsoft.com/azure/data-explorer/kusto/query/datatypes-string-operators)à la cas, tels que `has_cs` et , se `contains_cs` terminent généralement par `_cs` .</span><span class="sxs-lookup"><span data-stu-id="a5c5e-123">Names of case-sensitive [string operators](https://docs.microsoft.com/azure/data-explorer/kusto/query/datatypes-string-operators), such as `has_cs` and `contains_cs`, generally end with `_cs`.</span></span> <span data-ttu-id="a5c5e-124">Vous pouvez également utiliser l’opérateur d’égalité sensible à la cas `==` au lieu de `=~` .</span><span class="sxs-lookup"><span data-stu-id="a5c5e-124">You can also use the case-sensitive equals operator `==` instead of `=~`.</span></span>
- <span data-ttu-id="a5c5e-125">**Parse, n’extrayez** pas : [](https://docs.microsoft.com/azure/data-explorer/kusto/query/parseoperator) dans la mesure du possible, utilisez l’opérateur d’parse_json() . [](https://docs.microsoft.com/azure/data-explorer/kusto/query/parsejsonfunction)</span><span class="sxs-lookup"><span data-stu-id="a5c5e-125">**Parse, don't extract**—Whenever possible, use the [parse operator](https://docs.microsoft.com/azure/data-explorer/kusto/query/parseoperator) or a parsing function like [parse_json()](https://docs.microsoft.com/azure/data-explorer/kusto/query/parsejsonfunction).</span></span> <span data-ttu-id="a5c5e-126">Évitez `matches regex` l’opérateur de chaîne [ou la fonction extract(),](https://docs.microsoft.com/azure/data-explorer/kusto/query/extractfunction)qui utilisent toutes deux une expression régulière.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-126">Avoid the `matches regex` string operator or the [extract() function](https://docs.microsoft.com/azure/data-explorer/kusto/query/extractfunction), both of which use regular expression.</span></span> <span data-ttu-id="a5c5e-127">Réservez l’utilisation d’une expression régulière pour des scénarios plus complexes.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-127">Reserve the use of regular expression for more complex scenarios.</span></span> [<span data-ttu-id="a5c5e-128">En savoir plus sur les fonctions d’différentes fonctions</span><span class="sxs-lookup"><span data-stu-id="a5c5e-128">Read more about parsing functions</span></span>](#parse-strings)
- <span data-ttu-id="a5c5e-129">**Filtrer les tableaux et** non les expressions : ne filtrez pas sur une colonne calculée si vous pouvez filtrer sur une colonne de tableau.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-129">**Filter tables not expressions**—Don't filter on a calculated column if you can filter on a table column.</span></span>
- <span data-ttu-id="a5c5e-130">**Aucun terme à trois caractères**: évitez de comparer ou de filtrer à l’aide de termes de trois caractères ou moins.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-130">**No three-character terms**—Avoid comparing or filtering using terms with three characters or fewer.</span></span> <span data-ttu-id="a5c5e-131">Ces termes ne sont pas indexés et leur mise en correspondance nécessitera davantage de ressources.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-131">These terms are not indexed and matching them will require more resources.</span></span>
- <span data-ttu-id="a5c5e-132">**Projet de manière sélective**: facilitez la compréhension de vos résultats en projetant uniquement les colonnes dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-132">**Project selectively**—Make your results easier to understand by projecting only the columns you need.</span></span> <span data-ttu-id="a5c5e-133">Le fait de projeter des colonnes spécifiques avant [l’exécution](https://docs.microsoft.com/azure/data-explorer/kusto/query/joinoperator) d’opérations de jointage ou d’opérations similaires permet également d’améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-133">Projecting specific columns prior to running [join](https://docs.microsoft.com/azure/data-explorer/kusto/query/joinoperator) or similar operations also helps improve performance.</span></span>

## <a name="optimize-the-join-operator"></a><span data-ttu-id="a5c5e-134">Optimiser `join` l’opérateur</span><span class="sxs-lookup"><span data-stu-id="a5c5e-134">Optimize the `join` operator</span></span>
<span data-ttu-id="a5c5e-135">[L’opérateur de jointeur](https://docs.microsoft.com/azure/data-explorer/kusto/query/joinoperator) fusionne les lignes de deux tables en correspondant aux valeurs des colonnes spécifiées.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-135">The [join operator](https://docs.microsoft.com/azure/data-explorer/kusto/query/joinoperator) merges rows from two tables by matching values in specified columns.</span></span> <span data-ttu-id="a5c5e-136">Appliquez ces conseils pour optimiser les requêtes qui utilisent cet opérateur.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-136">Apply these tips to optimize queries that use this operator.</span></span>

- <span data-ttu-id="a5c5e-137">**Table plus petite à gauche —** L’opérateur fait la correspondance entre les enregistrements de la table sur le côté gauche de votre instruction de jointeur et les enregistrements de `join` droite.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-137">**Smaller table to your left**—The `join` operator matches records in the table on the left side of your join statement to records on the right.</span></span> <span data-ttu-id="a5c5e-138">En ayant la table plus petite à gauche, moins d’enregistrements devront être mis en correspondance, ce qui accélère la requête.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-138">By having the smaller table on the left, fewer records will need to be matched, thus speeding up the query.</span></span> 

    <span data-ttu-id="a5c5e-139">Dans le tableau ci-dessous, nous réduisons le tableau de gauche pour couvrir uniquement trois appareils spécifiques avant de le joindre par `DeviceLogonEvents` `IdentityLogonEvents` des SID de compte.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-139">In the table below, we reduce the left table `DeviceLogonEvents` to cover only three specific devices before joining it with `IdentityLogonEvents` by account SIDs.</span></span>
 
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

- <span data-ttu-id="a5c5e-140">Utilisez la jointure interne [](https://docs.microsoft.com/azure/data-explorer/kusto/query/joinoperator#join-flavors) : la jointure par défaut ou la jointure interne déduplique les lignes dans le tableau de gauche par la touche de jointure avant de renvoyer une ligne pour chaque correspondance à la table de droite. [](https://docs.microsoft.com/azure/data-explorer/kusto/query/joinoperator?pivots=azuredataexplorer#innerunique-join-flavor)</span><span class="sxs-lookup"><span data-stu-id="a5c5e-140">**Use the inner-join flavor**—The default [join flavor](https://docs.microsoft.com/azure/data-explorer/kusto/query/joinoperator#join-flavors) or the [innerunique-join](https://docs.microsoft.com/azure/data-explorer/kusto/query/joinoperator?pivots=azuredataexplorer#innerunique-join-flavor) deduplicates rows in the left table by the join key before returning a row for each match to the right table.</span></span> <span data-ttu-id="a5c5e-141">Si le tableau de gauche possède plusieurs lignes avec la même valeur pour la clé, ces lignes sont déduplicées pour laisser une seule ligne aléatoire pour `join` chaque valeur unique.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-141">If the left table has multiple rows with the same value for the `join` key, those rows will be deduplicated to leave a single random row for each unique value.</span></span>

    <span data-ttu-id="a5c5e-142">Ce comportement par défaut peut laisser de côté les informations importantes du tableau de gauche qui peuvent fournir des informations utiles.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-142">This default behavior can leave out important information from the left table that can provide useful insight.</span></span> <span data-ttu-id="a5c5e-143">Par exemple, la requête ci-dessous affiche uniquement un e-mail contenant une pièce jointe particulière, même si cette même pièce jointe a été envoyée à l’aide de plusieurs messages électroniques :</span><span class="sxs-lookup"><span data-stu-id="a5c5e-143">For example, the query below will only show one email containing a particular attachment, even if that same attachment was sent using multiple emails messages:</span></span>

    ```kusto
    EmailAttachmentInfo
    | where Timestamp > ago(1h)
    | where Subject == "Document Attachment" and FileName == "Document.pdf"
    | join (DeviceFileEvents | where Timestamp > ago(1h)) on SHA256 
    ```

    <span data-ttu-id="a5c5e-144">Pour résoudre cette limitation, [](https://docs.microsoft.com/azure/data-explorer/kusto/query/joinoperator?pivots=azuredataexplorer#inner-join-flavor) nous appliquons la couleur jointeur interne en spécifiant d’afficher toutes les lignes du tableau de gauche avec les `kind=inner` valeurs correspondantes à droite :</span><span class="sxs-lookup"><span data-stu-id="a5c5e-144">To address this limitation, we apply the [inner-join](https://docs.microsoft.com/azure/data-explorer/kusto/query/joinoperator?pivots=azuredataexplorer#inner-join-flavor) flavor by specifying `kind=inner` to show all rows in the left table with matching values in the right:</span></span>
    
    ```kusto
    EmailAttachmentInfo
    | where Timestamp > ago(1h)
    | where Subject == "Document Attachment" and FileName == "Document.pdf"
    | join kind=inner (DeviceFileEvents | where Timestamp > ago(1h)) on SHA256 
    ```
- <span data-ttu-id="a5c5e-145">**Joindre des enregistrements à partir d’une fenêtre de** temps — Lorsque vous examinez des événements de sécurité, les analystes recherchent les événements connexes qui se produisent autour de la même période.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-145">**Join records from a time window**—When investigating security events, analysts look for related events that occur around the same time period.</span></span> <span data-ttu-id="a5c5e-146">L’application de la même approche lors de l’utilisation de cette méthode permet également d’améliorer les performances en `join` réduisant le nombre d’enregistrements à vérifier.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-146">Applying the same approach when using `join` also benefits performance by reducing the number of records to check.</span></span>
    
    <span data-ttu-id="a5c5e-147">La requête ci-dessous recherche les événements d’logo dans les 30 minutes suivant la réception d’un fichier malveillant :</span><span class="sxs-lookup"><span data-stu-id="a5c5e-147">The query below checks for logon events within 30 minutes of receiving a malicious file:</span></span>

    ```kusto
    EmailEvents
    | where Timestamp > ago(7d)
    | where ThreatTypes has "Malware"
    | project EmailReceivedTime = Timestamp, Subject, SenderFromAddress, AccountName = tostring(split(RecipientEmailAddress, "@")[0])
    | join (
    DeviceLogonEvents 
    | where Timestamp > ago(7d)
    | project LogonTime = Timestamp, AccountName, DeviceName
    ) on AccountName 
    | where (LogonTime - EmailReceivedTime) between (0min .. 30min)
    ```
- <span data-ttu-id="a5c5e-148">Appliquer des filtres d’heure des deux côtés — Même si vous n’examinez pas une fenêtre de temps spécifique, l’application de filtres de temps dans les tableaux gauche et droit peut réduire le nombre d’enregistrements à vérifier et améliorer les `join` performances.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-148">**Apply time filters on both sides**—Even if you're not investigating a specific time window, applying time filters on both the left and right tables can reduce the number of records to check and improve `join` performance.</span></span> <span data-ttu-id="a5c5e-149">La requête ci-dessous s’applique aux deux tables afin qu’elle joint uniquement les enregistrements de `Timestamp > ago(1h)` l’heure passée :</span><span class="sxs-lookup"><span data-stu-id="a5c5e-149">The query below applies `Timestamp > ago(1h)` to both tables so that it joins only records from the past hour:</span></span>

    ```kusto
    EmailAttachmentInfo
    | where Timestamp > ago(1h)
    | where Subject == "Document Attachment" and FileName == "Document.pdf"
    | join kind=inner (DeviceFileEvents | where Timestamp > ago(1h)) on SHA256 
    ```  

- <span data-ttu-id="a5c5e-150">**Utiliser des conseils pour les performances**: utilisez des conseils avec l’opérateur pour indiquer au système backend de répartir la charge lors de l’exécution d’opérations qui utilisent beaucoup `join` de ressources.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-150">**Use hints for performance**—Use hints with the `join` operator to instruct the backend to distribute load when running resource-intensive operations.</span></span> [<span data-ttu-id="a5c5e-151">En savoir plus sur les conseils d’adhésion</span><span class="sxs-lookup"><span data-stu-id="a5c5e-151">Learn more about join hints</span></span>](https://docs.microsoft.com/azure/data-explorer/kusto/query/joinoperator#join-hints)

    <span data-ttu-id="a5c5e-152">Par exemple, le conseil **[de](https://docs.microsoft.com/azure/data-explorer/kusto/query/shufflequery)** mélange permet d’améliorer les performances des requêtes lors de la jointation de tables à l’aide d’une clé avec une cardinalité élevée (clé avec de nombreuses valeurs uniques), comme dans la requête ci-dessous `AccountObjectId` :</span><span class="sxs-lookup"><span data-stu-id="a5c5e-152">For example, the **[shuffle hint](https://docs.microsoft.com/azure/data-explorer/kusto/query/shufflequery)** helps improve query performance when joining tables using a key with high cardinality—a key with many unique values—such as the `AccountObjectId` in the query below:</span></span>

    ```kusto
    IdentityInfo
    | where JobTitle == "CONSULTANT"
    | join hint.shufflekey = AccountObjectId 
    (IdentityDirectoryEvents
        | where Application == "Active Directory"
        | where ActionType == "Private data retrieval")
    on AccountObjectId 
    ```
    
    <span data-ttu-id="a5c5e-153">**[L’indication de diffusion](https://docs.microsoft.com/azure/data-explorer/kusto/query/broadcastjoin)** est utile lorsque le tableau de gauche est petit (jusqu’à 100 000 enregistrements) et que la table de droite est extrêmement grande.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-153">The **[broadcast hint](https://docs.microsoft.com/azure/data-explorer/kusto/query/broadcastjoin)** helps when the left table is small (up to 100,000 records) and the right table is extremely large.</span></span> <span data-ttu-id="a5c5e-154">Par exemple, la requête ci-dessous tente de joindre quelques e-mails ayant des sujets spécifiques avec tous les _messages_ contenant des liens dans le `EmailUrlInfo` tableau :</span><span class="sxs-lookup"><span data-stu-id="a5c5e-154">For example, the query below is trying to join a few emails that have specific subjects with _all_ messages containing links in the `EmailUrlInfo` table:</span></span>

    ```kusto
    EmailEvents 
    | where Subject in ("Warning: Update your credentials now", "Action required: Update your credentials now")
    | join hint.strategy = broadcast EmailUrlInfo on NetworkMessageId 
    ```

## <a name="optimize-the-summarize-operator"></a><span data-ttu-id="a5c5e-155">Optimiser `summarize` l’opérateur</span><span class="sxs-lookup"><span data-stu-id="a5c5e-155">Optimize the `summarize` operator</span></span>
<span data-ttu-id="a5c5e-156">[L’opérateur de synthèse](https://docs.microsoft.com/azure/data-explorer/kusto/query/summarizeoperator) agrège le contenu d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-156">The [summarize operator](https://docs.microsoft.com/azure/data-explorer/kusto/query/summarizeoperator) aggregates the contents of a table.</span></span> <span data-ttu-id="a5c5e-157">Appliquez ces conseils pour optimiser les requêtes qui utilisent cet opérateur.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-157">Apply these tips to optimize queries that use this operator.</span></span>

- <span data-ttu-id="a5c5e-158">**Rechercher des valeurs distinctes**: en général, utilisez cette recherche pour `summarize` rechercher des valeurs distinctes qui peuvent être répétitives.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-158">**Find distinct values**—In general, use `summarize` to find distinct values that can be repetitive.</span></span> <span data-ttu-id="a5c5e-159">Il peut être inutile de l’utiliser pour agréger des colonnes qui n’ont pas de valeurs répétitives.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-159">It can be unnecessary to use it to aggregate columns that don't have repetitive values.</span></span>

    <span data-ttu-id="a5c5e-160">Bien qu’un seul e-mail puisse faire  partie de plusieurs événements, l’exemple ci-dessous n’est pas une utilisation efficace, car un ID de message réseau pour un message électronique individuel est toujours fourni avec une adresse d’expéditeur `summarize` unique.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-160">While a single email can be part of multiple events, the example below is _not_ an efficient use of `summarize` because a network message ID for an individual email always comes with a unique sender address.</span></span>
 
    ```kusto
    EmailEvents  
    | where Timestamp > ago(1h)
    | summarize by NetworkMessageId, SenderFromAddress   
    ```
    <span data-ttu-id="a5c5e-161">L’opérateur peut être facilement remplacé par , ce qui donne potentiellement les mêmes résultats `summarize` `project` tout en consommant moins de ressources :</span><span class="sxs-lookup"><span data-stu-id="a5c5e-161">The `summarize` operator can be easily replaced with `project`, yielding potentially the same results while consuming fewer resources:</span></span>

    ```kusto
    EmailEvents  
    | where Timestamp > ago(1h)
    | project NetworkMessageId, SenderFromAddress   
    ```
    <span data-ttu-id="a5c5e-162">L’exemple suivant est une utilisation plus efficace, car il peut y avoir plusieurs instances distinctes d’une adresse d’expéditeur envoyant des messages électroniques `summarize` à la même adresse de destinataire.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-162">The following example is a more efficient use of `summarize` because there can be multiple distinct instances of a sender address sending email to the same recipient address.</span></span> <span data-ttu-id="a5c5e-163">Ces combinaisons sont moins distinctes et sont susceptibles d’avoir des doublons.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-163">Such combinations are less distinct and are likely to have duplicates.</span></span>

    ```kusto
    EmailEvents  
    | where Timestamp > ago(1h)
    | summarize by SenderFromAddress, RecipientEmailAddress   
    ```

- <span data-ttu-id="a5c5e-164">**Mélangez la requête .** Bien qu’il soit préférable d’utiliser les colonnes avec des valeurs répétitives, les mêmes colonnes peuvent également avoir une cardinalité élevée ou un grand nombre `summarize` de valeurs uniques. </span><span class="sxs-lookup"><span data-stu-id="a5c5e-164">**Shuffle the query**—While `summarize` is best used in columns with repetitive values, the same columns can also have _high cardinality_ or large numbers of unique values.</span></span> <span data-ttu-id="a5c5e-165">Comme l’opérateur, vous pouvez également appliquer le conseil de mélange avec pour répartir la charge de traitement et potentiellement améliorer les performances lorsque vous fonctionnez sur des colonnes avec `join` une [](https://docs.microsoft.com/azure/data-explorer/kusto/query/shufflequery) `summarize` cardinalité élevée.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-165">Like the `join` operator, you can also apply the [shuffle hint](https://docs.microsoft.com/azure/data-explorer/kusto/query/shufflequery) with `summarize` to distribute processing load and potentially improve performance when operating on columns with high cardinality.</span></span>

    <span data-ttu-id="a5c5e-166">La requête ci-dessous permet de compter des adresses de messagerie de destinataire distinctes, qui peuvent s’exécuter par centaines de `summarize` milliers dans les grandes organisations.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-166">The query below uses `summarize` to count distinct recipient email address, which can run in the hundreds of thousands in large organizations.</span></span> <span data-ttu-id="a5c5e-167">Pour améliorer les performances, elle intègre `hint.shufflekey` :</span><span class="sxs-lookup"><span data-stu-id="a5c5e-167">To improve performance, it incorporates `hint.shufflekey`:</span></span>

    ```kusto
    EmailEvents  
    | where Timestamp > ago(1h)
    | summarize hint.shufflekey = RecipientEmailAddress count() by Subject, RecipientEmailAddress
    ```

## <a name="query-scenarios"></a><span data-ttu-id="a5c5e-168">Scénarios de requête</span><span class="sxs-lookup"><span data-stu-id="a5c5e-168">Query scenarios</span></span>

### <a name="identify-unique-processes-with-process-ids"></a><span data-ttu-id="a5c5e-169">Identifier des processus uniques avec des ID de processus</span><span class="sxs-lookup"><span data-stu-id="a5c5e-169">Identify unique processes with process IDs</span></span>
<span data-ttu-id="a5c5e-170">Les ID de processus (PID) sont recyclés dans Windows et réutilisés pour les nouveaux processus.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-170">Process IDs (PIDs) are recycled in Windows and reused for new processes.</span></span> <span data-ttu-id="a5c5e-171">Ils ne peuvent pas être utilisés comme identificateurs uniques pour des processus spécifiques.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-171">On their own, they can't serve as unique identifiers for specific processes.</span></span>

<span data-ttu-id="a5c5e-172">Pour obtenir un identificateur unique pour un processus sur un ordinateur spécifique, utilisez l’ID de processus conjointement avec l’heure de création du processus.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-172">To get a unique identifier for a process on a specific machine, use the process ID together with the process creation time.</span></span> <span data-ttu-id="a5c5e-173">Lorsque vous rejoignez ou résumez des données autour des processus, incluez des colonnes pour l’identificateur de l’ordinateur (`DeviceId` ou `DeviceName`), l’ID de processus (`ProcessId` ou `InitiatingProcessId`) et l’heure de création du processus (`ProcessCreationTime` ou `InitiatingProcessCreationTime`).</span><span class="sxs-lookup"><span data-stu-id="a5c5e-173">When you join or summarize data around processes, include columns for the machine identifier (either `DeviceId` or `DeviceName`), the process ID (`ProcessId` or `InitiatingProcessId`), and the process creation time (`ProcessCreationTime` or `InitiatingProcessCreationTime`)</span></span>

<span data-ttu-id="a5c5e-174">L’exemple de requête suivant trouve les processus qui accèdent à plus de 10 adresses IP via le port 445 (SMB), qui peut rechercher des partages de fichiers.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-174">The following example query finds processes that access more than 10 IP addresses over port 445 (SMB), possibly scanning for file shares.</span></span>

<span data-ttu-id="a5c5e-175">Exemples de requête :</span><span class="sxs-lookup"><span data-stu-id="a5c5e-175">Example query:</span></span>
```kusto
DeviceNetworkEvents
| where RemotePort == 445 and Timestamp > ago(12h) and InitiatingProcessId !in (0, 4)
| summarize RemoteIPCount=dcount(RemoteIP) by DeviceName, InitiatingProcessId
InitiatingProcessCreationTime, InitiatingProcessFileName
| where RemoteIPCount > 10
```

<span data-ttu-id="a5c5e-176">La requête se résume par `InitiatingProcessId` et `InitiatingProcessCreationTime` de sorte qu’elle examine un seul processus, sans mélanger plusieurs processus ayant le même ID de processus.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-176">The query summarizes by both `InitiatingProcessId` and `InitiatingProcessCreationTime` so that it looks at a single process, without mixing multiple processes with the same process ID.</span></span>

### <a name="query-command-lines"></a><span data-ttu-id="a5c5e-177">Lignes de commande de requête</span><span class="sxs-lookup"><span data-stu-id="a5c5e-177">Query command lines</span></span>
<span data-ttu-id="a5c5e-178">Plusieurs méthodes s’offrent à vous pour créer une ligne de commande pour accomplir une tâche.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-178">There are numerous ways to construct a command line to accomplish a task.</span></span> <span data-ttu-id="a5c5e-179">Par exemple, un attaquant peut faire référence à un fichier image sans chemin d’accès, sans extension de fichier, à l’aide de variables d’environnement ou de guillemets.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-179">For example, an attacker could reference an image file without a path, without a file extension, using environment variables, or with quotes.</span></span> <span data-ttu-id="a5c5e-180">L’attaquant peut également modifier l’ordre des paramètres ou ajouter plusieurs guillemets et espaces.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-180">The attacker could also change the order of parameters or add multiple quotes and spaces.</span></span>

<span data-ttu-id="a5c5e-181">Pour créer des requêtes plus durables autour des lignes de commande, appliquez les pratiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="a5c5e-181">To create more durable queries around command lines, apply the following practices:</span></span>

- <span data-ttu-id="a5c5e-182">Identifiez les processus connus (tels que *net.exe* ou *psexec.exe*) en correspondant sur les champs de nom de fichier, au lieu de filtrer sur la ligne de commande elle-même.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-182">Identify the known processes (such as *net.exe* or *psexec.exe*) by matching on the file name fields, instead of filtering on the command-line itself.</span></span>
- <span data-ttu-id="a5c5e-183">Parse command-line sections using the [parse_command_line() function](https://docs.microsoft.com/azure/data-explorer/kusto/query/parse-command-line)</span><span class="sxs-lookup"><span data-stu-id="a5c5e-183">Parse command-line sections using the [parse_command_line() function](https://docs.microsoft.com/azure/data-explorer/kusto/query/parse-command-line)</span></span> 
- <span data-ttu-id="a5c5e-184">Lors de l’interrogation des arguments de la ligne de commande, ne recherchez pas une correspondance exacte de plusieurs arguments non liés dans un certain ordre.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-184">When querying for command-line arguments, don't look for an exact match on multiple unrelated arguments in a certain order.</span></span> <span data-ttu-id="a5c5e-185">Au lieu de cela, vous devez utiliser des expressions régulières ou utiliser plusieurs opérateurs de contenu séparés..</span><span class="sxs-lookup"><span data-stu-id="a5c5e-185">Instead, use regular expressions or use multiple separate contains operators.</span></span>
- <span data-ttu-id="a5c5e-186">Utilisez des correspondances non respectées de casse.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-186">Use case insensitive matches.</span></span> <span data-ttu-id="a5c5e-187">Par exemple, utilisez `=~` , et à la place de , et `in~` `contains` `==` `in` `contains_cs` .</span><span class="sxs-lookup"><span data-stu-id="a5c5e-187">For example, use `=~`, `in~`, and `contains` instead of `==`, `in`, and `contains_cs`.</span></span>
- <span data-ttu-id="a5c5e-188">Pour atténuer les techniques d’obfuscation de ligne de commande, envisagez de supprimer des guillemets, de remplacer les virgules par des espaces et de remplacer plusieurs espaces consécutifs par un espace unique.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-188">To mitigate command-line obfuscation techniques, consider removing quotes, replacing commas with spaces, and replacing multiple consecutive spaces with a single space.</span></span> <span data-ttu-id="a5c5e-189">Il existe des techniques d’obfuscation plus complexes qui nécessitent d’autres approches, mais ces ajustements peuvent aider à résoudre les problèmes courants.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-189">There are more complex obfuscation techniques that require other approaches, but these tweaks can help address common ones.</span></span>

<span data-ttu-id="a5c5e-190">Les exemples suivants montrent différentes façons de construire une requête qui recherche le fichier *net.exe* pour arrêter le service de pare-feu « MpsSvc » :</span><span class="sxs-lookup"><span data-stu-id="a5c5e-190">The following examples show various ways to construct a query that looks for the file *net.exe* to stop the firewall service "MpsSvc":</span></span>

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

### <a name="ingest-data-from-external-sources"></a><span data-ttu-id="a5c5e-191">Ing d’ing de données provenant de sources externes</span><span class="sxs-lookup"><span data-stu-id="a5c5e-191">Ingest data from external sources</span></span>
<span data-ttu-id="a5c5e-192">Pour incorporer des listes longues ou de grandes tables dans votre requête, utilisez l’opérateur [externaldata](https://docs.microsoft.com/azure/data-explorer/kusto/query/externaldata-operator) pour ingère les données d’un URI spécifié.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-192">To incorporate long lists or large tables into your query, use the [externaldata operator](https://docs.microsoft.com/azure/data-explorer/kusto/query/externaldata-operator) to ingest data from a specified URI.</span></span> <span data-ttu-id="a5c5e-193">Vous pouvez obtenir des données à partir de fichiers au format TXT, CSV, JSON ou [d’autres formats.](https://docs.microsoft.com/azure/data-explorer/ingestion-supported-formats)</span><span class="sxs-lookup"><span data-stu-id="a5c5e-193">You can get data from files in TXT, CSV, JSON, or [other formats](https://docs.microsoft.com/azure/data-explorer/ingestion-supported-formats).</span></span> <span data-ttu-id="a5c5e-194">L’exemple ci-dessous montre comment vous pouvez utiliser la liste complète des codes de hoche SHA-256 des programmes malveillants fournis par MalwareBazaar (abuse.ch) pour vérifier les pièces jointes sur les e-mails :</span><span class="sxs-lookup"><span data-stu-id="a5c5e-194">The example below shows how you can utilize the extensive list of malware SHA-256  hashes provided by MalwareBazaar (abuse.ch) to check attachments on emails:</span></span>

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
SHA256,ThreatTypes,DetectionMethods
```

### <a name="parse-strings"></a><span data-ttu-id="a5c5e-195">Parse strings</span><span class="sxs-lookup"><span data-stu-id="a5c5e-195">Parse strings</span></span>
<span data-ttu-id="a5c5e-196">Il existe différentes fonctions que vous pouvez utiliser pour gérer efficacement les chaînes qui doivent être traitées ou converties.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-196">There are various functions you can use to efficiently handle strings that need parsing or conversion.</span></span> 

| <span data-ttu-id="a5c5e-197">String</span><span class="sxs-lookup"><span data-stu-id="a5c5e-197">String</span></span> | <span data-ttu-id="a5c5e-198">Fonction</span><span class="sxs-lookup"><span data-stu-id="a5c5e-198">Function</span></span> | <span data-ttu-id="a5c5e-199">Exemple d'utilisation</span><span class="sxs-lookup"><span data-stu-id="a5c5e-199">Usage example</span></span> |
|--|--|--|
| <span data-ttu-id="a5c5e-200">Lignes de commande</span><span class="sxs-lookup"><span data-stu-id="a5c5e-200">Command-lines</span></span> | [<span data-ttu-id="a5c5e-201">parse_command_line()</span><span class="sxs-lookup"><span data-stu-id="a5c5e-201">parse_command_line()</span></span>](https://docs.microsoft.com/azure/data-explorer/kusto/query/parse-command-line) | <span data-ttu-id="a5c5e-202">Extraire la commande et tous les arguments.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-202">Extract the command and all arguments.</span></span> | 
| <span data-ttu-id="a5c5e-203">Paths</span><span class="sxs-lookup"><span data-stu-id="a5c5e-203">Paths</span></span> | [<span data-ttu-id="a5c5e-204">parse_path()</span><span class="sxs-lookup"><span data-stu-id="a5c5e-204">parse_path()</span></span>](https://docs.microsoft.com/azure/data-explorer/kusto/query/parsepathfunction) | <span data-ttu-id="a5c5e-205">Extraire les sections d’un chemin d’accès à un fichier ou un dossier.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-205">Extract the sections of a file or folder path.</span></span> |
| <span data-ttu-id="a5c5e-206">Numéros de version</span><span class="sxs-lookup"><span data-stu-id="a5c5e-206">Version numbers</span></span> | [<span data-ttu-id="a5c5e-207">parse_version()</span><span class="sxs-lookup"><span data-stu-id="a5c5e-207">parse_version()</span></span>](https://docs.microsoft.com/azure/data-explorer/kusto/query/parse-versionfunction) | <span data-ttu-id="a5c5e-208">Déconstruire un numéro de version avec jusqu’à quatre sections et jusqu’à huit caractères par section.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-208">Deconstruct a version number with up to four sections and up to eight characters per section.</span></span> <span data-ttu-id="a5c5e-209">Utilisez les données analyse pour comparer l’âge de la version.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-209">Use the parsed data to compare version age.</span></span> |
| <span data-ttu-id="a5c5e-210">Adresses IPv4</span><span class="sxs-lookup"><span data-stu-id="a5c5e-210">IPv4 addresses</span></span> | [<span data-ttu-id="a5c5e-211">parse_ipv4()</span><span class="sxs-lookup"><span data-stu-id="a5c5e-211">parse_ipv4()</span></span>](https://docs.microsoft.com/azure/data-explorer/kusto/query/parse-ipv4function) | <span data-ttu-id="a5c5e-212">Convertissez une adresse IPv4 en un long integer.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-212">Convert an IPv4 address to a long integer.</span></span> <span data-ttu-id="a5c5e-213">Pour comparer les adresses IPv4 sans les convertir, [utilisez ipv4_compare()](https://docs.microsoft.com/azure/data-explorer/kusto/query/ipv4-comparefunction).</span><span class="sxs-lookup"><span data-stu-id="a5c5e-213">To compare IPv4 addresses without converting them, use [ipv4_compare()](https://docs.microsoft.com/azure/data-explorer/kusto/query/ipv4-comparefunction).</span></span> |
| <span data-ttu-id="a5c5e-214">Adresses IPv6</span><span class="sxs-lookup"><span data-stu-id="a5c5e-214">IPv6 addresses</span></span> | [<span data-ttu-id="a5c5e-215">parse_ipv6()</span><span class="sxs-lookup"><span data-stu-id="a5c5e-215">parse_ipv6()</span></span>](https://docs.microsoft.com/azure/data-explorer/kusto/query/parse-ipv6function)  | <span data-ttu-id="a5c5e-216">Convertissez une adresse IPv4 ou IPv6 en notation IPv6 canonique.</span><span class="sxs-lookup"><span data-stu-id="a5c5e-216">Convert an IPv4 or IPv6 address to the canonical IPv6 notation.</span></span> <span data-ttu-id="a5c5e-217">Pour comparer les adresses IPv6, [utilisez ipv6_compare()](https://docs.microsoft.com/azure/data-explorer/kusto/query/ipv6-comparefunction).</span><span class="sxs-lookup"><span data-stu-id="a5c5e-217">To compare IPv6 addresses, use [ipv6_compare()](https://docs.microsoft.com/azure/data-explorer/kusto/query/ipv6-comparefunction).</span></span> |

<span data-ttu-id="a5c5e-218">Pour en savoir plus sur toutes les fonctions d’parsage prise en charge, lisez la suite sur les fonctions [de chaîne Kusto.](https://docs.microsoft.com/azure/data-explorer/kusto/query/scalarfunctions#string-functions)</span><span class="sxs-lookup"><span data-stu-id="a5c5e-218">To learn about all supported parsing functions, [read about Kusto string functions](https://docs.microsoft.com/azure/data-explorer/kusto/query/scalarfunctions#string-functions).</span></span> 

## <a name="related-topics"></a><span data-ttu-id="a5c5e-219">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5c5e-219">Related topics</span></span>
- [<span data-ttu-id="a5c5e-220">Documentation sur le langage de requête Kusto</span><span class="sxs-lookup"><span data-stu-id="a5c5e-220">Kusto query language documentation</span></span>](https://docs.microsoft.com/azure/data-explorer/kusto/query/)
- [<span data-ttu-id="a5c5e-221">Paramètres d’utilisation et de quotas</span><span class="sxs-lookup"><span data-stu-id="a5c5e-221">Quotas and usage parameters</span></span>](advanced-hunting-limits.md)
- [<span data-ttu-id="a5c5e-222">Gérer les erreurs de recherche avancée</span><span class="sxs-lookup"><span data-stu-id="a5c5e-222">Handle advanced hunting errors</span></span>](advanced-hunting-errors.md)
- [<span data-ttu-id="a5c5e-223">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="a5c5e-223">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="a5c5e-224">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="a5c5e-224">Learn the query language</span></span>](advanced-hunting-query-language.md)
