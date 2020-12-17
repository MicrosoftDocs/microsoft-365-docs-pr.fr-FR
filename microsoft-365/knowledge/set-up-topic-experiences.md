---
title: Configuration des expériences de rubrique dans Microsoft 365
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
description: Découvrez comment configurer des expériences de rubrique dans Microsoft 365
ms.openlocfilehash: e11f0b75556a4a8ac0ffa40269d7166258128daf
ms.sourcegitcommit: 884ac262443c50362d0c3ded961d36d6b15d8b73
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/16/2020
ms.locfileid: "49698554"
---
# <a name="set-up-topic-experiences-in-microsoft-365"></a><span data-ttu-id="f35d9-103">Configuration des expériences de rubrique dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f35d9-103">Set up topic experiences in Microsoft 365</span></span>

<span data-ttu-id="f35d9-104">Vous pouvez utiliser le centre d’administration Microsoft 365 pour installer et configurer des [expériences de rubrique](topic-experiences-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f35d9-104">You can use the Microsoft 365 admin center to set up and configure [topic experiences](topic-experiences-overview.md).</span></span> 

<span data-ttu-id="f35d9-105">Il est important de planifier la meilleure façon de configurer et de configurer des rubriques dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="f35d9-105">It is important to plan the best way to set up and configure topics in your environment.</span></span> <span data-ttu-id="f35d9-106">Avant de commencer les procédures décrites dans cet article, lisez [plan topic Experiences](plan-topic-experiences.md) .</span><span class="sxs-lookup"><span data-stu-id="f35d9-106">Be sure to read [Plan topic experiences](plan-topic-experiences.md) before you begin the procedures in this article.</span></span>

<span data-ttu-id="f35d9-107">Vous devez être un administrateur général ou un administrateur SharePoint pour accéder au centre d’administration Microsoft 365 et configurer des expériences de rubrique.</span><span class="sxs-lookup"><span data-stu-id="f35d9-107">You must be a global administrator or SharePoint administrator to access the Microsoft 365 admin center and set up topic experiences.</span></span>

## <a name="set-up-topic-experiences"></a><span data-ttu-id="f35d9-108">Configurer des expériences de rubrique</span><span class="sxs-lookup"><span data-stu-id="f35d9-108">Set up topic experiences</span></span>

<span data-ttu-id="f35d9-109">Pour configurer des expériences de rubrique dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f35d9-109">To set up topic experiences in Microsoft 365</span></span>

1. <span data-ttu-id="f35d9-110">Dans le [Centre d’administration Microsoft 365](https://admin.microsoft.com), sélectionnez **configuration**, puis affichez la section **fichiers et contenu** .</span><span class="sxs-lookup"><span data-stu-id="f35d9-110">In the [Microsoft 365 admin center](https://admin.microsoft.com), select **Setup**, and then view the **Files and content** section.</span></span>
2. <span data-ttu-id="f35d9-111">Dans la section **fichiers et contenu** , cliquez sur **connecter des personnes à la connaissance**.</span><span class="sxs-lookup"><span data-stu-id="f35d9-111">In the **Files and content** section, click **Connect people to knowledge**.</span></span>

    ![Connecter des personnes aux connaissances](../media/admin-org-knowledge-options.png) 

3. <span data-ttu-id="f35d9-113">Sur la page **connecter des personnes au** niveau de connaissances, cliquez sur **prise en main** pour vous guider tout au long du processus de configuration.</span><span class="sxs-lookup"><span data-stu-id="f35d9-113">On the **Connect people to knowledge** page, click **Get started** to walk you through the setup process.</span></span>

    ![Prise en main](../media/k-get-started.png) 

4. <span data-ttu-id="f35d9-115">Sur la page **choisir comment le réseau de connaissances peut trouver des rubriques** , vous allez configurer la découverte de rubrique.</span><span class="sxs-lookup"><span data-stu-id="f35d9-115">On the **Choose how the knowledge network can find topics** page, you will configure topic discovery.</span></span> <span data-ttu-id="f35d9-116">Dans la section **Sélectionner les sources des rubriques SharePoint** , sélectionnez les sites SharePoint qui seront analysés en tant que sources pour vos rubriques lors de la découverte.</span><span class="sxs-lookup"><span data-stu-id="f35d9-116">In the **Select SharePoint topic sources** section, select which SharePoint sites will be crawled as sources for your topics during discovery.</span></span> <span data-ttu-id="f35d9-117">Choisissez parmi les autorisations suivantes :</span><span class="sxs-lookup"><span data-stu-id="f35d9-117">Choose from:</span></span>
    - <span data-ttu-id="f35d9-118">**Tous les sites**: tous les sites SharePoint de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f35d9-118">**All sites**: All SharePoint sites in your organization.</span></span> <span data-ttu-id="f35d9-119">Cela inclut les sites actuels et futurs.</span><span class="sxs-lookup"><span data-stu-id="f35d9-119">This includes current and future sites.</span></span>
    - <span data-ttu-id="f35d9-120">**Tout, à l’exception des sites sélectionnés**: saisissez les noms des sites à exclure.</span><span class="sxs-lookup"><span data-stu-id="f35d9-120">**All, except selected sites**: Type the names of the sites you want to exclude.</span></span>  <span data-ttu-id="f35d9-121">Vous pouvez également télécharger une liste de sites que vous souhaitez exclure de la découverte.</span><span class="sxs-lookup"><span data-stu-id="f35d9-121">You can also upload a list of sites that you want to opt out from discovery.</span></span> <span data-ttu-id="f35d9-122">Les sites créés à l’avenir seront inclus en tant que sources pour la découverte des rubriques.</span><span class="sxs-lookup"><span data-stu-id="f35d9-122">Sites created in future will be included as sources for topic discovery.</span></span> 
    - <span data-ttu-id="f35d9-123">**Sites sélectionnés uniquement**: saisissez les noms des sites que vous souhaitez inclure.</span><span class="sxs-lookup"><span data-stu-id="f35d9-123">**Only selected sites**: Type the names of the sites you want to include.</span></span> <span data-ttu-id="f35d9-124">Vous pouvez également télécharger une liste de sites.</span><span class="sxs-lookup"><span data-stu-id="f35d9-124">You can also upload a list of sites.</span></span> <span data-ttu-id="f35d9-125">Les sites créés à l’avenir ne seront pas inclus en tant que sources pour la découverte des rubriques.</span><span class="sxs-lookup"><span data-stu-id="f35d9-125">Sites created in the future will not be included as sources for topic discovery.</span></span>
    - <span data-ttu-id="f35d9-126">**Aucun site**: n’inclut aucun site SharePoint.</span><span class="sxs-lookup"><span data-stu-id="f35d9-126">**No sites**: Do not include any SharePoint sites.</span></span>

    ![Choisir comment rechercher des rubriques](../media/ksetup1.png) 
   
5. <span data-ttu-id="f35d9-128">Dans la section **exclure des rubriques par nom** , vous pouvez ajouter les noms des rubriques que vous souhaitez exclure de la découverte de rubrique.</span><span class="sxs-lookup"><span data-stu-id="f35d9-128">In the **Exclude topics by name** section, you can add names of topics you want to exclude from topic discovery.</span></span> <span data-ttu-id="f35d9-129">Utilisez ce paramètre pour empêcher que des informations sensibles soient incluses en tant que rubriques.</span><span class="sxs-lookup"><span data-stu-id="f35d9-129">Use this setting to prevent sensitive information from being included as topics.</span></span> <span data-ttu-id="f35d9-130">Les options disponibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="f35d9-130">The options are:</span></span>
    - <span data-ttu-id="f35d9-131">**Ne pas exclure les rubriques**</span><span class="sxs-lookup"><span data-stu-id="f35d9-131">**Don't exclude any topics**</span></span> 
    - <span data-ttu-id="f35d9-132">**Exclure les rubriques par nom**</span><span class="sxs-lookup"><span data-stu-id="f35d9-132">**Exclude topics by name**</span></span>

    ![Exclure des rubriques](../media/topics-excluded-by-name.png) 

    <span data-ttu-id="f35d9-134">(Les gestionnaires de connaissances peuvent également exclure des rubriques dans le Centre des rubriques après la découverte.)</span><span class="sxs-lookup"><span data-stu-id="f35d9-134">(Knowledge managers can also exclude topics in the topic center after discovery.)</span></span>

    #### <a name="how-to-exclude-topics-by-name"></a><span data-ttu-id="f35d9-135">Procédure exclure des rubriques par nom</span><span class="sxs-lookup"><span data-stu-id="f35d9-135">How to exclude topics by name</span></span>    

    <span data-ttu-id="f35d9-136">Si vous devez exclure des rubriques, après avoir sélectionné **exclure les rubriques par nom**, sélectionnez Télécharger le modèle. csv et mettez-le à jour à l’aide de la liste des rubriques que vous souhaitez exclure de vos résultats de découverte.</span><span class="sxs-lookup"><span data-stu-id="f35d9-136">If you need to exclude topics, after selecting **Exclude topics by name**, select download the .csv template and update it with the list of topics that you want to exclude from your discovery results.</span></span>

    ![Exclure les rubriques du modèle CSV](../media/exclude-topics-csv.png) 

    <span data-ttu-id="f35d9-138">Dans le modèle CSV, entrez les informations suivantes sur les rubriques à exclure :</span><span class="sxs-lookup"><span data-stu-id="f35d9-138">In the CSV template, enter the following information about the topics you want to exclude:</span></span>

    - <span data-ttu-id="f35d9-139">**Nom**: tapez le nom de la rubrique à exclure.</span><span class="sxs-lookup"><span data-stu-id="f35d9-139">**Name**: Type the name of the topic you want to exclude.</span></span> <span data-ttu-id="f35d9-140">Vous pouvez procéder de deux manières :</span><span class="sxs-lookup"><span data-stu-id="f35d9-140">There are two ways to do this:</span></span>
        - <span data-ttu-id="f35d9-141">Correspondance exacte : vous pouvez inclure le nom exact ou un acronyme (par exemple, *contoso* ou *ATL*).</span><span class="sxs-lookup"><span data-stu-id="f35d9-141">Exact match: You can include the exact name or acronym (for example, *Contoso* or *ATL*).</span></span>
        - <span data-ttu-id="f35d9-142">Correspondance partielle : vous pouvez exclure toutes les rubriques qui contiennent un mot spécifique.</span><span class="sxs-lookup"><span data-stu-id="f35d9-142">Partial match: You can exclude all topics that have a specific word in it.</span></span>  <span data-ttu-id="f35d9-143">Par exemple, *arc* exclut toutes les rubriques contenant le mot *arc* , comme un *cercle arc*, un *soudage* à l’arc de plasma ou un *arc de formation*. Notez qu’il n’exclura pas les rubriques dans lesquelles le texte est inclus dans un mot, tel que *architecture*.</span><span class="sxs-lookup"><span data-stu-id="f35d9-143">For example, *arc* will exclude all topics with the word *arc* in it, such as *Arc circle*, *Plasma arc welding*, or *Training arc*. Note that it will not exclude topics in which the text is included as part of a word, such as *Architecture*.</span></span>
    - <span data-ttu-id="f35d9-144">**Abréviation de (facultatif)**: Si vous souhaitez exclure un acronyme, tapez les mots de l’acronyme.</span><span class="sxs-lookup"><span data-stu-id="f35d9-144">**Stands for (optional)**: If you want to exclude an acronym, type the words the acronym stands for.</span></span>
    - <span data-ttu-id="f35d9-145">**MatchType-exacte/partielle**: spécifiez si le nom que vous avez entré est un type de correspondance *exacte* ou *partielle* .</span><span class="sxs-lookup"><span data-stu-id="f35d9-145">**MatchType-Exact/Partial**: Type whether the name you entered was an *exact* or *partial* match type.</span></span>

    <span data-ttu-id="f35d9-146">Une fois que vous avez terminé et enregistré votre fichier. csv, sélectionnez **Parcourir** pour le localiser et le sélectionner.</span><span class="sxs-lookup"><span data-stu-id="f35d9-146">After you've completed and saved your .csv file, select **Browse** to locate and select it.</span></span>
    
    <span data-ttu-id="f35d9-147">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="f35d9-147">Select **Next**.</span></span>

6. <span data-ttu-id="f35d9-148">Sur la page **qui peut voir les rubriques et où les afficher** , vous allez configurer la visibilité des rubriques.</span><span class="sxs-lookup"><span data-stu-id="f35d9-148">On the **Who can see topics and where can they see them** page, you will configure topic visibility.</span></span> <span data-ttu-id="f35d9-149">Dans le paramètre **qui peut voir les rubriques du paramètre de réseau de connaissances** , vous choisissez les utilisateurs qui auront accès aux détails de la rubrique, comme les rubriques en surbrillance, les fiches de rubrique, les réponses aux questions dans la recherche et les pages de rubrique.</span><span class="sxs-lookup"><span data-stu-id="f35d9-149">In the **Who can see topics in the knowledge network** setting, you choose who will have access to topic details, such as highlighted topics, topic cards, topic answers in search, and topic pages.</span></span> <span data-ttu-id="f35d9-150">Vous pouvez sélectionner :</span><span class="sxs-lookup"><span data-stu-id="f35d9-150">You can select:</span></span>
    - <span data-ttu-id="f35d9-151">**Tous les membres de mon organisation**</span><span class="sxs-lookup"><span data-stu-id="f35d9-151">**Everyone in my organization**</span></span>
    - <span data-ttu-id="f35d9-152">**Uniquement les personnes ou les groupes de sécurité sélectionnés**</span><span class="sxs-lookup"><span data-stu-id="f35d9-152">**Only selected people or security groups**</span></span>
    - <span data-ttu-id="f35d9-153">**Personne**</span><span class="sxs-lookup"><span data-stu-id="f35d9-153">**No one**</span></span>

    ![Qui peut voir les rubriques](../media/ksetup2.png)  

 > [!Note] 
 > <span data-ttu-id="f35d9-155">Bien que ce paramètre vous permette de sélectionner un utilisateur de votre organisation, seuls les utilisateurs disposant d’une rubrique sur laquelle des licences ont été attribuées pourront consulter les rubriques.</span><span class="sxs-lookup"><span data-stu-id="f35d9-155">While this setting allows you to select any user in your organization, only users who have Topic Experiences licenses assigned to them will be able to view topics.</span></span>

7. <span data-ttu-id="f35d9-156">Dans la page **autorisations pour la rubrique gestion des** rubriques, choisissez qui pourra créer, modifier ou gérer des rubriques.</span><span class="sxs-lookup"><span data-stu-id="f35d9-156">In the **Permissions for topic management** page, you choose who will be able to create, edit, or manage topics.</span></span> <span data-ttu-id="f35d9-157">Dans la section **qui peut créer et modifier des rubriques** , vous pouvez sélectionner :</span><span class="sxs-lookup"><span data-stu-id="f35d9-157">In the **Who can create and edit topics** section, you can select:</span></span>
    - <span data-ttu-id="f35d9-158">**Tous les membres de mon organisation**</span><span class="sxs-lookup"><span data-stu-id="f35d9-158">**Everyone in my organization**</span></span>
    - <span data-ttu-id="f35d9-159">**Uniquement les personnes ou les groupes de sécurité sélectionnés**</span><span class="sxs-lookup"><span data-stu-id="f35d9-159">**Only selected people or security groups**</span></span>
    - <span data-ttu-id="f35d9-160">**Personne**</span><span class="sxs-lookup"><span data-stu-id="f35d9-160">**No one**</span></span>

    ![Autorisations pour la gestion des rubriques, qui peut créer et modifier des rubriques](../media/ksetup3.png) 

8. <span data-ttu-id="f35d9-162">Dans la section **qui peut gérer les rubriques** , vous pouvez sélectionner :</span><span class="sxs-lookup"><span data-stu-id="f35d9-162">In the **Who can manage topics** section, you can select:</span></span>
    - <span data-ttu-id="f35d9-163">**Tous les membres de mon organisation**</span><span class="sxs-lookup"><span data-stu-id="f35d9-163">**Everyone in my organization**</span></span>
    - <span data-ttu-id="f35d9-164">**Uniquement les personnes ou les groupes de sécurité sélectionnés**</span><span class="sxs-lookup"><span data-stu-id="f35d9-164">**Only selected people or security groups**</span></span>

    ![Autorisations pour la gestion des rubriques](../media/km-setup-create-edit-topics.png) 

    <span data-ttu-id="f35d9-166">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="f35d9-166">Select **Next**.</span></span>

9. <span data-ttu-id="f35d9-167">Sur la page **créer un centre de rubriques** , vous pouvez créer votre site Centre de rubrique dans lequel les pages de rubrique peuvent être affichées et les rubriques peuvent être gérées.</span><span class="sxs-lookup"><span data-stu-id="f35d9-167">On the **Create topic center** page, you can create your topic center site in which topic pages can be viewed and topics can be managed.</span></span> <span data-ttu-id="f35d9-168">Dans la zone **nom du site** , tapez un nom pour le centre de la rubrique.</span><span class="sxs-lookup"><span data-stu-id="f35d9-168">In the **Site name** box, type a name for your Topic center.</span></span> <span data-ttu-id="f35d9-169">Vous pouvez éventuellement taper une brève description dans la zone **Description** .</span><span class="sxs-lookup"><span data-stu-id="f35d9-169">You can optionally type a short description in the **Description** box.</span></span> 

<span data-ttu-id="f35d9-170">Sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="f35d9-170">Select **Next**.</span></span>

   ![Créer un centre de connaissances](../media/ksetup4.png)  

10. <span data-ttu-id="f35d9-172">À la page **Examiner et finaliser**, vous pouvez consulter le paramètre sélectionné, puis choisir d’apporter des modifications.</span><span class="sxs-lookup"><span data-stu-id="f35d9-172">On the **Review and finish** page, you can look at your selected setting and choose to make changes.</span></span> <span data-ttu-id="f35d9-173">Si vos sélections vous conviennent, sélectionnez **Activer**.</span><span class="sxs-lookup"><span data-stu-id="f35d9-173">If you are satisfied with your selections, select **Activate**.</span></span>

11. <span data-ttu-id="f35d9-174">La page **activation du réseau de connaissances** s’affiche, confirmant que le système commence à analyser les sites sélectionnés pour les rubriques et la création du site Centre de connaissances.</span><span class="sxs-lookup"><span data-stu-id="f35d9-174">The **Knowledge network activated** page will display, confirming that the system will now start analyzing your selected sites for topics and creating the Knowledge Center site.</span></span> <span data-ttu-id="f35d9-175">Sélectionnez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="f35d9-175">Select **Done**.</span></span>

12. <span data-ttu-id="f35d9-176">Vous serez redirigé vers la page **connecter des personnes à la page de connaissances** .</span><span class="sxs-lookup"><span data-stu-id="f35d9-176">You'll be returned to your **Connect people to knowledge** page.</span></span> <span data-ttu-id="f35d9-177">Dans cette page, vous pouvez sélectionner **Gérer** pour modifier vos paramètres de configuration.</span><span class="sxs-lookup"><span data-stu-id="f35d9-177">From this page, you can select **Manage** to make any changes to your configuration settings.</span></span> 

    ![Paramètres appliqués](../media/ksetup7.png)    

## <a name="assign-licenses"></a><span data-ttu-id="f35d9-179">Attribuer des licences</span><span class="sxs-lookup"><span data-stu-id="f35d9-179">Assign licenses</span></span>

<span data-ttu-id="f35d9-180">Une fois que vous avez configuré les expériences de rubrique, vous devez attribuer des licences aux utilisateurs qui utiliseront des expériences de rubrique.</span><span class="sxs-lookup"><span data-stu-id="f35d9-180">Once you have configured topic experiences, you must assign licenses for the users who will be using topic experiences.</span></span> <span data-ttu-id="f35d9-181">Seuls les utilisateurs disposant d’une licence peuvent consulter des informations sur des sujets tels que des mises en évidence, des fiches de rubrique, des pages de rubrique et le Centre des rubriques.</span><span class="sxs-lookup"><span data-stu-id="f35d9-181">Only users with a license can see information on topics including highlights, topic cards, topic pages and the topic center.</span></span> 

<span data-ttu-id="f35d9-182">Pour attribuer des licences :</span><span class="sxs-lookup"><span data-stu-id="f35d9-182">To assign licenses:</span></span>

1. <span data-ttu-id="f35d9-183">Dans le Centre d’administration Microsoft 365, sous **Utilisateurs**, cliquez sur **Utilisateurs actifs**.</span><span class="sxs-lookup"><span data-stu-id="f35d9-183">In the Microsoft 365 admin center, under **Users**, click **Active users**.</span></span>

2. <span data-ttu-id="f35d9-184">Sélectionnez les utilisateurs auxquels attribuer une licence, puis cliquez sur **Gérer les licences de produits**.</span><span class="sxs-lookup"><span data-stu-id="f35d9-184">Select the users that you want to license, and click **Manage product licenses**.</span></span>

3. <span data-ttu-id="f35d9-185">Sélectionnez **Attribuer plus**.</span><span class="sxs-lookup"><span data-stu-id="f35d9-185">Select **Assign more**.</span></span>

4. <span data-ttu-id="f35d9-186">Sous **licences**, sélectionnez **expériences**.</span><span class="sxs-lookup"><span data-stu-id="f35d9-186">Under **Licenses**, select **Topic Experiences**.</span></span>

5. <span data-ttu-id="f35d9-187">Sous **applications**, assurez-vous que les **connecteurs graphiques de recherche avec index** et les **expériences de rubrique** sont tous deux sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="f35d9-187">Under **Apps**, make sure **Graph Connectors Search with Index** and **Topic Experiences** are both selected.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="f35d9-188">![Licences SharePoint Syntex dans le Centre d’administration Microsoft 365.](../media/topic-experiences-licenses.png)</span><span class="sxs-lookup"><span data-stu-id="f35d9-188">![SharePoint Syntex licenses in the Microsoft 365 admin center](../media/topic-experiences-licenses.png)</span></span>

6. <span data-ttu-id="f35d9-189">Cliquez sur **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="f35d9-189">Click **Save changes**.</span></span>

## <a name="manage-topic-experiences"></a><span data-ttu-id="f35d9-190">Gérer les expériences de rubrique</span><span class="sxs-lookup"><span data-stu-id="f35d9-190">Manage topic experiences</span></span>

<span data-ttu-id="f35d9-191">Une fois que vous avez configuré les expériences de rubrique, vous pouvez modifier les paramètres que vous avez choisis lors de l’installation dans le [Centre d’administration 365 de Microsoft](https://admin.microsoft.com/AdminPortal#/featureexplorer/csi/KnowledgeManagement).</span><span class="sxs-lookup"><span data-stu-id="f35d9-191">Once you have set up topic experiences, you can change the settings that you chose during setup in the [Microsoft 365 admin center](https://admin.microsoft.com/AdminPortal#/featureexplorer/csi/KnowledgeManagement).</span></span> <span data-ttu-id="f35d9-192">Consultez les références suivantes :</span><span class="sxs-lookup"><span data-stu-id="f35d9-192">See the following references:</span></span>

- [<span data-ttu-id="f35d9-193">Gestion de la découverte de rubrique dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f35d9-193">Manage topic discovery in Microsoft 365</span></span>](topic-experiences-discovery.md)
- [<span data-ttu-id="f35d9-194">Gestion de la visibilité des rubriques dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f35d9-194">Manage topic visibility in Microsoft 365</span></span>](topic-experiences-knowledge-rules.md)
- [<span data-ttu-id="f35d9-195">Gérer les autorisations de rubrique dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f35d9-195">Manage topic permissions in Microsoft 365</span></span>](topic-experiences-user-permissions.md)
- [<span data-ttu-id="f35d9-196">Modifier le nom du centre de rubrique dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f35d9-196">Change the name of the topic center in Microsoft 365</span></span>](topic-experiences-administration.md)

## <a name="see-also"></a><span data-ttu-id="f35d9-197">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f35d9-197">See also</span></span>

[<span data-ttu-id="f35d9-198">Présentation des expériences</span><span class="sxs-lookup"><span data-stu-id="f35d9-198">Topic Experiences Overview</span></span>](topic-experiences-overview.md)
