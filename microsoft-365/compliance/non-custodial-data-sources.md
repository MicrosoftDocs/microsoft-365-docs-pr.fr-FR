---
title: Ajouter des sources de données non privatives à un cas Advanced eDiscovery
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
description: Vous pouvez ajouter des sources de données non privatives à un cas Advanced eDiscovery et placer une mise en attente sur la source de données. Les sources de données non privatives sont réindexées, de sorte que tout contenu marqué comme partiellement indexé est retrait pour le rendre entièrement et rapidement utilisable dans une recherche.
ms.openlocfilehash: 467f0e1167bfebe21bd3f2bbd52acd81529b8685
ms.sourcegitcommit: 36d12e02f6fda199ae7f2fb72fe52d7e2b5b4efd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/31/2020
ms.locfileid: "49740351"
---
# <a name="add-non-custodial-data-sources-to-an-advanced-ediscovery-case"></a><span data-ttu-id="94c3b-104">Ajouter des sources de données non privatives à un cas Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="94c3b-104">Add non-custodial data sources to an Advanced eDiscovery case</span></span>

<span data-ttu-id="94c3b-105">Dans les cas Advanced eDiscovery, il ne répond pas toujours à vos besoins d’associer une source de données Microsoft 365 à un dépositaire dans le cas.</span><span class="sxs-lookup"><span data-stu-id="94c3b-105">In Advanced eDiscovery cases, it doesn't always meet your needs to associate a Microsoft 365 data source with a custodian in the case.</span></span> <span data-ttu-id="94c3b-106">Toutefois, vous devrez peut-être associer ces données à un cas afin de pouvoir les rechercher, les ajouter à un groupe de révision, les analyser et les réviser.</span><span class="sxs-lookup"><span data-stu-id="94c3b-106">But you may still need to associate that data with a case so that you can search it, add it to a review set, and analyze and review it.</span></span> <span data-ttu-id="94c3b-107">La fonctionnalité advanced eDiscovery est appelée sources de données *non* privatives et vous permet d’ajouter des données à un cas sans avoir à les associer à un dépositaire.</span><span class="sxs-lookup"><span data-stu-id="94c3b-107">The feature in Advanced eDiscovery is called *non-custodial data sources* and lets you add data to a case without having to associate it to a custodian.</span></span> <span data-ttu-id="94c3b-108">Il applique également la même fonctionnalité Advanced eDiscovery aux données qui ne sont pas en conservation qui sont disponibles pour les données associées au dépositaire.</span><span class="sxs-lookup"><span data-stu-id="94c3b-108">It also applies the same Advanced eDiscovery functionality to non-custodial data that's available for data associated with custodian.</span></span> <span data-ttu-id="94c3b-109">L’une des choses les plus utiles que vous pouvez appliquer aux données qui ne sont pas en attente est de les placer en attente et de les traiter à l’aide de [l’indexation avancée](indexing-custodian-data.md).</span><span class="sxs-lookup"><span data-stu-id="94c3b-109">Two of the most useful things that you can apply to non-custodial data is placing it on hold and processing it using [Advanced indexing](indexing-custodian-data.md).</span></span>

## <a name="add-a-non-custodial-data-source"></a><span data-ttu-id="94c3b-110">Ajouter une source de données non privative</span><span class="sxs-lookup"><span data-stu-id="94c3b-110">Add a non-custodial data source</span></span>

<span data-ttu-id="94c3b-111">Suivez ces étapes pour ajouter et gérer des sources de données non privatives dans un cas Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="94c3b-111">Follow these steps to add and manage non-custodial data sources in an Advanced eDiscovery case.</span></span>

1. <span data-ttu-id="94c3b-112">Dans la page **d’accueil Advanced eDiscovery,** cliquez sur le cas où vous souhaitez ajouter les données.</span><span class="sxs-lookup"><span data-stu-id="94c3b-112">On the **Advanced eDiscovery** home page, click the case that you want to add the data to.</span></span>

2. <span data-ttu-id="94c3b-113">Cliquez sur **l’onglet Sources** de données, puis sur **Ajouter une source** de données Ajouter des  >  **emplacements de données.**</span><span class="sxs-lookup"><span data-stu-id="94c3b-113">Click the **Data sources** tab and then click **Add data source** > **Add data locations**.</span></span>

3. <span data-ttu-id="94c3b-114">Dans la page **De nouveaux emplacements** de données non privatives, choisissez les sources de données que vous souhaitez ajouter au cas.</span><span class="sxs-lookup"><span data-stu-id="94c3b-114">On the **New non-custodial data locations** flyout page, choose the data sources that you want to add to the case.</span></span> <span data-ttu-id="94c3b-115">Vous pouvez ajouter plusieurs boîtes aux lettres et sites en développez les sections **SharePoint** ou **Exchange,** puis en cliquant sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="94c3b-115">You can add multiple mailboxes and sites by expanding the **SharePoint** or **Exchange** sections and then clicking **Edit**.</span></span>

   ![Ajouter des sites SharePoint et des boîtes aux lettres Exchange en tant que sources de données non privatives](../media/NonCustodialDataSources1.png)

   - <span data-ttu-id="94c3b-117">**SharePoint** - Cliquez sur **Modifier** pour ajouter des sites.</span><span class="sxs-lookup"><span data-stu-id="94c3b-117">**SharePoint** - Click **Edit** to add sites.</span></span> <span data-ttu-id="94c3b-118">Sélectionnez un site dans la liste ou vous pouvez rechercher un site en tapant l’URL du site dans la barre de recherche.</span><span class="sxs-lookup"><span data-stu-id="94c3b-118">Select a site in the list or you can search for a site by typing the URL of the site in the search bar.</span></span> <span data-ttu-id="94c3b-119">Sélectionnez les sites que vous souhaitez ajouter en tant que sources de données non-dépositaire, puis cliquez sur **Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="94c3b-119">Select the sites that you want to add as non-custodian data sources and click **Add**.</span></span>

   - <span data-ttu-id="94c3b-120">**Exchange** : cliquez sur **Modifier** pour ajouter des boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="94c3b-120">**Exchange** - Click **Edit** to add mailboxes.</span></span> <span data-ttu-id="94c3b-121">Tapez un nom ou un alias (un minimum de trois caractères) dans la zone de recherche pour les boîtes aux lettres ou les groupes de distribution.</span><span class="sxs-lookup"><span data-stu-id="94c3b-121">Type a name or alias (a minimum of three characters) in the search box for mailboxes or distribution groups.</span></span> <span data-ttu-id="94c3b-122">Sélectionnez les boîtes aux lettres que vous souhaitez ajouter en tant que sources de données non dépositaires, puis cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="94c3b-122">Select the mailboxes that you want to add as non-custodian data sources and click **Add**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="94c3b-123">Vous pouvez utiliser les sections **SharePoint** et **Exchange** pour ajouter des sites et des boîtes aux lettres associés à une équipe ou un groupe Yammer en tant que sources de données non privatives.</span><span class="sxs-lookup"><span data-stu-id="94c3b-123">You can use the **SharePoint** and **Exchange** sections to add sites and mailboxes associated with a Team or Yammer group as non-custodial data sources.</span></span> <span data-ttu-id="94c3b-124">Vous devez ajouter séparément la boîte aux lettres et le site associés à une équipe ou un Yammer groupe.</span><span class="sxs-lookup"><span data-stu-id="94c3b-124">You have to separately add the mailbox and site associated with a Team or Yammer group.</span></span>

4. <span data-ttu-id="94c3b-125">Après avoir ajouté des sources de données non privatives, vous avez la possibilité de placer ou non ces emplacements en attente.</span><span class="sxs-lookup"><span data-stu-id="94c3b-125">After you add non-custodial data sources, you have the option to place those locations on hold or not.</span></span> <span data-ttu-id="94c3b-126">Cochez ou désélectionnez la case **à** cocher Mettre en attente en regard de la source de données pour la placer en attente.</span><span class="sxs-lookup"><span data-stu-id="94c3b-126">Select or unselect the **Hold** checkbox next to the data source to place it on hold.</span></span>

5. <span data-ttu-id="94c3b-127">Cliquez **sur Ajouter** au bas de la page volant Nouveaux emplacements de données **non** privatives pour ajouter les sources de données au cas.</span><span class="sxs-lookup"><span data-stu-id="94c3b-127">Click **Add** at the bottom of the **New non-custodial data locations** flyout page to add the data sources to the case.</span></span>

   <span data-ttu-id="94c3b-128">Chaque source de données non privative que vous avez ajoutée est répertoriée dans la page **Sources de** données.</span><span class="sxs-lookup"><span data-stu-id="94c3b-128">Each non-custodial data source that you added is listed on the **Data sources** page.</span></span> <span data-ttu-id="94c3b-129">Les sources de données non privatives sont identifiées par la valeur **d’emplacement des** données dans la **colonne Type de** source.</span><span class="sxs-lookup"><span data-stu-id="94c3b-129">Non-custodial data sources are identified by the **Data location** value in the **Source type** column.</span></span>

   ![Sources de données non privatives sous l’onglet Sources de données](../media/NonCustodialDataSources2.png)

<span data-ttu-id="94c3b-131">Une fois que vous avez ajouté des sources de données non privatives au cas,  un travail nommé *Réindexation* des données non privatives est créé et affiché sous l’onglet Travaux du cas.</span><span class="sxs-lookup"><span data-stu-id="94c3b-131">After you add non-custodial data sources to the case, a job named *Reindexing non-custodial data* is created and displayed on the **Jobs** tab of the case.</span></span> <span data-ttu-id="94c3b-132">Une fois le travail créé, le processus d’indexation avancée est lancé et les sources de données sont réindexées.</span><span class="sxs-lookup"><span data-stu-id="94c3b-132">After the job is created, the Advanced indexing process in initiated and the data sources are reindexed.</span></span>

## <a name="manage-the-hold-for-non-custodial-data-sources"></a><span data-ttu-id="94c3b-133">Gérer la mise en attente pour les sources de données non privatives</span><span class="sxs-lookup"><span data-stu-id="94c3b-133">Manage the hold for non-custodial data sources</span></span>

<span data-ttu-id="94c3b-134">Après avoir mis en attente une source de données non privative, une stratégie de mise en attente contenant les sources de données non privatives du cas est automatiquement créée.</span><span class="sxs-lookup"><span data-stu-id="94c3b-134">After you place a hold on a non-custodial data source, a hold policy that contains the non-custodial data sources for the case is automatically created.</span></span> <span data-ttu-id="94c3b-135">Lorsque vous placez d’autres sources de données non privatives en attente, elles sont ajoutées à cette stratégie de mise en attente.</span><span class="sxs-lookup"><span data-stu-id="94c3b-135">When you place other non-custodial data sources on hold, they are added to this hold policy.</span></span>

1. <span data-ttu-id="94c3b-136">Ouvrez le cas Advanced eDiscovery et sélectionnez **l’onglet** Conserver.</span><span class="sxs-lookup"><span data-stu-id="94c3b-136">Open the Advanced eDiscovery case and select the **Hold** tab.</span></span>

2. <span data-ttu-id="94c3b-137">Cliquez **sur NCDSHold- \<GUID\>**, où la valeur GUID est propre au cas.</span><span class="sxs-lookup"><span data-stu-id="94c3b-137">Click **NCDSHold-\<GUID\>**, where the GUID value is unique to the case.</span></span>

   <span data-ttu-id="94c3b-138">La page volante affiche des informations et des statistiques sur les sources de données qui ne sont pas en attente.</span><span class="sxs-lookup"><span data-stu-id="94c3b-138">The flyout page display information and statistics about the non-custodial data sources on hold.</span></span>

   ![La page de présentation des sources de données non privatives affiche des statistiques](../media/NonCustodialDataSourcesHoldFlyout.png)

3. <span data-ttu-id="94c3b-140">Cliquez **sur Modifier la mise** en attente pour afficher les sources de données non privatives placées en attente et effectuer les tâches de gestion suivantes :</span><span class="sxs-lookup"><span data-stu-id="94c3b-140">Click **Edit hold** to view the non-custodial data sources placed on hold and perform the following management tasks:</span></span>

   - <span data-ttu-id="94c3b-141">Dans la page **Emplacements,** vous pouvez libérer une source de données qui n’est pas en attente en la supprimant de la mise en attente.</span><span class="sxs-lookup"><span data-stu-id="94c3b-141">On the **Locations** page, you can release a non-custodial data source by removing it from the hold.</span></span> <span data-ttu-id="94c3b-142">La libération d’une source de données ne supprime pas la source de données non privative du cas.</span><span class="sxs-lookup"><span data-stu-id="94c3b-142">Releasing a data source doesn't remove the non-custodial data source from the case.</span></span> <span data-ttu-id="94c3b-143">Elle supprime uniquement la mise en attente qui a été placée sur la source de données.</span><span class="sxs-lookup"><span data-stu-id="94c3b-143">It only removes the hold that was placed on the data source.</span></span>

   - <span data-ttu-id="94c3b-144">Dans **la** page Requête, vous pouvez modifier la mise en attente pour créer une mise en attente basée sur une requête qui est appliquée à toutes les sources de données sans mise en attente dans le cas.</span><span class="sxs-lookup"><span data-stu-id="94c3b-144">On the **Query** page, you can edit the hold to create a query-based hold that is applied to all tha non-custodial data sources in the case.</span></span>
