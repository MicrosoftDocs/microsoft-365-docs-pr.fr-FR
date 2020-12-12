---
title: Afficher les rapports de Defender pour Office 365 dans le tableau de bord rapports
f1.keywords:
- CSH
ms.author: tracyp
author: msfttracyp
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e47e838c-d99e-4c0b-b9aa-e66c4fae902f
ms.collection:
- M365-security-compliance
- m365initiative-defender-office365
description: Recherchez et utilisez des rapports pour Microsoft Defender pour Office 365 dans le centre de sécurité & conformité.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 82c003478538274be1dd1d2e04816de80d1eae6d
ms.sourcegitcommit: 0a8b0186cc041db7341e57f375d0d010b7682b7d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2020
ms.locfileid: "49659452"
---
# <a name="view-defender-for-office-365-reports-in-the-reports-dashboard-in-the-security--compliance-center"></a><span data-ttu-id="98553-103">Afficher les rapports de Defender pour Office 365 dans le tableau de bord rapports du centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="98553-103">View Defender for Office 365 reports in the Reports dashboard in the Security & Compliance Center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="98553-104">Microsoft Defender pour les organisations Office 365 (par exemple, les abonnements Microsoft 365 E5 ou Microsoft Defender pour Office 365 plan 1 ou Microsoft Defender for Office 365 plan 2 Add-ons) contiennent un grand nombre de rapports liés à la sécurité.</span><span class="sxs-lookup"><span data-stu-id="98553-104">Microsoft Defender for Office 365 organizations (for example, Microsoft 365 E5 subscriptions or Microsoft Defender for Office 365 Plan 1 or Microsoft Defender for Office 365 Plan 2 add-ons) contain a variety of security-related reports.</span></span> <span data-ttu-id="98553-105">Si vous disposez des [autorisations nécessaires](#what-permissions-are-needed-to-view-the-defender-for-office-365-reports), vous pouvez afficher ces rapports dans le centre de sécurité & conformité en accédant au  \> **tableau de bord** rapports.</span><span class="sxs-lookup"><span data-stu-id="98553-105">If you have the [necessary permissions](#what-permissions-are-needed-to-view-the-defender-for-office-365-reports), you can view these reports in the Security & Compliance Center by going to **Reports** \> **Dashboard**.</span></span> <span data-ttu-id="98553-106">Pour accéder directement au tableau de bord rapports, ouvrez <https://protection.office.com/insightdashboard> .</span><span class="sxs-lookup"><span data-stu-id="98553-106">To go directly to the Reports dashboard, open <https://protection.office.com/insightdashboard>.</span></span>

![Tableau de bord des rapports dans le centre de sécurité & conformité](../../media/6b213d34-adbb-44af-8549-be9a7e2db087.png)

## <a name="defender-for-office-365-file-types-report"></a><span data-ttu-id="98553-108">Rapport sur les types de fichiers de Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="98553-108">Defender for Office 365 file types report</span></span>

<span data-ttu-id="98553-109">Le rapport de **rapports sur les types de fichiers Office 365 Defender** indique le type de fichiers détectés comme malveillants par des [pièces jointes fiables](atp-safe-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="98553-109">The **Defender for Office 365 file types report** report shows you the type of files detected as malicious by [Safe Attachments](atp-safe-attachments.md).</span></span>

 <span data-ttu-id="98553-110">La vue agrégée du rapport autorise 90 jours de filtrage, tandis que l’affichage détaillé autorise uniquement les 10 jours de filtrage.</span><span class="sxs-lookup"><span data-stu-id="98553-110">The aggregate view of the report allows for 90 days of filtering, while the detail view only allows for 10 days of filtering.</span></span>

<span data-ttu-id="98553-111">Pour afficher le rapport, ouvrez le [Centre de sécurité & conformité](https://protection.office.com), accédez  au \> **tableau de bord** rapports et sélectionnez **types de fichiers Defender pour Office 365**.</span><span class="sxs-lookup"><span data-stu-id="98553-111">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Defender for Office 365 file types**.</span></span> <span data-ttu-id="98553-112">Pour accéder directement au rapport, ouvrez <https://protection.office.com/reportv2?id=ATPFileReport> .</span><span class="sxs-lookup"><span data-stu-id="98553-112">To go directly to the report, open <https://protection.office.com/reportv2?id=ATPFileReport>.</span></span>

![Widget de types de fichiers Office 365 Defender dans le tableau de bord rapports](../../media/atp-file-types-report-widget.png)

> [!NOTE]
> <span data-ttu-id="98553-114">Les informations contenues dans ce rapport sont également disponibles dans le [rapport de suppression des messages de Defender pour Office 365](#defender-for-office-365-message-disposition-report).</span><span class="sxs-lookup"><span data-stu-id="98553-114">The information in this report is also available in the [Defender for Office 365 message disposition report](#defender-for-office-365-message-disposition-report).</span></span>

### <a name="report-view-for-the-defender-for-office-365-file-types-report"></a><span data-ttu-id="98553-115">Affichage de rapport pour le rapport de types de fichiers Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="98553-115">Report view for the Defender for Office 365 file types report</span></span>

<span data-ttu-id="98553-116">Les vues disponibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="98553-116">The following views are available:</span></span>

- <span data-ttu-id="98553-117">**Afficher les données par : fichier**: le graphique contient les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="98553-117">**View data by: File**: The chart contains the following information:</span></span>

  - <span data-ttu-id="98553-118">**Pièces jointes Excel malveillantes**</span><span class="sxs-lookup"><span data-stu-id="98553-118">**Malicious Excel attachments**</span></span>
  - <span data-ttu-id="98553-119">**Pièces jointes Flash malveillantes**</span><span class="sxs-lookup"><span data-stu-id="98553-119">**Malicious Flash attachments**</span></span>
  - <span data-ttu-id="98553-120">**Pièces jointes PDF malveillantes**</span><span class="sxs-lookup"><span data-stu-id="98553-120">**Malicious PDF attachments**</span></span>
  - <span data-ttu-id="98553-121">**Pièces jointes PowerPoint malveillantes**</span><span class="sxs-lookup"><span data-stu-id="98553-121">**Malicious PowerPoint attachments**</span></span>
  - <span data-ttu-id="98553-122">**URL malveillantes**</span><span class="sxs-lookup"><span data-stu-id="98553-122">**Malicious URLs**</span></span>
  - <span data-ttu-id="98553-123">**Pièces jointes de mots malveillants**</span><span class="sxs-lookup"><span data-stu-id="98553-123">**Malicious Word attachments**</span></span>
  - <span data-ttu-id="98553-124">**Pièces jointes exécutables malveillants**</span><span class="sxs-lookup"><span data-stu-id="98553-124">**Malicious executable attachments**</span></span>
  - <span data-ttu-id="98553-125">**Autres**</span><span class="sxs-lookup"><span data-stu-id="98553-125">**Others**</span></span>

  <span data-ttu-id="98553-126">Lorsque vous pointez sur un jour particulier (point de données), vous pouvez voir la répartition des types de fichiers malveillants détectés par [les pièces jointes fiables](atp-safe-attachments.md) et la protection contre les [programmes malveillants dans EOP](anti-malware-protection.md).</span><span class="sxs-lookup"><span data-stu-id="98553-126">When you hover over a particular day (data point), you can see the breakdown of types of malicious files that were detected by [Safe Attachments](atp-safe-attachments.md) and [anti-malware protection in EOP](anti-malware-protection.md).</span></span>

  ![Affichage de fichiers dans le rapport de types de fichiers Defender pour Office 365](../../media/atp-file-types-report-file-view.png)

  <span data-ttu-id="98553-128">Si vous cliquez sur **filtres**, vous pouvez modifier le rapport avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="98553-128">If you click **Filters**, you can modify the report with the following filters:</span></span>

  - <span data-ttu-id="98553-129">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="98553-129">**Start date** and **End date**</span></span>
  - <span data-ttu-id="98553-130">Les mêmes valeurs de types de fichiers qui sont visibles dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="98553-130">The same file type values that are visible in the chart.</span></span>

- <span data-ttu-id="98553-131">**Afficher les données par : message**: le graphique contient les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="98553-131">**View data by: Message**: The chart contains the following information:</span></span>

  - <span data-ttu-id="98553-132">**Bloquer l’accès**</span><span class="sxs-lookup"><span data-stu-id="98553-132">**Block access**</span></span>
  - <span data-ttu-id="98553-133">**Messages remplacés**</span><span class="sxs-lookup"><span data-stu-id="98553-133">**Messages replaced**</span></span>
  - <span data-ttu-id="98553-134">**Messages surveillés**</span><span class="sxs-lookup"><span data-stu-id="98553-134">**Messages monitored**</span></span>
  - <span data-ttu-id="98553-135">**Remplacé par remise de courrier dynamique**: pour plus d’informations, consultez la rubrique [distribution dynamique dans les stratégies de pièces jointes approuvées](atp-safe-attachments.md#dynamic-delivery-in-safe-attachments-policies).</span><span class="sxs-lookup"><span data-stu-id="98553-135">**Replaced by Dynamic Email Delivery**: For more information, see [Dynamic Delivery in Safe Attachments policies](atp-safe-attachments.md#dynamic-delivery-in-safe-attachments-policies).</span></span>

  ![Affichage des messages dans le rapport de types de fichiers Defender pour Office 365](../../media/atp-file-types-report-message-view.png)

  <span data-ttu-id="98553-137">Si vous cliquez sur **filtres**, vous pouvez modifier le rapport avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="98553-137">If you click **Filters**, you can modify the report with the following filters:</span></span>

  - <span data-ttu-id="98553-138">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="98553-138">**Start date** and **End date**</span></span>
  - <span data-ttu-id="98553-139">Les mêmes valeurs de disposition de message disponibles dans le graphique et la valeur de **messages supplémentaires transmises** .</span><span class="sxs-lookup"><span data-stu-id="98553-139">The same message disposition values that are available in the chart, and the additional **Messages passed** value.</span></span>

### <a name="details-table-view-for-the-defender-for-office-365-file-types-report"></a><span data-ttu-id="98553-140">Vue de la table Détails pour le rapport de types de fichiers Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="98553-140">Details table view for the Defender for Office 365 file types report</span></span>

<span data-ttu-id="98553-141">Si vous cliquez sur **afficher les détails table**, le rapport fournit une vue quasi en temps réel de tous les clics effectués au sein de l’organisation au cours des 10 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="98553-141">If you click **View details table**, the report provides a near-real-time view of all clicks that happen within the organization for the last 10 days.</span></span> <span data-ttu-id="98553-142">Les informations affichées dépendent du graphique que vous recherchez :</span><span class="sxs-lookup"><span data-stu-id="98553-142">The information that's shown depends on the chart you were looking at:</span></span>

- <span data-ttu-id="98553-143">**Afficher les données par : fichier**:</span><span class="sxs-lookup"><span data-stu-id="98553-143">**View data by: File**:</span></span>

  - <span data-ttu-id="98553-144">**Date**</span><span class="sxs-lookup"><span data-stu-id="98553-144">**Date**</span></span>
  - <span data-ttu-id="98553-145">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="98553-145">**Recipient address**</span></span>
  - <span data-ttu-id="98553-146">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="98553-146">**Sender address**</span></span>
  - <span data-ttu-id="98553-147">**ID du message**: disponible dans le champ d’en-tête **message-ID** de l’en-tête du message et doit être unique.</span><span class="sxs-lookup"><span data-stu-id="98553-147">**Message ID**: Available in the **Message-ID** header field in the message header and should be unique.</span></span> <span data-ttu-id="98553-148">Un exemple de valeur est `<08f1e0f6806a47b4ac103961109ae6ef@server.domain>` (Notez les chevrons).</span><span class="sxs-lookup"><span data-stu-id="98553-148">An example value is `<08f1e0f6806a47b4ac103961109ae6ef@server.domain>` (note the angle brackets).</span></span>
  - <span data-ttu-id="98553-149">**File**</span><span class="sxs-lookup"><span data-stu-id="98553-149">**File**</span></span>

  <span data-ttu-id="98553-150">Si vous cliquez sur **filtres**, vous pouvez modifier le rapport avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="98553-150">If you click **Filters**, you can modify the report with the following filters:</span></span>

  - <span data-ttu-id="98553-151">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="98553-151">**Start date** and **End date**</span></span>
  - <span data-ttu-id="98553-152">Les mêmes valeurs de types de fichiers qui sont visibles dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="98553-152">The same file type values that are visible in the chart.</span></span>

- <span data-ttu-id="98553-153">**Afficher les données par : message**:</span><span class="sxs-lookup"><span data-stu-id="98553-153">**View data by: Message**:</span></span>

  - <span data-ttu-id="98553-154">**Date**</span><span class="sxs-lookup"><span data-stu-id="98553-154">**Date**</span></span>
  - <span data-ttu-id="98553-155">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="98553-155">**Recipient address**</span></span>
  - <span data-ttu-id="98553-156">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="98553-156">**Sender address**</span></span>
  - <span data-ttu-id="98553-157">**ID de message**</span><span class="sxs-lookup"><span data-stu-id="98553-157">**Message ID**</span></span>
  - <span data-ttu-id="98553-158">**File**</span><span class="sxs-lookup"><span data-stu-id="98553-158">**File**</span></span>
  - <span data-ttu-id="98553-159">**Subject**</span><span class="sxs-lookup"><span data-stu-id="98553-159">**Subject**</span></span>

  <span data-ttu-id="98553-160">Si vous cliquez sur **filtres**, vous pouvez modifier les résultats à l’aide des filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="98553-160">If you click **Filters**, you can modify the results with the following filters:</span></span>

  - <span data-ttu-id="98553-161">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="98553-161">**Start date** and **End date**</span></span>
  - <span data-ttu-id="98553-162">Les mêmes valeurs de disposition de message disponibles dans le graphique et la valeur de **messages supplémentaires transmises** .</span><span class="sxs-lookup"><span data-stu-id="98553-162">The same message disposition values that are available in the chart, and the additional **Messages passed** value.</span></span>

<span data-ttu-id="98553-163">Pour revenir à l’affichage rapports, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="98553-163">To get back to the reports view, click **View report**.</span></span>

## <a name="defender-for-office-365-message-disposition-report"></a><span data-ttu-id="98553-164">Rapport d’actions sur les messages de Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="98553-164">Defender for Office 365 message disposition report</span></span>

<span data-ttu-id="98553-165">Le rapport de **disposition des messages ATP** indique les actions qui ont été effectuées pour les messages électroniques détectés comme présentant du contenu malveillant.</span><span class="sxs-lookup"><span data-stu-id="98553-165">The **ATP Message Disposition** report shows you the actions that were taken for email messages that were detected as having malicious content.</span></span>

<span data-ttu-id="98553-166">Pour afficher le rapport, ouvrez le [Centre de sécurité & conformité](https://protection.office.com), accédez  au \> **tableau de bord** rapports et sélectionnez mise en **place de message Defender pour Office 365**.</span><span class="sxs-lookup"><span data-stu-id="98553-166">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Defender for Office 365 message disposition**.</span></span> <span data-ttu-id="98553-167">Pour accéder directement au rapport, ouvrez <https://protection.office.com/reportv2?id=ATPMessageReport> .</span><span class="sxs-lookup"><span data-stu-id="98553-167">To go directly to the report, open <https://protection.office.com/reportv2?id=ATPMessageReport>.</span></span>

![« Defender for Office 365 message disposition widget » dans le tableau de bord rapports](../../media/atp-message-disposition-report-widget.png)

> [!NOTE]
> <span data-ttu-id="98553-169">Les informations contenues dans ce rapport sont également disponibles dans le rapport sur les [types de fichiers Defender pour Office 365](#defender-for-office-365-file-types-report).</span><span class="sxs-lookup"><span data-stu-id="98553-169">The information in this report is also available in the [Defender for Office 365 file types report](#defender-for-office-365-file-types-report).</span></span>

### <a name="report-view-for-the-defender-for-office-365-message-disposition-report"></a><span data-ttu-id="98553-170">Affichage de rapport pour le rapport de suppression de messages de Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="98553-170">Report view for the Defender for Office 365 message disposition report</span></span>

<span data-ttu-id="98553-171">Les vues disponibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="98553-171">The following views are available:</span></span>

- <span data-ttu-id="98553-172">**Afficher les données par : message**: le graphique contient les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="98553-172">**View data by: Message**: The chart contains the following information:</span></span>

  - <span data-ttu-id="98553-173">**Bloquer l’accès**</span><span class="sxs-lookup"><span data-stu-id="98553-173">**Block access**</span></span>
  - <span data-ttu-id="98553-174">**Messages remplacés**</span><span class="sxs-lookup"><span data-stu-id="98553-174">**Messages replaced**</span></span>
  - <span data-ttu-id="98553-175">**Messages surveillés**</span><span class="sxs-lookup"><span data-stu-id="98553-175">**Messages monitored**</span></span>
  - <span data-ttu-id="98553-176">**Remplacé par remise de courrier dynamique**: pour plus d’informations, consultez la rubrique [distribution dynamique dans les stratégies de pièces jointes approuvées](atp-safe-attachments.md#dynamic-delivery-in-safe-attachments-policies).</span><span class="sxs-lookup"><span data-stu-id="98553-176">**Replaced by Dynamic Email Delivery**: For more information, see [Dynamic Delivery in Safe Attachments policies](atp-safe-attachments.md#dynamic-delivery-in-safe-attachments-policies).</span></span>

  ![Affichage des messages dans le rapport de types de fichiers Defender pour Office 365](../../media/atp-file-types-report-message-view.png)

  <span data-ttu-id="98553-178">Si vous cliquez sur **filtres**, vous pouvez modifier le rapport avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="98553-178">If you click **Filters**, you can modify the report with the following filters:</span></span>

  - <span data-ttu-id="98553-179">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="98553-179">**Start date** and **End date**</span></span>
  - <span data-ttu-id="98553-180">Les mêmes valeurs de disposition de message disponibles dans le graphique et la valeur de **messages supplémentaires transmises** .</span><span class="sxs-lookup"><span data-stu-id="98553-180">The same message disposition values that are available in the chart, and the additional **Messages passed** value.</span></span>

- <span data-ttu-id="98553-181">**Afficher les données par : fichier**: le graphique contient les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="98553-181">**View data by: File**: The chart contains the following information:</span></span>

  - <span data-ttu-id="98553-182">**Pièces jointes Excel malveillantes**</span><span class="sxs-lookup"><span data-stu-id="98553-182">**Malicious Excel attachments**</span></span>
  - <span data-ttu-id="98553-183">**Pièces jointes Flash malveillantes**</span><span class="sxs-lookup"><span data-stu-id="98553-183">**Malicious Flash attachments**</span></span>
  - <span data-ttu-id="98553-184">**Pièces jointes PDF malveillantes**</span><span class="sxs-lookup"><span data-stu-id="98553-184">**Malicious PDF attachments**</span></span>
  - <span data-ttu-id="98553-185">**Pièces jointes PowerPoint malveillantes**</span><span class="sxs-lookup"><span data-stu-id="98553-185">**Malicious PowerPoint attachments**</span></span>
  - <span data-ttu-id="98553-186">**URL malveillantes**</span><span class="sxs-lookup"><span data-stu-id="98553-186">**Malicious URLs**</span></span>
  - <span data-ttu-id="98553-187">**Pièces jointes de mots malveillants**</span><span class="sxs-lookup"><span data-stu-id="98553-187">**Malicious Word attachments**</span></span>
  - <span data-ttu-id="98553-188">**Pièces jointes exécutables malveillants**</span><span class="sxs-lookup"><span data-stu-id="98553-188">**Malicious executable attachments**</span></span>
  - <span data-ttu-id="98553-189">**Autres**</span><span class="sxs-lookup"><span data-stu-id="98553-189">**Others**</span></span>

  <span data-ttu-id="98553-190">Lorsque vous pointez sur un jour particulier (point de données), vous pouvez voir la répartition des types de fichiers malveillants détectés par [les pièces jointes fiables](atp-safe-attachments.md) et la protection contre les [programmes malveillants dans EOP](anti-malware-protection.md).</span><span class="sxs-lookup"><span data-stu-id="98553-190">When you hover over a particular day (data point), you can see the breakdown of types of malicious files that were detected by [Safe Attachments](atp-safe-attachments.md) and [anti-malware protection in EOP](anti-malware-protection.md).</span></span>

  ![Affichage de fichiers dans le rapport de types de fichiers Defender pour Office 365](../../media/atp-file-types-report-file-view.png)

  <span data-ttu-id="98553-192">Si vous cliquez sur **filtres**, vous pouvez modifier le rapport avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="98553-192">If you click **Filters**, you can modify the report with the following filters:</span></span>

  - <span data-ttu-id="98553-193">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="98553-193">**Start date** and **End date**</span></span>
  - <span data-ttu-id="98553-194">Les mêmes valeurs de types de fichiers qui sont visibles dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="98553-194">The same file type values that are visible in the chart.</span></span>

### <a name="details-table-view-for-the-defender-for-office-365-message-disposition-report"></a><span data-ttu-id="98553-195">Vue de la table Détails pour le rapport de suppression de messages de Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="98553-195">Details table view for the Defender for Office 365 message disposition report</span></span>

<span data-ttu-id="98553-196">Si vous cliquez sur **afficher les détails table**, le rapport fournit une vue quasi en temps réel de tous les clics effectués au sein de l’organisation au cours des 10 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="98553-196">If you click **View details table**, the report provides a near-real-time view of all clicks that happen within the organization for the last 10 days.</span></span> <span data-ttu-id="98553-197">Les informations affichées dépendent du graphique que vous recherchez :</span><span class="sxs-lookup"><span data-stu-id="98553-197">The information that's shown depends on the chart you were looking at:</span></span>

- <span data-ttu-id="98553-198">**Afficher les données par : message**:</span><span class="sxs-lookup"><span data-stu-id="98553-198">**View data by: Message**:</span></span>

  - <span data-ttu-id="98553-199">**Date**</span><span class="sxs-lookup"><span data-stu-id="98553-199">**Date**</span></span>
  - <span data-ttu-id="98553-200">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="98553-200">**Recipient address**</span></span>
  - <span data-ttu-id="98553-201">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="98553-201">**Sender address**</span></span>
  - <span data-ttu-id="98553-202">**ID de message**</span><span class="sxs-lookup"><span data-stu-id="98553-202">**Message ID**</span></span>
  - <span data-ttu-id="98553-203">**File**</span><span class="sxs-lookup"><span data-stu-id="98553-203">**File**</span></span>
  - <span data-ttu-id="98553-204">**Subject**</span><span class="sxs-lookup"><span data-stu-id="98553-204">**Subject**</span></span>

  <span data-ttu-id="98553-205">Si vous cliquez sur **filtres**, vous pouvez modifier les résultats à l’aide des filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="98553-205">If you click **Filters**, you can modify the results with the following filters:</span></span>

  - <span data-ttu-id="98553-206">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="98553-206">**Start date** and **End date**</span></span>
  - <span data-ttu-id="98553-207">Les mêmes valeurs de disposition de message disponibles dans le graphique et la valeur de **messages supplémentaires transmises** .</span><span class="sxs-lookup"><span data-stu-id="98553-207">The same message disposition values that are available in the chart, and the additional **Messages passed** value.</span></span>

- <span data-ttu-id="98553-208">**Afficher les données par : fichier**:</span><span class="sxs-lookup"><span data-stu-id="98553-208">**View data by: File**:</span></span>

  - <span data-ttu-id="98553-209">**Date**</span><span class="sxs-lookup"><span data-stu-id="98553-209">**Date**</span></span>
  - <span data-ttu-id="98553-210">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="98553-210">**Recipient address**</span></span>
  - <span data-ttu-id="98553-211">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="98553-211">**Sender address**</span></span>
  - <span data-ttu-id="98553-212">**ID de message**</span><span class="sxs-lookup"><span data-stu-id="98553-212">**Message ID**</span></span>
  - <span data-ttu-id="98553-213">**File**</span><span class="sxs-lookup"><span data-stu-id="98553-213">**File**</span></span>

  <span data-ttu-id="98553-214">Si vous cliquez sur **filtres**, vous pouvez modifier le rapport avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="98553-214">If you click **Filters**, you can modify the report with the following filters:</span></span>

  - <span data-ttu-id="98553-215">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="98553-215">**Start date** and **End date**</span></span>
  - <span data-ttu-id="98553-216">Les mêmes valeurs de types de fichiers qui sont visibles dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="98553-216">The same file type values that are visible in the chart.</span></span>

<span data-ttu-id="98553-217">Pour revenir à l’affichage rapports, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="98553-217">To get back to the reports view, click **View report**.</span></span>

## <a name="mail-latency-report"></a><span data-ttu-id="98553-218">Rapport de latence de messagerie</span><span class="sxs-lookup"><span data-stu-id="98553-218">Mail latency report</span></span>

<span data-ttu-id="98553-219">Le **rapport de latence du courrier** affiche une vue agrégée de la remise de courrier et de la détonation rencontrées au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="98553-219">The **Mail latency report** shows you an aggregate view of the mail delivery and detonation latency experienced within your organization.</span></span> <span data-ttu-id="98553-220">Les heures de remise du courrier dans le service sont affectées par un certain nombre de facteurs, et le délai de remise absolu en secondes n’est généralement pas un bon indicateur de réussite ou un problème.</span><span class="sxs-lookup"><span data-stu-id="98553-220">Mail delivery times in the service are affected by a number of factors, and the absolute delivery time in seconds is often not a good indicator of success or a problem.</span></span> <span data-ttu-id="98553-221">Un temps de remise lent sur un jour peut être considéré comme un temps de remise moyen un autre jour, ou inversement.</span><span class="sxs-lookup"><span data-stu-id="98553-221">A slow delivery time on one day might be considered an average delivery time on another day, or vice-versa.</span></span> <span data-ttu-id="98553-222">Le **rapport de latence du courrier** tente de qualifier la remise des messages en fonction des données statistiques relatives aux heures de remise observées des autres messages :</span><span class="sxs-lookup"><span data-stu-id="98553-222">The **Mail latency report** tries to qualify message delivery based on statistical data about the observed delivery times of other messages:</span></span>

- <span data-ttu-id="98553-223">**50e centile**: il s’agit du milieu des heures de remise des messages.</span><span class="sxs-lookup"><span data-stu-id="98553-223">**50th percentile**: This is the middle for message delivery times.</span></span> <span data-ttu-id="98553-224">Vous pouvez considérer cette valeur comme un temps de remise moyen.</span><span class="sxs-lookup"><span data-stu-id="98553-224">You can consider this value as an average delivery time.</span></span>
- <span data-ttu-id="98553-225">**quatre-vingt centile**: indique une latence élevée pour la remise des messages.</span><span class="sxs-lookup"><span data-stu-id="98553-225">**90th percentile**: This indicates a high latency for message delivery.</span></span> <span data-ttu-id="98553-226">Seul 10% des messages ont duré plus de cette valeur.</span><span class="sxs-lookup"><span data-stu-id="98553-226">Only 10% of messages took longer than this value to deliver.</span></span>
- <span data-ttu-id="98553-227">**99th centile**: indique la latence la plus élevée pour la remise des messages.</span><span class="sxs-lookup"><span data-stu-id="98553-227">**99th percentile**: This indicates the highest latency for message delivery.</span></span>

<span data-ttu-id="98553-228">La latence du réseau et du côté client ne sont pas incluses.</span><span class="sxs-lookup"><span data-stu-id="98553-228">Client side and network latency are not included.</span></span>

<span data-ttu-id="98553-229">Pour afficher le rapport, ouvrez le [Centre de sécurité & conformité](https://protection.office.com), accédez  au \> **tableau de bord** rapports et sélectionnez rapport de **latence de messagerie**.</span><span class="sxs-lookup"><span data-stu-id="98553-229">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Mail latency report**.</span></span> <span data-ttu-id="98553-230">Pour accéder directement au rapport, ouvrez <https://protection.office.com/mailLatencyReport?viewid=P50> .</span><span class="sxs-lookup"><span data-stu-id="98553-230">To go directly to the report, open <https://protection.office.com/mailLatencyReport?viewid=P50>.</span></span>

![Widget rapport de latence du courrier dans le tableau de bord rapports](../../media/mail-latency-report-widget.png)

### <a name="report-view-for-the-mail-latency-report"></a><span data-ttu-id="98553-232">Affichage de rapport pour le rapport de latence de messagerie</span><span class="sxs-lookup"><span data-stu-id="98553-232">Report view for the Mail latency report</span></span>

<span data-ttu-id="98553-233">Lorsque vous ouvrez le rapport, l’onglet **50e centiles** est sélectionné par défaut.</span><span class="sxs-lookup"><span data-stu-id="98553-233">When you open the report, the **50th percentiles** tab is selected by default.</span></span>

<span data-ttu-id="98553-234">Par défaut, cet affichage contient un graphique configuré avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="98553-234">By default, this view contains a chart that's configured with the following filters:</span></span>

- <span data-ttu-id="98553-235">**Date**: les 7 derniers jours</span><span class="sxs-lookup"><span data-stu-id="98553-235">**Date**: The last 7 days</span></span>
- <span data-ttu-id="98553-236">**Affichage des messages**:</span><span class="sxs-lookup"><span data-stu-id="98553-236">**Message View**:</span></span>
  - <span data-ttu-id="98553-237">Messages détonants</span><span class="sxs-lookup"><span data-stu-id="98553-237">Detonated messages</span></span>

<span data-ttu-id="98553-238">Ce graphique présente les messages organisés selon les catégories suivantes :</span><span class="sxs-lookup"><span data-stu-id="98553-238">This chart shows messages organized into the following categories:</span></span>

- <span data-ttu-id="98553-239">**Latence de remise de courrier**</span><span class="sxs-lookup"><span data-stu-id="98553-239">**Mail delivery latency**</span></span>
- <span data-ttu-id="98553-240">**Latence de la détonation**</span><span class="sxs-lookup"><span data-stu-id="98553-240">**Detonation latency**</span></span>

<span data-ttu-id="98553-241">Lorsque vous placez le curseur de la souris sur une catégorie dans le graphique, vous pouvez voir une répartition de la latence dans chaque catégorie.</span><span class="sxs-lookup"><span data-stu-id="98553-241">When you hover over a category in the chart, you can see a breakdown of the latency in each category.</span></span>

![Rapport de latence de messagerie](../../media/mail-latency-report.png)

<span data-ttu-id="98553-243">Si vous cliquez sur **filtre** dans le mode état, vous pouvez modifier les résultats à l’aide des filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="98553-243">If you click **Filter** in the report view, you can modify the results with the following filters:</span></span>

- <span data-ttu-id="98553-244">Tous les messages</span><span class="sxs-lookup"><span data-stu-id="98553-244">All messages</span></span>
- <span data-ttu-id="98553-245">Messages contenant des pièces jointes ou des URL</span><span class="sxs-lookup"><span data-stu-id="98553-245">Messages that contain attachments or URLs</span></span>

<span data-ttu-id="98553-246">Si vous cliquez sur l’onglet en **quatre-vingt les centiles** ou sur l’onglet **99th centile** , les mêmes filtres par défaut à partir de la vue **50e centiles** sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="98553-246">If you click the **90th percentiles** tab or the **99th percentiles** tab, the same default filters from the **50th percentiles** view are used.</span></span>

### <a name="details-table-view-for-the-mail-latency-report"></a><span data-ttu-id="98553-247">Vue de la table des détails pour le rapport de latence du courrier</span><span class="sxs-lookup"><span data-stu-id="98553-247">Details table view for the Mail latency report</span></span>

<span data-ttu-id="98553-248">Les informations suivantes sont affichées dans l’affichage tableau des détails :</span><span class="sxs-lookup"><span data-stu-id="98553-248">The following information is shown in the details table view:</span></span>

- <span data-ttu-id="98553-249">**Date**</span><span class="sxs-lookup"><span data-stu-id="98553-249">**Date**</span></span>
- <span data-ttu-id="98553-250">**Percentiles**</span><span class="sxs-lookup"><span data-stu-id="98553-250">**Percentiles**</span></span>
- <span data-ttu-id="98553-251">**Nombre de messages**</span><span class="sxs-lookup"><span data-stu-id="98553-251">**Message count**</span></span>
- <span data-ttu-id="98553-252">**Latence globale**</span><span class="sxs-lookup"><span data-stu-id="98553-252">**Overall latency**</span></span>

![Détails du rapport de latence du courrier](../../media/mail-latency-report-details.png)

<span data-ttu-id="98553-254">Les éléments ci-dessus montrent que, le 14 novembre, la latence moyenne observée pour tous les messages remis et détonants était de **108,033** secondes.</span><span class="sxs-lookup"><span data-stu-id="98553-254">The above shows that on November 14 the average latency experienced for all messages delivered and detonated was **108.033** seconds.</span></span>

<span data-ttu-id="98553-255">Le tableau détails contient les mêmes informations sur chaque onglet.</span><span class="sxs-lookup"><span data-stu-id="98553-255">The details table contains the same information on each tab.</span></span>

## <a name="threat-protection-status-report"></a><span data-ttu-id="98553-256">Rapport sur l’état de la protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="98553-256">Threat protection status report</span></span>

<span data-ttu-id="98553-257">Le rapport d' **État de protection contre les menaces** est une vue unique qui rassemble des informations sur le contenu malveillant et les e-mails malveillants détectés et bloqués par [Exchange Online Protection](exchange-online-protection-overview.md) (EoP) et Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="98553-257">The **Threat protection status** report is a single view that brings together information about malicious content and malicious email detected and blocked by [Exchange Online Protection](exchange-online-protection-overview.md) (EOP) and Microsoft Defender for Office 365.</span></span> <span data-ttu-id="98553-258">Pour plus d’informations, consultez la rubrique [Threat Protection Status Report](view-email-security-reports.md#threat-protection-status-report).</span><span class="sxs-lookup"><span data-stu-id="98553-258">For more information, see [Threat protection status report](view-email-security-reports.md#threat-protection-status-report).</span></span>

## <a name="url-threat-protection-report"></a><span data-ttu-id="98553-259">Rapport d’URL de protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="98553-259">URL threat protection report</span></span>

<span data-ttu-id="98553-260">Le **rapport URL protection contre les menaces** fournit des vues récapitulatives et des tendances pour les menaces détectées, ainsi que les actions effectuées sur les clics d’URL dans le cadre de [liens fiables](atp-safe-links.md).</span><span class="sxs-lookup"><span data-stu-id="98553-260">The **URL threat protection report** provides summary and trend views for threats detected and actions taken on URL clicks as part of [Safe Links](atp-safe-links.md).</span></span> <span data-ttu-id="98553-261">Ce rapport n’aura pas de clic sur les données des utilisateurs pour lesquels la stratégie de liens fiables est sélectionnée, l’option **ne pas suivre les clics utilisateur** est activée.</span><span class="sxs-lookup"><span data-stu-id="98553-261">This report will not have click data from users where the Safe Links policy applied has the **Do not track user clicks** option selected.</span></span>

<span data-ttu-id="98553-262">Pour afficher le rapport, ouvrez le [Centre de sécurité & conformité](https://protection.office.com), accédez  au \> **tableau de bord** rapports et sélectionnez **URL protection Report**.</span><span class="sxs-lookup"><span data-stu-id="98553-262">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **URL protection report**.</span></span> <span data-ttu-id="98553-263">Pour accéder directement au rapport, ouvrez <https://protection.office.com/reportv2?id=URLProtectionActionReport> .</span><span class="sxs-lookup"><span data-stu-id="98553-263">To go directly to the report, open <https://protection.office.com/reportv2?id=URLProtectionActionReport>.</span></span>

![Widget rapport de protection des URL dans le tableau de bord rapports](../../media/url-protection-report-widget.png)

> [!NOTE]
> <span data-ttu-id="98553-265">Il s’agit d’un *rapport de tendance de protection*, ce qui signifie que les données représentent des tendances dans un jeu de données plus volumineux.</span><span class="sxs-lookup"><span data-stu-id="98553-265">This is a *protection trend report*, meaning data represents trends in a larger dataset.</span></span> <span data-ttu-id="98553-266">Par conséquent, les données de l’affichage agrégé ne sont pas disponibles en temps réel ici, mais les données de la vue de la table des détails sont, de sorte que vous pouvez constater une légère divergence entre les deux vues.</span><span class="sxs-lookup"><span data-stu-id="98553-266">As a result, the data in the aggregate view is not available in real time here, but the data in the details table view is, so you may see a slight discrepancy between the two views.</span></span>

### <a name="report-view-for-the-url-threat-protection-report"></a><span data-ttu-id="98553-267">Affichage de rapport pour le rapport d’URL protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="98553-267">Report view for the URL threat protection report</span></span>

<span data-ttu-id="98553-268">Le rapport **URL protection contre les menaces** comporte deux vues agrégées qui sont actualisées toutes les quatre heures, qui affichent les données des 90 derniers jours :</span><span class="sxs-lookup"><span data-stu-id="98553-268">The **URL threat protection** report has two aggregated views that are refreshed once every four hours that shows data for the last 90 days:</span></span>

- <span data-ttu-id="98553-269">**URL cliquez sur protection action**: indique le nombre de clics d’URL par les utilisateurs de l’organisation, ainsi que les résultats du Click :</span><span class="sxs-lookup"><span data-stu-id="98553-269">**URL click protection action**: Shows the number of URL clicks by users in the organization and the results of the click:</span></span>

  - <span data-ttu-id="98553-270">**Bloqué** (l’utilisateur n’a pas pu accéder à l’URL)</span><span class="sxs-lookup"><span data-stu-id="98553-270">**Blocked** (the user was blocked from navigating to the URL)</span></span>
  - <span data-ttu-id="98553-271">**Bloqué et clic sur**</span><span class="sxs-lookup"><span data-stu-id="98553-271">**Blocked and clicked through**</span></span>
  - <span data-ttu-id="98553-272">**Clic lors de l’analyse**</span><span class="sxs-lookup"><span data-stu-id="98553-272">**Clicked through during scan**</span></span>

  <span data-ttu-id="98553-273">Un clic indique que l’utilisateur a cliqué sur la page bloquer pour le site Web malveillant (les administrateurs peuvent désactiver l’option cliquer via dans les stratégies de liens fiables).</span><span class="sxs-lookup"><span data-stu-id="98553-273">A click indicates that the user has clicked through the block page to the malicious website (admins can disable click through in Safe Links policies).</span></span>

  <span data-ttu-id="98553-274">Si vous cliquez sur **filtres**, vous pouvez modifier le rapport avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="98553-274">If you click **Filters**, you can modify the report with the following filters:</span></span>

  - <span data-ttu-id="98553-275">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="98553-275">**Start date** and **End date**</span></span>
  - <span data-ttu-id="98553-276">Les actions de protection clic disponibles, plus la valeur **autorisée** (l’utilisateur a été autorisé à accéder à l’URL).</span><span class="sxs-lookup"><span data-stu-id="98553-276">The available click protection actions, plus the value **Allowed** (the user was allowed to navigate to the URL).</span></span>

  ![URL cliquez sur affichage d’action de protection dans le rapport d’URL protection contre les menaces](../../media/url-threat-protection-report-url-click-protection-action-view.png)

- <span data-ttu-id="98553-278">**URL cliquez par application**: indique le nombre de clics d’URL par les applications qui prennent en charge les liens fiables :</span><span class="sxs-lookup"><span data-stu-id="98553-278">**URL click by application**: Shows the number of URL clicks by applications that support Safe Links:</span></span>

  - <span data-ttu-id="98553-279">**Client de messagerie**</span><span class="sxs-lookup"><span data-stu-id="98553-279">**Email client**</span></span>
  - <span data-ttu-id="98553-280">**PowerPoint**</span><span class="sxs-lookup"><span data-stu-id="98553-280">**PowerPoint**</span></span>
  - <span data-ttu-id="98553-281">**Word**</span><span class="sxs-lookup"><span data-stu-id="98553-281">**Word**</span></span>
  - <span data-ttu-id="98553-282">**Excel**</span><span class="sxs-lookup"><span data-stu-id="98553-282">**Excel**</span></span>
  - <span data-ttu-id="98553-283">**OneNote**</span><span class="sxs-lookup"><span data-stu-id="98553-283">**OneNote**</span></span>
  - <span data-ttu-id="98553-284">**Visio**</span><span class="sxs-lookup"><span data-stu-id="98553-284">**Visio**</span></span>
  - <span data-ttu-id="98553-285">**Teams**</span><span class="sxs-lookup"><span data-stu-id="98553-285">**Teams**</span></span>
  - <span data-ttu-id="98553-286">**Other**</span><span class="sxs-lookup"><span data-stu-id="98553-286">**Other**</span></span>

  <span data-ttu-id="98553-287">Si vous cliquez sur **filtres**, vous pouvez modifier le rapport avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="98553-287">If you click **Filters**, you can modify the report with the following filters:</span></span>

  - <span data-ttu-id="98553-288">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="98553-288">**Start date** and **End date**</span></span>
  - <span data-ttu-id="98553-289">Les applications disponibles.</span><span class="sxs-lookup"><span data-stu-id="98553-289">The available applications.</span></span>

### <a name="details-table-view-for-the-url-threat-protection-report"></a><span data-ttu-id="98553-290">Vue de la table Détails pour le rapport URL protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="98553-290">Details table view for the URL threat protection report</span></span>

<span data-ttu-id="98553-291">Si vous cliquez sur **afficher les détails** de la table, le rapport fournit une vue quasi en temps réel de tous les clics effectués au sein de l’organisation pendant les 7 derniers jours avec les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="98553-291">If you click **View details table**, the report provides a near-real-time view of all clicks that happen within the organization for the last 7 days with the following details:</span></span>

- <span data-ttu-id="98553-292">**Cliquez sur heure**</span><span class="sxs-lookup"><span data-stu-id="98553-292">**Click time**</span></span>
- <span data-ttu-id="98553-293">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="98553-293">**User**</span></span>
- <span data-ttu-id="98553-294">**URL**</span><span class="sxs-lookup"><span data-stu-id="98553-294">**URL**</span></span>
- <span data-ttu-id="98553-295">**Action**</span><span class="sxs-lookup"><span data-stu-id="98553-295">**Action**</span></span>
- <span data-ttu-id="98553-296">**App**</span><span class="sxs-lookup"><span data-stu-id="98553-296">**App**</span></span>

<span data-ttu-id="98553-297">Si vous cliquez sur **filtres** dans la vue table des détails, vous pouvez filtrer selon les mêmes critères que dans l’affichage rapport, ainsi que par les **domaines** ou les **destinataires** séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="98553-297">If you click **Filters** in the details table view, you can filter by the same criteria as in the report view, and also by **Domains** or **Recipients** separated by commas.</span></span>

<span data-ttu-id="98553-298">Pour revenir à l’affichage rapports, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="98553-298">To get back to the reports view, click **View report**.</span></span>

## <a name="additional-reports-to-view"></a><span data-ttu-id="98553-299">Rapports supplémentaires à afficher</span><span class="sxs-lookup"><span data-stu-id="98553-299">Additional reports to view</span></span>

<span data-ttu-id="98553-300">Outre les rapports décrits dans cet article, plusieurs autres rapports sont disponibles, comme décrit dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="98553-300">In addition to the reports described in this article, several other reports are available, as described in the following table:</span></span>

****

|<span data-ttu-id="98553-301">Rapport</span><span class="sxs-lookup"><span data-stu-id="98553-301">Report</span></span>|<span data-ttu-id="98553-302">Rubrique</span><span class="sxs-lookup"><span data-stu-id="98553-302">Topic</span></span>|
|---|---|
|<span data-ttu-id="98553-303">**Explorer** (Microsoft Defender pour Office 365 plan 2) ou **détections en temps réel** (microsoft Defender pour Office 365 plan 1)</span><span class="sxs-lookup"><span data-stu-id="98553-303">**Explorer** (Microsoft Defender for Office 365 Plan 2) or **real-time detections** (Microsoft Defender for Office 365 Plan 1)</span></span>|[<span data-ttu-id="98553-304">Explorateur de menaces (et détections en temps réel)</span><span class="sxs-lookup"><span data-stu-id="98553-304">Threat Explorer (and real-time detections)</span></span>](threat-explorer.md)|
|<span data-ttu-id="98553-305">**Rapports de sécurité de messagerie**, tels que le rapport des expéditeurs et des destinataires principaux, le rapport de courrier indésirable et le rapport des détections de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="98553-305">**Email security reports**, such as the Top senders and recipients report, the Spoof mail report, and the Spam detections report.</span></span>|[<span data-ttu-id="98553-306">Afficher les rapports de sécurité de courrier dans le centre de sécurité et conformité</span><span class="sxs-lookup"><span data-stu-id="98553-306">View email security reports in the Security & Compliance Center</span></span>](view-email-security-reports.md)|
|<span data-ttu-id="98553-307">Les **rapports de flux de messagerie**, tels que le rapport de transfert, le rapport d’état de flux de messagerie et le rapport des expéditeurs et des destinataires principaux.</span><span class="sxs-lookup"><span data-stu-id="98553-307">**Mail flow reports**, such as the Forwarding report, the Mailflow status report, and the Top senders and recipients report.</span></span>|[<span data-ttu-id="98553-308">Afficher les rapports de flux de messagerie dans le centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="98553-308">View mail flow reports in the Security & Compliance Center</span></span>](view-mail-flow-reports.md)|
|<span data-ttu-id="98553-309">**Suivi des URL pour les liens fiables** (PowerShell uniquement).</span><span class="sxs-lookup"><span data-stu-id="98553-309">**URL trace for Safe Links** (PowerShell only).</span></span> <span data-ttu-id="98553-310">La sortie de cette cmdlet vous indique les résultats des actions de liens fiables au cours des sept derniers jours.</span><span class="sxs-lookup"><span data-stu-id="98553-310">The output of this cmdlet shows you the results of Safe Links actions over the past seven days.</span></span>|[<span data-ttu-id="98553-311">Get-UrlTrace</span><span class="sxs-lookup"><span data-stu-id="98553-311">Get-UrlTrace</span></span>](https://docs.microsoft.com/powershell/module/exchange/get-urltrace)|
|<span data-ttu-id="98553-312">**Résultats du trafic de messagerie pour EOP et Microsoft Defender pour Office 365** (PowerShell uniquement).</span><span class="sxs-lookup"><span data-stu-id="98553-312">**Mail traffic results for EOP and Microsoft Defender for Office 365** (PowerShell only).</span></span> <span data-ttu-id="98553-313">La sortie de cette applet de commande contient des informations sur le domaine, la date, le type d’événement, la direction, l’action et le nombre de messages.</span><span class="sxs-lookup"><span data-stu-id="98553-313">The output of this cmdlet contains information about Domain, Date, Event Type, Direction, Action, and Message Count.</span></span>|[<span data-ttu-id="98553-314">Get-MailTrafficATPReport</span><span class="sxs-lookup"><span data-stu-id="98553-314">Get-MailTrafficATPReport</span></span>](https://docs.microsoft.com/powershell/module/exchange/get-mailtrafficatpreport)|
|<span data-ttu-id="98553-315">**Rapports de détail du courrier pour les détections EOP et Defender pour Office 365** (PowerShell uniquement).</span><span class="sxs-lookup"><span data-stu-id="98553-315">**Mail detail reports for EOP and Defender for Office 365 detections** (PowerShell only).</span></span> <span data-ttu-id="98553-316">La sortie de cette applet de commande contient des détails sur les URL ou les fichiers malveillants, les tentatives de hameçonnage, l’emprunt d’identité et d’autres menaces potentielles dans les messages ou les fichiers.</span><span class="sxs-lookup"><span data-stu-id="98553-316">The output of this cmdlet contains details about malicious files or URLs, phishing attempts, impersonation, and other potential threats in email or files.</span></span>|[<span data-ttu-id="98553-317">Get-MailDetailATPReport</span><span class="sxs-lookup"><span data-stu-id="98553-317">Get-MailDetailATPReport</span></span>](https://docs.microsoft.com/powershell/module/exchange/get-maildetailatpreport)|
|

## <a name="what-permissions-are-needed-to-view-the-defender-for-office-365-reports"></a><span data-ttu-id="98553-318">Quelles sont les autorisations nécessaires pour afficher les rapports Defender pour Office 365 ?</span><span class="sxs-lookup"><span data-stu-id="98553-318">What permissions are needed to view the Defender for Office 365 reports?</span></span>

<span data-ttu-id="98553-319">Pour afficher et utiliser les rapports décrits dans cet article, vous devez être membre de l’un des groupes de rôles suivants dans le centre de sécurité & conformité :</span><span class="sxs-lookup"><span data-stu-id="98553-319">In order to view and use the reports described in this article, you need to be a member of one of the following role groups in the Security & Compliance Center:</span></span>

- <span data-ttu-id="98553-320">**Gestion de l'organisation**</span><span class="sxs-lookup"><span data-stu-id="98553-320">**Organization Management**</span></span>
- <span data-ttu-id="98553-321">**Administrateur de la sécurité**</span><span class="sxs-lookup"><span data-stu-id="98553-321">**Security Administrator**</span></span>
- <span data-ttu-id="98553-322">**Lecteur de sécurité**</span><span class="sxs-lookup"><span data-stu-id="98553-322">**Security Reader**</span></span>
- <span data-ttu-id="98553-323">**Lecteur global**</span><span class="sxs-lookup"><span data-stu-id="98553-323">**Global Reader**</span></span>

<span data-ttu-id="98553-324">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="98553-324">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

<span data-ttu-id="98553-325">**Remarque**: l’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le centre d’administration 365 de Microsoft donne aux utilisateurs les autorisations requises dans le centre de sécurité & conformité _et_ des autorisations pour d’autres fonctionnalités de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="98553-325">**Note**: Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions in the Security & Compliance Center _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="98553-326">Pour plus d’informations, consultez [À propos des rôles d’administrateur](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles).</span><span class="sxs-lookup"><span data-stu-id="98553-326">For more information, see [About admin roles](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles).</span></span>

## <a name="what-if-the-reports-arent-showing-data"></a><span data-ttu-id="98553-327">Qu’en est-il si les rapports n’affichent pas de données ?</span><span class="sxs-lookup"><span data-stu-id="98553-327">What if the reports aren't showing data?</span></span>

<span data-ttu-id="98553-328">Si vous ne voyez pas de données dans votre compte Defender pour les rapports Office 365, vérifiez que vos stratégies sont correctement configurées.</span><span class="sxs-lookup"><span data-stu-id="98553-328">If you are not seeing data in your Defender for Office 365 reports, double-check that your policies are set up correctly.</span></span> <span data-ttu-id="98553-329">Votre organisation doit avoir [des stratégies de liens fiables](set-up-atp-safe-links-policies.md) et des [stratégies de pièces jointes approuvées](set-up-atp-safe-attachments-policies.md) définies de manière à ce que la protection Defender pour Office 365 soit mise en place.</span><span class="sxs-lookup"><span data-stu-id="98553-329">Your organization must have [Safe Links policies](set-up-atp-safe-links-policies.md) and [Safe Attachments policies](set-up-atp-safe-attachments-policies.md) defined in order for Defender for Office 365 protection to be in place.</span></span> <span data-ttu-id="98553-330">Consultez également la rubrique protection contre le [courrier indésirable et les programmes malveillants](anti-spam-and-anti-malware-protection.md).</span><span class="sxs-lookup"><span data-stu-id="98553-330">Also see [Anti-spam and anti-malware protection](anti-spam-and-anti-malware-protection.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="98553-331">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98553-331">Related topics</span></span>

[<span data-ttu-id="98553-332">Rapports intelligents et aperçus dans le Centre de sécurité et conformité</span><span class="sxs-lookup"><span data-stu-id="98553-332">Smart reports and insights in the Security & Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)

[<span data-ttu-id="98553-333">Autorisations de rôle (Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="98553-333">Role permissions (Azure Active Directory</span></span>](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#role-permissions)
