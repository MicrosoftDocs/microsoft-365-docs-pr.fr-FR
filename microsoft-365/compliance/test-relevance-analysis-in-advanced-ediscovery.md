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
description: Découvrez comment utiliser l’onglet test après le calcul par lot dans Advanced eDiscovery pour tester, comparer et valider la qualité globale du traitement.
ms.openlocfilehash: 3ac12c176f2e46ac0321976a7e0689fbd8893bba
ms.sourcegitcommit: 5ba0015c1554048f817fdfdc85359eee1368da64
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "49769169"
---
# <a name="test-relevance-analysis-in-advanced-ediscovery"></a><span data-ttu-id="bfa1c-103">Tester l’analyse de pertinence dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="bfa1c-103">Test Relevance analysis in Advanced eDiscovery</span></span>
  
<span data-ttu-id="bfa1c-104">L’onglet test dans Advanced eDiscovery vous permet de tester, de comparer et de valider la qualité globale du traitement.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-104">The Test tab in Advanced eDiscovery enables you to test, compare, and validate the overall quality of processing.</span></span> <span data-ttu-id="bfa1c-105">Ces tests sont effectués après le calcul par lots.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-105">These tests are performed after Batch calculation.</span></span> <span data-ttu-id="bfa1c-106">En marquant les fichiers dans la collection, un expert détermine si chaque fichier balisé est pertinent pour le cas.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-106">By tagging the files in the collection, an expert makes the final judgment about whether each tagged file is relevant to the case.</span></span>
  
<span data-ttu-id="bfa1c-107">Dans les scénarios à un ou plusieurs problèmes, les tests sont généralement effectués par problème.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-107">In single and multiple-issue scenarios, tests are typically performed per issue.</span></span> <span data-ttu-id="bfa1c-108">Les résultats peuvent être affichés après chaque test, et les résultats des tests peuvent être retravaillés avec les exemples de fichiers de test spécifiés.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-108">Results can be viewed after each test, and test results can be reworked with specified sample test files.</span></span>
  
## <a name="testing-the-rest"></a><span data-ttu-id="bfa1c-109">Test du reste</span><span class="sxs-lookup"><span data-stu-id="bfa1c-109">Testing the rest</span></span>

<span data-ttu-id="bfa1c-110">Le test « tester le reste » permet de valider les décisions de Culling, par exemple, pour examiner uniquement les fichiers situés au-dessus d’un score de pertinence spécifique basé sur les résultats avancés avancés de découverte électronique.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-110">The "Test the Rest" test is used to validate culling decisions, for example, to review only files above a specific Relevance cutoff score based on the final Advanced eDiscovery results.</span></span> <span data-ttu-id="bfa1c-111">L’expert examine un échantillon de fichiers sous un score de démarcation sélectionné pour évaluer le nombre de fichiers appropriés dans cet ensemble.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-111">The expert reviews a sample of files under a selected cutoff score to evaluate the number of relevant files within that set.</span></span>
  
<span data-ttu-id="bfa1c-112">Ce test fournit des statistiques et une comparaison entre l’ensemble de révision et le test la population Rest.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-112">This test provides statistics and a comparison between the Review set and the Test the Rest population.</span></span> <span data-ttu-id="bfa1c-113">Les résultats du jeu de révision sont ceux calculés par pertinence lors de la formation.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-113">The results of the review set are those calculated by Relevance during Training.</span></span> <span data-ttu-id="bfa1c-114">Les résultats incluent des calculs basés sur les paramètres et les paramètres d’entrée, tels que :</span><span class="sxs-lookup"><span data-stu-id="bfa1c-114">The results include calculations based on settings and input parameters, such as:</span></span>
  
- <span data-ttu-id="bfa1c-115">Tester des statistiques sur le nombre de fichiers dans un exemple et identifier les fichiers appropriés.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-115">Test sample statistics of the number of files in a sample and identified relevant files.</span></span>

- <span data-ttu-id="bfa1c-116">Comparaison tabulaire des paramètres de population du jeu de révision et des autres, par exemple, le nombre de fichiers, le nombre estimé de fichiers pertinents, la richesse estimée et le coût moyen de la recherche d’un autre fichier pertinent.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-116">Tabular comparison of the Population parameters of the Review set and the Rest, for example, the number of files, estimated number of relevant files, estimated richness, and the average cost of finding another relevant file.</span></span> <span data-ttu-id="bfa1c-117">Les paramètres de coût des paramètres peuvent être définis par l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-117">Cost parameter settings can be set by the administrator.</span></span>

<span data-ttu-id="bfa1c-118">Pour exécuter le test « tester le reste » :</span><span class="sxs-lookup"><span data-stu-id="bfa1c-118">To run the "Test the Rest" test:</span></span>

1. <span data-ttu-id="bfa1c-119">Ouvrez l' **onglet \> test de pertinence** .</span><span class="sxs-lookup"><span data-stu-id="bfa1c-119">Open the **Relevance \> Test** tab.</span></span>

2. <span data-ttu-id="bfa1c-120">Dans l’onglet **test** , cliquez sur **nouveau test**.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-120">In the **Test** tab, click **New test**.</span></span> <span data-ttu-id="bfa1c-121">La boîte de dialogue **créer un test** s’affiche, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-121">The **Create test** dialog is displayed, as shown in the following example.</span></span>

    ![Résultats de pertinence du test Tester les éléments restants](../media/46e6898a-f929-4fd0-88d9-6f91d04b6ce2.png)
  
3. <span data-ttu-id="bfa1c-123">Dans **nom du test** et **Description**, tapez le nom et la description.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-123">In **Test name**, and **Description**, type the name and description.</span></span>

4. <span data-ttu-id="bfa1c-124">Dans la liste **type de test** , sélectionnez **tester le reste**</span><span class="sxs-lookup"><span data-stu-id="bfa1c-124">In the **Test type** list, select **Test the Rest**</span></span>

5. <span data-ttu-id="bfa1c-125">Dans la liste **problème/catégorie** , sélectionnez le nom du problème.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-125">In the **Issue / Category** list, select the issue name.</span></span>

6. <span data-ttu-id="bfa1c-126">Dans la liste **charge** , sélectionnez la charge.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-126">In the **Load** list, select the load.</span></span> 

7. <span data-ttu-id="bfa1c-127">En **lecture%**, acceptez la valeur par défaut ou sélectionnez une valeur pour le score de pertinence de la limite.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-127">In **Read %**, accept the default value or select a value for the cutoff Relevance score.</span></span> 

8. <span data-ttu-id="bfa1c-128">Dans **définir la taille**, ou acceptez la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-128">In **Set size**, or accept the default value.</span></span> <span data-ttu-id="bfa1c-129">Les icônes de restauration restaureront les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-129">The restore icons will restore the default values.</span></span>

9. <span data-ttu-id="bfa1c-130">Cliquez sur **Démarrer le balisage**.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-130">Click **Start tagging**.</span></span> <span data-ttu-id="bfa1c-131">Un échantillon de test est généré.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-131">A test sample is generated.</span></span>

10. <span data-ttu-id="bfa1c-132">Examinez et marquez chacun des fichiers dans l’onglet de la **\> balise de pertinence** et, lorsque vous avez fini, cliquez sur **calculer**.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-132">Review and tag each of the files in the **Relevance \> Tag** tab and when done, click **Calculate**.</span></span>

11. <span data-ttu-id="bfa1c-133">Sous l’onglet test, vous pouvez cliquer sur **afficher les résultats** pour afficher les résultats des tests.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-133">In the Test tab, you can click **View results** to see the test results.</span></span> <span data-ttu-id="bfa1c-134">Un exemple est illustré dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-134">An example is shown in the following screenshot.</span></span>

    ![Résultats du test Tester les éléments restants](../media/b95744a9-047d-4c29-992d-04fa7e58e58a.png)
  
<span data-ttu-id="bfa1c-136">Dans la capture d’écran précédente, la section relative aux paramètres de l' **exemple** de tableau contient des détails sur le nombre de fichiers dans l’exemple, ainsi que le nombre de fichiers pertinents trouvés dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-136">In the previous screenshot, the **Sample parameters** section of the table contains details about the number of files in the sample tagged by the expert, and the number of relevant files found in that sample.</span></span>
  
<span data-ttu-id="bfa1c-137">La section **paramètres de remplissage** du tableau contient les résultats des tests, y compris le remplissage de l’ensemble des fichiers dont le score est inférieur à la limite sélectionnée et la population de fichiers Rest dont le score est supérieur à la limite sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-137">The **Population parameters** section of the table contains the test results, including the Review set population of files with a score below the selected cutoff and "The Rest" population of files with a score above the selected cutoff.</span></span> <span data-ttu-id="bfa1c-138">Pour chaque population, les résultats suivants s’affichent :</span><span class="sxs-lookup"><span data-stu-id="bfa1c-138">For each population, the following results are displayed:</span></span>
  
- <span data-ttu-id="bfa1c-139">Inclut des fichiers dont la limite de lecture est% indiquée</span><span class="sxs-lookup"><span data-stu-id="bfa1c-139">Includes files with read % - Stated cutoff</span></span>

- <span data-ttu-id="bfa1c-140">Nombre total de fichiers</span><span class="sxs-lookup"><span data-stu-id="bfa1c-140">The total number of files</span></span>

- <span data-ttu-id="bfa1c-141">Estimation du nombre de fichiers pertinents</span><span class="sxs-lookup"><span data-stu-id="bfa1c-141">The estimated number of relevant files</span></span>

- <span data-ttu-id="bfa1c-142">La richesse estimée</span><span class="sxs-lookup"><span data-stu-id="bfa1c-142">The estimated richness</span></span>

- <span data-ttu-id="bfa1c-143">Coût moyen de la recherche d’un autre fichier pertinent</span><span class="sxs-lookup"><span data-stu-id="bfa1c-143">The average review cost of finding another relevant file</span></span>

## <a name="testing-the-slice"></a><span data-ttu-id="bfa1c-144">Test du secteur</span><span class="sxs-lookup"><span data-stu-id="bfa1c-144">Testing the slice</span></span>

<span data-ttu-id="bfa1c-145">Le test « test the Slice » effectue un test semblable au test « test the Rest », mais à un segment de l’ensemble de fichiers, tel que spécifié par la pertinence% de lecture.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-145">The "Test the Slice" test performs testing similar to the "Test the Rest" test, but to a segment of the file set as specified by Relevance Read %.</span></span>

<span data-ttu-id="bfa1c-146">Pour exécuter le test « tester le secteur » :</span><span class="sxs-lookup"><span data-stu-id="bfa1c-146">To run the "Test the Slice" test:</span></span>
  
1. <span data-ttu-id="bfa1c-147">Ouvrez l' **onglet \> test de pertinence** .</span><span class="sxs-lookup"><span data-stu-id="bfa1c-147">Open the **Relevance \> Test** tab.</span></span>

2. <span data-ttu-id="bfa1c-148">Dans l’onglet **test** , cliquez sur **nouveau test**.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-148">In the **Test** tab, click **New test**.</span></span> <span data-ttu-id="bfa1c-149">La boîte de dialogue **créer un test** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-149">The **Create test** dialog is displayed.</span></span>

3. <span data-ttu-id="bfa1c-150">Dans **nom** et **Description** du test, entrez les informations.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-150">In **Test name** and **Description**, type the information.</span></span>

4. <span data-ttu-id="bfa1c-151">Dans la liste **type de test** , sélectionnez **tester la section**.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-151">In the **Test type** list, select **Test the Slice**.</span></span>

5. <span data-ttu-id="bfa1c-152">Dans la liste **problème** , sélectionnez le nom du problème.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-152">In the **Issue** list, select the issue name.</span></span>

6. <span data-ttu-id="bfa1c-153">Dans la liste **charge** , sélectionnez la charge.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-153">In the **Load** list, select the load.</span></span>

7. <span data-ttu-id="bfa1c-154">En **lecture% entre**, acceptez les valeurs par défaut de plage basse et haute ou sélectionnez des valeurs pour les scores de pertinence de la limite.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-154">In **Read % between**, accept the default low and high range values or select values for the cutoff Relevance scores.</span></span>

8. <span data-ttu-id="bfa1c-155">Dans **définir la taille**, sélectionnez une valeur ou acceptez la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-155">In **Set size**, select a value or accept the default value.</span></span>

    <span data-ttu-id="bfa1c-156">Les icônes de restauration restaureront la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-156">The restore icons will restore the default value.</span></span>

9. <span data-ttu-id="bfa1c-157">Cliquez sur **Démarrer le balisage**.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-157">Click **Start tagging**.</span></span> <span data-ttu-id="bfa1c-158">Un échantillon de test est généré.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-158">A test sample is generated.</span></span>

10. <span data-ttu-id="bfa1c-159">Examinez et marquez chacun des fichiers dans l’onglet de la **\> balise de pertinence** et, lorsque vous avez fini, cliquez sur **calculer**.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-159">Review and tag each of the files in the **Relevance \> Tag** tab and when done, click **Calculate**.</span></span>

11. <span data-ttu-id="bfa1c-160">Sous l’onglet test, vous pouvez cliquer sur **afficher les résultats** pour afficher les résultats des tests.</span><span class="sxs-lookup"><span data-stu-id="bfa1c-160">In the Test tab, you can click **View results** to see the test results.</span></span>
