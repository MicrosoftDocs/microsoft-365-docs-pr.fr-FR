---
title: Rapport de domaine non accepté dans le tableau de bord de flux de messagerie
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
description: Les administrateurs peuvent apprendre à utiliser le rapport de domaine non accepté dans le tableau de bord de flux de messagerie du Centre de sécurité & conformité pour surveiller les messages provenant de votre organisation sur site où le domaine de l’expéditeur n’est pas configuré dans Microsoft 365.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 573fb0ba2bf7981b6eb7df4eec7c8c4e5d596cac
ms.sourcegitcommit: e920e68c8d0eac8b152039b52cfc139d478a67b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2021
ms.locfileid: "50150819"
---
# <a name="non-accepted-domain-report-in-the-security--compliance-center"></a><span data-ttu-id="23a9e-103">Rapport de domaine non accepté dans le Centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="23a9e-103">Non-accepted domain report in the Security & Compliance Center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="23a9e-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="23a9e-104">**Applies to**</span></span>
- [<span data-ttu-id="23a9e-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="23a9e-105">Exchange Online Protection</span></span>](https://go.microsoft.com/fwlink/?linkid=2148611)
- [<span data-ttu-id="23a9e-106">Microsoft Defender pour Office 365 plan 1 et plan 2</span><span class="sxs-lookup"><span data-stu-id="23a9e-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](https://go.microsoft.com/fwlink/?linkid=2148715)
- [<span data-ttu-id="23a9e-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="23a9e-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

<span data-ttu-id="23a9e-108">Le  rapport de domaine non [](mail-flow-insights-v2.md) accepté dans le tableau de bord de flux de messagerie du Centre de sécurité [&](https://protection.office.com) conformité affiche des informations sur les messages provenant de votre organisation de messagerie sur site où le domaine de l’expéditeur n’est pas configuré en tant que domaine accepté dans votre organisation Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="23a9e-108">The **Non-accepted domain** report in the [Mail flow dashboard](mail-flow-insights-v2.md) in the [Security & Compliance Center](https://protection.office.com) displays information about messages from your on-premises email organization where the sender's domain isn't configured as an accepted domain in your Microsoft 365 organization.</span></span>

<span data-ttu-id="23a9e-109">Microsoft 365 peut limiter ces messages si nous avons des données pour prouver que l’intention de ces messages est malveillante.</span><span class="sxs-lookup"><span data-stu-id="23a9e-109">Microsoft 365 might throttle these messages if we have data to prove that the intent of these messages is malicious.</span></span> <span data-ttu-id="23a9e-110">Par conséquent, il est important que vous compreniez ce qui se passe et que vous corrigez le problème.</span><span class="sxs-lookup"><span data-stu-id="23a9e-110">Therefore, it's important for you to understand what's happening and to fix the issue.</span></span>

![Widget de domaine non accepté dans le tableau de bord de flux de messagerie dans le Centre de sécurité & conformité](../../media/mfi-non-accepted-domain-report-widget.png)

## <a name="report-view-for-the-non-accepted-domain-report"></a><span data-ttu-id="23a9e-112">Affichage du rapport pour le rapport de domaine non accepté</span><span class="sxs-lookup"><span data-stu-id="23a9e-112">Report view for the Non-accepted domain report</span></span>

<span data-ttu-id="23a9e-113">Le fait de cliquer sur le graphique sur le widget **de** domaine non accepté vous permet d’avoir accès au **rapport de domaine** non accepté.</span><span class="sxs-lookup"><span data-stu-id="23a9e-113">Clicking the chart on the **Non-accepted domain** widget will take you to the **Non-accepted domain** report.</span></span>

<span data-ttu-id="23a9e-114">Par défaut, l’activité de tous les connecteurs affectés est affichée.</span><span class="sxs-lookup"><span data-stu-id="23a9e-114">By default, the activity for all affected connectors is shown.</span></span> <span data-ttu-id="23a9e-115">Si vous cliquez **sur Afficher les données pour**, vous pouvez sélectionner un connecteur spécifique dans la dropdown.</span><span class="sxs-lookup"><span data-stu-id="23a9e-115">If you click **Show data for**, you can select a specific connector from the dropdown.</span></span>

<span data-ttu-id="23a9e-116">Si vous pointez sur un point de données (jour) dans le graphique, vous verrez le nombre total de messages pour le connecteur.</span><span class="sxs-lookup"><span data-stu-id="23a9e-116">If you hover over a data point (day) in the chart, you'll see the total number of messages for the connector.</span></span>

![Affichage du rapport dans le rapport de domaine non accepté](../../media/mfi-non-accepted-domain-report-overview-view.png)

## <a name="details-table-view-for-the-non-accepted-domain-report"></a><span data-ttu-id="23a9e-118">Vue de table Détails pour le rapport de domaine non accepté</span><span class="sxs-lookup"><span data-stu-id="23a9e-118">Details table view for the Non-accepted domain report</span></span>

<span data-ttu-id="23a9e-119">Si vous cliquez **sur Afficher le tableau des détails** dans un affichage de rapport, les informations suivantes sont affichées :</span><span class="sxs-lookup"><span data-stu-id="23a9e-119">If you click **View details table** in a report view, the following information is shown:</span></span>

- <span data-ttu-id="23a9e-120">**Date**</span><span class="sxs-lookup"><span data-stu-id="23a9e-120">**Date**</span></span>
- <span data-ttu-id="23a9e-121">**Nom du connecteur entrant**</span><span class="sxs-lookup"><span data-stu-id="23a9e-121">**Inbound connector name**</span></span>
- <span data-ttu-id="23a9e-122">**Domaine de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="23a9e-122">**Sender domain**</span></span>
- <span data-ttu-id="23a9e-123">**Nombre de messages**</span><span class="sxs-lookup"><span data-stu-id="23a9e-123">**Message count**</span></span>
- <span data-ttu-id="23a9e-124">**Exemples de messages**: ID de message d’un échantillon de messages affectés.</span><span class="sxs-lookup"><span data-stu-id="23a9e-124">**Sample messages**: The message IDs of a sample of affected messages.</span></span>

<span data-ttu-id="23a9e-125">Si vous cliquez sur **Filtres** dans une vue de tableau de détails, vous pouvez spécifier une plage de dates avec la **date** de début et la **date de fin.**</span><span class="sxs-lookup"><span data-stu-id="23a9e-125">If you click **Filters** in a details table view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="23a9e-126">Pour envoyer par courrier électronique le rapport pour une plage de dates spécifique à un ou plusieurs destinataires, cliquez **sur Télécharger la demande.**</span><span class="sxs-lookup"><span data-stu-id="23a9e-126">To email the report for a specific date range to one or more recipients, click **Request download**.</span></span>

<span data-ttu-id="23a9e-127">Lorsque vous sélectionnez une ligne dans le tableau, un flyout s’affiche avec les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="23a9e-127">When you select a row in the table, a flyout appears with the following information:</span></span>

- <span data-ttu-id="23a9e-128">**Date**</span><span class="sxs-lookup"><span data-stu-id="23a9e-128">**Date**</span></span>
- <span data-ttu-id="23a9e-129">**Nom du connecteur entrant**</span><span class="sxs-lookup"><span data-stu-id="23a9e-129">**Inbound connector name**</span></span>
- <span data-ttu-id="23a9e-130">**Domaine de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="23a9e-130">**Sender domain**</span></span>
- <span data-ttu-id="23a9e-131">**Nombre de messages**</span><span class="sxs-lookup"><span data-stu-id="23a9e-131">**Message count**</span></span>
- <span data-ttu-id="23a9e-132">**Exemples de messages**: vous pouvez cliquer sur Afficher les **exemples de messages** pour afficher les résultats du [suivi](message-trace-scc.md) des messages pour un échantillon des messages concernés.</span><span class="sxs-lookup"><span data-stu-id="23a9e-132">**Sample messages**: You can click **View sample messages** to see the [message trace](message-trace-scc.md) results for a sample of the affected messages.</span></span>

![Volant détails après sélection d’une ligne dans l’affichage De la table Détails dans le rapport de domaine non accepté](../../media/mfi-non-accepted-domain-report-details-flyout.png)

<span data-ttu-id="23a9e-134">Pour revenir à l’affichage Rapports, cliquez **sur Afficher le rapport.**</span><span class="sxs-lookup"><span data-stu-id="23a9e-134">To go back to the reports view, click **View report**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="23a9e-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="23a9e-135">Related topics</span></span>

<span data-ttu-id="23a9e-136">Pour plus d’informations sur d’autres informations dans le tableau de bord de flux de messagerie, voir Informations sur le flux de messagerie dans le Centre de sécurité [& conformité.](mail-flow-insights-v2.md)</span><span class="sxs-lookup"><span data-stu-id="23a9e-136">For information about other insights in the Mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
