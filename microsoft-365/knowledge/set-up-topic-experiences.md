---
title: Configurer Les rubriques microsoft
ms.author: mikeplum
author: MikePlumleyMSFT
manager: serdars
ms.reviewer: nkokoye
audience: admin
ms.topic: article
ms.service: o365-administration
search.appverid: MET150
localization_priority: Normal
description: Découvrez comment configurer les rubriques microsoft
ms.openlocfilehash: 19395cf3a9ecc991f08f375425803cb81a2a1d35
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51930220"
---
# <a name="set-up-microsoft-viva-topics"></a><span data-ttu-id="b6579-103">Configurer Les rubriques microsoft</span><span class="sxs-lookup"><span data-stu-id="b6579-103">Set up Microsoft Viva Topics</span></span>

<span data-ttu-id="b6579-104">Vous pouvez utiliser le centre Microsoft 365'administration pour configurer les [rubriques.](topic-experiences-overview.md)</span><span class="sxs-lookup"><span data-stu-id="b6579-104">You can use the Microsoft 365 admin center to set up and configure [Topics](topic-experiences-overview.md).</span></span> 

<span data-ttu-id="b6579-105">Il est important de planifier la meilleure façon de configurer des rubriques dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="b6579-105">It is important to plan the best way to set up and configure topics in your environment.</span></span> <span data-ttu-id="b6579-106">Veillez à lire [les rubriques planifier microsoft avant](plan-topic-experiences.md) de commencer les procédures de cet article.</span><span class="sxs-lookup"><span data-stu-id="b6579-106">Be sure to read [Plan for Microsoft Viva Topics](plan-topic-experiences.md) before you begin the procedures in this article.</span></span>

<span data-ttu-id="b6579-107">Vous devez être abonné à [Rubriques Et](https://www.microsoft.com/microsoft-viva/topics) être administrateur général ou administrateur SharePoint pour accéder au Centre d’administration Microsoft 365 et configurer Rubriques.</span><span class="sxs-lookup"><span data-stu-id="b6579-107">You must be [subscribed to Viva Topics](https://www.microsoft.com/microsoft-viva/topics) and be a global administrator or SharePoint administrator to access the Microsoft 365 admin center and set up Topics.</span></span>

<span data-ttu-id="b6579-108">Si vous avez configuré SharePoint pour exiger [des](/sharepoint/control-access-from-unmanaged-devices)appareils gérés, assurez-vous de configurer les rubriques à partir d’un appareil géré.</span><span class="sxs-lookup"><span data-stu-id="b6579-108">If you have configured SharePoint to [require managed devices](/sharepoint/control-access-from-unmanaged-devices), be sure to set up Topics from a managed device.</span></span>

## <a name="video-demonstration"></a><span data-ttu-id="b6579-109">Démonstration vidéo</span><span class="sxs-lookup"><span data-stu-id="b6579-109">Video demonstration</span></span>

<span data-ttu-id="b6579-110">Cette vidéo montre le processus de configuration des rubriques dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b6579-110">This video shows the process for setting up Topics in Microsoft 365.</span></span>

<br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4Li0E]  

<br>

## <a name="assign-licenses"></a><span data-ttu-id="b6579-111">Attribuer des licences</span><span class="sxs-lookup"><span data-stu-id="b6579-111">Assign licenses</span></span>

<span data-ttu-id="b6579-112">Vous devez attribuer des licences pour les utilisateurs qui utiliseront Rubriques.</span><span class="sxs-lookup"><span data-stu-id="b6579-112">You must assign licenses for the users who will be using Topics.</span></span> <span data-ttu-id="b6579-113">Seuls les utilisateurs titulaires d’une licence peuvent voir des informations sur des sujets tels que les points forts, les fiches de rubrique, les pages de rubriques et le centre de rubriques.</span><span class="sxs-lookup"><span data-stu-id="b6579-113">Only users with a license can see information on topics including highlights, topic cards, topic pages and the topic center.</span></span> 

<span data-ttu-id="b6579-114">Pour attribuer des licences :</span><span class="sxs-lookup"><span data-stu-id="b6579-114">To assign licenses:</span></span>

1. <span data-ttu-id="b6579-115">Dans le Centre d’administration Microsoft 365, sous **Utilisateurs**, cliquez sur **Utilisateurs actifs**.</span><span class="sxs-lookup"><span data-stu-id="b6579-115">In the Microsoft 365 admin center, under **Users**, click **Active users**.</span></span>

2. <span data-ttu-id="b6579-116">Sélectionnez les utilisateurs dont vous souhaitez obtenir une licence, puis cliquez **sur Licences et applications.**</span><span class="sxs-lookup"><span data-stu-id="b6579-116">Select the users that you want to license, and click **Licenses and apps**.</span></span>

3. <span data-ttu-id="b6579-117">Sous **Licences,** **sélectionnez Rubriques Titre.**</span><span class="sxs-lookup"><span data-stu-id="b6579-117">Under **Licenses**, select **Viva Topics**.</span></span>

4. <span data-ttu-id="b6579-118">Sous **Applications,** assurez-vous **que Graph connectors search with Index (Topics)** et **Topics Topics sont** tous deux sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="b6579-118">Under **Apps**, make sure **Graph Connectors Search with Index (Viva Topics)** and **Viva Topics** are both selected.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="b6579-119">![Licences Microsoft Topics dans le Centre d Microsoft 365'administration Microsoft](../media/topic-experiences-licenses.png)</span><span class="sxs-lookup"><span data-stu-id="b6579-119">![Microsoft Viva Topics licenses in the Microsoft 365 admin center](../media/topic-experiences-licenses.png)</span></span>

5. <span data-ttu-id="b6579-120">Cliquez sur **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="b6579-120">Click **Save changes**.</span></span>

<span data-ttu-id="b6579-121">Une fois les licences attribuées, l’accès aux rubriques peut prendre jusqu’à une heure.</span><span class="sxs-lookup"><span data-stu-id="b6579-121">It may take up to an hour for users to get access to Topics after the licenses are assigned.</span></span>

## <a name="set-up-topics"></a><span data-ttu-id="b6579-122">Configurer les rubriques</span><span class="sxs-lookup"><span data-stu-id="b6579-122">Set up Topics</span></span>

<span data-ttu-id="b6579-123">Pour configurer des rubriques</span><span class="sxs-lookup"><span data-stu-id="b6579-123">To set up Topics</span></span>

1. <span data-ttu-id="b6579-124">Dans le [centre Microsoft 365' administration,](https://admin.microsoft.com)sélectionnez **Installation,** puis affichez la section Fichiers **et** contenu.</span><span class="sxs-lookup"><span data-stu-id="b6579-124">In the [Microsoft 365 admin center](https://admin.microsoft.com), select **Setup**, and then view the **Files and content** section.</span></span>
2. <span data-ttu-id="b6579-125">Dans la section **Fichiers et contenu,** cliquez **Connecter personnes à connaître.**</span><span class="sxs-lookup"><span data-stu-id="b6579-125">In the **Files and content** section, click **Connect people to knowledge**.</span></span>

    ![Connecter personnes à connaître](../media/admin-org-knowledge-options.png) 

3. <span data-ttu-id="b6579-127">Dans la page **Connecter personnes à la** connaissance, cliquez sur **Commencer** pour vous aider dans le processus de configuration.</span><span class="sxs-lookup"><span data-stu-id="b6579-127">On the **Connect people to knowledge** page, click **Get started** to walk you through the setup process.</span></span>

    ![Prise en main](../media/k-get-started.png) 

4. <span data-ttu-id="b6579-129">Dans la page **Choisir la façon dont Rubriques peut trouver des rubriques,** vous allez configurer la découverte de rubriques.</span><span class="sxs-lookup"><span data-stu-id="b6579-129">On the **Choose how Viva Topics can find topics** page, you will configure topic discovery.</span></span> <span data-ttu-id="b6579-130">Dans la section **Sélectionner SharePoint sources** de rubriques, sélectionnez les sites SharePoint seront analyser en tant que sources pour vos rubriques lors de la découverte.</span><span class="sxs-lookup"><span data-stu-id="b6579-130">In the **Select SharePoint topic sources** section, select which SharePoint sites will be crawled as sources for your topics during discovery.</span></span> <span data-ttu-id="b6579-131">Choisissez parmi les autorisations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b6579-131">Choose from:</span></span>
    - <span data-ttu-id="b6579-132">**Tous les sites** : tous les sites SharePoint dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b6579-132">**All sites**: All SharePoint sites in your organization.</span></span> <span data-ttu-id="b6579-133">Cela inclut les sites actuels et futurs.</span><span class="sxs-lookup"><span data-stu-id="b6579-133">This includes current and future sites.</span></span>
    - <span data-ttu-id="b6579-134">**Tous, sauf les sites sélectionnés**: tapez les noms des sites que vous souhaitez exclure.</span><span class="sxs-lookup"><span data-stu-id="b6579-134">**All, except selected sites**: Type the names of the sites you want to exclude.</span></span>  <span data-ttu-id="b6579-135">Vous pouvez également charger une liste de sites que vous souhaitez refuser de découvrir.</span><span class="sxs-lookup"><span data-stu-id="b6579-135">You can also upload a list of sites that you want to opt out from discovery.</span></span> <span data-ttu-id="b6579-136">Les sites créés à l’avenir seront inclus en tant que sources pour la découverte de rubriques.</span><span class="sxs-lookup"><span data-stu-id="b6579-136">Sites created in future will be included as sources for topic discovery.</span></span> 
    - <span data-ttu-id="b6579-137">**Seuls les sites** sélectionnés : tapez les noms des sites que vous souhaitez inclure.</span><span class="sxs-lookup"><span data-stu-id="b6579-137">**Only selected sites**: Type the names of the sites you want to include.</span></span> <span data-ttu-id="b6579-138">Vous pouvez également charger une liste de sites.</span><span class="sxs-lookup"><span data-stu-id="b6579-138">You can also upload a list of sites.</span></span> <span data-ttu-id="b6579-139">Les sites créés dans le futur ne seront pas inclus comme sources pour la découverte de rubriques.</span><span class="sxs-lookup"><span data-stu-id="b6579-139">Sites created in the future will not be included as sources for topic discovery.</span></span>
    - <span data-ttu-id="b6579-140">**Aucun site** : n’incluez aucun site SharePoint.</span><span class="sxs-lookup"><span data-stu-id="b6579-140">**No sites**: Do not include any SharePoint sites.</span></span>

    ![Choisir comment rechercher des rubriques](../media/ksetup1.png) 
   
5. <span data-ttu-id="b6579-142">Dans la section **Exclure les rubriques par** nom, vous pouvez ajouter des noms de rubriques que vous souhaitez exclure de la découverte de rubriques.</span><span class="sxs-lookup"><span data-stu-id="b6579-142">In the **Exclude topics by name** section, you can add names of topics you want to exclude from topic discovery.</span></span> <span data-ttu-id="b6579-143">Utilisez ce paramètre pour empêcher que des informations sensibles ne figurent dans les rubriques.</span><span class="sxs-lookup"><span data-stu-id="b6579-143">Use this setting to prevent sensitive information from being included as topics.</span></span> <span data-ttu-id="b6579-144">Les options disponibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b6579-144">The options are:</span></span>
    - <span data-ttu-id="b6579-145">**N’exclure aucune rubrique**</span><span class="sxs-lookup"><span data-stu-id="b6579-145">**Don't exclude any topics**</span></span> 
    - <span data-ttu-id="b6579-146">**Exclure les rubriques par nom**</span><span class="sxs-lookup"><span data-stu-id="b6579-146">**Exclude topics by name**</span></span>

    ![Exclure des rubriques](../media/topics-excluded-by-name.png) 

    <span data-ttu-id="b6579-148">(Les gestionnaires de connaissances peuvent également exclure des rubriques dans le centre de rubriques après la découverte.)</span><span class="sxs-lookup"><span data-stu-id="b6579-148">(Knowledge managers can also exclude topics in the topic center after discovery.)</span></span>

    #### <a name="how-to-exclude-topics-by-name"></a><span data-ttu-id="b6579-149">Comment exclure des rubriques par nom</span><span class="sxs-lookup"><span data-stu-id="b6579-149">How to exclude topics by name</span></span>    

    <span data-ttu-id="b6579-150">Si vous devez exclure des rubriques, après avoir sélectionné Exclure les **rubriques** par nom, téléchargez le modèle .csv et mettez-le à jour avec la liste des rubriques que vous souhaitez exclure de vos résultats de découverte.</span><span class="sxs-lookup"><span data-stu-id="b6579-150">If you need to exclude topics, after selecting **Exclude topics by name**, download the .csv template and update it with the list of topics that you want to exclude from your discovery results.</span></span>

    ![Exclure des rubriques dans le modèle CSV](../media/exclude-topics-csv.png) 

    <span data-ttu-id="b6579-152">Dans le modèle CSV, entrez les informations suivantes sur les rubriques à exclure :</span><span class="sxs-lookup"><span data-stu-id="b6579-152">In the CSV template, enter the following information about the topics you want to exclude:</span></span>

    - <span data-ttu-id="b6579-153">**Nom** : tapez le nom de la rubrique à exclure.</span><span class="sxs-lookup"><span data-stu-id="b6579-153">**Name**: Type the name of the topic you want to exclude.</span></span> <span data-ttu-id="b6579-154">Il existe deux méthodes pour y parvenir :</span><span class="sxs-lookup"><span data-stu-id="b6579-154">There are two ways to do this:</span></span>
        - <span data-ttu-id="b6579-155">Correspondance exacte : vous pouvez inclure le nom exact ou l’acronyme (par exemple, *Contoso* ou *ATL*).</span><span class="sxs-lookup"><span data-stu-id="b6579-155">Exact match: You can include the exact name or acronym (for example, *Contoso* or *ATL*).</span></span>
        - <span data-ttu-id="b6579-156">Correspondance partielle : vous pouvez exclure toutes les rubriques qui ont un mot spécifique.</span><span class="sxs-lookup"><span data-stu-id="b6579-156">Partial match: You can exclude all topics that have a specific word in it.</span></span>  <span data-ttu-id="b6579-157">Par exemple, *arc exclura* toutes les rubriques avec le mot *arc* dans celui-ci, telles que le cercle *d’arc,* *l’arc de Pierre ou* *l’arc de formation*. Notez qu’il n’exclura pas les rubriques dans lesquelles le texte est inclus dans le cadre d’un mot, comme *Architecture*.</span><span class="sxs-lookup"><span data-stu-id="b6579-157">For example, *arc* will exclude all topics with the word *arc* in it, such as *Arc circle*, *Plasma arc welding*, or *Training arc*. Note that it will not exclude topics in which the text is included as part of a word, such as *Architecture*.</span></span>
    - <span data-ttu-id="b6579-158">**Signifie (facultatif)**: si vous souhaitez exclure un acronyme, tapez les mots qu’il signifie.</span><span class="sxs-lookup"><span data-stu-id="b6579-158">**Stands for (optional)**: If you want to exclude an acronym, type the words the acronym stands for.</span></span>
    - <span data-ttu-id="b6579-159">**MatchType-Exact/Partial**: tapez si le nom que vous avez entré était un type de correspondance *exacte* *ou* partielle.</span><span class="sxs-lookup"><span data-stu-id="b6579-159">**MatchType-Exact/Partial**: Type whether the name you entered was an *exact* or *partial* match type.</span></span>

    <span data-ttu-id="b6579-160">Une fois que vous avez terminé et enregistré votre fichier .csv, sélectionnez **Parcourir** pour le localiser et le sélectionner.</span><span class="sxs-lookup"><span data-stu-id="b6579-160">After you've completed and saved your .csv file, select **Browse** to locate and select it.</span></span>
    
    <span data-ttu-id="b6579-161">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b6579-161">Select **Next**.</span></span>

6. <span data-ttu-id="b6579-162">Sur la Qui pouvez voir les **rubriques** et où peuvent-elles les voir, vous allez configurer la visibilité des rubriques.</span><span class="sxs-lookup"><span data-stu-id="b6579-162">On the **Who can see topics and where can they see them** page, you will configure topic visibility.</span></span> <span data-ttu-id="b6579-163">Dans la Qui pouvez voir les paramètres des **rubriques,** vous choisissez les personnes qui auront accès aux détails des rubriques, telles que les rubriques mises en évidence, les fiches de rubrique, les réponses aux rubriques dans la recherche et les pages de rubriques.</span><span class="sxs-lookup"><span data-stu-id="b6579-163">In the **Who can see topics** setting, you choose who will have access to topic details, such as highlighted topics, topic cards, topic answers in search, and topic pages.</span></span> <span data-ttu-id="b6579-164">Vous pouvez sélectionner :</span><span class="sxs-lookup"><span data-stu-id="b6579-164">You can select:</span></span>
    - <span data-ttu-id="b6579-165">**Tous les membres de mon organisation**</span><span class="sxs-lookup"><span data-stu-id="b6579-165">**Everyone in my organization**</span></span>
    - <span data-ttu-id="b6579-166">**Personnes ou groupes de sécurité sélectionnés uniquement**</span><span class="sxs-lookup"><span data-stu-id="b6579-166">**Only selected people or security groups**</span></span>
    - <span data-ttu-id="b6579-167">**Personne**</span><span class="sxs-lookup"><span data-stu-id="b6579-167">**No one**</span></span>

    ![Qui pouvez voir les rubriques](../media/ksetup2.png)  

    > [!Note] 
    > <span data-ttu-id="b6579-169">Bien que ce paramètre vous permet de sélectionner n’importe quel utilisateur de votre organisation, seuls les utilisateurs qui ont des licences Expériences des rubriques qui leur sont attribuées pourront afficher les rubriques.</span><span class="sxs-lookup"><span data-stu-id="b6579-169">While this setting allows you to select any user in your organization, only users who have Topic Experiences licenses assigned to them will be able to view topics.</span></span>

7. <span data-ttu-id="b6579-170">Dans la page **Autorisations pour la** gestion des rubriques, vous choisissez qui sera en mesure de créer, modifier ou gérer des rubriques.</span><span class="sxs-lookup"><span data-stu-id="b6579-170">In the **Permissions for topic management** page, you choose who will be able to create, edit, or manage topics.</span></span> <span data-ttu-id="b6579-171">Dans la **section Qui créer et modifier des rubriques,** vous pouvez sélectionner :</span><span class="sxs-lookup"><span data-stu-id="b6579-171">In the **Who can create and edit topics** section, you can select:</span></span>
    - <span data-ttu-id="b6579-172">**Tous les membres de mon organisation**</span><span class="sxs-lookup"><span data-stu-id="b6579-172">**Everyone in my organization**</span></span>
    - <span data-ttu-id="b6579-173">**Personnes ou groupes de sécurité sélectionnés uniquement**</span><span class="sxs-lookup"><span data-stu-id="b6579-173">**Only selected people or security groups**</span></span>
    - <span data-ttu-id="b6579-174">**Personne**</span><span class="sxs-lookup"><span data-stu-id="b6579-174">**No one**</span></span>

    ![Autorisations pour la gestion des rubriques, qui peut créer et modifier des rubriques](../media/ksetup3.png) 

8. <span data-ttu-id="b6579-176">Dans la **section Qui pouvez gérer les rubriques,** vous pouvez sélectionner :</span><span class="sxs-lookup"><span data-stu-id="b6579-176">In the **Who can manage topics** section, you can select:</span></span>
    - <span data-ttu-id="b6579-177">**Tous les membres de mon organisation**</span><span class="sxs-lookup"><span data-stu-id="b6579-177">**Everyone in my organization**</span></span>
    - <span data-ttu-id="b6579-178">**Personnes ou groupes de sécurité sélectionnés uniquement**</span><span class="sxs-lookup"><span data-stu-id="b6579-178">**Only selected people or security groups**</span></span>

    ![Autorisations pour la gestion des rubriques](../media/km-setup-create-edit-topics.png) 

    <span data-ttu-id="b6579-180">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b6579-180">Select **Next**.</span></span>

9. <span data-ttu-id="b6579-181">Dans la page **Créer un** centre de rubriques, vous pouvez créer votre site de centre de rubriques dans lequel les pages de rubriques peuvent être vues et les rubriques peuvent être gérées.</span><span class="sxs-lookup"><span data-stu-id="b6579-181">On the **Create topic center** page, you can create your topic center site in which topic pages can be viewed and topics can be managed.</span></span> <span data-ttu-id="b6579-182">Dans la **zone Nom du site,** tapez un nom pour votre centre de rubriques.</span><span class="sxs-lookup"><span data-stu-id="b6579-182">In the **Site name** box, type a name for your topic center.</span></span> <span data-ttu-id="b6579-183">Vous pouvez éventuellement taper une brève description dans la **zone Description.**</span><span class="sxs-lookup"><span data-stu-id="b6579-183">You can optionally type a short description in the **Description** box.</span></span> 

   <span data-ttu-id="b6579-184">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b6579-184">Select **Next**.</span></span>

   ![Créer un Centre de connaissances](../media/ksetup4.png)  

10. <span data-ttu-id="b6579-186">À la page **Examiner et finaliser**, vous pouvez consulter le paramètre sélectionné, puis choisir d’apporter des modifications.</span><span class="sxs-lookup"><span data-stu-id="b6579-186">On the **Review and finish** page, you can look at your selected setting and choose to make changes.</span></span> <span data-ttu-id="b6579-187">Si vos sélections vous conviennent, sélectionnez **Activer**.</span><span class="sxs-lookup"><span data-stu-id="b6579-187">If you are satisfied with your selections, select **Activate**.</span></span>

11. <span data-ttu-id="b6579-188">La page **Activée rubriques** s’affiche, confirmant que le système va maintenant commencer à analyser les sites sélectionnés pour les rubriques et à créer le site centre de rubriques.</span><span class="sxs-lookup"><span data-stu-id="b6579-188">The **Viva Topics activated** page will display, confirming that the system will now start analyzing your selected sites for topics and creating the topic center site.</span></span> <span data-ttu-id="b6579-189">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="b6579-189">Select **Done**.</span></span>

12. <span data-ttu-id="b6579-190">Vous serez renvoyé à votre page de **Connecter personnes à la** page de connaissances.</span><span class="sxs-lookup"><span data-stu-id="b6579-190">You'll be returned to your **Connect people to knowledge** page.</span></span> <span data-ttu-id="b6579-191">Dans cette page, vous pouvez sélectionner **Gérer** pour modifier vos paramètres de configuration.</span><span class="sxs-lookup"><span data-stu-id="b6579-191">From this page, you can select **Manage** to make any changes to your configuration settings.</span></span> 

    ![Paramètres appliqué](../media/ksetup7.png)    

<span data-ttu-id="b6579-193">Notez que la première fois que la découverte de rubrique est activée, l’affichage Gérer les rubriques peut prendre jusqu’à deux semaines pour que toutes les rubriques suggérées apparaissent.</span><span class="sxs-lookup"><span data-stu-id="b6579-193">Note that the first time topic discovery is enabled, it may take up to two weeks for all suggested topics to appear in the Manage Topics view.</span></span> <span data-ttu-id="b6579-194">La découverte de rubriques se poursuit au cours de la mise à jour ou de la mise à jour du contenu.</span><span class="sxs-lookup"><span data-stu-id="b6579-194">Topic discovery continues as new content or updates to content are made.</span></span> <span data-ttu-id="b6579-195">Il est normal d’avoir des variations dans le nombre de rubriques suggérées dans votre organisation, car Topics évalue de nouvelles informations.</span><span class="sxs-lookup"><span data-stu-id="b6579-195">It is normal to have fluctuations in the number of suggested topics in your organization as Viva Topics evaluates new information.</span></span>

## <a name="manage-topic-experiences"></a><span data-ttu-id="b6579-196">Gérer les expériences de rubrique</span><span class="sxs-lookup"><span data-stu-id="b6579-196">Manage topic experiences</span></span>

<span data-ttu-id="b6579-197">Une fois que vous avez configuré Rubriques, vous pouvez modifier les paramètres que vous avez choisis lors de l’installation dans [Microsoft 365 centre d’administration.](https://admin.microsoft.com/AdminPortal#/featureexplorer/csi/KnowledgeManagement)</span><span class="sxs-lookup"><span data-stu-id="b6579-197">Once you have set up Topics, you can change the settings that you chose during setup in the [Microsoft 365 admin center](https://admin.microsoft.com/AdminPortal#/featureexplorer/csi/KnowledgeManagement).</span></span> <span data-ttu-id="b6579-198">Si vous souhaitez en savoir plus, veuillez consulter les références suivantes :</span><span class="sxs-lookup"><span data-stu-id="b6579-198">See the following references:</span></span>

- [<span data-ttu-id="b6579-199">Gérer la découverte de rubriques dans les rubriques microsoft</span><span class="sxs-lookup"><span data-stu-id="b6579-199">Manage topic discovery in Microsoft Viva Topics</span></span>](topic-experiences-discovery.md)
- [<span data-ttu-id="b6579-200">Gérer la visibilité des rubriques dans les rubriques microsoft</span><span class="sxs-lookup"><span data-stu-id="b6579-200">Manage topic visibility in Microsoft Viva Topics</span></span>](topic-experiences-knowledge-rules.md)
- [<span data-ttu-id="b6579-201">Gérer les autorisations des rubriques dans les rubriques microsoft</span><span class="sxs-lookup"><span data-stu-id="b6579-201">Manage topic permissions in Microsoft Viva Topics</span></span>](topic-experiences-user-permissions.md)
- [<span data-ttu-id="b6579-202">Modifier le nom du centre de rubriques dans Rubriques microsoft</span><span class="sxs-lookup"><span data-stu-id="b6579-202">Change the name of the topic center in Microsoft Viva Topics</span></span>](topic-experiences-administration.md)

## <a name="see-also"></a><span data-ttu-id="b6579-203">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6579-203">See also</span></span>

[<span data-ttu-id="b6579-204">Vue d’ensemble des expériences de rubrique</span><span class="sxs-lookup"><span data-stu-id="b6579-204">Topic Experiences Overview</span></span>](topic-experiences-overview.md)
