---
title: Rapport de domaine non accepté dans le tableau de bord de flux de messagerie
f1.keywords:
- NOCSH
ms.author: siosulli
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs peuvent apprendre à utiliser le rapport de domaine non accepté dans le tableau de bord de flux de messagerie dans le centre de sécurité & conformité pour surveiller les messages provenant de votre organisation locale où le domaine de l’expéditeur n’est pas configuré dans Microsoft 365.
ms.openlocfilehash: 06acacb79c826cb465b3fd28086a7df9d64eabdc
ms.sourcegitcommit: b64f36d3873fa0041b24bec029deb73ccfdfdbac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48877716"
---
# <a name="non-accepted-domain-report-in-the-security--compliance-center"></a><span data-ttu-id="7f23c-103">Rapport de domaine non accepté dans le centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="7f23c-103">Non-accepted domain report in the Security & Compliance Center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="7f23c-104">Le rapport de **domaine non accepté** dans le [tableau de bord de flux de messagerie](mail-flow-insights-v2.md) dans le [Centre de sécurité & conformité](https://protection.office.com) affiche des informations sur les messages provenant de votre organisation de messagerie locale où le domaine de l’expéditeur n’est pas configuré en tant que domaine accepté dans votre organisation 365 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7f23c-104">The **Non-accepted domain** report in the [Mail flow dashboard](mail-flow-insights-v2.md) in the [Security & Compliance Center](https://protection.office.com) displays information about messages from your on-premises email organization where the sender's domain isn't configured as an accepted domain in your Microsoft 365 organization.</span></span>

<span data-ttu-id="7f23c-105">Microsoft 365 peut limiter ces messages si nous disposons de données pour prouver que l’objectif de ces messages est malveillant.</span><span class="sxs-lookup"><span data-stu-id="7f23c-105">Microsoft 365 might throttle these messages if we have data to prove that the intent of these messages is malicious.</span></span> <span data-ttu-id="7f23c-106">Par conséquent, il est important de comprendre ce qui se passe et de résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="7f23c-106">Therefore, it's important for you to understand what's happening and to fix the issue.</span></span>

![Widget domaine non accepté dans le tableau de bord de flux de messagerie dans le centre de sécurité & conformité](../../media/mfi-non-accepted-domain-report-widget.png)

## <a name="report-view-for-the-non-accepted-domain-report"></a><span data-ttu-id="7f23c-108">Affichage de rapport pour le rapport de domaine non accepté</span><span class="sxs-lookup"><span data-stu-id="7f23c-108">Report view for the Non-accepted domain report</span></span>

<span data-ttu-id="7f23c-109">Si vous cliquez sur le graphique sur le widget de **domaine non accepté** , vous accédez au rapport de **domaine non accepté** .</span><span class="sxs-lookup"><span data-stu-id="7f23c-109">Clicking the chart on the **Non-accepted domain** widget will take you to the **Non-accepted domain** report.</span></span>

<span data-ttu-id="7f23c-110">Par défaut, l’activité de tous les connecteurs concernés est affichée.</span><span class="sxs-lookup"><span data-stu-id="7f23c-110">By default, the activity for all affected connectors is shown.</span></span> <span data-ttu-id="7f23c-111">Si vous cliquez sur **afficher les données pour** , vous pouvez sélectionner un connecteur spécifique dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="7f23c-111">If you click **Show data for** , you can select a specific connector from the dropdown.</span></span>

<span data-ttu-id="7f23c-112">Si vous placez le curseur de la souris sur un point de données (jour) dans le graphique, vous verrez le nombre total de messages pour le connecteur.</span><span class="sxs-lookup"><span data-stu-id="7f23c-112">If you hover over a data point (day) in the chart, you'll see the total number of messages for the connector.</span></span>

![Affichage de rapport dans le rapport de domaine non accepté](../../media/mfi-non-accepted-domain-report-overview-view.png)

## <a name="details-table-view-for-the-non-accepted-domain-report"></a><span data-ttu-id="7f23c-114">Vue de la table Détails pour le rapport de domaine non accepté</span><span class="sxs-lookup"><span data-stu-id="7f23c-114">Details table view for the Non-accepted domain report</span></span>

<span data-ttu-id="7f23c-115">Si vous cliquez sur **afficher la table des détails** dans un affichage de rapport, les informations suivantes s’affichent :</span><span class="sxs-lookup"><span data-stu-id="7f23c-115">If you click **View details table** in a report view, the following information is shown:</span></span>

- <span data-ttu-id="7f23c-116">**Date**</span><span class="sxs-lookup"><span data-stu-id="7f23c-116">**Date**</span></span>
- <span data-ttu-id="7f23c-117">**Nom du connecteur entrant**</span><span class="sxs-lookup"><span data-stu-id="7f23c-117">**Inbound connector name**</span></span>
- <span data-ttu-id="7f23c-118">**Domaine de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="7f23c-118">**Sender domain**</span></span>
- <span data-ttu-id="7f23c-119">**Nombre de messages**</span><span class="sxs-lookup"><span data-stu-id="7f23c-119">**Message count**</span></span>
- <span data-ttu-id="7f23c-120">**Exemples de messages** : ID de message d’un exemple de messages concernés.</span><span class="sxs-lookup"><span data-stu-id="7f23c-120">**Sample messages** : The message IDs of a sample of affected messages.</span></span>

<span data-ttu-id="7f23c-121">Si vous cliquez sur **filtres** dans un affichage tableau détaillé, vous pouvez spécifier une plage de dates avec **Date de début** et date de **fin**.</span><span class="sxs-lookup"><span data-stu-id="7f23c-121">If you click **Filters** in a details table view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="7f23c-122">Pour envoyer par courrier électronique le rapport pour une plage de dates spécifique à un ou plusieurs destinataires, cliquez sur **demander un téléchargement**.</span><span class="sxs-lookup"><span data-stu-id="7f23c-122">To email the report for a specific date range to one or more recipients, click **Request download**.</span></span>

<span data-ttu-id="7f23c-123">Lorsque vous sélectionnez une ligne dans le tableau, une fenêtre mobile apparaît avec les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="7f23c-123">When you select a row in the table, a flyout appears with the following information:</span></span>

- <span data-ttu-id="7f23c-124">**Date**</span><span class="sxs-lookup"><span data-stu-id="7f23c-124">**Date**</span></span>
- <span data-ttu-id="7f23c-125">**Nom du connecteur entrant**</span><span class="sxs-lookup"><span data-stu-id="7f23c-125">**Inbound connector name**</span></span>
- <span data-ttu-id="7f23c-126">**Domaine de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="7f23c-126">**Sender domain**</span></span>
- <span data-ttu-id="7f23c-127">**Nombre de messages**</span><span class="sxs-lookup"><span data-stu-id="7f23c-127">**Message count**</span></span>
- <span data-ttu-id="7f23c-128">**Exemples de messages** : vous pouvez cliquer sur **afficher les exemples de messages** pour afficher les résultats du [suivi](message-trace-scc.md) des messages pour un exemple des messages concernés.</span><span class="sxs-lookup"><span data-stu-id="7f23c-128">**Sample messages** : You can click **View sample messages** to see the [message trace](message-trace-scc.md) results for a sample of the affected messages.</span></span>

![Menu volant des détails après la sélection d’une ligne dans la vue du tableau de détails dans le rapport de domaine non accepté](../../media/mfi-non-accepted-domain-report-details-flyout.png)

<span data-ttu-id="7f23c-130">Pour revenir à l’affichage rapports, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="7f23c-130">To go back to the reports view, click **View report**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f23c-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7f23c-131">Related topics</span></span>

<span data-ttu-id="7f23c-132">Pour plus d’informations sur les autres informations du tableau de bord de flux de messagerie, consultez [la rubrique mail Flow Insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span><span class="sxs-lookup"><span data-stu-id="7f23c-132">For information about other insights in the Mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
