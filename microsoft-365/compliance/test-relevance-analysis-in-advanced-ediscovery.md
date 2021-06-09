---
title: Tester l’analyse de pertinence dans Advanced eDiscovery
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
titleSuffix: Office 365
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 1b092f7c-ea55-44f5-b419-63f3458fd7e0
ROBOTS: NOINDEX, NOFOLLOW
description: Découvrez comment utiliser l’onglet Test après le calcul par lots dans Advanced eDiscovery pour tester, comparer et valider la qualité globale du traitement.
ms.openlocfilehash: 3ac12c176f2e46ac0321976a7e0689fbd8893bba
ms.sourcegitcommit: 5ba0015c1554048f817fdfdc85359eee1368da64
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "49769169"
---
# <a name="test-relevance-analysis-in-advanced-ediscovery"></a><span data-ttu-id="19f46-103">Tester l’analyse de pertinence dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="19f46-103">Test Relevance analysis in Advanced eDiscovery</span></span>
  
<span data-ttu-id="19f46-104">L’onglet Test Advanced eDiscovery vous permet de tester, comparer et valider la qualité globale du traitement.</span><span class="sxs-lookup"><span data-stu-id="19f46-104">The Test tab in Advanced eDiscovery enables you to test, compare, and validate the overall quality of processing.</span></span> <span data-ttu-id="19f46-105">Ces tests sont effectués après le calcul par lots.</span><span class="sxs-lookup"><span data-stu-id="19f46-105">These tests are performed after Batch calculation.</span></span> <span data-ttu-id="19f46-106">En balant les fichiers de la collection, un expert décide de façon finale si chaque fichier balisé est pertinent pour le cas.</span><span class="sxs-lookup"><span data-stu-id="19f46-106">By tagging the files in the collection, an expert makes the final judgment about whether each tagged file is relevant to the case.</span></span>
  
<span data-ttu-id="19f46-107">Dans les scénarios à problème unique ou multiple, les tests sont généralement effectués par problème.</span><span class="sxs-lookup"><span data-stu-id="19f46-107">In single and multiple-issue scenarios, tests are typically performed per issue.</span></span> <span data-ttu-id="19f46-108">Les résultats peuvent être consultables après chaque test, et les résultats des tests peuvent être retravaillés avec des exemples de fichiers de test spécifiés.</span><span class="sxs-lookup"><span data-stu-id="19f46-108">Results can be viewed after each test, and test results can be reworked with specified sample test files.</span></span>
  
## <a name="testing-the-rest"></a><span data-ttu-id="19f46-109">Test du reste</span><span class="sxs-lookup"><span data-stu-id="19f46-109">Testing the rest</span></span>

<span data-ttu-id="19f46-110">Le test « Tester le reste » est utilisé pour valider les décisions d’élimination, par exemple, pour passer en revue uniquement les fichiers au-dessus d’un score de pertinence spécifique en fonction des résultats Advanced eDiscovery finaux.</span><span class="sxs-lookup"><span data-stu-id="19f46-110">The "Test the Rest" test is used to validate culling decisions, for example, to review only files above a specific Relevance cutoff score based on the final Advanced eDiscovery results.</span></span> <span data-ttu-id="19f46-111">L’expert examine un échantillon de fichiers sous un score de limite sélectionné pour évaluer le nombre de fichiers pertinents dans cet ensemble.</span><span class="sxs-lookup"><span data-stu-id="19f46-111">The expert reviews a sample of files under a selected cutoff score to evaluate the number of relevant files within that set.</span></span>
  
<span data-ttu-id="19f46-112">Ce test fournit des statistiques et une comparaison entre le jeu à réviser et la population Test du reste.</span><span class="sxs-lookup"><span data-stu-id="19f46-112">This test provides statistics and a comparison between the Review set and the Test the Rest population.</span></span> <span data-ttu-id="19f46-113">Les résultats du jeu à réviser sont ceux calculés par Pertinence lors de l’entraînement.</span><span class="sxs-lookup"><span data-stu-id="19f46-113">The results of the review set are those calculated by Relevance during Training.</span></span> <span data-ttu-id="19f46-114">Les résultats incluent des calculs basés sur des paramètres et des paramètres d’entrée, tels que :</span><span class="sxs-lookup"><span data-stu-id="19f46-114">The results include calculations based on settings and input parameters, such as:</span></span>
  
- <span data-ttu-id="19f46-115">Testez des exemples de statistiques sur le nombre de fichiers dans un exemple et identifiez les fichiers pertinents.</span><span class="sxs-lookup"><span data-stu-id="19f46-115">Test sample statistics of the number of files in a sample and identified relevant files.</span></span>

- <span data-ttu-id="19f46-116">Comparaison tabulaire des paramètres Population du jeu à réviser et du reste, par exemple, nombre de fichiers, nombre estimé de fichiers pertinents, richesse estimée et coût moyen de recherche d’un autre fichier pertinent.</span><span class="sxs-lookup"><span data-stu-id="19f46-116">Tabular comparison of the Population parameters of the Review set and the Rest, for example, the number of files, estimated number of relevant files, estimated richness, and the average cost of finding another relevant file.</span></span> <span data-ttu-id="19f46-117">Les paramètres de coût peuvent être définies par l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="19f46-117">Cost parameter settings can be set by the administrator.</span></span>

<span data-ttu-id="19f46-118">Pour exécuter le test « Tester le reste » :</span><span class="sxs-lookup"><span data-stu-id="19f46-118">To run the "Test the Rest" test:</span></span>

1. <span data-ttu-id="19f46-119">Ouvrez **l’onglet \> Test de** pertinence.</span><span class="sxs-lookup"><span data-stu-id="19f46-119">Open the **Relevance \> Test** tab.</span></span>

2. <span data-ttu-id="19f46-120">Dans **l’onglet Test,** cliquez **sur Nouveau test.**</span><span class="sxs-lookup"><span data-stu-id="19f46-120">In the **Test** tab, click **New test**.</span></span> <span data-ttu-id="19f46-121">La **boîte de dialogue** Créer un test s’affiche, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="19f46-121">The **Create test** dialog is displayed, as shown in the following example.</span></span>

    ![Résultats de pertinence du test Tester les éléments restants](../media/46e6898a-f929-4fd0-88d9-6f91d04b6ce2.png)
  
3. <span data-ttu-id="19f46-123">Dans **Nom du test** et **Description,** tapez le nom et la description.</span><span class="sxs-lookup"><span data-stu-id="19f46-123">In **Test name**, and **Description**, type the name and description.</span></span>

4. <span data-ttu-id="19f46-124">Dans la liste **des types de test,** **sélectionnez Tester le reste**</span><span class="sxs-lookup"><span data-stu-id="19f46-124">In the **Test type** list, select **Test the Rest**</span></span>

5. <span data-ttu-id="19f46-125">Dans la **liste Problème/Catégorie,** sélectionnez le nom du problème.</span><span class="sxs-lookup"><span data-stu-id="19f46-125">In the **Issue / Category** list, select the issue name.</span></span>

6. <span data-ttu-id="19f46-126">Dans la **liste Charger,** sélectionnez le chargement.</span><span class="sxs-lookup"><span data-stu-id="19f46-126">In the **Load** list, select the load.</span></span> 

7. <span data-ttu-id="19f46-127">Dans **% de** lecture, acceptez la valeur par défaut ou sélectionnez une valeur pour le score de pertinence cutoff.</span><span class="sxs-lookup"><span data-stu-id="19f46-127">In **Read %**, accept the default value or select a value for the cutoff Relevance score.</span></span> 

8. <span data-ttu-id="19f46-128">Dans **Définir la taille** ou accepter la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="19f46-128">In **Set size**, or accept the default value.</span></span> <span data-ttu-id="19f46-129">Les icônes de restauration restaurent les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="19f46-129">The restore icons will restore the default values.</span></span>

9. <span data-ttu-id="19f46-130">Cliquez **sur Démarrer le marquage.**</span><span class="sxs-lookup"><span data-stu-id="19f46-130">Click **Start tagging**.</span></span> <span data-ttu-id="19f46-131">Un exemple de test est généré.</span><span class="sxs-lookup"><span data-stu-id="19f46-131">A test sample is generated.</span></span>

10. <span data-ttu-id="19f46-132">Examinez et marquez chacun des fichiers dans l’onglet **Balise \>** de pertinence et, lorsque vous avez terminé, cliquez sur **Calculer**.</span><span class="sxs-lookup"><span data-stu-id="19f46-132">Review and tag each of the files in the **Relevance \> Tag** tab and when done, click **Calculate**.</span></span>

11. <span data-ttu-id="19f46-133">Dans l’onglet Test, vous pouvez cliquer sur **Afficher les résultats** pour afficher les résultats du test.</span><span class="sxs-lookup"><span data-stu-id="19f46-133">In the Test tab, you can click **View results** to see the test results.</span></span> <span data-ttu-id="19f46-134">Un exemple est illustré dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="19f46-134">An example is shown in the following screenshot.</span></span>

    ![Résultats du test Tester les éléments restants](../media/b95744a9-047d-4c29-992d-04fa7e58e58a.png)
  
<span data-ttu-id="19f46-136">Dans la capture d’écran précédente, la section Exemples de **paramètres** du tableau contient des détails sur le nombre de fichiers dans l’exemple balisé par l’expert et le nombre de fichiers pertinents trouvés dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="19f46-136">In the previous screenshot, the **Sample parameters** section of the table contains details about the number of files in the sample tagged by the expert, and the number of relevant files found in that sample.</span></span>
  
<span data-ttu-id="19f46-137">La section **Paramètres** de population du tableau contient les résultats des tests, y compris la population de fichiers du jeu à réviser avec un score inférieur au seuil sélectionné et la population de fichiers « Le reste » avec un score au-dessus du seuil sélectionné.</span><span class="sxs-lookup"><span data-stu-id="19f46-137">The **Population parameters** section of the table contains the test results, including the Review set population of files with a score below the selected cutoff and "The Rest" population of files with a score above the selected cutoff.</span></span> <span data-ttu-id="19f46-138">Pour chaque population, les résultats suivants sont affichés :</span><span class="sxs-lookup"><span data-stu-id="19f46-138">For each population, the following results are displayed:</span></span>
  
- <span data-ttu-id="19f46-139">Inclut les fichiers avec % de lecture - Cutoff indiqué</span><span class="sxs-lookup"><span data-stu-id="19f46-139">Includes files with read % - Stated cutoff</span></span>

- <span data-ttu-id="19f46-140">Nombre total de fichiers</span><span class="sxs-lookup"><span data-stu-id="19f46-140">The total number of files</span></span>

- <span data-ttu-id="19f46-141">Le nombre estimé de fichiers pertinents</span><span class="sxs-lookup"><span data-stu-id="19f46-141">The estimated number of relevant files</span></span>

- <span data-ttu-id="19f46-142">Richesse estimée</span><span class="sxs-lookup"><span data-stu-id="19f46-142">The estimated richness</span></span>

- <span data-ttu-id="19f46-143">Coût moyen d’examen de la recherche d’un autre fichier pertinent</span><span class="sxs-lookup"><span data-stu-id="19f46-143">The average review cost of finding another relevant file</span></span>

## <a name="testing-the-slice"></a><span data-ttu-id="19f46-144">Test de la tranche</span><span class="sxs-lookup"><span data-stu-id="19f46-144">Testing the slice</span></span>

<span data-ttu-id="19f46-145">Le test « Tester la tranche » effectue des tests similaires au test « Tester le reste », mais à un segment du jeu de fichiers tel que spécifié par Pertinence lecture %.</span><span class="sxs-lookup"><span data-stu-id="19f46-145">The "Test the Slice" test performs testing similar to the "Test the Rest" test, but to a segment of the file set as specified by Relevance Read %.</span></span>

<span data-ttu-id="19f46-146">Pour exécuter le test « Tester le slice » :</span><span class="sxs-lookup"><span data-stu-id="19f46-146">To run the "Test the Slice" test:</span></span>
  
1. <span data-ttu-id="19f46-147">Ouvrez **l’onglet \> Test de** pertinence.</span><span class="sxs-lookup"><span data-stu-id="19f46-147">Open the **Relevance \> Test** tab.</span></span>

2. <span data-ttu-id="19f46-148">Dans **l’onglet Test,** cliquez **sur Nouveau test.**</span><span class="sxs-lookup"><span data-stu-id="19f46-148">In the **Test** tab, click **New test**.</span></span> <span data-ttu-id="19f46-149">La **boîte de dialogue Créer** un test s’affiche.</span><span class="sxs-lookup"><span data-stu-id="19f46-149">The **Create test** dialog is displayed.</span></span>

3. <span data-ttu-id="19f46-150">Dans **Nom du test** et **Description,** tapez les informations.</span><span class="sxs-lookup"><span data-stu-id="19f46-150">In **Test name** and **Description**, type the information.</span></span>

4. <span data-ttu-id="19f46-151">Dans la **liste des types de test,** **sélectionnez Tester le slice.**</span><span class="sxs-lookup"><span data-stu-id="19f46-151">In the **Test type** list, select **Test the Slice**.</span></span>

5. <span data-ttu-id="19f46-152">Dans la **liste Problèmes,** sélectionnez le nom du problème.</span><span class="sxs-lookup"><span data-stu-id="19f46-152">In the **Issue** list, select the issue name.</span></span>

6. <span data-ttu-id="19f46-153">Dans la **liste Charger,** sélectionnez le chargement.</span><span class="sxs-lookup"><span data-stu-id="19f46-153">In the **Load** list, select the load.</span></span>

7. <span data-ttu-id="19f46-154">Dans **Lire le % entre**, acceptez les valeurs de plage basse et élevée par défaut ou sélectionnez des valeurs pour les scores de pertinence à couper.</span><span class="sxs-lookup"><span data-stu-id="19f46-154">In **Read % between**, accept the default low and high range values or select values for the cutoff Relevance scores.</span></span>

8. <span data-ttu-id="19f46-155">Dans **Définir la taille,** sélectionnez une valeur ou acceptez la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="19f46-155">In **Set size**, select a value or accept the default value.</span></span>

    <span data-ttu-id="19f46-156">Les icônes de restauration restaurent la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="19f46-156">The restore icons will restore the default value.</span></span>

9. <span data-ttu-id="19f46-157">Cliquez **sur Démarrer le marquage.**</span><span class="sxs-lookup"><span data-stu-id="19f46-157">Click **Start tagging**.</span></span> <span data-ttu-id="19f46-158">Un exemple de test est généré.</span><span class="sxs-lookup"><span data-stu-id="19f46-158">A test sample is generated.</span></span>

10. <span data-ttu-id="19f46-159">Examinez et marquez chacun des fichiers dans l’onglet **Balise \>** de pertinence et, lorsque vous avez terminé, cliquez sur **Calculer**.</span><span class="sxs-lookup"><span data-stu-id="19f46-159">Review and tag each of the files in the **Relevance \> Tag** tab and when done, click **Calculate**.</span></span>

11. <span data-ttu-id="19f46-160">Dans l’onglet Test, vous pouvez cliquer sur **Afficher les résultats** pour afficher les résultats du test.</span><span class="sxs-lookup"><span data-stu-id="19f46-160">In the Test tab, you can click **View results** to see the test results.</span></span>
