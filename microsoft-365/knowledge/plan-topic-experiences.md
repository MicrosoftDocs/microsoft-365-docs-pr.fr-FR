---
title: Planifier les rubriques microsoft
ms.author: mikeplum
author: MikePlumleyMSFT
manager: serdars
ms.reviewer: nkokoye
audience: admin
ms.topic: article
ms.service: o365-administration
search.appverid: MET150
localization_priority: Normal
description: Découvrez comment planifier le plan des rubriques microsoft
ms.openlocfilehash: a407fd6e6919c3b85235e317e5ed3ff103607700
ms.sourcegitcommit: 48195345b21b409b175d68acdc25d9f2fc4fc5f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "53229538"
---
# <a name="plan-for-microsoft-viva-topics"></a><span data-ttu-id="12ce9-103">Planifier les rubriques microsoft</span><span class="sxs-lookup"><span data-stu-id="12ce9-103">Plan for Microsoft Viva Topics</span></span>

<span data-ttu-id="12ce9-104">Vous contrôlez la façon dont les sujets sont abordés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="12ce9-104">You're in control of how topics are experienced in your organization.</span></span> <span data-ttu-id="12ce9-105">Vos décisions de planification pour Rubriques garantissent que les rubriques de haute qualité sont présentées à vos utilisateurs et qu’ils ont les autorisations nécessaires pour consommer et contribuer aux connaissances.</span><span class="sxs-lookup"><span data-stu-id="12ce9-105">Your planning decisions for Topics ensures that high quality topics are shown to your users and they have the right permissions to consume and contribute knowledge.</span></span>

<span data-ttu-id="12ce9-106">Dans cet article, nous examinerons les décisions de planification ci-après :</span><span class="sxs-lookup"><span data-stu-id="12ce9-106">In this article we'll examine these planning decisions:</span></span>

- <span data-ttu-id="12ce9-107">Les SharePoint sites que vous souhaitez analyser pour les rubriques</span><span class="sxs-lookup"><span data-stu-id="12ce9-107">Which SharePoint sites you want to crawl for topics</span></span>
- <span data-ttu-id="12ce9-108">Les rubriques, le cas besoin, que vous souhaitez exclure des expériences de rubrique</span><span class="sxs-lookup"><span data-stu-id="12ce9-108">Which topics, if any, you want to exclude from topic experiences</span></span>
- <span data-ttu-id="12ce9-109">Utilisateurs pour lesquels vous souhaitez rendre les rubriques visibles</span><span class="sxs-lookup"><span data-stu-id="12ce9-109">Which users you want to make topics visible to</span></span>
- <span data-ttu-id="12ce9-110">Utilisateurs que vous souhaitez autoriser à gérer les rubriques dans le centre de rubriques</span><span class="sxs-lookup"><span data-stu-id="12ce9-110">Which users you want to give permissions to manage topics in the topic center</span></span>
- <span data-ttu-id="12ce9-111">Utilisateurs que vous souhaitez autoriser à créer ou modifier des rubriques dans le centre de rubriques</span><span class="sxs-lookup"><span data-stu-id="12ce9-111">Which users you want to give permissions to create or edit topics in the topic center</span></span>
- <span data-ttu-id="12ce9-112">Quel nom voulez-vous donner à votre centre de rubriques ?</span><span class="sxs-lookup"><span data-stu-id="12ce9-112">What name you want to give your topic center</span></span>

<span data-ttu-id="12ce9-113">La sécurité et la confidentialité de vos données sont respectées, et les expériences de rubrique n’octroient pas aux utilisateurs un accès supplémentaire aux fichiers dont ils n’ont pas le droit.</span><span class="sxs-lookup"><span data-stu-id="12ce9-113">Security and privacy of your data is respected, and topic experiences does not grant users additional access to files they don’t have rights to.</span></span> <span data-ttu-id="12ce9-114">Nous vous recommandons également de lire les [rubriques microsoft sur](topic-experiences-security-privacy.md) la sécurité et la confidentialité dans le cadre de votre processus de planification.</span><span class="sxs-lookup"><span data-stu-id="12ce9-114">We recommend you also read [Microsoft Viva Topics security and privacy](topic-experiences-security-privacy.md) as part of your planning process.</span></span>

<span data-ttu-id="12ce9-115">Pour en savoir plus sur la technologie de l’IA derrière Rubriques, lisez La rubrique Sur le big data et le big knowledge dans [Microsoft Contrôles.](https://www.microsoft.com/research/blog/alexandria-in-microsoft-viva-topics-from-big-data-to-big-knowledge)</span><span class="sxs-lookup"><span data-stu-id="12ce9-115">To learn more about the AI technology behind Viva Topics, read [Alexandria in Microsoft Viva Topics: from big data to big knowledge](https://www.microsoft.com/research/blog/alexandria-in-microsoft-viva-topics-from-big-data-to-big-knowledge).</span></span>

## <a name="requirements"></a><span data-ttu-id="12ce9-116">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="12ce9-116">Requirements</span></span>

<span data-ttu-id="12ce9-117">Vous devez être [abonné à Rubriques Et](https://www.microsoft.com/microsoft-viva/topics) être administrateur général ou administrateur SharePoint pour accéder à la Centre d’administration Microsoft 365 et configurer Rubriques.</span><span class="sxs-lookup"><span data-stu-id="12ce9-117">You must be [subscribed to Viva Topics](https://www.microsoft.com/microsoft-viva/topics) and be a global administrator or SharePoint administrator to access the Microsoft 365 admin center and set up Topics.</span></span>

<span data-ttu-id="12ce9-118">Tous les utilisateurs qui vont utiliser rubriques nécessitent une licence **Expériences de** rubrique.</span><span class="sxs-lookup"><span data-stu-id="12ce9-118">All users who are going to use Topics require a **Topic Experiences** license.</span></span> <span data-ttu-id="12ce9-119">L’attribution de licences est couverte [par la rubrique Configurer Microsoft Topics.](set-up-topic-experiences.md)</span><span class="sxs-lookup"><span data-stu-id="12ce9-119">Assigning licenses is covered in [Set up Microsoft Viva Topics](set-up-topic-experiences.md).</span></span>

## <a name="topic-discovery"></a><span data-ttu-id="12ce9-120">Découverte de rubrique</span><span class="sxs-lookup"><span data-stu-id="12ce9-120">Topic discovery</span></span>

<span data-ttu-id="12ce9-121">Les paramètres de découverte des rubriques spécifient les sites SharePoint utilisés comme sources pour les rubriques.</span><span class="sxs-lookup"><span data-stu-id="12ce9-121">The topic discovery settings specify which SharePoint sites are used as sources for topics.</span></span> <span data-ttu-id="12ce9-122">Cela inclut les sites classiques et modernes, ainsi que les sites associés à Microsoft Teams et Microsoft 365 groupes.</span><span class="sxs-lookup"><span data-stu-id="12ce9-122">This includes both classic and modern sites, as well as sites associated with Microsoft Teams and Microsoft 365 Groups.</span></span> <span data-ttu-id="12ce9-123">OneDrive sites ne sont pas inclus.</span><span class="sxs-lookup"><span data-stu-id="12ce9-123">OneDrive sites are not included.</span></span>

<span data-ttu-id="12ce9-124">Vous pouvez choisir d'inclure tous les sites SharePoint, une liste spécifique de sites ou aucun site.</span><span class="sxs-lookup"><span data-stu-id="12ce9-124">You can choose to include all SharePoint sites, a specific list of sites, or no sites.</span></span> <span data-ttu-id="12ce9-125">Nous vous recommandons de choisir tous les sites afin que les expériences de rubriques puisse découvrir un grand nombre de bonnes rubriques pour vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="12ce9-125">We recommend that you choose all sites so that topic experiences can discover a large number of good topics for your users.</span></span>

<span data-ttu-id="12ce9-126">Lorsque vous définissez Rubriques, vous pouvez choisir l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="12ce9-126">When you set up Topics, you can choose from the following options:</span></span>

- <span data-ttu-id="12ce9-127">**Tous les sites** : tous les sites SharePoint dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="12ce9-127">**All sites**: All SharePoint sites in your organization.</span></span> <span data-ttu-id="12ce9-128">Cela inclut les sites actuels et futurs.</span><span class="sxs-lookup"><span data-stu-id="12ce9-128">This includes current and future sites.</span></span>
- <span data-ttu-id="12ce9-129">**Tous, sauf les sites sélectionnés** : tous les sites à l’exception de ceux que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="12ce9-129">**All, except selected sites**: All sites except for the ones you specify.</span></span> <span data-ttu-id="12ce9-130">Les sites créés à l’avenir seront inclus en tant que sources pour la découverte de rubriques.</span><span class="sxs-lookup"><span data-stu-id="12ce9-130">Sites created in future will be included as sources for topic discovery.</span></span> 
- <span data-ttu-id="12ce9-131">**Uniquement les sites sélectionnés**: uniquement les sites que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="12ce9-131">**Only selected sites**: Only the sites that you specify.</span></span> <span data-ttu-id="12ce9-132">Les sites créés dans le futur ne seront pas inclus comme sources pour la découverte de rubriques.</span><span class="sxs-lookup"><span data-stu-id="12ce9-132">Sites created in the future will not be included as sources for topic discovery.</span></span>
- <span data-ttu-id="12ce9-133">**Aucun site** : n’incluez aucun site SharePoint.</span><span class="sxs-lookup"><span data-stu-id="12ce9-133">**No sites**: Do not include any SharePoint sites.</span></span>

<span data-ttu-id="12ce9-134">Si vous choisissez **Tous, à** l’exception des sites sélectionnés ou uniquement des **sites** sélectionnés, vous pouvez télécharger un fichier .csv avec une liste de sites.</span><span class="sxs-lookup"><span data-stu-id="12ce9-134">If you choose either **All, except selected sites** or **Only selected sites**, you can upload a .csv file with a list of sites.</span></span> <span data-ttu-id="12ce9-135">Ces options sont utiles si vous faites un projet pilote et que vous souhaitez inclure un nombre limité de sites à démarrer.</span><span class="sxs-lookup"><span data-stu-id="12ce9-135">These options are useful if you're doing a pilot and you want to include a limited number of sites to start.</span></span>

<span data-ttu-id="12ce9-136">Vous pouvez copier le modèle .csv ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="12ce9-136">You can copy the .csv template below:</span></span>

``` csv
Site name,URL
```

<span data-ttu-id="12ce9-137">Nous vous déconseillons de choisir Aucun **site,** car cela empêche la création ou la mise à jour automatique des rubriques.</span><span class="sxs-lookup"><span data-stu-id="12ce9-137">We don't recommend choosing **No sites** because it prevents topics from being automatically created or updated.</span></span> <span data-ttu-id="12ce9-138">Toutefois, vous pouvez choisir cette option si vous souhaitez configurer Rubriques, puis ajouter des sites ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="12ce9-138">However, you can choose this option if you want to set up Topics and then add sites later.</span></span>

<span data-ttu-id="12ce9-139">Nous vous recommandons de créer un processus pour que les utilisateurs ou les gestionnaires de connaissances demandent que des sites individuels soient supprimés de la découverte de rubriques si nécessaire dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="12ce9-139">We recommend you create a process for users or knowledge managers to request individual sites be removed from topic discovery if needed in your organization.</span></span>

### <a name="multi-geo"></a><span data-ttu-id="12ce9-140">Multi-Géo</span><span class="sxs-lookup"><span data-stu-id="12ce9-140">Multi-geo</span></span>

<span data-ttu-id="12ce9-141">Si votre organisation a déployé [Microsoft 365 Multi-Géo,](/microsoft-365/enterprise/microsoft-365-multi-geo)le centre de rubriques est mis en service dans l’emplacement central et seuls les sites SharePoint de l’emplacement central peuvent être utilisés comme sources pour les rubriques.</span><span class="sxs-lookup"><span data-stu-id="12ce9-141">If your organization has deployed [Microsoft 365 Multi-Geo](/microsoft-365/enterprise/microsoft-365-multi-geo), the topic center is provisioned in the central location and only SharePoint sites in the central location are available to use as sources for topics.</span></span> <span data-ttu-id="12ce9-142">(Si vous sélectionnez **Tous les sites,** Rubriques Topics utilisera tous les sites dans l’emplacement central.)</span><span class="sxs-lookup"><span data-stu-id="12ce9-142">(If you select **All sites**, Viva Topics will use all site in the central location.)</span></span>

<span data-ttu-id="12ce9-143">Tout le traitement et le stockage du contenu sont effectués à l’emplacement central.</span><span class="sxs-lookup"><span data-stu-id="12ce9-143">All processing and storage of content is done in the central location.</span></span>

## <a name="user-permissions"></a><span data-ttu-id="12ce9-144">Autorisations utilisateur</span><span class="sxs-lookup"><span data-stu-id="12ce9-144">User permissions</span></span>

<span data-ttu-id="12ce9-145">Les autorisations utilisateur que vous spécifiez déterminent les personnes de votre organisation qui interagissent avec les rubriques et ce qu’elles peuvent faire.</span><span class="sxs-lookup"><span data-stu-id="12ce9-145">The user permissions that you specify determine which people in your organization interact with topics and what they can do.</span></span>

> [!Note] 
> <span data-ttu-id="12ce9-146">Pour l’instant, Topics ne prend pas en charge la fourniture de licences ou d’autorisations utilisateur pour les utilisateurs invités (externes).</span><span class="sxs-lookup"><span data-stu-id="12ce9-146">At this time, Viva Topics doesn't support providing licenses or user permissions for Guest (External) users.</span></span> 

<span data-ttu-id="12ce9-147">*Gestion des rubriques*</span><span class="sxs-lookup"><span data-stu-id="12ce9-147">*Manage topics*</span></span>

<span data-ttu-id="12ce9-148">Les gestionnaires de connaissances supervisent la qualité des informations, la façon dont elles sont structurées et d’autres meilleures pratiques au niveau de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="12ce9-148">Knowledge managers oversee the quality of information, how its structured, and other best practices in your organization.</span></span> <span data-ttu-id="12ce9-149">Ils peuvent confirmer et rejeter des rubriques.</span><span class="sxs-lookup"><span data-stu-id="12ce9-149">They can confirm and reject topics.</span></span>

<span data-ttu-id="12ce9-150">Bien que vous pouvez spécifier des responsables de rubriques individuels, nous vous recommandons de créer un groupe de sécurité (ou d’utiliser un groupe existant) qui contient les personnes que vous souhaitez utiliser comme responsables de connaissances.</span><span class="sxs-lookup"><span data-stu-id="12ce9-150">While you can specify individual topic managers, we recommend that you create a security group (or use an existing one) that contains the people who you want to be knowledge managers.</span></span> <span data-ttu-id="12ce9-151">Vous pouvez spécifier ce groupe de sécurité pendant le processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="12ce9-151">You can specify this security group during the setup process.</span></span>

<span data-ttu-id="12ce9-152">*Créer et modifier des rubriques.*</span><span class="sxs-lookup"><span data-stu-id="12ce9-152">*Create and edit topics*</span></span>

<span data-ttu-id="12ce9-153">Les contributeurs de rubriques sont les champions et les experts techniques de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="12ce9-153">Topic contributors are the champions and subject matter experts in your organization.</span></span> <span data-ttu-id="12ce9-154">Ils peuvent créer et modifier des rubriques.</span><span class="sxs-lookup"><span data-stu-id="12ce9-154">They can create and edit topics.</span></span> 

<span data-ttu-id="12ce9-155">Nous vous recommandons d’autoriser tous les membres de votre organisation à créer et modifier des rubriques, car les expériences de rubrique fonctionnent mieux lorsque tous les utilisateurs peuvent partager des informations.</span><span class="sxs-lookup"><span data-stu-id="12ce9-155">We recommend that you allow everyone in your organization to create and edit topics because topic experiences work best when all users can share information.</span></span>

<span data-ttu-id="12ce9-156">Si vous souhaitez limiter la création et la modification de rubriques à des personnes ou des groupes spécifiques, créez un groupe de sécurité pour eux et spécifiez-le pendant le processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="12ce9-156">If you want to limit creating and editing topics to specific people or groups, create a security group for them and specify it during the setup process.</span></span>

<span data-ttu-id="12ce9-157">Vous pouvez choisir de ne permettre à personne de contribuer à des rubriques, mais cela n’est pas recommandé.</span><span class="sxs-lookup"><span data-stu-id="12ce9-157">You can choose to not allow anyone to contribute to topics, however this is not recommended.</span></span> <span data-ttu-id="12ce9-158">Les gestionnaires de connaissances pourront toujours modifier et créer des rubriques si vous choisissez cette option.</span><span class="sxs-lookup"><span data-stu-id="12ce9-158">Knowledge managers will still be able to edit and create topics if you choose this option.</span></span>

<span data-ttu-id="12ce9-159">*Visionneuses de rubriques*</span><span class="sxs-lookup"><span data-stu-id="12ce9-159">*Topic viewers*</span></span>

<span data-ttu-id="12ce9-160">Les visiteurs peuvent voir des informations sur les pages de rubriques, dans les résultats de la recherche et lorsque des rubriques sont mises en surbrillez dans le contenu tel que SharePoint pages.</span><span class="sxs-lookup"><span data-stu-id="12ce9-160">Topic viewers can see information on topic pages, in search results and when topics are highlighted in the content like SharePoint pages.</span></span> <span data-ttu-id="12ce9-161">Les utilisateurs peuvent uniquement voir les rubriques découvertes lorsqu’ils ont accès aux fichiers et aux pages dans qui la rubrique a été découverte.</span><span class="sxs-lookup"><span data-stu-id="12ce9-161">Users can only see discovered topics when they have access to the files and pages the topic was discovered in.</span></span>

<span data-ttu-id="12ce9-162">Lors de la configuration des visionneuses de rubriques, vous pouvez choisir parmi :</span><span class="sxs-lookup"><span data-stu-id="12ce9-162">When setting up topic viewers, you can choose from:</span></span>

- <span data-ttu-id="12ce9-163">**Tous les membres de mon organisation**</span><span class="sxs-lookup"><span data-stu-id="12ce9-163">**Everyone in my organization**</span></span>
- <span data-ttu-id="12ce9-164">**Personnes ou groupes de sécurité sélectionnés uniquement**</span><span class="sxs-lookup"><span data-stu-id="12ce9-164">**Only selected people or security groups**</span></span>
- <span data-ttu-id="12ce9-165">**Personne**</span><span class="sxs-lookup"><span data-stu-id="12ce9-165">**No one**</span></span>

<span data-ttu-id="12ce9-166">Nous vous **recommandons tout le monde** dans mon organisation, mais si vous faites un projet pilote, vous pouvez choisir uniquement des personnes ou des groupes de sécurité sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="12ce9-166">We recommend **Everyone in my organization**, but if you're doing a pilot you may want to choose only selected people or security groups.</span></span> <span data-ttu-id="12ce9-167">Vous pouvez également choisir **Personne** si vous souhaitez configurer Des rubriques, mais ne pas autoriser les personnes à voir les rubriques pour le moment.</span><span class="sxs-lookup"><span data-stu-id="12ce9-167">You can also choose **No one** if you want to set up Topics, but not allow people to see topics yet.</span></span> <span data-ttu-id="12ce9-168">(Les gestionnaires de connaissances auront toujours accès pour leur permettre d’afficher les rubriques et d’aider à prendre la décision de rendre les rubriques largement disponibles.)</span><span class="sxs-lookup"><span data-stu-id="12ce9-168">(Knowledge managers will still have access to allow them view the topics and help with the decision to make Topics broadly available.)</span></span>

## <a name="knowledge-rules"></a><span data-ttu-id="12ce9-169">Règles de connaissance</span><span class="sxs-lookup"><span data-stu-id="12ce9-169">Knowledge rules</span></span>

<span data-ttu-id="12ce9-170">En tant qu’administrateur, vous pouvez exclure certaines rubriques des expériences de rubrique.</span><span class="sxs-lookup"><span data-stu-id="12ce9-170">As an administrator, you can exclude certain topics from topic experiences.</span></span> <span data-ttu-id="12ce9-171">Cela est utile si vous souhaitez empêcher les données sensibles d’apparaître dans les rubriques.</span><span class="sxs-lookup"><span data-stu-id="12ce9-171">This is useful if you want to keep sensitive data from appearing in topics.</span></span> <span data-ttu-id="12ce9-172">Bien que les gestionnaires de connaissances peuvent exclure des rubriques dans le centre de rubriques, les rubriques exclues par l’administrateur ne sont même pas visibles pour les gestionnaires de connaissances.</span><span class="sxs-lookup"><span data-stu-id="12ce9-172">While knowledge managers can exclude topics in the topic center, topics excluded by the administrator are not even visible to knowledge managers.</span></span> <span data-ttu-id="12ce9-173">(Les gestionnaires de connaissances peuvent également supprimer des rubriques dans le centre de rubriques après la découverte.)</span><span class="sxs-lookup"><span data-stu-id="12ce9-173">(Knowledge managers can also remove topics in the topic center after discovery.)</span></span>

<span data-ttu-id="12ce9-174">Si vous souhaitez exclure des rubriques au niveau de l’administrateur, vous devez les ajouter à un .csv et télécharger le fichier.</span><span class="sxs-lookup"><span data-stu-id="12ce9-174">If you want to exclude topics at the administrator level, you must add them to a .csv file and upload the file.</span></span> <span data-ttu-id="12ce9-175">Vous pouvez le faire lors de l’installation ou ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="12ce9-175">You can do this during setup or later.</span></span>

<span data-ttu-id="12ce9-176">Le .csv doit contenir les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="12ce9-176">The .csv file must contain the following parameters:</span></span>

- <span data-ttu-id="12ce9-177">**Nom** : tapez le nom de la rubrique à exclure.</span><span class="sxs-lookup"><span data-stu-id="12ce9-177">**Name**: Type the name of the topic you want to exclude.</span></span> <span data-ttu-id="12ce9-178">Il existe deux méthodes pour y parvenir :</span><span class="sxs-lookup"><span data-stu-id="12ce9-178">There are two ways to do this:</span></span>
- <span data-ttu-id="12ce9-179">**MatchType-Exact/Partial**: tapez si le nom que vous avez entré était un type de correspondance *exact* *ou* partiel.</span><span class="sxs-lookup"><span data-stu-id="12ce9-179">**MatchType-Exact/Partial**: Type whether the name you entered was an *exact* or *partial* match type.</span></span>
    - <span data-ttu-id="12ce9-180">Correspondance exacte : vous pouvez inclure le nom exact ou l’acronyme (par exemple, *Contoso* ou *ATL*).</span><span class="sxs-lookup"><span data-stu-id="12ce9-180">Exact match: You can include the exact name or acronym (for example, *Contoso* or *ATL*).</span></span>
    - <span data-ttu-id="12ce9-181">Correspondance partielle : vous pouvez exclure toutes les rubriques qui ont un mot spécifique.</span><span class="sxs-lookup"><span data-stu-id="12ce9-181">Partial match: You can exclude all topics that have a specific word in it.</span></span>  <span data-ttu-id="12ce9-182">Par exemple, *arc exclura* toutes les rubriques avec le mot *arc* dans celui-ci, telles que le cercle *d’arc,* *l’arc de Pierre ou* *l’arc de formation*. Notez qu’il n’exclura pas les rubriques dans lesquelles le texte est inclus dans le cadre d’un mot, comme *Architecture*.</span><span class="sxs-lookup"><span data-stu-id="12ce9-182">For example, *arc* will exclude all topics with the word *arc* in it, such as *Arc circle*, *Plasma arc welding*, or *Training arc*. Note that it will not exclude topics in which the text is included as part of a word, such as *Architecture*.</span></span>
- <span data-ttu-id="12ce9-183">**Signifie (facultatif)**: (également appelé *expansion)* Si vous souhaitez exclure un acronyme, tapez les mots qu’il signifie.</span><span class="sxs-lookup"><span data-stu-id="12ce9-183">**Stands for (optional)**: (Also known as *expansion*) If you want to exclude an acronym, type the words the acronym stands for.</span></span>

    ![Exclure des rubriques dans le modèle CSV](../media/exclude-topics-csv.png) 

<span data-ttu-id="12ce9-185">Vous pouvez copier le modèle csv ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="12ce9-185">You can copy the csv template below:</span></span>

``` csv
Name (required),Expansion,MatchType- Exact/Partial (required)
```

## <a name="administration"></a><span data-ttu-id="12ce9-186">Administration</span><span class="sxs-lookup"><span data-stu-id="12ce9-186">Administration</span></span>

<span data-ttu-id="12ce9-187">Lorsque vous définissez Rubriques, dans le cadre du processus d’installation, un centre de rubriques est automatiquement créé.</span><span class="sxs-lookup"><span data-stu-id="12ce9-187">When you set up Topics, as part of the setup process, a topic center is automatically created.</span></span> <span data-ttu-id="12ce9-188">Réfléchissez à ce que vous souhaitez nommer le centre de rubriques et à ce que doit être l’URL.</span><span class="sxs-lookup"><span data-stu-id="12ce9-188">Think about what you want to name the topic center and what you want the URL to be.</span></span> <span data-ttu-id="12ce9-189">Vous pouvez définir le nom et l’URL dans le cadre du processus d’installation, et vous pouvez modifier le nom (mais pas l’URL) plus loin dans la Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="12ce9-189">You can set both the name and URL as part of the setup process, and you can change the name (but not URL) later in the Microsoft 365 admin center.</span></span> <span data-ttu-id="12ce9-190">Vous ne pouvez avoir qu’un seul centre de rubriques.</span><span class="sxs-lookup"><span data-stu-id="12ce9-190">You can only have one topic center.</span></span>

## <a name="setup-checklist"></a><span data-ttu-id="12ce9-191">Liste de vérification du programme d’installation</span><span class="sxs-lookup"><span data-stu-id="12ce9-191">Setup checklist</span></span>

<span data-ttu-id="12ce9-192">Lorsque vous configurerez des expériences de rubrique, vous aurez besoin des éléments suivants à mesure que vous passerez par l’Assistant Installation :</span><span class="sxs-lookup"><span data-stu-id="12ce9-192">When you set up topic experiences, you'll need the following items as you go through the setup wizard:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="12ce9-193">La liste des sites à inclure ou à exclure si vous n’incluez pas tous les sites pour la découverte de rubriques</span><span class="sxs-lookup"><span data-stu-id="12ce9-193">List of sites to include or exclude if not including all sites for topic discovery</span></span>
> * <span data-ttu-id="12ce9-194">Le groupe de sécurité pour les spectateurs des rubriques s’il ne permet pas à tous les utilisateurs d’afficher les rubriques</span><span class="sxs-lookup"><span data-stu-id="12ce9-194">Security group for topic viewers if not allowing all users to view topics</span></span>
> * <span data-ttu-id="12ce9-195">Le groupe de sécurité pour les contributeurs de rubriques s’il ne permet pas à tous les utilisateurs de créer et de modifier des rubriques</span><span class="sxs-lookup"><span data-stu-id="12ce9-195">Security group for topic contributors if not allowing all users to create and edit topics</span></span>
> * <span data-ttu-id="12ce9-196">Le groupe de sécurité pour les gestionnaires des connaissances pour les rubriques s’il ne permet pas à tous les utilisateurs de gérer les rubriques</span><span class="sxs-lookup"><span data-stu-id="12ce9-196">Security group for topic knowledge managers if not allowing all users to manage topics</span></span>
> * <span data-ttu-id="12ce9-197">Liste des rubriques sensibles à exclure de la découverte de rubriques</span><span class="sxs-lookup"><span data-stu-id="12ce9-197">List of sensitive topics to exclude from topic discovery</span></span>
> * <span data-ttu-id="12ce9-198">Nom de votre site centre de rubriques</span><span class="sxs-lookup"><span data-stu-id="12ce9-198">A name for your topic center site</span></span>

## <a name="see-also"></a><span data-ttu-id="12ce9-199">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12ce9-199">See also</span></span>

[<span data-ttu-id="12ce9-200">Configurer les expériences de sujets</span><span class="sxs-lookup"><span data-stu-id="12ce9-200">Set up topic experiences</span></span>](set-up-topic-experiences.md)

[<span data-ttu-id="12ce9-201">Gérer la découverte de rubriques dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="12ce9-201">Manage topic discovery in Microsoft 365</span></span>](topic-experiences-discovery.md)

[<span data-ttu-id="12ce9-202">Gérer la visibilité des rubriques dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="12ce9-202">Manage topic visibility in Microsoft 365</span></span>](topic-experiences-knowledge-rules.md)

[<span data-ttu-id="12ce9-203">Gérer les autorisations de rubrique dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="12ce9-203">Manage topic permissions in Microsoft 365</span></span>](topic-experiences-user-permissions.md)

[<span data-ttu-id="12ce9-204">Modifier le nom du centre de rubriques dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="12ce9-204">Change the name of the topic center in Microsoft 365</span></span>](topic-experiences-administration.md)
