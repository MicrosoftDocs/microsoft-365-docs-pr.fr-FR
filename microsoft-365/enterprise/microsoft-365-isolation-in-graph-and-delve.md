---
title: Isolation du client Microsoft 365 dans Microsoft Graph et Delve
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
f1.keywords:
- NOCSH
description: Dans cet article, vous trouverez une explication sur la façon dont l’isolation du client Microsoft 365 fonctionne dans Office Graph et dans Delve.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: ab9b216656e076cc3ba02a4ef6c75b25b94547fe
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46689949"
---
# <a name="microsoft-365-tenant-isolation-in-the-microsoft-graph-and-delve"></a><span data-ttu-id="b6dee-103">Isolation du client Microsoft 365 dans Microsoft Graph et Delve</span><span class="sxs-lookup"><span data-stu-id="b6dee-103">Microsoft 365 Tenant Isolation in the Microsoft Graph and Delve</span></span>

## <a name="tenant-isolation-in-the-microsoft-graph"></a><span data-ttu-id="b6dee-104">Isolation du client dans Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="b6dee-104">Tenant Isolation in the Microsoft Graph</span></span>

<span data-ttu-id="b6dee-105">Activité des modèles [Microsoft Graph](https://developer.microsoft.com/graph) dans les services Microsoft 365, y compris Exchange Online, SharePoint Online, Yammer, Skype entreprise, Azure Active Directory, etc., et dans les services externes, tels que les autres services Microsoft ou services tiers.</span><span class="sxs-lookup"><span data-stu-id="b6dee-105">The [Microsoft Graph](https://developer.microsoft.com/graph) models activity in Microsoft 365 services, including Exchange Online, SharePoint Online, Yammer, Skype for Business, Azure Active Directory, and more, and in external services, such as other Microsoft services or third-party services.</span></span> <span data-ttu-id="b6dee-106">Les composants Microsoft Graph sont utilisés dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b6dee-106">Microsoft Graph components are used throughout Microsoft 365.</span></span> <span data-ttu-id="b6dee-107">Microsoft Graph représente une collection de contenu et d’activité, ainsi que les relations entre ceux-ci dans l’ensemble de la suite Office.</span><span class="sxs-lookup"><span data-stu-id="b6dee-107">The Microsoft Graph represents a collection of content and activity, and the relationships between them that happen across the entire Office suite.</span></span> <span data-ttu-id="b6dee-108">Il utilise des techniques d’apprentissage automatique sophistiquées pour connecter des personnes au contenu, aux conversations et aux personnes qui les entourent.</span><span class="sxs-lookup"><span data-stu-id="b6dee-108">It uses sophisticated machine learning techniques to connect people to the relevant content, conversations and people around them.</span></span> <span data-ttu-id="b6dee-109">Par exemple, l’index client dans SharePoint Online a un index Microsoft Graph utilisé pour traiter les requêtes de recherche, le moteur de traitement de l’analyse dans SharePoint Online est utilisé pour stocker les signaux et calculer les informations, et Exchange Online calcule le cache de destinataires de chaque utilisateur comme entrée dans l’analyse de client.</span><span class="sxs-lookup"><span data-stu-id="b6dee-109">For example, the tenant index in SharePoint Online has an Microsoft Graph index that is used to serve Delve queries, the Analytics Processing Engine in SharePoint Online is used to store signals and calculate insights, and Exchange Online calculates each user's recipient cache as input into tenant analytics.</span></span>

<span data-ttu-id="b6dee-110">Microsoft Graph contient des informations sur les objets d’entreprise, tels que les personnes et les documents, ainsi que sur les relations et les interactions entre ces objets.</span><span class="sxs-lookup"><span data-stu-id="b6dee-110">The Microsoft Graph contains information about enterprise objects, such as people and documents, as well as the relationships and interactions among these objects.</span></span> <span data-ttu-id="b6dee-111">Les relations et les interactions sont représentées par des *connexions*.</span><span class="sxs-lookup"><span data-stu-id="b6dee-111">The relationships and interactions are represented as *edges*.</span></span> <span data-ttu-id="b6dee-112">Microsoft Graph est segmenté par client, de sorte que les bords ne peuvent exister qu’entre les *nœuds* du même client.</span><span class="sxs-lookup"><span data-stu-id="b6dee-112">The Microsoft Graph is segmented by tenant such that edges can only exist between *nodes* in the same tenancy.</span></span> <span data-ttu-id="b6dee-113">Un *nœud* est une entité avec un URI (Uniform Resource Identifier), un type de nœud, une liste de contrôle d’accès et un ensemble de facettes contenant des *métadonnées* et des bords.</span><span class="sxs-lookup"><span data-stu-id="b6dee-113">A *node* is an entity with a Uniform Resource Identifier (URI), node type, access control list, and a set of facets containing *metadata* and edges.</span></span> <span data-ttu-id="b6dee-114">Chaque nœud est associé à des métadonnées et des bords, organisés en *facettes* comme dans le modèle de connaissances commun.</span><span class="sxs-lookup"><span data-stu-id="b6dee-114">Each node has associated metadata and edges, arranged into *facets* as in the Common Knowledge Model.</span></span> <span data-ttu-id="b6dee-115">Les *métadonnées* sont nommées les propriétés stockées sur un nœud qui peuvent être utilisées pour la recherche, le filtrage ou l’analyse dans Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="b6dee-115">*Metadata* are named properties stored on a node which can be used for searching, filtering, or analysis within the Microsoft Graph.</span></span> <span data-ttu-id="b6dee-116">Une *facette* est une collection logique de métadonnées et de bords sur un nœud.</span><span class="sxs-lookup"><span data-stu-id="b6dee-116">A *facet* is a logical collection of metadata and edges on a node.</span></span> <span data-ttu-id="b6dee-117">Chaque facette décrit un aspect d’un nœud.</span><span class="sxs-lookup"><span data-stu-id="b6dee-117">Each facet describes one aspect of a node.</span></span> 

<span data-ttu-id="b6dee-118">Microsoft Graph ne place pas toutes les données dans un seul référentiel ; au lieu de cela, il stocke les métadonnées et les relations relatives aux données qui se trouvent ailleurs.</span><span class="sxs-lookup"><span data-stu-id="b6dee-118">The Microsoft Graph does not bring all the data into a single repository; rather, it stores metadata and relationships about data that lives elsewhere.</span></span> <span data-ttu-id="b6dee-119">Microsoft Graph est constitué de plusieurs magasins de données et composants de traitement :</span><span class="sxs-lookup"><span data-stu-id="b6dee-119">The Microsoft Graph consists of several data stores and processing components:</span></span>

- <span data-ttu-id="b6dee-120">Le magasin Graph de client offre un stockage en bloc optimisé pour une analyse efficace.</span><span class="sxs-lookup"><span data-stu-id="b6dee-120">The Tenant Graph Store provides bulk storage optimized for efficient analytics.</span></span>
- <span data-ttu-id="b6dee-121">Le cache de contenu actif offre un accès aléatoire rapide aux nœuds actifs et aux périphéries pour conduire les expériences utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b6dee-121">The Active Content Cache provides quick random access to active node and edges to drive user experiences.</span></span>
- <span data-ttu-id="b6dee-122">Le routeur d’entrée avertit les composants internes et externes des modifications apportées au graphique client.</span><span class="sxs-lookup"><span data-stu-id="b6dee-122">The input router notifies components internal and external of changes to the tenant graph.</span></span>

<span data-ttu-id="b6dee-123">L’analyse de chaque charge de travail déduit des informations pertinentes pour les calculs à l’échelle du client et les achemine vers le graphique client.</span><span class="sxs-lookup"><span data-stu-id="b6dee-123">Analytics within each workload deduce insights relevant to the tenant-wide calculations and push them to the tenant graph.</span></span> <span data-ttu-id="b6dee-124">Des raisons d’analyse de client pour toutes les activités d’un client pour produire des idées dans des modèles de comportement.</span><span class="sxs-lookup"><span data-stu-id="b6dee-124">Tenant analytics reasons over all activity in a tenancy to produce insights into patterns of behavior.</span></span> <span data-ttu-id="b6dee-125">Par exemple, Exchange Online calcule le cache de destinataires de chaque utilisateur avec une analyse de la boîte aux lettres de chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b6dee-125">For example, Exchange Online calculates the recipient cache for each user with analytics that efficiently reason over each user's mailbox.</span></span> <span data-ttu-id="b6dee-126">Ces analyses par utilisateur produisent un ensemble de *périphéries RecipientCache* sur chaque personne, qui sont ensuite envoyées au graphique client.</span><span class="sxs-lookup"><span data-stu-id="b6dee-126">These per-user analytics produce a set of *RecipientCache Edges* on each person, which are in turn pushed to the tenant graph.</span></span> <span data-ttu-id="b6dee-127">Cela permet de conserver la plus grande partie du traitement de l’analyse aussi près que possible des données sources.</span><span class="sxs-lookup"><span data-stu-id="b6dee-127">This keeps the as much of the analytics processing as close to the source data as possible.</span></span>

## <a name="tenant-isolation-in-delve"></a><span data-ttu-id="b6dee-128">Isolation du client dans Delve</span><span class="sxs-lookup"><span data-stu-id="b6dee-128">Tenant Isolation in Delve</span></span>

<span data-ttu-id="b6dee-129">Comme mentionné précédemment, Microsoft Graph fournit des expériences qui aident les utilisateurs à découvrir et à collaborer sur les activités actuelles dans leur entreprise, et fournit une plateforme centrée sur l’entité pour les analyses pour des raisons de contenu et d’activité sur les charges de travail et au-delà de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b6dee-129">As mentioned previously, the Microsoft Graph powers experiences that help people discover and collaborate on current activities in their enterprise, and provides an entity-centric platform for analytics to reason over content and activity across workloads and beyond Microsoft 365.</span></span> <span data-ttu-id="b6dee-130">Delve est la première expérience de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="b6dee-130">Delve is the first such experience powered by the Microsoft Graph.</span></span>
<span data-ttu-id="b6dee-131">Delve est une expérience Web Microsoft 365 qui couvre le contenu de Microsoft 365 et Yammer Enterprise vers les utilisateurs de Microsoft 365 via Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="b6dee-131">Delve is a Microsoft 365 web experience that surfaces content from Microsoft 365 and Yammer Enterprise to Microsoft 365 users via the Microsoft Graph.</span></span> <span data-ttu-id="b6dee-132">L’expérience Web affiche les données sous la forme de différentes cartes, chacune comportant une rubrique particulière, telle que la *tendance à moi* ou *modifiée par moi*.</span><span class="sxs-lookup"><span data-stu-id="b6dee-132">The web experience displays data as different boards, each with a certain topic, such as *Trending around me* or *Modified by me*.</span></span> <span data-ttu-id="b6dee-133">Chaque carte se compose de plusieurs cartes de document qui affichent un texte de synthèse et une image du document.</span><span class="sxs-lookup"><span data-stu-id="b6dee-133">Each board consists of several document cards that display summary text and a picture from the document.</span></span> <span data-ttu-id="b6dee-134">La carte permet aux utilisateurs d’effectuer des actions comme ouvrir le document ou une page Yammer pour le document.</span><span class="sxs-lookup"><span data-stu-id="b6dee-134">The card lets users do things like open the document or a Yammer page for the document.</span></span> <span data-ttu-id="b6dee-135">Il existe une page pour chaque personne d’un client Microsoft 365 qui affiche les documents les plus pertinents pour cette personne, ainsi que les icônes qui peuvent appeler Exchange Online ou Skype entreprise pour interagir avec cette personne.</span><span class="sxs-lookup"><span data-stu-id="b6dee-135">There is a page for each person in a Microsoft 365 tenant that displays the most relevant documents for this person, and icons that can invoke Exchange Online or Skype for Business for interacting with that person.</span></span> <span data-ttu-id="b6dee-136">Étant donné que Delve est basé sur l’API Microsoft Graph, il est lié par l’isolation basée sur le client de cette API.</span><span class="sxs-lookup"><span data-stu-id="b6dee-136">Because Delve is based on the Microsoft Graph API, it is bound by the tenant-based isolation of that API.</span></span>