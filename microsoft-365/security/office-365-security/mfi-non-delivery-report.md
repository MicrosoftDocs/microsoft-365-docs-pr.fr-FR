---
title: Rapport de non-remise dans le tableau de bord de flux de messagerie
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
description: Les administrateurs peuvent apprendre à utiliser le rapport de non-remise dans le tableau de bord de flux de messagerie du Centre de sécurité & conformité pour surveiller les codes d’erreur les plus fréquemment rencontrés dans les rapports de non-remise (également appelés rapports de non-remise ou de non-remise) des expéditeurs de votre organisation.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: dbd27fc818a46a983874a04f0e313c622e047ea5
ms.sourcegitcommit: 537e513a4a232a01e44ecbc76d86a8bcaf142482
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/27/2021
ms.locfileid: "50029833"
---
# <a name="non-delivery-report-in-the-security--compliance-center"></a><span data-ttu-id="2d3f7-103">Rapport de non-remise dans le Centre de conformité & sécurité</span><span class="sxs-lookup"><span data-stu-id="2d3f7-103">Non-delivery report in the Security & Compliance Center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="2d3f7-104">Le rapport d’absence [](mail-flow-insights-v2.md) de remise dans le tableau de bord de flux de messagerie dans le Centre de sécurité [&](https://protection.office.com) conformité affiche les codes d’erreur les plus rencontrés dans les rapports de **non-remise** (également appelés rapports de non-remise) pour les utilisateurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="2d3f7-104">The **Non-delivery report** in the [Mail flow dashboard](mail-flow-insights-v2.md) in the [Security & Compliance Center](https://protection.office.com) shows the most-encountered error codes in non-delivery reports (also known as NDRs or bounce messages) for users in your organization.</span></span> <span data-ttu-id="2d3f7-105">Ce rapport présente les détails des rapports de non-remise pour vous aider à résoudre les problèmes de remise des e-mails.</span><span class="sxs-lookup"><span data-stu-id="2d3f7-105">This report shows the details of NDRs so you can troubleshoot email delivery problems.</span></span>

![Widget de rapport d’absence de remise dans le tableau de bord de flux de messagerie dans le Centre de sécurité & conformité](../../media/mfi-non-delivery-report-widget.png)

## <a name="report-view-for-the-non-delivery-report"></a><span data-ttu-id="2d3f7-107">Affichage du rapport de non-remise</span><span class="sxs-lookup"><span data-stu-id="2d3f7-107">Report view for the Non-delivery report</span></span>

<span data-ttu-id="2d3f7-108">Cliquez sur le widget de rapport de **non-remise** pour vous rendre dans la rapport **d’absence de remise.**</span><span class="sxs-lookup"><span data-stu-id="2d3f7-108">Clicking on the **Non-delivery report** widget will take you to the **Non-delivery report**.</span></span>

<span data-ttu-id="2d3f7-109">Par défaut, l’activité de tous les codes d’erreur s’affiche.</span><span class="sxs-lookup"><span data-stu-id="2d3f7-109">By default, the activity for all error codes is shown.</span></span> <span data-ttu-id="2d3f7-110">Si vous cliquez **sur Afficher les données pour**, vous pouvez sélectionner un code d’erreur spécifique dans ladown.</span><span class="sxs-lookup"><span data-stu-id="2d3f7-110">If you click **Show data for**, you can select a specific error code from the dropdown.</span></span>

<span data-ttu-id="2d3f7-111">Si vous pointez sur une couleur spécifique (code d’erreur) un jour spécifique du graphique, vous verrez le nombre total de messages pour l’erreur.</span><span class="sxs-lookup"><span data-stu-id="2d3f7-111">If you hover over a specific color (error code) on a specific day in the chart, you'll see the total number of messages for the error.</span></span>

![Affichage du rapport dans le rapport de domaine non accepté](../../media/mfi-non-delivery-report-overview-view.png)

## <a name="details-table-view-for-the-non-delivery-report"></a><span data-ttu-id="2d3f7-113">Affichage de table détails pour le rapport de non-remise</span><span class="sxs-lookup"><span data-stu-id="2d3f7-113">Details table view for the Non-delivery report</span></span>

<span data-ttu-id="2d3f7-114">Si vous cliquez **sur Afficher le tableau des détails** dans un affichage de rapport, les informations suivantes sont affichées :</span><span class="sxs-lookup"><span data-stu-id="2d3f7-114">If you click **View details table** in a report view, the following information is shown:</span></span>

- <span data-ttu-id="2d3f7-115">**Date**</span><span class="sxs-lookup"><span data-stu-id="2d3f7-115">**Date**</span></span>
- <span data-ttu-id="2d3f7-116">**Code de rapport de non-remise**</span><span class="sxs-lookup"><span data-stu-id="2d3f7-116">**Non-delivery report code**</span></span>
- <span data-ttu-id="2d3f7-117">**Count**</span><span class="sxs-lookup"><span data-stu-id="2d3f7-117">**Count**</span></span>
- <span data-ttu-id="2d3f7-118">**Exemples de messages**: ID de message d’un échantillon de messages affectés.</span><span class="sxs-lookup"><span data-stu-id="2d3f7-118">**Sample messages**: The message IDs of a sample of affected messages.</span></span>

<span data-ttu-id="2d3f7-119">Si vous cliquez sur **Filtres** dans une vue de tableau de détails, vous pouvez spécifier une plage de dates avec la **date** de début et la **date de fin.**</span><span class="sxs-lookup"><span data-stu-id="2d3f7-119">If you click **Filters** in a details table view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="2d3f7-120">Pour envoyer par courrier électronique le rapport pour une plage de dates spécifique à un ou plusieurs destinataires, cliquez **sur Télécharger la demande.**</span><span class="sxs-lookup"><span data-stu-id="2d3f7-120">To email the report for a specific date range to one or more recipients, click **Request download**.</span></span>

<span data-ttu-id="2d3f7-121">Lorsque vous sélectionnez une ligne dans le tableau, un flyout s’affiche avec les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2d3f7-121">When you select a row in the table, a flyout appears with the following information:</span></span>

- <span data-ttu-id="2d3f7-122">**Date**</span><span class="sxs-lookup"><span data-stu-id="2d3f7-122">**Date**</span></span>
- <span data-ttu-id="2d3f7-123">Code de rapport de **non-remise**: vous pouvez cliquer sur le lien pour obtenir plus d’informations sur les causes et solutions pour le code d’erreur spécifique.</span><span class="sxs-lookup"><span data-stu-id="2d3f7-123">**Non-delivery report code**: You can click on the link to find for more information about the causes and solutions for the specific error code.</span></span>
- <span data-ttu-id="2d3f7-124">**Count**</span><span class="sxs-lookup"><span data-stu-id="2d3f7-124">**Count**</span></span>
- <span data-ttu-id="2d3f7-125">**Exemples de messages**: vous pouvez cliquer sur Afficher les **exemples de messages** pour afficher les résultats du [suivi](message-trace-scc.md) des messages pour un échantillon des messages concernés.</span><span class="sxs-lookup"><span data-stu-id="2d3f7-125">**Sample messages**: You can click **View sample messages** to see the [message trace](message-trace-scc.md) results for a sample of the affected messages.</span></span>

![Volant détails après sélection d’une ligne dans l’affichage Tableau Détails dans le rapport de non-remise](../../media/mfi-non-delivery-report-details-flyout.png)

## <a name="related-topics"></a><span data-ttu-id="2d3f7-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d3f7-127">Related topics</span></span>

<span data-ttu-id="2d3f7-128">Pour plus d’informations sur d’autres informations dans le tableau de bord de flux de messagerie, voir Informations sur le flux de messagerie dans le Centre de sécurité [& conformité.](mail-flow-insights-v2.md)</span><span class="sxs-lookup"><span data-stu-id="2d3f7-128">For information about other insights in the Mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
