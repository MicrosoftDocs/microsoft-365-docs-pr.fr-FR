---
title: Utiliser les résultats de la recherche avancée dans Microsoft Threat Protection
description: Tirer le meilleur parti des résultats de la requête renvoyés par la recherche avancée dans Microsoft Threat Protection
keywords: chasse aux menaces, recherche de menace, recherche sur les menaces informatiques, protection contre les menaces Microsoft, Microsoft 365, MTP, M365, recherche, requête, télémétrie, détections personnalisées, schéma, Kusto, Microsoft 365, protection contre les menaces Microsoft, visualisation, graphique, filtres, exploration
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
ms.openlocfilehash: f9838908ca0dbfb498601c3509b920b064a2eb22
ms.sourcegitcommit: 3b2fdf159d7dd962493a3838e3cf0cf429ee2bf2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "42929150"
---
# <a name="work-with-advanced-hunting-query-results"></a><span data-ttu-id="af5df-104">Utiliser les résultats de la recherche avancée de la chasse</span><span class="sxs-lookup"><span data-stu-id="af5df-104">Work with advanced hunting query results</span></span>

<span data-ttu-id="af5df-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="af5df-105">**Applies to:**</span></span>
- <span data-ttu-id="af5df-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="af5df-106">Microsoft Threat Protection</span></span>

[!INCLUDE [Prerelease information](../includes/prerelease.md)]

<span data-ttu-id="af5df-107">Bien que vous puissiez construire vos requêtes de [chasse avancées](advanced-hunting-overview.md) pour renvoyer des informations très précises, vous pouvez également utiliser les résultats de la requête pour mieux comprendre et examiner des activités et des indicateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="af5df-107">While you can construct your [advanced hunting](advanced-hunting-overview.md) queries to return very precise information, you can also work with the query results to gain further insight and investigate specific activities and indicators.</span></span> <span data-ttu-id="af5df-108">Vous pouvez effectuer les actions suivantes sur les résultats de votre requête :</span><span class="sxs-lookup"><span data-stu-id="af5df-108">You can take the following actions on your query results:</span></span>

- <span data-ttu-id="af5df-109">Afficher les résultats sous la forme d’un tableau ou d’un graphique</span><span class="sxs-lookup"><span data-stu-id="af5df-109">View results as a table or chart</span></span>
- <span data-ttu-id="af5df-110">Exporter des tableaux et des graphiques</span><span class="sxs-lookup"><span data-stu-id="af5df-110">Export tables and charts</span></span>
- <span data-ttu-id="af5df-111">Explorer les informations détaillées de l’entité</span><span class="sxs-lookup"><span data-stu-id="af5df-111">Drill down to detailed entity information</span></span>
- <span data-ttu-id="af5df-112">Affiner vos requêtes directement à partir des résultats ou appliquer des filtres</span><span class="sxs-lookup"><span data-stu-id="af5df-112">Tweak your queries directly from the results or apply filters</span></span>

## <a name="view-query-results-as-a-table-or-chart"></a><span data-ttu-id="af5df-113">Afficher les résultats de la requête sous la forme d’un tableau ou d’un graphique</span><span class="sxs-lookup"><span data-stu-id="af5df-113">View query results as a table or chart</span></span>
<span data-ttu-id="af5df-114">Par défaut, la chasse avancée affiche les résultats de la requête sous forme de données tabulaires.</span><span class="sxs-lookup"><span data-stu-id="af5df-114">By default, advanced hunting displays query results as tabular data.</span></span> <span data-ttu-id="af5df-115">Vous pouvez également afficher les mêmes données sous la forme d’un graphique.</span><span class="sxs-lookup"><span data-stu-id="af5df-115">You can also display the same data as a chart.</span></span> <span data-ttu-id="af5df-116">La chasse avancée prend en charge les affichages suivants :</span><span class="sxs-lookup"><span data-stu-id="af5df-116">Advanced hunting supports the following views:</span></span>

| <span data-ttu-id="af5df-117">Type d’affichage</span><span class="sxs-lookup"><span data-stu-id="af5df-117">View type</span></span> | <span data-ttu-id="af5df-118">Description</span><span class="sxs-lookup"><span data-stu-id="af5df-118">Description</span></span> |
| -- | -- |
| <span data-ttu-id="af5df-119">**Table**</span><span class="sxs-lookup"><span data-stu-id="af5df-119">**Table**</span></span> | <span data-ttu-id="af5df-120">Affiche les résultats de la requête sous forme de tableau</span><span class="sxs-lookup"><span data-stu-id="af5df-120">Displays the query results in tabular format</span></span> |
| <span data-ttu-id="af5df-121">**Histogramme**</span><span class="sxs-lookup"><span data-stu-id="af5df-121">**Column chart**</span></span> | <span data-ttu-id="af5df-122">Affiche une série d’éléments uniques sur l’axe des x sous forme de barres verticales dont les hauteurs représentent les valeurs numériques d’un autre champ</span><span class="sxs-lookup"><span data-stu-id="af5df-122">Renders a series of unique items on the x-axis as vertical bars whose heights represent numeric values from another field</span></span> |
| <span data-ttu-id="af5df-123">**Histogramme empilé**</span><span class="sxs-lookup"><span data-stu-id="af5df-123">**Stacked column chart**</span></span> | <span data-ttu-id="af5df-124">Affiche une série d’éléments uniques sur l’axe des x sous forme de barres verticales empilées dont les hauteurs représentent les valeurs numériques d’un ou plusieurs autres champs</span><span class="sxs-lookup"><span data-stu-id="af5df-124">Renders a series of unique items on the x-axis as stacked vertical bars whose heights represent numeric values from one or more other fields</span></span> |
| <span data-ttu-id="af5df-125">**Graphique en secteurs**</span><span class="sxs-lookup"><span data-stu-id="af5df-125">**Pie chart**</span></span> | <span data-ttu-id="af5df-126">Affiche les secteurs de section représentant des éléments uniques.</span><span class="sxs-lookup"><span data-stu-id="af5df-126">Renders sectional pies representing unique items.</span></span> <span data-ttu-id="af5df-127">La taille de chaque graphique représente les valeurs numériques d’un autre champ.</span><span class="sxs-lookup"><span data-stu-id="af5df-127">The size of each pie represents numeric values from another field.</span></span> |
| <span data-ttu-id="af5df-128">**Graphique en bouée**</span><span class="sxs-lookup"><span data-stu-id="af5df-128">**Donut chart**</span></span> | <span data-ttu-id="af5df-129">Affiche les arcs de section représentant des éléments uniques.</span><span class="sxs-lookup"><span data-stu-id="af5df-129">Renders sectional arcs representing unique items.</span></span> <span data-ttu-id="af5df-130">La longueur de chaque arc représente les valeurs numériques d’un autre champ.</span><span class="sxs-lookup"><span data-stu-id="af5df-130">The length of each arc represents numeric values from another field.</span></span> |
| <span data-ttu-id="af5df-131">**Graphique en courbes**</span><span class="sxs-lookup"><span data-stu-id="af5df-131">**Line chart**</span></span> | <span data-ttu-id="af5df-132">Trace les valeurs numériques d’une série d’éléments uniques et connecte les valeurs tracées</span><span class="sxs-lookup"><span data-stu-id="af5df-132">Plots numeric values for a series of unique items and connects the plotted values</span></span> |
| <span data-ttu-id="af5df-133">**Nuages de points**</span><span class="sxs-lookup"><span data-stu-id="af5df-133">**Scatter chart**</span></span> | <span data-ttu-id="af5df-134">Trace les valeurs numériques d’une série d’éléments uniques</span><span class="sxs-lookup"><span data-stu-id="af5df-134">Plots numeric values for a series of unique items</span></span> |
| <span data-ttu-id="af5df-135">**Graphique en aires**</span><span class="sxs-lookup"><span data-stu-id="af5df-135">**Area chart**</span></span> | <span data-ttu-id="af5df-136">Trace les valeurs numériques d’une série d’éléments uniques et remplit les sections sous les valeurs tracées.</span><span class="sxs-lookup"><span data-stu-id="af5df-136">Plots numeric values for a series of unique items and fills the sections below the plotted values</span></span> |

### <a name="construct-queries-for-effective-charts"></a><span data-ttu-id="af5df-137">Créer des requêtes pour des graphiques efficaces</span><span class="sxs-lookup"><span data-stu-id="af5df-137">Construct queries for effective charts</span></span>
<span data-ttu-id="af5df-138">Lors du rendu des graphiques, la chasse avancée identifie automatiquement les colonnes d’intérêt et les valeurs numériques à agréger.</span><span class="sxs-lookup"><span data-stu-id="af5df-138">When rendering charts, advanced hunting automatically identifies columns of interest and the numeric values to aggregate.</span></span> <span data-ttu-id="af5df-139">Pour obtenir des graphiques significatifs, construisez vos requêtes pour renvoyer les valeurs spécifiques que vous souhaitez voir visibles.</span><span class="sxs-lookup"><span data-stu-id="af5df-139">To get meaningful charts, construct your queries to return the specific values you want to see visualized.</span></span> <span data-ttu-id="af5df-140">Voici quelques exemples de requêtes et les graphiques qui en résultent.</span><span class="sxs-lookup"><span data-stu-id="af5df-140">Here are some sample queries and the resulting charts.</span></span>

#### <a name="alerts-by-severity"></a><span data-ttu-id="af5df-141">Alertes par gravité</span><span class="sxs-lookup"><span data-stu-id="af5df-141">Alerts by severity</span></span>
<span data-ttu-id="af5df-142">Utilisez l' `summarize` opérateur pour obtenir le nombre de chiffres des valeurs que vous souhaitez graphiquer.</span><span class="sxs-lookup"><span data-stu-id="af5df-142">Use the `summarize` operator to obtain a numeric count of the values you want to chart.</span></span> <span data-ttu-id="af5df-143">La requête ci-dessous `summarize` utilise l’opérateur pour obtenir le nombre d’alertes par gravité.</span><span class="sxs-lookup"><span data-stu-id="af5df-143">The query below uses the `summarize` operator to get the number of alerts by severity.</span></span>

```kusto
AlertInfo
| summarize Total = count() by Severity
```
<span data-ttu-id="af5df-144">Lors du rendu des résultats, un histogramme affiche chaque valeur de gravité sous la forme d’une colonne distincte :</span><span class="sxs-lookup"><span data-stu-id="af5df-144">When rendering the results, a column chart displays each severity value as a separate column:</span></span>

<span data-ttu-id="af5df-145">![Image des résultats de la recherche avancée de la chasse affichés](../../media/advanced-hunting-column-chart.jpg)
sous la forme d’un graphique en histogramme*résultats de la requête pour les alertes par gravité affichée sous forme de graphique en histogrammes*</span><span class="sxs-lookup"><span data-stu-id="af5df-145">![Image of advanced hunting query results displayed as a column chart](../../media/advanced-hunting-column-chart.jpg)
*Query results for alerts by severity displayed as a column chart*</span></span>

#### <a name="alert-severity-by-operating-system"></a><span data-ttu-id="af5df-146">Gravité des alertes par système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="af5df-146">Alert severity by operating system</span></span>
<span data-ttu-id="af5df-147">Vous pouvez également utiliser l' `summarize` opérateur pour préparer les résultats pour les valeurs de graphique de plusieurs champs.</span><span class="sxs-lookup"><span data-stu-id="af5df-147">You could also use the `summarize` operator to prepare results for charting values from multiple fields.</span></span> <span data-ttu-id="af5df-148">Par exemple, vous souhaiterez peut-être comprendre comment les niveaux d’alerte sont distribués entre les systèmes d’exploitation (OS).</span><span class="sxs-lookup"><span data-stu-id="af5df-148">For example, you might want to understand how alert severities are distributed across operating systems (OS).</span></span> 

<span data-ttu-id="af5df-149">La requête ci-dessous `join` utilise un opérateur pour extraire les informations du `DeviceInfo` système d’exploitation à partir `summarize` de la table, puis utilise `OSPlatform` pour `Severity` compter les valeurs dans les colonnes et :</span><span class="sxs-lookup"><span data-stu-id="af5df-149">The query below uses a `join` operator to pull in OS information from the `DeviceInfo` table, and then uses `summarize` to count values in both the `OSPlatform` and `Severity` columns:</span></span>

```kusto
AlertInfo
| join AlertEvidence on AlertId
| join DeviceInfo on DeviceId
| summarize Count = count() by OSPlatform, Severity 
```
<span data-ttu-id="af5df-150">Ces résultats sont optimisés à l’aide d’un histogramme empilé :</span><span class="sxs-lookup"><span data-stu-id="af5df-150">These results are best visualized using a stacked column chart:</span></span>

<span data-ttu-id="af5df-151">![Image des résultats de la recherche avancée de la chasse affichés sous](../../media/advanced-hunting-stacked-chart.jpg)
la forme d’un graphique empilé*de résultats de requête pour les alertes par système d’exploitation et gravité affichées sous la forme d’un graphique empilé*</span><span class="sxs-lookup"><span data-stu-id="af5df-151">![Image of advanced hunting query results displayed as a stacked chart](../../media/advanced-hunting-stacked-chart.jpg)
*Query results for alerts by OS and severity displayed as a stacked chart*</span></span>

#### <a name="phishing-emails-across-top-ten-sender-domains"></a><span data-ttu-id="af5df-152">Courriers électroniques de hameçonnage sur les dix principaux domaines d’expéditeur</span><span class="sxs-lookup"><span data-stu-id="af5df-152">Phishing emails across top ten sender domains</span></span>
<span data-ttu-id="af5df-153">Si vous avez affaire à une liste de valeurs qui n’est pas finie, vous pouvez `Top` utiliser l’opérateur pour graphiquer uniquement les valeurs avec le plus d’instances.</span><span class="sxs-lookup"><span data-stu-id="af5df-153">If you're dealing with a list of values that isn’t finite, you can use the `Top` operator to chart only the values with the most instances.</span></span> <span data-ttu-id="af5df-154">Par exemple, pour obtenir les dix principaux domaines d’expéditeur avec le plus de courriers électroniques de hameçonnage, utilisez la requête ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="af5df-154">For example, to get the top ten sender domains with the most phishing emails, use the query below:</span></span>

```kusto
EmailEvents
| where PhishFilterVerdict == "Phish"
| summarize Count = count() by SenderFromDomain
| top 10 by Count
```
<span data-ttu-id="af5df-155">Utilisez la vue de graphique à secteurs pour afficher efficacement la distribution dans les domaines principaux :</span><span class="sxs-lookup"><span data-stu-id="af5df-155">Use the pie chart view to effectively show distribution across the top domains:</span></span>

<span data-ttu-id="af5df-156">![Image des résultats de la recherche avancée de la chasse affichée](../../media/advanced-hunting-pie-chart.jpg)
sous la forme d’un graphique en secteurs*illustrant la répartition des courriers électroniques de hameçonnage sur les domaines d’expéditeurs les plus fréquents*</span><span class="sxs-lookup"><span data-stu-id="af5df-156">![Image of advanced hunting query results displayed as a pie chart](../../media/advanced-hunting-pie-chart.jpg)
*Pie chart showing distribution of phishing emails across top sender domains*</span></span>

#### <a name="file-activities-over-time"></a><span data-ttu-id="af5df-157">Activités des fichiers dans le temps</span><span class="sxs-lookup"><span data-stu-id="af5df-157">File activities over time</span></span>
<span data-ttu-id="af5df-158">À l' `summarize` aide de l' `bin()` opérateur avec la fonction, vous pouvez rechercher des événements impliquant un indicateur particulier dans le temps.</span><span class="sxs-lookup"><span data-stu-id="af5df-158">Using the `summarize` operator with the `bin()` function, you can check for events involving a particular indicator over time.</span></span> <span data-ttu-id="af5df-159">La requête ci-dessous compte les événements `invoice.doc` impliquant le fichier à des intervalles de 30 minutes pour afficher les pics d’activité liés à ce fichier :</span><span class="sxs-lookup"><span data-stu-id="af5df-159">The query below counts events involving the file `invoice.doc` at 30 minute intervals to show spikes in activity related to that file:</span></span>

```kusto
AppFileEvents
| union DeviceFileEvents
| where FileName == "invoice.doc"
| summarize FileCount = count() by bin(Timestamp, 30m)
```
<span data-ttu-id="af5df-160">Le graphique en courbes ci-dessous met clairement en évidence les `invoice.doc`périodes d’activité impliquant :</span><span class="sxs-lookup"><span data-stu-id="af5df-160">The line chart below clearly highlights time periods with more activity involving `invoice.doc`:</span></span> 

<span data-ttu-id="af5df-161">![Image des résultats de la recherche avancée de la chasse affichée](../../media/advanced-hunting-line-chart.jpg)
sous la forme d’un graphique en courbes*illustrant le nombre d’événements impliquant un fichier dans le temps*</span><span class="sxs-lookup"><span data-stu-id="af5df-161">![Image of advanced hunting query results displayed as a line chart](../../media/advanced-hunting-line-chart.jpg)
*Line chart showing the number of events involving a file over time*</span></span>


## <a name="export-tables-and-charts"></a><span data-ttu-id="af5df-162">Exporter des tableaux et des graphiques</span><span class="sxs-lookup"><span data-stu-id="af5df-162">Export tables and charts</span></span>
<span data-ttu-id="af5df-163">Après avoir exécuté une requête, sélectionnez **Exporter** pour enregistrer les résultats dans un fichier local.</span><span class="sxs-lookup"><span data-stu-id="af5df-163">After running a query, select **Export** to save the results to local file.</span></span> <span data-ttu-id="af5df-164">L’affichage choisi détermine la façon dont les résultats sont exportés :</span><span class="sxs-lookup"><span data-stu-id="af5df-164">Your chosen view determines how the results are exported:</span></span>

- <span data-ttu-id="af5df-165">**Affichage tableau** : les résultats de la requête sont exportés sous forme de tableau sous forme de classeur Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="af5df-165">**Table view** — the query results are exported in tabular form as a Microsoft Excel workbook</span></span>
- <span data-ttu-id="af5df-166">**N’importe quel graphique** : les résultats de la requête sont exportés sous la forme d’une image JPEG du graphique affiché</span><span class="sxs-lookup"><span data-stu-id="af5df-166">**Any chart** — the query results are exported as a JPEG image of the rendered chart</span></span>

## <a name="drill-down-from-query-results"></a><span data-ttu-id="af5df-167">Explorer les résultats de la requête</span><span class="sxs-lookup"><span data-stu-id="af5df-167">Drill down from query results</span></span>
<span data-ttu-id="af5df-168">Pour afficher plus d’informations sur les entités, telles que des ordinateurs, fichiers, utilisateurs, adresses IP et URL, dans les résultats de votre requête, cliquez simplement sur l’identificateur d’entité.</span><span class="sxs-lookup"><span data-stu-id="af5df-168">To view more information about entities, such as machines, files, users, IP addresses, and URLs, in your query results, simply click the entity identifier.</span></span> <span data-ttu-id="af5df-169">Une page de profil détaillée s’ouvre pour l’entité sélectionnée dans le Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="af5df-169">This opens a detailed profile page for the selected entity in Microsoft Defender Security Center.</span></span>

## <a name="tweak-your-queries-from-the-results"></a><span data-ttu-id="af5df-170">Adaptez vos requêtes à partir des résultats</span><span class="sxs-lookup"><span data-stu-id="af5df-170">Tweak your queries from the results</span></span>
<span data-ttu-id="af5df-171">Cliquez avec le bouton droit de la souris sur une valeur du jeu de résultats pour améliorer rapidement votre requête.</span><span class="sxs-lookup"><span data-stu-id="af5df-171">Right-click a value in the result set to quickly enhance your query.</span></span> <span data-ttu-id="af5df-172">Vous pouvez utiliser les options suivantes pour :</span><span class="sxs-lookup"><span data-stu-id="af5df-172">You can use the options to:</span></span>

- <span data-ttu-id="af5df-173">Rechercher explicitement la valeur sélectionnée (`==`)</span><span class="sxs-lookup"><span data-stu-id="af5df-173">Explicitly look for the selected value (`==`)</span></span>
- <span data-ttu-id="af5df-174">Exclure la valeur sélectionnée de la requête (`!=`)</span><span class="sxs-lookup"><span data-stu-id="af5df-174">Exclude the selected value from the query (`!=`)</span></span>
- <span data-ttu-id="af5df-175">Obtenez des opérateurs plus avancés pour ajouter la valeur à votre requête (par exemple, `contains`, `starts with` et `ends with`)</span><span class="sxs-lookup"><span data-stu-id="af5df-175">Get more advanced operators for adding the value to your query, such as `contains`, `starts with` and `ends with`</span></span> 

![Image du jeu de résultats de la chasse avancée](../../media/advanced-hunting-results-filter.png)

## <a name="filter-the-query-results"></a><span data-ttu-id="af5df-177">Filtrer les résultats de la requête</span><span class="sxs-lookup"><span data-stu-id="af5df-177">Filter the query results</span></span>
<span data-ttu-id="af5df-178">Les filtres de droite fournissent un résumé du jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="af5df-178">The filters displayed to the right provide a summary of the result set.</span></span> <span data-ttu-id="af5df-179">Chaque colonne possède sa propre section qui répertorie les valeurs distinctes trouvées pour cette colonne et le nombre d’instances.</span><span class="sxs-lookup"><span data-stu-id="af5df-179">Each column has its own section that lists the distinct values found for that column and the number of instances.</span></span>

<span data-ttu-id="af5df-180">Affinez votre requête en sélectionnant `+` les `-` boutons ou sur les valeurs que vous souhaitez inclure ou exclure, puis en sélectionnant **exécuter la requête**.</span><span class="sxs-lookup"><span data-stu-id="af5df-180">Refine your query by selecting the `+` or `-` buttons on the values that you want to include or exclude and then selecting **Run query**.</span></span>

![Image du filtre de repérage avancé](../../media/advanced-hunting-filter.png)

<span data-ttu-id="af5df-182">Une fois le filtre appliqué pour modifier la requête, puis exécuter la requête, les résultats sont mis à jour en conséquence.</span><span class="sxs-lookup"><span data-stu-id="af5df-182">Once you apply the filter to modify the query and then run the query, the results are updated accordingly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af5df-183">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="af5df-183">Related topics</span></span>
- [<span data-ttu-id="af5df-184">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="af5df-184">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="af5df-185">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="af5df-185">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="af5df-186">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="af5df-186">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="af5df-187">Repérer les menaces sur divers appareils et e-mails</span><span class="sxs-lookup"><span data-stu-id="af5df-187">Hunt for threats across devices and emails</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="af5df-188">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="af5df-188">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="af5df-189">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="af5df-189">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
- [<span data-ttu-id="af5df-190">Vue d’ensemble des détections personnalisées</span><span class="sxs-lookup"><span data-stu-id="af5df-190">Custom detections overview</span></span>](custom-detections-overview.md)
