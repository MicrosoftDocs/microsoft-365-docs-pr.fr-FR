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
ms.openlocfilehash: 19baf8bdcfdd1fe38d64e3c2f259ace1ceab5a4b
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50925975"
---
# <a name="plan-for-microsoft-viva-topics"></a><span data-ttu-id="02c12-103">Planifier les rubriques microsoft</span><span class="sxs-lookup"><span data-stu-id="02c12-103">Plan for Microsoft Viva Topics</span></span>

<span data-ttu-id="02c12-104">Vous contrôlez la façon dont les sujets sont abordés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="02c12-104">You're in control of how topics are experienced in your organization.</span></span> <span data-ttu-id="02c12-105">Vos décisions de planification pour Rubriques garantissent que les rubriques de haute qualité sont présentées à vos utilisateurs et qu’ils ont les autorisations nécessaires pour consommer et contribuer aux connaissances.</span><span class="sxs-lookup"><span data-stu-id="02c12-105">Your planning decisions for Topics ensures that high quality topics are shown to your users and they have the right permissions to consume and contribute knowledge.</span></span>

<span data-ttu-id="02c12-106">Dans cet article, nous examinerons les décisions de planification ci-après :</span><span class="sxs-lookup"><span data-stu-id="02c12-106">In this article we'll examine these planning decisions:</span></span>

- <span data-ttu-id="02c12-107">Les sites SharePoint que vous souhaitez analyser pour les rubriques</span><span class="sxs-lookup"><span data-stu-id="02c12-107">Which SharePoint sites you want to crawl for topics</span></span>
- <span data-ttu-id="02c12-108">Les rubriques, le cas besoin, que vous souhaitez exclure des expériences de rubrique</span><span class="sxs-lookup"><span data-stu-id="02c12-108">Which topics, if any, you want to exclude from topic experiences</span></span>
- <span data-ttu-id="02c12-109">Utilisateurs pour lesquels vous souhaitez rendre les rubriques visibles</span><span class="sxs-lookup"><span data-stu-id="02c12-109">Which users you want to make topics visible to</span></span>
- <span data-ttu-id="02c12-110">Utilisateurs que vous souhaitez autoriser à gérer les rubriques dans le centre de rubriques</span><span class="sxs-lookup"><span data-stu-id="02c12-110">Which users you want to give permissions to manage topics in the topic center</span></span>
- <span data-ttu-id="02c12-111">Utilisateurs que vous souhaitez autoriser à créer ou modifier des rubriques dans le centre de rubriques</span><span class="sxs-lookup"><span data-stu-id="02c12-111">Which users you want to give permissions to create or edit topics in the topic center</span></span>
- <span data-ttu-id="02c12-112">Quel nom voulez-vous donner à votre centre de rubriques ?</span><span class="sxs-lookup"><span data-stu-id="02c12-112">What name you want to give your topic center</span></span>

<span data-ttu-id="02c12-113">La sécurité et la confidentialité de vos données sont respectées, et les expériences de rubrique n’octroient pas aux utilisateurs un accès supplémentaire aux fichiers dont ils n’ont pas le droit.</span><span class="sxs-lookup"><span data-stu-id="02c12-113">Security and privacy of your data is respected, and topic experiences does not grant users additional access to files they don’t have rights to.</span></span> <span data-ttu-id="02c12-114">Nous vous recommandons également de lire les [rubriques microsoft sur](topic-experiences-security-privacy.md) la sécurité et la confidentialité dans le cadre de votre processus de planification.</span><span class="sxs-lookup"><span data-stu-id="02c12-114">We recommend you also read [Microsoft Viva Topics security and privacy](topic-experiences-security-privacy.md) as part of your planning process.</span></span>

## <a name="requirements"></a><span data-ttu-id="02c12-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02c12-115">Requirements</span></span>

<span data-ttu-id="02c12-116">Vous devez être abonné à [Rubriques Et](https://www.microsoft.com/microsoft-viva/topics) être administrateur général ou administrateur SharePoint pour accéder au Centre d’administration Microsoft 365 et configurer Rubriques.</span><span class="sxs-lookup"><span data-stu-id="02c12-116">You must be [subscribed to Viva Topics](https://www.microsoft.com/microsoft-viva/topics) and be a global administrator or SharePoint administrator to access the Microsoft 365 admin center and set up Topics.</span></span>

<span data-ttu-id="02c12-117">Tous les utilisateurs qui vont utiliser rubriques nécessitent une licence **Expériences de** rubrique.</span><span class="sxs-lookup"><span data-stu-id="02c12-117">All users who are going to use Topics require a **Topic Experiences** license.</span></span> <span data-ttu-id="02c12-118">L’attribution de licences est couverte [par la rubrique Configurer Microsoft Topics.](set-up-topic-experiences.md)</span><span class="sxs-lookup"><span data-stu-id="02c12-118">Assigning licenses is covered in [Set up Microsoft Viva Topics](set-up-topic-experiences.md).</span></span>

## <a name="topic-discovery"></a><span data-ttu-id="02c12-119">Découverte de rubrique</span><span class="sxs-lookup"><span data-stu-id="02c12-119">Topic discovery</span></span>

<span data-ttu-id="02c12-120">Les paramètres de découverte de rubrique spécifient les sites SharePoint qui sont utilisés comme sources pour les rubriques.</span><span class="sxs-lookup"><span data-stu-id="02c12-120">The topic discovery settings specify which SharePoint sites are used as sources for topics.</span></span> <span data-ttu-id="02c12-121">Vous pouvez choisir d’inclure tous les sites SharePoint, une liste spécifique de sites ou aucun site.</span><span class="sxs-lookup"><span data-stu-id="02c12-121">You can choose to include all SharePoint sites, a specific list of sites, or no sites.</span></span> <span data-ttu-id="02c12-122">Nous vous recommandons de choisir tous les sites afin que les expériences de rubriques puisse découvrir un grand nombre de bonnes rubriques pour vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="02c12-122">We recommend that you choose all sites so that topic experiences can discover a large number of good topics for your users.</span></span>

<span data-ttu-id="02c12-123">Lorsque vous définissez Rubriques, vous pouvez choisir parmi les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="02c12-123">When you set up Topics, you can choose from the following options:</span></span>

- <span data-ttu-id="02c12-124">**Tous les sites**: tous les sites SharePoint de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="02c12-124">**All sites**: All SharePoint sites in your organization.</span></span> <span data-ttu-id="02c12-125">Cela inclut les sites actuels et futurs.</span><span class="sxs-lookup"><span data-stu-id="02c12-125">This includes current and future sites.</span></span>
- <span data-ttu-id="02c12-126">**Tous, à l’exception des sites** sélectionnés : tous les sites à l’exception de ceux que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="02c12-126">**All, except selected sites**: All sites except for the ones you specify.</span></span> <span data-ttu-id="02c12-127">Les sites créés à l’avenir seront inclus en tant que sources pour la découverte de rubriques.</span><span class="sxs-lookup"><span data-stu-id="02c12-127">Sites created in future will be included as sources for topic discovery.</span></span> 
- <span data-ttu-id="02c12-128">**Uniquement les sites sélectionnés**: uniquement les sites que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="02c12-128">**Only selected sites**: Only the sites that you specify.</span></span> <span data-ttu-id="02c12-129">Les sites créés à l’avenir ne seront pas inclus en tant que sources de découverte de sujet.</span><span class="sxs-lookup"><span data-stu-id="02c12-129">Sites created in the future will not be included as sources for topic discovery.</span></span>
- <span data-ttu-id="02c12-130">**Aucun site**: n’incluez aucun site SharePoint.</span><span class="sxs-lookup"><span data-stu-id="02c12-130">**No sites**: Do not include any SharePoint sites.</span></span>

<span data-ttu-id="02c12-131">Si vous choisissez **Tous, à** l’exception des sites sélectionnés ou uniquement des **sites** sélectionnés, vous pouvez télécharger un fichier .csv avec une liste de sites.</span><span class="sxs-lookup"><span data-stu-id="02c12-131">If you choose either **All, except selected sites** or **Only selected sites**, you can upload a .csv file with a list of sites.</span></span> <span data-ttu-id="02c12-132">Ces options sont utiles si vous faites un projet pilote et que vous souhaitez inclure un nombre limité de sites à démarrer.</span><span class="sxs-lookup"><span data-stu-id="02c12-132">These options are useful if you're doing a pilot and you want to include a limited number of sites to start.</span></span>

<span data-ttu-id="02c12-133">Vous pouvez copier le modèle .csv ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="02c12-133">You can copy the .csv template below:</span></span>

``` csv
Site name,URL
```

<span data-ttu-id="02c12-134">Nous vous déconseillons de choisir Aucun **site,** car cela empêche la création ou la mise à jour automatique des rubriques.</span><span class="sxs-lookup"><span data-stu-id="02c12-134">We don't recommend choosing **No sites** because it prevents topics from being automatically created or updated.</span></span> <span data-ttu-id="02c12-135">Toutefois, vous pouvez choisir cette option si vous souhaitez configurer Rubriques, puis ajouter des sites ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="02c12-135">However, you can choose this option if you want to set up Topics and then add sites later.</span></span>

<span data-ttu-id="02c12-136">Nous vous recommandons de créer un processus pour que les utilisateurs ou les gestionnaires de connaissances demandent que des sites individuels soient supprimés de la découverte de rubriques si nécessaire dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="02c12-136">We recommend you create a process for users or knowledge managers to request individual sites be removed from topic discovery if needed in your organization.</span></span>

### <a name="multi-geo"></a><span data-ttu-id="02c12-137">Multi-Géo</span><span class="sxs-lookup"><span data-stu-id="02c12-137">Multi-geo</span></span>

<span data-ttu-id="02c12-138">Si votre organisation a déployé [Microsoft 365 Multi-Géo,](/microsoft-365/enterprise/microsoft-365-multi-geo)le centre de rubriques est mis en service dans l’emplacement central et seuls les sites SharePoint de l’emplacement central peuvent être utilisés comme sources pour les rubriques.</span><span class="sxs-lookup"><span data-stu-id="02c12-138">If your organization has deployed [Microsoft 365 Multi-Geo](/microsoft-365/enterprise/microsoft-365-multi-geo), the topic center is provisioned in the central location and only SharePoint sites in the central location are available to use as sources for topics.</span></span> <span data-ttu-id="02c12-139">(Si vous sélectionnez **Tous les sites,** Rubriques Topics utilisera tous les sites dans l’emplacement central.)</span><span class="sxs-lookup"><span data-stu-id="02c12-139">(If you select **All sites**, Viva Topics will use all site in the central location.)</span></span>

<span data-ttu-id="02c12-140">Tout le traitement et le stockage du contenu sont effectués à l’emplacement central.</span><span class="sxs-lookup"><span data-stu-id="02c12-140">All processing and storage of content is done in the central location.</span></span>

## <a name="user-permissions"></a><span data-ttu-id="02c12-141">Autorisations utilisateur</span><span class="sxs-lookup"><span data-stu-id="02c12-141">User permissions</span></span>

<span data-ttu-id="02c12-142">Les autorisations utilisateur que vous spécifiez déterminent les personnes de votre organisation qui interagissent avec les rubriques et ce qu’elles peuvent faire.</span><span class="sxs-lookup"><span data-stu-id="02c12-142">The user permissions that you specify determine which people in your organization interact with topics and what they can do.</span></span>

<span data-ttu-id="02c12-143">*Gestion des rubriques*</span><span class="sxs-lookup"><span data-stu-id="02c12-143">*Manage topics*</span></span>

<span data-ttu-id="02c12-144">Les gestionnaires de connaissances supervisent la qualité des informations, la façon dont elles sont structurées et d’autres meilleures pratiques au niveau de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="02c12-144">Knowledge managers oversee the quality of information, how its structured, and other best practices in your organization.</span></span> <span data-ttu-id="02c12-145">Ils peuvent confirmer et rejeter des rubriques.</span><span class="sxs-lookup"><span data-stu-id="02c12-145">They can confirm and reject topics.</span></span>

<span data-ttu-id="02c12-146">Bien que vous pouvez spécifier des responsables de rubriques individuels, nous vous recommandons de créer un groupe de sécurité (ou d’utiliser un groupe existant) qui contient les personnes que vous souhaitez utiliser comme responsables de connaissances.</span><span class="sxs-lookup"><span data-stu-id="02c12-146">While you can specify individual topic managers, we recommend that you create a security group (or use an existing one) that contains the people who you want to be knowledge managers.</span></span> <span data-ttu-id="02c12-147">Vous pouvez spécifier ce groupe de sécurité pendant le processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="02c12-147">You can specify this security group during the setup process.</span></span>

<span data-ttu-id="02c12-148">*Créer et modifier des rubriques*</span><span class="sxs-lookup"><span data-stu-id="02c12-148">*Create and edit topics*</span></span>

<span data-ttu-id="02c12-149">Les contributeurs de rubriques sont les champions et les experts techniques de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="02c12-149">Topic contributors are the champions and subject matter experts in your organization.</span></span> <span data-ttu-id="02c12-150">Ils peuvent créer et modifier des rubriques.</span><span class="sxs-lookup"><span data-stu-id="02c12-150">They can create and edit topics.</span></span> 

<span data-ttu-id="02c12-151">Nous vous recommandons d’autoriser tous les membres de votre organisation à créer et modifier des rubriques, car les expériences de rubrique fonctionnent mieux lorsque tous les utilisateurs peuvent partager des informations.</span><span class="sxs-lookup"><span data-stu-id="02c12-151">We recommend that you allow everyone in your organization to create and edit topics because topic experiences work best when all users can share information.</span></span>

<span data-ttu-id="02c12-152">Si vous souhaitez limiter la création et la modification de rubriques à des personnes ou des groupes spécifiques, créez un groupe de sécurité pour eux et spécifiez-le pendant le processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="02c12-152">If you want to limit creating and editing topics to specific people or groups, create a security group for them and specify it during the setup process.</span></span>

<span data-ttu-id="02c12-153">Vous pouvez choisir de ne permettre à personne de contribuer à des rubriques, mais cela n’est pas recommandé.</span><span class="sxs-lookup"><span data-stu-id="02c12-153">You can choose to not allow anyone to contribute to topics, however this is not recommended.</span></span> <span data-ttu-id="02c12-154">Les gestionnaires de connaissances pourront toujours modifier et créer des rubriques si vous choisissez cette option.</span><span class="sxs-lookup"><span data-stu-id="02c12-154">Knowledge managers will still be able to edit and create topics if you choose this option.</span></span>

<span data-ttu-id="02c12-155">*Visionneuses de rubriques*</span><span class="sxs-lookup"><span data-stu-id="02c12-155">*Topic viewers*</span></span>

<span data-ttu-id="02c12-156">Les visiteurs peuvent voir des informations sur les pages de rubrique, dans les résultats de la recherche et lorsque des rubriques sont mises en surbrillables dans le contenu tel que les pages SharePoint.</span><span class="sxs-lookup"><span data-stu-id="02c12-156">Topic viewers can see information on topic pages, in search results and when topics are highlighted in the content like SharePoint pages.</span></span> <span data-ttu-id="02c12-157">Les utilisateurs peuvent uniquement voir les rubriques découvertes lorsqu’ils ont accès aux fichiers et aux pages dans qui la rubrique a été découverte.</span><span class="sxs-lookup"><span data-stu-id="02c12-157">Users can only see discovered topics when they have access to the files and pages the topic was discovered in.</span></span>

<span data-ttu-id="02c12-158">Lors de la configuration des visionneuses de rubriques, vous pouvez choisir parmi :</span><span class="sxs-lookup"><span data-stu-id="02c12-158">When setting up topic viewers, you can choose from:</span></span>

- <span data-ttu-id="02c12-159">**Tous les membres de mon organisation**</span><span class="sxs-lookup"><span data-stu-id="02c12-159">**Everyone in my organization**</span></span>
- <span data-ttu-id="02c12-160">**Personnes ou groupes de sécurité sélectionnés uniquement**</span><span class="sxs-lookup"><span data-stu-id="02c12-160">**Only selected people or security groups**</span></span>
- <span data-ttu-id="02c12-161">**Personne**</span><span class="sxs-lookup"><span data-stu-id="02c12-161">**No one**</span></span>

<span data-ttu-id="02c12-162">Nous vous **recommandons tout le monde** dans mon organisation, mais si vous faites un projet pilote, vous pouvez choisir uniquement des personnes ou des groupes de sécurité sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="02c12-162">We recommend **Everyone in my organization**, but if you're doing a pilot you may want to choose only selected people or security groups.</span></span> <span data-ttu-id="02c12-163">Vous pouvez également choisir **Personne** si vous souhaitez configurer Des rubriques, mais ne pas autoriser les utilisateurs à voir les rubriques pour le moment.</span><span class="sxs-lookup"><span data-stu-id="02c12-163">You can also choose **No one** if you want to set up Topics, but not allow people to see topics yet.</span></span> <span data-ttu-id="02c12-164">(Les gestionnaires de connaissances auront toujours accès pour leur permettre d’afficher les rubriques et d’aider à prendre la décision de rendre les rubriques largement disponibles.)</span><span class="sxs-lookup"><span data-stu-id="02c12-164">(Knowledge managers will still have access to allow them view the topics and help with the decision to make Topics broadly available.)</span></span>

## <a name="knowledge-rules"></a><span data-ttu-id="02c12-165">Règles de connaissance</span><span class="sxs-lookup"><span data-stu-id="02c12-165">Knowledge rules</span></span>

<span data-ttu-id="02c12-166">En tant qu’administrateur, vous pouvez exclure certaines rubriques des expériences de rubrique.</span><span class="sxs-lookup"><span data-stu-id="02c12-166">As an administrator, you can exclude certain topics from topic experiences.</span></span> <span data-ttu-id="02c12-167">Cela est utile si vous souhaitez empêcher les données sensibles d’apparaître dans les rubriques.</span><span class="sxs-lookup"><span data-stu-id="02c12-167">This is useful if you want to keep sensitive data from appearing in topics.</span></span> <span data-ttu-id="02c12-168">Bien que les gestionnaires de connaissances peuvent exclure des rubriques dans le centre de rubriques, les rubriques exclues par l’administrateur ne sont même pas visibles pour les gestionnaires de connaissances.</span><span class="sxs-lookup"><span data-stu-id="02c12-168">While knowledge managers can exclude topics in the topic center, topics excluded by the administrator are not even visible to knowledge managers.</span></span> <span data-ttu-id="02c12-169">(Les gestionnaires de connaissances peuvent également supprimer des rubriques dans le centre de rubriques après la découverte.)</span><span class="sxs-lookup"><span data-stu-id="02c12-169">(Knowledge managers can also remove topics in the topic center after discovery.)</span></span>

<span data-ttu-id="02c12-170">Si vous souhaitez exclure des rubriques au niveau de l’administrateur, vous devez les ajouter à un fichier .csv et télécharger le fichier.</span><span class="sxs-lookup"><span data-stu-id="02c12-170">If you want to exclude topics at the administrator level, you must add them to a .csv file and upload the file.</span></span> <span data-ttu-id="02c12-171">Vous pouvez le faire lors de l’installation ou ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="02c12-171">You can do this during setup or later.</span></span>

<span data-ttu-id="02c12-172">Le fichier .csv doit contenir les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="02c12-172">The .csv file must contain the following parameters:</span></span>

- <span data-ttu-id="02c12-173">**Nom**: tapez le nom de la rubrique que vous souhaitez exclure.</span><span class="sxs-lookup"><span data-stu-id="02c12-173">**Name**: Type the name of the topic you want to exclude.</span></span> <span data-ttu-id="02c12-174">Vous pouvez procéder de deux manières :</span><span class="sxs-lookup"><span data-stu-id="02c12-174">There are two ways to do this:</span></span>
- <span data-ttu-id="02c12-175">**MatchType-Exact/Partial**: tapez si le nom que vous avez entré était un type de correspondance *exacte* *ou* partielle.</span><span class="sxs-lookup"><span data-stu-id="02c12-175">**MatchType-Exact/Partial**: Type whether the name you entered was an *exact* or *partial* match type.</span></span>
    - <span data-ttu-id="02c12-176">Correspondance exacte : vous pouvez inclure le nom exact ou l’acronyme (par exemple, *Contoso* ou *ATL*).</span><span class="sxs-lookup"><span data-stu-id="02c12-176">Exact match: You can include the exact name or acronym (for example, *Contoso* or *ATL*).</span></span>
    - <span data-ttu-id="02c12-177">Correspondance partielle : vous pouvez exclure toutes les rubriques qui ont un mot spécifique.</span><span class="sxs-lookup"><span data-stu-id="02c12-177">Partial match: You can exclude all topics that have a specific word in it.</span></span>  <span data-ttu-id="02c12-178">Par exemple, *arc exclura* toutes les rubriques avec le mot *arc* dans celui-ci, telles que le cercle *d’arc,* *l’arc de Pierre ou* *l’arc de formation*. Notez qu’il n’exclura pas les rubriques dans lesquelles le texte est inclus dans le cadre d’un mot, comme *Architecture*.</span><span class="sxs-lookup"><span data-stu-id="02c12-178">For example, *arc* will exclude all topics with the word *arc* in it, such as *Arc circle*, *Plasma arc welding*, or *Training arc*. Note that it will not exclude topics in which the text is included as part of a word, such as *Architecture*.</span></span>
- <span data-ttu-id="02c12-179">**Signifie (facultatif)**: (également appelé *expansion)* Si vous souhaitez exclure un acronyme, tapez les mots qu’il signifie.</span><span class="sxs-lookup"><span data-stu-id="02c12-179">**Stands for (optional)**: (Also known as *expansion*) If you want to exclude an acronym, type the words the acronym stands for.</span></span>

    ![Exclure des rubriques dans le modèle CSV](../media/exclude-topics-csv.png) 

<span data-ttu-id="02c12-181">Vous pouvez copier le modèle csv ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="02c12-181">You can copy the csv template below:</span></span>

``` csv
Name (required),Expansion,MatchType- Exact/Partial (required)
```

## <a name="administration"></a><span data-ttu-id="02c12-182">Administration</span><span class="sxs-lookup"><span data-stu-id="02c12-182">Administration</span></span>

<span data-ttu-id="02c12-183">Lorsque vous définissez Rubriques, dans le cadre du processus d’installation, un centre de rubriques est automatiquement créé.</span><span class="sxs-lookup"><span data-stu-id="02c12-183">When you set up Topics, as part of the setup process, a topic center is automatically created.</span></span> <span data-ttu-id="02c12-184">Réfléchissez à ce que vous souhaitez nommer le centre de rubriques et à ce que doit être l’URL.</span><span class="sxs-lookup"><span data-stu-id="02c12-184">Think about what you want to name the topic center and what you want the URL to be.</span></span> <span data-ttu-id="02c12-185">Vous pouvez définir le nom et l’URL dans le cadre du processus de configuration, et vous pouvez modifier le nom (mais pas l’URL) ultérieurement dans le Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="02c12-185">You can set both the name and URL as part of the setup process, and you can change the name (but not URL) later in the Microsoft 365 admin center.</span></span> <span data-ttu-id="02c12-186">Vous ne pouvez avoir qu’un seul centre de rubriques.</span><span class="sxs-lookup"><span data-stu-id="02c12-186">You can only have one topic center.</span></span>

## <a name="setup-checklist"></a><span data-ttu-id="02c12-187">Liste de vérification du programme d’installation</span><span class="sxs-lookup"><span data-stu-id="02c12-187">Setup checklist</span></span>

<span data-ttu-id="02c12-188">Lorsque vous configurerez des expériences de rubrique, vous aurez besoin des éléments suivants à mesure que vous passerez par l’Assistant Installation :</span><span class="sxs-lookup"><span data-stu-id="02c12-188">When you set up topic experiences, you'll need the following items as you go through the setup wizard:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="02c12-189">Liste des sites à inclure ou à exclure si tous les sites pour la découverte de rubriques ne sont pas inclus</span><span class="sxs-lookup"><span data-stu-id="02c12-189">List of sites to include or exclude if not including all sites for topic discovery</span></span>
> * <span data-ttu-id="02c12-190">Groupe de sécurité pour les visiteurs des rubriques si tous les utilisateurs ne peuvent pas afficher les rubriques</span><span class="sxs-lookup"><span data-stu-id="02c12-190">Security group for topic viewers if not allowing all users to view topics</span></span>
> * <span data-ttu-id="02c12-191">Groupe de sécurité pour les collaborateurs de rubriques si tous les utilisateurs ne peuvent pas créer et modifier des rubriques</span><span class="sxs-lookup"><span data-stu-id="02c12-191">Security group for topic contributors if not allowing all users to create and edit topics</span></span>
> * <span data-ttu-id="02c12-192">Groupe de sécurité pour les gestionnaires de connaissances des rubriques si tous les utilisateurs ne peuvent pas gérer les rubriques</span><span class="sxs-lookup"><span data-stu-id="02c12-192">Security group for topic knowledge managers if not allowing all users to manage topics</span></span>
> * <span data-ttu-id="02c12-193">Liste des rubriques sensibles à exclure de la découverte de rubriques</span><span class="sxs-lookup"><span data-stu-id="02c12-193">List of sensitive topics to exclude from topic discovery</span></span>
> * <span data-ttu-id="02c12-194">Nom de votre site centre de rubriques</span><span class="sxs-lookup"><span data-stu-id="02c12-194">A name for your topic center site</span></span>

## <a name="see-also"></a><span data-ttu-id="02c12-195">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02c12-195">See also</span></span>

[<span data-ttu-id="02c12-196">Configurer les expériences de sujets</span><span class="sxs-lookup"><span data-stu-id="02c12-196">Set up topic experiences</span></span>](set-up-topic-experiences.md)

[<span data-ttu-id="02c12-197">Gérer la découverte de rubriques dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="02c12-197">Manage topic discovery in Microsoft 365</span></span>](topic-experiences-discovery.md)

[<span data-ttu-id="02c12-198">Gérer la visibilité des rubriques dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="02c12-198">Manage topic visibility in Microsoft 365</span></span>](topic-experiences-knowledge-rules.md)

[<span data-ttu-id="02c12-199">Gérer les autorisations de rubrique dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="02c12-199">Manage topic permissions in Microsoft 365</span></span>](topic-experiences-user-permissions.md)

[<span data-ttu-id="02c12-200">Modifier le nom du centre de rubriques dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="02c12-200">Change the name of the topic center in Microsoft 365</span></span>](topic-experiences-administration.md)
