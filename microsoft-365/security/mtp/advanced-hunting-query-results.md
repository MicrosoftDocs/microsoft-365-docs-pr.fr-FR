---
title: Travailler avec les résultats de requête de recherche avancée dans Microsoft 365 Defender
description: Exploitation des résultats de requête renvoyés par le recherche avancée dans Microsoft 365 Defender
keywords: repérage avancé, repérage de menace, repérage de cybermenace, protection microsoft contre les menaces, microsoft 365, mtp, m365, recherche, requête, télémétrie, détections personnalisées, schéma, kusto, microsoft 365, Protection Microsoft contre les menaces, visualisation, graphique, filtres, drill-down
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
ms.openlocfilehash: 462ba35f584b45bbfeb0d8a3de3b118ba1c9e17c
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49932321"
---
# <a name="work-with-advanced-hunting-query-results"></a><span data-ttu-id="d51b5-104">Travailler avec les résultats de requête de recherche avancée</span><span class="sxs-lookup"><span data-stu-id="d51b5-104">Work with advanced hunting query results</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="d51b5-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="d51b5-105">**Applies to:**</span></span>
- <span data-ttu-id="d51b5-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="d51b5-106">Microsoft 365 Defender</span></span>

[!INCLUDE [Prerelease information](../includes/prerelease.md)]

<span data-ttu-id="d51b5-107">Bien que vous [](advanced-hunting-overview.md) pouvez construire vos requêtes de recherche avancées pour renvoyer des informations très précises, vous pouvez également travailler avec les résultats de la requête pour obtenir des informations supplémentaires et examiner des activités et des indicateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="d51b5-107">While you can construct your [advanced hunting](advanced-hunting-overview.md) queries to return very precise information, you can also work with the query results to gain further insight and investigate specific activities and indicators.</span></span> <span data-ttu-id="d51b5-108">Vous pouvez prendre les mesures suivantes sur les résultats de votre requête :</span><span class="sxs-lookup"><span data-stu-id="d51b5-108">You can take the following actions on your query results:</span></span>

- <span data-ttu-id="d51b5-109">Afficher les résultats sous la mesure d’un tableau ou d’un graphique</span><span class="sxs-lookup"><span data-stu-id="d51b5-109">View results as a table or chart</span></span>
- <span data-ttu-id="d51b5-110">Exporter des tableaux et des graphiques</span><span class="sxs-lookup"><span data-stu-id="d51b5-110">Export tables and charts</span></span>
- <span data-ttu-id="d51b5-111">Accès aux informations détaillées sur l’entité</span><span class="sxs-lookup"><span data-stu-id="d51b5-111">Drill down to detailed entity information</span></span>
- <span data-ttu-id="d51b5-112">Ajustez vos requêtes directement à partir des résultats ou appliquez des filtres</span><span class="sxs-lookup"><span data-stu-id="d51b5-112">Tweak your queries directly from the results or apply filters</span></span>

## <a name="view-query-results-as-a-table-or-chart"></a><span data-ttu-id="d51b5-113">Afficher les résultats d’une requête sous la mesure d’un tableau ou d’un graphique</span><span class="sxs-lookup"><span data-stu-id="d51b5-113">View query results as a table or chart</span></span>
<span data-ttu-id="d51b5-114">Par défaut, le recherche avancée affiche les résultats de la requête sous la mesure de données tabulaires.</span><span class="sxs-lookup"><span data-stu-id="d51b5-114">By default, advanced hunting displays query results as tabular data.</span></span> <span data-ttu-id="d51b5-115">Vous pouvez également afficher les mêmes données qu’un graphique.</span><span class="sxs-lookup"><span data-stu-id="d51b5-115">You can also display the same data as a chart.</span></span> <span data-ttu-id="d51b5-116">Le recherche avancée prend en charge les affichages suivants :</span><span class="sxs-lookup"><span data-stu-id="d51b5-116">Advanced hunting supports the following views:</span></span>

| <span data-ttu-id="d51b5-117">Type d’affichage</span><span class="sxs-lookup"><span data-stu-id="d51b5-117">View type</span></span> | <span data-ttu-id="d51b5-118">Description</span><span class="sxs-lookup"><span data-stu-id="d51b5-118">Description</span></span> |
| -- | -- |
| <span data-ttu-id="d51b5-119">**Table**</span><span class="sxs-lookup"><span data-stu-id="d51b5-119">**Table**</span></span> | <span data-ttu-id="d51b5-120">Affiche les résultats de la requête au format tabulaire</span><span class="sxs-lookup"><span data-stu-id="d51b5-120">Displays the query results in tabular format</span></span> |
| <span data-ttu-id="d51b5-121">**Graphique en colonnes**</span><span class="sxs-lookup"><span data-stu-id="d51b5-121">**Column chart**</span></span> | <span data-ttu-id="d51b5-122">Restituer une série d’éléments uniques sur l’axe des x sous forme de barres verticales dont les hauteurs représentent des valeurs numériques d’un autre champ</span><span class="sxs-lookup"><span data-stu-id="d51b5-122">Renders a series of unique items on the x-axis as vertical bars whose heights represent numeric values from another field</span></span> |
| <span data-ttu-id="d51b5-123">**Graphique en colonnes empilées**</span><span class="sxs-lookup"><span data-stu-id="d51b5-123">**Stacked column chart**</span></span> | <span data-ttu-id="d51b5-124">Restituer une série d’éléments uniques sur l’axe des X sous forme de barres verticales empilées dont les hauteurs représentent des valeurs numériques d’un ou plusieurs autres champs</span><span class="sxs-lookup"><span data-stu-id="d51b5-124">Renders a series of unique items on the x-axis as stacked vertical bars whose heights represent numeric values from one or more other fields</span></span> |
| <span data-ttu-id="d51b5-125">**Graphique en secteurs**</span><span class="sxs-lookup"><span data-stu-id="d51b5-125">**Pie chart**</span></span> | <span data-ttu-id="d51b5-126">Restituer les secteurs de section représentant des éléments uniques.</span><span class="sxs-lookup"><span data-stu-id="d51b5-126">Renders sectional pies representing unique items.</span></span> <span data-ttu-id="d51b5-127">La taille de chaque secteur représente les valeurs numériques d’un autre champ.</span><span class="sxs-lookup"><span data-stu-id="d51b5-127">The size of each pie represents numeric values from another field.</span></span> |
| <span data-ttu-id="d51b5-128">**Graphique de donut**</span><span class="sxs-lookup"><span data-stu-id="d51b5-128">**Donut chart**</span></span> | <span data-ttu-id="d51b5-129">Restituer les arcs sectionnels représentant des éléments uniques.</span><span class="sxs-lookup"><span data-stu-id="d51b5-129">Renders sectional arcs representing unique items.</span></span> <span data-ttu-id="d51b5-130">La longueur de chaque arc représente les valeurs numériques d’un autre champ.</span><span class="sxs-lookup"><span data-stu-id="d51b5-130">The length of each arc represents numeric values from another field.</span></span> |
| <span data-ttu-id="d51b5-131">**Graphique en lignes**</span><span class="sxs-lookup"><span data-stu-id="d51b5-131">**Line chart**</span></span> | <span data-ttu-id="d51b5-132">Trace les valeurs numériques d’une série d’éléments uniques et connecte les valeurs tracées</span><span class="sxs-lookup"><span data-stu-id="d51b5-132">Plots numeric values for a series of unique items and connects the plotted values</span></span> |
| <span data-ttu-id="d51b5-133">**Graphique en nuages de points**</span><span class="sxs-lookup"><span data-stu-id="d51b5-133">**Scatter chart**</span></span> | <span data-ttu-id="d51b5-134">Trace les valeurs numériques d’une série d’éléments uniques</span><span class="sxs-lookup"><span data-stu-id="d51b5-134">Plots numeric values for a series of unique items</span></span> |
| <span data-ttu-id="d51b5-135">**Graphique en zone**</span><span class="sxs-lookup"><span data-stu-id="d51b5-135">**Area chart**</span></span> | <span data-ttu-id="d51b5-136">Trace les valeurs numériques d’une série d’éléments uniques et remplit les sections sous les valeurs tracées</span><span class="sxs-lookup"><span data-stu-id="d51b5-136">Plots numeric values for a series of unique items and fills the sections below the plotted values</span></span> |

### <a name="construct-queries-for-effective-charts"></a><span data-ttu-id="d51b5-137">Créer des requêtes pour des graphiques efficaces</span><span class="sxs-lookup"><span data-stu-id="d51b5-137">Construct queries for effective charts</span></span>
<span data-ttu-id="d51b5-138">Lors du rendu des graphiques, le recherche avancée identifie automatiquement les colonnes d’intérêt et les valeurs numériques à agréger.</span><span class="sxs-lookup"><span data-stu-id="d51b5-138">When rendering charts, advanced hunting automatically identifies columns of interest and the numeric values to aggregate.</span></span> <span data-ttu-id="d51b5-139">Pour obtenir des graphiques significatifs, construisez vos requêtes pour renvoyer les valeurs spécifiques que vous souhaitez visualiser.</span><span class="sxs-lookup"><span data-stu-id="d51b5-139">To get meaningful charts, construct your queries to return the specific values you want to see visualized.</span></span> <span data-ttu-id="d51b5-140">Voici quelques exemples de requêtes et les graphiques qui en résultent.</span><span class="sxs-lookup"><span data-stu-id="d51b5-140">Here are some sample queries and the resulting charts.</span></span>

#### <a name="alerts-by-severity"></a><span data-ttu-id="d51b5-141">Alertes par gravité</span><span class="sxs-lookup"><span data-stu-id="d51b5-141">Alerts by severity</span></span>
<span data-ttu-id="d51b5-142">Utilisez `summarize` l’opérateur pour obtenir un nombre numérique des valeurs que vous souhaitez graphiquer.</span><span class="sxs-lookup"><span data-stu-id="d51b5-142">Use the `summarize` operator to obtain a numeric count of the values you want to chart.</span></span> <span data-ttu-id="d51b5-143">La requête ci-dessous utilise `summarize` l’opérateur pour obtenir le nombre d’alertes par gravité.</span><span class="sxs-lookup"><span data-stu-id="d51b5-143">The query below uses the `summarize` operator to get the number of alerts by severity.</span></span>

```kusto
AlertInfo
| summarize Total = count() by Severity
```
<span data-ttu-id="d51b5-144">Lors de l’affichage des résultats, un graphique en colonnes affiche chaque valeur de gravité en tant que colonne distincte :</span><span class="sxs-lookup"><span data-stu-id="d51b5-144">When rendering the results, a column chart displays each severity value as a separate column:</span></span>

<span data-ttu-id="d51b5-145">![Image des résultats de requête de recherche avancée affichés en tant que résultats d’une requête dans un graphique en colonnes pour les alertes par gravité affichée sous la direction ](../../media/advanced-hunting-column-chart.jpg)
 *d’un graphique en colonnes*</span><span class="sxs-lookup"><span data-stu-id="d51b5-145">![Image of advanced hunting query results displayed as a column chart](../../media/advanced-hunting-column-chart.jpg)
*Query results for alerts by severity displayed as a column chart*</span></span>

#### <a name="alert-severity-by-operating-system"></a><span data-ttu-id="d51b5-146">Gravité des alertes par système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="d51b5-146">Alert severity by operating system</span></span>
<span data-ttu-id="d51b5-147">Vous pouvez également utiliser l’opérateur pour préparer les résultats pour la graphique `summarize` des valeurs de plusieurs champs.</span><span class="sxs-lookup"><span data-stu-id="d51b5-147">You could also use the `summarize` operator to prepare results for charting values from multiple fields.</span></span> <span data-ttu-id="d51b5-148">Par exemple, vous souhaitez peut-être comprendre comment les gravités des alertes sont distribuées entre les systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d51b5-148">For example, you might want to understand how alert severities are distributed across operating systems (OS).</span></span> 

<span data-ttu-id="d51b5-149">La requête ci-dessous utilise un opérateur pour tirer les informations du système d’exploitation du tableau, puis pour compter les valeurs dans les colonnes `join` `DeviceInfo` et les `summarize` `OSPlatform` `Severity` colonnes :</span><span class="sxs-lookup"><span data-stu-id="d51b5-149">The query below uses a `join` operator to pull in OS information from the `DeviceInfo` table, and then uses `summarize` to count values in both the `OSPlatform` and `Severity` columns:</span></span>

```kusto
AlertInfo
| join AlertEvidence on AlertId
| join DeviceInfo on DeviceId
| summarize Count = count() by OSPlatform, Severity 
```
<span data-ttu-id="d51b5-150">Ces résultats sont mieux visualisés à l’aide d’un graphique en colonnes empilées :</span><span class="sxs-lookup"><span data-stu-id="d51b5-150">These results are best visualized using a stacked column chart:</span></span>

<span data-ttu-id="d51b5-151">![Image des résultats de requête de recherche avancée affichés sous la mesure de résultats de requête de graphique empilé pour les alertes par système d’exploitation et la gravité affichées sous la mesure ](../../media/advanced-hunting-stacked-chart.jpg)
 *d’un graphique empilé*</span><span class="sxs-lookup"><span data-stu-id="d51b5-151">![Image of advanced hunting query results displayed as a stacked chart](../../media/advanced-hunting-stacked-chart.jpg)
*Query results for alerts by OS and severity displayed as a stacked chart*</span></span>

#### <a name="phishing-emails-across-top-ten-sender-domains"></a><span data-ttu-id="d51b5-152">Courriers électroniques de hameçonnage parmi les dix principaux domaines d’expéditeurs</span><span class="sxs-lookup"><span data-stu-id="d51b5-152">Phishing emails across top ten sender domains</span></span>
<span data-ttu-id="d51b5-153">Si vous avez affaire à une liste de valeurs qui n’est pas finie, vous pouvez utiliser l’opérateur pour graphiquer uniquement les valeurs avec le plus grand nombre `Top` d’instances.</span><span class="sxs-lookup"><span data-stu-id="d51b5-153">If you're dealing with a list of values that isn’t finite, you can use the `Top` operator to chart only the values with the most instances.</span></span> <span data-ttu-id="d51b5-154">Par exemple, pour obtenir les dix principaux domaines d’expéditeurs avec le plus de messages de hameçonnage, utilisez la requête ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="d51b5-154">For example, to get the top ten sender domains with the most phishing emails, use the query below:</span></span>

```kusto
EmailEvents
| where PhishFilterVerdict == "Phish"
| summarize Count = count() by SenderFromDomain
| top 10 by Count
```
<span data-ttu-id="d51b5-155">Utilisez l’affichage graphique en secteurs pour afficher efficacement la distribution dans les principaux domaines :</span><span class="sxs-lookup"><span data-stu-id="d51b5-155">Use the pie chart view to effectively show distribution across the top domains:</span></span>

<span data-ttu-id="d51b5-156">![Image des résultats de requête de recherche avancée affichés sous la mesure d’un graphique en secteurs de graphique en secteurs montrant la distribution des e-mails de hameçonnage sur les principaux ](../../media/advanced-hunting-pie-chart.jpg)
 *domaines des expéditeurs*</span><span class="sxs-lookup"><span data-stu-id="d51b5-156">![Image of advanced hunting query results displayed as a pie chart](../../media/advanced-hunting-pie-chart.jpg)
*Pie chart showing distribution of phishing emails across top sender domains*</span></span>

#### <a name="file-activities-over-time"></a><span data-ttu-id="d51b5-157">Activités de fichier au fil du temps</span><span class="sxs-lookup"><span data-stu-id="d51b5-157">File activities over time</span></span>
<span data-ttu-id="d51b5-158">À `summarize` l’aide de l’opérateur avec la fonction, vous pouvez vérifier les événements `bin()` impliquant un indicateur particulier au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="d51b5-158">Using the `summarize` operator with the `bin()` function, you can check for events involving a particular indicator over time.</span></span> <span data-ttu-id="d51b5-159">La requête ci-dessous compte les événements impliquant le fichier à intervalles de 30 minutes pour afficher les pics d’activité `invoice.doc` liés à ce fichier :</span><span class="sxs-lookup"><span data-stu-id="d51b5-159">The query below counts events involving the file `invoice.doc` at 30 minute intervals to show spikes in activity related to that file:</span></span>

```kusto
AppFileEvents
| union DeviceFileEvents
| where FileName == "invoice.doc"
| summarize FileCount = count() by bin(Timestamp, 30m)
```
<span data-ttu-id="d51b5-160">Le graphique en lignes ci-dessous met clairement en évidence les périodes avec une activité plus importante impliquant `invoice.doc` :</span><span class="sxs-lookup"><span data-stu-id="d51b5-160">The line chart below clearly highlights time periods with more activity involving `invoice.doc`:</span></span> 

<span data-ttu-id="d51b5-161">![Image des résultats de requête de recherche avancée affichés sous la la mesure d’un graphique en lignes montrant le nombre d’événements impliquant ](../../media/advanced-hunting-line-chart.jpg)
 *un fichier au fil du temps*</span><span class="sxs-lookup"><span data-stu-id="d51b5-161">![Image of advanced hunting query results displayed as a line chart](../../media/advanced-hunting-line-chart.jpg)
*Line chart showing the number of events involving a file over time*</span></span>


## <a name="export-tables-and-charts"></a><span data-ttu-id="d51b5-162">Exporter des tableaux et des graphiques</span><span class="sxs-lookup"><span data-stu-id="d51b5-162">Export tables and charts</span></span>
<span data-ttu-id="d51b5-163">Après avoir exécute une requête, **sélectionnez Exporter** pour enregistrer les résultats dans le fichier local.</span><span class="sxs-lookup"><span data-stu-id="d51b5-163">After running a query, select **Export** to save the results to local file.</span></span> <span data-ttu-id="d51b5-164">L’affichage choisi détermine la façon dont les résultats sont exportés :</span><span class="sxs-lookup"><span data-stu-id="d51b5-164">Your chosen view determines how the results are exported:</span></span>

- <span data-ttu-id="d51b5-165">**Mode Tableau** : les résultats de la requête sont exportés sous forme tabulaire en tant que workbook Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="d51b5-165">**Table view** — the query results are exported in tabular form as a Microsoft Excel workbook</span></span>
- <span data-ttu-id="d51b5-166">**N’importe** quel graphique : les résultats de la requête sont exportés en tant qu’image JPEG du graphique rendu</span><span class="sxs-lookup"><span data-stu-id="d51b5-166">**Any chart** — the query results are exported as a JPEG image of the rendered chart</span></span>

## <a name="drill-down-from-query-results"></a><span data-ttu-id="d51b5-167">Descendre des résultats de requête</span><span class="sxs-lookup"><span data-stu-id="d51b5-167">Drill down from query results</span></span>
<span data-ttu-id="d51b5-168">Pour inspecter rapidement un enregistrement dans les résultats de votre requête, sélectionnez la ligne correspondante pour ouvrir le panneau Inspecter **l’enregistrement.**</span><span class="sxs-lookup"><span data-stu-id="d51b5-168">To quickly inspect a record in your query results, select the corresponding row to open the **Inspect record** panel.</span></span> <span data-ttu-id="d51b5-169">Le panneau fournit les informations suivantes en fonction de l’enregistrement sélectionné :</span><span class="sxs-lookup"><span data-stu-id="d51b5-169">The panel provides the following information based on the selected record:</span></span>

- <span data-ttu-id="d51b5-170">Ressources : vue récapitulée des principaux biens (boîtes aux lettres, appareils et **utilisateurs)** trouvés dans l’enregistrement, enrichis d’informations disponibles, telles que les niveaux de risque et d’exposition</span><span class="sxs-lookup"><span data-stu-id="d51b5-170">**Assets** — summarized view of the main assets (mailboxes, devices, and users) found in the record, enriched with available information, such as risk and exposure levels</span></span>
- <span data-ttu-id="d51b5-171">**Arborescence de processus** : générée pour les enregistrements avec des informations de processus et enrichie à l’aide des informations contextuelles disponibles ; en règle générale, les requêtes qui retournent plus de colonnes peuvent entraîner des arbre de processus plus riches.</span><span class="sxs-lookup"><span data-stu-id="d51b5-171">**Process tree** — generated for records with process information and enriched using available contextual information; in general, queries that return more columns can result in richer process trees.</span></span>
- <span data-ttu-id="d51b5-172">**Tous les détails** : toutes les valeurs des colonnes de l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="d51b5-172">**All details** — all the values from the columns in the record</span></span>  

![Image de l’enregistrement sélectionné avec panneau pour l’inspection de l’enregistrement](../../media/mtp-ah/inspect-record.png)

<span data-ttu-id="d51b5-174">Pour afficher plus d’informations sur une entité spécifique dans les résultats de votre requête, telles qu’un ordinateur, un fichier, un utilisateur, une adresse IP ou une URL, sélectionnez l’identificateur d’entité pour ouvrir une page de profil détaillée pour cette entité.</span><span class="sxs-lookup"><span data-stu-id="d51b5-174">To view more information about a specific entity in your query results, such as a machine, file, user, IP address, or URL, select the entity identifier to open a detailed profile page for that entity.</span></span>

## <a name="tweak-your-queries-from-the-results"></a><span data-ttu-id="d51b5-175">Adaptez vos requêtes à partir des résultats</span><span class="sxs-lookup"><span data-stu-id="d51b5-175">Tweak your queries from the results</span></span>
<span data-ttu-id="d51b5-176">Cliquez avec le bouton droit de la souris sur une valeur du jeu de résultats pour améliorer rapidement votre requête.</span><span class="sxs-lookup"><span data-stu-id="d51b5-176">Right-click a value in the result set to quickly enhance your query.</span></span> <span data-ttu-id="d51b5-177">Vous pouvez utiliser les options suivantes pour :</span><span class="sxs-lookup"><span data-stu-id="d51b5-177">You can use the options to:</span></span>

- <span data-ttu-id="d51b5-178">Rechercher explicitement la valeur sélectionnée (`==`)</span><span class="sxs-lookup"><span data-stu-id="d51b5-178">Explicitly look for the selected value (`==`)</span></span>
- <span data-ttu-id="d51b5-179">Exclure la valeur sélectionnée de la requête (`!=`)</span><span class="sxs-lookup"><span data-stu-id="d51b5-179">Exclude the selected value from the query (`!=`)</span></span>
- <span data-ttu-id="d51b5-180">Obtenez des opérateurs plus avancés pour ajouter la valeur à votre requête (par exemple, `contains`, `starts with` et `ends with`)</span><span class="sxs-lookup"><span data-stu-id="d51b5-180">Get more advanced operators for adding the value to your query, such as `contains`, `starts with` and `ends with`</span></span> 

![Image du jeu de résultats de recherche avancé](../../media/advanced-hunting-results-filter.png)

## <a name="filter-the-query-results"></a><span data-ttu-id="d51b5-182">Filtrer les résultats de la requête</span><span class="sxs-lookup"><span data-stu-id="d51b5-182">Filter the query results</span></span>
<span data-ttu-id="d51b5-183">Les filtres de droite fournissent un résumé du jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="d51b5-183">The filters displayed to the right provide a summary of the result set.</span></span> <span data-ttu-id="d51b5-184">Chaque colonne possède sa propre section qui répertorie les valeurs distinctes trouvées pour cette colonne et le nombre d’instances.</span><span class="sxs-lookup"><span data-stu-id="d51b5-184">Each column has its own section that lists the distinct values found for that column and the number of instances.</span></span>

<span data-ttu-id="d51b5-185">Affinez votre requête en sélectionnant le ou les boutons sur les valeurs que vous souhaitez inclure ou exclure, puis en sélectionnant `+` `-` Exécuter la **requête**.</span><span class="sxs-lookup"><span data-stu-id="d51b5-185">Refine your query by selecting the `+` or `-` buttons on the values that you want to include or exclude and then selecting **Run query**.</span></span>

![Image du filtre de repérage avancé](../../media/advanced-hunting-filter.png)

<span data-ttu-id="d51b5-187">Une fois le filtre appliqué pour modifier la requête, puis exécuter la requête, les résultats sont mis à jour en conséquence.</span><span class="sxs-lookup"><span data-stu-id="d51b5-187">Once you apply the filter to modify the query and then run the query, the results are updated accordingly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d51b5-188">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="d51b5-188">Related topics</span></span>
- [<span data-ttu-id="d51b5-189">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="d51b5-189">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="d51b5-190">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="d51b5-190">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="d51b5-191">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="d51b5-191">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="d51b5-192">Repérer des menaces sur les appareils, les e-mails, les applications et les identités</span><span class="sxs-lookup"><span data-stu-id="d51b5-192">Hunt across devices, emails, apps, and identities</span></span>](advanced-hunting-query-emails-devices.md)
- [<span data-ttu-id="d51b5-193">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="d51b5-193">Understand the schema</span></span>](advanced-hunting-schema-tables.md)
- [<span data-ttu-id="d51b5-194">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="d51b5-194">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
- [<span data-ttu-id="d51b5-195">Vue d’ensemble des détections personnalisées</span><span class="sxs-lookup"><span data-stu-id="d51b5-195">Custom detections overview</span></span>](custom-detections-overview.md)
