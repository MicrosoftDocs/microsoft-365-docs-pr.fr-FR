---
title: Restreindre l’accès aux rubriques
description: Comment exclure des rubriques pour les empêcher d’être découvertes.
author: efrene
ms.author: efrene
manager: pamgreen
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
search.appverid: ''
ms.collection: enabler-strategic
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: None
ms.openlocfilehash: b23d01585d9282132d9e55c74bb22bcdc6ca314a
ms.sourcegitcommit: 884ac262443c50362d0c3ded961d36d6b15d8b73
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/16/2020
ms.locfileid: "49698964"
---
# <a name="restrict-access-to-topics-in-topic-experiences"></a><span data-ttu-id="a1af9-103">Restreindre l’accès aux rubriques d’expériences</span><span class="sxs-lookup"><span data-stu-id="a1af9-103">Restrict access to topics in Topic Experiences</span></span>

<span data-ttu-id="a1af9-104">Dans les expériences de rubrique, les parties prenantes de votre organisation peuvent souhaiter s’assurer que des rubriques spécifiques ne sont pas découvertes et exposées à vos utilisateurs sous licence.</span><span class="sxs-lookup"><span data-stu-id="a1af9-104">In Topic Experiences, stakeholders in your organization may want to make sure that specific topics are not discovered and exposed to your licensed users.</span></span> <span data-ttu-id="a1af9-105">Par exemple, vous pouvez travailler sur un projet pour lequel vous ne souhaitez pas exposer d’informations.</span><span class="sxs-lookup"><span data-stu-id="a1af9-105">For example, you may be working on a project that you don't want to expose any information about yet.</span></span> <span data-ttu-id="a1af9-106">Bien que les autorisations Office 365 sur les sites, les fichiers et les autres ressources empêchent les utilisateurs de consulter des informations sensibles dans les rubriques, il existe des mesures de sécurité supplémentaires pour empêcher les rubriques spécifiques d’être découvertes.</span><span class="sxs-lookup"><span data-stu-id="a1af9-106">While Office 365 permissions on sites, files and other resources will prevent Topic Experiences users from viewing sensitive information in topics, there are additional safeguards to prevent specific topics from ever being discovered.</span></span>

<span data-ttu-id="a1af9-107">Tandis que les administrateurs du savoir contrôlent les paramètres du réseau de connaissances pour empêcher la découverte des rubriques, les responsables des connaissances et les autres parties prenantes ont besoin de savoir comment procéder afin qu’ils puissent travailler en collaboration sur ce.</span><span class="sxs-lookup"><span data-stu-id="a1af9-107">While knowledge admins control the knowledge network settings to prevent topics from being discovered, knowledge managers and other stakeholders need to be know how this is done so that they can work collaboratively on this.</span></span>

> [!Important] 
> <span data-ttu-id="a1af9-108">Cet article décrit les moyens d’empêcher l’identification des rubriques via les IA ou l’affichage dans votre environnement en tant que dispositif de sécurité supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="a1af9-108">This article describes ways to prevent topics from being identified through AI or viewed in your environment as an additional security safeguard.</span></span> <span data-ttu-id="a1af9-109">Il est important de noter que dans les expériences de rubrique, les utilisateurs ne sont pas autorisés à afficher quoi que ce soit dans une rubrique qu’ils ne sont pas autorisés à accéder par le biais des autorisations Office 365.</span><span class="sxs-lookup"><span data-stu-id="a1af9-109">It is important to note that in Topic Experiences, users are not allowed to view anything in a topic that they are not allowed to access through Office 365 permissions.</span></span> <span data-ttu-id="a1af9-110">Même si un utilisateur peut afficher un sujet, ses fichiers, ses sites et ses pages n’ont pas d’autorisations Office 365 à afficher ne seront pas visibles.</span><span class="sxs-lookup"><span data-stu-id="a1af9-110">Even if a users is able to view a topic, its files, sites, and pages they do not have Office 365 permissions to view will not be visible to them.</span></span> <span data-ttu-id="a1af9-111">Assurez-vous que les autorisations de fichiers sensibles sont définies correctement.</span><span class="sxs-lookup"><span data-stu-id="a1af9-111">Making sure that permissions to sensitive files are correctly set should be your primary security safeguard.</span></span>

## <a name="prevent-topics-from-being-identified"></a><span data-ttu-id="a1af9-112">Empêcher l’identification des rubriques</span><span class="sxs-lookup"><span data-stu-id="a1af9-112">Prevent topics from being identified</span></span>

<span data-ttu-id="a1af9-113">Knowledge admin peut restreindre l’accès à des rubriques spécifiques en les empêchant de se trouver dans l’indexation initiale.</span><span class="sxs-lookup"><span data-stu-id="a1af9-113">Knowledge admin can restrict access to specific topics by preventing them from being found in initial indexing.</span></span> <span data-ttu-id="a1af9-114">Il existe deux façons de procéder dans les paramètres d’administrateur du réseau de connaissances dans le centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a1af9-114">There are two ways to do this in the Knowledge Network admin settings in the Microsoft 365 admin center.</span></span>
 
- <span data-ttu-id="a1af9-115">[Sélectionner les sites SharePoint à exclure de la découverte de rubrique](https://docs.microsoft.com/microsoft-365/knowledge/topic-experiences-discovery#select-sharepoint-topic-sources): vous pouvez utiliser ce paramètre pour empêcher que des sites SharePoint spécifiques soient analysés pour des rubriques.</span><span class="sxs-lookup"><span data-stu-id="a1af9-115">[Select SharePoint sites to exclude from topic discovery](https://docs.microsoft.com/microsoft-365/knowledge/topic-experiences-discovery#select-sharepoint-topic-sources): You can use this setting to prevent specific SharePoint sites from being crawled for topics.</span></span>
- <span data-ttu-id="a1af9-116">[Exclure les rubriques par nom](https://docs.microsoft.com/microsoft-365/knowledge/topic-experiences-discovery#exclude-topics-by-name): les administrateurs peuvent utiliser ce paramètre pour empêcher des rubriques spécifiques d’être découvertes par nom.</span><span class="sxs-lookup"><span data-stu-id="a1af9-116">[Exclude topics by name](https://docs.microsoft.com/microsoft-365/knowledge/topic-experiences-discovery#exclude-topics-by-name): Admins can use this setting to prevent specific topics from being discovered by name.</span></span> <span data-ttu-id="a1af9-117">Dans les paramètres d’administrateur du réseau de connaissances, un administrateur peut télécharger une liste de rubriques à exclure dans un fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="a1af9-117">In the Knowledge Network admin settings, an admin can upload a list of topics to be excluded in a CSV file.</span></span> <span data-ttu-id="a1af9-118">Vous pouvez exclure les rubriques qui ont des correspondances exactes ou partielles d’un nom de rubrique.</span><span class="sxs-lookup"><span data-stu-id="a1af9-118">You can exclude topics that have exact or partial matches of a topic name.</span></span>

## <a name="prevent-topics-from-being-viewed-by-specific-users"></a><span data-ttu-id="a1af9-119">Empêcher l’affichage des rubriques par des utilisateurs spécifiques</span><span class="sxs-lookup"><span data-stu-id="a1af9-119">Prevent topics from being viewed by specific users</span></span>

<span data-ttu-id="a1af9-120">Knowledge admins peut également [Sélectionner les personnes qui peuvent afficher les rubriques de votre organisation](https://docs.microsoft.com/microsoft-365/knowledge/topic-experiences-knowledge-rules).</span><span class="sxs-lookup"><span data-stu-id="a1af9-120">Knowledge admins can also [select who can view topics in your organization](https://docs.microsoft.com/microsoft-365/knowledge/topic-experiences-knowledge-rules).</span></span> <span data-ttu-id="a1af9-121">Ce paramètre vous permet de sélectionner les utilisateurs sous licence qui peuvent afficher toutes les rubriques.</span><span class="sxs-lookup"><span data-stu-id="a1af9-121">This setting lets you select which licensed users can view all topics.</span></span> <span data-ttu-id="a1af9-122">Par exemple, dans un environnement pilote, vous pouvez uniquement autoriser un petit groupe d’utilisateurs à afficher des rubriques.</span><span class="sxs-lookup"><span data-stu-id="a1af9-122">For example, in a pilot environment, you may want to only allow a small group of users to be able to view topics.</span></span>

## <a name="remove-topics-from-being-viewed"></a><span data-ttu-id="a1af9-123">Supprimer les rubriques de l’affichage</span><span class="sxs-lookup"><span data-stu-id="a1af9-123">Remove topics from being viewed</span></span>

<span data-ttu-id="a1af9-124">Les gestionnaires de connaissances peuvent choisir de [supprimer des rubriques](https://docs.microsoft.com/microsoft-365/knowledge/manage-topics) afin que les utilisateurs ne puissent plus les voir.</span><span class="sxs-lookup"><span data-stu-id="a1af9-124">Knowledge managers can choose to [remove topics](https://docs.microsoft.com/microsoft-365/knowledge/manage-topics) so that users can no longer see them.</span></span> <span data-ttu-id="a1af9-125">Sur la page **gérer les rubriques** dans le **Centre** des rubriques, les gestionnaires de connaissances peuvent choisir de rejeter des rubriques spécifiques afin de les empêcher d’être affichées.</span><span class="sxs-lookup"><span data-stu-id="a1af9-125">On the **Manage topics** page in the **Topic center**, knowledge managers can choose to reject specific topics to prevent them from being viewed.</span></span> <span data-ttu-id="a1af9-126">Les rubriques peuvent être supprimées, qu’elles soient dans un État suggéré ou confirmé.</span><span class="sxs-lookup"><span data-stu-id="a1af9-126">Topics can be removed regardless if they are in a suggested or confirmed state.</span></span>

<span data-ttu-id="a1af9-127">Les rubriques supprimées peuvent ensuite être rajoutées en tant que rubriques affichables si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="a1af9-127">Removed topics can later be added back as viewable topics if needed.</span></span> 


## <a name="see-also"></a><span data-ttu-id="a1af9-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1af9-128">See also</span></span>



  






