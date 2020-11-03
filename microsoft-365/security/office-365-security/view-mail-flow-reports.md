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
ms.openlocfilehash: a7e298a2cc3a5a33fbf4ed281d0ddd52b026096d
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48842983"
---
# <a name="view-mail-flow-reports-in-the-reports-dashboard-in-security--compliance-center"></a><span data-ttu-id="234e1-103">Afficher les rapports de flux de messagerie dans le tableau de bord rapports du centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="234e1-103">View mail flow reports in the Reports dashboard in Security & Compliance Center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="234e1-104">En plus des rapports de flux de messagerie disponibles dans le [tableau de bord de flux de messagerie](mail-flow-insights-v2.md) dans le centre de sécurité & conformité, un grand nombre de rapports de flux de messagerie supplémentaires sont disponibles dans le tableau de bord rapports pour vous aider à surveiller votre organisation Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="234e1-104">In addition to the mail flow reports that are available in the [Mail flow dashboard](mail-flow-insights-v2.md) in the Security & Compliance Center, a variety of additional mail flow reports are available in the Reports dashboard to help you monitor your Microsoft 365 organization.</span></span>

<span data-ttu-id="234e1-105">Si vous disposez des [autorisations nécessaires](#what-permissions-are-needed-to-view-these-reports), vous pouvez afficher ces rapports dans le [Centre de sécurité & conformité](https://office.protection.com) en accédant au tableau de **Reports** \> **bord** rapports.</span><span class="sxs-lookup"><span data-stu-id="234e1-105">If you have the [necessary permissions](#what-permissions-are-needed-to-view-these-reports), you can view these reports in the [Security & Compliance Center](https://office.protection.com) by going to **Reports** \> **Dashboard**.</span></span> <span data-ttu-id="234e1-106">Pour accéder directement au tableau de bord rapports, ouvrez <https://protection.office.com/insightdashboard> .</span><span class="sxs-lookup"><span data-stu-id="234e1-106">To go directly to the Reports dashboard, open <https://protection.office.com/insightdashboard>.</span></span>

![Tableau de bord des rapports dans le centre de sécurité & conformité](../../media/6b213d34-adbb-44af-8549-be9a7e2db087.png)

## <a name="connector-report"></a><span data-ttu-id="234e1-108">Rapport de connecteur</span><span class="sxs-lookup"><span data-stu-id="234e1-108">Connector report</span></span>

<span data-ttu-id="234e1-109">Le **rapport de connecteur** affiche l’activité de flux de messagerie sur les connecteurs entrants [et sortants](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow) configurés pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="234e1-109">The **Connector report** shows mail flow activity on the [inbound and outbound connectors](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow) that are configured for your organization.</span></span>

<span data-ttu-id="234e1-110">Pour afficher le rapport, ouvrez le [Centre de sécurité & conformité](https://protection.office.com), accédez **Reports** au \> **tableau de bord** rapports et sélectionnez rapport de **connecteur**.</span><span class="sxs-lookup"><span data-stu-id="234e1-110">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Connector report**.</span></span> <span data-ttu-id="234e1-111">Pour accéder directement au rapport, ouvrez <https://protection.office.com/reportv2?id=ConnectorReport> .</span><span class="sxs-lookup"><span data-stu-id="234e1-111">To go directly to the report, open <https://protection.office.com/reportv2?id=ConnectorReport>.</span></span>

![Widget rapport de connecteur dans le tableau de bord rapports](../../media/connector-report-widget.png)

### <a name="report-view-for-the-connector-report"></a><span data-ttu-id="234e1-113">Affichage de rapport pour le rapport de connecteur</span><span class="sxs-lookup"><span data-stu-id="234e1-113">Report view for the Connector report</span></span>

<span data-ttu-id="234e1-114">Les graphiques suivants sont disponibles en mode état :</span><span class="sxs-lookup"><span data-stu-id="234e1-114">The following charts are available in report view:</span></span>

- <span data-ttu-id="234e1-115">**Afficher les données par : flux de messagerie** : ce graphique indique le nombre de messages entrants et sortants organisés par :</span><span class="sxs-lookup"><span data-stu-id="234e1-115">**View data by: Mail flow** : This chart shows the number of inbound and outbound messages organized by:</span></span>

  - <span data-ttu-id="234e1-116">**Total**</span><span class="sxs-lookup"><span data-stu-id="234e1-116">**Total**</span></span>
  - <span data-ttu-id="234e1-117">**À partir d’Internet sans connecteur**</span><span class="sxs-lookup"><span data-stu-id="234e1-117">**From the internet without a connector**</span></span>
  - <span data-ttu-id="234e1-118">**Sur Internet sans connecteur**</span><span class="sxs-lookup"><span data-stu-id="234e1-118">**To the internet without a connector**</span></span>
  - <span data-ttu-id="234e1-119">Un connecteur spécifique que vous avez configuré.</span><span class="sxs-lookup"><span data-stu-id="234e1-119">A specific connector that you've configured.</span></span>

  <span data-ttu-id="234e1-120">Pour isoler les données du graphique, utilisez l’option **afficher les données pour** le contrôle pour sélectionner une de ces options ou **tout le flux de messagerie**.</span><span class="sxs-lookup"><span data-stu-id="234e1-120">To isolate the data in the chart, use the **Show data for** control to select one of these options or **All mail flow**.</span></span>

  ![Afficher les données par flux de messagerie dans le rapport du connecteur](../../media/connector-report-view-data-by-mail-flow.png)

- <span data-ttu-id="234e1-122">**Afficher les données par : utilisation de TLS** : ce graphique indique le pourcentage d’utilisation de la version TLS (Transport Layer Security) pour le flux de messagerie.</span><span class="sxs-lookup"><span data-stu-id="234e1-122">**View data by: TLS usage** : This chart shows the percentage of Transport Layer Security (TLS) version usage for mail flow.</span></span>

  <span data-ttu-id="234e1-123">Pour isoler les données dans le graphique, utilisez l’option **afficher les données pour** le contrôle afin de sélectionner l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="234e1-123">To isolate the data in the chart, use the **Show data for** control to select one of the following options:</span></span>

  - <span data-ttu-id="234e1-124">**Tout le flux de messagerie**</span><span class="sxs-lookup"><span data-stu-id="234e1-124">**All mail flow**</span></span>
  - <span data-ttu-id="234e1-125">**À partir d’Internet sans connecteur**</span><span class="sxs-lookup"><span data-stu-id="234e1-125">**From the internet without a connector**</span></span>
  - <span data-ttu-id="234e1-126">**Sur Internet sans connecteur**</span><span class="sxs-lookup"><span data-stu-id="234e1-126">**To the internet without a connector**</span></span>
  - <span data-ttu-id="234e1-127">Un connecteur spécifique que vous avez configuré.</span><span class="sxs-lookup"><span data-stu-id="234e1-127">A specific connector that you've configured.</span></span>

  ![Afficher les données par utilisation de TLS dans le rapport de connecteur](../../media/connector-report-view-data-by-tls-usage.png)

<span data-ttu-id="234e1-129">Si vous cliquez sur **filtres** dans un affichage de rapport, vous pouvez spécifier une plage de dates avec **Date de début** et date de **fin**.</span><span class="sxs-lookup"><span data-stu-id="234e1-129">If you click **Filters** in a report view, you can specify a date range with **Start date** and **End date**.</span></span>

### <a name="details-table-view-for-the-connector-report"></a><span data-ttu-id="234e1-130">Vue de la table Détails pour le rapport de connecteur</span><span class="sxs-lookup"><span data-stu-id="234e1-130">Details table view for the Connector report</span></span>

<span data-ttu-id="234e1-131">Si vous cliquez sur **afficher la table des détails** dans un affichage de rapport, les informations suivantes s’affichent :</span><span class="sxs-lookup"><span data-stu-id="234e1-131">If you click **View details table** in a report view, the following information is shown:</span></span>

- <span data-ttu-id="234e1-132">**Date**</span><span class="sxs-lookup"><span data-stu-id="234e1-132">**Date**</span></span>
- <span data-ttu-id="234e1-133">**Nom et direction du connecteur**</span><span class="sxs-lookup"><span data-stu-id="234e1-133">**Connector direction and name**</span></span>
- <span data-ttu-id="234e1-134">**Type de connecteur**</span><span class="sxs-lookup"><span data-stu-id="234e1-134">**Connector type**</span></span>
- <span data-ttu-id="234e1-135">**TLS forcé ?** : valeur **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="234e1-135">**Forced TLS?** : The value **True** or **False**.</span></span>
- <span data-ttu-id="234e1-136">**Pas de TLS** (pourcentage)</span><span class="sxs-lookup"><span data-stu-id="234e1-136">**No TLS** (percentage)</span></span>
- <span data-ttu-id="234e1-137">**TLS 1,0** (pourcentage)</span><span class="sxs-lookup"><span data-stu-id="234e1-137">**TLS 1.0** (percentage)</span></span>
- <span data-ttu-id="234e1-138">**TLS 1,1** (pourcentage)</span><span class="sxs-lookup"><span data-stu-id="234e1-138">**TLS 1.1** (percentage)</span></span>
- <span data-ttu-id="234e1-139">**TLS 1,2** (pourcentage)</span><span class="sxs-lookup"><span data-stu-id="234e1-139">**TLS 1.2** (percentage)</span></span>
- <span data-ttu-id="234e1-140">**Volume** : nombre de messages.</span><span class="sxs-lookup"><span data-stu-id="234e1-140">**Volume** : The number of messages.</span></span>

<span data-ttu-id="234e1-141">Si vous cliquez sur **filtres** dans un affichage tableau détaillé, vous pouvez spécifier une plage de dates avec **Date de début** et date de **fin**.</span><span class="sxs-lookup"><span data-stu-id="234e1-141">If you click **Filters** in a details table view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="234e1-142">Pour revenir à l’affichage de rapport, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="234e1-142">To go back to the report view, click **View report**.</span></span>

## <a name="exchange-transport-rule-report"></a><span data-ttu-id="234e1-143">Rapport de règle de transport Exchange</span><span class="sxs-lookup"><span data-stu-id="234e1-143">Exchange transport rule report</span></span>

<span data-ttu-id="234e1-144">Le rapport des règles de **transport Exchange** affiche l’effet des règles de flux de messagerie (également appelées règles de transport) sur les messages entrants et sortants dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="234e1-144">The **Exchange transport rule report** shows the effect of mail flow rules (also known as transport rules) on incoming and outgoing messages in your organization.</span></span>

<span data-ttu-id="234e1-145">Pour afficher le rapport, ouvrez le [Centre de sécurité & conformité](https://protection.office.com), accédez **Reports** au \> **tableau de bord** rapports et sélectionnez **règle de transport Exchange**.</span><span class="sxs-lookup"><span data-stu-id="234e1-145">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Exchange Transport rule**.</span></span> <span data-ttu-id="234e1-146">Pour accéder directement au rapport, ouvrez <https://protection.office.com/reportv2?id=ETRRuleReport> .</span><span class="sxs-lookup"><span data-stu-id="234e1-146">To go directly to the report, open <https://protection.office.com/reportv2?id=ETRRuleReport>.</span></span>

![Widget règle de transport Exchange dans le tableau de bord rapports](../../media/transport-rule-report-widget.png)

### <a name="report-view-for-the-exchange-transport-rule-report"></a><span data-ttu-id="234e1-148">Affichage de rapport pour le rapport des règles de transport Exchange</span><span class="sxs-lookup"><span data-stu-id="234e1-148">Report view for the Exchange transport rule report</span></span>

<span data-ttu-id="234e1-149">Les graphiques suivants sont disponibles en mode état :</span><span class="sxs-lookup"><span data-stu-id="234e1-149">The following charts are available in report view:</span></span>

- <span data-ttu-id="234e1-150">**Afficher les données par : règles** \> de transport Exchange **Décomposer en : sens** : ce graphique indique le **nombre de messages entrants** et **sortants** affectés par les règles de transport.</span><span class="sxs-lookup"><span data-stu-id="234e1-150">**View data by: Exchange transport rules** \> **Break down by: Direction** : This chart shows the number of **Inbound** and **Outbound** messages that were affected by transport rules.</span></span>

- <span data-ttu-id="234e1-151">**Afficher les données par : règles** \> de transport Exchange Dépanner **par : gravité** : ce graphique indique le nombre de messages de gravité **élevée** et de gravité **moyenne** , ainsi que les messages à **faible gravité** .</span><span class="sxs-lookup"><span data-stu-id="234e1-151">**View data by: Exchange transport rules** \> **Break down by: Severity** : This chart shows the number of **High severity** and **Medium severity** , and **Low severity** messages.</span></span> <span data-ttu-id="234e1-152">Vous définissez le niveau de gravité en tant qu’action dans la règle ( **auditez cette règle avec le niveau de gravité** ou _SetAuditSeverity_ ).</span><span class="sxs-lookup"><span data-stu-id="234e1-152">You set the severity level as an action in the rule ( **Audit this rule with severity level** or _SetAuditSeverity_ ).</span></span> <span data-ttu-id="234e1-153">Pour plus d’informations, consultez la rubrique [actions de règle de flux de messagerie dans Exchange Online](https://docs.microsoft.com//Exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions).</span><span class="sxs-lookup"><span data-stu-id="234e1-153">For more information, see [Mail flow rule actions in Exchange Online](https://docs.microsoft.com//Exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions).</span></span>

- <span data-ttu-id="234e1-154">**Afficher les données par : DLP Exchange transport Rules** \> **Décomposer en : sens** : ce graphique indique le **nombre de messages entrants** et **sortants** affectés par les règles de transport de la protection contre la perte de données (DLP).</span><span class="sxs-lookup"><span data-stu-id="234e1-154">**View data by: DLP Exchange transport rules** \> **Break down by: Direction** : This chart shows the number of **Inbound** and **Outbound** messages that were affected by data loss prevention (DLP) transport rules.</span></span> <span data-ttu-id="234e1-155">Vous pouvez affiner le graphique en sélectionnant l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="234e1-155">You can further refine the chart by selecting on of the following options:</span></span>

  - <span data-ttu-id="234e1-156">**Afficher les données pour : toutes les règles de transport DLP**</span><span class="sxs-lookup"><span data-stu-id="234e1-156">**Show data for: All DLP transport rules**</span></span>
  - <span data-ttu-id="234e1-157">**Afficher les données de : utilisateurs compromis**</span><span class="sxs-lookup"><span data-stu-id="234e1-157">**Show data for: Compromised users**</span></span>
  - <span data-ttu-id="234e1-158">**Afficher les données pour : faible volume de contenu détecté par les États-Unis Patriot Act**</span><span class="sxs-lookup"><span data-stu-id="234e1-158">**Show data for: Low volume of content detected U.S. Patriot Act**</span></span>

- <span data-ttu-id="234e1-159">**Afficher les données par : DLP Exchange transport Rules** \> **Décomposer en : sens** : cette vue indique le nombre de messages de gravité **élevée** et de gravité **moyenne** , ainsi que les messages à **faible gravité** qui ont été affectés par les règles de transport DLP.</span><span class="sxs-lookup"><span data-stu-id="234e1-159">**View data by: DLP Exchange transport rules** \> **Break down by: Direction** : This view shows the number of **High severity** and **Medium severity** , and **Low severity** messages that were affected by DLP transport rules.</span></span> <span data-ttu-id="234e1-160">Vous pouvez affiner le graphique en sélectionnant l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="234e1-160">You can further refine the chart by selecting on of the following options:</span></span>

  - <span data-ttu-id="234e1-161">**Afficher les données pour : toutes les règles de transport DLP**</span><span class="sxs-lookup"><span data-stu-id="234e1-161">**Show data for: All DLP transport rules**</span></span>
  - <span data-ttu-id="234e1-162">**Afficher les données de : utilisateurs compromis**</span><span class="sxs-lookup"><span data-stu-id="234e1-162">**Show data for: Compromised users**</span></span>
  - <span data-ttu-id="234e1-163">**Afficher les données pour : faible volume de contenu détecté par les États-Unis Patriot Act**</span><span class="sxs-lookup"><span data-stu-id="234e1-163">**Show data for: Low volume of content detected U.S. Patriot Act**</span></span>

<span data-ttu-id="234e1-164">Si vous cliquez sur **filtres** dans un affichage de rapport, vous pouvez modifier les résultats à l’aide des filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="234e1-164">If you click **Filters** in a report view, you can modify the results with the following filters::</span></span>

- <span data-ttu-id="234e1-165">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="234e1-165">**Start date** and **End date**</span></span>
- <span data-ttu-id="234e1-166">Valeurs de la direction</span><span class="sxs-lookup"><span data-stu-id="234e1-166">Direction values</span></span>
- <span data-ttu-id="234e1-167">Valeurs de gravité</span><span class="sxs-lookup"><span data-stu-id="234e1-167">Severity values</span></span>

![Affichage de rapport dans le rapport des règles de transport Exchange](../../media/transport-rule-report-report-view.png)

### <a name="details-table-view-for-the-exchange-transport-rule-report"></a><span data-ttu-id="234e1-169">Vue de la table Détails pour le rapport des règles de transport Exchange</span><span class="sxs-lookup"><span data-stu-id="234e1-169">Details table view for the Exchange transport rule report</span></span>

<span data-ttu-id="234e1-170">Si vous cliquez sur **afficher les détails table** , les informations affichées dépendent du graphique que vous examinez :</span><span class="sxs-lookup"><span data-stu-id="234e1-170">If you click **View details table** , the information that's shown depends on the chart you were looking at:</span></span>

- <span data-ttu-id="234e1-171">**Afficher les données par : règles de transport Exchange** :</span><span class="sxs-lookup"><span data-stu-id="234e1-171">**View data by: Exchange Transport rules** :</span></span>

  - <span data-ttu-id="234e1-172">**Date**</span><span class="sxs-lookup"><span data-stu-id="234e1-172">**Date**</span></span>
  - <span data-ttu-id="234e1-173">**Règle de transport**</span><span class="sxs-lookup"><span data-stu-id="234e1-173">**Transport rule**</span></span>
  - <span data-ttu-id="234e1-174">**Subject**</span><span class="sxs-lookup"><span data-stu-id="234e1-174">**Subject**</span></span>
  - <span data-ttu-id="234e1-175">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="234e1-175">**Sender address**</span></span>
  - <span data-ttu-id="234e1-176">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="234e1-176">**Recipient address**</span></span>
  - <span data-ttu-id="234e1-177">**Gravité**</span><span class="sxs-lookup"><span data-stu-id="234e1-177">**Severity**</span></span>
  - <span data-ttu-id="234e1-178">**Direction**</span><span class="sxs-lookup"><span data-stu-id="234e1-178">**Direction**</span></span>

- <span data-ttu-id="234e1-179">**Afficher les données par : DLP Exchange transport Rules** :</span><span class="sxs-lookup"><span data-stu-id="234e1-179">**View data by: DLP Exchange transport rules** :</span></span>

  - <span data-ttu-id="234e1-180">**Date**</span><span class="sxs-lookup"><span data-stu-id="234e1-180">**Date**</span></span>
  - <span data-ttu-id="234e1-181">**Stratégie DLP**</span><span class="sxs-lookup"><span data-stu-id="234e1-181">**DLP policy**</span></span>
  - <span data-ttu-id="234e1-182">**Règle de transport**</span><span class="sxs-lookup"><span data-stu-id="234e1-182">**Transport rule**</span></span>
  - <span data-ttu-id="234e1-183">**Subject**</span><span class="sxs-lookup"><span data-stu-id="234e1-183">**Subject**</span></span>
  - <span data-ttu-id="234e1-184">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="234e1-184">**Sender address**</span></span>
  - <span data-ttu-id="234e1-185">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="234e1-185">**Recipient address**</span></span>
  - <span data-ttu-id="234e1-186">**Gravité**</span><span class="sxs-lookup"><span data-stu-id="234e1-186">**Severity**</span></span>
  - <span data-ttu-id="234e1-187">**Direction**</span><span class="sxs-lookup"><span data-stu-id="234e1-187">**Direction**</span></span>

<span data-ttu-id="234e1-188">Si vous cliquez sur **filtres** dans un affichage tableau détaillé, vous pouvez modifier les résultats à l’aide des filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="234e1-188">If you click **Filters** in a details table view, you can modify the results with the following filters:</span></span>

- <span data-ttu-id="234e1-189">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="234e1-189">**Start date** and **End date**</span></span>
- <span data-ttu-id="234e1-190">Valeurs de la direction</span><span class="sxs-lookup"><span data-stu-id="234e1-190">Direction values</span></span>
- <span data-ttu-id="234e1-191">Valeurs de gravité</span><span class="sxs-lookup"><span data-stu-id="234e1-191">Severity values</span></span>

<span data-ttu-id="234e1-192">Pour revenir à l’affichage de rapport, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="234e1-192">To go back to the report view, click **View report**.</span></span>

## <a name="forwarding-report"></a><span data-ttu-id="234e1-193">Rapport de transfert</span><span class="sxs-lookup"><span data-stu-id="234e1-193">Forwarding report</span></span>

<span data-ttu-id="234e1-194">Le **rapport de transfert** indique que les messages envoyés par votre organisation sont transférés automatiquement vers des domaines externes à partir de boîtes aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="234e1-194">The **Forwarding report** shows your organization's automatically forwarded messages to external domains from Exchange Online mailboxes.</span></span> <span data-ttu-id="234e1-195">Les messages transférés peuvent présenter un risque de sécurité ou de conformité, et peuvent indiquer un compte compromis.</span><span class="sxs-lookup"><span data-stu-id="234e1-195">Forwarded messages can pose a security or compliance risk, and might indicate a compromised account.</span></span>

<span data-ttu-id="234e1-196">Pour afficher le rapport, ouvrez le [Centre de sécurité & conformité](https://protection.office.com), cliquez sur **rapports** de \> **tableau de bord** et sélectionnez rapport de **transfert**.</span><span class="sxs-lookup"><span data-stu-id="234e1-196">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Forwarding report**.</span></span> <span data-ttu-id="234e1-197">Pour accéder directement au rapport, ouvrez <https://protection.office.com/reportv2?id=MailFlowForwarding> .</span><span class="sxs-lookup"><span data-stu-id="234e1-197">To go directly to the report, open <https://protection.office.com/reportv2?id=MailFlowForwarding>.</span></span>

![Widget rapport de transfert dans le tableau de bord rapports](../../media/forwarding-report-widget.png)

### <a name="report-view-for-the-forwarding-report"></a><span data-ttu-id="234e1-199">Affichage de rapport pour le rapport de transfert</span><span class="sxs-lookup"><span data-stu-id="234e1-199">Report view for the Forwarding report</span></span>

<span data-ttu-id="234e1-200">Les graphiques suivants sont disponibles dans l’affichage rapport :</span><span class="sxs-lookup"><span data-stu-id="234e1-200">The following charts are available in the report view:</span></span>

- <span data-ttu-id="234e1-201">**Afficher les données pour : méthodes de transfert** : les méthodes suivantes sont affichées :</span><span class="sxs-lookup"><span data-stu-id="234e1-201">**Show data for: Forwarding methods** : The following methods are shown:</span></span>

  - <span data-ttu-id="234e1-202">**Règle de transport** : également appelée [règles de flux de messagerie](https://docs.microsoft.com/Exchange/security-and-compliance/mail-flow-rules/mail-flow-rules).</span><span class="sxs-lookup"><span data-stu-id="234e1-202">**Transport rule** : Also known as [mail flow rules](https://docs.microsoft.com/Exchange/security-and-compliance/mail-flow-rules/mail-flow-rules).</span></span>
  - <span data-ttu-id="234e1-203">**Règle de boîte aux lettres** : également appelée règles de boîte de [réception](https://support.microsoft.com/office/c24f5dea-9465-4df4-ad17-a50704d66c59).</span><span class="sxs-lookup"><span data-stu-id="234e1-203">**Mailbox rule** : Also known as [Inbox rules](https://support.microsoft.com/office/c24f5dea-9465-4df4-ad17-a50704d66c59).</span></span>

  ![Vue des méthodes de transfert dans le rapport de transfert](../../media/forwarding-report-forwarding-methods.png)

- <span data-ttu-id="234e1-205">**Afficher les données pour : transferts de domaines** : cette vue affiche les domaines de destinataire qui sont les destinations pour le transfert.</span><span class="sxs-lookup"><span data-stu-id="234e1-205">**Show data for: Forwarding domains** : This view shows the recipient domains that are the destinations for forwarding.</span></span>

  ![Vue des domaines de transfert dans le rapport de transfert](../../media/forwarding-report-forwarding-domains.png)

- <span data-ttu-id="234e1-207">**Afficher les données : redirecteurs** : les redirecteurs suivants sont affichés :</span><span class="sxs-lookup"><span data-stu-id="234e1-207">**Show data for: Forwarders** : The following forwarders are shown:</span></span>

  - <span data-ttu-id="234e1-208">**Règle de transport**</span><span class="sxs-lookup"><span data-stu-id="234e1-208">**Transport rule**</span></span>
  - <span data-ttu-id="234e1-209">Boîte aux lettres qui contient la règle de boîte de réception de transfert.</span><span class="sxs-lookup"><span data-stu-id="234e1-209">The mailbox that contains the forwarding Inbox rule.</span></span>

  ![Vue redirecteurs dans le rapport de transfert](../../media/forwarding-report-forwarders.png)

<span data-ttu-id="234e1-211">Si vous cliquez sur **filtres** dans un affichage de rapport, vous pouvez spécifier une plage de dates avec **Date de début** et date de **fin**.</span><span class="sxs-lookup"><span data-stu-id="234e1-211">If you click **Filters** in a report view, you can specify a date range with **Start date** and **End date**.</span></span>

### <a name="details-table-view-for-the-forwarding-report"></a><span data-ttu-id="234e1-212">Vue de la table Détails pour le rapport de transfert</span><span class="sxs-lookup"><span data-stu-id="234e1-212">Details table view for the Forwarding report</span></span>

<span data-ttu-id="234e1-213">Si vous cliquez sur **afficher la table des détails** dans un affichage de rapport, les informations suivantes s’affichent :</span><span class="sxs-lookup"><span data-stu-id="234e1-213">If you click **View details table** in a report view, the following information is shown:</span></span>

- <span data-ttu-id="234e1-214">**Redirecteurs** : la **règle de transport** value ou la boîte aux lettres qui contient la règle de boîte de réception de transfert.</span><span class="sxs-lookup"><span data-stu-id="234e1-214">**Forwarders** : The value **Transport rule** or the mailbox that contains the forwarding Inbox rule.</span></span>
- <span data-ttu-id="234e1-215">**Type de transfert** : règle de la **boîte aux lettres** ou **règle de transport**.</span><span class="sxs-lookup"><span data-stu-id="234e1-215">**Forwarding type** : The value **Mailbox rule** or **Transport rule**.</span></span>
- <span data-ttu-id="234e1-216">**Nom du destinataire**</span><span class="sxs-lookup"><span data-stu-id="234e1-216">**Recipient name**</span></span>
- <span data-ttu-id="234e1-217">**Domaine du destinataire**</span><span class="sxs-lookup"><span data-stu-id="234e1-217">**Recipient domain**</span></span>
- <span data-ttu-id="234e1-218">**Détails** : il s’agit de la valeur GUID de la règle de flux de messagerie ou de la valeur RuleIdentity de la règle de boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="234e1-218">**Details** : This is the GUID value of the mail flow rule, or the RuleIdentity value of the Inbox rule.</span></span>
- <span data-ttu-id="234e1-219">**Count**</span><span class="sxs-lookup"><span data-stu-id="234e1-219">**Count**</span></span>
- <span data-ttu-id="234e1-220">**Première date de transfert**</span><span class="sxs-lookup"><span data-stu-id="234e1-220">**First forward date**</span></span>

<span data-ttu-id="234e1-221">Si vous cliquez sur **filtres** dans un affichage tableau détaillé, vous pouvez spécifier une plage de dates avec **Date de début** et date de **fin**.</span><span class="sxs-lookup"><span data-stu-id="234e1-221">If you click **Filters** in a details table view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="234e1-222">Pour revenir à l’affichage rapports, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="234e1-222">To go back to the reports view, click **View report**.</span></span>

## <a name="mailflow-status-report"></a><span data-ttu-id="234e1-223">Rapport d’état de flux de flux</span><span class="sxs-lookup"><span data-stu-id="234e1-223">Mailflow status report</span></span>

<span data-ttu-id="234e1-224">Le **rapport d’état de flux** de messagerie est similaire au [rapport de courrier électronique envoyé et reçu](#sent-and-received-email-report), avec des informations supplémentaires sur le courrier électronique autorisé ou bloqué sur le serveur Edge.</span><span class="sxs-lookup"><span data-stu-id="234e1-224">The **Mailflow status report** is similar to the [Sent and received email report](#sent-and-received-email-report), with additional information about email allowed or blocked on the edge.</span></span> <span data-ttu-id="234e1-225">Il s’agit du seul rapport qui contient les informations de protection du serveur Edge et indique le nombre de messages bloqués avant d’être autorisés dans le service pour l’évaluation par Exchange Online Protection (EOP).</span><span class="sxs-lookup"><span data-stu-id="234e1-225">This is the only report that contains edge protection information, and shows just how much email is blocked before being allowed into the service for evaluation by Exchange Online Protection (EOP).</span></span> <span data-ttu-id="234e1-226">Il est important de comprendre que si un message est envoyé à cinq destinataires, nous le dénombrez cinq messages différents et pas un message.</span><span class="sxs-lookup"><span data-stu-id="234e1-226">It's important to understand that if a message is sent to five recipients we count it as five different messages and not one message.</span></span>
<span data-ttu-id="234e1-227">Pour afficher le rapport, ouvrez le [Centre de sécurité & conformité](https://protection.office.com), accédez **Reports** au \> **tableau de bord** rapports et sélectionnez rapport d’État du **flux de flux**.</span><span class="sxs-lookup"><span data-stu-id="234e1-227">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Mailflow status report**.</span></span> <span data-ttu-id="234e1-228">Pour accéder directement au **rapport d’État du flux de messagerie** , ouvrez <https://protection.office.com/mailflowStatusReport> .</span><span class="sxs-lookup"><span data-stu-id="234e1-228">To go directly to the **Mail flow status report** , open <https://protection.office.com/mailflowStatusReport>.</span></span>

![Widget rapport d’état de flux de notification dans le tableau de bord rapports](../../media/mail-flow-status-report-widget.png)

### <a name="type-view-for-the-mailflow-status-report"></a><span data-ttu-id="234e1-230">Vue type pour le rapport d’état de flux de flux</span><span class="sxs-lookup"><span data-stu-id="234e1-230">Type view for the Mailflow status report</span></span>

<span data-ttu-id="234e1-231">Lorsque vous ouvrez le rapport, l’onglet **type** est sélectionné par défaut.</span><span class="sxs-lookup"><span data-stu-id="234e1-231">When you open the report, the **Type** tab is selected by default.</span></span> <span data-ttu-id="234e1-232">Par défaut, cette vue contient un graphique et une table de données configurée avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="234e1-232">By default, this view contains a chart and a data table that's configured with the following filters:</span></span>

- <span data-ttu-id="234e1-233">**Date** : les 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="234e1-233">**Date** : The last 7 days.</span></span>
- <span data-ttu-id="234e1-234">**Sens** :</span><span class="sxs-lookup"><span data-stu-id="234e1-234">**Direction** :</span></span>

  - <span data-ttu-id="234e1-235">**Entrants**</span><span class="sxs-lookup"><span data-stu-id="234e1-235">**Inbound**</span></span>
  - <span data-ttu-id="234e1-236">**Sortant**</span><span class="sxs-lookup"><span data-stu-id="234e1-236">**Outbound**</span></span>
  - <span data-ttu-id="234e1-237">**Intra-org** : ce nombre est pour les messages au sein d’un client, c’est-à-dire</span><span class="sxs-lookup"><span data-stu-id="234e1-237">**Intra-org** : this count is for messages within a tenant i.e</span></span> <span data-ttu-id="234e1-238">l’expéditeur abc@domain.com envoie au destinataire xyz@domain.com (compté indépendamment des **ports entrants et** **sortants** )</span><span class="sxs-lookup"><span data-stu-id="234e1-238">sender abc@domain.com sends to recipient xyz@domain.com  (counted separately from **Inbound** and **Outbound** )</span></span>

- <span data-ttu-id="234e1-239">**Type** :</span><span class="sxs-lookup"><span data-stu-id="234e1-239">**Type** :</span></span>

  - <span data-ttu-id="234e1-240">**Courrier électronique approprié**</span><span class="sxs-lookup"><span data-stu-id="234e1-240">**Good mail**</span></span>
  - <span data-ttu-id="234e1-241">**Programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="234e1-241">**Malware**</span></span>
  - <span data-ttu-id="234e1-242">**Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="234e1-242">**Spam**</span></span>
  - <span data-ttu-id="234e1-243">**Protection des serveurs Edge**</span><span class="sxs-lookup"><span data-stu-id="234e1-243">**Edge protection**</span></span>
  - <span data-ttu-id="234e1-244">**Messages de règle**</span><span class="sxs-lookup"><span data-stu-id="234e1-244">**Rule messages**</span></span>
  - <span data-ttu-id="234e1-245">**Courriers hameçons**</span><span class="sxs-lookup"><span data-stu-id="234e1-245">**Phishing email**</span></span>

<span data-ttu-id="234e1-246">Le graphique est organisé selon les valeurs de **type** .</span><span class="sxs-lookup"><span data-stu-id="234e1-246">The chart is organized by the **Type** values.</span></span>

<span data-ttu-id="234e1-247">Vous pouvez modifier ces filtres en cliquant sur **Filtrer** ou en cliquant sur une valeur dans la légende du graphique.</span><span class="sxs-lookup"><span data-stu-id="234e1-247">You can change these filters by clicking **Filter** or by clicking a value in the chart legend.</span></span>

<span data-ttu-id="234e1-248">Le tableau de données contient les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="234e1-248">The data table contains the following information:</span></span>

- <span data-ttu-id="234e1-249">**Direction**</span><span class="sxs-lookup"><span data-stu-id="234e1-249">**Direction**</span></span>
- <span data-ttu-id="234e1-250">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="234e1-250">**Type**</span></span>
- <span data-ttu-id="234e1-251">**24 heures**</span><span class="sxs-lookup"><span data-stu-id="234e1-251">**24 hours**</span></span>
- <span data-ttu-id="234e1-252">**3 jours**</span><span class="sxs-lookup"><span data-stu-id="234e1-252">**3 days**</span></span>
- <span data-ttu-id="234e1-253">**7 jours**</span><span class="sxs-lookup"><span data-stu-id="234e1-253">**7 days**</span></span>
- <span data-ttu-id="234e1-254">**15 jours**</span><span class="sxs-lookup"><span data-stu-id="234e1-254">**15 days**</span></span>
- <span data-ttu-id="234e1-255">**30 jours**</span><span class="sxs-lookup"><span data-stu-id="234e1-255">**30 days**</span></span>

<span data-ttu-id="234e1-256">Si vous cliquez sur **choisir une catégorie pour plus d’informations** , vous pouvez sélectionner l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="234e1-256">If you click **Choose a category for more details** , you can select from the following values:</span></span>

- <span data-ttu-id="234e1-257">**Courrier électronique de hameçonnage** : cette sélection vous permet d’accéder au [rapport d’état de protection contre les menaces](view-email-security-reports.md#threat-protection-status-report).</span><span class="sxs-lookup"><span data-stu-id="234e1-257">**Phishing email** : This selection takes you to the [Threat protection status report](view-email-security-reports.md#threat-protection-status-report).</span></span>
- <span data-ttu-id="234e1-258">**Programme malveillant dans la messagerie** : cette sélection vous permet d’accéder au [rapport d’état de protection contre les menaces](view-email-security-reports.md#threat-protection-status-report).</span><span class="sxs-lookup"><span data-stu-id="234e1-258">**Malware in email** : This selection takes you to the [Threat protection status report](view-email-security-reports.md#threat-protection-status-report).</span></span>
- <span data-ttu-id="234e1-259">**Détections de courrier indésirable** : cette sélection vous permet d’accéder au [rapport des détections de courrier indésirable](view-email-security-reports.md#spam-detections-report).</span><span class="sxs-lookup"><span data-stu-id="234e1-259">**Spam detections** : This selection takes you to the [Spam Detections report](view-email-security-reports.md#spam-detections-report).</span></span>
- <span data-ttu-id="234e1-260">**Courrier indésirable bloqué** pour le serveur Edge : cette sélection vous permet d’accéder au [rapport des détections de courrier indésirable](view-email-security-reports.md#spam-detections-report).</span><span class="sxs-lookup"><span data-stu-id="234e1-260">**Edge blocked spam** : This selection takes you to the [Spam Detections report](view-email-security-reports.md#spam-detections-report).</span></span>

<span data-ttu-id="234e1-261">**Exportation** :</span><span class="sxs-lookup"><span data-stu-id="234e1-261">**Export** :</span></span>

<span data-ttu-id="234e1-262">Pour l’affichage détaillé, vous pouvez uniquement exporter des données pour un jour.</span><span class="sxs-lookup"><span data-stu-id="234e1-262">For the detail view, you can only export data for one day.</span></span> <span data-ttu-id="234e1-263">Par conséquent, si vous voulez exporter des données pendant 7 jours, vous devez effectuer 7 actions d’exportation différentes.</span><span class="sxs-lookup"><span data-stu-id="234e1-263">So, if you want to export data for 7 days, you need to do 7 different export actions.</span></span>

<span data-ttu-id="234e1-264">Chaque fichier. csv exporté est limité à 150 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="234e1-264">Each exported .csv file is limited to 150,000 rows.</span></span> <span data-ttu-id="234e1-265">Si les données de ce jour contiennent plus de 150 000 lignes, plusieurs fichiers. csv seront créés.</span><span class="sxs-lookup"><span data-stu-id="234e1-265">If the data for that day contains more than 150,000 rows, then multiple .csv files will be created.</span></span>

![<span data-ttu-id="234e1-266">Tapez View dans le rapport d’état de flux de flux</span><span class="sxs-lookup"><span data-stu-id="234e1-266">Type view in the Mailflow status report</span></span> ](../../media/mail-flow-status-report-type-view.png)

### <a name="direction-view-for-the-mailflow-status-report"></a><span data-ttu-id="234e1-267">Vue de direction pour le rapport d’état de flux de flux</span><span class="sxs-lookup"><span data-stu-id="234e1-267">Direction view for the Mailflow status report</span></span>

<span data-ttu-id="234e1-268">Si vous cliquez sur l’onglet **direction** , les mêmes filtres par défaut de la vue **type** sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="234e1-268">If you click the **Direction** tab, the same default filters from the **Type** view are used.</span></span>

<span data-ttu-id="234e1-269">Le graphique est organisé par les valeurs de **direction** .</span><span class="sxs-lookup"><span data-stu-id="234e1-269">The chart is organized by **Direction** values.</span></span>

<span data-ttu-id="234e1-270">Vous pouvez modifier ces filtres en cliquant sur **Filtrer** ou en cliquant sur une valeur dans la légende du graphique.</span><span class="sxs-lookup"><span data-stu-id="234e1-270">You can change these filters by clicking **Filter** or by clicking a value in the chart legend.</span></span> <span data-ttu-id="234e1-271">Les mêmes filtres de la vue **type** sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="234e1-271">The same filters from the **Type** view are used.</span></span>

<span data-ttu-id="234e1-272">La table de données contient les mêmes informations à partir de la vue **type** .</span><span class="sxs-lookup"><span data-stu-id="234e1-272">The data table contains same information from the **Type** view.</span></span>

<span data-ttu-id="234e1-273">La **catégorie choisir une catégorie pour plus de détails** disponibles et les sélections possibles est identique à la vue **type** .</span><span class="sxs-lookup"><span data-stu-id="234e1-273">The **Choose a category for more details** available selections and behavior are the same as the **Type** view.</span></span>

<span data-ttu-id="234e1-274">**Exportation** :</span><span class="sxs-lookup"><span data-stu-id="234e1-274">**Export** :</span></span>

<span data-ttu-id="234e1-275">Pour l’affichage détaillé, vous pouvez uniquement exporter des données pour un jour.</span><span class="sxs-lookup"><span data-stu-id="234e1-275">For the detail view, you can only export data for one day.</span></span> <span data-ttu-id="234e1-276">Par conséquent, si vous voulez exporter des données pendant 7 jours, vous devez effectuer 7 actions d’exportation différentes.</span><span class="sxs-lookup"><span data-stu-id="234e1-276">So, if you want to export data for 7 days, you need to do 7 different export actions.</span></span>

<span data-ttu-id="234e1-277">Chaque fichier. csv exporté est limité à 150 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="234e1-277">Each exported .csv file is limited to 150,000 rows.</span></span> <span data-ttu-id="234e1-278">Si les données de ce jour contiennent plus de 150 000 lignes, plusieurs fichiers. csv seront créés.</span><span class="sxs-lookup"><span data-stu-id="234e1-278">If the data for that day contains more than 150,000 rows, then multiple .csv files will be created.</span></span>

![<span data-ttu-id="234e1-279">Affichage de la direction dans le rapport d’état de flux de flux</span><span class="sxs-lookup"><span data-stu-id="234e1-279">Direction view in the Mailflow status report</span></span> ](../../media/mail-flow-status-report-direction-view.png)

### <a name="funnel-view-for-the-mailflow-status-report"></a><span data-ttu-id="234e1-280">Vue entonnoir pour le rapport d’état de flux de flux</span><span class="sxs-lookup"><span data-stu-id="234e1-280">Funnel view for the Mailflow status report</span></span>

<span data-ttu-id="234e1-281">L’affichage **entonnoir** vous montre comment les fonctionnalités de protection contre les menaces Microsoft filtrent le courrier électronique entrant et sortant dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="234e1-281">The **Funnel** view shows you how Microsoft's email threat protection features filter incoming and outgoing email in your organization.</span></span> <span data-ttu-id="234e1-282">Elle fournit des détails sur le nombre total de messages électroniques, ainsi que la façon dont les fonctionnalités de protection contre les menaces configurées, notamment la protection des serveurs Edge, les logiciels anti-programme malveillant, le hameçonnage, le blocage du courrier indésirable et la détection d’usurpation d’identité ont un impact sur ce nombre.</span><span class="sxs-lookup"><span data-stu-id="234e1-282">It provides details on the total email count, and how the configured threat protection features, including edge protection, anti-malware, anti-phishing, anti-spam, and anti-spoofing affect this count.</span></span>

<span data-ttu-id="234e1-283">Si vous cliquez sur l’onglet **entonnoir** , par défaut, cet affichage contient un graphique et une table de données configurée avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="234e1-283">If you click the **Funnel** tab, by default, this view contains a chart and a data table that's configured with the following filters:</span></span>

- <span data-ttu-id="234e1-284">**Date** : les 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="234e1-284">**Date** : The last 7 days.</span></span>

- <span data-ttu-id="234e1-285">**Sens** :</span><span class="sxs-lookup"><span data-stu-id="234e1-285">**Direction** :</span></span>

  - <span data-ttu-id="234e1-286">**Entrants**</span><span class="sxs-lookup"><span data-stu-id="234e1-286">**Inbound**</span></span>
  - <span data-ttu-id="234e1-287">**Sortant**</span><span class="sxs-lookup"><span data-stu-id="234e1-287">**Outbound**</span></span>
  - <span data-ttu-id="234e1-288">**Intra-org** : ce nombre est pour les messages envoyés au sein d’un client ; par exemple, l’expéditeur abc@domain.com envoie au destinataire xyz@domain.com (compté indépendamment des messages entrants et sortants).</span><span class="sxs-lookup"><span data-stu-id="234e1-288">**Intra-org** : This count is for messages sent within a tenant; i.e, sender abc@domain.com sends to recipient xyz@domain.com (counted separately from Inbound and Outbound).</span></span>

<span data-ttu-id="234e1-289">L’affichage d’agrégation et le tableau de données autorisent 90 jours de filtrage.</span><span class="sxs-lookup"><span data-stu-id="234e1-289">The aggregate view and data table view allow for 90 days of filtering.</span></span>

<span data-ttu-id="234e1-290">Si vous cliquez sur **filtre** , vous pouvez filtrer le graphique et la table de données.</span><span class="sxs-lookup"><span data-stu-id="234e1-290">If you click **Filter** , you can filter both the chart and the data table.</span></span>

<span data-ttu-id="234e1-291">Ce graphique indique le nombre de messages organisés par :</span><span class="sxs-lookup"><span data-stu-id="234e1-291">This chart shows the email count organized by:</span></span>

- <span data-ttu-id="234e1-292">**Nombre total de messages électroniques**</span><span class="sxs-lookup"><span data-stu-id="234e1-292">**Total email**</span></span>
- <span data-ttu-id="234e1-293">**Courrier électronique après la protection du serveur Edge**</span><span class="sxs-lookup"><span data-stu-id="234e1-293">**Email after edge protection**</span></span>
- <span data-ttu-id="234e1-294">**Courrier électronique après anti-programme malveillant, réputation de fichier, bloc de type fichier**</span><span class="sxs-lookup"><span data-stu-id="234e1-294">**Email after anti-malware, file reputation, file type block**</span></span>
- <span data-ttu-id="234e1-295">**Courrier électronique après hameçonnage, réputation de l’URL, emprunt d’identité de marque, anti-usurpation**</span><span class="sxs-lookup"><span data-stu-id="234e1-295">**Email after anti-phish, URL reputation, brand impersonation, anti-spoof**</span></span>
- <span data-ttu-id="234e1-296">**Courrier électronique après blocage du courrier indésirable et filtrage du courrier en nombre**</span><span class="sxs-lookup"><span data-stu-id="234e1-296">**Email after anti-spam, bulk mail filtering**</span></span>
- <span data-ttu-id="234e1-297">**Courrier électronique après l’emprunt d’identité d’utilisateur et de domaine**<sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="234e1-297">**Email after user and domain impersonation**<sup>1</sup></span></span>
- <span data-ttu-id="234e1-298">**Courrier électronique après la détonation 1 du fichier et de l’URL**<sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="234e1-298">**Email after file and URL detonation**<sup>1</sup></span></span>
- <span data-ttu-id="234e1-299">**Courrier électronique détecté comme étant Bénin après une protection post-remise (URL-clic sur la protection du temps de clic)**</span><span class="sxs-lookup"><span data-stu-id="234e1-299">**Email detected as benign after post-delivery protection (URL click time protection)**</span></span>

<span data-ttu-id="234e1-300"><sup>1</sup> Defender pour Office 365 uniquement</span><span class="sxs-lookup"><span data-stu-id="234e1-300"><sup>1</sup> Defender for Office 365 only</span></span>

<span data-ttu-id="234e1-301">Pour afficher le courrier électronique filtré par EOP ou Defender pour Office 365 séparément, cliquez sur la valeur dans la légende du graphique.</span><span class="sxs-lookup"><span data-stu-id="234e1-301">To view the email filtered by EOP or Defender for Office 365 separately, click on the value in the chart legend.</span></span>

<span data-ttu-id="234e1-302">La table de données contient les informations suivantes, indiquées dans l’ordre décroissant de date :</span><span class="sxs-lookup"><span data-stu-id="234e1-302">The data table contains the following information, shown in descending date order:</span></span>

- <span data-ttu-id="234e1-303">**Date**</span><span class="sxs-lookup"><span data-stu-id="234e1-303">**Date**</span></span>
- <span data-ttu-id="234e1-304">**Nombre total de messages électroniques**</span><span class="sxs-lookup"><span data-stu-id="234e1-304">**Total email**</span></span>
- <span data-ttu-id="234e1-305">**Protection des serveurs Edge**</span><span class="sxs-lookup"><span data-stu-id="234e1-305">**Edge protection**</span></span> 
- <span data-ttu-id="234e1-306">**Anti-programme malveillant, réputation de fichier, bloc de type de fichier** :</span><span class="sxs-lookup"><span data-stu-id="234e1-306">**Anti-malware, file reputation, file type block** :</span></span>
  - <span data-ttu-id="234e1-307">**Réputation de fichier** : messages filtrés en raison de l’identification d’un fichier joint par d’autres clients Microsoft.</span><span class="sxs-lookup"><span data-stu-id="234e1-307">**File reputation** : Messages filtered due to identification of an attached file by other Microsoft customers.</span></span>
  - <span data-ttu-id="234e1-308">**Bloc de type de fichier** : messages filtrés en raison du type de fichier malveillant identifié dans le message.</span><span class="sxs-lookup"><span data-stu-id="234e1-308">**File type block** : Messages filtered due to the type of malicious file identified in the message.</span></span>      
- <span data-ttu-id="234e1-309">**Hameçonnage, réputation de l’URL, emprunt d’identité de marque, anti-usurpation** :</span><span class="sxs-lookup"><span data-stu-id="234e1-309">**Anti-phish, URL reputation, Brand impersonation, anti-spoof** :</span></span>
  - <span data-ttu-id="234e1-310">**Réputation** de l’URL : messages filtrés en raison de l’identification de l’URL par d’autres clients Microsoft.</span><span class="sxs-lookup"><span data-stu-id="234e1-310">**URL reputation** : Messages filtered due to the identification of the URL by other Microsoft customers.</span></span>
  - <span data-ttu-id="234e1-311">Emprunt d’identité de la **marque** : messages filtrés en raison du message provenant de marques connues empruntant des expéditeurs.</span><span class="sxs-lookup"><span data-stu-id="234e1-311">**Brand impersonation** : Messages filtered due to the message coming from well-known brand impersonating senders.</span></span>
  - <span data-ttu-id="234e1-312">**Anti-usurpation** : messages filtrés en raison du message tentant d’usurper un domaine auquel appartient le destinataire, ou domaine dont l’expéditeur du message n’est pas propriétaire.</span><span class="sxs-lookup"><span data-stu-id="234e1-312">**Anti-spoof** : Messages filtered due to the message attempting to spoof a domain that the recipient belongs to, or a domain that the message sender doesn't own.</span></span>  
- <span data-ttu-id="234e1-313">**Blocage du courrier indésirable et filtrage du courrier en nombre** :</span><span class="sxs-lookup"><span data-stu-id="234e1-313">**Anti-spam, bulk mail filtering** :</span></span>
  - <span data-ttu-id="234e1-314">**Filtrage du courrier en nombre** : messages filtrés en raison d’une tentative de remise en nombre de messages à ses destinataires.</span><span class="sxs-lookup"><span data-stu-id="234e1-314">**Bulk mail filtering** : Messages filtered due to an attempt to deliver bulk mail to its recipients.</span></span> 
- <span data-ttu-id="234e1-315">**Emprunt d’identité d’utilisateur et de domaine (Defender pour Office 365)** :</span><span class="sxs-lookup"><span data-stu-id="234e1-315">**User and domain impersonation (Defender for Office 365)** :</span></span>
  - <span data-ttu-id="234e1-316">**Emprunt d’identité** de l’utilisateur : messages filtrés en raison d’une tentative d’emprunt d’identité d’un utilisateur (expéditeur du message) défini dans les paramètres de protection contre l’emprunt d’identité d’une stratégie anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="234e1-316">**User impersonation** : Messages filtered due to an attempt to impersonate a user (message sender) that's defined in the impersonation protection settings of an anti-phishing policy.</span></span>
  - <span data-ttu-id="234e1-317">**Emprunt** d’identité de domaine : messages filtrés en raison d’une tentative d’emprunt d’identité d’un domaine défini dans les paramètres de protection contre l’emprunt d’identité d’une stratégie anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="234e1-317">**Domain impersonation** : Messages filtered due to an attempt to impersonate a domain that's defined in the impersonation protection settings of an anti-phishing policy.</span></span> 
- <span data-ttu-id="234e1-318">**Détonation des fichiers et des URL (Defender pour Office 365)** :</span><span class="sxs-lookup"><span data-stu-id="234e1-318">**File and URL detonation (Defender for Office 365)** :</span></span>
  - <span data-ttu-id="234e1-319">**Détonation du fichier** : messages filtrés par une stratégie de pièces jointes fiables.</span><span class="sxs-lookup"><span data-stu-id="234e1-319">**File detonation** : Messages filtered by a Safe Attachments policy.</span></span>
  - <span data-ttu-id="234e1-320">**Détonation d’URL** : message filtré par une stratégie de liens fiables.</span><span class="sxs-lookup"><span data-stu-id="234e1-320">**URL detonation** : Message filtered by a Safe Links policy.</span></span>  
- <span data-ttu-id="234e1-321">**Post-livraison protection et zap (ATP), ou zap (EoP)** : zap indique zéro vidage automatique.</span><span class="sxs-lookup"><span data-stu-id="234e1-321">**Post-delivery protection and ZAP (ATP), or ZAP (EOP)** : ZAP indicates zero hour auto-purge.</span></span>

<span data-ttu-id="234e1-322">Si vous sélectionnez une ligne dans le tableau de données, une autre répartition du nombre de messages est affichée dans le menu volant.</span><span class="sxs-lookup"><span data-stu-id="234e1-322">If you select a row in the data table, a further breakdown of the email counts are shown in the flyout.</span></span>

<span data-ttu-id="234e1-323">**Exportation** :</span><span class="sxs-lookup"><span data-stu-id="234e1-323">**Export** :</span></span>

<span data-ttu-id="234e1-324">Après avoir cliqué sur **Exporter** sous **options** , vous pouvez sélectionner l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="234e1-324">After you click **Export** under **Options** , you can select one of the following values:</span></span>

- <span data-ttu-id="234e1-325">**Résumé (avec les données au plus des 90 derniers jours)**</span><span class="sxs-lookup"><span data-stu-id="234e1-325">**Summary (with data for last 90 days at most)**</span></span>
- <span data-ttu-id="234e1-326">**Détails (avec les données des 30 derniers jours)**</span><span class="sxs-lookup"><span data-stu-id="234e1-326">**Details (with data for last 30 days at most)**</span></span>

<span data-ttu-id="234e1-327">Sous **Date** , choisissez une plage, puis cliquez sur **appliquer**.</span><span class="sxs-lookup"><span data-stu-id="234e1-327">Under **Date** , choose a range, and then click **Apply**.</span></span> <span data-ttu-id="234e1-328">Les données des filtres actuels seront exportées dans un fichier. csv.</span><span class="sxs-lookup"><span data-stu-id="234e1-328">Data for the current filters will be exported to a .csv file.</span></span>

<span data-ttu-id="234e1-329">Chaque fichier. csv exporté est limité à 150 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="234e1-329">Each exported .csv file is limited to 150,000 rows.</span></span> <span data-ttu-id="234e1-330">Si les données contiennent plus de 150 000 lignes, plusieurs fichiers. csv seront créés.</span><span class="sxs-lookup"><span data-stu-id="234e1-330">If the data contains more than 150,000 rows, then multiple .csv files will be created.</span></span>

 ![<span data-ttu-id="234e1-331">Vue entonnoir dans le rapport d’état de flux de flux</span><span class="sxs-lookup"><span data-stu-id="234e1-331">Funnel view in the Mailflow status report</span></span> ](../../media/mail-flow-status-report-funnel-view.png)

### <a name="tech-view-for-the-mailflow-status-report"></a><span data-ttu-id="234e1-332">Vue technique pour le rapport d’état de flux de flux</span><span class="sxs-lookup"><span data-stu-id="234e1-332">Tech view for the Mailflow status report</span></span>

<span data-ttu-id="234e1-333">La **vue Tech** est similaire à l’affichage **entonnoir** , qui fournit des détails plus granulaires pour les fonctionnalités de protection contre les menaces configurées.</span><span class="sxs-lookup"><span data-stu-id="234e1-333">The **Tech view** is similar to the **Funnel** view, providing more granular details for the configured threat protections features.</span></span> <span data-ttu-id="234e1-334">À partir du graphique, vous pouvez voir comment les messages sont catégorisés aux différentes étapes de la protection contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="234e1-334">From the chart, you can see how messages are categorized at the different stages of threat protection.</span></span>

<span data-ttu-id="234e1-335">Si vous cliquez sur l’onglet **affichage Tech** , par défaut, cet affichage contient un graphique et une table de données configurée avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="234e1-335">If you click the **Tech view** tab, by default, this view contains a chart and a data table that's configured with the following filters:</span></span>

- <span data-ttu-id="234e1-336">**Date** : les 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="234e1-336">**Date** : The last 7 days.</span></span>

- <span data-ttu-id="234e1-337">**Sens** :</span><span class="sxs-lookup"><span data-stu-id="234e1-337">**Direction** :</span></span>

  - <span data-ttu-id="234e1-338">**Entrants**</span><span class="sxs-lookup"><span data-stu-id="234e1-338">**Inbound**</span></span>
  - <span data-ttu-id="234e1-339">**Sortant**</span><span class="sxs-lookup"><span data-stu-id="234e1-339">**Outbound**</span></span>
  - <span data-ttu-id="234e1-340">**Intra-org** : ce nombre est pour les messages au sein d’un client, c’est-à-dire</span><span class="sxs-lookup"><span data-stu-id="234e1-340">**Intra-org** : this count is for messages within a tenant i.e</span></span> <span data-ttu-id="234e1-341">l’expéditeur abc@domain.com envoie au destinataire xyz@domain.com (compté indépendamment des ports entrants et sortants)</span><span class="sxs-lookup"><span data-stu-id="234e1-341">sender abc@domain.com sends to recipient xyz@domain.com (counted separately from Inbound and Outbound)</span></span>

<span data-ttu-id="234e1-342">L’affichage d’agrégation et le tableau de données autorisent 90 jours de filtrage.</span><span class="sxs-lookup"><span data-stu-id="234e1-342">The aggregate view and data table view allow for 90 days of filtering.</span></span>

<span data-ttu-id="234e1-343">Si vous cliquez sur **filtre** , vous pouvez filtrer le graphique et la table de données.</span><span class="sxs-lookup"><span data-stu-id="234e1-343">If you click **Filter** , you can filter both the chart and the data table.</span></span>

<span data-ttu-id="234e1-344">Ce graphique présente les messages organisés selon les catégories suivantes :</span><span class="sxs-lookup"><span data-stu-id="234e1-344">This chart shows messages organized into the following categories:</span></span>

- <span data-ttu-id="234e1-345">**Nombre total de messages électroniques**</span><span class="sxs-lookup"><span data-stu-id="234e1-345">**Total email**</span></span>
- <span data-ttu-id="234e1-346">**Serveur Edge autorisé, serveur Edge filtré**</span><span class="sxs-lookup"><span data-stu-id="234e1-346">**Edge allow, edge filtered**</span></span>
- <span data-ttu-id="234e1-347">**Pas de programmes malveillants, détection de pièces jointes fiables (Defender pour Office 365), détection de moteur anti-programme malveillant, bloc de règles**</span><span class="sxs-lookup"><span data-stu-id="234e1-347">**Not malware, Safe attachments detection (Defender for Office 365), Anti-malware engine detection, rule block**</span></span>
- <span data-ttu-id="234e1-348">**Non-hameçonnage, échec DMARC, détection d’usurpation d’identité, détection d’usurpation d’identité, détection de hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="234e1-348">**Not phish, DMARC failure, impersonation detection, spoof detection, phish detection**</span></span>
- <span data-ttu-id="234e1-349">**Aucune détection avec détonation d’URL, détection de détonation d’URL (Defender pour Office 365)**</span><span class="sxs-lookup"><span data-stu-id="234e1-349">**No detection with URL detonation, URL detonation detection (Defender for Office 365)**</span></span>
- <span data-ttu-id="234e1-350">**Courrier indésirable, courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="234e1-350">**Not spam, spam**</span></span>
- <span data-ttu-id="234e1-351">**Courrier électronique non malveillant, détection de liens fiables (Defender pour Office 365), ZAP**</span><span class="sxs-lookup"><span data-stu-id="234e1-351">**Non-malicious email, Safe Links detection (Defender for Office 365), ZAP**</span></span>

<span data-ttu-id="234e1-352">Lorsque vous placez le curseur de la souris sur une catégorie dans le graphique, vous pouvez voir le nombre de messages dans cette catégorie.</span><span class="sxs-lookup"><span data-stu-id="234e1-352">When you hover over a category in the chart, you can see the number of messages in that category.</span></span>

<span data-ttu-id="234e1-353">La table de données contient les informations suivantes, indiquées dans l’ordre décroissant de date :</span><span class="sxs-lookup"><span data-stu-id="234e1-353">The data table contains the following information, shown in descending date order:</span></span>

- <span data-ttu-id="234e1-354">**Date**</span><span class="sxs-lookup"><span data-stu-id="234e1-354">**Date**</span></span>
- <span data-ttu-id="234e1-355">**Nombre total de messages électroniques**</span><span class="sxs-lookup"><span data-stu-id="234e1-355">**Total email**</span></span>
- <span data-ttu-id="234e1-356">**Serveur Edge filtré**</span><span class="sxs-lookup"><span data-stu-id="234e1-356">**Edge filtered**</span></span>
- <span data-ttu-id="234e1-357">**Moteur anti-programme malveillant, pièces jointes fiables, règle filtrée** :</span><span class="sxs-lookup"><span data-stu-id="234e1-357">**Anti-malware engine, safe attachments, rule filtered** :</span></span>
  - <span data-ttu-id="234e1-358">**Règle filtrée** : messages filtrés en raison de règles de flux de messagerie (également appelées règles de transport).</span><span class="sxs-lookup"><span data-stu-id="234e1-358">**Rule filtered** : Messages filtered due to  mail flow rules (also known as transport rules).</span></span>
- <span data-ttu-id="234e1-359">**DMARC, emprunt d’identité, usurpation, hameçonnage filtré** :</span><span class="sxs-lookup"><span data-stu-id="234e1-359">**DMARC, impersonation, spoof, phish filtered** :</span></span>
  - <span data-ttu-id="234e1-360">**DMARC** : messages filtrés en raison d’un échec de la vérification de l’authentification DMARC du message.</span><span class="sxs-lookup"><span data-stu-id="234e1-360">**DMARC** : Messages filtered due to the message failing its DMARC authentication check.</span></span> 
- <span data-ttu-id="234e1-361">**Détection de la détonation d’URL**</span><span class="sxs-lookup"><span data-stu-id="234e1-361">**URL detonation detection**</span></span>
- <span data-ttu-id="234e1-362">**Filtrage du courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="234e1-362">**Anti-spam filtered**</span></span>
- <span data-ttu-id="234e1-363">**ZAP supprimé**</span><span class="sxs-lookup"><span data-stu-id="234e1-363">**ZAP removed**</span></span>
- <span data-ttu-id="234e1-364">**Détection par les liens fiables**</span><span class="sxs-lookup"><span data-stu-id="234e1-364">**Detection by safe links**</span></span>

<span data-ttu-id="234e1-365">Si vous sélectionnez une ligne dans le tableau de données, une autre répartition du nombre de messages est affichée dans le menu volant.</span><span class="sxs-lookup"><span data-stu-id="234e1-365">If you select a row in the data table, a further breakdown of the email counts are shown in the flyout.</span></span>

<span data-ttu-id="234e1-366">**Exportation** :</span><span class="sxs-lookup"><span data-stu-id="234e1-366">**Export** :</span></span>

<span data-ttu-id="234e1-367">Lorsque vous cliquez sur **Exporter** , sous **options** , vous pouvez sélectionner l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="234e1-367">On clicking **Export** , under **Options** you can select one of the following values:</span></span>

- <span data-ttu-id="234e1-368">**Résumé (avec les données au plus des 90 derniers jours)**</span><span class="sxs-lookup"><span data-stu-id="234e1-368">**Summary (with data for last 90 days at most)**</span></span>
- <span data-ttu-id="234e1-369">**Détails (avec les données des 30 derniers jours)**</span><span class="sxs-lookup"><span data-stu-id="234e1-369">**Details (with data for last 30 days at most)**</span></span>

<span data-ttu-id="234e1-370">Sous **Date** , choisissez une plage, puis cliquez sur **appliquer**.</span><span class="sxs-lookup"><span data-stu-id="234e1-370">Under **Date** , choose a range, and then click **Apply**.</span></span> <span data-ttu-id="234e1-371">Les données des filtres actuels seront exportées dans un fichier. csv.</span><span class="sxs-lookup"><span data-stu-id="234e1-371">Data for the current filters will be exported to a .csv file.</span></span>

<span data-ttu-id="234e1-372">Chaque fichier. csv exporté est limité à 150 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="234e1-372">Each exported .csv file is limited to 150,000 rows.</span></span> <span data-ttu-id="234e1-373">Si les données contiennent plus de 150 000 lignes, plusieurs fichiers. csv seront créés.</span><span class="sxs-lookup"><span data-stu-id="234e1-373">If the data contains more than 150,000 rows, then multiple .csv files will be created.</span></span>

 ![<span data-ttu-id="234e1-374">Vue technique dans le rapport d’état de flux de flux</span><span class="sxs-lookup"><span data-stu-id="234e1-374">Tech view in the Mailflow status report</span></span> ](../../media/mail-flow-status-report-Tech-view.png)

## <a name="sent-and-received-email-report"></a><span data-ttu-id="234e1-375">Rapport de courrier électronique envoyé et reçu</span><span class="sxs-lookup"><span data-stu-id="234e1-375">Sent and received email report</span></span>

<span data-ttu-id="234e1-376">Le rapport de **courrier électronique envoyé et reçu** est un rapport intelligent qui affiche des informations sur les messages entrants et sortants, notamment les détections de courrier indésirable, les programmes malveillants et la messagerie électronique identifiés comme étant « en qualité ».</span><span class="sxs-lookup"><span data-stu-id="234e1-376">The **Sent and received email** report is a smart report that shows information about incoming and outgoing email, including spam detections, malware, and email identified as "good."</span></span> <span data-ttu-id="234e1-377">La différence entre ce rapport et le [rapport d’état de flux](#mailflow-status-report) de courrier est la suivante : ce rapport n’inclut pas de données sur les messages bloqués par la protection du serveur Edge. Il est important de comprendre que si un message est envoyé à cinq destinataires, il est considéré comme un seul message.</span><span class="sxs-lookup"><span data-stu-id="234e1-377">The difference between this report and the [Mailflow status report](#mailflow-status-report) is: this report doesn't include data about messages blocked by edge protection.It's important to understand that if a message is sent to five recipients we count it as one message.</span></span>

<span data-ttu-id="234e1-378">L’affichage Aggregate et l’affichage détaillé du rapport autorisent 90 jours de filtrage.</span><span class="sxs-lookup"><span data-stu-id="234e1-378">The aggregate view and the detail view of the report allow for 90 days of filtering.</span></span>

<span data-ttu-id="234e1-379">Pour afficher le rapport, ouvrez le [Centre de sécurité & conformité](https://protection.office.com), accédez **Reports** au \> **tableau de bord** rapports et sélectionnez **Envoyer et recevoir un message**.</span><span class="sxs-lookup"><span data-stu-id="234e1-379">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Sent and received email**.</span></span> <span data-ttu-id="234e1-380">Pour accéder directement au rapport, ouvrez <https://protection.office.com/reportv2?id=SentAndReceivedMailATP> .</span><span class="sxs-lookup"><span data-stu-id="234e1-380">To go directly to the report, open <https://protection.office.com/reportv2?id=SentAndReceivedMailATP>.</span></span>

![Widget courrier électronique envoyé et reçu dans le tableau de bord rapports](../../media/sent-and-received-email-report-widget.png)

### <a name="report-view-for-the-sent-and-received-email-report"></a><span data-ttu-id="234e1-382">Affichage de rapport pour le rapport de courrier électronique envoyé et reçu</span><span class="sxs-lookup"><span data-stu-id="234e1-382">Report view for the Sent and received email report</span></span>

<span data-ttu-id="234e1-383">Les graphiques suivants sont disponibles dans l’affichage rapport :</span><span class="sxs-lookup"><span data-stu-id="234e1-383">The following charts are available in the report view:</span></span>

- <span data-ttu-id="234e1-384">**Décomposer en : type** : le graphique affiche toutes les catégories disponibles :</span><span class="sxs-lookup"><span data-stu-id="234e1-384">**Break down by: Type** : The chart shows all available categories:</span></span>

  - <span data-ttu-id="234e1-385">**Total**</span><span class="sxs-lookup"><span data-stu-id="234e1-385">**Total**</span></span>
  - <span data-ttu-id="234e1-386">**Courrier électronique approprié**</span><span class="sxs-lookup"><span data-stu-id="234e1-386">**Good mail**</span></span>
  - <span data-ttu-id="234e1-387">**Programme malveillant (blocage des programmes malveillants)** (EoP)</span><span class="sxs-lookup"><span data-stu-id="234e1-387">**Malware (anti-malware)** (EOP)</span></span>
  - <span data-ttu-id="234e1-388">**Détections de courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="234e1-388">**Spam detections**</span></span>
  - <span data-ttu-id="234e1-389">**Messages de règle**</span><span class="sxs-lookup"><span data-stu-id="234e1-389">**Rule messages**</span></span>
  - <span data-ttu-id="234e1-390">**Programme malveillant avancé** (Microsoft Defender pour Office 365)</span><span class="sxs-lookup"><span data-stu-id="234e1-390">**Advanced malware** (Microsoft Defender for Office 365)</span></span>

  <span data-ttu-id="234e1-391">Lorsque vous placez le curseur de la souris sur un jour (point de données) dans le graphique, vous pouvez afficher les détails de ce jour.</span><span class="sxs-lookup"><span data-stu-id="234e1-391">When you hover over a day (data point) in the chart, you can see details for that day.</span></span>

  ![Type de vue dans le rapport des courriers électroniques envoyés et reçus](../../media/sent-and-received-email-report-type-view.png)

- <span data-ttu-id="234e1-393">**Décomposer en : sens** : le graphique indique le **total** , les données **entrantes** et **sortantes** .</span><span class="sxs-lookup"><span data-stu-id="234e1-393">**Break down by: Direction** : The chart shows **Total** , **Inbound** , and **Outbound** data.</span></span> <span data-ttu-id="234e1-394">Lorsque vous placez le curseur de la souris sur un jour (point de données) dans le graphique, vous pouvez afficher les détails de ce jour.</span><span class="sxs-lookup"><span data-stu-id="234e1-394">When you hover over a day (data point) in the chart, you can see details for that day.</span></span>

  ![Affichage de la direction dans le rapport de courrier électronique envoyé et reçu](../../media/sent-and-received-email-report-direction-view.png)

- <span data-ttu-id="234e1-396">**Explorer en détail** \> **Programme malveillant (anti-programme malveillant)** : cette sélection vous permet d’accéder aux [détections de programmes malveillants dans le rapport par courrier électronique](view-email-security-reports.md#malware-detections-in-email-report).</span><span class="sxs-lookup"><span data-stu-id="234e1-396">**Drill down by** \> **Malware (anti-malware)** : This selection takes you to the [Malware detections in email report](view-email-security-reports.md#malware-detections-in-email-report).</span></span>

- <span data-ttu-id="234e1-397">**Explorer en détail** \> **Détections de courrier indésirable)** : cette sélection vous permet d’accéder au [rapport des détections de courrier indésirable](view-email-security-reports.md#spam-detections-report).</span><span class="sxs-lookup"><span data-stu-id="234e1-397">**Drill down by** \> **Spam detections)** : This selection takes you to the [Spam Detections report](view-email-security-reports.md#spam-detections-report).</span></span>

<span data-ttu-id="234e1-398">Si vous cliquez sur **filtres** dans un affichage de rapport, vous pouvez modifier les résultats à l’aide des filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="234e1-398">If you click **Filters** in a report view, you can modify the results with the following filters:</span></span>

- <span data-ttu-id="234e1-399">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="234e1-399">**Start date** and **End date**</span></span>
- <span data-ttu-id="234e1-400">Valeurs de la direction</span><span class="sxs-lookup"><span data-stu-id="234e1-400">Direction values</span></span>
- <span data-ttu-id="234e1-401">Valeurs de type</span><span class="sxs-lookup"><span data-stu-id="234e1-401">Type values</span></span>

<span data-ttu-id="234e1-402">Pour revenir à l’affichage de rapport, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="234e1-402">To go back to the report view, click **View report**.</span></span>

### <a name="details-table-view-for-the-sent-and-received-email-report"></a><span data-ttu-id="234e1-403">Vue de la table des détails pour le rapport de courrier électronique envoyé et reçu</span><span class="sxs-lookup"><span data-stu-id="234e1-403">Details table view for the Sent and received email report</span></span>

<span data-ttu-id="234e1-404">Si vous cliquez sur **afficher les détails** de la table dans la fenêtre dépanner **par : direction** ou dépanner **par :** le mode de direction, les informations suivantes sont affichées :</span><span class="sxs-lookup"><span data-stu-id="234e1-404">If you click **View details table** in the **Break down by: Direction** or **Break down by: Direction** view, the following information is shown:</span></span>

- <span data-ttu-id="234e1-405">**Date (UTC)**</span><span class="sxs-lookup"><span data-stu-id="234e1-405">**Date (UTC)**</span></span>
- <span data-ttu-id="234e1-406">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="234e1-406">**Type**</span></span>
- <span data-ttu-id="234e1-407">**Direction**</span><span class="sxs-lookup"><span data-stu-id="234e1-407">**Direction**</span></span>
- <span data-ttu-id="234e1-408">**Nombre de messages**</span><span class="sxs-lookup"><span data-stu-id="234e1-408">**Message count**</span></span>

<span data-ttu-id="234e1-409">Si vous cliquez sur **filtres** dans un affichage tableau détaillé, vous pouvez modifier les résultats à l’aide des filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="234e1-409">If you click **Filters** in a details table view, you can modify the results with the following filters:</span></span>

- <span data-ttu-id="234e1-410">**Date de début** et **Date de fin**</span><span class="sxs-lookup"><span data-stu-id="234e1-410">**Start date** and **End date**</span></span>
- <span data-ttu-id="234e1-411">Valeurs de la direction</span><span class="sxs-lookup"><span data-stu-id="234e1-411">Direction values</span></span>
- <span data-ttu-id="234e1-412">Valeurs de type</span><span class="sxs-lookup"><span data-stu-id="234e1-412">Type values</span></span>

<span data-ttu-id="234e1-413">Pour revenir à l’affichage de rapport, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="234e1-413">To go back to the report view, click **View report**.</span></span>

## <a name="top-senders-and-recipients-report"></a><span data-ttu-id="234e1-414">Rapport des expéditeurs et des destinataires principaux</span><span class="sxs-lookup"><span data-stu-id="234e1-414">Top senders and recipients report</span></span>

<span data-ttu-id="234e1-415">Le rapport des **expéditeurs et des destinataires principaux** est un graphique en secteurs illustrant les principaux expéditeurs et destinataires de votre courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="234e1-415">The **Top senders and recipients** report is a pie chart showing your top email senders and recipients.</span></span>

<span data-ttu-id="234e1-416">Pour afficher le rapport, ouvrez le [Centre de sécurité & conformité](https://protection.office.com), accédez à **rapports** \> **Dashboard** et sélectionnez **principaux expéditeurs et destinataires**.</span><span class="sxs-lookup"><span data-stu-id="234e1-416">To view the report, open the [Security & Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** and select **Top senders and recipients**.</span></span> <span data-ttu-id="234e1-417">Pour accéder directement au rapport, ouvrez <https://protection.office.com/reportv2?id=TopSenderRecipientsATP> .</span><span class="sxs-lookup"><span data-stu-id="234e1-417">To go directly to the report, open <https://protection.office.com/reportv2?id=TopSenderRecipientsATP>.</span></span>

![Widget principaux expéditeurs et destinataires dans le tableau de bord rapports](../../media/top-senders-and-recipients-widget.png)

### <a name="report-view-for-the-top-senders-and-recipient-report"></a><span data-ttu-id="234e1-419">Affichage de rapport pour le rapport des expéditeurs et des destinataires principaux</span><span class="sxs-lookup"><span data-stu-id="234e1-419">Report view for the Top senders and recipient report</span></span>

<span data-ttu-id="234e1-420">Les graphiques suivants sont disponibles dans l’affichage rapport :</span><span class="sxs-lookup"><span data-stu-id="234e1-420">The following charts are available in the report view:</span></span>

- <span data-ttu-id="234e1-421">**Afficher les données des \> expéditeurs de messages principaux**</span><span class="sxs-lookup"><span data-stu-id="234e1-421">**Show data for \> Top mail senders**</span></span>
- <span data-ttu-id="234e1-422">**Afficher les données des \> destinataires de messagerie les plus fréquents**</span><span class="sxs-lookup"><span data-stu-id="234e1-422">**Show data for \> Top mail recipients**</span></span>
- <span data-ttu-id="234e1-423">**Afficher les données pour les \> destinataires de courrier indésirable principaux**</span><span class="sxs-lookup"><span data-stu-id="234e1-423">**Show data for \> Top spam recipients**</span></span>
- <span data-ttu-id="234e1-424">**Afficher les données pour \> Principaux destinataires de programmes malveillants** (EoP)</span><span class="sxs-lookup"><span data-stu-id="234e1-424">**Show data for \> Top malware recipients** (EOP)</span></span>
- <span data-ttu-id="234e1-425">**Afficher les données pour les \> destinataires de programmes malveillants principaux (Defender pour Office 365)**</span><span class="sxs-lookup"><span data-stu-id="234e1-425">**Show data for \> Top malware recipients (Defender for Office 365)**</span></span> 

<span data-ttu-id="234e1-426">La composition du graphique en secteurs est modifiée en fonction de ces sélections.</span><span class="sxs-lookup"><span data-stu-id="234e1-426">The composition of the pie chart changes based on these selections.</span></span>

<span data-ttu-id="234e1-427">Lorsque vous placez le curseur de la souris sur un coin du graphique en secteurs, vous pouvez voir le nombre de messages envoyés ou reçus.</span><span class="sxs-lookup"><span data-stu-id="234e1-427">When you hover over a wedge in the pie chart, you can see a count of messages sent or received.</span></span>

<span data-ttu-id="234e1-428">Si vous cliquez sur **filtres** dans un affichage de rapport, vous pouvez spécifier une plage de dates avec **Date de début** et date de **fin**.</span><span class="sxs-lookup"><span data-stu-id="234e1-428">If you click **Filters** in a report view, you can specify a date range with **Start date** and **End date**.</span></span>

![Graphique en secteurs en mode état dans le rapport des expéditeurs et destinataires principaux](../../media/top-senders-and-recipients-report-view.png)

### <a name="details-table-view-for-the-top-senders-and-recipient-report"></a><span data-ttu-id="234e1-430">Vue de la table Détails pour le rapport des expéditeurs et des destinataires principaux</span><span class="sxs-lookup"><span data-stu-id="234e1-430">Details table view for the Top senders and recipient report</span></span>

<span data-ttu-id="234e1-431">Si vous cliquez sur **afficher les détails table** , les informations affichées dépendent du graphique que vous examinez :</span><span class="sxs-lookup"><span data-stu-id="234e1-431">If you click **View details table** , the information that's shown depends on the chart you were looking at:</span></span>

- <span data-ttu-id="234e1-432">**Afficher les données des \> expéditeurs de messages principaux**</span><span class="sxs-lookup"><span data-stu-id="234e1-432">**Show data for \> Top mail senders**</span></span>

  - <span data-ttu-id="234e1-433">**Principaux expéditeurs de messagerie**</span><span class="sxs-lookup"><span data-stu-id="234e1-433">**Top mail senders**</span></span>
  - <span data-ttu-id="234e1-434">**Count**</span><span class="sxs-lookup"><span data-stu-id="234e1-434">**Count**</span></span>

- <span data-ttu-id="234e1-435">**Afficher les données des \> destinataires de messagerie les plus fréquents**</span><span class="sxs-lookup"><span data-stu-id="234e1-435">**Show data for \> Top mail recipients**</span></span>

  - <span data-ttu-id="234e1-436">**Principaux destinataires de messagerie**</span><span class="sxs-lookup"><span data-stu-id="234e1-436">**Top mail recipients**</span></span>
  - <span data-ttu-id="234e1-437">**Count**</span><span class="sxs-lookup"><span data-stu-id="234e1-437">**Count**</span></span>

- <span data-ttu-id="234e1-438">**Afficher les données pour les \> destinataires de courrier indésirable principaux**</span><span class="sxs-lookup"><span data-stu-id="234e1-438">**Show data for \> Top spam recipients**</span></span>

  - <span data-ttu-id="234e1-439">**Principaux destinataires de courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="234e1-439">**Top spam recipients**</span></span>
  - <span data-ttu-id="234e1-440">**Count**</span><span class="sxs-lookup"><span data-stu-id="234e1-440">**Count**</span></span>

- <span data-ttu-id="234e1-441">**Afficher les données pour \> Principaux destinataires de programmes malveillants** (EoP)</span><span class="sxs-lookup"><span data-stu-id="234e1-441">**Show data for \> Top malware recipients** (EOP)</span></span>

  - <span data-ttu-id="234e1-442">**Principaux destinataires de programmes malveillants**</span><span class="sxs-lookup"><span data-stu-id="234e1-442">**Top malware recipients**</span></span>
  - <span data-ttu-id="234e1-443">**Count**</span><span class="sxs-lookup"><span data-stu-id="234e1-443">**Count**</span></span>

- <span data-ttu-id="234e1-444">**Afficher les données pour les \> destinataires de programmes malveillants principaux (Defender pour Office 365)**</span><span class="sxs-lookup"><span data-stu-id="234e1-444">**Show data for \> Top malware recipients (Defender for Office 365)**</span></span> 

  - <span data-ttu-id="234e1-445">**Principaux destinataires de programmes malveillants (Defender pour Office 365)**</span><span class="sxs-lookup"><span data-stu-id="234e1-445">**Top malware recipients (Defender for Office 365)**</span></span>
  - <span data-ttu-id="234e1-446">**Count**</span><span class="sxs-lookup"><span data-stu-id="234e1-446">**Count**</span></span>

<span data-ttu-id="234e1-447">Si vous cliquez sur **filtres** dans un affichage tableau détaillé, vous pouvez spécifier une plage de dates avec **Date de début** et date de **fin**.</span><span class="sxs-lookup"><span data-stu-id="234e1-447">If you click **Filters** in a details table view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="234e1-448">Pour revenir à l’affichage de rapport, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="234e1-448">To go back to the report view, click **View report**.</span></span>

## <a name="what-permissions-are-needed-to-view-these-reports"></a><span data-ttu-id="234e1-449">Quelles sont les autorisations nécessaires pour afficher ces rapports ?</span><span class="sxs-lookup"><span data-stu-id="234e1-449">What permissions are needed to view these reports?</span></span>

<span data-ttu-id="234e1-450">Pour afficher et utiliser les rapports, vous devez être membre du groupe de rôles spécifié dans le centre de sécurité & conformité **et** dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="234e1-450">To view and use the reports, you need to be a member of the specified role group in the Security & Compliance Center **and** in Exchange Online.</span></span>

- <span data-ttu-id="234e1-451">Dans le centre de sécurité & conformité, vous devez être membre de l’un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="234e1-451">In the Security & Compliance Center, you need to be a member of one of the following role groups:</span></span>

  <span data-ttu-id="234e1-452">-Gestion de l’organisation-administrateur de la sécurité (vous pouvez également le faire dans le [Centre d’administration Azure Active Directory](https://aad.portal.azure.com) -lecteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="234e1-452">-Organization Management -Security Administrator (you can also do this in the [Azure Active Directory admin center](https://aad.portal.azure.com) -Security Reader</span></span>

  <span data-ttu-id="234e1-453">Pour en savoir plus, consultez [Autorisations dans le Centre de sécurité et de conformité](https://docs.microsoft.com/microsoft-365/security/office-365-security/permissions-in-the-security-and-compliance-center).</span><span class="sxs-lookup"><span data-stu-id="234e1-453">For more information, see [Permissions in the Security & Compliance Center](https://docs.microsoft.com/microsoft-365/security/office-365-security/permissions-in-the-security-and-compliance-center).</span></span>

- <span data-ttu-id="234e1-454">Dans Exchange Online, vous devez être membre de l’un des groupes de rôles suivants :</span><span class="sxs-lookup"><span data-stu-id="234e1-454">In Exchange Online, you need to be a member of one of the following role groups:</span></span>

  <span data-ttu-id="234e1-455">-Gestion de l’organisation-affichage uniquement-gestion de l’organisation-affichage uniquement des destinataires-gestion de la conformité</span><span class="sxs-lookup"><span data-stu-id="234e1-455">-Organization Management -View-only Organization Management -View-Only Recipients -Compliance Management</span></span>

<span data-ttu-id="234e1-456">Pour plus d’informations, consultez la rubrique [autorisations dans Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo) et [gérer les groupes de rôles dans Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/role-groups).</span><span class="sxs-lookup"><span data-stu-id="234e1-456">For more information, see [Permissions in Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/permissions-exo) and [Manage role groups in Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/role-groups).</span></span>

## <a name="related-topics"></a><span data-ttu-id="234e1-457">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="234e1-457">Related topics</span></span>

[<span data-ttu-id="234e1-458">Rapports intelligents et aperçus dans le Centre de sécurité et conformité</span><span class="sxs-lookup"><span data-stu-id="234e1-458">Smart reports and insights in the Security & Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)

[<span data-ttu-id="234e1-459">Informations sur le flux de messagerie dans le centre de sécurité et conformité</span><span class="sxs-lookup"><span data-stu-id="234e1-459">Mail flow insights in the Security & Compliance Center</span></span>](mail-flow-insights-v2.md)

[<span data-ttu-id="234e1-460">Afficher les rapports de sécurité de courrier dans le centre de sécurité et conformité</span><span class="sxs-lookup"><span data-stu-id="234e1-460">View email security reports in the Security & Compliance Center</span></span>](view-email-security-reports.md)

[<span data-ttu-id="234e1-461">Afficher les rapports pour Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="234e1-461">View reports for Microsoft Defender for Office 365</span></span>](view-reports-for-atp.md)
