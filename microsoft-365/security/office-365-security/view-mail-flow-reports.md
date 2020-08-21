---
title: Afficher les rapports de flux de messagerie dans le tableau de bord rapports
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: how-to
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: ''
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent en savoir plus sur les rapports de flux de messagerie disponibles dans le tableau de bord des rapports dans le centre de sécurité & conformité.
ms.custom: ''
ms.openlocfilehash: 9e9249eab5d3519dac0e33acf40d600d471b7cb2
ms.sourcegitcommit: e12fa502bc216f6083ef5666f693a04bb727d4df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "46826456"
---
# <a name="view-mail-flow-reports-in-the-reports-dashboard-in-security--compliance-center"></a><span data-ttu-id="f8753-103">Afficher les rapports de flux de messagerie dans le tableau de bord rapports du centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="f8753-103">View mail flow reports in the Reports dashboard in Security & Compliance Center</span></span>

<span data-ttu-id="f8753-104">En plus des rapports de flux de messagerie disponibles dans le [tableau de bord de flux de messagerie](mail-flow-insights-v2.md) dans le centre de sécurité & conformité, un grand nombre de rapports de flux de messagerie supplémentaires sont disponibles dans le tableau de bord rapports pour vous aider à surveiller votre organisation Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f8753-104">In addition to the mail flow reports that are available in the [Mail flow dashboard](mail-flow-insights-v2.md) in the Security & Compliance Center, a variety of additional mail flow reports are available in the Reports dashboard to help you monitor your Microsoft 365 organization.</span></span>

<span data-ttu-id="f8753-105">Si vous disposez des [autorisations nécessaires](#what-permissions-are-needed-to-view-these-reports), vous pouvez afficher ces rapports dans le [Centre de sécurité & conformité](https://office.protection.com) en accédant au tableau de **Reports** \> **bord**rapports.</span><span class="sxs-lookup"><span data-stu-id="f8753-105">If you have the [necessary permissions](#what-permissions-are-needed-to-view-these-reports), you can view these reports in the [Security & Compliance Center](https://office.protection.com) by going to **Reports** \> **Dashboard**.</span></span> <span data-ttu-id="f8753-106">Pour accéder directement au tableau de bord rapports, ouvrez <https://office.protection.office.com/insightdashboard> .</span><span class="sxs-lookup"><span data-stu-id="f8753-106">To go directly to the Reports dashboard, open <https://office.protection.office.com/insightdashboard>.</span></span>

![Tableau de bord des rapports dans le centre de sécurité & conformité](../../media/6b213d34-adbb-44af-8549-be9a7e2db087.png)

## <a name="connector-report"></a><span data-ttu-id="f8753-108">Rapport de connecteur</span><span class="sxs-lookup"><span data-stu-id="f8753-108">Connector report</span></span>

<span data-ttu-id="f8753-109">Le **rapport de connecteur** affiche l’activité de flux de messagerie sur les connecteurs entrants [et sortants](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow) configurés pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f8753-109">The **Connector report** shows mail flow activity on the [inbound and outbound connectors](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow) that are configured for your organization.</span></span>

<span data-ttu-id="f8753-110">Pour afficher le rapport, ouvrez le [Centre de sécurité & conformité](https://protection.office.com), accédez **Reports** au \> **tableau de bord** rapports et sélectionnez rapport de **connecteur**.</span><span class="sxs-lookup"><span data-stu-id="f8753-110">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Connector report**.</span></span> <span data-ttu-id="f8753-111">Pour accéder directement au rapport, ouvrez <https://protection.office.com/reportv2?id=ConnectorReport> .</span><span class="sxs-lookup"><span data-stu-id="f8753-111">To go directly to the report, open <https://protection.office.com/reportv2?id=ConnectorReport>.</span></span>

![Widget rapport de connecteur dans le tableau de bord rapports](../../media/connector-report-widget.png)

### <a name="report-view-for-the-connector-report"></a><span data-ttu-id="f8753-113">Affichage de rapport pour le rapport de connecteur</span><span class="sxs-lookup"><span data-stu-id="f8753-113">Report view for the Connector report</span></span>

<span data-ttu-id="f8753-114">Les graphiques suivants sont disponibles en mode état :</span><span class="sxs-lookup"><span data-stu-id="f8753-114">The following charts are available in report view:</span></span>

- <span data-ttu-id="f8753-115">**Afficher les données par : flux de messagerie**: ce graphique indique le nombre de messages entrants et sortants organisés par :</span><span class="sxs-lookup"><span data-stu-id="f8753-115">**View data by: Mail flow**: This chart shows the number of inbound and outbound messages organized by:</span></span>

  - <span data-ttu-id="f8753-116">**Total**</span><span class="sxs-lookup"><span data-stu-id="f8753-116">**Total**</span></span>
  - <span data-ttu-id="f8753-117">**À partir d’Internet sans connecteur**</span><span class="sxs-lookup"><span data-stu-id="f8753-117">**From the internet without a connector**</span></span>
  - <span data-ttu-id="f8753-118">**Sur Internet sans connecteur**</span><span class="sxs-lookup"><span data-stu-id="f8753-118">**To the internet without a connector**</span></span>
  - <span data-ttu-id="f8753-119">Un connecteur spécifique que vous avez configuré.</span><span class="sxs-lookup"><span data-stu-id="f8753-119">A specific connector that you've configured.</span></span>

  <span data-ttu-id="f8753-120">Pour isoler les données du graphique, utilisez l’option **afficher les données pour** le contrôle pour sélectionner une de ces options ou **tout le flux de messagerie**.</span><span class="sxs-lookup"><span data-stu-id="f8753-120">To isolate the data in the chart, use the **Show data for** control to select one of these options or **All mail flow**.</span></span>

  ![Afficher les données par flux de messagerie dans le rapport du connecteur](../../media/connector-report-view-data-by-mail-flow.png)

- <span data-ttu-id="f8753-122">**Afficher les données par : utilisation de TLS**: ce graphique indique le pourcentage d’utilisation de la version TLS (Transport Layer Security) pour le flux de messagerie.</span><span class="sxs-lookup"><span data-stu-id="f8753-122">**View data by: TLS usage**: This chart shows the percentage of Transport Layer Security (TLS) version usage for mail flow.</span></span>

  <span data-ttu-id="f8753-123">Pour isoler les données dans le graphique, utilisez l’option **afficher les données pour** le contrôle afin de sélectionner l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="f8753-123">To isolate the data in the chart, use the **Show data for** control to select one of the following options:</span></span>

  - <span data-ttu-id="f8753-124">**Tout le flux de messagerie**</span><span class="sxs-lookup"><span data-stu-id="f8753-124">**All mail flow**</span></span>
  - <span data-ttu-id="f8753-125">**À partir d’Internet sans connecteur**</span><span class="sxs-lookup"><span data-stu-id="f8753-125">**From the internet without a connector**</span></span>
  - <span data-ttu-id="f8753-126">**Sur Internet sans connecteur**</span><span class="sxs-lookup"><span data-stu-id="f8753-126">**To the internet without a connector**</span></span>
  - <span data-ttu-id="f8753-127">Un connecteur spécifique que vous avez configuré.</span><span class="sxs-lookup"><span data-stu-id="f8753-127">A specific connector that you've configured.</span></span>

  ![Afficher les données par utilisation de TLS dans le rapport de connecteur](../../media/connector-report-view-data-by-tls-usage.png)

<span data-ttu-id="f8753-129">Si vous cliquez sur **filtres** dans un affichage de rapport, vous pouvez spécifier une plage de dates avec **Date de début** et date de **fin**.</span><span class="sxs-lookup"><span data-stu-id="f8753-129">If you click **Filters** in a report view, you can specify a date range with **Start date** and **End date**.</span></span>

### <a name="details-table-view-for-the-connector-report"></a><span data-ttu-id="f8753-130">Vue de la table Détails pour le rapport de connecteur</span><span class="sxs-lookup"><span data-stu-id="f8753-130">Details table view for the Connector report</span></span>

<span data-ttu-id="f8753-131">Si vous cliquez sur **afficher la table des détails** dans un affichage de rapport, les informations suivantes s’affichent :</span><span class="sxs-lookup"><span data-stu-id="f8753-131">If you click **View details table** in a report view, the following information is shown:</span></span>

- <span data-ttu-id="f8753-132">**Date**</span><span class="sxs-lookup"><span data-stu-id="f8753-132">**Date**</span></span>
- <span data-ttu-id="f8753-133">**Nom et direction du connecteur**</span><span class="sxs-lookup"><span data-stu-id="f8753-133">**Connector direction and name**</span></span>
- <span data-ttu-id="f8753-134">**Type de connecteur**</span><span class="sxs-lookup"><span data-stu-id="f8753-134">**Connector type**</span></span>
- <span data-ttu-id="f8753-135">**TLS forcé ?**: valeur **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="f8753-135">**Forced TLS?**: The value **True** or **False**.</span></span>
- <span data-ttu-id="f8753-136">**Pas de TLS** (pourcentage)</span><span class="sxs-lookup"><span data-stu-id="f8753-136">**No TLS** (percentage)</span></span>
- <span data-ttu-id="f8753-137">**TLS 1,0** (pourcentage)</span><span class="sxs-lookup"><span data-stu-id="f8753-137">**TLS 1.0** (percentage)</span></span>
- <span data-ttu-id="f8753-138">**TLS 1,1** (pourcentage)</span><span class="sxs-lookup"><span data-stu-id="f8753-138">**TLS 1.1** (percentage)</span></span>
- <span data-ttu-id="f8753-139">**TLS 1,2** (pourcentage)</span><span class="sxs-lookup"><span data-stu-id="f8753-139">**TLS 1.2** (percentage)</span></span>
- <span data-ttu-id="f8753-140">**Volume**: nombre de messages.</span><span class="sxs-lookup"><span data-stu-id="f8753-140">**Volume**: The number of messages.</span></span>

<span data-ttu-id="f8753-141">Si vous cliquez sur **filtres** dans un affichage tableau détaillé, vous pouvez spécifier une plage de dates avec **Date de début** et date de **fin**.</span><span class="sxs-lookup"><span data-stu-id="f8753-141">If you click **Filters** in a details table view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="f8753-142">Pour revenir à l’affichage de rapport, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="f8753-142">To go back to the report view, click **View report**.</span></span>

## <a name="exchange-transport-rule-report"></a><span data-ttu-id="f8753-143">Rapport de règle de transport Exchange</span><span class="sxs-lookup"><span data-stu-id="f8753-143">Exchange transport rule report</span></span>

<span data-ttu-id="f8753-144">Le rapport des règles de **transport Exchange** affiche l’effet des règles de flux de messagerie (également appelées règles de transport) sur les messages entrants et sortants dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f8753-144">The **Exchange transport rule report** shows the effect of mail flow rules (also known as transport rules) on incoming and outgoing messages in your organization.</span></span>

<span data-ttu-id="f8753-145">Pour afficher le rapport, ouvrez le [Centre de sécurité & conformité](https://protection.office.com), accédez **Reports** au \> **tableau de bord** rapports et sélectionnez **règle de transport Exchange**.</span><span class="sxs-lookup"><span data-stu-id="f8753-145">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Exchange Transport rule**.</span></span> <span data-ttu-id="f8753-146">Pour accéder directement au rapport, ouvrez <https://protection.office.com/reportv2?id=ETRRuleReport> .</span><span class="sxs-lookup"><span data-stu-id="f8753-146">To go directly to the report, open <https://protection.office.com/reportv2?id=ETRRuleReport>.</span></span>

![Widget règle de transport Exchange dans le tableau de bord rapports](../../media/transport-rule-report-widget.png)

### <a name="report-view-for-the-exchange-transport-rule-report"></a><span data-ttu-id="f8753-148">Affichage de rapport pour le rapport des règles de transport Exchange</span><span class="sxs-lookup"><span data-stu-id="f8753-148">Report view for the Exchange transport rule report</span></span>

<span data-ttu-id="f8753-149">Les graphiques suivants sont disponibles en mode état :</span><span class="sxs-lookup"><span data-stu-id="f8753-149">The following charts are available in report view:</span></span>

- <span data-ttu-id="f8753-150">**Afficher les données par : règles** \> de transport Exchange **Décomposer en : sens**: ce graphique indique le **nombre de messages entrants** et **sortants** affectés par les règles de transport.</span><span class="sxs-lookup"><span data-stu-id="f8753-150">**View data by: Exchange transport rules** \> **Break down by: Direction**: This chart shows the number of **Inbound** and **Outbound** messages that were affected by transport rules.</span></span>

- <span data-ttu-id="f8753-151">**Afficher les données par : règles** \> de transport Exchange Dépanner **par : gravité**: ce graphique indique le nombre de messages de gravité **élevée** et de gravité **moyenne**, ainsi que les messages à **faible gravité** .</span><span class="sxs-lookup"><span data-stu-id="f8753-151">**View data by: Exchange transport rules** \> **Break down by: Severity**: This chart shows the number of **High severity** and **Medium severity**, and **Low severity** messages.</span></span> <span data-ttu-id="f8753-152">Vous définissez le niveau de gravité en tant qu’action dans la règle (**auditez cette règle avec le niveau de gravité** ou _SetAuditSeverity_).</span><span class="sxs-lookup"><span data-stu-id="f8753-152">You set the severity level as an action in the rule (**Audit this rule with severity level** or _SetAuditSeverity_).</span></span> <span data-ttu-id="f8753-153">Pour plus d’informations, consultez la rubrique [actions de règle de flux de messagerie dans Exchange Online](https://docs.microsoft.com//Exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions).</span><span class="sxs-lookup"><span data-stu-id="f8753-153">For more information, see [Mail flow rule actions in Exchange Online](https://docs.microsoft.com//Exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions).</span></span>

- <span data-ttu-id="f8753-154">**Afficher les données par : DLP Exchange transport Rules** \> **Décomposer en : sens**: ce graphique indique le **nombre de messages entrants** et **sortants** affectés par les règles de transport de la protection contre la perte de données (DLP).</span><span class="sxs-lookup"><span data-stu-id="f8753-154">**View data by: DLP Exchange transport rules** \> **Break down by: Direction**: This chart shows the number of **Inbound** and **Outbound** messages that were affected by data loss prevention (DLP) transport rules.</span></span> <span data-ttu-id="f8753-155">Vous pouvez affiner le graphique en sélectionnant l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="f8753-155">You can further refine the chart by selecting on of the following options:</span></span>

  - <span data-ttu-id="f8753-156">**Afficher les données pour : toutes les règles de transport DLP**</span><span class="sxs-lookup"><span data-stu-id="f8753-156">**Show data for: All DLP transport rules**</span></span>
  - <span data-ttu-id="f8753-157">**Afficher les données de : utilisateurs compromis**</span><span class="sxs-lookup"><span data-stu-id="f8753-157">**Show data for: Compromised users**</span></span>
  - <span data-ttu-id="f8753-158">**Afficher les données pour : faible volume de contenu détecté par les États-Unis Patriot Act**</span><span class="sxs-lookup"><span data-stu-id="f8753-158">**Show data for: Low volume of content detected U.S. Patriot Act**</span></span>

- <span data-ttu-id="f8753-159">**Afficher les données par : DLP Exchange transport Rules** \> **Décomposer en : sens**: cette vue indique le nombre de messages de gravité **élevée** et de gravité **moyenne**, ainsi que les messages à **faible gravité** qui ont été affectés par les règles de transport DLP.</span><span class="sxs-lookup"><span data-stu-id="f8753-159">**View data by: DLP Exchange transport rules** \> **Break down by: Direction**: This view shows the number of **High severity** and **Medium severity**, and **Low severity** messages that were affected by DLP transport rules.</span></span> <span data-ttu-id="f8753-160">Vous pouvez affiner le graphique en sélectionnant l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="f8753-160">You can further refine the chart by selecting on of the following options:</span></span>

  - <span data-ttu-id="f8753-161">**Afficher les données pour : toutes les règles de transport DLP**</span><span class="sxs-lookup"><span data-stu-id="f8753-161">**Show data for: All DLP transport rules**</span></span>
  - <span data-ttu-id="f8753-162">**Afficher les données de : utilisateurs compromis**</span><span class="sxs-lookup"><span data-stu-id="f8753-162">**Show data for: Compromised users**</span></span>
  - <span data-ttu-id="f8753-163">**Afficher les données pour : faible volume de contenu détecté par les États-Unis Patriot Act**</span><span class="sxs-lookup"><span data-stu-id="f8753-163">**Show data for: Low volume of content detected U.S. Patriot Act**</span></span>

<span data-ttu-id="f8753-164">Si vous cliquez sur **filtres** dans un affichage de rapport, vous pouvez modifier les résultats à l’aide des filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="f8753-164">If you click **Filters** in a report view, you can modify the results with the following filters::</span></span>

- <span data-ttu-id="f8753-165">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="f8753-165">**Start date** and **End date**</span></span>
- <span data-ttu-id="f8753-166">Valeurs de la direction</span><span class="sxs-lookup"><span data-stu-id="f8753-166">Direction values</span></span>
- <span data-ttu-id="f8753-167">Valeurs de gravité</span><span class="sxs-lookup"><span data-stu-id="f8753-167">Severity values</span></span>

![Affichage de rapport dans le rapport des règles de transport Exchange](../../media/transport-rule-report-report-view.png)

### <a name="details-table-view-for-the-exchange-transport-rule-report"></a><span data-ttu-id="f8753-169">Vue de la table Détails pour le rapport des règles de transport Exchange</span><span class="sxs-lookup"><span data-stu-id="f8753-169">Details table view for the Exchange transport rule report</span></span>

<span data-ttu-id="f8753-170">Si vous cliquez sur **afficher les détails table**, les informations affichées dépendent du graphique que vous examinez :</span><span class="sxs-lookup"><span data-stu-id="f8753-170">If you click **View details table**, the information that's shown depends on the chart you were looking at:</span></span>

- <span data-ttu-id="f8753-171">**Afficher les données par : règles de transport Exchange**:</span><span class="sxs-lookup"><span data-stu-id="f8753-171">**View data by: Exchange Transport rules**:</span></span>

  - <span data-ttu-id="f8753-172">**Date**</span><span class="sxs-lookup"><span data-stu-id="f8753-172">**Date**</span></span>
  - <span data-ttu-id="f8753-173">**Règle de transport**</span><span class="sxs-lookup"><span data-stu-id="f8753-173">**Transport rule**</span></span>
  - <span data-ttu-id="f8753-174">**Subject**</span><span class="sxs-lookup"><span data-stu-id="f8753-174">**Subject**</span></span>
  - <span data-ttu-id="f8753-175">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="f8753-175">**Sender address**</span></span>
  - <span data-ttu-id="f8753-176">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="f8753-176">**Recipient address**</span></span>
  - <span data-ttu-id="f8753-177">**Gravité**</span><span class="sxs-lookup"><span data-stu-id="f8753-177">**Severity**</span></span>
  - <span data-ttu-id="f8753-178">**Direction**</span><span class="sxs-lookup"><span data-stu-id="f8753-178">**Direction**</span></span>

- <span data-ttu-id="f8753-179">**Afficher les données par : DLP Exchange transport Rules**:</span><span class="sxs-lookup"><span data-stu-id="f8753-179">**View data by: DLP Exchange transport rules**:</span></span>

  - <span data-ttu-id="f8753-180">**Date**</span><span class="sxs-lookup"><span data-stu-id="f8753-180">**Date**</span></span>
  - <span data-ttu-id="f8753-181">**Stratégie DLP**</span><span class="sxs-lookup"><span data-stu-id="f8753-181">**DLP policy**</span></span>
  - <span data-ttu-id="f8753-182">**Règle de transport**</span><span class="sxs-lookup"><span data-stu-id="f8753-182">**Transport rule**</span></span>
  - <span data-ttu-id="f8753-183">**Subject**</span><span class="sxs-lookup"><span data-stu-id="f8753-183">**Subject**</span></span>
  - <span data-ttu-id="f8753-184">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="f8753-184">**Sender address**</span></span>
  - <span data-ttu-id="f8753-185">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="f8753-185">**Recipient address**</span></span>
  - <span data-ttu-id="f8753-186">**Gravité**</span><span class="sxs-lookup"><span data-stu-id="f8753-186">**Severity**</span></span>
  - <span data-ttu-id="f8753-187">**Direction**</span><span class="sxs-lookup"><span data-stu-id="f8753-187">**Direction**</span></span>

<span data-ttu-id="f8753-188">Si vous cliquez sur **filtres** dans un affichage tableau détaillé, vous pouvez modifier les résultats à l’aide des filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="f8753-188">If you click **Filters** in a details table view, you can modify the results with the following filters:</span></span>

- <span data-ttu-id="f8753-189">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="f8753-189">**Start date** and **End date**</span></span>
- <span data-ttu-id="f8753-190">Valeurs de la direction</span><span class="sxs-lookup"><span data-stu-id="f8753-190">Direction values</span></span>
- <span data-ttu-id="f8753-191">Valeurs de gravité</span><span class="sxs-lookup"><span data-stu-id="f8753-191">Severity values</span></span>

<span data-ttu-id="f8753-192">Pour revenir à l’affichage de rapport, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="f8753-192">To go back to the report view, click **View report**.</span></span>

## <a name="forwarding-report"></a><span data-ttu-id="f8753-193">Rapport de transfert</span><span class="sxs-lookup"><span data-stu-id="f8753-193">Forwarding report</span></span>

<span data-ttu-id="f8753-194">Le **rapport de transfert** indique que les messages envoyés par votre organisation sont transférés automatiquement vers des domaines externes à partir de boîtes aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="f8753-194">The **Forwarding report** shows your organization's automatically forwarded messages to external domains from Exchange Online mailboxes.</span></span> <span data-ttu-id="f8753-195">Les messages transférés peuvent présenter un risque de sécurité ou de conformité, et peuvent indiquer un compte compromis.</span><span class="sxs-lookup"><span data-stu-id="f8753-195">Forwarded messages can pose a security or compliance risk, and might indicate a compromised account.</span></span>

<span data-ttu-id="f8753-196">Pour afficher le rapport, ouvrez le [Centre de sécurité & conformité](https://protection.office.com), cliquez sur **rapports** de \> **tableau de bord** et sélectionnez rapport de **transfert**.</span><span class="sxs-lookup"><span data-stu-id="f8753-196">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Forwarding report**.</span></span> <span data-ttu-id="f8753-197">Pour accéder directement au rapport, ouvrez <https://protection.office.com/reportv2?id=MailFlowForwarding> .</span><span class="sxs-lookup"><span data-stu-id="f8753-197">To go directly to the report, open <https://protection.office.com/reportv2?id=MailFlowForwarding>.</span></span>

![Widget rapport de transfert dans le tableau de bord rapports](../../media/forwarding-report-widget.png)

### <a name="report-view-for-the-forwarding-report"></a><span data-ttu-id="f8753-199">Affichage de rapport pour le rapport de transfert</span><span class="sxs-lookup"><span data-stu-id="f8753-199">Report view for the Forwarding report</span></span>

<span data-ttu-id="f8753-200">Les graphiques suivants sont disponibles dans l’affichage rapport :</span><span class="sxs-lookup"><span data-stu-id="f8753-200">The following charts are available in the report view:</span></span>

- <span data-ttu-id="f8753-201">**Afficher les données pour : méthodes de transfert**: les méthodes suivantes sont affichées :</span><span class="sxs-lookup"><span data-stu-id="f8753-201">**Show data for: Forwarding methods**: The following methods are shown:</span></span>

  - <span data-ttu-id="f8753-202">**Règle de transport**: également appelée [règles de flux de messagerie](https://docs.microsoft.com/Exchange/security-and-compliance/mail-flow-rules/mail-flow-rules).</span><span class="sxs-lookup"><span data-stu-id="f8753-202">**Transport rule**: Also known as [mail flow rules](https://docs.microsoft.com/Exchange/security-and-compliance/mail-flow-rules/mail-flow-rules).</span></span>
  - <span data-ttu-id="f8753-203">**Règle de boîte aux lettres**: également appelée règles de boîte de [réception](https://support.microsoft.com/office/c24f5dea-9465-4df4-ad17-a50704d66c59).</span><span class="sxs-lookup"><span data-stu-id="f8753-203">**Mailbox rule**: Also known as [Inbox rules](https://support.microsoft.com/office/c24f5dea-9465-4df4-ad17-a50704d66c59).</span></span>

  ![Vue des méthodes de transfert dans le rapport de transfert](../../media/forwarding-report-forwarding-methods.png)

- <span data-ttu-id="f8753-205">**Afficher les données pour : transferts de domaines**: cette vue affiche les domaines de destinataire qui sont les destinations pour le transfert.</span><span class="sxs-lookup"><span data-stu-id="f8753-205">**Show data for: Forwarding domains**: This view shows the recipient domains that are the destinations for forwarding.</span></span>

  ![Vue des domaines de transfert dans le rapport de transfert](../../media/forwarding-report-forwarding-domains.png)

- <span data-ttu-id="f8753-207">**Afficher les données : redirecteurs**: les redirecteurs suivants sont affichés :</span><span class="sxs-lookup"><span data-stu-id="f8753-207">**Show data for: Forwarders**: The following forwarders are shown:</span></span>

  - <span data-ttu-id="f8753-208">**Règle de transport**</span><span class="sxs-lookup"><span data-stu-id="f8753-208">**Transport rule**</span></span>
  - <span data-ttu-id="f8753-209">Boîte aux lettres qui contient la règle de boîte de réception de transfert.</span><span class="sxs-lookup"><span data-stu-id="f8753-209">The mailbox that contains the forwarding Inbox rule.</span></span>

  ![Vue redirecteurs dans le rapport de transfert](../../media/forwarding-report-forwarders.png)

<span data-ttu-id="f8753-211">Si vous cliquez sur **filtres** dans un affichage de rapport, vous pouvez spécifier une plage de dates avec **Date de début** et date de **fin**.</span><span class="sxs-lookup"><span data-stu-id="f8753-211">If you click **Filters** in a report view, you can specify a date range with **Start date** and **End date**.</span></span>

### <a name="details-table-view-for-the-forwarding-report"></a><span data-ttu-id="f8753-212">Vue de la table Détails pour le rapport de transfert</span><span class="sxs-lookup"><span data-stu-id="f8753-212">Details table view for the Forwarding report</span></span>

<span data-ttu-id="f8753-213">Si vous cliquez sur **afficher la table des détails** dans un affichage de rapport, les informations suivantes s’affichent :</span><span class="sxs-lookup"><span data-stu-id="f8753-213">If you click **View details table** in a report view, the following information is shown:</span></span>

- <span data-ttu-id="f8753-214">**Redirecteurs**: la **règle de transport** value ou la boîte aux lettres qui contient la règle de boîte de réception de transfert.</span><span class="sxs-lookup"><span data-stu-id="f8753-214">**Forwarders**: The value **Transport rule** or the mailbox that contains the forwarding Inbox rule.</span></span>
- <span data-ttu-id="f8753-215">**Type de transfert**: règle de la **boîte aux lettres** ou **règle de transport**.</span><span class="sxs-lookup"><span data-stu-id="f8753-215">**Forwarding type**: The value **Mailbox rule** or **Transport rule**.</span></span>
- <span data-ttu-id="f8753-216">**Nom du destinataire**</span><span class="sxs-lookup"><span data-stu-id="f8753-216">**Recipient name**</span></span>
- <span data-ttu-id="f8753-217">**Domaine du destinataire**</span><span class="sxs-lookup"><span data-stu-id="f8753-217">**Recipient domain**</span></span>
- <span data-ttu-id="f8753-218">**Détails**: il s’agit de la valeur GUID de la règle de flux de messagerie ou de la valeur RuleIdentity de la règle de boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="f8753-218">**Details**: This is the GUID value of the mail flow rule, or the RuleIdentity value of the Inbox rule.</span></span>
- <span data-ttu-id="f8753-219">**Count**</span><span class="sxs-lookup"><span data-stu-id="f8753-219">**Count**</span></span>
- <span data-ttu-id="f8753-220">**Première date de transfert**</span><span class="sxs-lookup"><span data-stu-id="f8753-220">**First forward date**</span></span>

<span data-ttu-id="f8753-221">Si vous cliquez sur **filtres** dans un affichage tableau détaillé, vous pouvez spécifier une plage de dates avec **Date de début** et date de **fin**.</span><span class="sxs-lookup"><span data-stu-id="f8753-221">If you click **Filters** in a details table view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="f8753-222">Pour revenir à l’affichage rapports, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="f8753-222">To go back to the reports view, click **View report**.</span></span>

## <a name="mailflow-status-report"></a><span data-ttu-id="f8753-223">Rapport d’état de flux de flux</span><span class="sxs-lookup"><span data-stu-id="f8753-223">Mailflow status report</span></span>

<span data-ttu-id="f8753-224">Le **rapport d’état de flux** de messagerie est similaire au [rapport de courrier électronique envoyé et reçu](#sent-and-received-email-report), avec des informations supplémentaires sur le courrier électronique autorisé ou bloqué sur le serveur Edge.</span><span class="sxs-lookup"><span data-stu-id="f8753-224">The **Mailflow status report** is similar to the [Sent and received email report](#sent-and-received-email-report), with additional information about email allowed or blocked on the edge.</span></span> <span data-ttu-id="f8753-225">Il s’agit du seul rapport qui contient les informations de protection du serveur Edge et indique le nombre de messages bloqués avant d’être autorisés dans le service pour l’évaluation par Exchange Online Protection (EOP).</span><span class="sxs-lookup"><span data-stu-id="f8753-225">This is the only report that contains edge protection information, and shows just how much email is blocked before being allowed into the service for evaluation by Exchange Online Protection (EOP).</span></span> <span data-ttu-id="f8753-226">Il est important de comprendre que si un message est envoyé à cinq destinataires, nous le dénombrez cinq messages différents et pas un message.</span><span class="sxs-lookup"><span data-stu-id="f8753-226">It's important to understand that if a message is sent to five recipients we count it as five different messages and not one message.</span></span>
<span data-ttu-id="f8753-227">Pour afficher le rapport, ouvrez le [Centre de sécurité & conformité](https://protection.office.com), accédez **Reports** au \> **tableau de bord** rapports et sélectionnez rapport d’État du **flux de flux**.</span><span class="sxs-lookup"><span data-stu-id="f8753-227">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Mailflow status report**.</span></span> <span data-ttu-id="f8753-228">Pour accéder directement au **rapport d’État du flux de messagerie**, ouvrez <https://protection.office.com/mailflowStatusReport> .</span><span class="sxs-lookup"><span data-stu-id="f8753-228">To go directly to the **Mail flow status report**, open <https://protection.office.com/mailflowStatusReport>.</span></span>

![Widget rapport d’état de flux de notification dans le tableau de bord rapports](../../media/mail-flow-status-report-widget.png)

### <a name="type-view-for-the-mailflow-status-report"></a><span data-ttu-id="f8753-230">Vue type pour le rapport d’état de flux de flux</span><span class="sxs-lookup"><span data-stu-id="f8753-230">Type view for the Mailflow status report</span></span>

<span data-ttu-id="f8753-231">Lorsque vous ouvrez le rapport, l’onglet **type** est sélectionné par défaut.</span><span class="sxs-lookup"><span data-stu-id="f8753-231">When you open the report, the **Type** tab is selected by default.</span></span> <span data-ttu-id="f8753-232">Par défaut, cette vue contient un graphique et une table de données configurée avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="f8753-232">By default, this view contains a chart and a data table that's configured with the following filters:</span></span>

- <span data-ttu-id="f8753-233">**Date**: les 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="f8753-233">**Date**: The last 7 days.</span></span>
- <span data-ttu-id="f8753-234">**Sens**:</span><span class="sxs-lookup"><span data-stu-id="f8753-234">**Direction**:</span></span>

  - <span data-ttu-id="f8753-235">**Entrants**</span><span class="sxs-lookup"><span data-stu-id="f8753-235">**Inbound**</span></span>
  - <span data-ttu-id="f8753-236">**Sortant**</span><span class="sxs-lookup"><span data-stu-id="f8753-236">**Outbound**</span></span>
  - <span data-ttu-id="f8753-237">**Intra-org**: ce nombre est pour les messages au sein d’un client, c’est-à-dire</span><span class="sxs-lookup"><span data-stu-id="f8753-237">**Intra-org**: this count is for messages within a tenant i.e</span></span> <span data-ttu-id="f8753-238">l’expéditeur abc@domain.com envoie au destinataire xyz@domain.com (compté indépendamment des **ports entrants et** **sortants**)</span><span class="sxs-lookup"><span data-stu-id="f8753-238">sender abc@domain.com sends to recipient xyz@domain.com  (counted separately from **Inbound** and **Outbound**)</span></span>

- <span data-ttu-id="f8753-239">**Type**:</span><span class="sxs-lookup"><span data-stu-id="f8753-239">**Type**:</span></span>

  - <span data-ttu-id="f8753-240">**Courrier électronique approprié**</span><span class="sxs-lookup"><span data-stu-id="f8753-240">**Good mail**</span></span>
  - <span data-ttu-id="f8753-241">**Programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="f8753-241">**Malware**</span></span>
  - <span data-ttu-id="f8753-242">**Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="f8753-242">**Spam**</span></span>
  - <span data-ttu-id="f8753-243">**Protection des serveurs Edge**</span><span class="sxs-lookup"><span data-stu-id="f8753-243">**Edge protection**</span></span>
  - <span data-ttu-id="f8753-244">**Messages de règle**</span><span class="sxs-lookup"><span data-stu-id="f8753-244">**Rule messages**</span></span>
  - <span data-ttu-id="f8753-245">**Courriers hameçons**</span><span class="sxs-lookup"><span data-stu-id="f8753-245">**Phishing email**</span></span>

<span data-ttu-id="f8753-246">Le graphique est organisé selon les valeurs de **type** .</span><span class="sxs-lookup"><span data-stu-id="f8753-246">The chart is organized by the **Type** values.</span></span>

<span data-ttu-id="f8753-247">Vous pouvez modifier ces filtres en cliquant sur **Filtrer** ou en cliquant sur une valeur dans la légende du graphique.</span><span class="sxs-lookup"><span data-stu-id="f8753-247">You can change these filters by clicking **Filter** or by clicking a value in the chart legend.</span></span>

<span data-ttu-id="f8753-248">Le tableau de données contient les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="f8753-248">The data table contains the following information:</span></span>

- <span data-ttu-id="f8753-249">**Direction**</span><span class="sxs-lookup"><span data-stu-id="f8753-249">**Direction**</span></span>
- <span data-ttu-id="f8753-250">**Type**</span><span class="sxs-lookup"><span data-stu-id="f8753-250">**Type**</span></span>
- <span data-ttu-id="f8753-251">**24 heures**</span><span class="sxs-lookup"><span data-stu-id="f8753-251">**24 hours**</span></span>
- <span data-ttu-id="f8753-252">**3 jours**</span><span class="sxs-lookup"><span data-stu-id="f8753-252">**3 days**</span></span>
- <span data-ttu-id="f8753-253">**7 jours**</span><span class="sxs-lookup"><span data-stu-id="f8753-253">**7 days**</span></span>
- <span data-ttu-id="f8753-254">**15 jours**</span><span class="sxs-lookup"><span data-stu-id="f8753-254">**15 days**</span></span>
- <span data-ttu-id="f8753-255">**30 jours**</span><span class="sxs-lookup"><span data-stu-id="f8753-255">**30 days**</span></span>

<span data-ttu-id="f8753-256">Si vous cliquez sur **choisir une catégorie pour plus d’informations**, vous pouvez sélectionner l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="f8753-256">If you click **Choose a category for more details**, you can select from the following values:</span></span>

- <span data-ttu-id="f8753-257">**Courrier électronique de hameçonnage**: cette sélection vous permet d’accéder au [rapport d’état de protection contre les menaces](view-email-security-reports.md#threat-protection-status-report).</span><span class="sxs-lookup"><span data-stu-id="f8753-257">**Phishing email**: This selection takes you to the [Threat protection status report](view-email-security-reports.md#threat-protection-status-report).</span></span>
- <span data-ttu-id="f8753-258">**Programme malveillant dans la messagerie**: cette sélection vous permet d’accéder au [rapport d’état de protection contre les menaces](view-email-security-reports.md#threat-protection-status-report).</span><span class="sxs-lookup"><span data-stu-id="f8753-258">**Malware in email**: This selection takes you to the [Threat protection status report](view-email-security-reports.md#threat-protection-status-report).</span></span>
- <span data-ttu-id="f8753-259">**Détections de courrier indésirable**: cette sélection vous permet d’accéder au [rapport des détections de courrier indésirable](view-email-security-reports.md#spam-detections-report).</span><span class="sxs-lookup"><span data-stu-id="f8753-259">**Spam detections**: This selection takes you to the [Spam Detections report](view-email-security-reports.md#spam-detections-report).</span></span>
- <span data-ttu-id="f8753-260">**Courrier indésirable bloqué**pour le serveur Edge : cette sélection vous permet d’accéder au [rapport des détections de courrier indésirable](view-email-security-reports.md#spam-detections-report).</span><span class="sxs-lookup"><span data-stu-id="f8753-260">**Edge blocked spam**: This selection takes you to the [Spam Detections report](view-email-security-reports.md#spam-detections-report).</span></span>

<span data-ttu-id="f8753-261">**Exportation**:</span><span class="sxs-lookup"><span data-stu-id="f8753-261">**Export**:</span></span>

<span data-ttu-id="f8753-262">Pour l’affichage détaillé, vous pouvez uniquement exporter des données pour un jour.</span><span class="sxs-lookup"><span data-stu-id="f8753-262">For the detail view, you can only export data for one day.</span></span> <span data-ttu-id="f8753-263">Par conséquent, si vous voulez exporter des données pendant 7 jours, vous devez effectuer 7 actions d’exportation différentes.</span><span class="sxs-lookup"><span data-stu-id="f8753-263">So, if you want to export data for 7 days, you need to do 7 different export actions.</span></span>

<span data-ttu-id="f8753-264">Chaque fichier. csv exporté est limité à 150 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="f8753-264">Each exported .csv file is limited to 150,000 rows.</span></span> <span data-ttu-id="f8753-265">Si les données de ce jour contiennent plus de 150 000 lignes, plusieurs fichiers. csv seront créés.</span><span class="sxs-lookup"><span data-stu-id="f8753-265">If the data for that day contains more than 150,000 rows, then multiple .csv files will be created.</span></span>

![<span data-ttu-id="f8753-266">Tapez View dans le rapport d’état de flux de flux</span><span class="sxs-lookup"><span data-stu-id="f8753-266">Type view in the Mailflow status report</span></span> ](../../media/mail-flow-status-report-type-view.png)

### <a name="direction-view-for-the-mailflow-status-report"></a><span data-ttu-id="f8753-267">Vue de direction pour le rapport d’état de flux de flux</span><span class="sxs-lookup"><span data-stu-id="f8753-267">Direction view for the Mailflow status report</span></span>

<span data-ttu-id="f8753-268">Si vous cliquez sur l’onglet **direction** , les mêmes filtres par défaut de la vue **type** sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="f8753-268">If you click the **Direction** tab, the same default filters from the **Type** view are used.</span></span>

<span data-ttu-id="f8753-269">Le graphique est organisé par les valeurs de **direction** .</span><span class="sxs-lookup"><span data-stu-id="f8753-269">The chart is organized by **Direction** values.</span></span>

<span data-ttu-id="f8753-270">Vous pouvez modifier ces filtres en cliquant sur **Filtrer** ou en cliquant sur une valeur dans la légende du graphique.</span><span class="sxs-lookup"><span data-stu-id="f8753-270">You can change these filters by clicking **Filter** or by clicking a value in the chart legend.</span></span> <span data-ttu-id="f8753-271">Les mêmes filtres de la vue **type** sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="f8753-271">The same filters from the **Type** view are used.</span></span>

<span data-ttu-id="f8753-272">La table de données contient les mêmes informations à partir de la vue **type** .</span><span class="sxs-lookup"><span data-stu-id="f8753-272">The data table contains same information from the **Type** view.</span></span>

<span data-ttu-id="f8753-273">La **catégorie choisir une catégorie pour plus de détails** disponibles et les sélections possibles est identique à la vue **type** .</span><span class="sxs-lookup"><span data-stu-id="f8753-273">The **Choose a category for more details** available selections and behavior are the same as the **Type** view.</span></span>

<span data-ttu-id="f8753-274">**Exportation**:</span><span class="sxs-lookup"><span data-stu-id="f8753-274">**Export**:</span></span>

<span data-ttu-id="f8753-275">Pour l’affichage détaillé, vous pouvez uniquement exporter des données pour un jour.</span><span class="sxs-lookup"><span data-stu-id="f8753-275">For the detail view, you can only export data for one day.</span></span> <span data-ttu-id="f8753-276">Par conséquent, si vous voulez exporter des données pendant 7 jours, vous devez effectuer 7 actions d’exportation différentes.</span><span class="sxs-lookup"><span data-stu-id="f8753-276">So, if you want to export data for 7 days, you need to do 7 different export actions.</span></span>

<span data-ttu-id="f8753-277">Chaque fichier. csv exporté est limité à 150 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="f8753-277">Each exported .csv file is limited to 150,000 rows.</span></span> <span data-ttu-id="f8753-278">Si les données de ce jour contiennent plus de 150 000 lignes, plusieurs fichiers. csv seront créés.</span><span class="sxs-lookup"><span data-stu-id="f8753-278">If the data for that day contains more than 150,000 rows, then multiple .csv files will be created.</span></span>

![<span data-ttu-id="f8753-279">Affichage de la direction dans le rapport d’état de flux de flux</span><span class="sxs-lookup"><span data-stu-id="f8753-279">Direction view in the Mailflow status report</span></span> ](../../media/mail-flow-status-report-direction-view.png)

### <a name="funnel-view-for-the-mailflow-status-report"></a><span data-ttu-id="f8753-280">Vue entonnoir pour le rapport d’état de flux de flux</span><span class="sxs-lookup"><span data-stu-id="f8753-280">Funnel view for the Mailflow status report</span></span>

<span data-ttu-id="f8753-281">L’affichage **entonnoir** vous montre comment les fonctionnalités de protection contre les menaces Microsoft filtrent le courrier électronique entrant et sortant dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f8753-281">The **Funnel** view shows you how Microsoft's email threat protection features filter incoming and outgoing email in your organization.</span></span> <span data-ttu-id="f8753-282">Elle fournit des détails sur le nombre total de messages électroniques, ainsi que la façon dont les fonctionnalités de protection contre les menaces configurées, notamment la protection des serveurs Edge, les logiciels anti-programme malveillant, le hameçonnage, le blocage du courrier indésirable et la détection d’usurpation d’identité ont un impact sur ce nombre.</span><span class="sxs-lookup"><span data-stu-id="f8753-282">It provides details on the total email count, and how the configured threat protection features, including edge protection, anti-malware, anti-phishing, anti-spam, and anti-spoofing affect this count.</span></span>

<span data-ttu-id="f8753-283">Si vous cliquez sur l’onglet **entonnoir** , par défaut, cet affichage contient un graphique et une table de données configurée avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="f8753-283">If you click the **Funnel** tab, by default, this view contains a chart and a data table that's configured with the following filters:</span></span>

- <span data-ttu-id="f8753-284">**Date**: les 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="f8753-284">**Date**: The last 7 days.</span></span>

- <span data-ttu-id="f8753-285">**Sens**:</span><span class="sxs-lookup"><span data-stu-id="f8753-285">**Direction**:</span></span>

  - <span data-ttu-id="f8753-286">**Entrants**</span><span class="sxs-lookup"><span data-stu-id="f8753-286">**Inbound**</span></span>
  - <span data-ttu-id="f8753-287">**Sortant**</span><span class="sxs-lookup"><span data-stu-id="f8753-287">**Outbound**</span></span>
  - <span data-ttu-id="f8753-288">**Intra-org**: ce nombre est pour les messages envoyés au sein d’un client ; par exemple, l’expéditeur abc@domain.com envoie au destinataire xyz@domain.com (compté indépendamment des messages entrants et sortants).</span><span class="sxs-lookup"><span data-stu-id="f8753-288">**Intra-org**: This count is for messages sent within a tenant; i.e, sender abc@domain.com sends to recipient xyz@domain.com (counted separately from Inbound and Outbound).</span></span>

<span data-ttu-id="f8753-289">L’affichage d’agrégation et le tableau de données autorisent 90 jours de filtrage.</span><span class="sxs-lookup"><span data-stu-id="f8753-289">The aggregate view and data table view allow for 90 days of filtering.</span></span>

<span data-ttu-id="f8753-290">Si vous cliquez sur **filtre**, vous pouvez filtrer le graphique et la table de données.</span><span class="sxs-lookup"><span data-stu-id="f8753-290">If you click **Filter**, you can filter both the chart and the data table.</span></span>

<span data-ttu-id="f8753-291">Ce graphique indique le nombre de messages organisés par :</span><span class="sxs-lookup"><span data-stu-id="f8753-291">This chart shows the email count organized by:</span></span>

- <span data-ttu-id="f8753-292">**Nombre total de messages électroniques**</span><span class="sxs-lookup"><span data-stu-id="f8753-292">**Total email**</span></span>
- <span data-ttu-id="f8753-293">**Courrier électronique après la protection du serveur Edge**</span><span class="sxs-lookup"><span data-stu-id="f8753-293">**Email after edge protection**</span></span>
- <span data-ttu-id="f8753-294">**Courrier électronique après anti-programme malveillant, réputation de fichier, bloc de type fichier**</span><span class="sxs-lookup"><span data-stu-id="f8753-294">**Email after anti-malware, file reputation, file type block**</span></span>
- <span data-ttu-id="f8753-295">**Courrier électronique après hameçonnage, réputation de l’URL, emprunt d’identité de marque, anti-usurpation**</span><span class="sxs-lookup"><span data-stu-id="f8753-295">**Email after anti-phish, URL reputation, brand impersonation, anti-spoof**</span></span>
- <span data-ttu-id="f8753-296">**Courrier électronique après blocage du courrier indésirable et filtrage du courrier en nombre**</span><span class="sxs-lookup"><span data-stu-id="f8753-296">**Email after anti-spam, bulk mail filtering**</span></span>
- <span data-ttu-id="f8753-297">**Courrier électronique après l’emprunt d’identité d’utilisateur et de domaine**<sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="f8753-297">**Email after user and domain impersonation**<sup>1</sup></span></span>
- <span data-ttu-id="f8753-298">**Courrier électronique après la détonation 1 du fichier et de l’URL**<sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="f8753-298">**Email after file and URL detonation**<sup>1</sup></span></span>
- <span data-ttu-id="f8753-299">**Courrier électronique détecté comme étant Bénin après une protection post-remise (URL-clic sur la protection du temps de clic)**</span><span class="sxs-lookup"><span data-stu-id="f8753-299">**Email detected as benign after post-delivery protection (URL click time protection)**</span></span>

<span data-ttu-id="f8753-300"><sup>1</sup> ATP Office 365 uniquement</span><span class="sxs-lookup"><span data-stu-id="f8753-300"><sup>1</sup> Office 365 ATP only</span></span>

<span data-ttu-id="f8753-301">Pour afficher le courrier électronique filtré par EOP ou ATP séparément, cliquez sur la valeur dans la légende du graphique.</span><span class="sxs-lookup"><span data-stu-id="f8753-301">To view the email filtered by EOP or ATP separately, click on the value in the chart legend.</span></span>

<span data-ttu-id="f8753-302">La table de données contient les informations suivantes, indiquées dans l’ordre décroissant de date :</span><span class="sxs-lookup"><span data-stu-id="f8753-302">The data table contains the following information, shown in descending date order:</span></span>

- <span data-ttu-id="f8753-303">**Date**</span><span class="sxs-lookup"><span data-stu-id="f8753-303">**Date**</span></span>
- <span data-ttu-id="f8753-304">**Nombre total de messages électroniques**</span><span class="sxs-lookup"><span data-stu-id="f8753-304">**Total email**</span></span>
- <span data-ttu-id="f8753-305">**Protection des serveurs Edge**</span><span class="sxs-lookup"><span data-stu-id="f8753-305">**Edge protection**</span></span>
- <span data-ttu-id="f8753-306">**Anti-programme malveillant, réputation de fichier, bloc de type de fichier**</span><span class="sxs-lookup"><span data-stu-id="f8753-306">**Anti-malware, file reputation, file type block**</span></span>
- <span data-ttu-id="f8753-307">**Hameçonnage, réputation de l’URL, emprunt d’identité de marque, anti-usurpation**</span><span class="sxs-lookup"><span data-stu-id="f8753-307">**Anti-phish, URL reputation, Brand impersonation, anti-spoof**</span></span>
- <span data-ttu-id="f8753-308">**Blocage du courrier indésirable et du filtrage du courrier en nombre**</span><span class="sxs-lookup"><span data-stu-id="f8753-308">**Anti-spam, bulk mail filtering**</span></span>
- <span data-ttu-id="f8753-309">**Emprunt d’identité d’utilisateur et de domaine (ATP)**</span><span class="sxs-lookup"><span data-stu-id="f8753-309">**User and domain impersonation (ATP)**</span></span>
- <span data-ttu-id="f8753-310">**Détonation des fichiers et des URL (ATP)**</span><span class="sxs-lookup"><span data-stu-id="f8753-310">**File and URL detonation (ATP)**</span></span>
- <span data-ttu-id="f8753-311">**Protection après livraison après réception, ou ZAP (EOP)**</span><span class="sxs-lookup"><span data-stu-id="f8753-311">**Post-delivery protection and ZAP (ATP), or ZAP (EOP)**</span></span>

<span data-ttu-id="f8753-312">Si vous sélectionnez une ligne dans le tableau de données, une autre répartition du nombre de messages est affichée dans le menu volant.</span><span class="sxs-lookup"><span data-stu-id="f8753-312">If you select a row in the data table, a further breakdown of the email counts are shown in the flyout.</span></span>

<span data-ttu-id="f8753-313">**Exportation**:</span><span class="sxs-lookup"><span data-stu-id="f8753-313">**Export**:</span></span>

<span data-ttu-id="f8753-314">Après avoir cliqué sur **Exporter** sous **options**, vous pouvez sélectionner l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="f8753-314">After you click **Export** under **Options**, you can select one of the following values:</span></span>

- <span data-ttu-id="f8753-315">**Résumé (avec les données au plus des 90 derniers jours)**</span><span class="sxs-lookup"><span data-stu-id="f8753-315">**Summary (with data for last 90 days at most)**</span></span>
- <span data-ttu-id="f8753-316">**Détails (avec les données des 30 derniers jours)**</span><span class="sxs-lookup"><span data-stu-id="f8753-316">**Details (with data for last 30 days at most)**</span></span>

<span data-ttu-id="f8753-317">Sous **Date**, choisissez une plage, puis cliquez sur **appliquer**.</span><span class="sxs-lookup"><span data-stu-id="f8753-317">Under **Date**, choose a range, and then click **Apply**.</span></span> <span data-ttu-id="f8753-318">Les données des filtres actuels seront exportées dans un fichier. csv.</span><span class="sxs-lookup"><span data-stu-id="f8753-318">Data for the current filters will be exported to a .csv file.</span></span>

<span data-ttu-id="f8753-319">Chaque fichier. csv exporté est limité à 150 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="f8753-319">Each exported .csv file is limited to 150,000 rows.</span></span> <span data-ttu-id="f8753-320">Si les données contiennent plus de 150 000 lignes, plusieurs fichiers. csv seront créés.</span><span class="sxs-lookup"><span data-stu-id="f8753-320">If the data contains more than 150,000 rows, then multiple .csv files will be created.</span></span>

 ![<span data-ttu-id="f8753-321">Vue entonnoir dans le rapport d’état de flux de flux</span><span class="sxs-lookup"><span data-stu-id="f8753-321">Funnel view in the Mailflow status report</span></span> ](../../media/mail-flow-status-report-funnel-view.png)

### <a name="tech-view-for-the-mailflow-status-report"></a><span data-ttu-id="f8753-322">Vue technique pour le rapport d’état de flux de flux</span><span class="sxs-lookup"><span data-stu-id="f8753-322">Tech view for the Mailflow status report</span></span>

<span data-ttu-id="f8753-323">La **vue Tech** est similaire à l’affichage **entonnoir** , qui fournit des détails plus granulaires pour les fonctionnalités de protection contre les menaces configurées.</span><span class="sxs-lookup"><span data-stu-id="f8753-323">The **Tech view** is similar to the **Funnel** view, providing more granular details for the configured threat protections features.</span></span> <span data-ttu-id="f8753-324">À partir du graphique, vous pouvez voir comment les messages sont catégorisés aux différentes étapes de la protection contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="f8753-324">From the chart, you can see how messages are categorized at the different stages of threat protection.</span></span>

<span data-ttu-id="f8753-325">Si vous cliquez sur l’onglet **affichage Tech** , par défaut, cet affichage contient un graphique et une table de données configurée avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="f8753-325">If you click the **Tech view** tab, by default, this view contains a chart and a data table that's configured with the following filters:</span></span>

- <span data-ttu-id="f8753-326">**Date**: les 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="f8753-326">**Date**: The last 7 days.</span></span>

- <span data-ttu-id="f8753-327">**Sens**:</span><span class="sxs-lookup"><span data-stu-id="f8753-327">**Direction**:</span></span>

  - <span data-ttu-id="f8753-328">**Entrants**</span><span class="sxs-lookup"><span data-stu-id="f8753-328">**Inbound**</span></span>
  - <span data-ttu-id="f8753-329">**Sortant**</span><span class="sxs-lookup"><span data-stu-id="f8753-329">**Outbound**</span></span>
  - <span data-ttu-id="f8753-330">**Intra-org**: ce nombre est pour les messages au sein d’un client, c’est-à-dire</span><span class="sxs-lookup"><span data-stu-id="f8753-330">**Intra-org**: this count is for messages within a tenant i.e</span></span> <span data-ttu-id="f8753-331">l’expéditeur abc@domain.com envoie au destinataire xyz@domain.com (compté indépendamment des ports entrants et sortants)</span><span class="sxs-lookup"><span data-stu-id="f8753-331">sender abc@domain.com sends to recipient xyz@domain.com (counted separately from Inbound and Outbound)</span></span>

<span data-ttu-id="f8753-332">L’affichage d’agrégation et le tableau de données autorisent 90 jours de filtrage.</span><span class="sxs-lookup"><span data-stu-id="f8753-332">The aggregate view and data table view allow for 90 days of filtering.</span></span>

<span data-ttu-id="f8753-333">Si vous cliquez sur **filtre**, vous pouvez filtrer le graphique et la table de données.</span><span class="sxs-lookup"><span data-stu-id="f8753-333">If you click **Filter**, you can filter both the chart and the data table.</span></span>

<span data-ttu-id="f8753-334">Ce graphique présente les messages organisés selon les catégories suivantes :</span><span class="sxs-lookup"><span data-stu-id="f8753-334">This chart shows messages organized into the following categories:</span></span>

- <span data-ttu-id="f8753-335">**Nombre total de messages électroniques**</span><span class="sxs-lookup"><span data-stu-id="f8753-335">**Total email**</span></span>
- <span data-ttu-id="f8753-336">**Serveur Edge autorisé, serveur Edge filtré**</span><span class="sxs-lookup"><span data-stu-id="f8753-336">**Edge allow, edge filtered**</span></span>
- <span data-ttu-id="f8753-337">**Pas de programmes malveillants, détection de pièces jointes fiables (ATP), détection du moteur anti-programme malveillant, bloc de règles**</span><span class="sxs-lookup"><span data-stu-id="f8753-337">**Not malware, Safe attachments detection (ATP), Anti-malware engine detection, rule block**</span></span>
- <span data-ttu-id="f8753-338">**Non-hameçonnage, échec DMARC, détection d’usurpation d’identité, détection d’usurpation d’identité, détection de hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="f8753-338">**Not phish, DMARC failure, impersonation detection, spoof detection, phish detection**</span></span>
- <span data-ttu-id="f8753-339">**Aucune détection avec détonation d’URL, détection de détonation d’URL (ATP)**</span><span class="sxs-lookup"><span data-stu-id="f8753-339">**No detection with URL detonation, URL detonation detection (ATP)**</span></span>
- <span data-ttu-id="f8753-340">**Courrier indésirable, courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="f8753-340">**Not spam, spam**</span></span>
- <span data-ttu-id="f8753-341">**Courrier électronique non malveillant, détection de liens fiables (ATP), ZAP**</span><span class="sxs-lookup"><span data-stu-id="f8753-341">**Non-malicious email, safe links detection (ATP), ZAP**</span></span>

<span data-ttu-id="f8753-342">Lorsque vous placez le curseur de la souris sur une catégorie dans le graphique, vous pouvez voir le nombre de messages dans cette catégorie.</span><span class="sxs-lookup"><span data-stu-id="f8753-342">When you hover over a category in the chart, you can see the number of messages in that category.</span></span>

<span data-ttu-id="f8753-343">La table de données contient les informations suivantes, indiquées dans l’ordre décroissant de date :</span><span class="sxs-lookup"><span data-stu-id="f8753-343">The data table contains the following information, shown in descending date order:</span></span>

- <span data-ttu-id="f8753-344">**Date**</span><span class="sxs-lookup"><span data-stu-id="f8753-344">**Date**</span></span>
- <span data-ttu-id="f8753-345">**Nombre total de messages électroniques**</span><span class="sxs-lookup"><span data-stu-id="f8753-345">**Total email**</span></span>
- <span data-ttu-id="f8753-346">**Serveur Edge filtré**</span><span class="sxs-lookup"><span data-stu-id="f8753-346">**Edge filtered**</span></span>
- <span data-ttu-id="f8753-347">**Moteur anti-programme malveillant, pièces jointes fiables, règle filtrée**</span><span class="sxs-lookup"><span data-stu-id="f8753-347">**Anti-malware engine, safe attachments, rule filtered**</span></span>
- <span data-ttu-id="f8753-348">**DMARC, emprunt d’identité, usurpation, hameçonnage filtré**</span><span class="sxs-lookup"><span data-stu-id="f8753-348">**DMARC, impersonation, spoof, phish filtered**</span></span>
- <span data-ttu-id="f8753-349">**Détection de la détonation d’URL**</span><span class="sxs-lookup"><span data-stu-id="f8753-349">**URL detonation detection**</span></span>
- <span data-ttu-id="f8753-350">**Filtrage du courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="f8753-350">**Anti-spam filtered**</span></span>
- <span data-ttu-id="f8753-351">**ZAP supprimé**</span><span class="sxs-lookup"><span data-stu-id="f8753-351">**ZAP removed**</span></span>
- <span data-ttu-id="f8753-352">**Détection par les liens fiables**</span><span class="sxs-lookup"><span data-stu-id="f8753-352">**Detection by safe links**</span></span>

<span data-ttu-id="f8753-353">Si vous sélectionnez une ligne dans le tableau de données, une autre répartition du nombre de messages est affichée dans le menu volant.</span><span class="sxs-lookup"><span data-stu-id="f8753-353">If you select a row in the data table, a further breakdown of the email counts are shown in the flyout.</span></span>

<span data-ttu-id="f8753-354">**Exportation**:</span><span class="sxs-lookup"><span data-stu-id="f8753-354">**Export**:</span></span>

<span data-ttu-id="f8753-355">Lorsque vous cliquez sur **Exporter**, sous **options** , vous pouvez sélectionner l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="f8753-355">On clicking **Export**, under **Options** you can select one of the following values:</span></span>

- <span data-ttu-id="f8753-356">**Résumé (avec les données au plus des 90 derniers jours)**</span><span class="sxs-lookup"><span data-stu-id="f8753-356">**Summary (with data for last 90 days at most)**</span></span>
- <span data-ttu-id="f8753-357">**Détails (avec les données des 30 derniers jours)**</span><span class="sxs-lookup"><span data-stu-id="f8753-357">**Details (with data for last 30 days at most)**</span></span>

<span data-ttu-id="f8753-358">Sous **Date**, choisissez une plage, puis cliquez sur **appliquer**.</span><span class="sxs-lookup"><span data-stu-id="f8753-358">Under **Date**, choose a range, and then click **Apply**.</span></span> <span data-ttu-id="f8753-359">Les données des filtres actuels seront exportées dans un fichier. csv.</span><span class="sxs-lookup"><span data-stu-id="f8753-359">Data for the current filters will be exported to a .csv file.</span></span>

<span data-ttu-id="f8753-360">Chaque fichier. csv exporté est limité à 150 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="f8753-360">Each exported .csv file is limited to 150,000 rows.</span></span> <span data-ttu-id="f8753-361">Si les données contiennent plus de 150 000 lignes, plusieurs fichiers. csv seront créés.</span><span class="sxs-lookup"><span data-stu-id="f8753-361">If the data contains more than 150,000 rows, then multiple .csv files will be created.</span></span>

 ![<span data-ttu-id="f8753-362">Vue technique dans le rapport d’état de flux de flux</span><span class="sxs-lookup"><span data-stu-id="f8753-362">Tech view in the Mailflow status report</span></span> ](../../media/mail-flow-status-report-Tech-view.png)

## <a name="sent-and-received-email-report"></a><span data-ttu-id="f8753-363">Rapport de courrier électronique envoyé et reçu</span><span class="sxs-lookup"><span data-stu-id="f8753-363">Sent and received email report</span></span>

<span data-ttu-id="f8753-364">Le rapport de **courrier électronique envoyé et reçu** est un rapport intelligent qui affiche des informations sur les messages entrants et sortants, notamment les détections de courrier indésirable, les programmes malveillants et la messagerie électronique identifiés comme étant « en qualité ».</span><span class="sxs-lookup"><span data-stu-id="f8753-364">The **Sent and received email** report is a smart report that shows information about incoming and outgoing email, including spam detections, malware, and email identified as "good."</span></span> <span data-ttu-id="f8753-365">La différence entre ce rapport et le [rapport d’état de flux](#mailflow-status-report) de courrier est la suivante : ce rapport n’inclut pas de données sur les messages bloqués par la protection du serveur Edge.</span><span class="sxs-lookup"><span data-stu-id="f8753-365">The difference between this report and the [Mailflow status report](#mailflow-status-report) is: this report doesn't include data about messages blocked by edge protection.</span></span>

<span data-ttu-id="f8753-366">L’affichage Aggregate et l’affichage détaillé du rapport autorisent 90 jours de filtrage.</span><span class="sxs-lookup"><span data-stu-id="f8753-366">The aggregate view and the detail view of the report allow for 90 days of filtering.</span></span>

<span data-ttu-id="f8753-367">Pour afficher le rapport, ouvrez le [Centre de sécurité & conformité](https://protection.office.com), accédez **Reports** au \> **tableau de bord** rapports et sélectionnez **Envoyer et recevoir un message**.</span><span class="sxs-lookup"><span data-stu-id="f8753-367">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Sent and received email**.</span></span> <span data-ttu-id="f8753-368">Pour accéder directement au rapport, ouvrez <https://protection.office.com/reportv2?id=SentAndReceivedMailATP> .</span><span class="sxs-lookup"><span data-stu-id="f8753-368">To go directly to the report, open <https://protection.office.com/reportv2?id=SentAndReceivedMailATP>.</span></span>

![Widget courrier électronique envoyé et reçu dans le tableau de bord rapports](../../media/sent-and-received-email-report-widget.png)

### <a name="report-view-for-the-sent-and-received-email-report"></a><span data-ttu-id="f8753-370">Affichage de rapport pour le rapport de courrier électronique envoyé et reçu</span><span class="sxs-lookup"><span data-stu-id="f8753-370">Report view for the Sent and received email report</span></span>

<span data-ttu-id="f8753-371">Les graphiques suivants sont disponibles dans l’affichage rapport :</span><span class="sxs-lookup"><span data-stu-id="f8753-371">The following charts are available in the report view:</span></span>

- <span data-ttu-id="f8753-372">**Décomposer en : type**: le graphique affiche toutes les catégories disponibles :</span><span class="sxs-lookup"><span data-stu-id="f8753-372">**Break down by: Type**: The chart shows all available categories:</span></span>

  - <span data-ttu-id="f8753-373">**Total**</span><span class="sxs-lookup"><span data-stu-id="f8753-373">**Total**</span></span>
  - <span data-ttu-id="f8753-374">**Courrier électronique approprié**</span><span class="sxs-lookup"><span data-stu-id="f8753-374">**Good mail**</span></span>
  - <span data-ttu-id="f8753-375">**Programme malveillant (blocage des programmes malveillants)** (EoP)</span><span class="sxs-lookup"><span data-stu-id="f8753-375">**Malware (anti-malware)** (EOP)</span></span>
  - <span data-ttu-id="f8753-376">**Détections de courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="f8753-376">**Spam detections**</span></span>
  - <span data-ttu-id="f8753-377">**Messages de règle**</span><span class="sxs-lookup"><span data-stu-id="f8753-377">**Rule messages**</span></span>
  - <span data-ttu-id="f8753-378">**Programme malveillant avancé** (Office 365 ATP)</span><span class="sxs-lookup"><span data-stu-id="f8753-378">**Advanced malware** (Office 365 ATP)</span></span>

  <span data-ttu-id="f8753-379">Lorsque vous placez le curseur de la souris sur un jour (point de données) dans le graphique, vous pouvez afficher les détails de ce jour.</span><span class="sxs-lookup"><span data-stu-id="f8753-379">When you hover over a day (data point) in the chart, you can see details for that day.</span></span>

  ![Type de vue dans le rapport des courriers électroniques envoyés et reçus](../../media/sent-and-received-email-report-type-view.png)

- <span data-ttu-id="f8753-381">**Décomposer en : sens**: le graphique indique le **total**, les données **entrantes**et **sortantes** .</span><span class="sxs-lookup"><span data-stu-id="f8753-381">**Break down by: Direction**: The chart shows **Total**, **Inbound**, and **Outbound** data.</span></span> <span data-ttu-id="f8753-382">Lorsque vous placez le curseur de la souris sur un jour (point de données) dans le graphique, vous pouvez afficher les détails de ce jour.</span><span class="sxs-lookup"><span data-stu-id="f8753-382">When you hover over a day (data point) in the chart, you can see details for that day.</span></span>

  ![Affichage de la direction dans le rapport de courrier électronique envoyé et reçu](../../media/sent-and-received-email-report-direction-view.png)

- <span data-ttu-id="f8753-384">**Explorer en détail** \> **Programme malveillant (anti-programme malveillant)**: cette sélection vous permet d’accéder aux [détections de programmes malveillants dans le rapport par courrier électronique](view-email-security-reports.md#malware-detections-in-email-report).</span><span class="sxs-lookup"><span data-stu-id="f8753-384">**Drill down by** \> **Malware (anti-malware)**: This selection takes you to the [Malware detections in email report](view-email-security-reports.md#malware-detections-in-email-report).</span></span>

- <span data-ttu-id="f8753-385">**Explorer en détail** \> **Détections de courrier indésirable)**: cette sélection vous permet d’accéder au [rapport des détections de courrier indésirable](view-email-security-reports.md#spam-detections-report).</span><span class="sxs-lookup"><span data-stu-id="f8753-385">**Drill down by** \> **Spam detections)**: This selection takes you to the [Spam Detections report](view-email-security-reports.md#spam-detections-report).</span></span>

<span data-ttu-id="f8753-386">Si vous cliquez sur **filtres** dans un affichage de rapport, vous pouvez modifier les résultats à l’aide des filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="f8753-386">If you click **Filters** in a report view, you can modify the results with the following filters:</span></span>

- <span data-ttu-id="f8753-387">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="f8753-387">**Start date** and **End date**</span></span>
- <span data-ttu-id="f8753-388">Valeurs de la direction</span><span class="sxs-lookup"><span data-stu-id="f8753-388">Direction values</span></span>
- <span data-ttu-id="f8753-389">Valeurs de type</span><span class="sxs-lookup"><span data-stu-id="f8753-389">Type values</span></span>

<span data-ttu-id="f8753-390">Pour revenir à l’affichage de rapport, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="f8753-390">To go back to the report view, click **View report**.</span></span>

### <a name="details-table-view-for-the-sent-and-received-email-report"></a><span data-ttu-id="f8753-391">Vue de la table des détails pour le rapport de courrier électronique envoyé et reçu</span><span class="sxs-lookup"><span data-stu-id="f8753-391">Details table view for the Sent and received email report</span></span>

<span data-ttu-id="f8753-392">Si vous cliquez sur **afficher les détails** de la table dans la fenêtre dépanner **par : direction** ou dépanner **par :** le mode de direction, les informations suivantes sont affichées :</span><span class="sxs-lookup"><span data-stu-id="f8753-392">If you click **View details table** in the **Break down by: Direction** or **Break down by: Direction** view, the following information is shown:</span></span>

- <span data-ttu-id="f8753-393">**Date (UTC)**</span><span class="sxs-lookup"><span data-stu-id="f8753-393">**Date (UTC)**</span></span>
- <span data-ttu-id="f8753-394">**Type**</span><span class="sxs-lookup"><span data-stu-id="f8753-394">**Type**</span></span>
- <span data-ttu-id="f8753-395">**Direction**</span><span class="sxs-lookup"><span data-stu-id="f8753-395">**Direction**</span></span>
- <span data-ttu-id="f8753-396">**Nombre de messages**</span><span class="sxs-lookup"><span data-stu-id="f8753-396">**Message count**</span></span>

<span data-ttu-id="f8753-397">Si vous cliquez sur **filtres** dans un affichage tableau détaillé, vous pouvez modifier les résultats à l’aide des filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="f8753-397">If you click **Filters** in a details table view, you can modify the results with the following filters:</span></span>

- <span data-ttu-id="f8753-398">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="f8753-398">**Start date** and **End date**</span></span>
- <span data-ttu-id="f8753-399">Valeurs de la direction</span><span class="sxs-lookup"><span data-stu-id="f8753-399">Direction values</span></span>
- <span data-ttu-id="f8753-400">Valeurs de type</span><span class="sxs-lookup"><span data-stu-id="f8753-400">Type values</span></span>

<span data-ttu-id="f8753-401">Pour revenir à l’affichage de rapport, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="f8753-401">To go back to the report view, click **View report**.</span></span>

## <a name="top-senders-and-recipients-report"></a><span data-ttu-id="f8753-402">Rapport des expéditeurs et des destinataires principaux</span><span class="sxs-lookup"><span data-stu-id="f8753-402">Top senders and recipients report</span></span>

<span data-ttu-id="f8753-403">Le rapport des **expéditeurs et des destinataires principaux** est un graphique en secteurs illustrant les principaux expéditeurs et destinataires de votre courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="f8753-403">The **Top senders and recipients** report is a pie chart showing your top email senders and recipients.</span></span>

<span data-ttu-id="f8753-404">Pour afficher le rapport, ouvrez le [Centre de sécurité & conformité](https://protection.office.com), accédez à **rapports** \> **Dashboard** et sélectionnez **principaux expéditeurs et destinataires**.</span><span class="sxs-lookup"><span data-stu-id="f8753-404">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Top senders and recipients**.</span></span> <span data-ttu-id="f8753-405">Pour accéder directement au rapport, ouvrez <https://protection.office.com/reportv2?id=TopSenderRecipientsATP> .</span><span class="sxs-lookup"><span data-stu-id="f8753-405">To go directly to the report, open <https://protection.office.com/reportv2?id=TopSenderRecipientsATP>.</span></span>

![Widget principaux expéditeurs et destinataires dans le tableau de bord rapports](../../media/top-senders-and-recipients-widget.png)

### <a name="report-view-for-the-top-senders-and-recipient-report"></a><span data-ttu-id="f8753-407">Affichage de rapport pour le rapport des expéditeurs et des destinataires principaux</span><span class="sxs-lookup"><span data-stu-id="f8753-407">Report view for the Top senders and recipient report</span></span>

<span data-ttu-id="f8753-408">Les graphiques suivants sont disponibles dans l’affichage rapport :</span><span class="sxs-lookup"><span data-stu-id="f8753-408">The following charts are available in the report view:</span></span>

- <span data-ttu-id="f8753-409">**Afficher les données des \> expéditeurs de messages principaux**</span><span class="sxs-lookup"><span data-stu-id="f8753-409">**Show data for \> Top mail senders**</span></span>
- <span data-ttu-id="f8753-410">**Afficher les données des \> destinataires de messagerie les plus fréquents**</span><span class="sxs-lookup"><span data-stu-id="f8753-410">**Show data for \> Top mail recipients**</span></span>
- <span data-ttu-id="f8753-411">**Afficher les données pour les \> destinataires de courrier indésirable principaux**</span><span class="sxs-lookup"><span data-stu-id="f8753-411">**Show data for \> Top spam recipients**</span></span>
- <span data-ttu-id="f8753-412">**Afficher les données pour \> Principaux destinataires de programmes malveillants** (EoP)</span><span class="sxs-lookup"><span data-stu-id="f8753-412">**Show data for \> Top malware recipients** (EOP)</span></span>
- <span data-ttu-id="f8753-413">**Afficher les données pour \> Principaux destinataires de programmes malveillants (ATP)** (Office 365 ATP)</span><span class="sxs-lookup"><span data-stu-id="f8753-413">**Show data for \> Top malware recipients (ATP)** (Office 365 ATP)</span></span>

<span data-ttu-id="f8753-414">La composition du graphique en secteurs est modifiée en fonction de ces sélections.</span><span class="sxs-lookup"><span data-stu-id="f8753-414">The composition of the pie chart changes based on these selections.</span></span>

<span data-ttu-id="f8753-415">Lorsque vous placez le curseur de la souris sur un coin du graphique en secteurs, vous pouvez voir le nombre de messages envoyés ou reçus.</span><span class="sxs-lookup"><span data-stu-id="f8753-415">When you hover over a wedge in the pie chart, you can see a count of messages sent or received.</span></span>

<span data-ttu-id="f8753-416">Si vous cliquez sur **filtres** dans un affichage de rapport, vous pouvez spécifier une plage de dates avec **Date de début** et date de **fin**.</span><span class="sxs-lookup"><span data-stu-id="f8753-416">If you click **Filters** in a report view, you can specify a date range with **Start date** and **End date**.</span></span>

![Graphique en secteurs en mode état dans le rapport des expéditeurs et destinataires principaux](../../media/top-senders-and-recipients-report-view.png)

### <a name="details-table-view-for-the-top-senders-and-recipient-report"></a><span data-ttu-id="f8753-418">Vue de la table Détails pour le rapport des expéditeurs et des destinataires principaux</span><span class="sxs-lookup"><span data-stu-id="f8753-418">Details table view for the Top senders and recipient report</span></span>

<span data-ttu-id="f8753-419">Si vous cliquez sur **afficher les détails table**, les informations affichées dépendent du graphique que vous examinez :</span><span class="sxs-lookup"><span data-stu-id="f8753-419">If you click **View details table**, the information that's shown depends on the chart you were looking at:</span></span>

- <span data-ttu-id="f8753-420">**Afficher les données des \> expéditeurs de messages principaux**</span><span class="sxs-lookup"><span data-stu-id="f8753-420">**Show data for \> Top mail senders**</span></span>

  - <span data-ttu-id="f8753-421">**Principaux expéditeurs de messagerie**</span><span class="sxs-lookup"><span data-stu-id="f8753-421">**Top mail senders**</span></span>
  - <span data-ttu-id="f8753-422">**Count**</span><span class="sxs-lookup"><span data-stu-id="f8753-422">**Count**</span></span>

- <span data-ttu-id="f8753-423">**Afficher les données des \> destinataires de messagerie les plus fréquents**</span><span class="sxs-lookup"><span data-stu-id="f8753-423">**Show data for \> Top mail recipients**</span></span>

  - <span data-ttu-id="f8753-424">**Principaux destinataires de messagerie**</span><span class="sxs-lookup"><span data-stu-id="f8753-424">**Top mail recipients**</span></span>
  - <span data-ttu-id="f8753-425">**Count**</span><span class="sxs-lookup"><span data-stu-id="f8753-425">**Count**</span></span>

- <span data-ttu-id="f8753-426">**Afficher les données pour les \> destinataires de courrier indésirable principaux**</span><span class="sxs-lookup"><span data-stu-id="f8753-426">**Show data for \> Top spam recipients**</span></span>

  - <span data-ttu-id="f8753-427">**Principaux destinataires de courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="f8753-427">**Top spam recipients**</span></span>
  - <span data-ttu-id="f8753-428">**Count**</span><span class="sxs-lookup"><span data-stu-id="f8753-428">**Count**</span></span>

- <span data-ttu-id="f8753-429">**Afficher les données pour \> Principaux destinataires de programmes malveillants** (EoP)</span><span class="sxs-lookup"><span data-stu-id="f8753-429">**Show data for \> Top malware recipients** (EOP)</span></span>

  - <span data-ttu-id="f8753-430">**Principaux destinataires de programmes malveillants**</span><span class="sxs-lookup"><span data-stu-id="f8753-430">**Top malware recipients**</span></span>
  - <span data-ttu-id="f8753-431">**Count**</span><span class="sxs-lookup"><span data-stu-id="f8753-431">**Count**</span></span>

- <span data-ttu-id="f8753-432">**Afficher les données pour \> Principaux destinataires de programmes malveillants (ATP)** (Office 365 ATP)</span><span class="sxs-lookup"><span data-stu-id="f8753-432">**Show data for \> Top malware recipients (ATP)** (Office 365 ATP)</span></span>

  - <span data-ttu-id="f8753-433">**Principaux destinataires de programmes malveillants (ATP)**</span><span class="sxs-lookup"><span data-stu-id="f8753-433">**Top malware recipients (ATP)**</span></span>
  - <span data-ttu-id="f8753-434">**Count**</span><span class="sxs-lookup"><span data-stu-id="f8753-434">**Count**</span></span>

<span data-ttu-id="f8753-435">Si vous cliquez sur **filtres** dans un affichage tableau détaillé, vous pouvez spécifier une plage de dates avec **Date de début** et date de **fin**.</span><span class="sxs-lookup"><span data-stu-id="f8753-435">If you click **Filters** in a details table view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="f8753-436">Pour revenir à l’affichage de rapport, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="f8753-436">To go back to the report view, click **View report**.</span></span>

## <a name="what-permissions-are-needed-to-view-these-reports"></a><span data-ttu-id="f8753-437">Quelles sont les autorisations nécessaires pour afficher ces rapports ?</span><span class="sxs-lookup"><span data-stu-id="f8753-437">What permissions are needed to view these reports?</span></span>

<span data-ttu-id="f8753-438">Pour afficher et utiliser les rapports, vous devez être membre du groupe de rôles spécifié dans le centre de sécurité & conformité **et** dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="f8753-438">To view and use the reports, you need to be a member of the specified role group in the Security & Compliance Center **and** in Exchange Online.</span></span>

- <span data-ttu-id="f8753-439">Dans le centre de sécurité & conformité, vous devez être membre de l’un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="f8753-439">In the Security & Compliance Center, you need to be a member of one of the following role groups:</span></span>

  <span data-ttu-id="f8753-440">-Gestion de l’organisation-administrateur de la sécurité (vous pouvez également le faire dans le [Centre d’administration Azure Active Directory](https://aad.portal.azure.com) -lecteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="f8753-440">-Organization Management -Security Administrator (you can also do this in the [Azure Active Directory admin center](https://aad.portal.azure.com) -Security Reader</span></span>

  <span data-ttu-id="f8753-441">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](https://docs.microsoft.com/microsoft-365/security/office-365-security/permissions-in-the-security-and-compliance-center).</span><span class="sxs-lookup"><span data-stu-id="f8753-441">For more information, see [Permissions in the Security & Compliance Center](https://docs.microsoft.com/microsoft-365/security/office-365-security/permissions-in-the-security-and-compliance-center).</span></span>

- <span data-ttu-id="f8753-442">Dans Exchange Online, vous devez être membre de l’un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="f8753-442">In Exchange Online, you need to be a member of one of the following role groups:</span></span>

  <span data-ttu-id="f8753-443">-Gestion de l’organisation-affichage uniquement-gestion de l’organisation-affichage uniquement des destinataires-gestion de la conformité</span><span class="sxs-lookup"><span data-stu-id="f8753-443">-Organization Management -View-only Organization Management -View-Only Recipients -Compliance Management</span></span>

<span data-ttu-id="f8753-444">Pour plus d’informations, consultez la rubrique [autorisations dans Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo) et [gérer les groupes de rôles dans Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/role-groups).</span><span class="sxs-lookup"><span data-stu-id="f8753-444">For more information, see [Permissions in Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo) and [Manage role groups in Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/role-groups).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8753-445">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f8753-445">Related topics</span></span>

[<span data-ttu-id="f8753-446">Rapports intelligents et aperçus dans le Centre de sécurité et conformité</span><span class="sxs-lookup"><span data-stu-id="f8753-446">Smart reports and insights in the Security & Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)

[<span data-ttu-id="f8753-447">Informations sur le flux de messagerie dans le centre de sécurité et conformité</span><span class="sxs-lookup"><span data-stu-id="f8753-447">Mail flow insights in the Security & Compliance Center</span></span>](mail-flow-insights-v2.md)

[<span data-ttu-id="f8753-448">Afficher les rapports de sécurité de courrier dans le centre de sécurité et conformité</span><span class="sxs-lookup"><span data-stu-id="f8753-448">View email security reports in the Security & Compliance Center</span></span>](view-email-security-reports.md)

[<span data-ttu-id="f8753-449">Afficher les rapports pour Office 365 protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="f8753-449">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)
