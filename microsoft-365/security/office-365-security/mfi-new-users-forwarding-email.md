---
title: Informations sur les courriers électroniques de nouveaux utilisateurs
f1.keywords:
- NOCSH
ms.author: siosulli
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: conceptual
ms.service: exchange-online
localization_priority: Normal
ms.assetid: ''
description: Les administrateurs peuvent apprendre à utiliser les nouveaux utilisateurs pour transférer des courriers électroniques dans le centre de sécurité & conformité afin de déterminer quand les utilisateurs de leur organisation acheminent les messages vers de nouveaux domaines.
ms.openlocfilehash: cf1852169279e19ac00e5e29dd1c26e155936039
ms.sourcegitcommit: 0a8b0186cc041db7341e57f375d0d010b7682b7d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2020
ms.locfileid: "49660016"
---
# <a name="new-users-forwarding-email-insight-in-the-security--compliance-center"></a><span data-ttu-id="f45f2-103">Les nouveaux utilisateurs transférant des courriers électroniques dans le centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="f45f2-103">New users forwarding email insight in the Security & Compliance Center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="f45f2-104">Il est suspect lorsque les nouveaux comptes d’utilisateur dans votre organisation commencent soudainement à transférer les messages électroniques vers des domaines externes.</span><span class="sxs-lookup"><span data-stu-id="f45f2-104">It's suspicious when new user accounts in your organization suddenly start forwarding email messages to external domains.</span></span>

<span data-ttu-id="f45f2-105">Les **nouveaux domaines en cours de transmission de courrier électronique** dans le [centre de sécurité & de conformité](https://protection.office.com) vous avertit lorsque des utilisateurs nouvellement créés dans votre organisation acheminent des messages vers des domaines externes.</span><span class="sxs-lookup"><span data-stu-id="f45f2-105">The **New domains being forwarded email** insight in the [Security & Compliance Center](https://protection.office.com) notifies you when newly-created users in your organization are forwarding messages to external domains.</span></span> <span data-ttu-id="f45f2-106">Cette condition peut indiquer que des comptes d’administrateur compromis ont été utilisés pour créer les nouveaux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f45f2-106">This condition could indicate compromised admin accounts were used to create the new users.</span></span> <span data-ttu-id="f45f2-107">Si vous pensez que les comptes ont été compromis, consultez la rubrique relative [à la réponse à un compte de courrier compromis](responding-to-a-compromised-email-account.md).</span><span class="sxs-lookup"><span data-stu-id="f45f2-107">If you suspect the accounts have been compromised, see [Responding to a compromised email account](responding-to-a-compromised-email-account.md).</span></span>

<span data-ttu-id="f45f2-108">Cette vue s’affiche uniquement lorsque le problème est détecté et qu’il apparaît sur la page [rapport de transfert](view-mail-flow-reports.md#forwarding-report) .</span><span class="sxs-lookup"><span data-stu-id="f45f2-108">This insight appears only when the issue is detected, and it appears on the [Forwarding report](view-mail-flow-reports.md#forwarding-report) page.</span></span>

![Informations sur les courriers électroniques de nouveaux utilisateurs](../../media/mfi-new-users-forwarding-email.png)

<span data-ttu-id="f45f2-110">Lorsque vous cliquez sur le widget, un menu volant s’affiche pour vous permettre de trouver plus d’informations sur les messages transférés, y compris un lien vers le [rapport de modifications du transfert](#forwarding-modifications-report) , comme décrit plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="f45f2-110">When you click on the widget, a flyout appears where you can find more details about the forwarded messages, including a link to the [Forwarding modifications report](#forwarding-modifications-report) as described later in this article.</span></span>

![Fenêtre volante de détails qui apparaît après avoir cliqué sur le nouvel utilisateur.](../../media/mfi-new-users-forwarding-email-details.png)

<span data-ttu-id="f45f2-112">Vous pouvez également accéder à cette page de détails lorsque vous sélectionnez l’option **Afficher tout** dans la zone de **recommandations & premières Insights** (tableau de \> **bord** rapports ou <https://protection.office.com/insightdashboard> ).</span><span class="sxs-lookup"><span data-stu-id="f45f2-112">You can also get to this details page when you select the insight after you click **View all** in the **Top insights & recommendations** area on (**Reports** \> **Dashboard** or <https://protection.office.com/insightdashboard>).</span></span>

<span data-ttu-id="f45f2-113">Vous pouvez cliquer sur le lien **Voir le rapport associé** à la vue pour accéder au **rapport des modifications de transfert** , comme décrit dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="f45f2-113">You can click the **See report associated with insight** link to go to the **Forwarding modifications report** as described in the next section.</span></span>

## <a name="forwarding-modifications-report"></a><span data-ttu-id="f45f2-114">Rapport de transfert des modifications</span><span class="sxs-lookup"><span data-stu-id="f45f2-114">Forwarding modifications report</span></span>

<span data-ttu-id="f45f2-115">Le **rapport de transfert des modifications** affiche des détails sur les messages qui sont automatiquement transférés des expéditeurs au sein de votre organisation :</span><span class="sxs-lookup"><span data-stu-id="f45f2-115">The **Forwarding modifications report** shows details about messages that are being automatically forwarded from senders in your organization:</span></span>

- <span data-ttu-id="f45f2-116">Les comptes nouvellement créés qui transfèrent des messages vers des domaines externes.</span><span class="sxs-lookup"><span data-stu-id="f45f2-116">Newly-created accounts that are forwarding messages to external domains.</span></span>
- <span data-ttu-id="f45f2-117">Comptes qui transfèrent des messages vers des domaines externes qui n’ont jamais été transférés par d’autres expéditeurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f45f2-117">Accounts that are forwarding messages to external domains that have never been forwarded to by other senders in your organization.</span></span>

<span data-ttu-id="f45f2-118">Ces types de messages transférés peuvent présenter un risque de sécurité ou de conformité, et peuvent indiquer des comptes compromis.</span><span class="sxs-lookup"><span data-stu-id="f45f2-118">These types of forwarded messages can pose a security or compliance risk, and might indicate compromised accounts.</span></span>

<span data-ttu-id="f45f2-119">Le rapport contient des données pour 90 jours maximum.</span><span class="sxs-lookup"><span data-stu-id="f45f2-119">The report contains data for up to 90 days.</span></span> <span data-ttu-id="f45f2-120">Par défaut, le rapport affiche les données des 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="f45f2-120">By default, the report shows data for the last 7 days.</span></span>

<span data-ttu-id="f45f2-121">Ce rapport n’est pas disponible directement dans le [tableau de bord de flux de messagerie](mail-flow-insights-v2.md) ou dans le tableau de [bord rapports](view-mail-flow-reports.md).</span><span class="sxs-lookup"><span data-stu-id="f45f2-121">This report isn't directly available in the [Mail flow dashboard](mail-flow-insights-v2.md) or in the [Reports dashboard](view-mail-flow-reports.md).</span></span> <span data-ttu-id="f45f2-122">En plus de cliquer sur le lien **afficher le rapport associé** à la vue d' **envoi des nouveaux utilisateurs** , vous accédez au rapport en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="f45f2-122">In addition to clicking the **See report associated with insight** link in the **New users forwarding email** insight, you get to the report by:</span></span>

- <span data-ttu-id="f45f2-123">En cliquant sur le lien **rapport de notifications de transfert** dans les détails des [nouveaux domaines en cours de transmission de messages électroniques](mfi-new-domains-being-forwarded-email.md).</span><span class="sxs-lookup"><span data-stu-id="f45f2-123">Clicking the **Forwarding notifications report** link in the details of the [New domains being forwarded email insight](mfi-new-domains-being-forwarded-email.md).</span></span>
- <span data-ttu-id="f45f2-124">Ouverture <https://protection.office.com/reportv2?id=MailFlowNewForwarding> .</span><span class="sxs-lookup"><span data-stu-id="f45f2-124">Opening <https://protection.office.com/reportv2?id=MailFlowNewForwarding>.</span></span>

### <a name="report-view-for-the-forwarding-modifications-report"></a><span data-ttu-id="f45f2-125">Affichage de rapport pour le rapport des modifications du transfert</span><span class="sxs-lookup"><span data-stu-id="f45f2-125">Report view for the Forwarding modifications report</span></span>

<span data-ttu-id="f45f2-126">Les graphiques suivants sont disponibles dans l’affichage rapport :</span><span class="sxs-lookup"><span data-stu-id="f45f2-126">The following charts are available in the report view:</span></span>

- <span data-ttu-id="f45f2-127">**Afficher les données pour : nouveaux utilisateurs de transfert**:</span><span class="sxs-lookup"><span data-stu-id="f45f2-127">**Show data for: New forwarding users**:</span></span>

  ![Nouvel affichage des utilisateurs de transfert dans le rapport des modifications de transfert](../../media/forwarding-modifications-report-new-forwarding-users.png)

- <span data-ttu-id="f45f2-129">**Afficher les données pour : nouveaux domaines de transfert**:</span><span class="sxs-lookup"><span data-stu-id="f45f2-129">**Show data for: New forwarding domains**:</span></span>

  ![Nouvelle vue Domains transférées dans le rapport des modifications de transfert](../../media/forwarding-modifications-report-new-forwarded-domains.png)

<span data-ttu-id="f45f2-131">Si vous cliquez sur **filtres** dans un affichage de rapport, vous pouvez spécifier une plage de dates avec **Date de début** et date de **fin**.</span><span class="sxs-lookup"><span data-stu-id="f45f2-131">If you click **Filters** in a report view, you can specify a date range with **Start date** and **End date**.</span></span>

### <a name="details-table-view-for-the-forwarding-modifications-report"></a><span data-ttu-id="f45f2-132">Vue de la table Détails pour le rapport des modifications de transfert</span><span class="sxs-lookup"><span data-stu-id="f45f2-132">Details table view for the Forwarding modifications report</span></span>

<span data-ttu-id="f45f2-133">Si vous cliquez sur **afficher les détails table**, les informations affichées dépendent du graphique que vous examinez :</span><span class="sxs-lookup"><span data-stu-id="f45f2-133">If you click **View details table**, the information that's shown depends on the chart you were looking at:</span></span>

- <span data-ttu-id="f45f2-134">**Afficher les données pour : nouveaux utilisateurs de transfert**:</span><span class="sxs-lookup"><span data-stu-id="f45f2-134">**Show data for: New forwarding users**:</span></span>

  - <span data-ttu-id="f45f2-135">**Name**: adresse de messagerie de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="f45f2-135">**Name**: The email address of the sender.</span></span>
  - <span data-ttu-id="f45f2-136">**Type de transfert**</span><span class="sxs-lookup"><span data-stu-id="f45f2-136">**Forwarding type**</span></span>
  - <span data-ttu-id="f45f2-137">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="f45f2-137">**Recipient address**</span></span>
  - <span data-ttu-id="f45f2-138">**Details**</span><span class="sxs-lookup"><span data-stu-id="f45f2-138">**Details**</span></span>
  - <span data-ttu-id="f45f2-139">**Count**</span><span class="sxs-lookup"><span data-stu-id="f45f2-139">**Count**</span></span>
  - <span data-ttu-id="f45f2-140">**Première date de transfert**</span><span class="sxs-lookup"><span data-stu-id="f45f2-140">**First forward date**</span></span>

- <span data-ttu-id="f45f2-141">**Afficher les données pour : nouveaux domaines de transfert**:</span><span class="sxs-lookup"><span data-stu-id="f45f2-141">**Show data for: New forwarding domains**:</span></span>

  - <span data-ttu-id="f45f2-142">**Name**: domaine de messagerie de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="f45f2-142">**Name**: The email domain of the sender.</span></span>
  - <span data-ttu-id="f45f2-143">**Type de transfert**</span><span class="sxs-lookup"><span data-stu-id="f45f2-143">**Forwarding type**</span></span>
  - <span data-ttu-id="f45f2-144">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="f45f2-144">**Recipient address**</span></span>
  - <span data-ttu-id="f45f2-145">**Details**</span><span class="sxs-lookup"><span data-stu-id="f45f2-145">**Details**</span></span>
  - <span data-ttu-id="f45f2-146">**Count**</span><span class="sxs-lookup"><span data-stu-id="f45f2-146">**Count**</span></span>
  - <span data-ttu-id="f45f2-147">**Première date de transfert**</span><span class="sxs-lookup"><span data-stu-id="f45f2-147">**First forward date**</span></span>

<span data-ttu-id="f45f2-148">Si vous cliquez sur **filtres** dans un affichage tableau détaillé, vous pouvez spécifier une plage de dates avec **Date de début** et date de **fin**.</span><span class="sxs-lookup"><span data-stu-id="f45f2-148">If you click **Filters** in a details table view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="f45f2-149">Si vous sélectionnez une ligne dans le tableau, une fenêtre volante de **Détails** s’affiche avec les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="f45f2-149">If you select a row from the table, a **Details** flyout appears with the following information:</span></span>

- <span data-ttu-id="f45f2-150">**Name**: il s’agit de l’adresse de messagerie de l’expéditeur (de l’affichage des **données pour : nouvelle** vue des utilisateurs de transfert) ou du domaine de messagerie de l’expéditeur (de l’affichage des **données pour : nouvelle** vue des domaines de transfert).</span><span class="sxs-lookup"><span data-stu-id="f45f2-150">**Name**: This is either the sender's email address (from **Show data for: New forwarding users** view) or the sender's email domain (from **Show data for: New forwarding domains** view).</span></span>
- <span data-ttu-id="f45f2-151">**Type de transfert**</span><span class="sxs-lookup"><span data-stu-id="f45f2-151">**Forwarding type**</span></span>
- <span data-ttu-id="f45f2-152">**Destinataire**</span><span class="sxs-lookup"><span data-stu-id="f45f2-152">**Recipient**</span></span>
- <span data-ttu-id="f45f2-153">**Details**</span><span class="sxs-lookup"><span data-stu-id="f45f2-153">**Details**</span></span>
- <span data-ttu-id="f45f2-154">**Count**</span><span class="sxs-lookup"><span data-stu-id="f45f2-154">**Count**</span></span>
- <span data-ttu-id="f45f2-155">**Date de début**</span><span class="sxs-lookup"><span data-stu-id="f45f2-155">**Start date**</span></span>
- <span data-ttu-id="f45f2-156">**Recommandation**: à partir de là, vous pouvez cliquer sur le lien pour gérer l’utilisateur dans le centre d’administration 365 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f45f2-156">**Recommendation**: From here, you can click the link to manage the user in the Microsoft 365 admin center.</span></span>

![Fenêtre mobile détails à partir de la table Détails de la vue nouveaux utilisateurs de transfert dans le rapport des modifications de transfert](../../media/mfi-forwarding-modifications-report-new-forwarding-users-view-details-table-details.png)

<span data-ttu-id="f45f2-158">Pour revenir à l’affichage rapports, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="f45f2-158">To go back to the reports view, click **View report**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f45f2-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f45f2-159">Related topics</span></span>

<span data-ttu-id="f45f2-160">Pour plus d’informations sur les autres informations du tableau de bord de flux de messagerie, consultez [la rubrique mail Flow Insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span><span class="sxs-lookup"><span data-stu-id="f45f2-160">For information about other insights in the Mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
