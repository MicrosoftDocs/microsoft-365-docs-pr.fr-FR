---
title: Utiliser des dépositaires dans Advanced eDiscovery
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
description: L’outil de gestion des dépositaires dans Advanced eDiscovery vous permet de gérer le flux de travail concernant l’identification, la préservation et la collecte des données associées aux personnes concernées dans un cas juridique.
ms.openlocfilehash: 5f112b5229e2a13b329559786ffe82bce798fa72
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37079375"
---
# <a name="work-with-custodians-in-advanced-ediscovery"></a><span data-ttu-id="f7d94-103">Utiliser des dépositaires dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="f7d94-103">Work with custodians in Advanced eDiscovery</span></span>

<span data-ttu-id="f7d94-104">Lorsqu’une organisation répond à une enquête légale, le flux de travail concernant l’identification, la préservation et la collecte de contenu potentiellement pertinent est basé sur les personnes de l’organisation qui sont des dépositaires de données pertinentes.</span><span class="sxs-lookup"><span data-stu-id="f7d94-104">When an organization responds to a legal investigation, the workflow around identifying, preserving, and collecting potentially relevant content is based on the people in the organization who are the custodians of relevant data.</span></span> <span data-ttu-id="f7d94-105">Dans eDiscovery, ces individus sont appelés « *dépositaires de données* » (ou simplement des *dépositaires*) et sont définis en tant que « personnes ayant le contrôle administratif d’un document ou d’un fichier électronique ».</span><span class="sxs-lookup"><span data-stu-id="f7d94-105">In eDiscovery, these individuals are called *data custodians* (or just *custodians*) and are defined as "persons having administrative control of a document or electronic file".</span></span> <span data-ttu-id="f7d94-106">Par exemple, le dépositaire d’un message électronique peut être le propriétaire de la boîte aux lettres qui contient le message pertinent.</span><span class="sxs-lookup"><span data-stu-id="f7d94-106">For example, the custodian of an email message could be the owner of the mailbox that contains the relevant message.</span></span>  

<span data-ttu-id="f7d94-107">Lorsqu’une enquête commence, l’équipe eDiscovery doit identifier rapidement tous les dépositaires pertinents et les sources de données associées à l’incident.</span><span class="sxs-lookup"><span data-stu-id="f7d94-107">When an investigation begins, the eDiscovery team must quickly identify all the relevant custodians and data sources related to the case.</span></span> <span data-ttu-id="f7d94-108">Au fil du temps, la liste des dépositaires et de leurs sources de données peut augmenter ou decreasse.</span><span class="sxs-lookup"><span data-stu-id="f7d94-108">Over time, the list of custodians and their data sources may increase or decreasse.</span></span> <span data-ttu-id="f7d94-109">Par conséquent, les organisations doivent maintenir un processus contrôlé concernant l’identification, la préservation et la collecte de contenu privative de temps pendant le cycle de vie d’un cas.</span><span class="sxs-lookup"><span data-stu-id="f7d94-109">As a result, organizations must maintain a controlled process around identifying, preserving, and collecting custodial content throughout the life cycle of a case.</span></span>

<span data-ttu-id="f7d94-110">Dans un cas avancé eDiscovery, les équipes juridiques peuvent ajouter des personnes au sein de leur organisation en tant que dépositaires, et identifier et conserver automatiquement des sources de données privatives de ressources telles que des boîtes aux lettres Exchange, des comptes OneDrive et des sites SharePoint et Teams.</span><span class="sxs-lookup"><span data-stu-id="f7d94-110">In an Advanced eDiscovery case, legal teams can add individuals in their organization as custodians, and automatically identify and preserve custodial data sources such as Exchange mailboxes, OneDrive accounts, and SharePoint and Teams sites.</span></span> <span data-ttu-id="f7d94-111">À l’aide de l’outil de gestion des dépositaires intégré dans Advanced eDiscovery, les organisations peuvent sécuriser les informations stockées électroniquement d’une suppression involontaire (ou intentionnelle).</span><span class="sxs-lookup"><span data-stu-id="f7d94-111">By using the built-in custodian management tool in Advanced eDiscovery, organizations can secure electronically stored information from inadvertent (or intentional) deletion.</span></span> <span data-ttu-id="f7d94-112">Cela vous permet d’éliminer le processus de conservation du temps et source d’erreurs qui nécessite une utilisation manuelle.</span><span class="sxs-lookup"><span data-stu-id="f7d94-112">This lets you eliminate the time-consuming and error-prone process of manually having to perform the legal hold processes.</span></span> 

<span data-ttu-id="f7d94-113">Pour plus d’informations sur l’utilisation des dépositaires, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="f7d94-113">For more information about working with custodians, see the following:</span></span> 

- [<span data-ttu-id="f7d94-114">Ajouter des consignataires à un cas</span><span class="sxs-lookup"><span data-stu-id="f7d94-114">Add custodians to a case</span></span>](add-custodians-to-case.md)

- [<span data-ttu-id="f7d94-115">Gestion des dépositaires dans un cas</span><span class="sxs-lookup"><span data-stu-id="f7d94-115">Manage custodians in a case</span></span>](manage-new-custodians.md)

- [<span data-ttu-id="f7d94-116">Afficher l’activité des consignataires</span><span class="sxs-lookup"><span data-stu-id="f7d94-116">View custodian activity</span></span>](view-custodian-activity.md)

## <a name="advanced-ediscovery-permissions"></a><span data-ttu-id="f7d94-117">Autorisations eDiscovery avancées</span><span class="sxs-lookup"><span data-stu-id="f7d94-117">Advanced eDiscovery permissions</span></span>

<span data-ttu-id="f7d94-118">Dans Advanced eDiscovery, vous pouvez utiliser le groupe de rôles intégré eDiscovery Manager pour attribuer les autorisations nécessaires aux investigateurs légaux afin qu’ils puissent gérer le flux de travail de bout en bout dans Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="f7d94-118">In Advanced eDiscovery, you can use the built-in eDiscovery Manager role group to assign the necessary permissions to legal investigators so they can manage the end-to-end workflow in Advanced eDiscovery.</span></span> <span data-ttu-id="f7d94-119">Vous pouvez également créer des groupes de rôles personnalisés avec un sous-ensemble des rôles nécessaires pour effectuer certaines actions dans un cas dans Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="f7d94-119">Alternatively, you can create custom role groups with a subset of the roles necessary to perform certain actions in a case in Advanced eDiscovery.</span></span> <span data-ttu-id="f7d94-120">Pour plus d’informations sur les rôles liés à la découverte électronique, consultez [la rubrique attribution d’autorisations eDiscovery dans le centre de sécurité & conformité](assign-ediscovery-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="f7d94-120">For more information about eDiscovery-related roles, see [Assign eDiscovery permissions in the Security & Compliance Center](assign-ediscovery-permissions.md).</span></span>
