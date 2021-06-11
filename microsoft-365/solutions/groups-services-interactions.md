---
title: Interactions avec les services de groupes
ms.reviewer: ''
ms.author: mikeplum
author: MikePlumleyMSFT
manager: serdars
audience: Admin
ms.topic: article
ms.prod: microsoft-365-enterprise
localization_priority: Normal
ms.collection:
- M365-collaboration
- m365solution-collabgovernance
ms.custom:
- M365solutions
f1.keywords: NOCSH
recommendations: false
description: Interactions avec les services de groupes
ms.openlocfilehash: f9b0d7ca61d55e3d23aa94577fc8257073b26675
ms.sourcegitcommit: f780de91bc00caeb1598781e0076106c76234bad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52539202"
---
# <a name="groups-services-interactions"></a><span data-ttu-id="ca8d9-103">Interactions avec les services de groupes</span><span class="sxs-lookup"><span data-stu-id="ca8d9-103">Groups services interactions</span></span>

<span data-ttu-id="ca8d9-104">Microsoft 365 Les groupes fournissent une structure commune à un certain nombre de services et de charges de travail au sein de la plateforme Microsoft 365 pour offrir une expérience connectée aux utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-104">Microsoft 365 Groups provides a common fabric for a number of services and workloads within the Microsoft 365 platform to deliver a connected experience for end-users.</span></span> <span data-ttu-id="ca8d9-105">À la base, un groupe Microsoft 365 existe pour fournir :</span><span class="sxs-lookup"><span data-stu-id="ca8d9-105">At its core, a Microsoft 365 group exists to provide:</span></span>

- <span data-ttu-id="ca8d9-106">Un moyen de gérer l’appartenance (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="ca8d9-106">A way to manage the membership (Azure AD)</span></span>
- <span data-ttu-id="ca8d9-107">Un lieu de messagerie et de conversations (boîte aux lettres Exchange, Microsoft Teams, Yammer)</span><span class="sxs-lookup"><span data-stu-id="ca8d9-107">A place for messaging and conversations to take place (Exchange mailbox, Microsoft Teams, Yammer)</span></span>
- <span data-ttu-id="ca8d9-108">Un endroit où stocker des fichiers (SharePoint)</span><span class="sxs-lookup"><span data-stu-id="ca8d9-108">A place for files to be stored (SharePoint)</span></span>
- <span data-ttu-id="ca8d9-109">Un calendrier pour la planification (Exchange)</span><span class="sxs-lookup"><span data-stu-id="ca8d9-109">A calendar for scheduling (Exchange)</span></span>
- <span data-ttu-id="ca8d9-110">Un bloc-notes pour la capture de notes (OneNote)</span><span class="sxs-lookup"><span data-stu-id="ca8d9-110">A notebook for capturing notes (OneNote)</span></span>

<span data-ttu-id="ca8d9-111">Au moment de la création du groupe, un certain nombre d’autres ressources sont également mise en service, mais elles ne sont pas visibles tant qu’elles n’ont pas été accédées pour la première fois à partir du service :</span><span class="sxs-lookup"><span data-stu-id="ca8d9-111">At the point of group creation, a number of other resources are also provisioned, however they are not visible until accessed for the first time from the service:</span></span>

- <span data-ttu-id="ca8d9-112">Un tableau pour la gestion des tâches de groupe (Planificateur)</span><span class="sxs-lookup"><span data-stu-id="ca8d9-112">A board for managing group tasks (Planner)</span></span>
- <span data-ttu-id="ca8d9-113">Espace de travail pour les rapports (Power BI)</span><span class="sxs-lookup"><span data-stu-id="ca8d9-113">A workspace for reporting (Power BI)</span></span>
- <span data-ttu-id="ca8d9-114">Une zone pour les vidéos partagées (Microsoft Stream)</span><span class="sxs-lookup"><span data-stu-id="ca8d9-114">An area for shared videos (Microsoft Stream)</span></span>
- <span data-ttu-id="ca8d9-115">Une zone pour les formulaires partagés (formulaires)</span><span class="sxs-lookup"><span data-stu-id="ca8d9-115">An area for shared forms (Forms)</span></span>

<span data-ttu-id="ca8d9-116">Dans Microsoft 365, d’autres services peuvent interagir avec des groupes Microsoft 365 pour fournir des fonctionnalités et des fonctionnalités supplémentaires aux membres du groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-116">Across Microsoft 365, other services are able to interact with Microsoft 365 groups to deliver additional functionality and capabilities to group members.</span></span>
<span data-ttu-id="ca8d9-117">Voici quelques exemples :</span><span class="sxs-lookup"><span data-stu-id="ca8d9-117">Examples of this include:</span></span>

- <span data-ttu-id="ca8d9-118">Power Apps applications</span><span class="sxs-lookup"><span data-stu-id="ca8d9-118">Power Apps for apps</span></span>
- <span data-ttu-id="ca8d9-119">Power Automate flux de travail</span><span class="sxs-lookup"><span data-stu-id="ca8d9-119">Power Automate for workflows</span></span>
- <span data-ttu-id="ca8d9-120">Project sur le web et feuille de route pour la gestion de projet en cascade</span><span class="sxs-lookup"><span data-stu-id="ca8d9-120">Project on the web and Roadmap for waterfall-based project management</span></span>
- <span data-ttu-id="ca8d9-121">Teams pour les conversations basées sur un canal</span><span class="sxs-lookup"><span data-stu-id="ca8d9-121">Teams for channel-based conversations</span></span>
- <span data-ttu-id="ca8d9-122">Yammer pour les communautés d’intérêt</span><span class="sxs-lookup"><span data-stu-id="ca8d9-122">Yammer for communities of interest</span></span>

## <a name="user-interactions-with-groups"></a><span data-ttu-id="ca8d9-123">Interactions des utilisateurs avec les groupes</span><span class="sxs-lookup"><span data-stu-id="ca8d9-123">User interactions with groups</span></span>

<span data-ttu-id="ca8d9-124">Microsoft 365 Les groupes peuvent être créés et gérés à partir d’une variété d’interfaces, à la fois par les administrateurs et les utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-124">Microsoft 365 Groups can be created and managed from a variety of interfaces, both by administrators and end-users.</span></span> 

### <a name="administrative-experiences"></a><span data-ttu-id="ca8d9-125">Expériences administratives</span><span class="sxs-lookup"><span data-stu-id="ca8d9-125">Administrative experiences</span></span>

<span data-ttu-id="ca8d9-126">Les administrateurs peuvent créer et gérer des groupes Microsoft 365 à partir de plusieurs centres d’administration de charge de travail, des interfaces de ligne de commande qui gèrent les scripts, ainsi que des applications personnalisées qui interagissent avec l’API Graph.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-126">Administrators can create and manage Microsoft 365 groups from several of the workload admin centers, command-line interfaces that support scripting, as well as custom-built apps interacting with the Graph API.</span></span> <span data-ttu-id="ca8d9-127">La seule exception à ce problème concerne Yammer groupes , qui doivent être créés à partir de l’interface Yammer web.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-127">The only exception to this is Yammer groups – which must be created from within the Yammer web interface.</span></span>

<span data-ttu-id="ca8d9-128">**Paramètres associés**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-128">**Related settings**</span></span>

<span data-ttu-id="ca8d9-129">Dans les différentes interfaces d’administration qui peuvent gérer les paramètres de groupe, il existe plusieurs chevauchements que vous devez connaître.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-129">Across the various administrative interfaces that can manage group settings exists several overlaps which you should be aware of.</span></span>

<span data-ttu-id="ca8d9-130">**Centre d’administration Microsoft 365**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-130">**Microsoft 365 admin center**</span></span>

<span data-ttu-id="ca8d9-131">Dans le Microsoft 365 d’administration, l’accès invité aux groupes est activé par défaut, tout comme la possibilité d’autoriser les propriétaires à ajouter des invités.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-131">In the Microsoft 365 admin center, guest access to Groups is enabled by default, as is the ability to allow owners to add guests.</span></span> <span data-ttu-id="ca8d9-132">Aucun autre contrôle au niveau de l’organisation n’est disponible pour les groupes à partir de ce centre d’administration.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-132">There are no further organization-level controls available for Groups from this admin center.</span></span>

<span data-ttu-id="ca8d9-133">**Centre d’administration d’Azure AD**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-133">**Azure AD admin center**</span></span>

<span data-ttu-id="ca8d9-134">Le Centre d’administration Azure AD permet de contrôler si les utilisateurs peuvent créer des groupes ou affecter des propriétaires dans les portails Azure, ainsi que des paramètres de stratégie d’expiration et d’affectation de noms.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-134">The Azure AD admin center offers controls around whether users can create Groups or assign owners in Azure portals, as well as expiration and naming policy settings.</span></span>

<span data-ttu-id="ca8d9-135">Le Centre d’administration fournit également un certain nombre de mesures de contrôle d’invitation invité qui vont au-delà de celle du Centre d’administration Microsoft 365, telles que la possibilité de limiter si les non-propriétaires peuvent également inviter des invités</span><span class="sxs-lookup"><span data-stu-id="ca8d9-135">The admin center also provides a number of guest invitation control measures that go beyond that of the Microsoft 365 admin center, such as the ability to limit whether non-owners can also invite guests</span></span>

<span data-ttu-id="ca8d9-136">**SharePoint**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-136">**SharePoint**</span></span>

<span data-ttu-id="ca8d9-137">SharePoint sites sont créés avec les groupes de sécurité Propriétaire, Membre et Visiteur, les deux premiers correspondant à leurs équivalents Microsoft 365 groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-137">SharePoint sites are created with Owner, Member and Visitor security groups, with the first two matching up to their Microsoft 365 Group counterparts.</span></span> <span data-ttu-id="ca8d9-138">Bien que l’appartenance SharePoint sites en ligne soit généralement gérée par le groupe Microsoft 365 associé, il ne s’agit pas d’une relation bidirectionnelle.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-138">While membership for SharePoint Online sites is generally managed by the associated Microsoft 365 Group, it is not a bidirectional relationship.</span></span> <span data-ttu-id="ca8d9-139">Les modifications apportées à l’appartenance au niveau du groupe Microsoft 365 sont reflétées dans SharePoint. Toutefois, si l’appartenance est modifiée dans le groupe SharePoint, cela n’est pas reflété dans le groupe Microsoft 365 groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-139">Any changes to membership at the Microsoft 365 group level are reflected in SharePoint, however if membership is changed in the SharePoint group, this is not reflected in the Microsoft 365 group.</span></span>

### <a name="user-experiences"></a><span data-ttu-id="ca8d9-140">Expériences utilisateur</span><span class="sxs-lookup"><span data-stu-id="ca8d9-140">User experiences</span></span>

<span data-ttu-id="ca8d9-141">Les utilisateurs finaux peuvent créer des groupes à partir de plusieurs services au sein Microsoft 365, et dans d’autres, ils peuvent uniquement partager avec un groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-141">End users can create groups from several of the services within Microsoft 365, and in others they can only share with a group.</span></span>

<span data-ttu-id="ca8d9-142">Les services suivants permettent la création de groupes par les utilisateurs finaux :</span><span class="sxs-lookup"><span data-stu-id="ca8d9-142">The following services allow creation of groups by end users:</span></span>
                         
<span data-ttu-id="ca8d9-143">Outlook Planificateur Project pour la SharePoint Stream Microsoft Teams Yammer</span><span class="sxs-lookup"><span data-stu-id="ca8d9-143">Outlook Planner Project for the web SharePoint  Stream  Microsoft Teams Yammer</span></span>

<span data-ttu-id="ca8d9-144">**Restriction de la création de groupes**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-144">**Restriction of group creation**</span></span>

<span data-ttu-id="ca8d9-145">Une approche courante pour contrôler l’étendue des équipes consiste à limiter les utilisateurs qui peuvent les créer.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-145">A common approach to control sprawl of teams is to limit which users can create them.</span></span> <span data-ttu-id="ca8d9-146">Pour ce faire, vous ne pouvez le faire qu’en limitant la création de groupes.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-146">This can only be done by limiting the creation of groups.</span></span> <span data-ttu-id="ca8d9-147">Cela a une incidence sur la possibilité de créer des groupes à partir d’autres services qui peuvent être nécessaires pour l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-147">Doing this impacts the ability to create groups from other services where that may be necessary for end-user.</span></span> <span data-ttu-id="ca8d9-148">Microsoft 365 Les groupes ne permettent pas de restreindre la création de groupes à partir de certaines applications ou services tout en le permettant à d’autres.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-148">Microsoft 365 Groups does not support the ability to restrict the creation of groups from some apps or services while allowing it from others.</span></span>

<span data-ttu-id="ca8d9-149">L’expérience de restriction de création de groupe varie selon les applications et les services :</span><span class="sxs-lookup"><span data-stu-id="ca8d9-149">The experience of group creation restriction varies between apps and services:</span></span>


|<span data-ttu-id="ca8d9-150">Application ou service</span><span class="sxs-lookup"><span data-stu-id="ca8d9-150">App or service</span></span>|<span data-ttu-id="ca8d9-151">Expérience</span><span class="sxs-lookup"><span data-stu-id="ca8d9-151">Experience</span></span>|
|:-------------|:---------|
|<span data-ttu-id="ca8d9-152">Outlook</span><span class="sxs-lookup"><span data-stu-id="ca8d9-152">Outlook</span></span>|<span data-ttu-id="ca8d9-153">**L’option** Nouveau groupe est supprimée du menu Nouveau dans la page Personnes</span><span class="sxs-lookup"><span data-stu-id="ca8d9-153">**New group** option is removed from New menu in people page</span></span>|
|<span data-ttu-id="ca8d9-154">Planificateur</span><span class="sxs-lookup"><span data-stu-id="ca8d9-154">Planner</span></span>|<span data-ttu-id="ca8d9-155">**Le nouveau plan** explique que la création de groupe a été désactivée et propose d’ajouter le plan à un groupe existant</span><span class="sxs-lookup"><span data-stu-id="ca8d9-155">**New plan** explains that group creation has been turned off and offers to add the plan to an existing group</span></span>|
|<span data-ttu-id="ca8d9-156">Project web et feuille de route</span><span class="sxs-lookup"><span data-stu-id="ca8d9-156">Project for the web and Roadmap</span></span>|<span data-ttu-id="ca8d9-157">**Le** menu Créer un groupe explique que la création de groupe est restreinte et suggère l’utilisation d’un groupe existant.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-157">**Create group** menu explains that group creation is restricted and suggests using an existing group.</span></span>|
|<span data-ttu-id="ca8d9-158">SharePoint</span><span class="sxs-lookup"><span data-stu-id="ca8d9-158">SharePoint</span></span>|<span data-ttu-id="ca8d9-159">Toujours en mesure de créer un site d’équipe qui n’est pas connecté à un groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-159">Still able to create a team site that is not connected to a group.</span></span>|
|<span data-ttu-id="ca8d9-160">Flux</span><span class="sxs-lookup"><span data-stu-id="ca8d9-160">Stream</span></span>|<span data-ttu-id="ca8d9-161">**L’option** Groupe n’apparaît pas sous **le menu Créer.**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-161">**Group** option does not appear under the **Create menu**.</span></span>|
|<span data-ttu-id="ca8d9-162">Teams</span><span class="sxs-lookup"><span data-stu-id="ca8d9-162">Teams</span></span>|<span data-ttu-id="ca8d9-163">L’utilisateur ne peut pas créer d’équipe avec un nouveau groupe, mais peut toujours créer une équipe qui utilise un groupe existant.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-163">User cannot create a team with a new group but can still create a team that utilizes an existing group.</span></span><br><br><span data-ttu-id="ca8d9-164">**Créer un bouton d’équipe** est remplacé par **Créer une équipe à partir d’un groupe.**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-164">**Create a team** button is replaced with **Create team from a group**.</span></span>|
|<span data-ttu-id="ca8d9-165">Yammer</span><span class="sxs-lookup"><span data-stu-id="ca8d9-165">Yammer</span></span>|<span data-ttu-id="ca8d9-166">**L’option Créer un** groupe est supprimée de la navigation groupes/communautés principale.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-166">**Create a group** option is removed from main Groups/Communities navigation.</span></span>|

## <a name="services-interactions-with-groups"></a><span data-ttu-id="ca8d9-167">Interactions des services avec les groupes</span><span class="sxs-lookup"><span data-stu-id="ca8d9-167">Services interactions with groups</span></span>

<span data-ttu-id="ca8d9-168">Consultez l’affiche Groupes Microsoft 365 pour plus d’informations sur les différents types de groupes, la façon dont ils sont créés et gérés, ainsi que quelques recommandations de gouvernance.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-168">See the Groups in Microsoft 365 poster for information about different types of groups, how these are created and managed, and a few governance recommendations.</span></span>

<span data-ttu-id="ca8d9-169">[![Image miniature pour les groupes infographie](../downloads/msft-m365-groups-architecture-thumb.png)](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/downloads/msft-m365-groups.pdf)</span><span class="sxs-lookup"><span data-stu-id="ca8d9-169">[![Thumb image for groups infographic](../downloads/msft-m365-groups-architecture-thumb.png)](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/downloads/msft-m365-groups.pdf)</span></span>

<span data-ttu-id="ca8d9-170">[PDF](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/downloads/msft-m365-groups.pdf) \| [Visio](https://github.com/MicrosoftDocs/OfficeDocs-Enterprise/raw/live/Enterprise/downloads/msft-m365-groups.vsdx)</span><span class="sxs-lookup"><span data-stu-id="ca8d9-170">[PDF](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/downloads/msft-m365-groups.pdf) \| [Visio](https://github.com/MicrosoftDocs/OfficeDocs-Enterprise/raw/live/Enterprise/downloads/msft-m365-groups.vsdx)</span></span>

<span data-ttu-id="ca8d9-171">Le tableau suivant fournit une vue d’ensemble des interactions Microsoft 365 groupes avec différents services :</span><span class="sxs-lookup"><span data-stu-id="ca8d9-171">The following table provides an overview of Microsoft 365 Groups interactions with various services:</span></span>

|<span data-ttu-id="ca8d9-172">Produit</span><span class="sxs-lookup"><span data-stu-id="ca8d9-172">Product</span></span>|<span data-ttu-id="ca8d9-173">Fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="ca8d9-173">Features</span></span>|<span data-ttu-id="ca8d9-174">Fait le service</span><span class="sxs-lookup"><span data-stu-id="ca8d9-174">Does the service</span></span><br><span data-ttu-id="ca8d9-175">existe-t-il sans groupe ?</span><span class="sxs-lookup"><span data-stu-id="ca8d9-175">exist without a group?</span></span>|<span data-ttu-id="ca8d9-176">Le service peut-il être</span><span class="sxs-lookup"><span data-stu-id="ca8d9-176">Can the service</span></span><br><span data-ttu-id="ca8d9-177">créer un groupe</span><span class="sxs-lookup"><span data-stu-id="ca8d9-177">create a group?</span></span>|<span data-ttu-id="ca8d9-178">La suppression de la</span><span class="sxs-lookup"><span data-stu-id="ca8d9-178">Does deleting the</span></span><br><span data-ttu-id="ca8d9-179">supprimer le groupe ?</span><span class="sxs-lookup"><span data-stu-id="ca8d9-179">instance delete the group?</span></span>|
|:---|:---|:---|:---|:---|
|<span data-ttu-id="ca8d9-180">Azure AD</span><span class="sxs-lookup"><span data-stu-id="ca8d9-180">Azure AD</span></span>|<span data-ttu-id="ca8d9-181">Appartenance, contrôles de groupe, invités</span><span class="sxs-lookup"><span data-stu-id="ca8d9-181">Membership, Group controls, Guests</span></span>|<span data-ttu-id="ca8d9-182">Oui</span><span class="sxs-lookup"><span data-stu-id="ca8d9-182">Yes</span></span>|<span data-ttu-id="ca8d9-183">Oui</span><span class="sxs-lookup"><span data-stu-id="ca8d9-183">Yes</span></span>|<span data-ttu-id="ca8d9-184">Oui</span><span class="sxs-lookup"><span data-stu-id="ca8d9-184">Yes</span></span>|
|<span data-ttu-id="ca8d9-185">Exchange</span><span class="sxs-lookup"><span data-stu-id="ca8d9-185">Exchange</span></span>|<span data-ttu-id="ca8d9-186">Calendrier, boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="ca8d9-186">Calendar, mailbox</span></span>|<span data-ttu-id="ca8d9-187">Oui</span><span class="sxs-lookup"><span data-stu-id="ca8d9-187">Yes</span></span>|<span data-ttu-id="ca8d9-188">Oui</span><span class="sxs-lookup"><span data-stu-id="ca8d9-188">Yes</span></span>|<span data-ttu-id="ca8d9-189">Oui</span><span class="sxs-lookup"><span data-stu-id="ca8d9-189">Yes</span></span>|
|<span data-ttu-id="ca8d9-190">Formulaires</span><span class="sxs-lookup"><span data-stu-id="ca8d9-190">Forms</span></span>|<span data-ttu-id="ca8d9-191">Formulaire</span><span class="sxs-lookup"><span data-stu-id="ca8d9-191">Form</span></span>|<span data-ttu-id="ca8d9-192">Oui</span><span class="sxs-lookup"><span data-stu-id="ca8d9-192">Yes</span></span>|<span data-ttu-id="ca8d9-193">Non</span><span class="sxs-lookup"><span data-stu-id="ca8d9-193">No</span></span>|<span data-ttu-id="ca8d9-194">Non</span><span class="sxs-lookup"><span data-stu-id="ca8d9-194">No</span></span>|
|<span data-ttu-id="ca8d9-195">OneNote</span><span class="sxs-lookup"><span data-stu-id="ca8d9-195">OneNote</span></span>|<span data-ttu-id="ca8d9-196">Bloc-notes</span><span class="sxs-lookup"><span data-stu-id="ca8d9-196">Notebook</span></span>|<span data-ttu-id="ca8d9-197">Oui</span><span class="sxs-lookup"><span data-stu-id="ca8d9-197">Yes</span></span>|<span data-ttu-id="ca8d9-198">Non</span><span class="sxs-lookup"><span data-stu-id="ca8d9-198">No</span></span>|<span data-ttu-id="ca8d9-199">Non</span><span class="sxs-lookup"><span data-stu-id="ca8d9-199">No</span></span>|
|<span data-ttu-id="ca8d9-200">Planificateur</span><span class="sxs-lookup"><span data-stu-id="ca8d9-200">Planner</span></span>|<span data-ttu-id="ca8d9-201">Tableau des tâches</span><span class="sxs-lookup"><span data-stu-id="ca8d9-201">Task board</span></span>|<span data-ttu-id="ca8d9-202">Non</span><span class="sxs-lookup"><span data-stu-id="ca8d9-202">No</span></span>|<span data-ttu-id="ca8d9-203">Oui</span><span class="sxs-lookup"><span data-stu-id="ca8d9-203">Yes</span></span>|<span data-ttu-id="ca8d9-204">Oui</span><span class="sxs-lookup"><span data-stu-id="ca8d9-204">Yes</span></span>|
|<span data-ttu-id="ca8d9-205">Power Apps application</span><span class="sxs-lookup"><span data-stu-id="ca8d9-205">Power Apps app</span></span>|<span data-ttu-id="ca8d9-206">Application</span><span class="sxs-lookup"><span data-stu-id="ca8d9-206">App</span></span>|<span data-ttu-id="ca8d9-207">Oui</span><span class="sxs-lookup"><span data-stu-id="ca8d9-207">Yes</span></span>|<span data-ttu-id="ca8d9-208">Non</span><span class="sxs-lookup"><span data-stu-id="ca8d9-208">No</span></span>|<span data-ttu-id="ca8d9-209">Non</span><span class="sxs-lookup"><span data-stu-id="ca8d9-209">No</span></span>|
|<span data-ttu-id="ca8d9-210">Power Automate</span><span class="sxs-lookup"><span data-stu-id="ca8d9-210">Power Automate</span></span>|<span data-ttu-id="ca8d9-211">Flux de travail</span><span class="sxs-lookup"><span data-stu-id="ca8d9-211">Workflow</span></span>|<span data-ttu-id="ca8d9-212">Oui</span><span class="sxs-lookup"><span data-stu-id="ca8d9-212">Yes</span></span>|<span data-ttu-id="ca8d9-213">Non</span><span class="sxs-lookup"><span data-stu-id="ca8d9-213">No</span></span>|<span data-ttu-id="ca8d9-214">Non</span><span class="sxs-lookup"><span data-stu-id="ca8d9-214">No</span></span>|
|<span data-ttu-id="ca8d9-215">Power BI (classique)</span><span class="sxs-lookup"><span data-stu-id="ca8d9-215">Power BI (classic)</span></span>|<span data-ttu-id="ca8d9-216">Workspace</span><span class="sxs-lookup"><span data-stu-id="ca8d9-216">Workspace</span></span>|<span data-ttu-id="ca8d9-217">Non</span><span class="sxs-lookup"><span data-stu-id="ca8d9-217">No</span></span>|<span data-ttu-id="ca8d9-218">Oui</span><span class="sxs-lookup"><span data-stu-id="ca8d9-218">Yes</span></span>|<span data-ttu-id="ca8d9-219">Oui</span><span class="sxs-lookup"><span data-stu-id="ca8d9-219">Yes</span></span>|
|<span data-ttu-id="ca8d9-220">Power BI (nouveau)</span><span class="sxs-lookup"><span data-stu-id="ca8d9-220">Power BI (new)</span></span>|<span data-ttu-id="ca8d9-221">Workspace</span><span class="sxs-lookup"><span data-stu-id="ca8d9-221">Workspace</span></span>|<span data-ttu-id="ca8d9-222">Oui</span><span class="sxs-lookup"><span data-stu-id="ca8d9-222">Yes</span></span>|<span data-ttu-id="ca8d9-223">Non</span><span class="sxs-lookup"><span data-stu-id="ca8d9-223">No</span></span>|<span data-ttu-id="ca8d9-224">Oui</span><span class="sxs-lookup"><span data-stu-id="ca8d9-224">Yes</span></span>|
|<span data-ttu-id="ca8d9-225">Project for the web</span><span class="sxs-lookup"><span data-stu-id="ca8d9-225">Project for the web</span></span>|<span data-ttu-id="ca8d9-226">Project plan</span><span class="sxs-lookup"><span data-stu-id="ca8d9-226">Project plan</span></span>|<span data-ttu-id="ca8d9-227">Oui</span><span class="sxs-lookup"><span data-stu-id="ca8d9-227">Yes</span></span>|<span data-ttu-id="ca8d9-228">Oui</span><span class="sxs-lookup"><span data-stu-id="ca8d9-228">Yes</span></span>|<span data-ttu-id="ca8d9-229">Non</span><span class="sxs-lookup"><span data-stu-id="ca8d9-229">No</span></span>|
|<span data-ttu-id="ca8d9-230">Feuille de route</span><span class="sxs-lookup"><span data-stu-id="ca8d9-230">Roadmap</span></span>|<span data-ttu-id="ca8d9-231">Feuille de route</span><span class="sxs-lookup"><span data-stu-id="ca8d9-231">Roadmap</span></span>|<span data-ttu-id="ca8d9-232">Oui</span><span class="sxs-lookup"><span data-stu-id="ca8d9-232">Yes</span></span>|<span data-ttu-id="ca8d9-233">Oui</span><span class="sxs-lookup"><span data-stu-id="ca8d9-233">Yes</span></span>|<span data-ttu-id="ca8d9-234">Non</span><span class="sxs-lookup"><span data-stu-id="ca8d9-234">No</span></span>|
|<span data-ttu-id="ca8d9-235">SharePoint</span><span class="sxs-lookup"><span data-stu-id="ca8d9-235">SharePoint</span></span>|<span data-ttu-id="ca8d9-236">Site</span><span class="sxs-lookup"><span data-stu-id="ca8d9-236">Site</span></span>|<span data-ttu-id="ca8d9-237">Oui</span><span class="sxs-lookup"><span data-stu-id="ca8d9-237">Yes</span></span>|<span data-ttu-id="ca8d9-238">Oui</span><span class="sxs-lookup"><span data-stu-id="ca8d9-238">Yes</span></span>|<span data-ttu-id="ca8d9-239">Oui</span><span class="sxs-lookup"><span data-stu-id="ca8d9-239">Yes</span></span>|
|<span data-ttu-id="ca8d9-240">Flux</span><span class="sxs-lookup"><span data-stu-id="ca8d9-240">Stream</span></span>|<span data-ttu-id="ca8d9-241">Canal, vidéo</span><span class="sxs-lookup"><span data-stu-id="ca8d9-241">Channel, video</span></span>|<span data-ttu-id="ca8d9-242">Oui</span><span class="sxs-lookup"><span data-stu-id="ca8d9-242">Yes</span></span>|<span data-ttu-id="ca8d9-243">Oui</span><span class="sxs-lookup"><span data-stu-id="ca8d9-243">Yes</span></span>|<span data-ttu-id="ca8d9-244">Oui</span><span class="sxs-lookup"><span data-stu-id="ca8d9-244">Yes</span></span>|
|<span data-ttu-id="ca8d9-245">Teams</span><span class="sxs-lookup"><span data-stu-id="ca8d9-245">Teams</span></span>|<span data-ttu-id="ca8d9-246">Équipe</span><span class="sxs-lookup"><span data-stu-id="ca8d9-246">Team</span></span>|<span data-ttu-id="ca8d9-247">Non</span><span class="sxs-lookup"><span data-stu-id="ca8d9-247">No</span></span>|<span data-ttu-id="ca8d9-248">Oui</span><span class="sxs-lookup"><span data-stu-id="ca8d9-248">Yes</span></span>|<span data-ttu-id="ca8d9-249">Oui</span><span class="sxs-lookup"><span data-stu-id="ca8d9-249">Yes</span></span>|
|<span data-ttu-id="ca8d9-250">Yammer</span><span class="sxs-lookup"><span data-stu-id="ca8d9-250">Yammer</span></span>|<span data-ttu-id="ca8d9-251">Group</span><span class="sxs-lookup"><span data-stu-id="ca8d9-251">Group</span></span>|<span data-ttu-id="ca8d9-252">Oui</span><span class="sxs-lookup"><span data-stu-id="ca8d9-252">Yes</span></span>|<span data-ttu-id="ca8d9-253">Oui</span><span class="sxs-lookup"><span data-stu-id="ca8d9-253">Yes</span></span>|<span data-ttu-id="ca8d9-254">Oui</span><span class="sxs-lookup"><span data-stu-id="ca8d9-254">Yes</span></span>|

<span data-ttu-id="ca8d9-255">Bien que le tableau ci-dessus offre une vue d’ensemble des interactions de groupe avec les services Microsoft 365, il existe un certain nombre de nuances et de complexités que vous devez comprendre.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-255">While the table above provides a high-level overview of group interactions with Microsoft 365 services, there are a number of nuances and intricacies that you should understand.</span></span> <span data-ttu-id="ca8d9-256">Les sections suivantes analysent de façon plus approfondie les charges de travail spécifiques et leurs interactions avec les groupes.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-256">The following sections take a more in-depth look at the specific workloads and their interactions with groups.</span></span>

## <a name="azure-ad"></a><span data-ttu-id="ca8d9-257">Azure AD</span><span class="sxs-lookup"><span data-stu-id="ca8d9-257">Azure AD</span></span>

<span data-ttu-id="ca8d9-258">Azure AD fournit les fonctionnalités de gestion des identités sous-jacentes Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-258">Azure AD provides the underlying identity management capabilities across Microsoft 365.</span></span>

<span data-ttu-id="ca8d9-259">**Fonctionnalités clés fournies aux groupes**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-259">**Key features provided to Groups**</span></span>

- <span data-ttu-id="ca8d9-260">Appartenance aux groupes</span><span class="sxs-lookup"><span data-stu-id="ca8d9-260">Group membership</span></span>
- <span data-ttu-id="ca8d9-261">Stratégie d’attribution de noms</span><span class="sxs-lookup"><span data-stu-id="ca8d9-261">Naming policy</span></span>
- <span data-ttu-id="ca8d9-262">Stratégie d’expiration</span><span class="sxs-lookup"><span data-stu-id="ca8d9-262">Expiration policy</span></span>
- <span data-ttu-id="ca8d9-263">Invités</span><span class="sxs-lookup"><span data-stu-id="ca8d9-263">Guests</span></span>
- <span data-ttu-id="ca8d9-264">Restriction de création de groupes</span><span class="sxs-lookup"><span data-stu-id="ca8d9-264">Restriction of Group creation</span></span>

<span data-ttu-id="ca8d9-265">**Azure AD peut-il créer un groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-265">**Can Azure AD create a Group?**</span></span>

<span data-ttu-id="ca8d9-266">Oui, Microsoft 365 groupes peuvent être créés à partir d’Azure AD via le portail web d’administration, via PowerShell ou Graph API.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-266">Yes, Microsoft 365 Groups can be created from Azure AD either through the administration web portal, through PowerShell, or Graph API.</span></span>

<span data-ttu-id="ca8d9-267">**Azure AD existe-t-il sans groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-267">**Does Azure AD exist without a group?**</span></span>

<span data-ttu-id="ca8d9-268">Oui, Azure AD effectue un grand nombre de services qui n’ont aucune relation avec Microsoft 365 groupes.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-268">Yes, Azure AD performs a great number of services that have no relation to Microsoft 365 Groups.</span></span> <span data-ttu-id="ca8d9-269">Chaque Microsoft 365 groupe est représenté en tant qu’objet dans Azure AD.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-269">Each Microsoft 365 group is represented as an object in Azure AD.</span></span>

<span data-ttu-id="ca8d9-270">**Existe-t-il plusieurs instances d’Azure AD par groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-270">**Can there be multiple instances of Azure AD per Group?**</span></span>

<span data-ttu-id="ca8d9-271">Non, il n’existe qu’une seule instance d’Azure AD.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-271">No, there is only one instance of Azure AD.</span></span>

<span data-ttu-id="ca8d9-272">**Azure AD peut-il être associé à plusieurs groupes ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-272">**Can Azure AD be associated with multiple Groups?**</span></span>

<span data-ttu-id="ca8d9-273">Oui, car Azure AD est la plateforme sous-jacente qui fournit le service d’appartenance au groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-273">Yes, because Azure AD is the underlying platform that provides the group membership service.</span></span>

<span data-ttu-id="ca8d9-274">**L’association d’Azure AD à un groupe peut-elle changer ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-274">**Can Azure AD’s association with a group change?**</span></span>

<span data-ttu-id="ca8d9-275">Non, Azure AD est la plateforme sous-jacente où les groupes existent.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-275">No, Azure AD is the underlying platform where groups exist.</span></span>

<span data-ttu-id="ca8d9-276">**La suppression de l’instance supprime-t-elle le groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-276">**Does deleting the instance delete the Group?**</span></span>

<span data-ttu-id="ca8d9-277">La suppression du groupe dans Azure AD supprime les services et le contenu associés au groupe appropriés.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-277">Deleting the group in Azure AD will delete relevant group-associated services and content.</span></span>

## <a name="teams"></a><span data-ttu-id="ca8d9-278">Teams</span><span class="sxs-lookup"><span data-stu-id="ca8d9-278">Teams</span></span>

<span data-ttu-id="ca8d9-279">Teams est un espace de travail centré sur la conversation visant à améliorer la collaboration en fournissant une interface unique permettant d’interagir avec divers services Microsoft et tiers.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-279">Teams is a chat-centered workspace aimed at enhancing collaboration by providing a singular interface to interact with a variety of Microsoft and third-party services.</span></span>

<span data-ttu-id="ca8d9-280">Par défaut, lorsqu’une équipe est créée, la boîte aux lettres et le calendrier associés au groupe Microsoft 365 sont masqués à la fois dans la liste d’adresses globale dans Exchange, ainsi que dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-280">By default, when a team is created, the mailbox and calendar associated with the Microsoft 365 group are hidden from both the Global Address List in Exchange, as well as Outlook.</span></span> <span data-ttu-id="ca8d9-281">Un administrateur peut le faire manuellement si l’utilisateur souhaite utiliser à la fois Outlook et Teams sur le même groupe Microsoft 365 client.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-281">This can be manually overridden by an administrator if the user would like to use both Outlook and Teams on the same Microsoft 365 Group.</span></span>

<span data-ttu-id="ca8d9-282">**Fonctionnalités clés fournies aux groupes**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-282">**Key features provided to Groups**</span></span>

- <span data-ttu-id="ca8d9-283">Conversations</span><span class="sxs-lookup"><span data-stu-id="ca8d9-283">Conversations</span></span>
- <span data-ttu-id="ca8d9-284">Onglets & canaux</span><span class="sxs-lookup"><span data-stu-id="ca8d9-284">Channels & tabs</span></span>
- <span data-ttu-id="ca8d9-285">Réunions</span><span class="sxs-lookup"><span data-stu-id="ca8d9-285">Meetings</span></span>

<span data-ttu-id="ca8d9-286">**Pouvez Teams créer un groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-286">**Can Teams create a group?**</span></span>

<span data-ttu-id="ca8d9-287">Oui, la création d’une équipe crée un groupe Microsoft 365 groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-287">Yes, creating a new team will create a new Microsoft 365 group.</span></span> <span data-ttu-id="ca8d9-288">Il est également possible de créer une équipe pour un groupe existant qui n’en possède pas actuellement.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-288">It is also possible to create a team for an existing group that does not currently have one.</span></span>

<span data-ttu-id="ca8d9-289">**Les équipes existent-elles sans groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-289">**Do teams exist without a group?**</span></span>

<span data-ttu-id="ca8d9-290">Non, il n’est pas possible qu’une équipe existe sans groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-290">No, it is not possible for a team to exist without a Group.</span></span>

<span data-ttu-id="ca8d9-291">**Peut-il y avoir plusieurs équipes par groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-291">**Can there be multiple teams per group?**</span></span>

<span data-ttu-id="ca8d9-292">Non, la relation entre une équipe et un groupe est 1:1.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-292">No, the relationship between a team and a group is 1:1.</span></span>

<span data-ttu-id="ca8d9-293">**Une équipe peut-elle être associée à plusieurs groupes ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-293">**Can a team be associated with multiple groups?**</span></span>

<span data-ttu-id="ca8d9-294">Non, l’équipe elle-même ne peut être associée qu’à un seul groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-294">No, the team itself can only be associated with a single group.</span></span>

<span data-ttu-id="ca8d9-295">**L’association d’une équipe à un groupe peut-elle changer ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-295">**Can a team’s association with a group change?**</span></span>

<span data-ttu-id="ca8d9-296">Non, l’équipe ne peut être associée qu’au groupe auquel elle a été initialement associée.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-296">No, the team can only ever be associated with the group to which it was originally associated.</span></span>

<span data-ttu-id="ca8d9-297">**La suppression de l’équipe supprime-t-elle le groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-297">**Does deleting the team delete the group?**</span></span>

<span data-ttu-id="ca8d9-298">Oui, la suppression de l’équipe dans Microsoft Teams supprimera le groupe, les services associés au groupe et le contenu.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-298">Yes, deleting the team in Microsoft Teams will delete the group, group-associated services, and content.</span></span>

## <a name="exchange"></a><span data-ttu-id="ca8d9-299">Exchange</span><span class="sxs-lookup"><span data-stu-id="ca8d9-299">Exchange</span></span>

<span data-ttu-id="ca8d9-300">Exchange Online la messagerie, le calendrier, les contacts et les fonctionnalités associées.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-300">Exchange Online provides messaging, calendar, contact, and associated functionality.</span></span> <span data-ttu-id="ca8d9-301">Dans le contexte d’un groupe, une seule ressource est associée, par opposition à une instance de service entière.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-301">In the context of a Group, only a single resource is associated – as opposed to an entire service instance.</span></span>

<span data-ttu-id="ca8d9-302">**Fonctionnalités clés fournies aux groupes**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-302">**Key features provided to Groups**</span></span>

- <span data-ttu-id="ca8d9-303">Boîte aux lettres et calendrier</span><span class="sxs-lookup"><span data-stu-id="ca8d9-303">Mailbox and calendar</span></span>
- <span data-ttu-id="ca8d9-304">Possibilité d’envoyer un e-mail à tous les membres du groupe</span><span class="sxs-lookup"><span data-stu-id="ca8d9-304">Ability to email all Group members</span></span>
- <span data-ttu-id="ca8d9-305">Stockage des conversations Teams canal à des fins eDiscovery, commentaires du Planificateur</span><span class="sxs-lookup"><span data-stu-id="ca8d9-305">Storage of Teams channel conversations for eDiscovery purposes, Planner comments</span></span>

<span data-ttu-id="ca8d9-306">**Pouvez Exchange créer un groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-306">**Can Exchange create a group?**</span></span>

<span data-ttu-id="ca8d9-307">Oui, il est possible de créer un groupe à partir du centre d’administration Exchange Online, ainsi que de Outlook.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-307">Yes, it is possible to create a group from the Exchange Online admin center, as well as from Outlook.</span></span> <span data-ttu-id="ca8d9-308">Vous pouvez également convertir des listes Exchange distribution en listes Microsoft 365 groupes.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-308">You can also convert Exchange distribution lists to Microsoft 365 groups.</span></span>

<span data-ttu-id="ca8d9-309">**Existe-Exchange existe-t-il sans groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-309">**Does Exchange exist without a Group?**</span></span>

<span data-ttu-id="ca8d9-310">Oui, Exchange Online fournit un certain nombre de services, y compris des boîtes aux lettres et des calendriers partagés, sans association de groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-310">Yes, Exchange Online provides a number of services, including shared mailboxes and calendars, without any group association.</span></span>

<span data-ttu-id="ca8d9-311">**Peut-il y avoir plusieurs instances de boîtes Exchange ou de calendriers par groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-311">**Can there be multiple instances of Exchange mailboxes or calendars per group?**</span></span>

<span data-ttu-id="ca8d9-312">Non, il ne peut y avoir qu’un seul Exchange Online boîte aux lettres et un calendrier pour un groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-312">No, there can only be a single Exchange Online mailbox and calendar for a group.</span></span>

<span data-ttu-id="ca8d9-313">**Les Exchange boîtes aux lettres et les calendriers peuvent-ils être associés à plusieurs groupes ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-313">**Can Exchange mailboxes and calendars be associated with multiple groups?**</span></span>

<span data-ttu-id="ca8d9-314">Non, la boîte aux lettres et le calendrier ont une relation 1:1 avec le groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-314">No, the mailbox and calendar have a 1:1 relationship with the group.</span></span> <span data-ttu-id="ca8d9-315">Il est possible de partager la boîte aux lettres avec d’autres utilisateurs ou groupes, mais cela n’établit aucune forme d’association de service.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-315">It is possible to share the mailbox with other users or groups, however this does not establish any form of service association.</span></span>

<span data-ttu-id="ca8d9-316">**L’association Exchange boîte aux lettres ou du calendrier à un groupe peut-elle changer ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-316">**Can the Exchange mailbox or calendar’s association with a group change?**</span></span>

<span data-ttu-id="ca8d9-317">Non, la boîte aux lettres et le calendrier ne peuvent pas être modifiés dans un autre groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-317">No, the mailbox and calendar   cannot be changed to a different group.</span></span> <span data-ttu-id="ca8d9-318">Toutefois, le contenu peut être déplacé d’une boîte aux lettres à une autre au sein Outlook ou à l’aide d’un outil tiers.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-318">However, the content can be moved from one mailbox to another within Outlook or by using a third-party tool.</span></span>

<span data-ttu-id="ca8d9-319">**La suppression de la boîte aux lettres supprime-t-elle le groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-319">**Does deleting the mailbox delete the group?**</span></span>

<span data-ttu-id="ca8d9-320">Oui, la suppression de la boîte aux lettres dans Exchange supprimera le groupe, ainsi que les services et le contenu associés au groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-320">Yes, deleting the mailbox in Exchange will delete the group as well as group-associated services and content.</span></span>

## <a name="forms"></a><span data-ttu-id="ca8d9-321">Formulaires</span><span class="sxs-lookup"><span data-stu-id="ca8d9-321">Forms</span></span>

<span data-ttu-id="ca8d9-322">Les formulaires fournissent des questionnaires et des enquêtes web.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-322">Forms provides web-based surveys and quizzes.</span></span>

<span data-ttu-id="ca8d9-323">**Fonctionnalités clés fournies aux groupes**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-323">**Key features provided to groups**</span></span>

- <span data-ttu-id="ca8d9-324">Propriété des formulaires</span><span class="sxs-lookup"><span data-stu-id="ca8d9-324">Ownership of forms</span></span>

<span data-ttu-id="ca8d9-325">**Les formulaires peuvent-ils créer un groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-325">**Can Forms create a group?**</span></span>

<span data-ttu-id="ca8d9-326">Non, les formulaires ne peuvent pas créer de groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-326">No, Forms cannot create a group.</span></span>

<span data-ttu-id="ca8d9-327">**Les formulaires existent-ils sans groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-327">**Do forms exist without a group?**</span></span>

<span data-ttu-id="ca8d9-328">Oui, les enquêtes et les questionnaires peuvent être créés directement dans le compte d’un utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-328">Yes, surveys and quizzes can be created directly in an end-user’s account.</span></span>

<span data-ttu-id="ca8d9-329">**Y a-t-il plusieurs formulaires par groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-329">**Can there be multiple forms per group?**</span></span>

<span data-ttu-id="ca8d9-330">Oui, plusieurs formulaires peuvent être associés à un groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-330">Yes, there can be multiple forms associated with a group.</span></span>

<span data-ttu-id="ca8d9-331">**Les formulaires peuvent-ils être associés à plusieurs groupes ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-331">**Can forms be associated with multiple groups?**</span></span>

<span data-ttu-id="ca8d9-332">Non, un formulaire ne peut être associé qu’à un seul groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-332">No, a form can only be associated with a single group.</span></span>

<span data-ttu-id="ca8d9-333">**L’association d’un formulaire à un groupe peut-elle changer ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-333">**Can a form’s association with a group change?**</span></span>

<span data-ttu-id="ca8d9-334">Non, une fois qu’un formulaire est associé à un groupe (créé directement dans ou propriété transférée à partir d’un individu), il ne peut pas être déplacé vers un autre groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-334">No, once a form is associated with a group (either created directly within, or ownership transferred from an individual) it cannot be moved to another group.</span></span>

<span data-ttu-id="ca8d9-335">**La suppression du formulaire supprime-t-elle le groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-335">**Does deleting the form delete the group?**</span></span>

<span data-ttu-id="ca8d9-336">Non, il n’est pas possible de supprimer un groupe de l’interface Forms, uniquement des formulaires individuels.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-336">No, it is not possible to delete a group from the Forms interface, only individual forms.</span></span>

## <a name="onenote"></a><span data-ttu-id="ca8d9-337">OneNote</span><span class="sxs-lookup"><span data-stu-id="ca8d9-337">OneNote</span></span>

<span data-ttu-id="ca8d9-338">OneNote est une application de bloc-notes numérique.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-338">OneNote is a digital notebook application.</span></span> <span data-ttu-id="ca8d9-339">Le OneNote bloc-notes créé avec un groupe est un fichier dans le site SharePoint associé plutôt qu’un service connecté à un groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-339">The OneNote notebook created with a group is a file in the associated SharePoint site rather than a group-connected service.</span></span>

<span data-ttu-id="ca8d9-340">**Fonctionnalités clés fournies aux groupes**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-340">**Key features provided to groups**</span></span>

- <span data-ttu-id="ca8d9-341">Bloc-notes partagé (stocké dans la bibliothèque de SharePoint associée au groupe)</span><span class="sxs-lookup"><span data-stu-id="ca8d9-341">Shared notebook (stored in the Group-associated SharePoint library)</span></span>

<span data-ttu-id="ca8d9-342">**Pouvez OneNote créer un groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-342">**Can OneNote create a group?**</span></span>

<span data-ttu-id="ca8d9-343">Non, l’application OneNote ne peut pas créer de groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-343">No, the OneNote application cannot create a group.</span></span>

<span data-ttu-id="ca8d9-344">**Existe-OneNote blocs-notes sans groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-344">**Do OneNote notebooks exist without a group?**</span></span>

<span data-ttu-id="ca8d9-345">Oui, les blocs-notes peuvent être créés directement dans OneDrive ou dans d’autres emplacements partagés.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-345">Yes, notebooks can be created directly in OneDrive or in other shared locations.</span></span>

<span data-ttu-id="ca8d9-346">**Peut-il y avoir plusieurs blocs-OneNote par groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-346">**Can there be multiple OneNote notebooks per group?**</span></span>

<span data-ttu-id="ca8d9-347">Oui, un bloc-notes est créé par défaut et d’autres peuvent être ajoutés, mais n’importe quel lien vers OneNote à partir des services associés à un groupe sera toujours vers le bloc-notes par défaut.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-347">Yes, a notebook is created by default and others can be added, however any link to OneNote from group-associated services will always go to the default notebook.</span></span>

<span data-ttu-id="ca8d9-348">**Un bloc-OneNote peut-il être associé à plusieurs groupes ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-348">**Can a OneNote notebook be associated with multiple groups?**</span></span>

<span data-ttu-id="ca8d9-349">Non, le bloc-notes est stocké dans la bibliothèque SharePoint de sites associée au groupe et lié à partir de différentes interfaces.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-349">No, the notebook is stored in the group-associated SharePoint site library and linked from various interfaces.</span></span> <span data-ttu-id="ca8d9-350">Il peut toutefois être partagé avec d’autres groupes de la même manière qu’avec des individus.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-350">It can however be shared with other Groups in the same way it can be shared with individuals.</span></span>

<span data-ttu-id="ca8d9-351">**L’association du bloc-notes à un groupe peut-elle changer ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-351">**Can the notebook’s association with a group change?**</span></span>

<span data-ttu-id="ca8d9-352">Non, le bloc-notes lui-même est associé au groupe et est directement accessible à partir d’autres services connectés à un groupe, mais le contenu peut être déplacé d’un bloc-notes à un autre au sein de l’application OneNote.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-352">No, the notebook itself is associated with the group and can be directly accessed from other group-connected services, however the content can be moved from one notebook to another within the OneNote application.</span></span>

<span data-ttu-id="ca8d9-353">**La suppression du bloc-notes supprime-t-elle le groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-353">**Does deleting the notebook delete the group?**</span></span>

<span data-ttu-id="ca8d9-354">Non, toutefois, si OneNote bloc-notes est supprimé, il se peut que des liens rompus soient rompus dans certains services associés à un groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-354">No, however if the OneNote notebook is deleted there may be broken links in some of the group-associated services.</span></span>

## <a name="planner"></a><span data-ttu-id="ca8d9-355">Planificateur</span><span class="sxs-lookup"><span data-stu-id="ca8d9-355">Planner</span></span>

<span data-ttu-id="ca8d9-356">Le Planificateur est un service de gestion des tâches de groupe léger.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-356">Planner is a lightweight  group task management service.</span></span>

<span data-ttu-id="ca8d9-357">**Fonctionnalités clés fournies aux groupes**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-357">**Key features provided to groups**</span></span>

- <span data-ttu-id="ca8d9-358">Tableau de gestion des tâches de groupe</span><span class="sxs-lookup"><span data-stu-id="ca8d9-358">Board for managing group tasks</span></span>

<span data-ttu-id="ca8d9-359">**Le Planificateur peut-il créer un groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-359">**Can Planner create a group?**</span></span>

<span data-ttu-id="ca8d9-360">Oui, la création d’un plan crée un groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-360">Yes, creation of a plan will create a new group.</span></span>

<span data-ttu-id="ca8d9-361">**Existe-t-il un tableau du Planificateur sans groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-361">**Does a Planner board exist without a group?**</span></span>

<span data-ttu-id="ca8d9-362">Non, un plan doit être associé à un groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-362">No, a plan must be associated with a group.</span></span>

<span data-ttu-id="ca8d9-363">**Existe-t-il plusieurs plans par groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-363">**Can there be multiple plans per group?**</span></span>

<span data-ttu-id="ca8d9-364">Oui, il peut y avoir plusieurs plans par groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-364">Yes, there can be multiple plans per group.</span></span>

<span data-ttu-id="ca8d9-365">**Un plan peut-il être associé à plusieurs groupes ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-365">**Can a plan be associated with multiple groups?**</span></span>

<span data-ttu-id="ca8d9-366">Non, un plan s’appuie uniquement sur l’appartenance au groupe pour déterminer l’accès.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-366">No, a plan relies solely on the group membership to determine access.</span></span>

<span data-ttu-id="ca8d9-367">**L’association d’un plan à un groupe peut-elle changer ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-367">**Can a plan’s association with a group change?**</span></span>

<span data-ttu-id="ca8d9-368">Non, toutefois, la copie d’un plan crée un groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-368">No, however copying a plan creates a new group.</span></span>

> [!NOTE]
> <span data-ttu-id="ca8d9-369">Un groupe créé par une autre application ne s’affiche pas automatiquement dans le Planificateur pour un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-369">A Group created by any other application will not show up in Planner automatically for a user.</span></span> <span data-ttu-id="ca8d9-370">Pour accéder au tableau initialement, ils devront l’ouvrir à partir d’une autre interface basée sur un groupe telle que Outlook.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-370">To access the board initially they will need to open it from another Group-based interface such as Outlook.</span></span>

<span data-ttu-id="ca8d9-371">**La suppression du plan supprime-t-elle le groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-371">**Does deleting the plan delete the group?**</span></span>

<span data-ttu-id="ca8d9-372">Oui, la suppression du plan supprimera les services et le contenu associés au groupe et au groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-372">Yes, deleting the plan will delete the group and group-associated services and content.</span></span>

## <a name="power-apps"></a><span data-ttu-id="ca8d9-373">Power Apps</span><span class="sxs-lookup"><span data-stu-id="ca8d9-373">Power Apps</span></span>

<span data-ttu-id="ca8d9-374">Power Apps fournit un canevas pour le développement d’applications sans code.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-374">Power Apps provides a canvas for app development without code.</span></span>

<span data-ttu-id="ca8d9-375">**Fonctionnalités clés fournies aux groupes**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-375">**Key features provided to Groups**</span></span>

- <span data-ttu-id="ca8d9-376">Les applications peuvent être partagées avec un groupe à exécuter et à modifier</span><span class="sxs-lookup"><span data-stu-id="ca8d9-376">Apps can be shared with a group to be run and modified</span></span>

<span data-ttu-id="ca8d9-377">**Pouvez Power Apps créer un groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-377">**Can Power Apps create a group?**</span></span>

<span data-ttu-id="ca8d9-378">Non, Power Apps ne peut pas créer Microsoft 365 groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-378">No, Power Apps cannot create a Microsoft 365 group.</span></span>

<span data-ttu-id="ca8d9-379">**N Power Apps existe-t-il pas de groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-379">**Do Power Apps exist without a group?**</span></span>

<span data-ttu-id="ca8d9-380">Oui, les applications peuvent être créées au sein Power Apps et résident dans le compte créateurs jusqu’à ce qu’elles soient partagées ou publiées.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-380">Yes, apps can be created within Power Apps and reside within the creators account until shared or published.</span></span>

<span data-ttu-id="ca8d9-381">**Y a-t-il plusieurs applications par groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-381">**Can there be multiple apps per group?**</span></span>

<span data-ttu-id="ca8d9-382">Oui, il peut y avoir plusieurs applications partagées avec un groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-382">Yes, there can be multiple apps shared with a group.</span></span>

<span data-ttu-id="ca8d9-383">**Les applications peuvent-ils être associées à plusieurs groupes ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-383">**Can apps be associated with multiple groups?**</span></span>

<span data-ttu-id="ca8d9-384">Oui, une application peut être partagée avec plusieurs groupes.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-384">Yes, an app can be shared with multiple groups.</span></span>

<span data-ttu-id="ca8d9-385">**L’association d’une application à un groupe peut-elle changer ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-385">**Can an app’s association with a group change?**</span></span>

<span data-ttu-id="ca8d9-386">Oui, car l’association entre Power Apps et un groupe Microsoft 365 partage uniquement : l’application réside toujours avec le créateur.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-386">Yes, as the association between Power Apps and a Microsoft 365 group is sharing only – the app still resides with the creator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ca8d9-387">[La sécurité des groupes doit être activée pour que les applications soient partagées avec eux.](/powerapps/maker/canvas-apps/share-app#share-an-app-with-office-365-groups)</span><span class="sxs-lookup"><span data-stu-id="ca8d9-387">[Groups must be security enabled before apps can be shared with them](/powerapps/maker/canvas-apps/share-app#share-an-app-with-office-365-groups).</span></span>

<span data-ttu-id="ca8d9-388">**La suppression de l’application supprime-t-elle le groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-388">**Does deleting the app delete the group?**</span></span>

<span data-ttu-id="ca8d9-389">Non, les applications ne sont pas connectées au groupe autrement que d’être partagées avec eux.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-389">No, the apps are not connected to the group other than being shared with them.</span></span>

## <a name="power-automate"></a><span data-ttu-id="ca8d9-390">Power Automate</span><span class="sxs-lookup"><span data-stu-id="ca8d9-390">Power Automate</span></span>

<span data-ttu-id="ca8d9-391">Power Automate (anciennement appelé Microsoft Flow) fournit des flux de travail et des services d’automatisation.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-391">Power Automate (formerly known as Microsoft Flow) provides workflows and automation services.</span></span>

<span data-ttu-id="ca8d9-392">**Fonctionnalités clés fournies aux groupes**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-392">**Key features provided to groups**</span></span>

- <span data-ttu-id="ca8d9-393">Les flux de travail peuvent être partagés avec un groupe à exécuter et à modifier.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-393">Workflows can be shared with a group to be run and modified.</span></span>

<span data-ttu-id="ca8d9-394">**Pouvez Power Automate créer un groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-394">**Can Power Automate create a group?**</span></span>

<span data-ttu-id="ca8d9-395">Non, Power Automate ne peut pas créer Microsoft 365 groupe dans le contexte d’être associé à un groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-395">No, Power Automate cannot create a Microsoft 365 group in the context of being associated with one.</span></span>

<span data-ttu-id="ca8d9-396">Toutefois, il est possible de créer un flux qui effectue diverses opérations, telles que la création d’un groupe de sécurité Azure AD ou la mise à jour de l’appartenance à un Microsoft 365 groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-396">It is possible however to create a flow that performs various operations such as creating an Azure AD security group or updating membership of a Microsoft 365 group.</span></span>

<span data-ttu-id="ca8d9-397">**Existe-t-il des flux sans groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-397">**Do flows exist without a group?**</span></span>

<span data-ttu-id="ca8d9-398">Oui, les flux peuvent être créés au sein Power Automate et résider dans le compte créateurs jusqu’à ce qu’ils soient partagés ou publiés.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-398">Yes, flows can be created within Power Automate and reside within the creators account until shared or published.</span></span>

<span data-ttu-id="ca8d9-399">**Peut-il y avoir plusieurs flux par groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-399">**Can there be multiple flows per group?**</span></span>

<span data-ttu-id="ca8d9-400">Oui, il peut y avoir plusieurs flux partagés avec un groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-400">Yes, there can be multiple flows shared with a group.</span></span>

<span data-ttu-id="ca8d9-401">**Un flux peut-il être associé à plusieurs groupes ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-401">**Can a flow be associated with multiple groups?**</span></span>

<span data-ttu-id="ca8d9-402">Oui, un flux peut être partagé avec plusieurs groupes.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-402">Yes, a flow can be shared with multiple groups.</span></span>

<span data-ttu-id="ca8d9-403">**L’association d’un flux à un groupe peut-elle changer ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-403">**Can a flow’s association with a group change?**</span></span>

<span data-ttu-id="ca8d9-404">Oui, car l’association entre Power Automate et un groupe Microsoft 365 partage uniquement : le flux réside toujours avec le créateur.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-404">Yes, as the association between Power Automate and a Microsoft 365 group is sharing only – the flow still resides with the creator.</span></span>

<span data-ttu-id="ca8d9-405">**La suppression d’un flux supprime-t-elle le groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-405">**Does deleting a flow delete the group?**</span></span>

<span data-ttu-id="ca8d9-406">Non, comme Power Apps, les flux ne sont pas connectés au groupe autrement que d’être partagés avec eux.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-406">No, like Power Apps, the flows are not connected to the group other than being shared with them.</span></span>

## <a name="power-bi-classic"></a><span data-ttu-id="ca8d9-407">Power BI (classique)</span><span class="sxs-lookup"><span data-stu-id="ca8d9-407">Power BI (classic)</span></span>

<span data-ttu-id="ca8d9-408">Power BI fournit des rapports et des tableaux de bord interactifs pilotés par des données.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-408">Power BI provides interactive data-driven dashboards and reports.</span></span>

<span data-ttu-id="ca8d9-409">**Fonctionnalités clés fournies aux groupes**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-409">**Key features provided to groups**</span></span>

- <span data-ttu-id="ca8d9-410">Rapports de données</span><span class="sxs-lookup"><span data-stu-id="ca8d9-410">Data reporting</span></span>

<span data-ttu-id="ca8d9-411">**Pouvez Power BI créer un groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-411">**Can Power BI create a group?**</span></span>

<span data-ttu-id="ca8d9-412">Oui, la création d’un espace de travail classique crée un Microsoft 365 groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-412">Yes, creating a classic workspace will create a Microsoft 365 group.</span></span>

<span data-ttu-id="ca8d9-413">**Existe-t-Power BI un espace de travail classique sans groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-413">**Does a Power BI classic workspace exist without a group?**</span></span>

<span data-ttu-id="ca8d9-414">Non, [un espace de travail classique dans Power BI doit être associé à un groupe.](/power-bi/collaborate-share/service-collaborate-power-bi-workspace)</span><span class="sxs-lookup"><span data-stu-id="ca8d9-414">No, [a classic workspace in Power BI must be associated with a group](/power-bi/collaborate-share/service-collaborate-power-bi-workspace).</span></span>

<span data-ttu-id="ca8d9-415">**Peut-il y avoir plusieurs Power BI de travail par groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-415">**Can there be multiple Power BI workspaces per group?**</span></span>

<span data-ttu-id="ca8d9-416">Non, la relation entre un espace de travail classique et un groupe est 1:1.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-416">No, the relationship between a classic workspace and a group is 1:1.</span></span>

<span data-ttu-id="ca8d9-417">**Un espace de travail peut-il être associé à plusieurs groupes ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-417">**Can a workspace be associated with multiple groups?**</span></span>

<span data-ttu-id="ca8d9-418">Techniquement non, alors que l’espace de travail classique est créé avec le groupe, le contenu peut être partagé en dehors du groupe avec des utilisateurs et des groupes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-418">Technically no, while the classic workspace is created with the group, the content can be shared outside of the Group with users and security groups.</span></span>

<span data-ttu-id="ca8d9-419">**L’association de l’espace de travail à un groupe peut-elle changer ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-419">**Can the workspace's association with a group change?**</span></span>

<span data-ttu-id="ca8d9-420">Non, l’espace de travail classique lui-même est associé au groupe, mais le contenu peut être déplacé d’un espace de travail à un autre au sein de l’interface Power BI ou en exportant du contenu localement.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-420">No, the classic workspace itself is associated with the Group, however the content can be moved from one workspace to another within the Power BI interface or by exporting contents locally.</span></span>

<span data-ttu-id="ca8d9-421">**La suppression de l’espace de travail supprime-t-elle le groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-421">**Does deleting the workspace delete the group?**</span></span>

<span data-ttu-id="ca8d9-422">Oui, la suppression de l’espace de travail Power BI supprimera le contenu et les services associés aux groupes.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-422">Yes, deleting the workspace in Power BI will delete group and  group-associated services and content.</span></span>

## <a name="power-bi-new"></a><span data-ttu-id="ca8d9-423">Power BI (nouveau)</span><span class="sxs-lookup"><span data-stu-id="ca8d9-423">Power BI (new)</span></span>

<span data-ttu-id="ca8d9-424">Power BI fournit des rapports et des tableaux de bord interactifs pilotés par des données.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-424">Power BI provides interactive data-driven dashboards and reports.</span></span>

<span data-ttu-id="ca8d9-425">Bien que la création d’un espace de travail dans Power BI ne crée pas de groupe Microsoft 365, la création d’un groupe par d’autres moyens crée un nouvel espace de travail (et non classique) dans Power BI.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-425">While creating a new workspace in Power BI does not create a Microsoft 365 Group, creating a group by any other means creates a  new (not classic) workspace in Power BI.</span></span>

<span data-ttu-id="ca8d9-426">**Fonctionnalités clés fournies aux groupes**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-426">**Key features provided to groups**</span></span>

- <span data-ttu-id="ca8d9-427">Rapports de données</span><span class="sxs-lookup"><span data-stu-id="ca8d9-427">Data reporting</span></span>

<span data-ttu-id="ca8d9-428">**Pouvez Power BI créer un groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-428">**Can Power BI create a group?**</span></span>

<span data-ttu-id="ca8d9-429">Non, il n’est pas possible de créer un groupe Microsoft 365 à partir de la nouvelle interface Power BI’interface.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-429">No, it is not possible to create a Microsoft 365 group from the new Power BI interface.</span></span>

<span data-ttu-id="ca8d9-430">**Le nouvel espace Power BI de travail existe-t-il sans groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-430">**Does the new Power BI workspace exist without a group?**</span></span>

<span data-ttu-id="ca8d9-431">Oui, il est possible de créer des rapports et des espaces de travail dans des Power BI qui ne sont pas associés à Microsoft 365 groupes.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-431">Yes, it is possible to have reports and workspaces created in Power BI that are not associated with Microsoft 365 groups.</span></span>

<span data-ttu-id="ca8d9-432">**Peut-il y avoir plusieurs espaces de travail par groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-432">**Can there be multiple workspaces per group?**</span></span>

<span data-ttu-id="ca8d9-433">Oui, [plusieurs espaces de travail créés par Power BI peuvent être partagés avec un seul groupe.](/power-bi/collaborate-share/service-create-the-new-workspaces#give-access-to-your-workspace)</span><span class="sxs-lookup"><span data-stu-id="ca8d9-433">Yes, [multiple workspaces created by Power BI can be shared with a single group](/power-bi/collaborate-share/service-create-the-new-workspaces#give-access-to-your-workspace).</span></span>

<span data-ttu-id="ca8d9-434">**Un espace de travail peut-il être associé à plusieurs groupes ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-434">**Can a workspace be associated with multiple groups?**</span></span>

<span data-ttu-id="ca8d9-435">Non, un espace de travail créé par Power BI ne peut être associé qu’à un seul groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-435">No, a workspace created by Power BI can only be associated with a single group.</span></span>

<span data-ttu-id="ca8d9-436">**L’association d’un espace de travail à un groupe peut-elle changer ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-436">**Can a workspace's association with a group change?**</span></span>

<span data-ttu-id="ca8d9-437">Oui et non.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-437">Yes and no.</span></span> <span data-ttu-id="ca8d9-438">Un espace de travail créé par Power BI ne peut être associé qu’à un seul groupe à la fois, mais peut modifier l’association à tout moment.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-438">A workspace created by Power BI can only be associated with a single group at a time but can change the association at any time.</span></span> <span data-ttu-id="ca8d9-439">Un espace de travail créé dans Power BI par un groupe est associé définitivement à ce groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-439">A workspace created in Power BI by a group is permanently associated to that group.</span></span>

<span data-ttu-id="ca8d9-440">**La suppression de l’espace de travail supprime-t-elle le groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-440">**Does deleting the workspace delete the group?**</span></span>

<span data-ttu-id="ca8d9-441">Oui, la suppression de l’espace de travail Power BI supprimera le contenu et les services associés au groupe et au groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-441">Yes, deleting the workspace in Power BI will delete the group and group-associated services and content.</span></span>

## <a name="project-for-the-web"></a><span data-ttu-id="ca8d9-442">Project for the web</span><span class="sxs-lookup"><span data-stu-id="ca8d9-442">Project for the web</span></span>

<span data-ttu-id="ca8d9-443">Project web offre la possibilité de créer des plans de projet, des diagrammes de Gantt et des feuilles de route.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-443">Project for the web offers the ability to create project plans, Gantt charts, and roadmaps.</span></span>
<span data-ttu-id="ca8d9-444">Fonctionnalités clés fournies aux groupes.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-444">Key features provided to groups.</span></span>

- <span data-ttu-id="ca8d9-445">Project plans</span><span class="sxs-lookup"><span data-stu-id="ca8d9-445">Project plans</span></span>

<span data-ttu-id="ca8d9-446">**Est-Project pour le web de créer un groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-446">**Can Project for the web create a group?**</span></span>

<span data-ttu-id="ca8d9-447">Oui, il est possible de créer un groupe de Microsoft 365 directement à partir Project pour le web.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-447">Yes, it is possible to create a new Microsoft 365 group directly from Project for the web.</span></span>

<span data-ttu-id="ca8d9-448">**Les projets existent-ils sans groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-448">**Do projects exist without a group?**</span></span>

<span data-ttu-id="ca8d9-449">Oui, les projets peuvent exister sans être associés à un groupe Microsoft 365, mais l’affectation de tâches nécessite une association de groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-449">Yes, projects can exist without being associated with a Microsoft 365 group, however assignment of tasks requires group association.</span></span>

<span data-ttu-id="ca8d9-450">**Peut-il y avoir plusieurs projets par groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-450">**Can there be multiple projects per group?**</span></span>

<span data-ttu-id="ca8d9-451">Oui, il est possible de connecter plusieurs projets dans un même groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-451">Yes, it is possible to connect multiple projects in a single group.</span></span>

<span data-ttu-id="ca8d9-452">**Le projet peut-il être associé à plusieurs groupes ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-452">**Can project be associated with multiple groups?**</span></span>

<span data-ttu-id="ca8d9-453">Non, un projet ne peut être associé qu’à un seul groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-453">No, a project can only be associated with a single group.</span></span>

<span data-ttu-id="ca8d9-454">**L’association d’un projet à un groupe peut-elle changer ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-454">**Can a project’s association with a group change?**</span></span>

<span data-ttu-id="ca8d9-455">Non, une fois l’association avec un groupe établie, elle ne peut pas changer.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-455">No, once the association with a group is established, it cannot change.</span></span>

<span data-ttu-id="ca8d9-456">**La suppression du projet supprime-t-elle le groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-456">**Does deleting the project delete the group?**</span></span>

<span data-ttu-id="ca8d9-457">Non, la suppression du projet dans Project web ne supprime pas le groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-457">No, deleting the project in Project for the web will not delete the group.</span></span>

## <a name="roadmap"></a><span data-ttu-id="ca8d9-458">Feuille de route</span><span class="sxs-lookup"><span data-stu-id="ca8d9-458">Roadmap</span></span>

<span data-ttu-id="ca8d9-459">La feuille de route offre la possibilité de créer des feuilles de route de projet Project pour le web et Project Online.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-459">Roadmap provides the ability to create project roadmaps with Project for the web and Project Online.</span></span>

<span data-ttu-id="ca8d9-460">**Fonctionnalités clés fournies aux groupes**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-460">**Key features provided to Groups**</span></span>

- <span data-ttu-id="ca8d9-461">Project feuilles de route</span><span class="sxs-lookup"><span data-stu-id="ca8d9-461">Project roadmaps</span></span>

<span data-ttu-id="ca8d9-462">**La feuille de route peut-elle créer un groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-462">**Can Roadmap create a group?**</span></span>

<span data-ttu-id="ca8d9-463">Oui, il est possible de créer un groupe de Microsoft 365 directement à partir de la feuille de route.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-463">Yes, it is possible to create a new Microsoft 365 group directly from roadmap.</span></span>

<span data-ttu-id="ca8d9-464">**La feuille de route existe-t-elle sans groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-464">**Does Roadmap exist without a group?**</span></span>

<span data-ttu-id="ca8d9-465">Oui, les feuilles de route peuvent exister sans être associées à un groupe Microsoft 365, mais le partage de la feuille de route nécessite une association de groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-465">Yes, roadmaps can exist without being associated with a Microsoft 365 group, however sharing the roadmap requires group association.</span></span>

<span data-ttu-id="ca8d9-466">**Peut-il y avoir plusieurs feuilles de route par groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-466">**Can there be multiple roadmaps per group?**</span></span>

<span data-ttu-id="ca8d9-467">Oui, il est possible de connecter plusieurs feuilles de route à un seul groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-467">Yes, it is possible to connect multiple roadmaps to a single group.</span></span>

<span data-ttu-id="ca8d9-468">**Une feuille de route peut-elle être associée à plusieurs groupes ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-468">**Can a roadmap be associated with multiple groups?**</span></span>

<span data-ttu-id="ca8d9-469">Non, une feuille de route ne peut être associée qu’à un seul groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-469">No, a roadmap can only be associated with a single group.</span></span>

<span data-ttu-id="ca8d9-470">**L’association d’une feuille de route à un groupe peut-elle changer ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-470">**Can a roadmap's association with a group change?**</span></span>

<span data-ttu-id="ca8d9-471">Non, une fois l’association avec un groupe établie, elle ne peut pas changer.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-471">No, once the association with a group is established, it cannot change.</span></span>

<span data-ttu-id="ca8d9-472">**La suppression de la feuille de route supprime-t-elle le groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-472">**Does deleting the roadmap delete the group?**</span></span>

<span data-ttu-id="ca8d9-473">Non, la suppression de la feuille de route ne supprime pas le groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-473">No, deleting the roadmap will not delete the group.</span></span>

## <a name="sharepoint"></a><span data-ttu-id="ca8d9-474">SharePoint</span><span class="sxs-lookup"><span data-stu-id="ca8d9-474">SharePoint</span></span>

<span data-ttu-id="ca8d9-475">SharePoint est une plateforme de gestion de contenu web qui fournit, entre autres, des services de stockage pour un certain nombre de services Microsoft 365 web.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-475">SharePoint is a web-based content management platform that provides among other things, storage services for a number of Microsoft 365 services.</span></span>

<span data-ttu-id="ca8d9-476">**Fonctionnalités clés fournies aux groupes**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-476">**Key features provided to Groups**</span></span>

- <span data-ttu-id="ca8d9-477">Bibliothèque de documents</span><span class="sxs-lookup"><span data-stu-id="ca8d9-477">Document library</span></span>
- <span data-ttu-id="ca8d9-478">Bibliothèque pour le stockage du bloc-OneNote portable</span><span class="sxs-lookup"><span data-stu-id="ca8d9-478">Library for storage of OneNote notebook</span></span>
- <span data-ttu-id="ca8d9-479">Stockage de Teams wiki</span><span class="sxs-lookup"><span data-stu-id="ca8d9-479">Storage of Teams wiki files</span></span>

<span data-ttu-id="ca8d9-480">**Pouvez SharePoint créer un groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-480">**Can SharePoint create a group?**</span></span>

<span data-ttu-id="ca8d9-481">Oui, la création d’un site d’équipe SharePoint créera un groupe Microsoft 365 par défaut.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-481">Yes, creating a team site in SharePoint will create a Microsoft 365 group by default.</span></span> <span data-ttu-id="ca8d9-482">Il est également possible de créer un groupe et, éventuellement, une équipe pour un site existant.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-482">It is also possible to create a group and, optionally, a team for an existing site.</span></span>

<span data-ttu-id="ca8d9-483">**Existe-SharePoint sites sans groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-483">**Do SharePoint sites exist without a group?**</span></span>

<span data-ttu-id="ca8d9-484">Oui, SharePoint offre un certain nombre de services et sites non associés à un groupe, tels que des sites de communication et de hub.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-484">Yes, SharePoint offers a number of non-group-associated services and sites such as communication and hub sites.</span></span> 

<span data-ttu-id="ca8d9-485">**Peut-il y avoir plusieurs sites par groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-485">**Can there be multiple sites per group?**</span></span>

<span data-ttu-id="ca8d9-486">Non, il ne peut y avoir qu’un seul site par groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-486">No, there can only be a single site per group.</span></span> <span data-ttu-id="ca8d9-487">Les canaux privés Teams utiliser des sites supplémentaires qui ne sont pas connectés au groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-487">Private channels in Teams use additional sites that are not connected to the group.</span></span>

<span data-ttu-id="ca8d9-488">**Les sites peuvent-ils être associés à plusieurs groupes ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-488">**Can sites be associated with multiple groups?**</span></span>

<span data-ttu-id="ca8d9-489">Techniquement non, mais pendant la création d’un site avec un groupe, le contenu peut être partagé avec d’autres groupes.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-489">Technically no, but while a site is created with a group, the content can be shared with other groups.</span></span>

<span data-ttu-id="ca8d9-490">**L’association d’un site à un groupe peut-elle changer ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-490">**Can a site’s association with a group change?**</span></span>

<span data-ttu-id="ca8d9-491">Non, le site lui-même est associé au groupe, mais le contenu peut être déplacé d’un site à un autre au sein de l’interface SharePoint, en exportant du contenu localement ou à l’aide d’un outil tiers.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-491">No, the site itself is associated with the group, however the content can be moved from one site to another within the SharePoint interface, by exporting content locally, or by using a third-party tool.</span></span>

<span data-ttu-id="ca8d9-492">**La suppression du site supprime-t-elle le groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-492">**Does deleting the site delete the group?**</span></span>

<span data-ttu-id="ca8d9-493">Oui, la suppression du site dans SharePoint supprimera les services et le contenu associés aux groupes et aux groupes.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-493">Yes, deleting the site in SharePoint will delete group and group-associated services and content.</span></span>

## <a name="stream"></a><span data-ttu-id="ca8d9-494">Flux</span><span class="sxs-lookup"><span data-stu-id="ca8d9-494">Stream</span></span>

<span data-ttu-id="ca8d9-495">Microsoft Stream est une plateforme d’hébergement et de partage de vidéos.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-495">Microsoft Stream is a video hosting and sharing platform.</span></span>

<span data-ttu-id="ca8d9-496">**Fonctionnalités clés fournies aux groupes**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-496">**Key features provided to Groups**</span></span>

- <span data-ttu-id="ca8d9-497">Stockage vidéo</span><span class="sxs-lookup"><span data-stu-id="ca8d9-497">Video storage</span></span>
- <span data-ttu-id="ca8d9-498">Teams enregistrement de réunion</span><span class="sxs-lookup"><span data-stu-id="ca8d9-498">Teams meeting recording</span></span>
- <span data-ttu-id="ca8d9-499">Canaux vidéo</span><span class="sxs-lookup"><span data-stu-id="ca8d9-499">Video channels</span></span>

<span data-ttu-id="ca8d9-500">**Stream peut-il créer un groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-500">**Can Stream create a group?**</span></span>

<span data-ttu-id="ca8d9-501">Oui, il est possible de créer un groupe de Microsoft 365 directement à partir de Stream.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-501">Yes, it is possible to create a new Microsoft 365 group directly from Stream.</span></span>

<span data-ttu-id="ca8d9-502">**Stream existe-t-il sans groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-502">**Does Stream exist without a group?**</span></span>

<span data-ttu-id="ca8d9-503">Oui, les canaux vidéo et les vidéos peuvent exister dans Stream sans être associés à un groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-503">Yes, video channels and videos can exist in Stream without being associated with a group.</span></span>

<span data-ttu-id="ca8d9-504">**Peut-il y avoir plusieurs vidéos et canaux par groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-504">**Can there be multiple videos and channels per Group?**</span></span>

<span data-ttu-id="ca8d9-505">Oui, il peut y avoir plusieurs vidéos et canaux dans chaque groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-505">Yes, there can be multiple videos and channels in each group.</span></span>

<span data-ttu-id="ca8d9-506">**Une vidéo ou un canal peut-il être associé à plusieurs groupes ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-506">**Can a video or channel be associated with multiple groups?**</span></span>

<span data-ttu-id="ca8d9-507">Oui, alors qu’une vidéo ou un canal est créé avec un groupe, il peut être partagé avec d’autres groupes.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-507">Yes, while a video or channel is created with a group, it can be shared with other groups.</span></span>

<span data-ttu-id="ca8d9-508">**Son association à un groupe peut-elle changer ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-508">**Can its association with a Group change?**</span></span>

<span data-ttu-id="ca8d9-509">Oui et non ; Les vidéos dans Stream sont la propriété du téléchargeur ou de l’enregistreur de réunion d’origine et peuvent donc être associées à n’importe quel groupe, mais les canaux vidéo peuvent uniquement être associés au groupe dans qui ils ont été créés à l’origine.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-509">Yes and no; videos in Stream are owned by the original uploader or meeting recorder and so can be associated with any group, however video channels can only be associated with the group they were originally created in.</span></span>

<span data-ttu-id="ca8d9-510">**La suppression de vidéos ou de canaux supprime-t-elle le groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-510">**Does deleting videos or channels delete the group?**</span></span>

<span data-ttu-id="ca8d9-511">Non, la suppression de vidéos ou de canaux ne supprime pas le groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-511">No, deleting videos or channels doesn’t delete the group.</span></span> <span data-ttu-id="ca8d9-512">Toutefois, la suppression du groupe lui-même dans Stream supprimera les services et le contenu associés au groupe, à l’exception des vidéos réelles.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-512">However, deleting the group itself in Stream will delete group-associated services and content, except for the actual videos.</span></span>

## <a name="yammer"></a><span data-ttu-id="ca8d9-513">Yammer</span><span class="sxs-lookup"><span data-stu-id="ca8d9-513">Yammer</span></span>

<span data-ttu-id="ca8d9-514">Yammer est une plateforme sociale d’entreprise conçue pour favoriser l’engagement de la communauté au sein et entre les organisations.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-514">Yammer is an enterprise social platform designed to foster community engagement within and between organizations.</span></span>

<span data-ttu-id="ca8d9-515">La création d’une communauté (anciennement appelée « groupe ») dans Yammer crée une boîte aux lettres, mais elle n’est pas utilisée pour le moment.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-515">Creating a community (formerly known as “group”) in Yammer creates a mailbox, but at present this is not used.</span></span>

<span data-ttu-id="ca8d9-516">Un groupe Microsoft 365 associé à un Yammer ne peut pas être utilisé avec une équipe dans Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-516">A Microsoft 365 group that is associated with Yammer cannot be used with a team in Microsoft Teams.</span></span>

<span data-ttu-id="ca8d9-517">**Fonctionnalités clés fournies aux groupes**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-517">**Key features provided to Groups**</span></span>

- <span data-ttu-id="ca8d9-518">Zone de conversation</span><span class="sxs-lookup"><span data-stu-id="ca8d9-518">Conversation area</span></span>

<span data-ttu-id="ca8d9-519">**Pouvez Yammer créer un groupe Microsoft 365'équipe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-519">**Can Yammer create a Microsoft 365 group?**</span></span>

<span data-ttu-id="ca8d9-520">Oui, la création d’un groupe dans Yammer crée un groupe Microsoft 365, si les plateformes sont connectées et si l’utilisateur a la possibilité de créer un groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-520">Yes, creating a new group in Yammer will create a new Microsoft 365 group, if the platforms are connected and the user has the ability to create a group.</span></span>

<span data-ttu-id="ca8d9-521">Un groupe Yammer avec un groupe Microsoft 365 associé ne peut pas être créé dans une interface ou un service autre que Yammer lui-même.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-521">A Yammer group with associated Microsoft 365 group cannot be created in any interface or service other than Yammer itself.</span></span>

<span data-ttu-id="ca8d9-522">**Un groupe Yammer existe-t-il sans groupe Microsoft 365 de données ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-522">**Does a Yammer group exist without a Microsoft 365 group?**</span></span>

<span data-ttu-id="ca8d9-523">Oui, il est possible de créer un groupe Yammer sans groupe Microsoft 365 groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-523">Yes, it is possible to create a Yammer group without a Microsoft 365 group.</span></span>

<span data-ttu-id="ca8d9-524">Si la plateforme Yammer n’est pas connectée à des groupes Microsoft 365 ou si les utilisateurs n’ont pas la possibilité de créer un groupe Microsoft 365, les groupes Yammer sont créés sans association Microsoft 365 groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-524">If the Yammer platform is not connected to Microsoft 365 groups, or users do not have the ability to create a Microsoft 365 group, Yammer groups are created without a Microsoft 365 group association.</span></span>

<span data-ttu-id="ca8d9-525">**Peut-il y avoir plusieurs groupes Yammer par Microsoft 365 groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-525">**Can there be multiple Yammer groups per Microsoft 365 group?**</span></span>

<span data-ttu-id="ca8d9-526">Non, la relation entre un groupe Yammer et un groupe Microsoft 365 est 1:1.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-526">No, the relationship between a Yammer group and a Microsoft 365 group is 1:1.</span></span>

<span data-ttu-id="ca8d9-527">**Un groupe Yammer peut-il être associé à plusieurs groupes Microsoft 365'utilisateurs ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-527">**Can a Yammer group be associated with multiple Microsoft 365 groups?**</span></span>

<span data-ttu-id="ca8d9-528">Non, le groupe Yammer ne peut être associé qu’à un seul Microsoft 365 groupe.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-528">No, the Yammer group can only be associated with a single Microsoft 365 group.</span></span> <span data-ttu-id="ca8d9-529">Il est possible de partager des billets avec d’autres groupes de Yammer ou de les déplacer vers ceux-ci.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-529">It is possible for posts to be shared with or moved to other Yammer groups.</span></span>

<span data-ttu-id="ca8d9-530">**L’association Yammer’un groupe d’Microsoft 365 peut-elle changer ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-530">**Can a Yammer group’s association with a Microsoft 365 group change?**</span></span>

<span data-ttu-id="ca8d9-531">Non, le groupe Yammer ne peut être associé qu’au groupe de Microsoft 365 auquel il a été initialement associé.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-531">No, the Yammer group can only ever be associated with the Microsoft 365 group to which it was originally associated.</span></span>

<span data-ttu-id="ca8d9-532">**La suppression du groupe de Yammer supprime-t-elle le Microsoft 365 groupe ?**</span><span class="sxs-lookup"><span data-stu-id="ca8d9-532">**Does deleting the Yammer group delete the Microsoft 365 group?**</span></span>

<span data-ttu-id="ca8d9-533">Oui, la suppression du groupe dans Yammer supprimera le contenu et les services associés au groupe Microsoft associés.</span><span class="sxs-lookup"><span data-stu-id="ca8d9-533">Yes, deleting the group in Yammer will delete related Microsoft group and group-associated services and content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca8d9-534">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca8d9-534">Related topics</span></span>

[<span data-ttu-id="ca8d9-535">Planification pas à pas de la gouvernance de la collaboration</span><span class="sxs-lookup"><span data-stu-id="ca8d9-535">Collaboration governance planning step-by-step</span></span>](collaboration-governance-overview.md#collaboration-governance-planning-step-by-step)

[<span data-ttu-id="ca8d9-536">Créer votre plan de gouvernance de collaboration</span><span class="sxs-lookup"><span data-stu-id="ca8d9-536">Create your collaboration governance plan</span></span>](collaboration-governance-first.md)