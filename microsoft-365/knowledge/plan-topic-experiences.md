---
title: Planification des expériences de rubrique dans Microsoft 365
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
description: Découvrez comment planifier des expériences de rubrique dans Microsoft 365
ms.openlocfilehash: 153937cf6bc4a12f0a27866204b2286c343ddf55
ms.sourcegitcommit: 1a9f0f878c045e1ddd59088ca2a94397605a242a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "49668155"
---
# <a name="plan-topic-experiences-in-microsoft-365"></a><span data-ttu-id="42d0a-103">Planification des expériences de rubrique dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="42d0a-103">Plan topic experiences in Microsoft 365</span></span>

<span data-ttu-id="42d0a-104">Vous contrôlez le mode d’expérience des rubriques dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="42d0a-104">You're in control of how topics are experienced in your organization.</span></span> <span data-ttu-id="42d0a-105">Vos décisions de planification pour les expériences de rubrique permettent de s’assurer que des rubriques de qualité supérieure sont affichées pour vos utilisateurs et qu’ils disposent des autorisations appropriées pour utiliser et contribuer aux connaissances.</span><span class="sxs-lookup"><span data-stu-id="42d0a-105">Your planning decisions for topic experiences ensures that high quality topics are shown to your users and they have the right permissions to consume and contribute knowledge.</span></span>

<span data-ttu-id="42d0a-106">Dans cet article, nous allons examiner les décisions de planification suivantes :</span><span class="sxs-lookup"><span data-stu-id="42d0a-106">In this article we'll examine these planning decisions:</span></span>

- <span data-ttu-id="42d0a-107">Les sites SharePoint que vous souhaitez analyser.</span><span class="sxs-lookup"><span data-stu-id="42d0a-107">Which SharePoint sites you want to crawl for topics.</span></span>
- <span data-ttu-id="42d0a-108">Les rubriques, le cas échéant, que vous souhaitez exclure des expériences de rubrique</span><span class="sxs-lookup"><span data-stu-id="42d0a-108">Which topics, if any, you want to exclude from topic experiences</span></span>
- <span data-ttu-id="42d0a-109">Les utilisateurs auxquels vous souhaitez faire apparaître les rubriques.</span><span class="sxs-lookup"><span data-stu-id="42d0a-109">Which users you want to make topics visible to.</span></span>
- <span data-ttu-id="42d0a-110">Les utilisateurs auxquels vous souhaitez accorder des autorisations pour gérer les rubriques dans le Centre des rubriques.</span><span class="sxs-lookup"><span data-stu-id="42d0a-110">Which users you want to give permissions to manage topics in the topic center.</span></span>
- <span data-ttu-id="42d0a-111">Les utilisateurs auxquels vous souhaitez accorder des autorisations pour créer ou modifier des rubriques dans le Centre des rubriques.</span><span class="sxs-lookup"><span data-stu-id="42d0a-111">Which users you want to give permissions to create or edit topics in the topic center.</span></span>
- <span data-ttu-id="42d0a-112">Le nom que vous souhaitez donner à votre centre de sujets.</span><span class="sxs-lookup"><span data-stu-id="42d0a-112">What name you want to give your topic center.</span></span>

<span data-ttu-id="42d0a-113">La sécurité et la confidentialité de vos données sont respectées, et les expériences de rubrique n’accordent pas aux utilisateurs un accès supplémentaire aux fichiers auxquels ils ne disposent pas de droits.</span><span class="sxs-lookup"><span data-stu-id="42d0a-113">Security and privacy of your data is respected, and topic experiences does not grant users additional access to files they don’t have rights to.</span></span> <span data-ttu-id="42d0a-114">Nous vous recommandons également de lire la [rubrique relative à la sécurité et](topic-experiences-security-privacy.md) à la confidentialité dans le cadre de votre processus de planification.</span><span class="sxs-lookup"><span data-stu-id="42d0a-114">We recommend you also read [Topic experiences security and privacy](topic-experiences-security-privacy.md) as part of your planning process.</span></span>

## <a name="requirements"></a><span data-ttu-id="42d0a-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42d0a-115">Requirements</span></span>

<span data-ttu-id="42d0a-116">Vous devez être un administrateur général ou un administrateur SharePoint pour accéder au centre d’administration Microsoft 365 et configurer des expériences de rubrique.</span><span class="sxs-lookup"><span data-stu-id="42d0a-116">You must be a global administrator or SharePoint administrator to access the Microsoft 365 admin center and set up topic experiences.</span></span>

<span data-ttu-id="42d0a-117">Tous les utilisateurs qui vont utiliser des expériences de rubrique requièrent une **rubrique relative** aux licences.</span><span class="sxs-lookup"><span data-stu-id="42d0a-117">All users who are going to use topic experiences require a **Topic Experiences** license.</span></span> <span data-ttu-id="42d0a-118">Pour affecter des licences, reportez-vous à la [rubrique relative à la configuration des expériences](set-up-topic-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="42d0a-118">Assigning licenses is covered in [Set up topic experiences](set-up-topic-experiences.md).</span></span>

## <a name="topic-discovery"></a><span data-ttu-id="42d0a-119">Découverte de rubrique</span><span class="sxs-lookup"><span data-stu-id="42d0a-119">Topic discovery</span></span>

<span data-ttu-id="42d0a-120">Les paramètres de découverte de rubrique spécifient les sites SharePoint qui sont utilisés comme sources pour les rubriques.</span><span class="sxs-lookup"><span data-stu-id="42d0a-120">The topic discovery settings specify which SharePoint sites are used as sources for topics.</span></span> <span data-ttu-id="42d0a-121">Vous pouvez choisir d’inclure tous les sites SharePoint, une liste spécifique de sites ou aucun site.</span><span class="sxs-lookup"><span data-stu-id="42d0a-121">You can choose to include all SharePoint sites, a specific list of sites, or no sites.</span></span> <span data-ttu-id="42d0a-122">Nous vous recommandons de choisir tous les sites de sorte que les expériences de rubrique puissent découvrir un grand nombre de rubriques intéressantes pour vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="42d0a-122">We recommend that you choose all sites so that topic experiences can discover a large number of good topics for your users.</span></span>

<span data-ttu-id="42d0a-123">Lorsque vous configurez des expériences de rubrique, vous pouvez choisir l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="42d0a-123">When you set up topic experiences, you can choose from the following options:</span></span>

- <span data-ttu-id="42d0a-124">**Tous les sites**: tous les sites SharePoint de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="42d0a-124">**All sites**: All SharePoint sites in your organization.</span></span> <span data-ttu-id="42d0a-125">Cela inclut les sites actuels et futurs.</span><span class="sxs-lookup"><span data-stu-id="42d0a-125">This includes current and future sites.</span></span>
- <span data-ttu-id="42d0a-126">**Tout, à l’exception des sites sélectionnés**: tous les sites à l’exception de ceux que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="42d0a-126">**All, except selected sites**: All sites except for the ones you specify.</span></span> <span data-ttu-id="42d0a-127">Les sites créés à l’avenir seront inclus en tant que sources pour la découverte des rubriques.</span><span class="sxs-lookup"><span data-stu-id="42d0a-127">Sites created in future will be included as sources for topic discovery.</span></span> 
- <span data-ttu-id="42d0a-128">**Sites sélectionnés uniquement**: uniquement les sites que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="42d0a-128">**Only selected sites**: Only the sites that you specify.</span></span> <span data-ttu-id="42d0a-129">Les sites créés à l’avenir ne seront pas inclus en tant que sources pour la découverte des rubriques.</span><span class="sxs-lookup"><span data-stu-id="42d0a-129">Sites created in the future will not be included as sources for topic discovery.</span></span>
- <span data-ttu-id="42d0a-130">**Aucun site**: n’inclut aucun site SharePoint.</span><span class="sxs-lookup"><span data-stu-id="42d0a-130">**No sites**: Do not include any SharePoint sites.</span></span>

<span data-ttu-id="42d0a-131">Si vous choisissez **tous, à l’exception des sites sélectionnés** ou des **sites sélectionnés uniquement**, vous pouvez télécharger un fichier. csv avec une liste de sites.</span><span class="sxs-lookup"><span data-stu-id="42d0a-131">If you choose either **All, except selected sites** or **Only selected sites**, you can upload a .csv file with a list of sites.</span></span> <span data-ttu-id="42d0a-132">Ces options sont utiles si vous effectuez un projet pilote et si vous souhaitez inclure un nombre limité de sites à démarrer.</span><span class="sxs-lookup"><span data-stu-id="42d0a-132">These options are useful if you're doing a pilot and you want to include a limited number of sites to start.</span></span>

<span data-ttu-id="42d0a-133">Vous pouvez copier le modèle. csv ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="42d0a-133">You can copy the .csv template below:</span></span>

``` csv
Site name,URL
```

<span data-ttu-id="42d0a-134">Nous vous déconseillons de ne pas choisir de **sites** , car cela empêche la création ou la mise à jour automatique des rubriques.</span><span class="sxs-lookup"><span data-stu-id="42d0a-134">We don't recommend choosing **No sites** because it prevents topics from being automatically created or updated.</span></span> <span data-ttu-id="42d0a-135">Toutefois, vous pouvez choisir cette option si vous souhaitez configurer des expériences de rubrique, puis ajouter des sites ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="42d0a-135">However, you can choose this option if you want to set up topic experiences and then add sites later.</span></span>

<span data-ttu-id="42d0a-136">Nous vous recommandons de créer un processus pour les utilisateurs ou les responsables de la connaissance afin de demander la suppression des sites individuels de la découverte de rubrique, si nécessaire dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="42d0a-136">We recommend you create a process for users or knowledge managers to request individual sites be removed from topic discovery if needed in your organization.</span></span>

## <a name="user-permissions"></a><span data-ttu-id="42d0a-137">Autorisations utilisateur</span><span class="sxs-lookup"><span data-stu-id="42d0a-137">User permissions</span></span>

<span data-ttu-id="42d0a-138">Les autorisations utilisateur que vous spécifiez déterminent les personnes de votre organisation qui interagissent avec des rubriques et ce qu’elles peuvent faire.</span><span class="sxs-lookup"><span data-stu-id="42d0a-138">The user permissions that you specify determine which people in your organization interact with topics and what they can do.</span></span>

<span data-ttu-id="42d0a-139">*Gérer les rubriques*</span><span class="sxs-lookup"><span data-stu-id="42d0a-139">*Manage topics*</span></span>

<span data-ttu-id="42d0a-140">Les responsables des connaissances supervisent la qualité des informations, la façon dont ils sont structurés et d’autres meilleures pratiques au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="42d0a-140">Knowledge managers oversee the quality of information, how its structured, and other best practices in your organization.</span></span> <span data-ttu-id="42d0a-141">Ils peuvent confirmer et rejeter des rubriques.</span><span class="sxs-lookup"><span data-stu-id="42d0a-141">They can confirm and reject topics.</span></span>

<span data-ttu-id="42d0a-142">Bien que vous puissiez spécifier des gestionnaires de rubriques spécifiques, nous vous recommandons de créer un groupe de sécurité (ou d’utiliser un groupe existant) qui contient les personnes que vous voulez désigner comme responsables du savoir.</span><span class="sxs-lookup"><span data-stu-id="42d0a-142">While you can specify individual topic managers, we recommend that you create a security group (or use an existing one) that contains the people who you want to be knowledge managers.</span></span> <span data-ttu-id="42d0a-143">Vous pouvez spécifier ce groupe de sécurité pendant le processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="42d0a-143">You can specify this security group during the setup process.</span></span>

<span data-ttu-id="42d0a-144">*Créer et modifier des rubriques*</span><span class="sxs-lookup"><span data-stu-id="42d0a-144">*Create and edit topics*</span></span>

<span data-ttu-id="42d0a-145">Les contributeurs de rubrique sont les champions et les experts techniques de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="42d0a-145">Topic contributors are the champions and subject matter experts in your organization.</span></span> <span data-ttu-id="42d0a-146">Ils peuvent créer et modifier des rubriques.</span><span class="sxs-lookup"><span data-stu-id="42d0a-146">They can create and edit topics.</span></span> 

<span data-ttu-id="42d0a-147">Nous vous recommandons de permettre à tous les membres de votre organisation de créer et de modifier des rubriques, car les expériences de rubrique sont meilleures lorsque tous les utilisateurs peuvent partager des informations.</span><span class="sxs-lookup"><span data-stu-id="42d0a-147">We recommend that you allow everyone in your organization to create and edit topics because topic experiences work best when all users can share information.</span></span>

<span data-ttu-id="42d0a-148">Si vous souhaitez limiter la création et la modification des rubriques à des personnes ou des groupes spécifiques, créez un groupe de sécurité pour ceux-ci et spécifiez-le pendant le processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="42d0a-148">If you want to limit creating and editing topics to specific people or groups, create a security group for them and specify it during the setup process.</span></span>

<span data-ttu-id="42d0a-149">Vous pouvez choisir de ne pas autoriser quiconque à contribuer aux rubriques, mais cela n’est pas recommandé.</span><span class="sxs-lookup"><span data-stu-id="42d0a-149">You can choose to not allow anyone to contribute to topics, however this is not recommended.</span></span> <span data-ttu-id="42d0a-150">Les responsables de la connaissance seront toujours en mesure de modifier et de créer des rubriques.</span><span class="sxs-lookup"><span data-stu-id="42d0a-150">Knowledge managers will still be able to edit and create topics.</span></span>

<span data-ttu-id="42d0a-151">*Visionneuses de rubrique*</span><span class="sxs-lookup"><span data-stu-id="42d0a-151">*Topic viewers*</span></span>

<span data-ttu-id="42d0a-152">Les visionneuses de rubrique peuvent afficher des informations sur les pages de rubrique, dans les résultats de recherche et lorsque des rubriques sont mises en surbrillance dans le contenu comme les pages SharePoint.</span><span class="sxs-lookup"><span data-stu-id="42d0a-152">Topic viewers can see information on topic pages, in search results and when topics are highlighted in the content like SharePoint pages.</span></span> <span data-ttu-id="42d0a-153">Les utilisateurs peuvent uniquement voir les rubriques découvertes lorsqu’ils ont accès aux fichiers et aux pages sur lesquels la rubrique a été découverte.</span><span class="sxs-lookup"><span data-stu-id="42d0a-153">Users can only see discovered topics when they have access to the files and pages the topic was discovered in.</span></span>

<span data-ttu-id="42d0a-154">Lorsque vous configurez des visionneuses de rubrique, vous pouvez choisir parmi les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="42d0a-154">When setting up topic viewers, you can choose from:</span></span>

- <span data-ttu-id="42d0a-155">**Tous les membres de mon organisation**</span><span class="sxs-lookup"><span data-stu-id="42d0a-155">**Everyone in my organization**</span></span>
- <span data-ttu-id="42d0a-156">**Uniquement les personnes ou les groupes de sécurité sélectionnés**</span><span class="sxs-lookup"><span data-stu-id="42d0a-156">**Only selected people or security groups**</span></span>
- <span data-ttu-id="42d0a-157">**Personne**</span><span class="sxs-lookup"><span data-stu-id="42d0a-157">**No one**</span></span>

<span data-ttu-id="42d0a-158">Nous recommandons **tout le monde au sein de mon organisation**, mais si vous effectuez un test pilote, vous pouvez choisir uniquement des personnes ou des groupes de sécurité sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="42d0a-158">We recommend **Everyone in my organization**, but if you're doing a pilot you may want to choose only selected people or security groups.</span></span> <span data-ttu-id="42d0a-159">Vous pouvez également choisir **personne** si vous souhaitez configurer des expériences de rubrique, mais ne pas autoriser les utilisateurs à voir les rubriques.</span><span class="sxs-lookup"><span data-stu-id="42d0a-159">You can also choose **No one** if you want to set up topic experiences, but not allow people to see topics yet.</span></span> <span data-ttu-id="42d0a-160">(Les gestionnaires de connaissances auront toujours accès pour leur permettre d’afficher les rubriques et d’aider à la décision de rendre les expériences de rubrique largement disponibles.)</span><span class="sxs-lookup"><span data-stu-id="42d0a-160">(Knowledge managers will still have access to allow them view the topics and help with the decision to make topic experiences broadly available.)</span></span>

## <a name="knowledge-rules"></a><span data-ttu-id="42d0a-161">Règles de connaissances</span><span class="sxs-lookup"><span data-stu-id="42d0a-161">Knowledge rules</span></span>

<span data-ttu-id="42d0a-162">En tant qu’administrateur, vous pouvez exclure certaines rubriques de la rubrique expériences.</span><span class="sxs-lookup"><span data-stu-id="42d0a-162">As an administrator, you can exclude certain topics from topic experiences.</span></span> <span data-ttu-id="42d0a-163">Cela est utile si vous souhaitez que les données sensibles ne s’affichent pas dans les rubriques.</span><span class="sxs-lookup"><span data-stu-id="42d0a-163">This is useful if you want to keep sensitive data from appearing in topics.</span></span> <span data-ttu-id="42d0a-164">Alors que les gestionnaires de connaissances peuvent exclure des rubriques dans le Centre des rubriques, les rubriques exclues par l’administrateur ne sont même pas visibles par les gestionnaires de connaissances.</span><span class="sxs-lookup"><span data-stu-id="42d0a-164">While knowledge managers can exclude topics in the topic center, topics excluded by the administrator are not even visible to knowledge managers.</span></span> <span data-ttu-id="42d0a-165">(Les gestionnaires de connaissances peuvent également supprimer des rubriques dans le Centre des rubriques après la découverte.)</span><span class="sxs-lookup"><span data-stu-id="42d0a-165">(Knowledge managers can also remove topics in the topic center after discovery.)</span></span>

<span data-ttu-id="42d0a-166">Si vous souhaitez exclure des rubriques au niveau de l’administrateur, vous devez les ajouter à un fichier. csv et charger le fichier.</span><span class="sxs-lookup"><span data-stu-id="42d0a-166">If you want to exclude topics at the administrator level, you must add them to a .csv file and upload the file.</span></span> <span data-ttu-id="42d0a-167">Vous pouvez effectuer cette opération pendant l’installation ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="42d0a-167">You can do this during setup or later.</span></span>

<span data-ttu-id="42d0a-168">Le fichier. csv doit contenir les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="42d0a-168">The .csv file must contain the following parameters:</span></span>

- <span data-ttu-id="42d0a-169">**Nom**: tapez le nom de la rubrique à exclure.</span><span class="sxs-lookup"><span data-stu-id="42d0a-169">**Name**: Type the name of the topic you want to exclude.</span></span> <span data-ttu-id="42d0a-170">Vous pouvez procéder de deux manières :</span><span class="sxs-lookup"><span data-stu-id="42d0a-170">There are two ways to do this:</span></span>
- <span data-ttu-id="42d0a-171">**MatchType-exacte/partielle**: spécifiez si le nom que vous avez entré est un type de correspondance *exacte* ou *partielle* .</span><span class="sxs-lookup"><span data-stu-id="42d0a-171">**MatchType-Exact/Partial**: Type whether the name you entered was an *exact* or *partial* match type.</span></span>
    - <span data-ttu-id="42d0a-172">Correspondance exacte : vous pouvez inclure le nom exact ou un acronyme (par exemple, *contoso* ou *ATL*).</span><span class="sxs-lookup"><span data-stu-id="42d0a-172">Exact match: You can include the exact name or acronym (for example, *Contoso* or *ATL*).</span></span>
    - <span data-ttu-id="42d0a-173">Correspondance partielle : vous pouvez exclure toutes les rubriques qui contiennent un mot spécifique.</span><span class="sxs-lookup"><span data-stu-id="42d0a-173">Partial match: You can exclude all topics that have a specific word in it.</span></span>  <span data-ttu-id="42d0a-174">Par exemple, *arc* exclut toutes les rubriques contenant le mot *arc* , comme un *cercle arc*, un *soudage* à l’arc de plasma ou un *arc de formation*. Notez qu’il n’exclura pas les rubriques dans lesquelles le texte est inclus dans un mot, tel que *architecture*.</span><span class="sxs-lookup"><span data-stu-id="42d0a-174">For example, *arc* will exclude all topics with the word *arc* in it, such as *Arc circle*, *Plasma arc welding*, or *Training arc*. Note that it will not exclude topics in which the text is included as part of a word, such as *Architecture*.</span></span>
- <span data-ttu-id="42d0a-175">**Abréviation de (facultatif)**: (également appelée *expansion*) si vous souhaitez exclure un acronyme, tapez les mots que l’acronyme signifie.</span><span class="sxs-lookup"><span data-stu-id="42d0a-175">**Stands for (optional)**: (Also known as *expansion*) If you want to exclude an acronym, type the words the acronym stands for.</span></span>

    ![Exclure les rubriques du modèle CSV](../media/exclude-topics-csv.png) 

<span data-ttu-id="42d0a-177">Vous pouvez copier le modèle CSV ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="42d0a-177">You can copy the csv template below:</span></span>

``` csv
Name (required),Expansion,MatchType- Exact/Partial (required)
```

## <a name="administration"></a><span data-ttu-id="42d0a-178">Administration</span><span class="sxs-lookup"><span data-stu-id="42d0a-178">Administration</span></span>

<span data-ttu-id="42d0a-179">Lorsque vous configurez des expériences de rubrique, dans le cadre du processus de configuration, un centre de rubriques est créé automatiquement.</span><span class="sxs-lookup"><span data-stu-id="42d0a-179">When you set up topic experiences, as part of the setup process, a topic center is automatically created.</span></span> <span data-ttu-id="42d0a-180">Réfléchissez à ce que vous souhaitez nommer le centre de la rubrique et ce que vous voulez faire de l’URL.</span><span class="sxs-lookup"><span data-stu-id="42d0a-180">Think about what you want to name the topic center and what you want the URL to be.</span></span> <span data-ttu-id="42d0a-181">Vous pouvez définir le nom et l’URL dans le processus de configuration, et vous pouvez modifier le nom (mais pas l’URL) plus loin dans le centre d’administration 365 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="42d0a-181">You can set both the name and URL as part of the setup process, and you can change the name (but not URL) later in the Microsoft 365 admin center.</span></span> <span data-ttu-id="42d0a-182">Vous ne pouvez avoir qu’un seul centre de rubriques.</span><span class="sxs-lookup"><span data-stu-id="42d0a-182">You can only have one topic center.</span></span>

## <a name="setup-checklist"></a><span data-ttu-id="42d0a-183">Liste de vérification de configuration</span><span class="sxs-lookup"><span data-stu-id="42d0a-183">Setup checklist</span></span>

<span data-ttu-id="42d0a-184">Lorsque vous configurez des expériences de rubrique, vous aurez besoin des éléments suivants lors de l’installation de l’Assistant de configuration :</span><span class="sxs-lookup"><span data-stu-id="42d0a-184">When you set up topic experiences, you'll need the following items as you go through the setup wizard:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="42d0a-185">Liste des sites à inclure ou à exclure si tous les sites ne sont pas inclus pour la découverte de rubrique</span><span class="sxs-lookup"><span data-stu-id="42d0a-185">List of sites to include or exclude if not including all sites for topic discovery</span></span>
> * <span data-ttu-id="42d0a-186">Groupe de sécurité pour les visionneuses de rubrique si vous n’autorisez pas tous les utilisateurs à consulter les rubriques</span><span class="sxs-lookup"><span data-stu-id="42d0a-186">Security group for topic viewers if not allowing all users to view topics</span></span>
> * <span data-ttu-id="42d0a-187">Groupe de sécurité pour les contributeurs de rubrique si vous n’autorisez pas tous les utilisateurs à créer et modifier des rubriques</span><span class="sxs-lookup"><span data-stu-id="42d0a-187">Security group for topic contributors if not allowing all users to create and edit topics</span></span>
> * <span data-ttu-id="42d0a-188">Groupe de sécurité pour les gestionnaires de connaissances si vous n’autorisez pas tous les utilisateurs à gérer les rubriques</span><span class="sxs-lookup"><span data-stu-id="42d0a-188">Security group for topic knowledge managers if not allowing all users to manage topics</span></span>
> * <span data-ttu-id="42d0a-189">Liste des rubriques sensibles à exclure de la découverte de rubriques</span><span class="sxs-lookup"><span data-stu-id="42d0a-189">List of sensitive topics to exclude from topic discovery</span></span>
> * <span data-ttu-id="42d0a-190">Un nom pour votre site Centre de rubriques</span><span class="sxs-lookup"><span data-stu-id="42d0a-190">A name for your topic center site</span></span>

## <a name="see-also"></a><span data-ttu-id="42d0a-191">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42d0a-191">See also</span></span>

[<span data-ttu-id="42d0a-192">Configurer des expériences de rubrique</span><span class="sxs-lookup"><span data-stu-id="42d0a-192">Set up topic experiences</span></span>](set-up-topic-experiences.md)

[<span data-ttu-id="42d0a-193">Gestion de la découverte de rubrique dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="42d0a-193">Manage topic discovery in Microsoft 365</span></span>](topic-experiences-discovery.md)

[<span data-ttu-id="42d0a-194">Gestion de la visibilité des rubriques dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="42d0a-194">Manage topic visibility in Microsoft 365</span></span>](topic-experiences-knowledge-rules.md)

[<span data-ttu-id="42d0a-195">Gérer les autorisations de rubrique dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="42d0a-195">Manage topic permissions in Microsoft 365</span></span>](topic-experiences-user-permissions.md)

[<span data-ttu-id="42d0a-196">Modifier le nom du centre de rubrique dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="42d0a-196">Change the name of the topic center in Microsoft 365</span></span>](topic-experiences-administration.md)
