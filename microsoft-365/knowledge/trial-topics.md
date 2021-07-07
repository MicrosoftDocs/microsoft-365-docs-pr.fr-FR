---
title: Exécuter une version d’essai des rubriques microsoft
ms.author: chucked
author: chuckedmonson
manager: pamgreen
ms.reviewer: lauris; jaeccles
ms.date: ''
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
ms.custom: ''
search.appverid: ''
localization_priority: Normal
description: Découvrez comment planifier et exécuter un programme pilote d’essai pour Microsoft Topics dans votre organisation.
ms.openlocfilehash: 128e82e7664a76baa55d37e983319c9f344624fd
ms.sourcegitcommit: 53aebd492a4b998805c70c8e06a2cfa5d453905c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2021
ms.locfileid: "53327112"
---
# <a name="run-a-trial-of-microsoft-viva-topics"></a><span data-ttu-id="b89ef-103">Exécuter une version d’essai des rubriques microsoft</span><span class="sxs-lookup"><span data-stu-id="b89ef-103">Run a trial of Microsoft Viva Topics</span></span>

<span data-ttu-id="b89ef-104">Cet article explique comment configurer et exécuter un programme pilote d’essai pour déployer Topics dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b89ef-104">This article describes how to set up and run a trial pilot program to deploy Viva Topics to your organization.</span></span> <span data-ttu-id="b89ef-105">Cet article recommande également les meilleures pratiques pour la version d’essai.</span><span class="sxs-lookup"><span data-stu-id="b89ef-105">This article also recommends best practices for the trial.</span></span>

## <a name="sign-up-for-a-trial"></a><span data-ttu-id="b89ef-106">S’inscrire à une version d’essai</span><span class="sxs-lookup"><span data-stu-id="b89ef-106">Sign up for a trial</span></span>

<span data-ttu-id="b89ef-107">Les essais sont disponibles publiquement à partir de l’une des sources suivantes.</span><span class="sxs-lookup"><span data-stu-id="b89ef-107">Trials are publicly available from one of the following sources.</span></span> <span data-ttu-id="b89ef-108">Ces essais d’essai offrent à 25 utilisateurs l’accès aux rubriques Topics pendant 30 jours.</span><span class="sxs-lookup"><span data-stu-id="b89ef-108">These trials offer 25 users access to Viva Topics for 30 days.</span></span>

- <span data-ttu-id="b89ef-109">Page [Du produit Rubriques](https://www.microsoft.com/microsoft-viva/topics?activetab=pivot:overviewtab)</span><span class="sxs-lookup"><span data-stu-id="b89ef-109">The [Viva Topics product page](https://www.microsoft.com/microsoft-viva/topics?activetab=pivot:overviewtab)</span></span>

- <span data-ttu-id="b89ef-110">Le [Centre d’administration Microsoft 365](https://admin.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="b89ef-110">The [Microsoft 365 admin center](https://admin.microsoft.com)</span></span>
    1.  <span data-ttu-id="b89ef-111">Connectez-vous au [Centre d’administration Microsoft 365](https://admin.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="b89ef-111">Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com).</span></span>
    2.  <span data-ttu-id="b89ef-112">Go to **Billing**  >  **Purchase Services**.</span><span class="sxs-lookup"><span data-stu-id="b89ef-112">Go to **Billing** > **Purchase Services**.</span></span>
    3.  <span data-ttu-id="b89ef-113">Faites défiler la page vers le bas jusqu’à la section **Modules complémentaires**.</span><span class="sxs-lookup"><span data-stu-id="b89ef-113">Scroll down to the **Add-Ons** section.</span></span>
    4.  <span data-ttu-id="b89ef-114">Dans la vignette **Expériences des** **rubriques, sélectionnez Détails.**</span><span class="sxs-lookup"><span data-stu-id="b89ef-114">On the **Topic Experiences** tile, select **Details**.</span></span>
    5.  <span data-ttu-id="b89ef-115">Sélectionnez **Obtenir un essai gratuit**.</span><span class="sxs-lookup"><span data-stu-id="b89ef-115">Select **Get free trial**.</span></span>
    6.  <span data-ttu-id="b89ef-116">Suivez les étapes restantes de l’Assistant pour confirmer la version d’essai.</span><span class="sxs-lookup"><span data-stu-id="b89ef-116">Follow the remaining wizard steps to confirm the trial.</span></span>

<span data-ttu-id="b89ef-117">Vous devez être un administrateur Microsoft 365 général ou un administrateur de facturation pour activer une version d’essai.</span><span class="sxs-lookup"><span data-stu-id="b89ef-117">You must be a Microsoft 365 global administrator or billing administrator to activate a trial.</span></span>

> [!NOTE]
> <span data-ttu-id="b89ef-118">Les essais publics ne peuvent être ajoutés qu’une seule fois pour Microsoft 365 client.</span><span class="sxs-lookup"><span data-stu-id="b89ef-118">Public trials can only be added once for each Microsoft 365 tenant.</span></span>

### <a name="who-should-be-involved-in-a-trial"></a><span data-ttu-id="b89ef-119">Qui doivent être impliquées dans une version d’essai</span><span class="sxs-lookup"><span data-stu-id="b89ef-119">Who should be involved in a trial</span></span>

|<span data-ttu-id="b89ef-120">Rôle</span><span class="sxs-lookup"><span data-stu-id="b89ef-120">Role</span></span>  |<span data-ttu-id="b89ef-121">Activité</span><span class="sxs-lookup"><span data-stu-id="b89ef-121">Activity</span></span>  |
|---------|---------|
|<span data-ttu-id="b89ef-122">Microsoft 365 administrateur global ou administrateur de facturation</span><span class="sxs-lookup"><span data-stu-id="b89ef-122">Microsoft 365 global admin or billing admin</span></span>  |   <span data-ttu-id="b89ef-123">Activer la version d’essai et attribuer des licences</span><span class="sxs-lookup"><span data-stu-id="b89ef-123">Activate the trial and assign licenses</span></span>      |
|<span data-ttu-id="b89ef-124">Microsoft 365 administrateur global ou administrateur SharePoint administrateur</span><span class="sxs-lookup"><span data-stu-id="b89ef-124">Microsoft 365 global admin or SharePoint admin</span></span>    |       <span data-ttu-id="b89ef-125">Configurer des rubriques Et créer des centres de rubriques</span><span class="sxs-lookup"><span data-stu-id="b89ef-125">Configure  Viva Topics and create topic centers</span></span>  |
|<span data-ttu-id="b89ef-126">Utilisateur commercial</span><span class="sxs-lookup"><span data-stu-id="b89ef-126">Business user</span></span>     |   <span data-ttu-id="b89ef-127">Effectuer des rôles de gestionnaire de connaissances, de collaborateur de rubriques et de consommateur de rubriques</span><span class="sxs-lookup"><span data-stu-id="b89ef-127">Perform knowledge manager, topic contributor, and topic consumer roles</span></span>      |

### <a name="before-you-activate-a-trial"></a><span data-ttu-id="b89ef-128">Avant d’activer une version d’essai</span><span class="sxs-lookup"><span data-stu-id="b89ef-128">Before you activate a trial</span></span>

<span data-ttu-id="b89ef-129">La planification est essentielle pour une version d’essai efficace de Topics.</span><span class="sxs-lookup"><span data-stu-id="b89ef-129">Planning is essential for an effective trial of Viva Topics.</span></span> <span data-ttu-id="b89ef-130">La période d’essai est limitée et doit inclure la découverte et l’exploration de la qualité, de la gestion et des expériences des utilisateurs finux.</span><span class="sxs-lookup"><span data-stu-id="b89ef-130">The trial period is limited and must include topic discovery and exploring topic quality, management, and end-user experiences.</span></span>

#### <a name="discovery"></a><span data-ttu-id="b89ef-131">Discovery</span><span class="sxs-lookup"><span data-stu-id="b89ef-131">Discovery</span></span>

<span data-ttu-id="b89ef-132">Il existe deux options de stratégie de haut niveau pour la configuration de la découverte de sujets au cours d’une version d’essai :</span><span class="sxs-lookup"><span data-stu-id="b89ef-132">There are two high-level strategy options for configuration of topic discovery during a trial:</span></span>

- <span data-ttu-id="b89ef-133">Indexez l’ensemble ou la majeure partie SharePoint contenu en ligne.</span><span class="sxs-lookup"><span data-stu-id="b89ef-133">Index all or most of your SharePoint Online content.</span></span>
   - <span data-ttu-id="b89ef-134">L’indexation complète des locataires importants peut prendre jusqu’à deux semaines.</span><span class="sxs-lookup"><span data-stu-id="b89ef-134">Large tenants can take up to two weeks to fully index.</span></span> <span data-ttu-id="b89ef-135">Bien que les rubriques soient générées de manière incrémentielle tout au long de cette période, l’indexation complète peut consommer jusqu’à la moitié de la période d’essai.</span><span class="sxs-lookup"><span data-stu-id="b89ef-135">While topics will be generated incrementally throughout this period, full indexing could consume up to half the trial period.</span></span>
   - <span data-ttu-id="b89ef-136">Pour les clients avec un volume important de données, cette option peut produire un très grand nombre de rubriques, voire des dizaines de milliers.</span><span class="sxs-lookup"><span data-stu-id="b89ef-136">For tenants with a significant volume of data, this option can produce a very large number of topics, perhaps tens of thousands.</span></span>

- <span data-ttu-id="b89ef-137">Identifiez un sous-ensemble de vos sites SharePoint à indexer.</span><span class="sxs-lookup"><span data-stu-id="b89ef-137">Identify a subset of your SharePoint sites for indexing.</span></span>

<span data-ttu-id="b89ef-138">Le choix de ces stratégies est un équilibre entre les deux facteurs suivants :</span><span class="sxs-lookup"><span data-stu-id="b89ef-138">The choice of these strategies is a balance of the following two factors:</span></span>

- <span data-ttu-id="b89ef-139">Suffisamment de données pour générer des rubriques significatives.</span><span class="sxs-lookup"><span data-stu-id="b89ef-139">Having enough data to generate meaningful topics.</span></span> <span data-ttu-id="b89ef-140">L’IA de Topics est mise au point pour fonctionner sur des jeux de données de grande taille, dans l’idéal ceux qui ont plus de 10 000 documents.</span><span class="sxs-lookup"><span data-stu-id="b89ef-140">The AI in Viva Topics is tuned to work on large datasets, ideally ones that have more than 10,000 documents.</span></span>
- <span data-ttu-id="b89ef-141">Le fait de ne pas générer autant de rubriques pendant la période d’évaluation que leur évaluation pendant la période disponible est difficile.</span><span class="sxs-lookup"><span data-stu-id="b89ef-141">Not generating so many topics during the trial period that evaluating them during the available time period is overwhelming.</span></span>

<span data-ttu-id="b89ef-142">Pour la plupart des organisations, la deuxième stratégie produit le meilleur résultat.</span><span class="sxs-lookup"><span data-stu-id="b89ef-142">For most organizations, the second strategy produces the best outcome.</span></span>

> [!NOTE]
> <span data-ttu-id="b89ef-143">En raison du nombre de documents requis par l’IA, nous vous recommandons d’exécuter des essais de Rubriques Dans le cas d’un client de production.</span><span class="sxs-lookup"><span data-stu-id="b89ef-143">Due to the number of documents required by the AI, we recommend that you run Viva Topics trials on a production tenant.</span></span> <span data-ttu-id="b89ef-144">Il n’y a aucun impact sur les performances du client pendant cette période.</span><span class="sxs-lookup"><span data-stu-id="b89ef-144">There’s no impact on the performance of the tenant during this period.</span></span> <span data-ttu-id="b89ef-145">Seuls les utilisateurs titulaires d’une licence d’essai peuvent accéder à l’expérience utilisateur de Topics.</span><span class="sxs-lookup"><span data-stu-id="b89ef-145">Only users who have a trial license can access Viva Topics user experiences.</span></span>

#### <a name="roles"></a><span data-ttu-id="b89ef-146">Rôles</span><span class="sxs-lookup"><span data-stu-id="b89ef-146">Roles</span></span>

<span data-ttu-id="b89ef-147">Au cours de la version d’essai, trois rôles doivent être actifs, qui sont décrits dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b89ef-147">During the trial, there are three roles that must be active, which are described in the following table.</span></span>

|<span data-ttu-id="b89ef-148">Rôle</span><span class="sxs-lookup"><span data-stu-id="b89ef-148">Role</span></span>  |<span data-ttu-id="b89ef-149">Activité</span><span class="sxs-lookup"><span data-stu-id="b89ef-149">Activity</span></span>  |
|---------|---------|
|<span data-ttu-id="b89ef-150">Gestionnaire des connaissances</span><span class="sxs-lookup"><span data-stu-id="b89ef-150">Knowledge manager</span></span>     |   <span data-ttu-id="b89ef-151">Contrôler les étapes du cycle de vie des rubriques ; confirmer et supprimer des rubriques ; agir en tant que gestionnaire de communauté pour les contributeurs de rubriques ;</span><span class="sxs-lookup"><span data-stu-id="b89ef-151">Control the lifecycle stages of topics; confirm and remove topics; act as a community manager for topic contributors</span></span>      |
|<span data-ttu-id="b89ef-152">Contributeur de rubrique</span><span class="sxs-lookup"><span data-stu-id="b89ef-152">Topic contributor</span></span>    |      <span data-ttu-id="b89ef-153">Experts techniques du contenu, qui peuvent :</span><span class="sxs-lookup"><span data-stu-id="b89ef-153">Content subject matter experts, who can:</span></span><br> <span data-ttu-id="b89ef-154">Examiner les rubriques pour évaluer la qualité du contenu défini par l’IA</span><span class="sxs-lookup"><span data-stu-id="b89ef-154">Review topics to evaluate the quality of AI-defined content</span></span><br><span data-ttu-id="b89ef-155">Organiser des rubriques découvertes avec du contenu supplémentaire</span><span class="sxs-lookup"><span data-stu-id="b89ef-155">Curate discovered topics with additional content</span></span><br><span data-ttu-id="b89ef-156">Créer des rubriques supplémentaires qui n’ont pas été découvertes par l’IA</span><span class="sxs-lookup"><span data-stu-id="b89ef-156">Create additional topics that weren’t discovered by AI</span></span>   |
|<span data-ttu-id="b89ef-157">Consommateur de rubriques</span><span class="sxs-lookup"><span data-stu-id="b89ef-157">Topic consumer</span></span>    |     <span data-ttu-id="b89ef-158">Utiliser des rubriques par le biais des points forts de la page et de la recherche</span><span class="sxs-lookup"><span data-stu-id="b89ef-158">Consume topics through page highlights and search</span></span><br><span data-ttu-id="b89ef-159">Fournir des commentaires sur la valeur des rubriques présentées</span><span class="sxs-lookup"><span data-stu-id="b89ef-159">Provide feedback on the value of the topics presented</span></span>    |

#### <a name="expected-topics"></a><span data-ttu-id="b89ef-160">Rubriques attendues</span><span class="sxs-lookup"><span data-stu-id="b89ef-160">Expected topics</span></span>

<span data-ttu-id="b89ef-161">Il peut être utile de documenter les rubriques que vous prévoyez d’être générées par l’IA, même si cela est basé uniquement sur des hypothèses.</span><span class="sxs-lookup"><span data-stu-id="b89ef-161">It can be useful to document the topics you expect to be generated by the AI, even if this is based only on assumptions.</span></span> <span data-ttu-id="b89ef-162">Cette tâche est plus facile à accomplir lorsque vous indexez un sous-ensemble défini de vos sites SharePoint pour lesquels les PME peuvent être identifiées facilement.</span><span class="sxs-lookup"><span data-stu-id="b89ef-162">This task is most easily completed when you index a defined subset of your SharePoint sites for which SMEs can be easily identified.</span></span>

<span data-ttu-id="b89ef-163">Le fait de disposer d’une liste documentée vous aidera à :</span><span class="sxs-lookup"><span data-stu-id="b89ef-163">Having a documented list will help you to:</span></span>

- <span data-ttu-id="b89ef-164">Examinez la liste des rubriques générées par l’IA, qui peuvent être plus volumineuses que prévu.</span><span class="sxs-lookup"><span data-stu-id="b89ef-164">Review the list of AI-generated topics, which might be larger than you expect.</span></span>
- <span data-ttu-id="b89ef-165">Connaissez les rubriques que vous devrez peut-être créer manuellement ou qui sont des priorités pour la curation.</span><span class="sxs-lookup"><span data-stu-id="b89ef-165">Know the topics you might need to manually create or that are priorities for curation.</span></span>

<span data-ttu-id="b89ef-166">Vous aurez toujours besoin d’une combinaison de rubriques définies par l’IA et de rubriques créées par l’être humain dans le cas d’un déploiement ou d’une version d’essai réussi de Topics.</span><span class="sxs-lookup"><span data-stu-id="b89ef-166">There will always be a need for a mixture of AI-defined and human-created topics in a successful deployment or trial of Viva Topics.</span></span>

## <a name="activate-a-trial"></a><span data-ttu-id="b89ef-167">Activer une version d’essai</span><span class="sxs-lookup"><span data-stu-id="b89ef-167">Activate a trial</span></span>

<span data-ttu-id="b89ef-168">Lorsque vous lancez une version d’essai, vous devez :</span><span class="sxs-lookup"><span data-stu-id="b89ef-168">When you initiate a trial, you need to:</span></span>

- <span data-ttu-id="b89ef-169">Attribuer des licences aux utilisateurs concernés.</span><span class="sxs-lookup"><span data-stu-id="b89ef-169">Assign licenses to the relevant users.</span></span>
- <span data-ttu-id="b89ef-170">Effectuez [une configuration](set-up-topic-experiences.md) supplémentaire de Rubriques Sous-programme.</span><span class="sxs-lookup"><span data-stu-id="b89ef-170">Perform [additional setup](set-up-topic-experiences.md) of Viva Topics.</span></span>

<span data-ttu-id="b89ef-171">Lorsque la version d’évaluation est activée, le processus de découverte de sujet commence.</span><span class="sxs-lookup"><span data-stu-id="b89ef-171">When the trial is activated, the topic discovery process begins.</span></span>

## <a name="during-a-trial"></a><span data-ttu-id="b89ef-172">Pendant une version d’essai</span><span class="sxs-lookup"><span data-stu-id="b89ef-172">During a trial</span></span>

<span data-ttu-id="b89ef-173">La période d’évaluation doit être utilisée pour évaluer les composants suivants de Topics :</span><span class="sxs-lookup"><span data-stu-id="b89ef-173">The trial period should be used to evaluate the following components of Viva Topics:</span></span>

- <span data-ttu-id="b89ef-174">Rubriques suggérées par l’IA et contenu de rubrique</span><span class="sxs-lookup"><span data-stu-id="b89ef-174">The AI-suggested topics and topic content</span></span>
- <span data-ttu-id="b89ef-175">Expériences de l’utilisateur final, avec l’utilisation de cartes de sujet sur des pages SharePoint modernes et dans Recherche Microsoft</span><span class="sxs-lookup"><span data-stu-id="b89ef-175">The end-user experiences, surfacing topic cards on modern SharePoint pages and in Microsoft Search</span></span>

<span data-ttu-id="b89ef-176">Tenez compte de ces facteurs :</span><span class="sxs-lookup"><span data-stu-id="b89ef-176">Consider these factors:</span></span>

- <span data-ttu-id="b89ef-177">Pour que Topics offre la valeur maximale, le contenu des rubriques doit être une combinaison de contenu défini par l’IA et de contenu organisé par l’être humain.</span><span class="sxs-lookup"><span data-stu-id="b89ef-177">For Viva Topics to deliver the maximum value, the content in topics needs to be a combination of AI-defined content and human-curated content.</span></span>
- <span data-ttu-id="b89ef-178">Toutes les expériences utilisateur sont « découpées en autorisations » (y compris l’affichage du gestionnaire de connaissances sur la page Gérer **les rubriques).**</span><span class="sxs-lookup"><span data-stu-id="b89ef-178">All user experiences are “permission trimmed” (including the knowledge manager’s view on the **Manage topics** page).</span></span> <span data-ttu-id="b89ef-179">Les utilisateurs ne voient une rubrique que s’ils sont autorisés à afficher certaines des ressources qui ont été utilisées pour générer la rubrique.</span><span class="sxs-lookup"><span data-stu-id="b89ef-179">Users will only see a topic if they have permissions to view some of the resources that were used to generate the topic.</span></span> <span data-ttu-id="b89ef-180">Cela signifie que différents utilisateurs peuvent voir un contenu différent sur la même page de rubrique.</span><span class="sxs-lookup"><span data-stu-id="b89ef-180">This means that different users might see different content on the same topic page.</span></span>
- <span data-ttu-id="b89ef-181">Les utilisateurs peuvent voir plusieurs rubriques qui ont le même nom dans la page **Gérer les rubriques.**</span><span class="sxs-lookup"><span data-stu-id="b89ef-181">Users might see multiple topics that have the same name in the **Manage topics** page.</span></span> <span data-ttu-id="b89ef-182">Ces rubriques ne sont pas nécessairement des doublons, mais peuvent être dues à un seul terme utilisé dans plusieurs contextes dans les données, comme un nom de code de projet utilisé par deux projets distincts.</span><span class="sxs-lookup"><span data-stu-id="b89ef-182">These topics aren't necessarily duplicates but might be because of a single term that’s used in multiple contexts in the data, such as a project code name that’s used by two distinct projects.</span></span>

## <a name="after-a-trial"></a><span data-ttu-id="b89ef-183">Après une version d’essai</span><span class="sxs-lookup"><span data-stu-id="b89ef-183">After a trial</span></span>

<span data-ttu-id="b89ef-184">En fonction du résultat de la version d’essai, vous pouvez décider s’il faut passer à l’utilisation en production de Topics.</span><span class="sxs-lookup"><span data-stu-id="b89ef-184">Based on the outcome of the trial, you can decide whether to proceed to production use of Viva Topics.</span></span>

### <a name="proceed-to-production-use"></a><span data-ttu-id="b89ef-185">Passer à l’utilisation de la production</span><span class="sxs-lookup"><span data-stu-id="b89ef-185">Proceed to production use</span></span>

<span data-ttu-id="b89ef-186">Pour garantir la continuité du service, vous devez acheter le nombre requis de licences et les attribuer aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b89ef-186">To ensure continuity of service, you must purchase the required number of licenses and assign those licenses to users.</span></span> <span data-ttu-id="b89ef-187">Les utilisateurs de la version d’essai qui ne sont pas titulaires d’une licence complète à la fin de la période d’essai ne pourront accéder à aucune expérience Topics.</span><span class="sxs-lookup"><span data-stu-id="b89ef-187">Trial users who don’t have a full license at the end of the trial period won’t be able to access any Viva Topics experiences.</span></span>

### <a name="dont-proceed-to-production-use"></a><span data-ttu-id="b89ef-188">Ne pas passer à l’utilisation en production</span><span class="sxs-lookup"><span data-stu-id="b89ef-188">Don’t proceed to production use</span></span>

<span data-ttu-id="b89ef-189">Si vous n’achetez pas de licences à la suite de la version d’essai :</span><span class="sxs-lookup"><span data-stu-id="b89ef-189">If you don’t purchase licenses following the trial:</span></span>

- <span data-ttu-id="b89ef-190">La découverte de rubrique s’arrête.</span><span class="sxs-lookup"><span data-stu-id="b89ef-190">Topic discovery will stop.</span></span>
- <span data-ttu-id="b89ef-191">Les utilisateurs ne voient plus les points forts ou les cartes des rubriques.</span><span class="sxs-lookup"><span data-stu-id="b89ef-191">Users will no longer see topic highlights or cards.</span></span>
- <span data-ttu-id="b89ef-192">Le centre de rubriques ne sera pas supprimé, mais les rubriques suggérées et les expériences de gestion des rubriques ne seront pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="b89ef-192">The topic center won’t be deleted, but the suggested topics and manage topics experiences won’t be available.</span></span>
- <span data-ttu-id="b89ef-193">Toutes les rubriques définies par l’IA seront perdues.</span><span class="sxs-lookup"><span data-stu-id="b89ef-193">Any AI-defined topics will be lost.</span></span>
- <span data-ttu-id="b89ef-194">Les rubriques qui ont été modifiées par un collaborateur de rubrique resteront dans la bibliothèque de pages du centre de rubriques.</span><span class="sxs-lookup"><span data-stu-id="b89ef-194">Topics that have been edited by a topic contributor will remain in the topic center pages library.</span></span> <span data-ttu-id="b89ef-195">Seul le contenu fourni manuellement reste sur ces pages, pas sur le contenu suggéré par l’IA.</span><span class="sxs-lookup"><span data-stu-id="b89ef-195">Only the manually provided content will remain on these pages, not any AI-suggested content.</span></span>

## <a name="see-also"></a><span data-ttu-id="b89ef-196">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b89ef-196">See also</span></span>

[<span data-ttu-id="b89ef-197">Commencer à piloter l’adoption des rubriques microsoft</span><span class="sxs-lookup"><span data-stu-id="b89ef-197">Get started driving adoption of Microsoft Viva Topics</span></span>](topics-adoption-getstarted.md)

