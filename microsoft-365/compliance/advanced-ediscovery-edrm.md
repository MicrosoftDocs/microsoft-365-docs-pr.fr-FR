---
title: Alignement eDiscovery avancé avec l’EDRM
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
- m365solution-aed
- m365initiative-compliance
search.appverid:
- MOE150
- MET150
description: Le flux de travail intégré d’Advanced eDiscovery dans Microsoft 365 s’aligne sur le processus eDiscovery décrit par le modèle de référence de découverte électronique (EDRM).
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 4ca94baf1fc57ac014a32a80ddc5705feeb2c842
ms.sourcegitcommit: 83a40facd66e14343ad3ab72591cab9c41ce6ac0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/13/2021
ms.locfileid: "49841610"
---
# <a name="advanced-ediscovery-alignment-with-the-electronic-discovery-reference-model"></a><span data-ttu-id="74b15-103">Alignement advanced eDiscovery avec le modèle de référence de découverte électronique</span><span class="sxs-lookup"><span data-stu-id="74b15-103">Advanced eDiscovery alignment with the Electronic Discovery Reference Model</span></span>

<span data-ttu-id="74b15-104">Le flux de travail intégré d’Advanced eDiscovery dans Microsoft 365 s’aligne sur le processus eDiscovery décrit par le modèle de référence de découverte électronique (EDRM).</span><span class="sxs-lookup"><span data-stu-id="74b15-104">The built-in workflow of Advanced eDiscovery in Microsoft 365 aligns with the eDiscovery process outlined by the Electronic Discovery Reference Model (EDRM).</span></span>

![Modèle de référence de découverte électronique (EDRM)](../media/EDRMv1.png)

<span data-ttu-id="74b15-106">(Image source fournie par edrm.net.</span><span class="sxs-lookup"><span data-stu-id="74b15-106">(Image source courtesy of edrm.net.</span></span> <span data-ttu-id="74b15-107">L’image source a été rendue disponible sous Creative Commons Attribution 3.0 Unported License.)</span><span class="sxs-lookup"><span data-stu-id="74b15-107">The source image was made available under Creative Commons Attribution 3.0 Unported License.)</span></span>

<span data-ttu-id="74b15-108">À un niveau élevé, voici comment Advanced eDiscovery prend en charge le flux de travail EDRM :</span><span class="sxs-lookup"><span data-stu-id="74b15-108">At a high level, here's how Advanced eDiscovery supports the EDRM workflow:</span></span>

- <span data-ttu-id="74b15-109">**Identification.**</span><span class="sxs-lookup"><span data-stu-id="74b15-109">**Identification.**</span></span> <span data-ttu-id="74b15-110">Après avoir identifié les personnes potentielles concernées par une enquête, vous pouvez les ajouter en tant que dépositaires (également *appelés dépositaires* de données, car elles peuvent détenir des informations pertinentes pour l’enquête) à un cas Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="74b15-110">After you identify potential persons of interest in an investigation, you can add them as custodians (also called *data custodians*, because they may possess information that's relevant to the investigation) to an Advanced eDiscovery case.</span></span> <span data-ttu-id="74b15-111">Une fois que les utilisateurs sont ajoutés en tant que dépositaires, il est facile de conserver, de collecter et de réviser les documents des dépositaires.</span><span class="sxs-lookup"><span data-stu-id="74b15-111">After users are added as custodians, it's easy to preserve, collect, and review custodian documents.</span></span>

- <span data-ttu-id="74b15-112">**Conservation.**</span><span class="sxs-lookup"><span data-stu-id="74b15-112">**Preservation.**</span></span> <span data-ttu-id="74b15-113">Pour conserver et protéger les données pertinentes pour un examen, Advanced eDiscovery vous permet de placer une conservation légale sur les sources de données associées aux dépositaires dans un cas.</span><span class="sxs-lookup"><span data-stu-id="74b15-113">To preserve and protect data that's relevant to an investigation, Advanced eDiscovery lets you place a legal hold on the data sources associated with the custodians in a case.</span></span> <span data-ttu-id="74b15-114">Vous pouvez également placer les données non privatives en attente.</span><span class="sxs-lookup"><span data-stu-id="74b15-114">You can also place non-custodial data on hold.</span></span> <span data-ttu-id="74b15-115">Advanced eDiscovery dispose également d’un flux de travail de communications intégré qui vous permet d’envoyer des notifications de conservation légale aux dépositaires et de suivre leurs accusés de réception.</span><span class="sxs-lookup"><span data-stu-id="74b15-115">Advanced eDiscovery also has a built-in communications workflow so you can send legal hold notifications to custodians and track their acknowledgments.</span></span>

- <span data-ttu-id="74b15-116">**Collection.**</span><span class="sxs-lookup"><span data-stu-id="74b15-116">**Collection.**</span></span> <span data-ttu-id="74b15-117">Après avoir identifié (et conservé) les sources de données pertinentes pour l’examen, vous pouvez utiliser l’outil de recherche intégré dans advanced eDiscovery pour rechercher et collecter des données en direct à partir des sources de données récupérables (et des sources de données non privatives, le cas échéant) qui peuvent être pertinentes pour le cas.</span><span class="sxs-lookup"><span data-stu-id="74b15-117">After you identified (and preserved) the data sources relevant to the investigation, you can use the built-in search tool in Advanced eDiscovery search for and collect live data from the custodial data sources (and non-custodial data sources, if applicable) that may be relevant to the case.</span></span>

- <span data-ttu-id="74b15-118">**Traitement.**</span><span class="sxs-lookup"><span data-stu-id="74b15-118">**Processing.**</span></span> <span data-ttu-id="74b15-119">Une fois que vous avez collecté toutes les données pertinentes pour le cas, l’étape suivante consiste à les traiter pour une analyse et un examen approfondis.</span><span class="sxs-lookup"><span data-stu-id="74b15-119">After you've collected all data relevant to the case, the next step is process it for further review and analysis.</span></span> <span data-ttu-id="74b15-120">Dans Advanced eDiscovery, les données sur place que vous avez identifiées lors de la phase de collecte sont copiées dans un emplacement de stockage Azure (appelé ensemble de *révision),* ce qui vous fournit une vue statique des données de cas.</span><span class="sxs-lookup"><span data-stu-id="74b15-120">In Advanced eDiscovery, the in-place data that you identified in the collection phase is copied to an Azure Storage location (called a *review set*), which provides you with a static view of the case data.</span></span> 

- <span data-ttu-id="74b15-121">**Révision.**</span><span class="sxs-lookup"><span data-stu-id="74b15-121">**Review.**</span></span> <span data-ttu-id="74b15-122">Une fois que les données ont été ajoutées à un jeu à réviser, vous pouvez afficher des documents spécifiques et exécuter des requêtes supplémentaires pour réduire les données à ce qui est le plus pertinent pour le cas.</span><span class="sxs-lookup"><span data-stu-id="74b15-122">After data has been added to a review set, you can view specific documents and run additional queries to reduce the data to what is most relevant to the case.</span></span> <span data-ttu-id="74b15-123">Peut également annoter et baliser des documents spécifiques.</span><span class="sxs-lookup"><span data-stu-id="74b15-123">Also, can annotate and tag specific documents.</span></span>

- <span data-ttu-id="74b15-124">**Analyse.**</span><span class="sxs-lookup"><span data-stu-id="74b15-124">**Analysis.**</span></span> <span data-ttu-id="74b15-125">Advanced eDiscovery fournit un outil d’analyse intégré qui vous permet d’annuler davantage les données du jeu à réviser que vous déterminez ne sont pas pertinentes pour l’examen.</span><span class="sxs-lookup"><span data-stu-id="74b15-125">Advanced eDiscovery provides integrated analytics tool that helps you further cull data from the review set that you determine isn't relevant to the investigation.</span></span> <span data-ttu-id="74b15-126">En plus de réduire le volume de données pertinentes, Advance eDiscovery vous permet également d’économiser des coûts de révision juridique en vous permettant d’organiser le contenu afin de simplifier et d’améliorer l’efficacité du processus de révision.</span><span class="sxs-lookup"><span data-stu-id="74b15-126">In addition to reducing the volume of relevant data, Advance eDiscovery also helps you save legal review costs by letting you organize content to make the review process easier and more efficient.</span></span>

- <span data-ttu-id="74b15-127">**Production** et **présentation.**</span><span class="sxs-lookup"><span data-stu-id="74b15-127">**Production** and **Presentation.**</span></span> <span data-ttu-id="74b15-128">Lorsque vous êtes prêt, vous pouvez exporter des documents à partir d’un groupe de révision pour révision légale.</span><span class="sxs-lookup"><span data-stu-id="74b15-128">When you're ready, you can export documents from a review set for legal review.</span></span> <span data-ttu-id="74b15-129">Vous pouvez exporter des documents dans leur format natif ou dans un format EDRM spécifié afin qu’ils soient importés dans des applications de révision tierces.</span><span class="sxs-lookup"><span data-stu-id="74b15-129">You can export documents in their native format or in an EDRM-specified format so they can be imported into third-party review applications.</span></span>

## <a name="more-information"></a><span data-ttu-id="74b15-130">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="74b15-130">More information</span></span>

<span data-ttu-id="74b15-131">Pour commencer à utiliser Advanced eDiscovery, voir :</span><span class="sxs-lookup"><span data-stu-id="74b15-131">To get started using Advanced eDiscovery, see:</span></span>

- [<span data-ttu-id="74b15-132">Configurer Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="74b15-132">Set up Advanced eDiscovery</span></span>](get-started-with-advanced-ediscovery.md)

- [<span data-ttu-id="74b15-133">Créer et gérer un cas Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="74b15-133">Create and manage an Advanced eDiscovery case</span></span>](create-and-manage-advanced-ediscoveryv2-case.md)