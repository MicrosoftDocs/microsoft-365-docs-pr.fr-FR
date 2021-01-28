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
ms.openlocfilehash: e69085d1fad845ab519f2590b0527316463373a7
ms.sourcegitcommit: 537e513a4a232a01e44ecbc76d86a8bcaf142482
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/27/2021
ms.locfileid: "50029797"
---
# <a name="view-mail-flow-reports-in-the-reports-dashboard-in-security--compliance-center"></a><span data-ttu-id="4915d-103">Afficher les rapports de flux de messagerie dans le tableau de bord Rapports du Centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="4915d-103">View mail flow reports in the Reports dashboard in Security & Compliance Center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="4915d-104">Outre les rapports de flux de [](mail-flow-insights-v2.md) messagerie disponibles dans le tableau de bord de flux de messagerie dans le Centre de sécurité & conformité, divers rapports de flux de messagerie supplémentaires sont disponibles dans le tableau de bord Rapports pour vous aider à surveiller votre organisation Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4915d-104">In addition to the mail flow reports that are available in the [Mail flow dashboard](mail-flow-insights-v2.md) in the Security & Compliance Center, a variety of additional mail flow reports are available in the Reports dashboard to help you monitor your Microsoft 365 organization.</span></span>

<span data-ttu-id="4915d-105">Si vous avez les [autorisations](#what-permissions-are-needed-to-view-these-reports)nécessaires, vous pouvez afficher ces rapports dans le Centre de sécurité [& conformité](https://protection.office.com) en allant au Tableau de bord **des** \> **rapports.**</span><span class="sxs-lookup"><span data-stu-id="4915d-105">If you have the [necessary permissions](#what-permissions-are-needed-to-view-these-reports), you can view these reports in the [Security & Compliance Center](https://protection.office.com) by going to **Reports** \> **Dashboard**.</span></span> <span data-ttu-id="4915d-106">Pour aller directement au tableau de bord Rapports, ouvrez <https://protection.office.com/insightdashboard> .</span><span class="sxs-lookup"><span data-stu-id="4915d-106">To go directly to the Reports dashboard, open <https://protection.office.com/insightdashboard>.</span></span>

![Tableau de bord Rapports dans le Centre de sécurité & conformité](../../media/6b213d34-adbb-44af-8549-be9a7e2db087.png)

## <a name="connector-report"></a><span data-ttu-id="4915d-108">Rapport sur le connecteur</span><span class="sxs-lookup"><span data-stu-id="4915d-108">Connector report</span></span>

<span data-ttu-id="4915d-109">Le **rapport Connecteur indique** l’activité de flux de messagerie sur les connecteurs entrants et [sortants configurés](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow) pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4915d-109">The **Connector report** shows mail flow activity on the [inbound and outbound connectors](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow) that are configured for your organization.</span></span>

<span data-ttu-id="4915d-110">Pour afficher le rapport, ouvrez le Centre  de sécurité [& conformité,](https://protection.office.com)allez au tableau de bord rapports \>  et sélectionnez le **rapport connecteur.**</span><span class="sxs-lookup"><span data-stu-id="4915d-110">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Connector report**.</span></span> <span data-ttu-id="4915d-111">Pour aller directement dans le rapport, ouvrez <https://protection.office.com/reportv2?id=ConnectorReport> .</span><span class="sxs-lookup"><span data-stu-id="4915d-111">To go directly to the report, open <https://protection.office.com/reportv2?id=ConnectorReport>.</span></span>

![Widget de rapport connecteur dans le tableau de bord Rapports](../../media/connector-report-widget.png)

### <a name="report-view-for-the-connector-report"></a><span data-ttu-id="4915d-113">Affichage du rapport pour le rapport connecteur</span><span class="sxs-lookup"><span data-stu-id="4915d-113">Report view for the Connector report</span></span>

<span data-ttu-id="4915d-114">Les graphiques suivants sont disponibles en affichage état :</span><span class="sxs-lookup"><span data-stu-id="4915d-114">The following charts are available in report view:</span></span>

- <span data-ttu-id="4915d-115">**Afficher les données par : Flux de messagerie**: ce graphique affiche le nombre de messages entrants et sortants organisés par :</span><span class="sxs-lookup"><span data-stu-id="4915d-115">**View data by: Mail flow**: This chart shows the number of inbound and outbound messages organized by:</span></span>

  - <span data-ttu-id="4915d-116">**Total**</span><span class="sxs-lookup"><span data-stu-id="4915d-116">**Total**</span></span>
  - <span data-ttu-id="4915d-117">**À partir d’Internet sans connecteur**</span><span class="sxs-lookup"><span data-stu-id="4915d-117">**From the internet without a connector**</span></span>
  - <span data-ttu-id="4915d-118">**Vers Internet sans connecteur**</span><span class="sxs-lookup"><span data-stu-id="4915d-118">**To the internet without a connector**</span></span>
  - <span data-ttu-id="4915d-119">Connecteur spécifique que vous avez configuré.</span><span class="sxs-lookup"><span data-stu-id="4915d-119">A specific connector that you've configured.</span></span>

  <span data-ttu-id="4915d-120">Pour isoler les données dans le graphique, utilisez l’option **Afficher** les données pour le contrôle afin de sélectionner l’une de ces options ou tout **flux de messagerie.**</span><span class="sxs-lookup"><span data-stu-id="4915d-120">To isolate the data in the chart, use the **Show data for** control to select one of these options or **All mail flow**.</span></span>

  ![Afficher les données par flux de messagerie dans le rapport connecteur](../../media/connector-report-view-data-by-mail-flow.png)

- <span data-ttu-id="4915d-122">**Afficher les données par : utilisation de TLS**: ce graphique affiche le pourcentage d’utilisation de la version TLS (Transport Layer Security) pour le flux de messagerie.</span><span class="sxs-lookup"><span data-stu-id="4915d-122">**View data by: TLS usage**: This chart shows the percentage of Transport Layer Security (TLS) version usage for mail flow.</span></span>

  <span data-ttu-id="4915d-123">Pour isoler les données dans le graphique, utilisez l’option **Afficher les** données pour le contrôle pour sélectionner l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="4915d-123">To isolate the data in the chart, use the **Show data for** control to select one of the following options:</span></span>

  - <span data-ttu-id="4915d-124">**Tout le flux de messagerie**</span><span class="sxs-lookup"><span data-stu-id="4915d-124">**All mail flow**</span></span>
  - <span data-ttu-id="4915d-125">**À partir d’Internet sans connecteur**</span><span class="sxs-lookup"><span data-stu-id="4915d-125">**From the internet without a connector**</span></span>
  - <span data-ttu-id="4915d-126">**Vers Internet sans connecteur**</span><span class="sxs-lookup"><span data-stu-id="4915d-126">**To the internet without a connector**</span></span>
  - <span data-ttu-id="4915d-127">Connecteur spécifique que vous avez configuré.</span><span class="sxs-lookup"><span data-stu-id="4915d-127">A specific connector that you've configured.</span></span>

  ![Afficher les données par utilisation de TLS dans le rapport connecteur](../../media/connector-report-view-data-by-tls-usage.png)

<span data-ttu-id="4915d-129">Si vous cliquez sur **Filtres** dans un affichage de rapport, vous pouvez spécifier une plage de dates avec la **date** de début et la **date de fin.**</span><span class="sxs-lookup"><span data-stu-id="4915d-129">If you click **Filters** in a report view, you can specify a date range with **Start date** and **End date**.</span></span>

### <a name="details-table-view-for-the-connector-report"></a><span data-ttu-id="4915d-130">Vue de table Détails pour le rapport Connecteur</span><span class="sxs-lookup"><span data-stu-id="4915d-130">Details table view for the Connector report</span></span>

<span data-ttu-id="4915d-131">Si vous cliquez **sur Afficher le tableau des détails** dans un affichage de rapport, les informations suivantes sont affichées :</span><span class="sxs-lookup"><span data-stu-id="4915d-131">If you click **View details table** in a report view, the following information is shown:</span></span>

- <span data-ttu-id="4915d-132">**Date**</span><span class="sxs-lookup"><span data-stu-id="4915d-132">**Date**</span></span>
- <span data-ttu-id="4915d-133">**Direction et nom du connecteur**</span><span class="sxs-lookup"><span data-stu-id="4915d-133">**Connector direction and name**</span></span>
- <span data-ttu-id="4915d-134">**Type de connecteur**</span><span class="sxs-lookup"><span data-stu-id="4915d-134">**Connector type**</span></span>
- <span data-ttu-id="4915d-135">**TLS forcé ?**: la valeur **True** ou **False**.</span><span class="sxs-lookup"><span data-stu-id="4915d-135">**Forced TLS?**: The value **True** or **False**.</span></span>
- <span data-ttu-id="4915d-136">**Pas de TLS** (pourcentage)</span><span class="sxs-lookup"><span data-stu-id="4915d-136">**No TLS** (percentage)</span></span>
- <span data-ttu-id="4915d-137">**TLS 1.0** (pourcentage)</span><span class="sxs-lookup"><span data-stu-id="4915d-137">**TLS 1.0** (percentage)</span></span>
- <span data-ttu-id="4915d-138">**TLS 1.1** (pourcentage)</span><span class="sxs-lookup"><span data-stu-id="4915d-138">**TLS 1.1** (percentage)</span></span>
- <span data-ttu-id="4915d-139">**TLS 1.2** (pourcentage)</span><span class="sxs-lookup"><span data-stu-id="4915d-139">**TLS 1.2** (percentage)</span></span>
- <span data-ttu-id="4915d-140">**Volume**: nombre de messages.</span><span class="sxs-lookup"><span data-stu-id="4915d-140">**Volume**: The number of messages.</span></span>

<span data-ttu-id="4915d-141">Si vous cliquez sur **Filtres** dans une vue de table de détails, vous pouvez spécifier une plage de dates avec la **date** de début et la **date de fin**.</span><span class="sxs-lookup"><span data-stu-id="4915d-141">If you click **Filters** in a details table view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="4915d-142">Pour revenir à l’affichage du rapport, cliquez **sur Afficher le rapport.**</span><span class="sxs-lookup"><span data-stu-id="4915d-142">To go back to the report view, click **View report**.</span></span>

## <a name="exchange-transport-rule-report"></a><span data-ttu-id="4915d-143">Rapport de règles de transport Exchange</span><span class="sxs-lookup"><span data-stu-id="4915d-143">Exchange transport rule report</span></span>

<span data-ttu-id="4915d-144">Le **rapport des règles** de transport Exchange indique l’effet des règles de flux de messagerie (également appelées règles de transport) sur les messages entrants et sortants dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4915d-144">The **Exchange transport rule report** shows the effect of mail flow rules (also known as transport rules) on incoming and outgoing messages in your organization.</span></span>

<span data-ttu-id="4915d-145">Pour afficher le rapport, ouvrez le Centre  de sécurité [& conformité,](https://protection.office.com)puis sélectionnez Tableau de bord rapports \>  et **sélectionnez Règle de transport Exchange.**</span><span class="sxs-lookup"><span data-stu-id="4915d-145">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Exchange Transport rule**.</span></span> <span data-ttu-id="4915d-146">Pour aller directement dans le rapport, ouvrez <https://protection.office.com/reportv2?id=ETRRuleReport> .</span><span class="sxs-lookup"><span data-stu-id="4915d-146">To go directly to the report, open <https://protection.office.com/reportv2?id=ETRRuleReport>.</span></span>

![Widget de règle de transport Exchange dans le tableau de bord Rapports](../../media/transport-rule-report-widget.png)

### <a name="report-view-for-the-exchange-transport-rule-report"></a><span data-ttu-id="4915d-148">Affichage du rapport pour le rapport des règles de transport Exchange</span><span class="sxs-lookup"><span data-stu-id="4915d-148">Report view for the Exchange transport rule report</span></span>

<span data-ttu-id="4915d-149">Les graphiques suivants sont disponibles en affichage état :</span><span class="sxs-lookup"><span data-stu-id="4915d-149">The following charts are available in report view:</span></span>

- <span data-ttu-id="4915d-150">**Afficher les données par : règles de transport** \> Exchange **Décomposer par : Direction**: ce  graphique affiche le nombre de **messages** entrants et sortants affectés par les règles de transport.</span><span class="sxs-lookup"><span data-stu-id="4915d-150">**View data by: Exchange transport rules** \> **Break down by: Direction**: This chart shows the number of **Inbound** and **Outbound** messages that were affected by transport rules.</span></span>

- <span data-ttu-id="4915d-151">**Afficher les données par : règles de transport** \> Exchange **Décomposez par : Gravité :** ce  graphique affiche le nombre de messages de gravité élevée, moyenne et **faible.**</span><span class="sxs-lookup"><span data-stu-id="4915d-151">**View data by: Exchange transport rules** \> **Break down by: Severity**: This chart shows the number of **High severity** and **Medium severity**, and **Low severity** messages.</span></span> <span data-ttu-id="4915d-152">Vous définissez le niveau de gravité en tant qu’action dans la règle (**Auditez** cette règle avec le niveau de gravité _ou SetAuditSeverity_).</span><span class="sxs-lookup"><span data-stu-id="4915d-152">You set the severity level as an action in the rule (**Audit this rule with severity level** or _SetAuditSeverity_).</span></span> <span data-ttu-id="4915d-153">Pour plus d’informations, voir [Actions de règle de flux de messagerie dans Exchange Online.](https://docs.microsoft.com//Exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions)</span><span class="sxs-lookup"><span data-stu-id="4915d-153">For more information, see [Mail flow rule actions in Exchange Online](https://docs.microsoft.com//Exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions).</span></span>

- <span data-ttu-id="4915d-154">**Afficher les données par : règles de transport** \> Exchange DLP **Décomposer par : Direction**: ce  graphique indique le nombre de **messages** entrants et sortants affectés par les règles de transport de protection contre la perte de données (DLP).</span><span class="sxs-lookup"><span data-stu-id="4915d-154">**View data by: DLP Exchange transport rules** \> **Break down by: Direction**: This chart shows the number of **Inbound** and **Outbound** messages that were affected by data loss prevention (DLP) transport rules.</span></span> <span data-ttu-id="4915d-155">Vous pouvez affiner davantage le graphique en sélectionnant l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="4915d-155">You can further refine the chart by selecting on of the following options:</span></span>

  - <span data-ttu-id="4915d-156">**Afficher les données pour : toutes les règles de transport DLP**</span><span class="sxs-lookup"><span data-stu-id="4915d-156">**Show data for: All DLP transport rules**</span></span>
  - <span data-ttu-id="4915d-157">**Afficher les données pour : utilisateurs compromis**</span><span class="sxs-lookup"><span data-stu-id="4915d-157">**Show data for: Compromised users**</span></span>
  - <span data-ttu-id="4915d-158">**Afficher les données pour : faible volume de contenu détecté pour le Patriot Act des États-Unis**</span><span class="sxs-lookup"><span data-stu-id="4915d-158">**Show data for: Low volume of content detected U.S. Patriot Act**</span></span>

- <span data-ttu-id="4915d-159">**Afficher les données par : règles de transport** \> Exchange DLP **Décomposez par : Direction**: cet  affichage indique le nombre de **messages** de gravité élevée et moyenne **et** faible qui ont été affectés par les règles de transport DLP.</span><span class="sxs-lookup"><span data-stu-id="4915d-159">**View data by: DLP Exchange transport rules** \> **Break down by: Direction**: This view shows the number of **High severity** and **Medium severity**, and **Low severity** messages that were affected by DLP transport rules.</span></span> <span data-ttu-id="4915d-160">Vous pouvez affiner davantage le graphique en sélectionnant l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="4915d-160">You can further refine the chart by selecting on of the following options:</span></span>

  - <span data-ttu-id="4915d-161">**Afficher les données pour : toutes les règles de transport DLP**</span><span class="sxs-lookup"><span data-stu-id="4915d-161">**Show data for: All DLP transport rules**</span></span>
  - <span data-ttu-id="4915d-162">**Afficher les données pour : utilisateurs compromis**</span><span class="sxs-lookup"><span data-stu-id="4915d-162">**Show data for: Compromised users**</span></span>
  - <span data-ttu-id="4915d-163">**Afficher les données pour : faible volume de contenu détecté pour le Patriot Act des États-Unis**</span><span class="sxs-lookup"><span data-stu-id="4915d-163">**Show data for: Low volume of content detected U.S. Patriot Act**</span></span>

<span data-ttu-id="4915d-164">Si vous cliquez **sur Filtres** dans un affichage de rapport, vous pouvez modifier les résultats avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="4915d-164">If you click **Filters** in a report view, you can modify the results with the following filters::</span></span>

- <span data-ttu-id="4915d-165">**Date de début** et **date de fin**</span><span class="sxs-lookup"><span data-stu-id="4915d-165">**Start date** and **End date**</span></span>
- <span data-ttu-id="4915d-166">Valeurs de direction</span><span class="sxs-lookup"><span data-stu-id="4915d-166">Direction values</span></span>
- <span data-ttu-id="4915d-167">Valeurs de gravité</span><span class="sxs-lookup"><span data-stu-id="4915d-167">Severity values</span></span>

![Affichage du rapport dans le rapport de règles de transport Exchange](../../media/transport-rule-report-report-view.png)

### <a name="details-table-view-for-the-exchange-transport-rule-report"></a><span data-ttu-id="4915d-169">Vue de table Détails pour le rapport de règles de transport Exchange</span><span class="sxs-lookup"><span data-stu-id="4915d-169">Details table view for the Exchange transport rule report</span></span>

<span data-ttu-id="4915d-170">Si vous cliquez sur Afficher le tableau des **détails,** les informations affichées dépendent du graphique que vous regardiez :</span><span class="sxs-lookup"><span data-stu-id="4915d-170">If you click **View details table**, the information that's shown depends on the chart you were looking at:</span></span>

- <span data-ttu-id="4915d-171">**Afficher les données par : Règles de transport Exchange**:</span><span class="sxs-lookup"><span data-stu-id="4915d-171">**View data by: Exchange Transport rules**:</span></span>

  - <span data-ttu-id="4915d-172">**Date**</span><span class="sxs-lookup"><span data-stu-id="4915d-172">**Date**</span></span>
  - <span data-ttu-id="4915d-173">**Règle de transport**</span><span class="sxs-lookup"><span data-stu-id="4915d-173">**Transport rule**</span></span>
  - <span data-ttu-id="4915d-174">**Subject**</span><span class="sxs-lookup"><span data-stu-id="4915d-174">**Subject**</span></span>
  - <span data-ttu-id="4915d-175">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="4915d-175">**Sender address**</span></span>
  - <span data-ttu-id="4915d-176">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="4915d-176">**Recipient address**</span></span>
  - <span data-ttu-id="4915d-177">**Gravité**</span><span class="sxs-lookup"><span data-stu-id="4915d-177">**Severity**</span></span>
  - <span data-ttu-id="4915d-178">**Direction**</span><span class="sxs-lookup"><span data-stu-id="4915d-178">**Direction**</span></span>

- <span data-ttu-id="4915d-179">**Afficher les données par : Règles de transport Exchange DLP**:</span><span class="sxs-lookup"><span data-stu-id="4915d-179">**View data by: DLP Exchange transport rules**:</span></span>

  - <span data-ttu-id="4915d-180">**Date**</span><span class="sxs-lookup"><span data-stu-id="4915d-180">**Date**</span></span>
  - <span data-ttu-id="4915d-181">**Stratégie DLP**</span><span class="sxs-lookup"><span data-stu-id="4915d-181">**DLP policy**</span></span>
  - <span data-ttu-id="4915d-182">**Règle de transport**</span><span class="sxs-lookup"><span data-stu-id="4915d-182">**Transport rule**</span></span>
  - <span data-ttu-id="4915d-183">**Subject**</span><span class="sxs-lookup"><span data-stu-id="4915d-183">**Subject**</span></span>
  - <span data-ttu-id="4915d-184">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="4915d-184">**Sender address**</span></span>
  - <span data-ttu-id="4915d-185">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="4915d-185">**Recipient address**</span></span>
  - <span data-ttu-id="4915d-186">**Gravité**</span><span class="sxs-lookup"><span data-stu-id="4915d-186">**Severity**</span></span>
  - <span data-ttu-id="4915d-187">**Direction**</span><span class="sxs-lookup"><span data-stu-id="4915d-187">**Direction**</span></span>

<span data-ttu-id="4915d-188">Si vous cliquez **sur Filtres** dans une vue de tableau de détails, vous pouvez modifier les résultats avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="4915d-188">If you click **Filters** in a details table view, you can modify the results with the following filters:</span></span>

- <span data-ttu-id="4915d-189">**Date de début et** **date de fin**</span><span class="sxs-lookup"><span data-stu-id="4915d-189">**Start date** and **End date**</span></span>
- <span data-ttu-id="4915d-190">Valeurs de direction</span><span class="sxs-lookup"><span data-stu-id="4915d-190">Direction values</span></span>
- <span data-ttu-id="4915d-191">Valeurs de gravité</span><span class="sxs-lookup"><span data-stu-id="4915d-191">Severity values</span></span>

<span data-ttu-id="4915d-192">Pour revenir à l’affichage du rapport, cliquez **sur Afficher le rapport.**</span><span class="sxs-lookup"><span data-stu-id="4915d-192">To go back to the report view, click **View report**.</span></span>

## <a name="forwarding-report"></a><span data-ttu-id="4915d-193">Rapport de forwarding</span><span class="sxs-lookup"><span data-stu-id="4915d-193">Forwarding report</span></span>

<span data-ttu-id="4915d-194">Le **rapport de forwarding** affiche les messages automatiquement transmis par votre organisation à des domaines externes à partir de boîtes aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="4915d-194">The **Forwarding report** shows your organization's automatically forwarded messages to external domains from Exchange Online mailboxes.</span></span> <span data-ttu-id="4915d-195">Les messages transmis peuvent présenter un risque de sécurité ou de conformité, et peuvent indiquer un compte compromis.</span><span class="sxs-lookup"><span data-stu-id="4915d-195">Forwarded messages can pose a security or compliance risk, and might indicate a compromised account.</span></span>

<span data-ttu-id="4915d-196">Pour afficher le rapport, ouvrez le Centre de  sécurité [& conformité,](https://protection.office.com)puis sélectionnez Tableau de bord rapports \>  et **sélectionnez Rapport de report.**</span><span class="sxs-lookup"><span data-stu-id="4915d-196">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Forwarding report**.</span></span> <span data-ttu-id="4915d-197">Pour aller directement dans le rapport, ouvrez <https://protection.office.com/reportv2?id=MailFlowForwarding> .</span><span class="sxs-lookup"><span data-stu-id="4915d-197">To go directly to the report, open <https://protection.office.com/reportv2?id=MailFlowForwarding>.</span></span>

![Widget de rapport de forwarding dans le tableau de bord Rapports](../../media/forwarding-report-widget.png)

### <a name="report-view-for-the-forwarding-report"></a><span data-ttu-id="4915d-199">Affichage du rapport pour le rapport de report</span><span class="sxs-lookup"><span data-stu-id="4915d-199">Report view for the Forwarding report</span></span>

<span data-ttu-id="4915d-200">Les graphiques suivants sont disponibles dans l’affichage de rapport :</span><span class="sxs-lookup"><span data-stu-id="4915d-200">The following charts are available in the report view:</span></span>

- <span data-ttu-id="4915d-201">**Afficher les données pour : Méthodes de forwarding**: les méthodes suivantes sont affichées :</span><span class="sxs-lookup"><span data-stu-id="4915d-201">**Show data for: Forwarding methods**: The following methods are shown:</span></span>

  - <span data-ttu-id="4915d-202">**Règle de transport**: également appelée règles [de flux de messagerie.](https://docs.microsoft.com/Exchange/security-and-compliance/mail-flow-rules/mail-flow-rules)</span><span class="sxs-lookup"><span data-stu-id="4915d-202">**Transport rule**: Also known as [mail flow rules](https://docs.microsoft.com/Exchange/security-and-compliance/mail-flow-rules/mail-flow-rules).</span></span>
  - <span data-ttu-id="4915d-203">**Règle de boîte** aux lettres : également appelée [règles de boîte de réception.](https://support.microsoft.com/office/c24f5dea-9465-4df4-ad17-a50704d66c59)</span><span class="sxs-lookup"><span data-stu-id="4915d-203">**Mailbox rule**: Also known as [Inbox rules](https://support.microsoft.com/office/c24f5dea-9465-4df4-ad17-a50704d66c59).</span></span>

  ![Affichage des méthodes de forwarding dans le rapport de forwarding](../../media/forwarding-report-forwarding-methods.png)

- <span data-ttu-id="4915d-205">**Afficher les données pour : Domaines de forwarding**: cet affichage affiche les domaines destinataires qui sont les destinations pour le forwarding.</span><span class="sxs-lookup"><span data-stu-id="4915d-205">**Show data for: Forwarding domains**: This view shows the recipient domains that are the destinations for forwarding.</span></span>

  ![Affichage des domaines de forwarding dans le rapport de forwarding](../../media/forwarding-report-forwarding-domains.png)

- <span data-ttu-id="4915d-207">**Afficher les données pour : Forwarders**: les forwardeurs suivants sont affichés :</span><span class="sxs-lookup"><span data-stu-id="4915d-207">**Show data for: Forwarders**: The following forwarders are shown:</span></span>

  - <span data-ttu-id="4915d-208">**Règle de transport**</span><span class="sxs-lookup"><span data-stu-id="4915d-208">**Transport rule**</span></span>
  - <span data-ttu-id="4915d-209">Boîte aux lettres contenant la règle de boîte de réception de forwarding.</span><span class="sxs-lookup"><span data-stu-id="4915d-209">The mailbox that contains the forwarding Inbox rule.</span></span>

  ![Affichage des forwardeurs dans le rapport de forwarding](../../media/forwarding-report-forwarders.png)

<span data-ttu-id="4915d-211">Si vous cliquez sur **Filtres** dans un affichage de rapport, vous pouvez spécifier une plage de dates avec la **date** de début et la **date de fin.**</span><span class="sxs-lookup"><span data-stu-id="4915d-211">If you click **Filters** in a report view, you can specify a date range with **Start date** and **End date**.</span></span>

### <a name="details-table-view-for-the-forwarding-report"></a><span data-ttu-id="4915d-212">Vue de table Détails pour le rapport de report</span><span class="sxs-lookup"><span data-stu-id="4915d-212">Details table view for the Forwarding report</span></span>

<span data-ttu-id="4915d-213">Si vous cliquez **sur Afficher le tableau des détails** dans un affichage de rapport, les informations suivantes sont affichées :</span><span class="sxs-lookup"><span data-stu-id="4915d-213">If you click **View details table** in a report view, the following information is shown:</span></span>

- <span data-ttu-id="4915d-214">**Forwarders :** règle de **transport de valeur** ou boîte aux lettres qui contient la règle de boîte de réception de transport.</span><span class="sxs-lookup"><span data-stu-id="4915d-214">**Forwarders**: The value **Transport rule** or the mailbox that contains the forwarding Inbox rule.</span></span>
- <span data-ttu-id="4915d-215">**Type de transport :** la règle de boîte **aux lettres de valeur** ou la règle **de transport**.</span><span class="sxs-lookup"><span data-stu-id="4915d-215">**Forwarding type**: The value **Mailbox rule** or **Transport rule**.</span></span>
- <span data-ttu-id="4915d-216">**Nom du destinataire**</span><span class="sxs-lookup"><span data-stu-id="4915d-216">**Recipient name**</span></span>
- <span data-ttu-id="4915d-217">**Domaine du destinataire**</span><span class="sxs-lookup"><span data-stu-id="4915d-217">**Recipient domain**</span></span>
- <span data-ttu-id="4915d-218">**Détails**: il s’agit de la valeur GUID de la règle de flux de messagerie ou de la valeur RuleIdentity de la règle de boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="4915d-218">**Details**: This is the GUID value of the mail flow rule, or the RuleIdentity value of the Inbox rule.</span></span>
- <span data-ttu-id="4915d-219">**Count**</span><span class="sxs-lookup"><span data-stu-id="4915d-219">**Count**</span></span>
- <span data-ttu-id="4915d-220">**Première date d’avance**</span><span class="sxs-lookup"><span data-stu-id="4915d-220">**First forward date**</span></span>

<span data-ttu-id="4915d-221">Si vous cliquez sur **Filtres** dans une vue de tableau de détails, vous pouvez spécifier une plage de dates avec la **date** de début et la **date de fin.**</span><span class="sxs-lookup"><span data-stu-id="4915d-221">If you click **Filters** in a details table view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="4915d-222">Pour revenir à l’affichage Rapports, cliquez **sur Afficher le rapport.**</span><span class="sxs-lookup"><span data-stu-id="4915d-222">To go back to the reports view, click **View report**.</span></span>

## <a name="mailflow-status-report"></a><span data-ttu-id="4915d-223">Rapport d’état du flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="4915d-223">Mailflow status report</span></span>

<span data-ttu-id="4915d-224">Le **rapport d’état du** flux de messagerie est similaire au rapport de courrier électronique envoyé et reçu, avec des informations supplémentaires sur le courrier électronique autorisé ou bloqué sur le edge. [](#sent-and-received-email-report)</span><span class="sxs-lookup"><span data-stu-id="4915d-224">The **Mailflow status report** is similar to the [Sent and received email report](#sent-and-received-email-report), with additional information about email allowed or blocked on the edge.</span></span> <span data-ttu-id="4915d-225">Il s’agit du seul rapport qui contient des informations sur la protection edge et indique la quantité de courrier électronique bloquée avant d’être autorisé dans le service pour évaluation par Exchange Online Protection (EOP).</span><span class="sxs-lookup"><span data-stu-id="4915d-225">This is the only report that contains edge protection information, and shows just how much email is blocked before being allowed into the service for evaluation by Exchange Online Protection (EOP).</span></span> <span data-ttu-id="4915d-226">Il est important de comprendre que si un message est envoyé à cinq destinataires, nous le compterons comme cinq messages différents et pas un seul message.</span><span class="sxs-lookup"><span data-stu-id="4915d-226">It's important to understand that if a message is sent to five recipients we count it as five different messages and not one message.</span></span>
<span data-ttu-id="4915d-227">Pour afficher le rapport, ouvrez le Centre de  sécurité [& conformité,](https://protection.office.com)allez au tableau de bord rapports et sélectionnez Rapport d’état du \>  flux **de messagerie.**</span><span class="sxs-lookup"><span data-stu-id="4915d-227">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Mailflow status report**.</span></span> <span data-ttu-id="4915d-228">Pour aller directement au rapport d’état du **flux de messagerie,** ouvrez <https://protection.office.com/mailflowStatusReport> .</span><span class="sxs-lookup"><span data-stu-id="4915d-228">To go directly to the **Mail flow status report**, open <https://protection.office.com/mailflowStatusReport>.</span></span>

![Widget de rapport d’état du flux de messagerie dans le tableau de bord Rapports](../../media/mail-flow-status-report-widget.png)

### <a name="type-view-for-the-mailflow-status-report"></a><span data-ttu-id="4915d-230">Affichage des types pour le rapport d’état du flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="4915d-230">Type view for the Mailflow status report</span></span>

<span data-ttu-id="4915d-231">Lorsque vous ouvrez l’état, **l’onglet Type** est sélectionné par défaut.</span><span class="sxs-lookup"><span data-stu-id="4915d-231">When you open the report, the **Type** tab is selected by default.</span></span> <span data-ttu-id="4915d-232">Par défaut, cet affichage contient un graphique et une table de données configurés avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="4915d-232">By default, this view contains a chart and a data table that's configured with the following filters:</span></span>

- <span data-ttu-id="4915d-233">**Date**: 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="4915d-233">**Date**: The last 7 days.</span></span>
- <span data-ttu-id="4915d-234">**Direction**:</span><span class="sxs-lookup"><span data-stu-id="4915d-234">**Direction**:</span></span>

  - <span data-ttu-id="4915d-235">**Entrant**</span><span class="sxs-lookup"><span data-stu-id="4915d-235">**Inbound**</span></span>
  - <span data-ttu-id="4915d-236">**Sortant**</span><span class="sxs-lookup"><span data-stu-id="4915d-236">**Outbound**</span></span>
  - <span data-ttu-id="4915d-237">**Intra-organisation**: ce nombre est pour les messages au sein d’un client, c’est-à-dire</span><span class="sxs-lookup"><span data-stu-id="4915d-237">**Intra-org**: this count is for messages within a tenant i.e</span></span> <span data-ttu-id="4915d-238">sender abc@domain.com sends to recipient xyz@domain.com (counted separately from **Inbound** and **Outbound**)</span><span class="sxs-lookup"><span data-stu-id="4915d-238">sender abc@domain.com sends to recipient xyz@domain.com  (counted separately from **Inbound** and **Outbound**)</span></span>

- <span data-ttu-id="4915d-239">**Tapez**:</span><span class="sxs-lookup"><span data-stu-id="4915d-239">**Type**:</span></span>

  - <span data-ttu-id="4915d-240">**Bon courrier**</span><span class="sxs-lookup"><span data-stu-id="4915d-240">**Good mail**</span></span>
  - <span data-ttu-id="4915d-241">**Programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="4915d-241">**Malware**</span></span>
  - <span data-ttu-id="4915d-242">**Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="4915d-242">**Spam**</span></span>
  - <span data-ttu-id="4915d-243">**Protection Edge**</span><span class="sxs-lookup"><span data-stu-id="4915d-243">**Edge protection**</span></span>
  - <span data-ttu-id="4915d-244">**Messages de règle**</span><span class="sxs-lookup"><span data-stu-id="4915d-244">**Rule messages**</span></span>
  - <span data-ttu-id="4915d-245">**Courriers hameçons**</span><span class="sxs-lookup"><span data-stu-id="4915d-245">**Phishing email**</span></span>

<span data-ttu-id="4915d-246">Le graphique est organisé par les valeurs **Type.**</span><span class="sxs-lookup"><span data-stu-id="4915d-246">The chart is organized by the **Type** values.</span></span>

<span data-ttu-id="4915d-247">Vous pouvez modifier ces filtres en cliquant sur **Filtre** ou en cliquant sur une valeur dans la légende du graphique.</span><span class="sxs-lookup"><span data-stu-id="4915d-247">You can change these filters by clicking **Filter** or by clicking a value in the chart legend.</span></span>

<span data-ttu-id="4915d-248">La table de données contient les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="4915d-248">The data table contains the following information:</span></span>

- <span data-ttu-id="4915d-249">**Direction**</span><span class="sxs-lookup"><span data-stu-id="4915d-249">**Direction**</span></span>
- <span data-ttu-id="4915d-250">**Type**</span><span class="sxs-lookup"><span data-stu-id="4915d-250">**Type**</span></span>
- <span data-ttu-id="4915d-251">**24 heures**</span><span class="sxs-lookup"><span data-stu-id="4915d-251">**24 hours**</span></span>
- <span data-ttu-id="4915d-252">**3 jours**</span><span class="sxs-lookup"><span data-stu-id="4915d-252">**3 days**</span></span>
- <span data-ttu-id="4915d-253">**7 jours**</span><span class="sxs-lookup"><span data-stu-id="4915d-253">**7 days**</span></span>
- <span data-ttu-id="4915d-254">**15 jours**</span><span class="sxs-lookup"><span data-stu-id="4915d-254">**15 days**</span></span>
- <span data-ttu-id="4915d-255">**30 jours**</span><span class="sxs-lookup"><span data-stu-id="4915d-255">**30 days**</span></span>

<span data-ttu-id="4915d-256">Si vous cliquez **sur Choisir une catégorie pour plus de détails,** vous pouvez choisir parmi les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="4915d-256">If you click **Choose a category for more details**, you can select from the following values:</span></span>

- <span data-ttu-id="4915d-257">**E-mail de hameçonnage**: cette sélection vous place dans le rapport d’état [de la protection contre les menaces.](view-email-security-reports.md#threat-protection-status-report)</span><span class="sxs-lookup"><span data-stu-id="4915d-257">**Phishing email**: This selection takes you to the [Threat protection status report](view-email-security-reports.md#threat-protection-status-report).</span></span>
- <span data-ttu-id="4915d-258">**Programmes malveillants dans les e-mails**: cette sélection vous place dans le rapport d’état [de la protection contre les menaces.](view-email-security-reports.md#threat-protection-status-report)</span><span class="sxs-lookup"><span data-stu-id="4915d-258">**Malware in email**: This selection takes you to the [Threat protection status report](view-email-security-reports.md#threat-protection-status-report).</span></span>
- <span data-ttu-id="4915d-259">**Détections de courrier indésirable**: cette sélection vous permet d’envoyer le rapport [détections de courrier indésirable.](view-email-security-reports.md#spam-detections-report)</span><span class="sxs-lookup"><span data-stu-id="4915d-259">**Spam detections**: This selection takes you to the [Spam Detections report](view-email-security-reports.md#spam-detections-report).</span></span>
- <span data-ttu-id="4915d-260">**Courrier indésirable bloqué edge**: cette sélection vous permet d’envoyer le rapport [détections de courrier indésirable.](view-email-security-reports.md#spam-detections-report)</span><span class="sxs-lookup"><span data-stu-id="4915d-260">**Edge blocked spam**: This selection takes you to the [Spam Detections report](view-email-security-reports.md#spam-detections-report).</span></span>

<span data-ttu-id="4915d-261">**Exporter**:</span><span class="sxs-lookup"><span data-stu-id="4915d-261">**Export**:</span></span>

<span data-ttu-id="4915d-262">Pour l’affichage détaillé, vous ne pouvez exporter les données que pour une journée.</span><span class="sxs-lookup"><span data-stu-id="4915d-262">For the detail view, you can only export data for one day.</span></span> <span data-ttu-id="4915d-263">Par exemple, si vous souhaitez exporter des données pendant 7 jours, vous devez faire 7 actions d’exportation différentes.</span><span class="sxs-lookup"><span data-stu-id="4915d-263">So, if you want to export data for 7 days, you need to do 7 different export actions.</span></span>

<span data-ttu-id="4915d-264">Chaque fichier .csv exporté est limité à 150 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="4915d-264">Each exported .csv file is limited to 150,000 rows.</span></span> <span data-ttu-id="4915d-265">Si les données de ce jour contiennent plus de 150 000 lignes, plusieurs fichiers .csv seront créés.</span><span class="sxs-lookup"><span data-stu-id="4915d-265">If the data for that day contains more than 150,000 rows, then multiple .csv files will be created.</span></span>

![<span data-ttu-id="4915d-266">Affichage des types dans le rapport d’état du flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="4915d-266">Type view in the Mailflow status report</span></span> ](../../media/mail-flow-status-report-type-view.png)

### <a name="direction-view-for-the-mailflow-status-report"></a><span data-ttu-id="4915d-267">Affichage direction pour le rapport d’état du flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="4915d-267">Direction view for the Mailflow status report</span></span>

<span data-ttu-id="4915d-268">Si vous cliquez sur **l’onglet Direction,** les mêmes filtres par défaut de **l’affichage Type** sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="4915d-268">If you click the **Direction** tab, the same default filters from the **Type** view are used.</span></span>

<span data-ttu-id="4915d-269">Le graphique est organisé par **valeurs direction.**</span><span class="sxs-lookup"><span data-stu-id="4915d-269">The chart is organized by **Direction** values.</span></span>

<span data-ttu-id="4915d-270">Vous pouvez modifier ces filtres en cliquant sur **Filtre** ou en cliquant sur une valeur dans la légende du graphique.</span><span class="sxs-lookup"><span data-stu-id="4915d-270">You can change these filters by clicking **Filter** or by clicking a value in the chart legend.</span></span> <span data-ttu-id="4915d-271">Les mêmes filtres de **l’affichage Type** sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="4915d-271">The same filters from the **Type** view are used.</span></span>

<span data-ttu-id="4915d-272">La table de données contient les mêmes informations que **l’affichage Type.**</span><span class="sxs-lookup"><span data-stu-id="4915d-272">The data table contains same information from the **Type** view.</span></span>

<span data-ttu-id="4915d-273">La **sélection d’une catégorie pour plus d’informations** sur les sélections disponibles et le comportement sont identiques à l’affichage **Type.**</span><span class="sxs-lookup"><span data-stu-id="4915d-273">The **Choose a category for more details** available selections and behavior are the same as the **Type** view.</span></span>

<span data-ttu-id="4915d-274">**Exporter**:</span><span class="sxs-lookup"><span data-stu-id="4915d-274">**Export**:</span></span>

<span data-ttu-id="4915d-275">Pour l’affichage détaillé, vous ne pouvez exporter les données que pour une journée.</span><span class="sxs-lookup"><span data-stu-id="4915d-275">For the detail view, you can only export data for one day.</span></span> <span data-ttu-id="4915d-276">Par exemple, si vous souhaitez exporter des données pendant 7 jours, vous devez faire 7 actions d’exportation différentes.</span><span class="sxs-lookup"><span data-stu-id="4915d-276">So, if you want to export data for 7 days, you need to do 7 different export actions.</span></span>

<span data-ttu-id="4915d-277">Chaque fichier .csv exporté est limité à 150 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="4915d-277">Each exported .csv file is limited to 150,000 rows.</span></span> <span data-ttu-id="4915d-278">Si les données de ce jour contiennent plus de 150 000 lignes, plusieurs fichiers .csv seront créés.</span><span class="sxs-lookup"><span data-stu-id="4915d-278">If the data for that day contains more than 150,000 rows, then multiple .csv files will be created.</span></span>

![<span data-ttu-id="4915d-279">Affichage direction dans le rapport d’état du flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="4915d-279">Direction view in the Mailflow status report</span></span> ](../../media/mail-flow-status-report-direction-view.png)

### <a name="funnel-view-for-the-mailflow-status-report"></a><span data-ttu-id="4915d-280">Affichage en entonnoir pour le rapport d’état du flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="4915d-280">Funnel view for the Mailflow status report</span></span>

<span data-ttu-id="4915d-281">La **vue Entonnoir** vous montre comment les fonctionnalités de protection contre les menaces de courrier électronique de Microsoft filtrent le courrier électronique entrant et sortant dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4915d-281">The **Funnel** view shows you how Microsoft's email threat protection features filter incoming and outgoing email in your organization.</span></span> <span data-ttu-id="4915d-282">Il fournit des détails sur le nombre total de messages électroniques et sur la façon dont les fonctionnalités de protection contre les menaces configurées, y compris la protection edge, la protection contre les programmes malveillants, l’anti-hameçonnage, le courrier indésirable et la détection d’usurpation d’accès affectent ce nombre.</span><span class="sxs-lookup"><span data-stu-id="4915d-282">It provides details on the total email count, and how the configured threat protection features, including edge protection, anti-malware, anti-phishing, anti-spam, and anti-spoofing affect this count.</span></span>

<span data-ttu-id="4915d-283">Si vous  cliquez sur l’onglet Entonnoir, par défaut, cet affichage contient un graphique et une table de données configurés avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="4915d-283">If you click the **Funnel** tab, by default, this view contains a chart and a data table that's configured with the following filters:</span></span>

- <span data-ttu-id="4915d-284">**Date**: 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="4915d-284">**Date**: The last 7 days.</span></span>

- <span data-ttu-id="4915d-285">**Direction**:</span><span class="sxs-lookup"><span data-stu-id="4915d-285">**Direction**:</span></span>

  - <span data-ttu-id="4915d-286">**Entrant**</span><span class="sxs-lookup"><span data-stu-id="4915d-286">**Inbound**</span></span>
  - <span data-ttu-id="4915d-287">**Sortant**</span><span class="sxs-lookup"><span data-stu-id="4915d-287">**Outbound**</span></span>
  - <span data-ttu-id="4915d-288">**Intra-organisation**: ce nombre est le nombre de messages envoyés au sein d’un client ; Autrement dit, l’expéditeur abc@domain.com envoyé au destinataire xyz@domain.com (comptabilisé séparément des messages entrants et sortants).</span><span class="sxs-lookup"><span data-stu-id="4915d-288">**Intra-org**: This count is for messages sent within a tenant; i.e, sender abc@domain.com sends to recipient xyz@domain.com (counted separately from Inbound and Outbound).</span></span>

<span data-ttu-id="4915d-289">L’affichage agrégé et l’affichage de table de données autorisent 90 jours de filtrage.</span><span class="sxs-lookup"><span data-stu-id="4915d-289">The aggregate view and data table view allow for 90 days of filtering.</span></span>

<span data-ttu-id="4915d-290">Si vous cliquez **sur Filtre,** vous pouvez filtrer le graphique et la table de données.</span><span class="sxs-lookup"><span data-stu-id="4915d-290">If you click **Filter**, you can filter both the chart and the data table.</span></span>

<span data-ttu-id="4915d-291">Ce graphique indique le nombre de messages électroniques organisés par :</span><span class="sxs-lookup"><span data-stu-id="4915d-291">This chart shows the email count organized by:</span></span>

- <span data-ttu-id="4915d-292">**Nombre total de messages électroniques**</span><span class="sxs-lookup"><span data-stu-id="4915d-292">**Total email**</span></span>
- <span data-ttu-id="4915d-293">**Courrier électronique après protection edge**</span><span class="sxs-lookup"><span data-stu-id="4915d-293">**Email after edge protection**</span></span>
- <span data-ttu-id="4915d-294">**Courrier électronique après anti-programme malveillant, réputation du fichier, bloc de type de fichier**</span><span class="sxs-lookup"><span data-stu-id="4915d-294">**Email after anti-malware, file reputation, file type block**</span></span>
- <span data-ttu-id="4915d-295">**Courrier électronique après anti-hameçonnage, réputation d’URL, emprunt d’identité de marque, anti-usurpation**</span><span class="sxs-lookup"><span data-stu-id="4915d-295">**Email after anti-phish, URL reputation, brand impersonation, anti-spoof**</span></span>
- <span data-ttu-id="4915d-296">**Courrier électronique après filtrage du courrier indésirable en bloc**</span><span class="sxs-lookup"><span data-stu-id="4915d-296">**Email after anti-spam, bulk mail filtering**</span></span>
- <span data-ttu-id="4915d-297">**Courrier électronique après l’emprunt d’identité d’utilisateur et** de <sup>domaine 1</sup></span><span class="sxs-lookup"><span data-stu-id="4915d-297">**Email after user and domain impersonation**<sup>1</sup></span></span>
- <span data-ttu-id="4915d-298">**Email after file and URL detonation**<sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="4915d-298">**Email after file and URL detonation**<sup>1</sup></span></span>
- <span data-ttu-id="4915d-299">**Courrier électronique détecté comme étant anodin après la remise (protection de temps de clic d’URL)**</span><span class="sxs-lookup"><span data-stu-id="4915d-299">**Email detected as benign after post-delivery protection (URL click time protection)**</span></span>

<span data-ttu-id="4915d-300"><sup>1</sup> Defender pour Office 365 uniquement</span><span class="sxs-lookup"><span data-stu-id="4915d-300"><sup>1</sup> Defender for Office 365 only</span></span>

<span data-ttu-id="4915d-301">Pour afficher séparément les messages électroniques filtrés par EOP ou Defender pour Office 365, cliquez sur la valeur dans la légende du graphique.</span><span class="sxs-lookup"><span data-stu-id="4915d-301">To view the email filtered by EOP or Defender for Office 365 separately, click on the value in the chart legend.</span></span>

<span data-ttu-id="4915d-302">La table de données contient les informations suivantes, indiquées dans l’ordre décroit de date :</span><span class="sxs-lookup"><span data-stu-id="4915d-302">The data table contains the following information, shown in descending date order:</span></span>

- <span data-ttu-id="4915d-303">**Date**</span><span class="sxs-lookup"><span data-stu-id="4915d-303">**Date**</span></span>
- <span data-ttu-id="4915d-304">**Nombre total de messages électroniques**</span><span class="sxs-lookup"><span data-stu-id="4915d-304">**Total email**</span></span>
- <span data-ttu-id="4915d-305">**Protection Edge**</span><span class="sxs-lookup"><span data-stu-id="4915d-305">**Edge protection**</span></span>
- <span data-ttu-id="4915d-306">**Anti-programme malveillant, réputation de fichier, bloc de type de fichier**:</span><span class="sxs-lookup"><span data-stu-id="4915d-306">**Anti-malware, file reputation, file type block**:</span></span>
  - <span data-ttu-id="4915d-307">**Réputation du** fichier : messages filtrés en raison de l’identification d’un fichier joint par d’autres clients Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4915d-307">**File reputation**: Messages filtered due to identification of an attached file by other Microsoft customers.</span></span>
  - <span data-ttu-id="4915d-308">**Bloc de type de** fichier : messages filtrés en raison du type de fichier malveillant identifié dans le message.</span><span class="sxs-lookup"><span data-stu-id="4915d-308">**File type block**: Messages filtered due to the type of malicious file identified in the message.</span></span>
- <span data-ttu-id="4915d-309">**Anti-hameçonnage, réputation de l’URL, emprunt d’identité de marque, anti-usurpation d’identité**:</span><span class="sxs-lookup"><span data-stu-id="4915d-309">**Anti-phish, URL reputation, Brand impersonation, anti-spoof**:</span></span>
  - <span data-ttu-id="4915d-310">**Réputation de l’URL**: messages filtrés en raison de l’identification de l’URL par d’autres clients Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4915d-310">**URL reputation**: Messages filtered due to the identification of the URL by other Microsoft customers.</span></span>
  - <span data-ttu-id="4915d-311">**Emprunt d’identité de marque**: messages filtrés en raison du message provenant de la marque connue usurpant l’identité des expéditeurs.</span><span class="sxs-lookup"><span data-stu-id="4915d-311">**Brand impersonation**: Messages filtered due to the message coming from well-known brand impersonating senders.</span></span>
  - <span data-ttu-id="4915d-312">**Anti-usurpation**: messages filtrés en raison de la tentative d’usurpation d’un domaine appartenant au destinataire ou d’un domaine que l’expéditeur du message ne possède pas.</span><span class="sxs-lookup"><span data-stu-id="4915d-312">**Anti-spoof**: Messages filtered due to the message attempting to spoof a domain that the recipient belongs to, or a domain that the message sender doesn't own.</span></span>
- <span data-ttu-id="4915d-313">**Anti-courrier indésirable, filtrage du courrier en bloc**:</span><span class="sxs-lookup"><span data-stu-id="4915d-313">**Anti-spam, bulk mail filtering**:</span></span>
  - <span data-ttu-id="4915d-314">**Filtrage du courrier en nombre**: messages filtrés en raison d’une tentative de remettre des messages en nombre à ses destinataires.</span><span class="sxs-lookup"><span data-stu-id="4915d-314">**Bulk mail filtering**: Messages filtered due to an attempt to deliver bulk mail to its recipients.</span></span>
- <span data-ttu-id="4915d-315">**Emprunt d’identité d’utilisateur et de domaine (Defender pour Office 365)**:</span><span class="sxs-lookup"><span data-stu-id="4915d-315">**User and domain impersonation (Defender for Office 365)**:</span></span>
  - <span data-ttu-id="4915d-316">**Emprunt d’identité** d’utilisateur : messages filtrés en raison d’une tentative d’emprunt d’identité d’un utilisateur (expéditeur de message) défini dans les paramètres de protection contre l’emprunt d’identité d’une stratégie anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="4915d-316">**User impersonation**: Messages filtered due to an attempt to impersonate a user (message sender) that's defined in the impersonation protection settings of an anti-phishing policy.</span></span>
  - <span data-ttu-id="4915d-317">**Emprunt d’identité** de domaine : messages filtrés en raison d’une tentative d’emprunt d’identité d’un domaine défini dans les paramètres de protection contre l’emprunt d’identité d’une stratégie anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="4915d-317">**Domain impersonation**: Messages filtered due to an attempt to impersonate a domain that's defined in the impersonation protection settings of an anti-phishing policy.</span></span>
- <span data-ttu-id="4915d-318">**Détonation de fichiers et d’URL (Defender pour Office 365)**:</span><span class="sxs-lookup"><span data-stu-id="4915d-318">**File and URL detonation (Defender for Office 365)**:</span></span>
  - <span data-ttu-id="4915d-319">**Détonation de fichier**: messages filtrés par une stratégie de pièces jointes sécurisées.</span><span class="sxs-lookup"><span data-stu-id="4915d-319">**File detonation**: Messages filtered by a Safe Attachments policy.</span></span>
  - <span data-ttu-id="4915d-320">**Détonation d’URL**: message filtré par une stratégie de liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="4915d-320">**URL detonation**: Message filtered by a Safe Links policy.</span></span>
- <span data-ttu-id="4915d-321">**Protection post-remise et ZAP (ATP) ou ZAP (EOP)**: ZAP indique une purge automatique de zéro heure.</span><span class="sxs-lookup"><span data-stu-id="4915d-321">**Post-delivery protection and ZAP (ATP), or ZAP (EOP)**: ZAP indicates zero hour auto-purge.</span></span>

<span data-ttu-id="4915d-322">Si vous sélectionnez une ligne dans la table de données, une répartition supplémentaire du nombre de messages électroniques est affichée dans le volant.</span><span class="sxs-lookup"><span data-stu-id="4915d-322">If you select a row in the data table, a further breakdown of the email counts are shown in the flyout.</span></span>

<span data-ttu-id="4915d-323">**Exporter**:</span><span class="sxs-lookup"><span data-stu-id="4915d-323">**Export**:</span></span>

<span data-ttu-id="4915d-324">Après avoir cliqué **sur Exporter** sous **Options,** vous pouvez sélectionner l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="4915d-324">After you click **Export** under **Options**, you can select one of the following values:</span></span>

- <span data-ttu-id="4915d-325">**Résumé (avec des données pour les 90 derniers jours au maximum)**</span><span class="sxs-lookup"><span data-stu-id="4915d-325">**Summary (with data for last 90 days at most)**</span></span>
- <span data-ttu-id="4915d-326">**Détails (avec des données pour les 30 derniers jours au maximum)**</span><span class="sxs-lookup"><span data-stu-id="4915d-326">**Details (with data for last 30 days at most)**</span></span>

<span data-ttu-id="4915d-327">Sous **Date**, choisissez une plage, puis cliquez sur **Appliquer**.</span><span class="sxs-lookup"><span data-stu-id="4915d-327">Under **Date**, choose a range, and then click **Apply**.</span></span> <span data-ttu-id="4915d-328">Les données des filtres actuels sont exportées vers un fichier .csv.</span><span class="sxs-lookup"><span data-stu-id="4915d-328">Data for the current filters will be exported to a .csv file.</span></span>

<span data-ttu-id="4915d-329">Chaque fichier .csv exporté est limité à 150 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="4915d-329">Each exported .csv file is limited to 150,000 rows.</span></span> <span data-ttu-id="4915d-330">Si les données contiennent plus de 150 000 lignes, plusieurs fichiers .csv seront créés.</span><span class="sxs-lookup"><span data-stu-id="4915d-330">If the data contains more than 150,000 rows, then multiple .csv files will be created.</span></span>

 ![<span data-ttu-id="4915d-331">Affichage en entonnoir dans le rapport d’état du flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="4915d-331">Funnel view in the Mailflow status report</span></span> ](../../media/mail-flow-status-report-funnel-view.png)

### <a name="tech-view-for-the-mailflow-status-report"></a><span data-ttu-id="4915d-332">Affichage technique pour le rapport d’état du flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="4915d-332">Tech view for the Mailflow status report</span></span>

<span data-ttu-id="4915d-333">La **vue Tech est** similaire à la vue Entonnoir, fournissant des détails plus détaillés pour les fonctionnalités de protection contre les menaces configurées. </span><span class="sxs-lookup"><span data-stu-id="4915d-333">The **Tech view** is similar to the **Funnel** view, providing more granular details for the configured threat protections features.</span></span> <span data-ttu-id="4915d-334">À partir du graphique, vous pouvez voir comment les messages sont classés aux différentes étapes de la protection contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="4915d-334">From the chart, you can see how messages are categorized at the different stages of threat protection.</span></span>

<span data-ttu-id="4915d-335">Si vous cliquez sur **l’onglet Affichage** Technique, par défaut, cet affichage contient un graphique et une table de données configurés avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="4915d-335">If you click the **Tech view** tab, by default, this view contains a chart and a data table that's configured with the following filters:</span></span>

- <span data-ttu-id="4915d-336">**Date**: 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="4915d-336">**Date**: The last 7 days.</span></span>

- <span data-ttu-id="4915d-337">**Direction**:</span><span class="sxs-lookup"><span data-stu-id="4915d-337">**Direction**:</span></span>

  - <span data-ttu-id="4915d-338">**Entrant**</span><span class="sxs-lookup"><span data-stu-id="4915d-338">**Inbound**</span></span>
  - <span data-ttu-id="4915d-339">**Sortant**</span><span class="sxs-lookup"><span data-stu-id="4915d-339">**Outbound**</span></span>
  - <span data-ttu-id="4915d-340">**Intra-organisation**: ce nombre est pour les messages au sein d’un client, c’est-à-dire</span><span class="sxs-lookup"><span data-stu-id="4915d-340">**Intra-org**: this count is for messages within a tenant i.e</span></span> <span data-ttu-id="4915d-341">sender abc@domain.com sends to recipient xyz@domain.com (counted separately from Inbound and Outbound)</span><span class="sxs-lookup"><span data-stu-id="4915d-341">sender abc@domain.com sends to recipient xyz@domain.com (counted separately from Inbound and Outbound)</span></span>

<span data-ttu-id="4915d-342">L’affichage agrégé et l’affichage de table de données autorisent 90 jours de filtrage.</span><span class="sxs-lookup"><span data-stu-id="4915d-342">The aggregate view and data table view allow for 90 days of filtering.</span></span>

<span data-ttu-id="4915d-343">Si vous cliquez **sur Filtre,** vous pouvez filtrer le graphique et la table de données.</span><span class="sxs-lookup"><span data-stu-id="4915d-343">If you click **Filter**, you can filter both the chart and the data table.</span></span>

<span data-ttu-id="4915d-344">Ce graphique présente les messages organisés dans les catégories suivantes :</span><span class="sxs-lookup"><span data-stu-id="4915d-344">This chart shows messages organized into the following categories:</span></span>

- <span data-ttu-id="4915d-345">**Nombre total de messages électroniques**</span><span class="sxs-lookup"><span data-stu-id="4915d-345">**Total email**</span></span>
- <span data-ttu-id="4915d-346">**Edge autoriser** et **edge filtré**</span><span class="sxs-lookup"><span data-stu-id="4915d-346">**Edge allow** and **Edge filtered**</span></span>
- <span data-ttu-id="4915d-347">**Pas de programmes** **malveillants, de détection de pièces jointes fiables,** de détection de moteur <sup>\*</sup> **anti-programme** malveillant et de **messages de règle**</span><span class="sxs-lookup"><span data-stu-id="4915d-347">**Not malware**, **Safe Attachments detection**<sup>\*</sup>, **Anti-malware engine detection**, and **Rule messages**</span></span>
- <span data-ttu-id="4915d-348">**Pas de hameçonnage,**  **d’échec DMARC,** de détection d’emprunt d’identité, de détection d’usurpation **d’identité** et de **détection d’hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="4915d-348">**Not phish**, **DMARC failure**, **Impersonation detection**, **Spoof detection**, and **Phish detection**</span></span>
- <span data-ttu-id="4915d-349">**Aucune détection avec détection de détonation d’URL** et **de détonation d’URL**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="4915d-349">**No detection with URL detonation** and **URL detonation detection**<sup>\*</sup></span></span>
- <span data-ttu-id="4915d-350">**Pas de courrier indésirable** et  **de courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="4915d-350">**Not spam** and  **Spam**</span></span>
- <span data-ttu-id="4915d-351">**Courrier non malveillant,** **détection de liens fiables** <sup>\*</sup> et **ZAP**</span><span class="sxs-lookup"><span data-stu-id="4915d-351">**Non-malicious email**, **Safe Links detection**<sup>\*</sup>, and **ZAP**</span></span>

<span data-ttu-id="4915d-352"><sup>\*</sup> Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="4915d-352"><sup>\*</sup> Defender for Office 365</span></span>

<span data-ttu-id="4915d-353">Lorsque vous pointez sur une catégorie dans le graphique, vous pouvez voir le nombre de messages dans cette catégorie.</span><span class="sxs-lookup"><span data-stu-id="4915d-353">When you hover over a category in the chart, you can see the number of messages in that category.</span></span>

<span data-ttu-id="4915d-354">La table de données contient les informations suivantes, indiquées dans l’ordre décroit de date :</span><span class="sxs-lookup"><span data-stu-id="4915d-354">The data table contains the following information, shown in descending date order:</span></span>

- <span data-ttu-id="4915d-355">**Date**</span><span class="sxs-lookup"><span data-stu-id="4915d-355">**Date**</span></span>
- <span data-ttu-id="4915d-356">**Nombre total de messages électroniques**</span><span class="sxs-lookup"><span data-stu-id="4915d-356">**Total email**</span></span>
- <span data-ttu-id="4915d-357">**Edge filtré**</span><span class="sxs-lookup"><span data-stu-id="4915d-357">**Edge filtered**</span></span>
- <span data-ttu-id="4915d-358">**Moteur anti-programme malveillant, pièces jointes sécurisées, règle filtrée**:</span><span class="sxs-lookup"><span data-stu-id="4915d-358">**Anti-malware engine, Safe Attachments, rule filtered**:</span></span>
  - <span data-ttu-id="4915d-359">**Règle filtrée**: messages filtrés en raison de règles de flux de messagerie (également appelées règles de transport).</span><span class="sxs-lookup"><span data-stu-id="4915d-359">**Rule filtered**: Messages filtered due to  mail flow rules (also known as transport rules).</span></span>
- <span data-ttu-id="4915d-360">**DMARC, emprunt d’identité, usurpation d’identité, hameçonnage filtré**:</span><span class="sxs-lookup"><span data-stu-id="4915d-360">**DMARC, impersonation, spoof, phish filtered**:</span></span>
  - <span data-ttu-id="4915d-361">**DMARC**: messages filtrés en raison de l’échec de la vérification de l’authentification DMARC.</span><span class="sxs-lookup"><span data-stu-id="4915d-361">**DMARC**: Messages filtered due to the message failing its DMARC authentication check.</span></span>
- <span data-ttu-id="4915d-362">**Détection de détonation d’URL**</span><span class="sxs-lookup"><span data-stu-id="4915d-362">**URL detonation detection**</span></span>
- <span data-ttu-id="4915d-363">**Filtrage anti-courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="4915d-363">**Anti-spam filtered**</span></span>
- <span data-ttu-id="4915d-364">**ZAP supprimé**</span><span class="sxs-lookup"><span data-stu-id="4915d-364">**ZAP removed**</span></span>
- <span data-ttu-id="4915d-365">**Détection par liens fiables**</span><span class="sxs-lookup"><span data-stu-id="4915d-365">**Detection by Safe Links**</span></span>

<span data-ttu-id="4915d-366">Si vous sélectionnez une ligne dans la table de données, une répartition supplémentaire du nombre de messages électroniques est affichée dans le volant.</span><span class="sxs-lookup"><span data-stu-id="4915d-366">If you select a row in the data table, a further breakdown of the email counts are shown in the flyout.</span></span>

<span data-ttu-id="4915d-367">**Exporter**:</span><span class="sxs-lookup"><span data-stu-id="4915d-367">**Export**:</span></span>

<span data-ttu-id="4915d-368">En cliquant **sur Exporter,** sous **Options,** vous pouvez sélectionner l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="4915d-368">On clicking **Export**, under **Options** you can select one of the following values:</span></span>

- <span data-ttu-id="4915d-369">**Résumé (avec des données pour les 90 derniers jours au maximum)**</span><span class="sxs-lookup"><span data-stu-id="4915d-369">**Summary (with data for last 90 days at most)**</span></span>
- <span data-ttu-id="4915d-370">**Détails (avec des données pour les 30 derniers jours au maximum)**</span><span class="sxs-lookup"><span data-stu-id="4915d-370">**Details (with data for last 30 days at most)**</span></span>

<span data-ttu-id="4915d-371">Sous **Date**, choisissez une plage, puis cliquez sur **Appliquer**.</span><span class="sxs-lookup"><span data-stu-id="4915d-371">Under **Date**, choose a range, and then click **Apply**.</span></span> <span data-ttu-id="4915d-372">Les données des filtres actuels sont exportées vers un fichier .csv.</span><span class="sxs-lookup"><span data-stu-id="4915d-372">Data for the current filters will be exported to a .csv file.</span></span>

<span data-ttu-id="4915d-373">Chaque fichier .csv exporté est limité à 150 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="4915d-373">Each exported .csv file is limited to 150,000 rows.</span></span> <span data-ttu-id="4915d-374">Si les données contiennent plus de 150 000 lignes, plusieurs fichiers .csv seront créés.</span><span class="sxs-lookup"><span data-stu-id="4915d-374">If the data contains more than 150,000 rows, then multiple .csv files will be created.</span></span>

 ![<span data-ttu-id="4915d-375">Affichage technique dans le rapport d’état du flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="4915d-375">Tech view in the Mailflow status report</span></span> ](../../media/mail-flow-status-report-Tech-view.png)

## <a name="sent-and-received-email-report"></a><span data-ttu-id="4915d-376">Rapport de courrier électronique envoyé et reçu</span><span class="sxs-lookup"><span data-stu-id="4915d-376">Sent and received email report</span></span>

<span data-ttu-id="4915d-377">Le **rapport de** courrier électronique envoyé et reçu est un rapport intelligent qui affiche des informations sur le courrier électronique entrant et sortant, y compris les détections de courrier indésirable, les programmes malveillants et les messages électroniques identifiés comme « bons ».</span><span class="sxs-lookup"><span data-stu-id="4915d-377">The **Sent and received email** report is a smart report that shows information about incoming and outgoing email, including spam detections, malware, and email identified as "good."</span></span> <span data-ttu-id="4915d-378">La différence entre ce [](#mailflow-status-report) rapport et le rapport d’état du flux de messagerie est la suivante : ce rapport n’inclut pas de données sur les messages bloqués par la protection Edge. Il est important de comprendre que si un message est envoyé à cinq destinataires, nous le compterons comme un seul message.</span><span class="sxs-lookup"><span data-stu-id="4915d-378">The difference between this report and the [Mailflow status report](#mailflow-status-report) is: this report doesn't include data about messages blocked by edge protection.It's important to understand that if a message is sent to five recipients we count it as one message.</span></span>

<span data-ttu-id="4915d-379">L’affichage agrégé et l’affichage détaillé du rapport autorisent 90 jours de filtrage.</span><span class="sxs-lookup"><span data-stu-id="4915d-379">The aggregate view and the detail view of the report allow for 90 days of filtering.</span></span>

<span data-ttu-id="4915d-380">Pour afficher le rapport, ouvrez le Centre de  sécurité [& conformité,](https://protection.office.com)allez au tableau de bord rapports et sélectionnez \>  Courrier électronique envoyé **et reçu.**</span><span class="sxs-lookup"><span data-stu-id="4915d-380">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Sent and received email**.</span></span> <span data-ttu-id="4915d-381">Pour aller directement dans le rapport, ouvrez <https://protection.office.com/reportv2?id=SentAndReceivedMailATP> .</span><span class="sxs-lookup"><span data-stu-id="4915d-381">To go directly to the report, open <https://protection.office.com/reportv2?id=SentAndReceivedMailATP>.</span></span>

![Widget de courrier électronique envoyé et reçu dans le tableau de bord Rapports](../../media/sent-and-received-email-report-widget.png)

### <a name="report-view-for-the-sent-and-received-email-report"></a><span data-ttu-id="4915d-383">Affichage du rapport pour le rapport de courrier électronique envoyé et reçu</span><span class="sxs-lookup"><span data-stu-id="4915d-383">Report view for the Sent and received email report</span></span>

<span data-ttu-id="4915d-384">Les graphiques suivants sont disponibles dans l’affichage de rapport :</span><span class="sxs-lookup"><span data-stu-id="4915d-384">The following charts are available in the report view:</span></span>

- <span data-ttu-id="4915d-385">**Décomposez par : Type**: le graphique affiche toutes les catégories disponibles :</span><span class="sxs-lookup"><span data-stu-id="4915d-385">**Break down by: Type**: The chart shows all available categories:</span></span>

  - <span data-ttu-id="4915d-386">**Total**</span><span class="sxs-lookup"><span data-stu-id="4915d-386">**Total**</span></span>
  - <span data-ttu-id="4915d-387">**Bon courrier**</span><span class="sxs-lookup"><span data-stu-id="4915d-387">**Good mail**</span></span>
  - <span data-ttu-id="4915d-388">**Programmes malveillants (anti-programme malveillant)** (EOP)</span><span class="sxs-lookup"><span data-stu-id="4915d-388">**Malware (anti-malware)** (EOP)</span></span>
  - <span data-ttu-id="4915d-389">**Détections de courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="4915d-389">**Spam detections**</span></span>
  - <span data-ttu-id="4915d-390">**Messages de règle**</span><span class="sxs-lookup"><span data-stu-id="4915d-390">**Rule messages**</span></span>
  - <span data-ttu-id="4915d-391">**Programmes malveillants** avancés (Microsoft Defender pour Office 365)</span><span class="sxs-lookup"><span data-stu-id="4915d-391">**Advanced malware** (Microsoft Defender for Office 365)</span></span>

  <span data-ttu-id="4915d-392">Lorsque vous pointez sur un jour (point de données) dans le graphique, vous pouvez voir les détails de ce jour.</span><span class="sxs-lookup"><span data-stu-id="4915d-392">When you hover over a day (data point) in the chart, you can see details for that day.</span></span>

  ![Affichage des types dans le rapport de courrier électronique envoyé et reçu](../../media/sent-and-received-email-report-type-view.png)

- <span data-ttu-id="4915d-394">**Décomposer par : Direction**: le graphique affiche **le total,** le trafic **entrant** et les **données sortantes.**</span><span class="sxs-lookup"><span data-stu-id="4915d-394">**Break down by: Direction**: The chart shows **Total**, **Inbound**, and **Outbound** data.</span></span> <span data-ttu-id="4915d-395">Lorsque vous pointez sur un jour (point de données) dans le graphique, vous pouvez voir les détails de ce jour.</span><span class="sxs-lookup"><span data-stu-id="4915d-395">When you hover over a day (data point) in the chart, you can see details for that day.</span></span>

  ![Affichage de direction dans le rapport de courrier électronique envoyé et reçu](../../media/sent-and-received-email-report-direction-view.png)

- <span data-ttu-id="4915d-397">**Descendre** \> **Programmes malveillants (anti-programme malveillant)**: cette sélection vous permet d’en savoir plus sur les détections de programmes [malveillants dans le rapport de courrier électronique.](view-email-security-reports.md#malware-detections-in-email-report)</span><span class="sxs-lookup"><span data-stu-id="4915d-397">**Drill down by** \> **Malware (anti-malware)**: This selection takes you to the [Malware detections in email report](view-email-security-reports.md#malware-detections-in-email-report).</span></span>

- <span data-ttu-id="4915d-398">**Descendre** \> **Détections de courrier indésirable)**: cette sélection vous permet d’envoyer le rapport [détections de courrier indésirable.](view-email-security-reports.md#spam-detections-report)</span><span class="sxs-lookup"><span data-stu-id="4915d-398">**Drill down by** \> **Spam detections)**: This selection takes you to the [Spam Detections report](view-email-security-reports.md#spam-detections-report).</span></span>

<span data-ttu-id="4915d-399">Si vous cliquez sur **Filtres** dans un affichage de rapport, vous pouvez modifier les résultats avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="4915d-399">If you click **Filters** in a report view, you can modify the results with the following filters:</span></span>

- <span data-ttu-id="4915d-400">**Date de début** et **date de fin**</span><span class="sxs-lookup"><span data-stu-id="4915d-400">**Start date** and **End date**</span></span>
- <span data-ttu-id="4915d-401">Valeurs de direction</span><span class="sxs-lookup"><span data-stu-id="4915d-401">Direction values</span></span>
- <span data-ttu-id="4915d-402">Valeurs de type</span><span class="sxs-lookup"><span data-stu-id="4915d-402">Type values</span></span>

<span data-ttu-id="4915d-403">Pour revenir à l’affichage du rapport, cliquez **sur Afficher le rapport.**</span><span class="sxs-lookup"><span data-stu-id="4915d-403">To go back to the report view, click **View report**.</span></span>

### <a name="details-table-view-for-the-sent-and-received-email-report"></a><span data-ttu-id="4915d-404">Affichage du tableau détails pour le rapport de courrier électronique envoyé et reçu</span><span class="sxs-lookup"><span data-stu-id="4915d-404">Details table view for the Sent and received email report</span></span>

<span data-ttu-id="4915d-405">Si vous cliquez **sur Afficher les détails dans** le tableau Décomposer par : **Direction** ou Descendre en mode **Direction,** les informations suivantes sont affichées :</span><span class="sxs-lookup"><span data-stu-id="4915d-405">If you click **View details table** in the **Break down by: Direction** or **Break down by: Direction** view, the following information is shown:</span></span>

- <span data-ttu-id="4915d-406">**Date (UTC)**</span><span class="sxs-lookup"><span data-stu-id="4915d-406">**Date (UTC)**</span></span>
- <span data-ttu-id="4915d-407">**Type**</span><span class="sxs-lookup"><span data-stu-id="4915d-407">**Type**</span></span>
- <span data-ttu-id="4915d-408">**Direction**</span><span class="sxs-lookup"><span data-stu-id="4915d-408">**Direction**</span></span>
- <span data-ttu-id="4915d-409">**Nombre de messages**</span><span class="sxs-lookup"><span data-stu-id="4915d-409">**Message count**</span></span>

<span data-ttu-id="4915d-410">Si vous cliquez **sur Filtres** dans une vue de tableau de détails, vous pouvez modifier les résultats avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="4915d-410">If you click **Filters** in a details table view, you can modify the results with the following filters:</span></span>

- <span data-ttu-id="4915d-411">**Date de début** et **date de fin**</span><span class="sxs-lookup"><span data-stu-id="4915d-411">**Start date** and **End date**</span></span>
- <span data-ttu-id="4915d-412">Valeurs de direction</span><span class="sxs-lookup"><span data-stu-id="4915d-412">Direction values</span></span>
- <span data-ttu-id="4915d-413">Valeurs de type</span><span class="sxs-lookup"><span data-stu-id="4915d-413">Type values</span></span>

<span data-ttu-id="4915d-414">Pour revenir à l’affichage du rapport, cliquez **sur Afficher le rapport.**</span><span class="sxs-lookup"><span data-stu-id="4915d-414">To go back to the report view, click **View report**.</span></span>

## <a name="top-senders-and-recipients-report"></a><span data-ttu-id="4915d-415">Rapport des principaux expéditeurs et destinataires</span><span class="sxs-lookup"><span data-stu-id="4915d-415">Top senders and recipients report</span></span>

<span data-ttu-id="4915d-416">Le **rapport Des principaux expéditeurs et destinataires** est un graphique en secteurs montrant vos principaux expéditeurs et destinataires de courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="4915d-416">The **Top senders and recipients** report is a pie chart showing your top email senders and recipients.</span></span>

<span data-ttu-id="4915d-417">Pour afficher le rapport, ouvrez le Centre de  sécurité [& conformité,](https://protection.office.com)puis sélectionnez Tableau de bord des rapports et sélectionnez Principaux \>  **expéditeurs et destinataires.**</span><span class="sxs-lookup"><span data-stu-id="4915d-417">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Top senders and recipients**.</span></span> <span data-ttu-id="4915d-418">Pour aller directement dans le rapport, ouvrez <https://protection.office.com/reportv2?id=TopSenderRecipientsATP> .</span><span class="sxs-lookup"><span data-stu-id="4915d-418">To go directly to the report, open <https://protection.office.com/reportv2?id=TopSenderRecipientsATP>.</span></span>

![Widget des principaux expéditeurs et destinataires dans le tableau de bord Rapports](../../media/top-senders-and-recipients-widget.png)

### <a name="report-view-for-the-top-senders-and-recipient-report"></a><span data-ttu-id="4915d-420">Affichage du rapport pour le rapport des principaux expéditeurs et destinataires</span><span class="sxs-lookup"><span data-stu-id="4915d-420">Report view for the Top senders and recipient report</span></span>

<span data-ttu-id="4915d-421">Les graphiques suivants sont disponibles dans l’affichage de rapport :</span><span class="sxs-lookup"><span data-stu-id="4915d-421">The following charts are available in the report view:</span></span>

- <span data-ttu-id="4915d-422">**Afficher les données pour \> les principaux expéditeurs de courrier**</span><span class="sxs-lookup"><span data-stu-id="4915d-422">**Show data for \> Top mail senders**</span></span>
- <span data-ttu-id="4915d-423">**Afficher les données pour \> les principaux destinataires du courrier**</span><span class="sxs-lookup"><span data-stu-id="4915d-423">**Show data for \> Top mail recipients**</span></span>
- <span data-ttu-id="4915d-424">**Afficher les données des \> principaux destinataires du courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="4915d-424">**Show data for \> Top spam recipients**</span></span>
- <span data-ttu-id="4915d-425">**Afficher les données pour \> Principaux destinataires de programmes malveillants** (EOP)</span><span class="sxs-lookup"><span data-stu-id="4915d-425">**Show data for \> Top malware recipients** (EOP)</span></span>
- <span data-ttu-id="4915d-426">**Afficher les données \> des principaux destinataires de programmes malveillants (Defender pour Office 365)**</span><span class="sxs-lookup"><span data-stu-id="4915d-426">**Show data for \> Top malware recipients (Defender for Office 365)**</span></span>

<span data-ttu-id="4915d-427">La composition du graphique en secteurs change en fonction de ces sélections.</span><span class="sxs-lookup"><span data-stu-id="4915d-427">The composition of the pie chart changes based on these selections.</span></span>

<span data-ttu-id="4915d-428">Lorsque vous pointez sur une souris dans le graphique en secteurs, vous pouvez voir le nombre de messages envoyés ou reçus.</span><span class="sxs-lookup"><span data-stu-id="4915d-428">When you hover over a wedge in the pie chart, you can see a count of messages sent or received.</span></span>

<span data-ttu-id="4915d-429">Si vous cliquez sur **Filtres** dans un affichage de rapport, vous pouvez spécifier une plage de dates avec la **date** de début et la **date de fin.**</span><span class="sxs-lookup"><span data-stu-id="4915d-429">If you click **Filters** in a report view, you can specify a date range with **Start date** and **End date**.</span></span>

![Graphique en secteurs en affichage Rapport dans le rapport Des principaux expéditeurs et destinataires](../../media/top-senders-and-recipients-report-view.png)

### <a name="details-table-view-for-the-top-senders-and-recipient-report"></a><span data-ttu-id="4915d-431">Vue de table Détails pour le rapport des principaux expéditeurs et destinataires</span><span class="sxs-lookup"><span data-stu-id="4915d-431">Details table view for the Top senders and recipient report</span></span>

<span data-ttu-id="4915d-432">Si vous cliquez sur Afficher le tableau des **détails,** les informations affichées dépendent du graphique que vous regardiez :</span><span class="sxs-lookup"><span data-stu-id="4915d-432">If you click **View details table**, the information that's shown depends on the chart you were looking at:</span></span>

- <span data-ttu-id="4915d-433">**Afficher les données pour \> les principaux expéditeurs de courrier**</span><span class="sxs-lookup"><span data-stu-id="4915d-433">**Show data for \> Top mail senders**</span></span>

  - <span data-ttu-id="4915d-434">**Principaux expéditeurs de courrier**</span><span class="sxs-lookup"><span data-stu-id="4915d-434">**Top mail senders**</span></span>
  - <span data-ttu-id="4915d-435">**Count**</span><span class="sxs-lookup"><span data-stu-id="4915d-435">**Count**</span></span>

- <span data-ttu-id="4915d-436">**Afficher les données pour \> les principaux destinataires du courrier**</span><span class="sxs-lookup"><span data-stu-id="4915d-436">**Show data for \> Top mail recipients**</span></span>

  - <span data-ttu-id="4915d-437">**Principaux destinataires du courrier**</span><span class="sxs-lookup"><span data-stu-id="4915d-437">**Top mail recipients**</span></span>
  - <span data-ttu-id="4915d-438">**Count**</span><span class="sxs-lookup"><span data-stu-id="4915d-438">**Count**</span></span>

- <span data-ttu-id="4915d-439">**Afficher les données des \> principaux destinataires du courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="4915d-439">**Show data for \> Top spam recipients**</span></span>

  - <span data-ttu-id="4915d-440">**Principaux destinataires du courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="4915d-440">**Top spam recipients**</span></span>
  - <span data-ttu-id="4915d-441">**Count**</span><span class="sxs-lookup"><span data-stu-id="4915d-441">**Count**</span></span>

- <span data-ttu-id="4915d-442">**Afficher les données pour \> Principaux destinataires de programmes malveillants** (EOP)</span><span class="sxs-lookup"><span data-stu-id="4915d-442">**Show data for \> Top malware recipients** (EOP)</span></span>

  - <span data-ttu-id="4915d-443">**Principaux destinataires de programmes malveillants**</span><span class="sxs-lookup"><span data-stu-id="4915d-443">**Top malware recipients**</span></span>
  - <span data-ttu-id="4915d-444">**Count**</span><span class="sxs-lookup"><span data-stu-id="4915d-444">**Count**</span></span>

- <span data-ttu-id="4915d-445">**Afficher les données \> des principaux destinataires de programmes malveillants (Defender pour Office 365)**</span><span class="sxs-lookup"><span data-stu-id="4915d-445">**Show data for \> Top malware recipients (Defender for Office 365)**</span></span>

  - <span data-ttu-id="4915d-446">**Principaux destinataires des programmes malveillants (Defender pour Office 365)**</span><span class="sxs-lookup"><span data-stu-id="4915d-446">**Top malware recipients (Defender for Office 365)**</span></span>
  - <span data-ttu-id="4915d-447">**Count**</span><span class="sxs-lookup"><span data-stu-id="4915d-447">**Count**</span></span>

<span data-ttu-id="4915d-448">Si vous cliquez sur **Filtres** dans une vue de tableau de détails, vous pouvez spécifier une plage de dates avec la **date** de début et la **date de fin.**</span><span class="sxs-lookup"><span data-stu-id="4915d-448">If you click **Filters** in a details table view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="4915d-449">Pour revenir à l’affichage du rapport, cliquez **sur Afficher le rapport.**</span><span class="sxs-lookup"><span data-stu-id="4915d-449">To go back to the report view, click **View report**.</span></span>

## <a name="what-permissions-are-needed-to-view-these-reports"></a><span data-ttu-id="4915d-450">Quelles autorisations sont nécessaires pour afficher ces rapports ?</span><span class="sxs-lookup"><span data-stu-id="4915d-450">What permissions are needed to view these reports?</span></span>

<span data-ttu-id="4915d-451">Pour afficher et utiliser les rapports décrits dans cet article, vous devez être membre de l’un des groupes de rôles suivants dans le Centre de sécurité & conformité :</span><span class="sxs-lookup"><span data-stu-id="4915d-451">In order to view and use the reports described in this article, you need to be a member of one of the following role groups in the Security & Compliance Center:</span></span>

- <span data-ttu-id="4915d-452">**Gestion de l'organisation**</span><span class="sxs-lookup"><span data-stu-id="4915d-452">**Organization Management**</span></span>
- <span data-ttu-id="4915d-453">**Administrateur de la sécurité**</span><span class="sxs-lookup"><span data-stu-id="4915d-453">**Security Administrator**</span></span>
- <span data-ttu-id="4915d-454">**Lecteur sécurité**</span><span class="sxs-lookup"><span data-stu-id="4915d-454">**Security Reader**</span></span>
- <span data-ttu-id="4915d-455">**Lecteur général**</span><span class="sxs-lookup"><span data-stu-id="4915d-455">**Global Reader**</span></span>

<span data-ttu-id="4915d-456">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="4915d-456">For more information, see [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

> [!NOTE]
> <span data-ttu-id="4915d-457">L’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux utilisateurs les autorisations requises dans le centre de sécurité et de conformité _et_ les autorisations pour les autres fonctionnalités de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4915d-457">Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions in the Security & Compliance Center _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="4915d-458">Pour plus d’informations, consultez [À propos des rôles d’administrateur](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles).</span><span class="sxs-lookup"><span data-stu-id="4915d-458">For more information, see [About admin roles](https://docs.microsoft.com/microsoft-365/admin/add-users/about-admin-roles).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4915d-459">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4915d-459">Related topics</span></span>

[<span data-ttu-id="4915d-460">Rapports intelligents et aperçus dans le Centre de sécurité et conformité</span><span class="sxs-lookup"><span data-stu-id="4915d-460">Smart reports and insights in the Security & Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)

[<span data-ttu-id="4915d-461">Informations sur le flux de messagerie dans le centre de sécurité et conformité</span><span class="sxs-lookup"><span data-stu-id="4915d-461">Mail flow insights in the Security & Compliance Center</span></span>](mail-flow-insights-v2.md)

[<span data-ttu-id="4915d-462">Afficher les rapports de sécurité de courrier dans le centre de sécurité et conformité</span><span class="sxs-lookup"><span data-stu-id="4915d-462">View email security reports in the Security & Compliance Center</span></span>](view-email-security-reports.md)

[<span data-ttu-id="4915d-463">Afficher des rapports pour Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="4915d-463">View reports for Microsoft Defender for Office 365</span></span>](view-reports-for-atp.md)
