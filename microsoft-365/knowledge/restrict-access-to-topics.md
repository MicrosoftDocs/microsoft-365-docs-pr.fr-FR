---
title: Restreindre l’accès aux rubriques des rubriques microsoft
description: Comment exclure des rubriques pour les empêcher d’être découvertes.
author: efrene
ms.author: efrene
manager: pamgreen
ms.reviewer: cjtan
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
search.appverid: ''
ms.collection:
- enabler-strategic
- m365initiative-viva-topics
localization_priority: None
ms.openlocfilehash: d6dfb2f7f432a40c5b6e96a9437f50ba47e23387
ms.sourcegitcommit: 582555d2b4ef5f2e2494ffdeab2c1d49e5d6b724
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51500878"
---
# <a name="restrict-access-to-topics-in-microsoft-viva-topics"></a><span data-ttu-id="5d2dc-103">Restreindre l’accès aux rubriques des rubriques microsoft</span><span class="sxs-lookup"><span data-stu-id="5d2dc-103">Restrict access to topics in Microsoft Viva Topics</span></span>

<span data-ttu-id="5d2dc-104">Dans Microsoft Domaine, les parties prenantes de votre organisation peuvent vouloir s’assurer que des rubriques spécifiques ne sont pas découvertes et exposées à vos utilisateurs sous licence.</span><span class="sxs-lookup"><span data-stu-id="5d2dc-104">In Microsoft Viva, stakeholders in your organization may want to make sure that specific topics aren't discovered and exposed to your licensed users.</span></span> <span data-ttu-id="5d2dc-105">Par exemple, vous travaillez peut-être sur un projet dont vous ne souhaitez pas encore exposer d’informations.</span><span class="sxs-lookup"><span data-stu-id="5d2dc-105">For example, you may be working on a project that you don't want to expose any information about yet.</span></span> <span data-ttu-id="5d2dc-106">Bien que les autorisations Office 365 sur les sites, les fichiers et d’autres ressources empêchent les utilisateurs d’Expériences de rubrique d’afficher des informations sensibles dans des rubriques, il existe des protections supplémentaires pour empêcher la découverte de sujets spécifiques.</span><span class="sxs-lookup"><span data-stu-id="5d2dc-106">While Office 365 permissions on sites, files and other resources will prevent Topic Experiences users from viewing sensitive information in topics, there are additional safeguards to prevent specific topics from ever being discovered.</span></span>

<span data-ttu-id="5d2dc-107">Bien que les administrateurs du savoir contrôlent les paramètres afin d’empêcher la découverte de sujets, les gestionnaires de connaissances et les autres parties prenantes doivent savoir comment cela se fait pour travailler en collaboration.</span><span class="sxs-lookup"><span data-stu-id="5d2dc-107">While knowledge admins control the settings to prevent topics from being discovered, knowledge managers and other stakeholders need to know how it is done so that they can work collaboratively.</span></span>

> [!Important] 
> <span data-ttu-id="5d2dc-108">Cet article explique comment empêcher l’identification de rubriques par le biais de l’IA ou leur affichage dans votre environnement en tant que dispositif de sécurité supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="5d2dc-108">This article describes ways to prevent topics from being identified through AI or viewed in your environment as an additional security safeguard.</span></span> <span data-ttu-id="5d2dc-109">Il est important de noter que, dans rubriques Topics, les utilisateurs ne sont pas autorisés à afficher quoi que ce soit dans une rubrique à partir des autorisations Office 365.</span><span class="sxs-lookup"><span data-stu-id="5d2dc-109">It is important to note that in Viva Topics, users aren't allowed to view anything in a topic that they aren't allowed to access through Office 365 permissions.</span></span> <span data-ttu-id="5d2dc-110">Même si un utilisateur est en mesure d’afficher une rubrique, ses fichiers, ses sites et ses pages ne sont pas autorisés à afficher Office 365.</span><span class="sxs-lookup"><span data-stu-id="5d2dc-110">Even if a users is able to view a topic, its files, sites, and pages they do not have Office 365 permissions to view will not be visible to them.</span></span> <span data-ttu-id="5d2dc-111">Vous assurer que les autorisations sur les fichiers sensibles sont correctement définies doit être votre principal dispositif de sécurité.</span><span class="sxs-lookup"><span data-stu-id="5d2dc-111">Making sure that permissions to sensitive files are correctly set should be your primary security safeguard.</span></span>

## <a name="prevent-topics-from-being-identified"></a><span data-ttu-id="5d2dc-112">Empêcher l’identification des rubriques</span><span class="sxs-lookup"><span data-stu-id="5d2dc-112">Prevent topics from being identified</span></span>

<span data-ttu-id="5d2dc-113">L’administrateur du savoir peut restreindre l’accès à des rubriques spécifiques en les empêchant d’être trouvés dans l’indexation initiale.</span><span class="sxs-lookup"><span data-stu-id="5d2dc-113">Knowledge admin can restrict access to specific topics by preventing them from being found in initial indexing.</span></span> <span data-ttu-id="5d2dc-114">Il existe deux façons d’accomplir cette tâche dans les paramètres d’administration Rubriques Dans le Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="5d2dc-114">There are two ways to do this task in the Viva Topics admin settings in the Microsoft 365 admin center.</span></span>
 
- <span data-ttu-id="5d2dc-115">[Sélectionnez des sites SharePoint à exclure](./topic-experiences-discovery.md#select-sharepoint-topic-sources)de la découverte de rubriques : vous pouvez utiliser ce paramètre pour empêcher l’analyse de sites SharePoint spécifiques pour des rubriques.</span><span class="sxs-lookup"><span data-stu-id="5d2dc-115">[Select SharePoint sites to exclude from topic discovery](./topic-experiences-discovery.md#select-sharepoint-topic-sources): You can use this setting to prevent specific SharePoint sites from being crawled for topics.</span></span>
- <span data-ttu-id="5d2dc-116">[Exclure les rubriques par leur nom](./topic-experiences-discovery.md#exclude-topics-by-name): les administrateurs peuvent utiliser ce paramètre pour empêcher la découverte de sujets spécifiques par leur nom.</span><span class="sxs-lookup"><span data-stu-id="5d2dc-116">[Exclude topics by name](./topic-experiences-discovery.md#exclude-topics-by-name): Admins can use this setting to prevent specific topics from being discovered by name.</span></span> <span data-ttu-id="5d2dc-117">Dans les paramètres d’administration De Rubriques, un administrateur peut télécharger une liste de rubriques à exclure dans un fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="5d2dc-117">In the Viva Topics admin settings, an admin can upload a list of topics to be excluded in a CSV file.</span></span> <span data-ttu-id="5d2dc-118">Vous pouvez exclure les rubriques qui ont des correspondances exactes ou partielles d’un nom de rubrique.</span><span class="sxs-lookup"><span data-stu-id="5d2dc-118">You can exclude topics that have exact or partial matches of a topic name.</span></span>

## <a name="prevent-topics-from-being-viewed-by-specific-users"></a><span data-ttu-id="5d2dc-119">Empêcher des utilisateurs spécifiques d’afficher des rubriques</span><span class="sxs-lookup"><span data-stu-id="5d2dc-119">Prevent topics from being viewed by specific users</span></span>

<span data-ttu-id="5d2dc-120">Les administrateurs du savoir peuvent également sélectionner les personnes qui peuvent afficher [les rubriques de votre organisation.](./topic-experiences-knowledge-rules.md)</span><span class="sxs-lookup"><span data-stu-id="5d2dc-120">Knowledge admins can also [select who can view topics in your organization](./topic-experiences-knowledge-rules.md).</span></span> <span data-ttu-id="5d2dc-121">Ce paramètre vous permet de sélectionner les utilisateurs sous licence qui peuvent afficher toutes les rubriques.</span><span class="sxs-lookup"><span data-stu-id="5d2dc-121">This setting lets you select which licensed users can view all topics.</span></span> <span data-ttu-id="5d2dc-122">Par exemple, dans un environnement pilote, vous pouvez autoriser uniquement un petit groupe d’utilisateurs à afficher des rubriques.</span><span class="sxs-lookup"><span data-stu-id="5d2dc-122">For example, in a pilot environment, you may want to only allow a small group of users to be able to view topics.</span></span>

## <a name="remove-topics-from-being-viewed"></a><span data-ttu-id="5d2dc-123">Supprimer l’affichage des rubriques</span><span class="sxs-lookup"><span data-stu-id="5d2dc-123">Remove topics from being viewed</span></span>

<span data-ttu-id="5d2dc-124">Les gestionnaires de connaissances peuvent choisir [de supprimer des rubriques afin](./manage-topics.md) que les utilisateurs ne les voient plus.</span><span class="sxs-lookup"><span data-stu-id="5d2dc-124">Knowledge managers can choose to [remove topics](./manage-topics.md) so that users can no longer see them.</span></span> <span data-ttu-id="5d2dc-125">Dans la page Gérer les rubriques dans le centre de **rubriques,** les gestionnaires de connaissances peuvent choisir de rejeter des rubriques spécifiques afin d’empêcher leur affichage.</span><span class="sxs-lookup"><span data-stu-id="5d2dc-125">On the **Manage topics** page in the **Topic center**, knowledge managers can choose to reject specific topics to prevent them from being viewed.</span></span> <span data-ttu-id="5d2dc-126">Les rubriques peuvent être supprimées, qu’elles soient dans un état suggéré ou confirmé.</span><span class="sxs-lookup"><span data-stu-id="5d2dc-126">Topics can be removed regardless if they are in a suggested or confirmed state.</span></span>

<span data-ttu-id="5d2dc-127">Les rubriques supprimées peuvent être ajoutées ultérieurement en tant que rubriques consultables si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="5d2dc-127">Removed topics can later be added back as viewable topics if needed.</span></span> 


## <a name="see-also"></a><span data-ttu-id="5d2dc-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d2dc-128">See also</span></span>



