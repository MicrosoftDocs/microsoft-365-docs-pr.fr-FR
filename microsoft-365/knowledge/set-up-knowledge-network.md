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
ms.openlocfilehash: d6495f297f09ddc167d7c36835ac82a15abc91ac
ms.sourcegitcommit: 57b37a3ce40f205c7320d5be1a0d906dd492b863
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "47405648"
---
# <a name="set-up-knowledge-management-preview"></a><span data-ttu-id="2fa1a-103">Configurer la gestion des connaissances (aperçu)</span><span class="sxs-lookup"><span data-stu-id="2fa1a-103">Set up Knowledge Management (Preview)</span></span>

> [!Note] 
> <span data-ttu-id="2fa1a-104">Le contenu de cet article est destiné à Project cortex privé preview.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-104">The content in this article is for Project Cortex Private Preview.</span></span> <span data-ttu-id="2fa1a-105">Pour [plus d’informations sur le projet cortex](https://aka.ms/projectcortex).</span><span class="sxs-lookup"><span data-stu-id="2fa1a-105">[Find out more about Project Cortex](https://aka.ms/projectcortex).</span></span>

<span data-ttu-id="2fa1a-106">Vous pouvez utiliser le centre d’administration Microsoft 365 pour installer et configurer la [gestion des connaissances](knowledge-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2fa1a-106">You can use the Microsoft 365 admin center to set up and configure [Knowledge Management](knowledge-management-overview.md).</span></span> 

> [!Important]
> <span data-ttu-id="2fa1a-107">Il est important de planifier la meilleure façon de configurer et de configurer la gestion des connaissances dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-107">It is important to plan the best way to set up and configure Knowledge Management in your environment.</span></span> <span data-ttu-id="2fa1a-108">Par exemple, vous devez prendre en compte les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="2fa1a-108">For example, you will need to make considerations about the following:</span></span>
- <span data-ttu-id="2fa1a-109">Les sites SharePoint que vous souhaitez analyser pour les rubriques.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-109">Which SharePoint sites you want to analyze for topics.</span></span>
- <span data-ttu-id="2fa1a-110">Les utilisateurs auxquels vous souhaitez faire apparaître les rubriques.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-110">Which users you want to make topics visible to.</span></span>
- <span data-ttu-id="2fa1a-111">Les utilisateurs auxquels vous souhaitez accorder des autorisations pour gérer les rubriques dans le Centre des rubriques.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-111">Which users you want to give permissions to manage topics in the topic center.</span></span>
- <span data-ttu-id="2fa1a-112">Les utilisateurs auxquels vous souhaitez accorder des autorisations pour créer ou modifier des rubriques dans le Centre des rubriques.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-112">Which users you want to give permissions to create or edit topics in the topic center.</span></span>
- <span data-ttu-id="2fa1a-113">Le nom que vous souhaitez donner à votre centre de sujets.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-113">What name you want to give your topic center.</span></span>

> [!Note]
> <span data-ttu-id="2fa1a-114">Il peut s’avérer utile de créer des groupes de sécurité pour attribuer aux utilisateurs les autorisations nécessaires pour afficher des rubriques, gérer des rubriques et créer et modifier des rubriques.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-114">You may find it useful to create security groups to assign your users the permissions needed to view topics, manage topic, and create and edit topics.</span></span>

<span data-ttu-id="2fa1a-115">Un administrateur peut également [modifier les paramètres sélectionnés à tout moment après l’installation](manage-knowledge-network.md) via les paramètres de gestion des connaissances dans le centre d’administration 365 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-115">An admin can also [make changes to your selected settings anytime after setup](manage-knowledge-network.md) through the Knowledge Management settings in the Microsoft 365 admin center.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fa1a-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2fa1a-116">Requirements</span></span> 
<span data-ttu-id="2fa1a-117">Vous devez disposer d’autorisations d’administrateur général ou d’administrateur SharePoint pour pouvoir accéder au centre d’administration Microsoft 365 et configurer des tâches de connaissances organisationnelles.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-117">You must have Global Admin or SharePoint admin permissions to be able to access the Microsoft 365 admin center and set up Organizational knowledge tasks.</span></span>

## <a name="set-up-your-knowledge-network"></a><span data-ttu-id="2fa1a-118">Configurer votre réseau de connaissances</span><span class="sxs-lookup"><span data-stu-id="2fa1a-118">Set up your knowledge network</span></span>

<span data-ttu-id="2fa1a-119">La configuration de votre réseau de connaissances vous guide tout au long des étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="2fa1a-119">Setting up your knowledge network walks you through the following:</span></span>

- <span data-ttu-id="2fa1a-120">Découverte de rubrique : sélection des sources de rubrique et des rubriques à exclure de la découverte.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-120">Topic discovery: Selecting topic sources and topics to  exclude from discovery.</span></span>
- <span data-ttu-id="2fa1a-121">Visibilité de rubrique : sélection des personnes qui peuvent afficher les rubriques sous forme de mises en surbrillance dans les pages de recherche et de rubrique.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-121">Topic visibility: Selecting who can view topics as highlights, in search and topic pages.</span></span>
- <span data-ttu-id="2fa1a-122">Autorisations de rubrique : sélection des personnes qui peuvent créer, modifier et gérer des rubriques.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-122">Topic permissions: Selecting who can create, edit, and manage topics.</span></span>
- <span data-ttu-id="2fa1a-123">Centre des rubriques : créez votre centre de rubriques.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-123">Topic center: Create your topic center.</span></span>
- <span data-ttu-id="2fa1a-124">Révision : Vérifiez et appliquez vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-124">Review: Check and apply your settings.</span></span>

<span data-ttu-id="2fa1a-125">Pour configurer votre réseau de connaissances :</span><span class="sxs-lookup"><span data-stu-id="2fa1a-125">To set up your knowledge network:</span></span>

1. <span data-ttu-id="2fa1a-126">Dans le centre d’administration 365 de Microsoft (admin.microsoft.com), sélectionnez **configuration**, puis affichez la section connaissances de l' **organisation** .</span><span class="sxs-lookup"><span data-stu-id="2fa1a-126">In the Microsoft 365 admin center (admin.microsoft.com), select **Setup**, and then view the **Organizational Knowledge** section.</span></span>
2. <span data-ttu-id="2fa1a-127">Dans la section connaissances de l' **organisation** , cliquez sur **connecter les personnes aux connaissances**.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-127">In the **Organizational Knowledge** section, click **Connect people to knowledge**.</span></span><br/>

    ![Connecter des personnes aux connaissances](../media/content-understanding/admin-org-knowledge-options.png) </br>

3. <span data-ttu-id="2fa1a-129">Sur la page **connecter des personnes au** niveau de connaissances, cliquez sur **prise en main** pour vous guider tout au long du processus de configuration.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-129">On the **Connect people to knowledge** page, click **Get started** to walk you through the setup process.</span></span><br/>

    ![Prise en main](../media/content-understanding/k-get-started.png) </br>

4. <span data-ttu-id="2fa1a-131">Sur la page **choisir comment le réseau de connaissances peut trouver des rubriques** , vous allez configurer la découverte de rubrique.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-131">On the **Choose how the knowledge network can find topics** page, you will configure topic discovery.</span></span> <span data-ttu-id="2fa1a-132">Dans la section **Sélectionner les sources des rubriques SharePoint** , sélectionnez les sites SharePoint qui seront analysés en tant que sources pour vos rubriques lors de la découverte.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-132">In the **Select SharePoint topic sources** section, select which SharePoint sites will be crawled as sources for your topics during discovery.</span></span> <span data-ttu-id="2fa1a-133">Cela inclut les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2fa1a-133">This includes:</span></span></br>
    <span data-ttu-id="2fa1a-134">a.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-134">a.</span></span> <span data-ttu-id="2fa1a-135">**Tous les sites**: tous les sites SharePoint de votre client.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-135">**All sites**: All SharePoint sites in your tenant.</span></span> <span data-ttu-id="2fa1a-136">Ceci capture les sites actuels et futurs.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-136">This captures current and future sites.</span></span></br>
    <span data-ttu-id="2fa1a-137">b.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-137">b.</span></span> <span data-ttu-id="2fa1a-138">**Tout, à l’exception des sites sélectionnés**: saisissez les noms des sites à exclure.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-138">**All, except selected sites**: Type the names of the sites you want to exclude.</span></span>  <span data-ttu-id="2fa1a-139">Vous pouvez également télécharger une liste de sites que vous souhaitez exclure de la découverte.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-139">You can also upload a list of sites that you want to opt out from discovery.</span></span> <span data-ttu-id="2fa1a-140">Les sites créés à l’avenir seront inclus en tant que sources pour la découverte des rubriques.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-140">Sites created in future will be included as sources for topic discovery.</span></span> </br>
    <span data-ttu-id="2fa1a-141">c.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-141">c.</span></span> <span data-ttu-id="2fa1a-142">**Sites sélectionnés uniquement**: saisissez les noms des sites que vous souhaitez inclure.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-142">**Only selected sites**: Type the names of the sites you want to include.</span></span> <span data-ttu-id="2fa1a-143">Vous pouvez également télécharger une liste de sites.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-143">You can also upload a list of sites.</span></span> <span data-ttu-id="2fa1a-144">Les sites créés à l’avenir ne seront pas inclus en tant que sources pour la découverte des rubriques.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-144">Sites created in the future will not be included as sources for topic discovery.</span></span> </br>

    ![Choisir comment rechercher des rubriques](../media/content-understanding/ksetup1.png) </br>
   
5. <span data-ttu-id="2fa1a-146">Dans la section **exclure des rubriques par nom** , vous pouvez choisir d’inclure les noms des rubriques dont vous ne voulez pas dans les résultats découverts.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-146">In the **Exclude topics by name** section, you can choose to includes names of topics you don't want to be in the discovered results.</span></span> <span data-ttu-id="2fa1a-147">Utilisez ce paramètre pour empêcher les rubriques sensibles d’être incluses dans le cadre du réseau de connaissances.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-147">Use this setting to prevent sensitive topics from being included as part of the knowledge network.</span></span> <span data-ttu-id="2fa1a-148">Vos options sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2fa1a-148">Your options include:</span></span></br>
    <span data-ttu-id="2fa1a-149">a.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-149">a.</span></span> <span data-ttu-id="2fa1a-150">**Ne pas exclure les rubriques**</span><span class="sxs-lookup"><span data-stu-id="2fa1a-150">**Don't exclude any topics**</span></span> </br>
    <span data-ttu-id="2fa1a-151">b.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-151">b.</span></span> <span data-ttu-id="2fa1a-152">**Exclure les rubriques par nom**: Si vous avez des rubriques que vous ne voulez pas afficher aux utilisateurs dans le cadre du réseau de connaissances.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-152">**Exclude topics by name**:  If you have topics you don’t want shown to users as part of the knowledge network.</span></span></br>

    ![Exclure des rubriques](../media/content-understanding/topics-excluded-by-name.png) </br>

    #### <a name="how-to-exclude-topics-by-name"></a><span data-ttu-id="2fa1a-154">Procédure exclure des rubriques par nom</span><span class="sxs-lookup"><span data-stu-id="2fa1a-154">How to exclude topics by name</span></span>    

    <span data-ttu-id="2fa1a-155">Si vous devez exclure des rubriques, après avoir sélectionné **exclure les rubriques par nom**, sélectionnez **Télécharger le modèle. csv**.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-155">If you need to exclude topics, after selecting **Exclude topics by name**, select **Download the .csv template**.</span></span> <span data-ttu-id="2fa1a-156">Utilisez Excel. Modèle CSV pour inclure une liste des rubriques que vous souhaitez exclure de vos résultats de découverte.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-156">Use the Excel .CSV template to include a list of topics that you want to exclude from your discovery results.</span></span>

    ![Exclure les rubriques du modèle CSV](../media/content-understanding/csv1.png) </br>

    <span data-ttu-id="2fa1a-158">Dans le modèle CSV, entrez les informations suivantes sur les rubriques à exclure :</span><span class="sxs-lookup"><span data-stu-id="2fa1a-158">In the CSV template, enter the following information about the topics you want to exclude:</span></span>

    - <span data-ttu-id="2fa1a-159">**Nom**: tapez le nom de la rubrique à exclure.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-159">**Name**: Type the name of the topic you want to exclude.</span></span> <span data-ttu-id="2fa1a-160">Vous pouvez procéder de deux manières :</span><span class="sxs-lookup"><span data-stu-id="2fa1a-160">There are two ways to do this:</span></span></br>
        - <span data-ttu-id="2fa1a-161">Correspondance exacte : vous pouvez inclure le nom exact ou un acronyme (par exemple, *contoso* ou *ATL*).</span><span class="sxs-lookup"><span data-stu-id="2fa1a-161">Exact match: You can include the exact name or acronym (for example, *Contoso* or *ATL*).</span></span></br>
        - <span data-ttu-id="2fa1a-162">Correspondance partielle : vous pouvez exclure toutes les rubriques qui contiennent un mot spécifique.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-162">Partial match: You can exclude all topics that have a specific word in it.</span></span>  <span data-ttu-id="2fa1a-163">Par exemple, *arc* exclut toutes les rubriques contenant le mot *arc* , comme un *cercle arc*, un *soudage*à l’arc de plasma ou un *arc de formation*. Notez qu’il n’exclura pas les rubriques dans lesquelles le texte est inclus dans un mot, tel que *architecture*.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-163">For example, *arc* will exclude all topics with the word *arc* in it, such as *Arc circle*, *Plasma arc welding*, or *Training arc*. Note that it will not exclude topics in which the text is included as part of a word, such as *Architecture*.</span></span></br>
    - <span data-ttu-id="2fa1a-164">**Expansion (facultatif)**: Si vous souhaitez exclure un acronyme, tapez les mots de l’acronyme.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-164">**Expansion (optional)**: If you want to exclude an acronym, type the words the acronym stands for.</span></span></br>
    - <span data-ttu-id="2fa1a-165">**MatchType-exacte/partielle**: spécifiez si le nom que vous avez entré est un type de correspondance *exacte* ou *partielle* .</span><span class="sxs-lookup"><span data-stu-id="2fa1a-165">**MatchType-Exact/Partial**: Type whether the name you entered was an *exact* or *partial* match type.</span></span></br>

    <span data-ttu-id="2fa1a-166">Une fois que vous avez terminé et enregistré votre fichier de modèle CSV, sélectionnez **Parcourir** pour le localiser et le sélectionner.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-166">After you've completed and saved your CSV template file, select **Browse** to locate and select it.</span></span>
    
    <span data-ttu-id="2fa1a-167">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-167">Select **Next**.</span></span></br>

6. <span data-ttu-id="2fa1a-168">Sur la page **qui peut voir les rubriques et où elles peuvent les afficher** , vous allez configurer la visibilité des rubriques.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-168">On the **Who can see topics and where they can see them** page, you will configure topic visibility.</span></span> <span data-ttu-id="2fa1a-169">Dans le paramètre **qui peut voir les rubriques du paramètre de réseau de connaissances** , vous choisissez les utilisateurs qui auront accès aux détails de la rubrique, comme les rubriques en surbrillance, les fiches de rubrique, les réponses aux questions dans la recherche et les pages de rubrique.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-169">In the **Who can see topics in the knowledge network** setting, you choose who will have access to topic details, such as highlighted topics, topic cards, topic answers in search, and topic pages.</span></span> <span data-ttu-id="2fa1a-170">Vous pouvez sélectionner :</span><span class="sxs-lookup"><span data-stu-id="2fa1a-170">You can select:</span></span></br>
    <span data-ttu-id="2fa1a-171">a.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-171">a.</span></span> <span data-ttu-id="2fa1a-172">**Tout le monde dans votre organisation**</span><span class="sxs-lookup"><span data-stu-id="2fa1a-172">**Everyone in your organization**</span></span></br>
    <span data-ttu-id="2fa1a-173">b.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-173">b.</span></span> <span data-ttu-id="2fa1a-174">**Uniquement les personnes ou les groupes de sécurité sélectionnés**</span><span class="sxs-lookup"><span data-stu-id="2fa1a-174">**Only selected people or security groups**</span></span></br>
    <span data-ttu-id="2fa1a-175">c.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-175">c.</span></span> <span data-ttu-id="2fa1a-176">**Personne**</span><span class="sxs-lookup"><span data-stu-id="2fa1a-176">**No one**</span></span></br>

    ![Qui peut voir les rubriques](../media/content-understanding/ksetup2.png) </br> 

 > [!Note] 
 > <span data-ttu-id="2fa1a-178">Bien que ce paramètre vous permette de sélectionner un utilisateur au sein de votre organisation, seuls les utilisateurs qui disposent de licences de gestion des connaissances qui lui sont attribués pourront consulter les rubriques.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-178">While this setting allows you to select any user in your organization, only users who have knowledge management licenses assigned to them will be able to view topics.</span></span> 

7. <span data-ttu-id="2fa1a-179">Dans la page **autorisations pour la rubrique gestion des** rubriques, choisissez qui pourra créer, modifier ou gérer des rubriques.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-179">In the **Permissions for topic management** page, you choose who will be able to create, edit, or manage topics.</span></span> <span data-ttu-id="2fa1a-180">Dans la section **qui peut créer et modifier des rubriques** , vous pouvez sélectionner :</span><span class="sxs-lookup"><span data-stu-id="2fa1a-180">In the **Who can create and edit topics** section, you can select:</span></span></br>
    <span data-ttu-id="2fa1a-181">a.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-181">a.</span></span> <span data-ttu-id="2fa1a-182">**Tout le monde dans votre organisation**</span><span class="sxs-lookup"><span data-stu-id="2fa1a-182">**Everyone in your organization**</span></span></br>
    <span data-ttu-id="2fa1a-183">b.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-183">b.</span></span> <span data-ttu-id="2fa1a-184">**Uniquement les personnes ou les groupes de sécurité sélectionnés**</span><span class="sxs-lookup"><span data-stu-id="2fa1a-184">**Only selected people or security groups**</span></span></br>
8. <span data-ttu-id="2fa1a-185">Dans la section **qui peut gérer les rubriques** , vous pouvez sélectionner :</span><span class="sxs-lookup"><span data-stu-id="2fa1a-185">In the **Who can manage topics** section, you can select:</span></span></br>
    <span data-ttu-id="2fa1a-186">a.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-186">a.</span></span> <span data-ttu-id="2fa1a-187">**Tout le monde dans votre organisation**</span><span class="sxs-lookup"><span data-stu-id="2fa1a-187">**Everyone in your organization**</span></span></br>
    <span data-ttu-id="2fa1a-188">b.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-188">b.</span></span> <span data-ttu-id="2fa1a-189">**Personnes ou groupes de sécurité sélectionnés**</span><span class="sxs-lookup"><span data-stu-id="2fa1a-189">**Selected people or security groups**</span></span></br>

    ![Autorisations pour la gestion des rubriques](../media/content-understanding/ksetup3.png) </br>

    <span data-ttu-id="2fa1a-191">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-191">Select **Next**.</span></span></br>
9. <span data-ttu-id="2fa1a-192">Sur la page **créer un centre de rubriques** , vous pouvez créer votre site Centre de rubrique dans lequel les pages de rubrique peuvent être affichées et les rubriques peuvent être gérées.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-192">On the **Create Topic  Center** page, you can create your topic center site in which topic pages can be viewed and topics can be managed.</span></span>  <span data-ttu-id="2fa1a-193">Dans la zone **nom du centre** de la rubrique, tapez un nom pour le centre de la rubrique.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-193">In the **Topic center name** box, type a name for your Topic center.</span></span> <span data-ttu-id="2fa1a-194">Vous pouvez éventuellement taper une brève description dans la zone **Description du site** .</span><span class="sxs-lookup"><span data-stu-id="2fa1a-194">You can optionally type a short description in the **Site description** box.</span></span> </br>

<span data-ttu-id="2fa1a-195">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-195">Select **Next**.</span></span></br>

   ![Créer un centre de connaissances](../media/content-understanding/ksetup4.png) </br> 

10. <span data-ttu-id="2fa1a-197">Sur la page **révision et fin** , vous pouvez examiner le paramètre que vous avez sélectionné et choisir d’effectuer des modifications.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-197">On the **Review and finish** page, you can look at your selected setting and choose to make changes.</span></span> <span data-ttu-id="2fa1a-198">Si vos sélections vous conviennent, sélectionnez **activer**.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-198">If you are satisfied with your selections, select **Activate**.</span></span>

    ![Terminer et vérifier](../media/content-understanding/ksetup5.png) </br> 

11. <span data-ttu-id="2fa1a-200">La page **activation du réseau de connaissances** s’affiche, confirmant que le système commence à analyser les sites sélectionnés pour les rubriques et la création du site Centre de connaissances.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-200">The **Knowledge network activated** page will display, confirming that the system will now start analyzing your selected sites for topics and creating the Knowledge Center site.</span></span> <span data-ttu-id="2fa1a-201">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-201">Select **Done**.</span></span></br>

    ![Activated](../media/content-understanding/ksetup6.png) </br> 

12. <span data-ttu-id="2fa1a-203">Vous serez redirigé vers la page **connecter des personnes à la page de connaissances** .</span><span class="sxs-lookup"><span data-stu-id="2fa1a-203">You'll be returned to your **Connect people to knowledge** page.</span></span> <span data-ttu-id="2fa1a-204">À partir de cette page, vous pouvez sélectionner **gérer** pour modifier vos paramètres de configuration.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-204">From this page, you can select **Manage** to make any changes to your configuration settings.</span></span> 

    ![Paramètres appliqués](../media/content-understanding/ksetup7.png) </br>   

> [!Note]
> <span data-ttu-id="2fa1a-206">Après l’installation, un administrateur peut [modifier les paramètres de gestion des connaissances sélectionnés](manage-knowledge-network.md) à tout moment en retournant sur cette page.</span><span class="sxs-lookup"><span data-stu-id="2fa1a-206">After setup, an admin can [make changes to your selected knowledge management settings](manage-knowledge-network.md) any time by returning to this page.</span></span>


## <a name="see-also"></a><span data-ttu-id="2fa1a-207">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2fa1a-207">See also</span></span>



  






