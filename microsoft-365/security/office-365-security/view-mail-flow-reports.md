---
title: Afficher les rapports de flux de messagerie dans le tableau de bord Rapports
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: how-to
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: ''
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent en savoir plus sur les rapports de flux de messagerie disponibles dans le tableau de bord Rapports du Centre de sécurité & conformité.
ms.custom: ''
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: d1fea50ff0eaa5ed7d671485483ecb297b404db9
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50906551"
---
# <a name="view-mail-flow-reports-in-the-reports-dashboard-in-security--compliance-center"></a><span data-ttu-id="db820-103">Afficher les rapports de flux de messagerie dans le tableau de bord Rapports du Centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="db820-103">View mail flow reports in the Reports dashboard in Security & Compliance Center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="db820-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="db820-104">**Applies to**</span></span>
- [<span data-ttu-id="db820-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="db820-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="db820-106">Microsoft Defender pour Office 365 Plan 1 et Plan 2</span><span class="sxs-lookup"><span data-stu-id="db820-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](office-365-atp.md)
- [<span data-ttu-id="db820-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="db820-107">Microsoft 365 Defender</span></span>](../mtp/microsoft-threat-protection.md)

<span data-ttu-id="db820-108">Outre les rapports de flux de [](mail-flow-insights-v2.md) messagerie disponibles dans le tableau de bord de flux de messagerie dans le Centre de sécurité & conformité, plusieurs rapports de flux de messagerie supplémentaires sont disponibles dans le tableau de bord Rapports pour vous aider à surveiller votre organisation Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="db820-108">In addition to the mail flow reports that are available in the [Mail flow dashboard](mail-flow-insights-v2.md) in the Security & Compliance Center, a variety of additional mail flow reports are available in the Reports dashboard to help you monitor your Microsoft 365 organization.</span></span>

<span data-ttu-id="db820-109">Si vous avez les [autorisations](#what-permissions-are-needed-to-view-these-reports)nécessaires, vous pouvez afficher ces rapports dans le Centre de sécurité [& conformité](https://protection.office.com) en allant au Tableau **de bord des** \> **rapports.**</span><span class="sxs-lookup"><span data-stu-id="db820-109">If you have the [necessary permissions](#what-permissions-are-needed-to-view-these-reports), you can view these reports in the [Security & Compliance Center](https://protection.office.com) by going to **Reports** \> **Dashboard**.</span></span> <span data-ttu-id="db820-110">Pour aller directement au tableau de bord Rapports, ouvrez <https://protection.office.com/insightdashboard> .</span><span class="sxs-lookup"><span data-stu-id="db820-110">To go directly to the Reports dashboard, open <https://protection.office.com/insightdashboard>.</span></span>

![Tableau de bord Rapports dans le Centre de sécurité & conformité](../../media/6b213d34-adbb-44af-8549-be9a7e2db087.png)

## <a name="connector-report"></a><span data-ttu-id="db820-112">Rapport sur le connecteur</span><span class="sxs-lookup"><span data-stu-id="db820-112">Connector report</span></span>

<span data-ttu-id="db820-113">Le **rapport Connecteur indique** l’activité de flux de messagerie sur les connecteurs entrants et [sortants configurés](/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow) pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="db820-113">The **Connector report** shows mail flow activity on the [inbound and outbound connectors](/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow) that are configured for your organization.</span></span>

<span data-ttu-id="db820-114">Pour afficher le rapport, ouvrez le Centre  de sécurité [& conformité,](https://protection.office.com)allez au tableau de bord rapports \>  et sélectionnez le **rapport connecteur.**</span><span class="sxs-lookup"><span data-stu-id="db820-114">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Connector report**.</span></span> <span data-ttu-id="db820-115">Pour aller directement dans le rapport, ouvrez <https://protection.office.com/reportv2?id=ConnectorReport> .</span><span class="sxs-lookup"><span data-stu-id="db820-115">To go directly to the report, open <https://protection.office.com/reportv2?id=ConnectorReport>.</span></span>

![Widget de rapport connecteur dans le tableau de bord Rapports](../../media/connector-report-widget.png)

### <a name="report-view-for-the-connector-report"></a><span data-ttu-id="db820-117">Affichage du rapport pour le rapport connecteur</span><span class="sxs-lookup"><span data-stu-id="db820-117">Report view for the Connector report</span></span>

<span data-ttu-id="db820-118">Les graphiques suivants sont disponibles en affichage état :</span><span class="sxs-lookup"><span data-stu-id="db820-118">The following charts are available in report view:</span></span>

- <span data-ttu-id="db820-119">**Afficher les données par : Flux de messagerie**: ce graphique affiche le nombre de messages entrants et sortants organisés par :</span><span class="sxs-lookup"><span data-stu-id="db820-119">**View data by: Mail flow**: This chart shows the number of inbound and outbound messages organized by:</span></span>

  - <span data-ttu-id="db820-120">**Total**</span><span class="sxs-lookup"><span data-stu-id="db820-120">**Total**</span></span>
  - <span data-ttu-id="db820-121">**À partir d’Internet sans connecteur**</span><span class="sxs-lookup"><span data-stu-id="db820-121">**From the internet without a connector**</span></span>
  - <span data-ttu-id="db820-122">**Vers Internet sans connecteur**</span><span class="sxs-lookup"><span data-stu-id="db820-122">**To the internet without a connector**</span></span>
  - <span data-ttu-id="db820-123">Connecteur spécifique que vous avez configuré.</span><span class="sxs-lookup"><span data-stu-id="db820-123">A specific connector that you've configured.</span></span>

  <span data-ttu-id="db820-124">Pour isoler les données dans le graphique, utilisez l’option **Afficher** les données pour le contrôle afin de sélectionner l’une de ces options ou tout **flux de messagerie.**</span><span class="sxs-lookup"><span data-stu-id="db820-124">To isolate the data in the chart, use the **Show data for** control to select one of these options or **All mail flow**.</span></span>

  ![Afficher les données par flux de messagerie dans le rapport connecteur](../../media/connector-report-view-data-by-mail-flow.png)

- <span data-ttu-id="db820-126">**Afficher les données par : utilisation de TLS**: ce graphique affiche le pourcentage d’utilisation de la version TLS (Transport Layer Security) pour le flux de messagerie.</span><span class="sxs-lookup"><span data-stu-id="db820-126">**View data by: TLS usage**: This chart shows the percentage of Transport Layer Security (TLS) version usage for mail flow.</span></span>

  <span data-ttu-id="db820-127">Pour isoler les données dans le graphique, utilisez l’option **Afficher les** données pour le contrôle pour sélectionner l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="db820-127">To isolate the data in the chart, use the **Show data for** control to select one of the following options:</span></span>

  - <span data-ttu-id="db820-128">**Tout le flux de messagerie**</span><span class="sxs-lookup"><span data-stu-id="db820-128">**All mail flow**</span></span>
  - <span data-ttu-id="db820-129">**À partir d’Internet sans connecteur**</span><span class="sxs-lookup"><span data-stu-id="db820-129">**From the internet without a connector**</span></span>
  - <span data-ttu-id="db820-130">**Vers Internet sans connecteur**</span><span class="sxs-lookup"><span data-stu-id="db820-130">**To the internet without a connector**</span></span>
  - <span data-ttu-id="db820-131">Connecteur spécifique que vous avez configuré.</span><span class="sxs-lookup"><span data-stu-id="db820-131">A specific connector that you've configured.</span></span>

  ![Afficher les données par utilisation de TLS dans le rapport connecteur](../../media/connector-report-view-data-by-tls-usage.png)

<span data-ttu-id="db820-133">Si vous cliquez sur **Filtres** dans un affichage de rapport, vous pouvez spécifier une plage de dates avec la **date** de début et la **date de fin.**</span><span class="sxs-lookup"><span data-stu-id="db820-133">If you click **Filters** in a report view, you can specify a date range with **Start date** and **End date**.</span></span>

### <a name="details-table-view-for-the-connector-report"></a><span data-ttu-id="db820-134">Vue de table Détails pour le rapport Connecteur</span><span class="sxs-lookup"><span data-stu-id="db820-134">Details table view for the Connector report</span></span>

<span data-ttu-id="db820-135">Si vous cliquez **sur Afficher le tableau des détails** dans un affichage de rapport, les informations suivantes sont affichées :</span><span class="sxs-lookup"><span data-stu-id="db820-135">If you click **View details table** in a report view, the following information is shown:</span></span>

- <span data-ttu-id="db820-136">**Date**</span><span class="sxs-lookup"><span data-stu-id="db820-136">**Date**</span></span>
- <span data-ttu-id="db820-137">**Direction et nom du connecteur**</span><span class="sxs-lookup"><span data-stu-id="db820-137">**Connector direction and name**</span></span>
- <span data-ttu-id="db820-138">**Type de connecteur**</span><span class="sxs-lookup"><span data-stu-id="db820-138">**Connector type**</span></span>
- <span data-ttu-id="db820-139">**TLS forcé ?**: la valeur **True** ou **False**.</span><span class="sxs-lookup"><span data-stu-id="db820-139">**Forced TLS?**: The value **True** or **False**.</span></span>
- <span data-ttu-id="db820-140">**Pas de TLS** (pourcentage)</span><span class="sxs-lookup"><span data-stu-id="db820-140">**No TLS** (percentage)</span></span>
- <span data-ttu-id="db820-141">**TLS 1.0** (pourcentage)</span><span class="sxs-lookup"><span data-stu-id="db820-141">**TLS 1.0** (percentage)</span></span>
- <span data-ttu-id="db820-142">**TLS 1.1** (pourcentage)</span><span class="sxs-lookup"><span data-stu-id="db820-142">**TLS 1.1** (percentage)</span></span>
- <span data-ttu-id="db820-143">**TLS 1.2** (pourcentage)</span><span class="sxs-lookup"><span data-stu-id="db820-143">**TLS 1.2** (percentage)</span></span>
- <span data-ttu-id="db820-144">**Volume**: nombre de messages.</span><span class="sxs-lookup"><span data-stu-id="db820-144">**Volume**: The number of messages.</span></span>

<span data-ttu-id="db820-145">Si vous cliquez sur **Filtres** dans une vue de tableau de détails, vous pouvez spécifier une plage de dates avec la **date** de début et la **date de fin.**</span><span class="sxs-lookup"><span data-stu-id="db820-145">If you click **Filters** in a details table view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="db820-146">Pour revenir à l’affichage du rapport, cliquez **sur Afficher le rapport.**</span><span class="sxs-lookup"><span data-stu-id="db820-146">To go back to the report view, click **View report**.</span></span>

## <a name="exchange-transport-rule-report"></a><span data-ttu-id="db820-147">Rapport de règles de transport Exchange</span><span class="sxs-lookup"><span data-stu-id="db820-147">Exchange transport rule report</span></span>

<span data-ttu-id="db820-148">Le **rapport des règles** de transport Exchange indique l’effet des règles de flux de messagerie (également appelées règles de transport) sur les messages entrants et sortants dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="db820-148">The **Exchange transport rule report** shows the effect of mail flow rules (also known as transport rules) on incoming and outgoing messages in your organization.</span></span>

<span data-ttu-id="db820-149">Pour afficher le rapport, ouvrez le Centre  de sécurité [& conformité,](https://protection.office.com)puis sélectionnez Tableau de bord rapports \>  et **sélectionnez Règle de transport Exchange.**</span><span class="sxs-lookup"><span data-stu-id="db820-149">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Exchange Transport rule**.</span></span> <span data-ttu-id="db820-150">Pour aller directement dans le rapport, ouvrez <https://protection.office.com/reportv2?id=ETRRuleReport> .</span><span class="sxs-lookup"><span data-stu-id="db820-150">To go directly to the report, open <https://protection.office.com/reportv2?id=ETRRuleReport>.</span></span>

![Widget de règle de transport Exchange dans le tableau de bord Rapports](../../media/transport-rule-report-widget.png)

### <a name="report-view-for-the-exchange-transport-rule-report"></a><span data-ttu-id="db820-152">Affichage du rapport pour le rapport des règles de transport Exchange</span><span class="sxs-lookup"><span data-stu-id="db820-152">Report view for the Exchange transport rule report</span></span>

<span data-ttu-id="db820-153">Les graphiques suivants sont disponibles en affichage état :</span><span class="sxs-lookup"><span data-stu-id="db820-153">The following charts are available in report view:</span></span>

- <span data-ttu-id="db820-154">**Afficher les données par : règles de transport** \> Exchange **Décomposer par : Direction**: ce  graphique affiche le nombre de **messages** entrants et sortants affectés par les règles de transport.</span><span class="sxs-lookup"><span data-stu-id="db820-154">**View data by: Exchange transport rules** \> **Break down by: Direction**: This chart shows the number of **Inbound** and **Outbound** messages that were affected by transport rules.</span></span>

- <span data-ttu-id="db820-155">**Afficher les données par : règles de transport** \> Exchange **Décomposez par : Gravité :** ce  graphique affiche le nombre de messages de gravité élevée, moyenne et **faible.**</span><span class="sxs-lookup"><span data-stu-id="db820-155">**View data by: Exchange transport rules** \> **Break down by: Severity**: This chart shows the number of **High severity** and **Medium severity**, and **Low severity** messages.</span></span> <span data-ttu-id="db820-156">Vous définissez le niveau de gravité en tant qu’action dans la règle (**Auditez** cette règle avec le niveau de gravité _ou SetAuditSeverity_).</span><span class="sxs-lookup"><span data-stu-id="db820-156">You set the severity level as an action in the rule (**Audit this rule with severity level** or _SetAuditSeverity_).</span></span> <span data-ttu-id="db820-157">Pour plus d’informations, voir [Actions de règle de flux de messagerie dans Exchange Online.](//Exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions)</span><span class="sxs-lookup"><span data-stu-id="db820-157">For more information, see [Mail flow rule actions in Exchange Online](//Exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions).</span></span>

- <span data-ttu-id="db820-158">**Afficher les données par : règles de transport** \> Exchange DLP **Décomposer par : Direction**: ce  graphique affiche le nombre de **messages** entrants et sortants affectés par les règles de transport de protection contre la perte de données (DLP).</span><span class="sxs-lookup"><span data-stu-id="db820-158">**View data by: DLP Exchange transport rules** \> **Break down by: Direction**: This chart shows the number of **Inbound** and **Outbound** messages that were affected by data loss prevention (DLP) transport rules.</span></span> <span data-ttu-id="db820-159">Vous pouvez affiner davantage le graphique en sélectionnant l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="db820-159">You can further refine the chart by selecting on of the following options:</span></span>

  - <span data-ttu-id="db820-160">**Afficher les données pour : toutes les règles de transport DLP**</span><span class="sxs-lookup"><span data-stu-id="db820-160">**Show data for: All DLP transport rules**</span></span>
  - <span data-ttu-id="db820-161">**Afficher les données pour : utilisateurs compromis**</span><span class="sxs-lookup"><span data-stu-id="db820-161">**Show data for: Compromised users**</span></span>
  - <span data-ttu-id="db820-162">**Afficher les données pour : faible volume de contenu détecté pour le Patriot Act des États-Unis**</span><span class="sxs-lookup"><span data-stu-id="db820-162">**Show data for: Low volume of content detected U.S. Patriot Act**</span></span>

- <span data-ttu-id="db820-163">**Afficher les données par : règles de transport** \> Exchange DLP **Décomposez par : Direction**: cet  affichage indique le nombre de **messages** de gravité élevée et moyenne **et** faible qui ont été affectés par les règles de transport DLP.</span><span class="sxs-lookup"><span data-stu-id="db820-163">**View data by: DLP Exchange transport rules** \> **Break down by: Direction**: This view shows the number of **High severity** and **Medium severity**, and **Low severity** messages that were affected by DLP transport rules.</span></span> <span data-ttu-id="db820-164">Vous pouvez affiner davantage le graphique en sélectionnant l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="db820-164">You can further refine the chart by selecting on of the following options:</span></span>

  - <span data-ttu-id="db820-165">**Afficher les données pour : toutes les règles de transport DLP**</span><span class="sxs-lookup"><span data-stu-id="db820-165">**Show data for: All DLP transport rules**</span></span>
  - <span data-ttu-id="db820-166">**Afficher les données pour : utilisateurs compromis**</span><span class="sxs-lookup"><span data-stu-id="db820-166">**Show data for: Compromised users**</span></span>
  - <span data-ttu-id="db820-167">**Afficher les données pour : faible volume de contenu détecté pour le Patriot Act des États-Unis**</span><span class="sxs-lookup"><span data-stu-id="db820-167">**Show data for: Low volume of content detected U.S. Patriot Act**</span></span>

<span data-ttu-id="db820-168">Si vous cliquez **sur Filtres** dans un affichage de rapport, vous pouvez modifier les résultats avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="db820-168">If you click **Filters** in a report view, you can modify the results with the following filters::</span></span>

- <span data-ttu-id="db820-169">**Date de début** et **date de fin**</span><span class="sxs-lookup"><span data-stu-id="db820-169">**Start date** and **End date**</span></span>
- <span data-ttu-id="db820-170">Valeurs de direction</span><span class="sxs-lookup"><span data-stu-id="db820-170">Direction values</span></span>
- <span data-ttu-id="db820-171">Valeurs de gravité</span><span class="sxs-lookup"><span data-stu-id="db820-171">Severity values</span></span>

![Affichage du rapport dans le rapport des règles de transport Exchange](../../media/transport-rule-report-report-view.png)

### <a name="details-table-view-for-the-exchange-transport-rule-report"></a><span data-ttu-id="db820-173">Vue de table Détails pour le rapport de règles de transport Exchange</span><span class="sxs-lookup"><span data-stu-id="db820-173">Details table view for the Exchange transport rule report</span></span>

<span data-ttu-id="db820-174">Si vous cliquez sur Afficher le tableau des **détails,** les informations affichées dépendent du graphique que vous regardiez :</span><span class="sxs-lookup"><span data-stu-id="db820-174">If you click **View details table**, the information that's shown depends on the chart you were looking at:</span></span>

- <span data-ttu-id="db820-175">**Afficher les données par : Règles de transport Exchange**:</span><span class="sxs-lookup"><span data-stu-id="db820-175">**View data by: Exchange Transport rules**:</span></span>

  - <span data-ttu-id="db820-176">**Date**</span><span class="sxs-lookup"><span data-stu-id="db820-176">**Date**</span></span>
  - <span data-ttu-id="db820-177">**Règle de transport**</span><span class="sxs-lookup"><span data-stu-id="db820-177">**Transport rule**</span></span>
  - <span data-ttu-id="db820-178">**Subject**</span><span class="sxs-lookup"><span data-stu-id="db820-178">**Subject**</span></span>
  - <span data-ttu-id="db820-179">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="db820-179">**Sender address**</span></span>
  - <span data-ttu-id="db820-180">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="db820-180">**Recipient address**</span></span>
  - <span data-ttu-id="db820-181">**Gravité**</span><span class="sxs-lookup"><span data-stu-id="db820-181">**Severity**</span></span>
  - <span data-ttu-id="db820-182">**Direction**</span><span class="sxs-lookup"><span data-stu-id="db820-182">**Direction**</span></span>

- <span data-ttu-id="db820-183">**Afficher les données par : Règles de transport Exchange DLP**:</span><span class="sxs-lookup"><span data-stu-id="db820-183">**View data by: DLP Exchange transport rules**:</span></span>

  - <span data-ttu-id="db820-184">**Date**</span><span class="sxs-lookup"><span data-stu-id="db820-184">**Date**</span></span>
  - <span data-ttu-id="db820-185">**Stratégie DLP**</span><span class="sxs-lookup"><span data-stu-id="db820-185">**DLP policy**</span></span>
  - <span data-ttu-id="db820-186">**Règle de transport**</span><span class="sxs-lookup"><span data-stu-id="db820-186">**Transport rule**</span></span>
  - <span data-ttu-id="db820-187">**Subject**</span><span class="sxs-lookup"><span data-stu-id="db820-187">**Subject**</span></span>
  - <span data-ttu-id="db820-188">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="db820-188">**Sender address**</span></span>
  - <span data-ttu-id="db820-189">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="db820-189">**Recipient address**</span></span>
  - <span data-ttu-id="db820-190">**Gravité**</span><span class="sxs-lookup"><span data-stu-id="db820-190">**Severity**</span></span>
  - <span data-ttu-id="db820-191">**Direction**</span><span class="sxs-lookup"><span data-stu-id="db820-191">**Direction**</span></span>

<span data-ttu-id="db820-192">Si vous cliquez **sur Filtres** dans une vue de tableau de détails, vous pouvez modifier les résultats avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="db820-192">If you click **Filters** in a details table view, you can modify the results with the following filters:</span></span>

- <span data-ttu-id="db820-193">**Date de début** et **date de fin**</span><span class="sxs-lookup"><span data-stu-id="db820-193">**Start date** and **End date**</span></span>
- <span data-ttu-id="db820-194">Valeurs de direction</span><span class="sxs-lookup"><span data-stu-id="db820-194">Direction values</span></span>
- <span data-ttu-id="db820-195">Valeurs de gravité</span><span class="sxs-lookup"><span data-stu-id="db820-195">Severity values</span></span>

<span data-ttu-id="db820-196">Pour revenir à l’affichage du rapport, cliquez **sur Afficher le rapport.**</span><span class="sxs-lookup"><span data-stu-id="db820-196">To go back to the report view, click **View report**.</span></span>

## <a name="forwarding-report"></a><span data-ttu-id="db820-197">Rapport de forwarding</span><span class="sxs-lookup"><span data-stu-id="db820-197">Forwarding report</span></span>

<span data-ttu-id="db820-198">Le **rapport de forwarding** affiche les messages automatiquement transmis par votre organisation à des domaines externes à partir de boîtes aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="db820-198">The **Forwarding report** shows your organization's automatically forwarded messages to external domains from Exchange Online mailboxes.</span></span> <span data-ttu-id="db820-199">Les messages transmis peuvent présenter un risque de sécurité ou de conformité, et peuvent indiquer un compte compromis.</span><span class="sxs-lookup"><span data-stu-id="db820-199">Forwarded messages can pose a security or compliance risk, and might indicate a compromised account.</span></span>

<span data-ttu-id="db820-200">Pour afficher le rapport, ouvrez le Centre de  sécurité [& conformité,](https://protection.office.com)allez au Tableau de bord des rapports \>  et sélectionnez Rapport **de report.**</span><span class="sxs-lookup"><span data-stu-id="db820-200">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Forwarding report**.</span></span> <span data-ttu-id="db820-201">Pour aller directement dans le rapport, ouvrez <https://protection.office.com/reportv2?id=MailFlowForwarding> .</span><span class="sxs-lookup"><span data-stu-id="db820-201">To go directly to the report, open <https://protection.office.com/reportv2?id=MailFlowForwarding>.</span></span>

![Widget de rapport de forwarding dans le tableau de bord Rapports](../../media/forwarding-report-widget.png)

### <a name="report-view-for-the-forwarding-report"></a><span data-ttu-id="db820-203">Affichage du rapport pour le rapport de report</span><span class="sxs-lookup"><span data-stu-id="db820-203">Report view for the Forwarding report</span></span>

<span data-ttu-id="db820-204">Les graphiques suivants sont disponibles dans l’affichage de rapport :</span><span class="sxs-lookup"><span data-stu-id="db820-204">The following charts are available in the report view:</span></span>

- <span data-ttu-id="db820-205">**Afficher les données pour : Méthodes de forwarding**: les méthodes suivantes sont affichées :</span><span class="sxs-lookup"><span data-stu-id="db820-205">**Show data for: Forwarding methods**: The following methods are shown:</span></span>

  - <span data-ttu-id="db820-206">**Règle de transport**: également appelée règles [de flux de messagerie.](/Exchange/security-and-compliance/mail-flow-rules/mail-flow-rules)</span><span class="sxs-lookup"><span data-stu-id="db820-206">**Transport rule**: Also known as [mail flow rules](/Exchange/security-and-compliance/mail-flow-rules/mail-flow-rules).</span></span>
  - <span data-ttu-id="db820-207">**Règle de boîte** aux lettres : également appelée [règles de boîte de réception.](https://support.microsoft.com/office/c24f5dea-9465-4df4-ad17-a50704d66c59)</span><span class="sxs-lookup"><span data-stu-id="db820-207">**Mailbox rule**: Also known as [Inbox rules](https://support.microsoft.com/office/c24f5dea-9465-4df4-ad17-a50704d66c59).</span></span>

  ![Affichage des méthodes de forwarding dans le rapport de forwarding](../../media/forwarding-report-forwarding-methods.png)

- <span data-ttu-id="db820-209">**Afficher les données pour : Domaines de forwarding**: cet affichage affiche les domaines destinataires qui sont les destinations pour le forwarding.</span><span class="sxs-lookup"><span data-stu-id="db820-209">**Show data for: Forwarding domains**: This view shows the recipient domains that are the destinations for forwarding.</span></span>

  ![Affichage des domaines de forwarding dans le rapport de forwarding](../../media/forwarding-report-forwarding-domains.png)

- <span data-ttu-id="db820-211">**Afficher les données pour : Forwarders**: les forwardeurs suivants sont affichés :</span><span class="sxs-lookup"><span data-stu-id="db820-211">**Show data for: Forwarders**: The following forwarders are shown:</span></span>

  - <span data-ttu-id="db820-212">**Règle de transport**</span><span class="sxs-lookup"><span data-stu-id="db820-212">**Transport rule**</span></span>
  - <span data-ttu-id="db820-213">Boîte aux lettres contenant la règle de boîte de réception de forwarding.</span><span class="sxs-lookup"><span data-stu-id="db820-213">The mailbox that contains the forwarding Inbox rule.</span></span>

  ![Affichage des forwardeurs dans le rapport de forwarding](../../media/forwarding-report-forwarders.png)

<span data-ttu-id="db820-215">Si vous cliquez sur **Filtres** dans un affichage de rapport, vous pouvez spécifier une plage de dates avec la **date** de début et la **date de fin.**</span><span class="sxs-lookup"><span data-stu-id="db820-215">If you click **Filters** in a report view, you can specify a date range with **Start date** and **End date**.</span></span>

### <a name="details-table-view-for-the-forwarding-report"></a><span data-ttu-id="db820-216">Vue de table Détails pour le rapport de report</span><span class="sxs-lookup"><span data-stu-id="db820-216">Details table view for the Forwarding report</span></span>

<span data-ttu-id="db820-217">Si vous cliquez **sur Afficher le tableau des détails** dans un affichage de rapport, les informations suivantes sont affichées :</span><span class="sxs-lookup"><span data-stu-id="db820-217">If you click **View details table** in a report view, the following information is shown:</span></span>

- <span data-ttu-id="db820-218">**Forwarders :** règle de **transport de valeur** ou boîte aux lettres qui contient la règle de boîte de réception de transport.</span><span class="sxs-lookup"><span data-stu-id="db820-218">**Forwarders**: The value **Transport rule** or the mailbox that contains the forwarding Inbox rule.</span></span>
- <span data-ttu-id="db820-219">**Type de transport :** la règle de boîte **aux lettres de valeur** ou la règle **de transport**.</span><span class="sxs-lookup"><span data-stu-id="db820-219">**Forwarding type**: The value **Mailbox rule** or **Transport rule**.</span></span>
- <span data-ttu-id="db820-220">**Nom du destinataire**</span><span class="sxs-lookup"><span data-stu-id="db820-220">**Recipient name**</span></span>
- <span data-ttu-id="db820-221">**Domaine du destinataire**</span><span class="sxs-lookup"><span data-stu-id="db820-221">**Recipient domain**</span></span>
- <span data-ttu-id="db820-222">**Détails**: il s’agit de la valeur GUID de la règle de flux de messagerie ou de la valeur RuleIdentity de la règle de boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="db820-222">**Details**: This is the GUID value of the mail flow rule, or the RuleIdentity value of the Inbox rule.</span></span>
- <span data-ttu-id="db820-223">**Count**</span><span class="sxs-lookup"><span data-stu-id="db820-223">**Count**</span></span>
- <span data-ttu-id="db820-224">**Première date d’avance**</span><span class="sxs-lookup"><span data-stu-id="db820-224">**First forward date**</span></span>

<span data-ttu-id="db820-225">Si vous cliquez sur **Filtres** dans une vue de table de détails, vous pouvez spécifier une plage de dates avec la **date** de début et la **date de fin**.</span><span class="sxs-lookup"><span data-stu-id="db820-225">If you click **Filters** in a details table view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="db820-226">Pour revenir à l’affichage Rapports, cliquez **sur Afficher le rapport.**</span><span class="sxs-lookup"><span data-stu-id="db820-226">To go back to the reports view, click **View report**.</span></span>

## <a name="mailflow-status-report"></a><span data-ttu-id="db820-227">Rapport d’état du flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="db820-227">Mailflow status report</span></span>

<span data-ttu-id="db820-228">Le **rapport d’état du** flux de messagerie est similaire au rapport de courrier électronique envoyé et reçu, avec des informations supplémentaires sur le courrier électronique autorisé ou bloqué sur le edge. [](#sent-and-received-email-report)</span><span class="sxs-lookup"><span data-stu-id="db820-228">The **Mailflow status report** is similar to the [Sent and received email report](#sent-and-received-email-report), with additional information about email allowed or blocked on the edge.</span></span> <span data-ttu-id="db820-229">Il s’agit du seul rapport qui contient des informations sur la protection edge et qui indique la quantité de courrier électronique bloquée avant d’être autorisé dans le service pour évaluation par Exchange Online Protection (EOP).</span><span class="sxs-lookup"><span data-stu-id="db820-229">This is the only report that contains edge protection information, and shows just how much email is blocked before being allowed into the service for evaluation by Exchange Online Protection (EOP).</span></span> <span data-ttu-id="db820-230">Il est important de comprendre que si un message est envoyé à cinq destinataires, nous le compterons comme cinq messages différents et pas un seul message.</span><span class="sxs-lookup"><span data-stu-id="db820-230">It's important to understand that if a message is sent to five recipients we count it as five different messages and not one message.</span></span>
<span data-ttu-id="db820-231">Pour afficher le rapport, ouvrez le Centre de  sécurité [& conformité,](https://protection.office.com)puis sélectionnez Tableau de bord rapports et sélectionnez Rapport d’état du \>  flux **de messagerie.**</span><span class="sxs-lookup"><span data-stu-id="db820-231">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Mailflow status report**.</span></span> <span data-ttu-id="db820-232">Pour aller directement au rapport d’état du **flux de messagerie,** ouvrez <https://protection.office.com/mailflowStatusReport> .</span><span class="sxs-lookup"><span data-stu-id="db820-232">To go directly to the **Mail flow status report**, open <https://protection.office.com/mailflowStatusReport>.</span></span>

![Widget de rapport d’état du flux de messagerie dans le tableau de bord Rapports](../../media/mail-flow-status-report-widget.png)

### <a name="type-view-for-the-mailflow-status-report"></a><span data-ttu-id="db820-234">Affichage des types pour le rapport d’état du flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="db820-234">Type view for the Mailflow status report</span></span>

<span data-ttu-id="db820-235">Lorsque vous ouvrez l’état, **l’onglet Type** est sélectionné par défaut.</span><span class="sxs-lookup"><span data-stu-id="db820-235">When you open the report, the **Type** tab is selected by default.</span></span> <span data-ttu-id="db820-236">Par défaut, cet affichage contient un graphique et une table de données configurés avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="db820-236">By default, this view contains a chart and a data table that's configured with the following filters:</span></span>

- <span data-ttu-id="db820-237">**Date**: 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="db820-237">**Date**: The last 7 days.</span></span>
- <span data-ttu-id="db820-238">**Direction**:</span><span class="sxs-lookup"><span data-stu-id="db820-238">**Direction**:</span></span>

  - <span data-ttu-id="db820-239">**Entrant**</span><span class="sxs-lookup"><span data-stu-id="db820-239">**Inbound**</span></span>
  - <span data-ttu-id="db820-240">**Sortant**</span><span class="sxs-lookup"><span data-stu-id="db820-240">**Outbound**</span></span>
  - <span data-ttu-id="db820-241">**Intra-organisation**: ce nombre est pour les messages au sein d’un client, c’est-à-dire</span><span class="sxs-lookup"><span data-stu-id="db820-241">**Intra-org**: this count is for messages within a tenant i.e</span></span> <span data-ttu-id="db820-242">sender abc@domain.com sends to recipient xyz@domain.com (counted separately from **Inbound** and **Outbound**)</span><span class="sxs-lookup"><span data-stu-id="db820-242">sender abc@domain.com sends to recipient xyz@domain.com  (counted separately from **Inbound** and **Outbound**)</span></span>

- <span data-ttu-id="db820-243">**Tapez**:</span><span class="sxs-lookup"><span data-stu-id="db820-243">**Type**:</span></span>

  - <span data-ttu-id="db820-244">**Courrier électronique de qualité**</span><span class="sxs-lookup"><span data-stu-id="db820-244">**Good mail**</span></span>
  - <span data-ttu-id="db820-245">**Programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="db820-245">**Malware**</span></span>
  - <span data-ttu-id="db820-246">**Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="db820-246">**Spam**</span></span>
  - <span data-ttu-id="db820-247">**Protection Edge**</span><span class="sxs-lookup"><span data-stu-id="db820-247">**Edge protection**</span></span>
  - <span data-ttu-id="db820-248">**Messages de règle**</span><span class="sxs-lookup"><span data-stu-id="db820-248">**Rule messages**</span></span>
  - <span data-ttu-id="db820-249">**Courriers hameçons**</span><span class="sxs-lookup"><span data-stu-id="db820-249">**Phishing email**</span></span>

<span data-ttu-id="db820-250">Le graphique est organisé par les valeurs **Type.**</span><span class="sxs-lookup"><span data-stu-id="db820-250">The chart is organized by the **Type** values.</span></span>

<span data-ttu-id="db820-251">Vous pouvez modifier ces filtres en cliquant sur **Filtre** ou en cliquant sur une valeur dans la légende du graphique.</span><span class="sxs-lookup"><span data-stu-id="db820-251">You can change these filters by clicking **Filter** or by clicking a value in the chart legend.</span></span>

<span data-ttu-id="db820-252">La table de données contient les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="db820-252">The data table contains the following information:</span></span>

- <span data-ttu-id="db820-253">**Direction**</span><span class="sxs-lookup"><span data-stu-id="db820-253">**Direction**</span></span>
- <span data-ttu-id="db820-254">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="db820-254">**Type**</span></span>
- <span data-ttu-id="db820-255">**24 heures**</span><span class="sxs-lookup"><span data-stu-id="db820-255">**24 hours**</span></span>
- <span data-ttu-id="db820-256">**3 jours**</span><span class="sxs-lookup"><span data-stu-id="db820-256">**3 days**</span></span>
- <span data-ttu-id="db820-257">**7 jours**</span><span class="sxs-lookup"><span data-stu-id="db820-257">**7 days**</span></span>
- <span data-ttu-id="db820-258">**15 jours**</span><span class="sxs-lookup"><span data-stu-id="db820-258">**15 days**</span></span>
- <span data-ttu-id="db820-259">**30 jours**</span><span class="sxs-lookup"><span data-stu-id="db820-259">**30 days**</span></span>

<span data-ttu-id="db820-260">Si vous cliquez **sur Choisir une catégorie pour plus de détails,** vous pouvez choisir parmi les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="db820-260">If you click **Choose a category for more details**, you can select from the following values:</span></span>

- <span data-ttu-id="db820-261">**E-mail de hameçonnage**: cette sélection vous place dans le rapport d’état [de la protection contre les menaces.](view-email-security-reports.md#threat-protection-status-report)</span><span class="sxs-lookup"><span data-stu-id="db820-261">**Phishing email**: This selection takes you to the [Threat protection status report](view-email-security-reports.md#threat-protection-status-report).</span></span>
- <span data-ttu-id="db820-262">**Programmes malveillants dans les e-mails**: cette sélection vous place dans le rapport d’état [de la protection contre les menaces.](view-email-security-reports.md#threat-protection-status-report)</span><span class="sxs-lookup"><span data-stu-id="db820-262">**Malware in email**: This selection takes you to the [Threat protection status report](view-email-security-reports.md#threat-protection-status-report).</span></span>
- <span data-ttu-id="db820-263">**Détections de courrier indésirable**: cette sélection vous permet d’envoyer le rapport [détections de courrier indésirable.](view-email-security-reports.md#spam-detections-report)</span><span class="sxs-lookup"><span data-stu-id="db820-263">**Spam detections**: This selection takes you to the [Spam Detections report](view-email-security-reports.md#spam-detections-report).</span></span>
- <span data-ttu-id="db820-264">**Courrier indésirable bloqué edge**: cette sélection vous permet d’envoyer le rapport [détections de courrier indésirable.](view-email-security-reports.md#spam-detections-report)</span><span class="sxs-lookup"><span data-stu-id="db820-264">**Edge blocked spam**: This selection takes you to the [Spam Detections report](view-email-security-reports.md#spam-detections-report).</span></span>

<span data-ttu-id="db820-265">**Exporter**:</span><span class="sxs-lookup"><span data-stu-id="db820-265">**Export**:</span></span>

<span data-ttu-id="db820-266">Pour l’affichage détaillé, vous ne pouvez exporter les données que pour une journée.</span><span class="sxs-lookup"><span data-stu-id="db820-266">For the detail view, you can only export data for one day.</span></span> <span data-ttu-id="db820-267">Par exemple, si vous souhaitez exporter des données pendant 7 jours, vous devez faire 7 actions d’exportation différentes.</span><span class="sxs-lookup"><span data-stu-id="db820-267">So, if you want to export data for 7 days, you need to do 7 different export actions.</span></span>

<span data-ttu-id="db820-268">Chaque fichier .csv exporté est limité à 150 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="db820-268">Each exported .csv file is limited to 150,000 rows.</span></span> <span data-ttu-id="db820-269">Si les données de ce jour contiennent plus de 150 000 lignes, plusieurs fichiers .csv seront créés.</span><span class="sxs-lookup"><span data-stu-id="db820-269">If the data for that day contains more than 150,000 rows, then multiple .csv files will be created.</span></span>

![<span data-ttu-id="db820-270">Affichage des types dans le rapport d’état du flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="db820-270">Type view in the Mailflow status report</span></span> ](../../media/mail-flow-status-report-type-view.png)

### <a name="direction-view-for-the-mailflow-status-report"></a><span data-ttu-id="db820-271">Affichage direction pour le rapport d’état du flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="db820-271">Direction view for the Mailflow status report</span></span>

<span data-ttu-id="db820-272">Si vous cliquez sur **l’onglet Direction,** les mêmes filtres par défaut de **l’affichage Type** sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="db820-272">If you click the **Direction** tab, the same default filters from the **Type** view are used.</span></span>

<span data-ttu-id="db820-273">Le graphique est organisé par **valeurs de direction.**</span><span class="sxs-lookup"><span data-stu-id="db820-273">The chart is organized by **Direction** values.</span></span>

<span data-ttu-id="db820-274">Vous pouvez modifier ces filtres en cliquant sur **Filtre** ou en cliquant sur une valeur dans la légende du graphique.</span><span class="sxs-lookup"><span data-stu-id="db820-274">You can change these filters by clicking **Filter** or by clicking a value in the chart legend.</span></span> <span data-ttu-id="db820-275">Les mêmes filtres de **l’affichage Type** sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="db820-275">The same filters from the **Type** view are used.</span></span>

<span data-ttu-id="db820-276">La table de données contient les mêmes informations que **l’affichage Type.**</span><span class="sxs-lookup"><span data-stu-id="db820-276">The data table contains same information from the **Type** view.</span></span>

<span data-ttu-id="db820-277">La **sélection d’une catégorie pour obtenir plus d’informations** sur les sélections disponibles et le comportement sont identiques à l’affichage **Type.**</span><span class="sxs-lookup"><span data-stu-id="db820-277">The **Choose a category for more details** available selections and behavior are the same as the **Type** view.</span></span>

<span data-ttu-id="db820-278">**Exporter**:</span><span class="sxs-lookup"><span data-stu-id="db820-278">**Export**:</span></span>

<span data-ttu-id="db820-279">Pour l’affichage détaillé, vous ne pouvez exporter les données que pour une journée.</span><span class="sxs-lookup"><span data-stu-id="db820-279">For the detail view, you can only export data for one day.</span></span> <span data-ttu-id="db820-280">Par exemple, si vous souhaitez exporter des données pendant 7 jours, vous devez faire 7 actions d’exportation différentes.</span><span class="sxs-lookup"><span data-stu-id="db820-280">So, if you want to export data for 7 days, you need to do 7 different export actions.</span></span>

<span data-ttu-id="db820-281">Chaque fichier .csv exporté est limité à 150 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="db820-281">Each exported .csv file is limited to 150,000 rows.</span></span> <span data-ttu-id="db820-282">Si les données de ce jour contiennent plus de 150 000 lignes, plusieurs fichiers .csv seront créés.</span><span class="sxs-lookup"><span data-stu-id="db820-282">If the data for that day contains more than 150,000 rows, then multiple .csv files will be created.</span></span>

![<span data-ttu-id="db820-283">Affichage direction dans le rapport d’état du flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="db820-283">Direction view in the Mailflow status report</span></span> ](../../media/mail-flow-status-report-direction-view.png)

### <a name="funnel-view-for-the-mailflow-status-report"></a><span data-ttu-id="db820-284">Affichage en entonnoir pour le rapport d’état du flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="db820-284">Funnel view for the Mailflow status report</span></span>

<span data-ttu-id="db820-285">La **vue Entonnoir** vous montre comment les fonctionnalités de protection contre les menaces de courrier électronique de Microsoft filtrent le courrier électronique entrant et sortant dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="db820-285">The **Funnel** view shows you how Microsoft's email threat protection features filter incoming and outgoing email in your organization.</span></span> <span data-ttu-id="db820-286">Il fournit des détails sur le nombre total de messages électroniques et sur la façon dont les fonctionnalités de protection contre les menaces configurées, y compris la protection edge, les logiciels anti-programme malveillant, l’anti-hameçonnage, le courrier indésirable et la détection d’usurpation d’accès affectent ce nombre.</span><span class="sxs-lookup"><span data-stu-id="db820-286">It provides details on the total email count, and how the configured threat protection features, including edge protection, anti-malware, anti-phishing, anti-spam, and anti-spoofing affect this count.</span></span>

<span data-ttu-id="db820-287">Si vous  cliquez sur l’onglet Entonnoir, par défaut, cet affichage contient un graphique et une table de données configurés avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="db820-287">If you click the **Funnel** tab, by default, this view contains a chart and a data table that's configured with the following filters:</span></span>

- <span data-ttu-id="db820-288">**Date**: 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="db820-288">**Date**: The last 7 days.</span></span>

- <span data-ttu-id="db820-289">**Direction**:</span><span class="sxs-lookup"><span data-stu-id="db820-289">**Direction**:</span></span>

  - <span data-ttu-id="db820-290">**Entrant**</span><span class="sxs-lookup"><span data-stu-id="db820-290">**Inbound**</span></span>
  - <span data-ttu-id="db820-291">**Sortant**</span><span class="sxs-lookup"><span data-stu-id="db820-291">**Outbound**</span></span>
  - <span data-ttu-id="db820-292">**Intra-organisation**: ce nombre est le nombre de messages envoyés au sein d’un client ; Autrement dit, l’expéditeur abc@domain.com envoyé au destinataire xyz@domain.com (comptabilisé séparément des messages entrants et sortants).</span><span class="sxs-lookup"><span data-stu-id="db820-292">**Intra-org**: This count is for messages sent within a tenant; i.e, sender abc@domain.com sends to recipient xyz@domain.com (counted separately from Inbound and Outbound).</span></span>

<span data-ttu-id="db820-293">L’affichage agrégé et l’affichage table de données autorisent 90 jours de filtrage.</span><span class="sxs-lookup"><span data-stu-id="db820-293">The aggregate view and data table view allow for 90 days of filtering.</span></span>

<span data-ttu-id="db820-294">Si vous cliquez **sur Filtre,** vous pouvez filtrer le graphique et la table de données.</span><span class="sxs-lookup"><span data-stu-id="db820-294">If you click **Filter**, you can filter both the chart and the data table.</span></span>

<span data-ttu-id="db820-295">Ce graphique indique le nombre de messages électroniques organisés par :</span><span class="sxs-lookup"><span data-stu-id="db820-295">This chart shows the email count organized by:</span></span>

- <span data-ttu-id="db820-296">**Nombre total de messages électroniques**</span><span class="sxs-lookup"><span data-stu-id="db820-296">**Total email**</span></span>
- <span data-ttu-id="db820-297">**E-mail après protection edge**</span><span class="sxs-lookup"><span data-stu-id="db820-297">**Email after edge protection**</span></span>
- <span data-ttu-id="db820-298">**Courrier électronique après anti-programme malveillant, réputation de fichier, bloc de type de fichier**</span><span class="sxs-lookup"><span data-stu-id="db820-298">**Email after anti-malware, file reputation, file type block**</span></span>
- <span data-ttu-id="db820-299">**Courrier électronique après anti-hameçonnage, réputation d’URL, emprunt d’identité de marque, anti-usurpation**</span><span class="sxs-lookup"><span data-stu-id="db820-299">**Email after anti-phish, URL reputation, brand impersonation, anti-spoof**</span></span>
- <span data-ttu-id="db820-300">**Courrier électronique après filtrage du courrier indésirable en bloc**</span><span class="sxs-lookup"><span data-stu-id="db820-300">**Email after anti-spam, bulk mail filtering**</span></span>
- <span data-ttu-id="db820-301">**Courrier électronique après l’emprunt d’identité d’utilisateur et** de <sup>domaine 1</sup></span><span class="sxs-lookup"><span data-stu-id="db820-301">**Email after user and domain impersonation**<sup>1</sup></span></span>
- <span data-ttu-id="db820-302">**Email after file and URL detonation**<sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="db820-302">**Email after file and URL detonation**<sup>1</sup></span></span>
- <span data-ttu-id="db820-303">**Courrier électronique détecté comme étant anodin après la remise (protection de temps de clic d’URL)**</span><span class="sxs-lookup"><span data-stu-id="db820-303">**Email detected as benign after post-delivery protection (URL click time protection)**</span></span>

<span data-ttu-id="db820-304"><sup>1</sup> Defender pour Office 365 uniquement</span><span class="sxs-lookup"><span data-stu-id="db820-304"><sup>1</sup> Defender for Office 365 only</span></span>

<span data-ttu-id="db820-305">Pour afficher séparément les messages électroniques filtrés par EOP ou Defender pour Office 365, cliquez sur la valeur dans la légende du graphique.</span><span class="sxs-lookup"><span data-stu-id="db820-305">To view the email filtered by EOP or Defender for Office 365 separately, click on the value in the chart legend.</span></span>

<span data-ttu-id="db820-306">La table de données contient les informations suivantes, indiquées dans l’ordre décroit de date :</span><span class="sxs-lookup"><span data-stu-id="db820-306">The data table contains the following information, shown in descending date order:</span></span>

- <span data-ttu-id="db820-307">**Date**</span><span class="sxs-lookup"><span data-stu-id="db820-307">**Date**</span></span>
- <span data-ttu-id="db820-308">**Nombre total de messages électroniques**</span><span class="sxs-lookup"><span data-stu-id="db820-308">**Total email**</span></span>
- <span data-ttu-id="db820-309">**Protection Edge**</span><span class="sxs-lookup"><span data-stu-id="db820-309">**Edge protection**</span></span>
- <span data-ttu-id="db820-310">**Anti-programme malveillant, réputation de fichier, bloc de type de fichier**:</span><span class="sxs-lookup"><span data-stu-id="db820-310">**Anti-malware, file reputation, file type block**:</span></span>
  - <span data-ttu-id="db820-311">**Réputation du** fichier : messages filtrés en raison de l’identification d’un fichier joint par d’autres clients Microsoft.</span><span class="sxs-lookup"><span data-stu-id="db820-311">**File reputation**: Messages filtered due to identification of an attached file by other Microsoft customers.</span></span>
  - <span data-ttu-id="db820-312">**Bloc de type de** fichier : messages filtrés en raison du type de fichier malveillant identifié dans le message.</span><span class="sxs-lookup"><span data-stu-id="db820-312">**File type block**: Messages filtered due to the type of malicious file identified in the message.</span></span>
- <span data-ttu-id="db820-313">**Anti-hameçonnage, réputation de l’URL, emprunt d’identité de marque, anti-usurpation d’identité**:</span><span class="sxs-lookup"><span data-stu-id="db820-313">**Anti-phish, URL reputation, Brand impersonation, anti-spoof**:</span></span>
  - <span data-ttu-id="db820-314">**Réputation de l’URL**: messages filtrés en raison de l’identification de l’URL par d’autres clients Microsoft.</span><span class="sxs-lookup"><span data-stu-id="db820-314">**URL reputation**: Messages filtered due to the identification of the URL by other Microsoft customers.</span></span>
  - <span data-ttu-id="db820-315">**Emprunt d’identité de marque**: messages filtrés en raison du message provenant de la marque connue usurpant l’identité des expéditeurs.</span><span class="sxs-lookup"><span data-stu-id="db820-315">**Brand impersonation**: Messages filtered due to the message coming from well-known brand impersonating senders.</span></span>
  - <span data-ttu-id="db820-316">**Anti-usurpation**: messages filtrés en raison de la tentative d’usurpation d’un domaine appartenant au destinataire ou d’un domaine que l’expéditeur du message ne possède pas.</span><span class="sxs-lookup"><span data-stu-id="db820-316">**Anti-spoof**: Messages filtered due to the message attempting to spoof a domain that the recipient belongs to, or a domain that the message sender doesn't own.</span></span>
- <span data-ttu-id="db820-317">**Anti-courrier indésirable, filtrage du courrier en bloc**:</span><span class="sxs-lookup"><span data-stu-id="db820-317">**Anti-spam, bulk mail filtering**:</span></span>
  - <span data-ttu-id="db820-318">**Filtrage du courrier en nombre**: messages filtrés en raison d’une tentative de remettre des messages en nombre à ses destinataires.</span><span class="sxs-lookup"><span data-stu-id="db820-318">**Bulk mail filtering**: Messages filtered due to an attempt to deliver bulk mail to its recipients.</span></span>
- <span data-ttu-id="db820-319">**Emprunt d’identité d’utilisateur et de domaine (Defender pour Office 365)**:</span><span class="sxs-lookup"><span data-stu-id="db820-319">**User and domain impersonation (Defender for Office 365)**:</span></span>
  - <span data-ttu-id="db820-320">**Emprunt d’identité** d’utilisateur : messages filtrés en raison d’une tentative d’emprunt d’identité d’un utilisateur (expéditeur de message) défini dans les paramètres de protection contre l’emprunt d’identité d’une stratégie anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="db820-320">**User impersonation**: Messages filtered due to an attempt to impersonate a user (message sender) that's defined in the impersonation protection settings of an anti-phishing policy.</span></span>
  - <span data-ttu-id="db820-321">**Emprunt d’identité** de domaine : messages filtrés en raison d’une tentative d’emprunt d’identité d’un domaine défini dans les paramètres de protection contre l’emprunt d’identité d’une stratégie anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="db820-321">**Domain impersonation**: Messages filtered due to an attempt to impersonate a domain that's defined in the impersonation protection settings of an anti-phishing policy.</span></span>
- <span data-ttu-id="db820-322">**Détonation de fichiers et d’URL (Defender pour Office 365)**:</span><span class="sxs-lookup"><span data-stu-id="db820-322">**File and URL detonation (Defender for Office 365)**:</span></span>
  - <span data-ttu-id="db820-323">**Détonation de fichier**: messages filtrés par une stratégie de pièces jointes sécurisées.</span><span class="sxs-lookup"><span data-stu-id="db820-323">**File detonation**: Messages filtered by a Safe Attachments policy.</span></span>
  - <span data-ttu-id="db820-324">**Détonation d’URL**: message filtré par une stratégie de liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="db820-324">**URL detonation**: Message filtered by a Safe Links policy.</span></span>
- <span data-ttu-id="db820-325">**Protection post-remise et ZAP (ATP) ou ZAP (EOP)**: ZAP indique une purge automatique de zéro heure.</span><span class="sxs-lookup"><span data-stu-id="db820-325">**Post-delivery protection and ZAP (ATP), or ZAP (EOP)**: ZAP indicates zero hour auto-purge.</span></span>

<span data-ttu-id="db820-326">Si vous sélectionnez une ligne dans la table de données, une répartition supplémentaire du nombre de messages électroniques est affichée dans le volant.</span><span class="sxs-lookup"><span data-stu-id="db820-326">If you select a row in the data table, a further breakdown of the email counts are shown in the flyout.</span></span>

<span data-ttu-id="db820-327">**Exporter**:</span><span class="sxs-lookup"><span data-stu-id="db820-327">**Export**:</span></span>

<span data-ttu-id="db820-328">Après avoir cliqué **sur Exporter** sous **Options,** vous pouvez sélectionner l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="db820-328">After you click **Export** under **Options**, you can select one of the following values:</span></span>

- <span data-ttu-id="db820-329">**Résumé (avec des données pour les 90 derniers jours au maximum)**</span><span class="sxs-lookup"><span data-stu-id="db820-329">**Summary (with data for last 90 days at most)**</span></span>
- <span data-ttu-id="db820-330">**Détails (avec des données pour les 30 derniers jours au maximum)**</span><span class="sxs-lookup"><span data-stu-id="db820-330">**Details (with data for last 30 days at most)**</span></span>

<span data-ttu-id="db820-331">Sous **Date**, choisissez une plage, puis cliquez sur **Appliquer**.</span><span class="sxs-lookup"><span data-stu-id="db820-331">Under **Date**, choose a range, and then click **Apply**.</span></span> <span data-ttu-id="db820-332">Les données des filtres actuels sont exportées vers un fichier .csv.</span><span class="sxs-lookup"><span data-stu-id="db820-332">Data for the current filters will be exported to a .csv file.</span></span>

<span data-ttu-id="db820-333">Chaque fichier .csv exporté est limité à 150 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="db820-333">Each exported .csv file is limited to 150,000 rows.</span></span> <span data-ttu-id="db820-334">Si les données contiennent plus de 150 000 lignes, plusieurs fichiers .csv seront créés.</span><span class="sxs-lookup"><span data-stu-id="db820-334">If the data contains more than 150,000 rows, then multiple .csv files will be created.</span></span>

 ![<span data-ttu-id="db820-335">Affichage en entonnoir dans le rapport d’état du flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="db820-335">Funnel view in the Mailflow status report</span></span> ](../../media/mail-flow-status-report-funnel-view.png)

### <a name="tech-view-for-the-mailflow-status-report"></a><span data-ttu-id="db820-336">Affichage technique pour le rapport d’état du flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="db820-336">Tech view for the Mailflow status report</span></span>

<span data-ttu-id="db820-337">La **vue Tech est** similaire à la vue Entonnoir, fournissant des détails plus détaillés pour les fonctionnalités de protection contre les menaces configurées. </span><span class="sxs-lookup"><span data-stu-id="db820-337">The **Tech view** is similar to the **Funnel** view, providing more granular details for the configured threat protections features.</span></span> <span data-ttu-id="db820-338">À partir du graphique, vous pouvez voir comment les messages sont classés aux différentes étapes de la protection contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="db820-338">From the chart, you can see how messages are categorized at the different stages of threat protection.</span></span>

<span data-ttu-id="db820-339">Si vous cliquez sur **l’onglet Affichage** Technique, par défaut, cet affichage contient un graphique et une table de données configurés avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="db820-339">If you click the **Tech view** tab, by default, this view contains a chart and a data table that's configured with the following filters:</span></span>

- <span data-ttu-id="db820-340">**Date**: 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="db820-340">**Date**: The last 7 days.</span></span>

- <span data-ttu-id="db820-341">**Direction**:</span><span class="sxs-lookup"><span data-stu-id="db820-341">**Direction**:</span></span>

  - <span data-ttu-id="db820-342">**Entrant**</span><span class="sxs-lookup"><span data-stu-id="db820-342">**Inbound**</span></span>
  - <span data-ttu-id="db820-343">**Sortant**</span><span class="sxs-lookup"><span data-stu-id="db820-343">**Outbound**</span></span>
  - <span data-ttu-id="db820-344">**Intra-organisation**: ce nombre est pour les messages au sein d’un client, c’est-à-dire</span><span class="sxs-lookup"><span data-stu-id="db820-344">**Intra-org**: this count is for messages within a tenant i.e</span></span> <span data-ttu-id="db820-345">sender abc@domain.com sends to recipient xyz@domain.com (counted separately from Inbound and Outbound)</span><span class="sxs-lookup"><span data-stu-id="db820-345">sender abc@domain.com sends to recipient xyz@domain.com (counted separately from Inbound and Outbound)</span></span>

<span data-ttu-id="db820-346">L’affichage agrégé et l’affichage table de données autorisent 90 jours de filtrage.</span><span class="sxs-lookup"><span data-stu-id="db820-346">The aggregate view and data table view allow for 90 days of filtering.</span></span>

<span data-ttu-id="db820-347">Si vous cliquez **sur Filtre,** vous pouvez filtrer le graphique et la table de données.</span><span class="sxs-lookup"><span data-stu-id="db820-347">If you click **Filter**, you can filter both the chart and the data table.</span></span>

<span data-ttu-id="db820-348">Ce graphique présente les messages organisés dans les catégories suivantes :</span><span class="sxs-lookup"><span data-stu-id="db820-348">This chart shows messages organized into the following categories:</span></span>

- <span data-ttu-id="db820-349">**Nombre total de messages électroniques**</span><span class="sxs-lookup"><span data-stu-id="db820-349">**Total email**</span></span>
- <span data-ttu-id="db820-350">**Edge autoriser** et **edge filtré**</span><span class="sxs-lookup"><span data-stu-id="db820-350">**Edge allow** and **Edge filtered**</span></span>
- <span data-ttu-id="db820-351">**Pas de programmes** **malveillants, de détection de pièces jointes fiables,** de détection de moteur <sup>\*</sup> **anti-programme** malveillant et de **messages de règle**</span><span class="sxs-lookup"><span data-stu-id="db820-351">**Not malware**, **Safe Attachments detection**<sup>\*</sup>, **Anti-malware engine detection**, and **Rule messages**</span></span>
- <span data-ttu-id="db820-352">**Pas de hameçonnage,** **d’échec DMARC,** de détection **d’emprunt** d’identité, de détection d’usurpation **d’identité** et de **détection d’hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="db820-352">**Not phish**, **DMARC failure**, **Impersonation detection**, **Spoof detection**, and **Phish detection**</span></span>
- <span data-ttu-id="db820-353">**Aucune détection avec détection de détonation d’URL** et **de détonation d’URL**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="db820-353">**No detection with URL detonation** and **URL detonation detection**<sup>\*</sup></span></span>
- <span data-ttu-id="db820-354">**Pas de courrier indésirable** et  **de courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="db820-354">**Not spam** and  **Spam**</span></span>
- <span data-ttu-id="db820-355">**Courrier non malveillant,** **détection de liens fiables** <sup>\*</sup> et **ZAP**</span><span class="sxs-lookup"><span data-stu-id="db820-355">**Non-malicious email**, **Safe Links detection**<sup>\*</sup>, and **ZAP**</span></span>

<span data-ttu-id="db820-356"><sup>\*</sup> Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="db820-356"><sup>\*</sup> Defender for Office 365</span></span>

<span data-ttu-id="db820-357">Lorsque vous pointez sur une catégorie dans le graphique, vous pouvez voir le nombre de messages dans cette catégorie.</span><span class="sxs-lookup"><span data-stu-id="db820-357">When you hover over a category in the chart, you can see the number of messages in that category.</span></span>

<span data-ttu-id="db820-358">La table de données contient les informations suivantes, indiquées dans l’ordre décroit de date :</span><span class="sxs-lookup"><span data-stu-id="db820-358">The data table contains the following information, shown in descending date order:</span></span>

- <span data-ttu-id="db820-359">**Date**</span><span class="sxs-lookup"><span data-stu-id="db820-359">**Date**</span></span>
- <span data-ttu-id="db820-360">**Nombre total de messages électroniques**</span><span class="sxs-lookup"><span data-stu-id="db820-360">**Total email**</span></span>
- <span data-ttu-id="db820-361">**Edge filtré**</span><span class="sxs-lookup"><span data-stu-id="db820-361">**Edge filtered**</span></span>
- <span data-ttu-id="db820-362">**Moteur anti-programme malveillant, pièces jointes sécurisées, règle filtrée**:</span><span class="sxs-lookup"><span data-stu-id="db820-362">**Anti-malware engine, Safe Attachments, rule filtered**:</span></span>
  - <span data-ttu-id="db820-363">**Règle filtrée**: messages filtrés en raison de règles de flux de messagerie (également appelées règles de transport).</span><span class="sxs-lookup"><span data-stu-id="db820-363">**Rule filtered**: Messages filtered due to  mail flow rules (also known as transport rules).</span></span>
- <span data-ttu-id="db820-364">**DMARC, emprunt d’identité, usurpation d’identité, hameçonnage filtré**:</span><span class="sxs-lookup"><span data-stu-id="db820-364">**DMARC, impersonation, spoof, phish filtered**:</span></span>
  - <span data-ttu-id="db820-365">**DMARC**: messages filtrés en raison de l’échec de la vérification de l’authentification DMARC.</span><span class="sxs-lookup"><span data-stu-id="db820-365">**DMARC**: Messages filtered due to the message failing its DMARC authentication check.</span></span>
- <span data-ttu-id="db820-366">**Détection de détonation d’URL**</span><span class="sxs-lookup"><span data-stu-id="db820-366">**URL detonation detection**</span></span>
- <span data-ttu-id="db820-367">**Filtrage anti-courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="db820-367">**Anti-spam filtered**</span></span>
- <span data-ttu-id="db820-368">**ZAP supprimé**</span><span class="sxs-lookup"><span data-stu-id="db820-368">**ZAP removed**</span></span>
- <span data-ttu-id="db820-369">**Détection par liens fiables**</span><span class="sxs-lookup"><span data-stu-id="db820-369">**Detection by Safe Links**</span></span>

<span data-ttu-id="db820-370">Si vous sélectionnez une ligne dans la table de données, une répartition supplémentaire du nombre de messages électroniques est affichée dans le volant.</span><span class="sxs-lookup"><span data-stu-id="db820-370">If you select a row in the data table, a further breakdown of the email counts are shown in the flyout.</span></span>

<span data-ttu-id="db820-371">**Exporter**:</span><span class="sxs-lookup"><span data-stu-id="db820-371">**Export**:</span></span>

<span data-ttu-id="db820-372">En cliquant sur **Exporter,** sous **Options,** vous pouvez sélectionner l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="db820-372">On clicking **Export**, under **Options** you can select one of the following values:</span></span>

- <span data-ttu-id="db820-373">**Résumé (avec des données pour les 90 derniers jours au maximum)**</span><span class="sxs-lookup"><span data-stu-id="db820-373">**Summary (with data for last 90 days at most)**</span></span>
- <span data-ttu-id="db820-374">**Détails (avec des données pour les 30 derniers jours au maximum)**</span><span class="sxs-lookup"><span data-stu-id="db820-374">**Details (with data for last 30 days at most)**</span></span>

<span data-ttu-id="db820-375">Sous **Date**, choisissez une plage, puis cliquez sur **Appliquer**.</span><span class="sxs-lookup"><span data-stu-id="db820-375">Under **Date**, choose a range, and then click **Apply**.</span></span> <span data-ttu-id="db820-376">Les données des filtres actuels sont exportées vers un fichier .csv.</span><span class="sxs-lookup"><span data-stu-id="db820-376">Data for the current filters will be exported to a .csv file.</span></span>

<span data-ttu-id="db820-377">Chaque fichier .csv exporté est limité à 150 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="db820-377">Each exported .csv file is limited to 150,000 rows.</span></span> <span data-ttu-id="db820-378">Si les données contiennent plus de 150 000 lignes, plusieurs fichiers .csv seront créés.</span><span class="sxs-lookup"><span data-stu-id="db820-378">If the data contains more than 150,000 rows, then multiple .csv files will be created.</span></span>

 ![<span data-ttu-id="db820-379">Affichage technique dans le rapport d’état du flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="db820-379">Tech view in the Mailflow status report</span></span> ](../../media/mail-flow-status-report-Tech-view.png)

## <a name="sent-and-received-email-report"></a><span data-ttu-id="db820-380">Rapport de courrier électronique envoyé et reçu</span><span class="sxs-lookup"><span data-stu-id="db820-380">Sent and received email report</span></span>

<span data-ttu-id="db820-381">Le **rapport de** courrier électronique envoyé et reçu est un rapport intelligent qui affiche des informations sur le courrier électronique entrant et sortant, y compris les détections de courrier indésirable, les programmes malveillants et les messages électroniques identifiés comme « bons ».</span><span class="sxs-lookup"><span data-stu-id="db820-381">The **Sent and received email** report is a smart report that shows information about incoming and outgoing email, including spam detections, malware, and email identified as "good."</span></span> <span data-ttu-id="db820-382">La différence entre ce [](#mailflow-status-report) rapport et le rapport d’état du flux de messagerie est la suivante : ce rapport n’inclut pas de données sur les messages bloqués par la protection Edge. Il est important de comprendre que si un message est envoyé à cinq destinataires, nous le compterons comme un seul message.</span><span class="sxs-lookup"><span data-stu-id="db820-382">The difference between this report and the [Mailflow status report](#mailflow-status-report) is: this report doesn't include data about messages blocked by edge protection.It's important to understand that if a message is sent to five recipients we count it as one message.</span></span>

<span data-ttu-id="db820-383">L’affichage agrégé et l’affichage détaillé du rapport autorisent 90 jours de filtrage.</span><span class="sxs-lookup"><span data-stu-id="db820-383">The aggregate view and the detail view of the report allow for 90 days of filtering.</span></span>

<span data-ttu-id="db820-384">Pour afficher le rapport, ouvrez le Centre de  sécurité [& conformité,](https://protection.office.com)allez au tableau de bord rapports et sélectionnez \>  Courrier électronique envoyé **et reçu.**</span><span class="sxs-lookup"><span data-stu-id="db820-384">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Sent and received email**.</span></span> <span data-ttu-id="db820-385">Pour aller directement dans le rapport, ouvrez <https://protection.office.com/reportv2?id=SentAndReceivedMailATP> .</span><span class="sxs-lookup"><span data-stu-id="db820-385">To go directly to the report, open <https://protection.office.com/reportv2?id=SentAndReceivedMailATP>.</span></span>

![Widget de courrier électronique envoyé et reçu dans le tableau de bord Rapports](../../media/sent-and-received-email-report-widget.png)

### <a name="report-view-for-the-sent-and-received-email-report"></a><span data-ttu-id="db820-387">Affichage du rapport pour le rapport de courrier électronique envoyé et reçu</span><span class="sxs-lookup"><span data-stu-id="db820-387">Report view for the Sent and received email report</span></span>

<span data-ttu-id="db820-388">Les graphiques suivants sont disponibles dans l’affichage de rapport :</span><span class="sxs-lookup"><span data-stu-id="db820-388">The following charts are available in the report view:</span></span>

- <span data-ttu-id="db820-389">**Décomposez par : Type**: le graphique affiche toutes les catégories disponibles :</span><span class="sxs-lookup"><span data-stu-id="db820-389">**Break down by: Type**: The chart shows all available categories:</span></span>

  - <span data-ttu-id="db820-390">**Total**</span><span class="sxs-lookup"><span data-stu-id="db820-390">**Total**</span></span>
  - <span data-ttu-id="db820-391">**Courrier électronique de qualité**</span><span class="sxs-lookup"><span data-stu-id="db820-391">**Good mail**</span></span>
  - <span data-ttu-id="db820-392">**Programmes malveillants (anti-programme malveillant)** (EOP)</span><span class="sxs-lookup"><span data-stu-id="db820-392">**Malware (anti-malware)** (EOP)</span></span>
  - <span data-ttu-id="db820-393">**Détections de courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="db820-393">**Spam detections**</span></span>
  - <span data-ttu-id="db820-394">**Messages de règle**</span><span class="sxs-lookup"><span data-stu-id="db820-394">**Rule messages**</span></span>
  - <span data-ttu-id="db820-395">**Programmes malveillants** avancés (Microsoft Defender pour Office 365)</span><span class="sxs-lookup"><span data-stu-id="db820-395">**Advanced malware** (Microsoft Defender for Office 365)</span></span>

  <span data-ttu-id="db820-396">Lorsque vous pointez sur un jour (point de données) dans le graphique, vous pouvez voir les détails de ce jour.</span><span class="sxs-lookup"><span data-stu-id="db820-396">When you hover over a day (data point) in the chart, you can see details for that day.</span></span>

  ![Affichage des types dans le rapport de courrier électronique envoyé et reçu](../../media/sent-and-received-email-report-type-view.png)

- <span data-ttu-id="db820-398">**Décomposer par : Direction**: le graphique affiche **le total,** le trafic **entrant** et les **données sortantes.**</span><span class="sxs-lookup"><span data-stu-id="db820-398">**Break down by: Direction**: The chart shows **Total**, **Inbound**, and **Outbound** data.</span></span> <span data-ttu-id="db820-399">Lorsque vous pointez sur un jour (point de données) dans le graphique, vous pouvez voir les détails de ce jour.</span><span class="sxs-lookup"><span data-stu-id="db820-399">When you hover over a day (data point) in the chart, you can see details for that day.</span></span>

  ![Affichage de direction dans le rapport de courrier électronique envoyé et reçu](../../media/sent-and-received-email-report-direction-view.png)

- <span data-ttu-id="db820-401">**Descendre** \> **Programmes malveillants (anti-programme malveillant)**: cette sélection vous permet d’en savoir plus sur les détections de programmes [malveillants dans le rapport de courrier électronique.](view-email-security-reports.md#malware-detections-in-email-report)</span><span class="sxs-lookup"><span data-stu-id="db820-401">**Drill down by** \> **Malware (anti-malware)**: This selection takes you to the [Malware detections in email report](view-email-security-reports.md#malware-detections-in-email-report).</span></span>

- <span data-ttu-id="db820-402">**Descendre** \> **Détections de courrier indésirable)**: cette sélection vous permet d’envoyer le rapport [détections de courrier indésirable.](view-email-security-reports.md#spam-detections-report)</span><span class="sxs-lookup"><span data-stu-id="db820-402">**Drill down by** \> **Spam detections)**: This selection takes you to the [Spam Detections report](view-email-security-reports.md#spam-detections-report).</span></span>

<span data-ttu-id="db820-403">Si vous cliquez sur **Filtres** dans un affichage de rapport, vous pouvez modifier les résultats avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="db820-403">If you click **Filters** in a report view, you can modify the results with the following filters:</span></span>

- <span data-ttu-id="db820-404">**Date de début** et **date de fin**</span><span class="sxs-lookup"><span data-stu-id="db820-404">**Start date** and **End date**</span></span>
- <span data-ttu-id="db820-405">Valeurs de direction</span><span class="sxs-lookup"><span data-stu-id="db820-405">Direction values</span></span>
- <span data-ttu-id="db820-406">Valeurs de type</span><span class="sxs-lookup"><span data-stu-id="db820-406">Type values</span></span>

<span data-ttu-id="db820-407">Pour revenir à l’affichage du rapport, cliquez **sur Afficher le rapport.**</span><span class="sxs-lookup"><span data-stu-id="db820-407">To go back to the report view, click **View report**.</span></span>

### <a name="details-table-view-for-the-sent-and-received-email-report"></a><span data-ttu-id="db820-408">Affichage du tableau détails pour le rapport de courrier électronique envoyé et reçu</span><span class="sxs-lookup"><span data-stu-id="db820-408">Details table view for the Sent and received email report</span></span>

<span data-ttu-id="db820-409">Si vous cliquez **sur Afficher les détails dans** le tableau Décomposer par : **Direction** ou Descendre en mode **Direction,** les informations suivantes sont affichées :</span><span class="sxs-lookup"><span data-stu-id="db820-409">If you click **View details table** in the **Break down by: Direction** or **Break down by: Direction** view, the following information is shown:</span></span>

- <span data-ttu-id="db820-410">**Date (UTC)**</span><span class="sxs-lookup"><span data-stu-id="db820-410">**Date (UTC)**</span></span>
- <span data-ttu-id="db820-411">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="db820-411">**Type**</span></span>
- <span data-ttu-id="db820-412">**Direction**</span><span class="sxs-lookup"><span data-stu-id="db820-412">**Direction**</span></span>
- <span data-ttu-id="db820-413">**Nombre de messages**</span><span class="sxs-lookup"><span data-stu-id="db820-413">**Message count**</span></span>

<span data-ttu-id="db820-414">Si vous cliquez **sur Filtres** dans une vue de tableau de détails, vous pouvez modifier les résultats avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="db820-414">If you click **Filters** in a details table view, you can modify the results with the following filters:</span></span>

- <span data-ttu-id="db820-415">**Date de début** et **date de fin**</span><span class="sxs-lookup"><span data-stu-id="db820-415">**Start date** and **End date**</span></span>
- <span data-ttu-id="db820-416">Valeurs de direction</span><span class="sxs-lookup"><span data-stu-id="db820-416">Direction values</span></span>
- <span data-ttu-id="db820-417">Valeurs de type</span><span class="sxs-lookup"><span data-stu-id="db820-417">Type values</span></span>

<span data-ttu-id="db820-418">Pour revenir à l’affichage du rapport, cliquez **sur Afficher le rapport.**</span><span class="sxs-lookup"><span data-stu-id="db820-418">To go back to the report view, click **View report**.</span></span>

## <a name="top-senders-and-recipients-report"></a><span data-ttu-id="db820-419">Rapport sur les principaux expéditeurs et destinataires</span><span class="sxs-lookup"><span data-stu-id="db820-419">Top senders and recipients report</span></span>

<span data-ttu-id="db820-420">Le **rapport Des principaux expéditeurs et destinataires** est un graphique en secteurs montrant vos principaux expéditeurs et destinataires de courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="db820-420">The **Top senders and recipients** report is a pie chart showing your top email senders and recipients.</span></span>

<span data-ttu-id="db820-421">Pour afficher le rapport, ouvrez le Centre de  sécurité [& conformité,](https://protection.office.com)puis sélectionnez Tableau de bord des rapports et sélectionnez Principaux \>  **expéditeurs et destinataires.**</span><span class="sxs-lookup"><span data-stu-id="db820-421">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Top senders and recipients**.</span></span> <span data-ttu-id="db820-422">Pour aller directement dans le rapport, ouvrez <https://protection.office.com/reportv2?id=TopSenderRecipientsATP> .</span><span class="sxs-lookup"><span data-stu-id="db820-422">To go directly to the report, open <https://protection.office.com/reportv2?id=TopSenderRecipientsATP>.</span></span>

![Widget des principaux expéditeurs et destinataires dans le tableau de bord Rapports](../../media/top-senders-and-recipients-widget.png)

### <a name="report-view-for-the-top-senders-and-recipient-report"></a><span data-ttu-id="db820-424">Affichage du rapport pour le rapport des principaux expéditeurs et destinataires</span><span class="sxs-lookup"><span data-stu-id="db820-424">Report view for the Top senders and recipient report</span></span>

<span data-ttu-id="db820-425">Les graphiques suivants sont disponibles dans l’affichage de rapport :</span><span class="sxs-lookup"><span data-stu-id="db820-425">The following charts are available in the report view:</span></span>

- <span data-ttu-id="db820-426">**Afficher les données pour \> les principaux expéditeurs de courrier**</span><span class="sxs-lookup"><span data-stu-id="db820-426">**Show data for \> Top mail senders**</span></span>
- <span data-ttu-id="db820-427">**Afficher les données pour \> les principaux destinataires du courrier**</span><span class="sxs-lookup"><span data-stu-id="db820-427">**Show data for \> Top mail recipients**</span></span>
- <span data-ttu-id="db820-428">**Afficher les données des \> principaux destinataires du courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="db820-428">**Show data for \> Top spam recipients**</span></span>
- <span data-ttu-id="db820-429">**Afficher les données pour \> Principaux destinataires des programmes malveillants** (EOP)</span><span class="sxs-lookup"><span data-stu-id="db820-429">**Show data for \> Top malware recipients** (EOP)</span></span>
- <span data-ttu-id="db820-430">**Afficher les données \> des principaux destinataires de programmes malveillants (Defender pour Office 365)**</span><span class="sxs-lookup"><span data-stu-id="db820-430">**Show data for \> Top malware recipients (Defender for Office 365)**</span></span>

<span data-ttu-id="db820-431">La composition du graphique en secteurs change en fonction de ces sélections.</span><span class="sxs-lookup"><span data-stu-id="db820-431">The composition of the pie chart changes based on these selections.</span></span>

<span data-ttu-id="db820-432">Lorsque vous pointez sur une souris dans le graphique en secteurs, vous pouvez voir le nombre de messages envoyés ou reçus.</span><span class="sxs-lookup"><span data-stu-id="db820-432">When you hover over a wedge in the pie chart, you can see a count of messages sent or received.</span></span>

<span data-ttu-id="db820-433">Si vous cliquez sur **Filtres** dans un affichage de rapport, vous pouvez spécifier une plage de dates avec la **date** de début et la **date de fin.**</span><span class="sxs-lookup"><span data-stu-id="db820-433">If you click **Filters** in a report view, you can specify a date range with **Start date** and **End date**.</span></span>

![Graphique en secteurs en affichage Rapport dans le rapport Des principaux expéditeurs et destinataires](../../media/top-senders-and-recipients-report-view.png)

### <a name="details-table-view-for-the-top-senders-and-recipient-report"></a><span data-ttu-id="db820-435">Vue de table Détails pour le rapport des principaux expéditeurs et destinataires</span><span class="sxs-lookup"><span data-stu-id="db820-435">Details table view for the Top senders and recipient report</span></span>

<span data-ttu-id="db820-436">Si vous cliquez sur Afficher le tableau des **détails,** les informations affichées dépendent du graphique que vous regardiez :</span><span class="sxs-lookup"><span data-stu-id="db820-436">If you click **View details table**, the information that's shown depends on the chart you were looking at:</span></span>

- <span data-ttu-id="db820-437">**Afficher les données pour \> les principaux expéditeurs de courrier**</span><span class="sxs-lookup"><span data-stu-id="db820-437">**Show data for \> Top mail senders**</span></span>

  - <span data-ttu-id="db820-438">**Principaux expéditeurs de courrier**</span><span class="sxs-lookup"><span data-stu-id="db820-438">**Top mail senders**</span></span>
  - <span data-ttu-id="db820-439">**Count**</span><span class="sxs-lookup"><span data-stu-id="db820-439">**Count**</span></span>

- <span data-ttu-id="db820-440">**Afficher les données pour \> les principaux destinataires du courrier**</span><span class="sxs-lookup"><span data-stu-id="db820-440">**Show data for \> Top mail recipients**</span></span>

  - <span data-ttu-id="db820-441">**Principaux destinataires du courrier**</span><span class="sxs-lookup"><span data-stu-id="db820-441">**Top mail recipients**</span></span>
  - <span data-ttu-id="db820-442">**Count**</span><span class="sxs-lookup"><span data-stu-id="db820-442">**Count**</span></span>

- <span data-ttu-id="db820-443">**Afficher les données des \> principaux destinataires du courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="db820-443">**Show data for \> Top spam recipients**</span></span>

  - <span data-ttu-id="db820-444">**Principaux destinataires du courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="db820-444">**Top spam recipients**</span></span>
  - <span data-ttu-id="db820-445">**Count**</span><span class="sxs-lookup"><span data-stu-id="db820-445">**Count**</span></span>

- <span data-ttu-id="db820-446">**Afficher les données pour \> Principaux destinataires des programmes malveillants** (EOP)</span><span class="sxs-lookup"><span data-stu-id="db820-446">**Show data for \> Top malware recipients** (EOP)</span></span>

  - <span data-ttu-id="db820-447">**Principaux destinataires de programmes malveillants**</span><span class="sxs-lookup"><span data-stu-id="db820-447">**Top malware recipients**</span></span>
  - <span data-ttu-id="db820-448">**Count**</span><span class="sxs-lookup"><span data-stu-id="db820-448">**Count**</span></span>

- <span data-ttu-id="db820-449">**Afficher les données \> des principaux destinataires de programmes malveillants (Defender pour Office 365)**</span><span class="sxs-lookup"><span data-stu-id="db820-449">**Show data for \> Top malware recipients (Defender for Office 365)**</span></span>

  - <span data-ttu-id="db820-450">**Principaux destinataires des programmes malveillants (Defender pour Office 365)**</span><span class="sxs-lookup"><span data-stu-id="db820-450">**Top malware recipients (Defender for Office 365)**</span></span>
  - <span data-ttu-id="db820-451">**Count**</span><span class="sxs-lookup"><span data-stu-id="db820-451">**Count**</span></span>

<span data-ttu-id="db820-452">Si vous cliquez sur **Filtres** dans une vue de table de détails, vous pouvez spécifier une plage de dates avec la **date** de début et la **date de fin**.</span><span class="sxs-lookup"><span data-stu-id="db820-452">If you click **Filters** in a details table view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="db820-453">Pour revenir à l’affichage du rapport, cliquez **sur Afficher le rapport.**</span><span class="sxs-lookup"><span data-stu-id="db820-453">To go back to the report view, click **View report**.</span></span>

## <a name="what-permissions-are-needed-to-view-these-reports"></a><span data-ttu-id="db820-454">Quelles autorisations sont nécessaires pour afficher ces rapports ?</span><span class="sxs-lookup"><span data-stu-id="db820-454">What permissions are needed to view these reports?</span></span>

<span data-ttu-id="db820-455">Pour afficher et utiliser les rapports décrits dans cet article, vous devez être membre de l’un des groupes de rôles suivants dans le Centre de sécurité & conformité :</span><span class="sxs-lookup"><span data-stu-id="db820-455">In order to view and use the reports described in this article, you need to be a member of one of the following role groups in the Security & Compliance Center:</span></span>

- <span data-ttu-id="db820-456">**Gestion de l'organisation**</span><span class="sxs-lookup"><span data-stu-id="db820-456">**Organization Management**</span></span>
- <span data-ttu-id="db820-457">**Administrateur de sécurité**</span><span class="sxs-lookup"><span data-stu-id="db820-457">**Security Administrator**</span></span>
- <span data-ttu-id="db820-458">**Lecteur sécurité**</span><span class="sxs-lookup"><span data-stu-id="db820-458">**Security Reader**</span></span>
- <span data-ttu-id="db820-459">**Lecteur global**</span><span class="sxs-lookup"><span data-stu-id="db820-459">**Global Reader**</span></span>

<span data-ttu-id="db820-460">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="db820-460">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

> [!NOTE]
> <span data-ttu-id="db820-461">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux utilisateurs les autorisations requises dans le centre de sécurité et de conformité _et_ les autorisations pour les autres fonctionnalités de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="db820-461">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions in the Security & Compliance Center _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="db820-462">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="db820-462">For more information, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="db820-463">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="db820-463">Related topics</span></span>

[<span data-ttu-id="db820-464">Rapports intelligents et aperçus dans le Centre de sécurité et conformité</span><span class="sxs-lookup"><span data-stu-id="db820-464">Smart reports and insights in the Security & Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)

[<span data-ttu-id="db820-465">Informations sur le flux de messagerie dans le centre de sécurité et conformité</span><span class="sxs-lookup"><span data-stu-id="db820-465">Mail flow insights in the Security & Compliance Center</span></span>](mail-flow-insights-v2.md)

[<span data-ttu-id="db820-466">Afficher les rapports de sécurité de courrier dans le centre de sécurité et conformité</span><span class="sxs-lookup"><span data-stu-id="db820-466">View email security reports in the Security & Compliance Center</span></span>](view-email-security-reports.md)

[<span data-ttu-id="db820-467">Afficher des rapports pour Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="db820-467">View reports for Microsoft Defender for Office 365</span></span>](view-reports-for-atp.md)