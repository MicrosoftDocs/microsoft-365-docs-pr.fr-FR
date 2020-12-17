---
title: Gestion de la découverte de rubrique dans Microsoft 365
ms.author: mikeplum
author: MikePlumleyMSFT
manager: serdars
ms.reviewer: nkokoye
audience: admin
ms.topic: article
ms.service: o365-administration
search.appverid: MET150
localization_priority: Normal
ROBOTS: NOINDEX, NOFOLLOW
description: Découvrez comment administrer la découverte de rubrique dans Microsoft 365.
ms.openlocfilehash: dec8aeef9dda390fb19f5067638c2ebea6b6a2fe
ms.sourcegitcommit: 884ac262443c50362d0c3ded961d36d6b15d8b73
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/16/2020
ms.locfileid: "49698542"
---
# <a name="manage-topic-discovery-in-microsoft-365"></a><span data-ttu-id="8d976-103">Gestion de la découverte de rubrique dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="8d976-103">Manage topic discovery in Microsoft 365</span></span>

<span data-ttu-id="8d976-104">Vous pouvez gérer les paramètres de découverte de rubrique dans le [Centre d’administration 365 de Microsoft](https://admin.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="8d976-104">You can manage topic discovery settings in the [Microsoft 365 admin center](https://admin.microsoft.com).</span></span> <span data-ttu-id="8d976-105">Vous devez être un administrateur général ou un administrateur SharePoint pour effectuer ces tâches.</span><span class="sxs-lookup"><span data-stu-id="8d976-105">You must be a global administrator or SharePoint administrator to perform these tasks.</span></span>

## <a name="to-access-topics-management-settings"></a><span data-ttu-id="8d976-106">Pour accéder aux paramètres de gestion des rubriques :</span><span class="sxs-lookup"><span data-stu-id="8d976-106">To access topics management settings:</span></span>

1. <span data-ttu-id="8d976-107">Dans le centre d’administration Microsoft 365, cliquez sur **paramètres**, puis sur paramètres de l' **organisation**.</span><span class="sxs-lookup"><span data-stu-id="8d976-107">In the Microsoft 365 admin center, click **Settings**, then **Org settings**.</span></span>
2. <span data-ttu-id="8d976-108">Sous l’onglet **services** , cliquez sur le **réseau de connaissances**.</span><span class="sxs-lookup"><span data-stu-id="8d976-108">On the **Services** tab, click **Knowledge network**.</span></span>

    ![Connecter des personnes aux connaissances](../media/admin-org-knowledge-options-completed.png) 

3. <span data-ttu-id="8d976-110">Sélectionnez l’onglet découverte de la **rubrique** . Consultez les sections suivantes pour obtenir des informations sur chaque paramètre.</span><span class="sxs-lookup"><span data-stu-id="8d976-110">Select the **Topic discovery** tab. See the following sections for information about each setting.</span></span>

    ![connaissances-réseau-paramètres](../media/knowledge-network-settings-topic-discovery.png) 

## <a name="select-sharepoint-topic-sources"></a><span data-ttu-id="8d976-112">Sélectionner les sources des rubriques SharePoint</span><span class="sxs-lookup"><span data-stu-id="8d976-112">Select SharePoint topic sources</span></span>

<span data-ttu-id="8d976-113">Vous pouvez modifier les sites SharePoint de votre organisation qui seront analysés pour rechercher des rubriques.</span><span class="sxs-lookup"><span data-stu-id="8d976-113">You can change the SharePoint sites in your organization that will be crawled for topics.</span></span>

<span data-ttu-id="8d976-114">Si vous souhaitez inclure ou exclure une liste de sites spécifique, vous pouvez utiliser le modèle. csv suivant :</span><span class="sxs-lookup"><span data-stu-id="8d976-114">If you want to include or exclude a specific list of sites, you can use the following .csv template:</span></span>

``` csv
Site name,URL
```

<span data-ttu-id="8d976-115">Si vous ajoutez des sites à l’aide du sélecteur de site, ils sont ajoutés à la liste de sites existante à inclure ou à exclure.</span><span class="sxs-lookup"><span data-stu-id="8d976-115">If you add sites using the site picker, they are added to the existing list of sites to include or exclude.</span></span> <span data-ttu-id="8d976-116">Si vous téléchargez un fichier. csv, il remplace toutes les listes existantes.</span><span class="sxs-lookup"><span data-stu-id="8d976-116">If you upload a .csv file, it overwrites any existing list.</span></span> <span data-ttu-id="8d976-117">Si vous avez déjà inclus ou exclu des sites spécifiques, vous devez télécharger la liste en tant que fichier. csv, les modifier et télécharger la nouvelle liste.</span><span class="sxs-lookup"><span data-stu-id="8d976-117">If you have previously included or excluded specific sites, you and download the list as a .csv file, make changes, and upload the new list.</span></span>

<span data-ttu-id="8d976-118">Pour choisir les sites pour la découverte de rubrique</span><span class="sxs-lookup"><span data-stu-id="8d976-118">To choose sites for topic discovery</span></span>

1. <span data-ttu-id="8d976-119">Sous l’onglet découverte de la **rubrique** , sous sélectionner les **sources des rubriques SharePoint**, sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="8d976-119">On the **Topic discovery** tab, under **Select SharePoint topic sources**, select **Edit**.</span></span>
2. <span data-ttu-id="8d976-120">Sur la page **Sélectionner les sources des rubriques SharePoint** , sélectionnez les sites SharePoint qui seront analysés en tant que sources pour vos rubriques lors de la découverte.</span><span class="sxs-lookup"><span data-stu-id="8d976-120">On the **Select SharePoint topic sources** page, select which SharePoint sites will be crawled as sources for your topics during discovery.</span></span> <span data-ttu-id="8d976-121">Cela inclut les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="8d976-121">This includes:</span></span>
    - <span data-ttu-id="8d976-122">**Tous les sites**: tous les sites SharePoint de votre client.</span><span class="sxs-lookup"><span data-stu-id="8d976-122">**All sites**: All SharePoint sites in your tenant.</span></span> <span data-ttu-id="8d976-123">Ceci capture les sites actuels et futurs.</span><span class="sxs-lookup"><span data-stu-id="8d976-123">This captures current and future sites.</span></span>
    - <span data-ttu-id="8d976-124">**Tout, à l’exception des sites sélectionnés**: saisissez les noms des sites à exclure.</span><span class="sxs-lookup"><span data-stu-id="8d976-124">**All, except selected sites**: Type the names of the sites you want to exclude.</span></span>  <span data-ttu-id="8d976-125">Vous pouvez également télécharger une liste de sites que vous souhaitez exclure de la découverte.</span><span class="sxs-lookup"><span data-stu-id="8d976-125">You can also upload a list of sites you want to opt out from discovery.</span></span> <span data-ttu-id="8d976-126">Les sites créés à l’avenir seront inclus en tant que sources pour la découverte de rubriques.</span><span class="sxs-lookup"><span data-stu-id="8d976-126">Sites created in the future will be included as sources for topic discovery.</span></span> 
    - <span data-ttu-id="8d976-127">**Sites sélectionnés uniquement**: saisissez les noms des sites que vous souhaitez inclure.</span><span class="sxs-lookup"><span data-stu-id="8d976-127">**Only selected sites**: Type the names of the sites you want to include.</span></span> <span data-ttu-id="8d976-128">Vous pouvez également télécharger une liste de sites.</span><span class="sxs-lookup"><span data-stu-id="8d976-128">You can also upload a list of sites.</span></span> <span data-ttu-id="8d976-129">Les sites créés à l’avenir ne seront pas inclus en tant que sources pour la découverte des rubriques.</span><span class="sxs-lookup"><span data-stu-id="8d976-129">Sites created in the future will not be included as sources for topic discovery.</span></span>
    - <span data-ttu-id="8d976-130">**Aucun site**: les rubriques ne seront pas générées ni mises à jour automatiquement avec le contenu SharePoint.</span><span class="sxs-lookup"><span data-stu-id="8d976-130">**No sites**: Topics won't be automatically generated or updated with SharePoint content.</span></span> <span data-ttu-id="8d976-131">Les rubriques existantes restent dans le centre de la rubrique.</span><span class="sxs-lookup"><span data-stu-id="8d976-131">Existing topics remain in the topic center.</span></span>

    ![Capture d’écran de l’interface utilisateur des sources de rubrique SharePoint](../media/k-manage-select-topic-source.png)
   
3. <span data-ttu-id="8d976-133">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="8d976-133">Click **Save**.</span></span>

## <a name="exclude-topics-by-name"></a><span data-ttu-id="8d976-134">Exclure les rubriques par nom</span><span class="sxs-lookup"><span data-stu-id="8d976-134">Exclude topics by name</span></span>

<span data-ttu-id="8d976-135">Vous pouvez exclure des rubriques de la découverte en téléchargeant une liste à l’aide d’un fichier. csv.</span><span class="sxs-lookup"><span data-stu-id="8d976-135">You can exclude topics from discovery by uploading a list using a .csv file.</span></span> <span data-ttu-id="8d976-136">Si vous avez déjà exclu des rubriques, vous pouvez télécharger le fichier. csv, le modifier et le charger à nouveau.</span><span class="sxs-lookup"><span data-stu-id="8d976-136">If you've previously excluded topics, you can download the .csv, make changes, and upload it again.</span></span>

1. <span data-ttu-id="8d976-137">Sous l’onglet **découverte de rubrique** , sous exclure des **rubriques**, sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="8d976-137">On the **Topic discovery** tab, under **Exclude topics**, select **Edit**.</span></span>
2. <span data-ttu-id="8d976-138">Cliquez sur **exclure des rubriques par nom**.</span><span class="sxs-lookup"><span data-stu-id="8d976-138">Click **Exclude topics by name**.</span></span>
3. <span data-ttu-id="8d976-139">Si vous devez créer une liste, téléchargez le modèle. csv et ajoutez les rubriques à exclure (voir *utilisation du modèle. csv* ci-dessous).</span><span class="sxs-lookup"><span data-stu-id="8d976-139">If you need to create a list, download the .csv template and add the topics that you want to exclude (see *Working with the .csv template* below).</span></span> <span data-ttu-id="8d976-140">Lorsque le fichier est prêt, cliquez sur **Parcourir** et téléchargez le fichier.</span><span class="sxs-lookup"><span data-stu-id="8d976-140">When the file is ready, click **Browse** and upload the file.</span></span> <span data-ttu-id="8d976-141">S’il existe une liste existante, vous pouvez télécharger le fichier. csv contenant la liste.</span><span class="sxs-lookup"><span data-stu-id="8d976-141">If there's an existing list, you can download the .csv containing the list.</span></span>
4. <span data-ttu-id="8d976-142">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="8d976-142">Click **Save**.</span></span>

    ![Capture d’écran de l’interface utilisateur exclure des rubriques](../media/km-manage-exclude-topics.png)

### <a name="working-with-the-csv-template"></a><span data-ttu-id="8d976-144">Utilisation du modèle. csv</span><span class="sxs-lookup"><span data-stu-id="8d976-144">Working with the .csv template</span></span>

<span data-ttu-id="8d976-145">Vous pouvez copier le modèle CSV ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="8d976-145">You can copy the csv template below:</span></span>

``` csv
Name (required),Expansion,MatchType- Exact/Partial (required)
```

<span data-ttu-id="8d976-146">Dans le modèle CSV, entrez les informations suivantes sur les rubriques à exclure :</span><span class="sxs-lookup"><span data-stu-id="8d976-146">In the CSV template, enter the following information about the topics you want to exclude:</span></span>

- <span data-ttu-id="8d976-147">**Nom**: tapez le nom de la rubrique à exclure.</span><span class="sxs-lookup"><span data-stu-id="8d976-147">**Name**: Type the name of the topic you want to exclude.</span></span> <span data-ttu-id="8d976-148">Vous pouvez procéder de deux manières :</span><span class="sxs-lookup"><span data-stu-id="8d976-148">There are two ways to do this:</span></span>
    - <span data-ttu-id="8d976-149">Correspondance exacte : vous pouvez inclure le nom exact ou un acronyme (par exemple, *contoso* ou *ATL*).</span><span class="sxs-lookup"><span data-stu-id="8d976-149">Exact match: You can include the exact name or acronym (for example, *Contoso* or *ATL*).</span></span>
    - <span data-ttu-id="8d976-150">Correspondance partielle : vous pouvez exclure toutes les rubriques qui contiennent un mot spécifique.</span><span class="sxs-lookup"><span data-stu-id="8d976-150">Partial match: You can exclude all topics that have a specific word in it.</span></span>  <span data-ttu-id="8d976-151">Par exemple, *arc* exclut toutes les rubriques contenant le mot *arc* , comme un *cercle arc*, un *soudage* à l’arc de plasma ou un *arc de formation*. Notez qu’il n’exclura pas les rubriques dans lesquelles le texte est inclus dans un mot, tel que *architecture*.</span><span class="sxs-lookup"><span data-stu-id="8d976-151">For example, *arc* will exclude all topics with the word *arc* in it, such as *Arc circle*, *Plasma arc welding*, or *Training arc*. Note that it will not exclude topics in which the text is included as part of a word, such as *Architecture*.</span></span>
- <span data-ttu-id="8d976-152">**Abréviation de (facultatif)**: Si vous souhaitez exclure un acronyme, tapez les mots de l’acronyme.</span><span class="sxs-lookup"><span data-stu-id="8d976-152">**Stands for (optional)**: If you want to exclude an acronym, type the words the acronym stands for.</span></span>
- <span data-ttu-id="8d976-153">**MatchType-exacte/partielle**: spécifiez si le nom que vous avez entré est un type de correspondance *exacte* ou *partielle* .</span><span class="sxs-lookup"><span data-stu-id="8d976-153">**MatchType-Exact/Partial**: Type whether the name you entered was an *exact* or *partial* match type.</span></span>

    ![Exclure les rubriques du modèle CSV](../media/exclude-topics-csv.png) 

## <a name="see-also"></a><span data-ttu-id="8d976-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d976-155">See also</span></span>

[<span data-ttu-id="8d976-156">Gestion de la visibilité des rubriques dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="8d976-156">Manage topic visibility in Microsoft 365</span></span>](topic-experiences-knowledge-rules.md)

[<span data-ttu-id="8d976-157">Gérer les autorisations de rubrique dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="8d976-157">Manage topic permissions in Microsoft 365</span></span>](topic-experiences-user-permissions.md)

[<span data-ttu-id="8d976-158">Modifier le nom du centre de rubrique dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="8d976-158">Change the name of the topic center in Microsoft 365</span></span>](topic-experiences-administration.md)
