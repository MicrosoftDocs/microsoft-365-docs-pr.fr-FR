---
title: Informations sur les courriers électroniques de nouveaux utilisateurs
f1.keywords:
- NOCSH
ms.author: siosulli
author: siosulli
manager: dansimp
audience: ITPro
ms.topic: conceptual
localization_priority: Normal
ms.assetid: ''
description: Les administrateurs peuvent apprendre à utiliser les informations sur les nouveaux utilisateurs qui envoient des courriers électroniques dans le Centre de sécurité & conformité pour examiner quand les utilisateurs de leur organisation envoient des messages à de nouveaux domaines.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: af991cb0af20a0f48bc5283d4e4fb26ea75d6ba6
ms.sourcegitcommit: 537e513a4a232a01e44ecbc76d86a8bcaf142482
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/27/2021
ms.locfileid: "50029869"
---
# <a name="new-users-forwarding-email-insight-in-the-security--compliance-center"></a><span data-ttu-id="7366a-103">Nouveaux utilisateurs qui envoient des informations sur le courrier électronique dans le Centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="7366a-103">New users forwarding email insight in the Security & Compliance Center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="7366a-104">Il est suspect lorsque de nouveaux comptes d’utilisateurs de votre organisation commencent soudainement à envoyer des messages électroniques à des domaines externes.</span><span class="sxs-lookup"><span data-stu-id="7366a-104">It's suspicious when new user accounts in your organization suddenly start forwarding email messages to external domains.</span></span>

<span data-ttu-id="7366a-105">**L’aperçu** des nouveaux domaines transmis par courrier électronique dans le Centre de sécurité [&](https://protection.office.com) conformité vous informe lorsque des utilisateurs nouvellement créés dans votre organisation sont en train de forwarder des messages vers des domaines externes.</span><span class="sxs-lookup"><span data-stu-id="7366a-105">The **New domains being forwarded email** insight in the [Security & Compliance Center](https://protection.office.com) notifies you when newly-created users in your organization are forwarding messages to external domains.</span></span> <span data-ttu-id="7366a-106">Cette condition peut indiquer que des comptes d’administrateur compromis ont été utilisés pour créer les nouveaux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7366a-106">This condition could indicate compromised admin accounts were used to create the new users.</span></span> <span data-ttu-id="7366a-107">Si vous pensez que les comptes ont été compromis, voir Répondre [à un compte de messagerie compromis.](responding-to-a-compromised-email-account.md)</span><span class="sxs-lookup"><span data-stu-id="7366a-107">If you suspect the accounts have been compromised, see [Responding to a compromised email account](responding-to-a-compromised-email-account.md).</span></span>

<span data-ttu-id="7366a-108">Cette information apparaît uniquement lorsque le problème est détecté et apparaît sur la page du rapport [de forwarding.](view-mail-flow-reports.md#forwarding-report)</span><span class="sxs-lookup"><span data-stu-id="7366a-108">This insight appears only when the issue is detected, and it appears on the [Forwarding report](view-mail-flow-reports.md#forwarding-report) page.</span></span>

![Informations sur les courriers électroniques de nouveaux utilisateurs](../../media/mfi-new-users-forwarding-email.png)

<span data-ttu-id="7366a-110">Lorsque vous cliquez sur le widget, un volant s’affiche, dans lequel vous trouverez plus de détails sur les messages transmis, y compris un lien vers le rapport de [modifications](#forwarding-modifications-report) de report, comme décrit plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="7366a-110">When you click on the widget, a flyout appears where you can find more details about the forwarded messages, including a link to the [Forwarding modifications report](#forwarding-modifications-report) as described later in this article.</span></span>

![Volant d’informations qui s’affiche après avoir cliqué sur l’aperçu du courrier électronique nouveaux utilisateurs](../../media/mfi-new-users-forwarding-email-details.png)

<span data-ttu-id="7366a-112">Vous pouvez également vous rendre sur cette page de  détails lorsque vous sélectionnez l’aperçu après avoir cliqué sur Afficher tout dans la zone Recommandations & informations les plus **détaillées** **(** Tableau de bord de rapports \>  ou <https://protection.office.com/insightdashboard> ).</span><span class="sxs-lookup"><span data-stu-id="7366a-112">You can also get to this details page when you select the insight after you click **View all** in the **Top insights & recommendations** area on (**Reports** \> **Dashboard** or <https://protection.office.com/insightdashboard>).</span></span>

<span data-ttu-id="7366a-113">Vous pouvez cliquer sur le **rapport Voir associé au** lien d’informations pour vous rendre dans le rapport de modifications de **forwarding,** comme décrit dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="7366a-113">You can click the **See report associated with insight** link to go to the **Forwarding modifications report** as described in the next section.</span></span>

## <a name="forwarding-modifications-report"></a><span data-ttu-id="7366a-114">Rapport de modifications de forwarding</span><span class="sxs-lookup"><span data-stu-id="7366a-114">Forwarding modifications report</span></span>

<span data-ttu-id="7366a-115">Le **rapport de modifications de forwarding** affiche des détails sur les messages qui sont automatiquement transmis par des expéditeurs de votre organisation :</span><span class="sxs-lookup"><span data-stu-id="7366a-115">The **Forwarding modifications report** shows details about messages that are being automatically forwarded from senders in your organization:</span></span>

- <span data-ttu-id="7366a-116">Comptes nouvellement créés qui sont en cours de forwarding des messages vers des domaines externes.</span><span class="sxs-lookup"><span data-stu-id="7366a-116">Newly-created accounts that are forwarding messages to external domains.</span></span>
- <span data-ttu-id="7366a-117">Comptes qui envoient des messages à des domaines externes qui n’ont jamais été transmis par d’autres expéditeurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="7366a-117">Accounts that are forwarding messages to external domains that have never been forwarded to by other senders in your organization.</span></span>

<span data-ttu-id="7366a-118">Ces types de messages transmis peuvent poser un risque de sécurité ou de conformité, et peuvent indiquer des comptes compromis.</span><span class="sxs-lookup"><span data-stu-id="7366a-118">These types of forwarded messages can pose a security or compliance risk, and might indicate compromised accounts.</span></span>

<span data-ttu-id="7366a-119">Le rapport contient des données pendant 90 jours au plus.</span><span class="sxs-lookup"><span data-stu-id="7366a-119">The report contains data for up to 90 days.</span></span> <span data-ttu-id="7366a-120">Par défaut, le rapport affiche les données des 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="7366a-120">By default, the report shows data for the last 7 days.</span></span>

<span data-ttu-id="7366a-121">Ce rapport n’est pas directement disponible dans le tableau de bord de flux de [messagerie](mail-flow-insights-v2.md) ou dans le tableau de bord [Rapports.](view-mail-flow-reports.md)</span><span class="sxs-lookup"><span data-stu-id="7366a-121">This report isn't directly available in the [Mail flow dashboard](mail-flow-insights-v2.md) or in the [Reports dashboard](view-mail-flow-reports.md).</span></span> <span data-ttu-id="7366a-122">En plus de cliquer sur le rapport  **Voir** associé au lien Informations dans l’aperçu des nouveaux utilisateurs qui envoient des e-mails, vous pouvez obtenir le rapport en :</span><span class="sxs-lookup"><span data-stu-id="7366a-122">In addition to clicking the **See report associated with insight** link in the **New users forwarding email** insight, you get to the report by:</span></span>

- <span data-ttu-id="7366a-123">Cliquez sur le **lien du rapport de notifications** de forwarding dans les détails de l’aperçu des nouveaux domaines transmis par courrier [électronique.](mfi-new-domains-being-forwarded-email.md)</span><span class="sxs-lookup"><span data-stu-id="7366a-123">Clicking the **Forwarding notifications report** link in the details of the [New domains being forwarded email insight](mfi-new-domains-being-forwarded-email.md).</span></span>
- <span data-ttu-id="7366a-124">Ouverture <https://protection.office.com/reportv2?id=MailFlowNewForwarding> .</span><span class="sxs-lookup"><span data-stu-id="7366a-124">Opening <https://protection.office.com/reportv2?id=MailFlowNewForwarding>.</span></span>

### <a name="report-view-for-the-forwarding-modifications-report"></a><span data-ttu-id="7366a-125">Affichage du rapport pour le rapport de modifications de report</span><span class="sxs-lookup"><span data-stu-id="7366a-125">Report view for the Forwarding modifications report</span></span>

<span data-ttu-id="7366a-126">Les graphiques suivants sont disponibles dans l’affichage de rapport :</span><span class="sxs-lookup"><span data-stu-id="7366a-126">The following charts are available in the report view:</span></span>

- <span data-ttu-id="7366a-127">**Afficher les données pour : Nouveaux utilisateurs de forwarding**:</span><span class="sxs-lookup"><span data-stu-id="7366a-127">**Show data for: New forwarding users**:</span></span>

  ![Affichage des nouveaux utilisateurs de forwarding dans le rapport de modifications de forwarding](../../media/forwarding-modifications-report-new-forwarding-users.png)

- <span data-ttu-id="7366a-129">**Afficher les données pour : Nouveaux domaines de forwarding**:</span><span class="sxs-lookup"><span data-stu-id="7366a-129">**Show data for: New forwarding domains**:</span></span>

  ![Nouvel affichage des domaines transmis dans le rapport de modifications de forwarding](../../media/forwarding-modifications-report-new-forwarded-domains.png)

<span data-ttu-id="7366a-131">Si vous cliquez sur **Filtres** dans un affichage de rapport, vous pouvez spécifier une plage de dates avec la **date** de début et la **date de fin.**</span><span class="sxs-lookup"><span data-stu-id="7366a-131">If you click **Filters** in a report view, you can specify a date range with **Start date** and **End date**.</span></span>

### <a name="details-table-view-for-the-forwarding-modifications-report"></a><span data-ttu-id="7366a-132">Affichage du tableau détails pour le rapport de modifications de report</span><span class="sxs-lookup"><span data-stu-id="7366a-132">Details table view for the Forwarding modifications report</span></span>

<span data-ttu-id="7366a-133">Si vous cliquez sur Afficher le tableau des **détails,** les informations affichées dépendent du graphique que vous regardiez :</span><span class="sxs-lookup"><span data-stu-id="7366a-133">If you click **View details table**, the information that's shown depends on the chart you were looking at:</span></span>

- <span data-ttu-id="7366a-134">**Afficher les données pour : Nouveaux utilisateurs de forwarding**:</span><span class="sxs-lookup"><span data-stu-id="7366a-134">**Show data for: New forwarding users**:</span></span>

  - <span data-ttu-id="7366a-135">**Nom**: adresse e-mail de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="7366a-135">**Name**: The email address of the sender.</span></span>
  - <span data-ttu-id="7366a-136">**Type de forwarding**</span><span class="sxs-lookup"><span data-stu-id="7366a-136">**Forwarding type**</span></span>
  - <span data-ttu-id="7366a-137">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="7366a-137">**Recipient address**</span></span>
  - <span data-ttu-id="7366a-138">**Details**</span><span class="sxs-lookup"><span data-stu-id="7366a-138">**Details**</span></span>
  - <span data-ttu-id="7366a-139">**Count**</span><span class="sxs-lookup"><span data-stu-id="7366a-139">**Count**</span></span>
  - <span data-ttu-id="7366a-140">**Première date d’avance**</span><span class="sxs-lookup"><span data-stu-id="7366a-140">**First forward date**</span></span>

- <span data-ttu-id="7366a-141">**Afficher les données pour : Nouveaux domaines de forwarding**:</span><span class="sxs-lookup"><span data-stu-id="7366a-141">**Show data for: New forwarding domains**:</span></span>

  - <span data-ttu-id="7366a-142">**Nom**: domaine de messagerie de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="7366a-142">**Name**: The email domain of the sender.</span></span>
  - <span data-ttu-id="7366a-143">**Type de forwarding**</span><span class="sxs-lookup"><span data-stu-id="7366a-143">**Forwarding type**</span></span>
  - <span data-ttu-id="7366a-144">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="7366a-144">**Recipient address**</span></span>
  - <span data-ttu-id="7366a-145">**Details**</span><span class="sxs-lookup"><span data-stu-id="7366a-145">**Details**</span></span>
  - <span data-ttu-id="7366a-146">**Count**</span><span class="sxs-lookup"><span data-stu-id="7366a-146">**Count**</span></span>
  - <span data-ttu-id="7366a-147">**Première date d’avance**</span><span class="sxs-lookup"><span data-stu-id="7366a-147">**First forward date**</span></span>

<span data-ttu-id="7366a-148">Si vous cliquez sur **Filtres** dans une vue de tableau de détails, vous pouvez spécifier une plage de dates avec la **date** de début et la **date de fin.**</span><span class="sxs-lookup"><span data-stu-id="7366a-148">If you click **Filters** in a details table view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="7366a-149">Si vous sélectionnez une ligne dans le tableau, un volant **Détails** s’affiche avec les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="7366a-149">If you select a row from the table, a **Details** flyout appears with the following information:</span></span>

- <span data-ttu-id="7366a-150">**Nom**: il s’agit de l’adresse e-mail de l’expéditeur (à partir de l’affichage Afficher les données pour : Nouvel affichage **utilisateurs** de **forwarding)** ou du domaine de messagerie de l’expéditeur (à partir de l’affichage Afficher les données pour : Nouvel affichage des nouveaux domaines de forwarding).</span><span class="sxs-lookup"><span data-stu-id="7366a-150">**Name**: This is either the sender's email address (from **Show data for: New forwarding users** view) or the sender's email domain (from **Show data for: New forwarding domains** view).</span></span>
- <span data-ttu-id="7366a-151">**Type de forwarding**</span><span class="sxs-lookup"><span data-stu-id="7366a-151">**Forwarding type**</span></span>
- <span data-ttu-id="7366a-152">**Destinataire**</span><span class="sxs-lookup"><span data-stu-id="7366a-152">**Recipient**</span></span>
- <span data-ttu-id="7366a-153">**Details**</span><span class="sxs-lookup"><span data-stu-id="7366a-153">**Details**</span></span>
- <span data-ttu-id="7366a-154">**Count**</span><span class="sxs-lookup"><span data-stu-id="7366a-154">**Count**</span></span>
- <span data-ttu-id="7366a-155">**Date de début**</span><span class="sxs-lookup"><span data-stu-id="7366a-155">**Start date**</span></span>
- <span data-ttu-id="7366a-156">**Recommandation**: à partir de là, vous pouvez cliquer sur le lien pour gérer l’utilisateur dans le Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="7366a-156">**Recommendation**: From here, you can click the link to manage the user in the Microsoft 365 admin center.</span></span>

![Détails du tableau des détails de l’affichage Nouveaux utilisateurs de forwarding dans le rapport de modifications de forwarding](../../media/mfi-forwarding-modifications-report-new-forwarding-users-view-details-table-details.png)

<span data-ttu-id="7366a-158">Pour revenir à l’affichage Rapports, cliquez **sur Afficher le rapport.**</span><span class="sxs-lookup"><span data-stu-id="7366a-158">To go back to the reports view, click **View report**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7366a-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7366a-159">Related topics</span></span>

<span data-ttu-id="7366a-160">Pour plus d’informations sur d’autres informations dans le tableau de bord de flux de messagerie, voir Informations sur le flux de messagerie dans le Centre de sécurité [& conformité.](mail-flow-insights-v2.md)</span><span class="sxs-lookup"><span data-stu-id="7366a-160">For information about other insights in the Mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
