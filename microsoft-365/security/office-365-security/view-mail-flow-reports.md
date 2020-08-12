---
title: Afficher les rapports de flux de messagerie dans le tableau de bord rapports
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
description: Les administrateurs peuvent en savoir plus sur les rapports de flux de messagerie disponibles dans le tableau de bord des rapports dans le centre de sécurité & conformité.
ms.custom: ''
ms.openlocfilehash: acf74136fc61d38ea9aac47f36d96aa51a7b9905
ms.sourcegitcommit: 6319e73b3690b4cf1b7932f2b9f51c2c99e70eaa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2020
ms.locfileid: "46635033"
---
# <a name="view-mail-flow-reports-in-the-reports-dashboard-in-security--compliance-center"></a><span data-ttu-id="3da28-103">Afficher les rapports de flux de messagerie dans le tableau de bord rapports du centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="3da28-103">View mail flow reports in the Reports dashboard in Security & Compliance Center</span></span>

<span data-ttu-id="3da28-104">En plus des rapports de flux de messagerie disponibles dans le [tableau de bord de flux de messagerie](mail-flow-insights-v2.md) dans le centre de sécurité & conformité, un grand nombre de rapports de flux de messagerie supplémentaires sont disponibles dans le tableau de bord rapports pour vous aider à surveiller votre organisation Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="3da28-104">In addition to the mail flow reports that are available in the [Mail flow dashboard](mail-flow-insights-v2.md) in the Security & Compliance Center, a variety of additional mail flow reports are available in the Reports dashboard to help you monitor your Microsoft 365 organization.</span></span>

<span data-ttu-id="3da28-105">Si vous disposez des [autorisations nécessaires](#what-permissions-are-needed-to-view-these-reports), vous pouvez afficher ces rapports dans le [Centre de sécurité & conformité](https://office.protection.com) en accédant au tableau de **Reports** \> **bord**rapports.</span><span class="sxs-lookup"><span data-stu-id="3da28-105">If you have the [necessary permissions](#what-permissions-are-needed-to-view-these-reports), you can view these reports in the [Security & Compliance Center](https://office.protection.com) by going to **Reports** \> **Dashboard**.</span></span> <span data-ttu-id="3da28-106">Pour accéder directement au tableau de bord rapports, ouvrez <https://office.protection.office.com/insightdashboard> .</span><span class="sxs-lookup"><span data-stu-id="3da28-106">To go directly to the Reports dashboard, open <https://office.protection.office.com/insightdashboard>.</span></span>

![Tableau de bord des rapports dans le centre de sécurité & conformité](../../media/6b213d34-adbb-44af-8549-be9a7e2db087.png)

## <a name="connector-report"></a><span data-ttu-id="3da28-108">Rapport de connecteur</span><span class="sxs-lookup"><span data-stu-id="3da28-108">Connector report</span></span>

<span data-ttu-id="3da28-109">Le **rapport de connecteur** affiche l’activité de flux de messagerie sur les connecteurs entrants [et sortants](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow) configurés pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3da28-109">The **Connector report** shows mail flow activity on the [inbound and outbound connectors](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow) that are configured for your organization.</span></span>

<span data-ttu-id="3da28-110">Pour afficher le rapport, ouvrez le [Centre de sécurité & conformité](https://protection.office.com), accédez **Reports** au \> **tableau de bord** rapports et sélectionnez rapport de **connecteur**.</span><span class="sxs-lookup"><span data-stu-id="3da28-110">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Connector report**.</span></span> <span data-ttu-id="3da28-111">Pour accéder directement au rapport, ouvrez <https://protection.office.com/reportv2?id=ConnectorReport> .</span><span class="sxs-lookup"><span data-stu-id="3da28-111">To go directly to the report, open <https://protection.office.com/reportv2?id=ConnectorReport>.</span></span>

![Widget rapport de connecteur dans le tableau de bord rapports](../../media/connector-report-widget.png)

### <a name="report-view-for-the-connector-report"></a><span data-ttu-id="3da28-113">Affichage de rapport pour le rapport de connecteur</span><span class="sxs-lookup"><span data-stu-id="3da28-113">Report view for the Connector report</span></span>

<span data-ttu-id="3da28-114">Les graphiques suivants sont disponibles en mode état :</span><span class="sxs-lookup"><span data-stu-id="3da28-114">The following charts are available in report view:</span></span>

- <span data-ttu-id="3da28-115">**Afficher les données par : flux de messagerie**: ce graphique indique le nombre de messages entrants et sortants organisés par :</span><span class="sxs-lookup"><span data-stu-id="3da28-115">**View data by: Mail flow**: This chart shows the number of inbound and outbound messages organized by:</span></span>

  - <span data-ttu-id="3da28-116">**Total**</span><span class="sxs-lookup"><span data-stu-id="3da28-116">**Total**</span></span>
  - <span data-ttu-id="3da28-117">**À partir d’Internet sans connecteur**</span><span class="sxs-lookup"><span data-stu-id="3da28-117">**From the internet without a connector**</span></span>
  - <span data-ttu-id="3da28-118">**Sur Internet sans connecteur**</span><span class="sxs-lookup"><span data-stu-id="3da28-118">**To the internet without a connector**</span></span>
  - <span data-ttu-id="3da28-119">Un connecteur spécifique que vous avez configuré.</span><span class="sxs-lookup"><span data-stu-id="3da28-119">A specific connector that you've configured.</span></span>
  
  <span data-ttu-id="3da28-120">Pour isoler les données du graphique, utilisez l’option **afficher les données pour** le contrôle pour sélectionner une de ces options ou **tout le flux de messagerie**.</span><span class="sxs-lookup"><span data-stu-id="3da28-120">To isolate the data in the chart, use the **Show data for** control to select one of these options or **All mail flow**.</span></span>

  ![Afficher les données par flux de messagerie dans le rapport du connecteur](../../media/connector-report-view-data-by-mail-flow.png)

- <span data-ttu-id="3da28-122">**Afficher les données par : utilisation de TLS**: ce graphique indique le pourcentage d’utilisation de la version TLS (Transport Layer Security) pour le flux de messagerie.</span><span class="sxs-lookup"><span data-stu-id="3da28-122">**View data by: TLS usage**: This chart shows the percentage of Transport Layer Security (TLS) version usage for mail flow.</span></span>

  <span data-ttu-id="3da28-123">Pour isoler les données dans le graphique, utilisez l’option **afficher les données pour** le contrôle afin de sélectionner l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="3da28-123">To isolate the data in the chart, use the **Show data for** control to select one of the following options:</span></span>

  - <span data-ttu-id="3da28-124">**Tout le flux de messagerie**</span><span class="sxs-lookup"><span data-stu-id="3da28-124">**All mail flow**</span></span>
  - <span data-ttu-id="3da28-125">**À partir d’Internet sans connecteur**</span><span class="sxs-lookup"><span data-stu-id="3da28-125">**From the internet without a connector**</span></span>
  - <span data-ttu-id="3da28-126">**Sur Internet sans connecteur**</span><span class="sxs-lookup"><span data-stu-id="3da28-126">**To the internet without a connector**</span></span>
  - <span data-ttu-id="3da28-127">Un connecteur spécifique que vous avez configuré.</span><span class="sxs-lookup"><span data-stu-id="3da28-127">A specific connector that you've configured.</span></span>

  ![Afficher les données par utilisation de TLS dans le rapport de connecteur](../../media/connector-report-view-data-by-tls-usage.png)

<span data-ttu-id="3da28-129">Si vous cliquez sur **filtres** dans un affichage de rapport, vous pouvez spécifier une plage de dates avec **Date de début** et date de **fin**.</span><span class="sxs-lookup"><span data-stu-id="3da28-129">If you click **Filters** in a report view, you can specify a date range with **Start date** and **End date**.</span></span>

### <a name="details-table-view-for-the-connector-report"></a><span data-ttu-id="3da28-130">Vue de la table Détails pour le rapport de connecteur</span><span class="sxs-lookup"><span data-stu-id="3da28-130">Details table view for the Connector report</span></span>

<span data-ttu-id="3da28-131">Si vous cliquez sur **afficher la table des détails** dans un affichage de rapport, les informations suivantes s’affichent :</span><span class="sxs-lookup"><span data-stu-id="3da28-131">If you click **View details table** in a report view, the following information is shown:</span></span>

- <span data-ttu-id="3da28-132">**Date**</span><span class="sxs-lookup"><span data-stu-id="3da28-132">**Date**</span></span>
- <span data-ttu-id="3da28-133">**Nom et direction du connecteur**</span><span class="sxs-lookup"><span data-stu-id="3da28-133">**Connector direction and name**</span></span>
- <span data-ttu-id="3da28-134">**Type de connecteur**</span><span class="sxs-lookup"><span data-stu-id="3da28-134">**Connector type**</span></span>
- <span data-ttu-id="3da28-135">**TLS forcé ?**: valeur **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="3da28-135">**Forced TLS?**: The value **True** or **False**.</span></span>
- <span data-ttu-id="3da28-136">**Pas de TLS** (pourcentage)</span><span class="sxs-lookup"><span data-stu-id="3da28-136">**No TLS** (percentage)</span></span>
- <span data-ttu-id="3da28-137">**TLS 1,0** (pourcentage)</span><span class="sxs-lookup"><span data-stu-id="3da28-137">**TLS 1.0** (percentage)</span></span>
- <span data-ttu-id="3da28-138">**TLS 1,1** (pourcentage)</span><span class="sxs-lookup"><span data-stu-id="3da28-138">**TLS 1.1** (percentage)</span></span>
- <span data-ttu-id="3da28-139">**TLS 1,2** (pourcentage)</span><span class="sxs-lookup"><span data-stu-id="3da28-139">**TLS 1.2** (percentage)</span></span>
- <span data-ttu-id="3da28-140">**Volume**: nombre de messages.</span><span class="sxs-lookup"><span data-stu-id="3da28-140">**Volume**: The number of messages.</span></span>

<span data-ttu-id="3da28-141">Si vous cliquez sur **filtres** dans un affichage tableau détaillé, vous pouvez spécifier une plage de dates avec **Date de début** et date de **fin**.</span><span class="sxs-lookup"><span data-stu-id="3da28-141">If you click **Filters** in a details table view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="3da28-142">Pour revenir à l’affichage de rapport, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="3da28-142">To go back to the report view, click **View report**.</span></span>

## <a name="exchange-transport-rule-report"></a><span data-ttu-id="3da28-143">Rapport de règle de transport Exchange</span><span class="sxs-lookup"><span data-stu-id="3da28-143">Exchange transport rule report</span></span>

<span data-ttu-id="3da28-144">Le rapport des règles de **transport Exchange** affiche l’effet des règles de flux de messagerie (également appelées règles de transport) sur les messages entrants et sortants dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3da28-144">The **Exchange transport rule report** shows the effect of mail flow rules (also known as transport rules) on incoming and outgoing messages in your organization.</span></span>

<span data-ttu-id="3da28-145">Pour afficher le rapport, ouvrez le [Centre de sécurité & conformité](https://protection.office.com), accédez **Reports** au \> **tableau de bord** rapports et sélectionnez **règle de transport Exchange**.</span><span class="sxs-lookup"><span data-stu-id="3da28-145">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Exchange Transport rule**.</span></span> <span data-ttu-id="3da28-146">Pour accéder directement au rapport, ouvrez <https://protection.office.com/reportv2?id=ETRRuleReport> .</span><span class="sxs-lookup"><span data-stu-id="3da28-146">To go directly to the report, open <https://protection.office.com/reportv2?id=ETRRuleReport>.</span></span>

![Widget règle de transport Exchange dans le tableau de bord rapports](../../media/transport-rule-report-widget.png)

### <a name="report-view-for-the-exchange-transport-rule-report"></a><span data-ttu-id="3da28-148">Affichage de rapport pour le rapport des règles de transport Exchange</span><span class="sxs-lookup"><span data-stu-id="3da28-148">Report view for the Exchange transport rule report</span></span>

<span data-ttu-id="3da28-149">Les graphiques suivants sont disponibles en mode état :</span><span class="sxs-lookup"><span data-stu-id="3da28-149">The following charts are available in report view:</span></span>

- <span data-ttu-id="3da28-150">**Afficher les données par : règles** \> de transport Exchange **Décomposer en : sens**: ce graphique indique le **nombre de messages entrants** et **sortants** affectés par les règles de transport.</span><span class="sxs-lookup"><span data-stu-id="3da28-150">**View data by: Exchange transport rules** \> **Break down by: Direction**: This chart shows the number of **Inbound** and **Outbound** messages that were affected by transport rules.</span></span>

- <span data-ttu-id="3da28-151">**Afficher les données par : règles** \> de transport Exchange Dépanner **par : gravité**: ce graphique indique le nombre de messages de gravité **élevée** et de gravité **moyenne**, ainsi que les messages à **faible gravité** .</span><span class="sxs-lookup"><span data-stu-id="3da28-151">**View data by: Exchange transport rules** \> **Break down by: Severity**: This chart shows the number of **High severity** and **Medium severity**, and **Low severity** messages.</span></span> <span data-ttu-id="3da28-152">Vous définissez le niveau de gravité en tant qu’action dans la règle (**auditez cette règle avec le niveau de gravité** ou _SetAuditSeverity_).</span><span class="sxs-lookup"><span data-stu-id="3da28-152">You set the severity level as an action in the rule (**Audit this rule with severity level** or _SetAuditSeverity_).</span></span> <span data-ttu-id="3da28-153">Pour plus d’informations, consultez la rubrique [actions de règle de flux de messagerie dans Exchange Online](https://docs.microsoft.com//Exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions).</span><span class="sxs-lookup"><span data-stu-id="3da28-153">For more information, see [Mail flow rule actions in Exchange Online](https://docs.microsoft.com//Exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions).</span></span>

- <span data-ttu-id="3da28-154">**Afficher les données par : DLP Exchange transport Rules** \> **Décomposer en : sens**: ce graphique indique le **nombre de messages entrants** et **sortants** affectés par les règles de transport de la protection contre la perte de données (DLP).</span><span class="sxs-lookup"><span data-stu-id="3da28-154">**View data by: DLP Exchange transport rules** \> **Break down by: Direction**: This chart shows the number of **Inbound** and **Outbound** messages that were affected by data loss prevention (DLP) transport rules.</span></span> <span data-ttu-id="3da28-155">Vous pouvez affiner le graphique en sélectionnant l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="3da28-155">You can further refine the chart by selecting on of the following options:</span></span>

  - <span data-ttu-id="3da28-156">**Afficher les données pour : toutes les règles de transport DLP**</span><span class="sxs-lookup"><span data-stu-id="3da28-156">**Show data for: All DLP transport rules**</span></span>
  - <span data-ttu-id="3da28-157">**Afficher les données de : utilisateurs compromis**</span><span class="sxs-lookup"><span data-stu-id="3da28-157">**Show data for: Compromised users**</span></span>
  - <span data-ttu-id="3da28-158">**Afficher les données pour : faible volume de contenu détecté par les États-Unis Patriot Act**</span><span class="sxs-lookup"><span data-stu-id="3da28-158">**Show data for: Low volume of content detected U.S. Patriot Act**</span></span>

- <span data-ttu-id="3da28-159">**Afficher les données par : DLP Exchange transport Rules** \> **Décomposer en : sens**: cette vue indique le nombre de messages de gravité **élevée** et de gravité **moyenne**, ainsi que les messages à **faible gravité** qui ont été affectés par les règles de transport DLP.</span><span class="sxs-lookup"><span data-stu-id="3da28-159">**View data by: DLP Exchange transport rules** \> **Break down by: Direction**: This view shows the number of **High severity** and **Medium severity**, and **Low severity** messages that were affected by DLP transport rules.</span></span> <span data-ttu-id="3da28-160">Vous pouvez affiner le graphique en sélectionnant l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="3da28-160">You can further refine the chart by selecting on of the following options:</span></span>

  - <span data-ttu-id="3da28-161">**Afficher les données pour : toutes les règles de transport DLP**</span><span class="sxs-lookup"><span data-stu-id="3da28-161">**Show data for: All DLP transport rules**</span></span>
  - <span data-ttu-id="3da28-162">**Afficher les données de : utilisateurs compromis**</span><span class="sxs-lookup"><span data-stu-id="3da28-162">**Show data for: Compromised users**</span></span>
  - <span data-ttu-id="3da28-163">**Afficher les données pour : faible volume de contenu détecté par les États-Unis Patriot Act**</span><span class="sxs-lookup"><span data-stu-id="3da28-163">**Show data for: Low volume of content detected U.S. Patriot Act**</span></span>

<span data-ttu-id="3da28-164">Si vous cliquez sur **filtres** dans un affichage de rapport, vous pouvez modifier les résultats à l’aide des filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="3da28-164">If you click **Filters** in a report view, you can modify the results with the following filters::</span></span>

- <span data-ttu-id="3da28-165">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="3da28-165">**Start date** and **End date**</span></span>
- <span data-ttu-id="3da28-166">Valeurs de la direction</span><span class="sxs-lookup"><span data-stu-id="3da28-166">Direction values</span></span>
- <span data-ttu-id="3da28-167">Valeurs de gravité</span><span class="sxs-lookup"><span data-stu-id="3da28-167">Severity values</span></span>

![Affichage de rapport dans le rapport des règles de transport Exchange](../../media/transport-rule-report-report-view.png)

### <a name="details-table-view-for-the-exchange-transport-rule-report"></a><span data-ttu-id="3da28-169">Vue de la table Détails pour le rapport des règles de transport Exchange</span><span class="sxs-lookup"><span data-stu-id="3da28-169">Details table view for the Exchange transport rule report</span></span>

<span data-ttu-id="3da28-170">Si vous cliquez sur **afficher les détails table**, les informations affichées dépendent du graphique que vous examinez :</span><span class="sxs-lookup"><span data-stu-id="3da28-170">If you click **View details table**, the information that's shown depends on the chart you were looking at:</span></span>

- <span data-ttu-id="3da28-171">**Afficher les données par : règles de transport Exchange**:</span><span class="sxs-lookup"><span data-stu-id="3da28-171">**View data by: Exchange Transport rules**:</span></span>

  - <span data-ttu-id="3da28-172">**Date**</span><span class="sxs-lookup"><span data-stu-id="3da28-172">**Date**</span></span>
  - <span data-ttu-id="3da28-173">**Règle de transport**</span><span class="sxs-lookup"><span data-stu-id="3da28-173">**Transport rule**</span></span>
  - <span data-ttu-id="3da28-174">**Subject**</span><span class="sxs-lookup"><span data-stu-id="3da28-174">**Subject**</span></span>
  - <span data-ttu-id="3da28-175">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="3da28-175">**Sender address**</span></span>
  - <span data-ttu-id="3da28-176">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="3da28-176">**Recipient address**</span></span>
  - <span data-ttu-id="3da28-177">**Gravité**</span><span class="sxs-lookup"><span data-stu-id="3da28-177">**Severity**</span></span>
  - <span data-ttu-id="3da28-178">**Direction**</span><span class="sxs-lookup"><span data-stu-id="3da28-178">**Direction**</span></span>

- <span data-ttu-id="3da28-179">**Afficher les données par : DLP Exchange transport Rules**:</span><span class="sxs-lookup"><span data-stu-id="3da28-179">**View data by: DLP Exchange transport rules**:</span></span>

  - <span data-ttu-id="3da28-180">**Date**</span><span class="sxs-lookup"><span data-stu-id="3da28-180">**Date**</span></span>
  - <span data-ttu-id="3da28-181">**Stratégie DLP**</span><span class="sxs-lookup"><span data-stu-id="3da28-181">**DLP policy**</span></span>
  - <span data-ttu-id="3da28-182">**Règle de transport**</span><span class="sxs-lookup"><span data-stu-id="3da28-182">**Transport rule**</span></span>
  - <span data-ttu-id="3da28-183">**Subject**</span><span class="sxs-lookup"><span data-stu-id="3da28-183">**Subject**</span></span>
  - <span data-ttu-id="3da28-184">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="3da28-184">**Sender address**</span></span>
  - <span data-ttu-id="3da28-185">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="3da28-185">**Recipient address**</span></span>
  - <span data-ttu-id="3da28-186">**Gravité**</span><span class="sxs-lookup"><span data-stu-id="3da28-186">**Severity**</span></span>
  - <span data-ttu-id="3da28-187">**Direction**</span><span class="sxs-lookup"><span data-stu-id="3da28-187">**Direction**</span></span>

<span data-ttu-id="3da28-188">Si vous cliquez sur **filtres** dans un affichage tableau détaillé, vous pouvez modifier les résultats à l’aide des filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="3da28-188">If you click **Filters** in a details table view, you can modify the results with the following filters:</span></span>

- <span data-ttu-id="3da28-189">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="3da28-189">**Start date** and **End date**</span></span>
- <span data-ttu-id="3da28-190">Valeurs de la direction</span><span class="sxs-lookup"><span data-stu-id="3da28-190">Direction values</span></span>
- <span data-ttu-id="3da28-191">Valeurs de gravité</span><span class="sxs-lookup"><span data-stu-id="3da28-191">Severity values</span></span>

<span data-ttu-id="3da28-192">Pour revenir à l’affichage de rapport, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="3da28-192">To go back to the report view, click **View report**.</span></span>

## <a name="forwarding-report"></a><span data-ttu-id="3da28-193">Rapport de transfert</span><span class="sxs-lookup"><span data-stu-id="3da28-193">Forwarding report</span></span>

<span data-ttu-id="3da28-194">Le **rapport de transfert** indique que les messages envoyés par votre organisation sont transférés automatiquement vers des domaines externes à partir de boîtes aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="3da28-194">The **Forwarding report** shows your organization's automatically forwarded messages to external domains from Exchange Online mailboxes.</span></span> <span data-ttu-id="3da28-195">Les messages transférés peuvent présenter un risque de sécurité ou de conformité, et peuvent indiquer un compte compromis.</span><span class="sxs-lookup"><span data-stu-id="3da28-195">Forwarded messages can pose a security or compliance risk, and might indicate a compromised account.</span></span>

<span data-ttu-id="3da28-196">Pour afficher le rapport, ouvrez le [Centre de sécurité & conformité](https://protection.office.com), cliquez sur **rapports** de \> **tableau de bord** et sélectionnez rapport de **transfert**.</span><span class="sxs-lookup"><span data-stu-id="3da28-196">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Forwarding report**.</span></span> <span data-ttu-id="3da28-197">Pour accéder directement au rapport, ouvrez <https://protection.office.com/reportv2?id=MailFlowForwarding> .</span><span class="sxs-lookup"><span data-stu-id="3da28-197">To go directly to the report, open <https://protection.office.com/reportv2?id=MailFlowForwarding>.</span></span>

![Widget rapport de transfert dans le tableau de bord rapports](../../media/forwarding-report-widget.png)

### <a name="report-view-for-the-forwarding-report"></a><span data-ttu-id="3da28-199">Affichage de rapport pour le rapport de transfert</span><span class="sxs-lookup"><span data-stu-id="3da28-199">Report view for the Forwarding report</span></span>

<span data-ttu-id="3da28-200">Les graphiques suivants sont disponibles dans l’affichage rapport :</span><span class="sxs-lookup"><span data-stu-id="3da28-200">The following charts are available in the report view:</span></span>

- <span data-ttu-id="3da28-201">**Afficher les données pour : méthodes de transfert**: les méthodes suivantes sont affichées :</span><span class="sxs-lookup"><span data-stu-id="3da28-201">**Show data for: Forwarding methods**: The following methods are shown:</span></span>

  - <span data-ttu-id="3da28-202">**Règle de transport**: également appelée [règles de flux de messagerie](https://docs.microsoft.com/Exchange/security-and-compliance/mail-flow-rules/mail-flow-rules).</span><span class="sxs-lookup"><span data-stu-id="3da28-202">**Transport rule**: Also known as [mail flow rules](https://docs.microsoft.com/Exchange/security-and-compliance/mail-flow-rules/mail-flow-rules).</span></span>
  - <span data-ttu-id="3da28-203">**Règle de boîte aux lettres**: également appelée règles de boîte de [réception](https://support.microsoft.com/office/c24f5dea-9465-4df4-ad17-a50704d66c59).</span><span class="sxs-lookup"><span data-stu-id="3da28-203">**Mailbox rule**: Also known as [Inbox rules](https://support.microsoft.com/office/c24f5dea-9465-4df4-ad17-a50704d66c59).</span></span>

  ![Vue des méthodes de transfert dans le rapport de transfert](../../media/forwarding-report-forwarding-methods.png)

- <span data-ttu-id="3da28-205">**Afficher les données pour : transferts de domaines**: cette vue affiche les domaines de destinataire qui sont les destinations pour le transfert.</span><span class="sxs-lookup"><span data-stu-id="3da28-205">**Show data for: Forwarding domains**: This view shows the recipient domains that are the destinations for forwarding.</span></span>

  ![Vue des domaines de transfert dans le rapport de transfert](../../media/forwarding-report-forwarding-domains.png)

- <span data-ttu-id="3da28-207">**Afficher les données : redirecteurs**: les redirecteurs suivants sont affichés :</span><span class="sxs-lookup"><span data-stu-id="3da28-207">**Show data for: Forwarders**: The following forwarders are shown:</span></span>

  - <span data-ttu-id="3da28-208">**Règle de transport**</span><span class="sxs-lookup"><span data-stu-id="3da28-208">**Transport rule**</span></span>
  - <span data-ttu-id="3da28-209">Boîte aux lettres qui contient la règle de boîte de réception de transfert.</span><span class="sxs-lookup"><span data-stu-id="3da28-209">The mailbox that contains the forwarding Inbox rule.</span></span>

  ![Vue redirecteurs dans le rapport de transfert](../../media/forwarding-report-forwarders.png)

<span data-ttu-id="3da28-211">Si vous cliquez sur **filtres** dans un affichage de rapport, vous pouvez spécifier une plage de dates avec **Date de début** et date de **fin**.</span><span class="sxs-lookup"><span data-stu-id="3da28-211">If you click **Filters** in a report view, you can specify a date range with **Start date** and **End date**.</span></span>

### <a name="details-table-view-for-the-forwarding-report"></a><span data-ttu-id="3da28-212">Vue de la table Détails pour le rapport de transfert</span><span class="sxs-lookup"><span data-stu-id="3da28-212">Details table view for the Forwarding report</span></span>

<span data-ttu-id="3da28-213">Si vous cliquez sur **afficher la table des détails** dans un affichage de rapport, les informations suivantes s’affichent :</span><span class="sxs-lookup"><span data-stu-id="3da28-213">If you click **View details table** in a report view, the following information is shown:</span></span>

- <span data-ttu-id="3da28-214">**Redirecteurs**: la **règle de transport** value ou la boîte aux lettres qui contient la règle de boîte de réception de transfert.</span><span class="sxs-lookup"><span data-stu-id="3da28-214">**Forwarders**: The value **Transport rule** or the mailbox that contains the forwarding Inbox rule.</span></span>
- <span data-ttu-id="3da28-215">**Type de transfert**: règle de la **boîte aux lettres** ou **règle de transport**.</span><span class="sxs-lookup"><span data-stu-id="3da28-215">**Forwarding type**: The value **Mailbox rule** or **Transport rule**.</span></span>
- <span data-ttu-id="3da28-216">**Nom du destinataire**</span><span class="sxs-lookup"><span data-stu-id="3da28-216">**Recipient name**</span></span>
- <span data-ttu-id="3da28-217">**Domaine du destinataire**</span><span class="sxs-lookup"><span data-stu-id="3da28-217">**Recipient domain**</span></span>
- <span data-ttu-id="3da28-218">**Détails**: il s’agit de la valeur GUID de la règle de flux de messagerie ou de la valeur RuleIdentity de la règle de boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="3da28-218">**Details**: This is the GUID value of the mail flow rule, or the RuleIdentity value of the Inbox rule.</span></span>
- <span data-ttu-id="3da28-219">**Count**</span><span class="sxs-lookup"><span data-stu-id="3da28-219">**Count**</span></span>
- <span data-ttu-id="3da28-220">**Première date de transfert**</span><span class="sxs-lookup"><span data-stu-id="3da28-220">**First forward date**</span></span>

<span data-ttu-id="3da28-221">Si vous cliquez sur **filtres** dans un affichage tableau détaillé, vous pouvez spécifier une plage de dates avec **Date de début** et date de **fin**.</span><span class="sxs-lookup"><span data-stu-id="3da28-221">If you click **Filters** in a details table view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="3da28-222">Pour revenir à l’affichage rapports, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="3da28-222">To go back to the reports view, click **View report**.</span></span>

## <a name="mailflow-status-report"></a><span data-ttu-id="3da28-223">Rapport d’état de flux de flux</span><span class="sxs-lookup"><span data-stu-id="3da28-223">Mailflow status report</span></span>

<span data-ttu-id="3da28-224">Le **rapport d’état de flux** de messagerie est similaire au [rapport de courrier électronique envoyé et reçu](#sent-and-received-email-report), avec des informations supplémentaires sur le courrier électronique autorisé ou bloqué sur le serveur Edge.</span><span class="sxs-lookup"><span data-stu-id="3da28-224">The **Mailflow status report** is similar to the [Sent and received email report](#sent-and-received-email-report), with additional information about email allowed or blocked on the edge.</span></span> <span data-ttu-id="3da28-225">Il s’agit du seul rapport qui contient les informations de protection du serveur Edge et indique le nombre de messages bloqués avant d’être autorisés dans le service pour l’évaluation par Exchange Online Protection (EOP).</span><span class="sxs-lookup"><span data-stu-id="3da28-225">This is the only report that contains edge protection information, and shows just how much email is blocked before being allowed into the service for evaluation by Exchange Online Protection (EOP).</span></span> <span data-ttu-id="3da28-226">Il est important de comprendre que si un message est envoyé à cinq destinataires, nous le dénombrez cinq messages différents et pas un message.</span><span class="sxs-lookup"><span data-stu-id="3da28-226">It's important to understand that if a message is sent to five recipients we count it as five different messages and not one message.</span></span>  
<span data-ttu-id="3da28-227">Pour afficher le rapport, ouvrez le [Centre de sécurité & conformité](https://protection.office.com), accédez **Reports** au \> **tableau de bord** rapports et sélectionnez rapport d’État du **flux de flux**.</span><span class="sxs-lookup"><span data-stu-id="3da28-227">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Mailflow status report**.</span></span> <span data-ttu-id="3da28-228">Pour accéder directement au **rapport d’État du flux de messagerie**, ouvrez <https://protection.office.com/mailflowStatusReport> .</span><span class="sxs-lookup"><span data-stu-id="3da28-228">To go directly to the **Mail flow status report**, open <https://protection.office.com/mailflowStatusReport>.</span></span>

![Widget rapport d’état de flux de notification dans le tableau de bord rapports](../../media/mail-flow-status-report-widget.png)

### <a name="type-view-for-the-mailflow-status-report"></a><span data-ttu-id="3da28-230">Vue type pour le rapport d’état de flux de flux</span><span class="sxs-lookup"><span data-stu-id="3da28-230">Type view for the Mailflow status report</span></span>

<span data-ttu-id="3da28-231">Lorsque vous ouvrez le rapport, l’onglet **type** est sélectionné par défaut.</span><span class="sxs-lookup"><span data-stu-id="3da28-231">When you open the report, the **Type** tab is selected by default.</span></span> <span data-ttu-id="3da28-232">Par défaut, cette vue contient un graphique et une table de données configurée avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="3da28-232">By default, this view contains a chart and a data table that's configured with the following filters:</span></span>

- <span data-ttu-id="3da28-233">**Date**: les 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="3da28-233">**Date**: The last 7 days.</span></span>
- <span data-ttu-id="3da28-234">**Sens**:</span><span class="sxs-lookup"><span data-stu-id="3da28-234">**Direction**:</span></span>

  - <span data-ttu-id="3da28-235">**Entrants**</span><span class="sxs-lookup"><span data-stu-id="3da28-235">**Inbound**</span></span>
  - <span data-ttu-id="3da28-236">**Sortant**</span><span class="sxs-lookup"><span data-stu-id="3da28-236">**Outbound**</span></span>
  - <span data-ttu-id="3da28-237">**Intra-org**: ce nombre est pour les messages au sein d’un client, c’est-à-dire</span><span class="sxs-lookup"><span data-stu-id="3da28-237">**Intra-org**: this count is for messages within a tenant i.e</span></span> <span data-ttu-id="3da28-238">l’expéditeur abc@domain.com envoie au destinataire xyz@domain.com (compté indépendamment des **ports entrants et** **sortants**)</span><span class="sxs-lookup"><span data-stu-id="3da28-238">sender abc@domain.com sends to recipient xyz@domain.com  (counted separately from **Inbound** and **Outbound**)</span></span>

- <span data-ttu-id="3da28-239">**Type**:</span><span class="sxs-lookup"><span data-stu-id="3da28-239">**Type**:</span></span>

  - <span data-ttu-id="3da28-240">**Courrier électronique approprié**</span><span class="sxs-lookup"><span data-stu-id="3da28-240">**Good mail**</span></span>
  - <span data-ttu-id="3da28-241">**Programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="3da28-241">**Malware**</span></span>
  - <span data-ttu-id="3da28-242">**Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="3da28-242">**Spam**</span></span>
  - <span data-ttu-id="3da28-243">**Protection des serveurs Edge**</span><span class="sxs-lookup"><span data-stu-id="3da28-243">**Edge protection**</span></span>
  - <span data-ttu-id="3da28-244">**Messages de règle**</span><span class="sxs-lookup"><span data-stu-id="3da28-244">**Rule messages**</span></span>
  - <span data-ttu-id="3da28-245">**Courriers hameçons**</span><span class="sxs-lookup"><span data-stu-id="3da28-245">**Phishing email**</span></span>

<span data-ttu-id="3da28-246">Le graphique est organisé selon les valeurs de **type** .</span><span class="sxs-lookup"><span data-stu-id="3da28-246">The chart is organized by the **Type** values.</span></span>

<span data-ttu-id="3da28-247">Vous pouvez modifier ces filtres en cliquant sur **Filtrer** ou en cliquant sur une valeur dans la légende du graphique.</span><span class="sxs-lookup"><span data-stu-id="3da28-247">You can changes these filters by clicking **Filter** or by clicking a value in the chart legend.</span></span>

<span data-ttu-id="3da28-248">Le tableau de données contient les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="3da28-248">The data table contains the following information:</span></span>

- <span data-ttu-id="3da28-249">**Direction**</span><span class="sxs-lookup"><span data-stu-id="3da28-249">**Direction**</span></span>
- <span data-ttu-id="3da28-250">**Type**</span><span class="sxs-lookup"><span data-stu-id="3da28-250">**Type**</span></span>
- <span data-ttu-id="3da28-251">**24 heures**</span><span class="sxs-lookup"><span data-stu-id="3da28-251">**24 hours**</span></span>
- <span data-ttu-id="3da28-252">**3 jours**</span><span class="sxs-lookup"><span data-stu-id="3da28-252">**3 days**</span></span>
- <span data-ttu-id="3da28-253">**7 jours**</span><span class="sxs-lookup"><span data-stu-id="3da28-253">**7 days**</span></span>
- <span data-ttu-id="3da28-254">**15 jours**</span><span class="sxs-lookup"><span data-stu-id="3da28-254">**15 days**</span></span>
- <span data-ttu-id="3da28-255">**30 jours**</span><span class="sxs-lookup"><span data-stu-id="3da28-255">**30 days**</span></span>

<span data-ttu-id="3da28-256">Si vous cliquez sur **choisir une catégorie pour plus d’informations**, vous pouvez sélectionner l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="3da28-256">If you click **Choose a category for more details**, you can select from the following values:</span></span>

- <span data-ttu-id="3da28-257">**Courrier électronique de hameçonnage**: cette sélection vous permet d’accéder au [rapport d’état de protection contre les menaces](view-email-security-reports.md#threat-protection-status-report).</span><span class="sxs-lookup"><span data-stu-id="3da28-257">**Phishing email**: This selection takes you to the [Threat protection status report](view-email-security-reports.md#threat-protection-status-report).</span></span>
- <span data-ttu-id="3da28-258">**Programme malveillant dans la messagerie**: cette sélection vous permet d’accéder au [rapport d’état de protection contre les menaces](view-email-security-reports.md#threat-protection-status-report).</span><span class="sxs-lookup"><span data-stu-id="3da28-258">**Malware in email**: This selection takes you to the [Threat protection status report](view-email-security-reports.md#threat-protection-status-report).</span></span>
- <span data-ttu-id="3da28-259">**Détections de courrier indésirable**: cette sélection vous permet d’accéder au [rapport des détections de courrier indésirable](view-email-security-reports.md#spam-detections-report).</span><span class="sxs-lookup"><span data-stu-id="3da28-259">**Spam detections**: This selection takes you to the [Spam Detections report](view-email-security-reports.md#spam-detections-report).</span></span>
- <span data-ttu-id="3da28-260">**Courrier indésirable bloqué**pour le serveur Edge : cette sélection vous permet d’accéder au [rapport des détections de courrier indésirable](view-email-security-reports.md#spam-detections-report).</span><span class="sxs-lookup"><span data-stu-id="3da28-260">**Edge blocked spam**: This selection takes you to the [Spam Detections report](view-email-security-reports.md#spam-detections-report).</span></span>

<span data-ttu-id="3da28-261">**Exportation**:</span><span class="sxs-lookup"><span data-stu-id="3da28-261">**Export**:</span></span>

<span data-ttu-id="3da28-262">Pour l’affichage détaillé, vous pouvez uniquement exporter des données pour un jour.</span><span class="sxs-lookup"><span data-stu-id="3da28-262">For the detail view, you can only export data for one day.</span></span> <span data-ttu-id="3da28-263">Par conséquent, si vous voulez exporter des données pendant 7 jours, vous devez effectuer 7 actions d’exportation différentes.</span><span class="sxs-lookup"><span data-stu-id="3da28-263">So, if you want to export data for 7 days, you need to do 7 different export actions.</span></span>

<span data-ttu-id="3da28-264">Chaque fichier. csv exporté est limité à 150 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="3da28-264">Each exported .csv file is limited to 150,000 rows.</span></span> <span data-ttu-id="3da28-265">Si les données de ce jour contiennent plus de 150 000 lignes, plusieurs fichiers. csv seront créés.</span><span class="sxs-lookup"><span data-stu-id="3da28-265">If the data for that day contains more than 150,000 rows, then multiple .csv files will be created.</span></span>

![<span data-ttu-id="3da28-266">Tapez View dans le rapport d’état de flux de flux</span><span class="sxs-lookup"><span data-stu-id="3da28-266">Type view in the Mailflow status report</span></span> ](../../media/mail-flow-status-report-type-view.png)

### <a name="direction-view-for-the-mailflow-status-report"></a><span data-ttu-id="3da28-267">Vue de direction pour le rapport d’état de flux de flux</span><span class="sxs-lookup"><span data-stu-id="3da28-267">Direction view for the Mailflow status report</span></span>

<span data-ttu-id="3da28-268">Si vous cliquez sur l’onglet **direction** , les mêmes filtres par défaut de la vue **type** sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="3da28-268">If you click the **Direction** tab, the same default filters from the **Type** view are used.</span></span>

<span data-ttu-id="3da28-269">Le graphique est organisé par les valeurs de **direction** .</span><span class="sxs-lookup"><span data-stu-id="3da28-269">The chart is organized by **Direction** values.</span></span>

<span data-ttu-id="3da28-270">Vous pouvez modifier ces filtres en cliquant sur **Filtrer** ou en cliquant sur une valeur dans la légende du graphique.</span><span class="sxs-lookup"><span data-stu-id="3da28-270">You can change these filters by clicking **Filter** or by clicking a value in the chart legend.</span></span> <span data-ttu-id="3da28-271">Les mêmes filtres de la vue **type** sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="3da28-271">The same filters from the **Type** view are used.</span></span>

<span data-ttu-id="3da28-272">La table de données contient les mêmes informations à partir de la vue **type** .</span><span class="sxs-lookup"><span data-stu-id="3da28-272">The data table contains same information from the **Type** view.</span></span>

<span data-ttu-id="3da28-273">La **catégorie choisir une catégorie pour plus de détails** disponibles et les sélections possibles est identique à la vue **type** .</span><span class="sxs-lookup"><span data-stu-id="3da28-273">The **Choose a category for more details** available selections and behavior are the same as the **Type** view.</span></span>

<span data-ttu-id="3da28-274">**Exportation**:</span><span class="sxs-lookup"><span data-stu-id="3da28-274">**Export**:</span></span>

<span data-ttu-id="3da28-275">Pour l’affichage détaillé, vous pouvez uniquement exporter des données pour un jour.</span><span class="sxs-lookup"><span data-stu-id="3da28-275">For the detail view, you can only export data for one day.</span></span> <span data-ttu-id="3da28-276">Par conséquent, si vous voulez exporter des données pendant 7 jours, vous devez effectuer 7 actions d’exportation différentes.</span><span class="sxs-lookup"><span data-stu-id="3da28-276">So, if you want to export data for 7 days, you need to do 7 different export actions.</span></span>

<span data-ttu-id="3da28-277">Chaque fichier. csv exporté est limité à 150 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="3da28-277">Each exported .csv file is limited to 150,000 rows.</span></span> <span data-ttu-id="3da28-278">Si les données de ce jour contiennent plus de 150 000 lignes, plusieurs fichiers. csv seront créés.</span><span class="sxs-lookup"><span data-stu-id="3da28-278">If the data for that day contains more than 150,000 rows, then multiple .csv files will be created.</span></span>

![<span data-ttu-id="3da28-279">Affichage de la direction dans le rapport d’état de flux de flux</span><span class="sxs-lookup"><span data-stu-id="3da28-279">Direction view in the Mailflow status report</span></span> ](../../media/mail-flow-status-report-direction-view.png)

## <a name="sent-and-received-email-report"></a><span data-ttu-id="3da28-280">Rapport de courrier électronique envoyé et reçu</span><span class="sxs-lookup"><span data-stu-id="3da28-280">Sent and received email report</span></span>

<span data-ttu-id="3da28-281">Le rapport de **courrier électronique envoyé et reçu** est un rapport intelligent qui affiche des informations sur les messages entrants et sortants, notamment les détections de courrier indésirable, les programmes malveillants et la messagerie électronique identifiés comme étant « en qualité ».</span><span class="sxs-lookup"><span data-stu-id="3da28-281">The **Sent and received email** report is a smart report that shows information about incoming and outgoing email, including spam detections, malware, and email identified as "good."</span></span> <span data-ttu-id="3da28-282">La différence entre ce rapport et le [rapport d’état de flux](#mailflow-status-report) de courrier est la suivante : ce rapport n’inclut pas de données sur les messages bloqués par la protection du serveur Edge.</span><span class="sxs-lookup"><span data-stu-id="3da28-282">The difference between this report and the [Mailflow status report](#mailflow-status-report) is: this report doesn't include data about messages blocked by edge protection.</span></span>

<span data-ttu-id="3da28-283">L’affichage Aggregate et l’affichage détaillé du rapport autorisent 90 jours de filtrage.</span><span class="sxs-lookup"><span data-stu-id="3da28-283">The aggregate view and the detail view of the report allow for 90 days of filtering.</span></span>

<span data-ttu-id="3da28-284">Pour afficher le rapport, ouvrez le [Centre de sécurité & conformité](https://protection.office.com), accédez **Reports** au \> **tableau de bord** rapports et sélectionnez **Envoyer et recevoir un message**.</span><span class="sxs-lookup"><span data-stu-id="3da28-284">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Sent and received email**.</span></span> <span data-ttu-id="3da28-285">Pour accéder directement au rapport, ouvrez <https://protection.office.com/reportv2?id=SentAndReceivedMailATP> .</span><span class="sxs-lookup"><span data-stu-id="3da28-285">To go directly to the report, open <https://protection.office.com/reportv2?id=SentAndReceivedMailATP>.</span></span>

![Widget courrier électronique envoyé et reçu dans le tableau de bord rapports](../../media/sent-and-received-email-report-widget.png)

### <a name="report-view-for-the-sent-and-received-email-report"></a><span data-ttu-id="3da28-287">Affichage de rapport pour le rapport de courrier électronique envoyé et reçu</span><span class="sxs-lookup"><span data-stu-id="3da28-287">Report view for the Sent and received email report</span></span>

<span data-ttu-id="3da28-288">Les graphiques suivants sont disponibles dans l’affichage rapport :</span><span class="sxs-lookup"><span data-stu-id="3da28-288">The following charts are available in the report view:</span></span>

- <span data-ttu-id="3da28-289">**Décomposer en : type**: le graphique affiche toutes les catégories disponibles :</span><span class="sxs-lookup"><span data-stu-id="3da28-289">**Break down by: Type**: The chart shows all available categories:</span></span>

  - <span data-ttu-id="3da28-290">**Total**</span><span class="sxs-lookup"><span data-stu-id="3da28-290">**Total**</span></span>
  - <span data-ttu-id="3da28-291">**Courrier électronique approprié**</span><span class="sxs-lookup"><span data-stu-id="3da28-291">**Good mail**</span></span>
  - <span data-ttu-id="3da28-292">**Programme malveillant (blocage des programmes malveillants)** (EoP)</span><span class="sxs-lookup"><span data-stu-id="3da28-292">**Malware (anti-malware)** (EOP)</span></span>
  - <span data-ttu-id="3da28-293">**Détections de courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="3da28-293">**Spam detections**</span></span>
  - <span data-ttu-id="3da28-294">**Messages de règle**</span><span class="sxs-lookup"><span data-stu-id="3da28-294">**Rule messages**</span></span>
  - <span data-ttu-id="3da28-295">**Programme malveillant avancé** (Office 365 ATP)</span><span class="sxs-lookup"><span data-stu-id="3da28-295">**Advanced malware** (Office 365 ATP)</span></span>

  <span data-ttu-id="3da28-296">Lorsque vous placez le curseur de la souris sur un jour (point de données) dans le graphique, vous pouvez afficher les détails de ce jour.</span><span class="sxs-lookup"><span data-stu-id="3da28-296">When you hover over a day (data point) in the chart, you can see details for that day.</span></span>

  ![Type de vue dans le rapport des courriers électroniques envoyés et reçus](../../media/sent-and-received-email-report-type-view.png)

- <span data-ttu-id="3da28-298">**Décomposer en : sens**: le graphique indique le **total**, les données **entrantes**et **sortantes** .</span><span class="sxs-lookup"><span data-stu-id="3da28-298">**Break down by: Direction**: The chart shows **Total**, **Inbound**, and **Outbound** data.</span></span> <span data-ttu-id="3da28-299">Lorsque vous placez le curseur de la souris sur un jour (point de données) dans le graphique, vous pouvez afficher les détails de ce jour.</span><span class="sxs-lookup"><span data-stu-id="3da28-299">When you hover over a day (data point) in the chart, you can see details for that day.</span></span>

  ![Affichage de la direction dans le rapport de courrier électronique envoyé et reçu](../../media/sent-and-received-email-report-direction-view.png)

- <span data-ttu-id="3da28-301">**Explorer en détail** \> **Programme malveillant (anti-programme malveillant)**: cette sélection vous permet d’accéder aux [détections de programmes malveillants dans le rapport par courrier électronique](view-email-security-reports.md#malware-detections-in-email-report).</span><span class="sxs-lookup"><span data-stu-id="3da28-301">**Drill down by** \> **Malware (anti-malware)**: This selection takes you to the [Malware detections in email report](view-email-security-reports.md#malware-detections-in-email-report).</span></span>

- <span data-ttu-id="3da28-302">**Explorer en détail** \> **Détections de courrier indésirable)**: cette sélection vous permet d’accéder au [rapport des détections de courrier indésirable](view-email-security-reports.md#spam-detections-report).</span><span class="sxs-lookup"><span data-stu-id="3da28-302">**Drill down by** \> **Spam detections)**: This selection takes you to the [Spam Detections report](view-email-security-reports.md#spam-detections-report).</span></span>

<span data-ttu-id="3da28-303">Si vous cliquez sur **filtres** dans un affichage de rapport, vous pouvez modifier les résultats à l’aide des filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="3da28-303">If you click **Filters** in a report view, you can modify the results with the following filters:</span></span>

- <span data-ttu-id="3da28-304">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="3da28-304">**Start date** and **End date**</span></span>
- <span data-ttu-id="3da28-305">Valeurs de la direction</span><span class="sxs-lookup"><span data-stu-id="3da28-305">Direction values</span></span>
- <span data-ttu-id="3da28-306">Valeurs de type</span><span class="sxs-lookup"><span data-stu-id="3da28-306">Type values</span></span>

<span data-ttu-id="3da28-307">Pour revenir à l’affichage de rapport, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="3da28-307">To go back to the report view, click **View report**.</span></span>

### <a name="details-table-view-for-the-sent-and-received-email-report"></a><span data-ttu-id="3da28-308">Vue de la table des détails pour le rapport de courrier électronique envoyé et reçu</span><span class="sxs-lookup"><span data-stu-id="3da28-308">Details table view for the Sent and received email report</span></span>

<span data-ttu-id="3da28-309">Si vous cliquez sur **afficher les détails** de la table dans la fenêtre dépanner **par : direction** ou dépanner **par :** le mode de direction, les informations suivantes sont affichées :</span><span class="sxs-lookup"><span data-stu-id="3da28-309">If you click **View details table** in the **Break down by: Direction** or **Break down by: Direction** view, the following information is shown:</span></span>

- <span data-ttu-id="3da28-310">**Date (UTC)**</span><span class="sxs-lookup"><span data-stu-id="3da28-310">**Date (UTC)**</span></span>
- <span data-ttu-id="3da28-311">**Type**</span><span class="sxs-lookup"><span data-stu-id="3da28-311">**Type**</span></span>
- <span data-ttu-id="3da28-312">**Direction**</span><span class="sxs-lookup"><span data-stu-id="3da28-312">**Direction**</span></span>
- <span data-ttu-id="3da28-313">**Nombre de messages**</span><span class="sxs-lookup"><span data-stu-id="3da28-313">**Message count**</span></span>

<span data-ttu-id="3da28-314">Si vous cliquez sur **filtres** dans un affichage tableau détaillé, vous pouvez modifier les résultats à l’aide des filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="3da28-314">If you click **Filters** in a details table view, you can modify the results with the following filters:</span></span>

- <span data-ttu-id="3da28-315">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="3da28-315">**Start date** and **End date**</span></span>
- <span data-ttu-id="3da28-316">Valeurs de la direction</span><span class="sxs-lookup"><span data-stu-id="3da28-316">Direction values</span></span>
- <span data-ttu-id="3da28-317">Valeurs de type</span><span class="sxs-lookup"><span data-stu-id="3da28-317">Type values</span></span>

<span data-ttu-id="3da28-318">Pour revenir à l’affichage de rapport, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="3da28-318">To go back to the report view, click **View report**.</span></span>

## <a name="top-senders-and-recipients-report"></a><span data-ttu-id="3da28-319">Rapport des expéditeurs et des destinataires principaux</span><span class="sxs-lookup"><span data-stu-id="3da28-319">Top senders and recipients report</span></span>

<span data-ttu-id="3da28-320">Le rapport des **expéditeurs et des destinataires principaux** est un graphique en secteurs illustrant les principaux expéditeurs et destinataires de votre courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="3da28-320">The **Top senders and recipients** report is a pie chart showing your top email senders and recipients.</span></span>

<span data-ttu-id="3da28-321">Pour afficher le rapport, ouvrez le [Centre de sécurité & conformité](https://protection.office.com), accédez à **rapports** \> **Dashboard** et sélectionnez **principaux expéditeurs et destinataires**.</span><span class="sxs-lookup"><span data-stu-id="3da28-321">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Top senders and recipients**.</span></span> <span data-ttu-id="3da28-322">Pour accéder directement au rapport, ouvrez <https://protection.office.com/reportv2?id=TopSenderRecipientsATP> .</span><span class="sxs-lookup"><span data-stu-id="3da28-322">To go directly to the report, open <https://protection.office.com/reportv2?id=TopSenderRecipientsATP>.</span></span>

![Widget principaux expéditeurs et destinataires dans le tableau de bord rapports](../../media/top-senders-and-recipients-widget.png)

### <a name="report-view-for-the-top-senders-and-recipient-report"></a><span data-ttu-id="3da28-324">Affichage de rapport pour le rapport des expéditeurs et des destinataires principaux</span><span class="sxs-lookup"><span data-stu-id="3da28-324">Report view for the Top senders and recipient report</span></span>

<span data-ttu-id="3da28-325">Les graphiques suivants sont disponibles dans l’affichage rapport :</span><span class="sxs-lookup"><span data-stu-id="3da28-325">The following charts are available in the report view:</span></span>

- <span data-ttu-id="3da28-326">**Afficher les données des \> expéditeurs de messages principaux**</span><span class="sxs-lookup"><span data-stu-id="3da28-326">**Show data for \> Top mail senders**</span></span>
- <span data-ttu-id="3da28-327">**Afficher les données des \> destinataires de messagerie les plus fréquents**</span><span class="sxs-lookup"><span data-stu-id="3da28-327">**Show data for \> Top mail recipients**</span></span>
- <span data-ttu-id="3da28-328">**Afficher les données pour les \> destinataires de courrier indésirable principaux**</span><span class="sxs-lookup"><span data-stu-id="3da28-328">**Show data for \> Top spam recipients**</span></span>
- <span data-ttu-id="3da28-329">**Afficher les données pour \> Principaux destinataires de programmes malveillants** (EoP)</span><span class="sxs-lookup"><span data-stu-id="3da28-329">**Show data for \> Top malware recipients** (EOP)</span></span>
- <span data-ttu-id="3da28-330">**Afficher les données pour \> Principaux destinataires de programmes malveillants (ATP)** (Office 365 ATP)</span><span class="sxs-lookup"><span data-stu-id="3da28-330">**Show data for \> Top malware recipients (ATP)** (Office 365 ATP)</span></span>

<span data-ttu-id="3da28-331">La composition du graphique en secteurs est modifiée en fonction de ces sélections.</span><span class="sxs-lookup"><span data-stu-id="3da28-331">The composition of the pie chart changes based on these selections.</span></span>

<span data-ttu-id="3da28-332">Lorsque vous placez le curseur de la souris sur un coin du graphique en secteurs, vous pouvez voir le nombre de messages envoyés ou reçus.</span><span class="sxs-lookup"><span data-stu-id="3da28-332">When you hover over a wedge in the pie chart, you can see a count of messages sent or received.</span></span>

<span data-ttu-id="3da28-333">Si vous cliquez sur **filtres** dans un affichage de rapport, vous pouvez spécifier une plage de dates avec **Date de début** et date de **fin**.</span><span class="sxs-lookup"><span data-stu-id="3da28-333">If you click **Filters** in a report view, you can specify a date range with **Start date** and **End date**.</span></span>

![Graphique en secteurs en mode état dans le rapport des expéditeurs et destinataires principaux](../../media/top-senders-and-recipients-report-view.png)

### <a name="details-table-view-for-the-top-senders-and-recipient-report"></a><span data-ttu-id="3da28-335">Vue de la table Détails pour le rapport des expéditeurs et des destinataires principaux</span><span class="sxs-lookup"><span data-stu-id="3da28-335">Details table view for the Top senders and recipient report</span></span>

<span data-ttu-id="3da28-336">Si vous cliquez sur **afficher les détails table**, les informations affichées dépendent du graphique que vous examinez :</span><span class="sxs-lookup"><span data-stu-id="3da28-336">If you click **View details table**, the information that's shown depends on the chart you were looking at:</span></span>

- <span data-ttu-id="3da28-337">**Afficher les données des \> expéditeurs de messages principaux**</span><span class="sxs-lookup"><span data-stu-id="3da28-337">**Show data for \> Top mail senders**</span></span>

  - <span data-ttu-id="3da28-338">**Principaux expéditeurs de messagerie**</span><span class="sxs-lookup"><span data-stu-id="3da28-338">**Top mail senders**</span></span>
  - <span data-ttu-id="3da28-339">**Count**</span><span class="sxs-lookup"><span data-stu-id="3da28-339">**Count**</span></span>

- <span data-ttu-id="3da28-340">**Afficher les données des \> destinataires de messagerie les plus fréquents**</span><span class="sxs-lookup"><span data-stu-id="3da28-340">**Show data for \> Top mail recipients**</span></span>

  - <span data-ttu-id="3da28-341">**Principaux destinataires de messagerie**</span><span class="sxs-lookup"><span data-stu-id="3da28-341">**Top mail recipients**</span></span>
  - <span data-ttu-id="3da28-342">**Count**</span><span class="sxs-lookup"><span data-stu-id="3da28-342">**Count**</span></span>

- <span data-ttu-id="3da28-343">**Afficher les données pour les \> destinataires de courrier indésirable principaux**</span><span class="sxs-lookup"><span data-stu-id="3da28-343">**Show data for \> Top spam recipients**</span></span>

  - <span data-ttu-id="3da28-344">**Principaux destinataires de courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="3da28-344">**Top spam recipients**</span></span>
  - <span data-ttu-id="3da28-345">**Count**</span><span class="sxs-lookup"><span data-stu-id="3da28-345">**Count**</span></span>

- <span data-ttu-id="3da28-346">**Afficher les données pour \> Principaux destinataires de programmes malveillants** (EoP)</span><span class="sxs-lookup"><span data-stu-id="3da28-346">**Show data for \> Top malware recipients** (EOP)</span></span>

  - <span data-ttu-id="3da28-347">**Principaux destinataires de programmes malveillants**</span><span class="sxs-lookup"><span data-stu-id="3da28-347">**Top malware recipients**</span></span>
  - <span data-ttu-id="3da28-348">**Count**</span><span class="sxs-lookup"><span data-stu-id="3da28-348">**Count**</span></span>

- <span data-ttu-id="3da28-349">**Afficher les données pour \> Principaux destinataires de programmes malveillants (ATP)** (Office 365 ATP)</span><span class="sxs-lookup"><span data-stu-id="3da28-349">**Show data for \> Top malware recipients (ATP)** (Office 365 ATP)</span></span>

  - <span data-ttu-id="3da28-350">**Principaux destinataires de programmes malveillants (ATP)**</span><span class="sxs-lookup"><span data-stu-id="3da28-350">**Top malware recipients (ATP)**</span></span>
  - <span data-ttu-id="3da28-351">**Count**</span><span class="sxs-lookup"><span data-stu-id="3da28-351">**Count**</span></span>

<span data-ttu-id="3da28-352">Si vous cliquez sur **filtres** dans un affichage tableau détaillé, vous pouvez spécifier une plage de dates avec **Date de début** et date de **fin**.</span><span class="sxs-lookup"><span data-stu-id="3da28-352">If you click **Filters** in a details table view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="3da28-353">Pour revenir à l’affichage de rapport, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="3da28-353">To go back to the report view, click **View report**.</span></span>

## <a name="what-permissions-are-needed-to-view-these-reports"></a><span data-ttu-id="3da28-354">Quelles sont les autorisations nécessaires pour afficher ces rapports ?</span><span class="sxs-lookup"><span data-stu-id="3da28-354">What permissions are needed to view these reports?</span></span>

<span data-ttu-id="3da28-355">Pour afficher et utiliser les rapports, vous devez être membre du groupe de rôles spécifié dans le centre de sécurité & conformité **et** dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="3da28-355">To view and use the reports, you need to be a member of the specified role group in the Security & Compliance Center **and** in Exchange Online.</span></span>

- <span data-ttu-id="3da28-356">Dans le centre de sécurité & conformité, vous devez être membre de l’un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="3da28-356">In the Security & Compliance Center, you need to be a member of one of the following role groups:</span></span>

  <span data-ttu-id="3da28-357">-Gestion de l’organisation-administrateur de la sécurité (vous pouvez également le faire dans le [Centre d’administration Azure Active Directory](https://aad.portal.azure.com) -lecteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="3da28-357">-Organization Management -Security Administrator (you can also do this in the [Azure Active Directory admin center](https://aad.portal.azure.com) -Security Reader</span></span>

  <span data-ttu-id="3da28-358">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](https://docs.microsoft.com/microsoft-365/security/office-365-security/permissions-in-the-security-and-compliance-center).</span><span class="sxs-lookup"><span data-stu-id="3da28-358">For more information, see [Permissions in the Security & Compliance Center](https://docs.microsoft.com/microsoft-365/security/office-365-security/permissions-in-the-security-and-compliance-center).</span></span>

- <span data-ttu-id="3da28-359">Dans Exchange Online, vous devez être membre de l’un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="3da28-359">In Exchange Online, you need to be a member of one of the following role groups:</span></span>

  <span data-ttu-id="3da28-360">-Gestion de l’organisation-affichage uniquement-gestion de l’organisation-affichage uniquement des destinataires-gestion de la conformité</span><span class="sxs-lookup"><span data-stu-id="3da28-360">-Organization Management -View-only Organization Management -View-Only Recipients -Compliance Management</span></span>

<span data-ttu-id="3da28-361">Pour plus d’informations, consultez la rubrique [autorisations dans Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo) et [gérer les groupes de rôles dans Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/role-groups).</span><span class="sxs-lookup"><span data-stu-id="3da28-361">For more information, see [Permissions in Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo) and [Manage role groups in Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/role-groups).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3da28-362">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3da28-362">Related topics</span></span>

[<span data-ttu-id="3da28-363">Rapports intelligents et aperçus dans le Centre de sécurité et conformité</span><span class="sxs-lookup"><span data-stu-id="3da28-363">Smart reports and insights in the Security & Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)

[<span data-ttu-id="3da28-364">Informations sur le flux de messagerie dans le centre de sécurité et conformité</span><span class="sxs-lookup"><span data-stu-id="3da28-364">Mail flow insights in the Security & Compliance Center</span></span>](mail-flow-insights-v2.md)

[<span data-ttu-id="3da28-365">Afficher les rapports de sécurité de courrier dans le centre de sécurité et conformité</span><span class="sxs-lookup"><span data-stu-id="3da28-365">View email security reports in the Security & Compliance Center</span></span>](view-email-security-reports.md)

[<span data-ttu-id="3da28-366">Afficher les rapports pour Office 365 protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="3da28-366">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)
