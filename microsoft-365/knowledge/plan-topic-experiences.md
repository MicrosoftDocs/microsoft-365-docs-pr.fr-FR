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
ms.openlocfilehash: 2f7b85399f0b1f49e25aae1f1d4627413594f618
ms.sourcegitcommit: e920e68c8d0eac8b152039b52cfc139d478a67b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2021
ms.locfileid: "50150477"
---
# <a name="plan-for-microsoft-viva-topics"></a><span data-ttu-id="53746-103">Planifier les rubriques microsoft</span><span class="sxs-lookup"><span data-stu-id="53746-103">Plan for Microsoft Viva Topics</span></span>

<span data-ttu-id="53746-104">Vous contrôlez la façon dont les sujets sont abordés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="53746-104">You're in control of how topics are experienced in your organization.</span></span> <span data-ttu-id="53746-105">Vos décisions de planification pour Rubriques garantissent que les rubriques de haute qualité sont présentées à vos utilisateurs et qu’ils ont les autorisations nécessaires pour consommer et contribuer aux connaissances.</span><span class="sxs-lookup"><span data-stu-id="53746-105">Your planning decisions for Topics ensures that high quality topics are shown to your users and they have the right permissions to consume and contribute knowledge.</span></span>

<span data-ttu-id="53746-106">Dans cet article, nous examinerons les décisions de planification ci-après :</span><span class="sxs-lookup"><span data-stu-id="53746-106">In this article we'll examine these planning decisions:</span></span>

- <span data-ttu-id="53746-107">Les sites SharePoint que vous souhaitez analyser pour les rubriques</span><span class="sxs-lookup"><span data-stu-id="53746-107">Which SharePoint sites you want to crawl for topics</span></span>
- <span data-ttu-id="53746-108">Les rubriques, le cas besoin, que vous souhaitez exclure des expériences de rubrique</span><span class="sxs-lookup"><span data-stu-id="53746-108">Which topics, if any, you want to exclude from topic experiences</span></span>
- <span data-ttu-id="53746-109">Utilisateurs pour lesquels vous souhaitez rendre les rubriques visibles</span><span class="sxs-lookup"><span data-stu-id="53746-109">Which users you want to make topics visible to</span></span>
- <span data-ttu-id="53746-110">Utilisateurs que vous souhaitez autoriser à gérer les rubriques dans le centre de rubriques</span><span class="sxs-lookup"><span data-stu-id="53746-110">Which users you want to give permissions to manage topics in the topic center</span></span>
- <span data-ttu-id="53746-111">Utilisateurs que vous souhaitez autoriser à créer ou modifier des rubriques dans le centre de rubriques</span><span class="sxs-lookup"><span data-stu-id="53746-111">Which users you want to give permissions to create or edit topics in the topic center</span></span>
- <span data-ttu-id="53746-112">Quel nom voulez-vous donner à votre centre de rubriques ?</span><span class="sxs-lookup"><span data-stu-id="53746-112">What name you want to give your topic center</span></span>

<span data-ttu-id="53746-113">La sécurité et la confidentialité de vos données sont respectées, et les expériences de rubrique n’octroient pas aux utilisateurs un accès supplémentaire aux fichiers dont ils n’ont pas le droit.</span><span class="sxs-lookup"><span data-stu-id="53746-113">Security and privacy of your data is respected, and topic experiences does not grant users additional access to files they don’t have rights to.</span></span> <span data-ttu-id="53746-114">Nous vous recommandons également de lire les [rubriques microsoft sur](topic-experiences-security-privacy.md) la sécurité et la confidentialité dans le cadre de votre processus de planification.</span><span class="sxs-lookup"><span data-stu-id="53746-114">We recommend you also read [Microsoft Viva Topics security and privacy](topic-experiences-security-privacy.md) as part of your planning process.</span></span>

## <a name="requirements"></a><span data-ttu-id="53746-115">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="53746-115">Requirements</span></span>

<span data-ttu-id="53746-116">Vous devez être abonné à [Rubriques Et](https://www.microsoft.com/microsoft-viva/topics) être administrateur général ou administrateur SharePoint pour accéder au Centre d’administration Microsoft 365 et configurer Rubriques.</span><span class="sxs-lookup"><span data-stu-id="53746-116">You must be [subscribed to Viva Topics](https://www.microsoft.com/microsoft-viva/topics) and be a global administrator or SharePoint administrator to access the Microsoft 365 admin center and set up Topics.</span></span>

<span data-ttu-id="53746-117">Tous les utilisateurs qui vont utiliser Les rubriques nécessitent une licence **Expériences de** rubrique.</span><span class="sxs-lookup"><span data-stu-id="53746-117">All users who are going to use Topics require a **Topic Experiences** license.</span></span> <span data-ttu-id="53746-118">L’attribution de licences est couverte [par la rubrique Configurer Microsoft Topics.](set-up-topic-experiences.md)</span><span class="sxs-lookup"><span data-stu-id="53746-118">Assigning licenses is covered in [Set up Microsoft Viva Topics](set-up-topic-experiences.md).</span></span>

## <a name="topic-discovery"></a><span data-ttu-id="53746-119">Découverte de rubrique</span><span class="sxs-lookup"><span data-stu-id="53746-119">Topic discovery</span></span>

<span data-ttu-id="53746-120">Les paramètres de découverte de rubrique spécifient les sites SharePoint qui sont utilisés comme sources pour les rubriques.</span><span class="sxs-lookup"><span data-stu-id="53746-120">The topic discovery settings specify which SharePoint sites are used as sources for topics.</span></span> <span data-ttu-id="53746-121">Vous pouvez choisir d’inclure tous les sites SharePoint, une liste spécifique de sites ou aucun site.</span><span class="sxs-lookup"><span data-stu-id="53746-121">You can choose to include all SharePoint sites, a specific list of sites, or no sites.</span></span> <span data-ttu-id="53746-122">Nous vous recommandons de choisir tous les sites afin que les expériences de rubriques puisse découvrir un grand nombre de bonnes rubriques pour vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="53746-122">We recommend that you choose all sites so that topic experiences can discover a large number of good topics for your users.</span></span>

<span data-ttu-id="53746-123">Lorsque vous définissez Rubriques, vous pouvez choisir parmi les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="53746-123">When you set up Topics, you can choose from the following options:</span></span>

- <span data-ttu-id="53746-124">**Tous les sites**: tous les sites SharePoint de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="53746-124">**All sites**: All SharePoint sites in your organization.</span></span> <span data-ttu-id="53746-125">Cela inclut les sites actuels et futurs.</span><span class="sxs-lookup"><span data-stu-id="53746-125">This includes current and future sites.</span></span>
- <span data-ttu-id="53746-126">**Tous, à l’exception des sites** sélectionnés : tous les sites à l’exception de ceux que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="53746-126">**All, except selected sites**: All sites except for the ones you specify.</span></span> <span data-ttu-id="53746-127">Les sites créés à l’avenir seront inclus en tant que sources pour la découverte de rubriques.</span><span class="sxs-lookup"><span data-stu-id="53746-127">Sites created in future will be included as sources for topic discovery.</span></span> 
- <span data-ttu-id="53746-128">**Uniquement les sites sélectionnés**: uniquement les sites que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="53746-128">**Only selected sites**: Only the sites that you specify.</span></span> <span data-ttu-id="53746-129">Les sites créés à l’avenir ne seront pas inclus en tant que sources de découverte de sujet.</span><span class="sxs-lookup"><span data-stu-id="53746-129">Sites created in the future will not be included as sources for topic discovery.</span></span>
- <span data-ttu-id="53746-130">**Aucun site**: n’incluez aucun site SharePoint.</span><span class="sxs-lookup"><span data-stu-id="53746-130">**No sites**: Do not include any SharePoint sites.</span></span>

<span data-ttu-id="53746-131">Si vous choisissez **Tous, à** l’exception des sites sélectionnés ou uniquement des **sites** sélectionnés, vous pouvez télécharger un fichier .csv avec une liste de sites.</span><span class="sxs-lookup"><span data-stu-id="53746-131">If you choose either **All, except selected sites** or **Only selected sites**, you can upload a .csv file with a list of sites.</span></span> <span data-ttu-id="53746-132">Ces options sont utiles si vous faites un projet pilote et que vous souhaitez inclure un nombre limité de sites à démarrer.</span><span class="sxs-lookup"><span data-stu-id="53746-132">These options are useful if you're doing a pilot and you want to include a limited number of sites to start.</span></span>

<span data-ttu-id="53746-133">Vous pouvez copier le modèle .csv ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="53746-133">You can copy the .csv template below:</span></span>

``` csv
Site name,URL
```

<span data-ttu-id="53746-134">Nous vous déconseillons de choisir Aucun **site,** car cela empêche la création ou la mise à jour automatique des rubriques.</span><span class="sxs-lookup"><span data-stu-id="53746-134">We don't recommend choosing **No sites** because it prevents topics from being automatically created or updated.</span></span> <span data-ttu-id="53746-135">Toutefois, vous pouvez choisir cette option si vous souhaitez configurer Rubriques, puis ajouter des sites ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="53746-135">However, you can choose this option if you want to set up Topics and then add sites later.</span></span>

<span data-ttu-id="53746-136">Nous vous recommandons de créer un processus pour que les utilisateurs ou les gestionnaires de connaissances demandent que des sites individuels soient supprimés de la découverte de rubriques si nécessaire dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="53746-136">We recommend you create a process for users or knowledge managers to request individual sites be removed from topic discovery if needed in your organization.</span></span>

## <a name="user-permissions"></a><span data-ttu-id="53746-137">Autorisations utilisateur</span><span class="sxs-lookup"><span data-stu-id="53746-137">User permissions</span></span>

<span data-ttu-id="53746-138">Les autorisations utilisateur que vous spécifiez déterminent les personnes de votre organisation qui interagissent avec les rubriques et ce qu’elles peuvent faire.</span><span class="sxs-lookup"><span data-stu-id="53746-138">The user permissions that you specify determine which people in your organization interact with topics and what they can do.</span></span>

<span data-ttu-id="53746-139">*Gérer les rubriques*</span><span class="sxs-lookup"><span data-stu-id="53746-139">*Manage topics*</span></span>

<span data-ttu-id="53746-140">Les gestionnaires de connaissances supervisent la qualité des informations, la façon dont elles sont structurées et d’autres meilleures pratiques au niveau de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="53746-140">Knowledge managers oversee the quality of information, how its structured, and other best practices in your organization.</span></span> <span data-ttu-id="53746-141">Ils peuvent confirmer et rejeter des rubriques.</span><span class="sxs-lookup"><span data-stu-id="53746-141">They can confirm and reject topics.</span></span>

<span data-ttu-id="53746-142">Bien que vous pouvez spécifier des responsables de rubriques individuels, nous vous recommandons de créer un groupe de sécurité (ou d’utiliser un groupe existant) qui contient les personnes qui vous souhaitez être des gestionnaires de connaissances.</span><span class="sxs-lookup"><span data-stu-id="53746-142">While you can specify individual topic managers, we recommend that you create a security group (or use an existing one) that contains the people who you want to be knowledge managers.</span></span> <span data-ttu-id="53746-143">Vous pouvez spécifier ce groupe de sécurité pendant le processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="53746-143">You can specify this security group during the setup process.</span></span>

<span data-ttu-id="53746-144">*Créer et modifier des rubriques*</span><span class="sxs-lookup"><span data-stu-id="53746-144">*Create and edit topics*</span></span>

<span data-ttu-id="53746-145">Les contributeurs de rubriques sont les champions et les experts techniques de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="53746-145">Topic contributors are the champions and subject matter experts in your organization.</span></span> <span data-ttu-id="53746-146">Ils peuvent créer et modifier des rubriques.</span><span class="sxs-lookup"><span data-stu-id="53746-146">They can create and edit topics.</span></span> 

<span data-ttu-id="53746-147">Nous vous recommandons d’autoriser tous les membres de votre organisation à créer et modifier des rubriques, car les expériences de rubrique fonctionnent mieux lorsque tous les utilisateurs peuvent partager des informations.</span><span class="sxs-lookup"><span data-stu-id="53746-147">We recommend that you allow everyone in your organization to create and edit topics because topic experiences work best when all users can share information.</span></span>

<span data-ttu-id="53746-148">Si vous souhaitez limiter la création et la modification de rubriques à des personnes ou des groupes spécifiques, créez un groupe de sécurité pour eux et spécifiez-le pendant le processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="53746-148">If you want to limit creating and editing topics to specific people or groups, create a security group for them and specify it during the setup process.</span></span>

<span data-ttu-id="53746-149">Vous pouvez choisir de ne permettre à personne de contribuer à des rubriques, mais cela n’est pas recommandé.</span><span class="sxs-lookup"><span data-stu-id="53746-149">You can choose to not allow anyone to contribute to topics, however this is not recommended.</span></span> <span data-ttu-id="53746-150">Les gestionnaires de connaissances pourront toujours modifier et créer des rubriques si vous choisissez cette option.</span><span class="sxs-lookup"><span data-stu-id="53746-150">Knowledge managers will still be able to edit and create topics if you choose this option.</span></span>

<span data-ttu-id="53746-151">*Visionneuses de rubriques*</span><span class="sxs-lookup"><span data-stu-id="53746-151">*Topic viewers*</span></span>

<span data-ttu-id="53746-152">Les visiteurs peuvent voir des informations sur les pages de rubriques, dans les résultats de la recherche et lorsque des rubriques sont mises en surbrillables dans le contenu tel que les pages SharePoint.</span><span class="sxs-lookup"><span data-stu-id="53746-152">Topic viewers can see information on topic pages, in search results and when topics are highlighted in the content like SharePoint pages.</span></span> <span data-ttu-id="53746-153">Les utilisateurs peuvent uniquement voir les rubriques découvertes lorsqu’ils ont accès aux fichiers et aux pages dans qui la rubrique a été découverte.</span><span class="sxs-lookup"><span data-stu-id="53746-153">Users can only see discovered topics when they have access to the files and pages the topic was discovered in.</span></span>

<span data-ttu-id="53746-154">Lors de la configuration des visionneuses de rubriques, vous pouvez choisir parmi :</span><span class="sxs-lookup"><span data-stu-id="53746-154">When setting up topic viewers, you can choose from:</span></span>

- <span data-ttu-id="53746-155">**Tous les membres de mon organisation**</span><span class="sxs-lookup"><span data-stu-id="53746-155">**Everyone in my organization**</span></span>
- <span data-ttu-id="53746-156">**Personnes ou groupes de sécurité sélectionnés uniquement**</span><span class="sxs-lookup"><span data-stu-id="53746-156">**Only selected people or security groups**</span></span>
- <span data-ttu-id="53746-157">**Personne**</span><span class="sxs-lookup"><span data-stu-id="53746-157">**No one**</span></span>

<span data-ttu-id="53746-158">Nous vous **recommandons tout le monde** dans mon organisation, mais si vous faites un projet pilote, vous pouvez choisir uniquement des personnes ou des groupes de sécurité sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="53746-158">We recommend **Everyone in my organization**, but if you're doing a pilot you may want to choose only selected people or security groups.</span></span> <span data-ttu-id="53746-159">Vous pouvez également choisir **Personne** si vous souhaitez configurer Des rubriques, mais ne pas autoriser les utilisateurs à voir les rubriques pour le moment.</span><span class="sxs-lookup"><span data-stu-id="53746-159">You can also choose **No one** if you want to set up Topics, but not allow people to see topics yet.</span></span> <span data-ttu-id="53746-160">(Les gestionnaires de connaissances auront toujours accès pour leur permettre d’afficher les rubriques et d’aider à prendre la décision de rendre les rubriques largement disponibles.)</span><span class="sxs-lookup"><span data-stu-id="53746-160">(Knowledge managers will still have access to allow them view the topics and help with the decision to make Topics broadly available.)</span></span>

## <a name="knowledge-rules"></a><span data-ttu-id="53746-161">Règles de connaissance</span><span class="sxs-lookup"><span data-stu-id="53746-161">Knowledge rules</span></span>

<span data-ttu-id="53746-162">En tant qu’administrateur, vous pouvez exclure certaines rubriques des expériences de rubrique.</span><span class="sxs-lookup"><span data-stu-id="53746-162">As an administrator, you can exclude certain topics from topic experiences.</span></span> <span data-ttu-id="53746-163">Cela est utile si vous souhaitez empêcher les données sensibles d’apparaître dans les rubriques.</span><span class="sxs-lookup"><span data-stu-id="53746-163">This is useful if you want to keep sensitive data from appearing in topics.</span></span> <span data-ttu-id="53746-164">Bien que les gestionnaires de connaissances peuvent exclure des rubriques dans le centre de rubriques, les rubriques exclues par l’administrateur ne sont même pas visibles pour les gestionnaires de connaissances.</span><span class="sxs-lookup"><span data-stu-id="53746-164">While knowledge managers can exclude topics in the topic center, topics excluded by the administrator are not even visible to knowledge managers.</span></span> <span data-ttu-id="53746-165">(Les gestionnaires de connaissances peuvent également supprimer des rubriques dans le centre de rubriques après la découverte.)</span><span class="sxs-lookup"><span data-stu-id="53746-165">(Knowledge managers can also remove topics in the topic center after discovery.)</span></span>

<span data-ttu-id="53746-166">Si vous souhaitez exclure des rubriques au niveau de l’administrateur, vous devez les ajouter à un fichier .csv et télécharger le fichier.</span><span class="sxs-lookup"><span data-stu-id="53746-166">If you want to exclude topics at the administrator level, you must add them to a .csv file and upload the file.</span></span> <span data-ttu-id="53746-167">Vous pouvez le faire lors de l’installation ou ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="53746-167">You can do this during setup or later.</span></span>

<span data-ttu-id="53746-168">Le fichier .csv doit contenir les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="53746-168">The .csv file must contain the following parameters:</span></span>

- <span data-ttu-id="53746-169">**Nom**: tapez le nom de la rubrique que vous souhaitez exclure.</span><span class="sxs-lookup"><span data-stu-id="53746-169">**Name**: Type the name of the topic you want to exclude.</span></span> <span data-ttu-id="53746-170">Vous pouvez procéder de deux manières :</span><span class="sxs-lookup"><span data-stu-id="53746-170">There are two ways to do this:</span></span>
- <span data-ttu-id="53746-171">**MatchType-Exact/Partial**: tapez si le nom que vous avez entré était un type de correspondance *exact* *ou* partiel.</span><span class="sxs-lookup"><span data-stu-id="53746-171">**MatchType-Exact/Partial**: Type whether the name you entered was an *exact* or *partial* match type.</span></span>
    - <span data-ttu-id="53746-172">Correspondance exacte : vous pouvez inclure le nom exact ou l’acronyme (par exemple, *Contoso* ou *ATL*).</span><span class="sxs-lookup"><span data-stu-id="53746-172">Exact match: You can include the exact name or acronym (for example, *Contoso* or *ATL*).</span></span>
    - <span data-ttu-id="53746-173">Correspondance partielle : vous pouvez exclure toutes les rubriques qui ont un mot spécifique.</span><span class="sxs-lookup"><span data-stu-id="53746-173">Partial match: You can exclude all topics that have a specific word in it.</span></span>  <span data-ttu-id="53746-174">Par exemple, *arc exclura* toutes les rubriques avec le mot *arc* dans celui-ci, telles que le cercle *d’arc,* *l’arc de Pierre ou* *l’arc de formation*. Notez qu’il n’exclura pas les rubriques dans lesquelles le texte est inclus dans le cadre d’un mot, comme *Architecture*.</span><span class="sxs-lookup"><span data-stu-id="53746-174">For example, *arc* will exclude all topics with the word *arc* in it, such as *Arc circle*, *Plasma arc welding*, or *Training arc*. Note that it will not exclude topics in which the text is included as part of a word, such as *Architecture*.</span></span>
- <span data-ttu-id="53746-175">**Signifie (facultatif)**: (également appelé *expansion)* Si vous souhaitez exclure un acronyme, tapez les mots qu’il signifie.</span><span class="sxs-lookup"><span data-stu-id="53746-175">**Stands for (optional)**: (Also known as *expansion*) If you want to exclude an acronym, type the words the acronym stands for.</span></span>

    ![Exclure des rubriques dans le modèle CSV](../media/exclude-topics-csv.png) 

<span data-ttu-id="53746-177">Vous pouvez copier le modèle csv ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="53746-177">You can copy the csv template below:</span></span>

``` csv
Name (required),Expansion,MatchType- Exact/Partial (required)
```

## <a name="administration"></a><span data-ttu-id="53746-178">Administration</span><span class="sxs-lookup"><span data-stu-id="53746-178">Administration</span></span>

<span data-ttu-id="53746-179">Lorsque vous définissez Rubriques, dans le cadre du processus d’installation, un centre de rubriques est automatiquement créé.</span><span class="sxs-lookup"><span data-stu-id="53746-179">When you set up Topics, as part of the setup process, a topic center is automatically created.</span></span> <span data-ttu-id="53746-180">Réfléchissez à ce que vous souhaitez nommer le centre de rubriques et à ce que doit être l’URL.</span><span class="sxs-lookup"><span data-stu-id="53746-180">Think about what you want to name the topic center and what you want the URL to be.</span></span> <span data-ttu-id="53746-181">Vous pouvez définir le nom et l’URL dans le cadre du processus de configuration, et vous pouvez modifier le nom (mais pas l’URL) ultérieurement dans le Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="53746-181">You can set both the name and URL as part of the setup process, and you can change the name (but not URL) later in the Microsoft 365 admin center.</span></span> <span data-ttu-id="53746-182">Vous ne pouvez avoir qu’un seul centre de rubriques.</span><span class="sxs-lookup"><span data-stu-id="53746-182">You can only have one topic center.</span></span>

## <a name="setup-checklist"></a><span data-ttu-id="53746-183">Liste de vérification du programme d’installation</span><span class="sxs-lookup"><span data-stu-id="53746-183">Setup checklist</span></span>

<span data-ttu-id="53746-184">Lorsque vous configurerez des expériences de rubrique, vous aurez besoin des éléments suivants à mesure que vous passerez par l’Assistant Installation :</span><span class="sxs-lookup"><span data-stu-id="53746-184">When you set up topic experiences, you'll need the following items as you go through the setup wizard:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="53746-185">Liste des sites à inclure ou à exclure si tous les sites pour la découverte de rubriques ne sont pas inclus</span><span class="sxs-lookup"><span data-stu-id="53746-185">List of sites to include or exclude if not including all sites for topic discovery</span></span>
> * <span data-ttu-id="53746-186">Groupe de sécurité pour les visiteurs des rubriques si tous les utilisateurs ne peuvent pas afficher les rubriques</span><span class="sxs-lookup"><span data-stu-id="53746-186">Security group for topic viewers if not allowing all users to view topics</span></span>
> * <span data-ttu-id="53746-187">Groupe de sécurité pour les collaborateurs de rubriques si tous les utilisateurs ne peuvent pas créer et modifier des rubriques</span><span class="sxs-lookup"><span data-stu-id="53746-187">Security group for topic contributors if not allowing all users to create and edit topics</span></span>
> * <span data-ttu-id="53746-188">Groupe de sécurité pour les gestionnaires de connaissances des rubriques si tous les utilisateurs ne peuvent pas gérer les rubriques</span><span class="sxs-lookup"><span data-stu-id="53746-188">Security group for topic knowledge managers if not allowing all users to manage topics</span></span>
> * <span data-ttu-id="53746-189">Liste des rubriques sensibles à exclure de la découverte de rubriques</span><span class="sxs-lookup"><span data-stu-id="53746-189">List of sensitive topics to exclude from topic discovery</span></span>
> * <span data-ttu-id="53746-190">Nom de votre site centre de rubriques</span><span class="sxs-lookup"><span data-stu-id="53746-190">A name for your topic center site</span></span>

## <a name="see-also"></a><span data-ttu-id="53746-191">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53746-191">See also</span></span>

[<span data-ttu-id="53746-192">Configurer les expériences de sujets</span><span class="sxs-lookup"><span data-stu-id="53746-192">Set up topic experiences</span></span>](set-up-topic-experiences.md)

[<span data-ttu-id="53746-193">Gérer la découverte de rubriques dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="53746-193">Manage topic discovery in Microsoft 365</span></span>](topic-experiences-discovery.md)

[<span data-ttu-id="53746-194">Gérer la visibilité des rubriques dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="53746-194">Manage topic visibility in Microsoft 365</span></span>](topic-experiences-knowledge-rules.md)

[<span data-ttu-id="53746-195">Gérer les autorisations de rubrique dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="53746-195">Manage topic permissions in Microsoft 365</span></span>](topic-experiences-user-permissions.md)

[<span data-ttu-id="53746-196">Modifier le nom du centre de rubriques dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="53746-196">Change the name of the topic center in Microsoft 365</span></span>](topic-experiences-administration.md)
