---
title: Utiliser des dépositaires dans Advanced eDiscovery
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
ms.custom:
- seo-marvel-apr2020
description: Découvrez comment utiliser l’outil de gestion des dépositaires dans Advanced eDiscovery pour gérer les données d’un cas juridique.
ms.openlocfilehash: 159ee0b0365ec7c2419fd9abe1426ad9c5efed4a
ms.sourcegitcommit: 51a9f34796535309b8ca8b52da92da0a3621327b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/02/2020
ms.locfileid: "45024684"
---
# <a name="work-with-custodians-and-non-custodial-data-sources-in-advanced-ediscovery"></a><span data-ttu-id="74244-103">Utilisation de conservateurs et de sources de données non privatives de ressources dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="74244-103">Work with custodians and non-custodial data sources in Advanced eDiscovery</span></span>

<span data-ttu-id="74244-104">Lorsqu’une organisation répond à une enquête légale, le flux de travail concernant l’identification, la préservation et la collecte de contenu potentiellement pertinent est basé sur les personnes de l’organisation qui sont des dépositaires de données pertinentes.</span><span class="sxs-lookup"><span data-stu-id="74244-104">When an organization responds to a legal investigation, the workflow around identifying, preserving, and collecting potentially relevant content is based on the people in the organization who are the custodians of relevant data.</span></span> <span data-ttu-id="74244-105">Dans eDiscovery, ces individus sont appelés « *dépositaires de données* » (ou simplement des *dépositaires*) et sont définis en tant que « personnes ayant le contrôle administratif d’un document ou d’un fichier électronique ».</span><span class="sxs-lookup"><span data-stu-id="74244-105">In eDiscovery, these individuals are called *data custodians* (or just *custodians*) and are defined as "persons having administrative control of a document or electronic file".</span></span> <span data-ttu-id="74244-106">Par exemple, le dépositaire d’un message électronique peut être le propriétaire de la boîte aux lettres qui contient le message pertinent.</span><span class="sxs-lookup"><span data-stu-id="74244-106">For example, the custodian of an email message could be the owner of the mailbox that contains the relevant message.</span></span>

<span data-ttu-id="74244-107">De plus, il peut y avoir du contenu dans les boîtes aux lettres et les sites qui ne sont pas associés à un dépositaire, mais cela est pertinent pour le cas.</span><span class="sxs-lookup"><span data-stu-id="74244-107">Additionally, there may be content located in mailboxes and sites that aren't associated with a custodian but that's relevant to the case.</span></span> <span data-ttu-id="74244-108">Pour différencier les emplacements de contenu lorsque les dépositaires de cas ne disposent pas d’un contrôle administratif mais peuvent contenir des données pertinentes, ces sources sont connues sous le nom de *sources de données non privatives*de privilèges.</span><span class="sxs-lookup"><span data-stu-id="74244-108">To differentiate content locations where case custodians don't have administrative control but may contain relevant data, these are known as *non-custodial data sources*.</span></span>

<span data-ttu-id="74244-109">Dans un cas avancé eDiscovery, les équipes juridiques peuvent ajouter des personnes au sein de leur organisation en tant que dépositaires, et identifier et conserver automatiquement des sources de données privatives de ressources telles que des boîtes aux lettres Exchange, des comptes OneDrive et des sites SharePoint et Teams.</span><span class="sxs-lookup"><span data-stu-id="74244-109">In an Advanced eDiscovery case, legal teams can add individuals in their organization as custodians, and automatically identify and preserve custodial data sources such as Exchange mailboxes, OneDrive accounts, and SharePoint and Teams sites.</span></span> <span data-ttu-id="74244-110">Ils peuvent également identifier et conserver des sources de données non privatives de cœur.</span><span class="sxs-lookup"><span data-stu-id="74244-110">They can also identify and preserve non-custodial data sources.</span></span> <span data-ttu-id="74244-111">En utilisant l’outil de gestion des sources de données et des dépositaires intégré dans Advanced eDiscovery, les organisations peuvent sécuriser les informations stockées électroniquement par une suppression involontaire (ou intentionnelle).</span><span class="sxs-lookup"><span data-stu-id="74244-111">By using the built-in custodian and data source management tool in Advanced eDiscovery, organizations can secure electronically stored information from inadvertent (or intentional) deletion.</span></span> <span data-ttu-id="74244-112">Cela vous permet d’éliminer le processus de conservation du temps et source d’erreurs qui nécessite une utilisation manuelle.</span><span class="sxs-lookup"><span data-stu-id="74244-112">This lets you eliminate the time-consuming and error-prone process of manually having to perform the legal hold processes.</span></span>

<span data-ttu-id="74244-113">Pour plus d’informations sur l’utilisation des dépositaires, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="74244-113">For more information about working with custodians, see the following:</span></span>

- [<span data-ttu-id="74244-114">Ajouter des consignataires à un cas</span><span class="sxs-lookup"><span data-stu-id="74244-114">Add custodians to a case</span></span>](add-custodians-to-case.md)

- [<span data-ttu-id="74244-115">Ajouter des dépositaires en bloc à un cas</span><span class="sxs-lookup"><span data-stu-id="74244-115">Bulk-add custodians to a case</span></span>](bulk-add-custodians.md)

- [<span data-ttu-id="74244-116">Gestion des dépositaires dans un cas</span><span class="sxs-lookup"><span data-stu-id="74244-116">Manage custodians in a case</span></span>](manage-new-custodians.md)

- [<span data-ttu-id="74244-117">Afficher l’activité des consignataires</span><span class="sxs-lookup"><span data-stu-id="74244-117">View custodian activity</span></span>](view-custodian-activity.md)

- [<span data-ttu-id="74244-118">Ajout de sources de données non privatives de Troie à un cas</span><span class="sxs-lookup"><span data-stu-id="74244-118">Add non-custodial data sources to a case</span></span>](non-custodial-data-sources.md)
