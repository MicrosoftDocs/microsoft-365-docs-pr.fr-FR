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
ms.openlocfilehash: 42f84b9b792907d7fe118e0b15c3767674ddf19b
ms.sourcegitcommit: 48195345b21b409b175d68acdc25d9f2fc4fc5f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "53229586"
---
# <a name="set-up-microsoft-viva-topics"></a><span data-ttu-id="82b15-103">Configurer Les rubriques microsoft</span><span class="sxs-lookup"><span data-stu-id="82b15-103">Set up Microsoft Viva Topics</span></span>

<span data-ttu-id="82b15-104">Vous pouvez utiliser la Centre d’administration Microsoft 365 pour configurer des [rubriques.](topic-experiences-overview.md)</span><span class="sxs-lookup"><span data-stu-id="82b15-104">You can use the Microsoft 365 admin center to set up and configure [Topics](topic-experiences-overview.md).</span></span> 

<span data-ttu-id="82b15-105">Il est important de planifier la meilleure façon de configurer des rubriques dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="82b15-105">It is important to plan the best way to set up and configure topics in your environment.</span></span> <span data-ttu-id="82b15-106">Veillez à lire [les rubriques planifier microsoft avant](plan-topic-experiences.md) de commencer les procédures de cet article.</span><span class="sxs-lookup"><span data-stu-id="82b15-106">Be sure to read [Plan for Microsoft Viva Topics](plan-topic-experiences.md) before you begin the procedures in this article.</span></span>

<span data-ttu-id="82b15-107">Vous devez être [abonné à Rubriques Et](https://www.microsoft.com/microsoft-viva/topics) être administrateur général ou administrateur SharePoint pour accéder à la Centre d’administration Microsoft 365 et configurer Rubriques.</span><span class="sxs-lookup"><span data-stu-id="82b15-107">You must be [subscribed to Viva Topics](https://www.microsoft.com/microsoft-viva/topics) and be a global administrator or SharePoint administrator to access the Microsoft 365 admin center and set up Topics.</span></span>

<span data-ttu-id="82b15-108">Si vous avez configuré SharePoint pour exiger [des](/sharepoint/control-access-from-unmanaged-devices)appareils gérés, assurez-vous de configurer les rubriques à partir d’un appareil géré.</span><span class="sxs-lookup"><span data-stu-id="82b15-108">If you have configured SharePoint to [require managed devices](/sharepoint/control-access-from-unmanaged-devices), be sure to set up Topics from a managed device.</span></span>

## <a name="video-demonstration"></a><span data-ttu-id="82b15-109">Démonstration vidéo</span><span class="sxs-lookup"><span data-stu-id="82b15-109">Video demonstration</span></span>

<span data-ttu-id="82b15-110">Cette vidéo montre le processus de configuration des rubriques dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="82b15-110">This video shows the process for setting up Topics in Microsoft 365.</span></span>

<br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4Li0E]  

<br>

## <a name="assign-licenses"></a><span data-ttu-id="82b15-111">Attribuer les licences</span><span class="sxs-lookup"><span data-stu-id="82b15-111">Assign licenses</span></span>

<span data-ttu-id="82b15-112">Vous devez attribuer des licences pour les utilisateurs qui utiliseront Rubriques.</span><span class="sxs-lookup"><span data-stu-id="82b15-112">You must assign licenses for the users who will be using Topics.</span></span> <span data-ttu-id="82b15-113">Seuls les utilisateurs disposant d’une licence peuvent voir des informations sur les sujets, notamment les points forts, les cartes de rubriques, les pages de rubriques et le centre thématique.</span><span class="sxs-lookup"><span data-stu-id="82b15-113">Only users with a license can see information on topics including highlights, topic cards, topic pages and the topic center.</span></span> 

<span data-ttu-id="82b15-114">Pour attribuer des licences :</span><span class="sxs-lookup"><span data-stu-id="82b15-114">To assign licenses:</span></span>

1. <span data-ttu-id="82b15-115">Dans le Centre d’administration Microsoft 365, sous **Utilisateurs**, cliquez sur **Utilisateurs actifs**.</span><span class="sxs-lookup"><span data-stu-id="82b15-115">In the Microsoft 365 admin center, under **Users**, click **Active users**.</span></span>

2. <span data-ttu-id="82b15-116">Sélectionnez les utilisateurs que vous souhaitez obtenir une licence, puis cliquez **sur Licences et applications.**</span><span class="sxs-lookup"><span data-stu-id="82b15-116">Select the users that you want to license, and click **Licenses and apps**.</span></span>

3. <span data-ttu-id="82b15-117">Sous **Licences,** **sélectionnez Rubriques Titre.**</span><span class="sxs-lookup"><span data-stu-id="82b15-117">Under **Licenses**, select **Viva Topics**.</span></span>

4. <span data-ttu-id="82b15-118">Sous **Applications,** assurez-vous **que Graph connectors search with Index (Topics)** et **Topics Topics sont** tous deux sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="82b15-118">Under **Apps**, make sure **Graph Connectors Search with Index (Viva Topics)** and **Viva Topics** are both selected.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="82b15-119">![Licences Microsoft Topics dans le Centre d’administration Microsoft 365](../media/topic-experiences-licenses.png)</span><span class="sxs-lookup"><span data-stu-id="82b15-119">![Microsoft Viva Topics licenses in the Microsoft 365 admin center](../media/topic-experiences-licenses.png)</span></span>

5. <span data-ttu-id="82b15-120">Cliquez sur **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="82b15-120">Click **Save changes**.</span></span>

<span data-ttu-id="82b15-121">Une fois les licences attribuées, l’accès aux rubriques peut prendre jusqu’à une heure.</span><span class="sxs-lookup"><span data-stu-id="82b15-121">It may take up to an hour for users to get access to Topics after the licenses are assigned.</span></span>

## <a name="set-up-topics"></a><span data-ttu-id="82b15-122">Configurer les rubriques</span><span class="sxs-lookup"><span data-stu-id="82b15-122">Set up Topics</span></span>

> [!Note]
> <span data-ttu-id="82b15-123">La première fois que la découverte de rubrique est activée, l’affichage De toutes les rubriques suggérées dans l’affichage Gérer les rubriques peut prendre jusqu’à deux semaines.</span><span class="sxs-lookup"><span data-stu-id="82b15-123">The first time topic discovery is enabled, it may take up to two weeks for all suggested topics to appear in the Manage Topics view.</span></span> <span data-ttu-id="82b15-124">La découverte de rubriques se poursuit au cours de la mise à jour ou de la mise à jour du contenu.</span><span class="sxs-lookup"><span data-stu-id="82b15-124">Topic discovery continues as new content or updates to content are made.</span></span> <span data-ttu-id="82b15-125">Il est normal d’avoir des fluctuations dans le nombre de rubriques suggérées dans votre organisation, car les Rubriques Viva évaluent de nouvelles informations.</span><span class="sxs-lookup"><span data-stu-id="82b15-125">It is normal to have fluctuations in the number of suggested topics in your organization as Viva Topics evaluates new information.</span></span>

<span data-ttu-id="82b15-126">Pour configurer des rubriques</span><span class="sxs-lookup"><span data-stu-id="82b15-126">To set up Topics</span></span>
1. <span data-ttu-id="82b15-127">Dans la [Centre d’administration Microsoft 365,](https://admin.microsoft.com)sélectionnez **Installation,** puis affichez la section **Fichiers et** contenu.</span><span class="sxs-lookup"><span data-stu-id="82b15-127">In the [Microsoft 365 admin center](https://admin.microsoft.com), select **Setup**, and then view the **Files and content** section.</span></span>
2. <span data-ttu-id="82b15-128">Dans la section **Fichiers et contenu,** cliquez **Connecter personnes à connaître.**</span><span class="sxs-lookup"><span data-stu-id="82b15-128">In the **Files and content** section, click **Connect people to knowledge**.</span></span>

    ![Connecter personnes à connaître](../media/admin-org-knowledge-options.png) 

3. <span data-ttu-id="82b15-130">Dans la page **Connecter personnes à la** connaissance, cliquez sur **Commencer** pour vous aider dans le processus de configuration.</span><span class="sxs-lookup"><span data-stu-id="82b15-130">On the **Connect people to knowledge** page, click **Get started** to walk you through the setup process.</span></span>

    ![Prise en main](../media/k-get-started.png) 

4. <span data-ttu-id="82b15-132">Dans la page Choisir la façon dont Topics peut trouver des **rubriques,** vous allez configurer la découverte de rubriques.</span><span class="sxs-lookup"><span data-stu-id="82b15-132">On the **Choose how Viva Topics can find topics** page, you will configure topic discovery.</span></span> <span data-ttu-id="82b15-133">Dans la section **Sélectionner SharePoint sources** de rubriques, sélectionnez les sites SharePoint à analyser en tant que sources pour vos rubriques lors de la découverte.</span><span class="sxs-lookup"><span data-stu-id="82b15-133">In the **Select SharePoint topic sources** section, select which SharePoint sites will be crawled as sources for your topics during discovery.</span></span> <span data-ttu-id="82b15-134">Choisissez parmi les autorisations suivantes :</span><span class="sxs-lookup"><span data-stu-id="82b15-134">Choose from:</span></span>
    - <span data-ttu-id="82b15-135">**Tous les sites** : tous les sites SharePoint dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="82b15-135">**All sites**: All SharePoint sites in your organization.</span></span> <span data-ttu-id="82b15-136">Cela inclut les sites actuels et futurs.</span><span class="sxs-lookup"><span data-stu-id="82b15-136">This includes current and future sites.</span></span>
    - <span data-ttu-id="82b15-137">**Tous, sauf les sites sélectionnés**: tapez les noms des sites que vous souhaitez exclure.</span><span class="sxs-lookup"><span data-stu-id="82b15-137">**All, except selected sites**: Type the names of the sites you want to exclude.</span></span>  <span data-ttu-id="82b15-138">Vous pouvez également charger une liste de sites que vous souhaitez refuser de découvrir.</span><span class="sxs-lookup"><span data-stu-id="82b15-138">You can also upload a list of sites that you want to opt out from discovery.</span></span> <span data-ttu-id="82b15-139">Les sites créés à l’avenir seront inclus en tant que sources pour la découverte de rubriques.</span><span class="sxs-lookup"><span data-stu-id="82b15-139">Sites created in future will be included as sources for topic discovery.</span></span> 
    - <span data-ttu-id="82b15-140">**Seuls les sites** sélectionnés : tapez les noms des sites que vous souhaitez inclure.</span><span class="sxs-lookup"><span data-stu-id="82b15-140">**Only selected sites**: Type the names of the sites you want to include.</span></span> <span data-ttu-id="82b15-141">Vous pouvez également charger une liste de sites.</span><span class="sxs-lookup"><span data-stu-id="82b15-141">You can also upload a list of sites.</span></span> <span data-ttu-id="82b15-142">Les sites créés dans le futur ne seront pas inclus comme sources pour la découverte de rubriques.</span><span class="sxs-lookup"><span data-stu-id="82b15-142">Sites created in the future will not be included as sources for topic discovery.</span></span>
    - <span data-ttu-id="82b15-143">**Aucun site** : n’incluez aucun site SharePoint.</span><span class="sxs-lookup"><span data-stu-id="82b15-143">**No sites**: Do not include any SharePoint sites.</span></span>

    ![Choisir comment rechercher des rubriques](../media/ksetup1.png) 
   
5. <span data-ttu-id="82b15-145">Dans la section **Exclure les rubriques par** nom, vous pouvez ajouter des noms de rubriques que vous souhaitez exclure de la découverte de rubriques.</span><span class="sxs-lookup"><span data-stu-id="82b15-145">In the **Exclude topics by name** section, you can add names of topics you want to exclude from topic discovery.</span></span> <span data-ttu-id="82b15-146">Utilisez ce paramètre pour empêcher que des informations sensibles ne figurent dans les rubriques.</span><span class="sxs-lookup"><span data-stu-id="82b15-146">Use this setting to prevent sensitive information from being included as topics.</span></span> <span data-ttu-id="82b15-147">Les options disponibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="82b15-147">The options are:</span></span>
    - <span data-ttu-id="82b15-148">**N’excluez aucune rubrique**</span><span class="sxs-lookup"><span data-stu-id="82b15-148">**Don't exclude any topics**</span></span> 
    - <span data-ttu-id="82b15-149">**Exclure les rubriques par nom**</span><span class="sxs-lookup"><span data-stu-id="82b15-149">**Exclude topics by name**</span></span>

    ![Exclure des rubriques](../media/topics-excluded-by-name.png) 

    <span data-ttu-id="82b15-151">(Les gestionnaires de connaissances peuvent également exclure des rubriques dans le centre de rubriques après la découverte.)</span><span class="sxs-lookup"><span data-stu-id="82b15-151">(Knowledge managers can also exclude topics in the topic center after discovery.)</span></span>

    #### <a name="how-to-exclude-topics-by-name"></a><span data-ttu-id="82b15-152">Comment exclure des rubriques par nom</span><span class="sxs-lookup"><span data-stu-id="82b15-152">How to exclude topics by name</span></span>    

    <span data-ttu-id="82b15-153">Si vous devez exclure des rubriques, après avoir sélectionné Exclure les **rubriques** par nom, téléchargez le modèle .csv et mettez-le à jour avec la liste des rubriques que vous souhaitez exclure de vos résultats de découverte.</span><span class="sxs-lookup"><span data-stu-id="82b15-153">If you need to exclude topics, after selecting **Exclude topics by name**, download the .csv template and update it with the list of topics that you want to exclude from your discovery results.</span></span>

    ![Exclure des rubriques dans le modèle CSV](../media/exclude-topics-csv.png) 

    <span data-ttu-id="82b15-155">Dans le modèle CSV, entrez les informations suivantes sur les rubriques à exclure :</span><span class="sxs-lookup"><span data-stu-id="82b15-155">In the CSV template, enter the following information about the topics you want to exclude:</span></span>

    - <span data-ttu-id="82b15-156">**Nom** : tapez le nom de la rubrique à exclure.</span><span class="sxs-lookup"><span data-stu-id="82b15-156">**Name**: Type the name of the topic you want to exclude.</span></span> <span data-ttu-id="82b15-157">Il existe deux méthodes pour y parvenir :</span><span class="sxs-lookup"><span data-stu-id="82b15-157">There are two ways to do this:</span></span>
        - <span data-ttu-id="82b15-158">Correspondance exacte : vous pouvez inclure le nom exact ou l’acronyme (par exemple, *Contoso* ou *ATL*).</span><span class="sxs-lookup"><span data-stu-id="82b15-158">Exact match: You can include the exact name or acronym (for example, *Contoso* or *ATL*).</span></span>
        - <span data-ttu-id="82b15-159">Correspondance partielle : vous pouvez exclure toutes les rubriques qui ont un mot spécifique.</span><span class="sxs-lookup"><span data-stu-id="82b15-159">Partial match: You can exclude all topics that have a specific word in it.</span></span>  <span data-ttu-id="82b15-160">Par exemple, *arc exclura* toutes les rubriques avec le mot *arc* dans celui-ci, telles que le cercle *d’arc,* *l’arc de Pierre ou* *l’arc de formation*. Notez qu’il n’exclura pas les rubriques dans lesquelles le texte est inclus dans le cadre d’un mot, comme *Architecture*.</span><span class="sxs-lookup"><span data-stu-id="82b15-160">For example, *arc* will exclude all topics with the word *arc* in it, such as *Arc circle*, *Plasma arc welding*, or *Training arc*. Note that it will not exclude topics in which the text is included as part of a word, such as *Architecture*.</span></span>
    - <span data-ttu-id="82b15-161">**Signifie (facultatif)**: si vous souhaitez exclure un acronyme, tapez les mots qu’il signifie.</span><span class="sxs-lookup"><span data-stu-id="82b15-161">**Stands for (optional)**: If you want to exclude an acronym, type the words the acronym stands for.</span></span>
    - <span data-ttu-id="82b15-162">**MatchType-Exact/Partial**: tapez si le nom que vous avez entré était un type de correspondance *exact* *ou* partiel.</span><span class="sxs-lookup"><span data-stu-id="82b15-162">**MatchType-Exact/Partial**: Type whether the name you entered was an *exact* or *partial* match type.</span></span>

    <span data-ttu-id="82b15-163">Une fois que vous avez terminé et enregistré votre fichier .csv, sélectionnez **Parcourir** pour le localiser et le sélectionner.</span><span class="sxs-lookup"><span data-stu-id="82b15-163">After you've completed and saved your .csv file, select **Browse** to locate and select it.</span></span>
    
    <span data-ttu-id="82b15-164">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="82b15-164">Select **Next**.</span></span>

6. <span data-ttu-id="82b15-165">Sur la Qui pouvez voir les **rubriques** et où peuvent-elles les voir, vous allez configurer la visibilité des rubriques.</span><span class="sxs-lookup"><span data-stu-id="82b15-165">On the **Who can see topics and where can they see them** page, you will configure topic visibility.</span></span> <span data-ttu-id="82b15-166">Dans la Qui pouvez voir les paramètres des **rubriques,** vous choisissez les personnes qui auront accès aux détails des rubriques, telles que les rubriques mises en évidence, les fiches de rubrique, les réponses aux rubriques dans la recherche et les pages de rubriques.</span><span class="sxs-lookup"><span data-stu-id="82b15-166">In the **Who can see topics** setting, you choose who will have access to topic details, such as highlighted topics, topic cards, topic answers in search, and topic pages.</span></span> <span data-ttu-id="82b15-167">Vous pouvez sélectionner :</span><span class="sxs-lookup"><span data-stu-id="82b15-167">You can select:</span></span>
    - <span data-ttu-id="82b15-168">**Tous les membres de mon organisation**</span><span class="sxs-lookup"><span data-stu-id="82b15-168">**Everyone in my organization**</span></span>
    - <span data-ttu-id="82b15-169">**Personnes ou groupes de sécurité sélectionnés uniquement**</span><span class="sxs-lookup"><span data-stu-id="82b15-169">**Only selected people or security groups**</span></span>
    - <span data-ttu-id="82b15-170">**Personne**</span><span class="sxs-lookup"><span data-stu-id="82b15-170">**No one**</span></span>

    ![Qui pouvez voir les rubriques](../media/ksetup2.png)  

    > [!Note] 
    > <span data-ttu-id="82b15-172">Bien que ce paramètre vous permet de sélectionner n’importe quel utilisateur de votre organisation, seuls les utilisateurs qui ont des licences Expériences des rubriques qui leur sont attribuées pourront afficher les rubriques.</span><span class="sxs-lookup"><span data-stu-id="82b15-172">While this setting allows you to select any user in your organization, only users who have Topic Experiences licenses assigned to them will be able to view topics.</span></span>

7. <span data-ttu-id="82b15-173">Dans la page **Autorisations pour la** gestion des rubriques, vous choisissez qui sera en mesure de créer, modifier ou gérer des rubriques.</span><span class="sxs-lookup"><span data-stu-id="82b15-173">In the **Permissions for topic management** page, you choose who will be able to create, edit, or manage topics.</span></span> <span data-ttu-id="82b15-174">Dans la **section Qui créer et modifier des rubriques,** vous pouvez sélectionner :</span><span class="sxs-lookup"><span data-stu-id="82b15-174">In the **Who can create and edit topics** section, you can select:</span></span>
    - <span data-ttu-id="82b15-175">**Tous les membres de mon organisation**</span><span class="sxs-lookup"><span data-stu-id="82b15-175">**Everyone in my organization**</span></span>
    - <span data-ttu-id="82b15-176">**Personnes ou groupes de sécurité sélectionnés uniquement**</span><span class="sxs-lookup"><span data-stu-id="82b15-176">**Only selected people or security groups**</span></span>
    - <span data-ttu-id="82b15-177">**Personne**</span><span class="sxs-lookup"><span data-stu-id="82b15-177">**No one**</span></span>

    ![Autorisations pour la gestion des rubriques, qui peut créer et modifier des rubriques](../media/ksetup3.png) 

8. <span data-ttu-id="82b15-179">Dans la **section Qui pouvez gérer les rubriques,** vous pouvez sélectionner :</span><span class="sxs-lookup"><span data-stu-id="82b15-179">In the **Who can manage topics** section, you can select:</span></span>
    - <span data-ttu-id="82b15-180">**Tous les membres de mon organisation**</span><span class="sxs-lookup"><span data-stu-id="82b15-180">**Everyone in my organization**</span></span>
    - <span data-ttu-id="82b15-181">**Personnes ou groupes de sécurité sélectionnés uniquement**</span><span class="sxs-lookup"><span data-stu-id="82b15-181">**Only selected people or security groups**</span></span>

    ![Autorisations pour la gestion des rubriques](../media/km-setup-create-edit-topics.png) 

    <span data-ttu-id="82b15-183">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="82b15-183">Select **Next**.</span></span>

9. <span data-ttu-id="82b15-184">Dans la page **Créer un** centre de rubriques, vous pouvez créer votre site de centre de rubriques dans lequel les pages de rubriques peuvent être vues et les rubriques peuvent être gérées.</span><span class="sxs-lookup"><span data-stu-id="82b15-184">On the **Create topic center** page, you can create your topic center site in which topic pages can be viewed and topics can be managed.</span></span> <span data-ttu-id="82b15-185">Dans la **zone Nom du site,** tapez un nom pour votre centre de rubriques.</span><span class="sxs-lookup"><span data-stu-id="82b15-185">In the **Site name** box, type a name for your topic center.</span></span> <span data-ttu-id="82b15-186">Vous pouvez cliquer sur l’icône de crayon si vous souhaitez modifier l’URL.</span><span class="sxs-lookup"><span data-stu-id="82b15-186">You can click the pencil icon if you want to change the URL.</span></span> <span data-ttu-id="82b15-187">Vous pourz éventuellement taper une brève description dans la **zone Description.**</span><span class="sxs-lookup"><span data-stu-id="82b15-187">Optionally, type a short description in the **Description** box.</span></span> 

   > [!Important]
   > <span data-ttu-id="82b15-188">Vous pouvez modifier le nom du site ultérieurement, mais vous ne pouvez pas modifier l’URL une fois l’Assistant terminé.</span><span class="sxs-lookup"><span data-stu-id="82b15-188">You can change the site name later, but you can't change the URL after you complete the wizard.</span></span>

   <span data-ttu-id="82b15-189">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="82b15-189">Select **Next**.</span></span>

   ![Créer le Centre de connaissances](../media/ksetup4.png)  

10. <span data-ttu-id="82b15-191">À la page **Examiner et finaliser**, vous pouvez consulter le paramètre sélectionné, puis choisir d’apporter des modifications.</span><span class="sxs-lookup"><span data-stu-id="82b15-191">On the **Review and finish** page, you can look at your selected setting and choose to make changes.</span></span> <span data-ttu-id="82b15-192">Si vos sélections vous conviennent, sélectionnez **Activer**.</span><span class="sxs-lookup"><span data-stu-id="82b15-192">If you are satisfied with your selections, select **Activate**.</span></span>

11. <span data-ttu-id="82b15-193">La page **Rubriques** activée s’affiche, confirmant que le système va maintenant commencer à analyser les sites sélectionnés pour les rubriques et à créer le site centre de rubriques.</span><span class="sxs-lookup"><span data-stu-id="82b15-193">The **Viva Topics activated** page will display, confirming that the system will now start analyzing your selected sites for topics and creating the topic center site.</span></span> <span data-ttu-id="82b15-194">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="82b15-194">Select **Done**.</span></span>

12. <span data-ttu-id="82b15-195">Vous serez renvoyé à votre page de **Connecter de** connaissances.</span><span class="sxs-lookup"><span data-stu-id="82b15-195">You'll be returned to your **Connect people to knowledge** page.</span></span> <span data-ttu-id="82b15-196">Dans cette page, vous pouvez sélectionner **Gérer** pour modifier vos paramètres de configuration.</span><span class="sxs-lookup"><span data-stu-id="82b15-196">From this page, you can select **Manage** to make any changes to your configuration settings.</span></span> 

    ![Paramètres appliqué](../media/ksetup7.png)    

## <a name="manage-topic-experiences"></a><span data-ttu-id="82b15-198">Gérer les expériences de rubrique</span><span class="sxs-lookup"><span data-stu-id="82b15-198">Manage topic experiences</span></span>

<span data-ttu-id="82b15-199">Une fois que vous avez configuré Rubriques, vous pouvez modifier les paramètres que vous avez choisis lors de l’installation dans le [Centre d’administration Microsoft 365](https://admin.microsoft.com/AdminPortal#/featureexplorer/csi/KnowledgeManagement).</span><span class="sxs-lookup"><span data-stu-id="82b15-199">Once you have set up Topics, you can change the settings that you chose during setup in the [Microsoft 365 admin center](https://admin.microsoft.com/AdminPortal#/featureexplorer/csi/KnowledgeManagement).</span></span> <span data-ttu-id="82b15-200">Si vous souhaitez en savoir plus, veuillez consulter les références suivantes :</span><span class="sxs-lookup"><span data-stu-id="82b15-200">See the following references:</span></span>

- [<span data-ttu-id="82b15-201">Gérer la découverte de rubriques dans les rubriques microsoft</span><span class="sxs-lookup"><span data-stu-id="82b15-201">Manage topic discovery in Microsoft Viva Topics</span></span>](topic-experiences-discovery.md)
- [<span data-ttu-id="82b15-202">Gérer la visibilité des rubriques dans les rubriques microsoft</span><span class="sxs-lookup"><span data-stu-id="82b15-202">Manage topic visibility in Microsoft Viva Topics</span></span>](topic-experiences-knowledge-rules.md)
- [<span data-ttu-id="82b15-203">Gérer les autorisations des rubriques dans les rubriques microsoft</span><span class="sxs-lookup"><span data-stu-id="82b15-203">Manage topic permissions in Microsoft Viva Topics</span></span>](topic-experiences-user-permissions.md)
- [<span data-ttu-id="82b15-204">Modifier le nom du centre de rubriques dans Rubriques microsoft</span><span class="sxs-lookup"><span data-stu-id="82b15-204">Change the name of the topic center in Microsoft Viva Topics</span></span>](topic-experiences-administration.md)

## <a name="see-also"></a><span data-ttu-id="82b15-205">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82b15-205">See also</span></span>

[<span data-ttu-id="82b15-206">Vue d’ensemble des expériences de rubrique</span><span class="sxs-lookup"><span data-stu-id="82b15-206">Topic Experiences Overview</span></span>](topic-experiences-overview.md)
