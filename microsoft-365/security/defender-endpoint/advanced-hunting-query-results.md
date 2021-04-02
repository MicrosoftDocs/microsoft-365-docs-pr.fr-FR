---
title: Travailler avec les résultats de requête de recherche avancée dans Microsoft Defender ATP
description: Exploitation des résultats de requête renvoyés par le recherche avancée dans Microsoft Defender ATP
keywords: repérage avancé, repérage de menace, repérage de cybermenace, mdatp, microsoft defender atp, recherche wdatp, requête, télémétrie, détections personnalisées, schéma, kusto, visualisation, graphique, filtres, descendre
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
ms.openlocfilehash: 4abec618a79704804b5e3349f5c4c5a4827d35ef
ms.sourcegitcommit: 582555d2b4ef5f2e2494ffdeab2c1d49e5d6b724
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51499441"
---
# <a name="work-with-advanced-hunting-query-results"></a><span data-ttu-id="5132f-104">Travailler avec des résultats de requête de recherche avancés</span><span class="sxs-lookup"><span data-stu-id="5132f-104">Work with advanced hunting query results</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="5132f-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="5132f-105">**Applies to:**</span></span>
- [<span data-ttu-id="5132f-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="5132f-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)

><span data-ttu-id="5132f-107">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="5132f-107">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="5132f-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="5132f-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-advancedhunting-abovefoldlink)

<span data-ttu-id="5132f-109">Bien que vous [](advanced-hunting-overview.md) pouvez construire vos requêtes de recherche avancées pour renvoyer des informations très précises, vous pouvez également travailler avec les résultats de la requête pour obtenir des informations plus précises et examiner des activités et des indicateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="5132f-109">While you can construct your [advanced hunting](advanced-hunting-overview.md) queries to return very precise information, you can also work with the query results to gain further insight and investigate specific activities and indicators.</span></span> <span data-ttu-id="5132f-110">Vous pouvez prendre les mesures suivantes sur les résultats de votre requête :</span><span class="sxs-lookup"><span data-stu-id="5132f-110">You can take the following actions on your query results:</span></span>

- <span data-ttu-id="5132f-111">Afficher les résultats sous la mesure d’un tableau ou d’un graphique</span><span class="sxs-lookup"><span data-stu-id="5132f-111">View results as a table or chart</span></span>
- <span data-ttu-id="5132f-112">Exporter des tableaux et des graphiques</span><span class="sxs-lookup"><span data-stu-id="5132f-112">Export tables and charts</span></span>
- <span data-ttu-id="5132f-113">Accès aux informations détaillées sur l’entité</span><span class="sxs-lookup"><span data-stu-id="5132f-113">Drill down to detailed entity information</span></span>
- <span data-ttu-id="5132f-114">Ajustez vos requêtes directement à partir des résultats ou appliquez des filtres</span><span class="sxs-lookup"><span data-stu-id="5132f-114">Tweak your queries directly from the results or apply filters</span></span>

## <a name="view-query-results-as-a-table-or-chart"></a><span data-ttu-id="5132f-115">Afficher les résultats d’une requête sous la mesure d’un tableau ou d’un graphique</span><span class="sxs-lookup"><span data-stu-id="5132f-115">View query results as a table or chart</span></span>
<span data-ttu-id="5132f-116">Par défaut, le recherche avancée affiche les résultats de la requête sous la mesure de données tabulaires.</span><span class="sxs-lookup"><span data-stu-id="5132f-116">By default, advanced hunting displays query results as tabular data.</span></span> <span data-ttu-id="5132f-117">Vous pouvez également afficher les mêmes données qu’un graphique.</span><span class="sxs-lookup"><span data-stu-id="5132f-117">You can also display the same data as a chart.</span></span> <span data-ttu-id="5132f-118">Le recherche avancée prend en charge les affichages suivants :</span><span class="sxs-lookup"><span data-stu-id="5132f-118">Advanced hunting supports the following views:</span></span>

| <span data-ttu-id="5132f-119">Type d’affichage</span><span class="sxs-lookup"><span data-stu-id="5132f-119">View type</span></span> | <span data-ttu-id="5132f-120">Description</span><span class="sxs-lookup"><span data-stu-id="5132f-120">Description</span></span> |
| -- | -- |
| <span data-ttu-id="5132f-121">**Tableau**</span><span class="sxs-lookup"><span data-stu-id="5132f-121">**Table**</span></span> | <span data-ttu-id="5132f-122">Affiche les résultats de la requête au format tabulaire</span><span class="sxs-lookup"><span data-stu-id="5132f-122">Displays the query results in tabular format</span></span> |
| <span data-ttu-id="5132f-123">**Graphique en colonnes**</span><span class="sxs-lookup"><span data-stu-id="5132f-123">**Column chart**</span></span> | <span data-ttu-id="5132f-124">Restituer une série d’éléments uniques sur l’axe des x sous forme de barres verticales dont les hauteurs représentent des valeurs numériques d’un autre champ</span><span class="sxs-lookup"><span data-stu-id="5132f-124">Renders a series of unique items on the x-axis as vertical bars whose heights represent numeric values from another field</span></span> |
| <span data-ttu-id="5132f-125">**Graphique en colonnes empilées**</span><span class="sxs-lookup"><span data-stu-id="5132f-125">**Stacked column chart**</span></span> | <span data-ttu-id="5132f-126">Restituer une série d’éléments uniques sur l’axe des X sous forme de barres verticales empilées dont les hauteurs représentent des valeurs numériques d’un ou plusieurs autres champs</span><span class="sxs-lookup"><span data-stu-id="5132f-126">Renders a series of unique items on the x-axis as stacked vertical bars whose heights represent numeric values from one or more other fields</span></span> |
| <span data-ttu-id="5132f-127">**Graphique en secteurs**</span><span class="sxs-lookup"><span data-stu-id="5132f-127">**Pie chart**</span></span> | <span data-ttu-id="5132f-128">Restituer les secteurs de section représentant des éléments uniques.</span><span class="sxs-lookup"><span data-stu-id="5132f-128">Renders sectional pies representing unique items.</span></span> <span data-ttu-id="5132f-129">La taille de chaque secteur représente les valeurs numériques d’un autre champ.</span><span class="sxs-lookup"><span data-stu-id="5132f-129">The size of each pie represents numeric values from another field.</span></span> |
| <span data-ttu-id="5132f-130">**Graphique de donut**</span><span class="sxs-lookup"><span data-stu-id="5132f-130">**Donut chart**</span></span> | <span data-ttu-id="5132f-131">Restituer les arcs sectionnels représentant des éléments uniques.</span><span class="sxs-lookup"><span data-stu-id="5132f-131">Renders sectional arcs representing unique items.</span></span> <span data-ttu-id="5132f-132">La longueur de chaque arc représente les valeurs numériques d’un autre champ.</span><span class="sxs-lookup"><span data-stu-id="5132f-132">The length of each arc represents numeric values from another field.</span></span> |
| <span data-ttu-id="5132f-133">**Graphique en lignes**</span><span class="sxs-lookup"><span data-stu-id="5132f-133">**Line chart**</span></span> | <span data-ttu-id="5132f-134">Trace les valeurs numériques d’une série d’éléments uniques et connecte les valeurs tracées</span><span class="sxs-lookup"><span data-stu-id="5132f-134">Plots numeric values for a series of unique items and connects the plotted values</span></span> |
| <span data-ttu-id="5132f-135">**Graphique en nuages de points**</span><span class="sxs-lookup"><span data-stu-id="5132f-135">**Scatter chart**</span></span> | <span data-ttu-id="5132f-136">Trace les valeurs numériques d’une série d’éléments uniques</span><span class="sxs-lookup"><span data-stu-id="5132f-136">Plots numeric values for a series of unique items</span></span> |
| <span data-ttu-id="5132f-137">**Graphique en zone**</span><span class="sxs-lookup"><span data-stu-id="5132f-137">**Area chart**</span></span> | <span data-ttu-id="5132f-138">Trace les valeurs numériques d’une série d’éléments uniques et remplit les sections sous les valeurs tracées</span><span class="sxs-lookup"><span data-stu-id="5132f-138">Plots numeric values for a series of unique items and fills the sections below the plotted values</span></span> |

### <a name="construct-queries-for-effective-charts"></a><span data-ttu-id="5132f-139">Créer des requêtes pour des graphiques efficaces</span><span class="sxs-lookup"><span data-stu-id="5132f-139">Construct queries for effective charts</span></span>
<span data-ttu-id="5132f-140">Lors du rendu des graphiques, le recherche avancée identifie automatiquement les colonnes d’intérêt et les valeurs numériques à agréger.</span><span class="sxs-lookup"><span data-stu-id="5132f-140">When rendering charts, advanced hunting automatically identifies columns of interest and the numeric values to aggregate.</span></span> <span data-ttu-id="5132f-141">Pour obtenir des graphiques significatifs, construisez vos requêtes pour renvoyer les valeurs spécifiques que vous souhaitez visualiser.</span><span class="sxs-lookup"><span data-stu-id="5132f-141">To get meaningful charts, construct your queries to return the specific values you want to see visualized.</span></span> <span data-ttu-id="5132f-142">Voici quelques exemples de requêtes et les graphiques qui en résultent.</span><span class="sxs-lookup"><span data-stu-id="5132f-142">Here are some sample queries and the resulting charts.</span></span>

#### <a name="alerts-by-severity"></a><span data-ttu-id="5132f-143">Alertes par gravité</span><span class="sxs-lookup"><span data-stu-id="5132f-143">Alerts by severity</span></span>
<span data-ttu-id="5132f-144">Utilisez `summarize` l’opérateur pour obtenir un nombre numérique des valeurs que vous souhaitez graphiquer.</span><span class="sxs-lookup"><span data-stu-id="5132f-144">Use the `summarize` operator to obtain a numeric count of the values you want to chart.</span></span> <span data-ttu-id="5132f-145">La requête ci-dessous utilise `summarize` l’opérateur pour obtenir le nombre d’alertes par gravité.</span><span class="sxs-lookup"><span data-stu-id="5132f-145">The query below uses the `summarize` operator to get the number of alerts by severity.</span></span>

```kusto
DeviceAlertEvents
| summarize Total = count() by Severity
```
<span data-ttu-id="5132f-146">Lors de l’affichage des résultats, un graphique en colonnes affiche chaque valeur de gravité en tant que colonne distincte :</span><span class="sxs-lookup"><span data-stu-id="5132f-146">When rendering the results, a column chart displays each severity value as a separate column:</span></span>

<span data-ttu-id="5132f-147">![Image des résultats de requête de recherche avancée affichés en tant que résultats d’une requête dans un graphique en colonnes pour les alertes par gravité affichée sous la direction ](images/advanced-hunting-column-chart.jpg)
 *d’un graphique en colonnes*</span><span class="sxs-lookup"><span data-stu-id="5132f-147">![Image of advanced hunting query results displayed as a column chart](images/advanced-hunting-column-chart.jpg)
*Query results for alerts by severity displayed as a column chart*</span></span>

#### <a name="alert-severity-by-operating-system"></a><span data-ttu-id="5132f-148">Gravité des alertes par système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="5132f-148">Alert severity by operating system</span></span>
<span data-ttu-id="5132f-149">Vous pouvez également utiliser `summarize` l’opérateur pour préparer les résultats pour la graphique des valeurs de plusieurs champs.</span><span class="sxs-lookup"><span data-stu-id="5132f-149">You could also use the `summarize` operator to prepare results for charting values from multiple fields.</span></span> <span data-ttu-id="5132f-150">Par exemple, vous souhaitez peut-être comprendre comment les gravités des alertes sont distribuées entre les systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="5132f-150">For example, you might want to understand how alert severities are distributed across operating systems (OS).</span></span> 

<span data-ttu-id="5132f-151">La requête ci-dessous utilise un opérateur pour tirer les informations du système d’exploitation à partir du tableau, puis pour compter les valeurs à la fois dans `join` `DeviceInfo` les `summarize` `OSPlatform` colonnes et dans les `Severity` colonnes :</span><span class="sxs-lookup"><span data-stu-id="5132f-151">The query below uses a `join` operator to pull in OS information from the `DeviceInfo` table, and then uses `summarize` to count values in both the `OSPlatform` and `Severity` columns:</span></span>

```kusto
DeviceAlertEvents
| join DeviceInfo on DeviceId
| summarize Count = count() by OSPlatform, Severity
```
<span data-ttu-id="5132f-152">Ces résultats sont mieux visualisés à l’aide d’un graphique en colonnes empilées :</span><span class="sxs-lookup"><span data-stu-id="5132f-152">These results are best visualized using a stacked column chart:</span></span>

<span data-ttu-id="5132f-153">![Image des résultats de requête de recherche avancée affichés sous la mesure d’un graphique empilé Résultats de requête pour les alertes par système d’exploitation et gravité affichées sous la mesure ](images/advanced-hunting-stacked-chart.jpg)
 *d’un graphique empilé*</span><span class="sxs-lookup"><span data-stu-id="5132f-153">![Image of advanced hunting query results displayed as a stacked chart](images/advanced-hunting-stacked-chart.jpg)
*Query results for alerts by OS and severity displayed as a stacked chart*</span></span>

#### <a name="top-ten-device-groups-with-alerts"></a><span data-ttu-id="5132f-154">Dix principaux groupes d’appareils avec alertes</span><span class="sxs-lookup"><span data-stu-id="5132f-154">Top ten device groups with alerts</span></span>
<span data-ttu-id="5132f-155">Si vous avez affaire à une liste de valeurs qui n’est pas finie, vous pouvez utiliser l’opérateur pour graphiquer uniquement les valeurs avec le plus grand nombre `Top` d’instances.</span><span class="sxs-lookup"><span data-stu-id="5132f-155">If you're dealing with a list of values that isn’t finite, you can use the `Top` operator to chart only the values with the most instances.</span></span> <span data-ttu-id="5132f-156">Par exemple, pour obtenir les dix premiers groupes d’appareils avec le plus d’alertes, utilisez la requête ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="5132f-156">For example, to get the top ten device groups with the most alerts, use the query below:</span></span>

```kusto
DeviceAlertEvents
| join DeviceInfo on DeviceId
| summarize Count = count() by MachineGroup
| top 10 by Count
```
<span data-ttu-id="5132f-157">Utilisez l’affichage graphique en secteurs pour afficher efficacement la distribution dans les groupes principaux :</span><span class="sxs-lookup"><span data-stu-id="5132f-157">Use the pie chart view to effectively show distribution across the top groups:</span></span>

<span data-ttu-id="5132f-158">![Image des résultats de requête de recherche avancée affichés sous la la figure d’un graphique en secteurs de graphique en secteurs montrant la distribution des ](images/advanced-hunting-pie-chart.jpg)
 *alertes entre les groupes d’appareils*</span><span class="sxs-lookup"><span data-stu-id="5132f-158">![Image of advanced hunting query results displayed as a pie chart](images/advanced-hunting-pie-chart.jpg)
*Pie chart showing distribution of alerts across device groups*</span></span>

#### <a name="malware-detections-over-time"></a><span data-ttu-id="5132f-159">Détections de programmes malveillants au fil du temps</span><span class="sxs-lookup"><span data-stu-id="5132f-159">Malware detections over time</span></span>
<span data-ttu-id="5132f-160">À `summarize` l’aide de l’opérateur avec la fonction, vous pouvez vérifier les événements `bin()` impliquant un indicateur particulier au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="5132f-160">Using the `summarize` operator with the `bin()` function, you can check for events involving a particular indicator over time.</span></span> <span data-ttu-id="5132f-161">La requête ci-dessous compte les détections d’un fichier de test EICAR à intervalles de 30 minutes pour afficher les pics de détection de ce fichier :</span><span class="sxs-lookup"><span data-stu-id="5132f-161">The query below counts detections of an EICAR test file at 30 minute intervals to show spikes in detections of that file:</span></span>

```kusto
DeviceEvents
| where ActionType == "AntivirusDetection"
| where SHA1 == "3395856ce81f2b7382dee72602f798b642f14140"
| summarize Detections = count() by bin(Timestamp, 30m)
```
<span data-ttu-id="5132f-162">Le graphique en lignes ci-dessous met clairement en évidence les périodes avec davantage de détections de programmes malveillants de test :</span><span class="sxs-lookup"><span data-stu-id="5132f-162">The line chart below clearly highlights time periods with more detections of the test malware:</span></span> 

<span data-ttu-id="5132f-163">![Image des résultats de requête de repérage avancé affichés sous la mesure d’un graphique en lignes affichant le nombre de détections d’un programme malveillant ](images/advanced-hunting-line-chart.jpg)
 *de test au fil du temps*</span><span class="sxs-lookup"><span data-stu-id="5132f-163">![Image of advanced hunting query results displayed as a line chart](images/advanced-hunting-line-chart.jpg)
*Line chart showing the number of detections of a test malware over time*</span></span>


## <a name="export-tables-and-charts"></a><span data-ttu-id="5132f-164">Exporter des tableaux et des graphiques</span><span class="sxs-lookup"><span data-stu-id="5132f-164">Export tables and charts</span></span>
<span data-ttu-id="5132f-165">Après avoir exécute une requête, **sélectionnez Exporter** pour enregistrer les résultats dans le fichier local.</span><span class="sxs-lookup"><span data-stu-id="5132f-165">After running a query, select **Export** to save the results to local file.</span></span> <span data-ttu-id="5132f-166">L’affichage choisi détermine la façon dont les résultats sont exportés :</span><span class="sxs-lookup"><span data-stu-id="5132f-166">Your chosen view determines how the results are exported:</span></span>

- <span data-ttu-id="5132f-167">**Mode Tableau** : les résultats de la requête sont exportés sous forme tabulaire en tant que workbook Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="5132f-167">**Table view** — the query results are exported in tabular form as a Microsoft Excel workbook</span></span>
- <span data-ttu-id="5132f-168">**N’importe** quel graphique : les résultats de la requête sont exportés en tant qu’image JPEG du graphique rendu</span><span class="sxs-lookup"><span data-stu-id="5132f-168">**Any chart** — the query results are exported as a JPEG image of the rendered chart</span></span>

## <a name="drill-down-from-query-results"></a><span data-ttu-id="5132f-169">Descendre des résultats de requête</span><span class="sxs-lookup"><span data-stu-id="5132f-169">Drill down from query results</span></span>
<span data-ttu-id="5132f-170">Pour afficher plus d’informations sur les entités, telles que les appareils, les fichiers, les utilisateurs, les adresses IP et les URL, dans les résultats de votre requête, cliquez simplement sur l’identificateur d’entité.</span><span class="sxs-lookup"><span data-stu-id="5132f-170">To view more information about entities, such as devices, files, users, IP addresses, and URLs, in your query results, simply click the entity identifier.</span></span> <span data-ttu-id="5132f-171">Cela ouvre une page de profil détaillée pour l’entité sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="5132f-171">This opens a detailed profile page for the selected entity.</span></span>

<span data-ttu-id="5132f-172">Pour inspecter rapidement un enregistrement dans les résultats de votre requête, sélectionnez la ligne correspondante pour ouvrir le panneau Inspecter l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="5132f-172">To quickly inspect a record in your query results, select the corresponding row to open the Inspect record panel.</span></span> <span data-ttu-id="5132f-173">Le panneau fournit les informations suivantes en fonction de l’enregistrement sélectionné :</span><span class="sxs-lookup"><span data-stu-id="5132f-173">The panel provides the following information based on the selected record:</span></span>

- <span data-ttu-id="5132f-174">Ressources : vue récapitulée des principaux biens (boîtes aux lettres, appareils et **utilisateurs)** trouvés dans l’enregistrement, enrichis d’informations disponibles, telles que les niveaux de risque et d’exposition</span><span class="sxs-lookup"><span data-stu-id="5132f-174">**Assets** — A summarized view of the main assets (mailboxes, devices, and users) found in the record, enriched with available information, such as risk and exposure levels</span></span>
- <span data-ttu-id="5132f-175">**Arborescence de processus** : graphique généré pour les enregistrements avec des informations de processus et enrichi à l’aide d’informations contextuelles disponibles ; en règle générale, les requêtes qui retournent plus de colonnes peuvent entraîner des arbre de processus plus riches.</span><span class="sxs-lookup"><span data-stu-id="5132f-175">**Process tree** — A chart generated for records with process information and enriched using available contextual information; in general, queries that return more columns can result in richer process trees.</span></span>
- <span data-ttu-id="5132f-176">**Tous les détails** : répertorie toutes les valeurs des colonnes de l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="5132f-176">**All details** — Lists all the values from the columns in the record</span></span>

## <a name="tweak-your-queries-from-the-results"></a><span data-ttu-id="5132f-177">Adaptez vos requêtes à partir des résultats</span><span class="sxs-lookup"><span data-stu-id="5132f-177">Tweak your queries from the results</span></span>
<span data-ttu-id="5132f-178">Cliquez avec le bouton droit de la souris sur une valeur du jeu de résultats pour améliorer rapidement votre requête.</span><span class="sxs-lookup"><span data-stu-id="5132f-178">Right-click a value in the result set to quickly enhance your query.</span></span> <span data-ttu-id="5132f-179">Vous pouvez utiliser les options suivantes pour :</span><span class="sxs-lookup"><span data-stu-id="5132f-179">You can use the options to:</span></span>

- <span data-ttu-id="5132f-180">Rechercher explicitement la valeur sélectionnée (`==`)</span><span class="sxs-lookup"><span data-stu-id="5132f-180">Explicitly look for the selected value (`==`)</span></span>
- <span data-ttu-id="5132f-181">Exclure la valeur sélectionnée de la requête (`!=`)</span><span class="sxs-lookup"><span data-stu-id="5132f-181">Exclude the selected value from the query (`!=`)</span></span>
- <span data-ttu-id="5132f-182">Obtenez des opérateurs plus avancés pour ajouter la valeur à votre requête (par exemple, `contains`, `starts with` et `ends with`)</span><span class="sxs-lookup"><span data-stu-id="5132f-182">Get more advanced operators for adding the value to your query, such as `contains`, `starts with` and `ends with`</span></span> 

![Image du jeu de résultats de recherche avancée](images/advanced-hunting-results-filter.png)

## <a name="filter-the-query-results"></a><span data-ttu-id="5132f-184">Filtrer les résultats de la requête</span><span class="sxs-lookup"><span data-stu-id="5132f-184">Filter the query results</span></span>
<span data-ttu-id="5132f-185">Les filtres affichés dans le volet droit fournissent un résumé du jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="5132f-185">The filters displayed in the right pane provide a summary of the result set.</span></span> <span data-ttu-id="5132f-186">Chaque colonne possède sa propre section dans le volet, chacune répertoriant les valeurs trouvées dans cette colonne et le nombre d’instances.</span><span class="sxs-lookup"><span data-stu-id="5132f-186">Every column has its own section in the pane, each of which lists the values found in that column, and the number of instances.</span></span>

<span data-ttu-id="5132f-187">Affinez votre requête en sélectionnant le ou les boutons sur les valeurs que vous `+` `-` souhaitez inclure ou exclure.</span><span class="sxs-lookup"><span data-stu-id="5132f-187">Refine your query by selecting the `+` or `-` buttons on the values that you want to include or exclude.</span></span> <span data-ttu-id="5132f-188">Ensuite, **sélectionnez Exécuter la requête.**</span><span class="sxs-lookup"><span data-stu-id="5132f-188">Then select **Run query**.</span></span>

![Image du filtre de repérage avancé](images/advanced-hunting-filter.png)

<span data-ttu-id="5132f-190">Une fois le filtre appliqué pour modifier la requête, puis exécuter la requête, les résultats sont mis à jour en conséquence.</span><span class="sxs-lookup"><span data-stu-id="5132f-190">Once you apply the filter to modify the query and then run the query, the results are updated accordingly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5132f-191">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="5132f-191">Related topics</span></span>
- [<span data-ttu-id="5132f-192">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="5132f-192">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="5132f-193">Apprendre le langage de requête</span><span class="sxs-lookup"><span data-stu-id="5132f-193">Learn the query language</span></span>](advanced-hunting-query-language.md)
- [<span data-ttu-id="5132f-194">Utiliser des requêtes partagées</span><span class="sxs-lookup"><span data-stu-id="5132f-194">Use shared queries</span></span>](advanced-hunting-shared-queries.md)
- [<span data-ttu-id="5132f-195">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="5132f-195">Understand the schema</span></span>](advanced-hunting-schema-reference.md)
- [<span data-ttu-id="5132f-196">Appliquer les meilleures pratiques de requête</span><span class="sxs-lookup"><span data-stu-id="5132f-196">Apply query best practices</span></span>](advanced-hunting-best-practices.md)
- [<span data-ttu-id="5132f-197">Vue d’ensemble des détections personnalisées</span><span class="sxs-lookup"><span data-stu-id="5132f-197">Custom detections overview</span></span>](overview-custom-detections.md)
