---
title: Afficher les rapports de sécurité du courrier électronique dans le portail Microsoft 365 Defender
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: conceptual
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 3a137e28-1174-42d5-99af-f18868b43e86
ms.collection:
- M365-security-compliance
description: Découvrez comment rechercher et utiliser des rapports de sécurité du courrier électronique pour votre organisation. Les rapports de sécurité du courrier électronique sont disponibles dans le portail Microsoft 365 Defender.
ms.custom: seo-marvel-apr2020
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: d46aec8601d19234eed8682955ffef27b7e9b467
ms.sourcegitcommit: 34c06715e036255faa75c66ebf95c12a85f8ef42
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2021
ms.locfileid: "52985204"
---
# <a name="view-email-security-reports-in-the-microsoft-365-defender-portal"></a><span data-ttu-id="1c8f9-104">Afficher les rapports de sécurité du courrier électronique dans le portail Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="1c8f9-104">View email security reports in the Microsoft 365 Defender portal</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="1c8f9-105">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-105">**Applies to**</span></span>
- [<span data-ttu-id="1c8f9-106">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="1c8f9-106">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="1c8f9-107">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="1c8f9-107">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="1c8f9-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="1c8f9-108">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="1c8f9-109">De nombreux rapports sont disponibles sur le portail Microsoft 365 Defender pour vous aider à voir comment les fonctionnalités de sécurité du courrier électronique, telles que les fonctionnalités anti-courrier indésirable, anti-programme malveillant et de chiffrement dans <https://security.microsoft.com> Microsoft 365, protègent votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-109">A variety of reports are available in the Microsoft 365 Defender portal at <https://security.microsoft.com> to help you see how email security features, such as anti-spam, anti-malware, and encryption features in Microsoft 365 are protecting your organization.</span></span> <span data-ttu-id="1c8f9-110">Si vous avez les [autorisations](#what-permissions-are-needed-to-view-these-reports)nécessaires, vous pouvez afficher ces rapports dans  le portail Microsoft 365 Defender en allant dans Rapports e-mail & \> **collaboration** \> **e-mail & rapports de collaboration.**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-110">If you have the [necessary permissions](#what-permissions-are-needed-to-view-these-reports), you can view these reports in the Microsoft 365 Defender portal by going to **Reports** \> **Email & collaboration** \> **Email & collaboration reports**.</span></span> <span data-ttu-id="1c8f9-111">Pour aller directement à la page **e-mail & rapports** de collaboration, ouvrez <https://security.microsoft.com/emailandcollabreport> .</span><span class="sxs-lookup"><span data-stu-id="1c8f9-111">To go directly to the **Email & collaboration reports** page, open <https://security.microsoft.com/emailandcollabreport>.</span></span>

![Page de & de collaboration par courrier électronique dans le portail Microsoft 365 Defender](../../media/email-collaboration-reports.png)

> [!NOTE]
>
> <span data-ttu-id="1c8f9-113">Certains rapports de la page rapports de collaboration & **courrier** électronique nécessitent Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-113">Some of the reports on the **Email & collaboration reports** page require Microsoft Defender for Office 365.</span></span> <span data-ttu-id="1c8f9-114">Pour plus d’informations sur ces rapports, voir les rapports View Defender pour Office 365 dans le portail [Microsoft 365 Defender.](view-reports-for-mdo.md)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-114">For information about these reports, see [View Defender for Office 365 reports in the Microsoft 365 Defender portal](view-reports-for-mdo.md).</span></span>
>
> <span data-ttu-id="1c8f9-115">Les rapports liés au flux de messagerie sont désormais dans le Centre d’administration Exchange (EAC).</span><span class="sxs-lookup"><span data-stu-id="1c8f9-115">Reports that are related to mail flow are now in the Exchange admin center (EAC).</span></span> <span data-ttu-id="1c8f9-116">Pour plus d’informations sur ces rapports, voir Rapports de [flux de messagerie dans le nouveau Centre d’administration Exchange.](/exchange/monitoring/mail-flow-reports/mail-flow-reports)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-116">For more information about these reports, see [Mail flow reports in the new Exchange admin center](/exchange/monitoring/mail-flow-reports/mail-flow-reports).</span></span>

## <a name="compromised-users-report"></a><span data-ttu-id="1c8f9-117">Rapport utilisateurs compromis</span><span class="sxs-lookup"><span data-stu-id="1c8f9-117">Compromised users report</span></span>

> [!NOTE]
> <span data-ttu-id="1c8f9-118">Ce rapport est disponible dans les organisations Microsoft 365 avec des boîtes aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-118">This report is available in Microsoft 365 organizations with Exchange Online mailboxes.</span></span> <span data-ttu-id="1c8f9-119">Il n’est pas disponible dans les organisations Exchange Online Protection (EOP) autonomes.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-119">It's not available in standalone Exchange Online Protection (EOP) organizations.</span></span>

<span data-ttu-id="1c8f9-120">Le **rapport Utilisateurs** compromis indique le nombre de  comptes  d’utilisateurs marqués comme suspects ou restreints au cours des 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-120">The **Compromised users** report shows shows the number of user accounts that were marked as **Suspicious** or **Restricted** within the last 7 days.</span></span> <span data-ttu-id="1c8f9-121">Les comptes dans l’un de ces états sont problématiques, voire compromis.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-121">Accounts in either of these states are problematic or even compromised.</span></span> <span data-ttu-id="1c8f9-122">Avec une utilisation fréquente, vous pouvez utiliser le rapport pour repérer des pics, voire des tendances, dans des comptes suspects ou restreints.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-122">With frequent use, you can use the report to spot spikes, and even trends, in suspicious or restricted accounts.</span></span> <span data-ttu-id="1c8f9-123">Pour plus d’informations sur les utilisateurs compromis, voir [Répondre à un compte de messagerie compromis.](responding-to-a-compromised-email-account.md)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-123">For more information about compromised users, see [Responding to a compromised email account](responding-to-a-compromised-email-account.md).</span></span>

![Widget Utilisateurs compromis sur la page rapports de collaboration & messagerie](../../media/compromised-users-report-widget.png)

<span data-ttu-id="1c8f9-125">L’affichage agrégé affiche les données des 90 derniers jours et l’affichage détail affiche les données des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-125">The aggregate view shows data for the last 90 days and the detail view shows data for the last 30 days.</span></span>

<span data-ttu-id="1c8f9-126">Pour afficher le rapport dans le portail Microsoft  365 Defender, consultez La boîte aux & collaboration de rapports e-mail \>  \> **& rapports de collaboration.**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-126">To view the report in the Microsoft 365 Defender portal, go to **Reports** \> **Email & collaboration** \> **Email & collaboration reports**.</span></span> <span data-ttu-id="1c8f9-127">Sur **Utilisateurs compromis,** cliquez **sur Afficher les détails.**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-127">On **Compromised users**, click **View details**.</span></span> <span data-ttu-id="1c8f9-128">Pour aller directement dans le rapport, ouvrez <https://security.microsoft.com/reports/CompromisedUsers> .</span><span class="sxs-lookup"><span data-stu-id="1c8f9-128">To go directly to the report, open <https://security.microsoft.com/reports/CompromisedUsers>.</span></span>

<span data-ttu-id="1c8f9-129">Après avoir cliqué sur Afficher les **détails,** vous pouvez  filtrer à la fois le graphique et le tableau de détails en cliquant sur Filtrer et en sélectionnant une ou plusieurs des valeurs suivantes dans le volant qui s’affiche :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-129">After you click **View details**, you can filter both the chart and the details table by clicking **Filter** and selecting one or more of the following values in the flyout that appears:</span></span>

- <span data-ttu-id="1c8f9-130">**Date (UTC)**: **date de début** et date de **fin.**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-130">**Date (UTC)**: **Start date** and **End date**.</span></span>
- <span data-ttu-id="1c8f9-131">**Activité**:</span><span class="sxs-lookup"><span data-stu-id="1c8f9-131">**Activity**:</span></span>
  - <span data-ttu-id="1c8f9-132">**Suspect**: le compte d’utilisateur a envoyé des messages suspects et risque d’être limité à l’envoi de courriers électroniques.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-132">**Suspicious**: The user account has sent suspicious email and is at risk of being restricted from sending email.</span></span>
  - <span data-ttu-id="1c8f9-133">**Restreint :** le compte d’utilisateur n’a pas pu envoyer de courrier électronique en raison de modèles hautement suspects.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-133">**Restricted**: The user account has been restricted from sending email due to highly suspicious patterns.</span></span>

<span data-ttu-id="1c8f9-134">Lorsque vous avez terminé le filtrage, cliquez sur **Appliquer** ou **Annuler.**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-134">When you're finished filtering, click **Apply** or **Cancel**.</span></span>

![Affichage du rapport dans le rapport Utilisateurs compromis](../../media/compromised-users-report-activity-view.png)

<span data-ttu-id="1c8f9-136">Dans le tableau sous le graphique, vous pouvez voir les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-136">In the table below the graph, you can see the following details:</span></span>

- <span data-ttu-id="1c8f9-137">**Heure de création**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-137">**Creation time**</span></span>
- <span data-ttu-id="1c8f9-138">**ID d'utilisateur**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-138">**User ID**</span></span>
- <span data-ttu-id="1c8f9-139">**Action**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-139">**Action**</span></span>

## <a name="exchange-transport-rule-report"></a><span data-ttu-id="1c8f9-140">Rapport de règles de transport Exchange</span><span class="sxs-lookup"><span data-stu-id="1c8f9-140">Exchange transport rule report</span></span>

<span data-ttu-id="1c8f9-141">Le **rapport des règles** de transport Exchange indique l’effet des règles de flux de messagerie (également appelées règles de transport) sur les messages entrants et sortants dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-141">The **Exchange transport rule** report shows the effect of mail flow rules (also known as transport rules) on incoming and outgoing messages in your organization.</span></span>

<span data-ttu-id="1c8f9-142">Pour afficher le rapport dans le portail Microsoft  365 Defender, consultez La boîte aux & collaboration de rapports e-mail \>  \> **& rapports de collaboration.**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-142">To view the report in the Microsoft 365 Defender portal, go to **Reports** \> **Email & collaboration** \> **Email & collaboration reports**.</span></span> <span data-ttu-id="1c8f9-143">Dans la **règle de transport Exchange,** cliquez **sur Afficher les détails.**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-143">On **Exchange transport rule**, click **View details**.</span></span> <span data-ttu-id="1c8f9-144">Pour aller directement dans le rapport, ouvrez <https://security.microsoft.com/reports/ETRRuleReport> .</span><span class="sxs-lookup"><span data-stu-id="1c8f9-144">To go directly to the report, open <https://security.microsoft.com/reports/ETRRuleReport>.</span></span>

![Widget de règles de transport Exchange dans la page rapports de collaboration & courrier électronique](../../media/transport-rule-report-widget.png)

<span data-ttu-id="1c8f9-146">Une fois que vous avez **cliqué sur Afficher les détails,** les graphiques et données suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-146">After you click **View details**, the following charts and data are available:</span></span>

- <span data-ttu-id="1c8f9-147">**Afficher les données par règles de transport** \> Exchange **Répartition du graphique par direction**:  ce graphique indique le nombre de **messages** entrants et sortants affectés par les règles de flux de messagerie.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-147">**View data by Exchange transport rules** \> **Chart breakdown by Direction**: This chart shows the number of **Inbound** and **Outbound** messages that were affected by mail flow rules.</span></span>

- <span data-ttu-id="1c8f9-148">**Afficher les données par règles de transport** \> Exchange **Répartition du graphique par gravité**: ce graphique indique le nombre de messages de gravité **élevée,** moyenne et **faible.**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-148">**View data by Exchange transport rules** \> **Chart breakdown by Severity**: This chart shows the number of **High severity**, **Medium severity**, and **Low severity** messages.</span></span> <span data-ttu-id="1c8f9-149">Vous définissez le niveau de gravité en tant qu’action dans la règle (**Auditez** cette règle avec le niveau de gravité _ou SetAuditSeverity_).</span><span class="sxs-lookup"><span data-stu-id="1c8f9-149">You set the severity level as an action in the rule (**Audit this rule with severity level** or _SetAuditSeverity_).</span></span> <span data-ttu-id="1c8f9-150">Pour plus d’informations, voir [Actions de règle de flux de messagerie dans Exchange Online.](/Exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-150">For more information, see [Mail flow rule actions in Exchange Online](/Exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions).</span></span>

- <span data-ttu-id="1c8f9-151">**Afficher les données par règles de transport** \> Exchange DLP **Répartition du graphique par direction**:  ce graphique indique le nombre de **messages** entrants et sortants affectés par les règles de flux de messagerie de protection contre la perte de données (DLP).</span><span class="sxs-lookup"><span data-stu-id="1c8f9-151">**View data by DLP Exchange transport rules** \> **Chart breakdown by Direction**: This chart shows the number of **Inbound** and **Outbound** messages that were affected by data loss prevention (DLP) mail flow rules.</span></span>

- <span data-ttu-id="1c8f9-152">**Afficher les données par règles de transport** \> Exchange DLP **Répartition du graphique par gravité**: cet affichage indique le nombre de **messages** de gravité **élevée,** moyenne et faible qui ont été affectés par les règles de flux de messagerie DLP.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-152">**View data by DLP Exchange transport rules** \> **Chart breakdown by Severity**: This view shows the number of **High severity**, **Medium severity**, and **Low severity** messages that were affected by DLP mail flow rules.</span></span>

<span data-ttu-id="1c8f9-153">Pour **afficher les données par sélections de** règles de transport Exchange, les informations suivantes sont affichées dans le tableau de détails sous le graphique :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-153">For **View data by Exchange transport rules** selections, the following information is shown in the details table below the graph:</span></span>

- <span data-ttu-id="1c8f9-154">**Date**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-154">**Date**</span></span>
- <span data-ttu-id="1c8f9-155">**Règle de transport**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-155">**Transport rule**</span></span>
- <span data-ttu-id="1c8f9-156">**Subject**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-156">**Subject**</span></span>
- <span data-ttu-id="1c8f9-157">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-157">**Sender address**</span></span>
- <span data-ttu-id="1c8f9-158">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-158">**Recipient address**</span></span>
- <span data-ttu-id="1c8f9-159">**Gravité**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-159">**Severity**</span></span>
- <span data-ttu-id="1c8f9-160">**Direction**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-160">**Direction**</span></span>

<span data-ttu-id="1c8f9-161">Pour afficher les données par sélections de règles de **transport Exchange DLP,** les informations suivantes sont affichées dans le tableau de détails sous le graphique :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-161">For **View data by DLP Exchange transport rules** selections, the following information is shown in the details table below the graph:</span></span>

- <span data-ttu-id="1c8f9-162">**Date**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-162">**Date**</span></span>
- <span data-ttu-id="1c8f9-163">**Stratégie DLP**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-163">**DLP policy**</span></span>
- <span data-ttu-id="1c8f9-164">**Règle de transport**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-164">**Transport rule**</span></span>
- <span data-ttu-id="1c8f9-165">**Subject**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-165">**Subject**</span></span>
- <span data-ttu-id="1c8f9-166">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-166">**Sender address**</span></span>
- <span data-ttu-id="1c8f9-167">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-167">**Recipient address**</span></span>
- <span data-ttu-id="1c8f9-168">**Gravité**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-168">**Severity**</span></span>
- <span data-ttu-id="1c8f9-169">**Direction**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-169">**Direction**</span></span>

<span data-ttu-id="1c8f9-170">Vous pouvez filtrer le graphique et le tableau de détails en cliquant sur **Filtrer** et en sélectionnant une ou plusieurs des valeurs suivantes dans le volant qui s’affiche :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-170">You can filter both the chart and the details table by clicking **Filter** and selecting one or more of the following values in the flyout that appears:</span></span>

- <span data-ttu-id="1c8f9-171">**Date de début** et **date de fin**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-171">**Start date** and **End date**</span></span>
- <span data-ttu-id="1c8f9-172">**Direction**: **sortant et** **entrant**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-172">**Direction**: **Outbound** and **Inbound**</span></span>
- <span data-ttu-id="1c8f9-173">**Gravité :** **gravité élevée,** **gravité moyenne** et gravité **faible**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-173">**Severity**: **High severity**, **Medium severity**, and **Low severity**</span></span>

![Affichage du rapport dans le rapport de règles de transport Exchange](../../media/transport-rule-report-report-view.png)

## <a name="mailflow-status-report"></a><span data-ttu-id="1c8f9-175">Rapport d’état du flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="1c8f9-175">Mailflow status report</span></span>

<span data-ttu-id="1c8f9-176">Le  rapport d’état du flux de messagerie est un rapport intelligent qui affiche des informations sur le courrier électronique entrant et sortant, les détections de courrier indésirable, les programmes malveillants, les e-mails identifiés comme « bons » et les informations sur les messages électroniques autorisés ou bloqués sur le edge.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-176">The **Mailflow status report** is a smart report that shows information about incoming and outgoing email, spam detections, malware, email identified as "good", and information about email allowed or blocked on the edge.</span></span> <span data-ttu-id="1c8f9-177">Il s’agit du seul rapport qui contient des informations de protection Edge et indique la quantité de courrier électronique bloquée avant d’être autorisé dans le service pour évaluation par Exchange Online Protection (EOP).</span><span class="sxs-lookup"><span data-stu-id="1c8f9-177">This is the only report that contains edge protection information, and shows just how much email is blocked before being allowed into the service for evaluation by Exchange Online Protection (EOP).</span></span> <span data-ttu-id="1c8f9-178">Il est important de comprendre que si un message est envoyé à cinq destinataires, nous le compterons comme cinq messages différents et pas un seul message.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-178">It's important to understand that if a message is sent to five recipients we count it as five different messages and not one message.</span></span>

<span data-ttu-id="1c8f9-179">Pour afficher le rapport dans le portail Microsoft  365 Defender, consultez La boîte aux & collaboration de rapports e-mail \>  \> **& rapports de collaboration.**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-179">To view the report in the Microsoft 365 Defender portal, go to **Reports** \> **Email & collaboration** \> **Email & collaboration reports**.</span></span> <span data-ttu-id="1c8f9-180">Dans **le résumé de l’état du flux de messagerie,** cliquez sur Afficher les **détails.**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-180">On **Mailflow status summary**, click **View details**.</span></span> <span data-ttu-id="1c8f9-181">Pour aller directement dans le rapport, ouvrez <https://security.microsoft.com/reports/mailflowStatusReport> .</span><span class="sxs-lookup"><span data-stu-id="1c8f9-181">To go directly to the report, open <https://security.microsoft.com/reports/mailflowStatusReport>.</span></span>

![Widget de synthèse de l’état du flux de messagerie dans la page Rapports de collaboration & courrier électronique](../../media/mail-flow-status-report-widget.png)

### <a name="type-view-for-the-mailflow-status-report"></a><span data-ttu-id="1c8f9-183">Affichage des types pour le rapport d’état du flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="1c8f9-183">Type view for the Mailflow status report</span></span>

<span data-ttu-id="1c8f9-184">Lorsque vous ouvrez l’état, **l’onglet Type** est sélectionné par défaut.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-184">When you open the report, the **Type** tab is selected by default.</span></span> <span data-ttu-id="1c8f9-185">Par défaut, cet affichage contient un graphique et une table de données configurés avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-185">By default, this view contains a chart and a data table that's configured with the following filters:</span></span>

- <span data-ttu-id="1c8f9-186">**Date**: 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-186">**Date**: The last 7 days.</span></span>
- <span data-ttu-id="1c8f9-187">**Direction du courrier**:</span><span class="sxs-lookup"><span data-stu-id="1c8f9-187">**Mail direction**:</span></span>
  - <span data-ttu-id="1c8f9-188">**Entrant**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-188">**Inbound**</span></span>
  - <span data-ttu-id="1c8f9-189">**Sortant**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-189">**Outbound**</span></span>
  - <span data-ttu-id="1c8f9-190">**Intra-organisation**: ce nombre est pour les messages au sein d’un client, c’est-à-dire</span><span class="sxs-lookup"><span data-stu-id="1c8f9-190">**Intra-org**: this count is for messages within a tenant i.e</span></span> <span data-ttu-id="1c8f9-191">sender abc@domain.com sends to recipient xyz@domain.com (counted separately from **Inbound** and **Outbound**)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-191">sender abc@domain.com sends to recipient xyz@domain.com  (counted separately from **Inbound** and **Outbound**)</span></span>
- <span data-ttu-id="1c8f9-192">**Tapez**:</span><span class="sxs-lookup"><span data-stu-id="1c8f9-192">**Type**:</span></span>
  - <span data-ttu-id="1c8f9-193">**Bon courrier**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-193">**Good mail**</span></span>
  - <span data-ttu-id="1c8f9-194">**Programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-194">**Malware**</span></span>
  - <span data-ttu-id="1c8f9-195">**Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-195">**Spam**</span></span>
  - <span data-ttu-id="1c8f9-196">**Protection Edge**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-196">**Edge protection**</span></span>
  - <span data-ttu-id="1c8f9-197">**Messages de règle**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-197">**Rule messages**</span></span>
  - <span data-ttu-id="1c8f9-198">**Courriers hameçons**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-198">**Phishing email**</span></span>
- <span data-ttu-id="1c8f9-199">**Domaine**: **Tous**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-199">**Domain**: **All**</span></span>

<span data-ttu-id="1c8f9-200">Le graphique est organisé par les valeurs **Type.**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-200">The chart is organized by the **Type** values.</span></span>

<span data-ttu-id="1c8f9-201">Vous pouvez modifier ces filtres en cliquant sur **Filtre** ou en cliquant sur une valeur dans la légende du graphique.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-201">You can change these filters by clicking **Filter** or by clicking a value in the chart legend.</span></span>

<span data-ttu-id="1c8f9-202">La table de données contient les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-202">The data table contains the following information:</span></span>

- <span data-ttu-id="1c8f9-203">**Direction**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-203">**Direction**</span></span>
- <span data-ttu-id="1c8f9-204">**Type**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-204">**Type**</span></span>
- <span data-ttu-id="1c8f9-205">**24 heures**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-205">**24 hours**</span></span>
- <span data-ttu-id="1c8f9-206">**3 jours**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-206">**3 days**</span></span>
- <span data-ttu-id="1c8f9-207">**7 jours**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-207">**7 days**</span></span>
- <span data-ttu-id="1c8f9-208">**15 jours**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-208">**15 days**</span></span>
- <span data-ttu-id="1c8f9-209">**30 jours**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-209">**30 days**</span></span>

<span data-ttu-id="1c8f9-210">Si vous cliquez **sur Choisir une catégorie pour plus d’informations,** vous pouvez sélectionner l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-210">If you click **Choose a category for more details**, you can select from the following values:</span></span>

- <span data-ttu-id="1c8f9-211">**E-mail de hameçonnage**: cette sélection vous place dans le rapport d’état [de la protection contre les menaces.](view-email-security-reports.md#threat-protection-status-report)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-211">**Phishing email**: This selection takes you to the [Threat protection status report](view-email-security-reports.md#threat-protection-status-report).</span></span>
- <span data-ttu-id="1c8f9-212">**Programmes malveillants dans les e-mails**: cette sélection vous place dans le rapport d’état [de la protection contre les menaces.](view-email-security-reports.md#threat-protection-status-report)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-212">**Malware in email**: This selection takes you to the [Threat protection status report](view-email-security-reports.md#threat-protection-status-report).</span></span>
- <span data-ttu-id="1c8f9-213">**Détections de courrier indésirable**: cette sélection vous permet d’envoyer le rapport [détections de courrier indésirable.](view-email-security-reports.md#spam-detections-report)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-213">**Spam detections**: This selection takes you to the [Spam Detections report](view-email-security-reports.md#spam-detections-report).</span></span>
- <span data-ttu-id="1c8f9-214">**Courrier indésirable bloqué edge**: cette sélection vous permet d’envoyer le rapport [détections de courrier indésirable.](view-email-security-reports.md#spam-detections-report)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-214">**Edge blocked spam**: This selection takes you to the [Spam Detections report](view-email-security-reports.md#spam-detections-report).</span></span>

#### <a name="export-from-type-view"></a><span data-ttu-id="1c8f9-215">Exporter à partir de l’affichage Type</span><span class="sxs-lookup"><span data-stu-id="1c8f9-215">Export from Type view</span></span>

<span data-ttu-id="1c8f9-216">Pour l’affichage détaillé, vous ne pouvez exporter les données que pour une journée.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-216">For the detail view, you can only export data for one day.</span></span> <span data-ttu-id="1c8f9-217">Par exemple, si vous souhaitez exporter des données pendant 7 jours, vous devez faire 7 actions d’exportation différentes.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-217">So, if you want to export data for 7 days, you need to do 7 different export actions.</span></span>

<span data-ttu-id="1c8f9-218">Chaque fichier .csv exporté est limité à 150 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-218">Each exported .csv file is limited to 150,000 rows.</span></span> <span data-ttu-id="1c8f9-219">Si les données de ce jour contiennent plus de 150 000 lignes, plusieurs fichiers .csv seront créés.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-219">If the data for that day contains more than 150,000 rows, then multiple .csv files will be created.</span></span>

![Affichage des types dans le rapport d’état du flux de messagerie](../../media/mail-flow-status-report-type-view.png)

### <a name="direction-view-for-the-mailflow-status-report"></a><span data-ttu-id="1c8f9-221">Affichage direction pour le rapport d’état du flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="1c8f9-221">Direction view for the Mailflow status report</span></span>

<span data-ttu-id="1c8f9-222">Si vous cliquez sur **l’onglet Direction,** les mêmes filtres par défaut de **l’affichage Type** sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-222">If you click the **Direction** tab, the same default filters from the **Type** view are used.</span></span>

<span data-ttu-id="1c8f9-223">Le graphique est organisé par **valeurs direction.**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-223">The chart is organized by **Direction** values.</span></span>

<span data-ttu-id="1c8f9-224">Vous pouvez modifier ces filtres en cliquant sur **Filtre** ou en cliquant sur une valeur dans la légende du graphique.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-224">You can change these filters by clicking **Filter** or by clicking a value in the chart legend.</span></span> <span data-ttu-id="1c8f9-225">Les mêmes filtres de **l’affichage Type** sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-225">The same filters from the **Type** view are used.</span></span>

<span data-ttu-id="1c8f9-226">La table de données contient les mêmes informations que **l’affichage Type.**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-226">The data table contains same information from the **Type** view.</span></span>

<span data-ttu-id="1c8f9-227">La **sélection d’une catégorie pour plus d’informations** sur les sélections disponibles et le comportement sont identiques à l’affichage **Type.**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-227">The **Choose a category for more details** available selections and behavior are the same as the **Type** view.</span></span>

#### <a name="export-from-direction-view"></a><span data-ttu-id="1c8f9-228">Exporter à partir du mode Direction</span><span class="sxs-lookup"><span data-stu-id="1c8f9-228">Export from Direction view</span></span>

<span data-ttu-id="1c8f9-229">Pour l’affichage détaillé, vous ne pouvez exporter les données que pour une journée.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-229">For the detail view, you can only export data for one day.</span></span> <span data-ttu-id="1c8f9-230">Par exemple, si vous souhaitez exporter des données pendant 7 jours, vous devez faire 7 actions d’exportation différentes.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-230">So, if you want to export data for 7 days, you need to do 7 different export actions.</span></span>

<span data-ttu-id="1c8f9-231">Chaque fichier .csv exporté est limité à 150 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-231">Each exported .csv file is limited to 150,000 rows.</span></span> <span data-ttu-id="1c8f9-232">Si les données de ce jour contiennent plus de 150 000 lignes, plusieurs fichiers .csv seront créés.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-232">If the data for that day contains more than 150,000 rows, then multiple .csv files will be created.</span></span>

![Affichage direction dans le rapport d’état du flux de messagerie](../../media/mail-flow-status-report-direction-view.png)

### <a name="funnel-view-for-the-mailflow-status-report"></a><span data-ttu-id="1c8f9-234">Affichage en entonnoir pour le rapport d’état du flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="1c8f9-234">Funnel view for the Mailflow status report</span></span>

<span data-ttu-id="1c8f9-235">La **vue Entonnoir** vous montre comment les fonctionnalités de protection contre les menaces de courrier électronique de Microsoft filtrent le courrier électronique entrant et sortant dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-235">The **Funnel** view shows you how Microsoft's email threat protection features filter incoming and outgoing email in your organization.</span></span> <span data-ttu-id="1c8f9-236">Il fournit des détails sur le nombre total de messages électroniques et sur la façon dont les fonctionnalités de protection contre les menaces configurées, y compris la protection edge, la protection contre les programmes malveillants, l’anti-hameçonnage, le courrier indésirable et la détection d’usurpation d’accès affectent ce nombre.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-236">It provides details on the total email count, and how the configured threat protection features, including edge protection, anti-malware, anti-phishing, anti-spam, and anti-spoofing affect this count.</span></span>

<span data-ttu-id="1c8f9-237">Si vous  cliquez sur l’onglet Entonnoir, par défaut, cet affichage contient un graphique et une table de données configurés avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-237">If you click the **Funnel** tab, by default, this view contains a chart and a data table that's configured with the following filters:</span></span>

- <span data-ttu-id="1c8f9-238">**Date**: 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-238">**Date**: The last 7 days.</span></span>

- <span data-ttu-id="1c8f9-239">**Direction**:</span><span class="sxs-lookup"><span data-stu-id="1c8f9-239">**Direction**:</span></span>

  - <span data-ttu-id="1c8f9-240">**Entrant**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-240">**Inbound**</span></span>
  - <span data-ttu-id="1c8f9-241">**Sortant**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-241">**Outbound**</span></span>
  - <span data-ttu-id="1c8f9-242">**Intra-organisation**: ce nombre est le nombre de messages envoyés au sein d’un client ; Autrement dit, l’expéditeur abc@domain.com envoyé au destinataire xyz@domain.com (comptabilisé séparément des messages entrants et sortants).</span><span class="sxs-lookup"><span data-stu-id="1c8f9-242">**Intra-org**: This count is for messages sent within a tenant; i.e, sender abc@domain.com sends to recipient xyz@domain.com (counted separately from Inbound and Outbound).</span></span>

<span data-ttu-id="1c8f9-243">L’affichage agrégé et l’affichage de table de données autorisent 90 jours de filtrage.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-243">The aggregate view and data table view allow for 90 days of filtering.</span></span>

<span data-ttu-id="1c8f9-244">Si vous cliquez **sur Filtre,** vous pouvez filtrer le graphique et la table de données.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-244">If you click **Filter**, you can filter both the chart and the data table.</span></span>

<span data-ttu-id="1c8f9-245">Ce graphique indique le nombre de messages électroniques organisés par :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-245">This chart shows the email count organized by:</span></span>

- <span data-ttu-id="1c8f9-246">**Nombre total de messages électroniques**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-246">**Total email**</span></span>
- <span data-ttu-id="1c8f9-247">**Courrier électronique après protection edge**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-247">**Email after edge protection**</span></span>
- <span data-ttu-id="1c8f9-248">**Règle de messagerie après transport** (règle de flux de messagerie)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-248">**Email after transport rule** (mail flow rule)</span></span>
- <span data-ttu-id="1c8f9-249">**Courrier électronique après anti-programme malveillant, réputation du fichier, bloc de type de fichier**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-249">**Email after anti-malware, file reputation, file type block**</span></span>
- <span data-ttu-id="1c8f9-250">**Courrier électronique après anti-hameçonnage, réputation d’URL, emprunt d’identité de marque, anti-usurpation d’identité**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-250">**Email after anti-phish, URL reputation, brand impersonation, anti-spoof**</span></span>
- <span data-ttu-id="1c8f9-251">**Courrier électronique après filtrage du courrier indésirable en bloc**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-251">**Email after anti-spam, bulk mail filtering**</span></span>
- <span data-ttu-id="1c8f9-252">**Courrier électronique après l’emprunt d’identité de l’utilisateur et du domaine**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="1c8f9-252">**Email after user and domain impersonation**<sup>\*</sup></span></span>
- <span data-ttu-id="1c8f9-253">**E-mail après détonation du fichier et de l’URL**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="1c8f9-253">**Email after file and URL detonation**<sup>\*</sup></span></span>
- <span data-ttu-id="1c8f9-254">**Courrier électronique détecté comme étant anodin après la remise (protection de temps de clic d’URL)**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-254">**Email detected as benign after post-delivery protection (URL click time protection)**</span></span>

<span data-ttu-id="1c8f9-255"><sup>\*</sup>Defender pour Office 365 uniquement</span><span class="sxs-lookup"><span data-stu-id="1c8f9-255"><sup>\*</sup> Defender for Office 365 only</span></span>

<span data-ttu-id="1c8f9-256">Pour afficher l’e-mail filtré par EOP ou Defender Office 365 séparément, cliquez sur la valeur dans la légende du graphique.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-256">To view the email filtered by EOP or Defender for Office 365 separately, click on the value in the chart legend.</span></span>

<span data-ttu-id="1c8f9-257">La table de données contient les informations suivantes, indiquées dans l’ordre décroit de date :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-257">The data table contains the following information, shown in descending date order:</span></span>

- <span data-ttu-id="1c8f9-258">**Date**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-258">**Date**</span></span>
- <span data-ttu-id="1c8f9-259">**Nombre total de messages électroniques**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-259">**Total email**</span></span>
- <span data-ttu-id="1c8f9-260">**Protection Edge**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-260">**Edge protection**</span></span>
- <span data-ttu-id="1c8f9-261">**Anti-programme malveillant, réputation de fichier, bloc de type de fichier**:</span><span class="sxs-lookup"><span data-stu-id="1c8f9-261">**Anti-malware, file reputation, file type block**:</span></span>
  - <span data-ttu-id="1c8f9-262">**Réputation du** fichier : messages filtrés en raison de l’identification d’un fichier joint par d’autres clients Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-262">**File reputation**: Messages filtered due to identification of an attached file by other Microsoft customers.</span></span>
  - <span data-ttu-id="1c8f9-263">**Bloc de type de** fichier : messages filtrés en raison du type de fichier malveillant identifié dans le message.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-263">**File type block**: Messages filtered due to the type of malicious file identified in the message.</span></span>
- <span data-ttu-id="1c8f9-264">**Anti-hameçonnage, réputation de l’URL, emprunt d’identité de marque, anti-usurpation d’identité**:</span><span class="sxs-lookup"><span data-stu-id="1c8f9-264">**Anti-phish, URL reputation, Brand impersonation, anti-spoof**:</span></span>
  - <span data-ttu-id="1c8f9-265">**Réputation de l’URL**: messages filtrés en raison de l’identification de l’URL par d’autres clients Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-265">**URL reputation**: Messages filtered due to the identification of the URL by other Microsoft customers.</span></span>
  - <span data-ttu-id="1c8f9-266">**Emprunt d’identité de marque**: messages filtrés en raison du message provenant de la marque connue usurpant l’identité des expéditeurs.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-266">**Brand impersonation**: Messages filtered due to the message coming from well-known brand impersonating senders.</span></span>
  - <span data-ttu-id="1c8f9-267">**Anti-usurpation**: messages filtrés en raison de la tentative d’usurpation d’un domaine appartenant au destinataire ou d’un domaine que l’expéditeur du message ne possède pas.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-267">**Anti-spoof**: Messages filtered due to the message attempting to spoof a domain that the recipient belongs to, or a domain that the message sender doesn't own.</span></span>
- <span data-ttu-id="1c8f9-268">**Anti-courrier indésirable, filtrage du courrier en bloc**:</span><span class="sxs-lookup"><span data-stu-id="1c8f9-268">**Anti-spam, bulk mail filtering**:</span></span>
  - <span data-ttu-id="1c8f9-269">**Filtrage du courrier en bloc**: messages filtrés en fonction du seuil bcl (seuil de plainte en bloc) dans une stratégie anti-courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-269">**Bulk mail filtering**: Messages filtered based on the bulk complain level (BCL) threshold in an anti-spam policy.</span></span>
- <span data-ttu-id="1c8f9-270">**Emprunt d’identité d’utilisateur et** de domaine (Defender pour Office 365) :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-270">**User and domain impersonation (Defender for Office 365)**:</span></span>
  - <span data-ttu-id="1c8f9-271">**Emprunt d’identité** d’utilisateur : messages filtrés en raison d’une tentative d’emprunt d’identité d’un utilisateur (expéditeur de message) défini dans les paramètres de protection contre l’emprunt d’identité d’une stratégie anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-271">**User impersonation**: Messages filtered due to an attempt to impersonate a user (message sender) that's defined in the impersonation protection settings of an anti-phishing policy.</span></span>
  - <span data-ttu-id="1c8f9-272">**Emprunt d’identité** de domaine : messages filtrés en raison d’une tentative d’emprunt d’identité d’un domaine défini dans les paramètres de protection contre l’emprunt d’identité d’une stratégie anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-272">**Domain impersonation**: Messages filtered due to an attempt to impersonate a domain that's defined in the impersonation protection settings of an anti-phishing policy.</span></span>
- <span data-ttu-id="1c8f9-273">**Détonation de fichier et d’URL (Defender pour Office 365)**:</span><span class="sxs-lookup"><span data-stu-id="1c8f9-273">**File and URL detonation (Defender for Office 365)**:</span></span>
  - <span data-ttu-id="1c8f9-274">**Détonation de fichier**: messages filtrés par une stratégie Safe pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-274">**File detonation**: Messages filtered by a Safe Attachments policy.</span></span>
  - <span data-ttu-id="1c8f9-275">**Détonation d’URL**: message filtré par une stratégie Safe liens.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-275">**URL detonation**: Message filtered by a Safe Links policy.</span></span>
- <span data-ttu-id="1c8f9-276">Protection post-remise et ZAP (Protection contre les menaces) ou **ZAP (EOP)**: purge automatique de zéro heure (ZAP) pour les programmes malveillants, le courrier indésirable et le hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-276">**Post-delivery protection and ZAP (ATP), or ZAP (EOP)**: Zero-hour auto purge (ZAP) for malware, spam, and phishing.</span></span>

<span data-ttu-id="1c8f9-277">Si vous sélectionnez une ligne dans la table de données, une répartition supplémentaire du nombre de messages électroniques est affichée dans le volant.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-277">If you select a row in the data table, a further breakdown of the email counts are shown in the flyout.</span></span>

#### <a name="export-from-funnel-view"></a><span data-ttu-id="1c8f9-278">Exporter à partir du affichage Entonnoir</span><span class="sxs-lookup"><span data-stu-id="1c8f9-278">Export from Funnel view</span></span>

<span data-ttu-id="1c8f9-279">Après avoir cliqué **sur Exporter** sous **Options,** vous pouvez sélectionner l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-279">After you click **Export** under **Options**, you can select one of the following values:</span></span>

- <span data-ttu-id="1c8f9-280">**Résumé (avec des données pour les 90 derniers jours au maximum)**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-280">**Summary (with data for last 90 days at most)**</span></span>
- <span data-ttu-id="1c8f9-281">**Détails (avec des données pour les 30 derniers jours au maximum)**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-281">**Details (with data for last 30 days at most)**</span></span>

<span data-ttu-id="1c8f9-282">Sous **Date**, choisissez une plage, puis cliquez sur **Appliquer**.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-282">Under **Date**, choose a range, and then click **Apply**.</span></span> <span data-ttu-id="1c8f9-283">Les données des filtres actuels sont exportées vers un .csv de données.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-283">Data for the current filters will be exported to a .csv file.</span></span>

<span data-ttu-id="1c8f9-284">Chaque fichier .csv exporté est limité à 150 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-284">Each exported .csv file is limited to 150,000 rows.</span></span> <span data-ttu-id="1c8f9-285">Si les données contiennent plus de 150 000 lignes, plusieurs .csv fichiers seront créés.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-285">If the data contains more than 150,000 rows, then multiple .csv files will be created.</span></span>

![Affichage en entonnoir dans le rapport d’état du flux de messagerie](../../media/mail-flow-status-report-funnel-view.png)

### <a name="tech-view-for-the-mailflow-status-report"></a><span data-ttu-id="1c8f9-287">Affichage technique pour le rapport d’état du flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="1c8f9-287">Tech view for the Mailflow status report</span></span>

<span data-ttu-id="1c8f9-288">La **vue Tech est** similaire à la vue Entonnoir, fournissant des détails plus détaillés pour les fonctionnalités de protection contre les menaces configurées. </span><span class="sxs-lookup"><span data-stu-id="1c8f9-288">The **Tech view** is similar to the **Funnel** view, providing more granular details for the configured threat protections features.</span></span> <span data-ttu-id="1c8f9-289">À partir du graphique, vous pouvez voir comment les messages sont classés aux différentes étapes de la protection contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-289">From the chart, you can see how messages are categorized at the different stages of threat protection.</span></span>

<span data-ttu-id="1c8f9-290">Si vous cliquez sur **l’onglet Affichage** Technique, par défaut, cet affichage contient un graphique et une table de données configurés avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-290">If you click the **Tech view** tab, by default, this view contains a chart and a data table that's configured with the following filters:</span></span>

- <span data-ttu-id="1c8f9-291">**Date**: 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-291">**Date**: The last 7 days.</span></span>

- <span data-ttu-id="1c8f9-292">**Direction**:</span><span class="sxs-lookup"><span data-stu-id="1c8f9-292">**Direction**:</span></span>

  - <span data-ttu-id="1c8f9-293">**Entrant**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-293">**Inbound**</span></span>
  - <span data-ttu-id="1c8f9-294">**Sortant**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-294">**Outbound**</span></span>
  - <span data-ttu-id="1c8f9-295">**Intra-organisation**: ce nombre est pour les messages au sein d’un client, c’est-à-dire</span><span class="sxs-lookup"><span data-stu-id="1c8f9-295">**Intra-org**: this count is for messages within a tenant i.e</span></span> <span data-ttu-id="1c8f9-296">sender abc@domain.com sends to recipient xyz@domain.com (counted separately from Inbound and Outbound)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-296">sender abc@domain.com sends to recipient xyz@domain.com (counted separately from Inbound and Outbound)</span></span>

<span data-ttu-id="1c8f9-297">L’affichage agrégé et l’affichage de table de données autorisent 90 jours de filtrage.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-297">The aggregate view and data table view allow for 90 days of filtering.</span></span>

<span data-ttu-id="1c8f9-298">Si vous cliquez **sur Filtre,** vous pouvez filtrer le graphique et la table de données.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-298">If you click **Filter**, you can filter both the chart and the data table.</span></span>

<span data-ttu-id="1c8f9-299">Ce graphique présente les messages organisés dans les catégories suivantes :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-299">This chart shows messages organized into the following categories:</span></span>

- <span data-ttu-id="1c8f9-300">**Nombre total de messages électroniques**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-300">**Total email**</span></span>
- <span data-ttu-id="1c8f9-301">**Edge autoriser** et **edge filtré**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-301">**Edge allow** and **Edge filtered**</span></span>
- <span data-ttu-id="1c8f9-302">**Règles de transport d’autoriser** et **de transport filtrées** (règles de flux de messagerie)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-302">**Transport rule allow** and **Transport rule filtered** (mail flow rules)</span></span>
- <span data-ttu-id="1c8f9-303">**Pas de programmes** **malveillants, Safe détection des pièces jointes** <sup>\*</sup> et détection du moteur **anti-programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-303">**Not malware**, **Safe Attachments detection**<sup>\*</sup>, and **Anti-malware engine detection**</span></span>
- <span data-ttu-id="1c8f9-304">**Pas de hameçonnage,**  **d’échec DMARC,** de détection d’emprunt d’identité, de détection d’usurpation <sup>\*</sup> d’identité et de détection **d’hameçonnage** </span><span class="sxs-lookup"><span data-stu-id="1c8f9-304">**Not phish**, **DMARC failure**, **Impersonation detection**<sup>\*</sup>, **Spoof detection**, and **Phish detection**</span></span>
- <span data-ttu-id="1c8f9-305">**Aucune détection avec détection de détonation d’URL** et **de détonation d’URL**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="1c8f9-305">**No detection with URL detonation** and **URL detonation detection**<sup>\*</sup></span></span>
- <span data-ttu-id="1c8f9-306">**Pas de courrier indésirable** et  **de courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-306">**Not spam** and  **Spam**</span></span>
- <span data-ttu-id="1c8f9-307">**E-mail** non malveillant, **détection Safe liens et** <sup>\*</sup> **ZAP**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-307">**Non-malicious email**, **Safe Links detection**<sup>\*</sup>, and **ZAP**</span></span>

<span data-ttu-id="1c8f9-308"><sup>\*</sup>Defender for Office 365</span><span class="sxs-lookup"><span data-stu-id="1c8f9-308"><sup>\*</sup> Defender for Office 365</span></span>

<span data-ttu-id="1c8f9-309">Lorsque vous pointez sur une catégorie dans le graphique, vous pouvez voir le nombre de messages dans cette catégorie.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-309">When you hover over a category in the chart, you can see the number of messages in that category.</span></span>

<span data-ttu-id="1c8f9-310">La table de données contient les informations suivantes, indiquées dans l’ordre décroit de date :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-310">The data table contains the following information, shown in descending date order:</span></span>

- <span data-ttu-id="1c8f9-311">**Date**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-311">**Date**</span></span>
- <span data-ttu-id="1c8f9-312">**Nombre total de messages électroniques**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-312">**Total email**</span></span>
- <span data-ttu-id="1c8f9-313">**Edge filtré**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-313">**Edge filtered**</span></span>
- <span data-ttu-id="1c8f9-314">**Messages de règle**: messages filtrés en raison de règles de flux de messagerie (également appelées règles de transport).</span><span class="sxs-lookup"><span data-stu-id="1c8f9-314">**Rule messages**: Messages filtered due to  mail flow rules (also known as transport rules).</span></span>
- <span data-ttu-id="1c8f9-315">**Moteur anti-programme malveillant,** **Safe pièces jointes** <sup>\*</sup> :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-315">**Anti-malware engine**, **Safe Attachments**<sup>\*</sup>:</span></span>
- <span data-ttu-id="1c8f9-316">**DMARC, emprunt d’identité,** <sup>\*</sup> **usurpation** d’identité, **hameçonnage filtré**:</span><span class="sxs-lookup"><span data-stu-id="1c8f9-316">**DMARC, impersonation**<sup>\*</sup>, **spoof**, **phish filtered**:</span></span>
  - <span data-ttu-id="1c8f9-317">**DMARC**: messages filtrés en raison de l’échec de la vérification de l’authentification DMARC.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-317">**DMARC**: Messages filtered due to the message failing its DMARC authentication check.</span></span>
- <span data-ttu-id="1c8f9-318">**Détection de détonation d’URL**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="1c8f9-318">**URL detonation detection**<sup>\*</sup></span></span>
- <span data-ttu-id="1c8f9-319">**Filtrage anti-courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-319">**Anti-spam filtered**</span></span>
- <span data-ttu-id="1c8f9-320">**ZAP supprimé**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-320">**ZAP removed**</span></span>
- <span data-ttu-id="1c8f9-321">**Détection par liens Safe de détection**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="1c8f9-321">**Detection by Safe Links**<sup>\*</sup></span></span>

<span data-ttu-id="1c8f9-322"><sup>\*</sup>Defender for Office 365</span><span class="sxs-lookup"><span data-stu-id="1c8f9-322"><sup>\*</sup> Defender for Office 365</span></span>

<span data-ttu-id="1c8f9-323">Si vous sélectionnez une ligne dans la table de données, une répartition supplémentaire du nombre de messages électroniques est affichée dans le volant.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-323">If you select a row in the data table, a further breakdown of the email counts are shown in the flyout.</span></span>

#### <a name="export-from-tech-view"></a><span data-ttu-id="1c8f9-324">Exporter à partir d’un affichage tech</span><span class="sxs-lookup"><span data-stu-id="1c8f9-324">Export from Tech view</span></span>

<span data-ttu-id="1c8f9-325">En cliquant **sur Exporter,** sous **Options,** vous pouvez sélectionner l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-325">On clicking **Export**, under **Options** you can select one of the following values:</span></span>

- <span data-ttu-id="1c8f9-326">**Résumé (avec des données pour les 90 derniers jours au maximum)**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-326">**Summary (with data for last 90 days at most)**</span></span>
- <span data-ttu-id="1c8f9-327">**Détails (avec des données pour les 30 derniers jours au maximum)**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-327">**Details (with data for last 30 days at most)**</span></span>

<span data-ttu-id="1c8f9-328">Sous **Date**, choisissez une plage, puis cliquez sur **Appliquer**.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-328">Under **Date**, choose a range, and then click **Apply**.</span></span> <span data-ttu-id="1c8f9-329">Les données des filtres actuels sont exportées vers un .csv de données.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-329">Data for the current filters will be exported to a .csv file.</span></span>

<span data-ttu-id="1c8f9-330">Chaque fichier .csv exporté est limité à 150 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-330">Each exported .csv file is limited to 150,000 rows.</span></span> <span data-ttu-id="1c8f9-331">Si les données contiennent plus de 150 000 lignes, plusieurs .csv fichiers seront créés.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-331">If the data contains more than 150,000 rows, then multiple .csv files will be created.</span></span>

![Affichage technique dans le rapport d’état du flux de messagerie](../../media/mail-flow-status-report-tech-view.png)

## <a name="malware-detections-report"></a><span data-ttu-id="1c8f9-333">Rapport sur les détections de programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="1c8f9-333">Malware detections report</span></span>

<span data-ttu-id="1c8f9-334">Le rapport détections de programmes malveillants affiche des informations sur les détections de programmes malveillants dans les messages électroniques entrants et sortants (programmes **malveillants détectés** par Exchange Online Protection ou EOP).</span><span class="sxs-lookup"><span data-stu-id="1c8f9-334">The **Malware detections report** report shows information about malware detections in incoming and outgoing email messages (malware detected by Exchange Online Protection or EOP).</span></span> <span data-ttu-id="1c8f9-335">Pour plus d’informations sur la protection contre les programmes malveillants dans EOP, voir Protection contre les programmes [malveillants dans EOP.](anti-malware-protection.md)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-335">For more information about malware protection in EOP, see [Anti-malware protection in EOP](anti-malware-protection.md).</span></span>

<span data-ttu-id="1c8f9-336">Le filtre d’affichage agrégé autorise 90 jours, tandis que le filtre de tableau détails ne le permet que sur 10 jours.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-336">The aggregate view filter allows for 90 days, while the details table filter only allows for 10 days.</span></span>

<span data-ttu-id="1c8f9-337">Pour afficher le rapport dans le portail  Microsoft 365 Defender, consultez la & collaboration de rapports e-mail \>  \> **& rapports de collaboration.**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-337">To view the report in the Microsoft 365 Defender portal, go to **Reports** \> **Email & collaboration** \> **Email & collaboration reports**.</span></span> <span data-ttu-id="1c8f9-338">Sur **les programmes malveillants détectés dans le courrier** électronique, cliquez sur Afficher les **détails.**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-338">On **Malware detected in email**, click **View details**.</span></span> <span data-ttu-id="1c8f9-339">Pour aller directement dans le rapport, ouvrez <https://security.microsoft.com/reports/MalwareDetections> .</span><span class="sxs-lookup"><span data-stu-id="1c8f9-339">To go directly to the report, open <https://security.microsoft.com/reports/MalwareDetections>.</span></span>

![Détections de programmes malveillants dans le widget de messagerie sur la page rapports de collaboration & messagerie](../../media/malware-detections-widget.png)

<span data-ttu-id="1c8f9-341">Après avoir **cliqué sur Afficher les détails,** vous pouvez filtrer à la fois le graphique et le tableau détails en cliquant sur **Filtrer** et en sélectionnant :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-341">After you click **View details**, you can filter both the chart and the details table by clicking **Filter** and selecting:</span></span>

- <span data-ttu-id="1c8f9-342">**Date**: **Date de début et** date de **fin**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-342">**Date**: **Start date** and **End date**</span></span>
- <span data-ttu-id="1c8f9-343">**Direction**: **trafic entrant** et **sortant**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-343">**Direction**: **Inbound** and **Outbound**</span></span>

![Affichage du rapport dans le rapport de détection des programmes malveillants dans le rapport de courrier électronique](../../media/malware-detections-report-view.png)

<span data-ttu-id="1c8f9-345">Dans le tableau de détails sous le graphique, vous pouvez voir les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-345">In the details table below the graph, you can see the following details:</span></span>

- <span data-ttu-id="1c8f9-346">**Date**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-346">**Date**</span></span>
- <span data-ttu-id="1c8f9-347">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-347">**Sender address**</span></span>
- <span data-ttu-id="1c8f9-348">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-348">**Recipient address**</span></span>
- <span data-ttu-id="1c8f9-349">**ID de message**: disponible dans le champ d’en-tête **Message-ID** dans l’en-tête du message et doit être unique.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-349">**Message ID**: Available in the **Message-ID** header field in the message header and should be unique.</span></span> <span data-ttu-id="1c8f9-350">Un exemple de valeur est `<08f1e0f6806a47b4ac103961109ae6ef@server.domain>` (notez les crochets).</span><span class="sxs-lookup"><span data-stu-id="1c8f9-350">An example value is `<08f1e0f6806a47b4ac103961109ae6ef@server.domain>` (note the angle brackets).</span></span>
- <span data-ttu-id="1c8f9-351">**Subject**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-351">**Subject**</span></span>
- <span data-ttu-id="1c8f9-352">**Filename**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-352">**Filename**</span></span>
- <span data-ttu-id="1c8f9-353">**Nom du programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-353">**Malware name**</span></span>

## <a name="mail-latency-report"></a><span data-ttu-id="1c8f9-354">Rapport de latence du courrier</span><span class="sxs-lookup"><span data-stu-id="1c8f9-354">Mail latency report</span></span>

<span data-ttu-id="1c8f9-355">Le **rapport de latence de messagerie** dans Defender pour Office 365 contient des informations sur la remise et la latence de détonation du courrier au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-355">The **Mail latency report** in Defender for Office 365 contains information on the mail delivery and detonation latency experienced within your organization.</span></span> <span data-ttu-id="1c8f9-356">Pour plus d’informations, voir [Rapport de latence de messagerie.](view-reports-for-mdo.md#mail-latency-report)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-356">For more information, see [Mail latency report](view-reports-for-mdo.md#mail-latency-report).</span></span>

## <a name="spam-detections-report"></a><span data-ttu-id="1c8f9-357">Rapport sur la détection des courriers indésirables</span><span class="sxs-lookup"><span data-stu-id="1c8f9-357">Spam detections report</span></span>

> [!NOTE]
> <span data-ttu-id="1c8f9-358">Le **rapport de détection du** courrier indésirable sera publié le 30 juin 2021.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-358">The **Spam detections report** will go away on June 30, 2021.</span></span> <span data-ttu-id="1c8f9-359">Les mêmes informations sont disponibles dans le rapport d’état [de la protection contre les menaces.](#threat-protection-status-report)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-359">The same information is available in the [Threat protection status report](#threat-protection-status-report).</span></span>

## <a name="spoof-detections-report"></a><span data-ttu-id="1c8f9-360">Rapport sur les détections d’usurpation d’usurpation</span><span class="sxs-lookup"><span data-stu-id="1c8f9-360">Spoof detections report</span></span>

> [!NOTE]
> <span data-ttu-id="1c8f9-361">Le rapport sur les détections d’usurpation d’usurpation d’informations amélioré, tel que décrit dans cet article, est disponible en prévisualisation, peut faire l’objet de changements et n’est pas disponible dans toutes les organisations.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-361">The improved Spoof detections report as described in this article is in Preview, is subject to change, and is not available in all organizations.</span></span> <span data-ttu-id="1c8f9-362">L’ancienne version du rapport affiche uniquement les messages **de bonne qualité** et les courriers **indésirables**.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-362">The older version of the report shows only **Good mail** and **Caught as spam**.</span></span>

<span data-ttu-id="1c8f9-363">Le **rapport sur les détections d’usurpation d’informations** affiche des informations sur les messages qui ont été bloqués ou autorisés en raison de l’usurpation d’informations.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-363">The **Spoof detections** report shows information about messages that were blocked or allowed due to spoofing.</span></span> <span data-ttu-id="1c8f9-364">Pour plus d’informations sur l’usurpation d’adresse, consultez la protection contre l’usurpation [d’adresse dans EOP.](anti-spoofing-protection.md)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-364">For more information about spoofing, see [Anti-spoofing protection in EOP](anti-spoofing-protection.md).</span></span>

<span data-ttu-id="1c8f9-365">L’affichage agrégé du rapport autorise 45 jours de filtrage, tandis que l’affichage détaillé ne permet que dix jours <sup>\*</sup> de filtrage.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-365">The aggregate view of the report allows for 45 days of filtering<sup>\*</sup>, while the detail view only allows for ten days of filtering.</span></span>

<span data-ttu-id="1c8f9-366"><sup>\*</sup> Au final, vous pourrez utiliser jusqu’à 90 jours de filtrage.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-366"><sup>\*</sup> Eventually, you'll be able to use up to 90 days of filtering.</span></span>

<span data-ttu-id="1c8f9-367">Pour afficher le rapport dans le portail  Microsoft 365 Defender, consultez la & collaboration de rapports e-mail \>  \> **& rapports de collaboration.**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-367">To view the report in the Microsoft 365 Defender portal, go to **Reports** \> **Email & collaboration** \> **Email & collaboration reports**.</span></span> <span data-ttu-id="1c8f9-368">Sur **les détections d’usurpation** d’informations, cliquez **sur Afficher les détails.**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-368">On **Spoof detections**, click **View details**.</span></span> <span data-ttu-id="1c8f9-369">Pour aller directement dans le rapport, ouvrez <https://security.microsoft.com/reports/SpoofMailReportV2> .</span><span class="sxs-lookup"><span data-stu-id="1c8f9-369">To go directly to the report, open <https://security.microsoft.com/reports/SpoofMailReportV2>.</span></span>

![Widget de détections d’usurpation d'& dans la page Rapports de collaboration & courrier électronique](../../media/spoof-detections-widget.png)

<span data-ttu-id="1c8f9-371">Lorsque vous pointez sur un jour (point de données) dans le graphique, vous pouvez voir combien de messages usurpés ont été détectés et pourquoi.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-371">When you hover over a day (data point) in the chart, you can see how many spoofed messages were detected and why.</span></span>

<span data-ttu-id="1c8f9-372">Après avoir cliqué sur Afficher les **détails,** vous pouvez  filtrer à la fois le graphique et le tableau détails en cliquant sur Filtrer et en sélectionnant une ou plusieurs des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-372">After you click **View details**, you can filter both the chart and the details table by clicking **Filter** and selecting one or more of the following values:</span></span>

- <span data-ttu-id="1c8f9-373">**Date**: **Date de début et** date de **fin**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-373">**Date**: **Start date** and **End date**</span></span>
- <span data-ttu-id="1c8f9-374">**Résultat**:</span><span class="sxs-lookup"><span data-stu-id="1c8f9-374">**Result**:</span></span>
  - <span data-ttu-id="1c8f9-375">**Pass**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-375">**Pass**</span></span>
  - <span data-ttu-id="1c8f9-376">**Échec**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-376">**Fail**</span></span>
  - <span data-ttu-id="1c8f9-377">**SoftPass**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-377">**SoftPass**</span></span>
  - <span data-ttu-id="1c8f9-378">**Aucune**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-378">**None**</span></span>
  - <span data-ttu-id="1c8f9-379">**Other**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-379">**Other**</span></span>
- <span data-ttu-id="1c8f9-380">**Type d’usurpation :** **interne** et **externe**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-380">**Spoof type**: **Internal** and **External**</span></span>

![Page de rapport de courrier électronique usurpant l’Microsoft 365 Defender](../../media/spoof-detections-report-page.png)

<span data-ttu-id="1c8f9-382">Dans le tableau sous le graphique, vous pouvez voir les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-382">In the table below the graph, you can see the following details:</span></span>

- <span data-ttu-id="1c8f9-383">**Date**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-383">**Date**</span></span>
- <span data-ttu-id="1c8f9-384">**Utilisateur usurpé**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-384">**Spoofed user**</span></span>
- <span data-ttu-id="1c8f9-385">**Infrastructure d’envoi**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-385">**Sending infrastructure**</span></span>
- <span data-ttu-id="1c8f9-386">**Type d’usurpation**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-386">**Spoof type**</span></span>
- <span data-ttu-id="1c8f9-387">**Résultat**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-387">**Result**</span></span>
- <span data-ttu-id="1c8f9-388">**Code de résultat**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-388">**Result code**</span></span>
- <span data-ttu-id="1c8f9-389">**SPF**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-389">**SPF**</span></span>
- <span data-ttu-id="1c8f9-390">**DKIM**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-390">**DKIM**</span></span>
- <span data-ttu-id="1c8f9-391">**DMARC**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-391">**DMARC**</span></span>
- <span data-ttu-id="1c8f9-392">**Nombre de messages**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-392">**Message count**</span></span>

<span data-ttu-id="1c8f9-393">Pour plus d’informations sur les codes de résultats d’authentification composite, consultez les [en-têtes de message anti-courrier](anti-spam-message-headers.md)indésirable Microsoft 365 .</span><span class="sxs-lookup"><span data-stu-id="1c8f9-393">For more information about composite authentication result codes, see [Anti-spam message headers in Microsoft 365](anti-spam-message-headers.md).</span></span>

## <a name="threat-protection-status-report"></a><span data-ttu-id="1c8f9-394">Rapport sur l’état de la protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="1c8f9-394">Threat protection status report</span></span>

<span data-ttu-id="1c8f9-395">Le **rapport d’état de la protection** contre les menaces est disponible dans EOP et Defender pour Office 365 ; toutefois, les rapports contiennent des données différentes.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-395">The **Threat protection status** report is available in both EOP and Defender for Office 365; however, the reports contain different data.</span></span> <span data-ttu-id="1c8f9-396">Par exemple, les clients EOP peuvent afficher des informations sur les programmes malveillants détectés dans le courrier électronique, mais pas sur les fichiers [malveillants détectés](mdo-for-spo-odb-and-teams.md)par les pièces jointes Safe pour SharePoint, OneDrive et Microsoft Teams .</span><span class="sxs-lookup"><span data-stu-id="1c8f9-396">For example, EOP customers can view information about malware detected in email, but not information about malicious files detected by [Safe Attachments for SharePoint, OneDrive, and Microsoft Teams](mdo-for-spo-odb-and-teams.md).</span></span>

<span data-ttu-id="1c8f9-397">Le rapport fournit le nombre de messages électroniques avec du contenu malveillant, tels que des fichiers ou des adresses de site web (URL) qui ont été bloqués par le moteur anti-programme malveillant, la purge automatique d’heure zéro [(ZAP)](zero-hour-auto-purge.md)et Defender pour des fonctionnalités de Office 365 telles que les liens [Safe,](safe-links.md)les pièces [jointes Safe](safe-attachments.md)et les fonctionnalités de protection contre l’emprunt d’identité dans les stratégies [anti-hameçonnage.](set-up-anti-phishing-policies.md#exclusive-settings-in-anti-phishing-policies-in-microsoft-defender-for-office-365)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-397">The report provides the count of email messages with malicious content, such as files or website addresses (URLs) that were blocked by the anti-malware engine, [zero-hour auto purge (ZAP)](zero-hour-auto-purge.md), and Defender for Office 365 features like [Safe Links](safe-links.md), [Safe Attachments](safe-attachments.md), and [impersonation protection features in anti-phishing policies](set-up-anti-phishing-policies.md#exclusive-settings-in-anti-phishing-policies-in-microsoft-defender-for-office-365).</span></span> <span data-ttu-id="1c8f9-398">Vous pouvez utiliser ces informations pour identifier les tendances ou déterminer si des stratégies d’organisation doivent être ajuster.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-398">You can use this information to identify trends or determine whether organization policies need adjustment.</span></span>

<span data-ttu-id="1c8f9-399">**Remarque**: il est important de comprendre que si un message est envoyé à cinq destinataires, nous le compterons comme cinq messages différents et pas un seul message.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-399">**Note**: It's important to understand that if a message is sent to five recipients we count it as five different messages and not one message.</span></span>

<span data-ttu-id="1c8f9-400">Pour afficher le rapport dans le portail  Microsoft 365 Defender, consultez la & collaboration de rapports e-mail \>  \> **& rapports de collaboration.**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-400">To view the report in the Microsoft 365 Defender portal, go to **Reports** \> **Email & collaboration** \> **Email & collaboration reports**.</span></span> <span data-ttu-id="1c8f9-401">Sur **l’état de la protection contre les** menaces, cliquez sur Afficher les **détails.**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-401">On **Threat protection status**, click **View details**.</span></span> <span data-ttu-id="1c8f9-402">Pour aller directement dans le rapport, ouvrez l’une des URL suivantes :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-402">To go directly to the report, open one of the following URLs:</span></span>

- <span data-ttu-id="1c8f9-403">Defender pour Office 365 :<https://security.microsoft.com/reports/TPSAggregateReportATP></span><span class="sxs-lookup"><span data-stu-id="1c8f9-403">Defender for Office 365: <https://security.microsoft.com/reports/TPSAggregateReportATP></span></span>
- <span data-ttu-id="1c8f9-404">EOP : <https://security.microsoft.com/reports/TPSAggregateReport></span><span class="sxs-lookup"><span data-stu-id="1c8f9-404">EOP: <https://security.microsoft.com/reports/TPSAggregateReport></span></span>

![Widget d’état de la protection contre les menaces dans la page Rapports de collaboration & courrier électronique](../../media/threat-protection-status-report-widget.png)

<span data-ttu-id="1c8f9-406">Par défaut, après avoir cliqué sur **Afficher les détails,** le graphique affiche les données des 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-406">By default, after you click **View details**, the chart shows data for the past 7 days.</span></span> <span data-ttu-id="1c8f9-407">Si vous cliquez **sur Filtre,** vous pouvez sélectionner une plage de dates de 90 jours (les abonnements d’essai peuvent être limités à 30 jours).</span><span class="sxs-lookup"><span data-stu-id="1c8f9-407">If you click **Filter**, you can select a 90 day date range (trial subscriptions might be limited to 30 days).</span></span> <span data-ttu-id="1c8f9-408">Le tableau de détails autorise le filtrage pendant 30 jours.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-408">The details table allows filtering for 30 days.</span></span>

<span data-ttu-id="1c8f9-409">Les vues disponibles sont décrites dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-409">The available views are described in the following sections.</span></span>

### <a name="view-data-by-overview"></a><span data-ttu-id="1c8f9-410">Afficher les données par vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="1c8f9-410">View data by Overview</span></span>

![Vue d’ensemble dans le rapport d’état de la protection contre les menaces](../../media/threat-protection-status-report-overview-view.png)

<span data-ttu-id="1c8f9-412">Dans **l’affichage Des données par vue d’ensemble,** les informations de détection suivantes sont affichées dans le graphique :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-412">In the **View data by Overview** view, the following detection information is shown in the chart:</span></span>

- <span data-ttu-id="1c8f9-413">**Programme malveillant de messagerie**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-413">**Email malware**</span></span>
- <span data-ttu-id="1c8f9-414">**Hameçonnage par e-mail**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-414">**Email phish**</span></span>
- <span data-ttu-id="1c8f9-415">**Programme malveillant de contenu**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-415">**Content malware**</span></span>

<span data-ttu-id="1c8f9-416">Aucun tableau de détails n’est disponible sous le graphique.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-416">No details table is available below the chart.</span></span>

<span data-ttu-id="1c8f9-417">Si vous cliquez **sur Filtre,** les filtres suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-417">If you click **Filter**, the following filters are available:</span></span>

- <span data-ttu-id="1c8f9-418">**Date**: **Date de début et** date de **fin**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-418">**Date**: **Start date** and **End date**</span></span>
- <span data-ttu-id="1c8f9-419">**Détection :** programme **malveillant de messagerie,** **hameçonnage de messagerie** ou programme malveillant de **contenu**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-419">**Detection**: **Email malware**, **Email phish**, or **Content malware**</span></span>
- <span data-ttu-id="1c8f9-420">**Protégé par**: **MDO** (Defender for Office 365) ou **EOP**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-420">**Protected by**: **MDO** (Defender for Office 365) or **EOP**</span></span>
- <span data-ttu-id="1c8f9-421">**Balise**: filtrer les résultats par utilisateurs ou groupes pour lesquels la balise utilisateur spécifiée a été appliquée (y compris les comptes de priorité).</span><span class="sxs-lookup"><span data-stu-id="1c8f9-421">**Tag**: Filter the results by users or groups that have had the specified user tag applied (including priority accounts).</span></span> <span data-ttu-id="1c8f9-422">Pour plus d’informations sur les balises utilisateur, voir [Balises utilisateur.](user-tags.md)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-422">For more information about user tags, see [User tags](user-tags.md).</span></span>
- <span data-ttu-id="1c8f9-423">**Direction**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-423">**Direction**</span></span>
- <span data-ttu-id="1c8f9-424">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-424">**Domain**</span></span>
- <span data-ttu-id="1c8f9-425">**Type de stratégie**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-425">**Policy type**</span></span>

<span data-ttu-id="1c8f9-426">Lorsque vous avez terminé la configuration des filtres, cliquez sur **Appliquer,** **Annuler** ou **Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-426">When you're finished configuring the filters, click **Apply**, **Cancel**, or **Clear filters**.</span></span>

### <a name="view-data-by-email--phish-and-chart-breakdown-by-detection-technology"></a><span data-ttu-id="1c8f9-427">Afficher les données par hameçonnage de messagerie \> électronique et répartition des graphiques par technologie de détection</span><span class="sxs-lookup"><span data-stu-id="1c8f9-427">View data by Email \> Phish and Chart breakdown by Detection Technology</span></span>

![Affichage de la technologie de détection pour le courrier d’hameçonnage dans le rapport d’état de la protection contre les menaces](../../media/threat-protection-status-report-phishing-detection-tech-view.png)

<span data-ttu-id="1c8f9-429">Dans **l’affichage \> des données par hameçonnage par courrier électronique** et répartition **du** graphique par technologie de détection, les informations suivantes sont affichées dans le graphique :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-429">In the **View data by Email \> Phish** and **Chart breakdown by Detection Technology** view, the following information is shown in the chart:</span></span>

- <span data-ttu-id="1c8f9-430">**Réputation malveillante d’URL**: réputation d’URL malveillante générée à partir de <sup>\*</sup> Defender pour Office 365 détonations dans d’autres Microsoft 365 clients.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-430">**URL malicious reputation**<sup>\*</sup>: Malicious URL reputation generated from Defender for Office 365 detonations in other Microsoft 365 customers.</span></span>
- <span data-ttu-id="1c8f9-431">**Filtre avancé :** signaux de hameçonnage basés sur l’apprentissage automatique.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-431">**Advanced filter**: Phishing signals based on machine learning.</span></span>
- <span data-ttu-id="1c8f9-432">**Filtre général :** signaux de hameçonnage basés sur des règles d’analyste.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-432">**General filter**: Phishing signals based on analyst rules.</span></span>
- <span data-ttu-id="1c8f9-433">**Usurpation d’adresse intra-organisation**: l’expéditeur tente d’usurper le domaine du destinataire.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-433">**Spoof intra-org**: Sender is trying to spoof the recipient domain.</span></span>
- <span data-ttu-id="1c8f9-434">**Usurpation d’un domaine externe**: l’expéditeur tente d’usurper un autre domaine.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-434">**Spoof external domain**: Sender is trying to spoof some other domain.</span></span>
- <span data-ttu-id="1c8f9-435">**Usurpation d’identité DMARC**: échec de l’authentification DMARC sur les messages.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-435">**Spoof DMARC**: DMARC authentication failure on messages.</span></span>
- <span data-ttu-id="1c8f9-436">**Marque d’emprunt d’identité**: emprunt d’identité de marques connues basées sur des expéditeurs.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-436">**Impersonation brand**: Impersonation of well-known brands based on senders.</span></span>
- <span data-ttu-id="1c8f9-437">**Détection d’analyse mixte**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-437">**Mixed analysis detection**</span></span>
- <span data-ttu-id="1c8f9-438">**Réputation des fichiers**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-438">**File reputation**</span></span>
- <span data-ttu-id="1c8f9-439">**Correspondance de l’empreinte**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-439">**Fingerprint matching**</span></span>
- <span data-ttu-id="1c8f9-440">**Réputation de détonation d’URL**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="1c8f9-440">**URL detonation reputation**<sup>\*</sup></span></span>
- <span data-ttu-id="1c8f9-441">**Détonation d’URL**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="1c8f9-441">**URL detonation**<sup>\*</sup></span></span>
- <span data-ttu-id="1c8f9-442">**Utilisateur de l’emprunt d’identité**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="1c8f9-442">**Impersonation user**<sup>\*</sup></span></span>
- <span data-ttu-id="1c8f9-443">**Domaine d’emprunt d’identité**: emprunt d’identité des domaines que le client <sup>\*</sup> possède ou définit.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-443">**Impersonation domain**<sup>\*</sup>: Impersonation of domains that the customer owns or defines.</span></span>
- <span data-ttu-id="1c8f9-444">**Emprunt d’identité d’intelligence de** boîte aux lettres : emprunt d’identité des utilisateurs définis par l’administrateur ou appris par le biais de l’intelligence <sup>\*</sup> des boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-444">**Mailbox intelligence impersonation**<sup>\*</sup>: Impersonation of users defined by admin or learned through mailbox intelligence.</span></span>
- <span data-ttu-id="1c8f9-445">**Détonation de fichier**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="1c8f9-445">**File detonation**<sup>\*</sup></span></span>
- <span data-ttu-id="1c8f9-446">**Campagne**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="1c8f9-446">**Campaign**<sup>\*</sup></span></span>

<span data-ttu-id="1c8f9-447">Dans le tableau de détails sous le graphique, les informations suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-447">In the details table below the chart, the following information is available:</span></span>

- <span data-ttu-id="1c8f9-448">**Date**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-448">**Date**</span></span>
- <span data-ttu-id="1c8f9-449">**Subject**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-449">**Subject**</span></span>
- <span data-ttu-id="1c8f9-450">**Expéditeur**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-450">**Sender**</span></span>
- <span data-ttu-id="1c8f9-451">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-451">**Recipients**</span></span>
- <span data-ttu-id="1c8f9-452">**Détecté par**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-452">**Detected by**</span></span>
- <span data-ttu-id="1c8f9-453">**État de remise**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-453">**Delivery Status**</span></span>
- <span data-ttu-id="1c8f9-454">**Source de compromis**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-454">**Source of Compromise**</span></span>
- <span data-ttu-id="1c8f9-455">**Tags**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-455">**Tags**</span></span>

<span data-ttu-id="1c8f9-456">Si vous cliquez **sur Filtre,** les filtres suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-456">If you click **Filter**, the following filters are available:</span></span>

- <span data-ttu-id="1c8f9-457">**Date**: **Date de début et** date de **fin**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-457">**Date**: **Start date** and **End date**</span></span>
- <span data-ttu-id="1c8f9-458">**Détection**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-458">**Detection**</span></span>
- <span data-ttu-id="1c8f9-459">**Protégé par**: **MDO** (Defender for Office 365) ou **EOP**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-459">**Protected by**: **MDO** (Defender for Office 365) or **EOP**</span></span>
- <span data-ttu-id="1c8f9-460">**Direction**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-460">**Direction**</span></span>
- <span data-ttu-id="1c8f9-461">**Balise**: filtrer les résultats par utilisateurs ou groupes pour lesquels la balise utilisateur spécifiée a été appliquée (y compris les comptes de priorité).</span><span class="sxs-lookup"><span data-stu-id="1c8f9-461">**Tag**: Filter the results by users or groups that have had the specified user tag applied (including priority accounts).</span></span> <span data-ttu-id="1c8f9-462">Pour plus d’informations sur les balises utilisateur, voir [Balises utilisateur.](user-tags.md)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-462">For more information about user tags, see [User tags](user-tags.md).</span></span>
- <span data-ttu-id="1c8f9-463">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-463">**Domain**</span></span>
- <span data-ttu-id="1c8f9-464">**Type de stratégie**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-464">**Policy type**</span></span>
- <span data-ttu-id="1c8f9-465">**Nom de la stratégie** (tableau de détails uniquement)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-465">**Policy name** (details table only)</span></span>
- <span data-ttu-id="1c8f9-466">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-466">**Recipients**</span></span>

<span data-ttu-id="1c8f9-467">Lorsque vous avez terminé la configuration des filtres, cliquez sur **Appliquer,** **Annuler** ou **Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-467">When you're finished configuring the filters, click **Apply**, **Cancel**, or **Clear filters**.</span></span>

### <a name="view-data-by-email--malware-and-chart-breakdown-by-detection-technology"></a><span data-ttu-id="1c8f9-468">Afficher les données par programme malveillant et \> répartition des graphiques par technologie de détection</span><span class="sxs-lookup"><span data-stu-id="1c8f9-468">View data by Email \> Malware and Chart breakdown by Detection Technology</span></span>

![Affichage de la technologie de détection pour les programmes malveillants dans le rapport d’état de la protection contre les menaces](../../media/threat-protection-status-report-malware-detection-tech-view.png)

<span data-ttu-id="1c8f9-470">Dans **l’affichage \> des données par programme** malveillant par courrier électronique et **répartition des** graphiques par technologie de détection, les informations suivantes sont affichées dans le graphique :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-470">In the **View data by Email \> Malware** and **Chart breakdown by Detection Technology** view, the following information is shown in the chart:</span></span>

- <span data-ttu-id="1c8f9-471">**Détonation de fichier** <sup>\*</sup> : détection par Safe pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-471">**File detonation**<sup>\*</sup>: Detection by Safe Attachments.</span></span>
- <span data-ttu-id="1c8f9-472">**Réputation de détonation de fichier**: toutes les réputations de fichiers <sup>\*</sup> malveillants générées par Defender pour Office 365 détonations.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-472">**File detonation reputation**<sup>\*</sup>: All malicious file reputation generated by Defender for Office 365 detonations.</span></span>
- <span data-ttu-id="1c8f9-473">**Réputation des fichiers**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-473">**File reputation**</span></span>
- <span data-ttu-id="1c8f9-474">**Moteur anti-programme malveillant :** détection à partir de moteurs <sup>\*</sup> anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-474">**Anti-malware engine**<sup>\*</sup>: Detection from anti-malware engines.</span></span>
- <span data-ttu-id="1c8f9-475">Blocage du type de fichier de stratégie **anti-programme** malveillant : il s’adresse aux messages électroniques filtrés en raison du type de fichier malveillant identifié dans le message.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-475">**Anti-malware policy file type block**: These are email messages filtered out due to the type of malicious file identified in the message.</span></span>
- <span data-ttu-id="1c8f9-476">**Réputation d’URL malveillante**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-476">**URL malicious reputation**</span></span>
- <span data-ttu-id="1c8f9-477">**Détonation d’URL**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-477">**URL detonation**</span></span>
- <span data-ttu-id="1c8f9-478">**Réputation de détonation d’URL**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-478">**URL detonation reputation**</span></span>
- <span data-ttu-id="1c8f9-479">**Campagne**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-479">**Campaign**</span></span>

<span data-ttu-id="1c8f9-480">Dans le tableau de détails sous le graphique, les informations suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-480">In the details table below the chart, the following information is available:</span></span>

- <span data-ttu-id="1c8f9-481">**Date**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-481">**Date**</span></span>
- <span data-ttu-id="1c8f9-482">**Subject**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-482">**Subject**</span></span>
- <span data-ttu-id="1c8f9-483">**Expéditeur**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-483">**Sender**</span></span>
- <span data-ttu-id="1c8f9-484">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-484">**Recipients**</span></span>
- <span data-ttu-id="1c8f9-485">**Détecté par**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-485">**Detected by**</span></span>
- <span data-ttu-id="1c8f9-486">**État de remise**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-486">**Delivery Status**</span></span>
- <span data-ttu-id="1c8f9-487">**Source de compromis**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-487">**Source of Compromise**</span></span>
- <span data-ttu-id="1c8f9-488">**Tags**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-488">**Tags**</span></span>

<span data-ttu-id="1c8f9-489">Si vous cliquez **sur Filtre,** les filtres suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-489">If you click **Filter**, the following filters are available:</span></span>

- <span data-ttu-id="1c8f9-490">**Date**: **Date de début et** date de **fin**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-490">**Date**: **Start date** and **End date**</span></span>
- <span data-ttu-id="1c8f9-491">**Détection**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-491">**Detection**</span></span>
- <span data-ttu-id="1c8f9-492">**Protégé par**: **MDO** (Defender for Office 365) ou **EOP**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-492">**Protected by**: **MDO** (Defender for Office 365) or **EOP**</span></span>
- <span data-ttu-id="1c8f9-493">**Direction**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-493">**Direction**</span></span>
- <span data-ttu-id="1c8f9-494">**Balise**: filtrer les résultats par utilisateurs ou groupes pour lesquels la balise utilisateur spécifiée a été appliquée (y compris les comptes de priorité).</span><span class="sxs-lookup"><span data-stu-id="1c8f9-494">**Tag**: Filter the results by users or groups that have had the specified user tag applied (including priority accounts).</span></span> <span data-ttu-id="1c8f9-495">Pour plus d’informations sur les balises utilisateur, voir [Balises utilisateur.](user-tags.md)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-495">For more information about user tags, see [User tags](user-tags.md).</span></span>
- <span data-ttu-id="1c8f9-496">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-496">**Domain**</span></span>
- <span data-ttu-id="1c8f9-497">**Type de stratégie**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-497">**Policy type**</span></span>
- <span data-ttu-id="1c8f9-498">**Nom de la stratégie** (tableau de détails uniquement)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-498">**Policy name** (details table only)</span></span>
- <span data-ttu-id="1c8f9-499">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-499">**Recipients**</span></span>

<span data-ttu-id="1c8f9-500">Lorsque vous avez terminé la configuration des filtres, cliquez sur **Appliquer,** **Annuler** ou **Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-500">When you're finished configuring the filters, click **Apply**, **Cancel**, or **Clear filters**.</span></span>

### <a name="chart-breakdown-by-policy-type-and-view-data-by-email--phish-or-view-data-by-email--malware"></a><span data-ttu-id="1c8f9-501">Répartition des graphiques par type de stratégie et affichage des données par hameçonnage de messagerie ou affichage des données par programme malveillant \> de \> messagerie</span><span class="sxs-lookup"><span data-stu-id="1c8f9-501">Chart breakdown by Policy type and View data by Email \> Phish or View data by Email \> Malware</span></span>

![Affichage du type de stratégie pour les courriers électroniques de hameçonnage ou de programmes malveillants dans le rapport d’état de la protection contre les menaces](../../media/threat-protection-status-report-phishing-policy-type-view.png)

<span data-ttu-id="1c8f9-503">Dans la répartition **du graphique** par type de stratégie et l’affichage des données par hameçonnage de messagerie ou affichage des données par affichage des programmes malveillants de messagerie, les informations suivantes sont affichées dans les graphiques : **\>** **\>**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-503">In the **Chart breakdown by Policy type** and **View data by Email \> Phish** or **View data by Email \> Malware** views, the following information is shown in the charts:</span></span>

- <span data-ttu-id="1c8f9-504">**Anti-programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-504">**Anti-malware**</span></span>
- <span data-ttu-id="1c8f9-505">**Safe Pièces jointes**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="1c8f9-505">**Safe Attachments**<sup>\*</sup></span></span>
- <span data-ttu-id="1c8f9-506">**Anti-hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-506">**Anti-phish**</span></span>
- <span data-ttu-id="1c8f9-507">**Anti-courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-507">**Anti-spam**</span></span>
- <span data-ttu-id="1c8f9-508">**Règle de flux de messagerie** (également appelée règle de transport)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-508">**Mail flow rule** (also known as a transport rule)</span></span>
- <span data-ttu-id="1c8f9-509">**Autres**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-509">**Others**</span></span>

<span data-ttu-id="1c8f9-510">Dans le tableau de détails sous le graphique, les informations suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-510">In the details table below the chart, the following information is available:</span></span>

- <span data-ttu-id="1c8f9-511">**Date**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-511">**Date**</span></span>
- <span data-ttu-id="1c8f9-512">**Subject**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-512">**Subject**</span></span>
- <span data-ttu-id="1c8f9-513">**Expéditeur**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-513">**Sender**</span></span>
- <span data-ttu-id="1c8f9-514">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-514">**Recipients**</span></span>
- <span data-ttu-id="1c8f9-515">**Détecté par**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-515">**Detected by**</span></span>
- <span data-ttu-id="1c8f9-516">**État de remise**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-516">**Delivery Status**</span></span>
- <span data-ttu-id="1c8f9-517">**Source de compromis**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-517">**Source of Compromise**</span></span>
- <span data-ttu-id="1c8f9-518">**Tags**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-518">**Tags**</span></span>

<span data-ttu-id="1c8f9-519">Si vous cliquez **sur Filtre,** les filtres suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-519">If you click **Filter**, the following filters are available:</span></span>

- <span data-ttu-id="1c8f9-520">**Date**: **Date de début et** date de **fin**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-520">**Date**: **Start date** and **End date**</span></span>
- <span data-ttu-id="1c8f9-521">**Détection**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-521">**Detection**</span></span>
- <span data-ttu-id="1c8f9-522">**Protégé par**: **MDO** (Defender for Office 365) ou **EOP**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-522">**Protected by**: **MDO** (Defender for Office 365) or **EOP**</span></span>
- <span data-ttu-id="1c8f9-523">**Direction**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-523">**Direction**</span></span>
- <span data-ttu-id="1c8f9-524">**Balise**: filtrer les résultats par utilisateurs ou groupes pour lesquels la balise utilisateur spécifiée a été appliquée (y compris les comptes de priorité).</span><span class="sxs-lookup"><span data-stu-id="1c8f9-524">**Tag**: Filter the results by users or groups that have had the specified user tag applied (including priority accounts).</span></span> <span data-ttu-id="1c8f9-525">Pour plus d’informations sur les balises utilisateur, voir [Balises utilisateur.](user-tags.md)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-525">For more information about user tags, see [User tags](user-tags.md).</span></span>
- <span data-ttu-id="1c8f9-526">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-526">**Domain**</span></span>
- <span data-ttu-id="1c8f9-527">**Type de stratégie**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-527">**Policy type**</span></span>
- <span data-ttu-id="1c8f9-528">**Nom de la stratégie** (tableau de détails uniquement)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-528">**Policy name** (details table only)</span></span>
- <span data-ttu-id="1c8f9-529">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-529">**Recipients**</span></span>

<span data-ttu-id="1c8f9-530">Lorsque vous avez terminé la configuration des filtres, cliquez sur **Appliquer,** **Annuler** ou **Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-530">When you're finished configuring the filters, click **Apply**, **Cancel**, or **Clear filters**.</span></span>

### <a name="chart-breakdown-by-delivery-status-and-view-data-by-email--phish-or-view-data-by-email--malware"></a><span data-ttu-id="1c8f9-531">Répartition des graphiques par état de remise et affichage des données par hameçonnage de messagerie ou affichage des données par programme malveillant \> de \> messagerie</span><span class="sxs-lookup"><span data-stu-id="1c8f9-531">Chart breakdown by Delivery status and View data by Email \> Phish or View data by Email \> Malware</span></span>

![Affichage de l’état de remise du courrier électronique de hameçonnage et des programmes malveillants dans le rapport d’état de la protection contre les menaces](../../media/threat-protection-status-report-phishing-delivery-status-view.png)

<span data-ttu-id="1c8f9-533">Dans la répartition **du graphique** par état de remise et affichage des données par hameçonnage de messagerie ou affichage des données par affichage des programmes malveillants de messagerie, les informations suivantes sont affichées dans les graphiques : **\>** **\>**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-533">In the **Chart breakdown by Delivery status** and **View data by Email \> Phish** or **View data by Email \> Malware** views, the following information is shown in the charts:</span></span>

- <span data-ttu-id="1c8f9-534">**Boîte aux lettres hébergée : Boîte de réception**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-534">**Hosted mailbox: Inbox**</span></span>
- <span data-ttu-id="1c8f9-535">**Boîte aux lettres hébergée : courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-535">**Hosted mailbox: Junk**</span></span>
- <span data-ttu-id="1c8f9-536">**Boîte aux lettres hébergée : dossier personnalisé**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-536">**Hosted mailbox: Custom folder**</span></span>
- <span data-ttu-id="1c8f9-537">**Boîte aux lettres hébergée : éléments supprimés**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-537">**Hosted mailbox: Deleted items**</span></span>
- <span data-ttu-id="1c8f9-538">**Forwarded**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-538">**Forwarded**</span></span>
- <span data-ttu-id="1c8f9-539">**Serveur local : remis**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-539">**On-premises server: Delivered**</span></span>
- <span data-ttu-id="1c8f9-540">**Mise en quarantaine**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-540">**Quarantine**</span></span>
- <span data-ttu-id="1c8f9-541">**Échec de remise**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-541">**Delivery failed**</span></span>
- <span data-ttu-id="1c8f9-542">**Dropped**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-542">**Dropped**</span></span>

<span data-ttu-id="1c8f9-543">Dans le tableau de détails sous le graphique, les informations suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-543">In the details table below the chart, the following information is available:</span></span>

- <span data-ttu-id="1c8f9-544">**Date**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-544">**Date**</span></span>
- <span data-ttu-id="1c8f9-545">**Subject**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-545">**Subject**</span></span>
- <span data-ttu-id="1c8f9-546">**Expéditeur**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-546">**Sender**</span></span>
- <span data-ttu-id="1c8f9-547">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-547">**Recipients**</span></span>
- <span data-ttu-id="1c8f9-548">**Détecté par**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-548">**Detected by**</span></span>
- <span data-ttu-id="1c8f9-549">**État de remise**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-549">**Delivery Status**</span></span>
- <span data-ttu-id="1c8f9-550">**Source de compromis**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-550">**Source of Compromise**</span></span>
- <span data-ttu-id="1c8f9-551">**Tags**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-551">**Tags**</span></span>

<span data-ttu-id="1c8f9-552">Si vous cliquez **sur Filtre,** les filtres suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-552">If you click **Filter**, the following filters are available:</span></span>

- <span data-ttu-id="1c8f9-553">**Date**: **Date de début et** date de **fin**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-553">**Date**: **Start date** and **End date**</span></span>
- <span data-ttu-id="1c8f9-554">**Détection**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-554">**Detection**</span></span>
- <span data-ttu-id="1c8f9-555">**Protégé par**: **MDO** (Defender for Office 365) ou **EOP**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-555">**Protected by**: **MDO** (Defender for Office 365) or **EOP**</span></span>
- <span data-ttu-id="1c8f9-556">**Direction**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-556">**Direction**</span></span>
- <span data-ttu-id="1c8f9-557">**Balise**: filtrer les résultats par utilisateurs ou groupes pour lesquels la balise utilisateur spécifiée a été appliquée (y compris les comptes de priorité).</span><span class="sxs-lookup"><span data-stu-id="1c8f9-557">**Tag**: Filter the results by users or groups that have had the specified user tag applied (including priority accounts).</span></span> <span data-ttu-id="1c8f9-558">Pour plus d’informations sur les balises utilisateur, voir [Balises utilisateur.](user-tags.md)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-558">For more information about user tags, see [User tags](user-tags.md).</span></span>
- <span data-ttu-id="1c8f9-559">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-559">**Domain**</span></span>
- <span data-ttu-id="1c8f9-560">**Type de stratégie**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-560">**Policy type**</span></span>
- <span data-ttu-id="1c8f9-561">**Nom de la stratégie** (tableau de détails uniquement)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-561">**Policy name** (details table only)</span></span>
- <span data-ttu-id="1c8f9-562">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-562">**Recipients**</span></span>

<span data-ttu-id="1c8f9-563">Lorsque vous avez terminé la configuration des filtres, cliquez sur **Appliquer,** **Annuler** ou **Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-563">When you're finished configuring the filters, click **Apply**, **Cancel**, or **Clear filters**.</span></span>

### <a name="view-data-by-content--malware"></a><span data-ttu-id="1c8f9-564">Afficher les données par programme malveillant de \> contenu</span><span class="sxs-lookup"><span data-stu-id="1c8f9-564">View data by Content \> Malware</span></span>

![Affichage des programmes malveillants de contenu dans le rapport d’état de la protection contre les menaces](../../media/threat-protection-status-report-content-malware-view.png)

<span data-ttu-id="1c8f9-566">Dans la **vue \> Afficher les données par programme** malveillant de contenu, les informations suivantes sont affichées dans le graphique de Microsoft Defender pour Office 365 organisations :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-566">In the **View data by Content \> Malware** view, the following information is shown in the chart for Microsoft Defender for Office 365 organizations:</span></span>

- <span data-ttu-id="1c8f9-567">**Moteur anti-programme** malveillant : fichiers malveillants détectés dans Sharepoint, OneDrive et Microsoft Teams par la détection de virus intégrée dans [Microsoft 365](virus-detection-in-spo.md).</span><span class="sxs-lookup"><span data-stu-id="1c8f9-567">**Anti-malware engine**: Malicious files detected in Sharepoint, OneDrive, and Microsoft Teams by the [built-in virus detection in Microsoft 365](virus-detection-in-spo.md).</span></span>
- <span data-ttu-id="1c8f9-568">**Détonation de fichiers**: fichiers malveillants détectés par Safe pièces jointes pour [SharePoint, OneDrive et Microsoft Teams](mdo-for-spo-odb-and-teams.md).</span><span class="sxs-lookup"><span data-stu-id="1c8f9-568">**File detonation**: Malicious files detected by [Safe Attachments for SharePoint, OneDrive, and Microsoft Teams](mdo-for-spo-odb-and-teams.md).</span></span>

<span data-ttu-id="1c8f9-569">Dans le tableau de détails sous le graphique, les informations suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-569">In the details table below the chart, the following information is available:</span></span>

- <span data-ttu-id="1c8f9-570">**Date**: **Date de début et** date de **fin**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-570">**Date**: **Start date** and **End date**</span></span>
- <span data-ttu-id="1c8f9-571">**Emplacement**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-571">**Location**</span></span>
- <span data-ttu-id="1c8f9-572">**Détecté par**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-572">**Detected by**</span></span>
- <span data-ttu-id="1c8f9-573">**Nom du programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-573">**Malware name**</span></span>

<span data-ttu-id="1c8f9-574">Si vous cliquez **sur Filtre,** les filtres suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-574">If you click **Filter**, the following filters are available:</span></span>

- <span data-ttu-id="1c8f9-575">**Date**: **Date de début et** date de **fin**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-575">**Date**: **Start date** and **End date**</span></span>
- <span data-ttu-id="1c8f9-576">**Détection**: **moteur anti-programme malveillant** ou **détonation de fichiers**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-576">**Detection**: **Anti-malware engine** or **File detonation**</span></span>

<span data-ttu-id="1c8f9-577">Lorsque vous avez terminé la configuration des filtres, cliquez sur **Appliquer,** **Annuler** ou **Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-577">When you're finished configuring the filters, click **Apply**, **Cancel**, or **Clear filters**.</span></span>

### <a name="view-data-by-system-override"></a><span data-ttu-id="1c8f9-578">Afficher les données par remplacement du système</span><span class="sxs-lookup"><span data-stu-id="1c8f9-578">View data by System override</span></span>

![Affichage des remplacements de messages dans le rapport d’état de la protection contre les menaces](../../media/threat-protection-status-report-message-override-view.png)

<span data-ttu-id="1c8f9-580">Dans **l’affichage d’affichage** des données par remplacement du système, les informations de motif de remplacement suivantes sont affichées dans le graphique :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-580">In the **View data by System override** view, the following override reason information is shown in the chart:</span></span>

- <span data-ttu-id="1c8f9-581">**Ignorer l’local**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-581">**On-premises skip**</span></span>
- <span data-ttu-id="1c8f9-582">**Ip allow**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-582">**IP allow**</span></span>
- <span data-ttu-id="1c8f9-583">**Exchange de transport de messagerie** (règle de flux de messagerie)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-583">**Exchange mail transport rule** (mail flow rule)</span></span>
- <span data-ttu-id="1c8f9-584">**Expéditeurs autorisés par l’organisation**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-584">**Organization allowed senders**</span></span>
- <span data-ttu-id="1c8f9-585">**Domaines autorisés par l’organisation**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-585">**Organization allowed domains**</span></span>
- <span data-ttu-id="1c8f9-586">**ZAP non activé**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-586">**ZAP not enabled**</span></span>
- <span data-ttu-id="1c8f9-587">**Dossier Courrier indésirable non activé**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-587">**Junk Mail folder not enabled**</span></span>
- <span data-ttu-id="1c8f9-588">**Expéditeur Safe utilisateur**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-588">**User Safe Sender**</span></span>
- <span data-ttu-id="1c8f9-589">**Domaine Safe utilisateur**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-589">**User Safe Domain**</span></span>

<span data-ttu-id="1c8f9-590">Dans le tableau de détails sous le graphique, les informations suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-590">In the details table below the chart, the following information is available:</span></span>

- <span data-ttu-id="1c8f9-591">**Date**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-591">**Date**</span></span>
- <span data-ttu-id="1c8f9-592">**Subject**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-592">**Subject**</span></span>
- <span data-ttu-id="1c8f9-593">**Expéditeur**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-593">**Sender**</span></span>
- <span data-ttu-id="1c8f9-594">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-594">**Recipients**</span></span>
- <span data-ttu-id="1c8f9-595">**Détecté par**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-595">**Detected by**</span></span>
- <span data-ttu-id="1c8f9-596">**État de remise**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-596">**Delivery Status**</span></span>
- <span data-ttu-id="1c8f9-597">**Source de compromis**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-597">**Source of Compromise**</span></span>
- <span data-ttu-id="1c8f9-598">**Tags**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-598">**Tags**</span></span>

<span data-ttu-id="1c8f9-599">Si vous cliquez **sur Filtre,** les filtres suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-599">If you click **Filter**, the following filters are available:</span></span>

- <span data-ttu-id="1c8f9-600">**Date**: **Date de début et** date de **fin**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-600">**Date**: **Start date** and **End date**</span></span>
- <span data-ttu-id="1c8f9-601">**Détection**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-601">**Detection**</span></span>
- <span data-ttu-id="1c8f9-602">**Protégé par**: **MDO** (Defender for Office 365) ou **EOP**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-602">**Protected by**: **MDO** (Defender for Office 365) or **EOP**</span></span>
- <span data-ttu-id="1c8f9-603">**Direction**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-603">**Direction**</span></span>
- <span data-ttu-id="1c8f9-604">**Balise**: filtrer les résultats par utilisateurs ou groupes pour lesquels la balise utilisateur spécifiée a été appliquée (y compris les comptes de priorité).</span><span class="sxs-lookup"><span data-stu-id="1c8f9-604">**Tag**: Filter the results by users or groups that have had the specified user tag applied (including priority accounts).</span></span> <span data-ttu-id="1c8f9-605">Pour plus d’informations sur les balises utilisateur, voir [Balises utilisateur.](user-tags.md)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-605">For more information about user tags, see [User tags](user-tags.md).</span></span>
- <span data-ttu-id="1c8f9-606">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-606">**Domain**</span></span>
- <span data-ttu-id="1c8f9-607">**Type de stratégie**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-607">**Policy type**</span></span>
- <span data-ttu-id="1c8f9-608">**Nom de la stratégie** (tableau de détails uniquement)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-608">**Policy name** (details table only)</span></span>
- <span data-ttu-id="1c8f9-609">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-609">**Recipients**</span></span>

<span data-ttu-id="1c8f9-610">Lorsque vous avez terminé la configuration des filtres, cliquez sur **Appliquer,** **Annuler** ou **Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-610">When you're finished configuring the filters, click **Apply**, **Cancel**, or **Clear filters**.</span></span>

<span data-ttu-id="1c8f9-611"><sup>\*</sup>Defender pour Office 365 uniquement</span><span class="sxs-lookup"><span data-stu-id="1c8f9-611"><sup>\*</sup> Defender for Office 365 only</span></span>

## <a name="top-malware-report"></a><span data-ttu-id="1c8f9-612">Principaux rapports sur les programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="1c8f9-612">Top malware report</span></span>

<span data-ttu-id="1c8f9-613">Le **rapport des principaux programmes** malveillants présente les différents types de programmes malveillants détectés par la protection [anti-programme malveillant dans EOP.](anti-malware-protection.md)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-613">The **Top malware** report shows the various kinds of malware that was detected by [anti-malware protection in EOP](anti-malware-protection.md).</span></span>

<span data-ttu-id="1c8f9-614">Pour afficher le rapport dans le portail  Microsoft 365 Defender, consultez la & collaboration de rapports e-mail \>  \> **& rapports de collaboration.**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-614">To view the report in the Microsoft 365 Defender portal, go to **Reports** \> **Email & collaboration** \> **Email & collaboration reports**.</span></span> <span data-ttu-id="1c8f9-615">Sur **les programmes malveillants** en haut, cliquez **sur Afficher les détails.**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-615">On **Top malware**, click **View details**.</span></span> <span data-ttu-id="1c8f9-616">Pour aller directement dans le rapport, ouvrez <https://security.microsoft.com/reports/TopMalware> .</span><span class="sxs-lookup"><span data-stu-id="1c8f9-616">To go directly to the report, open <https://security.microsoft.com/reports/TopMalware>.</span></span>

![Widget de programmes malveillants de premier niveau sur la page rapports de collaboration & messagerie](../../media/top-malware-report-widget.png)

<span data-ttu-id="1c8f9-618">Lorsque vous pointez sur une souris dans le graphique en secteurs, vous pouvez voir le nom d’un type de programme malveillant et le nombre de messages détectés comme ayant ce programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-618">When you hover over a wedge in the pie chart, you can see the name of a kind of malware and how many messages were detected as having that malware.</span></span>

<span data-ttu-id="1c8f9-619">Une fois que vous avez cliqué sur Afficher les **détails,** une version plus grande du graphique en secteurs s’affiche sur la page de rapport. Le tableau de détails sous le graphique présente les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-619">After you click **View details**, a larger version of the pie chart is displayed on the report page.The details table below the chart shows the following information:</span></span>

- <span data-ttu-id="1c8f9-620">**Principaux programmes malveillants**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-620">**Top malware**</span></span>
- <span data-ttu-id="1c8f9-621">**Count**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-621">**Count**</span></span>

<span data-ttu-id="1c8f9-622">Si vous cliquez **sur Filtre,** vous pouvez spécifier une plage de dates avec la **date de** début et la date **de fin.**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-622">If you click **Filter**, you can specify a date range with **Start date** and **End date**.</span></span>

![Affichage du rapport sur les programmes malveillants le plus haut](../../media/top-malware-report-view.png)

## <a name="url-threat-protection-report"></a><span data-ttu-id="1c8f9-624">Rapport sur la protection contre les menaces d’URL</span><span class="sxs-lookup"><span data-stu-id="1c8f9-624">URL threat protection report</span></span>

<span data-ttu-id="1c8f9-625">Le **rapport sur la protection contre les menaces d’URL** est disponible dans Microsoft Defender Office 365.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-625">The **URL threat protection report** is available in Microsoft Defender for Office 365.</span></span> <span data-ttu-id="1c8f9-626">Pour plus d’informations, voir le rapport sur la [protection contre les menaces d’URL.](view-reports-for-mdo.md#url-threat-protection-report)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-626">For more information, see [URL threat protection report](view-reports-for-mdo.md#url-threat-protection-report).</span></span>

## <a name="user-reported-messages-report"></a><span data-ttu-id="1c8f9-627">Rapport des messages signalés par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="1c8f9-627">User reported messages report</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1c8f9-628">Pour que le rapport des **messages** signalés par l’utilisateur fonctionne correctement, l’enregistrement **d’audit** doit être Microsoft 365 votre environnement.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-628">In order for the **User reported messages** report to work correctly, **audit logging must be turned on** for your Microsoft 365 environment.</span></span> <span data-ttu-id="1c8f9-629">Cette tâche est généralement effectuée par une personne dont le rôle Journaux d’audit est Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-629">This is typically done by someone who has the Audit Logs role assigned in Exchange Online.</span></span> <span data-ttu-id="1c8f9-630">Pour plus d’informations, [voir Turn Microsoft 365 audit log search on or off](../../compliance/turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="1c8f9-630">For more information, see [Turn Microsoft 365 audit log search on or off](../../compliance/turn-audit-log-search-on-or-off.md).</span></span>

<span data-ttu-id="1c8f9-631">Le rapport des **messages** signalés par l’utilisateur affiche des informations sur les messages électroniques que les utilisateurs ont signalés comme courrier indésirable, tentatives d’hameçonnage ou courrier de qualité à l’aide du module complémentaire Signaler un [message](enable-the-report-message-add-in.md) ou signaler le hameçonnage. [](enable-the-report-phish-add-in.md)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-631">The **User reported messages** report shows information about email messages that users have reported as junk, phishing attempts, or good mail by using the [Report Message add-in](enable-the-report-message-add-in.md) or the [Report Phishing add-in](enable-the-report-phish-add-in.md).</span></span>

<span data-ttu-id="1c8f9-632">Pour afficher le rapport dans le portail  Microsoft 365 Defender, consultez l’adresse e-mail rapports & collaboration e-mail & rapports de collaboration Messages signalés par \>  \>  \> **l’utilisateur.**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-632">To view the report in the Microsoft 365 Defender portal, go to **Reports** \> **Email & collaboration** \>**Email & collaboration reports** \> **User reported messages**.</span></span> <span data-ttu-id="1c8f9-633">Dans **les messages signalés par l’utilisateur,** cliquez **sur Afficher les détails.**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-633">On **User reported messages**, click **View details**.</span></span> <span data-ttu-id="1c8f9-634">Pour aller directement dans le rapport, ouvrez <https://security.microsoft.com/reports/userSubmissionReport> .</span><span class="sxs-lookup"><span data-stu-id="1c8f9-634">To go directly to the report, open <https://security.microsoft.com/reports/userSubmissionReport>.</span></span> <span data-ttu-id="1c8f9-635">Pour aller aux [soumissions d’administrateur dans le portail Microsoft 365 Defender,](admin-submission.md)cliquez **sur Go to Submissions**.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-635">To go to [admin submissions in the Microsoft 365 Defender portal](admin-submission.md), click **Go to Submissions**.</span></span>

![Widget de messages signalés par l’utilisateur sur la page rapports de collaboration & courrier électronique](../../media/user-reported-messages-widget.png)

<span data-ttu-id="1c8f9-637">Après avoir cliqué sur Afficher les **détails,** vous pouvez  filtrer à la fois le graphique et le tableau de détails en cliquant sur Filtrer et en sélectionnant une ou plusieurs des valeurs suivantes dans le volant qui s’affiche :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-637">After you click **View details**, you can filter both the chart and the details table by clicking **Filter** and selecting one or more of the following values in the flyout that appears:</span></span>

- <span data-ttu-id="1c8f9-638">**Date signalée :** **heure de début** et heure de **fin**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-638">**Date reported**: **Start time** and **End time**</span></span>
- <span data-ttu-id="1c8f9-639">**Auteur du rapport**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-639">**Reported by**</span></span>
- <span data-ttu-id="1c8f9-640">**Sujet de l’e-mail**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-640">**Email subject**</span></span>
- <span data-ttu-id="1c8f9-641">**ID de message signalé**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-641">**Message reported ID**</span></span>
- <span data-ttu-id="1c8f9-642">**ID de message réseau**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-642">**Network Message ID**</span></span>
- <span data-ttu-id="1c8f9-643">**Sender**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-643">**Sender**</span></span>
- <span data-ttu-id="1c8f9-644">**Raison signalée**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-644">**Reported reason**</span></span>
  - <span data-ttu-id="1c8f9-645">**Non indésirable**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-645">**Not junk**</span></span>
  - <span data-ttu-id="1c8f9-646">**Hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-646">**Phish**</span></span>
  - <span data-ttu-id="1c8f9-647">**Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-647">**Spam**</span></span>
- <span data-ttu-id="1c8f9-648">**Simulation de hameçonnage**: **Oui** ou **Non**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-648">**Phish simulation**: **Yes** or **No**</span></span>

<span data-ttu-id="1c8f9-649">Lorsque vous avez terminé la configuration des filtres, cliquez sur **Appliquer,** **Annuler** ou **Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-649">When you're finished configuring the filters, click **Apply**, **Cancel**, or **Clear filters**.</span></span>

<span data-ttu-id="1c8f9-650">Pour grouper les entrées, cliquez sur **Grouper** et sélectionnez l’une des valeurs suivantes dans la liste suivante :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-650">To group the entries, click **Group** and select one of the following values from the drop down list:</span></span>

- <span data-ttu-id="1c8f9-651">**Aucune**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-651">**None**</span></span>
- <span data-ttu-id="1c8f9-652">**Raison**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-652">**Reason**</span></span>
- <span data-ttu-id="1c8f9-653">**Sender**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-653">**Sender**</span></span>
- <span data-ttu-id="1c8f9-654">**Auteur du rapport**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-654">**Reported by**</span></span>
- <span data-ttu-id="1c8f9-655">**Résultat rescan**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-655">**Rescan result**</span></span>
- <span data-ttu-id="1c8f9-656">**Simulation de hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-656">**Phish simulation**</span></span>

![Rapport des messages signalés par l’utilisateur](../../media/user-reported-messages-report.png)

<span data-ttu-id="1c8f9-658">Dans le tableau sous le graphique, vous pouvez voir les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-658">In the table below the graph, you can see the following details:</span></span>

- <span data-ttu-id="1c8f9-659">**Sujet de l’e-mail**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-659">**Email subject**</span></span>
- <span data-ttu-id="1c8f9-660">**Auteur du rapport**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-660">**Reported by**</span></span>
- <span data-ttu-id="1c8f9-661">**Date de rapport**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-661">**Date reported**</span></span>
- <span data-ttu-id="1c8f9-662">**Sender**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-662">**Sender**</span></span>
- <span data-ttu-id="1c8f9-663">**Raison signalée**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-663">**Reported reason**</span></span>
- <span data-ttu-id="1c8f9-664">**Résultat rescan**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-664">**Rescan result**</span></span>
- <span data-ttu-id="1c8f9-665">**Tags**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-665">**Tags**</span></span>

<span data-ttu-id="1c8f9-666">Pour envoyer un message à Microsoft pour analyse, sélectionnez l’entrée du message dans le tableau, cliquez sur Envoyer à **Microsoft** pour analyse, puis sélectionnez l’une des valeurs suivantes dans la liste liste suivante :</span><span class="sxs-lookup"><span data-stu-id="1c8f9-666">To submit a message to Microsoft for analysis, select the message entry from the table, click **Submit to Microsoft for analysis** and then select one of the following values from the drop down list:</span></span>

- <span data-ttu-id="1c8f9-667">**Signaler propre**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-667">**Report clean**</span></span>
- <span data-ttu-id="1c8f9-668">**Signaler le hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-668">**Report phishing**</span></span>
- <span data-ttu-id="1c8f9-669">**Signaler un programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-669">**Report malware**</span></span>
- <span data-ttu-id="1c8f9-670">**Signaler le courrier indésirable**'</span><span class="sxs-lookup"><span data-stu-id="1c8f9-670">**Report spam**'</span></span>
- <span data-ttu-id="1c8f9-671">**Examen du déclencheur** (Defender for Office 365)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-671">**Trigger investigation** (Defender for Office 365)</span></span>

## <a name="what-permissions-are-needed-to-view-these-reports"></a><span data-ttu-id="1c8f9-672">Quelles autorisations sont nécessaires pour afficher ces rapports ?</span><span class="sxs-lookup"><span data-stu-id="1c8f9-672">What permissions are needed to view these reports?</span></span>

<span data-ttu-id="1c8f9-673">Pour afficher et utiliser les rapports décrits dans cet article, vous devez être membre de l’un des groupes de rôles suivants dans le portail Microsoft 365 Defender:</span><span class="sxs-lookup"><span data-stu-id="1c8f9-673">In order to view and use the reports described in this article, you need to be a member of one of the following role groups in the Microsoft 365 Defender portal:</span></span>

- <span data-ttu-id="1c8f9-674">**Gestion de l'organisation**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-674">**Organization Management**</span></span>
- <span data-ttu-id="1c8f9-675">**Administrateur de sécurité**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-675">**Security Administrator**</span></span>
- <span data-ttu-id="1c8f9-676">**Lecteur sécurité**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-676">**Security Reader**</span></span>
- <span data-ttu-id="1c8f9-677">**Lecteur global**</span><span class="sxs-lookup"><span data-stu-id="1c8f9-677">**Global Reader**</span></span>

<span data-ttu-id="1c8f9-678">Pour plus d’informations, [voir Autorisations dans le portail Microsoft 365 Defender.](permissions-in-the-security-and-compliance-center.md)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-678">For more information, see [Permissions in the Microsoft 365 Defender portal](permissions-in-the-security-and-compliance-center.md).</span></span>

<span data-ttu-id="1c8f9-679">**Remarque**: l’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux  utilisateurs les autorisations requises dans le portail Microsoft 365 Defender et les autorisations pour d’autres fonctionnalités dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-679">**Note**: Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions in the Microsoft 365 Defender portal _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="1c8f9-680">Pour plus d’informations, consultez la rubrique [À propos des rôles d’administrateur](../../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1c8f9-680">For more information, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>

## <a name="what-if-the-reports-arent-showing-data"></a><span data-ttu-id="1c8f9-681">Que se passe-t-il si les rapports n’affichent pas de données ?</span><span class="sxs-lookup"><span data-stu-id="1c8f9-681">What if the reports aren't showing data?</span></span>

<span data-ttu-id="1c8f9-682">Si vous ne voyez pas de données dans vos rapports, vérifiez que vos stratégies sont correctement définies.</span><span class="sxs-lookup"><span data-stu-id="1c8f9-682">If you are not seeing data in your reports, double-check that your policies are set up correctly.</span></span> <span data-ttu-id="1c8f9-683">Pour en savoir plus, [consultez La protection contre les menaces.](protect-against-threats.md)</span><span class="sxs-lookup"><span data-stu-id="1c8f9-683">To learn more, see [Protect against threats](protect-against-threats.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c8f9-684">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c8f9-684">Related topics</span></span>

[<span data-ttu-id="1c8f9-685">Protection contre le courrier indésirable et les programmes malveillants dans EOP</span><span class="sxs-lookup"><span data-stu-id="1c8f9-685">Anti-spam and anti-malware protection in EOP</span></span>](anti-spam-and-anti-malware-protection.md)

[<span data-ttu-id="1c8f9-686">Rapports intelligents et informations sur le portail Microsoft 365 Defender web</span><span class="sxs-lookup"><span data-stu-id="1c8f9-686">Smart reports and insights in the Microsoft 365 Defender portal</span></span>](reports-and-insights-in-security-and-compliance.md)

[<span data-ttu-id="1c8f9-687">Afficher les rapports de flux de messagerie dans le portail Microsoft 365 Defender messagerie</span><span class="sxs-lookup"><span data-stu-id="1c8f9-687">View mail flow reports in the Microsoft 365 Defender portal</span></span>](view-mail-flow-reports.md)

[<span data-ttu-id="1c8f9-688">Afficher des rapports pour Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="1c8f9-688">View reports for Defender for Office 365</span></span>](view-reports-for-mdo.md)
