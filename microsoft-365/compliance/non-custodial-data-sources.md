---
title: Ajout de sources de données non privatives de Troie à un cas avancé eDiscovery
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Vous pouvez ajouter des sources de données non privatives de Troie à un cas avancé eDiscovery et mettre en attente la source de données. Les sources de données non privatives de cœur sont réindexées, de sorte que tout contenu marqué comme partiellement indexé est retraité afin de pouvoir faire l’objet d’une recherche complète et rapide.
ms.openlocfilehash: 467f0e1167bfebe21bd3f2bbd52acd81529b8685
ms.sourcegitcommit: 36d12e02f6fda199ae7f2fb72fe52d7e2b5b4efd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/31/2020
ms.locfileid: "49740351"
---
# <a name="add-non-custodial-data-sources-to-an-advanced-ediscovery-case"></a><span data-ttu-id="abc44-104">Ajout de sources de données non privatives de Troie à un cas avancé eDiscovery</span><span class="sxs-lookup"><span data-stu-id="abc44-104">Add non-custodial data sources to an Advanced eDiscovery case</span></span>

<span data-ttu-id="abc44-105">Dans les cas de découverte électronique avancée, il ne répond pas toujours à vos besoins pour associer une source de données Microsoft 365 à un dépositaire dans le cas.</span><span class="sxs-lookup"><span data-stu-id="abc44-105">In Advanced eDiscovery cases, it doesn't always meet your needs to associate a Microsoft 365 data source with a custodian in the case.</span></span> <span data-ttu-id="abc44-106">Toutefois, vous devrez peut-être toujours associer ces données à un cas afin de pouvoir les Rechercher, de les ajouter à un jeu de révision et de les analyser et de les consulter.</span><span class="sxs-lookup"><span data-stu-id="abc44-106">But you may still need to associate that data with a case so that you can search it, add it to a review set, and analyze and review it.</span></span> <span data-ttu-id="abc44-107">La fonctionnalité de Advanced eDiscovery est appelée *sources de données non privatives* et vous permet d’ajouter des données à un cas sans avoir à l’associer à un dépositaire.</span><span class="sxs-lookup"><span data-stu-id="abc44-107">The feature in Advanced eDiscovery is called *non-custodial data sources* and lets you add data to a case without having to associate it to a custodian.</span></span> <span data-ttu-id="abc44-108">Elle applique également la même fonctionnalité eDiscovery avancée aux données non privatives de Troie qui sont disponibles pour les données associées aux dépositaires.</span><span class="sxs-lookup"><span data-stu-id="abc44-108">It also applies the same Advanced eDiscovery functionality to non-custodial data that's available for data associated with custodian.</span></span> <span data-ttu-id="abc44-109">Deux des éléments les plus utiles que vous pouvez appliquer à des données non privatives de temps sont mis en attente et traités à l’aide de l' [indexation avancée](indexing-custodian-data.md).</span><span class="sxs-lookup"><span data-stu-id="abc44-109">Two of the most useful things that you can apply to non-custodial data is placing it on hold and processing it using [Advanced indexing](indexing-custodian-data.md).</span></span>

## <a name="add-a-non-custodial-data-source"></a><span data-ttu-id="abc44-110">Ajouter une source de données non-privatives de cœur</span><span class="sxs-lookup"><span data-stu-id="abc44-110">Add a non-custodial data source</span></span>

<span data-ttu-id="abc44-111">Procédez comme suit pour ajouter et gérer des sources de données non privatives de Troie dans un cas avancé de découverte électronique.</span><span class="sxs-lookup"><span data-stu-id="abc44-111">Follow these steps to add and manage non-custodial data sources in an Advanced eDiscovery case.</span></span>

1. <span data-ttu-id="abc44-112">Sur la page d’accueil de la **découverte électronique avancée** , cliquez sur le cas auquel vous souhaitez ajouter les données.</span><span class="sxs-lookup"><span data-stu-id="abc44-112">On the **Advanced eDiscovery** home page, click the case that you want to add the data to.</span></span>

2. <span data-ttu-id="abc44-113">Cliquez sur l’onglet **sources de données** , puis cliquez sur **Ajouter une source** de données pour ajouter des  >  **emplacements de données**.</span><span class="sxs-lookup"><span data-stu-id="abc44-113">Click the **Data sources** tab and then click **Add data source** > **Add data locations**.</span></span>

3. <span data-ttu-id="abc44-114">Sur la nouvelle page de menu volant **emplacements des données non privatives** de personnes, choisissez les sources de données que vous souhaitez ajouter à l’incident.</span><span class="sxs-lookup"><span data-stu-id="abc44-114">On the **New non-custodial data locations** flyout page, choose the data sources that you want to add to the case.</span></span> <span data-ttu-id="abc44-115">Vous pouvez ajouter plusieurs boîtes aux lettres et sites en développant les sections **SharePoint** ou **Exchange** , puis en cliquant sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="abc44-115">You can add multiple mailboxes and sites by expanding the **SharePoint** or **Exchange** sections and then clicking **Edit**.</span></span>

   ![Ajouter des sites SharePoint et des boîtes aux lettres Exchange en tant que sources de données non privatives de cœur](../media/NonCustodialDataSources1.png)

   - <span data-ttu-id="abc44-117">**SharePoint** : cliquez sur **modifier** pour ajouter des sites.</span><span class="sxs-lookup"><span data-stu-id="abc44-117">**SharePoint** - Click **Edit** to add sites.</span></span> <span data-ttu-id="abc44-118">Sélectionnez un site dans la liste ou recherchez un site en tapant l’URL du site dans la barre de recherche.</span><span class="sxs-lookup"><span data-stu-id="abc44-118">Select a site in the list or you can search for a site by typing the URL of the site in the search bar.</span></span> <span data-ttu-id="abc44-119">Sélectionnez les sites que vous souhaitez ajouter en tant que sources de données autres que les dépositaires, puis cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="abc44-119">Select the sites that you want to add as non-custodian data sources and click **Add**.</span></span>

   - <span data-ttu-id="abc44-120">**Exchange** -cliquez sur **modifier** pour ajouter des boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="abc44-120">**Exchange** - Click **Edit** to add mailboxes.</span></span> <span data-ttu-id="abc44-121">Tapez un nom ou un alias (un minimum de trois caractères) dans la zone de recherche pour les boîtes aux lettres ou les groupes de distribution.</span><span class="sxs-lookup"><span data-stu-id="abc44-121">Type a name or alias (a minimum of three characters) in the search box for mailboxes or distribution groups.</span></span> <span data-ttu-id="abc44-122">Sélectionnez les boîtes aux lettres que vous souhaitez ajouter en tant que sources de données autres que les dépositaires, puis cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="abc44-122">Select the mailboxes that you want to add as non-custodian data sources and click **Add**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="abc44-123">Vous pouvez utiliser les sections **SharePoint** et **Exchange** pour ajouter des sites et des boîtes aux lettres associés à une équipe ou un groupe yammer en tant que sources de données non-privatives de cœur.</span><span class="sxs-lookup"><span data-stu-id="abc44-123">You can use the **SharePoint** and **Exchange** sections to add sites and mailboxes associated with a Team or Yammer group as non-custodial data sources.</span></span> <span data-ttu-id="abc44-124">Vous devez ajouter séparément la boîte aux lettres et le site associés à une équipe ou un groupe Yammer.</span><span class="sxs-lookup"><span data-stu-id="abc44-124">You have to separately add the mailbox and site associated with a Team or Yammer group.</span></span>

4. <span data-ttu-id="abc44-125">Une fois que vous avez ajouté des sources de données non-privatives de place, vous avez la possibilité de placer ces emplacements en conservation.</span><span class="sxs-lookup"><span data-stu-id="abc44-125">After you add non-custodial data sources, you have the option to place those locations on hold or not.</span></span> <span data-ttu-id="abc44-126">Activez ou désactivez la case à cocher **maintenir** en regard de la source de données pour la placer en conservation.</span><span class="sxs-lookup"><span data-stu-id="abc44-126">Select or unselect the **Hold** checkbox next to the data source to place it on hold.</span></span>

5. <span data-ttu-id="abc44-127">Cliquez sur **Ajouter** au bas de la nouvelle page de menu volant **emplacements des données non privatives** pour ajouter les sources de données au cas.</span><span class="sxs-lookup"><span data-stu-id="abc44-127">Click **Add** at the bottom of the **New non-custodial data locations** flyout page to add the data sources to the case.</span></span>

   <span data-ttu-id="abc44-128">Chaque source de données qui n’est pas une source de données non privatives ajoutée est indiquée dans la page **sources de données** .</span><span class="sxs-lookup"><span data-stu-id="abc44-128">Each non-custodial data source that you added is listed on the **Data sources** page.</span></span> <span data-ttu-id="abc44-129">Les sources de données non privatives de cœur sont identifiées par la valeur d' **emplacement des données** dans la colonne **type de source** .</span><span class="sxs-lookup"><span data-stu-id="abc44-129">Non-custodial data sources are identified by the **Data location** value in the **Source type** column.</span></span>

   ![Sources de données non privatives de Troie sous l’onglet sources de données](../media/NonCustodialDataSources2.png)

<span data-ttu-id="abc44-131">Une fois que vous avez ajouté des sources de données non-privatives de Troie, une tâche nommée *réindexation des données non privatives* est créée et affichée sous l’onglet **travaux** de l’incident.</span><span class="sxs-lookup"><span data-stu-id="abc44-131">After you add non-custodial data sources to the case, a job named *Reindexing non-custodial data* is created and displayed on the **Jobs** tab of the case.</span></span> <span data-ttu-id="abc44-132">Une fois le travail créé, le processus d’indexation avancé dans initié et les sources de données sont réindexés.</span><span class="sxs-lookup"><span data-stu-id="abc44-132">After the job is created, the Advanced indexing process in initiated and the data sources are reindexed.</span></span>

## <a name="manage-the-hold-for-non-custodial-data-sources"></a><span data-ttu-id="abc44-133">Gérer la conservation pour les sources de données non-privatives de cœur</span><span class="sxs-lookup"><span data-stu-id="abc44-133">Manage the hold for non-custodial data sources</span></span>

<span data-ttu-id="abc44-134">Une fois que vous avez placé une conservation sur une source de données non privatives de place, une stratégie de blocage contenant les sources de données non privatives de l’incident est automatiquement créée.</span><span class="sxs-lookup"><span data-stu-id="abc44-134">After you place a hold on a non-custodial data source, a hold policy that contains the non-custodial data sources for the case is automatically created.</span></span> <span data-ttu-id="abc44-135">Lorsque vous placez d’autres sources de données qui ne sont pas privatives de place en conservation, elles sont ajoutées à cette stratégie de blocage.</span><span class="sxs-lookup"><span data-stu-id="abc44-135">When you place other non-custodial data sources on hold, they are added to this hold policy.</span></span>

1. <span data-ttu-id="abc44-136">Ouvrez le cas eDiscovery avancé et sélectionnez l’onglet **blocage** .</span><span class="sxs-lookup"><span data-stu-id="abc44-136">Open the Advanced eDiscovery case and select the **Hold** tab.</span></span>

2. <span data-ttu-id="abc44-137">Cliquez sur **NCDSHold \<GUID\> -**, où la valeur GUID est unique pour le cas.</span><span class="sxs-lookup"><span data-stu-id="abc44-137">Click **NCDSHold-\<GUID\>**, where the GUID value is unique to the case.</span></span>

   <span data-ttu-id="abc44-138">La page de menu volant affiche des informations et des statistiques sur les sources de données non-privatives de stock en attente.</span><span class="sxs-lookup"><span data-stu-id="abc44-138">The flyout page display information and statistics about the non-custodial data sources on hold.</span></span>

   ![La page de menu volant pour les sources de données non-privatives de ressources contient les statistiques](../media/NonCustodialDataSourcesHoldFlyout.png)

3. <span data-ttu-id="abc44-140">Cliquez sur **modifier le blocage** pour afficher les sources de données qui ne sont pas privatives de place et effectuez les tâches de gestion suivantes :</span><span class="sxs-lookup"><span data-stu-id="abc44-140">Click **Edit hold** to view the non-custodial data sources placed on hold and perform the following management tasks:</span></span>

   - <span data-ttu-id="abc44-141">Sur la page **emplacements** , vous pouvez libérer une source de données non privatives de ressources en la supprimant de la conservation.</span><span class="sxs-lookup"><span data-stu-id="abc44-141">On the **Locations** page, you can release a non-custodial data source by removing it from the hold.</span></span> <span data-ttu-id="abc44-142">La libération d’une source de données ne supprime pas la source de données non privatives de la casse.</span><span class="sxs-lookup"><span data-stu-id="abc44-142">Releasing a data source doesn't remove the non-custodial data source from the case.</span></span> <span data-ttu-id="abc44-143">Il supprime uniquement le blocage passé sur la source de données.</span><span class="sxs-lookup"><span data-stu-id="abc44-143">It only removes the hold that was placed on the data source.</span></span>

   - <span data-ttu-id="abc44-144">Sur la page de **requête** , vous pouvez modifier la conservation pour créer une conservation basée sur une requête qui est appliquée à toutes les sources de données non-privatives Tha dans le cas.</span><span class="sxs-lookup"><span data-stu-id="abc44-144">On the **Query** page, you can edit the hold to create a query-based hold that is applied to all tha non-custodial data sources in the case.</span></span>
