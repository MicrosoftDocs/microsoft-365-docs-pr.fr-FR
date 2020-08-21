---
title: Rapport de non-remise dans le tableau de bord de flux de messagerie
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs peuvent apprendre à utiliser le rapport sur les détails de non-remise dans le tableau de bord de flux de messagerie dans le centre de sécurité & conformité pour surveiller les codes d’erreur les plus fréquemment rencontrés dans les notifications d’échec de remise (également appelés notifications de non-remise) des expéditeurs de votre organisation.
ms.openlocfilehash: bdc2a2a16f76f4e6ada629c82b86423422ab56c9
ms.sourcegitcommit: e12fa502bc216f6083ef5666f693a04bb727d4df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "46826916"
---
# <a name="non-delivery-report-in-the-security--compliance-center"></a><span data-ttu-id="592c7-103">Notification d’échec de remise dans le centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="592c7-103">Non-delivery report in the Security & Compliance Center</span></span>

<span data-ttu-id="592c7-104">Le **rapport de non-remise** dans le [tableau de bord de flux de messagerie](mail-flow-insights-v2.md) dans le centre de sécurité & conformité affiche les codes d’erreur les plus détectés dans les notifications d’échec de remise (également appelées notifications de non-remise) pour les utilisateurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="592c7-104">The **Non-delivery report** in the [Mail flow dashboard](mail-flow-insights-v2.md) in the Security & Compliance Center shows the most-encountered error codes in non-delivery reports (also known as NDRs or bounce messages) for users in your organization.</span></span> <span data-ttu-id="592c7-105">Ce rapport affiche les détails des notifications d’échec de remise afin que vous puissiez résoudre les problèmes de remise des messages.</span><span class="sxs-lookup"><span data-stu-id="592c7-105">This report shows the details of NDRs so you can troubleshoot email delivery problems.</span></span>

![Widget rapport de non-remise dans le tableau de bord de flux de messagerie dans le centre de sécurité & conformité](../../media/mfi-non-delivery-report-widget.png)

## <a name="report-view-for-the-non-delivery-report"></a><span data-ttu-id="592c7-107">Affichage de rapport pour la notification d’échec de remise</span><span class="sxs-lookup"><span data-stu-id="592c7-107">Report view for the Non-delivery report</span></span>

<span data-ttu-id="592c7-108">Cliquez sur le widget **rapport de non-remise** pour accéder à la **notification**d’échec de remise.</span><span class="sxs-lookup"><span data-stu-id="592c7-108">Clicking on the **Non-delivery report** widget will take you to the **Non-delivery report**.</span></span>

<span data-ttu-id="592c7-109">Par défaut, l’activité de tous les codes d’erreur est affichée.</span><span class="sxs-lookup"><span data-stu-id="592c7-109">By default, the activity for all error codes is shown.</span></span> <span data-ttu-id="592c7-110">Si vous cliquez sur **afficher les données pour**, vous pouvez sélectionner un code d’erreur spécifique dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="592c7-110">If you click **Show data for**, you can select a specific error code from the dropdown.</span></span>

<span data-ttu-id="592c7-111">Si vous pointez sur une couleur spécifique (code d’erreur) sur un jour spécifique du graphique, vous verrez le nombre total de messages pour l’erreur.</span><span class="sxs-lookup"><span data-stu-id="592c7-111">If you hover over a specific color (error code) on a specific day in the chart, you'll see the total number of messages for the error.</span></span>

![Affichage de rapport dans le rapport de domaine non accepté](../../media/mfi-non-delivery-report-overview-view.png)

## <a name="details-table-view-for-the-non-delivery-report"></a><span data-ttu-id="592c7-113">Vue de la table Détails pour la notification d’échec de remise</span><span class="sxs-lookup"><span data-stu-id="592c7-113">Details table view for the Non-delivery report</span></span>

<span data-ttu-id="592c7-114">Si vous cliquez sur **afficher la table des détails** dans un affichage de rapport, les informations suivantes s’affichent :</span><span class="sxs-lookup"><span data-stu-id="592c7-114">If you click **View details table** in a report view, the following information is shown:</span></span>

- <span data-ttu-id="592c7-115">**Date**</span><span class="sxs-lookup"><span data-stu-id="592c7-115">**Date**</span></span>
- <span data-ttu-id="592c7-116">**Code de rapport de non-remise**</span><span class="sxs-lookup"><span data-stu-id="592c7-116">**Non-delivery report code**</span></span>
- <span data-ttu-id="592c7-117">**Count**</span><span class="sxs-lookup"><span data-stu-id="592c7-117">**Count**</span></span>
- <span data-ttu-id="592c7-118">**Exemples de messages**: ID de message d’un exemple de messages concernés.</span><span class="sxs-lookup"><span data-stu-id="592c7-118">**Sample messages**: The message IDs of a sample of affected messages.</span></span>

<span data-ttu-id="592c7-119">Si vous cliquez sur **filtres** dans un affichage tableau détaillé, vous pouvez spécifier une plage de dates avec **Date de début** et date de **fin**.</span><span class="sxs-lookup"><span data-stu-id="592c7-119">If you click **Filters** in a details table view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="592c7-120">Pour envoyer par courrier électronique le rapport pour une plage de dates spécifique à un ou plusieurs destinataires, cliquez sur **demander un téléchargement**.</span><span class="sxs-lookup"><span data-stu-id="592c7-120">To email the report for a specific date range to one or more recipients, click **Request download**.</span></span>

<span data-ttu-id="592c7-121">Lorsque vous sélectionnez une ligne dans le tableau, une fenêtre mobile apparaît avec les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="592c7-121">When you select a row in the table, a flyout appears with the following information:</span></span>

- <span data-ttu-id="592c7-122">**Date**</span><span class="sxs-lookup"><span data-stu-id="592c7-122">**Date**</span></span>
- <span data-ttu-id="592c7-123">**Code de rapport de non-remise**: vous pouvez cliquer sur le lien pour trouver des informations supplémentaires sur les causes et solutions pour le code d’erreur spécifique.</span><span class="sxs-lookup"><span data-stu-id="592c7-123">**Non-delivery report code**: You can click on the link to find for more information about the causes and solutions for the specific error code.</span></span>
- <span data-ttu-id="592c7-124">**Count**</span><span class="sxs-lookup"><span data-stu-id="592c7-124">**Count**</span></span>
- <span data-ttu-id="592c7-125">**Exemples de messages**: vous pouvez cliquer sur **afficher les exemples de messages** pour afficher les résultats du [suivi](message-trace-scc.md) des messages pour un exemple des messages concernés.</span><span class="sxs-lookup"><span data-stu-id="592c7-125">**Sample messages**: You can click **View sample messages** to see the [message trace](message-trace-scc.md) results for a sample of the affected messages.</span></span>

![Menu volant des détails après la sélection d’une ligne dans la vue du tableau de détails dans le rapport de non-remise](../../media/mfi-non-delivery-report-details-flyout.png)

## <a name="related-topics"></a><span data-ttu-id="592c7-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="592c7-127">Related topics</span></span>

<span data-ttu-id="592c7-128">Pour plus d’informations sur les autres informations du tableau de bord de flux de messagerie, consultez [la rubrique mail Flow Insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span><span class="sxs-lookup"><span data-stu-id="592c7-128">For information about other insights in the Mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
