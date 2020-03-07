---
title: Préparation des données pour Office 365 Advanced eDiscovery
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
titleSuffix: Office 365
ms.date: 9/14/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 2fb94c23-1846-4a0e-994d-da6d02445f15
description: 'Découvrez comment utiliser le centre de sécurité &amp; conformité Microsoft 365 pour préparer les données Office 365 pour analyse avec Office 365 Advanced eDiscovery. '
ms.openlocfilehash: 44ccb6250e28e0fa75f6d1a037236a100fca102c
ms.sourcegitcommit: e741930c41abcde61add22d4b773dbf171ed72ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/07/2020
ms.locfileid: "42557864"
---
# <a name="prepare-data-for-advanced-ediscovery-classic"></a><span data-ttu-id="b1a4d-103">Préparation des données pour Advanced eDiscovery (classique)</span><span class="sxs-lookup"><span data-stu-id="b1a4d-103">Prepare data for Advanced eDiscovery (classic)</span></span>

<span data-ttu-id="b1a4d-104">Cette rubrique décrit comment charger les résultats d’une recherche de contenu dans dans un cas dans Advanced eDiscovery (classique).</span><span class="sxs-lookup"><span data-stu-id="b1a4d-104">This topic describes how to load the results of a Content Search in to a case in Advanced eDiscovery (classic).</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="b1a4d-105">À mesure que nous continuons à investir dans les versions plus récentes de la découverte électronique avancée, nous annonçaons le retrait d’Office 365 Advanced eDiscovery, également appelé *Advanced eDiscovery (Classic)* ou *Advanced eDiscovery v 1.0*.</span><span class="sxs-lookup"><span data-stu-id="b1a4d-105">As we continue to invest in newer versions of Advanced eDiscovery, we are announcing the retirement of Office 365 Advanced eDiscovery, also known as *Advanced eDiscovery (classic)* or *Advanced eDiscovery v1.0*.</span></span> <span data-ttu-id="b1a4d-106">Si vous utilisez Advanced eDiscovery v 1.0, veuillez faire la transition vers [Advanced eDiscovery v2.0](overview-ediscovery-20.md) (également connu sous le nom de *solution eDiscovery avancée dans Microsoft 365*) dès que possible.</span><span class="sxs-lookup"><span data-stu-id="b1a4d-106">If you're still using Advanced eDiscovery v1.0, please transition to [Advanced eDiscovery v2.0](overview-ediscovery-20.md) (also known as the *Advanced eDiscovery solution in Microsoft 365*) as soon as possible.</span></span> <span data-ttu-id="b1a4d-107">Advanced eDiscovery 2.0 contient des fonctionnalités similaires à celles de Advanced eDiscovery v1.0, et elle offre également de nombreuses fonctions inédites telles que la gestion des consignataires, la gestion des communications et les jeux à réviser.</span><span class="sxs-lookup"><span data-stu-id="b1a4d-107">Advanced eDiscovery 2.0 contains similar functionality found in Advanced eDiscovery v1.0, but also offers many new features such as custodian management, communications management, and review sets.</span></span> <span data-ttu-id="b1a4d-108">Pour en savoir plus sur le retrait d’Advanced eDiscovery v1.0, voir la [Suppression des outils hérités eDiscovery](legacy-ediscovery-retirement.md#advanced-ediscovery-v10).</span><span class="sxs-lookup"><span data-stu-id="b1a4d-108">To learn more about the retirement of Advanced eDiscovery v1.0, see [Retirement of legacy eDiscovery tools](legacy-ediscovery-retirement.md#advanced-ediscovery-v10).</span></span>  
  
## <a name="step-1-prepare-office-365-data-for-advanced-ediscovery"></a><span data-ttu-id="b1a4d-109">Étape 1 : préparer les données Office 365 pour Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="b1a4d-109">Step 1: Prepare Office 365 data for Advanced eDiscovery</span></span>

<span data-ttu-id="b1a4d-110">Pour analyser les données avec Advanced eDiscovery, vous pouvez utiliser les résultats d’une recherche de contenu que vous exécutez dans le centre &amp; de sécurité conformité Microsoft 365 (qui se trouve sur la page **recherche** de &amp; contenu dans le centre de sécurité conformité de Microsoft 365) ou dans une recherche associée à un cas de &amp; découverte électronique (dans la page **eDiscovery** du centre de sécurité conformité).</span><span class="sxs-lookup"><span data-stu-id="b1a4d-110">To analyze data with Advanced eDiscovery, you can use the results of a Content Search that you run in the Microsoft 365 Security &amp; Compliance Center (listed on the **Content search** page in the Microsoft 365 Security &amp; Compliance Center) or a search associated with an eDiscovery case (listed on the **eDiscovery** page in the Security &amp; Compliance Center).</span></span> 
  
<span data-ttu-id="b1a4d-111">Pour obtenir la procédure détaillée sur la préparation des résultats de recherche pour analyse dans Advanced eDiscovery, voir [Prepare Search Results for Office 365 Advanced eDiscovery](prepare-search-results-for-advanced-ediscovery.md).</span><span class="sxs-lookup"><span data-stu-id="b1a4d-111">For the detailed steps on preparing search results for analysis in Advanced eDiscovery, see [Prepare search results for Office 365 Advanced eDiscovery](prepare-search-results-for-advanced-ediscovery.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="b1a4d-112">Si vous disposez de données en dehors d’Office 365 et que vous souhaitez les importer dans Office 365 de manière à pouvoir les préparer et les analyser dans Advanced eDiscovery, voir [Overview of Import PST Files to office 365](https://support.office.com/article/ba688e0a-0fcb-4bd7-8e57-2b669564ea84) et [Archiving tiers data in Office 365](https://go.microsoft.com/fwlink/p/?linkid=716918).</span><span class="sxs-lookup"><span data-stu-id="b1a4d-112">If you have data outside of Office 365 and want to import it to Office 365 so that you can prepare and analyze it in Advanced eDiscovery, a see [Overview of importing PST files to Office 365](https://support.office.com/article/ba688e0a-0fcb-4bd7-8e57-2b669564ea84) and [Archiving third-party data in Office 365](https://go.microsoft.com/fwlink/p/?linkid=716918).</span></span> 
  
## <a name="step-2-load-search-result-data-in-to-a-case-in-advanced-ediscovery"></a><span data-ttu-id="b1a4d-113">Étape 2 : chargement des données de résultats de recherche dans dans un cas dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="b1a4d-113">Step 2: Load search result data in to a case in Advanced eDiscovery</span></span>

<span data-ttu-id="b1a4d-114">Une fois que vous avez préparé les résultats de &amp; la recherche dans le centre de sécurité conformité pour analyse, l’étape suivante consiste à charger les résultats de la recherche dans un cas dans Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="b1a4d-114">After you prepare the search results in the Security &amp; Compliance Center for analysis, the next step is to load the search results in to a case in Advanced eDiscovery.</span></span> <span data-ttu-id="b1a4d-115">Pour plus d’informations, consultez [la rubrique exécuter le module de processus](run-the-process-module-in-advanced-ediscovery.md).</span><span class="sxs-lookup"><span data-stu-id="b1a4d-115">For more detailed information, see [Run the Process module](run-the-process-module-in-advanced-ediscovery.md).</span></span>
  
1. <span data-ttu-id="b1a4d-116">Accédez à [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="b1a4d-116">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="b1a4d-117">Ouvrez une session Office 365 en utilisant votre compte scolaire ou professionnel.</span><span class="sxs-lookup"><span data-stu-id="b1a4d-117">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="b1a4d-118">Dans le Centre de sécurité &amp; conformité, cliquez sur **Recherches &amp; enquêtes** \> **eDiscovery** pour afficher la liste des cas de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b1a4d-118">In the Security &amp; Compliance Center, click **Search &amp; investigation** \> **eDiscovery** to display the list of cases in your organization.</span></span> 
    
4. <span data-ttu-id="b1a4d-119">Cliquez sur **ouvrir** en regard du cas dans lequel vous souhaitez charger les données dans Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="b1a4d-119">Click **Open** next to the case that you want to load data in to in Advanced eDiscovery.</span></span> 
    
5. <span data-ttu-id="b1a4d-120">Sur la page **Accueil** du cas, cliquez sur **Advanced eDiscovery**.</span><span class="sxs-lookup"><span data-stu-id="b1a4d-120">On the **Home** page for the case, click **Advanced eDiscovery**.</span></span> 
    
    ![Cliquez sur basculer vers Advanced eDiscovery pour ouvrir le cas dans Advanced eDiscovery](../media/8e34ba23-62e3-4e68-a530-b6ece39b54be.png)
  
    <span data-ttu-id="b1a4d-122">La barre **de progression de la connexion à Advanced eDiscovery** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="b1a4d-122">The **Connecting to Advanced eDiscovery** progress bar is displayed.</span></span> <span data-ttu-id="b1a4d-123">Lorsque vous êtes connecté à Advanced eDiscovery, une liste de conteneurs apparaît dans la page de configuration de l’incident.</span><span class="sxs-lookup"><span data-stu-id="b1a4d-123">When you're connected to Advanced eDiscovery, a list of containers is displayed on the setup page for the case.</span></span> 
    
    ![Le cas est affiché dans Advanced eDiscovery](../media/8036e152-70dc-4bb7-9379-61c1ed8326b4.png)
  
     <span data-ttu-id="b1a4d-125">Ces conteneurs représentent les résultats de recherche que vous avez préparés pour l’analyse dans Advanced eDiscovery à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="b1a4d-125">These containers represent the search results that you prepared for analysis in Advanced eDiscovery in Step 1.</span></span> <span data-ttu-id="b1a4d-126">Notez que le nom du conteneur porte le même nom que la recherche de contenu dans le centre de sécurité &amp; conformité.</span><span class="sxs-lookup"><span data-stu-id="b1a4d-126">Note that the name of the container has the same name as the Content Search in the case in the Security &amp; Compliance Center.</span></span> <span data-ttu-id="b1a4d-127">Les conteneurs de la liste sont ceux que vous avez préparés.</span><span class="sxs-lookup"><span data-stu-id="b1a4d-127">The containers in the list are the ones that you prepared.</span></span> <span data-ttu-id="b1a4d-128">Si un autre utilisateur a préparé des résultats de recherche pour Advanced eDiscovery, les conteneurs correspondants ne seront pas inclus dans la liste.</span><span class="sxs-lookup"><span data-stu-id="b1a4d-128">If a different user prepared search results for Advanced eDiscovery, the corresponding containers won't be included in the list.</span></span> 
    
6. <span data-ttu-id="b1a4d-129">Pour charger les données de résultats de recherche à partir d’un conteneur dans le cas dans Advanced eDiscovery, sélectionnez un conteneur, puis cliquez sur **traiter**.</span><span class="sxs-lookup"><span data-stu-id="b1a4d-129">To load the search result data from a container in to the case in Advanced eDiscovery, select a container and then click **Process**.</span></span>
    
<span data-ttu-id="b1a4d-130">Une fois que les résultats de la &amp; recherche du centre de sécurité conformité sont ajoutés à l’incident dans Advanced eDiscovery, l’étape suivante consiste à utiliser les outils dans Advanced eDiscovery pour analyser et rechercher les données pertinentes pour le cas.</span><span class="sxs-lookup"><span data-stu-id="b1a4d-130">After the search results from the Security &amp; Compliance Center are added to the case in Advanced eDiscovery, the next step is to use the tools in Advanced eDiscovery to analyze and cull the data that's relevant to the case.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b1a4d-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1a4d-131">See also</span></span>

[<span data-ttu-id="b1a4d-132">Découverte électronique avancée (classique)</span><span class="sxs-lookup"><span data-stu-id="b1a4d-132">Advanced eDiscovery (classic)</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="b1a4d-133">Configurer des utilisateurs et des cas</span><span class="sxs-lookup"><span data-stu-id="b1a4d-133">Set up users and cases</span></span>](set-up-users-and-cases-in-advanced-ediscovery.md)
  
[<span data-ttu-id="b1a4d-134">Analyse des données d’un cas</span><span class="sxs-lookup"><span data-stu-id="b1a4d-134">Analyzing case data</span></span>](analyze-case-data-with-advanced-ediscovery.md)
  
[<span data-ttu-id="b1a4d-135">Gestion de la configuration de la pertinence</span><span class="sxs-lookup"><span data-stu-id="b1a4d-135">Managing Relevance setup</span></span>](manage-relevance-setup-in-advanced-ediscovery.md)
  
[<span data-ttu-id="b1a4d-136">Utilisation du module de pertinence</span><span class="sxs-lookup"><span data-stu-id="b1a4d-136">Using the Relevance module</span></span>](use-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="b1a4d-137">Exportation des données d’un cas</span><span class="sxs-lookup"><span data-stu-id="b1a4d-137">Exporting case data</span></span>](export-case-data-in-advanced-ediscovery.md)

