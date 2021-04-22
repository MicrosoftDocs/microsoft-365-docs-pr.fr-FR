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
# <a name="set-up-microsoft-viva-topics"></a><span data-ttu-id="cc828-103">Configurer Les rubriques microsoft</span><span class="sxs-lookup"><span data-stu-id="cc828-103">Set up Microsoft Viva Topics</span></span>

<span data-ttu-id="cc828-104">Vous pouvez utiliser le Centre d'administration Microsoft 365 pour configurer les [rubriques.](topic-experiences-overview.md)</span><span class="sxs-lookup"><span data-stu-id="cc828-104">You can use the Microsoft 365 admin center to set up and configure [Topics](topic-experiences-overview.md).</span></span> 

<span data-ttu-id="cc828-105">Il est important de planifier la meilleure façon de configurer des rubriques dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="cc828-105">It is important to plan the best way to set up and configure topics in your environment.</span></span> <span data-ttu-id="cc828-106">Veillez à lire [les rubriques planifier microsoft avant](plan-topic-experiences.md) de commencer les procédures de cet article.</span><span class="sxs-lookup"><span data-stu-id="cc828-106">Be sure to read [Plan for Microsoft Viva Topics](plan-topic-experiences.md) before you begin the procedures in this article.</span></span>

<span data-ttu-id="cc828-107">Vous devez être abonné à [Rubriques Et](https://www.microsoft.com/microsoft-viva/topics) être administrateur général ou administrateur SharePoint pour accéder au Centre d'administration Microsoft 365 et configurer Rubriques.</span><span class="sxs-lookup"><span data-stu-id="cc828-107">You must be [subscribed to Viva Topics](https://www.microsoft.com/microsoft-viva/topics) and be a global administrator or SharePoint administrator to access the Microsoft 365 admin center and set up Topics.</span></span>

<span data-ttu-id="cc828-108">Si vous avez configuré [](/sharepoint/control-access-from-unmanaged-devices)SharePoint pour exiger des appareils gérés, assurez-vous de configurer les rubriques à partir d'un appareil géré.</span><span class="sxs-lookup"><span data-stu-id="cc828-108">If you have configured SharePoint to [require managed devices](/sharepoint/control-access-from-unmanaged-devices), be sure to set up Topics from a managed device.</span></span>

## <a name="video-demonstration"></a><span data-ttu-id="cc828-109">Démonstration vidéo</span><span class="sxs-lookup"><span data-stu-id="cc828-109">Video demonstration</span></span>

<span data-ttu-id="cc828-110">Cette vidéo montre le processus de configuration des rubriques dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cc828-110">This video shows the process for setting up Topics in Microsoft 365.</span></span>

<br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4Li0E]  

<br>

## <a name="assign-licenses"></a><span data-ttu-id="cc828-111">Attribuer des licences</span><span class="sxs-lookup"><span data-stu-id="cc828-111">Assign licenses</span></span>

<span data-ttu-id="cc828-112">Vous devez attribuer des licences pour les utilisateurs qui utiliseront Rubriques.</span><span class="sxs-lookup"><span data-stu-id="cc828-112">You must assign licenses for the users who will be using Topics.</span></span> <span data-ttu-id="cc828-113">Seuls les utilisateurs titulaires d'une licence peuvent voir des informations sur des sujets tels que les points forts, les cartes de rubrique, les pages de rubriques et le centre de rubriques.</span><span class="sxs-lookup"><span data-stu-id="cc828-113">Only users with a license can see information on topics including highlights, topic cards, topic pages and the topic center.</span></span> 

<span data-ttu-id="cc828-114">Pour attribuer des licences :</span><span class="sxs-lookup"><span data-stu-id="cc828-114">To assign licenses:</span></span>

1. <span data-ttu-id="cc828-115">Dans le Centre d’administration Microsoft 365, sous **Utilisateurs**, cliquez sur **Utilisateurs actifs**.</span><span class="sxs-lookup"><span data-stu-id="cc828-115">In the Microsoft 365 admin center, under **Users**, click **Active users**.</span></span>

2. <span data-ttu-id="cc828-116">Sélectionnez les utilisateurs que vous souhaitez obtenir une licence, puis cliquez **sur Licences et applications.**</span><span class="sxs-lookup"><span data-stu-id="cc828-116">Select the users that you want to license, and click **Licenses and apps**.</span></span>

3. <span data-ttu-id="cc828-117">Sous **Licences,** **sélectionnez Rubriques Titre.**</span><span class="sxs-lookup"><span data-stu-id="cc828-117">Under **Licenses**, select **Viva Topics**.</span></span>

4. <span data-ttu-id="cc828-118">Sous **Applications,** assurez-vous **que les rubriques Recherche des connecteurs Graph avec index (Rubriques)** et **Rubriques De** la sélection sont toutes les deux sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="cc828-118">Under **Apps**, make sure **Graph Connectors Search with Index (Viva Topics)** and **Viva Topics** are both selected.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="cc828-119">![Licences Rubriques Microsoft dans le Centre d'administration Microsoft 365](../media/topic-experiences-licenses.png)</span><span class="sxs-lookup"><span data-stu-id="cc828-119">![Microsoft Viva Topics licenses in the Microsoft 365 admin center](../media/topic-experiences-licenses.png)</span></span>

5. <span data-ttu-id="cc828-120">Cliquez sur **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="cc828-120">Click **Save changes**.</span></span>

<span data-ttu-id="cc828-121">Une fois les licences attribuées, l'accès aux rubriques peut prendre jusqu'à une heure.</span><span class="sxs-lookup"><span data-stu-id="cc828-121">It may take up to an hour for users to get access to Topics after the licenses are assigned.</span></span>

## <a name="set-up-topics"></a><span data-ttu-id="cc828-122">Configurer les rubriques</span><span class="sxs-lookup"><span data-stu-id="cc828-122">Set up Topics</span></span>

<span data-ttu-id="cc828-123">Pour configurer des rubriques</span><span class="sxs-lookup"><span data-stu-id="cc828-123">To set up Topics</span></span>

1. <span data-ttu-id="cc828-124">Dans le [Centre d'administration Microsoft 365,](https://admin.microsoft.com)sélectionnez **Installation,** puis affichez la section Fichiers **et** contenu.</span><span class="sxs-lookup"><span data-stu-id="cc828-124">In the [Microsoft 365 admin center](https://admin.microsoft.com), select **Setup**, and then view the **Files and content** section.</span></span>
2. <span data-ttu-id="cc828-125">Dans la section **Fichiers et contenu,** cliquez **sur Connecter les personnes aux connaissances.**</span><span class="sxs-lookup"><span data-stu-id="cc828-125">In the **Files and content** section, click **Connect people to knowledge**.</span></span>

    ![Connecter les personnes aux connaissances](../media/admin-org-knowledge-options.png) 

3. <span data-ttu-id="cc828-127">Dans la page **Connecter des personnes aux connaissances,** cliquez sur **Commencer** pour vous aider dans le processus de configuration.</span><span class="sxs-lookup"><span data-stu-id="cc828-127">On the **Connect people to knowledge** page, click **Get started** to walk you through the setup process.</span></span>

    ![Prise en main](../media/k-get-started.png) 

4. <span data-ttu-id="cc828-129">Dans la page Choisir la façon dont Topics peut trouver des **rubriques,** vous allez configurer la découverte de rubriques.</span><span class="sxs-lookup"><span data-stu-id="cc828-129">On the **Choose how Viva Topics can find topics** page, you will configure topic discovery.</span></span> <span data-ttu-id="cc828-130">Dans la section Sélectionner des sources de rubrique **SharePoint,** sélectionnez les sites SharePoint à analyser en tant que sources pour vos rubriques lors de la découverte.</span><span class="sxs-lookup"><span data-stu-id="cc828-130">In the **Select SharePoint topic sources** section, select which SharePoint sites will be crawled as sources for your topics during discovery.</span></span> <span data-ttu-id="cc828-131">Choisissez parmi les autorisations suivantes :</span><span class="sxs-lookup"><span data-stu-id="cc828-131">Choose from:</span></span>
    - <span data-ttu-id="cc828-132">**Tous les sites**: tous les sites SharePoint de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cc828-132">**All sites**: All SharePoint sites in your organization.</span></span> <span data-ttu-id="cc828-133">Cela inclut les sites actuels et futurs.</span><span class="sxs-lookup"><span data-stu-id="cc828-133">This includes current and future sites.</span></span>
    - <span data-ttu-id="cc828-134">**Tous, sauf les sites sélectionnés**: tapez les noms des sites que vous souhaitez exclure.</span><span class="sxs-lookup"><span data-stu-id="cc828-134">**All, except selected sites**: Type the names of the sites you want to exclude.</span></span>  <span data-ttu-id="cc828-135">Vous pouvez également charger une liste de sites que vous souhaitez refuser de découvrir.</span><span class="sxs-lookup"><span data-stu-id="cc828-135">You can also upload a list of sites that you want to opt out from discovery.</span></span> <span data-ttu-id="cc828-136">Les sites créés à l'avenir seront inclus en tant que sources pour la découverte de rubriques.</span><span class="sxs-lookup"><span data-stu-id="cc828-136">Sites created in future will be included as sources for topic discovery.</span></span> 
    - <span data-ttu-id="cc828-137">**Seuls les sites** sélectionnés : tapez les noms des sites que vous souhaitez inclure.</span><span class="sxs-lookup"><span data-stu-id="cc828-137">**Only selected sites**: Type the names of the sites you want to include.</span></span> <span data-ttu-id="cc828-138">Vous pouvez également charger une liste de sites.</span><span class="sxs-lookup"><span data-stu-id="cc828-138">You can also upload a list of sites.</span></span> <span data-ttu-id="cc828-139">Les sites créés à l'avenir ne seront pas inclus en tant que sources de découverte de sujet.</span><span class="sxs-lookup"><span data-stu-id="cc828-139">Sites created in the future will not be included as sources for topic discovery.</span></span>
    - <span data-ttu-id="cc828-140">**Aucun site**: n'incluez aucun site SharePoint.</span><span class="sxs-lookup"><span data-stu-id="cc828-140">**No sites**: Do not include any SharePoint sites.</span></span>

    ![Choisir comment rechercher des rubriques](../media/ksetup1.png) 
   
5. <span data-ttu-id="cc828-142">Dans la section **Exclure les rubriques par** nom, vous pouvez ajouter des noms de rubriques que vous souhaitez exclure de la découverte de rubriques.</span><span class="sxs-lookup"><span data-stu-id="cc828-142">In the **Exclude topics by name** section, you can add names of topics you want to exclude from topic discovery.</span></span> <span data-ttu-id="cc828-143">Utilisez ce paramètre pour empêcher que des informations sensibles ne figurent dans les rubriques.</span><span class="sxs-lookup"><span data-stu-id="cc828-143">Use this setting to prevent sensitive information from being included as topics.</span></span> <span data-ttu-id="cc828-144">Les options disponibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="cc828-144">The options are:</span></span>
    - <span data-ttu-id="cc828-145">**N'excluez aucune rubrique**</span><span class="sxs-lookup"><span data-stu-id="cc828-145">**Don't exclude any topics**</span></span> 
    - <span data-ttu-id="cc828-146">**Exclure des rubriques par nom**</span><span class="sxs-lookup"><span data-stu-id="cc828-146">**Exclude topics by name**</span></span>

    ![Exclure des rubriques](../media/topics-excluded-by-name.png) 

    <span data-ttu-id="cc828-148">(Les gestionnaires de connaissances peuvent également exclure les rubriques du centre de rubriques après la découverte.)</span><span class="sxs-lookup"><span data-stu-id="cc828-148">(Knowledge managers can also exclude topics in the topic center after discovery.)</span></span>

    #### <a name="how-to-exclude-topics-by-name"></a><span data-ttu-id="cc828-149">Comment exclure des rubriques par nom</span><span class="sxs-lookup"><span data-stu-id="cc828-149">How to exclude topics by name</span></span>    

    <span data-ttu-id="cc828-150">Si vous devez exclure des rubriques, après avoir sélectionné Exclure les **rubriques** par nom, téléchargez le modèle .csv et mettez-le à jour avec la liste des rubriques que vous souhaitez exclure de vos résultats de découverte.</span><span class="sxs-lookup"><span data-stu-id="cc828-150">If you need to exclude topics, after selecting **Exclude topics by name**, download the .csv template and update it with the list of topics that you want to exclude from your discovery results.</span></span>

    ![Exclure des rubriques dans le modèle CSV](../media/exclude-topics-csv.png) 

    <span data-ttu-id="cc828-152">Dans le modèle CSV, entrez les informations suivantes sur les rubriques que vous souhaitez exclure :</span><span class="sxs-lookup"><span data-stu-id="cc828-152">In the CSV template, enter the following information about the topics you want to exclude:</span></span>

    - <span data-ttu-id="cc828-153">**Nom**: tapez le nom de la rubrique que vous souhaitez exclure.</span><span class="sxs-lookup"><span data-stu-id="cc828-153">**Name**: Type the name of the topic you want to exclude.</span></span> <span data-ttu-id="cc828-154">Vous pouvez procéder de deux manières :</span><span class="sxs-lookup"><span data-stu-id="cc828-154">There are two ways to do this:</span></span>
        - <span data-ttu-id="cc828-155">Correspondance exacte : vous pouvez inclure le nom exact ou l'acronyme (par exemple, *Contoso* ou *ATL*).</span><span class="sxs-lookup"><span data-stu-id="cc828-155">Exact match: You can include the exact name or acronym (for example, *Contoso* or *ATL*).</span></span>
        - <span data-ttu-id="cc828-156">Correspondance partielle : vous pouvez exclure toutes les rubriques qui ont un mot spécifique.</span><span class="sxs-lookup"><span data-stu-id="cc828-156">Partial match: You can exclude all topics that have a specific word in it.</span></span>  <span data-ttu-id="cc828-157">Par exemple, *arc exclura* toutes les rubriques avec le mot *arc* dans celui-ci, telles que le cercle *d'arc,* *l'arc de Pierre ou* *l'arc de formation*. Notez qu'il n'exclura pas les rubriques dans lesquelles le texte est inclus dans le cadre d'un mot, comme *Architecture*.</span><span class="sxs-lookup"><span data-stu-id="cc828-157">For example, *arc* will exclude all topics with the word *arc* in it, such as *Arc circle*, *Plasma arc welding*, or *Training arc*. Note that it will not exclude topics in which the text is included as part of a word, such as *Architecture*.</span></span>
    - <span data-ttu-id="cc828-158">**Signifie (facultatif)**: si vous souhaitez exclure un acronyme, tapez les mots qu'il signifie.</span><span class="sxs-lookup"><span data-stu-id="cc828-158">**Stands for (optional)**: If you want to exclude an acronym, type the words the acronym stands for.</span></span>
    - <span data-ttu-id="cc828-159">**MatchType-Exact/Partial**: tapez si le nom que vous avez entré était un type de correspondance *exact* *ou* partiel.</span><span class="sxs-lookup"><span data-stu-id="cc828-159">**MatchType-Exact/Partial**: Type whether the name you entered was an *exact* or *partial* match type.</span></span>

    <span data-ttu-id="cc828-160">Une fois que vous avez terminé et enregistré votre fichier .csv, sélectionnez **Parcourir** pour le localiser et le sélectionner.</span><span class="sxs-lookup"><span data-stu-id="cc828-160">After you've completed and saved your .csv file, select **Browse** to locate and select it.</span></span>
    
    <span data-ttu-id="cc828-161">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cc828-161">Select **Next**.</span></span>

6. <span data-ttu-id="cc828-162">Dans la page **Qui peut voir les rubriques** et où peuvent-ils les voir, vous allez configurer la visibilité des rubriques.</span><span class="sxs-lookup"><span data-stu-id="cc828-162">On the **Who can see topics and where can they see them** page, you will configure topic visibility.</span></span> <span data-ttu-id="cc828-163">Dans le paramètre Qui peut voir les **rubriques,** vous choisissez les personnes qui auront accès aux détails des rubriques, telles que les rubriques mises en évidence, les fiches de rubrique, les réponses aux rubriques dans la recherche et les pages de rubriques.</span><span class="sxs-lookup"><span data-stu-id="cc828-163">In the **Who can see topics** setting, you choose who will have access to topic details, such as highlighted topics, topic cards, topic answers in search, and topic pages.</span></span> <span data-ttu-id="cc828-164">Vous pouvez sélectionner :</span><span class="sxs-lookup"><span data-stu-id="cc828-164">You can select:</span></span>
    - <span data-ttu-id="cc828-165">**Tous les membres de mon organisation**</span><span class="sxs-lookup"><span data-stu-id="cc828-165">**Everyone in my organization**</span></span>
    - <span data-ttu-id="cc828-166">**Personnes ou groupes de sécurité sélectionnés uniquement**</span><span class="sxs-lookup"><span data-stu-id="cc828-166">**Only selected people or security groups**</span></span>
    - <span data-ttu-id="cc828-167">**Personne**</span><span class="sxs-lookup"><span data-stu-id="cc828-167">**No one**</span></span>

    ![Personnes qui peuvent voir les rubriques](../media/ksetup2.png)  

    > [!Note] 
    > <span data-ttu-id="cc828-169">Bien que ce paramètre vous permet de sélectionner n'importe quel utilisateur de votre organisation, seuls les utilisateurs qui ont des licences Expériences des rubriques qui leur sont attribuées pourront afficher les rubriques.</span><span class="sxs-lookup"><span data-stu-id="cc828-169">While this setting allows you to select any user in your organization, only users who have Topic Experiences licenses assigned to them will be able to view topics.</span></span>

7. <span data-ttu-id="cc828-170">Dans la page **Autorisations pour la** gestion des rubriques, vous choisissez qui sera en mesure de créer, modifier ou gérer des rubriques.</span><span class="sxs-lookup"><span data-stu-id="cc828-170">In the **Permissions for topic management** page, you choose who will be able to create, edit, or manage topics.</span></span> <span data-ttu-id="cc828-171">Dans la section **Qui peut créer et modifier des rubriques,** vous pouvez sélectionner :</span><span class="sxs-lookup"><span data-stu-id="cc828-171">In the **Who can create and edit topics** section, you can select:</span></span>
    - <span data-ttu-id="cc828-172">**Tous les membres de mon organisation**</span><span class="sxs-lookup"><span data-stu-id="cc828-172">**Everyone in my organization**</span></span>
    - <span data-ttu-id="cc828-173">**Personnes ou groupes de sécurité sélectionnés uniquement**</span><span class="sxs-lookup"><span data-stu-id="cc828-173">**Only selected people or security groups**</span></span>
    - <span data-ttu-id="cc828-174">**Personne**</span><span class="sxs-lookup"><span data-stu-id="cc828-174">**No one**</span></span>

    ![Autorisations pour la gestion des rubriques, qui peut créer et modifier des rubriques](../media/ksetup3.png) 

8. <span data-ttu-id="cc828-176">Dans la section **Qui peut gérer les rubriques,** vous pouvez sélectionner :</span><span class="sxs-lookup"><span data-stu-id="cc828-176">In the **Who can manage topics** section, you can select:</span></span>
    - <span data-ttu-id="cc828-177">**Tous les membres de mon organisation**</span><span class="sxs-lookup"><span data-stu-id="cc828-177">**Everyone in my organization**</span></span>
    - <span data-ttu-id="cc828-178">**Personnes ou groupes de sécurité sélectionnés uniquement**</span><span class="sxs-lookup"><span data-stu-id="cc828-178">**Only selected people or security groups**</span></span>

    ![Autorisations pour la gestion des rubriques](../media/km-setup-create-edit-topics.png) 

    <span data-ttu-id="cc828-180">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cc828-180">Select **Next**.</span></span>

9. <span data-ttu-id="cc828-181">Dans la page **Créer un** centre de rubriques, vous pouvez créer votre site de centre de rubriques dans lequel les pages de rubriques peuvent être vues et les rubriques peuvent être gérées.</span><span class="sxs-lookup"><span data-stu-id="cc828-181">On the **Create topic center** page, you can create your topic center site in which topic pages can be viewed and topics can be managed.</span></span> <span data-ttu-id="cc828-182">Dans la **zone Nom du site,** tapez un nom pour votre centre de rubriques.</span><span class="sxs-lookup"><span data-stu-id="cc828-182">In the **Site name** box, type a name for your topic center.</span></span> <span data-ttu-id="cc828-183">Vous pouvez éventuellement taper une brève description dans la **zone Description.**</span><span class="sxs-lookup"><span data-stu-id="cc828-183">You can optionally type a short description in the **Description** box.</span></span> 

   <span data-ttu-id="cc828-184">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="cc828-184">Select **Next**.</span></span>

   ![Créer le Centre de connaissances](../media/ksetup4.png)  

10. <span data-ttu-id="cc828-186">À la page **Examiner et finaliser**, vous pouvez consulter le paramètre sélectionné, puis choisir d’apporter des modifications.</span><span class="sxs-lookup"><span data-stu-id="cc828-186">On the **Review and finish** page, you can look at your selected setting and choose to make changes.</span></span> <span data-ttu-id="cc828-187">Si vos sélections vous conviennent, sélectionnez **Activer**.</span><span class="sxs-lookup"><span data-stu-id="cc828-187">If you are satisfied with your selections, select **Activate**.</span></span>

11. <span data-ttu-id="cc828-188">La page **Rubriques** activée s'affiche, confirmant que le système va maintenant commencer à analyser les sites sélectionnés pour les rubriques et à créer le site centre de rubriques.</span><span class="sxs-lookup"><span data-stu-id="cc828-188">The **Viva Topics activated** page will display, confirming that the system will now start analyzing your selected sites for topics and creating the topic center site.</span></span> <span data-ttu-id="cc828-189">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="cc828-189">Select **Done**.</span></span>

12. <span data-ttu-id="cc828-190">Vous serez renvoyé à votre page De **connexion des personnes à la** base de connaissances.</span><span class="sxs-lookup"><span data-stu-id="cc828-190">You'll be returned to your **Connect people to knowledge** page.</span></span> <span data-ttu-id="cc828-191">Dans cette page, vous pouvez sélectionner **Gérer** pour modifier vos paramètres de configuration.</span><span class="sxs-lookup"><span data-stu-id="cc828-191">From this page, you can select **Manage** to make any changes to your configuration settings.</span></span> 

    ![Paramètres appliqués](../media/ksetup7.png)    

<span data-ttu-id="cc828-193">Notez que la première fois que la découverte de rubrique est activée, l'affichage De toutes les rubriques suggérées dans l'affichage Gérer les rubriques peut prendre jusqu'à deux semaines.</span><span class="sxs-lookup"><span data-stu-id="cc828-193">Note that the first time topic discovery is enabled, it may take up to two weeks for all suggested topics to appear in the Manage Topics view.</span></span> <span data-ttu-id="cc828-194">La découverte de rubriques se poursuit à mesure que de nouveaux contenus ou mises à jour du contenu sont effectués.</span><span class="sxs-lookup"><span data-stu-id="cc828-194">Topic discovery continues as new content or updates to content are made.</span></span> <span data-ttu-id="cc828-195">Il est normal d'avoir des variations dans le nombre de rubriques suggérées dans votre organisation, car Rubriques de Rubriques évalue de nouvelles informations.</span><span class="sxs-lookup"><span data-stu-id="cc828-195">It is normal to have fluctuations in the number of suggested topics in your organization as Viva Topics evaluates new information.</span></span>

## <a name="manage-topic-experiences"></a><span data-ttu-id="cc828-196">Gérer les expériences de rubrique</span><span class="sxs-lookup"><span data-stu-id="cc828-196">Manage topic experiences</span></span>

<span data-ttu-id="cc828-197">Une fois que vous avez configuré Rubriques, vous pouvez modifier les paramètres que vous avez choisis lors de l'installation dans le Centre d'administration [Microsoft 365.](https://admin.microsoft.com/AdminPortal#/featureexplorer/csi/KnowledgeManagement)</span><span class="sxs-lookup"><span data-stu-id="cc828-197">Once you have set up Topics, you can change the settings that you chose during setup in the [Microsoft 365 admin center](https://admin.microsoft.com/AdminPortal#/featureexplorer/csi/KnowledgeManagement).</span></span> <span data-ttu-id="cc828-198">Si vous souhaitez en savoir plus, veuillez consulter les références suivantes :</span><span class="sxs-lookup"><span data-stu-id="cc828-198">See the following references:</span></span>

- [<span data-ttu-id="cc828-199">Gérer la découverte de rubriques dans les rubriques microsoft</span><span class="sxs-lookup"><span data-stu-id="cc828-199">Manage topic discovery in Microsoft Viva Topics</span></span>](topic-experiences-discovery.md)
- [<span data-ttu-id="cc828-200">Gérer la visibilité des rubriques dans les rubriques microsoft</span><span class="sxs-lookup"><span data-stu-id="cc828-200">Manage topic visibility in Microsoft Viva Topics</span></span>](topic-experiences-knowledge-rules.md)
- [<span data-ttu-id="cc828-201">Gérer les autorisations des rubriques dans les rubriques microsoft</span><span class="sxs-lookup"><span data-stu-id="cc828-201">Manage topic permissions in Microsoft Viva Topics</span></span>](topic-experiences-user-permissions.md)
- [<span data-ttu-id="cc828-202">Modifier le nom du centre de rubriques dans Rubriques microsoft</span><span class="sxs-lookup"><span data-stu-id="cc828-202">Change the name of the topic center in Microsoft Viva Topics</span></span>](topic-experiences-administration.md)

## <a name="see-also"></a><span data-ttu-id="cc828-203">Articles associés</span><span class="sxs-lookup"><span data-stu-id="cc828-203">See also</span></span>

[<span data-ttu-id="cc828-204">Vue d'ensemble des expériences de rubrique</span><span class="sxs-lookup"><span data-stu-id="cc828-204">Topic Experiences Overview</span></span>](topic-experiences-overview.md)
