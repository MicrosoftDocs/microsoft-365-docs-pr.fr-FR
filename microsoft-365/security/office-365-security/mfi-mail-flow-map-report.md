---
title: Carte du flux de courriers
f1.keywords:
- NOCSH
ms.author: siosulli
author: siosulli
manager: dansimp
audience: ITPro
ms.topic: conceptual
localization_priority: Normal
ms.assetid: ''
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs peuvent apprendre à utiliser le plan de flux de messagerie dans le tableau de bord du flux de messagerie dans le Centre de sécurité & conformité pour visualiser et suivre la façon dont les messages circulent vers et depuis leur organisation via des connecteurs et sans utiliser de connecteurs.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 6e806dde2e6f3ddde5cce3b61c85fe0b024ba2fe
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51204929"
---
# <a name="mail-flow-map-in-the-security--compliance-center"></a><span data-ttu-id="2ffee-103">Carte de flux de messagerie dans le Centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="2ffee-103">Mail flow map in the Security & Compliance Center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="2ffee-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="2ffee-104">**Applies to**</span></span>
- [<span data-ttu-id="2ffee-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="2ffee-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="2ffee-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="2ffee-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="2ffee-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="2ffee-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="2ffee-108">Le plan de [](mail-flow-insights-v2.md) flux de **messagerie** dans le tableau de bord de flux de messagerie du Centre de sécurité & [conformité](https://protection.office.com) donne des informations sur la façon dont le courrier circule dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="2ffee-108">The **Mail flow map** in the [Mail flow dashboard](mail-flow-insights-v2.md) in the [Security & Compliance Center](https://protection.office.com) gives insight as to how mail flows through your organization.</span></span> <span data-ttu-id="2ffee-109">Vous pouvez utiliser ces informations pour apprendre des modèles, identifier des anomalies et résoudre les problèmes au moment où ils se produisent.</span><span class="sxs-lookup"><span data-stu-id="2ffee-109">You can use this information to learn patterns, identify anomalies, and fix issues as they occur.</span></span>

![Widget de carte de flux de messagerie dans le tableau de bord de flux de messagerie dans le Centre de sécurité & conformité](../../media/mfi-mail-flow-map-widget.png)

<span data-ttu-id="2ffee-111">Par défaut, le widget affiche le modèle de flux de messagerie du jour précédent dans un graphique appelé *diagramme Sankey.*</span><span class="sxs-lookup"><span data-stu-id="2ffee-111">By default, the widget shows the mail flow pattern from the previous day in a chart known as a *Sankey* diagram.</span></span> <span data-ttu-id="2ffee-112">Vous pouvez utiliser la flèche gauche et la flèche droite pour afficher les informations de ![ ](../../media/scc-left-arrow.png) différents ![ ](../../media/scc-right-arrow.png) jours.</span><span class="sxs-lookup"><span data-stu-id="2ffee-112">You can use the left arrow ![Left arrow](../../media/scc-left-arrow.png) and right arrow ![Right arrow](../../media/scc-right-arrow.png) to show information from different days.</span></span> <span data-ttu-id="2ffee-113">Chaque couleur représente le flux de messagerie sur un connecteur entrant ou sortant différent (ou sans utiliser de connecteurs).</span><span class="sxs-lookup"><span data-stu-id="2ffee-113">Each different color represents mail flow over a different inbound or outbound connector (or without using connectors).</span></span> <span data-ttu-id="2ffee-114">Si vous pointez sur une couleur spécifique, le nombre de messages s’affiche pour ce type de connecteur.</span><span class="sxs-lookup"><span data-stu-id="2ffee-114">If you hover over a specific color, the number of messages is displayed for that type of connector.</span></span>

## <a name="report-view-for-the-mail-flow-map"></a><span data-ttu-id="2ffee-115">Affichage de rapport pour le map point de flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="2ffee-115">Report view for the Mail flow map</span></span>

<span data-ttu-id="2ffee-116">En cliquant sur le widget de **carte de flux** de messagerie, vous allez dans le rapport de carte de flux **de** messagerie.</span><span class="sxs-lookup"><span data-stu-id="2ffee-116">Clicking on the **Mail flow map** widget will take you to the **Mail flow map** report.</span></span>

<span data-ttu-id="2ffee-117">Les graphiques suivants sont disponibles dans l’affichage de rapport :</span><span class="sxs-lookup"><span data-stu-id="2ffee-117">The following charts are available in the report view:</span></span>

- <span data-ttu-id="2ffee-118">**Afficher les données pour : Vue d’ensemble**: il s’agit essentiellement d’une vue plus grande du widget.</span><span class="sxs-lookup"><span data-stu-id="2ffee-118">**Show data for: Overview**: This is basically a larger view of the widget.</span></span> <span data-ttu-id="2ffee-119">Si vous pointez sur une couleur spécifique, le nombre de messages s’affiche pour ce type de connecteur.</span><span class="sxs-lookup"><span data-stu-id="2ffee-119">If you hover over a specific color, the number of messages is displayed for that type of connector.</span></span>

  ![Vue d’ensemble dans le rapport de carte de flux de messagerie](../../media/mfi-mail-flow-map-report-overview.png)

- <span data-ttu-id="2ffee-121">**Afficher les données pour : Détail**: cet affichage affiche des détails sur les connecteurs et les domaines de destination.</span><span class="sxs-lookup"><span data-stu-id="2ffee-121">**Show data for: Detail**: This view shows details about the connectors and destination domains.</span></span> <span data-ttu-id="2ffee-122">Les principaux domaines de l’expéditeur et du destinataire sont répertoriés et les autres sont placés dans **d’autres domaines.**</span><span class="sxs-lookup"><span data-stu-id="2ffee-122">The top sender and recipient domains are listed, and the rest are put in **Others**.</span></span> <span data-ttu-id="2ffee-123">Si vous pointez sur une couleur et une section spécifiques, le nombre de messages s’affiche.</span><span class="sxs-lookup"><span data-stu-id="2ffee-123">If you hover over a specific color and section, the number of messages is displayed.</span></span>

  ![Affichage détaillé dans le rapport de carte de flux de messagerie](../../media/mfi-mail-flow-map-report-detail.png)

<span data-ttu-id="2ffee-125">Si vous cliquez sur **Filtres** dans un affichage de rapport, vous pouvez spécifier une plage de dates avec la **date de** début et la date **de fin.**</span><span class="sxs-lookup"><span data-stu-id="2ffee-125">If you click **Filters** in a report view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="2ffee-126">Pour envoyer par courrier électronique le rapport pour une plage de dates spécifique à un ou plusieurs destinataires, cliquez **sur Télécharger la demande.**</span><span class="sxs-lookup"><span data-stu-id="2ffee-126">To email the report for a specific date range to one or more recipients, click **Request download**.</span></span>

<span data-ttu-id="2ffee-127">Les informations associées sont affichées sous le plan de flux de messagerie si elles sont disponibles (par exemple, l’aperçu de la boucle de courrier de [correction possible).](mfi-mail-loop-insight.md)</span><span class="sxs-lookup"><span data-stu-id="2ffee-127">Related insights are shown beneath the Mail flow map if they're available (for example, the [Fix possible mail loop insight](mfi-mail-loop-insight.md)).</span></span>

## <a name="details-table-view-for-the-mail-flow-map"></a><span data-ttu-id="2ffee-128">Vue de table Détails pour le plan de flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="2ffee-128">Details table view for the Mail flow map</span></span>

<span data-ttu-id="2ffee-129">Si vous cliquez **sur Afficher le tableau des détails** dans un affichage de rapport, les informations suivantes sont affichées :</span><span class="sxs-lookup"><span data-stu-id="2ffee-129">If you click **View details table** in a report view, the following information is shown:</span></span>

- <span data-ttu-id="2ffee-130">**Date**</span><span class="sxs-lookup"><span data-stu-id="2ffee-130">**Date**</span></span>
- <span data-ttu-id="2ffee-131">**Catégorie**</span><span class="sxs-lookup"><span data-stu-id="2ffee-131">**Category**</span></span>
- <span data-ttu-id="2ffee-132">**Connecteur / Fournisseur de services tiers**</span><span class="sxs-lookup"><span data-stu-id="2ffee-132">**Connector / Third-party service provider**</span></span>
- <span data-ttu-id="2ffee-133">**Domaine de l’expéditeur/du destinataire**</span><span class="sxs-lookup"><span data-stu-id="2ffee-133">**Sender/Recipient domain**</span></span>
- <span data-ttu-id="2ffee-134">**Nombre de messages**</span><span class="sxs-lookup"><span data-stu-id="2ffee-134">**Message count**</span></span>

<span data-ttu-id="2ffee-135">Si vous cliquez sur **Filtres** dans une vue de tableau de détails, vous pouvez spécifier une plage de dates avec la **date** de début et la **date de fin.**</span><span class="sxs-lookup"><span data-stu-id="2ffee-135">If you click **Filters** in a details table view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="2ffee-136">Si vous sélectionnez une ligne, des détails similaires sont affichés dans un volant :</span><span class="sxs-lookup"><span data-stu-id="2ffee-136">If you select a row, similar details are shown in a flyout:</span></span>

![Volant détails du tableau détails dans le plan de flux de messagerie](../../media/mfi-mail-flow-map-view-details-table-details.png)

<span data-ttu-id="2ffee-138">Pour envoyer par courrier électronique le rapport pour une plage de dates spécifique à un ou plusieurs destinataires, cliquez **sur Télécharger la demande.**</span><span class="sxs-lookup"><span data-stu-id="2ffee-138">To email the report for a specific date range to one or more recipients, click **Request download**.</span></span>

<span data-ttu-id="2ffee-139">Pour revenir à l’affichage Rapports, cliquez **sur Afficher le rapport.**</span><span class="sxs-lookup"><span data-stu-id="2ffee-139">To go back to the reports view, click **View report**.</span></span>

## <a name="see-also"></a><span data-ttu-id="2ffee-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ffee-140">See also</span></span>

<span data-ttu-id="2ffee-141">Pour plus d’informations sur d’autres informations dans le tableau de bord de flux de messagerie, voir Informations sur le flux de messagerie dans le Centre de sécurité [& conformité.](mail-flow-insights-v2.md)</span><span class="sxs-lookup"><span data-stu-id="2ffee-141">For information about other insights in the Mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
