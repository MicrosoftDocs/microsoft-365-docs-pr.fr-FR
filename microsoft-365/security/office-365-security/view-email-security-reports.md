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
ms.openlocfilehash: f3dcf533c232a89adf0dc1ff3fcc7c2ca4fc5d8f
ms.sourcegitcommit: bc64d9f619259bd0a94e43a9010aae5cffb4d6c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "53022910"
---
# <a name="view-email-security-reports-in-the-microsoft-365-defender-portal"></a><span data-ttu-id="20586-103">Afficher les rapports de sécurité du courrier électronique dans le portail Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="20586-103">View email security reports in the Microsoft 365 Defender portal</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="20586-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="20586-104">**Applies to**</span></span>
- [<span data-ttu-id="20586-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="20586-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="20586-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="20586-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="20586-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="20586-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="20586-108">De nombreux rapports sont disponibles sur le portail Microsoft 365 Defender pour vous aider à voir comment les fonctionnalités de sécurité du courrier électronique, telles que les fonctionnalités anti-courrier indésirable, anti-programme malveillant et de chiffrement dans <https://security.microsoft.com> Microsoft 365, protègent votre organisation.</span><span class="sxs-lookup"><span data-stu-id="20586-108">A variety of reports are available in the Microsoft 365 Defender portal at <https://security.microsoft.com> to help you see how email security features, such as anti-spam, anti-malware, and encryption features in Microsoft 365 are protecting your organization.</span></span> <span data-ttu-id="20586-109">Si vous avez les [autorisations](#what-permissions-are-needed-to-view-these-reports)nécessaires, vous pouvez afficher ces rapports dans  le portail Microsoft 365 Defender en allant dans Rapports e-mail & \> **collaboration** \> **e-mail & rapports de collaboration.**</span><span class="sxs-lookup"><span data-stu-id="20586-109">If you have the [necessary permissions](#what-permissions-are-needed-to-view-these-reports), you can view these reports in the Microsoft 365 Defender portal by going to **Reports** \> **Email & collaboration** \> **Email & collaboration reports**.</span></span> <span data-ttu-id="20586-110">Pour aller directement à la page **e-mail & rapports** de collaboration, ouvrez <https://security.microsoft.com/emailandcollabreport> .</span><span class="sxs-lookup"><span data-stu-id="20586-110">To go directly to the **Email & collaboration reports** page, open <https://security.microsoft.com/emailandcollabreport>.</span></span>

![Page de & de collaboration par courrier électronique dans le portail Microsoft 365 Defender](../../media/email-collaboration-reports.png)

> [!NOTE]
>
> <span data-ttu-id="20586-112">Certains rapports de la page rapports de collaboration & **courrier** électronique nécessitent Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="20586-112">Some of the reports on the **Email & collaboration reports** page require Microsoft Defender for Office 365.</span></span> <span data-ttu-id="20586-113">Pour plus d’informations sur ces rapports, voir les rapports View Defender pour Office 365 dans le portail [Microsoft 365 Defender.](view-reports-for-mdo.md)</span><span class="sxs-lookup"><span data-stu-id="20586-113">For information about these reports, see [View Defender for Office 365 reports in the Microsoft 365 Defender portal](view-reports-for-mdo.md).</span></span>
>
> <span data-ttu-id="20586-114">Les rapports liés au flux de messagerie sont désormais dans le Centre d’administration Exchange (EAC).</span><span class="sxs-lookup"><span data-stu-id="20586-114">Reports that are related to mail flow are now in the Exchange admin center (EAC).</span></span> <span data-ttu-id="20586-115">Pour plus d’informations sur ces rapports, voir Rapports de [flux de messagerie dans le nouveau Centre d’administration Exchange.](/exchange/monitoring/mail-flow-reports/mail-flow-reports)</span><span class="sxs-lookup"><span data-stu-id="20586-115">For more information about these reports, see [Mail flow reports in the new Exchange admin center](/exchange/monitoring/mail-flow-reports/mail-flow-reports).</span></span>

## <a name="compromised-users-report"></a><span data-ttu-id="20586-116">Rapport utilisateurs compromis</span><span class="sxs-lookup"><span data-stu-id="20586-116">Compromised users report</span></span>

> [!NOTE]
> <span data-ttu-id="20586-117">Ce rapport est disponible dans les organisations Microsoft 365 avec des boîtes aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="20586-117">This report is available in Microsoft 365 organizations with Exchange Online mailboxes.</span></span> <span data-ttu-id="20586-118">Il n’est pas disponible dans les organisations Exchange Online Protection (EOP) autonomes.</span><span class="sxs-lookup"><span data-stu-id="20586-118">It's not available in standalone Exchange Online Protection (EOP) organizations.</span></span>

<span data-ttu-id="20586-119">Le **rapport Utilisateurs** compromis indique le nombre de  comptes  d’utilisateurs marqués comme suspects ou restreints au cours des 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="20586-119">The **Compromised users** report shows shows the number of user accounts that were marked as **Suspicious** or **Restricted** within the last 7 days.</span></span> <span data-ttu-id="20586-120">Les comptes dans l’un de ces états sont problématiques, voire compromis.</span><span class="sxs-lookup"><span data-stu-id="20586-120">Accounts in either of these states are problematic or even compromised.</span></span> <span data-ttu-id="20586-121">Avec une utilisation fréquente, vous pouvez utiliser le rapport pour repérer des pics, voire des tendances, dans des comptes suspects ou restreints.</span><span class="sxs-lookup"><span data-stu-id="20586-121">With frequent use, you can use the report to spot spikes, and even trends, in suspicious or restricted accounts.</span></span> <span data-ttu-id="20586-122">Pour plus d’informations sur les utilisateurs compromis, voir [Répondre à un compte de messagerie compromis.](responding-to-a-compromised-email-account.md)</span><span class="sxs-lookup"><span data-stu-id="20586-122">For more information about compromised users, see [Responding to a compromised email account](responding-to-a-compromised-email-account.md).</span></span>

![Widget Utilisateurs compromis sur la page rapports de collaboration & messagerie](../../media/compromised-users-report-widget.png)

<span data-ttu-id="20586-124">L’affichage agrégé affiche les données des 90 derniers jours et l’affichage détail affiche les données des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="20586-124">The aggregate view shows data for the last 90 days and the detail view shows data for the last 30 days.</span></span>

<span data-ttu-id="20586-125">Pour afficher le rapport dans le portail Microsoft  365 Defender, consultez La boîte aux & collaboration de rapports e-mail \>  \> **& rapports de collaboration.**</span><span class="sxs-lookup"><span data-stu-id="20586-125">To view the report in the Microsoft 365 Defender portal, go to **Reports** \> **Email & collaboration** \> **Email & collaboration reports**.</span></span> <span data-ttu-id="20586-126">Dans la page **& de collaboration,** recherchez les utilisateurs **compromis,** puis cliquez sur Afficher **les détails.**</span><span class="sxs-lookup"><span data-stu-id="20586-126">On the **Email & collaboration reports** page, find **Compromised users** and then click **View details**.</span></span> <span data-ttu-id="20586-127">Pour aller directement dans le rapport, ouvrez <https://security.microsoft.com/reports/CompromisedUsers> .</span><span class="sxs-lookup"><span data-stu-id="20586-127">To go directly to the report, open <https://security.microsoft.com/reports/CompromisedUsers>.</span></span>

<span data-ttu-id="20586-128">Dans **la** page Utilisateurs compromis, vous pouvez filtrer le  graphique et le tableau de détails en cliquant sur Filtrer et en sélectionnant une ou plusieurs des valeurs suivantes dans le volant qui s’affiche :</span><span class="sxs-lookup"><span data-stu-id="20586-128">On the **Compromised users** page, you can filter both the chart and the details table by clicking **Filter** and selecting one or more of the following values in the flyout that appears:</span></span>

- <span data-ttu-id="20586-129">**Date (UTC)**: **date de début** et date de **fin.**</span><span class="sxs-lookup"><span data-stu-id="20586-129">**Date (UTC)**: **Start date** and **End date**.</span></span>
- <span data-ttu-id="20586-130">**Activité**:</span><span class="sxs-lookup"><span data-stu-id="20586-130">**Activity**:</span></span>
  - <span data-ttu-id="20586-131">**Suspect**: le compte d’utilisateur a envoyé des messages suspects et risque d’être limité à l’envoi de courriers électroniques.</span><span class="sxs-lookup"><span data-stu-id="20586-131">**Suspicious**: The user account has sent suspicious email and is at risk of being restricted from sending email.</span></span>
  - <span data-ttu-id="20586-132">**Restreint :** le compte d’utilisateur n’a pas pu envoyer de courrier électronique en raison de modèles hautement suspects.</span><span class="sxs-lookup"><span data-stu-id="20586-132">**Restricted**: The user account has been restricted from sending email due to highly suspicious patterns.</span></span>

<span data-ttu-id="20586-133">Lorsque vous avez terminé la configuration des filtres, cliquez sur **Appliquer,** **Annuler** ou **Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="20586-133">When you're finished configuring the filters, click **Apply**, **Cancel**, or **Clear filters**.</span></span>

![Affichage du rapport dans le rapport Utilisateurs compromis](../../media/compromised-users-report-activity-view.png)

<span data-ttu-id="20586-135">Dans le tableau de détails sous le graphique, vous pouvez voir les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="20586-135">In the details table below the graph, you can see the following details:</span></span>

- <span data-ttu-id="20586-136">**Heure de création**</span><span class="sxs-lookup"><span data-stu-id="20586-136">**Creation time**</span></span>
- <span data-ttu-id="20586-137">**ID d'utilisateur**</span><span class="sxs-lookup"><span data-stu-id="20586-137">**User ID**</span></span>
- <span data-ttu-id="20586-138">**Action**</span><span class="sxs-lookup"><span data-stu-id="20586-138">**Action**</span></span>

## <a name="exchange-transport-rule-report"></a><span data-ttu-id="20586-139">Rapport de règles de transport Exchange</span><span class="sxs-lookup"><span data-stu-id="20586-139">Exchange transport rule report</span></span>

<span data-ttu-id="20586-140">Le **rapport des règles** de transport Exchange indique l’effet des règles de flux de messagerie (également appelées règles de transport) sur les messages entrants et sortants dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="20586-140">The **Exchange transport rule** report shows the effect of mail flow rules (also known as transport rules) on incoming and outgoing messages in your organization.</span></span>

<span data-ttu-id="20586-141">Pour afficher le rapport dans le portail Microsoft  365 Defender, consultez La boîte aux & collaboration de rapports e-mail \>  \> **& rapports de collaboration.**</span><span class="sxs-lookup"><span data-stu-id="20586-141">To view the report in the Microsoft 365 Defender portal, go to **Reports** \> **Email & collaboration** \> **Email & collaboration reports**.</span></span> <span data-ttu-id="20586-142">Dans la page **Rapports de collaboration & courrier** électronique, recherchez la règle de transport **Exchange,** puis cliquez sur **Afficher les détails.**</span><span class="sxs-lookup"><span data-stu-id="20586-142">On the **Email & collaboration reports** page, find **Exchange transport rule** and then click **View details**.</span></span> <span data-ttu-id="20586-143">Pour aller directement dans le rapport, ouvrez <https://security.microsoft.com/reports/ETRRuleReport> .</span><span class="sxs-lookup"><span data-stu-id="20586-143">To go directly to the report, open <https://security.microsoft.com/reports/ETRRuleReport>.</span></span>

![Widget de règles de transport Exchange dans la page rapports de collaboration & courrier électronique](../../media/transport-rule-report-widget.png)

<span data-ttu-id="20586-145">Dans la page rapport des règles de **transport Exchange,** les graphiques et données disponibles sont décrits dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="20586-145">On the **Exchange transport rule report** page, the available charts and data are described in the following sections.</span></span>

### <a name="chart-breakdown-by-direction"></a><span data-ttu-id="20586-146">Répartition du graphique par direction</span><span class="sxs-lookup"><span data-stu-id="20586-146">Chart breakdown by Direction</span></span>

![Affichage direction pour les règles de transport Exchange dans le rapport de règles de transport Exchange](../../media/transport-rule-report-etr-direction-view.png)

<span data-ttu-id="20586-148">Si vous sélectionnez **répartition des graphiques par direction,** les graphiques suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="20586-148">If you select **Chart breakdown by Direction**, the follow charts are available:</span></span>

- <span data-ttu-id="20586-149">**Afficher les données par règles**  de transport Exchange : nombre de **messages** entrants et sortants affectés par les règles de flux de messagerie.</span><span class="sxs-lookup"><span data-stu-id="20586-149">**View data by Exchange transport rules**: The number of **Inbound** and **Outbound** messages that were affected by mail flow rules.</span></span>
- <span data-ttu-id="20586-150">Afficher les données par règles de  **transport Exchange DLP**: nombre de **messages** entrants et sortants affectés par les règles de flux de messagerie de protection contre la perte de données (DLP).</span><span class="sxs-lookup"><span data-stu-id="20586-150">**View data by DLP Exchange transport rules**: The number of **Inbound** and **Outbound** messages that were affected by data loss prevention (DLP) mail flow rules.</span></span>

<span data-ttu-id="20586-151">Les informations suivantes sont affichées dans le tableau de détails sous le graphique :</span><span class="sxs-lookup"><span data-stu-id="20586-151">The following information is shown in the details table below the graph:</span></span>

- <span data-ttu-id="20586-152">**Date**</span><span class="sxs-lookup"><span data-stu-id="20586-152">**Date**</span></span>
- <span data-ttu-id="20586-153">**Stratégie DLP** ( Afficher les données par les règles de **transport Exchange DLP** uniquement)</span><span class="sxs-lookup"><span data-stu-id="20586-153">**DLP policy** (**View data by DLP Exchange transport rules** only)</span></span>
- <span data-ttu-id="20586-154">**Règle de transport**</span><span class="sxs-lookup"><span data-stu-id="20586-154">**Transport rule**</span></span>
- <span data-ttu-id="20586-155">**Subject**</span><span class="sxs-lookup"><span data-stu-id="20586-155">**Subject**</span></span>
- <span data-ttu-id="20586-156">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="20586-156">**Sender address**</span></span>
- <span data-ttu-id="20586-157">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="20586-157">**Recipient address**</span></span>
- <span data-ttu-id="20586-158">**Gravité**</span><span class="sxs-lookup"><span data-stu-id="20586-158">**Severity**</span></span>
- <span data-ttu-id="20586-159">**Direction**</span><span class="sxs-lookup"><span data-stu-id="20586-159">**Direction**</span></span>

<span data-ttu-id="20586-160">Vous pouvez filtrer le graphique et le tableau de détails en cliquant sur **Filtrer** et en sélectionnant une ou plusieurs des valeurs suivantes dans le volant qui s’affiche :</span><span class="sxs-lookup"><span data-stu-id="20586-160">You can filter both the chart and the details table by clicking **Filter** and selecting one or more of the following values in the flyout that appears:</span></span>

- <span data-ttu-id="20586-161">**Date (UTC)** **Date de début et** date de **fin**</span><span class="sxs-lookup"><span data-stu-id="20586-161">**Date (UTC)** **Start date** and **End date**</span></span>
- <span data-ttu-id="20586-162">**Direction**: **sortant et** **entrant**</span><span class="sxs-lookup"><span data-stu-id="20586-162">**Direction**: **Outbound** and **Inbound**</span></span>
- <span data-ttu-id="20586-163">**Gravité :** **gravité élevée,** **gravité moyenne** et gravité **faible**</span><span class="sxs-lookup"><span data-stu-id="20586-163">**Severity**: **High severity**, **Medium severity**, and **Low severity**</span></span>

<span data-ttu-id="20586-164">Lorsque vous avez terminé la configuration des filtres, cliquez sur **Appliquer,** **Annuler** ou **Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="20586-164">When you're finished configuring the filters, click **Apply**, **Cancel**, or **Clear filters**.</span></span>

### <a name="chart-breakdown-by-severity"></a><span data-ttu-id="20586-165">Répartition du graphique par gravité</span><span class="sxs-lookup"><span data-stu-id="20586-165">Chart breakdown by Severity</span></span>

![Affichage gravité des règles de transport Exchange dans le rapport des règles de transport Exchange](../../media/transport-rule-report-etr-severity-view.png)

<span data-ttu-id="20586-167">Si vous sélectionnez **répartition des graphiques par gravité,** les graphiques suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="20586-167">If you select **Chart breakdown by Severity**, the follow charts are available:</span></span>

- <span data-ttu-id="20586-168">**Afficher les données par règles de transport Exchange**: nombre de messages **de** gravité **élevée,** moyenne et **faible.**</span><span class="sxs-lookup"><span data-stu-id="20586-168">**View data by Exchange transport rules**: The number of **High severity**, **Medium severity**, and **Low severity** messages.</span></span> <span data-ttu-id="20586-169">Vous définissez le niveau de gravité en tant qu’action dans la règle (**Auditez** cette règle avec le niveau de gravité _ou SetAuditSeverity_).</span><span class="sxs-lookup"><span data-stu-id="20586-169">You set the severity level as an action in the rule (**Audit this rule with severity level** or _SetAuditSeverity_).</span></span> <span data-ttu-id="20586-170">Pour plus d’informations, voir [Actions de règle de flux de messagerie dans Exchange Online.](/Exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions)</span><span class="sxs-lookup"><span data-stu-id="20586-170">For more information, see [Mail flow rule actions in Exchange Online](/Exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions).</span></span>

- <span data-ttu-id="20586-171">Afficher les données par règles de transport Exchange  **DLP**: nombre de **messages** de gravité **élevée,** moyenne et faible affectés par les règles de flux de messagerie DLP.</span><span class="sxs-lookup"><span data-stu-id="20586-171">**View data by DLP Exchange transport rules**: The number of **High severity**, **Medium severity**, and **Low severity** messages that were affected by DLP mail flow rules.</span></span>

<span data-ttu-id="20586-172">Les informations suivantes sont affichées dans le tableau de détails sous le graphique :</span><span class="sxs-lookup"><span data-stu-id="20586-172">The following information is shown in the details table below the graph:</span></span>

- <span data-ttu-id="20586-173">**Date**</span><span class="sxs-lookup"><span data-stu-id="20586-173">**Date**</span></span>
- <span data-ttu-id="20586-174">**Stratégie DLP** ( Afficher les données par les règles de **transport Exchange DLP** uniquement)</span><span class="sxs-lookup"><span data-stu-id="20586-174">**DLP policy** (**View data by DLP Exchange transport rules** only)</span></span>
- <span data-ttu-id="20586-175">**Règle de transport**</span><span class="sxs-lookup"><span data-stu-id="20586-175">**Transport rule**</span></span>
- <span data-ttu-id="20586-176">**Subject**</span><span class="sxs-lookup"><span data-stu-id="20586-176">**Subject**</span></span>
- <span data-ttu-id="20586-177">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="20586-177">**Sender address**</span></span>
- <span data-ttu-id="20586-178">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="20586-178">**Recipient address**</span></span>
- <span data-ttu-id="20586-179">**Gravité**</span><span class="sxs-lookup"><span data-stu-id="20586-179">**Severity**</span></span>
- <span data-ttu-id="20586-180">**Direction**</span><span class="sxs-lookup"><span data-stu-id="20586-180">**Direction**</span></span>

<span data-ttu-id="20586-181">Vous pouvez filtrer le graphique et le tableau de détails en cliquant sur **Filtrer** et en sélectionnant une ou plusieurs des valeurs suivantes dans le volant qui s’affiche :</span><span class="sxs-lookup"><span data-stu-id="20586-181">You can filter both the chart and the details table by clicking **Filter** and selecting one or more of the following values in the flyout that appears:</span></span>

- <span data-ttu-id="20586-182">**Date (UTC)** **Date de début et** date de **fin**</span><span class="sxs-lookup"><span data-stu-id="20586-182">**Date (UTC)** **Start date** and **End date**</span></span>
- <span data-ttu-id="20586-183">**Direction**: **sortant et** **entrant**</span><span class="sxs-lookup"><span data-stu-id="20586-183">**Direction**: **Outbound** and **Inbound**</span></span>
- <span data-ttu-id="20586-184">**Gravité :** **gravité élevée,** **gravité moyenne** et gravité **faible**</span><span class="sxs-lookup"><span data-stu-id="20586-184">**Severity**: **High severity**, **Medium severity**, and **Low severity**</span></span>

<span data-ttu-id="20586-185">Lorsque vous avez terminé la configuration des filtres, cliquez sur **Appliquer,** **Annuler** ou **Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="20586-185">When you're finished configuring the filters, click **Apply**, **Cancel**, or **Clear filters**.</span></span>

## <a name="forwarding-report"></a><span data-ttu-id="20586-186">Rapport de forwarding</span><span class="sxs-lookup"><span data-stu-id="20586-186">Forwarding report</span></span>

> [!NOTE]
> <span data-ttu-id="20586-187">Le **rapport de forwarding** est désormais disponible dans le EAC.</span><span class="sxs-lookup"><span data-stu-id="20586-187">The **Forwarding report** is now available in the EAC.</span></span> <span data-ttu-id="20586-188">Pour plus d’informations, [reportez-vous au](/exchange/monitoring/mail-flow-reports/mfr-auto-forwarded-messages-report)rapport des messages transmis automatiquement dans le nouveau EAC.</span><span class="sxs-lookup"><span data-stu-id="20586-188">For more information, see [Auto forwarded messages report in the new EAC](/exchange/monitoring/mail-flow-reports/mfr-auto-forwarded-messages-report).</span></span>

## <a name="mailflow-status-report"></a><span data-ttu-id="20586-189">Rapport d’état du flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="20586-189">Mailflow status report</span></span>

<span data-ttu-id="20586-190">Le  rapport d’état du flux de messagerie est un rapport intelligent qui affiche des informations sur le courrier électronique entrant et sortant, les détections de courrier indésirable, les programmes malveillants, les e-mails identifiés comme « bons » et les informations sur les messages électroniques autorisés ou bloqués sur le edge.</span><span class="sxs-lookup"><span data-stu-id="20586-190">The **Mailflow status report** is a smart report that shows information about incoming and outgoing email, spam detections, malware, email identified as "good", and information about email allowed or blocked on the edge.</span></span> <span data-ttu-id="20586-191">Il s’agit du seul rapport qui contient des informations de protection Edge et indique la quantité de courrier électronique bloquée avant d’être autorisé dans le service pour évaluation par Exchange Online Protection (EOP).</span><span class="sxs-lookup"><span data-stu-id="20586-191">This is the only report that contains edge protection information, and shows just how much email is blocked before being allowed into the service for evaluation by Exchange Online Protection (EOP).</span></span> <span data-ttu-id="20586-192">Il est important de comprendre que si un message est envoyé à cinq destinataires, nous le compterons comme cinq messages différents et pas un seul message.</span><span class="sxs-lookup"><span data-stu-id="20586-192">It's important to understand that if a message is sent to five recipients we count it as five different messages and not one message.</span></span>

<span data-ttu-id="20586-193">Pour afficher le rapport dans le portail Microsoft  365 Defender, consultez La boîte aux & collaboration de rapports e-mail \>  \> **& rapports de collaboration.**</span><span class="sxs-lookup"><span data-stu-id="20586-193">To view the report in the Microsoft 365 Defender portal, go to **Reports** \> **Email & collaboration** \> **Email & collaboration reports**.</span></span> <span data-ttu-id="20586-194">Dans la page **Rapports de collaboration &** courrier électronique, recherchez le résumé **de** l’état du flux de messagerie, puis cliquez sur Afficher **les détails.**</span><span class="sxs-lookup"><span data-stu-id="20586-194">On the **Email & collaboration reports** page, find **Mailflow status summary** and then click **View details**.</span></span> <span data-ttu-id="20586-195">Pour aller directement dans le rapport, ouvrez <https://security.microsoft.com/reports/mailflowStatusReport> .</span><span class="sxs-lookup"><span data-stu-id="20586-195">To go directly to the report, open <https://security.microsoft.com/reports/mailflowStatusReport>.</span></span>

![Widget de synthèse de l’état du flux de messagerie dans la page Rapports de collaboration & courrier électronique](../../media/mail-flow-status-report-widget.png)

### <a name="type-view-for-the-mailflow-status-report"></a><span data-ttu-id="20586-197">Affichage des types pour le rapport d’état du flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="20586-197">Type view for the Mailflow status report</span></span>

<span data-ttu-id="20586-198">Lorsque vous ouvrez l’état, **l’onglet Type** est sélectionné par défaut.</span><span class="sxs-lookup"><span data-stu-id="20586-198">When you open the report, the **Type** tab is selected by default.</span></span> <span data-ttu-id="20586-199">Par défaut, cet affichage contient un graphique et un tableau de détails configurés avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="20586-199">By default, this view contains a chart and a details table that's configured with the following filters:</span></span>

- <span data-ttu-id="20586-200">**Date (UTC)** 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="20586-200">**Date (UTC)** The last 7 days.</span></span>
- <span data-ttu-id="20586-201">**Direction du courrier**:</span><span class="sxs-lookup"><span data-stu-id="20586-201">**Mail direction**:</span></span>
  - <span data-ttu-id="20586-202">**Entrant**</span><span class="sxs-lookup"><span data-stu-id="20586-202">**Inbound**</span></span>
  - <span data-ttu-id="20586-203">**Sortant**</span><span class="sxs-lookup"><span data-stu-id="20586-203">**Outbound**</span></span>
  - <span data-ttu-id="20586-204">**Intra-organisation**: ce nombre est pour les messages au sein d’un client, c’est-à-dire</span><span class="sxs-lookup"><span data-stu-id="20586-204">**Intra-org**: this count is for messages within a tenant i.e</span></span> <span data-ttu-id="20586-205">sender abc@domain.com sends to recipient xyz@domain.com (counted separately from **Inbound** and **Outbound**)</span><span class="sxs-lookup"><span data-stu-id="20586-205">sender abc@domain.com sends to recipient xyz@domain.com  (counted separately from **Inbound** and **Outbound**)</span></span>
- <span data-ttu-id="20586-206">**Tapez**:</span><span class="sxs-lookup"><span data-stu-id="20586-206">**Type**:</span></span>
  - <span data-ttu-id="20586-207">**Bon courrier**</span><span class="sxs-lookup"><span data-stu-id="20586-207">**Good mail**</span></span>
  - <span data-ttu-id="20586-208">**Programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="20586-208">**Malware**</span></span>
  - <span data-ttu-id="20586-209">**Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="20586-209">**Spam**</span></span>
  - <span data-ttu-id="20586-210">**Protection Edge**</span><span class="sxs-lookup"><span data-stu-id="20586-210">**Edge protection**</span></span>
  - <span data-ttu-id="20586-211">**Messages de règle**</span><span class="sxs-lookup"><span data-stu-id="20586-211">**Rule messages**</span></span>
  - <span data-ttu-id="20586-212">**Courriers hameçons**</span><span class="sxs-lookup"><span data-stu-id="20586-212">**Phishing email**</span></span>
- <span data-ttu-id="20586-213">**Domaine**: **Tous**</span><span class="sxs-lookup"><span data-stu-id="20586-213">**Domain**: **All**</span></span>

<span data-ttu-id="20586-214">Le graphique est organisé par les valeurs **Type.**</span><span class="sxs-lookup"><span data-stu-id="20586-214">The chart is organized by the **Type** values.</span></span>

<span data-ttu-id="20586-215">Vous pouvez modifier ces filtres en cliquant sur **Filtre** ou en cliquant sur une valeur dans la légende du graphique.</span><span class="sxs-lookup"><span data-stu-id="20586-215">You can change these filters by clicking **Filter** or by clicking a value in the chart legend.</span></span>

<span data-ttu-id="20586-216">Les informations suivantes sont affichées dans le tableau de détails sous le graphique :</span><span class="sxs-lookup"><span data-stu-id="20586-216">The following information is shown in the details table below the graph:</span></span>

- <span data-ttu-id="20586-217">**Direction**</span><span class="sxs-lookup"><span data-stu-id="20586-217">**Direction**</span></span>
- <span data-ttu-id="20586-218">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="20586-218">**Type**</span></span>
- <span data-ttu-id="20586-219">**24 heures**</span><span class="sxs-lookup"><span data-stu-id="20586-219">**24 hours**</span></span>
- <span data-ttu-id="20586-220">**3 jours**</span><span class="sxs-lookup"><span data-stu-id="20586-220">**3 days**</span></span>
- <span data-ttu-id="20586-221">**7 jours**</span><span class="sxs-lookup"><span data-stu-id="20586-221">**7 days**</span></span>
- <span data-ttu-id="20586-222">**15 jours**</span><span class="sxs-lookup"><span data-stu-id="20586-222">**15 days**</span></span>
- <span data-ttu-id="20586-223">**30 jours**</span><span class="sxs-lookup"><span data-stu-id="20586-223">**30 days**</span></span>

<span data-ttu-id="20586-224">Si vous cliquez **sur Choisir une catégorie pour plus d’informations,** vous pouvez sélectionner l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="20586-224">If you click **Choose a category for more details**, you can select from the following values:</span></span>

- <span data-ttu-id="20586-225">**E-mail de hameçonnage**: cette sélection vous place dans le rapport d’état [de la protection contre les menaces.](view-email-security-reports.md#threat-protection-status-report)</span><span class="sxs-lookup"><span data-stu-id="20586-225">**Phishing email**: This selection takes you to the [Threat protection status report](view-email-security-reports.md#threat-protection-status-report).</span></span>
- <span data-ttu-id="20586-226">**Programmes malveillants dans les e-mails**: cette sélection vous place dans le rapport d’état [de la protection contre les menaces.](view-email-security-reports.md#threat-protection-status-report)</span><span class="sxs-lookup"><span data-stu-id="20586-226">**Malware in email**: This selection takes you to the [Threat protection status report](view-email-security-reports.md#threat-protection-status-report).</span></span>
- <span data-ttu-id="20586-227">**Détections de courrier indésirable**: cette sélection vous permet d’envoyer le rapport [détections de courrier indésirable.](view-email-security-reports.md#spam-detections-report)</span><span class="sxs-lookup"><span data-stu-id="20586-227">**Spam detections**: This selection takes you to the [Spam Detections report](view-email-security-reports.md#spam-detections-report).</span></span>
- <span data-ttu-id="20586-228">**Courrier indésirable bloqué edge**: cette sélection vous permet d’envoyer le rapport [détections de courrier indésirable.](view-email-security-reports.md#spam-detections-report)</span><span class="sxs-lookup"><span data-stu-id="20586-228">**Edge blocked spam**: This selection takes you to the [Spam Detections report](view-email-security-reports.md#spam-detections-report).</span></span>

#### <a name="export-from-type-view"></a><span data-ttu-id="20586-229">Exporter à partir de l’affichage Type</span><span class="sxs-lookup"><span data-stu-id="20586-229">Export from Type view</span></span>

<span data-ttu-id="20586-230">Pour l’affichage détaillé, vous ne pouvez exporter les données que pour une journée.</span><span class="sxs-lookup"><span data-stu-id="20586-230">For the detail view, you can only export data for one day.</span></span> <span data-ttu-id="20586-231">Par exemple, si vous souhaitez exporter des données pendant 7 jours, vous devez faire 7 actions d’exportation différentes.</span><span class="sxs-lookup"><span data-stu-id="20586-231">So, if you want to export data for 7 days, you need to do 7 different export actions.</span></span>

<span data-ttu-id="20586-232">Chaque fichier .csv exporté est limité à 150 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="20586-232">Each exported .csv file is limited to 150,000 rows.</span></span> <span data-ttu-id="20586-233">Si les données de ce jour contiennent plus de 150 000 lignes, plusieurs fichiers .csv seront créés.</span><span class="sxs-lookup"><span data-stu-id="20586-233">If the data for that day contains more than 150,000 rows, then multiple .csv files will be created.</span></span>

![Affichage des types dans le rapport d’état du flux de messagerie](../../media/mail-flow-status-report-type-view.png)

### <a name="direction-view-for-the-mailflow-status-report"></a><span data-ttu-id="20586-235">Affichage direction pour le rapport d’état du flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="20586-235">Direction view for the Mailflow status report</span></span>

<span data-ttu-id="20586-236">Si vous cliquez sur **l’onglet Direction,** les mêmes filtres par défaut de **l’affichage Type** sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="20586-236">If you click the **Direction** tab, the same default filters from the **Type** view are used.</span></span>

<span data-ttu-id="20586-237">Le graphique est organisé par **valeurs direction.**</span><span class="sxs-lookup"><span data-stu-id="20586-237">The chart is organized by **Direction** values.</span></span>

<span data-ttu-id="20586-238">Vous pouvez modifier ces filtres en cliquant sur **Filtre.**</span><span class="sxs-lookup"><span data-stu-id="20586-238">You can change these filters by clicking **Filter**.</span></span> <span data-ttu-id="20586-239">Les mêmes filtres de **l’affichage Type** sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="20586-239">The same filters from the **Type** view are used.</span></span>

<span data-ttu-id="20586-240">Le tableau de détails contient les mêmes informations que **l’affichage Type.**</span><span class="sxs-lookup"><span data-stu-id="20586-240">The details table contains same information from the **Type** view.</span></span>

<span data-ttu-id="20586-241">La **sélection d’une catégorie pour plus d’informations** sur les sélections disponibles et le comportement sont identiques à l’affichage **Type.**</span><span class="sxs-lookup"><span data-stu-id="20586-241">The **Choose a category for more details** available selections and behavior are the same as the **Type** view.</span></span>

#### <a name="export-from-direction-view"></a><span data-ttu-id="20586-242">Exporter à partir du mode Direction</span><span class="sxs-lookup"><span data-stu-id="20586-242">Export from Direction view</span></span>

<span data-ttu-id="20586-243">Pour l’affichage détaillé, vous ne pouvez exporter les données que pour une journée.</span><span class="sxs-lookup"><span data-stu-id="20586-243">For the detail view, you can only export data for one day.</span></span> <span data-ttu-id="20586-244">Par exemple, si vous souhaitez exporter des données pendant 7 jours, vous devez faire 7 actions d’exportation différentes.</span><span class="sxs-lookup"><span data-stu-id="20586-244">So, if you want to export data for 7 days, you need to do 7 different export actions.</span></span>

<span data-ttu-id="20586-245">Chaque fichier .csv exporté est limité à 150 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="20586-245">Each exported .csv file is limited to 150,000 rows.</span></span> <span data-ttu-id="20586-246">Si les données de ce jour contiennent plus de 150 000 lignes, plusieurs fichiers .csv seront créés.</span><span class="sxs-lookup"><span data-stu-id="20586-246">If the data for that day contains more than 150,000 rows, then multiple .csv files will be created.</span></span>

![Affichage direction dans le rapport d’état du flux de messagerie](../../media/mail-flow-status-report-direction-view.png)

### <a name="funnel-view-for-the-mailflow-status-report"></a><span data-ttu-id="20586-248">Affichage en entonnoir pour le rapport d’état du flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="20586-248">Funnel view for the Mailflow status report</span></span>

<span data-ttu-id="20586-249">La **vue Entonnoir** vous montre comment les fonctionnalités de protection contre les menaces de courrier électronique de Microsoft filtrent le courrier électronique entrant et sortant dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="20586-249">The **Funnel** view shows you how Microsoft's email threat protection features filter incoming and outgoing email in your organization.</span></span> <span data-ttu-id="20586-250">Il fournit des détails sur le nombre total de messages électroniques et sur la façon dont les fonctionnalités de protection contre les menaces configurées, y compris la protection edge, la protection contre les programmes malveillants, l’anti-hameçonnage, le courrier indésirable et la détection d’usurpation d’accès affectent ce nombre.</span><span class="sxs-lookup"><span data-stu-id="20586-250">It provides details on the total email count, and how the configured threat protection features, including edge protection, anti-malware, anti-phishing, anti-spam, and anti-spoofing affect this count.</span></span>

<span data-ttu-id="20586-251">Si vous  cliquez sur l’onglet Entonnoir, par défaut, cet affichage contient un graphique et un tableau de détails configuré avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="20586-251">If you click the **Funnel** tab, by default, this view contains a chart and a details table that's configured with the following filters:</span></span>

- <span data-ttu-id="20586-252">**Date**: 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="20586-252">**Date**: The last 7 days.</span></span>

- <span data-ttu-id="20586-253">**Direction**:</span><span class="sxs-lookup"><span data-stu-id="20586-253">**Direction**:</span></span>
  - <span data-ttu-id="20586-254">**Entrant**</span><span class="sxs-lookup"><span data-stu-id="20586-254">**Inbound**</span></span>
  - <span data-ttu-id="20586-255">**Sortant**</span><span class="sxs-lookup"><span data-stu-id="20586-255">**Outbound**</span></span>
  - <span data-ttu-id="20586-256">**Intra-organisation**: ce nombre est le nombre de messages envoyés au sein d’un client ; Autrement dit, l’expéditeur abc@domain.com envoyé au destinataire xyz@domain.com (comptabilisé séparément des messages entrants et sortants).</span><span class="sxs-lookup"><span data-stu-id="20586-256">**Intra-org**: This count is for messages sent within a tenant; i.e, sender abc@domain.com sends to recipient xyz@domain.com (counted separately from Inbound and Outbound).</span></span>

<span data-ttu-id="20586-257">L’affichage agrégé et le tableau détails autorisent 90 jours de filtrage.</span><span class="sxs-lookup"><span data-stu-id="20586-257">The aggregate view and details table view allow for 90 days of filtering.</span></span>

<span data-ttu-id="20586-258">Vous pouvez modifier ces filtres en cliquant sur **Filtre.**</span><span class="sxs-lookup"><span data-stu-id="20586-258">You can change these filters by clicking **Filter**.</span></span> <span data-ttu-id="20586-259">Les mêmes filtres de **l’affichage Type** sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="20586-259">The same filters from the **Type** view are used.</span></span>

<span data-ttu-id="20586-260">Ce graphique indique le nombre de messages électroniques organisés par :</span><span class="sxs-lookup"><span data-stu-id="20586-260">This chart shows the email count organized by:</span></span>

- <span data-ttu-id="20586-261">**Nombre total de messages électroniques**</span><span class="sxs-lookup"><span data-stu-id="20586-261">**Total email**</span></span>
- <span data-ttu-id="20586-262">**Courrier électronique après protection edge**</span><span class="sxs-lookup"><span data-stu-id="20586-262">**Email after edge protection**</span></span>
- <span data-ttu-id="20586-263">**Règle de messagerie après transport** (règle de flux de messagerie)</span><span class="sxs-lookup"><span data-stu-id="20586-263">**Email after transport rule** (mail flow rule)</span></span>
- <span data-ttu-id="20586-264">**Courrier électronique après anti-programme malveillant, réputation du fichier, bloc de type de fichier**</span><span class="sxs-lookup"><span data-stu-id="20586-264">**Email after anti-malware, file reputation, file type block**</span></span>
- <span data-ttu-id="20586-265">**Courrier électronique après anti-hameçonnage, réputation d’URL, emprunt d’identité de marque, anti-usurpation d’identité**</span><span class="sxs-lookup"><span data-stu-id="20586-265">**Email after anti-phish, URL reputation, brand impersonation, anti-spoof**</span></span>
- <span data-ttu-id="20586-266">**Courrier électronique après filtrage du courrier indésirable en bloc**</span><span class="sxs-lookup"><span data-stu-id="20586-266">**Email after anti-spam, bulk mail filtering**</span></span>
- <span data-ttu-id="20586-267">**Courrier électronique après l’emprunt d’identité de l’utilisateur et du domaine**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="20586-267">**Email after user and domain impersonation**<sup>\*</sup></span></span>
- <span data-ttu-id="20586-268">**E-mail après détonation du fichier et de l’URL**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="20586-268">**Email after file and URL detonation**<sup>\*</sup></span></span>
- <span data-ttu-id="20586-269">**Courrier électronique détecté comme étant anodin après la remise (protection de temps de clic d’URL)**</span><span class="sxs-lookup"><span data-stu-id="20586-269">**Email detected as benign after post-delivery protection (URL click time protection)**</span></span>

<span data-ttu-id="20586-270"><sup>\*</sup>Defender pour Office 365 uniquement</span><span class="sxs-lookup"><span data-stu-id="20586-270"><sup>\*</sup> Defender for Office 365 only</span></span>

<span data-ttu-id="20586-271">Pour afficher l’e-mail filtré par EOP ou Defender Office 365 séparément, cliquez sur la valeur dans la légende du graphique.</span><span class="sxs-lookup"><span data-stu-id="20586-271">To view the email filtered by EOP or Defender for Office 365 separately, click on the value in the chart legend.</span></span>

<span data-ttu-id="20586-272">Le tableau de détails contient les informations suivantes, indiquées dans l’ordre décroit de date :</span><span class="sxs-lookup"><span data-stu-id="20586-272">The details table contains the following information, shown in descending date order:</span></span>

- <span data-ttu-id="20586-273">**Date**</span><span class="sxs-lookup"><span data-stu-id="20586-273">**Date**</span></span>
- <span data-ttu-id="20586-274">**Nombre total de messages électroniques**</span><span class="sxs-lookup"><span data-stu-id="20586-274">**Total email**</span></span>
- <span data-ttu-id="20586-275">**Protection Edge**</span><span class="sxs-lookup"><span data-stu-id="20586-275">**Edge protection**</span></span>
- <span data-ttu-id="20586-276">**Anti-programme malveillant, réputation de fichier, bloc de type de fichier**:</span><span class="sxs-lookup"><span data-stu-id="20586-276">**Anti-malware, file reputation, file type block**:</span></span>
  - <span data-ttu-id="20586-277">**Réputation du** fichier : messages filtrés en raison de l’identification d’un fichier joint par d’autres clients Microsoft.</span><span class="sxs-lookup"><span data-stu-id="20586-277">**File reputation**: Messages filtered due to identification of an attached file by other Microsoft customers.</span></span>
  - <span data-ttu-id="20586-278">**Bloc de type de** fichier : messages filtrés en raison du type de fichier malveillant identifié dans le message.</span><span class="sxs-lookup"><span data-stu-id="20586-278">**File type block**: Messages filtered due to the type of malicious file identified in the message.</span></span>
- <span data-ttu-id="20586-279">**Anti-hameçonnage, réputation de l’URL, emprunt d’identité de marque, anti-usurpation d’identité**:</span><span class="sxs-lookup"><span data-stu-id="20586-279">**Anti-phish, URL reputation, Brand impersonation, anti-spoof**:</span></span>
  - <span data-ttu-id="20586-280">**Réputation de l’URL**: messages filtrés en raison de l’identification de l’URL par d’autres clients Microsoft.</span><span class="sxs-lookup"><span data-stu-id="20586-280">**URL reputation**: Messages filtered due to the identification of the URL by other Microsoft customers.</span></span>
  - <span data-ttu-id="20586-281">**Emprunt d’identité de marque**: messages filtrés en raison du message provenant de la marque connue usurpant l’identité des expéditeurs.</span><span class="sxs-lookup"><span data-stu-id="20586-281">**Brand impersonation**: Messages filtered due to the message coming from well-known brand impersonating senders.</span></span>
  - <span data-ttu-id="20586-282">**Anti-usurpation**: messages filtrés en raison de la tentative d’usurpation d’un domaine appartenant au destinataire ou d’un domaine que l’expéditeur du message ne possède pas.</span><span class="sxs-lookup"><span data-stu-id="20586-282">**Anti-spoof**: Messages filtered due to the message attempting to spoof a domain that the recipient belongs to, or a domain that the message sender doesn't own.</span></span>
- <span data-ttu-id="20586-283">**Anti-courrier indésirable, filtrage du courrier en bloc**:</span><span class="sxs-lookup"><span data-stu-id="20586-283">**Anti-spam, bulk mail filtering**:</span></span>
  - <span data-ttu-id="20586-284">**Filtrage du courrier en bloc**: messages filtrés en fonction du seuil bcl (seuil de plainte en bloc) dans une stratégie anti-courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="20586-284">**Bulk mail filtering**: Messages filtered based on the bulk complain level (BCL) threshold in an anti-spam policy.</span></span>
- <span data-ttu-id="20586-285">**Emprunt d’identité d’utilisateur et** de domaine (Defender pour Office 365) :</span><span class="sxs-lookup"><span data-stu-id="20586-285">**User and domain impersonation (Defender for Office 365)**:</span></span>
  - <span data-ttu-id="20586-286">**Emprunt d’identité** d’utilisateur : messages filtrés en raison d’une tentative d’emprunt d’identité d’un utilisateur (expéditeur de message) défini dans les paramètres de protection contre l’emprunt d’identité d’une stratégie anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="20586-286">**User impersonation**: Messages filtered due to an attempt to impersonate a user (message sender) that's defined in the impersonation protection settings of an anti-phishing policy.</span></span>
  - <span data-ttu-id="20586-287">**Emprunt d’identité** de domaine : messages filtrés en raison d’une tentative d’emprunt d’identité d’un domaine défini dans les paramètres de protection contre l’emprunt d’identité d’une stratégie anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="20586-287">**Domain impersonation**: Messages filtered due to an attempt to impersonate a domain that's defined in the impersonation protection settings of an anti-phishing policy.</span></span>
- <span data-ttu-id="20586-288">**Détonation de fichier et d’URL (Defender pour Office 365)**:</span><span class="sxs-lookup"><span data-stu-id="20586-288">**File and URL detonation (Defender for Office 365)**:</span></span>
  - <span data-ttu-id="20586-289">**Détonation de fichier**: messages filtrés par une stratégie Safe pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="20586-289">**File detonation**: Messages filtered by a Safe Attachments policy.</span></span>
  - <span data-ttu-id="20586-290">**Détonation d’URL**: message filtré par une stratégie Safe liens.</span><span class="sxs-lookup"><span data-stu-id="20586-290">**URL detonation**: Message filtered by a Safe Links policy.</span></span>
- <span data-ttu-id="20586-291">Protection post-remise et ZAP (Protection contre les menaces) ou **ZAP (EOP)**: purge automatique de zéro heure (ZAP) pour les programmes malveillants, le courrier indésirable et le hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="20586-291">**Post-delivery protection and ZAP (ATP), or ZAP (EOP)**: Zero-hour auto purge (ZAP) for malware, spam, and phishing.</span></span>

<span data-ttu-id="20586-292">Si vous sélectionnez une ligne dans le tableau de détails, une répartition supplémentaire du nombre de messages est affichée dans le volant.</span><span class="sxs-lookup"><span data-stu-id="20586-292">If you select a row in the details table, a further breakdown of the email counts are shown in the flyout.</span></span>

#### <a name="export-from-funnel-view"></a><span data-ttu-id="20586-293">Exporter à partir du affichage Entonnoir</span><span class="sxs-lookup"><span data-stu-id="20586-293">Export from Funnel view</span></span>

<span data-ttu-id="20586-294">Après avoir cliqué **sur Exporter** sous **Options,** vous pouvez sélectionner l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="20586-294">After you click **Export** under **Options**, you can select one of the following values:</span></span>

- <span data-ttu-id="20586-295">**Résumé (avec des données pour les 90 derniers jours au maximum)**</span><span class="sxs-lookup"><span data-stu-id="20586-295">**Summary (with data for last 90 days at most)**</span></span>
- <span data-ttu-id="20586-296">**Détails (avec des données pour les 30 derniers jours au maximum)**</span><span class="sxs-lookup"><span data-stu-id="20586-296">**Details (with data for last 30 days at most)**</span></span>

<span data-ttu-id="20586-297">Sous **Date**, choisissez une plage, puis cliquez sur **Appliquer**.</span><span class="sxs-lookup"><span data-stu-id="20586-297">Under **Date**, choose a range, and then click **Apply**.</span></span> <span data-ttu-id="20586-298">Les données des filtres actuels sont exportées vers un .csv de données.</span><span class="sxs-lookup"><span data-stu-id="20586-298">Data for the current filters will be exported to a .csv file.</span></span>

<span data-ttu-id="20586-299">Chaque fichier .csv exporté est limité à 150 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="20586-299">Each exported .csv file is limited to 150,000 rows.</span></span> <span data-ttu-id="20586-300">Si les données contiennent plus de 150 000 lignes, plusieurs .csv fichiers seront créés.</span><span class="sxs-lookup"><span data-stu-id="20586-300">If the data contains more than 150,000 rows, then multiple .csv files will be created.</span></span>

![Affichage en entonnoir dans le rapport d’état du flux de messagerie](../../media/mail-flow-status-report-funnel-view.png)

### <a name="tech-view-for-the-mailflow-status-report"></a><span data-ttu-id="20586-302">Affichage technique pour le rapport d’état du flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="20586-302">Tech view for the Mailflow status report</span></span>

<span data-ttu-id="20586-303">La **vue Tech est** similaire à la vue Entonnoir, fournissant des détails plus détaillés pour les fonctionnalités de protection contre les menaces configurées. </span><span class="sxs-lookup"><span data-stu-id="20586-303">The **Tech view** is similar to the **Funnel** view, providing more granular details for the configured threat protections features.</span></span> <span data-ttu-id="20586-304">À partir du graphique, vous pouvez voir comment les messages sont classés aux différentes étapes de la protection contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="20586-304">From the chart, you can see how messages are categorized at the different stages of threat protection.</span></span>

<span data-ttu-id="20586-305">Si vous cliquez sur **l’onglet** Affichage Technique, par défaut, cet affichage contient un graphique et un tableau de détails configurés avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="20586-305">If you click the **Tech view** tab, by default, this view contains a chart and a details table that's configured with the following filters:</span></span>

- <span data-ttu-id="20586-306">**Date**: 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="20586-306">**Date**: The last 7 days.</span></span>

- <span data-ttu-id="20586-307">**Direction**:</span><span class="sxs-lookup"><span data-stu-id="20586-307">**Direction**:</span></span>
  - <span data-ttu-id="20586-308">**Entrant**</span><span class="sxs-lookup"><span data-stu-id="20586-308">**Inbound**</span></span>
  - <span data-ttu-id="20586-309">**Sortant**</span><span class="sxs-lookup"><span data-stu-id="20586-309">**Outbound**</span></span>
  - <span data-ttu-id="20586-310">**Intra-organisation**: ce nombre est pour les messages au sein d’un client, c’est-à-dire</span><span class="sxs-lookup"><span data-stu-id="20586-310">**Intra-org**: this count is for messages within a tenant i.e</span></span> <span data-ttu-id="20586-311">sender abc@domain.com sends to recipient xyz@domain.com (counted separately from Inbound and Outbound)</span><span class="sxs-lookup"><span data-stu-id="20586-311">sender abc@domain.com sends to recipient xyz@domain.com (counted separately from Inbound and Outbound)</span></span>

<span data-ttu-id="20586-312">L’affichage agrégé et le tableau détails autorisent 90 jours de filtrage.</span><span class="sxs-lookup"><span data-stu-id="20586-312">The aggregate view and details table view allow for 90 days of filtering.</span></span>

<span data-ttu-id="20586-313">Vous pouvez modifier ces filtres en cliquant sur **Filtre.**</span><span class="sxs-lookup"><span data-stu-id="20586-313">You can change these filters by clicking **Filter**.</span></span> <span data-ttu-id="20586-314">Les mêmes filtres de **l’affichage Type** sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="20586-314">The same filters from the **Type** view are used.</span></span>

<span data-ttu-id="20586-315">Ce graphique présente les messages organisés dans les catégories suivantes :</span><span class="sxs-lookup"><span data-stu-id="20586-315">This chart shows messages organized into the following categories:</span></span>

- <span data-ttu-id="20586-316">**Nombre total de messages électroniques**</span><span class="sxs-lookup"><span data-stu-id="20586-316">**Total email**</span></span>
- <span data-ttu-id="20586-317">**Edge autoriser** et **edge filtré**</span><span class="sxs-lookup"><span data-stu-id="20586-317">**Edge allow** and **Edge filtered**</span></span>
- <span data-ttu-id="20586-318">**Règles de transport d’autoriser** et **de transport filtrées** (règles de flux de messagerie)</span><span class="sxs-lookup"><span data-stu-id="20586-318">**Transport rule allow** and **Transport rule filtered** (mail flow rules)</span></span>
- <span data-ttu-id="20586-319">**Pas de programmes** **malveillants, Safe détection des pièces jointes** <sup>\*</sup> et détection du moteur **anti-programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="20586-319">**Not malware**, **Safe Attachments detection**<sup>\*</sup>, and **Anti-malware engine detection**</span></span>
- <span data-ttu-id="20586-320">**Pas de hameçonnage,**  **d’échec DMARC,** de détection d’emprunt d’identité, de détection d’usurpation <sup>\*</sup> d’identité et de détection **d’hameçonnage** </span><span class="sxs-lookup"><span data-stu-id="20586-320">**Not phish**, **DMARC failure**, **Impersonation detection**<sup>\*</sup>, **Spoof detection**, and **Phish detection**</span></span>
- <span data-ttu-id="20586-321">**Aucune détection avec détection de détonation d’URL** et **de détonation d’URL**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="20586-321">**No detection with URL detonation** and **URL detonation detection**<sup>\*</sup></span></span>
- <span data-ttu-id="20586-322">**Pas de courrier indésirable** et  **de courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="20586-322">**Not spam** and  **Spam**</span></span>
- <span data-ttu-id="20586-323">**E-mail** non malveillant, **détection Safe liens et** <sup>\*</sup> **ZAP**</span><span class="sxs-lookup"><span data-stu-id="20586-323">**Non-malicious email**, **Safe Links detection**<sup>\*</sup>, and **ZAP**</span></span>

<span data-ttu-id="20586-324"><sup>\*</sup>Defender for Office 365</span><span class="sxs-lookup"><span data-stu-id="20586-324"><sup>\*</sup> Defender for Office 365</span></span>

<span data-ttu-id="20586-325">Lorsque vous pointez sur une catégorie dans le graphique, vous pouvez voir le nombre de messages dans cette catégorie.</span><span class="sxs-lookup"><span data-stu-id="20586-325">When you hover over a category in the chart, you can see the number of messages in that category.</span></span>

<span data-ttu-id="20586-326">Le tableau de détails contient les informations suivantes, indiquées dans l’ordre décroit de date :</span><span class="sxs-lookup"><span data-stu-id="20586-326">The details table contains the following information, shown in descending date order:</span></span>

- <span data-ttu-id="20586-327">**Date (UTC)**</span><span class="sxs-lookup"><span data-stu-id="20586-327">**Date (UTC)**</span></span>
- <span data-ttu-id="20586-328">**Nombre total de messages électroniques**</span><span class="sxs-lookup"><span data-stu-id="20586-328">**Total email**</span></span>
- <span data-ttu-id="20586-329">**Edge filtré**</span><span class="sxs-lookup"><span data-stu-id="20586-329">**Edge filtered**</span></span>
- <span data-ttu-id="20586-330">**Messages de règle**: messages filtrés en raison de règles de flux de messagerie (également appelées règles de transport).</span><span class="sxs-lookup"><span data-stu-id="20586-330">**Rule messages**: Messages filtered due to  mail flow rules (also known as transport rules).</span></span>
- <span data-ttu-id="20586-331">**Moteur anti-programme malveillant,** **Safe pièces jointes** <sup>\*</sup> :</span><span class="sxs-lookup"><span data-stu-id="20586-331">**Anti-malware engine**, **Safe Attachments**<sup>\*</sup>:</span></span>
- <span data-ttu-id="20586-332">**DMARC, emprunt d’identité,** <sup>\*</sup> **usurpation** d’identité, **hameçonnage filtré**:</span><span class="sxs-lookup"><span data-stu-id="20586-332">**DMARC, impersonation**<sup>\*</sup>, **spoof**, **phish filtered**:</span></span>
  - <span data-ttu-id="20586-333">**DMARC**: messages filtrés en raison de l’échec de la vérification de l’authentification DMARC.</span><span class="sxs-lookup"><span data-stu-id="20586-333">**DMARC**: Messages filtered due to the message failing its DMARC authentication check.</span></span>
- <span data-ttu-id="20586-334">**Détection de détonation d’URL**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="20586-334">**URL detonation detection**<sup>\*</sup></span></span>
- <span data-ttu-id="20586-335">**Filtrage anti-courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="20586-335">**Anti-spam filtered**</span></span>
- <span data-ttu-id="20586-336">**ZAP supprimé**</span><span class="sxs-lookup"><span data-stu-id="20586-336">**ZAP removed**</span></span>
- <span data-ttu-id="20586-337">**Détection par liens Safe de détection**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="20586-337">**Detection by Safe Links**<sup>\*</sup></span></span>

<span data-ttu-id="20586-338"><sup>\*</sup>Defender for Office 365</span><span class="sxs-lookup"><span data-stu-id="20586-338"><sup>\*</sup> Defender for Office 365</span></span>

<span data-ttu-id="20586-339">Si vous sélectionnez une ligne dans le tableau de détails, une répartition supplémentaire du nombre de messages est affichée dans le volant.</span><span class="sxs-lookup"><span data-stu-id="20586-339">If you select a row in the details table, a further breakdown of the email counts are shown in the flyout.</span></span>

#### <a name="export-from-tech-view"></a><span data-ttu-id="20586-340">Exporter à partir d’un affichage tech</span><span class="sxs-lookup"><span data-stu-id="20586-340">Export from Tech view</span></span>

<span data-ttu-id="20586-341">En cliquant **sur Exporter,** sous **Options,** vous pouvez sélectionner l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="20586-341">On clicking **Export**, under **Options** you can select one of the following values:</span></span>

- <span data-ttu-id="20586-342">**Résumé (avec des données pour les 90 derniers jours au maximum)**</span><span class="sxs-lookup"><span data-stu-id="20586-342">**Summary (with data for last 90 days at most)**</span></span>
- <span data-ttu-id="20586-343">**Détails (avec des données pour les 30 derniers jours au maximum)**</span><span class="sxs-lookup"><span data-stu-id="20586-343">**Details (with data for last 30 days at most)**</span></span>

<span data-ttu-id="20586-344">Sous **Date**, choisissez une plage, puis cliquez sur **Appliquer**.</span><span class="sxs-lookup"><span data-stu-id="20586-344">Under **Date**, choose a range, and then click **Apply**.</span></span> <span data-ttu-id="20586-345">Les données des filtres actuels sont exportées vers un .csv de données.</span><span class="sxs-lookup"><span data-stu-id="20586-345">Data for the current filters will be exported to a .csv file.</span></span>

<span data-ttu-id="20586-346">Chaque fichier .csv exporté est limité à 150 000 lignes.</span><span class="sxs-lookup"><span data-stu-id="20586-346">Each exported .csv file is limited to 150,000 rows.</span></span> <span data-ttu-id="20586-347">Si les données contiennent plus de 150 000 lignes, plusieurs .csv fichiers seront créés.</span><span class="sxs-lookup"><span data-stu-id="20586-347">If the data contains more than 150,000 rows, then multiple .csv files will be created.</span></span>

![Affichage technique dans le rapport d’état du flux de messagerie](../../media/mail-flow-status-report-tech-view.png)

## <a name="malware-detections-report"></a><span data-ttu-id="20586-349">Rapport sur les détections de programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="20586-349">Malware detections report</span></span>

<span data-ttu-id="20586-350">Le rapport détections de programmes malveillants affiche des informations sur les détections de programmes malveillants dans les messages électroniques entrants et sortants (programmes **malveillants détectés** par Exchange Online Protection ou EOP).</span><span class="sxs-lookup"><span data-stu-id="20586-350">The **Malware detections report** report shows information about malware detections in incoming and outgoing email messages (malware detected by Exchange Online Protection or EOP).</span></span> <span data-ttu-id="20586-351">Pour plus d’informations sur la protection contre les programmes malveillants dans EOP, voir Protection contre les programmes [malveillants dans EOP.](anti-malware-protection.md)</span><span class="sxs-lookup"><span data-stu-id="20586-351">For more information about malware protection in EOP, see [Anti-malware protection in EOP](anti-malware-protection.md).</span></span>

<span data-ttu-id="20586-352">Le filtre d’affichage agrégé autorise 90 jours, tandis que le filtre de tableau détails ne le permet que sur 10 jours.</span><span class="sxs-lookup"><span data-stu-id="20586-352">The aggregate view filter allows for 90 days, while the details table filter only allows for 10 days.</span></span>

<span data-ttu-id="20586-353">Pour afficher le rapport dans le portail  Microsoft 365 Defender, consultez la & collaboration de rapports e-mail \>  \> **& rapports de collaboration.**</span><span class="sxs-lookup"><span data-stu-id="20586-353">To view the report in the Microsoft 365 Defender portal, go to **Reports** \> **Email & collaboration** \> **Email & collaboration reports**.</span></span> <span data-ttu-id="20586-354">Dans la page **& de collaboration,** recherchez les programmes malveillants détectés dans le courrier **électronique,** puis cliquez sur Afficher **les détails.**</span><span class="sxs-lookup"><span data-stu-id="20586-354">On the **Email & collaboration reports** page, find **Malware detected in email** and then click **View details**.</span></span> <span data-ttu-id="20586-355">Pour aller directement dans le rapport, ouvrez <https://security.microsoft.com/reports/MalwareDetections> .</span><span class="sxs-lookup"><span data-stu-id="20586-355">To go directly to the report, open <https://security.microsoft.com/reports/MalwareDetections>.</span></span>

![Détections de programmes malveillants dans le widget de messagerie sur la page rapports de collaboration & messagerie](../../media/malware-detections-widget.png)

<span data-ttu-id="20586-357">Dans la page Du rapport détections de programmes **malveillants,** vous  pouvez filtrer à la fois le graphique et le tableau de détails en cliquant sur Filtrer et en sélectionnant l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="20586-357">On the **Malware detections report** page, you can filter both the chart and the details table by clicking **Filter** and selecting one of the following values:</span></span>

- <span data-ttu-id="20586-358">**Date (UTC)** **Date de début et** date de **fin**</span><span class="sxs-lookup"><span data-stu-id="20586-358">**Date (UTC)** **Start date** and **End date**</span></span>
- <span data-ttu-id="20586-359">**Direction**: **trafic entrant** et **sortant**</span><span class="sxs-lookup"><span data-stu-id="20586-359">**Direction**: **Inbound** and **Outbound**</span></span>

![Affichage du rapport dans le rapport de détection des programmes malveillants dans le rapport de courrier électronique](../../media/malware-detections-report-view.png)

<span data-ttu-id="20586-361">Dans le tableau de détails sous le graphique, vous pouvez voir les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="20586-361">In the details table below the graph, you can see the following details:</span></span>

- <span data-ttu-id="20586-362">**Date**</span><span class="sxs-lookup"><span data-stu-id="20586-362">**Date**</span></span>
- <span data-ttu-id="20586-363">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="20586-363">**Sender address**</span></span>
- <span data-ttu-id="20586-364">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="20586-364">**Recipient address**</span></span>
- <span data-ttu-id="20586-365">**ID de message**: disponible dans le champ d’en-tête **Message-ID** dans l’en-tête du message et doit être unique.</span><span class="sxs-lookup"><span data-stu-id="20586-365">**Message ID**: Available in the **Message-ID** header field in the message header and should be unique.</span></span> <span data-ttu-id="20586-366">Un exemple de valeur est `<08f1e0f6806a47b4ac103961109ae6ef@server.domain>` (notez les crochets).</span><span class="sxs-lookup"><span data-stu-id="20586-366">An example value is `<08f1e0f6806a47b4ac103961109ae6ef@server.domain>` (note the angle brackets).</span></span>
- <span data-ttu-id="20586-367">**Subject**</span><span class="sxs-lookup"><span data-stu-id="20586-367">**Subject**</span></span>
- <span data-ttu-id="20586-368">**Filename**</span><span class="sxs-lookup"><span data-stu-id="20586-368">**Filename**</span></span>
- <span data-ttu-id="20586-369">**Nom du programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="20586-369">**Malware name**</span></span>

## <a name="mail-latency-report"></a><span data-ttu-id="20586-370">Rapport de latence du courrier</span><span class="sxs-lookup"><span data-stu-id="20586-370">Mail latency report</span></span>

<span data-ttu-id="20586-371">Le **rapport de latence de messagerie** dans Defender pour Office 365 contient des informations sur la remise et la latence de détonation du courrier au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="20586-371">The **Mail latency report** in Defender for Office 365 contains information on the mail delivery and detonation latency experienced within your organization.</span></span> <span data-ttu-id="20586-372">Pour plus d’informations, voir [Rapport de latence de messagerie.](view-reports-for-mdo.md#mail-latency-report)</span><span class="sxs-lookup"><span data-stu-id="20586-372">For more information, see [Mail latency report](view-reports-for-mdo.md#mail-latency-report).</span></span>

## <a name="spam-detections-report"></a><span data-ttu-id="20586-373">Rapport sur la détection des courriers indésirables</span><span class="sxs-lookup"><span data-stu-id="20586-373">Spam detections report</span></span>

> [!NOTE]
> <span data-ttu-id="20586-374">Le **rapport de détection du courrier** indésirable va finir par disparaître.</span><span class="sxs-lookup"><span data-stu-id="20586-374">The **Spam detections report** will eventually go away.</span></span> <span data-ttu-id="20586-375">Les mêmes informations sont disponibles dans le rapport d’état [de la protection contre les menaces.](#threat-protection-status-report)</span><span class="sxs-lookup"><span data-stu-id="20586-375">The same information is available in the [Threat protection status report](#threat-protection-status-report).</span></span>

## <a name="spoof-detections-report"></a><span data-ttu-id="20586-376">Rapport sur les détections d’usurpation d’usurpation</span><span class="sxs-lookup"><span data-stu-id="20586-376">Spoof detections report</span></span>

> [!NOTE]
> <span data-ttu-id="20586-377">Le rapport sur les détections d’usurpation d’usurpation d’informations amélioré, tel que décrit dans cet article, est disponible en prévisualisation, peut faire l’objet de changements et n’est pas disponible dans toutes les organisations.</span><span class="sxs-lookup"><span data-stu-id="20586-377">The improved Spoof detections report as described in this article is in Preview, is subject to change, and is not available in all organizations.</span></span> <span data-ttu-id="20586-378">L’ancienne version du rapport affiche uniquement les messages **de bonne qualité** et les courriers **indésirables**.</span><span class="sxs-lookup"><span data-stu-id="20586-378">The older version of the report shows only **Good mail** and **Caught as spam**.</span></span>

<span data-ttu-id="20586-379">Le **rapport sur les détections d’usurpation d’informations** affiche des informations sur les messages qui ont été bloqués ou autorisés en raison de l’usurpation d’informations.</span><span class="sxs-lookup"><span data-stu-id="20586-379">The **Spoof detections** report shows information about messages that were blocked or allowed due to spoofing.</span></span> <span data-ttu-id="20586-380">Pour plus d’informations sur l’usurpation d’adresse, consultez la protection contre l’usurpation [d’adresse dans EOP.](anti-spoofing-protection.md)</span><span class="sxs-lookup"><span data-stu-id="20586-380">For more information about spoofing, see [Anti-spoofing protection in EOP](anti-spoofing-protection.md).</span></span>

<span data-ttu-id="20586-381">L’affichage agrégé du rapport autorise 45 jours de filtrage, tandis que l’affichage détaillé ne permet que dix jours <sup>\*</sup> de filtrage.</span><span class="sxs-lookup"><span data-stu-id="20586-381">The aggregate view of the report allows for 45 days of filtering<sup>\*</sup>, while the detail view only allows for ten days of filtering.</span></span>

<span data-ttu-id="20586-382"><sup>\*</sup> Au final, vous pourrez utiliser jusqu’à 90 jours de filtrage.</span><span class="sxs-lookup"><span data-stu-id="20586-382"><sup>\*</sup> Eventually, you'll be able to use up to 90 days of filtering.</span></span>

<span data-ttu-id="20586-383">Pour afficher le rapport dans le portail  Microsoft 365 Defender, consultez la & collaboration de rapports e-mail \>  \> **& rapports de collaboration.**</span><span class="sxs-lookup"><span data-stu-id="20586-383">To view the report in the Microsoft 365 Defender portal, go to **Reports** \> **Email & collaboration** \> **Email & collaboration reports**.</span></span> <span data-ttu-id="20586-384">Dans la page **& de collaboration,** recherchez les détections d’usurpation **d’adresse,** puis cliquez sur **Afficher les détails.**</span><span class="sxs-lookup"><span data-stu-id="20586-384">On the **Email & collaboration reports** page, find **Spoof detections** and then click **View details**.</span></span> <span data-ttu-id="20586-385">Pour aller directement dans le rapport, ouvrez <https://security.microsoft.com/reports/SpoofMailReportV2> .</span><span class="sxs-lookup"><span data-stu-id="20586-385">To go directly to the report, open <https://security.microsoft.com/reports/SpoofMailReportV2>.</span></span>

![Widget de détections d’usurpation d'& dans la page Rapports de collaboration & courrier électronique](../../media/spoof-detections-widget.png)

<span data-ttu-id="20586-387">Le graphique présente les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="20586-387">The chart shows the following information:</span></span>

- <span data-ttu-id="20586-388">**Pass**</span><span class="sxs-lookup"><span data-stu-id="20586-388">**Pass**</span></span>
- <span data-ttu-id="20586-389">**Échec**</span><span class="sxs-lookup"><span data-stu-id="20586-389">**Fail**</span></span>
- <span data-ttu-id="20586-390">**SoftPass**</span><span class="sxs-lookup"><span data-stu-id="20586-390">**SoftPass**</span></span>
- <span data-ttu-id="20586-391">**Aucune**</span><span class="sxs-lookup"><span data-stu-id="20586-391">**None**</span></span>
- <span data-ttu-id="20586-392">**Other**</span><span class="sxs-lookup"><span data-stu-id="20586-392">**Other**</span></span>

<span data-ttu-id="20586-393">Lorsque vous pointez sur un jour (point de données) dans le graphique, vous pouvez voir combien de messages usurpés ont été détectés et pourquoi.</span><span class="sxs-lookup"><span data-stu-id="20586-393">When you hover over a day (data point) in the chart, you can see how many spoofed messages were detected and why.</span></span>

<span data-ttu-id="20586-394">Dans la page **Rapport** de courrier usurpation d’adresse, vous pouvez  filtrer à la fois le graphique et le tableau de détails en cliquant sur Filtrer et en sélectionnant une ou plusieurs des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="20586-394">On the **Spoof mail report** page, you can filter both the chart and the details table by clicking **Filter** and selecting one or more of the following values:</span></span>

- <span data-ttu-id="20586-395">**Date (UTC)** **Date de début et** date de **fin**</span><span class="sxs-lookup"><span data-stu-id="20586-395">**Date (UTC)** **Start date** and **End date**</span></span>
- <span data-ttu-id="20586-396">**Résultat**:</span><span class="sxs-lookup"><span data-stu-id="20586-396">**Result**:</span></span>
  - <span data-ttu-id="20586-397">**Pass**</span><span class="sxs-lookup"><span data-stu-id="20586-397">**Pass**</span></span>
  - <span data-ttu-id="20586-398">**Échec**</span><span class="sxs-lookup"><span data-stu-id="20586-398">**Fail**</span></span>
  - <span data-ttu-id="20586-399">**SoftPass**</span><span class="sxs-lookup"><span data-stu-id="20586-399">**SoftPass**</span></span>
  - <span data-ttu-id="20586-400">**Aucune**</span><span class="sxs-lookup"><span data-stu-id="20586-400">**None**</span></span>
  - <span data-ttu-id="20586-401">**Other**</span><span class="sxs-lookup"><span data-stu-id="20586-401">**Other**</span></span>
- <span data-ttu-id="20586-402">**Type d’usurpation :** **interne** et **externe**</span><span class="sxs-lookup"><span data-stu-id="20586-402">**Spoof type**: **Internal** and **External**</span></span>

![Page de rapport de courrier électronique usurpant l’Microsoft 365 Defender](../../media/spoof-detections-report-page.png)

<span data-ttu-id="20586-404">Dans le tableau de détails sous le graphique, vous pouvez voir les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="20586-404">In the details table below the graph, you can see the following details:</span></span>

- <span data-ttu-id="20586-405">**Date**</span><span class="sxs-lookup"><span data-stu-id="20586-405">**Date**</span></span>
- <span data-ttu-id="20586-406">**Utilisateur usurpé**</span><span class="sxs-lookup"><span data-stu-id="20586-406">**Spoofed user**</span></span>
- <span data-ttu-id="20586-407">**Infrastructure d’envoi**</span><span class="sxs-lookup"><span data-stu-id="20586-407">**Sending infrastructure**</span></span>
- <span data-ttu-id="20586-408">**Type d’usurpation**</span><span class="sxs-lookup"><span data-stu-id="20586-408">**Spoof type**</span></span>
- <span data-ttu-id="20586-409">**Résultat**</span><span class="sxs-lookup"><span data-stu-id="20586-409">**Result**</span></span>
- <span data-ttu-id="20586-410">**Code de résultat**</span><span class="sxs-lookup"><span data-stu-id="20586-410">**Result code**</span></span>
- <span data-ttu-id="20586-411">**SPF**</span><span class="sxs-lookup"><span data-stu-id="20586-411">**SPF**</span></span>
- <span data-ttu-id="20586-412">**DKIM**</span><span class="sxs-lookup"><span data-stu-id="20586-412">**DKIM**</span></span>
- <span data-ttu-id="20586-413">**DMARC**</span><span class="sxs-lookup"><span data-stu-id="20586-413">**DMARC**</span></span>
- <span data-ttu-id="20586-414">**Nombre de messages**</span><span class="sxs-lookup"><span data-stu-id="20586-414">**Message count**</span></span>

<span data-ttu-id="20586-415">Pour plus d’informations sur les codes de résultats d’authentification composite, consultez les [en-têtes de message anti-courrier](anti-spam-message-headers.md)indésirable Microsoft 365 .</span><span class="sxs-lookup"><span data-stu-id="20586-415">For more information about composite authentication result codes, see [Anti-spam message headers in Microsoft 365](anti-spam-message-headers.md).</span></span>

## <a name="submissions-report"></a><span data-ttu-id="20586-416">Rapport soumissions</span><span class="sxs-lookup"><span data-stu-id="20586-416">Submissions report</span></span>

<span data-ttu-id="20586-417">Le **rapport Soumissions** affiche des informations sur les éléments que les administrateurs ont signalés à Microsoft pour analyse.</span><span class="sxs-lookup"><span data-stu-id="20586-417">The **Submissions** report shows information about items that admins have reported to Microsoft for analysis.</span></span> <span data-ttu-id="20586-418">Pour plus d’informations, voir Utiliser la soumission d’administrateur pour soumettre des messages suspects de courrier indésirable, d’hameçonnage, d’URL et [de fichiers à Microsoft.](admin-submission.md)</span><span class="sxs-lookup"><span data-stu-id="20586-418">For more information, see [Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft](admin-submission.md).</span></span>

<span data-ttu-id="20586-419">Pour afficher le rapport dans le portail  Microsoft 365 Defender, consultez la & collaboration de rapports e-mail \>  \> **& rapports de collaboration.**</span><span class="sxs-lookup"><span data-stu-id="20586-419">To view the report in the Microsoft 365 Defender portal, go to **Reports** \> **Email & collaboration** \> **Email & collaboration reports**.</span></span> <span data-ttu-id="20586-420">Dans la page **& de collaboration,** recherchez **Soumissions,** puis cliquez sur **Afficher les détails.**</span><span class="sxs-lookup"><span data-stu-id="20586-420">On the **Email & collaboration reports** page, find **Submissions** and then click **View details**.</span></span> <span data-ttu-id="20586-421">Pour aller directement dans le rapport, ouvrez <https://security.microsoft.com/adminSubmissionReport> .</span><span class="sxs-lookup"><span data-stu-id="20586-421">To go directly to the report, open <https://security.microsoft.com/adminSubmissionReport>.</span></span> <span data-ttu-id="20586-422">Pour aller aux [soumissions d’administrateur dans le portail Microsoft 365 Defender,](admin-submission.md)cliquez **sur Go to Submissions**.</span><span class="sxs-lookup"><span data-stu-id="20586-422">To go to [admin submissions in the Microsoft 365 Defender portal](admin-submission.md), click **Go to Submissions**.</span></span>

![Widget soumissions sur la page rapports de collaboration & courrier électronique](../../media/submissions-report-widget.png)

<span data-ttu-id="20586-424">Le graphique présente les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="20586-424">The chart shows the following information:</span></span>

- <span data-ttu-id="20586-425">**Pending**</span><span class="sxs-lookup"><span data-stu-id="20586-425">**Pending**</span></span>
- <span data-ttu-id="20586-426">**Terminée**</span><span class="sxs-lookup"><span data-stu-id="20586-426">**Completed**</span></span>

<span data-ttu-id="20586-427">Dans la page **Soumissions,** vous pouvez filtrer le graphique  et le tableau de détails en cliquant sur Filtrer et en sélectionnant une ou plusieurs des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="20586-427">On the **Submissions** page, you can filter both the chart and the details table by clicking **Filter** and selecting one or more of the following values:</span></span>

- <span data-ttu-id="20586-428">**Date signalée :** **heure de début** et heure de **fin**</span><span class="sxs-lookup"><span data-stu-id="20586-428">**Date reported**: **Start time** and **End time**</span></span>
- <span data-ttu-id="20586-429">**Type de soumission**: **e-mail,** **URL** ou **fichier**</span><span class="sxs-lookup"><span data-stu-id="20586-429">**Submission type**: **Email**, **URL**, or **File**</span></span>
- <span data-ttu-id="20586-430">**ID de soumission**</span><span class="sxs-lookup"><span data-stu-id="20586-430">**Submission ID**</span></span>
- <span data-ttu-id="20586-431">**ID de message réseau**</span><span class="sxs-lookup"><span data-stu-id="20586-431">**Network Message ID**</span></span>
- <span data-ttu-id="20586-432">**Sender**</span><span class="sxs-lookup"><span data-stu-id="20586-432">**Sender**</span></span>
- <span data-ttu-id="20586-433">**Name**</span><span class="sxs-lookup"><span data-stu-id="20586-433">**Name**</span></span>
- <span data-ttu-id="20586-434">**Soumis par**</span><span class="sxs-lookup"><span data-stu-id="20586-434">**Submitted by**</span></span>
- <span data-ttu-id="20586-435">**Raison de l’envoi :** courrier non **indésirable,** **hameçonnage,** **programme malveillant** ou **courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="20586-435">**Reason for submitting**: **Not junk**, **Phish**, **Malware**, or **Spam**</span></span>
- <span data-ttu-id="20586-436">**État de la rescan**: **En attente** ou **terminé**</span><span class="sxs-lookup"><span data-stu-id="20586-436">**Rescan status**: **Pending** or **Completed**</span></span>

<span data-ttu-id="20586-437">Le tableau de détails sous le graphique  présente les mêmes informations  et possède les  mêmes **options** de colonnes De groupe ou de personnalisation que sous l’onglet Soumis pour analyse dans envois de collaboration & courrier \> **électronique.**</span><span class="sxs-lookup"><span data-stu-id="20586-437">The details table below the graph shows the same information and has the same **Group** or **Customize columns** options as on the **Submitted for analysis** tab at **Email & collaboration** \> **Submissions**.</span></span> <span data-ttu-id="20586-438">Pour plus d’informations, voir [Afficher les soumissions d’administrateur à Microsoft.](admin-submission.md#view-admin-submissions-to-microsoft)</span><span class="sxs-lookup"><span data-stu-id="20586-438">For more information, see [View admin submissions to Microsoft](admin-submission.md#view-admin-submissions-to-microsoft).</span></span>

![Page de rapport soumissions dans le portail Microsoft 365 Defender web](../../media/submissions-report-page.png)

## <a name="threat-protection-status-report"></a><span data-ttu-id="20586-440">Rapport sur l’état de la protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="20586-440">Threat protection status report</span></span>

<span data-ttu-id="20586-441">Le **rapport d’état de la protection** contre les menaces est disponible dans EOP et Defender pour Office 365 ; toutefois, les rapports contiennent des données différentes.</span><span class="sxs-lookup"><span data-stu-id="20586-441">The **Threat protection status** report is available in both EOP and Defender for Office 365; however, the reports contain different data.</span></span> <span data-ttu-id="20586-442">Par exemple, les clients EOP peuvent afficher des informations sur les programmes malveillants détectés dans le courrier électronique, mais pas sur les fichiers [malveillants détectés](mdo-for-spo-odb-and-teams.md)par les pièces jointes Safe pour SharePoint, OneDrive et Microsoft Teams .</span><span class="sxs-lookup"><span data-stu-id="20586-442">For example, EOP customers can view information about malware detected in email, but not information about malicious files detected by [Safe Attachments for SharePoint, OneDrive, and Microsoft Teams](mdo-for-spo-odb-and-teams.md).</span></span>

<span data-ttu-id="20586-443">Le rapport fournit le nombre de messages électroniques avec du contenu malveillant, tels que des fichiers ou des adresses de site web (URL) qui ont été bloqués par le moteur anti-programme malveillant, la purge automatique d’heure zéro [(ZAP)](zero-hour-auto-purge.md)et Defender pour des fonctionnalités de Office 365 telles que les liens [Safe,](safe-links.md)les pièces [jointes Safe](safe-attachments.md)et les fonctionnalités de protection contre l’emprunt d’identité dans les stratégies [anti-hameçonnage.](set-up-anti-phishing-policies.md#exclusive-settings-in-anti-phishing-policies-in-microsoft-defender-for-office-365)</span><span class="sxs-lookup"><span data-stu-id="20586-443">The report provides the count of email messages with malicious content, such as files or website addresses (URLs) that were blocked by the anti-malware engine, [zero-hour auto purge (ZAP)](zero-hour-auto-purge.md), and Defender for Office 365 features like [Safe Links](safe-links.md), [Safe Attachments](safe-attachments.md), and [impersonation protection features in anti-phishing policies](set-up-anti-phishing-policies.md#exclusive-settings-in-anti-phishing-policies-in-microsoft-defender-for-office-365).</span></span> <span data-ttu-id="20586-444">Vous pouvez utiliser ces informations pour identifier les tendances ou déterminer si des stratégies d’organisation doivent être ajuster.</span><span class="sxs-lookup"><span data-stu-id="20586-444">You can use this information to identify trends or determine whether organization policies need adjustment.</span></span>

<span data-ttu-id="20586-445">**Remarque**: il est important de comprendre que si un message est envoyé à cinq destinataires, nous le compterons comme cinq messages différents et pas un seul message.</span><span class="sxs-lookup"><span data-stu-id="20586-445">**Note**: It's important to understand that if a message is sent to five recipients we count it as five different messages and not one message.</span></span>

<span data-ttu-id="20586-446">Pour afficher le rapport dans le portail  Microsoft 365 Defender, consultez la & collaboration de rapports e-mail \>  \> **& rapports de collaboration.**</span><span class="sxs-lookup"><span data-stu-id="20586-446">To view the report in the Microsoft 365 Defender portal, go to **Reports** \> **Email & collaboration** \> **Email & collaboration reports**.</span></span> <span data-ttu-id="20586-447">Dans la page **Rapports de collaboration & courrier** électronique, recherchez l’état de la **protection** contre les menaces, puis cliquez sur Afficher **les détails.**</span><span class="sxs-lookup"><span data-stu-id="20586-447">On the **Email & collaboration reports** page, find **Threat protection status** and then click **View details**.</span></span> <span data-ttu-id="20586-448">Pour aller directement dans le rapport, ouvrez l’une des URL suivantes :</span><span class="sxs-lookup"><span data-stu-id="20586-448">To go directly to the report, open one of the following URLs:</span></span>

- <span data-ttu-id="20586-449">Defender pour Office 365 :<https://security.microsoft.com/reports/TPSAggregateReportATP></span><span class="sxs-lookup"><span data-stu-id="20586-449">Defender for Office 365: <https://security.microsoft.com/reports/TPSAggregateReportATP></span></span>
- <span data-ttu-id="20586-450">EOP : <https://security.microsoft.com/reports/TPSAggregateReport></span><span class="sxs-lookup"><span data-stu-id="20586-450">EOP: <https://security.microsoft.com/reports/TPSAggregateReport></span></span>

![Widget d’état de la protection contre les menaces dans la page Rapports de collaboration & courrier électronique](../../media/threat-protection-status-report-widget.png)

<span data-ttu-id="20586-452">Par défaut, le graphique affiche les données des 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="20586-452">By default, the chart shows data for the past 7 days.</span></span> <span data-ttu-id="20586-453">Si vous cliquez sur **Filtrer** dans la page du rapport d’état de la **protection** contre les menaces, vous pouvez sélectionner une plage de dates de 90 jours (les abonnements d’essai peuvent être limités à 30 jours).</span><span class="sxs-lookup"><span data-stu-id="20586-453">If you click **Filter** on the **Threat protection status report** page, you can select a 90 day date range (trial subscriptions might be limited to 30 days).</span></span> <span data-ttu-id="20586-454">Le tableau de détails autorise le filtrage pendant 30 jours.</span><span class="sxs-lookup"><span data-stu-id="20586-454">The details table allows filtering for 30 days.</span></span>

<span data-ttu-id="20586-455">Les vues disponibles sont décrites dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="20586-455">The available views are described in the following sections.</span></span>

### <a name="view-data-by-overview"></a><span data-ttu-id="20586-456">Afficher les données par vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="20586-456">View data by Overview</span></span>

![Vue d’ensemble dans le rapport d’état de la protection contre les menaces](../../media/threat-protection-status-report-overview-view.png)

<span data-ttu-id="20586-458">Dans **l’affichage Des données par vue d’ensemble,** les informations de détection suivantes sont affichées dans le graphique :</span><span class="sxs-lookup"><span data-stu-id="20586-458">In the **View data by Overview** view, the following detection information is shown in the chart:</span></span>

- <span data-ttu-id="20586-459">**Programme malveillant de messagerie**</span><span class="sxs-lookup"><span data-stu-id="20586-459">**Email malware**</span></span>
- <span data-ttu-id="20586-460">**Hameçonnage par e-mail**</span><span class="sxs-lookup"><span data-stu-id="20586-460">**Email phish**</span></span>
- <span data-ttu-id="20586-461">**Programme malveillant de contenu**</span><span class="sxs-lookup"><span data-stu-id="20586-461">**Content malware**</span></span>

<span data-ttu-id="20586-462">Aucun tableau de détails n’est disponible sous le graphique.</span><span class="sxs-lookup"><span data-stu-id="20586-462">No details table is available below the chart.</span></span>

<span data-ttu-id="20586-463">Si vous cliquez **sur Filtre,** les filtres suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="20586-463">If you click **Filter**, the following filters are available:</span></span>

- <span data-ttu-id="20586-464">**Date (UTC)** **Date de début et** date de **fin**</span><span class="sxs-lookup"><span data-stu-id="20586-464">**Date (UTC)** **Start date** and **End date**</span></span>
- <span data-ttu-id="20586-465">**Détection :** programme **malveillant de messagerie,** **hameçonnage de messagerie** ou programme malveillant de **contenu**</span><span class="sxs-lookup"><span data-stu-id="20586-465">**Detection**: **Email malware**, **Email phish**, or **Content malware**</span></span>
- <span data-ttu-id="20586-466">**Protégé par**: **MDO** (Defender for Office 365) ou **EOP**</span><span class="sxs-lookup"><span data-stu-id="20586-466">**Protected by**: **MDO** (Defender for Office 365) or **EOP**</span></span>
- <span data-ttu-id="20586-467">**Balise**: filtrer les résultats par utilisateurs ou groupes pour lesquels la balise utilisateur spécifiée a été appliquée (y compris les comptes de priorité).</span><span class="sxs-lookup"><span data-stu-id="20586-467">**Tag**: Filter the results by users or groups that have had the specified user tag applied (including priority accounts).</span></span> <span data-ttu-id="20586-468">Pour plus d’informations sur les balises utilisateur, voir [Balises utilisateur.](user-tags.md)</span><span class="sxs-lookup"><span data-stu-id="20586-468">For more information about user tags, see [User tags](user-tags.md).</span></span>
- <span data-ttu-id="20586-469">**Direction**</span><span class="sxs-lookup"><span data-stu-id="20586-469">**Direction**</span></span>
- <span data-ttu-id="20586-470">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="20586-470">**Domain**</span></span>
- <span data-ttu-id="20586-471">**Type de stratégie**</span><span class="sxs-lookup"><span data-stu-id="20586-471">**Policy type**</span></span>

<span data-ttu-id="20586-472">Lorsque vous avez terminé la configuration des filtres, cliquez sur **Appliquer,** **Annuler** ou **Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="20586-472">When you're finished configuring the filters, click **Apply**, **Cancel**, or **Clear filters**.</span></span>

### <a name="view-data-by-email--phish-and-chart-breakdown-by-detection-technology"></a><span data-ttu-id="20586-473">Afficher les données par hameçonnage de messagerie \> électronique et répartition des graphiques par technologie de détection</span><span class="sxs-lookup"><span data-stu-id="20586-473">View data by Email \> Phish and Chart breakdown by Detection Technology</span></span>

![Affichage de la technologie de détection pour le courrier d’hameçonnage dans le rapport d’état de la protection contre les menaces](../../media/threat-protection-status-report-phishing-detection-tech-view.png)

<span data-ttu-id="20586-475">Dans **l’affichage \> des données par hameçonnage par courrier électronique** et répartition **du** graphique par technologie de détection, les informations suivantes sont affichées dans le graphique :</span><span class="sxs-lookup"><span data-stu-id="20586-475">In the **View data by Email \> Phish** and **Chart breakdown by Detection Technology** view, the following information is shown in the chart:</span></span>

- <span data-ttu-id="20586-476">**Réputation malveillante d’URL**: réputation d’URL malveillante générée à partir de <sup>\*</sup> Defender pour Office 365 détonations dans d’autres Microsoft 365 clients.</span><span class="sxs-lookup"><span data-stu-id="20586-476">**URL malicious reputation**<sup>\*</sup>: Malicious URL reputation generated from Defender for Office 365 detonations in other Microsoft 365 customers.</span></span>
- <span data-ttu-id="20586-477">**Filtre avancé :** signaux de hameçonnage basés sur l’apprentissage automatique.</span><span class="sxs-lookup"><span data-stu-id="20586-477">**Advanced filter**: Phishing signals based on machine learning.</span></span>
- <span data-ttu-id="20586-478">**Filtre général :** signaux de hameçonnage basés sur des règles d’analyste.</span><span class="sxs-lookup"><span data-stu-id="20586-478">**General filter**: Phishing signals based on analyst rules.</span></span>
- <span data-ttu-id="20586-479">**Usurpation d’adresse intra-organisation**: l’expéditeur tente d’usurper le domaine du destinataire.</span><span class="sxs-lookup"><span data-stu-id="20586-479">**Spoof intra-org**: Sender is trying to spoof the recipient domain.</span></span>
- <span data-ttu-id="20586-480">**Usurpation d’un domaine externe**: l’expéditeur tente d’usurper un autre domaine.</span><span class="sxs-lookup"><span data-stu-id="20586-480">**Spoof external domain**: Sender is trying to spoof some other domain.</span></span>
- <span data-ttu-id="20586-481">**Usurpation d’identité DMARC**: échec de l’authentification DMARC sur les messages.</span><span class="sxs-lookup"><span data-stu-id="20586-481">**Spoof DMARC**: DMARC authentication failure on messages.</span></span>
- <span data-ttu-id="20586-482">**Marque d’emprunt d’identité**: emprunt d’identité de marques connues basées sur des expéditeurs.</span><span class="sxs-lookup"><span data-stu-id="20586-482">**Impersonation brand**: Impersonation of well-known brands based on senders.</span></span>
- <span data-ttu-id="20586-483">**Détection d’analyse mixte**</span><span class="sxs-lookup"><span data-stu-id="20586-483">**Mixed analysis detection**</span></span>
- <span data-ttu-id="20586-484">**Réputation des fichiers**</span><span class="sxs-lookup"><span data-stu-id="20586-484">**File reputation**</span></span>
- <span data-ttu-id="20586-485">**Correspondance de l’empreinte**</span><span class="sxs-lookup"><span data-stu-id="20586-485">**Fingerprint matching**</span></span>
- <span data-ttu-id="20586-486">**Réputation de détonation d’URL**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="20586-486">**URL detonation reputation**<sup>\*</sup></span></span>
- <span data-ttu-id="20586-487">**Détonation d’URL**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="20586-487">**URL detonation**<sup>\*</sup></span></span>
- <span data-ttu-id="20586-488">**Utilisateur de l’emprunt d’identité**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="20586-488">**Impersonation user**<sup>\*</sup></span></span>
- <span data-ttu-id="20586-489">**Domaine d’emprunt d’identité**: emprunt d’identité des domaines que le client <sup>\*</sup> possède ou définit.</span><span class="sxs-lookup"><span data-stu-id="20586-489">**Impersonation domain**<sup>\*</sup>: Impersonation of domains that the customer owns or defines.</span></span>
- <span data-ttu-id="20586-490">**Emprunt d’identité d’intelligence de** boîte aux lettres : emprunt d’identité des utilisateurs définis par l’administrateur ou appris par le biais de l’intelligence <sup>\*</sup> des boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="20586-490">**Mailbox intelligence impersonation**<sup>\*</sup>: Impersonation of users defined by admin or learned through mailbox intelligence.</span></span>
- <span data-ttu-id="20586-491">**Détonation de fichier**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="20586-491">**File detonation**<sup>\*</sup></span></span>
- <span data-ttu-id="20586-492">**Campagne**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="20586-492">**Campaign**<sup>\*</sup></span></span>

<span data-ttu-id="20586-493">Dans le tableau de détails sous le graphique, les informations suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="20586-493">In the details table below the chart, the following information is available:</span></span>

- <span data-ttu-id="20586-494">**Date**</span><span class="sxs-lookup"><span data-stu-id="20586-494">**Date**</span></span>
- <span data-ttu-id="20586-495">**Subject**</span><span class="sxs-lookup"><span data-stu-id="20586-495">**Subject**</span></span>
- <span data-ttu-id="20586-496">**Expéditeur**</span><span class="sxs-lookup"><span data-stu-id="20586-496">**Sender**</span></span>
- <span data-ttu-id="20586-497">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="20586-497">**Recipients**</span></span>
- <span data-ttu-id="20586-498">**Détecté par**</span><span class="sxs-lookup"><span data-stu-id="20586-498">**Detected by**</span></span>
- <span data-ttu-id="20586-499">**État de remise**</span><span class="sxs-lookup"><span data-stu-id="20586-499">**Delivery Status**</span></span>
- <span data-ttu-id="20586-500">**Source de compromis**</span><span class="sxs-lookup"><span data-stu-id="20586-500">**Source of Compromise**</span></span>
- <span data-ttu-id="20586-501">**Tags**</span><span class="sxs-lookup"><span data-stu-id="20586-501">**Tags**</span></span>

<span data-ttu-id="20586-502">Si vous cliquez **sur Filtre,** les filtres suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="20586-502">If you click **Filter**, the following filters are available:</span></span>

- <span data-ttu-id="20586-503">**Date (UTC)** **Date de début et** date de **fin**</span><span class="sxs-lookup"><span data-stu-id="20586-503">**Date (UTC)** **Start date** and **End date**</span></span>
- <span data-ttu-id="20586-504">**Détection**</span><span class="sxs-lookup"><span data-stu-id="20586-504">**Detection**</span></span>
- <span data-ttu-id="20586-505">**Protégé par**: **MDO** (Defender for Office 365) ou **EOP**</span><span class="sxs-lookup"><span data-stu-id="20586-505">**Protected by**: **MDO** (Defender for Office 365) or **EOP**</span></span>
- <span data-ttu-id="20586-506">**Direction**</span><span class="sxs-lookup"><span data-stu-id="20586-506">**Direction**</span></span>
- <span data-ttu-id="20586-507">**Balise**: filtrer les résultats par utilisateurs ou groupes pour lesquels la balise utilisateur spécifiée a été appliquée (y compris les comptes de priorité).</span><span class="sxs-lookup"><span data-stu-id="20586-507">**Tag**: Filter the results by users or groups that have had the specified user tag applied (including priority accounts).</span></span> <span data-ttu-id="20586-508">Pour plus d’informations sur les balises utilisateur, voir [Balises utilisateur.](user-tags.md)</span><span class="sxs-lookup"><span data-stu-id="20586-508">For more information about user tags, see [User tags](user-tags.md).</span></span>
- <span data-ttu-id="20586-509">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="20586-509">**Domain**</span></span>
- <span data-ttu-id="20586-510">**Type de stratégie**</span><span class="sxs-lookup"><span data-stu-id="20586-510">**Policy type**</span></span>
- <span data-ttu-id="20586-511">**Nom de la stratégie** (tableau de détails uniquement)</span><span class="sxs-lookup"><span data-stu-id="20586-511">**Policy name** (details table only)</span></span>
- <span data-ttu-id="20586-512">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="20586-512">**Recipients**</span></span>

<span data-ttu-id="20586-513">Lorsque vous avez terminé la configuration des filtres, cliquez sur **Appliquer,** **Annuler** ou **Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="20586-513">When you're finished configuring the filters, click **Apply**, **Cancel**, or **Clear filters**.</span></span>

### <a name="view-data-by-email--malware-and-chart-breakdown-by-detection-technology"></a><span data-ttu-id="20586-514">Afficher les données par programme malveillant et \> répartition des graphiques par technologie de détection</span><span class="sxs-lookup"><span data-stu-id="20586-514">View data by Email \> Malware and Chart breakdown by Detection Technology</span></span>

![Affichage de la technologie de détection pour les programmes malveillants dans le rapport d’état de la protection contre les menaces](../../media/threat-protection-status-report-malware-detection-tech-view.png)

<span data-ttu-id="20586-516">Dans **l’affichage \> des données par programme** malveillant par courrier électronique et **répartition des** graphiques par technologie de détection, les informations suivantes sont affichées dans le graphique :</span><span class="sxs-lookup"><span data-stu-id="20586-516">In the **View data by Email \> Malware** and **Chart breakdown by Detection Technology** view, the following information is shown in the chart:</span></span>

- <span data-ttu-id="20586-517">**Détonation de fichier** <sup>\*</sup> : détection par Safe pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="20586-517">**File detonation**<sup>\*</sup>: Detection by Safe Attachments.</span></span>
- <span data-ttu-id="20586-518">**Réputation de détonation de fichier**: toutes les réputations de fichiers <sup>\*</sup> malveillants générées par Defender pour Office 365 détonations.</span><span class="sxs-lookup"><span data-stu-id="20586-518">**File detonation reputation**<sup>\*</sup>: All malicious file reputation generated by Defender for Office 365 detonations.</span></span>
- <span data-ttu-id="20586-519">**Réputation des fichiers**</span><span class="sxs-lookup"><span data-stu-id="20586-519">**File reputation**</span></span>
- <span data-ttu-id="20586-520">**Moteur anti-programme malveillant :** détection à partir de moteurs <sup>\*</sup> anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="20586-520">**Anti-malware engine**<sup>\*</sup>: Detection from anti-malware engines.</span></span>
- <span data-ttu-id="20586-521">Blocage du type de fichier de stratégie **anti-programme** malveillant : il s’adresse aux messages électroniques filtrés en raison du type de fichier malveillant identifié dans le message.</span><span class="sxs-lookup"><span data-stu-id="20586-521">**Anti-malware policy file type block**: These are email messages filtered out due to the type of malicious file identified in the message.</span></span>
- <span data-ttu-id="20586-522">**Réputation d’URL malveillante**</span><span class="sxs-lookup"><span data-stu-id="20586-522">**URL malicious reputation**</span></span>
- <span data-ttu-id="20586-523">**Détonation d’URL**</span><span class="sxs-lookup"><span data-stu-id="20586-523">**URL detonation**</span></span>
- <span data-ttu-id="20586-524">**Réputation de détonation d’URL**</span><span class="sxs-lookup"><span data-stu-id="20586-524">**URL detonation reputation**</span></span>
- <span data-ttu-id="20586-525">**Campagne**</span><span class="sxs-lookup"><span data-stu-id="20586-525">**Campaign**</span></span>

<span data-ttu-id="20586-526">Dans le tableau de détails sous le graphique, les informations suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="20586-526">In the details table below the chart, the following information is available:</span></span>

- <span data-ttu-id="20586-527">**Date**</span><span class="sxs-lookup"><span data-stu-id="20586-527">**Date**</span></span>
- <span data-ttu-id="20586-528">**Subject**</span><span class="sxs-lookup"><span data-stu-id="20586-528">**Subject**</span></span>
- <span data-ttu-id="20586-529">**Expéditeur**</span><span class="sxs-lookup"><span data-stu-id="20586-529">**Sender**</span></span>
- <span data-ttu-id="20586-530">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="20586-530">**Recipients**</span></span>
- <span data-ttu-id="20586-531">**Détecté par**</span><span class="sxs-lookup"><span data-stu-id="20586-531">**Detected by**</span></span>
- <span data-ttu-id="20586-532">**État de remise**</span><span class="sxs-lookup"><span data-stu-id="20586-532">**Delivery Status**</span></span>
- <span data-ttu-id="20586-533">**Source de compromis**</span><span class="sxs-lookup"><span data-stu-id="20586-533">**Source of Compromise**</span></span>
- <span data-ttu-id="20586-534">**Tags**</span><span class="sxs-lookup"><span data-stu-id="20586-534">**Tags**</span></span>

<span data-ttu-id="20586-535">Si vous cliquez **sur Filtre,** les filtres suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="20586-535">If you click **Filter**, the following filters are available:</span></span>

- <span data-ttu-id="20586-536">**Date (UTC)** **Date de début et** date de **fin**</span><span class="sxs-lookup"><span data-stu-id="20586-536">**Date (UTC)** **Start date** and **End date**</span></span>
- <span data-ttu-id="20586-537">**Détection**</span><span class="sxs-lookup"><span data-stu-id="20586-537">**Detection**</span></span>
- <span data-ttu-id="20586-538">**Protégé par**: **MDO** (Defender for Office 365) ou **EOP**</span><span class="sxs-lookup"><span data-stu-id="20586-538">**Protected by**: **MDO** (Defender for Office 365) or **EOP**</span></span>
- <span data-ttu-id="20586-539">**Direction**</span><span class="sxs-lookup"><span data-stu-id="20586-539">**Direction**</span></span>
- <span data-ttu-id="20586-540">**Balise**: filtrer les résultats par utilisateurs ou groupes pour lesquels la balise utilisateur spécifiée a été appliquée (y compris les comptes de priorité).</span><span class="sxs-lookup"><span data-stu-id="20586-540">**Tag**: Filter the results by users or groups that have had the specified user tag applied (including priority accounts).</span></span> <span data-ttu-id="20586-541">Pour plus d’informations sur les balises utilisateur, voir [Balises utilisateur.](user-tags.md)</span><span class="sxs-lookup"><span data-stu-id="20586-541">For more information about user tags, see [User tags](user-tags.md).</span></span>
- <span data-ttu-id="20586-542">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="20586-542">**Domain**</span></span>
- <span data-ttu-id="20586-543">**Type de stratégie**</span><span class="sxs-lookup"><span data-stu-id="20586-543">**Policy type**</span></span>
- <span data-ttu-id="20586-544">**Nom de la stratégie** (tableau de détails uniquement)</span><span class="sxs-lookup"><span data-stu-id="20586-544">**Policy name** (details table only)</span></span>
- <span data-ttu-id="20586-545">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="20586-545">**Recipients**</span></span>

<span data-ttu-id="20586-546">Lorsque vous avez terminé la configuration des filtres, cliquez sur **Appliquer,** **Annuler** ou **Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="20586-546">When you're finished configuring the filters, click **Apply**, **Cancel**, or **Clear filters**.</span></span>

### <a name="chart-breakdown-by-policy-type-and-view-data-by-email--phish-or-view-data-by-email--malware"></a><span data-ttu-id="20586-547">Répartition des graphiques par type de stratégie et affichage des données par hameçonnage de messagerie ou affichage des données par programme malveillant \> de \> messagerie</span><span class="sxs-lookup"><span data-stu-id="20586-547">Chart breakdown by Policy type and View data by Email \> Phish or View data by Email \> Malware</span></span>

![Affichage du type de stratégie pour les courriers électroniques de hameçonnage ou de programmes malveillants dans le rapport d’état de la protection contre les menaces](../../media/threat-protection-status-report-phishing-policy-type-view.png)

<span data-ttu-id="20586-549">Dans la répartition **du graphique** par type de stratégie et l’affichage des données par hameçonnage de messagerie ou affichage des données par affichage des programmes malveillants de messagerie, les informations suivantes sont affichées dans les graphiques : **\>** **\>**</span><span class="sxs-lookup"><span data-stu-id="20586-549">In the **Chart breakdown by Policy type** and **View data by Email \> Phish** or **View data by Email \> Malware** views, the following information is shown in the charts:</span></span>

- <span data-ttu-id="20586-550">**Anti-programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="20586-550">**Anti-malware**</span></span>
- <span data-ttu-id="20586-551">**Safe Pièces jointes**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="20586-551">**Safe Attachments**<sup>\*</sup></span></span>
- <span data-ttu-id="20586-552">**Anti-hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="20586-552">**Anti-phish**</span></span>
- <span data-ttu-id="20586-553">**Anti-courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="20586-553">**Anti-spam**</span></span>
- <span data-ttu-id="20586-554">**Règle de flux de messagerie** (également appelée règle de transport)</span><span class="sxs-lookup"><span data-stu-id="20586-554">**Mail flow rule** (also known as a transport rule)</span></span>
- <span data-ttu-id="20586-555">**Autres**</span><span class="sxs-lookup"><span data-stu-id="20586-555">**Others**</span></span>

<span data-ttu-id="20586-556">Dans le tableau de détails sous le graphique, les informations suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="20586-556">In the details table below the chart, the following information is available:</span></span>

- <span data-ttu-id="20586-557">**Date**</span><span class="sxs-lookup"><span data-stu-id="20586-557">**Date**</span></span>
- <span data-ttu-id="20586-558">**Subject**</span><span class="sxs-lookup"><span data-stu-id="20586-558">**Subject**</span></span>
- <span data-ttu-id="20586-559">**Expéditeur**</span><span class="sxs-lookup"><span data-stu-id="20586-559">**Sender**</span></span>
- <span data-ttu-id="20586-560">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="20586-560">**Recipients**</span></span>
- <span data-ttu-id="20586-561">**Détecté par**</span><span class="sxs-lookup"><span data-stu-id="20586-561">**Detected by**</span></span>
- <span data-ttu-id="20586-562">**État de remise**</span><span class="sxs-lookup"><span data-stu-id="20586-562">**Delivery Status**</span></span>
- <span data-ttu-id="20586-563">**Source de compromis**</span><span class="sxs-lookup"><span data-stu-id="20586-563">**Source of Compromise**</span></span>
- <span data-ttu-id="20586-564">**Tags**</span><span class="sxs-lookup"><span data-stu-id="20586-564">**Tags**</span></span>

<span data-ttu-id="20586-565">Si vous cliquez **sur Filtre,** les filtres suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="20586-565">If you click **Filter**, the following filters are available:</span></span>

- <span data-ttu-id="20586-566">**Date (UTC)** **Date de début et** date de **fin**</span><span class="sxs-lookup"><span data-stu-id="20586-566">**Date (UTC)** **Start date** and **End date**</span></span>
- <span data-ttu-id="20586-567">**Détection**</span><span class="sxs-lookup"><span data-stu-id="20586-567">**Detection**</span></span>
- <span data-ttu-id="20586-568">**Protégé par**: **MDO** (Defender for Office 365) ou **EOP**</span><span class="sxs-lookup"><span data-stu-id="20586-568">**Protected by**: **MDO** (Defender for Office 365) or **EOP**</span></span>
- <span data-ttu-id="20586-569">**Direction**</span><span class="sxs-lookup"><span data-stu-id="20586-569">**Direction**</span></span>
- <span data-ttu-id="20586-570">**Balise**: filtrer les résultats par utilisateurs ou groupes pour lesquels la balise utilisateur spécifiée a été appliquée (y compris les comptes de priorité).</span><span class="sxs-lookup"><span data-stu-id="20586-570">**Tag**: Filter the results by users or groups that have had the specified user tag applied (including priority accounts).</span></span> <span data-ttu-id="20586-571">Pour plus d’informations sur les balises utilisateur, voir [Balises utilisateur.](user-tags.md)</span><span class="sxs-lookup"><span data-stu-id="20586-571">For more information about user tags, see [User tags](user-tags.md).</span></span>
- <span data-ttu-id="20586-572">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="20586-572">**Domain**</span></span>
- <span data-ttu-id="20586-573">**Type de stratégie**</span><span class="sxs-lookup"><span data-stu-id="20586-573">**Policy type**</span></span>
- <span data-ttu-id="20586-574">**Nom de la stratégie** (tableau de détails uniquement)</span><span class="sxs-lookup"><span data-stu-id="20586-574">**Policy name** (details table only)</span></span>
- <span data-ttu-id="20586-575">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="20586-575">**Recipients**</span></span>

<span data-ttu-id="20586-576">Lorsque vous avez terminé la configuration des filtres, cliquez sur **Appliquer,** **Annuler** ou **Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="20586-576">When you're finished configuring the filters, click **Apply**, **Cancel**, or **Clear filters**.</span></span>

### <a name="chart-breakdown-by-delivery-status-and-view-data-by-email--phish-or-view-data-by-email--malware"></a><span data-ttu-id="20586-577">Répartition des graphiques par état de remise et affichage des données par hameçonnage de messagerie ou affichage des données par programme malveillant \> de \> messagerie</span><span class="sxs-lookup"><span data-stu-id="20586-577">Chart breakdown by Delivery status and View data by Email \> Phish or View data by Email \> Malware</span></span>

![Affichage de l’état de remise du courrier électronique de hameçonnage et des programmes malveillants dans le rapport d’état de la protection contre les menaces](../../media/threat-protection-status-report-phishing-delivery-status-view.png)

<span data-ttu-id="20586-579">Dans la répartition **du graphique** par état de remise et affichage des données par hameçonnage de messagerie ou affichage des données par affichage des programmes malveillants de messagerie, les informations suivantes sont affichées dans les graphiques : **\>** **\>**</span><span class="sxs-lookup"><span data-stu-id="20586-579">In the **Chart breakdown by Delivery status** and **View data by Email \> Phish** or **View data by Email \> Malware** views, the following information is shown in the charts:</span></span>

- <span data-ttu-id="20586-580">**Boîte aux lettres hébergée : Boîte de réception**</span><span class="sxs-lookup"><span data-stu-id="20586-580">**Hosted mailbox: Inbox**</span></span>
- <span data-ttu-id="20586-581">**Boîte aux lettres hébergée : courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="20586-581">**Hosted mailbox: Junk**</span></span>
- <span data-ttu-id="20586-582">**Boîte aux lettres hébergée : dossier personnalisé**</span><span class="sxs-lookup"><span data-stu-id="20586-582">**Hosted mailbox: Custom folder**</span></span>
- <span data-ttu-id="20586-583">**Boîte aux lettres hébergée : éléments supprimés**</span><span class="sxs-lookup"><span data-stu-id="20586-583">**Hosted mailbox: Deleted items**</span></span>
- <span data-ttu-id="20586-584">**Forwarded**</span><span class="sxs-lookup"><span data-stu-id="20586-584">**Forwarded**</span></span>
- <span data-ttu-id="20586-585">**Serveur local : remis**</span><span class="sxs-lookup"><span data-stu-id="20586-585">**On-premises server: Delivered**</span></span>
- <span data-ttu-id="20586-586">**Mise en quarantaine**</span><span class="sxs-lookup"><span data-stu-id="20586-586">**Quarantine**</span></span>
- <span data-ttu-id="20586-587">**Échec de remise**</span><span class="sxs-lookup"><span data-stu-id="20586-587">**Delivery failed**</span></span>
- <span data-ttu-id="20586-588">**Dropped**</span><span class="sxs-lookup"><span data-stu-id="20586-588">**Dropped**</span></span>

<span data-ttu-id="20586-589">Dans le tableau de détails sous le graphique, les informations suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="20586-589">In the details table below the chart, the following information is available:</span></span>

- <span data-ttu-id="20586-590">**Date**</span><span class="sxs-lookup"><span data-stu-id="20586-590">**Date**</span></span>
- <span data-ttu-id="20586-591">**Subject**</span><span class="sxs-lookup"><span data-stu-id="20586-591">**Subject**</span></span>
- <span data-ttu-id="20586-592">**Expéditeur**</span><span class="sxs-lookup"><span data-stu-id="20586-592">**Sender**</span></span>
- <span data-ttu-id="20586-593">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="20586-593">**Recipients**</span></span>
- <span data-ttu-id="20586-594">**Détecté par**</span><span class="sxs-lookup"><span data-stu-id="20586-594">**Detected by**</span></span>
- <span data-ttu-id="20586-595">**État de remise**</span><span class="sxs-lookup"><span data-stu-id="20586-595">**Delivery Status**</span></span>
- <span data-ttu-id="20586-596">**Source de compromis**</span><span class="sxs-lookup"><span data-stu-id="20586-596">**Source of Compromise**</span></span>
- <span data-ttu-id="20586-597">**Tags**</span><span class="sxs-lookup"><span data-stu-id="20586-597">**Tags**</span></span>

<span data-ttu-id="20586-598">Si vous cliquez **sur Filtre,** les filtres suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="20586-598">If you click **Filter**, the following filters are available:</span></span>

- <span data-ttu-id="20586-599">**Date (UTC)** **Date de début et** date de **fin**</span><span class="sxs-lookup"><span data-stu-id="20586-599">**Date (UTC)** **Start date** and **End date**</span></span>
- <span data-ttu-id="20586-600">**Détection**</span><span class="sxs-lookup"><span data-stu-id="20586-600">**Detection**</span></span>
- <span data-ttu-id="20586-601">**Protégé par**: **MDO** (Defender for Office 365) ou **EOP**</span><span class="sxs-lookup"><span data-stu-id="20586-601">**Protected by**: **MDO** (Defender for Office 365) or **EOP**</span></span>
- <span data-ttu-id="20586-602">**Direction**</span><span class="sxs-lookup"><span data-stu-id="20586-602">**Direction**</span></span>
- <span data-ttu-id="20586-603">**Balise**: filtrer les résultats par utilisateurs ou groupes pour lesquels la balise utilisateur spécifiée a été appliquée (y compris les comptes de priorité).</span><span class="sxs-lookup"><span data-stu-id="20586-603">**Tag**: Filter the results by users or groups that have had the specified user tag applied (including priority accounts).</span></span> <span data-ttu-id="20586-604">Pour plus d’informations sur les balises utilisateur, voir [Balises utilisateur.](user-tags.md)</span><span class="sxs-lookup"><span data-stu-id="20586-604">For more information about user tags, see [User tags](user-tags.md).</span></span>
- <span data-ttu-id="20586-605">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="20586-605">**Domain**</span></span>
- <span data-ttu-id="20586-606">**Type de stratégie**</span><span class="sxs-lookup"><span data-stu-id="20586-606">**Policy type**</span></span>
- <span data-ttu-id="20586-607">**Nom de la stratégie** (tableau de détails uniquement)</span><span class="sxs-lookup"><span data-stu-id="20586-607">**Policy name** (details table only)</span></span>
- <span data-ttu-id="20586-608">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="20586-608">**Recipients**</span></span>

<span data-ttu-id="20586-609">Lorsque vous avez terminé la configuration des filtres, cliquez sur **Appliquer,** **Annuler** ou **Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="20586-609">When you're finished configuring the filters, click **Apply**, **Cancel**, or **Clear filters**.</span></span>

### <a name="view-data-by-content--malware"></a><span data-ttu-id="20586-610">Afficher les données par programme malveillant de \> contenu</span><span class="sxs-lookup"><span data-stu-id="20586-610">View data by Content \> Malware</span></span>

![Affichage des programmes malveillants de contenu dans le rapport d’état de la protection contre les menaces](../../media/threat-protection-status-report-content-malware-view.png)

<span data-ttu-id="20586-612">Dans la **vue \> Afficher les données par programme** malveillant de contenu, les informations suivantes sont affichées dans le graphique de Microsoft Defender pour Office 365 organisations :</span><span class="sxs-lookup"><span data-stu-id="20586-612">In the **View data by Content \> Malware** view, the following information is shown in the chart for Microsoft Defender for Office 365 organizations:</span></span>

- <span data-ttu-id="20586-613">**Moteur anti-programme** malveillant : fichiers malveillants détectés dans Sharepoint, OneDrive et Microsoft Teams par la détection de virus intégrée dans [Microsoft 365](virus-detection-in-spo.md).</span><span class="sxs-lookup"><span data-stu-id="20586-613">**Anti-malware engine**: Malicious files detected in Sharepoint, OneDrive, and Microsoft Teams by the [built-in virus detection in Microsoft 365](virus-detection-in-spo.md).</span></span>
- <span data-ttu-id="20586-614">**Détonation de fichiers**: fichiers malveillants détectés par Safe pièces jointes pour [SharePoint, OneDrive et Microsoft Teams](mdo-for-spo-odb-and-teams.md).</span><span class="sxs-lookup"><span data-stu-id="20586-614">**File detonation**: Malicious files detected by [Safe Attachments for SharePoint, OneDrive, and Microsoft Teams](mdo-for-spo-odb-and-teams.md).</span></span>

<span data-ttu-id="20586-615">Dans le tableau de détails sous le graphique, les informations suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="20586-615">In the details table below the chart, the following information is available:</span></span>

- <span data-ttu-id="20586-616">**Date (UTC)** **Date de début et** date de **fin**</span><span class="sxs-lookup"><span data-stu-id="20586-616">**Date (UTC)** **Start date** and **End date**</span></span>
- <span data-ttu-id="20586-617">**Emplacement**</span><span class="sxs-lookup"><span data-stu-id="20586-617">**Location**</span></span>
- <span data-ttu-id="20586-618">**Détecté par**</span><span class="sxs-lookup"><span data-stu-id="20586-618">**Detected by**</span></span>
- <span data-ttu-id="20586-619">**Nom du programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="20586-619">**Malware name**</span></span>

<span data-ttu-id="20586-620">Si vous cliquez **sur Filtre,** les filtres suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="20586-620">If you click **Filter**, the following filters are available:</span></span>

- <span data-ttu-id="20586-621">**Date (UTC)** **Date de début et** date de **fin**</span><span class="sxs-lookup"><span data-stu-id="20586-621">**Date (UTC)** **Start date** and **End date**</span></span>
- <span data-ttu-id="20586-622">**Détection**: **moteur anti-programme malveillant** ou **détonation de fichiers**</span><span class="sxs-lookup"><span data-stu-id="20586-622">**Detection**: **Anti-malware engine** or **File detonation**</span></span>

<span data-ttu-id="20586-623">Lorsque vous avez terminé la configuration des filtres, cliquez sur **Appliquer,** **Annuler** ou **Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="20586-623">When you're finished configuring the filters, click **Apply**, **Cancel**, or **Clear filters**.</span></span>

### <a name="view-data-by-system-override"></a><span data-ttu-id="20586-624">Afficher les données par remplacement du système</span><span class="sxs-lookup"><span data-stu-id="20586-624">View data by System override</span></span>

![Affichage des remplacements de messages dans le rapport d’état de la protection contre les menaces](../../media/threat-protection-status-report-message-override-view.png)

<span data-ttu-id="20586-626">Dans **l’affichage d’affichage** des données par remplacement du système, les informations de motif de remplacement suivantes sont affichées dans le graphique :</span><span class="sxs-lookup"><span data-stu-id="20586-626">In the **View data by System override** view, the following override reason information is shown in the chart:</span></span>

- <span data-ttu-id="20586-627">**Ignorer l’local**</span><span class="sxs-lookup"><span data-stu-id="20586-627">**On-premises skip**</span></span>
- <span data-ttu-id="20586-628">**Ip allow**</span><span class="sxs-lookup"><span data-stu-id="20586-628">**IP allow**</span></span>
- <span data-ttu-id="20586-629">**Exchange de transport de messagerie** (règle de flux de messagerie)</span><span class="sxs-lookup"><span data-stu-id="20586-629">**Exchange mail transport rule** (mail flow rule)</span></span>
- <span data-ttu-id="20586-630">**Expéditeurs autorisés par l’organisation**</span><span class="sxs-lookup"><span data-stu-id="20586-630">**Organization allowed senders**</span></span>
- <span data-ttu-id="20586-631">**Domaines autorisés par l’organisation**</span><span class="sxs-lookup"><span data-stu-id="20586-631">**Organization allowed domains**</span></span>
- <span data-ttu-id="20586-632">**ZAP non activé**</span><span class="sxs-lookup"><span data-stu-id="20586-632">**ZAP not enabled**</span></span>
- <span data-ttu-id="20586-633">**Dossier Courrier indésirable non activé**</span><span class="sxs-lookup"><span data-stu-id="20586-633">**Junk Mail folder not enabled**</span></span>
- <span data-ttu-id="20586-634">**Expéditeur Safe utilisateur**</span><span class="sxs-lookup"><span data-stu-id="20586-634">**User Safe Sender**</span></span>
- <span data-ttu-id="20586-635">**Domaine Safe utilisateur**</span><span class="sxs-lookup"><span data-stu-id="20586-635">**User Safe Domain**</span></span>

<span data-ttu-id="20586-636">Dans le tableau de détails sous le graphique, les informations suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="20586-636">In the details table below the chart, the following information is available:</span></span>

- <span data-ttu-id="20586-637">**Date**</span><span class="sxs-lookup"><span data-stu-id="20586-637">**Date**</span></span>
- <span data-ttu-id="20586-638">**Subject**</span><span class="sxs-lookup"><span data-stu-id="20586-638">**Subject**</span></span>
- <span data-ttu-id="20586-639">**Expéditeur**</span><span class="sxs-lookup"><span data-stu-id="20586-639">**Sender**</span></span>
- <span data-ttu-id="20586-640">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="20586-640">**Recipients**</span></span>
- <span data-ttu-id="20586-641">**Détecté par**</span><span class="sxs-lookup"><span data-stu-id="20586-641">**Detected by**</span></span>
- <span data-ttu-id="20586-642">**État de remise**</span><span class="sxs-lookup"><span data-stu-id="20586-642">**Delivery Status**</span></span>
- <span data-ttu-id="20586-643">**Source de compromis**</span><span class="sxs-lookup"><span data-stu-id="20586-643">**Source of Compromise**</span></span>
- <span data-ttu-id="20586-644">**Tags**</span><span class="sxs-lookup"><span data-stu-id="20586-644">**Tags**</span></span>

<span data-ttu-id="20586-645">Si vous cliquez **sur Filtre,** les filtres suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="20586-645">If you click **Filter**, the following filters are available:</span></span>

- <span data-ttu-id="20586-646">**Date (UTC)** **Date de début et** date de **fin**</span><span class="sxs-lookup"><span data-stu-id="20586-646">**Date (UTC)** **Start date** and **End date**</span></span>
- <span data-ttu-id="20586-647">**Détection**</span><span class="sxs-lookup"><span data-stu-id="20586-647">**Detection**</span></span>
- <span data-ttu-id="20586-648">**Protégé par**: **MDO** (Defender for Office 365) ou **EOP**</span><span class="sxs-lookup"><span data-stu-id="20586-648">**Protected by**: **MDO** (Defender for Office 365) or **EOP**</span></span>
- <span data-ttu-id="20586-649">**Direction**</span><span class="sxs-lookup"><span data-stu-id="20586-649">**Direction**</span></span>
- <span data-ttu-id="20586-650">**Balise**: filtrer les résultats par utilisateurs ou groupes pour lesquels la balise utilisateur spécifiée a été appliquée (y compris les comptes de priorité).</span><span class="sxs-lookup"><span data-stu-id="20586-650">**Tag**: Filter the results by users or groups that have had the specified user tag applied (including priority accounts).</span></span> <span data-ttu-id="20586-651">Pour plus d’informations sur les balises utilisateur, voir [Balises utilisateur.](user-tags.md)</span><span class="sxs-lookup"><span data-stu-id="20586-651">For more information about user tags, see [User tags](user-tags.md).</span></span>
- <span data-ttu-id="20586-652">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="20586-652">**Domain**</span></span>
- <span data-ttu-id="20586-653">**Type de stratégie**</span><span class="sxs-lookup"><span data-stu-id="20586-653">**Policy type**</span></span>
- <span data-ttu-id="20586-654">**Nom de la stratégie** (tableau de détails uniquement)</span><span class="sxs-lookup"><span data-stu-id="20586-654">**Policy name** (details table only)</span></span>
- <span data-ttu-id="20586-655">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="20586-655">**Recipients**</span></span>

<span data-ttu-id="20586-656">Lorsque vous avez terminé la configuration des filtres, cliquez sur **Appliquer,** **Annuler** ou **Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="20586-656">When you're finished configuring the filters, click **Apply**, **Cancel**, or **Clear filters**.</span></span>

<span data-ttu-id="20586-657"><sup>\*</sup>Defender pour Office 365 uniquement</span><span class="sxs-lookup"><span data-stu-id="20586-657"><sup>\*</sup> Defender for Office 365 only</span></span>

## <a name="top-malware-report"></a><span data-ttu-id="20586-658">Principaux rapports sur les programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="20586-658">Top malware report</span></span>

<span data-ttu-id="20586-659">Le **rapport des principaux programmes** malveillants présente les différents types de programmes malveillants détectés par la protection [anti-programme malveillant dans EOP.](anti-malware-protection.md)</span><span class="sxs-lookup"><span data-stu-id="20586-659">The **Top malware** report shows the various kinds of malware that was detected by [anti-malware protection in EOP](anti-malware-protection.md).</span></span>

<span data-ttu-id="20586-660">Pour afficher le rapport dans le portail  Microsoft 365 Defender, consultez la & collaboration de rapports e-mail \>  \> **& rapports de collaboration.**</span><span class="sxs-lookup"><span data-stu-id="20586-660">To view the report in the Microsoft 365 Defender portal, go to **Reports** \> **Email & collaboration** \> **Email & collaboration reports**.</span></span> <span data-ttu-id="20586-661">Dans la page **Rapports de collaboration & courrier** électronique, recherchez **les** principaux programmes malveillants, puis cliquez sur Afficher **les détails.**</span><span class="sxs-lookup"><span data-stu-id="20586-661">On the **Email & collaboration reports** page, find **Top malware** and then click **View details**.</span></span> <span data-ttu-id="20586-662">Pour aller directement dans le rapport, ouvrez <https://security.microsoft.com/reports/TopMalware> .</span><span class="sxs-lookup"><span data-stu-id="20586-662">To go directly to the report, open <https://security.microsoft.com/reports/TopMalware>.</span></span>

![Widget de programmes malveillants de premier niveau sur la page rapports de collaboration & messagerie](../../media/top-malware-report-widget.png)

<span data-ttu-id="20586-664">Lorsque vous pointez sur une souris dans le graphique en secteurs, vous pouvez voir le nom d’un type de programme malveillant et le nombre de messages détectés comme ayant ce programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="20586-664">When you hover over a wedge in the pie chart, you can see the name of a kind of malware and how many messages were detected as having that malware.</span></span>

<span data-ttu-id="20586-665">Dans la page **Rapport de programmes malveillants supérieure,** une version plus grande du graphique en secteurs s’affiche sur la page de rapport. Le tableau de détails sous le graphique présente les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="20586-665">On the **Top malware report** page, a larger version of the pie chart is displayed on the report page.The details table below the chart shows the following information:</span></span>

- <span data-ttu-id="20586-666">**Principaux programmes malveillants**</span><span class="sxs-lookup"><span data-stu-id="20586-666">**Top malware**</span></span>
- <span data-ttu-id="20586-667">**Count**</span><span class="sxs-lookup"><span data-stu-id="20586-667">**Count**</span></span>

<span data-ttu-id="20586-668">Si vous cliquez **sur Filtre,** vous pouvez spécifier une plage de dates avec la **date de** début et la date **de fin.**</span><span class="sxs-lookup"><span data-stu-id="20586-668">If you click **Filter**, you can specify a date range with **Start date** and **End date**.</span></span>

![Affichage du rapport sur les programmes malveillants le plus haut](../../media/top-malware-report-view.png)

## <a name="url-threat-protection-report"></a><span data-ttu-id="20586-670">Rapport sur la protection contre les menaces d’URL</span><span class="sxs-lookup"><span data-stu-id="20586-670">URL threat protection report</span></span>

<span data-ttu-id="20586-671">Le **rapport sur la protection contre les menaces d’URL** est disponible dans Microsoft Defender Office 365.</span><span class="sxs-lookup"><span data-stu-id="20586-671">The **URL threat protection report** is available in Microsoft Defender for Office 365.</span></span> <span data-ttu-id="20586-672">Pour plus d’informations, voir le rapport sur la [protection contre les menaces d’URL.](view-reports-for-mdo.md#url-threat-protection-report)</span><span class="sxs-lookup"><span data-stu-id="20586-672">For more information, see [URL threat protection report](view-reports-for-mdo.md#url-threat-protection-report).</span></span>

## <a name="user-reported-messages-report"></a><span data-ttu-id="20586-673">Rapport des messages signalés par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="20586-673">User reported messages report</span></span>

> [!IMPORTANT]
> <span data-ttu-id="20586-674">Pour que le rapport des **messages** signalés par l’utilisateur fonctionne correctement, l’enregistrement **d’audit** doit être Microsoft 365 votre environnement.</span><span class="sxs-lookup"><span data-stu-id="20586-674">In order for the **User reported messages** report to work correctly, **audit logging must be turned on** for your Microsoft 365 environment.</span></span> <span data-ttu-id="20586-675">Cette tâche est généralement effectuée par une personne dont le rôle Journaux d’audit est Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="20586-675">This is typically done by someone who has the Audit Logs role assigned in Exchange Online.</span></span> <span data-ttu-id="20586-676">Pour plus d’informations, [voir Turn Microsoft 365 audit log search on or off](../../compliance/turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="20586-676">For more information, see [Turn Microsoft 365 audit log search on or off](../../compliance/turn-audit-log-search-on-or-off.md).</span></span>

<span data-ttu-id="20586-677">Le rapport des **messages** signalés par l’utilisateur affiche des informations sur les messages électroniques que les utilisateurs ont signalés comme courrier indésirable, tentatives d’hameçonnage ou courrier de qualité à l’aide du module complémentaire Signaler un [message](enable-the-report-message-add-in.md) ou signaler le hameçonnage. [](enable-the-report-phish-add-in.md)</span><span class="sxs-lookup"><span data-stu-id="20586-677">The **User reported messages** report shows information about email messages that users have reported as junk, phishing attempts, or good mail by using the [Report Message add-in](enable-the-report-message-add-in.md) or the [Report Phishing add-in](enable-the-report-phish-add-in.md).</span></span>

<span data-ttu-id="20586-678">Pour afficher le rapport dans le portail  Microsoft 365 Defender, consultez la & collaboration de rapports e-mail \>  \> **& rapports de collaboration.**</span><span class="sxs-lookup"><span data-stu-id="20586-678">To view the report in the Microsoft 365 Defender portal, go to **Reports** \> **Email & collaboration** \> **Email & collaboration reports**.</span></span> <span data-ttu-id="20586-679">Dans la page **& de collaboration,** recherchez les **messages** signalés par l’utilisateur, puis cliquez sur Afficher **les détails.**</span><span class="sxs-lookup"><span data-stu-id="20586-679">On the **Email & collaboration reports** page, find **User reported messages** and then click **View details**.</span></span> <span data-ttu-id="20586-680">Pour aller directement dans le rapport, ouvrez <https://security.microsoft.com/reports/userSubmissionReport> .</span><span class="sxs-lookup"><span data-stu-id="20586-680">To go directly to the report, open <https://security.microsoft.com/reports/userSubmissionReport>.</span></span> <span data-ttu-id="20586-681">Pour aller aux [soumissions d’administrateur dans le portail Microsoft 365 Defender,](admin-submission.md)cliquez **sur Go to Submissions**.</span><span class="sxs-lookup"><span data-stu-id="20586-681">To go to [admin submissions in the Microsoft 365 Defender portal](admin-submission.md), click **Go to Submissions**.</span></span>

![Widget de messages signalés par l’utilisateur sur la page rapports de collaboration & courrier électronique](../../media/user-reported-messages-widget.png)

<span data-ttu-id="20586-683">Dans **la** page Messages signalés par l’utilisateur, vous pouvez  filtrer à la fois le graphique et le tableau de détails en cliquant sur Filtrer et en sélectionnant une ou plusieurs des valeurs suivantes dans le volant qui s’affiche :</span><span class="sxs-lookup"><span data-stu-id="20586-683">On the **User reported messages** page, you can filter both the chart and the details table by clicking **Filter** and selecting one or more of the following values in the flyout that appears:</span></span>

- <span data-ttu-id="20586-684">**Date signalée :** **heure de début** et heure de **fin**</span><span class="sxs-lookup"><span data-stu-id="20586-684">**Date reported**: **Start time** and **End time**</span></span>
- <span data-ttu-id="20586-685">**Auteur du rapport**</span><span class="sxs-lookup"><span data-stu-id="20586-685">**Reported by**</span></span>
- <span data-ttu-id="20586-686">**Sujet de l’e-mail**</span><span class="sxs-lookup"><span data-stu-id="20586-686">**Email subject**</span></span>
- <span data-ttu-id="20586-687">**ID de message signalé**</span><span class="sxs-lookup"><span data-stu-id="20586-687">**Message reported ID**</span></span>
- <span data-ttu-id="20586-688">**ID de message réseau**</span><span class="sxs-lookup"><span data-stu-id="20586-688">**Network Message ID**</span></span>
- <span data-ttu-id="20586-689">**Sender**</span><span class="sxs-lookup"><span data-stu-id="20586-689">**Sender**</span></span>
- <span data-ttu-id="20586-690">**Raison signalée**</span><span class="sxs-lookup"><span data-stu-id="20586-690">**Reported reason**</span></span>
  - <span data-ttu-id="20586-691">**Non indésirable**</span><span class="sxs-lookup"><span data-stu-id="20586-691">**Not junk**</span></span>
  - <span data-ttu-id="20586-692">**Hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="20586-692">**Phish**</span></span>
  - <span data-ttu-id="20586-693">**Courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="20586-693">**Spam**</span></span>
- <span data-ttu-id="20586-694">**Simulation de hameçonnage**: **Oui** ou **Non**</span><span class="sxs-lookup"><span data-stu-id="20586-694">**Phish simulation**: **Yes** or **No**</span></span>

<span data-ttu-id="20586-695">Lorsque vous avez terminé la configuration des filtres, cliquez sur **Appliquer,** **Annuler** ou **Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="20586-695">When you're finished configuring the filters, click **Apply**, **Cancel**, or **Clear filters**.</span></span>

<span data-ttu-id="20586-696">Pour grouper les entrées, cliquez sur **Grouper** et sélectionnez l’une des valeurs suivantes dans la liste suivante :</span><span class="sxs-lookup"><span data-stu-id="20586-696">To group the entries, click **Group** and select one of the following values from the drop down list:</span></span>

- <span data-ttu-id="20586-697">**Aucune**</span><span class="sxs-lookup"><span data-stu-id="20586-697">**None**</span></span>
- <span data-ttu-id="20586-698">**Raison**</span><span class="sxs-lookup"><span data-stu-id="20586-698">**Reason**</span></span>
- <span data-ttu-id="20586-699">**Sender**</span><span class="sxs-lookup"><span data-stu-id="20586-699">**Sender**</span></span>
- <span data-ttu-id="20586-700">**Auteur du rapport**</span><span class="sxs-lookup"><span data-stu-id="20586-700">**Reported by**</span></span>
- <span data-ttu-id="20586-701">**Résultat rescan**</span><span class="sxs-lookup"><span data-stu-id="20586-701">**Rescan result**</span></span>
- <span data-ttu-id="20586-702">**Simulation de hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="20586-702">**Phish simulation**</span></span>

![Rapport des messages signalés par l’utilisateur](../../media/user-reported-messages-report.png)

<span data-ttu-id="20586-704">Dans le tableau de détails sous le graphique, vous pouvez voir les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="20586-704">In the details table below the graph, you can see the following details:</span></span>

- <span data-ttu-id="20586-705">**Sujet de l’e-mail**</span><span class="sxs-lookup"><span data-stu-id="20586-705">**Email subject**</span></span>
- <span data-ttu-id="20586-706">**Auteur du rapport**</span><span class="sxs-lookup"><span data-stu-id="20586-706">**Reported by**</span></span>
- <span data-ttu-id="20586-707">**Date de rapport**</span><span class="sxs-lookup"><span data-stu-id="20586-707">**Date reported**</span></span>
- <span data-ttu-id="20586-708">**Sender**</span><span class="sxs-lookup"><span data-stu-id="20586-708">**Sender**</span></span>
- <span data-ttu-id="20586-709">**Raison signalée**</span><span class="sxs-lookup"><span data-stu-id="20586-709">**Reported reason**</span></span>
- <span data-ttu-id="20586-710">**Résultat rescan**</span><span class="sxs-lookup"><span data-stu-id="20586-710">**Rescan result**</span></span>
- <span data-ttu-id="20586-711">**Tags**</span><span class="sxs-lookup"><span data-stu-id="20586-711">**Tags**</span></span>

<span data-ttu-id="20586-712">Pour envoyer un message à Microsoft pour analyse, sélectionnez l’entrée du message dans le tableau, cliquez sur Envoyer à **Microsoft** pour analyse, puis sélectionnez l’une des valeurs suivantes dans la liste liste suivante :</span><span class="sxs-lookup"><span data-stu-id="20586-712">To submit a message to Microsoft for analysis, select the message entry from the table, click **Submit to Microsoft for analysis** and then select one of the following values from the drop down list:</span></span>

- <span data-ttu-id="20586-713">**Signaler propre**</span><span class="sxs-lookup"><span data-stu-id="20586-713">**Report clean**</span></span>
- <span data-ttu-id="20586-714">**Signaler le hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="20586-714">**Report phishing**</span></span>
- <span data-ttu-id="20586-715">**Signaler un programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="20586-715">**Report malware**</span></span>
- <span data-ttu-id="20586-716">**Signaler le courrier indésirable**'</span><span class="sxs-lookup"><span data-stu-id="20586-716">**Report spam**'</span></span>
- <span data-ttu-id="20586-717">**Examen du déclencheur** (Defender for Office 365)</span><span class="sxs-lookup"><span data-stu-id="20586-717">**Trigger investigation** (Defender for Office 365)</span></span>

## <a name="what-permissions-are-needed-to-view-these-reports"></a><span data-ttu-id="20586-718">Quelles autorisations sont nécessaires pour afficher ces rapports ?</span><span class="sxs-lookup"><span data-stu-id="20586-718">What permissions are needed to view these reports?</span></span>

<span data-ttu-id="20586-719">Pour afficher et utiliser les rapports décrits dans cet article, vous devez être membre de l’un des groupes de rôles suivants dans le portail Microsoft 365 Defender:</span><span class="sxs-lookup"><span data-stu-id="20586-719">In order to view and use the reports described in this article, you need to be a member of one of the following role groups in the Microsoft 365 Defender portal:</span></span>

- <span data-ttu-id="20586-720">**Gestion de l'organisation**</span><span class="sxs-lookup"><span data-stu-id="20586-720">**Organization Management**</span></span>
- <span data-ttu-id="20586-721">**Administrateur de sécurité**</span><span class="sxs-lookup"><span data-stu-id="20586-721">**Security Administrator**</span></span>
- <span data-ttu-id="20586-722">**Lecteur sécurité**</span><span class="sxs-lookup"><span data-stu-id="20586-722">**Security Reader**</span></span>
- <span data-ttu-id="20586-723">**Lecteur global**</span><span class="sxs-lookup"><span data-stu-id="20586-723">**Global Reader**</span></span>

<span data-ttu-id="20586-724">Pour plus d’informations, [voir Autorisations dans le portail Microsoft 365 Defender.](permissions-in-the-security-and-compliance-center.md)</span><span class="sxs-lookup"><span data-stu-id="20586-724">For more information, see [Permissions in the Microsoft 365 Defender portal](permissions-in-the-security-and-compliance-center.md).</span></span>

<span data-ttu-id="20586-725">**Remarque**: l’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux  utilisateurs les autorisations requises dans le portail Microsoft 365 Defender et les autorisations pour d’autres fonctionnalités dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="20586-725">**Note**: Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions in the Microsoft 365 Defender portal _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="20586-726">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="20586-726">For more information, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>

## <a name="what-if-the-reports-arent-showing-data"></a><span data-ttu-id="20586-727">Que se passe-t-il si les rapports n’affichent pas de données ?</span><span class="sxs-lookup"><span data-stu-id="20586-727">What if the reports aren't showing data?</span></span>

<span data-ttu-id="20586-728">Si vous ne voyez pas de données dans vos rapports, vérifiez que vos stratégies sont correctement définies.</span><span class="sxs-lookup"><span data-stu-id="20586-728">If you are not seeing data in your reports, double-check that your policies are set up correctly.</span></span> <span data-ttu-id="20586-729">Pour en savoir plus, [consultez La protection contre les menaces.](protect-against-threats.md)</span><span class="sxs-lookup"><span data-stu-id="20586-729">To learn more, see [Protect against threats](protect-against-threats.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="20586-730">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20586-730">Related topics</span></span>

[<span data-ttu-id="20586-731">Protection contre le courrier indésirable et les programmes malveillants dans EOP</span><span class="sxs-lookup"><span data-stu-id="20586-731">Anti-spam and anti-malware protection in EOP</span></span>](anti-spam-and-anti-malware-protection.md)

[<span data-ttu-id="20586-732">Rapports intelligents et informations sur le portail Microsoft 365 Defender web</span><span class="sxs-lookup"><span data-stu-id="20586-732">Smart reports and insights in the Microsoft 365 Defender portal</span></span>](reports-and-insights-in-security-and-compliance.md)

[<span data-ttu-id="20586-733">Afficher les rapports de flux de messagerie dans le portail Microsoft 365 Defender messagerie</span><span class="sxs-lookup"><span data-stu-id="20586-733">View mail flow reports in the Microsoft 365 Defender portal</span></span>](view-mail-flow-reports.md)

[<span data-ttu-id="20586-734">Afficher des rapports pour Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="20586-734">View reports for Defender for Office 365</span></span>](view-reports-for-mdo.md)
