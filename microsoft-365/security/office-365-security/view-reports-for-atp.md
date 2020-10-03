---
title: Afficher les rapports de protection avancée contre les menaces
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
description: Recherchez et utilisez des rapports pour Office 365 protection avancée contre les menaces dans le centre de sécurité &amp; conformité.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 4f871432f29138acb8bee3a14b9bb161d87193e3
ms.sourcegitcommit: 3a0accd616ca94d6ba7f50e502552b45e9661a95
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/03/2020
ms.locfileid: "48351034"
---
# <a name="view-reports-for-office-365-advanced-threat-protection"></a><span data-ttu-id="310c9-103">Afficher les rapports pour Office 365 protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="310c9-103">View reports for Office 365 Advanced Threat Protection</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="310c9-104">Les organisations Office 365 Advanced Threat Protection (ATP) (par exemple, les abonnements Microsoft 365 E5 ou les modules complémentaires ATP plan 1 ou ATP plan 2) contiennent un grand nombre de rapports liés à la sécurité.</span><span class="sxs-lookup"><span data-stu-id="310c9-104">Office 365 Advanced Threat Protection (ATP) organizations (for example, Microsoft 365 E5 subscriptions or ATP Plan 1 or ATP Plan 2 add-ons) contain a variety of security-related reports.</span></span> <span data-ttu-id="310c9-105">Si vous disposez des [autorisations nécessaires](#what-permissions-are-needed-to-view-the-atp-reports), vous pouvez afficher ces rapports dans le centre de sécurité & conformité en accédant au **Reports** \> **tableau de bord**rapports.</span><span class="sxs-lookup"><span data-stu-id="310c9-105">If you have the [necessary permissions](#what-permissions-are-needed-to-view-the-atp-reports), you can view these reports in the Security & Compliance Center by going to **Reports** \> **Dashboard**.</span></span> <span data-ttu-id="310c9-106">Pour accéder directement au tableau de bord rapports, ouvrez <https://protection.office.com/insightdashboard> .</span><span class="sxs-lookup"><span data-stu-id="310c9-106">To go directly to the Reports dashboard, open <https://protection.office.com/insightdashboard>.</span></span>

![Tableau de bord des rapports dans le centre de sécurité & conformité](../../media/6b213d34-adbb-44af-8549-be9a7e2db087.png)

## <a name="advanced-threat-protection-file-types-report"></a><span data-ttu-id="310c9-108">Rapport sur les types de fichiers de Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="310c9-108">Advanced Threat Protection file types report</span></span>

<span data-ttu-id="310c9-109">Le rapport de rapports sur les **types de fichiers de protection avancée contre les menaces** indique le type de fichiers détectés comme malveillants par des [pièces jointes fiables](atp-safe-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="310c9-109">The **Advanced Threat Protection file types report** report shows you the type of files detected as malicious by [Safe Attachments](atp-safe-attachments.md).</span></span>

 <span data-ttu-id="310c9-110">La vue agrégée du rapport autorise 90 jours de filtrage, tandis que l’affichage détaillé autorise uniquement les 10 jours de filtrage.</span><span class="sxs-lookup"><span data-stu-id="310c9-110">The aggregate view of the report allows for 90 days of filtering, while the detail view only allows for 10 days of filtering.</span></span>

<span data-ttu-id="310c9-111">Pour afficher le rapport, ouvrez le [Centre de sécurité & conformité](https://protection.office.com), accédez **Reports** au \> **tableau de bord** rapports et sélectionnez **types de fichiers Office ATP**.</span><span class="sxs-lookup"><span data-stu-id="310c9-111">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Office ATP file types**.</span></span> <span data-ttu-id="310c9-112">Pour accéder directement au rapport, ouvrez <https://protection.office.com/reportv2?id=ATPFileReport> .</span><span class="sxs-lookup"><span data-stu-id="310c9-112">To go directly to the report, open <https://protection.office.com/reportv2?id=ATPFileReport>.</span></span>

![Widget de types de fichiers ATP Office dans le tableau de bord rapports](../../media/atp-file-types-report-widget.png)

> [!NOTE]
> <span data-ttu-id="310c9-114">Les informations contenues dans ce rapport sont également disponibles dans le [rapport de suppression des messages de protection avancée contre les menaces](#advanced-threat-protection-message-disposition-report).</span><span class="sxs-lookup"><span data-stu-id="310c9-114">The information in this report is also available in the [Advanced Threat Protection message disposition report](#advanced-threat-protection-message-disposition-report).</span></span>

### <a name="report-view-for-the-advanced-threat-protection-file-types-report"></a><span data-ttu-id="310c9-115">Affichage de rapport pour le rapport de types de fichiers de protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="310c9-115">Report view for the Advanced Threat Protection file types report</span></span>

<span data-ttu-id="310c9-116">Les vues disponibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="310c9-116">The following views are available:</span></span>

- <span data-ttu-id="310c9-117">**Afficher les données par : fichier**: le graphique contient les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="310c9-117">**View data by: File**: The chart contains the following information:</span></span>

  - <span data-ttu-id="310c9-118">**Pièces jointes Excel malveillantes**</span><span class="sxs-lookup"><span data-stu-id="310c9-118">**Malicious Excel attachments**</span></span>
  - <span data-ttu-id="310c9-119">**Pièces jointes Flash malveillantes**</span><span class="sxs-lookup"><span data-stu-id="310c9-119">**Malicious Flash attachments**</span></span>
  - <span data-ttu-id="310c9-120">**Pièces jointes PDF malveillantes**</span><span class="sxs-lookup"><span data-stu-id="310c9-120">**Malicious PDF attachments**</span></span>
  - <span data-ttu-id="310c9-121">**Pièces jointes PowerPoint malveillantes**</span><span class="sxs-lookup"><span data-stu-id="310c9-121">**Malicious PowerPoint attachments**</span></span>
  - <span data-ttu-id="310c9-122">**URL malveillantes**</span><span class="sxs-lookup"><span data-stu-id="310c9-122">**Malicious URLs**</span></span>
  - <span data-ttu-id="310c9-123">**Pièces jointes de mots malveillants**</span><span class="sxs-lookup"><span data-stu-id="310c9-123">**Malicious Word attachments**</span></span>
  - <span data-ttu-id="310c9-124">**Pièces jointes exécutables malveillants**</span><span class="sxs-lookup"><span data-stu-id="310c9-124">**Malicious executable attachments**</span></span>
  - <span data-ttu-id="310c9-125">**Autres**</span><span class="sxs-lookup"><span data-stu-id="310c9-125">**Others**</span></span>

  <span data-ttu-id="310c9-126">Lorsque vous pointez sur un jour particulier (point de données), vous pouvez voir la répartition des types de fichiers malveillants détectés par [les pièces jointes fiables](atp-safe-attachments.md) et la protection contre les [programmes malveillants dans EOP](anti-malware-protection.md).</span><span class="sxs-lookup"><span data-stu-id="310c9-126">When you hover over a particular day (data point), you can see the breakdown of types of malicious files that were detected by [Safe Attachments](atp-safe-attachments.md) and [anti-malware protection in EOP](anti-malware-protection.md).</span></span>

  ![Vue de fichier dans le rapport des types de fichiers ATP](../../media/atp-file-types-report-file-view.png)

  <span data-ttu-id="310c9-128">Si vous cliquez sur **filtres**, vous pouvez modifier le rapport avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="310c9-128">If you click **Filters**, you can modify the report with the following filters:</span></span>

  - <span data-ttu-id="310c9-129">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="310c9-129">**Start date** and **End date**</span></span>
  - <span data-ttu-id="310c9-130">Les mêmes valeurs de types de fichiers qui sont visibles dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="310c9-130">The same file type values that are visible in the chart.</span></span>

- <span data-ttu-id="310c9-131">**Afficher les données par : message**: le graphique contient les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="310c9-131">**View data by: Message**: The chart contains the following information:</span></span>

  - <span data-ttu-id="310c9-132">**Bloquer l’accès**</span><span class="sxs-lookup"><span data-stu-id="310c9-132">**Block access**</span></span>
  - <span data-ttu-id="310c9-133">**Messages remplacés**</span><span class="sxs-lookup"><span data-stu-id="310c9-133">**Messages replaced**</span></span>
  - <span data-ttu-id="310c9-134">**Messages surveillés**</span><span class="sxs-lookup"><span data-stu-id="310c9-134">**Messages monitored**</span></span>
  - <span data-ttu-id="310c9-135">**Remplacé par remise de courrier dynamique**: pour plus d’informations, consultez la rubrique [distribution dynamique dans les stratégies de pièces jointes approuvées](atp-safe-attachments.md#dynamic-delivery-in-safe-attachments-policies).</span><span class="sxs-lookup"><span data-stu-id="310c9-135">**Replaced by Dynamic Email Delivery**: For more information, see [Dynamic Delivery in Safe Attachments policies](atp-safe-attachments.md#dynamic-delivery-in-safe-attachments-policies).</span></span>

  ![Affichage des messages dans le rapport sur les types de fichiers ATP](../../media/atp-file-types-report-message-view.png)

  <span data-ttu-id="310c9-137">Si vous cliquez sur **filtres**, vous pouvez modifier le rapport avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="310c9-137">If you click **Filters**, you can modify the report with the following filters:</span></span>

  - <span data-ttu-id="310c9-138">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="310c9-138">**Start date** and **End date**</span></span>
  - <span data-ttu-id="310c9-139">Les mêmes valeurs de disposition de message disponibles dans le graphique et la valeur de **messages supplémentaires transmises** .</span><span class="sxs-lookup"><span data-stu-id="310c9-139">The same message disposition values that are available in the chart, and the additional **Messages passed** value.</span></span>

### <a name="details-table-view-for-the-advanced-threat-protection-file-types-report"></a><span data-ttu-id="310c9-140">Vue de la table Détails pour le rapport des types de fichiers de protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="310c9-140">Details table view for the Advanced Threat Protection file types report</span></span>

<span data-ttu-id="310c9-141">Si vous cliquez sur **afficher les détails table**, le rapport fournit une vue quasi en temps réel de tous les clics effectués au sein de l’organisation au cours des 10 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="310c9-141">If you click **View details table**, the report provides a near-real-time view of all clicks that happen within the organization for the last 10 days.</span></span> <span data-ttu-id="310c9-142">Les informations affichées dépendent du graphique que vous recherchez :</span><span class="sxs-lookup"><span data-stu-id="310c9-142">The information that's shown depends on the chart you were looking at:</span></span>

- <span data-ttu-id="310c9-143">**Afficher les données par : fichier**:</span><span class="sxs-lookup"><span data-stu-id="310c9-143">**View data by: File**:</span></span>

  - <span data-ttu-id="310c9-144">**Date**</span><span class="sxs-lookup"><span data-stu-id="310c9-144">**Date**</span></span>
  - <span data-ttu-id="310c9-145">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="310c9-145">**Recipient address**</span></span>
  - <span data-ttu-id="310c9-146">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="310c9-146">**Sender address**</span></span>
  - <span data-ttu-id="310c9-147">**ID du message**: disponible dans le champ d’en-tête **message-ID** de l’en-tête du message et doit être unique.</span><span class="sxs-lookup"><span data-stu-id="310c9-147">**Message ID**: Available in the **Message-ID** header field in the message header and should be unique.</span></span> <span data-ttu-id="310c9-148">Un exemple de valeur est `<08f1e0f6806a47b4ac103961109ae6ef@server.domain>` (Notez les chevrons).</span><span class="sxs-lookup"><span data-stu-id="310c9-148">An example value is `<08f1e0f6806a47b4ac103961109ae6ef@server.domain>` (note the angle brackets).</span></span>
  - <span data-ttu-id="310c9-149">**File**</span><span class="sxs-lookup"><span data-stu-id="310c9-149">**File**</span></span>

  <span data-ttu-id="310c9-150">Si vous cliquez sur **filtres**, vous pouvez modifier le rapport avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="310c9-150">If you click **Filters**, you can modify the report with the following filters:</span></span>

  - <span data-ttu-id="310c9-151">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="310c9-151">**Start date** and **End date**</span></span>
  - <span data-ttu-id="310c9-152">Les mêmes valeurs de types de fichiers qui sont visibles dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="310c9-152">The same file type values that are visible in the chart.</span></span>

- <span data-ttu-id="310c9-153">**Afficher les données par : message**:</span><span class="sxs-lookup"><span data-stu-id="310c9-153">**View data by: Message**:</span></span>

  - <span data-ttu-id="310c9-154">**Date**</span><span class="sxs-lookup"><span data-stu-id="310c9-154">**Date**</span></span>
  - <span data-ttu-id="310c9-155">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="310c9-155">**Recipient address**</span></span>
  - <span data-ttu-id="310c9-156">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="310c9-156">**Sender address**</span></span>
  - <span data-ttu-id="310c9-157">**ID de message**</span><span class="sxs-lookup"><span data-stu-id="310c9-157">**Message ID**</span></span>
  - <span data-ttu-id="310c9-158">**File**</span><span class="sxs-lookup"><span data-stu-id="310c9-158">**File**</span></span>
  - <span data-ttu-id="310c9-159">**Subject**</span><span class="sxs-lookup"><span data-stu-id="310c9-159">**Subject**</span></span>

  <span data-ttu-id="310c9-160">Si vous cliquez sur **filtres**, vous pouvez modifier les résultats à l’aide des filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="310c9-160">If you click **Filters**, you can modify the results with the following filters:</span></span>

  - <span data-ttu-id="310c9-161">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="310c9-161">**Start date** and **End date**</span></span>
  - <span data-ttu-id="310c9-162">Les mêmes valeurs de disposition de message disponibles dans le graphique et la valeur de **messages supplémentaires transmises** .</span><span class="sxs-lookup"><span data-stu-id="310c9-162">The same message disposition values that are available in the chart, and the additional **Messages passed** value.</span></span>

<span data-ttu-id="310c9-163">Pour revenir à l’affichage rapports, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="310c9-163">To get back to the reports view, click **View report**.</span></span>

## <a name="advanced-threat-protection-message-disposition-report"></a><span data-ttu-id="310c9-164">Rapport sur la destruction des messages de Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="310c9-164">Advanced Threat Protection message disposition report</span></span>

<span data-ttu-id="310c9-165">Le rapport de **disposition des messages ATP** indique les actions qui ont été effectuées pour les messages électroniques détectés comme présentant du contenu malveillant.</span><span class="sxs-lookup"><span data-stu-id="310c9-165">The **ATP Message Disposition** report shows you the actions that were taken for email messages that were detected as having malicious content.</span></span>

<span data-ttu-id="310c9-166">Pour afficher le rapport, ouvrez le [Centre de sécurité & conformité](https://protection.office.com), accédez à **rapports** \> **Dashboard** et sélectionnez **Office ATP message disposition**.</span><span class="sxs-lookup"><span data-stu-id="310c9-166">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Office ATP message disposition**.</span></span> <span data-ttu-id="310c9-167">Pour accéder directement au rapport, ouvrez <https://protection.office.com/reportv2?id=ATPMessageReport> .</span><span class="sxs-lookup"><span data-stu-id="310c9-167">To go directly to the report, open <https://protection.office.com/reportv2?id=ATPMessageReport>.</span></span>

![Widget disposition du message DAV Office 365 dans le tableau de bord rapports](../../media/atp-message-disposition-report-widget.png)

> [!NOTE]
> <span data-ttu-id="310c9-169">Les informations contenues dans ce rapport sont également disponibles dans le [rapport types de fichiers de protection avancée contre les menaces](#advanced-threat-protection-file-types-report).</span><span class="sxs-lookup"><span data-stu-id="310c9-169">The information in this report is also available in the [Advanced Threat Protection file types report](#advanced-threat-protection-file-types-report).</span></span>

### <a name="report-view-for-the-advanced-threat-protection-message-disposition-report"></a><span data-ttu-id="310c9-170">Affichage de rapport pour le rapport de disposition de messages de protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="310c9-170">Report view for the Advanced Threat Protection message disposition report</span></span>

<span data-ttu-id="310c9-171">Les vues disponibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="310c9-171">The following views are available:</span></span>

- <span data-ttu-id="310c9-172">**Afficher les données par : message**: le graphique contient les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="310c9-172">**View data by: Message**: The chart contains the following information:</span></span>

  - <span data-ttu-id="310c9-173">**Bloquer l’accès**</span><span class="sxs-lookup"><span data-stu-id="310c9-173">**Block access**</span></span>
  - <span data-ttu-id="310c9-174">**Messages remplacés**</span><span class="sxs-lookup"><span data-stu-id="310c9-174">**Messages replaced**</span></span>
  - <span data-ttu-id="310c9-175">**Messages surveillés**</span><span class="sxs-lookup"><span data-stu-id="310c9-175">**Messages monitored**</span></span>
  - <span data-ttu-id="310c9-176">**Remplacé par remise de courrier dynamique**: pour plus d’informations, consultez la rubrique [distribution dynamique dans les stratégies de pièces jointes approuvées](atp-safe-attachments.md#dynamic-delivery-in-safe-attachments-policies).</span><span class="sxs-lookup"><span data-stu-id="310c9-176">**Replaced by Dynamic Email Delivery**: For more information, see [Dynamic Delivery in Safe Attachments policies](atp-safe-attachments.md#dynamic-delivery-in-safe-attachments-policies).</span></span>

  ![Affichage des messages dans le rapport sur les types de fichiers ATP](../../media/atp-file-types-report-message-view.png)

  <span data-ttu-id="310c9-178">Si vous cliquez sur **filtres**, vous pouvez modifier le rapport avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="310c9-178">If you click **Filters**, you can modify the report with the following filters:</span></span>

  - <span data-ttu-id="310c9-179">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="310c9-179">**Start date** and **End date**</span></span>
  - <span data-ttu-id="310c9-180">Les mêmes valeurs de disposition de message disponibles dans le graphique et la valeur de **messages supplémentaires transmises** .</span><span class="sxs-lookup"><span data-stu-id="310c9-180">The same message disposition values that are available in the chart, and the additional **Messages passed** value.</span></span>

- <span data-ttu-id="310c9-181">**Afficher les données par : fichier**: le graphique contient les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="310c9-181">**View data by: File**: The chart contains the following information:</span></span>

  - <span data-ttu-id="310c9-182">**Pièces jointes Excel malveillantes**</span><span class="sxs-lookup"><span data-stu-id="310c9-182">**Malicious Excel attachments**</span></span>
  - <span data-ttu-id="310c9-183">**Pièces jointes Flash malveillantes**</span><span class="sxs-lookup"><span data-stu-id="310c9-183">**Malicious Flash attachments**</span></span>
  - <span data-ttu-id="310c9-184">**Pièces jointes PDF malveillantes**</span><span class="sxs-lookup"><span data-stu-id="310c9-184">**Malicious PDF attachments**</span></span>
  - <span data-ttu-id="310c9-185">**Pièces jointes PowerPoint malveillantes**</span><span class="sxs-lookup"><span data-stu-id="310c9-185">**Malicious PowerPoint attachments**</span></span>
  - <span data-ttu-id="310c9-186">**URL malveillantes**</span><span class="sxs-lookup"><span data-stu-id="310c9-186">**Malicious URLs**</span></span>
  - <span data-ttu-id="310c9-187">**Pièces jointes de mots malveillants**</span><span class="sxs-lookup"><span data-stu-id="310c9-187">**Malicious Word attachments**</span></span>
  - <span data-ttu-id="310c9-188">**Pièces jointes exécutables malveillants**</span><span class="sxs-lookup"><span data-stu-id="310c9-188">**Malicious executable attachments**</span></span>
  - <span data-ttu-id="310c9-189">**Autres**</span><span class="sxs-lookup"><span data-stu-id="310c9-189">**Others**</span></span>

  <span data-ttu-id="310c9-190">Lorsque vous pointez sur un jour particulier (point de données), vous pouvez voir la répartition des types de fichiers malveillants détectés par [les pièces jointes fiables](atp-safe-attachments.md) et la protection contre les [programmes malveillants dans EOP](anti-malware-protection.md).</span><span class="sxs-lookup"><span data-stu-id="310c9-190">When you hover over a particular day (data point), you can see the breakdown of types of malicious files that were detected by [Safe Attachments](atp-safe-attachments.md) and [anti-malware protection in EOP](anti-malware-protection.md).</span></span>

  ![Vue de fichier dans le rapport des types de fichiers ATP](../../media/atp-file-types-report-file-view.png)

  <span data-ttu-id="310c9-192">Si vous cliquez sur **filtres**, vous pouvez modifier le rapport avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="310c9-192">If you click **Filters**, you can modify the report with the following filters:</span></span>

  - <span data-ttu-id="310c9-193">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="310c9-193">**Start date** and **End date**</span></span>
  - <span data-ttu-id="310c9-194">Les mêmes valeurs de types de fichiers qui sont visibles dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="310c9-194">The same file type values that are visible in the chart.</span></span>

### <a name="details-table-view-for-the-advanced-threat-protection-message-disposition-report"></a><span data-ttu-id="310c9-195">Vue de la table Détails pour le rapport de disposition de messages de protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="310c9-195">Details table view for the Advanced Threat Protection message disposition report</span></span>

<span data-ttu-id="310c9-196">Si vous cliquez sur **afficher les détails table**, le rapport fournit une vue quasi en temps réel de tous les clics effectués au sein de l’organisation au cours des 10 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="310c9-196">If you click **View details table**, the report provides a near-real-time view of all clicks that happen within the organization for the last 10 days.</span></span> <span data-ttu-id="310c9-197">Les informations affichées dépendent du graphique que vous recherchez :</span><span class="sxs-lookup"><span data-stu-id="310c9-197">The information that's shown depends on the chart you were looking at:</span></span>

- <span data-ttu-id="310c9-198">**Afficher les données par : message**:</span><span class="sxs-lookup"><span data-stu-id="310c9-198">**View data by: Message**:</span></span>

  - <span data-ttu-id="310c9-199">**Date**</span><span class="sxs-lookup"><span data-stu-id="310c9-199">**Date**</span></span>
  - <span data-ttu-id="310c9-200">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="310c9-200">**Recipient address**</span></span>
  - <span data-ttu-id="310c9-201">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="310c9-201">**Sender address**</span></span>
  - <span data-ttu-id="310c9-202">**ID de message**</span><span class="sxs-lookup"><span data-stu-id="310c9-202">**Message ID**</span></span>
  - <span data-ttu-id="310c9-203">**File**</span><span class="sxs-lookup"><span data-stu-id="310c9-203">**File**</span></span>
  - <span data-ttu-id="310c9-204">**Subject**</span><span class="sxs-lookup"><span data-stu-id="310c9-204">**Subject**</span></span>

  <span data-ttu-id="310c9-205">Si vous cliquez sur **filtres**, vous pouvez modifier les résultats à l’aide des filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="310c9-205">If you click **Filters**, you can modify the results with the following filters:</span></span>

  - <span data-ttu-id="310c9-206">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="310c9-206">**Start date** and **End date**</span></span>
  - <span data-ttu-id="310c9-207">Les mêmes valeurs de disposition de message disponibles dans le graphique et la valeur de **messages supplémentaires transmises** .</span><span class="sxs-lookup"><span data-stu-id="310c9-207">The same message disposition values that are available in the chart, and the additional **Messages passed** value.</span></span>

- <span data-ttu-id="310c9-208">**Afficher les données par : fichier**:</span><span class="sxs-lookup"><span data-stu-id="310c9-208">**View data by: File**:</span></span>

  - <span data-ttu-id="310c9-209">**Date**</span><span class="sxs-lookup"><span data-stu-id="310c9-209">**Date**</span></span>
  - <span data-ttu-id="310c9-210">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="310c9-210">**Recipient address**</span></span>
  - <span data-ttu-id="310c9-211">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="310c9-211">**Sender address**</span></span>
  - <span data-ttu-id="310c9-212">**ID de message**</span><span class="sxs-lookup"><span data-stu-id="310c9-212">**Message ID**</span></span>
  - <span data-ttu-id="310c9-213">**File**</span><span class="sxs-lookup"><span data-stu-id="310c9-213">**File**</span></span>

  <span data-ttu-id="310c9-214">Si vous cliquez sur **filtres**, vous pouvez modifier le rapport avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="310c9-214">If you click **Filters**, you can modify the report with the following filters:</span></span>

  - <span data-ttu-id="310c9-215">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="310c9-215">**Start date** and **End date**</span></span>
  - <span data-ttu-id="310c9-216">Les mêmes valeurs de types de fichiers qui sont visibles dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="310c9-216">The same file type values that are visible in the chart.</span></span>

<span data-ttu-id="310c9-217">Pour revenir à l’affichage rapports, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="310c9-217">To get back to the reports view, click **View report**.</span></span>

## <a name="threat-protection-status-report"></a><span data-ttu-id="310c9-218">Rapport sur l’état de la protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="310c9-218">Threat protection status report</span></span>

<span data-ttu-id="310c9-219">Le rapport d' **État de protection contre les menaces** est une vue unique qui rassemble des informations sur le contenu malveillant et les e-mails malveillants détectés et bloqués par [Exchange Online Protection](exchange-online-protection-overview.md) (EOP) et Office 365 ATP.</span><span class="sxs-lookup"><span data-stu-id="310c9-219">The **Threat protection status** report is a single view that brings together information about malicious content and malicious email detected and blocked by [Exchange Online Protection](exchange-online-protection-overview.md) (EOP) and Office 365 ATP.</span></span> <span data-ttu-id="310c9-220">Pour plus d’informations, consultez la rubrique [Threat Protection Status Report](view-email-security-reports.md#threat-protection-status-report).</span><span class="sxs-lookup"><span data-stu-id="310c9-220">For more information, see [Threat protection status report](view-email-security-reports.md#threat-protection-status-report).</span></span>

## <a name="url-threat-protection-report"></a><span data-ttu-id="310c9-221">Rapport d’URL de protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="310c9-221">URL threat protection report</span></span>

<span data-ttu-id="310c9-222">Le **rapport URL protection contre les menaces** fournit des vues récapitulatives et des tendances pour les menaces détectées, ainsi que les actions effectuées sur les clics d’URL dans le cadre de [liens fiables](atp-safe-links.md).</span><span class="sxs-lookup"><span data-stu-id="310c9-222">The **URL threat protection report** provides summary and trend views for threats detected and actions taken on URL clicks as part of [Safe Links](atp-safe-links.md).</span></span> <span data-ttu-id="310c9-223">Ce rapport n’aura pas de clic sur les données des utilisateurs pour lesquels la stratégie de liens fiables est sélectionnée, l’option **ne pas suivre les clics utilisateur** est activée.</span><span class="sxs-lookup"><span data-stu-id="310c9-223">This report will not have click data from users where the Safe Links policy applied has the **Do not track user clicks** option selected.</span></span>

<span data-ttu-id="310c9-224">Pour afficher le rapport, ouvrez le [Centre de sécurité & conformité](https://protection.office.com), accédez **Reports** au \> **tableau de bord** rapports et sélectionnez **URL protection Report**.</span><span class="sxs-lookup"><span data-stu-id="310c9-224">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **URL protection report**.</span></span> <span data-ttu-id="310c9-225">Pour accéder directement au rapport, ouvrez <https://protection.office.com/reportv2?id=URLProtectionActionReport> .</span><span class="sxs-lookup"><span data-stu-id="310c9-225">To go directly to the report, open <https://protection.office.com/reportv2?id=URLProtectionActionReport>.</span></span>

![Widget rapport de protection des URL dans le tableau de bord rapports](../../media/url-protection-report-widget.png)

> [!NOTE]
> <span data-ttu-id="310c9-227">Il s’agit d’un *rapport de tendance de protection*, ce qui signifie que les données représentent des tendances dans un jeu de données plus volumineux.</span><span class="sxs-lookup"><span data-stu-id="310c9-227">This is a *protection trend report*, meaning data represents trends in a larger dataset.</span></span> <span data-ttu-id="310c9-228">Par conséquent, les données de l’affichage agrégé ne sont pas disponibles en temps réel ici, mais les données de la vue de la table des détails sont, de sorte que vous pouvez constater une légère divergence entre les deux vues.</span><span class="sxs-lookup"><span data-stu-id="310c9-228">As a result, the data in the aggregate view is not available in real time here, but the data in the details table view is, so you may see a slight discrepancy between the two views.</span></span>

### <a name="report-view-for-the-url-threat-protection-report"></a><span data-ttu-id="310c9-229">Affichage de rapport pour le rapport d’URL protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="310c9-229">Report view for the URL threat protection report</span></span>

<span data-ttu-id="310c9-230">Le rapport **URL protection contre les menaces** comporte deux vues agrégées qui sont actualisées toutes les quatre heures, qui affichent les données des 90 derniers jours :</span><span class="sxs-lookup"><span data-stu-id="310c9-230">The **URL threat protection** report has two aggregated views that are refreshed once every four hours that shows data for the last 90 days:</span></span>

- <span data-ttu-id="310c9-231">**URL cliquez sur protection action**: indique le nombre de clics d’URL par les utilisateurs de l’organisation, ainsi que les résultats du Click :</span><span class="sxs-lookup"><span data-stu-id="310c9-231">**URL click protection action**: Shows the number of URL clicks by users in the organization and the results of the click:</span></span>

  - <span data-ttu-id="310c9-232">**Bloqué** (l’utilisateur n’a pas pu accéder à l’URL)</span><span class="sxs-lookup"><span data-stu-id="310c9-232">**Blocked** (the user was blocked from navigating to the URL)</span></span>
  - <span data-ttu-id="310c9-233">**Bloqué et clic sur**</span><span class="sxs-lookup"><span data-stu-id="310c9-233">**Blocked and clicked through**</span></span>
  - <span data-ttu-id="310c9-234">**Clic lors de l’analyse**</span><span class="sxs-lookup"><span data-stu-id="310c9-234">**Clicked through during scan**</span></span>

  <span data-ttu-id="310c9-235">Un clic indique que l’utilisateur a cliqué sur la page bloquer pour le site Web malveillant (les administrateurs peuvent désactiver l’option cliquer via dans les stratégies de liens fiables).</span><span class="sxs-lookup"><span data-stu-id="310c9-235">A click indicates that the user has clicked through the block page to the malicious website (admins can disable click through in Safe Links policies).</span></span>

  <span data-ttu-id="310c9-236">Si vous cliquez sur **filtres**, vous pouvez modifier le rapport avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="310c9-236">If you click **Filters**, you can modify the report with the following filters:</span></span>

  - <span data-ttu-id="310c9-237">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="310c9-237">**Start date** and **End date**</span></span>
  - <span data-ttu-id="310c9-238">Les actions de protection clic disponibles, plus la valeur **autorisée** (l’utilisateur a été autorisé à accéder à l’URL).</span><span class="sxs-lookup"><span data-stu-id="310c9-238">The available click protection actions, plus the value **Allowed** (the user was allowed to navigate to the URL).</span></span>

  ![URL cliquez sur affichage d’action de protection dans le rapport d’URL protection contre les menaces](../../media/url-threat-protection-report-url-click-protection-action-view.png)

- <span data-ttu-id="310c9-240">**URL cliquez par application**: indique le nombre de clics d’URL par les applications qui prennent en charge les liens fiables :</span><span class="sxs-lookup"><span data-stu-id="310c9-240">**URL click by application**: Shows the number of URL clicks by applications that support Safe Links:</span></span>

  - <span data-ttu-id="310c9-241">**Client de messagerie**</span><span class="sxs-lookup"><span data-stu-id="310c9-241">**Email client**</span></span>
  - <span data-ttu-id="310c9-242">**PowerPoint**</span><span class="sxs-lookup"><span data-stu-id="310c9-242">**PowerPoint**</span></span>
  - <span data-ttu-id="310c9-243">**Word**</span><span class="sxs-lookup"><span data-stu-id="310c9-243">**Word**</span></span>
  - <span data-ttu-id="310c9-244">**Excel**</span><span class="sxs-lookup"><span data-stu-id="310c9-244">**Excel**</span></span>
  - <span data-ttu-id="310c9-245">**OneNote**</span><span class="sxs-lookup"><span data-stu-id="310c9-245">**OneNote**</span></span>
  - <span data-ttu-id="310c9-246">**Visio**</span><span class="sxs-lookup"><span data-stu-id="310c9-246">**Visio**</span></span>
  - <span data-ttu-id="310c9-247">**Équipes**</span><span class="sxs-lookup"><span data-stu-id="310c9-247">**Teams**</span></span>
  - <span data-ttu-id="310c9-248">**Other**</span><span class="sxs-lookup"><span data-stu-id="310c9-248">**Other**</span></span>

  <span data-ttu-id="310c9-249">Si vous cliquez sur **filtres**, vous pouvez modifier le rapport avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="310c9-249">If you click **Filters**, you can modify the report with the following filters:</span></span>

  - <span data-ttu-id="310c9-250">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="310c9-250">**Start date** and **End date**</span></span>
  - <span data-ttu-id="310c9-251">Les applications disponibles.</span><span class="sxs-lookup"><span data-stu-id="310c9-251">The available applications.</span></span>

### <a name="details-table-view-for-the-url-threat-protection-report"></a><span data-ttu-id="310c9-252">Vue de la table Détails pour le rapport URL protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="310c9-252">Details table view for the URL threat protection report</span></span>

<span data-ttu-id="310c9-253">Si vous cliquez sur **afficher les détails**de la table, le rapport fournit une vue quasi en temps réel de tous les clics effectués au sein de l’organisation pendant les 7 derniers jours avec les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="310c9-253">If you click **View details table**, the report provides a near-real-time view of all clicks that happen within the organization for the last 7 days with the following details:</span></span>

- <span data-ttu-id="310c9-254">**Cliquez sur heure**</span><span class="sxs-lookup"><span data-stu-id="310c9-254">**Click time**</span></span>
- <span data-ttu-id="310c9-255">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="310c9-255">**User**</span></span>
- <span data-ttu-id="310c9-256">**URL**</span><span class="sxs-lookup"><span data-stu-id="310c9-256">**URL**</span></span>
- <span data-ttu-id="310c9-257">**Action**</span><span class="sxs-lookup"><span data-stu-id="310c9-257">**Action**</span></span>
- <span data-ttu-id="310c9-258">**App**</span><span class="sxs-lookup"><span data-stu-id="310c9-258">**App**</span></span>

<span data-ttu-id="310c9-259">Si vous cliquez sur **filtres** dans la vue table des détails, vous pouvez filtrer selon les mêmes critères que dans l’affichage rapport, ainsi que par les **domaines** ou les **destinataires** séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="310c9-259">If you click **Filters** in the details table view, you can filter by the same criteria as in the report view, and also by **Domains** or **Recipients** separated by commas.</span></span>

<span data-ttu-id="310c9-260">Pour revenir à l’affichage rapports, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="310c9-260">To get back to the reports view, click **View report**.</span></span>

## <a name="additional-reports-to-view"></a><span data-ttu-id="310c9-261">Rapports supplémentaires à afficher</span><span class="sxs-lookup"><span data-stu-id="310c9-261">Additional reports to view</span></span>

<span data-ttu-id="310c9-262">Outre les rapports ATP décrits dans cette rubrique, plusieurs autres rapports sont disponibles, comme décrit dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="310c9-262">In addition to the ATP reports described in this topic, several other reports are available, as described in the following table:</span></span>

****

|<span data-ttu-id="310c9-263">Rapport</span><span class="sxs-lookup"><span data-stu-id="310c9-263">Report</span></span>|<span data-ttu-id="310c9-264">Rubrique</span><span class="sxs-lookup"><span data-stu-id="310c9-264">Topic</span></span>|
|---|---|
|<span data-ttu-id="310c9-265">**Explorateur** (plan ATP 2) ou **détections en temps réel** (plan ATP 1)</span><span class="sxs-lookup"><span data-stu-id="310c9-265">**Explorer** (ATP Plan 2) or **real-time detections** (ATP Plan 1)</span></span>|[<span data-ttu-id="310c9-266">Explorateur de menaces (et détections en temps réel)</span><span class="sxs-lookup"><span data-stu-id="310c9-266">Threat Explorer (and real-time detections)</span></span>](threat-explorer.md)|
|<span data-ttu-id="310c9-267">**Rapports de sécurité de messagerie**, tels que le rapport des expéditeurs et des destinataires principaux, le rapport de courrier indésirable et le rapport des détections de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="310c9-267">**Email security reports**, such as the Top senders and recipients report, the Spoof mail report, and the Spam detections report.</span></span>|[<span data-ttu-id="310c9-268">Afficher les rapports de sécurité de courrier dans le centre de sécurité et conformité</span><span class="sxs-lookup"><span data-stu-id="310c9-268">View email security reports in the Security & Compliance Center</span></span>](view-email-security-reports.md)|
|<span data-ttu-id="310c9-269">Les **rapports de flux de messagerie**, tels que le rapport de transfert, le rapport d’état de flux de messagerie et le rapport des expéditeurs et des destinataires principaux.</span><span class="sxs-lookup"><span data-stu-id="310c9-269">**Mail flow reports**, such as the Forwarding report, the Mailflow status report, and the Top senders and recipients report.</span></span>|[<span data-ttu-id="310c9-270">Afficher les rapports de flux de messagerie dans le centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="310c9-270">View mail flow reports in the Security & Compliance Center</span></span>](view-mail-flow-reports.md)|
|<span data-ttu-id="310c9-271">**Suivi des URL pour les liens fiables** (PowerShell uniquement).</span><span class="sxs-lookup"><span data-stu-id="310c9-271">**URL trace for Safe Links** (PowerShell only).</span></span> <span data-ttu-id="310c9-272">La sortie de cette cmdlet vous indique les résultats des actions de liens fiables au cours des sept derniers jours.</span><span class="sxs-lookup"><span data-stu-id="310c9-272">The output of this cmdlet shows you the results of Safe Links actions over the past seven days.</span></span>|[<span data-ttu-id="310c9-273">Get-UrlTrace</span><span class="sxs-lookup"><span data-stu-id="310c9-273">Get-UrlTrace</span></span>](https://docs.microsoft.com/powershell/module/exchange/get-urltrace)|
|<span data-ttu-id="310c9-274">**Résultats du trafic de messagerie pour EOP et ATP** (PowerShell uniquement).</span><span class="sxs-lookup"><span data-stu-id="310c9-274">**Mail traffic results for EOP and ATP** (PowerShell only).</span></span> <span data-ttu-id="310c9-275">La sortie de cette applet de commande contient des informations sur le domaine, la date, le type d’événement, la direction, l’action et le nombre de messages.</span><span class="sxs-lookup"><span data-stu-id="310c9-275">The output of this cmdlet contains information about Domain, Date, Event Type, Direction, Action, and Message Count.</span></span>|[<span data-ttu-id="310c9-276">Get-MailTrafficATPReport</span><span class="sxs-lookup"><span data-stu-id="310c9-276">Get-MailTrafficATPReport</span></span>](https://docs.microsoft.com/powershell/module/exchange/get-mailtrafficatpreport)|
|<span data-ttu-id="310c9-277">**Rapports de détail du courrier pour les détections EOP et ATP** (PowerShell uniquement).</span><span class="sxs-lookup"><span data-stu-id="310c9-277">**Mail detail reports for EOP and ATP detections** (PowerShell only).</span></span> <span data-ttu-id="310c9-278">La sortie de cette applet de commande contient des détails sur les URL ou les fichiers malveillants, les tentatives de hameçonnage, l’emprunt d’identité et d’autres menaces potentielles dans les messages ou les fichiers.</span><span class="sxs-lookup"><span data-stu-id="310c9-278">The output of this cmdlet contains details about malicious files or URLs, phishing attempts, impersonation, and other potential threats in email or files.</span></span>|[<span data-ttu-id="310c9-279">Get-MailDetailATPReport</span><span class="sxs-lookup"><span data-stu-id="310c9-279">Get-MailDetailATPReport</span></span>](https://docs.microsoft.com/powershell/module/exchange/get-maildetailatpreport)|
|

## <a name="what-permissions-are-needed-to-view-the-atp-reports"></a><span data-ttu-id="310c9-280">Quelles sont les autorisations nécessaires pour afficher les rapports ATP ?</span><span class="sxs-lookup"><span data-stu-id="310c9-280">What permissions are needed to view the ATP reports?</span></span>

<span data-ttu-id="310c9-281">Pour afficher et utiliser les rapports décrits dans cette rubrique, **vous devez disposer d’un rôle approprié pour le centre de sécurité &amp; et le centre d’administration Exchange**.</span><span class="sxs-lookup"><span data-stu-id="310c9-281">In order to view and use the reports described in this topic, **you must have an appropriate role assigned for both the Security &amp; Compliance Center and the Exchange admin center**.</span></span>

- <span data-ttu-id="310c9-282">Pour le centre de sécurité & conformité, vous devez disposer de l’un des rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="310c9-282">For the Security & Compliance Center, you must have one of the following roles assigned:</span></span>

  - <span data-ttu-id="310c9-283">Gestion de l’organisation</span><span class="sxs-lookup"><span data-stu-id="310c9-283">Organization Management</span></span>
  - <span data-ttu-id="310c9-284">Administrateur de la sécurité (qui peut être affecté dans le centre d’administration Azure Active Directory ( [https://aad.portal.azure.com](https://aad.portal.azure.com) ))</span><span class="sxs-lookup"><span data-stu-id="310c9-284">Security Administrator (this can be assigned in the Azure Active Directory admin center ([https://aad.portal.azure.com](https://aad.portal.azure.com)))</span></span>
  - <span data-ttu-id="310c9-285">Opérateur de sécurité (cela peut être attribué dans le centre d’administration Azure Active Directory ( [https://aad.portal.azure.com](https://aad.portal.azure.com) ))</span><span class="sxs-lookup"><span data-stu-id="310c9-285">Security Operator (this can be assigned in the Azure Active Directory admin center ([https://aad.portal.azure.com](https://aad.portal.azure.com)))</span></span>
  - <span data-ttu-id="310c9-286">Lecteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="310c9-286">Security Reader</span></span>

- <span data-ttu-id="310c9-287">Pour Exchange Online, vous devez disposer de l’un des rôles suivants, qui est affecté dans le centre d’administration Exchange ( [https://outlook.office365.com/ecp](https://outlook.office365.com/ecp) ) ou avec des applets de commande PowerShell (consultez la rubrique [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online-powershell)) :</span><span class="sxs-lookup"><span data-stu-id="310c9-287">For Exchange Online, you must have one of the following roles assigned in either the Exchange admin center ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) or with PowerShell cmdlets (See [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online-powershell)):</span></span>

  - <span data-ttu-id="310c9-288">Gestion de l’organisation</span><span class="sxs-lookup"><span data-stu-id="310c9-288">Organization Management</span></span>
  - <span data-ttu-id="310c9-289">Gestion de l’organisation en affichage seul</span><span class="sxs-lookup"><span data-stu-id="310c9-289">View-only Organization Management</span></span>
  - <span data-ttu-id="310c9-290">Rôle Destinataires en affichage uniquement</span><span class="sxs-lookup"><span data-stu-id="310c9-290">View-Only Recipients role</span></span>
  - <span data-ttu-id="310c9-291">Gestion de la conformité</span><span class="sxs-lookup"><span data-stu-id="310c9-291">Compliance Management</span></span>

<span data-ttu-id="310c9-292">Pour en savoir plus, consultez les ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="310c9-292">To learn more, see the following resources:</span></span>

- [<span data-ttu-id="310c9-293">Autorisations dans le centre de conformité et de sécurité</span><span class="sxs-lookup"><span data-stu-id="310c9-293">Permissions in the Security & Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)

- [<span data-ttu-id="310c9-294">Autorisations des fonctionnalités dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="310c9-294">Feature permissions in Exchange Online</span></span>](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)

## <a name="what-if-the-reports-arent-showing-data"></a><span data-ttu-id="310c9-295">Qu’en est-il si les rapports n’affichent pas de données ?</span><span class="sxs-lookup"><span data-stu-id="310c9-295">What if the reports aren't showing data?</span></span>

<span data-ttu-id="310c9-296">Si vous ne voyez pas de données dans vos rapports ATP, vérifiez que vos stratégies sont correctement configurées.</span><span class="sxs-lookup"><span data-stu-id="310c9-296">If you are not seeing data in your ATP reports, double-check that your policies are set up correctly.</span></span> <span data-ttu-id="310c9-297">Votre organisation doit avoir [des stratégies de liens fiables](set-up-atp-safe-links-policies.md) et des [stratégies de pièces jointes approuvées](set-up-atp-safe-attachments-policies.md) définies afin que la protection ATP soit mise en place.</span><span class="sxs-lookup"><span data-stu-id="310c9-297">Your organization must have [Safe Links policies](set-up-atp-safe-links-policies.md) and [Safe Attachments policies](set-up-atp-safe-attachments-policies.md) defined in order for ATP protection to be in place.</span></span> <span data-ttu-id="310c9-298">Consultez également la rubrique protection contre le [courrier indésirable et les programmes malveillants](anti-spam-and-anti-malware-protection.md).</span><span class="sxs-lookup"><span data-stu-id="310c9-298">Also see [Anti-spam and anti-malware protection](anti-spam-and-anti-malware-protection.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="310c9-299">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="310c9-299">Related topics</span></span>

[<span data-ttu-id="310c9-300">Rapports intelligents et aperçus dans le Centre de sécurité et conformité</span><span class="sxs-lookup"><span data-stu-id="310c9-300">Smart reports and insights in the Security & Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="310c9-301">Autorisations de rôle (Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="310c9-301">Role permissions (Azure Active Directory</span></span>](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#role-permissions)
