---
title: 'Configurer la gestion des connaissances (aperçu) '
description: La configuration de la gestion des connaissances ;
author: efrene
ms.author: efrene
manager: pamgreen
ms.date: 8/1/2020
audience: admin
ms.topic: article
ms.service: ''
search.appverid: ''
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: None
ms.openlocfilehash: ba8cb8ceb3c98019099bfe5438d274c9d2b32280
ms.sourcegitcommit: a3a5dc541b0c971608cc86ef480509c25a13ca60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/10/2020
ms.locfileid: "46612547"
---
# <a name="set-up-knowledge-management-preview"></a><span data-ttu-id="e19dc-103">Configurer la gestion des connaissances (aperçu)</span><span class="sxs-lookup"><span data-stu-id="e19dc-103">Set up Knowledge Management (Preview)</span></span>

> [!Note] 
> <span data-ttu-id="e19dc-104">Le contenu de cet article est destiné à Project cortex privé preview.</span><span class="sxs-lookup"><span data-stu-id="e19dc-104">The content in this article is for Project Cortex Private Preview.</span></span> <span data-ttu-id="e19dc-105">Pour [plus d’informations sur le projet cortex](https://aka.ms/projectcortex).</span><span class="sxs-lookup"><span data-stu-id="e19dc-105">[Find out more about Project Cortex](https://aka.ms/projectcortex).</span></span>

<span data-ttu-id="e19dc-106">Vous pouvez utiliser le centre d’administration Microsoft 365 pour installer et configurer la [gestion des connaissances](knowledge-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e19dc-106">You can use the Microsoft 365 admin center to set up and configure [Knowledge Management](knowledge-management-overview.md).</span></span> 

> [!Important]
> <span data-ttu-id="e19dc-107">Il est important de planifier la meilleure façon de configurer et de configurer la gestion des connaissances dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="e19dc-107">It is important to plan the best way to set up and configure Knowledge Management in your environment.</span></span> <span data-ttu-id="e19dc-108">Par exemple, vous devez prendre en compte les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="e19dc-108">For example, you will need to make considerations about the following:</span></span>
- <span data-ttu-id="e19dc-109">Les sites SharePoint que vous souhaitez analyser pour les rubriques.</span><span class="sxs-lookup"><span data-stu-id="e19dc-109">Which SharePoint sites you want to analyze for topics.</span></span>
- <span data-ttu-id="e19dc-110">Les utilisateurs auxquels vous souhaitez faire apparaître les rubriques.</span><span class="sxs-lookup"><span data-stu-id="e19dc-110">Which users you want to make topics visible to.</span></span>
- <span data-ttu-id="e19dc-111">Les utilisateurs auxquels vous souhaitez accorder des autorisations pour gérer les rubriques dans le Centre des rubriques.</span><span class="sxs-lookup"><span data-stu-id="e19dc-111">Which users you want to give permissions to manage topics in the topic center.</span></span>
- <span data-ttu-id="e19dc-112">Les utilisateurs auxquels vous souhaitez accorder des autorisations pour créer ou modifier des rubriques dans le Centre des rubriques.</span><span class="sxs-lookup"><span data-stu-id="e19dc-112">Which users you want to give permissions to create or edit topics in the topic center.</span></span>
- <span data-ttu-id="e19dc-113">Le nom que vous souhaitez donner à votre centre de sujets.</span><span class="sxs-lookup"><span data-stu-id="e19dc-113">What name you want to give your topic center.</span></span>

> [!Note]
> <span data-ttu-id="e19dc-114">Il peut s’avérer utile de créer des groupes de sécurité pour attribuer aux utilisateurs les autorisations nécessaires pour afficher des rubriques, gérer des rubriques et créer et modifier des rubriques.</span><span class="sxs-lookup"><span data-stu-id="e19dc-114">You may find it useful to create security groups to assign your users the permissions needed to view topics, manage topic, and create and edit topics.</span></span>

<span data-ttu-id="e19dc-115">Un administrateur peut également [modifier les paramètres sélectionnés à tout moment après l’installation](manage-knowledge-network.md) via les paramètres de gestion des connaissances dans le centre d’administration 365 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e19dc-115">An admin can also [make changes to your selected settings anytime after setup](manage-knowledge-network.md) through the Knowledge Management settings in the Microsoft 365 admin center.</span></span>

## <a name="requirements"></a><span data-ttu-id="e19dc-116">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="e19dc-116">Requirements</span></span> 
<span data-ttu-id="e19dc-117">Vous devez disposer d’autorisations d’administrateur général ou d’administrateur SharePoint pour pouvoir accéder au centre d’administration Microsoft 365 et configurer des tâches de connaissances organisationnelles.</span><span class="sxs-lookup"><span data-stu-id="e19dc-117">You must have Global Admin or SharePoint admin permissions to be able to access the Microsoft 365 admin center and set up Organizational knowledge tasks.</span></span>

## <a name="set-up-your-knowledge-network"></a><span data-ttu-id="e19dc-118">Configurer votre réseau de connaissances</span><span class="sxs-lookup"><span data-stu-id="e19dc-118">Set up your knowledge network</span></span>

<span data-ttu-id="e19dc-119">La configuration de votre réseau de connaissances vous guide tout au long des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="e19dc-119">Setting up your knowledge network walks you through the following:</span></span>

- <span data-ttu-id="e19dc-120">Découverte de rubrique : sélection des sources de rubrique et des rubriques à exclure de la découverte.</span><span class="sxs-lookup"><span data-stu-id="e19dc-120">Topic discovery: Selecting topic sources and topics to  exclude from discovery.</span></span>
- <span data-ttu-id="e19dc-121">Visibilité de rubrique : sélection des personnes qui peuvent afficher les rubriques sous forme de mises en surbrillance dans les pages de recherche et de rubrique.</span><span class="sxs-lookup"><span data-stu-id="e19dc-121">Topic visibility: Selecting who can view topics as highlights, in search and topic pages.</span></span>
- <span data-ttu-id="e19dc-122">Autorisations de rubrique : sélection des personnes qui peuvent créer, modifier et gérer des rubriques.</span><span class="sxs-lookup"><span data-stu-id="e19dc-122">Topic permissions: Selecting who can create, edit, and manage topics.</span></span>
- <span data-ttu-id="e19dc-123">Centre des rubriques : créez votre centre de rubriques.</span><span class="sxs-lookup"><span data-stu-id="e19dc-123">Topic center: Create your topic center.</span></span>
- <span data-ttu-id="e19dc-124">Révision : Vérifiez et appliquez vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="e19dc-124">Review: Check and apply your settings.</span></span>

<span data-ttu-id="e19dc-125">Pour configurer votre réseau de connaissances :</span><span class="sxs-lookup"><span data-stu-id="e19dc-125">To set up your knowledge network:</span></span>

1. <span data-ttu-id="e19dc-126">Dans le centre d’administration 365 de Microsoft (admin.microsoft.com), sélectionnez **configuration**, puis affichez la section connaissances de l' **organisation** .</span><span class="sxs-lookup"><span data-stu-id="e19dc-126">In the Microsoft 365 admin center (admin.microsoft.com), select **Setup**, and then view the **Organizational Knowledge** section.</span></span>
2. <span data-ttu-id="e19dc-127">Dans la section connaissances de l' **organisation** , cliquez sur **connecter les personnes aux connaissances**.</span><span class="sxs-lookup"><span data-stu-id="e19dc-127">In the **Organizational Knowledge** section, click **Connect people to knowledge**.</span></span><br/>

    ![Connecter des personnes aux connaissances](../media/content-understanding/admin-org-knowledge-options.png) </br>

3. <span data-ttu-id="e19dc-129">Sur la page **connecter des personnes au** niveau de connaissances, cliquez sur **prise en main** pour vous guider tout au long du processus de configuration.</span><span class="sxs-lookup"><span data-stu-id="e19dc-129">On the **Connect people to knowledge** page, click **Get started** to walk you through the setup process.</span></span><br/>

    ![Prise en main](../media/content-understanding/k-get-started.png) </br>

4. <span data-ttu-id="e19dc-131">Sur la page **choisir comment le réseau de connaissances peut trouver des rubriques** , vous allez configurer la découverte de rubrique.</span><span class="sxs-lookup"><span data-stu-id="e19dc-131">On the **Choose how the knowledge network can find topics** page, you will configure topic discovery.</span></span> <span data-ttu-id="e19dc-132">Dans la section **Sélectionner les sources des rubriques SharePoint** , sélectionnez les sites SharePoint qui seront analysés en tant que sources pour vos rubriques lors de la découverte.</span><span class="sxs-lookup"><span data-stu-id="e19dc-132">In the **Select SharePoint topic sources** section, select which SharePoint sites will be crawled as sources for your topics during discovery.</span></span> <span data-ttu-id="e19dc-133">Cela inclut les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="e19dc-133">This includes:</span></span></br>
    <span data-ttu-id="e19dc-134">a.</span><span class="sxs-lookup"><span data-stu-id="e19dc-134">a.</span></span> <span data-ttu-id="e19dc-135">**Tous les sites**: tous les sites SharePoint de votre client.</span><span class="sxs-lookup"><span data-stu-id="e19dc-135">**All sites**: All SharePoint sites in your tenant.</span></span> <span data-ttu-id="e19dc-136">Ceci capture les sites actuels et futurs.</span><span class="sxs-lookup"><span data-stu-id="e19dc-136">This captures current and future sites.</span></span></br>
    <span data-ttu-id="e19dc-137">b.</span><span class="sxs-lookup"><span data-stu-id="e19dc-137">b.</span></span> <span data-ttu-id="e19dc-138">**Tout, à l’exception des sites sélectionnés**: saisissez les noms des sites à exclure.</span><span class="sxs-lookup"><span data-stu-id="e19dc-138">**All, except selected sites**: Type the names of the sites you want to exclude.</span></span>  <span data-ttu-id="e19dc-139">Vous pouvez également télécharger une liste de sites que vous souhaitez exclure de la découverte.</span><span class="sxs-lookup"><span data-stu-id="e19dc-139">You can also upload a list of sites that you want to opt out from discovery.</span></span> <span data-ttu-id="e19dc-140">Les sites créés à l’avenir seront inclus en tant que sources pour la découverte des rubriques.</span><span class="sxs-lookup"><span data-stu-id="e19dc-140">Sites created in future will be included as sources for topic discovery.</span></span> </br>
    <span data-ttu-id="e19dc-141">c.</span><span class="sxs-lookup"><span data-stu-id="e19dc-141">c.</span></span> <span data-ttu-id="e19dc-142">**Sites sélectionnés uniquement**: saisissez les noms des sites que vous souhaitez inclure.</span><span class="sxs-lookup"><span data-stu-id="e19dc-142">**Only selected sites**: Type the names of the sites you want to include.</span></span> <span data-ttu-id="e19dc-143">Vous pouvez également télécharger une liste de sites.</span><span class="sxs-lookup"><span data-stu-id="e19dc-143">You can also upload a list of sites.</span></span> <span data-ttu-id="e19dc-144">Les sites créés à l’avenir ne seront pas inclus en tant que sources pour la découverte des rubriques.</span><span class="sxs-lookup"><span data-stu-id="e19dc-144">Sites created in the future will not be included as sources for topic discovery.</span></span> </br>

    ![Choisir comment rechercher des rubriques](../media/content-understanding/ksetup1.png) </br>
   
5. <span data-ttu-id="e19dc-146">Dans la section **exclure des rubriques par nom** , vous pouvez choisir d’inclure les noms des rubriques dont vous ne voulez pas dans les résultats découverts.</span><span class="sxs-lookup"><span data-stu-id="e19dc-146">In the **Exclude topics by name** section, you can choose to includes names of topics you don't want to be in the discovered results.</span></span> <span data-ttu-id="e19dc-147">Utilisez ce paramètre pour empêcher les rubriques sensibles d’être incluses dans le cadre du réseau de connaissances.</span><span class="sxs-lookup"><span data-stu-id="e19dc-147">Use this setting to prevent sensitive topics from being included as part of the knowledge network.</span></span> <span data-ttu-id="e19dc-148">Vos options sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e19dc-148">Your options include:</span></span></br>
    <span data-ttu-id="e19dc-149">a.</span><span class="sxs-lookup"><span data-stu-id="e19dc-149">a.</span></span> <span data-ttu-id="e19dc-150">**Ne pas exclure les rubriques**</span><span class="sxs-lookup"><span data-stu-id="e19dc-150">**Don't exclude any topics**</span></span> </br>
    <span data-ttu-id="e19dc-151">b.</span><span class="sxs-lookup"><span data-stu-id="e19dc-151">b.</span></span> <span data-ttu-id="e19dc-152">**Exclure la rubrique contenant ces termes**: Si vous avez des rubriques que vous ne souhaitez pas afficher aux utilisateurs dans le cadre du réseau de connaissances.</span><span class="sxs-lookup"><span data-stu-id="e19dc-152">**Exclude topic that contain these terms**:  If you have topics you don’t want shown to users as part of the knowledge network.</span></span>
   <span data-ttu-id="e19dc-153">-Téléchargez le modèle fourni.</span><span class="sxs-lookup"><span data-stu-id="e19dc-153">- Download the provided template.</span></span>
   <span data-ttu-id="e19dc-154">-Entrez les noms de rubrique à exclure.</span><span class="sxs-lookup"><span data-stu-id="e19dc-154">- Enter the topic names you want to exclude.</span></span> <span data-ttu-id="e19dc-155">Vous devez indiquer le type de correspondance comme exact ou partiel.</span><span class="sxs-lookup"><span data-stu-id="e19dc-155">You must indicate the match type as exact or partial.</span></span> <span data-ttu-id="e19dc-156">Une correspondance exacte signifie que les rubriques qui correspondent au terme exact seront exclues.</span><span class="sxs-lookup"><span data-stu-id="e19dc-156">Exact match means that topics that fit the exact term will be excluded.</span></span> <span data-ttu-id="e19dc-157">La correspondance partielle est plus stricte et signifie que les rubriques qui contiennent le terme seront exclues.</span><span class="sxs-lookup"><span data-stu-id="e19dc-157">Partial match is stricter and means that topics that contain the term will be excluded.</span></span> <span data-ttu-id="e19dc-158">Par exemple, si vous saisissez *doc* comme nom de rubrique, l' *assembly doc* sera exclu au lieu de l' *ancrage* .</span><span class="sxs-lookup"><span data-stu-id="e19dc-158">For example, if you enter *Doc* as the topic name, *Doc assembly* will be excluded while *Docker* won't.</span></span> <span data-ttu-id="e19dc-159">Les noms de rubrique ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="e19dc-159">Topic names are case insensitive.</span></span>  
        <span data-ttu-id="e19dc-160">-Sélectionnez  **+**   pour importer votre fichier CSV terminé.</span><span class="sxs-lookup"><span data-stu-id="e19dc-160">- Select **+** to import your completed CSV file.</span></span> <span data-ttu-id="e19dc-161">Ensuite, sélectionnez **Télécharger**.</span><span class="sxs-lookup"><span data-stu-id="e19dc-161">Then select **Upload**.</span></span> <span data-ttu-id="e19dc-162">Une coche verte s’affiche si votre fichier a été traité avec succès.</span><span class="sxs-lookup"><span data-stu-id="e19dc-162">You’ll see a green check mark if your file has been processed successfully.</span></span> <span data-ttu-id="e19dc-163">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="e19dc-163">Select **Next**.</span></span></br>


6. <span data-ttu-id="e19dc-164">Sur la page **qui peut voir les rubriques et où elles peuvent les afficher** , vous allez configurer la visibilité des rubriques.</span><span class="sxs-lookup"><span data-stu-id="e19dc-164">On the **Who can see topics and where they can see them** page, you will configure topic visibility.</span></span> <span data-ttu-id="e19dc-165">Dans le paramètre **qui peut voir les rubriques du paramètre de réseau de connaissances** , vous choisissez les utilisateurs qui auront accès aux détails de la rubrique, comme les rubriques en surbrillance, les fiches de rubrique, les réponses aux questions dans la recherche et les pages de rubrique.</span><span class="sxs-lookup"><span data-stu-id="e19dc-165">In the **Who can see topics in the knowledge network** setting, you choose who will have access to topic details, such as highlighted topics, topic cards, topic answers in search, and topic pages.</span></span> <span data-ttu-id="e19dc-166">Vous pouvez sélectionner :</span><span class="sxs-lookup"><span data-stu-id="e19dc-166">You can select:</span></span></br>
    <span data-ttu-id="e19dc-167">a.</span><span class="sxs-lookup"><span data-stu-id="e19dc-167">a.</span></span> <span data-ttu-id="e19dc-168">**Tout le monde dans votre organisation**</span><span class="sxs-lookup"><span data-stu-id="e19dc-168">**Everyone in your organization**</span></span></br>
    <span data-ttu-id="e19dc-169">b.</span><span class="sxs-lookup"><span data-stu-id="e19dc-169">b.</span></span> <span data-ttu-id="e19dc-170">**Uniquement les personnes ou les groupes de sécurité sélectionnés**</span><span class="sxs-lookup"><span data-stu-id="e19dc-170">**Only selected people or security groups**</span></span></br>
    <span data-ttu-id="e19dc-171">c.</span><span class="sxs-lookup"><span data-stu-id="e19dc-171">c.</span></span> <span data-ttu-id="e19dc-172">**Personne**</span><span class="sxs-lookup"><span data-stu-id="e19dc-172">**No one**</span></span></br>

    ![Qui peut voir les rubriques](../media/content-understanding/ksetup2.png) </br> 

 > [!Note] 
 > <span data-ttu-id="e19dc-174">Bien que ce paramètre vous permette de sélectionner un utilisateur au sein de votre organisation, seuls les utilisateurs qui disposent de licences de gestion des connaissances qui lui sont attribués pourront consulter les rubriques.</span><span class="sxs-lookup"><span data-stu-id="e19dc-174">While this setting allows you to select any user in your organization, only users who have knowledge management licenses assigned to them will be able to view topics.</span></span> 

7. <span data-ttu-id="e19dc-175">Dans la page **autorisations pour la rubrique gestion des** rubriques, choisissez qui pourra créer, modifier ou gérer des rubriques.</span><span class="sxs-lookup"><span data-stu-id="e19dc-175">In the **Permissions for topic management** page, you choose who will be able to create, edit, or manage topics.</span></span> <span data-ttu-id="e19dc-176">Dans la section **qui peut créer et modifier des rubriques** , vous pouvez sélectionner :</span><span class="sxs-lookup"><span data-stu-id="e19dc-176">In the **Who can create and edit topics** section, you can select:</span></span></br>
    <span data-ttu-id="e19dc-177">a.</span><span class="sxs-lookup"><span data-stu-id="e19dc-177">a.</span></span> <span data-ttu-id="e19dc-178">**Tout le monde dans votre organisation**</span><span class="sxs-lookup"><span data-stu-id="e19dc-178">**Everyone in your organization**</span></span></br>
    <span data-ttu-id="e19dc-179">b.</span><span class="sxs-lookup"><span data-stu-id="e19dc-179">b.</span></span> <span data-ttu-id="e19dc-180">**Uniquement les personnes ou les groupes de sécurité sélectionnés**</span><span class="sxs-lookup"><span data-stu-id="e19dc-180">**Only selected people or security groups**</span></span></br>
8. <span data-ttu-id="e19dc-181">Dans la section **qui peut gérer les rubriques** , vous pouvez sélectionner :</span><span class="sxs-lookup"><span data-stu-id="e19dc-181">In the **Who can manage topics** section, you can select:</span></span></br>
    <span data-ttu-id="e19dc-182">a.</span><span class="sxs-lookup"><span data-stu-id="e19dc-182">a.</span></span> <span data-ttu-id="e19dc-183">**Tout le monde dans votre organisation**</span><span class="sxs-lookup"><span data-stu-id="e19dc-183">**Everyone in your organization**</span></span></br>
    <span data-ttu-id="e19dc-184">b.</span><span class="sxs-lookup"><span data-stu-id="e19dc-184">b.</span></span> <span data-ttu-id="e19dc-185">**Personnes ou groupes de sécurité sélectionnés**</span><span class="sxs-lookup"><span data-stu-id="e19dc-185">**Selected people or security groups**</span></span></br>

    ![Autorisations pour la gestion des rubriques](../media/content-understanding/ksetup3.png) </br>

    <span data-ttu-id="e19dc-187">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="e19dc-187">Select **Next**.</span></span></br>
9. <span data-ttu-id="e19dc-188">Sur la page **créer un centre de rubriques** , vous pouvez créer votre site Centre de rubrique dans lequel les pages de rubrique peuvent être affichées et les rubriques peuvent être gérées.</span><span class="sxs-lookup"><span data-stu-id="e19dc-188">On the **Create Topic  Center** page, you can create your topic center site in which topic pages can be viewed and topics can be managed.</span></span>  <span data-ttu-id="e19dc-189">Dans la zone **nom du centre** de la rubrique, tapez un nom pour le centre de la rubrique.</span><span class="sxs-lookup"><span data-stu-id="e19dc-189">In the **Topic center name** box, type a name for your Topic center.</span></span> <span data-ttu-id="e19dc-190">Vous pouvez éventuellement taper une brève description dans la zone **Description du site** .</span><span class="sxs-lookup"><span data-stu-id="e19dc-190">You can optionally type a short description in the **Site description** box.</span></span> </br>

<span data-ttu-id="e19dc-191">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="e19dc-191">Select **Next**.</span></span></br>

   ![Créer un centre de connaissances](../media/content-understanding/ksetup4.png) </br> 

10. <span data-ttu-id="e19dc-193">Sur la page **révision et fin** , vous pouvez examiner le paramètre que vous avez sélectionné et choisir d’effectuer des modifications.</span><span class="sxs-lookup"><span data-stu-id="e19dc-193">On the **Review and finish** page, you can look at your selected setting and choose to make changes.</span></span> <span data-ttu-id="e19dc-194">Si vos sélections vous conviennent, sélectionnez **activer**.</span><span class="sxs-lookup"><span data-stu-id="e19dc-194">If you are satisfied with your selections, select **Activate**.</span></span>

    ![Terminer et vérifier](../media/content-understanding/ksetup5.png) </br> 

11. <span data-ttu-id="e19dc-196">La page **activation du réseau de connaissances** s’affiche, confirmant que le système commence à analyser les sites sélectionnés pour les rubriques et la création du site Centre de connaissances.</span><span class="sxs-lookup"><span data-stu-id="e19dc-196">The **Knowledge network activated** page will display, confirming that the system will now start analyzing your selected sites for topics and creating the Knowledge Center site.</span></span> <span data-ttu-id="e19dc-197">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="e19dc-197">Select **Done**.</span></span></br>

    ![Activated](../media/content-understanding/ksetup6.png) </br> 

12. <span data-ttu-id="e19dc-199">Vous serez redirigé vers la page **connecter des personnes à la page de connaissances** .</span><span class="sxs-lookup"><span data-stu-id="e19dc-199">You'll be returned to your **Connect people to knowledge** page.</span></span> <span data-ttu-id="e19dc-200">À partir de cette page, vous pouvez sélectionner **gérer** pour modifier vos paramètres de configuration.</span><span class="sxs-lookup"><span data-stu-id="e19dc-200">From this page, you can select **Manage** to make any changes to your configuration settings.</span></span> 

    ![Paramètres appliqués](../media/content-understanding/ksetup7.png) </br>   

> [!Note]
> <span data-ttu-id="e19dc-202">Après l’installation, un administrateur peut [modifier les paramètres de gestion des connaissances sélectionnés](manage-knowledge-network.md) à tout moment en retournant sur cette page.</span><span class="sxs-lookup"><span data-stu-id="e19dc-202">After setup, an admin can [make changes to your selected knowledge management settings](manage-knowledge-network.md) any time by returning to this page.</span></span>


## <a name="see-also"></a><span data-ttu-id="e19dc-203">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e19dc-203">See also</span></span>



  






