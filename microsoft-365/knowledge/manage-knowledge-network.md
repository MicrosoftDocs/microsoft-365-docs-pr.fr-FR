---
title: 'Gérer votre réseau de gestion des connaissances (aperçu) '
description: La configuration de la gestion des connaissances ;
author: efrene
ms.author: efrene
manager: pamgreen
ms.date: 08/01/2020
audience: admin
ms.topic: article
ms.service: ''
search.appverid: ''
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: Normal
ms.openlocfilehash: 87275dba78ab402a9ea9553198ce1a84072e3351
ms.sourcegitcommit: 3a47efcbdf3d2b39caa2798ea5be806839b05ed1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/01/2020
ms.locfileid: "46540117"
---
# <a name="manage-your-knowledge-management-network-preview"></a><span data-ttu-id="3bb54-103">Gérer votre réseau de gestion des connaissances (aperçu)</span><span class="sxs-lookup"><span data-stu-id="3bb54-103">Manage your knowledge management network (Preview)</span></span>

> [!Note] 
> <span data-ttu-id="3bb54-104">Le contenu de cet article est destiné à Project cortex privé preview.</span><span class="sxs-lookup"><span data-stu-id="3bb54-104">The content in this article is for Project Cortex Private Preview.</span></span> <span data-ttu-id="3bb54-105">Pour [plus d’informations sur le projet cortex](https://aka.ms/projectcortex).</span><span class="sxs-lookup"><span data-stu-id="3bb54-105">[Find out more about Project Cortex](https://aka.ms/projectcortex).</span></span>


<span data-ttu-id="3bb54-106">Une fois que vous avez [configuré la gestion des connaissances](set-up-knowledge-network.md), un administrateur peut à tout moment apporter des modifications à vos paramètres de configuration via le centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="3bb54-106">After you [set up knowledge management](set-up-knowledge-network.md), at any time afterwards an admin can make adjustments to your configuration settings through the Microsoft 365 admin center.</span></span>

<span data-ttu-id="3bb54-107">Par exemple, vous devrez peut-être ajuster vos paramètres pour l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="3bb54-107">For example, you may need to adjust your settings for any of the following:</span></span>
- <span data-ttu-id="3bb54-108">Ajoutez de nouvelles sources SharePoint aux rubriques de la mienne.</span><span class="sxs-lookup"><span data-stu-id="3bb54-108">Add new SharePoint sources to mine topics.</span></span>
- <span data-ttu-id="3bb54-109">Modifier les utilisateurs qui auront accès aux rubriques.</span><span class="sxs-lookup"><span data-stu-id="3bb54-109">Change which users will have access to topics.</span></span>
- <span data-ttu-id="3bb54-110">Modifier les utilisateurs qui disposent des autorisations pour effectuer des tâches dans le Centre des rubriques.</span><span class="sxs-lookup"><span data-stu-id="3bb54-110">Change which users have permissions to do tasks on the topic center.</span></span>
- <span data-ttu-id="3bb54-111">Modifier le nom de votre centre de rubrique</span><span class="sxs-lookup"><span data-stu-id="3bb54-111">Change the name of your topic center</span></span>


## <a name="requirements"></a><span data-ttu-id="3bb54-112">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="3bb54-112">Requirements</span></span> 
<span data-ttu-id="3bb54-113">Vous devez disposer d’autorisations d’administrateur général ou d’administrateur SharePoint pour pouvoir accéder au centre d’administration Microsoft 365 et gérer les tâches des connaissances de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="3bb54-113">You must have Global Admin or SharePoint admin permissions to be able to access the Microsoft 365 admin center and manage Organizational knowledge tasks.</span></span>


## <a name="to-access-knowledge-management-settings"></a><span data-ttu-id="3bb54-114">Pour accéder aux paramètres de gestion des connaissances :</span><span class="sxs-lookup"><span data-stu-id="3bb54-114">To access knowledge management settings:</span></span>

1. <span data-ttu-id="3bb54-115">Dans le centre d’administration 365 de Microsoft, sélectionnez **configuration**, puis affichez la section connaissances de l' **organisation** .</span><span class="sxs-lookup"><span data-stu-id="3bb54-115">In the Microsoft 365 admin center, select **Setup**, and then view the **Organizational Knowledge** section.</span></span>
2. <span data-ttu-id="3bb54-116">Dans la section connaissances de l' **organisation** , cliquez sur **connecter les personnes aux connaissances**.</span><span class="sxs-lookup"><span data-stu-id="3bb54-116">In the **Organizational Knowledge** section, click **Connect people to knowledge**.</span></span><br/>

    ![Connecter des personnes aux connaissances](../media/content-understanding/admin-org-knowledge-options.png) </br>

3. <span data-ttu-id="3bb54-118">Sur la page **connecter des personnes à la page de connaissances** , sélectionnez **gérer** pour ouvrir le volet Paramètres du **réseau de connaissances** .</span><span class="sxs-lookup"><span data-stu-id="3bb54-118">On the **Connect people to knowledge** page, select **Manage** to open the **Knowledge network settings** pane.</span></span><br/>

    ![connaissances-réseau-paramètres](../media/content-understanding/knowledge-network-settings.png) </br>

## <a name="change-how-the-knowledge-network-can-find-topics"></a><span data-ttu-id="3bb54-120">Modifier la façon dont le réseau Knowledge peut trouver des rubriques</span><span class="sxs-lookup"><span data-stu-id="3bb54-120">Change how the knowledge network can find topics</span></span>

<span data-ttu-id="3bb54-121">Sélectionnez l’onglet **découverte de rubrique** si vous souhaitez mettre à jour vos choix pour les sources de rubrique SharePoint.</span><span class="sxs-lookup"><span data-stu-id="3bb54-121">Select the **Topic discovery** tab if you want to update your choices for  for SharePoint topic sources.</span></span> <span data-ttu-id="3bb54-122">Ce paramètre vous permet de sélectionner les sites SharePoint de votre client qui seront analysés et extraits de rubriques.</span><span class="sxs-lookup"><span data-stu-id="3bb54-122">This setting let you select the SharePoint sites in your tenant that will be crawled and mined for topics.</span></span>

1. <span data-ttu-id="3bb54-123">Sous l’onglet découverte de la **rubrique** , sous sélectionner les **sources des rubriques SharePoint**, sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="3bb54-123">On the **Topic discovery** tab, under **Select SharePoint topic sources**, select **Edit**.</span></span>
2. <span data-ttu-id="3bb54-124">Sur la page **Sélectionner les sources des rubriques SharePoint** , sélectionnez les sites SharePoint qui seront analysés en tant que sources pour vos rubriques lors de la découverte.</span><span class="sxs-lookup"><span data-stu-id="3bb54-124">On the **Select SharePoint topic sources** page, select which SharePoint sites will be crawled as sources for your topics during discovery.</span></span> <span data-ttu-id="3bb54-125">Cela inclut les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="3bb54-125">This includes:</span></span></br>
    <span data-ttu-id="3bb54-126">a.</span><span class="sxs-lookup"><span data-stu-id="3bb54-126">a.</span></span> <span data-ttu-id="3bb54-127">**Tous les sites**: tous les sites SharePoint de votre client.</span><span class="sxs-lookup"><span data-stu-id="3bb54-127">**All sites**: All SharePoint sites in your tenant.</span></span> <span data-ttu-id="3bb54-128">Ceci capture les sites actuels et futurs.</span><span class="sxs-lookup"><span data-stu-id="3bb54-128">This captures current and future sites.</span></span></br>
    <span data-ttu-id="3bb54-129">b.</span><span class="sxs-lookup"><span data-stu-id="3bb54-129">b.</span></span> <span data-ttu-id="3bb54-130">**Tout, à l’exception des sites sélectionnés**: saisissez les noms des sites à exclure.</span><span class="sxs-lookup"><span data-stu-id="3bb54-130">**All, except selected sites**: Type the names of the sites you want to exclude.</span></span>  <span data-ttu-id="3bb54-131">Vous pouvez également télécharger une liste de sites que vous souhaitez exclure de la découverte.</span><span class="sxs-lookup"><span data-stu-id="3bb54-131">You can also upload a list of sites you want to opt out from discovery.</span></span> <span data-ttu-id="3bb54-132">Les sites créés à l’avenir seront inclus en tant que sources pour la découverte de rubriques.</span><span class="sxs-lookup"><span data-stu-id="3bb54-132">Sites created in the future will be included as sources for topic discovery.</span></span> </br>
    <span data-ttu-id="3bb54-133">c.</span><span class="sxs-lookup"><span data-stu-id="3bb54-133">c.</span></span> <span data-ttu-id="3bb54-134">**Sites sélectionnés uniquement**: saisissez les noms des sites que vous souhaitez inclure.</span><span class="sxs-lookup"><span data-stu-id="3bb54-134">**Only selected sites**: Type the names of the sites you want to include.</span></span> <span data-ttu-id="3bb54-135">Vous pouvez également télécharger une liste de sites.</span><span class="sxs-lookup"><span data-stu-id="3bb54-135">You can also upload a list of sites.</span></span> <span data-ttu-id="3bb54-136">Les sites créés à l’avenir ne seront pas inclus en tant que sources pour la découverte des rubriques.</span><span class="sxs-lookup"><span data-stu-id="3bb54-136">Sites created in the future will not be included as sources for topic discovery.</span></span> </br>

    ![Choisir comment rechercher des rubriques](../media/content-understanding/k-manage-select-topic-source.png) </br>
   
    <span data-ttu-id="3bb54-138">Si vous avez un certain nombre de sites à exclure (si vous sélectionnez **tous, sauf sites sélectionnés**) ou inclure (si vous avez sélectionné **uniquement les sites sélectionnés**), vous pouvez choisir de télécharger un fichier CSV avec les noms de site et les URL.</span><span class="sxs-lookup"><span data-stu-id="3bb54-138">If you have a number of sites that you want to exclude (if you select **All, except selected sites**) or include (if you selected **Only selected sites**), you can choose to upload a CSV file with the site names and URLs.</span></span> <span data-ttu-id="3bb54-139">Vous pouvez sélectionner **Télécharger le modèle de site. csv** si vous voulez utiliser le fichier de modèle CSV.</span><span class="sxs-lookup"><span data-stu-id="3bb54-139">You can select **Download site template .csv** if you want to use the CSV template file.</span></span>

3. <span data-ttu-id="3bb54-140">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="3bb54-140">Select **Save**.</span></span>

##  <a name="change-who-can-see-topics-in-your-organization"></a><span data-ttu-id="3bb54-141">Modifier les personnes qui peuvent voir les rubriques de votre organisation</span><span class="sxs-lookup"><span data-stu-id="3bb54-141">Change who can see topics in your organization</span></span>

<span data-ttu-id="3bb54-142">Sélectionnez l’onglet découverte de la **rubrique** si vous souhaitez mettre à jour les personnes de votre organisation qui peuvent voir les rubriques découvertes dans les résultats de la recherche et quand les rubriques sont mises en surbrillance dans le contenu comme les pages SharePoint.</span><span class="sxs-lookup"><span data-stu-id="3bb54-142">Select the **Topic discovery** tab if you want to update who in your organization can see discovered topics in search results and when topics are highlighted in content like SharePoint pages.</span></span>

1. <span data-ttu-id="3bb54-143">Sous l’onglet **découverte de rubrique** , sous **qui peut voir les rubriques dans le réseau de connaissances**, sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="3bb54-143">On the **Topic discovery** tab, under **Who can see topics in the knowledge network**, select **Edit**.</span></span>
2. <span data-ttu-id="3bb54-144">Sur la page **qui peut voir les rubriques de la page du réseau de connaissances** , vous sélectionnez les utilisateurs qui auront accès aux détails de la rubrique, comme les rubriques mises en surbrillance, les fiches de rubrique, les réponses aux questions dans la recherche et les pages de rubrique.</span><span class="sxs-lookup"><span data-stu-id="3bb54-144">On the **Who can see topics in the knowledge network** page, you choose who will have access to topic details, such as highlighted topics, topic cards, topic answers in search, and topic pages.</span></span> <span data-ttu-id="3bb54-145">Vous pouvez sélectionner :</span><span class="sxs-lookup"><span data-stu-id="3bb54-145">You can select:</span></span></br>
    <span data-ttu-id="3bb54-146">a.</span><span class="sxs-lookup"><span data-stu-id="3bb54-146">a.</span></span> <span data-ttu-id="3bb54-147">**Tout le monde dans votre organisation**</span><span class="sxs-lookup"><span data-stu-id="3bb54-147">**Everyone in your organization**</span></span></br>
    <span data-ttu-id="3bb54-148">b.</span><span class="sxs-lookup"><span data-stu-id="3bb54-148">b.</span></span> <span data-ttu-id="3bb54-149">**Uniquement les personnes ou les groupes de sécurité sélectionnés**</span><span class="sxs-lookup"><span data-stu-id="3bb54-149">**Only selected people or security groups**</span></span></br>
    <span data-ttu-id="3bb54-150">c.</span><span class="sxs-lookup"><span data-stu-id="3bb54-150">c.</span></span> <span data-ttu-id="3bb54-151">**Personne**</span><span class="sxs-lookup"><span data-stu-id="3bb54-151">**No one**</span></span></br>

    ![Qui peut voir les rubriques](../media/content-understanding/k-manage-who-can-see-topics.png) </br> 
3. <span data-ttu-id="3bb54-153">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="3bb54-153">Select **Save**.</span></span>  
 
> [!Note] 
> <span data-ttu-id="3bb54-154">Bien que ce paramètre vous permette de sélectionner un utilisateur au sein de votre organisation, seuls les utilisateurs qui disposent de licences de gestion des connaissances qui lui sont attribués pourront consulter les rubriques.</span><span class="sxs-lookup"><span data-stu-id="3bb54-154">While this setting allows you to select any user in your organization, only users who have knowledge management licenses assigned to them will be able to view topics.</span></span>

## <a name="change-who-has-permissions-to-do-tasks-on-the-topic-center"></a><span data-ttu-id="3bb54-155">Modifier la personne qui dispose des autorisations pour effectuer des tâches dans le centre de la rubrique</span><span class="sxs-lookup"><span data-stu-id="3bb54-155">Change who has permissions to do tasks on the topic center</span></span>

<span data-ttu-id="3bb54-156">Sélectionnez l’onglet Autorisations de la **rubrique** si vous souhaitez mettre à jour les personnes autorisées à effectuer les opérations suivantes dans la page du Centre des rubriques :</span><span class="sxs-lookup"><span data-stu-id="3bb54-156">Select the **Topic permissions** tab if you want to update who has permissions to do the following in the topic center page:</span></span>

- <span data-ttu-id="3bb54-157">Les utilisateurs qui peuvent créer et modifier des rubriques : créer des rubriques introuvables lors de la découverte ou modifier les détails d’une page de rubrique existante.</span><span class="sxs-lookup"><span data-stu-id="3bb54-157">Which users can create and edit topics: Create new topics that were not found during discovery or edit existing topic page details.</span></span>
- <span data-ttu-id="3bb54-158">Les utilisateurs qui peuvent gérer les rubriques : confirmer ou rejeter les rubriques découvertes.</span><span class="sxs-lookup"><span data-stu-id="3bb54-158">Which users can manage topics: Confirm or reject discovered topics.</span></span>

<span data-ttu-id="3bb54-159">Pour mettre à jour les utilisateurs disposant des autorisations permettant de créer et de modifier des rubriques :</span><span class="sxs-lookup"><span data-stu-id="3bb54-159">To update who has permissions to create and edit topics:</span></span>

1. <span data-ttu-id="3bb54-160">Sous l’onglet **autorisations de rubrique** , sous **qui peut créer et modifier des rubriques**, sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="3bb54-160">On the **Topic permissions** tab, under **Who can create and edit topics**, select **Edit**.</span></span></br>
2. <span data-ttu-id="3bb54-161">Sur la page **qui peut créer et modifier des rubriques** , vous pouvez sélectionner :</span><span class="sxs-lookup"><span data-stu-id="3bb54-161">On the **Who can create and edit topics** page, you can select:</span></span></br>
    <span data-ttu-id="3bb54-162">a.</span><span class="sxs-lookup"><span data-stu-id="3bb54-162">a.</span></span> <span data-ttu-id="3bb54-163">**Tout le monde dans votre organisation**</span><span class="sxs-lookup"><span data-stu-id="3bb54-163">**Everyone in your organization**</span></span></br>
    <span data-ttu-id="3bb54-164">b.</span><span class="sxs-lookup"><span data-stu-id="3bb54-164">b.</span></span> <span data-ttu-id="3bb54-165">**Uniquement les personnes ou les groupes de sécurité sélectionnés**</span><span class="sxs-lookup"><span data-stu-id="3bb54-165">**Only selected people or security groups**</span></span></br>

    ![Créer et modifier des rubriques](../media/content-understanding/k-manage-who-can-create-and-edit.png) </br> 

3. <span data-ttu-id="3bb54-167">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="3bb54-167">Select **Save**.</span></span></br>

<span data-ttu-id="3bb54-168">Pour mettre à jour les personnes autorisées à gérer les rubriques, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="3bb54-168">To update who has permissions to manage topics:</span></span>

1. <span data-ttu-id="3bb54-169">Sous l’onglet **autorisations de rubrique** , sous **qui peut gérer les rubriques**, sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="3bb54-169">On the **Topic permissions** tab, under **Who can manage topics**, select **Edit**.</span></span></br>
2. <span data-ttu-id="3bb54-170">Sur la page **qui peut gérer les rubriques** , vous pouvez sélectionner les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="3bb54-170">On the **Who can manage topics** page, you can select:</span></span></br>
    <span data-ttu-id="3bb54-171">a.</span><span class="sxs-lookup"><span data-stu-id="3bb54-171">a.</span></span> <span data-ttu-id="3bb54-172">**Tout le monde dans votre organisation**</span><span class="sxs-lookup"><span data-stu-id="3bb54-172">**Everyone in your organization**</span></span></br>
    <span data-ttu-id="3bb54-173">b.</span><span class="sxs-lookup"><span data-stu-id="3bb54-173">b.</span></span> <span data-ttu-id="3bb54-174">**Personnes ou groupes de sécurité sélectionnés**</span><span class="sxs-lookup"><span data-stu-id="3bb54-174">**Selected people or security groups**</span></span></br>

    ![Gérer les rubriques](../media/content-understanding/k-manage-who-can-manage-topics.png) </br> 

3. <span data-ttu-id="3bb54-176">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="3bb54-176">Select **Save**.</span></span></br>


##  <a name="update-your-topic-center-name"></a><span data-ttu-id="3bb54-177">Mettre à jour le nom du centre de rubrique</span><span class="sxs-lookup"><span data-stu-id="3bb54-177">Update your topic center name</span></span>

<span data-ttu-id="3bb54-178">Sélectionnez l’onglet **Centre des rubriques** si vous souhaitez mettre à jour le nom de votre centre de rubriques.</span><span class="sxs-lookup"><span data-stu-id="3bb54-178">Select the **Topic center** tab if you want to update the name of your topic center.</span></span> 

1. <span data-ttu-id="3bb54-179">Sous l’onglet **Centre des rubriques** , sous nom du centre de **rubriques**, sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="3bb54-179">On the **Topic center** tab, under **Topic center name**, select **Edit**.</span></span>
2. <span data-ttu-id="3bb54-180">Dans la page **modifier le nom du centre de rubrique** , dans la zone Nom du centre de la **rubrique** , tapez le nouveau nom de votre centre de rubrique.</span><span class="sxs-lookup"><span data-stu-id="3bb54-180">On the **Edit topic center name** page, in the **Topic center name** box, type the new name for your topic center.</span></span>
3. <span data-ttu-id="3bb54-181">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="3bb54-181">Select **Save**</span></span>

    ![Modifier le nom du centre de rubriques](../media/content-understanding/manage-topic-center-name.png) </br> 











## <a name="see-also"></a><span data-ttu-id="3bb54-183">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3bb54-183">See also</span></span>



  






