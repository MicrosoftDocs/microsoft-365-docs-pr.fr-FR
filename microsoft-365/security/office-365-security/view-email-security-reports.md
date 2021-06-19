---
title: Afficher les rapports sur la sécurité des e-mails
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
description: Les administrateurs peuvent découvrir comment rechercher et utiliser les rapports de sécurité de messagerie disponibles dans le portail Microsoft 365 Defender.
ms.custom: seo-marvel-apr2020
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: ad5a9f0d87902deb1985daebfa61cd733d22cbec
ms.sourcegitcommit: c70067b4ef9c6f8f04aca68c35bb5141857c4e4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "53029546"
---
# <a name="view-email-security-reports-in-the-microsoft-365-defender-portal"></a><span data-ttu-id="bc746-103">Afficher les rapports de sécurité du courrier électronique dans le portail Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="bc746-103">View email security reports in the Microsoft 365 Defender portal</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="bc746-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="bc746-104">**Applies to**</span></span>
- [<span data-ttu-id="bc746-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="bc746-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="bc746-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="bc746-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="bc746-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="bc746-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="bc746-108">De nombreux rapports sont disponibles sur le portail Microsoft 365 Defender pour vous aider à voir comment les fonctionnalités de sécurité du courrier électronique, telles que les fonctionnalités anti-courrier indésirable, anti-programme malveillant et de chiffrement dans <https://security.microsoft.com> Microsoft 365, protègent votre organisation.</span><span class="sxs-lookup"><span data-stu-id="bc746-108">A variety of reports are available in the Microsoft 365 Defender portal at <https://security.microsoft.com> to help you see how email security features, such as anti-spam, anti-malware, and encryption features in Microsoft 365 are protecting your organization.</span></span> <span data-ttu-id="bc746-109">Si vous avez les [autorisations](#what-permissions-are-needed-to-view-these-reports)nécessaires, vous pouvez afficher ces rapports dans  le portail Microsoft 365 Defender en allant dans Rapports e-mail & \> **collaboration** \> **e-mail & rapports de collaboration.**</span><span class="sxs-lookup"><span data-stu-id="bc746-109">If you have the [necessary permissions](#what-permissions-are-needed-to-view-these-reports), you can view these reports in the Microsoft 365 Defender portal by going to **Reports** \> **Email & collaboration** \> **Email & collaboration reports**.</span></span> <span data-ttu-id="bc746-110">Pour aller directement à la page **e-mail & rapports** de collaboration, ouvrez <https://security.microsoft.com/emailandcollabreport> .</span><span class="sxs-lookup"><span data-stu-id="bc746-110">To go directly to the **Email & collaboration reports** page, open <https://security.microsoft.com/emailandcollabreport>.</span></span>

![Page de & de collaboration par courrier électronique dans le portail Microsoft 365 Defender](../../media/email-collaboration-reports.png)

> [!NOTE]
>
> <span data-ttu-id="bc746-112">Certains rapports de la page rapports de collaboration & **courrier** électronique nécessitent Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="bc746-112">Some of the reports on the **Email & collaboration reports** page require Microsoft Defender for Office 365.</span></span> <span data-ttu-id="bc746-113">Pour plus d’informations sur ces rapports, voir les rapports View Defender pour Office 365 dans le portail [Microsoft 365 Defender.](view-reports-for-mdo.md)</span><span class="sxs-lookup"><span data-stu-id="bc746-113">For information about these reports, see [View Defender for Office 365 reports in the Microsoft 365 Defender portal](view-reports-for-mdo.md).</span></span>
>
> <span data-ttu-id="bc746-114">Les rapports liés au flux de messagerie sont désormais dans le Centre d’administration Exchange (EAC).</span><span class="sxs-lookup"><span data-stu-id="bc746-114">Reports that are related to mail flow are now in the Exchange admin center (EAC).</span></span> <span data-ttu-id="bc746-115">Pour plus d’informations sur ces rapports, voir Rapports de [flux de messagerie dans le nouveau Centre d’administration Exchange.](/exchange/monitoring/mail-flow-reports/mail-flow-reports)</span><span class="sxs-lookup"><span data-stu-id="bc746-115">For more information about these reports, see [Mail flow reports in the new Exchange admin center](/exchange/monitoring/mail-flow-reports/mail-flow-reports).</span></span>

## <a name="compromised-users-report"></a><span data-ttu-id="bc746-116">Rapport utilisateurs compromis</span><span class="sxs-lookup"><span data-stu-id="bc746-116">Compromised users report</span></span>

> [!NOTE]
> <span data-ttu-id="bc746-117">Ce rapport est disponible dans les organisations Microsoft 365 avec des boîtes aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="bc746-117">This report is available in Microsoft 365 organizations with Exchange Online mailboxes.</span></span> <span data-ttu-id="bc746-118">Il n’est pas disponible dans les organisations Exchange Online Protection (EOP) autonomes.</span><span class="sxs-lookup"><span data-stu-id="bc746-118">It's not available in standalone Exchange Online Protection (EOP) organizations.</span></span>

<span data-ttu-id="bc746-119">Le **rapport Utilisateurs** compromis indique le nombre de  comptes  d’utilisateurs marqués comme suspects ou restreints au cours des 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="bc746-119">The **Compromised users** report shows shows the number of user accounts that were marked as **Suspicious** or **Restricted** within the last 7 days.</span></span> <span data-ttu-id="bc746-120">Les comptes dans l’un de ces états sont problématiques, voire compromis.</span><span class="sxs-lookup"><span data-stu-id="bc746-120">Accounts in either of these states are problematic or even compromised.</span></span> <span data-ttu-id="bc746-121">Avec une utilisation fréquente, vous pouvez utiliser le rapport pour repérer des pics, voire des tendances, dans des comptes suspects ou restreints.</span><span class="sxs-lookup"><span data-stu-id="bc746-121">With frequent use, you can use the report to spot spikes, and even trends, in suspicious or restricted accounts.</span></span> <span data-ttu-id="bc746-122">Pour plus d’informations sur les utilisateurs compromis, voir [Répondre à un compte de messagerie compromis.](responding-to-a-compromised-email-account.md)</span><span class="sxs-lookup"><span data-stu-id="bc746-122">For more information about compromised users, see [Responding to a compromised email account](responding-to-a-compromised-email-account.md).</span></span>

![Widget Utilisateurs compromis sur la page rapports de collaboration & messagerie](../../media/compromised-users-report-widget.png)

<span data-ttu-id="bc746-124">L’affichage agrégé affiche les données des 90 derniers jours et l’affichage détail affiche les données des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="bc746-124">The aggregate view shows data for the last 90 days and the detail view shows data for the last 30 days.</span></span>

<span data-ttu-id="bc746-125">Pour afficher le rapport dans le portail Microsoft  365 Defender, consultez La boîte aux & collaboration de rapports e-mail \>  \> **& rapports de collaboration.**</span><span class="sxs-lookup"><span data-stu-id="bc746-125">To view the report in the Microsoft 365 Defender portal, go to **Reports** \> **Email & collaboration** \> **Email & collaboration reports**.</span></span> <span data-ttu-id="bc746-126">Dans la page **& de collaboration,** recherchez les utilisateurs **compromis,** puis cliquez sur Afficher **les détails.**</span><span class="sxs-lookup"><span data-stu-id="bc746-126">On the **Email & collaboration reports** page, find **Compromised users** and then click **View details**.</span></span> <span data-ttu-id="bc746-127">Pour aller directement dans le rapport, ouvrez <https://security.microsoft.com/reports/CompromisedUsers> .</span><span class="sxs-lookup"><span data-stu-id="bc746-127">To go directly to the report, open <https://security.microsoft.com/reports/CompromisedUsers>.</span></span>

<span data-ttu-id="bc746-128">Dans **la** page Utilisateurs compromis, vous pouvez filtrer le  graphique et le tableau de détails en cliquant sur Filtrer et en sélectionnant une ou plusieurs des valeurs suivantes dans le volant qui s’affiche :</span><span class="sxs-lookup"><span data-stu-id="bc746-128">On the **Compromised users** page, you can filter both the chart and the details table by clicking **Filter** and selecting one or more of the following values in the flyout that appears:</span></span>

- <span data-ttu-id="bc746-129">**Date (UTC)**: **date de début** et date de **fin.**</span><span class="sxs-lookup"><span data-stu-id="bc746-129">**Date (UTC)**: **Start date** and **End date**.</span></span>
- <span data-ttu-id="bc746-130">**Activité**:</span><span class="sxs-lookup"><span data-stu-id="bc746-130">**Activity**:</span></span>
  - <span data-ttu-id="bc746-131">**Suspect**: le compte d’utilisateur a envoyé des messages suspects et risque d’être limité à l’envoi de courriers électroniques.</span><span class="sxs-lookup"><span data-stu-id="bc746-131">**Suspicious**: The user account has sent suspicious email and is at risk of being restricted from sending email.</span></span>
  - <span data-ttu-id="bc746-132">**Restreint :** le compte d’utilisateur n’a pas pu envoyer de courrier électronique en raison de modèles hautement suspects.</span><span class="sxs-lookup"><span data-stu-id="bc746-132">**Restricted**: The user account has been restricted from sending email due to highly suspicious patterns.</span></span>

<span data-ttu-id="bc746-133">Lorsque vous avez terminé la configuration des filtres, cliquez sur **Appliquer,** **Annuler** ou **Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="bc746-133">When you're finished configuring the filters, click **Apply**, **Cancel**, or **Clear filters**.</span></span>

![Affichage du rapport dans le rapport Utilisateurs compromis](../../media/compromised-users-report-activity-view.png)

<span data-ttu-id="bc746-135">Dans le tableau de détails sous le graphique, vous pouvez voir les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="bc746-135">In the details table below the graph, you can see the following details:</span></span>

- <span data-ttu-id="bc746-136">**Heure de création**</span><span class="sxs-lookup"><span data-stu-id="bc746-136">**Creation time**</span></span>
- <span data-ttu-id="bc746-137">**ID d'utilisateur**</span><span class="sxs-lookup"><span data-stu-id="bc746-137">**User ID**</span></span>
- <span data-ttu-id="bc746-138">**Action**</span><span class="sxs-lookup"><span data-stu-id="bc746-138">**Action**</span></span>

## <a name="exchange-transport-rule-report"></a><span data-ttu-id="bc746-139">Rapport de règles de transport Exchange</span><span class="sxs-lookup"><span data-stu-id="bc746-139">Exchange transport rule report</span></span>

<span data-ttu-id="bc746-140">Le **rapport des règles** de transport Exchange indique l’effet des règles de flux de messagerie (également appelées règles de transport) sur les messages entrants et sortants dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="bc746-140">The **Exchange transport rule** report shows the effect of mail flow rules (also known as transport rules) on incoming and outgoing messages in your organization.</span></span>

<span data-ttu-id="bc746-141">Pour afficher le rapport dans le portail Microsoft  365 Defender, consultez La boîte aux & collaboration de rapports e-mail \>  \> **& rapports de collaboration.**</span><span class="sxs-lookup"><span data-stu-id="bc746-141">To view the report in the Microsoft 365 Defender portal, go to **Reports** \> **Email & collaboration** \> **Email & collaboration reports**.</span></span> <span data-ttu-id="bc746-142">Dans la page **Rapports de collaboration & courrier** électronique, recherchez la règle de transport **Exchange,** puis cliquez sur **Afficher les détails.**</span><span class="sxs-lookup"><span data-stu-id="bc746-142">On the **Email & collaboration reports** page, find **Exchange transport rule** and then click **View details**.</span></span> <span data-ttu-id="bc746-143">Pour aller directement dans le rapport, ouvrez <https://security.microsoft.com/reports/ETRRuleReport> .</span><span class="sxs-lookup"><span data-stu-id="bc746-143">To go directly to the report, open <https://security.microsoft.com/reports/ETRRuleReport>.</span></span>

![Widget de règles de transport Exchange dans la page rapports de collaboration & courrier électronique](../../media/transport-rule-report-widget.png)

<span data-ttu-id="bc746-145">Dans la page rapport des règles de **transport Exchange,** les graphiques et données disponibles sont décrits dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="bc746-145">On the **Exchange transport rule report** page, the available charts and data are described in the following sections.</span></span>

### <a name="chart-breakdown-by-direction"></a><span data-ttu-id="bc746-146">Répartition du graphique par direction</span><span class="sxs-lookup"><span data-stu-id="bc746-146">Chart breakdown by Direction</span></span>

![Affichage direction pour les règles de transport Exchange dans le rapport de règles de transport Exchange](../../media/transport-rule-report-etr-direction-view.png)

<span data-ttu-id="bc746-148">Si vous sélectionnez **répartition des graphiques par direction,** les graphiques suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="bc746-148">If you select **Chart breakdown by Direction**, the follow charts are available:</span></span>

- <span data-ttu-id="bc746-149">**Afficher les données par règles**  de transport Exchange : nombre de **messages** entrants et sortants affectés par les règles de flux de messagerie.</span><span class="sxs-lookup"><span data-stu-id="bc746-149">**View data by Exchange transport rules**: The number of **Inbound** and **Outbound** messages that were affected by mail flow rules.</span></span>
- <span data-ttu-id="bc746-150">Afficher les données par règles de  **transport Exchange DLP**: nombre de **messages** entrants et sortants affectés par les règles de flux de messagerie de protection contre la perte de données (DLP).</span><span class="sxs-lookup"><span data-stu-id="bc746-150">**View data by DLP Exchange transport rules**: The number of **Inbound** and **Outbound** messages that were affected by data loss prevention (DLP) mail flow rules.</span></span>

<span data-ttu-id="bc746-151">Les informations suivantes sont affichées dans le tableau de détails sous le graphique :</span><span class="sxs-lookup"><span data-stu-id="bc746-151">The following information is shown in the details table below the graph:</span></span>

- <span data-ttu-id="bc746-152">**Date**</span><span class="sxs-lookup"><span data-stu-id="bc746-152">**Date**</span></span>
- <span data-ttu-id="bc746-153">**Stratégie DLP** ( Afficher les données par les règles de **transport Exchange DLP** uniquement)</span><span class="sxs-lookup"><span data-stu-id="bc746-153">**DLP policy** (**View data by DLP Exchange transport rules** only)</span></span>
- <span data-ttu-id="bc746-154">**Règle de transport**</span><span class="sxs-lookup"><span data-stu-id="bc746-154">**Transport rule**</span></span>
- <span data-ttu-id="bc746-155">**Subject**</span><span class="sxs-lookup"><span data-stu-id="bc746-155">**Subject**</span></span>
- <span data-ttu-id="bc746-156">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="bc746-156">**Sender address**</span></span>
- <span data-ttu-id="bc746-157">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="bc746-157">**Recipient address**</span></span>
- <span data-ttu-id="bc746-158">**Gravité**</span><span class="sxs-lookup"><span data-stu-id="bc746-158">**Severity**</span></span>
- <span data-ttu-id="bc746-159">**Direction**</span><span class="sxs-lookup"><span data-stu-id="bc746-159">**Direction**</span></span>

<span data-ttu-id="bc746-160">Vous pouvez filtrer le graphique et le tableau de détails en cliquant sur **Filtrer** et en sélectionnant une ou plusieurs des valeurs suivantes dans le volant qui s’affiche :</span><span class="sxs-lookup"><span data-stu-id="bc746-160">You can filter both the chart and the details table by clicking **Filter** and selecting one or more of the following values in the flyout that appears:</span></span>

- <span data-ttu-id="bc746-161">**Date (UTC)** **Date de début et** date de **fin**</span><span class="sxs-lookup"><span data-stu-id="bc746-161">**Date (UTC)** **Start date** and **End date**</span></span>
- <span data-ttu-id="bc746-162">**Direction**: **sortant et** **entrant**</span><span class="sxs-lookup"><span data-stu-id="bc746-162">**Direction**: **Outbound** and **Inbound**</span></span>
- <span data-ttu-id="bc746-163">**Gravité :** **gravité élevée,** **gravité moyenne** et gravité **faible**</span><span class="sxs-lookup"><span data-stu-id="bc746-163">**Severity**: **High severity**, **Medium severity**, and **Low severity**</span></span>

<span data-ttu-id="bc746-164">Lorsque vous avez terminé la configuration des filtres, cliquez sur **Appliquer,** **Annuler** ou **Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="bc746-164">When you're finished configuring the filters, click **Apply**, **Cancel**, or **Clear filters**.</span></span>

### <a name="chart-breakdown-by-severity"></a><span data-ttu-id="bc746-165">Répartition du graphique par gravité</span><span class="sxs-lookup"><span data-stu-id="bc746-165">Chart breakdown by Severity</span></span>

![Affichage gravité des règles de transport Exchange dans le rapport des règles de transport Exchange](../../media/transport-rule-report-etr-severity-view.png)

<span data-ttu-id="bc746-167">Si vous sélectionnez **répartition des graphiques par gravité,** les graphiques suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="bc746-167">If you select **Chart breakdown by Severity**, the follow charts are available:</span></span>

- <span data-ttu-id="bc746-168">**Afficher les données par règles de transport Exchange**: nombre de messages **de** gravité **élevée,** moyenne et **faible.**</span><span class="sxs-lookup"><span data-stu-id="bc746-168">**View data by Exchange transport rules**: The number of **High severity**, **Medium severity**, and **Low severity** messages.</span></span> <span data-ttu-id="bc746-169">Vous définissez le niveau de gravité en tant qu’action dans la règle (**Auditez** cette règle avec le niveau de gravité _ou SetAuditSeverity_).</span><span class="sxs-lookup"><span data-stu-id="bc746-169">You set the severity level as an action in the rule (**Audit this rule with severity level** or _SetAuditSeverity_).</span></span> <span data-ttu-id="bc746-170">Pour plus d’informations, voir [Actions de règle de flux de messagerie dans Exchange Online.](/Exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions)</span><span class="sxs-lookup"><span data-stu-id="bc746-170">For more information, see [Mail flow rule actions in Exchange Online](/Exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions).</span></span>

- <span data-ttu-id="bc746-171">Afficher les données par règles de transport Exchange  **DLP**: nombre de **messages** de gravité **élevée,** moyenne et faible affectés par les règles de flux de messagerie DLP.</span><span class="sxs-lookup"><span data-stu-id="bc746-171">**View data by DLP Exchange transport rules**: The number of **High severity**, **Medium severity**, and **Low severity** messages that were affected by DLP mail flow rules.</span></span>

<span data-ttu-id="bc746-172">Les informations suivantes sont affichées dans le tableau de détails sous le graphique :</span><span class="sxs-lookup"><span data-stu-id="bc746-172">The following information is shown in the details table below the graph:</span></span>

- <span data-ttu-id="bc746-173">**Date**</span><span class="sxs-lookup"><span data-stu-id="bc746-173">**Date**</span></span>
- <span data-ttu-id="bc746-174">**Stratégie DLP** ( Afficher les données par les règles de **transport Exchange DLP** uniquement)</span><span class="sxs-lookup"><span data-stu-id="bc746-174">**DLP policy** (**View data by DLP Exchange transport rules** only)</span></span>
- <span data-ttu-id="bc746-175">**Règle de transport**</span><span class="sxs-lookup"><span data-stu-id="bc746-175">**Transport rule**</span></span>
- <span data-ttu-id="bc746-176">**Subject**</span><span class="sxs-lookup"><span data-stu-id="bc746-176">**Subject**</span></span>
- <span data-ttu-id="bc746-177">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="bc746-177">**Sender address**</span></span>
- <span data-ttu-id="bc746-178">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="bc746-178">**Recipient address**</span></span>
- <span data-ttu-id="bc746-179">**Gravité**</span><span class="sxs-lookup"><span data-stu-id="bc746-179">**Severity**</span></span>
- <span data-ttu-id="bc746-180">**Direction**</span><span class="sxs-lookup"><span data-stu-id="bc746-180">**Direction**</span></span>

<span data-ttu-id="bc746-181">Vous pouvez filtrer le graphique et le tableau de détails en cliquant sur **Filtrer** et en sélectionnant une ou plusieurs des valeurs suivantes dans le volant qui s’affiche :</span><span class="sxs-lookup"><span data-stu-id="bc746-181">You can filter both the chart and the details table by clicking **Filter** and selecting one or more of the following values in the flyout that appears:</span></span>

- <span data-ttu-id="bc746-182">**Date (UTC)** **Date de début et** date de **fin**</span><span class="sxs-lookup"><span data-stu-id="bc746-182">**Date (UTC)** **Start date** and **End date**</span></span>
- <span data-ttu-id="bc746-183">**Direction**: **sortant et** **entrant**</span><span class="sxs-lookup"><span data-stu-id="bc746-183">**Direction**: **Outbound** and **Inbound**</span></span>
- <span data-ttu-id="bc746-184">**Gravité :** **gravité élevée,** **gravité moyenne** et gravité **faible**</span><span class="sxs-lookup"><span data-stu-id="bc746-184">**Severity**: **High severity**, **Medium severity**, and **Low severity**</span></span>

<span data-ttu-id="bc746-185">Lorsque vous avez terminé la configuration des filtres, cliquez sur **Appliquer,** **Annuler** ou **Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="bc746-185">When you're finished configuring the filters, click **Apply**, **Cancel**, or **Clear filters**.</span></span>

## <a name="forwarding-report"></a><span data-ttu-id="bc746-186">Rapport de forwarding</span><span class="sxs-lookup"><span data-stu-id="bc746-186">Forwarding report</span></span>

> [!NOTE]
> <span data-ttu-id="bc746-187">Le **rapport de forwarding** est désormais disponible dans le EAC.</span><span class="sxs-lookup"><span data-stu-id="bc746-187">The **Forwarding report** is now available in the EAC.</span></span> <span data-ttu-id="bc746-188">Pour plus d’informations, [reportez-vous au](/exchange/monitoring/mail-flow-reports/mfr-auto-forwarded-messages-report)rapport des messages transmis automatiquement dans le nouveau EAC.</span><span class="sxs-lookup"><span data-stu-id="bc746-188">For more information, see [Auto forwarded messages report in the new EAC](/exchange/monitoring/mail-flow-reports/mfr-auto-forwarded-messages-report).</span></span>

## <a name="mailflow-status-report"></a><span data-ttu-id="bc746-189">Rapport d’état du flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="bc746-189">Mailflow status report</span></span>

<span data-ttu-id="bc746-190">Le  rapport d’état du flux de messagerie est un rapport intelligent qui affiche des informations sur le courrier électronique entrant et sortant, les détections de courrier indésirable, les programmes malveillants, les e-mails identifiés comme « bons » et les informations sur les messages électroniques autorisés ou bloqués sur le edge.</span><span class="sxs-lookup"><span data-stu-id="bc746-190">The **Mailflow status report** is a smart report that shows information about incoming and outgoing email, spam detections, malware, email identified as "good", and information about email allowed or blocked on the edge.</span></span> <span data-ttu-id="bc746-191">Il s’agit du seul rapport qui contient des informations de protection Edge et indique la quantité de courrier électronique bloquée avant d’être autorisé dans le service pour évaluation par Exchange Online Protection (EOP).</span><span class="sxs-lookup"><span data-stu-id="bc746-191">This is the only report that contains edge protection information, and shows just how much email is blocked before being allowed into the service for evaluation by Exchange Online Protection (EOP).</span></span> <span data-ttu-id="bc746-192">Il est important de comprendre que si un message est envoyé à cinq destinataires, nous le compterons comme cinq messages différents et pas un seul message.</span><span class="sxs-lookup"><span data-stu-id="bc746-192">It's important to understand that if a message is sent to five recipients we count it as five different messages and not one message.</span></span>

<span data-ttu-id="bc746-193">Pour afficher le rapport dans le portail Microsoft  365 Defender, consultez La boîte aux & collaboration de rapports e-mail \>  \> **& rapports de collaboration.**</span><span class="sxs-lookup"><span data-stu-id="bc746-193">To view the report in the Microsoft 365 Defender portal, go to **Reports** \> **Email & collaboration** \> **Email & collaboration reports**.</span></span> <span data-ttu-id="bc746-194">Dans la page **Rapports de collaboration &** courrier électronique, recherchez le résumé **de** l’état du flux de messagerie, puis cliquez sur Afficher **les détails.**</span><span class="sxs-lookup"><span data-stu-id="bc746-194">On the **Email & collaboration reports** page, find **Mailflow status summary** and then click **View details**.</span></span> <span data-ttu-id="bc746-195">Pour aller directement dans le rapport, ouvrez <https://security.microsoft.com/reports/mailflowStatusReport> .</span><span class="sxs-lookup"><span data-stu-id="bc746-195">To go directly to the report, open <https://security.microsoft.com/reports/mailflowStatusReport>.</span></span>

![Widget de synthèse de l’état du flux de messagerie dans la page Rapports de collaboration & courrier électronique](../../media/mail-flow-status-report-widget.png)

### <a name="type-view-for-the-mailflow-status-report"></a><span data-ttu-id="bc746-197">Affichage des types pour le rapport d’état du flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="bc746-197">Type view for the Mailflow status report</span></span>

![Affichage des types dans le rapport d’état du flux de messagerie](../../media/mail-flow-status-report-type-view.png)

<span data-ttu-id="bc746-199">Dans la page **Rapport d’état du** flux de messagerie, l’onglet **Type** est sélectionné par défaut.</span><span class="sxs-lookup"><span data-stu-id="bc746-199">On the **Mailflow status report** page, the **Type** tab is selected by default.</span></span> <span data-ttu-id="bc746-200">Par défaut, cet affichage contient un graphique et un tableau de détails configurés avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="bc746-200">By default, this view contains a chart and a details table that's configured with the following filters:</span></span>

- <span data-ttu-id="bc746-201">**Date (UTC)** 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="bc746-201">**Date (UTC)** The last 7 days.</span></span>
- <span data-ttu-id="bc746-202">**Direction du courrier**:</span><span class="sxs-lookup"><span data-stu-id="bc746-202">**Mail direction**:</span></span>
  - <span data-ttu-id="bc746-203">**Entrant**</span><span class="sxs-lookup"><span data-stu-id="bc746-203">**Inbound**</span></span>
  - <span data-ttu-id="bc746-204">**Sortant**</span><span class="sxs-lookup"><span data-stu-id="bc746-204">**Outbound**</span></span>
  - <span data-ttu-id="bc746-205">**Intra-organisation**: ce nombre est pour les messages au sein d’un client, c’est-à-dire</span><span class="sxs-lookup"><span data-stu-id="bc746-205">**Intra-org**: this count is for messages within a tenant i.e</span></span> <span data-ttu-id="bc746-206">sender abc@domain.com sends to recipient xyz@domain.com (counted separately from **Inbound** and **Outbound**)</span><span class="sxs-lookup"><span data-stu-id="bc746-206">sender abc@domain.com sends to recipient xyz@domain.com  (counted separately from **Inbound** and **Outbound**)</span></span>
- <span data-ttu-id="bc746-207">**Tapez**:</span><span class="sxs-lookup"><span data-stu-id="bc746-207">**Type**:</span></span>
  - <span data-ttu-id="bc746-208">**Bon courrier**</span><span class="sxs-lookup"><span data-stu-id="bc746-208">**Good mail**</span></span>
  - <span data-ttu-id="bc746-209">**Programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="bc746-209">**Malware**</span></span>
  - <span data-ttu-id="bc746-210">**Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="bc746-210">**Spam**</span></span>
  - <span data-ttu-id="bc746-211">**Protection Edge**</span><span class="sxs-lookup"><span data-stu-id="bc746-211">**Edge protection**</span></span>
  - <span data-ttu-id="bc746-212">**Messages de règle**</span><span class="sxs-lookup"><span data-stu-id="bc746-212">**Rule messages**</span></span>
  - <span data-ttu-id="bc746-213">**Courriers hameçons**</span><span class="sxs-lookup"><span data-stu-id="bc746-213">**Phishing email**</span></span>
- <span data-ttu-id="bc746-214">**Domaine**: **Tous**</span><span class="sxs-lookup"><span data-stu-id="bc746-214">**Domain**: **All**</span></span>

<span data-ttu-id="bc746-215">Le graphique est organisé par les valeurs **Type.**</span><span class="sxs-lookup"><span data-stu-id="bc746-215">The chart is organized by the **Type** values.</span></span>

<span data-ttu-id="bc746-216">Vous pouvez modifier ces filtres en cliquant sur **Filtre.**</span><span class="sxs-lookup"><span data-stu-id="bc746-216">You can change these filters by clicking **Filter**.</span></span>

<span data-ttu-id="bc746-217">Les informations suivantes sont affichées dans le tableau de détails sous le graphique :</span><span class="sxs-lookup"><span data-stu-id="bc746-217">The following information is shown in the details table below the graph:</span></span>

- <span data-ttu-id="bc746-218">**Direction**</span><span class="sxs-lookup"><span data-stu-id="bc746-218">**Direction**</span></span>
- <span data-ttu-id="bc746-219">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="bc746-219">**Type**</span></span>
- <span data-ttu-id="bc746-220">**24 heures**</span><span class="sxs-lookup"><span data-stu-id="bc746-220">**24 hours**</span></span>
- <span data-ttu-id="bc746-221">**3 jours**</span><span class="sxs-lookup"><span data-stu-id="bc746-221">**3 days**</span></span>
- <span data-ttu-id="bc746-222">**7 jours**</span><span class="sxs-lookup"><span data-stu-id="bc746-222">**7 days**</span></span>
- <span data-ttu-id="bc746-223">**15 jours**</span><span class="sxs-lookup"><span data-stu-id="bc746-223">**15 days**</span></span>
- <span data-ttu-id="bc746-224">**30 jours**</span><span class="sxs-lookup"><span data-stu-id="bc746-224">**30 days**</span></span>

<span data-ttu-id="bc746-225">Si vous cliquez **sur Choisir une catégorie pour plus d’informations,** vous pouvez sélectionner l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="bc746-225">If you click **Choose a category for more details**, you can select from the following values:</span></span>

- <span data-ttu-id="bc746-226">**E-mail de hameçonnage**: cette sélection vous place dans le rapport d’état [de la protection contre les menaces.](view-email-security-reports.md#threat-protection-status-report)</span><span class="sxs-lookup"><span data-stu-id="bc746-226">**Phishing email**: This selection takes you to the [Threat protection status report](view-email-security-reports.md#threat-protection-status-report).</span></span>
- <span data-ttu-id="bc746-227">**Programmes malveillants dans les e-mails**: cette sélection vous place dans le rapport d’état [de la protection contre les menaces.](view-email-security-reports.md#threat-protection-status-report)</span><span class="sxs-lookup"><span data-stu-id="bc746-227">**Malware in email**: This selection takes you to the [Threat protection status report](view-email-security-reports.md#threat-protection-status-report).</span></span>
- <span data-ttu-id="bc746-228">**Détections de courrier indésirable**: cette sélection vous permet d’envoyer le rapport [détections de courrier indésirable.](view-email-security-reports.md#spam-detections-report)</span><span class="sxs-lookup"><span data-stu-id="bc746-228">**Spam detections**: This selection takes you to the [Spam Detections report](view-email-security-reports.md#spam-detections-report).</span></span>
- <span data-ttu-id="bc746-229">**Courrier indésirable bloqué edge**: cette sélection vous permet d’envoyer le rapport [détections de courrier indésirable.](view-email-security-reports.md#spam-detections-report)</span><span class="sxs-lookup"><span data-stu-id="bc746-229">**Edge blocked spam**: This selection takes you to the [Spam Detections report](view-email-security-reports.md#spam-detections-report).</span></span>

#### <a name="export-from-type-view"></a><span data-ttu-id="bc746-230">Exporter à partir de l’affichage Type</span><span class="sxs-lookup"><span data-stu-id="bc746-230">Export from Type view</span></span>

<span data-ttu-id="bc746-231">Pour l’affichage détaillé, vous ne pouvez exporter les données que pour une journée.</span><span class="sxs-lookup"><span data-stu-id="bc746-231">For the detail view, you can only export data for one day.</span></span> <span data-ttu-id="bc746-232">Par exemple, si vous souhaitez exporter des données pendant 7 jours, vous devez faire 7 actions d’exportation différentes.</span><span class="sxs-lookup"><span data-stu-id="bc746-232">So, if you want to export data for 7 days, you need to do 7 different export actions.</span></span>

<span data-ttu-id="bc746-233">Chaque fichier .csv exporté est limité à 150 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="bc746-233">Each exported .csv file is limited to 150,000 rows.</span></span> <span data-ttu-id="bc746-234">Si les données de ce jour contiennent plus de 150 000 lignes, plusieurs fichiers .csv seront créés.</span><span class="sxs-lookup"><span data-stu-id="bc746-234">If the data for that day contains more than 150,000 rows, then multiple .csv files will be created.</span></span>

### <a name="direction-view-for-the-mailflow-status-report"></a><span data-ttu-id="bc746-235">Affichage direction pour le rapport d’état du flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="bc746-235">Direction view for the Mailflow status report</span></span>

![Affichage direction dans le rapport d’état du flux de messagerie](../../media/mail-flow-status-report-direction-view.png)

<span data-ttu-id="bc746-237">Si vous cliquez sur **l’onglet Direction,** les mêmes filtres par défaut de **l’affichage Type** sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="bc746-237">If you click the **Direction** tab, the same default filters from the **Type** view are used.</span></span>

<span data-ttu-id="bc746-238">Le graphique est organisé par **valeurs direction.**</span><span class="sxs-lookup"><span data-stu-id="bc746-238">The chart is organized by **Direction** values.</span></span>

<span data-ttu-id="bc746-239">Vous pouvez modifier ces filtres en cliquant sur **Filtre.**</span><span class="sxs-lookup"><span data-stu-id="bc746-239">You can change these filters by clicking **Filter**.</span></span> <span data-ttu-id="bc746-240">Les mêmes filtres de **l’affichage Type** sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="bc746-240">The same filters from the **Type** view are used.</span></span>

<span data-ttu-id="bc746-241">Le tableau de détails contient les mêmes informations que **l’affichage Type.**</span><span class="sxs-lookup"><span data-stu-id="bc746-241">The details table contains same information from the **Type** view.</span></span>

<span data-ttu-id="bc746-242">La **sélection d’une catégorie pour plus d’informations** sur les sélections disponibles et le comportement sont identiques à l’affichage **Type.**</span><span class="sxs-lookup"><span data-stu-id="bc746-242">The **Choose a category for more details** available selections and behavior are the same as the **Type** view.</span></span>

#### <a name="export-from-direction-view"></a><span data-ttu-id="bc746-243">Exporter à partir du mode Direction</span><span class="sxs-lookup"><span data-stu-id="bc746-243">Export from Direction view</span></span>

<span data-ttu-id="bc746-244">Pour l’affichage détaillé, vous ne pouvez exporter les données que pour une journée.</span><span class="sxs-lookup"><span data-stu-id="bc746-244">For the detail view, you can only export data for one day.</span></span> <span data-ttu-id="bc746-245">Par exemple, si vous souhaitez exporter des données pendant 7 jours, vous devez faire 7 actions d’exportation différentes.</span><span class="sxs-lookup"><span data-stu-id="bc746-245">So, if you want to export data for 7 days, you need to do 7 different export actions.</span></span>

<span data-ttu-id="bc746-246">Chaque fichier .csv exporté est limité à 150 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="bc746-246">Each exported .csv file is limited to 150,000 rows.</span></span> <span data-ttu-id="bc746-247">Si les données de ce jour contiennent plus de 150 000 lignes, plusieurs fichiers .csv seront créés.</span><span class="sxs-lookup"><span data-stu-id="bc746-247">If the data for that day contains more than 150,000 rows, then multiple .csv files will be created.</span></span>

### <a name="funnel-view-for-the-mailflow-status-report"></a><span data-ttu-id="bc746-248">Affichage en entonnoir pour le rapport d’état du flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="bc746-248">Funnel view for the Mailflow status report</span></span>

<span data-ttu-id="bc746-249">La **vue Entonnoir** vous montre comment les fonctionnalités de protection contre les menaces de courrier électronique de Microsoft filtrent le courrier électronique entrant et sortant dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="bc746-249">The **Funnel** view shows you how Microsoft's email threat protection features filter incoming and outgoing email in your organization.</span></span> <span data-ttu-id="bc746-250">Il fournit des détails sur le nombre total de messages électroniques et sur la façon dont les fonctionnalités de protection contre les menaces configurées, y compris la protection edge, la protection contre les programmes malveillants, l’anti-hameçonnage, le courrier indésirable et la détection d’usurpation d’accès affectent ce nombre.</span><span class="sxs-lookup"><span data-stu-id="bc746-250">It provides details on the total email count, and how the configured threat protection features, including edge protection, anti-malware, anti-phishing, anti-spam, and anti-spoofing affect this count.</span></span>

![Affichage en entonnoir dans le rapport d’état du flux de messagerie](../../media/mail-flow-status-report-funnel-view.png)

<span data-ttu-id="bc746-252">Si vous  cliquez sur l’onglet Entonnoir, par défaut, cet affichage contient un graphique et un tableau de détails configuré avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="bc746-252">If you click the **Funnel** tab, by default, this view contains a chart and a details table that's configured with the following filters:</span></span>

- <span data-ttu-id="bc746-253">**Date**: 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="bc746-253">**Date**: The last 7 days.</span></span>

- <span data-ttu-id="bc746-254">**Direction**:</span><span class="sxs-lookup"><span data-stu-id="bc746-254">**Direction**:</span></span>
  - <span data-ttu-id="bc746-255">**Entrant**</span><span class="sxs-lookup"><span data-stu-id="bc746-255">**Inbound**</span></span>
  - <span data-ttu-id="bc746-256">**Sortant**</span><span class="sxs-lookup"><span data-stu-id="bc746-256">**Outbound**</span></span>
  - <span data-ttu-id="bc746-257">**Intra-organisation**: ce nombre est le nombre de messages envoyés au sein d’un client ; Autrement dit, l’expéditeur abc@domain.com envoyé au destinataire xyz@domain.com (comptabilisé séparément des messages entrants et sortants).</span><span class="sxs-lookup"><span data-stu-id="bc746-257">**Intra-org**: This count is for messages sent within a tenant; i.e, sender abc@domain.com sends to recipient xyz@domain.com (counted separately from Inbound and Outbound).</span></span>

<span data-ttu-id="bc746-258">L’affichage agrégé et le tableau détails autorisent 90 jours de filtrage.</span><span class="sxs-lookup"><span data-stu-id="bc746-258">The aggregate view and details table view allow for 90 days of filtering.</span></span>

<span data-ttu-id="bc746-259">Vous pouvez modifier ces filtres en cliquant sur **Filtre.**</span><span class="sxs-lookup"><span data-stu-id="bc746-259">You can change these filters by clicking **Filter**.</span></span> <span data-ttu-id="bc746-260">Les mêmes filtres de **l’affichage Type** sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="bc746-260">The same filters from the **Type** view are used.</span></span>

<span data-ttu-id="bc746-261">Ce graphique indique le nombre de messages électroniques organisés par :</span><span class="sxs-lookup"><span data-stu-id="bc746-261">This chart shows the email count organized by:</span></span>

- <span data-ttu-id="bc746-262">**Nombre total de messages électroniques**</span><span class="sxs-lookup"><span data-stu-id="bc746-262">**Total email**</span></span>
- <span data-ttu-id="bc746-263">**Courrier électronique après protection edge**</span><span class="sxs-lookup"><span data-stu-id="bc746-263">**Email after edge protection**</span></span>
- <span data-ttu-id="bc746-264">**Règle de messagerie après transport** (règle de flux de messagerie)</span><span class="sxs-lookup"><span data-stu-id="bc746-264">**Email after transport rule** (mail flow rule)</span></span>
- <span data-ttu-id="bc746-265">**Courrier électronique après anti-programme malveillant, réputation du fichier, bloc de type de fichier**</span><span class="sxs-lookup"><span data-stu-id="bc746-265">**Email after anti-malware, file reputation, file type block**</span></span>
- <span data-ttu-id="bc746-266">**Courrier électronique après anti-hameçonnage, réputation d’URL, emprunt d’identité de marque, anti-usurpation d’identité**</span><span class="sxs-lookup"><span data-stu-id="bc746-266">**Email after anti-phish, URL reputation, brand impersonation, anti-spoof**</span></span>
- <span data-ttu-id="bc746-267">**Courrier électronique après filtrage du courrier indésirable en bloc**</span><span class="sxs-lookup"><span data-stu-id="bc746-267">**Email after anti-spam, bulk mail filtering**</span></span>
- <span data-ttu-id="bc746-268">**Courrier électronique après l’emprunt d’identité de l’utilisateur et du domaine**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="bc746-268">**Email after user and domain impersonation**<sup>\*</sup></span></span>
- <span data-ttu-id="bc746-269">**E-mail après détonation du fichier et de l’URL**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="bc746-269">**Email after file and URL detonation**<sup>\*</sup></span></span>
- <span data-ttu-id="bc746-270">**Courrier électronique détecté comme étant anodin après la remise (protection de temps de clic d’URL)**</span><span class="sxs-lookup"><span data-stu-id="bc746-270">**Email detected as benign after post-delivery protection (URL click time protection)**</span></span>

<span data-ttu-id="bc746-271"><sup>\*</sup>Defender pour Office 365 uniquement</span><span class="sxs-lookup"><span data-stu-id="bc746-271"><sup>\*</sup> Defender for Office 365 only</span></span>

<span data-ttu-id="bc746-272">Pour afficher l’e-mail filtré par EOP ou Defender Office 365 séparément, cliquez sur la valeur dans la légende du graphique.</span><span class="sxs-lookup"><span data-stu-id="bc746-272">To view the email filtered by EOP or Defender for Office 365 separately, click on the value in the chart legend.</span></span>

<span data-ttu-id="bc746-273">Le tableau de détails contient les informations suivantes, indiquées dans l’ordre décroit de date :</span><span class="sxs-lookup"><span data-stu-id="bc746-273">The details table contains the following information, shown in descending date order:</span></span>

- <span data-ttu-id="bc746-274">**Date**</span><span class="sxs-lookup"><span data-stu-id="bc746-274">**Date**</span></span>
- <span data-ttu-id="bc746-275">**Nombre total de messages électroniques**</span><span class="sxs-lookup"><span data-stu-id="bc746-275">**Total email**</span></span>
- <span data-ttu-id="bc746-276">**Protection Edge**</span><span class="sxs-lookup"><span data-stu-id="bc746-276">**Edge protection**</span></span>
- <span data-ttu-id="bc746-277">**Anti-programme malveillant, réputation de fichier, bloc de type de fichier**:</span><span class="sxs-lookup"><span data-stu-id="bc746-277">**Anti-malware, file reputation, file type block**:</span></span>
  - <span data-ttu-id="bc746-278">**Réputation du** fichier : messages filtrés en raison de l’identification d’un fichier joint par d’autres clients Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bc746-278">**File reputation**: Messages filtered due to identification of an attached file by other Microsoft customers.</span></span>
  - <span data-ttu-id="bc746-279">**Bloc de type de** fichier : messages filtrés en raison du type de fichier malveillant identifié dans le message.</span><span class="sxs-lookup"><span data-stu-id="bc746-279">**File type block**: Messages filtered due to the type of malicious file identified in the message.</span></span>
- <span data-ttu-id="bc746-280">**Anti-hameçonnage, réputation de l’URL, emprunt d’identité de marque, anti-usurpation d’identité**:</span><span class="sxs-lookup"><span data-stu-id="bc746-280">**Anti-phish, URL reputation, Brand impersonation, anti-spoof**:</span></span>
  - <span data-ttu-id="bc746-281">**Réputation de l’URL**: messages filtrés en raison de l’identification de l’URL par d’autres clients Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bc746-281">**URL reputation**: Messages filtered due to the identification of the URL by other Microsoft customers.</span></span>
  - <span data-ttu-id="bc746-282">**Emprunt d’identité de marque**: messages filtrés en raison du message provenant de la marque connue usurpant l’identité des expéditeurs.</span><span class="sxs-lookup"><span data-stu-id="bc746-282">**Brand impersonation**: Messages filtered due to the message coming from well-known brand impersonating senders.</span></span>
  - <span data-ttu-id="bc746-283">**Anti-usurpation**: messages filtrés en raison de la tentative d’usurpation d’un domaine appartenant au destinataire ou d’un domaine que l’expéditeur du message ne possède pas.</span><span class="sxs-lookup"><span data-stu-id="bc746-283">**Anti-spoof**: Messages filtered due to the message attempting to spoof a domain that the recipient belongs to, or a domain that the message sender doesn't own.</span></span>
- <span data-ttu-id="bc746-284">**Anti-courrier indésirable, filtrage du courrier en bloc**:</span><span class="sxs-lookup"><span data-stu-id="bc746-284">**Anti-spam, bulk mail filtering**:</span></span>
  - <span data-ttu-id="bc746-285">**Filtrage du courrier en bloc**: messages filtrés en fonction du seuil bcl (seuil de plainte en bloc) dans une stratégie anti-courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="bc746-285">**Bulk mail filtering**: Messages filtered based on the bulk complain level (BCL) threshold in an anti-spam policy.</span></span>
- <span data-ttu-id="bc746-286">**Emprunt d’identité d’utilisateur et** de domaine (Defender pour Office 365) :</span><span class="sxs-lookup"><span data-stu-id="bc746-286">**User and domain impersonation (Defender for Office 365)**:</span></span>
  - <span data-ttu-id="bc746-287">**Emprunt d’identité** d’utilisateur : messages filtrés en raison d’une tentative d’emprunt d’identité d’un utilisateur (expéditeur de message) défini dans les paramètres de protection contre l’emprunt d’identité d’une stratégie anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="bc746-287">**User impersonation**: Messages filtered due to an attempt to impersonate a user (message sender) that's defined in the impersonation protection settings of an anti-phishing policy.</span></span>
  - <span data-ttu-id="bc746-288">**Emprunt d’identité** de domaine : messages filtrés en raison d’une tentative d’emprunt d’identité d’un domaine défini dans les paramètres de protection contre l’emprunt d’identité d’une stratégie anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="bc746-288">**Domain impersonation**: Messages filtered due to an attempt to impersonate a domain that's defined in the impersonation protection settings of an anti-phishing policy.</span></span>
- <span data-ttu-id="bc746-289">**Détonation de fichier et d’URL (Defender pour Office 365)**:</span><span class="sxs-lookup"><span data-stu-id="bc746-289">**File and URL detonation (Defender for Office 365)**:</span></span>
  - <span data-ttu-id="bc746-290">**Détonation de fichier**: messages filtrés par une stratégie Safe pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="bc746-290">**File detonation**: Messages filtered by a Safe Attachments policy.</span></span>
  - <span data-ttu-id="bc746-291">**Détonation d’URL**: message filtré par une stratégie Safe liens.</span><span class="sxs-lookup"><span data-stu-id="bc746-291">**URL detonation**: Message filtered by a Safe Links policy.</span></span>
- <span data-ttu-id="bc746-292">Protection post-remise et ZAP (Protection contre les menaces) ou **ZAP (EOP)**: purge automatique de zéro heure (ZAP) pour les programmes malveillants, le courrier indésirable et le hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="bc746-292">**Post-delivery protection and ZAP (ATP), or ZAP (EOP)**: Zero-hour auto purge (ZAP) for malware, spam, and phishing.</span></span>

<span data-ttu-id="bc746-293">Si vous sélectionnez une ligne dans le tableau de détails, une répartition supplémentaire du nombre de messages est affichée dans le volant.</span><span class="sxs-lookup"><span data-stu-id="bc746-293">If you select a row in the details table, a further breakdown of the email counts are shown in the flyout.</span></span>

#### <a name="export-from-funnel-view"></a><span data-ttu-id="bc746-294">Exporter à partir du affichage Entonnoir</span><span class="sxs-lookup"><span data-stu-id="bc746-294">Export from Funnel view</span></span>

<span data-ttu-id="bc746-295">Après avoir cliqué **sur Exporter** sous **Options,** vous pouvez sélectionner l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="bc746-295">After you click **Export** under **Options**, you can select one of the following values:</span></span>

- <span data-ttu-id="bc746-296">**Résumé (avec des données pour les 90 derniers jours au maximum)**</span><span class="sxs-lookup"><span data-stu-id="bc746-296">**Summary (with data for last 90 days at most)**</span></span>
- <span data-ttu-id="bc746-297">**Détails (avec des données pour les 30 derniers jours au maximum)**</span><span class="sxs-lookup"><span data-stu-id="bc746-297">**Details (with data for last 30 days at most)**</span></span>

<span data-ttu-id="bc746-298">Sous **Date**, choisissez une plage, puis cliquez sur **Appliquer**.</span><span class="sxs-lookup"><span data-stu-id="bc746-298">Under **Date**, choose a range, and then click **Apply**.</span></span> <span data-ttu-id="bc746-299">Les données des filtres actuels sont exportées vers un .csv de données.</span><span class="sxs-lookup"><span data-stu-id="bc746-299">Data for the current filters will be exported to a .csv file.</span></span>

<span data-ttu-id="bc746-300">Chaque fichier .csv exporté est limité à 150 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="bc746-300">Each exported .csv file is limited to 150,000 rows.</span></span> <span data-ttu-id="bc746-301">Si les données contiennent plus de 150 000 lignes, plusieurs .csv fichiers seront créés.</span><span class="sxs-lookup"><span data-stu-id="bc746-301">If the data contains more than 150,000 rows, then multiple .csv files will be created.</span></span>

### <a name="tech-view-for-the-mailflow-status-report"></a><span data-ttu-id="bc746-302">Affichage technique pour le rapport d’état du flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="bc746-302">Tech view for the Mailflow status report</span></span>

<span data-ttu-id="bc746-303">La **vue Tech est** similaire à la vue Entonnoir, fournissant des détails plus détaillés pour les fonctionnalités de protection contre les menaces configurées. </span><span class="sxs-lookup"><span data-stu-id="bc746-303">The **Tech view** is similar to the **Funnel** view, providing more granular details for the configured threat protections features.</span></span> <span data-ttu-id="bc746-304">À partir du graphique, vous pouvez voir comment les messages sont classés aux différentes étapes de la protection contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="bc746-304">From the chart, you can see how messages are categorized at the different stages of threat protection.</span></span>

<span data-ttu-id="bc746-305">Si vous cliquez sur **l’onglet** Affichage Technique, par défaut, cet affichage contient un graphique et un tableau de détails configurés avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="bc746-305">If you click the **Tech view** tab, by default, this view contains a chart and a details table that's configured with the following filters:</span></span>

- <span data-ttu-id="bc746-306">**Date**: 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="bc746-306">**Date**: The last 7 days.</span></span>

- <span data-ttu-id="bc746-307">**Direction**:</span><span class="sxs-lookup"><span data-stu-id="bc746-307">**Direction**:</span></span>
  - <span data-ttu-id="bc746-308">**Entrant**</span><span class="sxs-lookup"><span data-stu-id="bc746-308">**Inbound**</span></span>
  - <span data-ttu-id="bc746-309">**Sortant**</span><span class="sxs-lookup"><span data-stu-id="bc746-309">**Outbound**</span></span>
  - <span data-ttu-id="bc746-310">**Intra-organisation**: ce nombre est pour les messages au sein d’un client, c’est-à-dire</span><span class="sxs-lookup"><span data-stu-id="bc746-310">**Intra-org**: this count is for messages within a tenant i.e</span></span> <span data-ttu-id="bc746-311">sender abc@domain.com sends to recipient xyz@domain.com (counted separately from Inbound and Outbound)</span><span class="sxs-lookup"><span data-stu-id="bc746-311">sender abc@domain.com sends to recipient xyz@domain.com (counted separately from Inbound and Outbound)</span></span>

<span data-ttu-id="bc746-312">L’affichage agrégé et le tableau détails autorisent 90 jours de filtrage.</span><span class="sxs-lookup"><span data-stu-id="bc746-312">The aggregate view and details table view allow for 90 days of filtering.</span></span>

<span data-ttu-id="bc746-313">Vous pouvez modifier ces filtres en cliquant sur **Filtre.**</span><span class="sxs-lookup"><span data-stu-id="bc746-313">You can change these filters by clicking **Filter**.</span></span> <span data-ttu-id="bc746-314">Les mêmes filtres de **l’affichage Type** sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="bc746-314">The same filters from the **Type** view are used.</span></span>

<span data-ttu-id="bc746-315">Ce graphique présente les messages organisés dans les catégories suivantes :</span><span class="sxs-lookup"><span data-stu-id="bc746-315">This chart shows messages organized into the following categories:</span></span>

- <span data-ttu-id="bc746-316">**Nombre total de messages électroniques**</span><span class="sxs-lookup"><span data-stu-id="bc746-316">**Total email**</span></span>
- <span data-ttu-id="bc746-317">**Edge autoriser** et **edge filtré**</span><span class="sxs-lookup"><span data-stu-id="bc746-317">**Edge allow** and **Edge filtered**</span></span>
- <span data-ttu-id="bc746-318">**Règles de transport d’autoriser** et **de transport filtrées** (règles de flux de messagerie)</span><span class="sxs-lookup"><span data-stu-id="bc746-318">**Transport rule allow** and **Transport rule filtered** (mail flow rules)</span></span>
- <span data-ttu-id="bc746-319">**Pas de programmes** **malveillants, Safe détection des pièces jointes** <sup>\*</sup> et détection du moteur **anti-programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="bc746-319">**Not malware**, **Safe Attachments detection**<sup>\*</sup>, and **Anti-malware engine detection**</span></span>
- <span data-ttu-id="bc746-320">**Pas de hameçonnage,**  **d’échec DMARC,** de détection d’emprunt d’identité, de détection d’usurpation <sup>\*</sup> d’identité et de détection **d’hameçonnage** </span><span class="sxs-lookup"><span data-stu-id="bc746-320">**Not phish**, **DMARC failure**, **Impersonation detection**<sup>\*</sup>, **Spoof detection**, and **Phish detection**</span></span>
- <span data-ttu-id="bc746-321">**Aucune détection avec détection de détonation d’URL** et **de détonation d’URL**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="bc746-321">**No detection with URL detonation** and **URL detonation detection**<sup>\*</sup></span></span>
- <span data-ttu-id="bc746-322">**Pas de courrier indésirable** et  **de courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="bc746-322">**Not spam** and  **Spam**</span></span>
- <span data-ttu-id="bc746-323">**E-mail** non malveillant, **détection Safe liens et** <sup>\*</sup> **ZAP**</span><span class="sxs-lookup"><span data-stu-id="bc746-323">**Non-malicious email**, **Safe Links detection**<sup>\*</sup>, and **ZAP**</span></span>

<span data-ttu-id="bc746-324"><sup>\*</sup>Defender for Office 365</span><span class="sxs-lookup"><span data-stu-id="bc746-324"><sup>\*</sup> Defender for Office 365</span></span>

<span data-ttu-id="bc746-325">Lorsque vous pointez sur une catégorie dans le graphique, vous pouvez voir le nombre de messages dans cette catégorie.</span><span class="sxs-lookup"><span data-stu-id="bc746-325">When you hover over a category in the chart, you can see the number of messages in that category.</span></span>

<span data-ttu-id="bc746-326">Le tableau de détails contient les informations suivantes, indiquées dans l’ordre décroit de date :</span><span class="sxs-lookup"><span data-stu-id="bc746-326">The details table contains the following information, shown in descending date order:</span></span>

- <span data-ttu-id="bc746-327">**Date (UTC)**</span><span class="sxs-lookup"><span data-stu-id="bc746-327">**Date (UTC)**</span></span>
- <span data-ttu-id="bc746-328">**Nombre total de messages électroniques**</span><span class="sxs-lookup"><span data-stu-id="bc746-328">**Total email**</span></span>
- <span data-ttu-id="bc746-329">**Edge filtré**</span><span class="sxs-lookup"><span data-stu-id="bc746-329">**Edge filtered**</span></span>
- <span data-ttu-id="bc746-330">**Messages de règle**: messages filtrés en raison de règles de flux de messagerie (également appelées règles de transport).</span><span class="sxs-lookup"><span data-stu-id="bc746-330">**Rule messages**: Messages filtered due to  mail flow rules (also known as transport rules).</span></span>
- <span data-ttu-id="bc746-331">**Moteur anti-programme malveillant,** **Safe pièces jointes** <sup>\*</sup> :</span><span class="sxs-lookup"><span data-stu-id="bc746-331">**Anti-malware engine**, **Safe Attachments**<sup>\*</sup>:</span></span>
- <span data-ttu-id="bc746-332">**DMARC, emprunt d’identité,** <sup>\*</sup> **usurpation** d’identité, **hameçonnage filtré**:</span><span class="sxs-lookup"><span data-stu-id="bc746-332">**DMARC, impersonation**<sup>\*</sup>, **spoof**, **phish filtered**:</span></span>
  - <span data-ttu-id="bc746-333">**DMARC**: messages filtrés en raison de l’échec de la vérification de l’authentification DMARC.</span><span class="sxs-lookup"><span data-stu-id="bc746-333">**DMARC**: Messages filtered due to the message failing its DMARC authentication check.</span></span>
- <span data-ttu-id="bc746-334">**Détection de détonation d’URL**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="bc746-334">**URL detonation detection**<sup>\*</sup></span></span>
- <span data-ttu-id="bc746-335">**Filtrage anti-courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="bc746-335">**Anti-spam filtered**</span></span>
- <span data-ttu-id="bc746-336">**ZAP supprimé**</span><span class="sxs-lookup"><span data-stu-id="bc746-336">**ZAP removed**</span></span>
- <span data-ttu-id="bc746-337">**Détection par liens Safe de détection**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="bc746-337">**Detection by Safe Links**<sup>\*</sup></span></span>

<span data-ttu-id="bc746-338"><sup>\*</sup>Defender for Office 365</span><span class="sxs-lookup"><span data-stu-id="bc746-338"><sup>\*</sup> Defender for Office 365</span></span>

<span data-ttu-id="bc746-339">Si vous sélectionnez une ligne dans le tableau de détails, une répartition supplémentaire du nombre de messages est affichée dans le volant.</span><span class="sxs-lookup"><span data-stu-id="bc746-339">If you select a row in the details table, a further breakdown of the email counts are shown in the flyout.</span></span>

#### <a name="export-from-tech-view"></a><span data-ttu-id="bc746-340">Exporter à partir d’un affichage tech</span><span class="sxs-lookup"><span data-stu-id="bc746-340">Export from Tech view</span></span>

<span data-ttu-id="bc746-341">En cliquant **sur Exporter,** sous **Options,** vous pouvez sélectionner l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="bc746-341">On clicking **Export**, under **Options** you can select one of the following values:</span></span>

- <span data-ttu-id="bc746-342">**Résumé (avec des données pour les 90 derniers jours au maximum)**</span><span class="sxs-lookup"><span data-stu-id="bc746-342">**Summary (with data for last 90 days at most)**</span></span>
- <span data-ttu-id="bc746-343">**Détails (avec des données pour les 30 derniers jours au maximum)**</span><span class="sxs-lookup"><span data-stu-id="bc746-343">**Details (with data for last 30 days at most)**</span></span>

<span data-ttu-id="bc746-344">Sous **Date**, choisissez une plage, puis cliquez sur **Appliquer**.</span><span class="sxs-lookup"><span data-stu-id="bc746-344">Under **Date**, choose a range, and then click **Apply**.</span></span> <span data-ttu-id="bc746-345">Les données des filtres actuels sont exportées vers un .csv de données.</span><span class="sxs-lookup"><span data-stu-id="bc746-345">Data for the current filters will be exported to a .csv file.</span></span>

<span data-ttu-id="bc746-346">Chaque fichier .csv exporté est limité à 150 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="bc746-346">Each exported .csv file is limited to 150,000 rows.</span></span> <span data-ttu-id="bc746-347">Si les données contiennent plus de 150 000 lignes, plusieurs .csv fichiers seront créés.</span><span class="sxs-lookup"><span data-stu-id="bc746-347">If the data contains more than 150,000 rows, then multiple .csv files will be created.</span></span>

![Affichage technique dans le rapport d’état du flux de messagerie](../../media/mail-flow-status-report-tech-view.png)

## <a name="malware-detections-report"></a><span data-ttu-id="bc746-349">Rapport sur les détections de programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="bc746-349">Malware detections report</span></span>

<span data-ttu-id="bc746-350">Le rapport détections de programmes malveillants affiche des informations sur les détections de programmes malveillants dans les messages électroniques entrants et sortants (programmes **malveillants détectés** par Exchange Online Protection ou EOP).</span><span class="sxs-lookup"><span data-stu-id="bc746-350">The **Malware detections report** report shows information about malware detections in incoming and outgoing email messages (malware detected by Exchange Online Protection or EOP).</span></span> <span data-ttu-id="bc746-351">Pour plus d’informations sur la protection contre les programmes malveillants dans EOP, voir Protection contre les programmes [malveillants dans EOP.](anti-malware-protection.md)</span><span class="sxs-lookup"><span data-stu-id="bc746-351">For more information about malware protection in EOP, see [Anti-malware protection in EOP](anti-malware-protection.md).</span></span>

<span data-ttu-id="bc746-352">Le filtre d’affichage agrégé autorise 90 jours, tandis que le filtre de tableau détails ne le permet que sur 10 jours.</span><span class="sxs-lookup"><span data-stu-id="bc746-352">The aggregate view filter allows for 90 days, while the details table filter only allows for 10 days.</span></span>

<span data-ttu-id="bc746-353">Pour afficher le rapport dans le portail  Microsoft 365 Defender, consultez la & collaboration de rapports e-mail \>  \> **& rapports de collaboration.**</span><span class="sxs-lookup"><span data-stu-id="bc746-353">To view the report in the Microsoft 365 Defender portal, go to **Reports** \> **Email & collaboration** \> **Email & collaboration reports**.</span></span> <span data-ttu-id="bc746-354">Dans la page **& de collaboration,** recherchez les programmes malveillants détectés dans le courrier **électronique,** puis cliquez sur Afficher **les détails.**</span><span class="sxs-lookup"><span data-stu-id="bc746-354">On the **Email & collaboration reports** page, find **Malware detected in email** and then click **View details**.</span></span> <span data-ttu-id="bc746-355">Pour aller directement dans le rapport, ouvrez <https://security.microsoft.com/reports/MalwareDetections> .</span><span class="sxs-lookup"><span data-stu-id="bc746-355">To go directly to the report, open <https://security.microsoft.com/reports/MalwareDetections>.</span></span>

![Détections de programmes malveillants dans le widget de messagerie sur la page rapports de collaboration & messagerie](../../media/malware-detections-widget.png)

<span data-ttu-id="bc746-357">Dans la page Du rapport détections de programmes **malveillants,** vous  pouvez filtrer à la fois le graphique et le tableau de détails en cliquant sur Filtrer et en sélectionnant l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="bc746-357">On the **Malware detections report** page, you can filter both the chart and the details table by clicking **Filter** and selecting one of the following values:</span></span>

- <span data-ttu-id="bc746-358">**Date (UTC)** **Date de début et** date de **fin**</span><span class="sxs-lookup"><span data-stu-id="bc746-358">**Date (UTC)** **Start date** and **End date**</span></span>
- <span data-ttu-id="bc746-359">**Direction**: **trafic entrant** et **sortant**</span><span class="sxs-lookup"><span data-stu-id="bc746-359">**Direction**: **Inbound** and **Outbound**</span></span>

![Affichage du rapport dans le rapport de détection des programmes malveillants dans le rapport de courrier électronique](../../media/malware-detections-report-view.png)

<span data-ttu-id="bc746-361">Dans le tableau de détails sous le graphique, vous pouvez voir les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="bc746-361">In the details table below the graph, you can see the following details:</span></span>

- <span data-ttu-id="bc746-362">**Date**</span><span class="sxs-lookup"><span data-stu-id="bc746-362">**Date**</span></span>
- <span data-ttu-id="bc746-363">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="bc746-363">**Sender address**</span></span>
- <span data-ttu-id="bc746-364">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="bc746-364">**Recipient address**</span></span>
- <span data-ttu-id="bc746-365">**ID de message**: disponible dans le champ d’en-tête **Message-ID** dans l’en-tête du message et doit être unique.</span><span class="sxs-lookup"><span data-stu-id="bc746-365">**Message ID**: Available in the **Message-ID** header field in the message header and should be unique.</span></span> <span data-ttu-id="bc746-366">Un exemple de valeur est `<08f1e0f6806a47b4ac103961109ae6ef@server.domain>` (notez les crochets).</span><span class="sxs-lookup"><span data-stu-id="bc746-366">An example value is `<08f1e0f6806a47b4ac103961109ae6ef@server.domain>` (note the angle brackets).</span></span>
- <span data-ttu-id="bc746-367">**Subject**</span><span class="sxs-lookup"><span data-stu-id="bc746-367">**Subject**</span></span>
- <span data-ttu-id="bc746-368">**Filename**</span><span class="sxs-lookup"><span data-stu-id="bc746-368">**Filename**</span></span>
- <span data-ttu-id="bc746-369">**Nom du programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="bc746-369">**Malware name**</span></span>

## <a name="mail-latency-report"></a><span data-ttu-id="bc746-370">Rapport de latence du courrier</span><span class="sxs-lookup"><span data-stu-id="bc746-370">Mail latency report</span></span>

<span data-ttu-id="bc746-371">Le **rapport de latence de messagerie** dans Defender pour Office 365 contient des informations sur la remise et la latence de détonation du courrier au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="bc746-371">The **Mail latency report** in Defender for Office 365 contains information on the mail delivery and detonation latency experienced within your organization.</span></span> <span data-ttu-id="bc746-372">Pour plus d’informations, voir [Rapport de latence de messagerie.](view-reports-for-mdo.md#mail-latency-report)</span><span class="sxs-lookup"><span data-stu-id="bc746-372">For more information, see [Mail latency report](view-reports-for-mdo.md#mail-latency-report).</span></span>

## <a name="spam-detections-report"></a><span data-ttu-id="bc746-373">Rapport sur la détection des courriers indésirables</span><span class="sxs-lookup"><span data-stu-id="bc746-373">Spam detections report</span></span>

> [!NOTE]
> <span data-ttu-id="bc746-374">Le **rapport de détection du courrier** indésirable va finir par disparaître.</span><span class="sxs-lookup"><span data-stu-id="bc746-374">The **Spam detections report** will eventually go away.</span></span> <span data-ttu-id="bc746-375">Les mêmes informations sont disponibles dans le rapport d’état [de la protection contre les menaces.](#threat-protection-status-report)</span><span class="sxs-lookup"><span data-stu-id="bc746-375">The same information is available in the [Threat protection status report](#threat-protection-status-report).</span></span>

## <a name="spoof-detections-report"></a><span data-ttu-id="bc746-376">Rapport sur les détections d’usurpation d’usurpation</span><span class="sxs-lookup"><span data-stu-id="bc746-376">Spoof detections report</span></span>

> [!NOTE]
> <span data-ttu-id="bc746-377">Le rapport sur les détections d’usurpation d’usurpation d’informations amélioré, tel que décrit dans cet article, est disponible en prévisualisation, peut faire l’objet de changements et n’est pas disponible dans toutes les organisations.</span><span class="sxs-lookup"><span data-stu-id="bc746-377">The improved Spoof detections report as described in this article is in Preview, is subject to change, and is not available in all organizations.</span></span> <span data-ttu-id="bc746-378">L’ancienne version du rapport affiche uniquement les messages **de bonne qualité** et les courriers **indésirables**.</span><span class="sxs-lookup"><span data-stu-id="bc746-378">The older version of the report shows only **Good mail** and **Caught as spam**.</span></span>

<span data-ttu-id="bc746-379">Le **rapport sur les détections d’usurpation d’informations** affiche des informations sur les messages qui ont été bloqués ou autorisés en raison de l’usurpation d’informations.</span><span class="sxs-lookup"><span data-stu-id="bc746-379">The **Spoof detections** report shows information about messages that were blocked or allowed due to spoofing.</span></span> <span data-ttu-id="bc746-380">Pour plus d’informations sur l’usurpation d’adresse, consultez la protection contre l’usurpation [d’adresse dans EOP.](anti-spoofing-protection.md)</span><span class="sxs-lookup"><span data-stu-id="bc746-380">For more information about spoofing, see [Anti-spoofing protection in EOP](anti-spoofing-protection.md).</span></span>

<span data-ttu-id="bc746-381">L’affichage agrégé du rapport autorise 45 jours de filtrage, tandis que l’affichage détaillé ne permet que dix jours <sup>\*</sup> de filtrage.</span><span class="sxs-lookup"><span data-stu-id="bc746-381">The aggregate view of the report allows for 45 days of filtering<sup>\*</sup>, while the detail view only allows for ten days of filtering.</span></span>

<span data-ttu-id="bc746-382"><sup>\*</sup> Au final, vous pourrez utiliser jusqu’à 90 jours de filtrage.</span><span class="sxs-lookup"><span data-stu-id="bc746-382"><sup>\*</sup> Eventually, you'll be able to use up to 90 days of filtering.</span></span>

<span data-ttu-id="bc746-383">Pour afficher le rapport dans le portail  Microsoft 365 Defender, consultez la & collaboration de rapports e-mail \>  \> **& rapports de collaboration.**</span><span class="sxs-lookup"><span data-stu-id="bc746-383">To view the report in the Microsoft 365 Defender portal, go to **Reports** \> **Email & collaboration** \> **Email & collaboration reports**.</span></span> <span data-ttu-id="bc746-384">Dans la page **& de collaboration,** recherchez les détections d’usurpation **d’adresse,** puis cliquez sur **Afficher les détails.**</span><span class="sxs-lookup"><span data-stu-id="bc746-384">On the **Email & collaboration reports** page, find **Spoof detections** and then click **View details**.</span></span> <span data-ttu-id="bc746-385">Pour aller directement dans le rapport, ouvrez <https://security.microsoft.com/reports/SpoofMailReportV2> .</span><span class="sxs-lookup"><span data-stu-id="bc746-385">To go directly to the report, open <https://security.microsoft.com/reports/SpoofMailReportV2>.</span></span>

![Widget de détections d’usurpation d'& dans la page Rapports de collaboration & courrier électronique](../../media/spoof-detections-widget.png)

<span data-ttu-id="bc746-387">Le graphique présente les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="bc746-387">The chart shows the following information:</span></span>

- <span data-ttu-id="bc746-388">**Pass**</span><span class="sxs-lookup"><span data-stu-id="bc746-388">**Pass**</span></span>
- <span data-ttu-id="bc746-389">**Échec**</span><span class="sxs-lookup"><span data-stu-id="bc746-389">**Fail**</span></span>
- <span data-ttu-id="bc746-390">**SoftPass**</span><span class="sxs-lookup"><span data-stu-id="bc746-390">**SoftPass**</span></span>
- <span data-ttu-id="bc746-391">**Aucune**</span><span class="sxs-lookup"><span data-stu-id="bc746-391">**None**</span></span>
- <span data-ttu-id="bc746-392">**Other**</span><span class="sxs-lookup"><span data-stu-id="bc746-392">**Other**</span></span>

<span data-ttu-id="bc746-393">Lorsque vous pointez sur un jour (point de données) dans le graphique, vous pouvez voir combien de messages usurpés ont été détectés et pourquoi.</span><span class="sxs-lookup"><span data-stu-id="bc746-393">When you hover over a day (data point) in the chart, you can see how many spoofed messages were detected and why.</span></span>

<span data-ttu-id="bc746-394">Dans la page **Rapport** de courrier usurpation d’adresse, vous pouvez  filtrer à la fois le graphique et le tableau de détails en cliquant sur Filtrer et en sélectionnant une ou plusieurs des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="bc746-394">On the **Spoof mail report** page, you can filter both the chart and the details table by clicking **Filter** and selecting one or more of the following values:</span></span>

- <span data-ttu-id="bc746-395">**Date (UTC)** **Date de début et** date de **fin**</span><span class="sxs-lookup"><span data-stu-id="bc746-395">**Date (UTC)** **Start date** and **End date**</span></span>
- <span data-ttu-id="bc746-396">**Résultat**:</span><span class="sxs-lookup"><span data-stu-id="bc746-396">**Result**:</span></span>
  - <span data-ttu-id="bc746-397">**Pass**</span><span class="sxs-lookup"><span data-stu-id="bc746-397">**Pass**</span></span>
  - <span data-ttu-id="bc746-398">**Échec**</span><span class="sxs-lookup"><span data-stu-id="bc746-398">**Fail**</span></span>
  - <span data-ttu-id="bc746-399">**SoftPass**</span><span class="sxs-lookup"><span data-stu-id="bc746-399">**SoftPass**</span></span>
  - <span data-ttu-id="bc746-400">**Aucune**</span><span class="sxs-lookup"><span data-stu-id="bc746-400">**None**</span></span>
  - <span data-ttu-id="bc746-401">**Other**</span><span class="sxs-lookup"><span data-stu-id="bc746-401">**Other**</span></span>
- <span data-ttu-id="bc746-402">**Type d’usurpation :** **interne** et **externe**</span><span class="sxs-lookup"><span data-stu-id="bc746-402">**Spoof type**: **Internal** and **External**</span></span>

![Page de rapport de courrier électronique usurpant l’Microsoft 365 Defender](../../media/spoof-detections-report-page.png)

<span data-ttu-id="bc746-404">Dans le tableau de détails sous le graphique, vous pouvez voir les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="bc746-404">In the details table below the graph, you can see the following details:</span></span>

- <span data-ttu-id="bc746-405">**Date**</span><span class="sxs-lookup"><span data-stu-id="bc746-405">**Date**</span></span>
- <span data-ttu-id="bc746-406">**Utilisateur usurpé**</span><span class="sxs-lookup"><span data-stu-id="bc746-406">**Spoofed user**</span></span>
- <span data-ttu-id="bc746-407">**Infrastructure d’envoi**</span><span class="sxs-lookup"><span data-stu-id="bc746-407">**Sending infrastructure**</span></span>
- <span data-ttu-id="bc746-408">**Type d’usurpation**</span><span class="sxs-lookup"><span data-stu-id="bc746-408">**Spoof type**</span></span>
- <span data-ttu-id="bc746-409">**Résultat**</span><span class="sxs-lookup"><span data-stu-id="bc746-409">**Result**</span></span>
- <span data-ttu-id="bc746-410">**Code de résultat**</span><span class="sxs-lookup"><span data-stu-id="bc746-410">**Result code**</span></span>
- <span data-ttu-id="bc746-411">**SPF**</span><span class="sxs-lookup"><span data-stu-id="bc746-411">**SPF**</span></span>
- <span data-ttu-id="bc746-412">**DKIM**</span><span class="sxs-lookup"><span data-stu-id="bc746-412">**DKIM**</span></span>
- <span data-ttu-id="bc746-413">**DMARC**</span><span class="sxs-lookup"><span data-stu-id="bc746-413">**DMARC**</span></span>
- <span data-ttu-id="bc746-414">**Nombre de messages**</span><span class="sxs-lookup"><span data-stu-id="bc746-414">**Message count**</span></span>

<span data-ttu-id="bc746-415">Pour plus d’informations sur les codes de résultats d’authentification composite, consultez les [en-têtes de message anti-courrier](anti-spam-message-headers.md)indésirable Microsoft 365 .</span><span class="sxs-lookup"><span data-stu-id="bc746-415">For more information about composite authentication result codes, see [Anti-spam message headers in Microsoft 365](anti-spam-message-headers.md).</span></span>

## <a name="submissions-report"></a><span data-ttu-id="bc746-416">Rapport soumissions</span><span class="sxs-lookup"><span data-stu-id="bc746-416">Submissions report</span></span>

<span data-ttu-id="bc746-417">Le **rapport Soumissions** affiche des informations sur les éléments que les administrateurs ont signalés à Microsoft pour analyse.</span><span class="sxs-lookup"><span data-stu-id="bc746-417">The **Submissions** report shows information about items that admins have reported to Microsoft for analysis.</span></span> <span data-ttu-id="bc746-418">Pour plus d’informations, voir Utiliser la soumission d’administrateur pour soumettre des messages suspects de courrier indésirable, d’hameçonnage, d’URL et [de fichiers à Microsoft.](admin-submission.md)</span><span class="sxs-lookup"><span data-stu-id="bc746-418">For more information, see [Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft](admin-submission.md).</span></span>

<span data-ttu-id="bc746-419">Pour afficher le rapport dans le portail  Microsoft 365 Defender, consultez la & collaboration de rapports e-mail \>  \> **& rapports de collaboration.**</span><span class="sxs-lookup"><span data-stu-id="bc746-419">To view the report in the Microsoft 365 Defender portal, go to **Reports** \> **Email & collaboration** \> **Email & collaboration reports**.</span></span> <span data-ttu-id="bc746-420">Dans la page **& de collaboration,** recherchez **Soumissions,** puis cliquez sur **Afficher les détails.**</span><span class="sxs-lookup"><span data-stu-id="bc746-420">On the **Email & collaboration reports** page, find **Submissions** and then click **View details**.</span></span> <span data-ttu-id="bc746-421">Pour aller directement dans le rapport, ouvrez <https://security.microsoft.com/adminSubmissionReport> .</span><span class="sxs-lookup"><span data-stu-id="bc746-421">To go directly to the report, open <https://security.microsoft.com/adminSubmissionReport>.</span></span> <span data-ttu-id="bc746-422">Pour aller aux [soumissions d’administrateur dans le portail Microsoft 365 Defender,](admin-submission.md)cliquez **sur Go to Submissions**.</span><span class="sxs-lookup"><span data-stu-id="bc746-422">To go to [admin submissions in the Microsoft 365 Defender portal](admin-submission.md), click **Go to Submissions**.</span></span>

![Widget soumissions sur la page rapports de collaboration & courrier électronique](../../media/submissions-report-widget.png)

<span data-ttu-id="bc746-424">Le graphique présente les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="bc746-424">The chart shows the following information:</span></span>

- <span data-ttu-id="bc746-425">**Pending**</span><span class="sxs-lookup"><span data-stu-id="bc746-425">**Pending**</span></span>
- <span data-ttu-id="bc746-426">**Terminée**</span><span class="sxs-lookup"><span data-stu-id="bc746-426">**Completed**</span></span>

<span data-ttu-id="bc746-427">Dans la page **Soumissions,** vous pouvez filtrer le graphique  et le tableau de détails en cliquant sur Filtrer et en sélectionnant une ou plusieurs des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="bc746-427">On the **Submissions** page, you can filter both the chart and the details table by clicking **Filter** and selecting one or more of the following values:</span></span>

- <span data-ttu-id="bc746-428">**Date signalée :** **heure de début** et heure de **fin**</span><span class="sxs-lookup"><span data-stu-id="bc746-428">**Date reported**: **Start time** and **End time**</span></span>
- <span data-ttu-id="bc746-429">**Type de soumission**:</span><span class="sxs-lookup"><span data-stu-id="bc746-429">**Submission type**:</span></span>
  - <span data-ttu-id="bc746-430">**E-mail**</span><span class="sxs-lookup"><span data-stu-id="bc746-430">**Email**</span></span>
  - <span data-ttu-id="bc746-431">**URL**</span><span class="sxs-lookup"><span data-stu-id="bc746-431">**URL**</span></span>
  - <span data-ttu-id="bc746-432">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="bc746-432">**File**</span></span>
- <span data-ttu-id="bc746-433">**ID de soumission**</span><span class="sxs-lookup"><span data-stu-id="bc746-433">**Submission ID**</span></span>
- <span data-ttu-id="bc746-434">**ID de message réseau**</span><span class="sxs-lookup"><span data-stu-id="bc746-434">**Network Message ID**</span></span>
- <span data-ttu-id="bc746-435">**Sender**</span><span class="sxs-lookup"><span data-stu-id="bc746-435">**Sender**</span></span>
- <span data-ttu-id="bc746-436">**Name**</span><span class="sxs-lookup"><span data-stu-id="bc746-436">**Name**</span></span>
- <span data-ttu-id="bc746-437">**Soumis par**</span><span class="sxs-lookup"><span data-stu-id="bc746-437">**Submitted by**</span></span>
- <span data-ttu-id="bc746-438">**Raison de l’envoi**:</span><span class="sxs-lookup"><span data-stu-id="bc746-438">**Reason for submitting**:</span></span>
  - <span data-ttu-id="bc746-439">**Non indésirable**</span><span class="sxs-lookup"><span data-stu-id="bc746-439">**Not junk**</span></span>
  - <span data-ttu-id="bc746-440">**Hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="bc746-440">**Phish**</span></span>
  - <span data-ttu-id="bc746-441">**Programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="bc746-441">**Malware**</span></span>
  - <span data-ttu-id="bc746-442">**Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="bc746-442">**Spam**</span></span>
- <span data-ttu-id="bc746-443">**État de rescan :**</span><span class="sxs-lookup"><span data-stu-id="bc746-443">**Rescan status**:</span></span>
  - <span data-ttu-id="bc746-444">**Pending**</span><span class="sxs-lookup"><span data-stu-id="bc746-444">**Pending**</span></span>
  - <span data-ttu-id="bc746-445">**Terminée**</span><span class="sxs-lookup"><span data-stu-id="bc746-445">**Completed**</span></span>

<span data-ttu-id="bc746-446">Le tableau de détails sous le graphique  présente les mêmes informations  et possède les  mêmes **options** de colonnes De groupe ou de personnalisation que sous l’onglet Soumis pour analyse dans envois de collaboration & courrier \> **électronique.**</span><span class="sxs-lookup"><span data-stu-id="bc746-446">The details table below the graph shows the same information and has the same **Group** or **Customize columns** options as on the **Submitted for analysis** tab at **Email & collaboration** \> **Submissions**.</span></span> <span data-ttu-id="bc746-447">Pour plus d’informations, voir [Afficher les soumissions d’administrateur à Microsoft.](admin-submission.md#view-admin-submissions-to-microsoft)</span><span class="sxs-lookup"><span data-stu-id="bc746-447">For more information, see [View admin submissions to Microsoft](admin-submission.md#view-admin-submissions-to-microsoft).</span></span>

![Page de rapport soumissions dans le portail Microsoft 365 Defender web](../../media/submissions-report-page.png)

## <a name="threat-protection-status-report"></a><span data-ttu-id="bc746-449">Rapport sur l’état de la protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="bc746-449">Threat protection status report</span></span>

<span data-ttu-id="bc746-450">Le **rapport d’état de la protection** contre les menaces est disponible dans EOP et Defender pour Office 365 ; toutefois, les rapports contiennent des données différentes.</span><span class="sxs-lookup"><span data-stu-id="bc746-450">The **Threat protection status** report is available in both EOP and Defender for Office 365; however, the reports contain different data.</span></span> <span data-ttu-id="bc746-451">Par exemple, les clients EOP peuvent afficher des informations sur les programmes malveillants détectés dans le courrier électronique, mais pas sur les fichiers [malveillants détectés](mdo-for-spo-odb-and-teams.md)par les pièces jointes Safe pour SharePoint, OneDrive et Microsoft Teams .</span><span class="sxs-lookup"><span data-stu-id="bc746-451">For example, EOP customers can view information about malware detected in email, but not information about malicious files detected by [Safe Attachments for SharePoint, OneDrive, and Microsoft Teams](mdo-for-spo-odb-and-teams.md).</span></span>

<span data-ttu-id="bc746-452">Le rapport fournit le nombre de messages électroniques avec du contenu malveillant, tels que des fichiers ou des adresses de site web (URL) qui ont été bloqués par le moteur anti-programme malveillant, la purge automatique d’heure zéro [(ZAP)](zero-hour-auto-purge.md)et Defender pour des fonctionnalités de Office 365 telles que les liens [Safe,](safe-links.md)les pièces [jointes Safe](safe-attachments.md)et les fonctionnalités de protection contre l’emprunt d’identité dans les stratégies [anti-hameçonnage.](set-up-anti-phishing-policies.md#exclusive-settings-in-anti-phishing-policies-in-microsoft-defender-for-office-365)</span><span class="sxs-lookup"><span data-stu-id="bc746-452">The report provides the count of email messages with malicious content, such as files or website addresses (URLs) that were blocked by the anti-malware engine, [zero-hour auto purge (ZAP)](zero-hour-auto-purge.md), and Defender for Office 365 features like [Safe Links](safe-links.md), [Safe Attachments](safe-attachments.md), and [impersonation protection features in anti-phishing policies](set-up-anti-phishing-policies.md#exclusive-settings-in-anti-phishing-policies-in-microsoft-defender-for-office-365).</span></span> <span data-ttu-id="bc746-453">Vous pouvez utiliser ces informations pour identifier les tendances ou déterminer si les stratégies d’organisation doivent être ajuster.</span><span class="sxs-lookup"><span data-stu-id="bc746-453">You can use this information to identify trends or determine whether organization policies need adjustment.</span></span>

<span data-ttu-id="bc746-454">**Remarque**: il est important de comprendre que si un message est envoyé à cinq destinataires, nous le compterons comme cinq messages différents et pas un seul message.</span><span class="sxs-lookup"><span data-stu-id="bc746-454">**Note**: It's important to understand that if a message is sent to five recipients we count it as five different messages and not one message.</span></span>

<span data-ttu-id="bc746-455">Pour afficher le rapport dans le portail  Microsoft 365 Defender, consultez la & collaboration de rapports e-mail \>  \> **& rapports de collaboration.**</span><span class="sxs-lookup"><span data-stu-id="bc746-455">To view the report in the Microsoft 365 Defender portal, go to **Reports** \> **Email & collaboration** \> **Email & collaboration reports**.</span></span> <span data-ttu-id="bc746-456">Dans la page **Rapports de collaboration & courrier** électronique, recherchez l’état de la **protection** contre les menaces, puis cliquez sur Afficher **les détails.**</span><span class="sxs-lookup"><span data-stu-id="bc746-456">On the **Email & collaboration reports** page, find **Threat protection status** and then click **View details**.</span></span> <span data-ttu-id="bc746-457">Pour aller directement dans le rapport, ouvrez l’une des URL suivantes :</span><span class="sxs-lookup"><span data-stu-id="bc746-457">To go directly to the report, open one of the following URLs:</span></span>

- <span data-ttu-id="bc746-458">Defender pour Office 365 :<https://security.microsoft.com/reports/TPSAggregateReportATP></span><span class="sxs-lookup"><span data-stu-id="bc746-458">Defender for Office 365: <https://security.microsoft.com/reports/TPSAggregateReportATP></span></span>
- <span data-ttu-id="bc746-459">EOP : <https://security.microsoft.com/reports/TPSAggregateReport></span><span class="sxs-lookup"><span data-stu-id="bc746-459">EOP: <https://security.microsoft.com/reports/TPSAggregateReport></span></span>

![Widget d’état de la protection contre les menaces dans la page Rapports de collaboration & courrier électronique](../../media/threat-protection-status-report-widget.png)

<span data-ttu-id="bc746-461">Par défaut, le graphique affiche les données des 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="bc746-461">By default, the chart shows data for the past 7 days.</span></span> <span data-ttu-id="bc746-462">Si vous cliquez sur **Filtrer** dans la page du rapport d’état de la **protection** contre les menaces, vous pouvez sélectionner une plage de dates de 90 jours (les abonnements d’essai peuvent être limités à 30 jours).</span><span class="sxs-lookup"><span data-stu-id="bc746-462">If you click **Filter** on the **Threat protection status report** page, you can select a 90 day date range (trial subscriptions might be limited to 30 days).</span></span> <span data-ttu-id="bc746-463">Le tableau de détails autorise le filtrage pendant 30 jours.</span><span class="sxs-lookup"><span data-stu-id="bc746-463">The details table allows filtering for 30 days.</span></span>

<span data-ttu-id="bc746-464">Les vues disponibles sont décrites dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="bc746-464">The available views are described in the following sections.</span></span>

### <a name="view-data-by-overview"></a><span data-ttu-id="bc746-465">Afficher les données par vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="bc746-465">View data by Overview</span></span>

![Vue d’ensemble dans le rapport d’état de la protection contre les menaces](../../media/threat-protection-status-report-overview-view.png)

<span data-ttu-id="bc746-467">Dans **l’affichage Des données par vue d’ensemble,** les informations de détection suivantes sont affichées dans le graphique :</span><span class="sxs-lookup"><span data-stu-id="bc746-467">In the **View data by Overview** view, the following detection information is shown in the chart:</span></span>

- <span data-ttu-id="bc746-468">**Programme malveillant de messagerie**</span><span class="sxs-lookup"><span data-stu-id="bc746-468">**Email malware**</span></span>
- <span data-ttu-id="bc746-469">**Hameçonnage par e-mail**</span><span class="sxs-lookup"><span data-stu-id="bc746-469">**Email phish**</span></span>
- <span data-ttu-id="bc746-470">**Programme malveillant de contenu**</span><span class="sxs-lookup"><span data-stu-id="bc746-470">**Content malware**</span></span>

<span data-ttu-id="bc746-471">Aucun tableau de détails n’est disponible sous le graphique.</span><span class="sxs-lookup"><span data-stu-id="bc746-471">No details table is available below the chart.</span></span>

<span data-ttu-id="bc746-472">Si vous cliquez **sur Filtre,** les filtres suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="bc746-472">If you click **Filter**, the following filters are available:</span></span>

- <span data-ttu-id="bc746-473">**Date (UTC)** **Date de début et** date de **fin**</span><span class="sxs-lookup"><span data-stu-id="bc746-473">**Date (UTC)** **Start date** and **End date**</span></span>
- <span data-ttu-id="bc746-474">**Détection :** programme **malveillant de messagerie,** **hameçonnage de messagerie** ou programme malveillant de **contenu**</span><span class="sxs-lookup"><span data-stu-id="bc746-474">**Detection**: **Email malware**, **Email phish**, or **Content malware**</span></span>
- <span data-ttu-id="bc746-475">**Protégé par**: **MDO** (Defender for Office 365) ou **EOP**</span><span class="sxs-lookup"><span data-stu-id="bc746-475">**Protected by**: **MDO** (Defender for Office 365) or **EOP**</span></span>
- <span data-ttu-id="bc746-476">**Balise**: filtrer les résultats par utilisateurs ou groupes pour lesquels la balise utilisateur spécifiée a été appliquée (y compris les comptes de priorité).</span><span class="sxs-lookup"><span data-stu-id="bc746-476">**Tag**: Filter the results by users or groups that have had the specified user tag applied (including priority accounts).</span></span> <span data-ttu-id="bc746-477">Pour plus d’informations sur les balises utilisateur, voir [Balises utilisateur.](user-tags.md)</span><span class="sxs-lookup"><span data-stu-id="bc746-477">For more information about user tags, see [User tags](user-tags.md).</span></span>
- <span data-ttu-id="bc746-478">**Direction**</span><span class="sxs-lookup"><span data-stu-id="bc746-478">**Direction**</span></span>
- <span data-ttu-id="bc746-479">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="bc746-479">**Domain**</span></span>
- <span data-ttu-id="bc746-480">**Type de stratégie**</span><span class="sxs-lookup"><span data-stu-id="bc746-480">**Policy type**</span></span>

<span data-ttu-id="bc746-481">Lorsque vous avez terminé la configuration des filtres, cliquez sur **Appliquer,** **Annuler** ou **Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="bc746-481">When you're finished configuring the filters, click **Apply**, **Cancel**, or **Clear filters**.</span></span>

### <a name="view-data-by-email--phish-and-chart-breakdown-by-detection-technology"></a><span data-ttu-id="bc746-482">Afficher les données par hameçonnage de messagerie \> électronique et répartition des graphiques par technologie de détection</span><span class="sxs-lookup"><span data-stu-id="bc746-482">View data by Email \> Phish and Chart breakdown by Detection Technology</span></span>

![Affichage de la technologie de détection pour le courrier d’hameçonnage dans le rapport d’état de la protection contre les menaces](../../media/threat-protection-status-report-phishing-detection-tech-view.png)

<span data-ttu-id="bc746-484">Dans **l’affichage \> des données par hameçonnage par courrier électronique** et répartition **du** graphique par technologie de détection, les informations suivantes sont affichées dans le graphique :</span><span class="sxs-lookup"><span data-stu-id="bc746-484">In the **View data by Email \> Phish** and **Chart breakdown by Detection Technology** view, the following information is shown in the chart:</span></span>

- <span data-ttu-id="bc746-485">**Réputation malveillante d’URL**: réputation d’URL malveillante générée à partir de <sup>\*</sup> Defender pour Office 365 détonations dans d’autres Microsoft 365 clients.</span><span class="sxs-lookup"><span data-stu-id="bc746-485">**URL malicious reputation**<sup>\*</sup>: Malicious URL reputation generated from Defender for Office 365 detonations in other Microsoft 365 customers.</span></span>
- <span data-ttu-id="bc746-486">**Filtre avancé :** signaux de hameçonnage basés sur l’apprentissage automatique.</span><span class="sxs-lookup"><span data-stu-id="bc746-486">**Advanced filter**: Phishing signals based on machine learning.</span></span>
- <span data-ttu-id="bc746-487">**Filtre général :** signaux de hameçonnage basés sur des règles d’analyste.</span><span class="sxs-lookup"><span data-stu-id="bc746-487">**General filter**: Phishing signals based on analyst rules.</span></span>
- <span data-ttu-id="bc746-488">**Usurpation d’adresse intra-organisation**: l’expéditeur tente d’usurper le domaine du destinataire.</span><span class="sxs-lookup"><span data-stu-id="bc746-488">**Spoof intra-org**: Sender is trying to spoof the recipient domain.</span></span>
- <span data-ttu-id="bc746-489">**Usurpation d’un domaine externe**: l’expéditeur tente d’usurper un autre domaine.</span><span class="sxs-lookup"><span data-stu-id="bc746-489">**Spoof external domain**: Sender is trying to spoof some other domain.</span></span>
- <span data-ttu-id="bc746-490">**Usurpation d’identité DMARC**: échec de l’authentification DMARC sur les messages.</span><span class="sxs-lookup"><span data-stu-id="bc746-490">**Spoof DMARC**: DMARC authentication failure on messages.</span></span>
- <span data-ttu-id="bc746-491">**Marque d’emprunt d’identité**: emprunt d’identité de marques connues basées sur des expéditeurs.</span><span class="sxs-lookup"><span data-stu-id="bc746-491">**Impersonation brand**: Impersonation of well-known brands based on senders.</span></span>
- <span data-ttu-id="bc746-492">**Détection d’analyse mixte**</span><span class="sxs-lookup"><span data-stu-id="bc746-492">**Mixed analysis detection**</span></span>
- <span data-ttu-id="bc746-493">**Réputation des fichiers**</span><span class="sxs-lookup"><span data-stu-id="bc746-493">**File reputation**</span></span>
- <span data-ttu-id="bc746-494">**Correspondance de l’empreinte**</span><span class="sxs-lookup"><span data-stu-id="bc746-494">**Fingerprint matching**</span></span>
- <span data-ttu-id="bc746-495">**Réputation de détonation d’URL**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="bc746-495">**URL detonation reputation**<sup>\*</sup></span></span>
- <span data-ttu-id="bc746-496">**Détonation d’URL**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="bc746-496">**URL detonation**<sup>\*</sup></span></span>
- <span data-ttu-id="bc746-497">**Utilisateur de l’emprunt d’identité**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="bc746-497">**Impersonation user**<sup>\*</sup></span></span>
- <span data-ttu-id="bc746-498">**Domaine d’emprunt d’identité**: emprunt d’identité des domaines que le client <sup>\*</sup> possède ou définit.</span><span class="sxs-lookup"><span data-stu-id="bc746-498">**Impersonation domain**<sup>\*</sup>: Impersonation of domains that the customer owns or defines.</span></span>
- <span data-ttu-id="bc746-499">**Emprunt d’identité d’intelligence de** boîte aux lettres : emprunt d’identité des utilisateurs définis par l’administrateur ou appris par le biais de l’intelligence <sup>\*</sup> des boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="bc746-499">**Mailbox intelligence impersonation**<sup>\*</sup>: Impersonation of users defined by admin or learned through mailbox intelligence.</span></span>
- <span data-ttu-id="bc746-500">**Détonation de fichier**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="bc746-500">**File detonation**<sup>\*</sup></span></span>
- <span data-ttu-id="bc746-501">**Campagne**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="bc746-501">**Campaign**<sup>\*</sup></span></span>

<span data-ttu-id="bc746-502">Dans le tableau de détails sous le graphique, les informations suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="bc746-502">In the details table below the chart, the following information is available:</span></span>

- <span data-ttu-id="bc746-503">**Date**</span><span class="sxs-lookup"><span data-stu-id="bc746-503">**Date**</span></span>
- <span data-ttu-id="bc746-504">**Subject**</span><span class="sxs-lookup"><span data-stu-id="bc746-504">**Subject**</span></span>
- <span data-ttu-id="bc746-505">**Expéditeur**</span><span class="sxs-lookup"><span data-stu-id="bc746-505">**Sender**</span></span>
- <span data-ttu-id="bc746-506">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="bc746-506">**Recipients**</span></span>
- <span data-ttu-id="bc746-507">**Détecté par**</span><span class="sxs-lookup"><span data-stu-id="bc746-507">**Detected by**</span></span>
- <span data-ttu-id="bc746-508">**État de remise**</span><span class="sxs-lookup"><span data-stu-id="bc746-508">**Delivery Status**</span></span>
- <span data-ttu-id="bc746-509">**Source de compromis**</span><span class="sxs-lookup"><span data-stu-id="bc746-509">**Source of Compromise**</span></span>
- <span data-ttu-id="bc746-510">**Tags**</span><span class="sxs-lookup"><span data-stu-id="bc746-510">**Tags**</span></span>

<span data-ttu-id="bc746-511">Si vous cliquez **sur Filtre,** les filtres suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="bc746-511">If you click **Filter**, the following filters are available:</span></span>

- <span data-ttu-id="bc746-512">**Date (UTC)** **Date de début et** date de **fin**</span><span class="sxs-lookup"><span data-stu-id="bc746-512">**Date (UTC)** **Start date** and **End date**</span></span>
- <span data-ttu-id="bc746-513">**Détection**</span><span class="sxs-lookup"><span data-stu-id="bc746-513">**Detection**</span></span>
- <span data-ttu-id="bc746-514">**Protégé par**: **MDO** (Defender for Office 365) ou **EOP**</span><span class="sxs-lookup"><span data-stu-id="bc746-514">**Protected by**: **MDO** (Defender for Office 365) or **EOP**</span></span>
- <span data-ttu-id="bc746-515">**Direction**</span><span class="sxs-lookup"><span data-stu-id="bc746-515">**Direction**</span></span>
- <span data-ttu-id="bc746-516">**Balise**: filtrer les résultats par utilisateurs ou groupes pour lesquels la balise utilisateur spécifiée a été appliquée (y compris les comptes de priorité).</span><span class="sxs-lookup"><span data-stu-id="bc746-516">**Tag**: Filter the results by users or groups that have had the specified user tag applied (including priority accounts).</span></span> <span data-ttu-id="bc746-517">Pour plus d’informations sur les balises utilisateur, voir [Balises utilisateur.](user-tags.md)</span><span class="sxs-lookup"><span data-stu-id="bc746-517">For more information about user tags, see [User tags](user-tags.md).</span></span>
- <span data-ttu-id="bc746-518">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="bc746-518">**Domain**</span></span>
- <span data-ttu-id="bc746-519">**Type de stratégie**</span><span class="sxs-lookup"><span data-stu-id="bc746-519">**Policy type**</span></span>
- <span data-ttu-id="bc746-520">**Nom de la stratégie** (tableau de détails uniquement)</span><span class="sxs-lookup"><span data-stu-id="bc746-520">**Policy name** (details table only)</span></span>
- <span data-ttu-id="bc746-521">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="bc746-521">**Recipients**</span></span>

<span data-ttu-id="bc746-522">Lorsque vous avez terminé la configuration des filtres, cliquez sur **Appliquer,** **Annuler** ou **Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="bc746-522">When you're finished configuring the filters, click **Apply**, **Cancel**, or **Clear filters**.</span></span>

### <a name="view-data-by-email--malware-and-chart-breakdown-by-detection-technology"></a><span data-ttu-id="bc746-523">Afficher les données par programme malveillant et \> répartition des graphiques par technologie de détection</span><span class="sxs-lookup"><span data-stu-id="bc746-523">View data by Email \> Malware and Chart breakdown by Detection Technology</span></span>

![Affichage de la technologie de détection pour les programmes malveillants dans le rapport d’état de la protection contre les menaces](../../media/threat-protection-status-report-malware-detection-tech-view.png)

<span data-ttu-id="bc746-525">Dans **l’affichage \> des données par programme** malveillant par courrier électronique et **répartition des** graphiques par technologie de détection, les informations suivantes sont affichées dans le graphique :</span><span class="sxs-lookup"><span data-stu-id="bc746-525">In the **View data by Email \> Malware** and **Chart breakdown by Detection Technology** view, the following information is shown in the chart:</span></span>

- <span data-ttu-id="bc746-526">**Détonation de fichier** <sup>\*</sup> : détection par Safe pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="bc746-526">**File detonation**<sup>\*</sup>: Detection by Safe Attachments.</span></span>
- <span data-ttu-id="bc746-527">**Réputation de détonation de fichier**: toutes les réputations de fichiers <sup>\*</sup> malveillants générées par Defender pour Office 365 détonations.</span><span class="sxs-lookup"><span data-stu-id="bc746-527">**File detonation reputation**<sup>\*</sup>: All malicious file reputation generated by Defender for Office 365 detonations.</span></span>
- <span data-ttu-id="bc746-528">**Réputation des fichiers**</span><span class="sxs-lookup"><span data-stu-id="bc746-528">**File reputation**</span></span>
- <span data-ttu-id="bc746-529">**Moteur anti-programme malveillant :** détection à partir de moteurs <sup>\*</sup> anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="bc746-529">**Anti-malware engine**<sup>\*</sup>: Detection from anti-malware engines.</span></span>
- <span data-ttu-id="bc746-530">Blocage du type de fichier de stratégie **anti-programme** malveillant : il s’adresse aux messages électroniques filtrés en raison du type de fichier malveillant identifié dans le message.</span><span class="sxs-lookup"><span data-stu-id="bc746-530">**Anti-malware policy file type block**: These are email messages filtered out due to the type of malicious file identified in the message.</span></span>
- <span data-ttu-id="bc746-531">**Réputation d’URL malveillante**</span><span class="sxs-lookup"><span data-stu-id="bc746-531">**URL malicious reputation**</span></span>
- <span data-ttu-id="bc746-532">**Détonation d’URL**</span><span class="sxs-lookup"><span data-stu-id="bc746-532">**URL detonation**</span></span>
- <span data-ttu-id="bc746-533">**Réputation de détonation d’URL**</span><span class="sxs-lookup"><span data-stu-id="bc746-533">**URL detonation reputation**</span></span>
- <span data-ttu-id="bc746-534">**Campagne**</span><span class="sxs-lookup"><span data-stu-id="bc746-534">**Campaign**</span></span>

<span data-ttu-id="bc746-535">Dans le tableau de détails sous le graphique, les informations suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="bc746-535">In the details table below the chart, the following information is available:</span></span>

- <span data-ttu-id="bc746-536">**Date**</span><span class="sxs-lookup"><span data-stu-id="bc746-536">**Date**</span></span>
- <span data-ttu-id="bc746-537">**Subject**</span><span class="sxs-lookup"><span data-stu-id="bc746-537">**Subject**</span></span>
- <span data-ttu-id="bc746-538">**Expéditeur**</span><span class="sxs-lookup"><span data-stu-id="bc746-538">**Sender**</span></span>
- <span data-ttu-id="bc746-539">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="bc746-539">**Recipients**</span></span>
- <span data-ttu-id="bc746-540">**Détecté par**</span><span class="sxs-lookup"><span data-stu-id="bc746-540">**Detected by**</span></span>
- <span data-ttu-id="bc746-541">**État de remise**</span><span class="sxs-lookup"><span data-stu-id="bc746-541">**Delivery Status**</span></span>
- <span data-ttu-id="bc746-542">**Source de compromis**</span><span class="sxs-lookup"><span data-stu-id="bc746-542">**Source of Compromise**</span></span>
- <span data-ttu-id="bc746-543">**Tags**</span><span class="sxs-lookup"><span data-stu-id="bc746-543">**Tags**</span></span>

<span data-ttu-id="bc746-544">Si vous cliquez **sur Filtre,** les filtres suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="bc746-544">If you click **Filter**, the following filters are available:</span></span>

- <span data-ttu-id="bc746-545">**Date (UTC)** **Date de début et** date de **fin**</span><span class="sxs-lookup"><span data-stu-id="bc746-545">**Date (UTC)** **Start date** and **End date**</span></span>
- <span data-ttu-id="bc746-546">**Détection**</span><span class="sxs-lookup"><span data-stu-id="bc746-546">**Detection**</span></span>
- <span data-ttu-id="bc746-547">**Protégé par**: **MDO** (Defender for Office 365) ou **EOP**</span><span class="sxs-lookup"><span data-stu-id="bc746-547">**Protected by**: **MDO** (Defender for Office 365) or **EOP**</span></span>
- <span data-ttu-id="bc746-548">**Direction**</span><span class="sxs-lookup"><span data-stu-id="bc746-548">**Direction**</span></span>
- <span data-ttu-id="bc746-549">**Balise**: filtrer les résultats par utilisateurs ou groupes pour lesquels la balise utilisateur spécifiée a été appliquée (y compris les comptes de priorité).</span><span class="sxs-lookup"><span data-stu-id="bc746-549">**Tag**: Filter the results by users or groups that have had the specified user tag applied (including priority accounts).</span></span> <span data-ttu-id="bc746-550">Pour plus d’informations sur les balises utilisateur, voir [Balises utilisateur.](user-tags.md)</span><span class="sxs-lookup"><span data-stu-id="bc746-550">For more information about user tags, see [User tags](user-tags.md).</span></span>
- <span data-ttu-id="bc746-551">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="bc746-551">**Domain**</span></span>
- <span data-ttu-id="bc746-552">**Type de stratégie**</span><span class="sxs-lookup"><span data-stu-id="bc746-552">**Policy type**</span></span>
- <span data-ttu-id="bc746-553">**Nom de la stratégie** (tableau de détails uniquement)</span><span class="sxs-lookup"><span data-stu-id="bc746-553">**Policy name** (details table only)</span></span>
- <span data-ttu-id="bc746-554">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="bc746-554">**Recipients**</span></span>

<span data-ttu-id="bc746-555">Lorsque vous avez terminé la configuration des filtres, cliquez sur **Appliquer,** **Annuler** ou **Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="bc746-555">When you're finished configuring the filters, click **Apply**, **Cancel**, or **Clear filters**.</span></span>

### <a name="chart-breakdown-by-policy-type-and-view-data-by-email--phish-or-view-data-by-email--malware"></a><span data-ttu-id="bc746-556">Répartition des graphiques par type de stratégie et affichage des données par hameçonnage de messagerie ou affichage des données par programme malveillant \> de \> messagerie</span><span class="sxs-lookup"><span data-stu-id="bc746-556">Chart breakdown by Policy type and View data by Email \> Phish or View data by Email \> Malware</span></span>

![Affichage du type de stratégie pour les courriers électroniques de hameçonnage ou de programmes malveillants dans le rapport d’état de la protection contre les menaces](../../media/threat-protection-status-report-phishing-policy-type-view.png)

<span data-ttu-id="bc746-558">Dans la répartition **du graphique** par type de stratégie et l’affichage des données par hameçonnage de messagerie ou affichage des données par affichage des programmes malveillants de messagerie, les informations suivantes sont affichées dans les graphiques : **\>** **\>**</span><span class="sxs-lookup"><span data-stu-id="bc746-558">In the **Chart breakdown by Policy type** and **View data by Email \> Phish** or **View data by Email \> Malware** views, the following information is shown in the charts:</span></span>

- <span data-ttu-id="bc746-559">**Anti-programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="bc746-559">**Anti-malware**</span></span>
- <span data-ttu-id="bc746-560">**Safe Pièces jointes**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="bc746-560">**Safe Attachments**<sup>\*</sup></span></span>
- <span data-ttu-id="bc746-561">**Anti-hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="bc746-561">**Anti-phish**</span></span>
- <span data-ttu-id="bc746-562">**Anti-courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="bc746-562">**Anti-spam**</span></span>
- <span data-ttu-id="bc746-563">**Règle de flux de messagerie** (également appelée règle de transport)</span><span class="sxs-lookup"><span data-stu-id="bc746-563">**Mail flow rule** (also known as a transport rule)</span></span>
- <span data-ttu-id="bc746-564">**Autres**</span><span class="sxs-lookup"><span data-stu-id="bc746-564">**Others**</span></span>

<span data-ttu-id="bc746-565">Dans le tableau de détails sous le graphique, les informations suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="bc746-565">In the details table below the chart, the following information is available:</span></span>

- <span data-ttu-id="bc746-566">**Date**</span><span class="sxs-lookup"><span data-stu-id="bc746-566">**Date**</span></span>
- <span data-ttu-id="bc746-567">**Subject**</span><span class="sxs-lookup"><span data-stu-id="bc746-567">**Subject**</span></span>
- <span data-ttu-id="bc746-568">**Expéditeur**</span><span class="sxs-lookup"><span data-stu-id="bc746-568">**Sender**</span></span>
- <span data-ttu-id="bc746-569">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="bc746-569">**Recipients**</span></span>
- <span data-ttu-id="bc746-570">**Détecté par**</span><span class="sxs-lookup"><span data-stu-id="bc746-570">**Detected by**</span></span>
- <span data-ttu-id="bc746-571">**État de remise**</span><span class="sxs-lookup"><span data-stu-id="bc746-571">**Delivery Status**</span></span>
- <span data-ttu-id="bc746-572">**Source de compromis**</span><span class="sxs-lookup"><span data-stu-id="bc746-572">**Source of Compromise**</span></span>
- <span data-ttu-id="bc746-573">**Tags**</span><span class="sxs-lookup"><span data-stu-id="bc746-573">**Tags**</span></span>

<span data-ttu-id="bc746-574">Si vous cliquez **sur Filtre,** les filtres suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="bc746-574">If you click **Filter**, the following filters are available:</span></span>

- <span data-ttu-id="bc746-575">**Date (UTC)** **Date de début et** date de **fin**</span><span class="sxs-lookup"><span data-stu-id="bc746-575">**Date (UTC)** **Start date** and **End date**</span></span>
- <span data-ttu-id="bc746-576">**Détection**</span><span class="sxs-lookup"><span data-stu-id="bc746-576">**Detection**</span></span>
- <span data-ttu-id="bc746-577">**Protégé par**: **MDO** (Defender for Office 365) ou **EOP**</span><span class="sxs-lookup"><span data-stu-id="bc746-577">**Protected by**: **MDO** (Defender for Office 365) or **EOP**</span></span>
- <span data-ttu-id="bc746-578">**Direction**</span><span class="sxs-lookup"><span data-stu-id="bc746-578">**Direction**</span></span>
- <span data-ttu-id="bc746-579">**Balise**: filtrer les résultats par utilisateurs ou groupes pour lesquels la balise utilisateur spécifiée a été appliquée (y compris les comptes de priorité).</span><span class="sxs-lookup"><span data-stu-id="bc746-579">**Tag**: Filter the results by users or groups that have had the specified user tag applied (including priority accounts).</span></span> <span data-ttu-id="bc746-580">Pour plus d’informations sur les balises utilisateur, voir [Balises utilisateur.](user-tags.md)</span><span class="sxs-lookup"><span data-stu-id="bc746-580">For more information about user tags, see [User tags](user-tags.md).</span></span>
- <span data-ttu-id="bc746-581">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="bc746-581">**Domain**</span></span>
- <span data-ttu-id="bc746-582">**Type de stratégie**</span><span class="sxs-lookup"><span data-stu-id="bc746-582">**Policy type**</span></span>
- <span data-ttu-id="bc746-583">**Nom de la stratégie** (tableau de détails uniquement)</span><span class="sxs-lookup"><span data-stu-id="bc746-583">**Policy name** (details table only)</span></span>
- <span data-ttu-id="bc746-584">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="bc746-584">**Recipients**</span></span>

<span data-ttu-id="bc746-585">Lorsque vous avez terminé la configuration des filtres, cliquez sur **Appliquer,** **Annuler** ou **Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="bc746-585">When you're finished configuring the filters, click **Apply**, **Cancel**, or **Clear filters**.</span></span>

### <a name="chart-breakdown-by-delivery-status-and-view-data-by-email--phish-or-view-data-by-email--malware"></a><span data-ttu-id="bc746-586">Répartition des graphiques par état de remise et affichage des données par hameçonnage de messagerie ou affichage des données par programme malveillant \> de \> messagerie</span><span class="sxs-lookup"><span data-stu-id="bc746-586">Chart breakdown by Delivery status and View data by Email \> Phish or View data by Email \> Malware</span></span>

![Affichage de l’état de remise du courrier électronique de hameçonnage et des programmes malveillants dans le rapport d’état de la protection contre les menaces](../../media/threat-protection-status-report-phishing-delivery-status-view.png)

<span data-ttu-id="bc746-588">Dans la répartition **du graphique** par état de remise et affichage des données par hameçonnage de messagerie ou affichage des données par affichage des programmes malveillants de messagerie, les informations suivantes sont affichées dans les graphiques : **\>** **\>**</span><span class="sxs-lookup"><span data-stu-id="bc746-588">In the **Chart breakdown by Delivery status** and **View data by Email \> Phish** or **View data by Email \> Malware** views, the following information is shown in the charts:</span></span>

- <span data-ttu-id="bc746-589">**Boîte aux lettres hébergée : Boîte de réception**</span><span class="sxs-lookup"><span data-stu-id="bc746-589">**Hosted mailbox: Inbox**</span></span>
- <span data-ttu-id="bc746-590">**Boîte aux lettres hébergée : courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="bc746-590">**Hosted mailbox: Junk**</span></span>
- <span data-ttu-id="bc746-591">**Boîte aux lettres hébergée : dossier personnalisé**</span><span class="sxs-lookup"><span data-stu-id="bc746-591">**Hosted mailbox: Custom folder**</span></span>
- <span data-ttu-id="bc746-592">**Boîte aux lettres hébergée : éléments supprimés**</span><span class="sxs-lookup"><span data-stu-id="bc746-592">**Hosted mailbox: Deleted items**</span></span>
- <span data-ttu-id="bc746-593">**Forwarded**</span><span class="sxs-lookup"><span data-stu-id="bc746-593">**Forwarded**</span></span>
- <span data-ttu-id="bc746-594">**Serveur local : remis**</span><span class="sxs-lookup"><span data-stu-id="bc746-594">**On-premises server: Delivered**</span></span>
- <span data-ttu-id="bc746-595">**Mise en quarantaine**</span><span class="sxs-lookup"><span data-stu-id="bc746-595">**Quarantine**</span></span>
- <span data-ttu-id="bc746-596">**Échec de remise**</span><span class="sxs-lookup"><span data-stu-id="bc746-596">**Delivery failed**</span></span>
- <span data-ttu-id="bc746-597">**Dropped**</span><span class="sxs-lookup"><span data-stu-id="bc746-597">**Dropped**</span></span>

<span data-ttu-id="bc746-598">Dans le tableau de détails sous le graphique, les informations suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="bc746-598">In the details table below the chart, the following information is available:</span></span>

- <span data-ttu-id="bc746-599">**Date**</span><span class="sxs-lookup"><span data-stu-id="bc746-599">**Date**</span></span>
- <span data-ttu-id="bc746-600">**Subject**</span><span class="sxs-lookup"><span data-stu-id="bc746-600">**Subject**</span></span>
- <span data-ttu-id="bc746-601">**Expéditeur**</span><span class="sxs-lookup"><span data-stu-id="bc746-601">**Sender**</span></span>
- <span data-ttu-id="bc746-602">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="bc746-602">**Recipients**</span></span>
- <span data-ttu-id="bc746-603">**Détecté par**</span><span class="sxs-lookup"><span data-stu-id="bc746-603">**Detected by**</span></span>
- <span data-ttu-id="bc746-604">**État de remise**</span><span class="sxs-lookup"><span data-stu-id="bc746-604">**Delivery Status**</span></span>
- <span data-ttu-id="bc746-605">**Source de compromis**</span><span class="sxs-lookup"><span data-stu-id="bc746-605">**Source of Compromise**</span></span>
- <span data-ttu-id="bc746-606">**Tags**</span><span class="sxs-lookup"><span data-stu-id="bc746-606">**Tags**</span></span>

<span data-ttu-id="bc746-607">Si vous cliquez **sur Filtre,** les filtres suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="bc746-607">If you click **Filter**, the following filters are available:</span></span>

- <span data-ttu-id="bc746-608">**Date (UTC)** **Date de début et** date de **fin**</span><span class="sxs-lookup"><span data-stu-id="bc746-608">**Date (UTC)** **Start date** and **End date**</span></span>
- <span data-ttu-id="bc746-609">**Détection**</span><span class="sxs-lookup"><span data-stu-id="bc746-609">**Detection**</span></span>
- <span data-ttu-id="bc746-610">**Protégé par**: **MDO** (Defender for Office 365) ou **EOP**</span><span class="sxs-lookup"><span data-stu-id="bc746-610">**Protected by**: **MDO** (Defender for Office 365) or **EOP**</span></span>
- <span data-ttu-id="bc746-611">**Direction**</span><span class="sxs-lookup"><span data-stu-id="bc746-611">**Direction**</span></span>
- <span data-ttu-id="bc746-612">**Balise**: filtrer les résultats par utilisateurs ou groupes pour lesquels la balise utilisateur spécifiée a été appliquée (y compris les comptes de priorité).</span><span class="sxs-lookup"><span data-stu-id="bc746-612">**Tag**: Filter the results by users or groups that have had the specified user tag applied (including priority accounts).</span></span> <span data-ttu-id="bc746-613">Pour plus d’informations sur les balises utilisateur, voir [Balises utilisateur.](user-tags.md)</span><span class="sxs-lookup"><span data-stu-id="bc746-613">For more information about user tags, see [User tags](user-tags.md).</span></span>
- <span data-ttu-id="bc746-614">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="bc746-614">**Domain**</span></span>
- <span data-ttu-id="bc746-615">**Type de stratégie**</span><span class="sxs-lookup"><span data-stu-id="bc746-615">**Policy type**</span></span>
- <span data-ttu-id="bc746-616">**Nom de la stratégie** (tableau de détails uniquement)</span><span class="sxs-lookup"><span data-stu-id="bc746-616">**Policy name** (details table only)</span></span>
- <span data-ttu-id="bc746-617">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="bc746-617">**Recipients**</span></span>

<span data-ttu-id="bc746-618">Lorsque vous avez terminé la configuration des filtres, cliquez sur **Appliquer,** **Annuler** ou **Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="bc746-618">When you're finished configuring the filters, click **Apply**, **Cancel**, or **Clear filters**.</span></span>

### <a name="view-data-by-content--malware"></a><span data-ttu-id="bc746-619">Afficher les données par programme malveillant de \> contenu</span><span class="sxs-lookup"><span data-stu-id="bc746-619">View data by Content \> Malware</span></span>

![Affichage des programmes malveillants de contenu dans le rapport d’état de la protection contre les menaces](../../media/threat-protection-status-report-content-malware-view.png)

<span data-ttu-id="bc746-621">Dans la **vue \> Afficher les données par programme** malveillant de contenu, les informations suivantes sont affichées dans le graphique de Microsoft Defender pour Office 365 organisations :</span><span class="sxs-lookup"><span data-stu-id="bc746-621">In the **View data by Content \> Malware** view, the following information is shown in the chart for Microsoft Defender for Office 365 organizations:</span></span>

- <span data-ttu-id="bc746-622">**Moteur anti-programme** malveillant : fichiers malveillants détectés dans Sharepoint, OneDrive et Microsoft Teams par la détection de virus intégrée dans [Microsoft 365](virus-detection-in-spo.md).</span><span class="sxs-lookup"><span data-stu-id="bc746-622">**Anti-malware engine**: Malicious files detected in Sharepoint, OneDrive, and Microsoft Teams by the [built-in virus detection in Microsoft 365](virus-detection-in-spo.md).</span></span>
- <span data-ttu-id="bc746-623">**Détonation de fichiers**: fichiers malveillants détectés par Safe pièces jointes pour [SharePoint, OneDrive et Microsoft Teams](mdo-for-spo-odb-and-teams.md).</span><span class="sxs-lookup"><span data-stu-id="bc746-623">**File detonation**: Malicious files detected by [Safe Attachments for SharePoint, OneDrive, and Microsoft Teams](mdo-for-spo-odb-and-teams.md).</span></span>

<span data-ttu-id="bc746-624">Dans le tableau de détails sous le graphique, les informations suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="bc746-624">In the details table below the chart, the following information is available:</span></span>

- <span data-ttu-id="bc746-625">**Date (UTC)** **Date de début et** date de **fin**</span><span class="sxs-lookup"><span data-stu-id="bc746-625">**Date (UTC)** **Start date** and **End date**</span></span>
- <span data-ttu-id="bc746-626">**Emplacement**</span><span class="sxs-lookup"><span data-stu-id="bc746-626">**Location**</span></span>
- <span data-ttu-id="bc746-627">**Détecté par**</span><span class="sxs-lookup"><span data-stu-id="bc746-627">**Detected by**</span></span>
- <span data-ttu-id="bc746-628">**Nom du programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="bc746-628">**Malware name**</span></span>

<span data-ttu-id="bc746-629">Si vous cliquez **sur Filtre,** les filtres suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="bc746-629">If you click **Filter**, the following filters are available:</span></span>

- <span data-ttu-id="bc746-630">**Date (UTC)** **Date de début et** date de **fin**</span><span class="sxs-lookup"><span data-stu-id="bc746-630">**Date (UTC)** **Start date** and **End date**</span></span>
- <span data-ttu-id="bc746-631">**Détection**: **moteur anti-programme malveillant** ou **détonation de fichiers**</span><span class="sxs-lookup"><span data-stu-id="bc746-631">**Detection**: **Anti-malware engine** or **File detonation**</span></span>

<span data-ttu-id="bc746-632">Lorsque vous avez terminé la configuration des filtres, cliquez sur **Appliquer,** **Annuler** ou **Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="bc746-632">When you're finished configuring the filters, click **Apply**, **Cancel**, or **Clear filters**.</span></span>

### <a name="view-data-by-system-override"></a><span data-ttu-id="bc746-633">Afficher les données par remplacement du système</span><span class="sxs-lookup"><span data-stu-id="bc746-633">View data by System override</span></span>

![Affichage des remplacements de messages dans le rapport d’état de la protection contre les menaces](../../media/threat-protection-status-report-message-override-view.png)

<span data-ttu-id="bc746-635">Dans **l’affichage d’affichage** des données par remplacement du système, les informations de motif de remplacement suivantes sont affichées dans le graphique :</span><span class="sxs-lookup"><span data-stu-id="bc746-635">In the **View data by System override** view, the following override reason information is shown in the chart:</span></span>

- <span data-ttu-id="bc746-636">**Ignorer l’local**</span><span class="sxs-lookup"><span data-stu-id="bc746-636">**On-premises skip**</span></span>
- <span data-ttu-id="bc746-637">**Ip allow**</span><span class="sxs-lookup"><span data-stu-id="bc746-637">**IP allow**</span></span>
- <span data-ttu-id="bc746-638">**Exchange de transport de messagerie** (règle de flux de messagerie)</span><span class="sxs-lookup"><span data-stu-id="bc746-638">**Exchange mail transport rule** (mail flow rule)</span></span>
- <span data-ttu-id="bc746-639">**Expéditeurs autorisés par l’organisation**</span><span class="sxs-lookup"><span data-stu-id="bc746-639">**Organization allowed senders**</span></span>
- <span data-ttu-id="bc746-640">**Domaines autorisés par l’organisation**</span><span class="sxs-lookup"><span data-stu-id="bc746-640">**Organization allowed domains**</span></span>
- <span data-ttu-id="bc746-641">**ZAP non activé**</span><span class="sxs-lookup"><span data-stu-id="bc746-641">**ZAP not enabled**</span></span>
- <span data-ttu-id="bc746-642">**Dossier Courrier indésirable non activé**</span><span class="sxs-lookup"><span data-stu-id="bc746-642">**Junk Mail folder not enabled**</span></span>
- <span data-ttu-id="bc746-643">**Expéditeur Safe utilisateur**</span><span class="sxs-lookup"><span data-stu-id="bc746-643">**User Safe Sender**</span></span>
- <span data-ttu-id="bc746-644">**Domaine Safe utilisateur**</span><span class="sxs-lookup"><span data-stu-id="bc746-644">**User Safe Domain**</span></span>

<span data-ttu-id="bc746-645">Dans le tableau de détails sous le graphique, les informations suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="bc746-645">In the details table below the chart, the following information is available:</span></span>

- <span data-ttu-id="bc746-646">**Date**</span><span class="sxs-lookup"><span data-stu-id="bc746-646">**Date**</span></span>
- <span data-ttu-id="bc746-647">**Subject**</span><span class="sxs-lookup"><span data-stu-id="bc746-647">**Subject**</span></span>
- <span data-ttu-id="bc746-648">**Expéditeur**</span><span class="sxs-lookup"><span data-stu-id="bc746-648">**Sender**</span></span>
- <span data-ttu-id="bc746-649">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="bc746-649">**Recipients**</span></span>
- <span data-ttu-id="bc746-650">**Détecté par**</span><span class="sxs-lookup"><span data-stu-id="bc746-650">**Detected by**</span></span>
- <span data-ttu-id="bc746-651">**État de remise**</span><span class="sxs-lookup"><span data-stu-id="bc746-651">**Delivery Status**</span></span>
- <span data-ttu-id="bc746-652">**Source de compromis**</span><span class="sxs-lookup"><span data-stu-id="bc746-652">**Source of Compromise**</span></span>
- <span data-ttu-id="bc746-653">**Tags**</span><span class="sxs-lookup"><span data-stu-id="bc746-653">**Tags**</span></span>

<span data-ttu-id="bc746-654">Si vous cliquez **sur Filtre,** les filtres suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="bc746-654">If you click **Filter**, the following filters are available:</span></span>

- <span data-ttu-id="bc746-655">**Date (UTC)** **Date de début et** date de **fin**</span><span class="sxs-lookup"><span data-stu-id="bc746-655">**Date (UTC)** **Start date** and **End date**</span></span>
- <span data-ttu-id="bc746-656">**Détection**</span><span class="sxs-lookup"><span data-stu-id="bc746-656">**Detection**</span></span>
- <span data-ttu-id="bc746-657">**Protégé par**: **MDO** (Defender for Office 365) ou **EOP**</span><span class="sxs-lookup"><span data-stu-id="bc746-657">**Protected by**: **MDO** (Defender for Office 365) or **EOP**</span></span>
- <span data-ttu-id="bc746-658">**Direction**</span><span class="sxs-lookup"><span data-stu-id="bc746-658">**Direction**</span></span>
- <span data-ttu-id="bc746-659">**Balise**: filtrer les résultats par utilisateurs ou groupes pour lesquels la balise utilisateur spécifiée a été appliquée (y compris les comptes de priorité).</span><span class="sxs-lookup"><span data-stu-id="bc746-659">**Tag**: Filter the results by users or groups that have had the specified user tag applied (including priority accounts).</span></span> <span data-ttu-id="bc746-660">Pour plus d’informations sur les balises utilisateur, voir [Balises utilisateur.](user-tags.md)</span><span class="sxs-lookup"><span data-stu-id="bc746-660">For more information about user tags, see [User tags](user-tags.md).</span></span>
- <span data-ttu-id="bc746-661">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="bc746-661">**Domain**</span></span>
- <span data-ttu-id="bc746-662">**Type de stratégie**</span><span class="sxs-lookup"><span data-stu-id="bc746-662">**Policy type**</span></span>
- <span data-ttu-id="bc746-663">**Nom de la stratégie** (tableau de détails uniquement)</span><span class="sxs-lookup"><span data-stu-id="bc746-663">**Policy name** (details table only)</span></span>
- <span data-ttu-id="bc746-664">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="bc746-664">**Recipients**</span></span>

<span data-ttu-id="bc746-665">Lorsque vous avez terminé la configuration des filtres, cliquez sur **Appliquer,** **Annuler** ou **Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="bc746-665">When you're finished configuring the filters, click **Apply**, **Cancel**, or **Clear filters**.</span></span>

<span data-ttu-id="bc746-666"><sup>\*</sup>Defender pour Office 365 uniquement</span><span class="sxs-lookup"><span data-stu-id="bc746-666"><sup>\*</sup> Defender for Office 365 only</span></span>

## <a name="top-malware-report"></a><span data-ttu-id="bc746-667">Principaux rapports sur les programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="bc746-667">Top malware report</span></span>

<span data-ttu-id="bc746-668">Le **rapport des principaux programmes** malveillants présente les différents types de programmes malveillants détectés par la protection [anti-programme malveillant dans EOP.](anti-malware-protection.md)</span><span class="sxs-lookup"><span data-stu-id="bc746-668">The **Top malware** report shows the various kinds of malware that was detected by [anti-malware protection in EOP](anti-malware-protection.md).</span></span>

<span data-ttu-id="bc746-669">Pour afficher le rapport dans le portail  Microsoft 365 Defender, consultez la & collaboration de rapports e-mail \>  \> **& rapports de collaboration.**</span><span class="sxs-lookup"><span data-stu-id="bc746-669">To view the report in the Microsoft 365 Defender portal, go to **Reports** \> **Email & collaboration** \> **Email & collaboration reports**.</span></span> <span data-ttu-id="bc746-670">Dans la page **Rapports de collaboration & courrier** électronique, recherchez **les** principaux programmes malveillants, puis cliquez sur Afficher **les détails.**</span><span class="sxs-lookup"><span data-stu-id="bc746-670">On the **Email & collaboration reports** page, find **Top malware** and then click **View details**.</span></span> <span data-ttu-id="bc746-671">Pour aller directement dans le rapport, ouvrez <https://security.microsoft.com/reports/TopMalware> .</span><span class="sxs-lookup"><span data-stu-id="bc746-671">To go directly to the report, open <https://security.microsoft.com/reports/TopMalware>.</span></span>

![Widget de programmes malveillants de premier niveau sur la page rapports de collaboration & messagerie](../../media/top-malware-report-widget.png)

<span data-ttu-id="bc746-673">Lorsque vous pointez sur une souris dans le graphique en secteurs, vous pouvez voir le nom d’un type de programme malveillant et le nombre de messages détectés comme ayant ce programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="bc746-673">When you hover over a wedge in the pie chart, you can see the name of a kind of malware and how many messages were detected as having that malware.</span></span>

<span data-ttu-id="bc746-674">Dans la page **Rapport de programmes malveillants supérieure,** une version plus grande du graphique en secteurs s’affiche sur la page de rapport. Le tableau de détails sous le graphique présente les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="bc746-674">On the **Top malware report** page, a larger version of the pie chart is displayed on the report page.The details table below the chart shows the following information:</span></span>

- <span data-ttu-id="bc746-675">**Principaux programmes malveillants**</span><span class="sxs-lookup"><span data-stu-id="bc746-675">**Top malware**</span></span>
- <span data-ttu-id="bc746-676">**Count**</span><span class="sxs-lookup"><span data-stu-id="bc746-676">**Count**</span></span>

<span data-ttu-id="bc746-677">Si vous cliquez **sur Filtre,** vous pouvez spécifier une plage de dates avec la **date de** début et la date **de fin.**</span><span class="sxs-lookup"><span data-stu-id="bc746-677">If you click **Filter**, you can specify a date range with **Start date** and **End date**.</span></span>

![Affichage du rapport sur les programmes malveillants le plus haut](../../media/top-malware-report-view.png)

## <a name="url-threat-protection-report"></a><span data-ttu-id="bc746-679">Rapport sur la protection contre les menaces d’URL</span><span class="sxs-lookup"><span data-stu-id="bc746-679">URL threat protection report</span></span>

<span data-ttu-id="bc746-680">Le **rapport sur la protection contre les menaces d’URL** est disponible uniquement dans Microsoft Defender Office 365.</span><span class="sxs-lookup"><span data-stu-id="bc746-680">The **URL threat protection report** is available only in Microsoft Defender for Office 365.</span></span> <span data-ttu-id="bc746-681">Pour plus d’informations, voir le rapport sur la [protection contre les menaces d’URL.](view-reports-for-mdo.md#url-threat-protection-report)</span><span class="sxs-lookup"><span data-stu-id="bc746-681">For more information, see [URL threat protection report](view-reports-for-mdo.md#url-threat-protection-report).</span></span>

## <a name="user-reported-messages-report"></a><span data-ttu-id="bc746-682">Rapport des messages signalés par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="bc746-682">User reported messages report</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bc746-683">Pour que le rapport des **messages** signalés par l’utilisateur fonctionne correctement, l’enregistrement **d’audit** doit être Microsoft 365 votre environnement.</span><span class="sxs-lookup"><span data-stu-id="bc746-683">In order for the **User reported messages** report to work correctly, **audit logging must be turned on** for your Microsoft 365 environment.</span></span> <span data-ttu-id="bc746-684">Cette tâche est généralement effectuée par une personne dont le rôle Journaux d’audit est Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="bc746-684">This is typically done by someone who has the Audit Logs role assigned in Exchange Online.</span></span> <span data-ttu-id="bc746-685">Pour plus d’informations, [voir Turn Microsoft 365 audit log search on or off](../../compliance/turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="bc746-685">For more information, see [Turn Microsoft 365 audit log search on or off](../../compliance/turn-audit-log-search-on-or-off.md).</span></span>

<span data-ttu-id="bc746-686">Le rapport des **messages** signalés par l’utilisateur affiche des informations sur les messages électroniques que les utilisateurs ont signalés comme courrier indésirable, tentatives d’hameçonnage ou courrier de qualité à l’aide du module complémentaire Signaler un [message](enable-the-report-message-add-in.md) ou signaler le hameçonnage. [](enable-the-report-phish-add-in.md)</span><span class="sxs-lookup"><span data-stu-id="bc746-686">The **User reported messages** report shows information about email messages that users have reported as junk, phishing attempts, or good mail by using the [Report Message add-in](enable-the-report-message-add-in.md) or the [Report Phishing add-in](enable-the-report-phish-add-in.md).</span></span>

<span data-ttu-id="bc746-687">Pour afficher le rapport dans le portail  Microsoft 365 Defender, consultez la & collaboration de rapports e-mail \>  \> **& rapports de collaboration.**</span><span class="sxs-lookup"><span data-stu-id="bc746-687">To view the report in the Microsoft 365 Defender portal, go to **Reports** \> **Email & collaboration** \> **Email & collaboration reports**.</span></span> <span data-ttu-id="bc746-688">Dans la page **& de collaboration,** recherchez les **messages** signalés par l’utilisateur, puis cliquez sur Afficher **les détails.**</span><span class="sxs-lookup"><span data-stu-id="bc746-688">On the **Email & collaboration reports** page, find **User reported messages** and then click **View details**.</span></span> <span data-ttu-id="bc746-689">Pour aller directement dans le rapport, ouvrez <https://security.microsoft.com/reports/userSubmissionReport> .</span><span class="sxs-lookup"><span data-stu-id="bc746-689">To go directly to the report, open <https://security.microsoft.com/reports/userSubmissionReport>.</span></span> <span data-ttu-id="bc746-690">Pour aller aux [soumissions d’administrateur dans le portail Microsoft 365 Defender,](admin-submission.md)cliquez **sur Go to Submissions**.</span><span class="sxs-lookup"><span data-stu-id="bc746-690">To go to [admin submissions in the Microsoft 365 Defender portal](admin-submission.md), click **Go to Submissions**.</span></span>

![Widget de messages signalés par l’utilisateur sur la page rapports de collaboration & courrier électronique](../../media/user-reported-messages-widget.png)

<span data-ttu-id="bc746-692">Dans **la** page Messages signalés par l’utilisateur, vous pouvez  filtrer à la fois le graphique et le tableau de détails en cliquant sur Filtrer et en sélectionnant une ou plusieurs des valeurs suivantes dans le volant qui s’affiche :</span><span class="sxs-lookup"><span data-stu-id="bc746-692">On the **User reported messages** page, you can filter both the chart and the details table by clicking **Filter** and selecting one or more of the following values in the flyout that appears:</span></span>

- <span data-ttu-id="bc746-693">**Date signalée :** **heure de début** et heure de **fin**</span><span class="sxs-lookup"><span data-stu-id="bc746-693">**Date reported**: **Start time** and **End time**</span></span>
- <span data-ttu-id="bc746-694">**Auteur du rapport**</span><span class="sxs-lookup"><span data-stu-id="bc746-694">**Reported by**</span></span>
- <span data-ttu-id="bc746-695">**Sujet de l’e-mail**</span><span class="sxs-lookup"><span data-stu-id="bc746-695">**Email subject**</span></span>
- <span data-ttu-id="bc746-696">**ID de message signalé**</span><span class="sxs-lookup"><span data-stu-id="bc746-696">**Message reported ID**</span></span>
- <span data-ttu-id="bc746-697">**ID de message réseau**</span><span class="sxs-lookup"><span data-stu-id="bc746-697">**Network Message ID**</span></span>
- <span data-ttu-id="bc746-698">**Sender**</span><span class="sxs-lookup"><span data-stu-id="bc746-698">**Sender**</span></span>
- <span data-ttu-id="bc746-699">**Raison signalée**</span><span class="sxs-lookup"><span data-stu-id="bc746-699">**Reported reason**</span></span>
  - <span data-ttu-id="bc746-700">**Non indésirable**</span><span class="sxs-lookup"><span data-stu-id="bc746-700">**Not junk**</span></span>
  - <span data-ttu-id="bc746-701">**Hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="bc746-701">**Phish**</span></span>
  - <span data-ttu-id="bc746-702">**Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="bc746-702">**Spam**</span></span>
- <span data-ttu-id="bc746-703">**Simulation de hameçonnage**: **Oui** ou **Non**</span><span class="sxs-lookup"><span data-stu-id="bc746-703">**Phish simulation**: **Yes** or **No**</span></span>

<span data-ttu-id="bc746-704">Lorsque vous avez terminé la configuration des filtres, cliquez sur **Appliquer,** **Annuler** ou **Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="bc746-704">When you're finished configuring the filters, click **Apply**, **Cancel**, or **Clear filters**.</span></span>

<span data-ttu-id="bc746-705">Pour grouper les entrées, cliquez sur **Grouper** et sélectionnez l’une des valeurs suivantes dans la liste suivante :</span><span class="sxs-lookup"><span data-stu-id="bc746-705">To group the entries, click **Group** and select one of the following values from the drop down list:</span></span>

- <span data-ttu-id="bc746-706">**Aucune**</span><span class="sxs-lookup"><span data-stu-id="bc746-706">**None**</span></span>
- <span data-ttu-id="bc746-707">**Raison**</span><span class="sxs-lookup"><span data-stu-id="bc746-707">**Reason**</span></span>
- <span data-ttu-id="bc746-708">**Sender**</span><span class="sxs-lookup"><span data-stu-id="bc746-708">**Sender**</span></span>
- <span data-ttu-id="bc746-709">**Auteur du rapport**</span><span class="sxs-lookup"><span data-stu-id="bc746-709">**Reported by**</span></span>
- <span data-ttu-id="bc746-710">**Résultat rescan**</span><span class="sxs-lookup"><span data-stu-id="bc746-710">**Rescan result**</span></span>
- <span data-ttu-id="bc746-711">**Simulation de hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="bc746-711">**Phish simulation**</span></span>

![Rapport des messages signalés par l’utilisateur](../../media/user-reported-messages-report.png)

<span data-ttu-id="bc746-713">Dans le tableau de détails sous le graphique, vous pouvez voir les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="bc746-713">In the details table below the graph, you can see the following details:</span></span>

- <span data-ttu-id="bc746-714">**Sujet de l’e-mail**</span><span class="sxs-lookup"><span data-stu-id="bc746-714">**Email subject**</span></span>
- <span data-ttu-id="bc746-715">**Auteur du rapport**</span><span class="sxs-lookup"><span data-stu-id="bc746-715">**Reported by**</span></span>
- <span data-ttu-id="bc746-716">**Date de rapport**</span><span class="sxs-lookup"><span data-stu-id="bc746-716">**Date reported**</span></span>
- <span data-ttu-id="bc746-717">**Sender**</span><span class="sxs-lookup"><span data-stu-id="bc746-717">**Sender**</span></span>
- <span data-ttu-id="bc746-718">**Raison signalée**</span><span class="sxs-lookup"><span data-stu-id="bc746-718">**Reported reason**</span></span>
- <span data-ttu-id="bc746-719">**Résultat rescan**</span><span class="sxs-lookup"><span data-stu-id="bc746-719">**Rescan result**</span></span>
- <span data-ttu-id="bc746-720">**Tags**</span><span class="sxs-lookup"><span data-stu-id="bc746-720">**Tags**</span></span>

<span data-ttu-id="bc746-721">Pour envoyer un message à Microsoft pour analyse, sélectionnez l’entrée du message dans le tableau, cliquez sur Envoyer à **Microsoft** pour analyse, puis sélectionnez l’une des valeurs suivantes dans la liste liste suivante :</span><span class="sxs-lookup"><span data-stu-id="bc746-721">To submit a message to Microsoft for analysis, select the message entry from the table, click **Submit to Microsoft for analysis** and then select one of the following values from the drop down list:</span></span>

- <span data-ttu-id="bc746-722">**Signaler propre**</span><span class="sxs-lookup"><span data-stu-id="bc746-722">**Report clean**</span></span>
- <span data-ttu-id="bc746-723">**Signaler le hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="bc746-723">**Report phishing**</span></span>
- <span data-ttu-id="bc746-724">**Signaler un programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="bc746-724">**Report malware**</span></span>
- <span data-ttu-id="bc746-725">**Signaler le courrier indésirable**'</span><span class="sxs-lookup"><span data-stu-id="bc746-725">**Report spam**'</span></span>
- <span data-ttu-id="bc746-726">**Examen du déclencheur** (Defender for Office 365)</span><span class="sxs-lookup"><span data-stu-id="bc746-726">**Trigger investigation** (Defender for Office 365)</span></span>

## <a name="what-permissions-are-needed-to-view-these-reports"></a><span data-ttu-id="bc746-727">Quelles autorisations sont nécessaires pour afficher ces rapports ?</span><span class="sxs-lookup"><span data-stu-id="bc746-727">What permissions are needed to view these reports?</span></span>

<span data-ttu-id="bc746-728">Pour afficher et utiliser les rapports décrits dans cet article, vous devez être membre de l’un des groupes de rôles suivants dans le portail Microsoft 365 Defender:</span><span class="sxs-lookup"><span data-stu-id="bc746-728">In order to view and use the reports described in this article, you need to be a member of one of the following role groups in the Microsoft 365 Defender portal:</span></span>

- <span data-ttu-id="bc746-729">**Gestion de l'organisation**</span><span class="sxs-lookup"><span data-stu-id="bc746-729">**Organization Management**</span></span>
- <span data-ttu-id="bc746-730">**Administrateur de sécurité**</span><span class="sxs-lookup"><span data-stu-id="bc746-730">**Security Administrator**</span></span>
- <span data-ttu-id="bc746-731">**Lecteur sécurité**</span><span class="sxs-lookup"><span data-stu-id="bc746-731">**Security Reader**</span></span>
- <span data-ttu-id="bc746-732">**Lecteur global**</span><span class="sxs-lookup"><span data-stu-id="bc746-732">**Global Reader**</span></span>

<span data-ttu-id="bc746-733">Pour plus d’informations, [voir Autorisations dans le portail Microsoft 365 Defender.](permissions-in-the-security-and-compliance-center.md)</span><span class="sxs-lookup"><span data-stu-id="bc746-733">For more information, see [Permissions in the Microsoft 365 Defender portal](permissions-in-the-security-and-compliance-center.md).</span></span>

<span data-ttu-id="bc746-734">**Remarque**: l’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux  utilisateurs les autorisations requises dans le portail Microsoft 365 Defender et les autorisations pour d’autres fonctionnalités dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="bc746-734">**Note**: Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions in the Microsoft 365 Defender portal _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="bc746-735">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="bc746-735">For more information, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>

## <a name="what-if-the-reports-arent-showing-data"></a><span data-ttu-id="bc746-736">Que se passe-t-il si les rapports n’affichent pas de données ?</span><span class="sxs-lookup"><span data-stu-id="bc746-736">What if the reports aren't showing data?</span></span>

<span data-ttu-id="bc746-737">Si vous ne voyez pas de données dans vos rapports, vérifiez que vos stratégies sont correctement définies.</span><span class="sxs-lookup"><span data-stu-id="bc746-737">If you are not seeing data in your reports, double-check that your policies are set up correctly.</span></span> <span data-ttu-id="bc746-738">Pour en savoir plus, [consultez La protection contre les menaces.](protect-against-threats.md)</span><span class="sxs-lookup"><span data-stu-id="bc746-738">To learn more, see [Protect against threats](protect-against-threats.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc746-739">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc746-739">Related topics</span></span>

[<span data-ttu-id="bc746-740">Protection contre le courrier indésirable et les programmes malveillants dans EOP</span><span class="sxs-lookup"><span data-stu-id="bc746-740">Anti-spam and anti-malware protection in EOP</span></span>](anti-spam-and-anti-malware-protection.md)

[<span data-ttu-id="bc746-741">Rapports intelligents et informations sur le portail Microsoft 365 Defender web</span><span class="sxs-lookup"><span data-stu-id="bc746-741">Smart reports and insights in the Microsoft 365 Defender portal</span></span>](reports-and-insights-in-security-and-compliance.md)

[<span data-ttu-id="bc746-742">Afficher les rapports de flux de messagerie dans le portail Microsoft 365 Defender messagerie</span><span class="sxs-lookup"><span data-stu-id="bc746-742">View mail flow reports in the Microsoft 365 Defender portal</span></span>](view-mail-flow-reports.md)

[<span data-ttu-id="bc746-743">Afficher des rapports pour Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="bc746-743">View reports for Defender for Office 365</span></span>](view-reports-for-mdo.md)
