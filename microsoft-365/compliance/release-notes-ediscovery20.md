---
title: Notes de publication pour Advanced eDiscovery
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Cet article contient des notes de publication pour Advanced eDiscovery, notamment des problèmes connus, des problèmes résolus et de nouvelles fonctionnalités.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 45a4647856fef0186840ec5465bb9250e5d78de4
ms.sourcegitcommit: a45cf8b887587a1810caf9afa354638e68ec5243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/05/2020
ms.locfileid: "44034618"
---
# <a name="release-notes-for-advanced-ediscovery"></a><span data-ttu-id="baef5-103">Notes de publication pour Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="baef5-103">Release notes for Advanced eDiscovery</span></span>

<span data-ttu-id="baef5-104">Le programme de préversion public pour Advanced eDiscovery est le moyen d’accéder en avant-première aux fonctionnalités et mises à jour à venir.</span><span class="sxs-lookup"><span data-stu-id="baef5-104">The Public Preview program for Advanced eDiscovery is the way to get early access to the upcoming functionality and updates.</span></span> <span data-ttu-id="baef5-105">Pour accéder en avant-première aux fonctionnalités les plus récentes, il vous suffit de créer et d’utiliser un cas avancé eDiscovery dans le centre de conformité & Compliance Center.</span><span class="sxs-lookup"><span data-stu-id="baef5-105">To get early access to the newest features, just create and use an Advanced eDiscovery case in the Security & Compliance Center.</span></span> <span data-ttu-id="baef5-106">Voir [Create a New case](create-new-ediscovery-case.md).</span><span class="sxs-lookup"><span data-stu-id="baef5-106">See [Create a new case](create-new-ediscovery-case.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="baef5-107">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="baef5-107">Known issues</span></span>

<span data-ttu-id="baef5-108">**Microsoft Forms**</span><span class="sxs-lookup"><span data-stu-id="baef5-108">**Microsoft Forms**</span></span>

- <span data-ttu-id="baef5-109">Les données correspondant à un formulaire créé avant le 31 janvier 2019 ne pourront pas être recherchées lors de l’utilisation de l’outil de recherche dans Advanced eDiscovery pour rechercher des boîtes aux lettres de dépositaire.</span><span class="sxs-lookup"><span data-stu-id="baef5-109">The data corresponding to a form created before January 31, 2019 will not be searchable when using the Search tool in Advanced eDiscovery to search custodian mailboxes.</span></span> <span data-ttu-id="baef5-110">Les formulaires créés après cette date seront disponibles pour la recherche.</span><span class="sxs-lookup"><span data-stu-id="baef5-110">Forms created after this date will be available to search.</span></span>

- <span data-ttu-id="baef5-111">Un formulaire créé par un utilisateur peut toujours recevoir des réponses même après la suppression de l’utilisateur qui a créé le formulaire.</span><span class="sxs-lookup"><span data-stu-id="baef5-111">A form created by a user can still receive responses even after the user who created the Form is deleted.</span></span> <span data-ttu-id="baef5-112">Toutefois, les données correspondantes de ces réponses (qui ont eu lieu après la suppression de la boîte aux lettres de dépositaire) ne peuvent pas être recherchées lors de l’utilisation de l’outil de recherche dans Advanced eDiscovery pour rechercher des boîtes aux lettres de dépositaire.</span><span class="sxs-lookup"><span data-stu-id="baef5-112">However, the corresponding data for those responses (that occurred after the custodian mailbox was deleted) will not be searchable when using the Search tool in Advanced eDiscovery to search custodian mailboxes.</span></span>
 
<span data-ttu-id="baef5-113">**Microsoft Sway**</span><span class="sxs-lookup"><span data-stu-id="baef5-113">**Microsoft Sway**</span></span>

- <span data-ttu-id="baef5-114">Si un utilisateur modifie un Sway juste avant la suppression du compte d’utilisateur pour le propriétaire de ce Sway, il se peut que ces modifications ne puissent pas être recherchées lors de l’utilisation de l’outil de recherche dans Advanced eDiscovery pour rechercher des boîtes aux lettres de dépositaire.</span><span class="sxs-lookup"><span data-stu-id="baef5-114">If a user edits a sway just prior to the deletion of the user account for the owner of that sway, then those changes may not be be searchable when using the Search tool in Advanced eDiscovery to search custodian mailboxes.</span></span> <span data-ttu-id="baef5-115">Sway bloque les modifications apportées à un Sway dès qu’il reçoit un signal indiquant que le compte a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="baef5-115">Sway blocks changes to to a sway as soon as it receives a signal that the account was deleted.</span></span> <span data-ttu-id="baef5-116">Toutefois, il existe une petite chance qu’un Sway puisse être modifié avant la réception de ce signal.</span><span class="sxs-lookup"><span data-stu-id="baef5-116">However, there's a small chance that a sway can be edited before this signal is received.</span></span>

## <a name="issues-fixed-in-this-release"></a><span data-ttu-id="baef5-117">Problèmes résolus dans cette version</span><span class="sxs-lookup"><span data-stu-id="baef5-117">Issues fixed in this release</span></span>

- <span data-ttu-id="baef5-118">DCR : gestion des exceptions pour les éléments non indexés et les éléments orphelins</span><span class="sxs-lookup"><span data-stu-id="baef5-118">DCR: Exception handling for unindexed items and orphaned items</span></span>
- <span data-ttu-id="baef5-119">DCR : notifications de blocage</span><span class="sxs-lookup"><span data-stu-id="baef5-119">DCR: Hold notifications</span></span>
- <span data-ttu-id="baef5-120">DCR : dépositaires dans eDiscovery</span><span class="sxs-lookup"><span data-stu-id="baef5-120">DCR: Custodians in eDiscovery</span></span>

## <a name="whats-new"></a><span data-ttu-id="baef5-121">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="baef5-121">What's new</span></span>

- <span data-ttu-id="baef5-122">**Reconception de la navigation dans le centre de sécurité & conformité** – Advanced eDiscovery a une nouvelle apparence.</span><span class="sxs-lookup"><span data-stu-id="baef5-122">**Redesigned navigation in the Security & Compliance Center** – Advanced eDiscovery has a new look and feel.</span></span> <span data-ttu-id="baef5-123">Utilisez Advanced eDiscovery pour gérer davantage votre flux de travail de cas.</span><span class="sxs-lookup"><span data-stu-id="baef5-123">Use Advanced eDiscovery to manage more of your case workflow.</span></span>

- <span data-ttu-id="baef5-124">**Gestion des cas** : il existe une prise en charge supplémentaire pour les nouveaux types de cas.</span><span class="sxs-lookup"><span data-stu-id="baef5-124">**Case management** – There's additional support for new case types.</span></span> <span data-ttu-id="baef5-125">Vous pouvez également sélectionner et enregistrer vos dossiers récents et favoris.</span><span class="sxs-lookup"><span data-stu-id="baef5-125">You can also select and save your recent and favorite cases.</span></span> <span data-ttu-id="baef5-126">Suivre et surveiller l’activité dans et dans les cas à l’aide de nouveaux tableaux de bord.</span><span class="sxs-lookup"><span data-stu-id="baef5-126">Track and monitor activity within and across cases using new dashboards.</span></span>

- <span data-ttu-id="baef5-127">**Gestion des dépositaires** : ajoutez et supprimez des utilisateurs comme dépositaires de données dans un cas.</span><span class="sxs-lookup"><span data-stu-id="baef5-127">**Custodian management** – Add and remove users as data custodians within a case.</span></span>

- <span data-ttu-id="baef5-128">**Intégration d’Exchange, de onedrive et de teams** : ajoutez automatiquement la boîte aux lettres actuelle d’un utilisateur, le compte OneDrive entreprise et les sites Microsoft teams à un cas.</span><span class="sxs-lookup"><span data-stu-id="baef5-128">**Exchange, OneDrive, and Teams Integration** – Automatically add a user's current mailbox, OneDrive for Business account, and Microsoft Teams sites to a case.</span></span> 

- <span data-ttu-id="baef5-129">**Communications des dépositaires** : envoyez et gérez les notifications de conservation légale au nom de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="baef5-129">**Custodian communications** – Send and manage legal hold notifications on behalf of your organization.</span></span>

- <span data-ttu-id="baef5-130">**Portail dépositaire** : nouveau portail pour les dépositaires pour accéder à leurs notifications d’attente actives.</span><span class="sxs-lookup"><span data-stu-id="baef5-130">**Custodian portal** – New portal for custodians to access their active hold notices.</span></span>

- <span data-ttu-id="baef5-131">**Indexation profonde** : ré-analyse des éléments partiellement indexés à la demande.</span><span class="sxs-lookup"><span data-stu-id="baef5-131">**Deep indexing** – Re-crawl partially indexed items on demand.</span></span>

- <span data-ttu-id="baef5-132">**Correction d’erreur** : correction ou téléchargement des erreurs de traitement ; Il s’agit notamment de la prise en charge des types de fichiers volumineux, des fichiers protégés par mot de passe et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="baef5-132">**Error remediation** – Remediate or download processing errors; this include remediation support for large file types, password protected files, and more.</span></span> 

- <span data-ttu-id="baef5-133">**Améliorations de la recherche** : permet de créer une recherche en identifiant des dépositaires et/ou des emplacements.</span><span class="sxs-lookup"><span data-stu-id="baef5-133">**Improvements to search** – Create a search by identifying custodians and/or locations.</span></span>

- <span data-ttu-id="baef5-134">**Examiner les ensembles** : gérer, suivre et auditer des ensembles de documents statiques.</span><span class="sxs-lookup"><span data-stu-id="baef5-134">**Review sets** – Manage, track, and audit static sets of documents.</span></span>

- <span data-ttu-id="baef5-135">**Révision** : utilisez une vue native, texte et quasi native pour consulter les documents ajoutés à votre jeu de révision.</span><span class="sxs-lookup"><span data-stu-id="baef5-135">**Review** – Use a native, text, and near-native view to review documents added to your review set.</span></span>

- <span data-ttu-id="baef5-136">**Biffer, Baliser et annoter** : Biffer du texte, appliquer des balises et créer des annotations lors de la révision des documents.</span><span class="sxs-lookup"><span data-stu-id="baef5-136">**Redact, tag, and annotate** – Redact text, apply tags, and make annotations as you review documents.</span></span>
  
- <span data-ttu-id="baef5-137">Analyse **assistée**: Tirez parti de l’analyse avancée de la découverte électronique pour rechercher, Rechercher et effectuer des recherches dans un jeu de révision.</span><span class="sxs-lookup"><span data-stu-id="baef5-137">**Analytics-powered review**– Leverage Advanced eDiscovery analytics to find, search, and cull results within a review set.</span></span>

- <span data-ttu-id="baef5-138">**Travaux** : suivre l’état des processus de longue durée.</span><span class="sxs-lookup"><span data-stu-id="baef5-138">**Jobs** – Track status of long-running processes.</span></span>

- <span data-ttu-id="baef5-139">**Nouvelles activités d’audit** : suivez et affichez les nouvelles activités d’audit pour Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="baef5-139">**New audit activities** – Track and view new audit activity for Advanced eDiscovery.</span></span>
