---
title: Gérer la découverte de rubriques dans les rubriques microsoft
ms.author: mikeplum
author: MikePlumleyMSFT
manager: serdars
ms.reviewer: nkokoye
audience: admin
ms.topic: article
ms.service: o365-administration
search.appverid: MET150
localization_priority: Normal
description: Découvrez comment administrer la découverte de rubriques dans les rubriques microsoft.
ms.openlocfilehash: 53e304dc69ccf2ca6fe01d29f0997c539406b0fe
ms.sourcegitcommit: 4acf613587128cae27e0fd470d1216b509775529
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/15/2021
ms.locfileid: "51768973"
---
# <a name="manage-topic-discovery-in-microsoft-viva-topics"></a><span data-ttu-id="64fef-103">Gérer la découverte de rubriques dans les rubriques microsoft</span><span class="sxs-lookup"><span data-stu-id="64fef-103">Manage topic discovery in Microsoft Viva Topics</span></span>

<span data-ttu-id="64fef-104">Vous pouvez gérer les paramètres de découverte de rubrique dans [le centre Microsoft 365'administration.](https://admin.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="64fef-104">You can manage topic discovery settings in the [Microsoft 365 admin center](https://admin.microsoft.com).</span></span> <span data-ttu-id="64fef-105">Vous devez être administrateur général ou administrateur SharePoint pour effectuer ces tâches.</span><span class="sxs-lookup"><span data-stu-id="64fef-105">You must be a global administrator or SharePoint administrator to perform these tasks.</span></span>

## <a name="to-access-topics-management-settings"></a><span data-ttu-id="64fef-106">Pour accéder aux paramètres de gestion des rubriques :</span><span class="sxs-lookup"><span data-stu-id="64fef-106">To access topics management settings:</span></span>

1. <span data-ttu-id="64fef-107">Dans le Microsoft 365 d’administration, cliquez **sur Paramètres,** puis sur **Paramètres de l’organisation.**</span><span class="sxs-lookup"><span data-stu-id="64fef-107">In the Microsoft 365 admin center, click **Settings**, then **Org settings**.</span></span>
2. <span data-ttu-id="64fef-108">Sous **l’onglet Services,** cliquez sur **Expériences de rubrique.**</span><span class="sxs-lookup"><span data-stu-id="64fef-108">On the **Services** tab, click **Topic experiences**.</span></span>

    ![Connecter personnes à connaître](../media/admin-org-knowledge-options-completed.png) 

3. <span data-ttu-id="64fef-110">Sélectionnez **l’onglet Découverte de** rubrique. Consultez les sections suivantes pour plus d’informations sur chaque paramètre.</span><span class="sxs-lookup"><span data-stu-id="64fef-110">Select the **Topic discovery** tab. See the following sections for information about each setting.</span></span>

    ![knowledge-network-settings](../media/knowledge-network-settings-topic-discovery.png) 

## <a name="select-sharepoint-topic-sources"></a><span data-ttu-id="64fef-112">Sélectionner SharePoint sources de rubriques</span><span class="sxs-lookup"><span data-stu-id="64fef-112">Select SharePoint topic sources</span></span>

<span data-ttu-id="64fef-113">Vous pouvez modifier les SharePoint sites de votre organisation qui seront analyser pour les rubriques.</span><span class="sxs-lookup"><span data-stu-id="64fef-113">You can change the SharePoint sites in your organization that will be crawled for topics.</span></span>

<span data-ttu-id="64fef-114">Si vous souhaitez inclure ou exclure une liste spécifique de sites, vous pouvez utiliser le modèle .csv suivant :</span><span class="sxs-lookup"><span data-stu-id="64fef-114">If you want to include or exclude a specific list of sites, you can use the following .csv template:</span></span>

``` csv
Site name,URL
```

<span data-ttu-id="64fef-115">Si vous ajoutez des sites à l'aide du sélecteur de sites, ils sont ajoutés à la liste existante des sites à inclure ou à exclure.</span><span class="sxs-lookup"><span data-stu-id="64fef-115">If you add sites using the site picker, they are added to the existing list of sites to include or exclude.</span></span> <span data-ttu-id="64fef-116">Si vous téléchargez un fichier .csv, il remplace toute liste existante.</span><span class="sxs-lookup"><span data-stu-id="64fef-116">If you upload a .csv file, it overwrites any existing list.</span></span> <span data-ttu-id="64fef-117">Si vous avez précédemment inclus ou exclu des sites spécifiques, vous et téléchargez la liste sous la forme d’un fichier .csv, a apporté des modifications et chargez la nouvelle liste.</span><span class="sxs-lookup"><span data-stu-id="64fef-117">If you have previously included or excluded specific sites, you and download the list as a .csv file, make changes, and upload the new list.</span></span>

<span data-ttu-id="64fef-118">Pour choisir des sites pour la découverte de rubriques</span><span class="sxs-lookup"><span data-stu-id="64fef-118">To choose sites for topic discovery</span></span>

1. <span data-ttu-id="64fef-119">Sous l’onglet **Découverte de rubrique** , sous **Sélectionner les sources de rubrique SharePoint**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="64fef-119">On the **Topic discovery** tab, under **Select SharePoint topic sources**, select **Edit**.</span></span>
2. <span data-ttu-id="64fef-120">Dans la page **Sélectionner SharePoint sources** de rubrique, sélectionnez les sites SharePoint qui seront analyser en tant que sources pour vos rubriques lors de la découverte.</span><span class="sxs-lookup"><span data-stu-id="64fef-120">On the **Select SharePoint topic sources** page, select which SharePoint sites will be crawled as sources for your topics during discovery.</span></span> <span data-ttu-id="64fef-121">Cela inclut les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="64fef-121">This includes:</span></span>
    - <span data-ttu-id="64fef-122">**Tous les sites**: tous SharePoint sites de votre client.</span><span class="sxs-lookup"><span data-stu-id="64fef-122">**All sites**: All SharePoint sites in your tenant.</span></span> <span data-ttu-id="64fef-123">Cela capture les sites actuels et futurs.</span><span class="sxs-lookup"><span data-stu-id="64fef-123">This captures current and future sites.</span></span>
    - <span data-ttu-id="64fef-124">**Tous, sauf les sites sélectionnés**: tapez les noms des sites que vous souhaitez exclure.</span><span class="sxs-lookup"><span data-stu-id="64fef-124">**All, except selected sites**: Type the names of the sites you want to exclude.</span></span>  <span data-ttu-id="64fef-125">Vous pouvez également charger une liste de sites que vous souhaitez refuser de découvrir.</span><span class="sxs-lookup"><span data-stu-id="64fef-125">You can also upload a list of sites you want to opt out from discovery.</span></span> <span data-ttu-id="64fef-126">Les sites créés dans le futur seront inclus comme sources pour la découverte de rubriques.</span><span class="sxs-lookup"><span data-stu-id="64fef-126">Sites created in the future will be included as sources for topic discovery.</span></span> 
    - <span data-ttu-id="64fef-127">**Seuls les sites** sélectionnés : tapez les noms des sites que vous souhaitez inclure.</span><span class="sxs-lookup"><span data-stu-id="64fef-127">**Only selected sites**: Type the names of the sites you want to include.</span></span> <span data-ttu-id="64fef-128">Vous pouvez également charger une liste de sites.</span><span class="sxs-lookup"><span data-stu-id="64fef-128">You can also upload a list of sites.</span></span> <span data-ttu-id="64fef-129">Les sites créés dans le futur ne seront pas inclus comme sources pour la découverte de rubriques.</span><span class="sxs-lookup"><span data-stu-id="64fef-129">Sites created in the future will not be included as sources for topic discovery.</span></span>
    - <span data-ttu-id="64fef-130">**Aucun site**: les rubriques ne seront pas générées ou mises à jour automatiquement avec SharePoint contenu.</span><span class="sxs-lookup"><span data-stu-id="64fef-130">**No sites**: Topics won't be automatically generated or updated with SharePoint content.</span></span> <span data-ttu-id="64fef-131">Les rubriques existantes restent dans le centre de rubriques.</span><span class="sxs-lookup"><span data-stu-id="64fef-131">Existing topics remain in the topic center.</span></span>

    ![Capture d’écran SharePoint’interface utilisateur des sources de rubriques](../media/k-manage-select-topic-source.png)
   
3. <span data-ttu-id="64fef-133">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="64fef-133">Click **Save**.</span></span>

## <a name="exclude-topics-by-name"></a><span data-ttu-id="64fef-134">Exclure les rubriques par nom</span><span class="sxs-lookup"><span data-stu-id="64fef-134">Exclude topics by name</span></span>

<span data-ttu-id="64fef-135">Vous pouvez exclure des rubriques de la découverte en téléchargeant une liste à l'aide d'un fichier .csv.</span><span class="sxs-lookup"><span data-stu-id="64fef-135">You can exclude topics from discovery by uploading a list using a .csv file.</span></span> <span data-ttu-id="64fef-136">Si vous avez précédemment exclu des sujets, vous pouvez télécharger le fichier .csv, apporter des modifications , puis le télécharger à nouveau.</span><span class="sxs-lookup"><span data-stu-id="64fef-136">If you've previously excluded topics, you can download the .csv, make changes, and upload it again.</span></span>

1. <span data-ttu-id="64fef-137">Sous l’onglet **Découverte de rubrique**, sous **Exclure les rubriques**, sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="64fef-137">On the **Topic discovery** tab, under **Exclude topics**, select **Edit**.</span></span>
2. <span data-ttu-id="64fef-138">Cliquez **sur Exclure des rubriques par nom.**</span><span class="sxs-lookup"><span data-stu-id="64fef-138">Click **Exclude topics by name**.</span></span>
3. <span data-ttu-id="64fef-139">Si vous avez besoin de créer une liste, téléchargez le modèle .csv et ajoutez les rubriques que vous souhaitez exclure (voir Utiliser le modèle *.csv ci-dessous).*</span><span class="sxs-lookup"><span data-stu-id="64fef-139">If you need to create a list, download the .csv template and add the topics that you want to exclude (see *Working with the .csv template* below).</span></span> <span data-ttu-id="64fef-140">Lorsque le fichier est prêt, cliquez sur **Parcourir** et téléchargez le fichier.</span><span class="sxs-lookup"><span data-stu-id="64fef-140">When the file is ready, click **Browse** and upload the file.</span></span> <span data-ttu-id="64fef-141">S’il existe une liste, vous pouvez télécharger le .csv contenant la liste.</span><span class="sxs-lookup"><span data-stu-id="64fef-141">If there's an existing list, you can download the .csv containing the list.</span></span>
4. <span data-ttu-id="64fef-142">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="64fef-142">Click **Save**.</span></span>

    ![Capture d’écran de l’interface utilisateur exclure des rubriques](../media/km-manage-exclude-topics.png)

### <a name="working-with-the-csv-template"></a><span data-ttu-id="64fef-144">Utiliser le modèle .csv modèle</span><span class="sxs-lookup"><span data-stu-id="64fef-144">Working with the .csv template</span></span>

<span data-ttu-id="64fef-145">Vous pouvez copier le modèle csv ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="64fef-145">You can copy the csv template below:</span></span>

``` csv
Name (required),Expansion,MatchType- Exact/Partial (required)
```

<span data-ttu-id="64fef-146">Dans le modèle CSV, entrez les informations suivantes sur les rubriques à exclure :</span><span class="sxs-lookup"><span data-stu-id="64fef-146">In the CSV template, enter the following information about the topics you want to exclude:</span></span>

- <span data-ttu-id="64fef-147">**Nom** : tapez le nom de la rubrique à exclure.</span><span class="sxs-lookup"><span data-stu-id="64fef-147">**Name**: Type the name of the topic you want to exclude.</span></span> <span data-ttu-id="64fef-148">Il existe deux méthodes pour y parvenir :</span><span class="sxs-lookup"><span data-stu-id="64fef-148">There are two ways to do this:</span></span>
    - <span data-ttu-id="64fef-149">Correspondance exacte : vous pouvez exclure le nom exact ou l’acronyme (par exemple, *Contoso* ou *ATL*).</span><span class="sxs-lookup"><span data-stu-id="64fef-149">Exact match: You can exclude the exact name or acronym (for example, *Contoso* or *ATL*).</span></span>
    - <span data-ttu-id="64fef-150">Correspondance partielle : vous pouvez exclure toutes les rubriques qui ont un mot spécifique.</span><span class="sxs-lookup"><span data-stu-id="64fef-150">Partial match: You can exclude all topics that have a specific word in it.</span></span>  <span data-ttu-id="64fef-151">Par exemple, *arc exclura* toutes les rubriques avec le mot *arc* dans celui-ci, telles que le cercle *d’arc,* *l’arc de Pierre ou* *l’arc de formation*. Notez qu’il n’exclura pas les rubriques dans lesquelles le texte est inclus dans le cadre d’un mot, comme *Architecture*.</span><span class="sxs-lookup"><span data-stu-id="64fef-151">For example, *arc* will exclude all topics with the word *arc* in it, such as *Arc circle*, *Plasma arc welding*, or *Training arc*. Note that it will not exclude topics in which the text is included as part of a word, such as *Architecture*.</span></span>
- <span data-ttu-id="64fef-152">**Signifie (facultatif)**: si vous souhaitez exclure un acronyme, tapez les mots qu’il signifie.</span><span class="sxs-lookup"><span data-stu-id="64fef-152">**Stands for (optional)**: If you want to exclude an acronym, type the words the acronym stands for.</span></span>
- <span data-ttu-id="64fef-153">**MatchType-Exact/Partial**: tapez si le nom que vous avez entré était un type de correspondance *exacte* *ou* partielle.</span><span class="sxs-lookup"><span data-stu-id="64fef-153">**MatchType-Exact/Partial**: Type whether the name you entered was an *exact* or *partial* match type.</span></span>

    ![Exclure des rubriques dans le modèle CSV](../media/exclude-topics-csv.png) 

## <a name="see-also"></a><span data-ttu-id="64fef-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64fef-155">See also</span></span>

[<span data-ttu-id="64fef-156">Gérer la visibilité des rubriques dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="64fef-156">Manage topic visibility in Microsoft 365</span></span>](topic-experiences-knowledge-rules.md)

[<span data-ttu-id="64fef-157">Gérer les autorisations de rubrique dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="64fef-157">Manage topic permissions in Microsoft 365</span></span>](topic-experiences-user-permissions.md)

[<span data-ttu-id="64fef-158">Modifier le nom du centre de rubriques dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="64fef-158">Change the name of the topic center in Microsoft 365</span></span>](topic-experiences-administration.md)
