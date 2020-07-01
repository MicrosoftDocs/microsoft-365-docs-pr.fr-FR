---
title: Afficher les rapports de flux de messagerie dans le centre de sécurité & conformité
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: ''
ms.collection:
- M365-security-compliance
description: Découvrez comment rechercher et utiliser des rapports de sécurité de flux de messagerie pour votre organisation. Les rapports de flux de messagerie sont disponibles dans le centre de sécurité & conformité.
ms.custom: ''
ms.openlocfilehash: 70c96bb4f43edb80f98fdc98aa173fed9e54e7d7
ms.sourcegitcommit: c43ebb915fa0eb7eb720b21b62c0d1e58e7cde3d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2020
ms.locfileid: "44937182"
---
# <a name="view-mail-flow-reports-in-the-security--compliance-center"></a><span data-ttu-id="9385c-104">Afficher les rapports de flux de messagerie dans le centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="9385c-104">View mail flow reports in the Security & Compliance Center</span></span>

<span data-ttu-id="9385c-105">Outre les informations de [flux de messagerie](mail-flow-insights-v2.md) disponibles dans le centre de sécurité & conformité, différents rapports de flux de messagerie sont également disponibles pour vous aider à surveiller votre organisation Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="9385c-105">In addition to the [Mail flow insights](mail-flow-insights-v2.md) that are available in the Security & Compliance Center, a variety of mail flow reports are also available to help you monitor your Microsoft 365 organization.</span></span> <span data-ttu-id="9385c-106">Si vous disposez des [autorisations nécessaires](#what-permissions-are-needed-to-view-these-reports), vous pouvez afficher ces rapports dans le centre de sécurité & conformité à l' <https://office.protection.com> aide du tableau de **Reports** \> **bord**rapports.</span><span class="sxs-lookup"><span data-stu-id="9385c-106">If you have the [necessary permissions](#what-permissions-are-needed-to-view-these-reports), you can view these reports in the Security & Compliance Center at <https://office.protection.com> by going to **Reports** \> **Dashboard**.</span></span> <span data-ttu-id="9385c-107">Pour accéder directement au tableau de bord rapports, ouvrez <https://office.protection.office.com/insightdashboard> .</span><span class="sxs-lookup"><span data-stu-id="9385c-107">To go directly to the reports dashboard, open <https://office.protection.office.com/insightdashboard>.</span></span>

![Tableau de bord des rapports dans le centre de sécurité & conformité](../../media/6b213d34-adbb-44af-8549-be9a7e2db087.png)

## <a name="connector-report"></a><span data-ttu-id="9385c-109">Rapport de connecteur</span><span class="sxs-lookup"><span data-stu-id="9385c-109">Connector report</span></span>

<span data-ttu-id="9385c-110">Le **rapport de connecteur** affiche l’activité de flux de messagerie sur les connecteurs entrants [et sortants](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow) configurés pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="9385c-110">The **Connector report** shows mail flow activity on the [inbound and outbound connectors](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow) that are configured for your organization.</span></span>

<span data-ttu-id="9385c-111">Pour afficher le rapport, ouvrez le [Centre de sécurité & conformité](https://protection.office.com), accédez **Reports** au \> **tableau de bord** rapports et sélectionnez rapport de **connecteur**.</span><span class="sxs-lookup"><span data-stu-id="9385c-111">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Connector report**.</span></span> <span data-ttu-id="9385c-112">Pour accéder directement au rapport, ouvrez <https://protection.office.com/reportv2?id=ConnectorReport> .</span><span class="sxs-lookup"><span data-stu-id="9385c-112">To go directly to the report, open <https://protection.office.com/reportv2?id=ConnectorReport>.</span></span>

![Widget rapport de connecteur dans le tableau de bord rapports](../../media/connector-report-widget.png)

### <a name="report-view-for-the-connector-report"></a><span data-ttu-id="9385c-114">Affichage de rapport pour le rapport de connecteur</span><span class="sxs-lookup"><span data-stu-id="9385c-114">Report view for the Connector report</span></span>

<span data-ttu-id="9385c-115">Les graphiques suivants sont disponibles en mode état :</span><span class="sxs-lookup"><span data-stu-id="9385c-115">The following charts are available in report view:</span></span>

- <span data-ttu-id="9385c-116">**Afficher les données par : flux de messagerie**: ce graphique indique le nombre de messages entrants et sortants organisés par :</span><span class="sxs-lookup"><span data-stu-id="9385c-116">**View data by: Mail flow**: This chart shows the number of inbound and outbound messages organized by:</span></span>

  - <span data-ttu-id="9385c-117">**Total**</span><span class="sxs-lookup"><span data-stu-id="9385c-117">**Total**</span></span>
  - <span data-ttu-id="9385c-118">**À partir d’Internet sans connecteur**</span><span class="sxs-lookup"><span data-stu-id="9385c-118">**From the internet without a connector**</span></span>
  - <span data-ttu-id="9385c-119">**Sur Internet sans connecteur**</span><span class="sxs-lookup"><span data-stu-id="9385c-119">**To the internet without a connector**</span></span>
  - <span data-ttu-id="9385c-120">Un connecteur spécifique que vous avez configuré.</span><span class="sxs-lookup"><span data-stu-id="9385c-120">A specific connector that you've configured.</span></span>
  
  <span data-ttu-id="9385c-121">Pour isoler les données du graphique, utilisez l’option **afficher les données pour** le contrôle pour sélectionner une de ces options ou **tout le flux de messagerie**.</span><span class="sxs-lookup"><span data-stu-id="9385c-121">To isolate the data in the chart, use the **Show data for** control to select one of these options or **All mail flow**.</span></span>

  ![Afficher les données par flux de messagerie dans le rapport du connecteur](../../media/connector-report-view-data-by-mail-flow.png)

- <span data-ttu-id="9385c-123">**Afficher les données par : utilisation de TLS**: ce graphique indique le pourcentage d’utilisation de la version TLS (Transport Layer Security) pour le flux de messagerie.</span><span class="sxs-lookup"><span data-stu-id="9385c-123">**View data by: TLS usage**: This chart shows the percentage of Transport Layer Security (TLS) version usage for mail flow.</span></span>

  <span data-ttu-id="9385c-124">Pour isoler les données dans le graphique, utilisez l’option **afficher les données pour** le contrôle afin de sélectionner l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="9385c-124">To isolate the data in the chart, use the **Show data for** control to select one of the following options:</span></span>

  - <span data-ttu-id="9385c-125">**Tout le flux de messagerie**</span><span class="sxs-lookup"><span data-stu-id="9385c-125">**All mail flow**</span></span>
  - <span data-ttu-id="9385c-126">**À partir d’Internet sans connecteur**</span><span class="sxs-lookup"><span data-stu-id="9385c-126">**From the internet without a connector**</span></span>
  - <span data-ttu-id="9385c-127">**Sur Internet sans connecteur**</span><span class="sxs-lookup"><span data-stu-id="9385c-127">**To the internet without a connector**</span></span>
  - <span data-ttu-id="9385c-128">Un connecteur spécifique que vous avez configuré.</span><span class="sxs-lookup"><span data-stu-id="9385c-128">A specific connector that you've configured.</span></span>

  ![Afficher les données par utilisation de TLS dans le rapport de connecteur](../../media/connector-report-view-data-by-tls-usage.png)

<span data-ttu-id="9385c-130">Si vous cliquez sur **filtres** dans un affichage de rapport, vous pouvez spécifier une plage de dates avec **Date de début** et date de **fin**.</span><span class="sxs-lookup"><span data-stu-id="9385c-130">If you click **Filters** in a report view, you can specify a date range with **Start date** and **End date**.</span></span>

### <a name="details-table-view-for-the-connector-report"></a><span data-ttu-id="9385c-131">Vue de la table Détails pour le rapport de connecteur</span><span class="sxs-lookup"><span data-stu-id="9385c-131">Details table view for the Connector report</span></span>

<span data-ttu-id="9385c-132">Si vous cliquez sur **afficher la table des détails** dans un affichage de rapport, les informations suivantes s’affichent :</span><span class="sxs-lookup"><span data-stu-id="9385c-132">If you click **View details table** in a report view, the following information is shown:</span></span>

- <span data-ttu-id="9385c-133">**Date**</span><span class="sxs-lookup"><span data-stu-id="9385c-133">**Date**</span></span>
- <span data-ttu-id="9385c-134">**Nom et direction du connecteur**</span><span class="sxs-lookup"><span data-stu-id="9385c-134">**Connector direction and name**</span></span>
- <span data-ttu-id="9385c-135">**Type de connecteur**</span><span class="sxs-lookup"><span data-stu-id="9385c-135">**Connector type**</span></span>
- <span data-ttu-id="9385c-136">**TLS forcé ?**: valeur **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="9385c-136">**Forced TLS?**: The value **True** or **False**.</span></span>
- <span data-ttu-id="9385c-137">**Pas de TLS** (pourcentage)</span><span class="sxs-lookup"><span data-stu-id="9385c-137">**No TLS** (percentage)</span></span>
- <span data-ttu-id="9385c-138">**TLS 1,0** (pourcentage)</span><span class="sxs-lookup"><span data-stu-id="9385c-138">**TLS 1.0** (percentage)</span></span>
- <span data-ttu-id="9385c-139">**TLS 1,1** (pourcentage)</span><span class="sxs-lookup"><span data-stu-id="9385c-139">**TLS 1.1** (percentage)</span></span>
- <span data-ttu-id="9385c-140">**TLS 1,2** (pourcentage)</span><span class="sxs-lookup"><span data-stu-id="9385c-140">**TLS 1.2** (percentage)</span></span>
- <span data-ttu-id="9385c-141">**Volume**: nombre de messages.</span><span class="sxs-lookup"><span data-stu-id="9385c-141">**Volume**: The number of messages.</span></span>

<span data-ttu-id="9385c-142">Si vous cliquez sur **filtres** dans un affichage tableau détaillé, vous pouvez spécifier une plage de dates avec **Date de début** et date de **fin**.</span><span class="sxs-lookup"><span data-stu-id="9385c-142">If you click **Filters** in a details table view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="9385c-143">Pour revenir à l’affichage de rapport, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="9385c-143">To go back to the report view, click **View report**.</span></span>

## <a name="exchange-transport-rule-report"></a><span data-ttu-id="9385c-144">Rapport de règle de transport Exchange</span><span class="sxs-lookup"><span data-stu-id="9385c-144">Exchange transport rule report</span></span>

<span data-ttu-id="9385c-145">Le rapport des règles de **transport Exchange** affiche l’effet des règles de flux de messagerie (également appelées règles de transport) sur les messages entrants et sortants dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="9385c-145">The **Exchange transport rule report** shows the effect of mail flow rules (also known as transport rules) on incoming and outgoing messages in your organization.</span></span>

<span data-ttu-id="9385c-146">Pour afficher le rapport, ouvrez le [Centre de sécurité & conformité](https://protection.office.com), accédez **Reports** au \> **tableau de bord** rapports et sélectionnez **règle de transport Exchange**.</span><span class="sxs-lookup"><span data-stu-id="9385c-146">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Exchange Transport rule**.</span></span> <span data-ttu-id="9385c-147">Pour accéder directement au rapport, ouvrez <https://protection.office.com/reportv2?id=ETRRuleReport> .</span><span class="sxs-lookup"><span data-stu-id="9385c-147">To go directly to the report, open <https://protection.office.com/reportv2?id=ETRRuleReport>.</span></span>

![Widget règle de transport Exchange dans le tableau de bord rapports](../../media/transport-rule-report-widget.png)

### <a name="report-view-for-the-exchange-transport-rule-report"></a><span data-ttu-id="9385c-149">Affichage de rapport pour le rapport des règles de transport Exchange</span><span class="sxs-lookup"><span data-stu-id="9385c-149">Report view for the Exchange transport rule report</span></span>

<span data-ttu-id="9385c-150">Les graphiques suivants sont disponibles en mode état :</span><span class="sxs-lookup"><span data-stu-id="9385c-150">The following charts are available in report view:</span></span>

- <span data-ttu-id="9385c-151">**Afficher les données par : règles** \> de transport Exchange **Décomposer en : sens**: ce graphique indique le **nombre de messages entrants** et **sortants** affectés par les règles de transport.</span><span class="sxs-lookup"><span data-stu-id="9385c-151">**View data by: Exchange transport rules** \> **Break down by: Direction**: This chart shows the number of **Inbound** and **Outbound** messages that were affected by transport rules.</span></span>

- <span data-ttu-id="9385c-152">**Afficher les données par : règles** \> de transport Exchange Dépanner **par : gravité**: ce graphique indique le nombre de messages de gravité **élevée** et de gravité **moyenne**, ainsi que les messages à **faible gravité** .</span><span class="sxs-lookup"><span data-stu-id="9385c-152">**View data by: Exchange transport rules** \> **Break down by: Severity**: This chart shows the number of **High severity** and **Medium severity**, and **Low severity** messages.</span></span> <span data-ttu-id="9385c-153">Vous définissez le niveau de gravité en tant qu’action dans la règle (**auditez cette règle avec le niveau de gravité** ou _SetAuditSeverity_).</span><span class="sxs-lookup"><span data-stu-id="9385c-153">You set the severity level as an action in the rule (**Audit this rule with severity level** or _SetAuditSeverity_).</span></span> <span data-ttu-id="9385c-154">Pour plus d’informations, consultez la rubrique [actions de règle de flux de messagerie dans Exchange Online](https://docs.microsoft.com//Exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions).</span><span class="sxs-lookup"><span data-stu-id="9385c-154">For more information, see [Mail flow rule actions in Exchange Online](https://docs.microsoft.com//Exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions).</span></span>

- <span data-ttu-id="9385c-155">**Afficher les données par : DLP Exchange transport Rules** \> **Décomposer en : sens**: ce graphique indique le **nombre de messages entrants** et **sortants** affectés par les règles de transport de la protection contre la perte de données (DLP).</span><span class="sxs-lookup"><span data-stu-id="9385c-155">**View data by: DLP Exchange transport rules** \> **Break down by: Direction**: This chart shows the number of **Inbound** and **Outbound** messages that were affected by data loss prevention (DLP) transport rules.</span></span> <span data-ttu-id="9385c-156">Vous pouvez affiner le graphique en sélectionnant l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="9385c-156">You can further refine the chart by selecting on of the following options:</span></span>

  - <span data-ttu-id="9385c-157">**Afficher les données pour : toutes les règles de transport DLP**</span><span class="sxs-lookup"><span data-stu-id="9385c-157">**Show data for: All DLP transport rules**</span></span>
  - <span data-ttu-id="9385c-158">**Afficher les données de : utilisateurs compromis**</span><span class="sxs-lookup"><span data-stu-id="9385c-158">**Show data for: Compromised users**</span></span>
  - <span data-ttu-id="9385c-159">**Afficher les données pour : faible volume de contenu détecté par les États-Unis Patriot Act**</span><span class="sxs-lookup"><span data-stu-id="9385c-159">**Show data for: Low volume of content detected U.S. Patriot Act**</span></span>

- <span data-ttu-id="9385c-160">**Afficher les données par : DLP Exchange transport Rules** \> **Décomposer en : sens**: cette vue indique le nombre de messages de gravité **élevée** et de gravité **moyenne**, ainsi que les messages à **faible gravité** qui ont été affectés par les règles de transport DLP.</span><span class="sxs-lookup"><span data-stu-id="9385c-160">**View data by: DLP Exchange transport rules** \> **Break down by: Direction**: This view shows the number of **High severity** and **Medium severity**, and **Low severity** messages that were affected by DLP transport rules.</span></span> <span data-ttu-id="9385c-161">Vous pouvez affiner le graphique en sélectionnant l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="9385c-161">You can further refine the chart by selecting on of the following options:</span></span>

  - <span data-ttu-id="9385c-162">**Afficher les données pour : toutes les règles de transport DLP**</span><span class="sxs-lookup"><span data-stu-id="9385c-162">**Show data for: All DLP transport rules**</span></span>
  - <span data-ttu-id="9385c-163">**Afficher les données de : utilisateurs compromis**</span><span class="sxs-lookup"><span data-stu-id="9385c-163">**Show data for: Compromised users**</span></span>
  - <span data-ttu-id="9385c-164">**Afficher les données pour : faible volume de contenu détecté par les États-Unis Patriot Act**</span><span class="sxs-lookup"><span data-stu-id="9385c-164">**Show data for: Low volume of content detected U.S. Patriot Act**</span></span>

<span data-ttu-id="9385c-165">Si vous cliquez sur **filtres** dans un affichage de rapport, vous pouvez modifier les résultats à l’aide des filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="9385c-165">If you click **Filters** in a report view, you can modify the results with the following filters::</span></span>

- <span data-ttu-id="9385c-166">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="9385c-166">**Start date** and **End date**</span></span>
- <span data-ttu-id="9385c-167">Valeurs de la direction</span><span class="sxs-lookup"><span data-stu-id="9385c-167">Direction values</span></span>
- <span data-ttu-id="9385c-168">Valeurs de gravité</span><span class="sxs-lookup"><span data-stu-id="9385c-168">Severity values</span></span>

![Affichage de rapport dans le rapport des règles de transport Exchange](../../media/transport-rule-report-report-view.png)

### <a name="details-table-view-for-the-exchange-transport-rule-report"></a><span data-ttu-id="9385c-170">Vue de la table Détails pour le rapport des règles de transport Exchange</span><span class="sxs-lookup"><span data-stu-id="9385c-170">Details table view for the Exchange transport rule report</span></span>

<span data-ttu-id="9385c-171">Si vous cliquez sur **afficher les détails table**, les informations affichées dépendent du graphique que vous examinez :</span><span class="sxs-lookup"><span data-stu-id="9385c-171">If you click **View details table**, the information that's shown depends on the chart you were looking at:</span></span>

- <span data-ttu-id="9385c-172">**Afficher les données par : règles de transport Exchange**:</span><span class="sxs-lookup"><span data-stu-id="9385c-172">**View data by: Exchange Transport rules**:</span></span>

  - <span data-ttu-id="9385c-173">**Date**</span><span class="sxs-lookup"><span data-stu-id="9385c-173">**Date**</span></span>
  - <span data-ttu-id="9385c-174">**Règle de transport**</span><span class="sxs-lookup"><span data-stu-id="9385c-174">**Transport rule**</span></span>
  - <span data-ttu-id="9385c-175">**Subject**</span><span class="sxs-lookup"><span data-stu-id="9385c-175">**Subject**</span></span>
  - <span data-ttu-id="9385c-176">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="9385c-176">**Sender address**</span></span>
  - <span data-ttu-id="9385c-177">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="9385c-177">**Recipient address**</span></span>
  - <span data-ttu-id="9385c-178">**Gravité**</span><span class="sxs-lookup"><span data-stu-id="9385c-178">**Severity**</span></span>
  - <span data-ttu-id="9385c-179">**Direction**</span><span class="sxs-lookup"><span data-stu-id="9385c-179">**Direction**</span></span>

- <span data-ttu-id="9385c-180">**Afficher les données par : DLP Exchange transport Rules**:</span><span class="sxs-lookup"><span data-stu-id="9385c-180">**View data by: DLP Exchange transport rules**:</span></span>

  - <span data-ttu-id="9385c-181">**Date**</span><span class="sxs-lookup"><span data-stu-id="9385c-181">**Date**</span></span>
  - <span data-ttu-id="9385c-182">**Stratégie DLP**</span><span class="sxs-lookup"><span data-stu-id="9385c-182">**DLP policy**</span></span>
  - <span data-ttu-id="9385c-183">**Règle de transport**</span><span class="sxs-lookup"><span data-stu-id="9385c-183">**Transport rule**</span></span>
  - <span data-ttu-id="9385c-184">**Subject**</span><span class="sxs-lookup"><span data-stu-id="9385c-184">**Subject**</span></span>
  - <span data-ttu-id="9385c-185">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="9385c-185">**Sender address**</span></span>
  - <span data-ttu-id="9385c-186">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="9385c-186">**Recipient address**</span></span>
  - <span data-ttu-id="9385c-187">**Gravité**</span><span class="sxs-lookup"><span data-stu-id="9385c-187">**Severity**</span></span>
  - <span data-ttu-id="9385c-188">**Direction**</span><span class="sxs-lookup"><span data-stu-id="9385c-188">**Direction**</span></span>

<span data-ttu-id="9385c-189">Si vous cliquez sur **filtres** dans un affichage tableau détaillé, vous pouvez modifier les résultats à l’aide des filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="9385c-189">If you click **Filters** in a details table view, you can modify the results with the following filters:</span></span>

- <span data-ttu-id="9385c-190">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="9385c-190">**Start date** and **End date**</span></span>
- <span data-ttu-id="9385c-191">Valeurs de la direction</span><span class="sxs-lookup"><span data-stu-id="9385c-191">Direction values</span></span>
- <span data-ttu-id="9385c-192">Valeurs de gravité</span><span class="sxs-lookup"><span data-stu-id="9385c-192">Severity values</span></span>

<span data-ttu-id="9385c-193">Pour revenir à l’affichage de rapport, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="9385c-193">To go back to the report view, click **View report**.</span></span>

## <a name="forwarding-report"></a><span data-ttu-id="9385c-194">Rapport de transfert</span><span class="sxs-lookup"><span data-stu-id="9385c-194">Forwarding report</span></span>

<span data-ttu-id="9385c-195">Le **rapport de transfert** indique que les messages envoyés par votre organisation sont transférés automatiquement vers des domaines externes à partir de boîtes aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="9385c-195">The **Forwarding report** shows your organization's automatically forwarded messages to external domains from Exchange Online mailboxes.</span></span> <span data-ttu-id="9385c-196">Les messages transférés peuvent présenter un risque de sécurité ou de conformité, et peuvent indiquer un compte compromis.</span><span class="sxs-lookup"><span data-stu-id="9385c-196">Forwarded messages can pose a security or compliance risk, and might indicate a compromised account.</span></span>

<span data-ttu-id="9385c-197">Pour afficher le rapport, ouvrez le [Centre de sécurité & conformité](https://protection.office.com), cliquez sur **rapports** de \> **tableau de bord** et sélectionnez rapport de **transfert**.</span><span class="sxs-lookup"><span data-stu-id="9385c-197">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Forwarding report**.</span></span> <span data-ttu-id="9385c-198">Pour accéder directement au rapport, ouvrez <https://protection.office.com/reportv2?id=MailFlowForwarding> .</span><span class="sxs-lookup"><span data-stu-id="9385c-198">To go directly to the report, open <https://protection.office.com/reportv2?id=MailFlowForwarding>.</span></span>

![Widget rapport de transfert dans le tableau de bord rapports](../../media/forwarding-report-widget.png)

### <a name="report-view-for-the-forwarding-report"></a><span data-ttu-id="9385c-200">Affichage de rapport pour le rapport de transfert</span><span class="sxs-lookup"><span data-stu-id="9385c-200">Report view for the Forwarding report</span></span>

<span data-ttu-id="9385c-201">Les graphiques suivants sont disponibles dans l’affichage rapport :</span><span class="sxs-lookup"><span data-stu-id="9385c-201">The following charts are available in the report view:</span></span>

- <span data-ttu-id="9385c-202">**Afficher les données pour : méthodes de transfert**: les méthodes suivantes sont affichées :</span><span class="sxs-lookup"><span data-stu-id="9385c-202">**Show data for: Forwarding methods**: The following methods are shown:</span></span>

  - <span data-ttu-id="9385c-203">**Règle de transport**: également appelée [règles de flux de messagerie](https://docs.microsoft.com/Exchange/security-and-compliance/mail-flow-rules/mail-flow-rules).</span><span class="sxs-lookup"><span data-stu-id="9385c-203">**Transport rule**: Also known as [mail flow rules](https://docs.microsoft.com/Exchange/security-and-compliance/mail-flow-rules/mail-flow-rules).</span></span>
  - <span data-ttu-id="9385c-204">**Règle de boîte aux lettres**: également appelée règles de boîte de [réception](https://support.microsoft.com/office/c24f5dea-9465-4df4-ad17-a50704d66c59).</span><span class="sxs-lookup"><span data-stu-id="9385c-204">**Mailbox rule**: Also known as [Inbox rules](https://support.microsoft.com/office/c24f5dea-9465-4df4-ad17-a50704d66c59).</span></span>

  ![Vue des méthodes de transfert dans le rapport de transfert](../../media/forwarding-report-forwarding-methods.png)

- <span data-ttu-id="9385c-206">**Afficher les données pour : transferts de domaines**: cette vue affiche les domaines de destinataire qui sont les destinations pour le transfert.</span><span class="sxs-lookup"><span data-stu-id="9385c-206">**Show data for: Forwarding domains**: This view shows the recipient domains that are the destinations for forwarding.</span></span>

  ![Vue des domaines de transfert dans le rapport de transfert](../../media/forwarding-report-forwarding-domains.png)

- <span data-ttu-id="9385c-208">**Afficher les données : redirecteurs**: les redirecteurs suivants sont affichés :</span><span class="sxs-lookup"><span data-stu-id="9385c-208">**Show data for: Forwarders**: The following forwarders are shown:</span></span>

  - <span data-ttu-id="9385c-209">**Règle de transport**</span><span class="sxs-lookup"><span data-stu-id="9385c-209">**Transport rule**</span></span>
  - <span data-ttu-id="9385c-210">Boîte aux lettres qui contient la règle de boîte de réception de transfert.</span><span class="sxs-lookup"><span data-stu-id="9385c-210">The mailbox that contains the forwarding Inbox rule.</span></span>

  ![Vue redirecteurs dans le rapport de transfert](../../media/forwarding-report-forwarders.png)

<span data-ttu-id="9385c-212">Si vous cliquez sur **filtres** dans un affichage de rapport, vous pouvez spécifier une plage de dates avec **Date de début** et date de **fin**.</span><span class="sxs-lookup"><span data-stu-id="9385c-212">If you click **Filters** in a report view, you can specify a date range with **Start date** and **End date**.</span></span>

### <a name="details-table-view-for-the-forwarding-report"></a><span data-ttu-id="9385c-213">Vue de la table Détails pour le rapport de transfert</span><span class="sxs-lookup"><span data-stu-id="9385c-213">Details table view for the Forwarding report</span></span>

<span data-ttu-id="9385c-214">Si vous cliquez sur **afficher la table des détails** dans un affichage de rapport, les informations suivantes s’affichent :</span><span class="sxs-lookup"><span data-stu-id="9385c-214">If you click **View details table** in a report view, the following information is shown:</span></span>

- <span data-ttu-id="9385c-215">**Redirecteurs**: la **règle de transport** value ou la boîte aux lettres qui contient la règle de boîte de réception de transfert.</span><span class="sxs-lookup"><span data-stu-id="9385c-215">**Forwarders**: The value **Transport rule** or the mailbox that contains the forwarding Inbox rule.</span></span>
- <span data-ttu-id="9385c-216">**Type de transfert**: règle de la **boîte aux lettres** ou **règle de transport**.</span><span class="sxs-lookup"><span data-stu-id="9385c-216">**Forwarding type**: The value **Mailbox rule** or **Transport rule**.</span></span>
- <span data-ttu-id="9385c-217">**Nom du destinataire**</span><span class="sxs-lookup"><span data-stu-id="9385c-217">**Recipient name**</span></span>
- <span data-ttu-id="9385c-218">**Domaine du destinataire**</span><span class="sxs-lookup"><span data-stu-id="9385c-218">**Recipient domain**</span></span>
- <span data-ttu-id="9385c-219">**Détails**: il s’agit de la valeur GUID de la règle de flux de messagerie ou de la valeur RuleIdentity de la règle de boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="9385c-219">**Details**: This is the GUID value of the mail flow rule, or the RuleIdentity value of the Inbox rule.</span></span>
- <span data-ttu-id="9385c-220">**Count**</span><span class="sxs-lookup"><span data-stu-id="9385c-220">**Count**</span></span>
- <span data-ttu-id="9385c-221">**Première date de transfert**</span><span class="sxs-lookup"><span data-stu-id="9385c-221">**First forward date**</span></span>

<span data-ttu-id="9385c-222">Si vous cliquez sur **filtres** dans un affichage tableau détaillé, vous pouvez spécifier une plage de dates avec **Date de début** et date de **fin**.</span><span class="sxs-lookup"><span data-stu-id="9385c-222">If you click **Filters** in a details table view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="9385c-223">Pour revenir à l’affichage rapports, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="9385c-223">To go back to the reports view, click **View report**.</span></span>

## <a name="mailflow-status-report"></a><span data-ttu-id="9385c-224">Rapport d’état de flux de flux</span><span class="sxs-lookup"><span data-stu-id="9385c-224">Mailflow status report</span></span>

<span data-ttu-id="9385c-225">Le **rapport d’état de flux** de messagerie est similaire au [rapport de courrier électronique envoyé et reçu](#sent-and-received-email-report), avec des informations supplémentaires sur le courrier électronique autorisé ou bloqué sur le serveur Edge.</span><span class="sxs-lookup"><span data-stu-id="9385c-225">The **Mailflow status report** is similar to the [Sent and received email report](#sent-and-received-email-report), with additional information about email allowed or blocked on the edge.</span></span> <span data-ttu-id="9385c-226">Il s’agit du seul rapport qui contient les informations de protection du serveur Edge et indique le nombre de messages bloqués avant d’être autorisés dans le service pour l’évaluation par Exchange Online Protection (EOP).</span><span class="sxs-lookup"><span data-stu-id="9385c-226">This is the only report that contains edge protection information, and shows just how much email is blocked before being allowed into the service for evaluation by Exchange Online Protection (EOP).</span></span>

<span data-ttu-id="9385c-227">Pour afficher le rapport, ouvrez le [Centre de sécurité & conformité](https://protection.office.com), accédez **Reports** au \> **tableau de bord** rapports et sélectionnez rapport d’État du **flux de flux**.</span><span class="sxs-lookup"><span data-stu-id="9385c-227">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Mailflow status report**.</span></span> <span data-ttu-id="9385c-228">Pour accéder directement au **rapport d’État du flux de messagerie**, ouvrez <https://protection.office.com/mailflowStatusReport> .</span><span class="sxs-lookup"><span data-stu-id="9385c-228">To go directly to the **Mail flow status report**, open <https://protection.office.com/mailflowStatusReport>.</span></span>

![Widget rapport d’état de flux de notification dans le tableau de bord rapports](../../media/mail-flow-status-report-widget.png)

### <a name="type-view-for-the-mailflow-status-report"></a><span data-ttu-id="9385c-230">Vue type pour le rapport d’état de flux de flux</span><span class="sxs-lookup"><span data-stu-id="9385c-230">Type view for the Mailflow status report</span></span>

<span data-ttu-id="9385c-231">Lorsque vous ouvrez le rapport, l’onglet **type** est sélectionné par défaut.</span><span class="sxs-lookup"><span data-stu-id="9385c-231">When you open the report, the **Type** tab is selected by default.</span></span> <span data-ttu-id="9385c-232">Par défaut, cette vue contient un graphique et une table de données configurée avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="9385c-232">By default, this view contains a chart and a data table that's configured with the following filters:</span></span>

- <span data-ttu-id="9385c-233">**Date**: les 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="9385c-233">**Date**: The last 7 days.</span></span>
- <span data-ttu-id="9385c-234">**Sens**:</span><span class="sxs-lookup"><span data-stu-id="9385c-234">**Direction**:</span></span>

  - <span data-ttu-id="9385c-235">**Entrants**</span><span class="sxs-lookup"><span data-stu-id="9385c-235">**Inbound**</span></span>
  - <span data-ttu-id="9385c-236">**Sortant**</span><span class="sxs-lookup"><span data-stu-id="9385c-236">**Outbound**</span></span>
  - <span data-ttu-id="9385c-237">**Intra-org** (compté indépendamment des **ports entrants et** **sortants**)</span><span class="sxs-lookup"><span data-stu-id="9385c-237">**Intra-org** (counted separately from **Inbound** and **Outbound**)</span></span>

- <span data-ttu-id="9385c-238">**Type**:</span><span class="sxs-lookup"><span data-stu-id="9385c-238">**Type**:</span></span>

  - <span data-ttu-id="9385c-239">**Courrier électronique approprié**</span><span class="sxs-lookup"><span data-stu-id="9385c-239">**Good mail**</span></span>
  - <span data-ttu-id="9385c-240">**Programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="9385c-240">**Malware**</span></span>
  - <span data-ttu-id="9385c-241">**Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="9385c-241">**Spam**</span></span>
  - <span data-ttu-id="9385c-242">**Protection des serveurs Edge**</span><span class="sxs-lookup"><span data-stu-id="9385c-242">**Edge protection**</span></span>
  - <span data-ttu-id="9385c-243">**Messages de règle**</span><span class="sxs-lookup"><span data-stu-id="9385c-243">**Rule messages**</span></span>
  - <span data-ttu-id="9385c-244">**Courriers hameçons**</span><span class="sxs-lookup"><span data-stu-id="9385c-244">**Phishing email**</span></span>

<span data-ttu-id="9385c-245">Le graphique est organisé selon les valeurs de **type** .</span><span class="sxs-lookup"><span data-stu-id="9385c-245">The chart is organized by the **Type** values.</span></span>

<span data-ttu-id="9385c-246">Vous pouvez modifier ces filtres en cliquant sur **Filtrer** ou en cliquant sur une valeur dans la légende du graphique.</span><span class="sxs-lookup"><span data-stu-id="9385c-246">You can changes these filters by clicking **Filter** or by clicking a value in the chart legend.</span></span>

<span data-ttu-id="9385c-247">Le tableau de données contient les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="9385c-247">The data table contains the following information:</span></span>

- <span data-ttu-id="9385c-248">**Direction**</span><span class="sxs-lookup"><span data-stu-id="9385c-248">**Direction**</span></span>
- <span data-ttu-id="9385c-249">**Type**</span><span class="sxs-lookup"><span data-stu-id="9385c-249">**Type**</span></span>
- <span data-ttu-id="9385c-250">**24 heures**</span><span class="sxs-lookup"><span data-stu-id="9385c-250">**24 hours**</span></span>
- <span data-ttu-id="9385c-251">**3 jours**</span><span class="sxs-lookup"><span data-stu-id="9385c-251">**3 days**</span></span>
- <span data-ttu-id="9385c-252">**7 jours**</span><span class="sxs-lookup"><span data-stu-id="9385c-252">**7 days**</span></span>
- <span data-ttu-id="9385c-253">**15 jours**</span><span class="sxs-lookup"><span data-stu-id="9385c-253">**15 days**</span></span>
- <span data-ttu-id="9385c-254">**30 jours**</span><span class="sxs-lookup"><span data-stu-id="9385c-254">**30 days**</span></span>

<span data-ttu-id="9385c-255">Si vous cliquez sur **choisir une catégorie pour plus d’informations**, vous pouvez sélectionner l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="9385c-255">If you click **Choose a category for more details**, you can select from the following values:</span></span>

- <span data-ttu-id="9385c-256">**Courrier électronique de hameçonnage**: cette sélection vous permet d’accéder au [rapport d’état de protection contre les menaces](view-email-security-reports.md#threat-protection-status-report).</span><span class="sxs-lookup"><span data-stu-id="9385c-256">**Phishing email**: This selection takes you to the [Threat protection status report](view-email-security-reports.md#threat-protection-status-report).</span></span>
- <span data-ttu-id="9385c-257">**Programme malveillant dans la messagerie**: cette sélection vous permet d’accéder au [rapport d’état de protection contre les menaces](view-email-security-reports.md#threat-protection-status-report).</span><span class="sxs-lookup"><span data-stu-id="9385c-257">**Malware in email**: This selection takes you to the [Threat protection status report](view-email-security-reports.md#threat-protection-status-report).</span></span>
- <span data-ttu-id="9385c-258">**Détections de courrier indésirable**: cette sélection vous permet d’accéder au [rapport des détections de courrier indésirable](view-email-security-reports.md#spam-detections-report).</span><span class="sxs-lookup"><span data-stu-id="9385c-258">**Spam detections**: This selection takes you to the [Spam Detections report](view-email-security-reports.md#spam-detections-report).</span></span>
- <span data-ttu-id="9385c-259">**Courrier indésirable bloqué**pour le serveur Edge : cette sélection vous permet d’accéder au [rapport des détections de courrier indésirable](view-email-security-reports.md#spam-detections-report).</span><span class="sxs-lookup"><span data-stu-id="9385c-259">**Edge blocked spam**: This selection takes you to the [Spam Detections report](view-email-security-reports.md#spam-detections-report).</span></span>

<span data-ttu-id="9385c-260">**Exportation**:</span><span class="sxs-lookup"><span data-stu-id="9385c-260">**Export**:</span></span>

<span data-ttu-id="9385c-261">Pour l’affichage détaillé, vous pouvez uniquement exporter des données pour un jour.</span><span class="sxs-lookup"><span data-stu-id="9385c-261">For the detail view, you can only export data for one day.</span></span> <span data-ttu-id="9385c-262">Par conséquent, si vous voulez exporter des données pendant 7 jours, vous devez effectuer 7 actions d’exportation différentes.</span><span class="sxs-lookup"><span data-stu-id="9385c-262">So, if you want to export data for 7 days, you need to do 7 different export actions.</span></span>

<span data-ttu-id="9385c-263">Chaque fichier. csv exporté est limité à 150 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="9385c-263">Each exported .csv file is limited to 150,000 rows.</span></span> <span data-ttu-id="9385c-264">Si les données de ce jour contiennent plus de 150 000 lignes, plusieurs fichiers. csv seront créés.</span><span class="sxs-lookup"><span data-stu-id="9385c-264">If the data for that day contains more than 150,000 rows, then multiple .csv files will be created.</span></span>

![<span data-ttu-id="9385c-265">Tapez View dans le rapport d’état de flux de flux</span><span class="sxs-lookup"><span data-stu-id="9385c-265">Type view in the Mailflow status report</span></span> ](../../media/mail-flow-status-report-type-view.png)

### <a name="direction-view-for-the-mailflow-status-report"></a><span data-ttu-id="9385c-266">Vue de direction pour le rapport d’état de flux de flux</span><span class="sxs-lookup"><span data-stu-id="9385c-266">Direction view for the Mailflow status report</span></span>

<span data-ttu-id="9385c-267">Si vous cliquez sur l’onglet **direction** , les mêmes filtres par défaut de la vue **type** sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="9385c-267">If you click the **Direction** tab, the same default filters from the **Type** view are used.</span></span>

<span data-ttu-id="9385c-268">Le graphique est organisé par les valeurs de **direction** .</span><span class="sxs-lookup"><span data-stu-id="9385c-268">The chart is organized by **Direction** values.</span></span>

<span data-ttu-id="9385c-269">Vous pouvez modifier ces filtres en cliquant sur **Filtrer** ou en cliquant sur une valeur dans la légende du graphique.</span><span class="sxs-lookup"><span data-stu-id="9385c-269">You can change these filters by clicking **Filter** or by clicking a value in the chart legend.</span></span> <span data-ttu-id="9385c-270">Les mêmes filtres de la vue **type** sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="9385c-270">The same filters from the **Type** view are used.</span></span>

<span data-ttu-id="9385c-271">La table de données contient les mêmes informations à partir de la vue **type** .</span><span class="sxs-lookup"><span data-stu-id="9385c-271">The data table contains same information from the **Type** view.</span></span>

<span data-ttu-id="9385c-272">La **catégorie choisir une catégorie pour plus de détails** disponibles et les sélections possibles est identique à la vue **type** .</span><span class="sxs-lookup"><span data-stu-id="9385c-272">The **Choose a category for more details** available selections and behavior are the same as the **Type** view.</span></span>

<span data-ttu-id="9385c-273">**Exportation**:</span><span class="sxs-lookup"><span data-stu-id="9385c-273">**Export**:</span></span>

<span data-ttu-id="9385c-274">Pour l’affichage détaillé, vous pouvez uniquement exporter des données pour un jour.</span><span class="sxs-lookup"><span data-stu-id="9385c-274">For the detail view, you can only export data for one day.</span></span> <span data-ttu-id="9385c-275">Par conséquent, si vous voulez exporter des données pendant 7 jours, vous devez effectuer 7 actions d’exportation différentes.</span><span class="sxs-lookup"><span data-stu-id="9385c-275">So, if you want to export data for 7 days, you need to do 7 different export actions.</span></span>

<span data-ttu-id="9385c-276">Chaque fichier. csv exporté est limité à 150 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="9385c-276">Each exported .csv file is limited to 150,000 rows.</span></span> <span data-ttu-id="9385c-277">Si les données de ce jour contiennent plus de 150 000 lignes, plusieurs fichiers. csv seront créés.</span><span class="sxs-lookup"><span data-stu-id="9385c-277">If the data for that day contains more than 150,000 rows, then multiple .csv files will be created.</span></span>

![<span data-ttu-id="9385c-278">Affichage de la direction dans le rapport d’état de flux de flux</span><span class="sxs-lookup"><span data-stu-id="9385c-278">Direction view in the Mailflow status report</span></span> ](../../media/mail-flow-status-report-direction-view.png)

## <a name="sent-and-received-email-report"></a><span data-ttu-id="9385c-279">Rapport de courrier électronique envoyé et reçu</span><span class="sxs-lookup"><span data-stu-id="9385c-279">Sent and received email report</span></span>

<span data-ttu-id="9385c-280">Le rapport de **courrier électronique envoyé et reçu** est un rapport intelligent qui affiche des informations sur les messages entrants et sortants, notamment les détections de courrier indésirable, les programmes malveillants et la messagerie électronique identifiés comme étant « en qualité ».</span><span class="sxs-lookup"><span data-stu-id="9385c-280">The **Sent and received email** report is a smart report that shows information about incoming and outgoing email, including spam detections, malware, and email identified as "good."</span></span> <span data-ttu-id="9385c-281">La différence entre ce rapport et le [rapport d’état de flux](#mailflow-status-report) de courrier est la suivante : ce rapport n’inclut pas de données sur les messages bloqués par la protection du serveur Edge.</span><span class="sxs-lookup"><span data-stu-id="9385c-281">The difference between this report and the [Mailflow status report](#mailflow-status-report) is: this report doesn't include data about messages blocked by edge protection.</span></span>

<span data-ttu-id="9385c-282">L’affichage Aggregate et l’affichage détaillé du rapport autorisent 90 jours de filtrage.</span><span class="sxs-lookup"><span data-stu-id="9385c-282">The aggregate view and the detail view of the report allow for 90 days of filtering.</span></span>

<span data-ttu-id="9385c-283">Pour afficher le rapport, ouvrez le [Centre de sécurité & conformité](https://protection.office.com), accédez **Reports** au \> **tableau de bord** rapports et sélectionnez **Envoyer et recevoir un message**.</span><span class="sxs-lookup"><span data-stu-id="9385c-283">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Sent and received email**.</span></span> <span data-ttu-id="9385c-284">Pour accéder directement au rapport, ouvrez <https://protection.office.com/reportv2?id=SentAndReceivedMailATP> .</span><span class="sxs-lookup"><span data-stu-id="9385c-284">To go directly to the report, open <https://protection.office.com/reportv2?id=SentAndReceivedMailATP>.</span></span>

![Widget courrier électronique envoyé et reçu dans le tableau de bord rapports](../../media/sent-and-received-email-report-widget.png)

### <a name="report-view-for-the-sent-and-received-email-report"></a><span data-ttu-id="9385c-286">Affichage de rapport pour le rapport de courrier électronique envoyé et reçu</span><span class="sxs-lookup"><span data-stu-id="9385c-286">Report view for the Sent and received email report</span></span>

<span data-ttu-id="9385c-287">Les graphiques suivants sont disponibles dans l’affichage rapport :</span><span class="sxs-lookup"><span data-stu-id="9385c-287">The following charts are available in the report view:</span></span>

- <span data-ttu-id="9385c-288">**Décomposer en : type**: le graphique affiche toutes les catégories disponibles :</span><span class="sxs-lookup"><span data-stu-id="9385c-288">**Break down by: Type**: The chart shows all available categories:</span></span>

  - <span data-ttu-id="9385c-289">**Total**</span><span class="sxs-lookup"><span data-stu-id="9385c-289">**Total**</span></span>
  - <span data-ttu-id="9385c-290">**Courrier électronique approprié**</span><span class="sxs-lookup"><span data-stu-id="9385c-290">**Good mail**</span></span>
  - <span data-ttu-id="9385c-291">**Programme malveillant (blocage des programmes malveillants)** (EoP)</span><span class="sxs-lookup"><span data-stu-id="9385c-291">**Malware (anti-malware)** (EOP)</span></span>
  - <span data-ttu-id="9385c-292">**Détections de courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="9385c-292">**Spam detections**</span></span>
  - <span data-ttu-id="9385c-293">**Messages de règle**</span><span class="sxs-lookup"><span data-stu-id="9385c-293">**Rule messages**</span></span>
  - <span data-ttu-id="9385c-294">**Programme malveillant avancé** (Office 365 ATP)</span><span class="sxs-lookup"><span data-stu-id="9385c-294">**Advanced malware** (Office 365 ATP)</span></span>

  <span data-ttu-id="9385c-295">Lorsque vous placez le curseur de la souris sur un jour (point de données) dans le graphique, vous pouvez afficher les détails de ce jour.</span><span class="sxs-lookup"><span data-stu-id="9385c-295">When you hover over a day (data point) in the chart, you can see details for that day.</span></span>

  ![Type de vue dans le rapport des courriers électroniques envoyés et reçus](../../media/sent-and-received-email-report-type-view.png)

- <span data-ttu-id="9385c-297">**Décomposer en : sens**: le graphique indique le **total**, les données **entrantes**et **sortantes** .</span><span class="sxs-lookup"><span data-stu-id="9385c-297">**Break down by: Direction**: The chart shows **Total**, **Inbound**, and **Outbound** data.</span></span> <span data-ttu-id="9385c-298">Lorsque vous placez le curseur de la souris sur un jour (point de données) dans le graphique, vous pouvez afficher les détails de ce jour.</span><span class="sxs-lookup"><span data-stu-id="9385c-298">When you hover over a day (data point) in the chart, you can see details for that day.</span></span>

  ![Affichage de la direction dans le rapport de courrier électronique envoyé et reçu](../../media/sent-and-received-email-report-direction-view.png)

- <span data-ttu-id="9385c-300">**Explorer en détail** \> **Programme malveillant (anti-programme malveillant)**: cette sélection vous permet d’accéder à la [détection de programmes malveillants dans le rapport par courrier électronique](view-email-security-reports.md#malware-detection-in-email-report).</span><span class="sxs-lookup"><span data-stu-id="9385c-300">**Drill down by** \> **Malware (anti-malware)**: This selection takes you to the [Malware detection in email report](view-email-security-reports.md#malware-detection-in-email-report).</span></span>

- <span data-ttu-id="9385c-301">**Explorer en détail** \> **Détections de courrier indésirable)**: cette sélection vous permet d’accéder au [rapport des détections de courrier indésirable](view-email-security-reports.md#spam-detections-report).</span><span class="sxs-lookup"><span data-stu-id="9385c-301">**Drill down by** \> **Spam detections)**: This selection takes you to the [Spam Detections report](view-email-security-reports.md#spam-detections-report).</span></span>

<span data-ttu-id="9385c-302">Si vous cliquez sur **filtres** dans un affichage de rapport, vous pouvez modifier les résultats à l’aide des filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="9385c-302">If you click **Filters** in a report view, you can modify the results with the following filters:</span></span>

- <span data-ttu-id="9385c-303">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="9385c-303">**Start date** and **End date**</span></span>
- <span data-ttu-id="9385c-304">Valeurs de la direction</span><span class="sxs-lookup"><span data-stu-id="9385c-304">Direction values</span></span>
- <span data-ttu-id="9385c-305">Valeurs de type</span><span class="sxs-lookup"><span data-stu-id="9385c-305">Type values</span></span>

<span data-ttu-id="9385c-306">Pour revenir à l’affichage de rapport, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="9385c-306">To go back to the report view, click **View report**.</span></span>

### <a name="details-table-view-for-the-sent-and-received-email-report"></a><span data-ttu-id="9385c-307">Vue de la table des détails pour le rapport de courrier électronique envoyé et reçu</span><span class="sxs-lookup"><span data-stu-id="9385c-307">Details table view for the Sent and received email report</span></span>

<span data-ttu-id="9385c-308">Si vous cliquez sur **afficher les détails** de la table dans la fenêtre dépanner **par : direction** ou dépanner **par :** le mode de direction, les informations suivantes sont affichées :</span><span class="sxs-lookup"><span data-stu-id="9385c-308">If you click **View details table** in the **Break down by: Direction** or **Break down by: Direction** view, the following information is shown:</span></span>

- <span data-ttu-id="9385c-309">**Date (UTC)**</span><span class="sxs-lookup"><span data-stu-id="9385c-309">**Date (UTC)**</span></span>
- <span data-ttu-id="9385c-310">**Type**</span><span class="sxs-lookup"><span data-stu-id="9385c-310">**Type**</span></span>
- <span data-ttu-id="9385c-311">**Direction**</span><span class="sxs-lookup"><span data-stu-id="9385c-311">**Direction**</span></span>
- <span data-ttu-id="9385c-312">**Nombre de messages**</span><span class="sxs-lookup"><span data-stu-id="9385c-312">**Message count**</span></span>

<span data-ttu-id="9385c-313">Si vous cliquez sur **filtres** dans un affichage tableau détaillé, vous pouvez modifier les résultats à l’aide des filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="9385c-313">If you click **Filters** in a details table view, you can modify the results with the following filters:</span></span>

- <span data-ttu-id="9385c-314">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="9385c-314">**Start date** and **End date**</span></span>
- <span data-ttu-id="9385c-315">Valeurs de la direction</span><span class="sxs-lookup"><span data-stu-id="9385c-315">Direction values</span></span>
- <span data-ttu-id="9385c-316">Valeurs de type</span><span class="sxs-lookup"><span data-stu-id="9385c-316">Type values</span></span>

<span data-ttu-id="9385c-317">Pour revenir à l’affichage de rapport, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="9385c-317">To go back to the report view, click **View report**.</span></span>

## <a name="top-senders-and-recipients-report"></a><span data-ttu-id="9385c-318">Rapport des expéditeurs et des destinataires principaux</span><span class="sxs-lookup"><span data-stu-id="9385c-318">Top senders and recipients report</span></span>

<span data-ttu-id="9385c-319">Le rapport des **expéditeurs et des destinataires principaux** est un graphique en secteurs illustrant les principaux expéditeurs et destinataires de votre courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="9385c-319">The **Top senders and recipients** report is a pie chart showing your top email senders and recipients.</span></span>

<span data-ttu-id="9385c-320">Pour afficher le rapport, ouvrez le [Centre de sécurité & conformité](https://protection.office.com), accédez à **rapports** \> **Dashboard** et sélectionnez **principaux expéditeurs et destinataires**.</span><span class="sxs-lookup"><span data-stu-id="9385c-320">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Top senders and recipients**.</span></span> <span data-ttu-id="9385c-321">Pour accéder directement au rapport, ouvrez <https://protection.office.com/reportv2?id=TopSenderRecipientsATP> .</span><span class="sxs-lookup"><span data-stu-id="9385c-321">To go directly to the report, open <https://protection.office.com/reportv2?id=TopSenderRecipientsATP>.</span></span>

![Widget principaux expéditeurs et destinataires dans le tableau de bord rapports](../../media/top-senders-and-recipients-widget.png)

### <a name="report-view-for-the-top-senders-and-recipient-report"></a><span data-ttu-id="9385c-323">Affichage de rapport pour le rapport des expéditeurs et des destinataires principaux</span><span class="sxs-lookup"><span data-stu-id="9385c-323">Report view for the Top senders and recipient report</span></span>

<span data-ttu-id="9385c-324">Les graphiques suivants sont disponibles dans l’affichage rapport :</span><span class="sxs-lookup"><span data-stu-id="9385c-324">The following charts are available in the report view:</span></span>

- <span data-ttu-id="9385c-325">**Afficher les données des \> expéditeurs de messages principaux**</span><span class="sxs-lookup"><span data-stu-id="9385c-325">**Show data for \> Top mail senders**</span></span>
- <span data-ttu-id="9385c-326">**Afficher les données des \> destinataires de messagerie les plus fréquents**</span><span class="sxs-lookup"><span data-stu-id="9385c-326">**Show data for \> Top mail recipients**</span></span>
- <span data-ttu-id="9385c-327">**Afficher les données pour les \> destinataires de courrier indésirable principaux**</span><span class="sxs-lookup"><span data-stu-id="9385c-327">**Show data for \> Top spam recipients**</span></span>
- <span data-ttu-id="9385c-328">**Afficher les données pour \> Principaux destinataires de programmes malveillants** (EoP)</span><span class="sxs-lookup"><span data-stu-id="9385c-328">**Show data for \> Top malware recipients** (EOP)</span></span>
- <span data-ttu-id="9385c-329">**Afficher les données pour \> Principaux destinataires de programmes malveillants (ATP)** (Office 365 ATP)</span><span class="sxs-lookup"><span data-stu-id="9385c-329">**Show data for \> Top malware recipients (ATP)** (Office 365 ATP)</span></span>

<span data-ttu-id="9385c-330">La composition du graphique en secteurs est modifiée en fonction de ces sélections.</span><span class="sxs-lookup"><span data-stu-id="9385c-330">The composition of the pie chart changes based on these selections.</span></span>

<span data-ttu-id="9385c-331">Lorsque vous placez le curseur de la souris sur un coin du graphique en secteurs, vous pouvez voir le nombre de messages envoyés ou reçus.</span><span class="sxs-lookup"><span data-stu-id="9385c-331">When you hover over a wedge in the pie chart, you can see a count of messages sent or received.</span></span>

<span data-ttu-id="9385c-332">Si vous cliquez sur **filtres** dans un affichage de rapport, vous pouvez spécifier une plage de dates avec **Date de début** et date de **fin**.</span><span class="sxs-lookup"><span data-stu-id="9385c-332">If you click **Filters** in a report view, you can specify a date range with **Start date** and **End date**.</span></span>

![Graphique en secteurs en mode état dans le rapport des expéditeurs et destinataires principaux](../../media/top-senders-and-recipients-report-view.png)

### <a name="details-table-view-for-the-top-senders-and-recipient-report"></a><span data-ttu-id="9385c-334">Vue de la table Détails pour le rapport des expéditeurs et des destinataires principaux</span><span class="sxs-lookup"><span data-stu-id="9385c-334">Details table view for the Top senders and recipient report</span></span>

<span data-ttu-id="9385c-335">Si vous cliquez sur **afficher les détails table**, les informations affichées dépendent du graphique que vous examinez :</span><span class="sxs-lookup"><span data-stu-id="9385c-335">If you click **View details table**, the information that's shown depends on the chart you were looking at:</span></span>

- <span data-ttu-id="9385c-336">**Afficher les données des \> expéditeurs de messages principaux**</span><span class="sxs-lookup"><span data-stu-id="9385c-336">**Show data for \> Top mail senders**</span></span>

  - <span data-ttu-id="9385c-337">**Principaux expéditeurs de messagerie**</span><span class="sxs-lookup"><span data-stu-id="9385c-337">**Top mail senders**</span></span>
  - <span data-ttu-id="9385c-338">**Count**</span><span class="sxs-lookup"><span data-stu-id="9385c-338">**Count**</span></span>

- <span data-ttu-id="9385c-339">**Afficher les données des \> destinataires de messagerie les plus fréquents**</span><span class="sxs-lookup"><span data-stu-id="9385c-339">**Show data for \> Top mail recipients**</span></span>

  - <span data-ttu-id="9385c-340">**Principaux destinataires de messagerie**</span><span class="sxs-lookup"><span data-stu-id="9385c-340">**Top mail recipients**</span></span>
  - <span data-ttu-id="9385c-341">**Count**</span><span class="sxs-lookup"><span data-stu-id="9385c-341">**Count**</span></span>

- <span data-ttu-id="9385c-342">**Afficher les données pour les \> destinataires de courrier indésirable principaux**</span><span class="sxs-lookup"><span data-stu-id="9385c-342">**Show data for \> Top spam recipients**</span></span>

  - <span data-ttu-id="9385c-343">**Principaux destinataires de courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="9385c-343">**Top spam recipients**</span></span>
  - <span data-ttu-id="9385c-344">**Count**</span><span class="sxs-lookup"><span data-stu-id="9385c-344">**Count**</span></span>

- <span data-ttu-id="9385c-345">**Afficher les données pour \> Principaux destinataires de programmes malveillants** (EoP)</span><span class="sxs-lookup"><span data-stu-id="9385c-345">**Show data for \> Top malware recipients** (EOP)</span></span>

  - <span data-ttu-id="9385c-346">**Principaux destinataires de programmes malveillants**</span><span class="sxs-lookup"><span data-stu-id="9385c-346">**Top malware recipients**</span></span>
  - <span data-ttu-id="9385c-347">**Count**</span><span class="sxs-lookup"><span data-stu-id="9385c-347">**Count**</span></span>

- <span data-ttu-id="9385c-348">**Afficher les données pour \> Principaux destinataires de programmes malveillants (ATP)** (Office 365 ATP)</span><span class="sxs-lookup"><span data-stu-id="9385c-348">**Show data for \> Top malware recipients (ATP)** (Office 365 ATP)</span></span>

  - <span data-ttu-id="9385c-349">**Principaux destinataires de programmes malveillants (ATP)**</span><span class="sxs-lookup"><span data-stu-id="9385c-349">**Top malware recipients (ATP)**</span></span>
  - <span data-ttu-id="9385c-350">**Count**</span><span class="sxs-lookup"><span data-stu-id="9385c-350">**Count**</span></span>

<span data-ttu-id="9385c-351">Si vous cliquez sur **filtres** dans un affichage tableau détaillé, vous pouvez spécifier une plage de dates avec **Date de début** et date de **fin**.</span><span class="sxs-lookup"><span data-stu-id="9385c-351">If you click **Filters** in a details table view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="9385c-352">Pour revenir à l’affichage de rapport, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="9385c-352">To go back to the report view, click **View report**.</span></span>

## <a name="what-permissions-are-needed-to-view-these-reports"></a><span data-ttu-id="9385c-353">Quelles sont les autorisations nécessaires pour afficher ces rapports ?</span><span class="sxs-lookup"><span data-stu-id="9385c-353">What permissions are needed to view these reports?</span></span>

<span data-ttu-id="9385c-354">Pour afficher et utiliser les rapports, vous devez être membre du groupe de rôles spécifié dans le centre de sécurité & conformité **et** dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="9385c-354">To view and use the reports, you need to be a member of the specified role group in the Security & Compliance Center **and** in Exchange Online.</span></span>

- <span data-ttu-id="9385c-355">Dans le centre de sécurité & conformité, vous devez être membre de l’un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="9385c-355">In the Security & Compliance Center, you need to be a member of one of the following role groups:</span></span>

  <span data-ttu-id="9385c-356">-Gestion de l’Organisation</span><span class="sxs-lookup"><span data-stu-id="9385c-356">-Organization Management</span></span>

  <span data-ttu-id="9385c-357">-Administrateur de la sécurité (vous pouvez également le faire dans le [Centre d’administration Azure Active Directory](https://aad.portal.azure.com) -lecteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="9385c-357">-Security Administrator (you can also do this in the [Azure Active Directory admin center](https://aad.portal.azure.com) -Security Reader</span></span>

  <span data-ttu-id="9385c-358">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](https://docs.microsoft.com/microsoft-365/security/office-365-security/permissions-in-the-security-and-compliance-center).</span><span class="sxs-lookup"><span data-stu-id="9385c-358">For more information, see [Permissions in the Security & Compliance Center](https://docs.microsoft.com/microsoft-365/security/office-365-security/permissions-in-the-security-and-compliance-center).</span></span>

- <span data-ttu-id="9385c-359">Dans Exchange Online, vous devez être membre de l’un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="9385c-359">In Exchange Online, you need to be a member of one of the following role groups:</span></span>

  <span data-ttu-id="9385c-360">-Gestion de l’Organisation</span><span class="sxs-lookup"><span data-stu-id="9385c-360">-Organization Management</span></span>

  <span data-ttu-id="9385c-361">-View-Only Organization Management</span><span class="sxs-lookup"><span data-stu-id="9385c-361">-View-only Organization Management</span></span>

  <span data-ttu-id="9385c-362">-Affichage uniquement des destinataires</span><span class="sxs-lookup"><span data-stu-id="9385c-362">-View-Only Recipients</span></span>

  <span data-ttu-id="9385c-363">-Gestion de la conformité</span><span class="sxs-lookup"><span data-stu-id="9385c-363">-Compliance Management</span></span>

<span data-ttu-id="9385c-364">Pour plus d’informations, consultez la rubrique [autorisations dans Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo) et [gérer les groupes de rôles dans Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/role-groups).</span><span class="sxs-lookup"><span data-stu-id="9385c-364">For more information, see [Permissions in Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo) and [Manage role groups in Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/role-groups).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9385c-365">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9385c-365">Related topics</span></span>

[<span data-ttu-id="9385c-366">Rapports intelligents et aperçus dans le centre de sécurité et conformité</span><span class="sxs-lookup"><span data-stu-id="9385c-366">Smart reports and insights in the Security & Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)

[<span data-ttu-id="9385c-367">Afficher les rapports de sécurité de courrier dans le centre de sécurité et conformité</span><span class="sxs-lookup"><span data-stu-id="9385c-367">View email security reports in the Security & Compliance Center</span></span>](view-email-security-reports.md)
