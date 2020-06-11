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
ROBOTS: NOINDEX, NOFOLLOW
description: Vous pouvez ajouter des sources de données non privatives de Troie à un cas avancé eDiscovery et mettre en attente la source de données. Les sources de données non privatives de cœur sont réindexées, de sorte que tout contenu considéré comme partiellement indexé est retraité afin de pouvoir faire l’objet d’une recherche complète et rapide.
ms.openlocfilehash: 618d39bfb7be6cd260c88cdf4c57501747f440f1
ms.sourcegitcommit: b03a7ad0a80f8b839f40b8d396ab3a049491a12f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/10/2020
ms.locfileid: "44695499"
---
# <a name="add-non-custodial-data-sources-to-an-advanced-ediscovery-case"></a><span data-ttu-id="1997a-104">Ajout de sources de données non privatives de Troie à un cas avancé eDiscovery</span><span class="sxs-lookup"><span data-stu-id="1997a-104">Add non-custodial data sources to an Advanced eDiscovery case</span></span>

<span data-ttu-id="1997a-105">Dans les cas de découverte électronique avancée, il ne répond pas toujours à vos besoins pour associer une source de données Microsoft 365 à un dépositaire dans le cas.</span><span class="sxs-lookup"><span data-stu-id="1997a-105">In Advanced eDiscovery cases, it doesn't always meet your needs to associate a Microsoft 365 data source with a custodian in the case.</span></span> <span data-ttu-id="1997a-106">Toutefois, vous devrez peut-être toujours associer ces données à un cas afin de les Rechercher, de les ajouter à l’ensemble de la révision et de les consulter.</span><span class="sxs-lookup"><span data-stu-id="1997a-106">But you may still need to associate that data with a case so that you search it, add it to review set, and review it.</span></span> <span data-ttu-id="1997a-107">La nouvelle fonctionnalité *, appelée sources de données non privatives de ressources,* vous permet d’ajouter des données à un cas sans avoir à associer les données à un dépositaire.</span><span class="sxs-lookup"><span data-stu-id="1997a-107">The new feature called *non-custodial data sources* lets you add data to a case without having to associate the data to a custodian.</span></span> <span data-ttu-id="1997a-108">Elle applique également la même fonctionnalité eDiscovery avancée aux données non privatives de Troie qui sont disponibles pour les données associées aux dépositaires.</span><span class="sxs-lookup"><span data-stu-id="1997a-108">It also applies the same Advanced eDiscovery functionality to non-custodial data that's available for data associated with custodian.</span></span> <span data-ttu-id="1997a-109">Deux des fonctionnalités les plus utiles que vous pouvez appliquer à des données non privatives de temps sont placées en conservation et traitées à l’aide de l' [indexation avancée](indexing-custodian-data.md).</span><span class="sxs-lookup"><span data-stu-id="1997a-109">Two of the most useful features that you can apply to non-custodial data is placing it on hold and processing it using [Advanced indexing](indexing-custodian-data.md).</span></span>

## <a name="add-a-non-custodial-data-source"></a><span data-ttu-id="1997a-110">Ajouter une source de données non-privatives de cœur</span><span class="sxs-lookup"><span data-stu-id="1997a-110">Add a non-custodial data source</span></span>

<span data-ttu-id="1997a-111">Procédez comme suit pour ajouter et gérer des sources de données non privatives de Troie dans un cas avancé de découverte électronique.</span><span class="sxs-lookup"><span data-stu-id="1997a-111">Follow these steps to add and manage non-custodial data sources in an Advanced eDiscovery case.</span></span>

1. <span data-ttu-id="1997a-112">Sur la page d’accueil de la **découverte électronique avancée** , cliquez sur le cas auquel vous souhaitez ajouter les données.</span><span class="sxs-lookup"><span data-stu-id="1997a-112">On the **Advanced eDiscovery** home page, click the case that you want to add the data to.</span></span>

2. <span data-ttu-id="1997a-113">Sur la page **sources** , cliquez sur l’onglet **emplacements de données** , puis cliquez sur Ajouter un emplacement de **données**.</span><span class="sxs-lookup"><span data-stu-id="1997a-113">On the **Sources** page, click the **Data locations** tab, and then click **Add data location**.</span></span>

3. <span data-ttu-id="1997a-114">Cliquez sur **Ajouter un emplacement de données** , puis choisissez les sources de données que vous souhaitez ajouter à l’incident.</span><span class="sxs-lookup"><span data-stu-id="1997a-114">Click **Add data location** and choose the data sources that you want to add to the case.</span></span> <span data-ttu-id="1997a-115">Vous pouvez ajouter plusieurs sites et boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="1997a-115">You can add multiple mailboxes and sites.</span></span>

4. <span data-ttu-id="1997a-116">Dans la page **choisir les emplacements** de l’Assistant, ajoutez des boîtes aux lettres ou des sites (ou les deux) comme sources de données non-privatives de ressources pour le cas.</span><span class="sxs-lookup"><span data-stu-id="1997a-116">On the **Choose locations** page in the wizard, add mailboxes or sites (or both) as non-custodial data sources to the case.</span></span>

5. <span data-ttu-id="1997a-117">Après avoir ajouté les sources de données, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="1997a-117">After adding the data sources, click **Next**.</span></span>

6. <span data-ttu-id="1997a-118">Sur la page **Placer** en attente, choisissez les sources de données que vous souhaitez mettre en attente en activant ou en désactivant la case à cocher associée.</span><span class="sxs-lookup"><span data-stu-id="1997a-118">On the **Place holds** page, choose which data sources you want to place on hold by selecting or unselecting the associated checkbox.</span></span>

7. <span data-ttu-id="1997a-119">Vérifiez les sélections de blocage, puis cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="1997a-119">Verify the hold selections and then click **Submit**.</span></span>

   <span data-ttu-id="1997a-120">Chaque source de données qui n’est pas une source de données non privatives ajoutée est indiquée dans la page **sources de données** .</span><span class="sxs-lookup"><span data-stu-id="1997a-120">Each non-custodial data source that you added is listed on the **Data sources** page.</span></span>

   <span data-ttu-id="1997a-121">De plus, un travail appelé *ré-indexation des données non privatives* est créé et affiché sous l’onglet **travaux** de l’incident.</span><span class="sxs-lookup"><span data-stu-id="1997a-121">Also, a job named *Re-indexing non-custodial data* is created and displayed on the **Jobs** tab of the case.</span></span> <span data-ttu-id="1997a-122">Une fois le travail créé, le processus d’indexation avancé dans initié et les sources de données sont réindexés.</span><span class="sxs-lookup"><span data-stu-id="1997a-122">After the job is created, the Advanced indexing process in initiated and the data sources are re-indexed.</span></span>

## <a name="managing-the-hold-on-non-custodial-data-sources"></a><span data-ttu-id="1997a-123">Gestion de la conservation sur des sources de données non-privatives de cœur</span><span class="sxs-lookup"><span data-stu-id="1997a-123">Managing the hold on non-custodial data sources</span></span>

<span data-ttu-id="1997a-124">Une fois que vous avez placé une conservation sur une source de données non privatives de place, une stratégie de blocage contenant toutes les sources de données non privatives de l’incident est automatiquement créée.</span><span class="sxs-lookup"><span data-stu-id="1997a-124">After you place a hold on a non-custodial data source, a hold policy that contains all non-custodial data sources for the case is automatically created.</span></span> <span data-ttu-id="1997a-125">Lorsque vous placez des sources de données non privatives de conservation supplémentaires, elles sont ajoutées à cette stratégie de blocage.</span><span class="sxs-lookup"><span data-stu-id="1997a-125">When you place additional non-custodial data sources on hold, they are added to this hold policy.</span></span>

1. <span data-ttu-id="1997a-126">Sur la page d' **Accueil** de l’incident, cliquez sur l’onglet **suspensions** .</span><span class="sxs-lookup"><span data-stu-id="1997a-126">On the **Home** page of the case, click the **Holds** tab.</span></span>

2. <span data-ttu-id="1997a-127">Sur la page **suspensions** , cliquez sur **NCDSHold \<GUID\> -**, où la valeur GUID est unique pour le cas.</span><span class="sxs-lookup"><span data-stu-id="1997a-127">On the **Holds** page, and click **NCDSHold-\<GUID\>**, where the GUID value is unique to the case.</span></span>

3. <span data-ttu-id="1997a-128">Sur la page de la fenêtre déroulante, cliquez sur **modifier le blocage** pour afficher toutes les sources de données non-privatives de stock mises en attente.</span><span class="sxs-lookup"><span data-stu-id="1997a-128">On the flyout page, click **Edit hold** to view all the non-custodial data sources that are placed on hold.</span></span>

<span data-ttu-id="1997a-129">Vous pouvez effectuer la tâche de gestion suivante sur des sources de données non privatives de Troie :</span><span class="sxs-lookup"><span data-stu-id="1997a-129">You can perform the following management task on non-custodial data sources:</span></span>

- <span data-ttu-id="1997a-130">Vous pouvez modifier la conservation pour créer une conservation basée sur une requête qui est appliquée à toutes les sources de données non-privatives dans le cas.</span><span class="sxs-lookup"><span data-stu-id="1997a-130">You can edit the hold to create a query-based hold that is applied to all non-custodial data sources in the case.</span></span>

- <span data-ttu-id="1997a-131">Vous pouvez libérer une source de données non privatives de personnes à partir de la suspension.</span><span class="sxs-lookup"><span data-stu-id="1997a-131">You can release a non-custodial data source from the hold.</span></span> <span data-ttu-id="1997a-132">La libération d’une source de données ne supprime pas la source de données non privatives de la casse.</span><span class="sxs-lookup"><span data-stu-id="1997a-132">Releasing a data source doesn't remove the non-custodial data source from the case.</span></span> <span data-ttu-id="1997a-133">Il supprime uniquement le blocage passé sur la source de données.</span><span class="sxs-lookup"><span data-stu-id="1997a-133">It only removes the hold that was placed on the data source.</span></span>
