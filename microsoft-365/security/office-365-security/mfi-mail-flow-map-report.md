---
title: Carte de flux de messagerie
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs peuvent apprendre à utiliser la carte de flux de messagerie dans le tableau de bord de flux de messagerie dans le centre de sécurité & conformité pour visualiser et suivre la façon dont les messages circulent vers et depuis leur organisation via des connecteurs et sans utiliser de connecteurs.
ms.openlocfilehash: 2996227de3e0141635522ada4e41f2e8e65e9040
ms.sourcegitcommit: c04f1207cfaddac2a9abef38967c17d689756a96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2020
ms.locfileid: "46577695"
---
# <a name="mail-flow-map-in-the-security--compliance-center"></a><span data-ttu-id="446eb-103">Carte de flux de messagerie dans le centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="446eb-103">Mail flow map in the Security & Compliance Center</span></span>

<span data-ttu-id="446eb-104">La **carte de flux de messagerie** dans le [tableau de bord de flux de messagerie](mail-flow-insights-v2.md) dans le centre de sécurité & conformité offre un aperçu de la façon dont les messages circulent dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="446eb-104">The **Mail flow map** in the [Mail flow dashboard](mail-flow-insights-v2.md) in the Security & Compliance Center gives insight as to how mail flows through your organization.</span></span> <span data-ttu-id="446eb-105">Vous pouvez utiliser ces informations pour apprendre des modèles, identifier des anomalies et corriger les problèmes au fur et à mesure qu’ils se produisent.</span><span class="sxs-lookup"><span data-stu-id="446eb-105">You can use this information to learn patterns, identify anomalies, and fix issues as they occur.</span></span>

![Widget carte de flux de messagerie dans le tableau de bord de flux de messagerie dans le centre de sécurité & conformité](../../media/mfi-mail-flow-map-widget.png)

<span data-ttu-id="446eb-107">Par défaut, le widget affiche le modèle de flux de messagerie du jour précédent dans un graphique appelé diagramme *Sankey* .</span><span class="sxs-lookup"><span data-stu-id="446eb-107">By default, the widget shows the mail flow pattern from the previous day in a chart known as a *Sankey* diagram.</span></span> <span data-ttu-id="446eb-108">Vous pouvez utiliser la flèche gauche et la flèche droite ![ ](../../media/scc-left-arrow.png) ![ ](../../media/scc-right-arrow.png) pour afficher les informations de jours différents.</span><span class="sxs-lookup"><span data-stu-id="446eb-108">You can use the left arrow ![Left arrow](../../media/scc-left-arrow.png) and right arrow ![Right arrow](../../media/scc-right-arrow.png) to show information from different days.</span></span> <span data-ttu-id="446eb-109">Chaque couleur représente le flux de messagerie sur un connecteur entrant ou sortant différent (ou sans connecteurs).</span><span class="sxs-lookup"><span data-stu-id="446eb-109">Each different color represents mail flow over a different inbound or outbound connector (or without using connectors).</span></span> <span data-ttu-id="446eb-110">Si vous placez le curseur de la souris sur une couleur spécifique, le nombre de messages s’affiche pour ce type de connecteur.</span><span class="sxs-lookup"><span data-stu-id="446eb-110">If you hover over a specific color, the number of messages is displayed for that type of connector.</span></span>

## <a name="report-view-for-the-mail-flow-map"></a><span data-ttu-id="446eb-111">Affichage de rapport pour la carte de flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="446eb-111">Report view for the Mail flow map</span></span>

<span data-ttu-id="446eb-112">Cliquez sur le widget **carte de flux de messagerie** pour accéder au rapport de carte de flux de **messagerie** .</span><span class="sxs-lookup"><span data-stu-id="446eb-112">Clicking on the **Mail flow map** widget will take you to the **Mail flow map** report.</span></span>

<span data-ttu-id="446eb-113">Les graphiques suivants sont disponibles dans l’affichage rapport :</span><span class="sxs-lookup"><span data-stu-id="446eb-113">The following charts are available in the report view:</span></span>

- <span data-ttu-id="446eb-114">**Afficher les données de : vue d’ensemble**: il s’agit fondamentalement d’un affichage plus large du widget.</span><span class="sxs-lookup"><span data-stu-id="446eb-114">**Show data for: Overview**: This is basically a larger view of the widget.</span></span> <span data-ttu-id="446eb-115">Si vous placez le curseur de la souris sur une couleur spécifique, le nombre de messages s’affiche pour ce type de connecteur.</span><span class="sxs-lookup"><span data-stu-id="446eb-115">If you hover over a specific color, the number of messages is displayed for that type of connector.</span></span>

  ![Vue d’ensemble dans le rapport de carte de flux de messagerie](../../media/mfi-mail-flow-map-report-overview.png)

- <span data-ttu-id="446eb-117">**Afficher les données pour : Detail**: cette vue affiche des détails sur les connecteurs et les domaines de destination.</span><span class="sxs-lookup"><span data-stu-id="446eb-117">**Show data for: Detail**: This view shows details about the connectors and destination domains.</span></span> <span data-ttu-id="446eb-118">Les principaux domaines expéditeur et destinataire sont répertoriés et les autres sont placés dans **d’autres**.</span><span class="sxs-lookup"><span data-stu-id="446eb-118">The top sender and recipient domains are listed, and the rest are put in **Others**.</span></span> <span data-ttu-id="446eb-119">Si vous placez le curseur de la souris sur une couleur et une section spécifiques, le nombre de messages s’affiche.</span><span class="sxs-lookup"><span data-stu-id="446eb-119">If you hover over a specific color and section, the number of messages is displayed.</span></span>

  ![Affichage détaillé dans le rapport de carte de flux de messagerie](../../media/mfi-mail-flow-map-report-detail.png)

<span data-ttu-id="446eb-121">Si vous cliquez sur **filtres** dans un affichage de rapport, vous pouvez spécifier une plage de dates avec **Date de début** et date de **fin**.</span><span class="sxs-lookup"><span data-stu-id="446eb-121">If you click **Filters** in a report view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="446eb-122">Pour envoyer par courrier électronique le rapport pour une plage de dates spécifique à un ou plusieurs destinataires, cliquez sur **demander un téléchargement**.</span><span class="sxs-lookup"><span data-stu-id="446eb-122">To email the report for a specific date range to one or more recipients, click **Request download**.</span></span>

<span data-ttu-id="446eb-123">Les informations associées s’affichent sous la carte de flux de messagerie si elles sont disponibles (par exemple, l’analyseur de la [boucle de messagerie possible](mfi-mail-loop-insight.md)).</span><span class="sxs-lookup"><span data-stu-id="446eb-123">Related insights are shown beneath the Mail flow map if they're available (for example, the [Fix possible mail loop insight](mfi-mail-loop-insight.md)).</span></span>

## <a name="details-table-view-for-the-mail-flow-map"></a><span data-ttu-id="446eb-124">Vue de la table des détails pour la carte de flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="446eb-124">Details table view for the Mail flow map</span></span>

<span data-ttu-id="446eb-125">Si vous cliquez sur **afficher la table des détails** dans un affichage de rapport, les informations suivantes s’affichent :</span><span class="sxs-lookup"><span data-stu-id="446eb-125">If you click **View details table** in a report view, the following information is shown:</span></span>

- <span data-ttu-id="446eb-126">**Date**</span><span class="sxs-lookup"><span data-stu-id="446eb-126">**Date**</span></span>
- <span data-ttu-id="446eb-127">**Catégorie**</span><span class="sxs-lookup"><span data-stu-id="446eb-127">**Category**</span></span>
- <span data-ttu-id="446eb-128">**Connecteur/fournisseur de services tiers**</span><span class="sxs-lookup"><span data-stu-id="446eb-128">**Connector / Third-party service provider**</span></span>
- <span data-ttu-id="446eb-129">**Domaine de l’expéditeur/du destinataire**</span><span class="sxs-lookup"><span data-stu-id="446eb-129">**Sender/Recipient domain**</span></span>
- <span data-ttu-id="446eb-130">**Nombre de messages**</span><span class="sxs-lookup"><span data-stu-id="446eb-130">**Message count**</span></span>

<span data-ttu-id="446eb-131">Si vous cliquez sur **filtres** dans un affichage tableau détaillé, vous pouvez spécifier une plage de dates avec **Date de début** et date de **fin**.</span><span class="sxs-lookup"><span data-stu-id="446eb-131">If you click **Filters** in a details table view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="446eb-132">Si vous sélectionnez une ligne, des détails similaires s’affichent dans un menu volant :</span><span class="sxs-lookup"><span data-stu-id="446eb-132">If you select a row, similar details are shown in a flyout:</span></span>

![Fenêtre mobile détails à partir de la table Détails dans la carte de flux de messagerie](../../media/mfi-mail-flow-map-view-details-table-details.png)

<span data-ttu-id="446eb-134">Pour envoyer par courrier électronique le rapport pour une plage de dates spécifique à un ou plusieurs destinataires, cliquez sur **demander un téléchargement**.</span><span class="sxs-lookup"><span data-stu-id="446eb-134">To email the report for a specific date range to one or more recipients, click **Request download**.</span></span>

<span data-ttu-id="446eb-135">Pour revenir à l’affichage rapports, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="446eb-135">To go back to the reports view, click **View report**.</span></span>

## <a name="see-also"></a><span data-ttu-id="446eb-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="446eb-136">See also</span></span>

<span data-ttu-id="446eb-137">Pour plus d’informations sur les autres informations du tableau de bord de flux de messagerie, consultez [la rubrique mail Flow Insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span><span class="sxs-lookup"><span data-stu-id="446eb-137">For information about other insights in the Mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
