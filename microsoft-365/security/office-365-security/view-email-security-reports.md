---
title: Afficher les rapports de sécurité de messagerie dans le portail Microsoft 365 Defender
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
description: Découvrez comment rechercher et utiliser des rapports de sécurité du courrier électronique pour votre organisation. Les rapports de sécurité de messagerie sont disponibles dans le portail Microsoft 365 Defender.
ms.custom: seo-marvel-apr2020
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: bb7570722fcc957ca86d68f6b42ef254578d7bd7
ms.sourcegitcommit: 3d30ec03628870a22c54b6ec5d865cbe94f34245
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "52930320"
---
# <a name="view-email-security-reports-in-the-microsoft-365-defender-portal"></a><span data-ttu-id="8e13b-104">Afficher les rapports de sécurité de messagerie dans le portail Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8e13b-104">View email security reports in the Microsoft 365 Defender portal</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="8e13b-105">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="8e13b-105">**Applies to**</span></span>
- [<span data-ttu-id="8e13b-106">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="8e13b-106">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="8e13b-107">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="8e13b-107">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="8e13b-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8e13b-108">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="8e13b-109">De nombreux rapports sont disponibles dans le portail [Microsoft 365 Defender](https://security.microsoft.com) pour vous aider à voir comment les fonctionnalités de sécurité du courrier électronique, telles que les fonctionnalités anti-courrier indésirable, anti-programme malveillant et chiffrement dans Microsoft 365 protègent votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8e13b-109">A variety of reports are available in the [Microsoft 365 Defender portal](https://security.microsoft.com) to help you see how email security features, such as anti-spam, anti-malware, and encryption features in Microsoft 365 are protecting your organization.</span></span> <span data-ttu-id="8e13b-110">Si vous avez les [autorisations](#what-permissions-are-needed-to-view-these-reports)nécessaires, vous pouvez afficher ces rapports  dans le portail Microsoft 365 Defender en allant à Rapports e-mail & \> **collaboration** \> **e-mail & rapports de collaboration.**</span><span class="sxs-lookup"><span data-stu-id="8e13b-110">If you have the [necessary permissions](#what-permissions-are-needed-to-view-these-reports), you can view these reports in the Microsoft 365 Defender portal by going to **Reports** \> **Email & collaboration** \> **Email & collaboration reports**.</span></span> <span data-ttu-id="8e13b-111">Pour aller directement au tableau de bord Rapports, ouvrez <https://security.microsoft.com/emailandcollabreport> .</span><span class="sxs-lookup"><span data-stu-id="8e13b-111">To go directly to the Reports dashboard, open <https://security.microsoft.com/emailandcollabreport>.</span></span>

![Tableau de bord Rapports dans le portail Microsoft 365 Defender](../../media/email-collaboration-reports.png)

## <a name="compromised-users-report"></a><span data-ttu-id="8e13b-113">Rapport utilisateurs compromis</span><span class="sxs-lookup"><span data-stu-id="8e13b-113">Compromised users report</span></span>

> [!NOTE]
> <span data-ttu-id="8e13b-114">Ce rapport est disponible dans les organisations Microsoft 365 avec Exchange Online boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="8e13b-114">This report is available in Microsoft 365 organizations with Exchange Online mailboxes.</span></span> <span data-ttu-id="8e13b-115">Il n’est pas disponible dans les organisations Exchange Online Protection autonomes (EOP).</span><span class="sxs-lookup"><span data-stu-id="8e13b-115">It's not available in standalone Exchange Online Protection (EOP) organizations.</span></span>

<span data-ttu-id="8e13b-116">Le **rapport Utilisateurs** compromis indique le nombre de  comptes  d’utilisateurs marqués comme suspects ou restreints au cours des 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="8e13b-116">The **Compromised users** report shows shows the number of user accounts that were marked as **Suspicious** or **Restricted** within the last 7 days.</span></span> <span data-ttu-id="8e13b-117">Les comptes dans l’un de ces états sont problématiques, voire compromis.</span><span class="sxs-lookup"><span data-stu-id="8e13b-117">Accounts in either of these states are problematic or even compromised.</span></span> <span data-ttu-id="8e13b-118">Avec une utilisation fréquente, vous pouvez utiliser le rapport pour repérer des pics, voire des tendances, dans des comptes suspects ou restreints.</span><span class="sxs-lookup"><span data-stu-id="8e13b-118">With frequent use, you can use the report to spot spikes, and even trends, in suspicious or restricted accounts.</span></span> <span data-ttu-id="8e13b-119">Pour plus d’informations sur les utilisateurs compromis, voir [Répondre à un compte de messagerie compromis.](responding-to-a-compromised-email-account.md)</span><span class="sxs-lookup"><span data-stu-id="8e13b-119">For more information about compromised users, see [Responding to a compromised email account](responding-to-a-compromised-email-account.md).</span></span>

![Widget Utilisateurs compromis dans le tableau de bord Rapports](../../media/compromised-users-report-widget.png)

<span data-ttu-id="8e13b-121">L’affichage agrégé affiche les données des 90 derniers jours et l’affichage détail affiche les données des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="8e13b-121">The aggregate view shows data for the last 90 days and the detail view shows data for the last 30 days.</span></span>

<span data-ttu-id="8e13b-122">Pour afficher le rapport, ouvrez le portail  [Microsoft 365 Defender,](https://security.microsoft.com)allez à Rapports e-mail \> **& collaboration** \> **e-mail & rapports** de collaboration et cliquez sur Afficher les détails sous **Utilisateurs** compromis.</span><span class="sxs-lookup"><span data-stu-id="8e13b-122">To view the report, open the [Microsoft 365 Defender portal](https://security.microsoft.com), go to **Reports** \> **Email & collaboration** \> **Email & collaboration reports** and click **View details** under **Compromised users**.</span></span> <span data-ttu-id="8e13b-123">Pour aller directement dans le rapport, ouvrez <https://security.microsoft.com/reports/CompromisedUsers> .</span><span class="sxs-lookup"><span data-stu-id="8e13b-123">To go directly to the report, open <https://security.microsoft.com/reports/CompromisedUsers>.</span></span>

<span data-ttu-id="8e13b-124">Vous pouvez filtrer le graphique et le tableau de détails en cliquant sur **Filtres** et en sélectionnant une ou plusieurs des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="8e13b-124">You can filter both the chart and the details table by clicking **Filters** and selecting one or more of the following values:</span></span>

- <span data-ttu-id="8e13b-125">**Date de début et** **date de fin**</span><span class="sxs-lookup"><span data-stu-id="8e13b-125">**Start date** and **End date**</span></span>

- <span data-ttu-id="8e13b-126">**Suspect**: le compte d’utilisateur a envoyé des messages suspects et risque d’être limité à l’envoi de courriers électroniques.</span><span class="sxs-lookup"><span data-stu-id="8e13b-126">**Suspicious**: The user account has sent suspicious email and is at risk of being restricted from sending email.</span></span>

- <span data-ttu-id="8e13b-127">**Restreint :** le compte d’utilisateur n’a pas pu envoyer de courrier électronique en raison de modèles hautement suspects.</span><span class="sxs-lookup"><span data-stu-id="8e13b-127">**Restricted**: The user account has been restricted from sending email due to highly suspicious patterns.</span></span>

![Affichage du rapport dans le rapport Utilisateurs compromis](../../media/compromised-users-report-activity-view.png)

<span data-ttu-id="8e13b-129">Si vous cliquez **sur Afficher le tableau des détails,** vous pouvez voir les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="8e13b-129">If you click **View details table**, you can see the following details:</span></span>

- <span data-ttu-id="8e13b-130">**Heure de création**</span><span class="sxs-lookup"><span data-stu-id="8e13b-130">**Creation time**</span></span>
- <span data-ttu-id="8e13b-131">**ID d'utilisateur**</span><span class="sxs-lookup"><span data-stu-id="8e13b-131">**User ID**</span></span>
- <span data-ttu-id="8e13b-132">**Action**</span><span class="sxs-lookup"><span data-stu-id="8e13b-132">**Action**</span></span>

<span data-ttu-id="8e13b-133">Pour revenir à l’affichage du rapport, cliquez **sur Afficher le rapport.**</span><span class="sxs-lookup"><span data-stu-id="8e13b-133">To go back to the report view, click **View report**.</span></span>

## <a name="encryption-report"></a><span data-ttu-id="8e13b-134">Rapport de chiffrement</span><span class="sxs-lookup"><span data-stu-id="8e13b-134">Encryption report</span></span>

<span data-ttu-id="8e13b-135">Le **rapport de chiffrement** est disponible dans EOP (abonnements avec boîtes aux lettres dans Exchange Online ou EOP autonome sans boîtes aux lettres Exchange Online autonomes).</span><span class="sxs-lookup"><span data-stu-id="8e13b-135">The **Encryption report** is available in EOP (subscriptions with mailboxes in Exchange Online or standalone EOP without Exchange Online mailboxes).</span></span> <span data-ttu-id="8e13b-136">L’équipe de sécurité de votre organisation peut utiliser les informations de ce rapport pour identifier les modèles et appliquer ou ajuster de manière proactive les stratégies pour les messages électroniques sensibles.</span><span class="sxs-lookup"><span data-stu-id="8e13b-136">Your organization's security team can use information in this report to identify patterns and proactively apply or adjust policies for sensitive email messages.</span></span> <span data-ttu-id="8e13b-137">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="8e13b-137">For example:</span></span>

- <span data-ttu-id="8e13b-138">Si un nombre élevé de messages électroniques est chiffré par les utilisateurs, vous pouvez ajouter une stratégie de chiffrement pour automatiser le chiffrement dans certains cas d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="8e13b-138">If you see a high number of email messages encrypted by users, you might want to add an encryption policy to automate encryption for certain use cases.</span></span> <span data-ttu-id="8e13b-139">Pour plus d’informations, voir Définir des règles de flux de messagerie [pour chiffrer](../../compliance/define-mail-flow-rules-to-encrypt-email.md)les messages électroniques Microsoft 365 .</span><span class="sxs-lookup"><span data-stu-id="8e13b-139">For more information, see [Define mail flow rules to encrypt email messages in Microsoft 365](../../compliance/define-mail-flow-rules-to-encrypt-email.md).</span></span>

- <span data-ttu-id="8e13b-140">Si plusieurs modèles de chiffrement sont disponibles, mais que personne ne les utilise, vous pouvez déterminer si les utilisateurs ont besoin d’une formation sur les fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="8e13b-140">If you have a number of encryption templates available but no one is using them, you might explore whether users need feature training.</span></span>

<span data-ttu-id="8e13b-141">L’affichage agrégé autorise le filtrage pour les 90 derniers jours, tandis que l’affichage détail autorise le filtrage pendant 10 jours.</span><span class="sxs-lookup"><span data-stu-id="8e13b-141">The aggregate view allows filtering for the last 90 days, while the detail view allows filtering for 10 days.</span></span>

<span data-ttu-id="8e13b-142">Pour afficher le rapport, ouvrez le portail  [Microsoft 365 Defender,](https://security.microsoft.com)allez à Rapports e-mail & collaboration e-mail & rapports de collaboration et cliquez sur Afficher les détails sous Rapport de \>  \>  **chiffrement.** </span><span class="sxs-lookup"><span data-stu-id="8e13b-142">To view the report, open the [Microsoft 365 Defender portal](https://security.microsoft.com), go to **Reports** \> **Email & collaboration** \> **Email & collaboration reports** and click **View details** under **Encryption report**.</span></span> <span data-ttu-id="8e13b-143">Pour aller directement dans le rapport, ouvrez <https://protection.office.com/reportv2?id=EncryptionReport> .</span><span class="sxs-lookup"><span data-stu-id="8e13b-143">To go directly to the report, open <https://protection.office.com/reportv2?id=EncryptionReport>.</span></span>

<span data-ttu-id="8e13b-144">Pour en savoir plus sur le chiffrement, voir [chiffrement de courrier électronique dans Microsoft 365](../../compliance/email-encryption.md).</span><span class="sxs-lookup"><span data-stu-id="8e13b-144">To learn more about encryption, see [Email encryption in Microsoft 365](../../compliance/email-encryption.md).</span></span>

### <a name="report-view-for-the-encryption-report"></a><span data-ttu-id="8e13b-145">Affichage du rapport pour le rapport de chiffrement</span><span class="sxs-lookup"><span data-stu-id="8e13b-145">Report view for the Encryption report</span></span>

<span data-ttu-id="8e13b-146">Vous pouvez utiliser les filtres suivants sur le graphique :</span><span class="sxs-lookup"><span data-stu-id="8e13b-146">You can use the following filters on the chart:</span></span>

- <span data-ttu-id="8e13b-147">**Afficher les données par : Rapport de chiffrement des** messages et Décomposer par **:** Méthode de chiffrement : les méthodes de chiffrement suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="8e13b-147">**View data by: Message Encryption Report** and **Break down by: Encryption method**: The following encryption methods are available:</span></span>

  - <span data-ttu-id="8e13b-148">**Chiffrement par utilisateur**</span><span class="sxs-lookup"><span data-stu-id="8e13b-148">**Encryption by user**</span></span>
  - <span data-ttu-id="8e13b-149">**Chiffrement par stratégie**</span><span class="sxs-lookup"><span data-stu-id="8e13b-149">**Encryption by policy**</span></span>

  <span data-ttu-id="8e13b-150">Si vous cliquez **sur Filtres,** vous pouvez modifier le graphique avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="8e13b-150">If you click **Filters**, you can modify the chart with the following filters:</span></span>

  - <span data-ttu-id="8e13b-151">**Date de début et** **date de fin**</span><span class="sxs-lookup"><span data-stu-id="8e13b-151">**Start date** and **End date**</span></span>
  - <span data-ttu-id="8e13b-152">Méthode de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="8e13b-152">Encryption method.</span></span>
  - <span data-ttu-id="8e13b-153">Modèle de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="8e13b-153">Encryption template.</span></span>

- <span data-ttu-id="8e13b-154">**Afficher les données par : Rapport de chiffrement des** messages et Décomposer par **:** Modèle de chiffrement : les méthodes de chiffrement suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="8e13b-154">**View data by: Message Encryption Report** and **Break down by: Encryption template**: The following encryption methods are available:</span></span>

  - <span data-ttu-id="8e13b-155">**Ne pas avancer**</span><span class="sxs-lookup"><span data-stu-id="8e13b-155">**Do not forward**</span></span>
  - <span data-ttu-id="8e13b-156">**Chiffrer uniquement**</span><span class="sxs-lookup"><span data-stu-id="8e13b-156">**Encrypt only**</span></span>
  - <span data-ttu-id="8e13b-157">**Précédent d’OME**</span><span class="sxs-lookup"><span data-stu-id="8e13b-157">**OME previous**</span></span>
  - <span data-ttu-id="8e13b-158">**Custom**</span><span class="sxs-lookup"><span data-stu-id="8e13b-158">**Custom**</span></span>

  <span data-ttu-id="8e13b-159">Si vous cliquez **sur Filtres,** vous pouvez modifier le graphique avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="8e13b-159">If you click **Filters**, you can modify the chart with the following filters:</span></span>

  - <span data-ttu-id="8e13b-160">**Date de début et** **date de fin**</span><span class="sxs-lookup"><span data-stu-id="8e13b-160">**Start date** and **End date**</span></span>
  - <span data-ttu-id="8e13b-161">Méthode de chiffrement</span><span class="sxs-lookup"><span data-stu-id="8e13b-161">Encryption method</span></span>
  - <span data-ttu-id="8e13b-162">Modèle de chiffrement</span><span class="sxs-lookup"><span data-stu-id="8e13b-162">Encryption template</span></span>

- <span data-ttu-id="8e13b-163">**Afficher les données par : 5** principaux domaines de destinataires : cet affichage affiche un graphique en secteurs avec le nombre de messages envoyés pour les 5 principaux domaines de destinataires.</span><span class="sxs-lookup"><span data-stu-id="8e13b-163">**View data by: Top 5 recipient domains**: This view shows a pie chart with sent message counts for the top 5 recipient domains.</span></span>

  <span data-ttu-id="8e13b-164">Si vous cliquez sur **Filtres,** vous pouvez sélectionner une **date de début** et une **date de fin.**</span><span class="sxs-lookup"><span data-stu-id="8e13b-164">If you click **Filters**, you can select a **Start date** and **End date**.</span></span>

### <a name="details-table-view-for-the-encryption-report"></a><span data-ttu-id="8e13b-165">Vue de table Détails pour le rapport de chiffrement</span><span class="sxs-lookup"><span data-stu-id="8e13b-165">Details table view for the Encryption report</span></span>

<span data-ttu-id="8e13b-166">Si vous cliquez sur Afficher le tableau des **détails,** les informations affichées dépendent du graphique que vous regardiez :</span><span class="sxs-lookup"><span data-stu-id="8e13b-166">If you click **View details table**, the information that's shown depends on the chart you were looking at:</span></span>

- <span data-ttu-id="8e13b-167">**Décomposez par : méthode de chiffrement** ou décomposer par : modèle de **chiffrement**: les informations suivantes sont affichées :</span><span class="sxs-lookup"><span data-stu-id="8e13b-167">**Break down by: Encryption method** or **Break down by: Encryption template**: The following information is shown:</span></span>

  - <span data-ttu-id="8e13b-168">**Date**</span><span class="sxs-lookup"><span data-stu-id="8e13b-168">**Date**</span></span>
  - <span data-ttu-id="8e13b-169">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="8e13b-169">**Sender address**</span></span>
  - <span data-ttu-id="8e13b-170">**Modèle de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="8e13b-170">**Encryption template**</span></span>
  - <span data-ttu-id="8e13b-171">**Méthode de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="8e13b-171">**Encryption method**</span></span>
  - <span data-ttu-id="8e13b-172">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="8e13b-172">**Recipient address**</span></span>
  - <span data-ttu-id="8e13b-173">**Subject**</span><span class="sxs-lookup"><span data-stu-id="8e13b-173">**Subject**</span></span>

- <span data-ttu-id="8e13b-174">**Afficher les données par : 5 principaux domaines de destinataires**:</span><span class="sxs-lookup"><span data-stu-id="8e13b-174">**View data by: Top 5 recipient domains**:</span></span>

  - <span data-ttu-id="8e13b-175">**Date**</span><span class="sxs-lookup"><span data-stu-id="8e13b-175">**Date**</span></span>
  - <span data-ttu-id="8e13b-176">**Domaine du destinataire**</span><span class="sxs-lookup"><span data-stu-id="8e13b-176">**Recipient domain**</span></span>
  - <span data-ttu-id="8e13b-177">**Nombre de messages**</span><span class="sxs-lookup"><span data-stu-id="8e13b-177">**Message count**</span></span>

<span data-ttu-id="8e13b-178">Si vous cliquez **sur Filtres** dans une vue de tableau de détails, vous pouvez modifier les résultats avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="8e13b-178">If you click **Filters** in a details table view, you can modify the results with the following filters:</span></span>

- <span data-ttu-id="8e13b-179">**Date de début et** **date de fin**</span><span class="sxs-lookup"><span data-stu-id="8e13b-179">**Start date** and **End date**</span></span>
- <span data-ttu-id="8e13b-180">Méthode de chiffrement</span><span class="sxs-lookup"><span data-stu-id="8e13b-180">Encryption method</span></span>
- <span data-ttu-id="8e13b-181">Modèle de chiffrement</span><span class="sxs-lookup"><span data-stu-id="8e13b-181">Encryption template</span></span>

<span data-ttu-id="8e13b-182">Pour revenir à l’affichage du rapport, cliquez **sur Afficher le rapport.**</span><span class="sxs-lookup"><span data-stu-id="8e13b-182">To go back to the report view, click **View report**.</span></span>

## <a name="mailflow-status-report"></a><span data-ttu-id="8e13b-183">Rapport d’état du flux de messagerie</span><span class="sxs-lookup"><span data-stu-id="8e13b-183">Mailflow status report</span></span>

<span data-ttu-id="8e13b-184">Le **rapport d’état du flux de messagerie** contient des informations sur les programmes malveillants, le courrier indésirable, le hameçonnage et les messages edge bloqués.</span><span class="sxs-lookup"><span data-stu-id="8e13b-184">The **Mailflow status report** contains information about malware, spam, phishing and edge blocked messages.</span></span> <span data-ttu-id="8e13b-185">Pour plus d’informations, consultez [le rapport d’état du flux de messagerie.](view-mail-flow-reports.md#mailflow-status-report)</span><span class="sxs-lookup"><span data-stu-id="8e13b-185">For more details, see [Mailflow status report](view-mail-flow-reports.md#mailflow-status-report).</span></span>

## <a name="malware-detections-in-email-report"></a><span data-ttu-id="8e13b-186">Détections de programmes malveillants dans le rapport de courrier électronique</span><span class="sxs-lookup"><span data-stu-id="8e13b-186">Malware detections in email report</span></span>

<span data-ttu-id="8e13b-187">Le **rapport sur les programmes malveillants détectés** dans le rapport de courrier électronique affiche des informations sur les programmes malveillants détectés dans les messages électroniques entrants et sortants (programmes malveillants détectés par Exchange Online Protection ou EOP).</span><span class="sxs-lookup"><span data-stu-id="8e13b-187">The **Malware detections in email** report shows information about malware detections in incoming and outgoing email messages (malware detected by Exchange Online Protection or EOP).</span></span> <span data-ttu-id="8e13b-188">Pour plus d’informations sur la protection contre les programmes malveillants dans EOP, voir Protection contre les programmes [malveillants dans EOP.](anti-malware-protection.md)</span><span class="sxs-lookup"><span data-stu-id="8e13b-188">For more information about malware protection in EOP, see [Anti-malware protection in EOP](anti-malware-protection.md).</span></span>

 <span data-ttu-id="8e13b-189">Le filtre d’affichage agrégé autorise 90 jours, tandis que le filtre de tableau détails ne le permet que sur 10 jours.</span><span class="sxs-lookup"><span data-stu-id="8e13b-189">The aggregate view filter allows for 90 days, while the details table filter only allows for 10 days.</span></span>

<span data-ttu-id="8e13b-190">Pour afficher le rapport, ouvrez le portail  [Microsoft 365 Defender,](https://security.microsoft.com)allez à Rapports e-mail & collaboration e-mail & rapports de collaboration et cliquez sur Afficher les détails sous Programmes \>  \>  **malveillants détectés** dans le courrier **électronique.**</span><span class="sxs-lookup"><span data-stu-id="8e13b-190">To view the report, open the [Microsoft 365 Defender portal](https://security.microsoft.com), go to **Reports** \> **Email & collaboration** \> **Email & collaboration reports** and click **View details** under **Malware detected in email**.</span></span> <span data-ttu-id="8e13b-191">Pour aller directement dans le rapport, ouvrez <https://security.microsoft.com/reports/MalwareDetections> .</span><span class="sxs-lookup"><span data-stu-id="8e13b-191">To go directly to the report, open <https://security.microsoft.com/reports/MalwareDetections>.</span></span>

![Détections de programmes malveillants dans le widget de messagerie dans le tableau de bord Rapports](../../media/malware-detections-widget.png)

<span data-ttu-id="8e13b-193">Vous pouvez filtrer le graphique et le tableau de détails en cliquant sur **Filtres** et en sélectionnant :</span><span class="sxs-lookup"><span data-stu-id="8e13b-193">You can filter both the chart and the details table by clicking **Filters** and selecting:</span></span>

- <span data-ttu-id="8e13b-194">**Date de début et** **date de fin**</span><span class="sxs-lookup"><span data-stu-id="8e13b-194">**Start date** and **End date**</span></span>
- <span data-ttu-id="8e13b-195">**Entrant**</span><span class="sxs-lookup"><span data-stu-id="8e13b-195">**Inbound**</span></span>
- <span data-ttu-id="8e13b-196">**Sortant**</span><span class="sxs-lookup"><span data-stu-id="8e13b-196">**Outbound**</span></span>

![Affichage du rapport dans le rapport de détection des programmes malveillants dans le rapport de courrier électronique](../../media/malware-detections-report-view.png)

<span data-ttu-id="8e13b-198">Si vous cliquez **sur Afficher le tableau des détails,** vous pouvez voir les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="8e13b-198">If you click **View details table**, you can see the following details:</span></span>

- <span data-ttu-id="8e13b-199">**Date**</span><span class="sxs-lookup"><span data-stu-id="8e13b-199">**Date**</span></span>
- <span data-ttu-id="8e13b-200">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="8e13b-200">**Sender address**</span></span>
- <span data-ttu-id="8e13b-201">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="8e13b-201">**Recipient address**</span></span>
- <span data-ttu-id="8e13b-202">**ID de message**: disponible dans le champ d’en-tête **Message-ID** dans l’en-tête du message et doit être unique.</span><span class="sxs-lookup"><span data-stu-id="8e13b-202">**Message ID**: Available in the **Message-ID** header field in the message header and should be unique.</span></span> <span data-ttu-id="8e13b-203">Un exemple de valeur est `<08f1e0f6806a47b4ac103961109ae6ef@server.domain>` (notez les crochets).</span><span class="sxs-lookup"><span data-stu-id="8e13b-203">An example value is `<08f1e0f6806a47b4ac103961109ae6ef@server.domain>` (note the angle brackets).</span></span>
- <span data-ttu-id="8e13b-204">**Subject**</span><span class="sxs-lookup"><span data-stu-id="8e13b-204">**Subject**</span></span>
- <span data-ttu-id="8e13b-205">**Filename**</span><span class="sxs-lookup"><span data-stu-id="8e13b-205">**Filename**</span></span>
- <span data-ttu-id="8e13b-206">**Nom du programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="8e13b-206">**Malware name**</span></span>

<span data-ttu-id="8e13b-207">Pour revenir à l’affichage du rapport, cliquez **sur Afficher le rapport.**</span><span class="sxs-lookup"><span data-stu-id="8e13b-207">To go back to the report view, click **View report**.</span></span>

## <a name="mail-latency-report"></a><span data-ttu-id="8e13b-208">Rapport de latence du courrier</span><span class="sxs-lookup"><span data-stu-id="8e13b-208">Mail latency report</span></span>

<span data-ttu-id="8e13b-209">Le **rapport de latence du courrier** contient des informations sur la remise et la latence de détonation du courrier au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8e13b-209">The **Mail latency report** contains information on the mail delivery and detonation latency experienced within your organization.</span></span> <span data-ttu-id="8e13b-210">Pour plus d’informations, voir [Rapport de latence de messagerie.](view-reports-for-mdo.md#mail-latency-report)</span><span class="sxs-lookup"><span data-stu-id="8e13b-210">For more information, see [Mail latency report](view-reports-for-mdo.md#mail-latency-report).</span></span>

## <a name="sent-and-received-email-report"></a><span data-ttu-id="8e13b-211">Rapport de courrier électronique envoyé et reçu</span><span class="sxs-lookup"><span data-stu-id="8e13b-211">Sent and received email report</span></span>

<span data-ttu-id="8e13b-212">Le **rapport de** courrier électronique envoyé et reçu contient des informations sur les programmes malveillants, le courrier indésirable, les règles de flux de messagerie (également appelées règles de transport) et les détections avancées de programmes malveillants une fois que le courrier électronique est entré dans le service.</span><span class="sxs-lookup"><span data-stu-id="8e13b-212">The **Sent and received email** report contains information about malware, spam, mail flow rules (also known as transport rules), and advanced malware detections after email enters the service.</span></span> <span data-ttu-id="8e13b-213">Pour plus d’informations, consultez [le rapport de courrier électronique envoyé et reçu.](view-mail-flow-reports.md#sent-and-received-email-report)</span><span class="sxs-lookup"><span data-stu-id="8e13b-213">For more information, see [Sent and received email report](view-mail-flow-reports.md#sent-and-received-email-report).</span></span>

## <a name="spam-detections-report"></a><span data-ttu-id="8e13b-214">Rapport sur la détection des courriers indésirables</span><span class="sxs-lookup"><span data-stu-id="8e13b-214">Spam detections report</span></span>

<span data-ttu-id="8e13b-215">Le **rapport détections de** courrier indésirable affiche les messages électroniques de courrier indésirable bloqués par EOP.</span><span class="sxs-lookup"><span data-stu-id="8e13b-215">The **Spam detections** report shows spam email messages that were blocked by EOP.</span></span> <span data-ttu-id="8e13b-216">Les messages sont comptés individuellement, et non par destinataire.</span><span class="sxs-lookup"><span data-stu-id="8e13b-216">Messages are counted individually, not per recipient.</span></span> <span data-ttu-id="8e13b-217">Par exemple, si le même message de courrier indésirable a été envoyé à 100 destinataires de votre organisation, il compte comme un seul message.</span><span class="sxs-lookup"><span data-stu-id="8e13b-217">For example, if the same spam message was sent to 100 recipients in your organization, it counts as one message.</span></span>

<span data-ttu-id="8e13b-218">L’affichage agrégé autorise le filtrage sur 90 jours, tandis que le tableau de détails autorise le filtrage sur 10 jours.</span><span class="sxs-lookup"><span data-stu-id="8e13b-218">The aggregate view allows for 90 days filtering, while the details table allows for 10 days filtering.</span></span>

<span data-ttu-id="8e13b-219">Pour afficher le rapport, ouvrez le portail  [Microsoft 365 Defender,](https://security.microsoft.com)allez à Rapports e-mail & collaboration e-mail & rapports de collaboration et cliquez sur Afficher les \>  \>  **détails** sous Détections de courrier **indésirable.**</span><span class="sxs-lookup"><span data-stu-id="8e13b-219">To view the report, open the [Microsoft 365 Defender portal](https://security.microsoft.com), go to **Reports** \> **Email & collaboration** \> **Email & collaboration reports** and click click **View details** under **Spam detections**.</span></span> <span data-ttu-id="8e13b-220">Pour aller directement dans le rapport, ouvrez <https://security.microsoft.com/reports/SpamDetections> .</span><span class="sxs-lookup"><span data-stu-id="8e13b-220">To go directly to the report, open <https://security.microsoft.com/reports/SpamDetections>.</span></span>

![Widget de détection de courrier indésirable dans le tableau de bord Rapports](../../media/spam-detections-report-widget.png)

<span data-ttu-id="8e13b-222">Pour plus d’informations sur la protection contre le courrier indésirable, consultez la [protection anti-courrier indésirable dans EOP.](anti-spam-protection.md)</span><span class="sxs-lookup"><span data-stu-id="8e13b-222">For more information about anti-spam protection, see [Anti-spam protection in EOP](anti-spam-protection.md).</span></span>

### <a name="report-view-for-the-spam-detections-report"></a><span data-ttu-id="8e13b-223">Affichage du rapport pour le rapport détections de courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="8e13b-223">Report view for the Spam detections report</span></span>

<span data-ttu-id="8e13b-224">Les graphiques suivants sont disponibles dans l’affichage de rapport :</span><span class="sxs-lookup"><span data-stu-id="8e13b-224">The following charts are available in the report view:</span></span>

- <span data-ttu-id="8e13b-225">**Décomposez par : Action**: les types d’événements suivants sont affichés :</span><span class="sxs-lookup"><span data-stu-id="8e13b-225">**Break down by: Action**: The following event types are shown:</span></span>

  - <span data-ttu-id="8e13b-226">**Contenu de courrier indésirable filtré**</span><span class="sxs-lookup"><span data-stu-id="8e13b-226">**Spam content filtered**</span></span>
  - <span data-ttu-id="8e13b-227">**Blocage d’adresses IP de courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="8e13b-227">**Spam IP block**</span></span>
  - <span data-ttu-id="8e13b-228">**Bloc d’enveloppe de courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="8e13b-228">**Spam envelope block**</span></span>
  - <span data-ttu-id="8e13b-229">**Filtre DBEB de courrier indésirable**: blocage du bord basé sur l’annuaire (DBEB)</span><span class="sxs-lookup"><span data-stu-id="8e13b-229">**Spam DBEB filter**: Directory based edge blocking (DBEB)</span></span>

  <span data-ttu-id="8e13b-230">Lorsque vous pointez sur un jour (point de données) dans le graphique, vous pouvez voir le nombre d’éléments bloqués ce jour-là, ainsi que la façon dont ces éléments sont classés.</span><span class="sxs-lookup"><span data-stu-id="8e13b-230">When you hover over a day (data point) in the chart, you can see how many items were blocked that day, as well as how those items are categorized.</span></span>

  ![Affichage des actions dans le rapport détections de courrier indésirable](../../media/spam-detections-report-action-view.png)

- <span data-ttu-id="8e13b-232">**Décomposez par : Direction**: les instructions suivantes sont indiquées :</span><span class="sxs-lookup"><span data-stu-id="8e13b-232">**Break down by: Direction**: The following directions are shown:</span></span>

  - <span data-ttu-id="8e13b-233">**Entrant**</span><span class="sxs-lookup"><span data-stu-id="8e13b-233">**Inbound**</span></span>
  - <span data-ttu-id="8e13b-234">**Sortant**</span><span class="sxs-lookup"><span data-stu-id="8e13b-234">**Outbound**</span></span>

  ![Affichage de direction dans le rapport détections de courrier indésirable](../../media/spam-detections-report-direction-view.png)

<span data-ttu-id="8e13b-236">Si vous cliquez **sur Filtres** dans un affichage de rapport, vous pouvez modifier les résultats avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="8e13b-236">If you click **Filters** in a report view, you can modify the results with the following filters:</span></span>

- <span data-ttu-id="8e13b-237">**Date de début et** **date de fin**</span><span class="sxs-lookup"><span data-stu-id="8e13b-237">**Start date** and **End date**</span></span>
- <span data-ttu-id="8e13b-238">Valeurs de direction</span><span class="sxs-lookup"><span data-stu-id="8e13b-238">Direction values</span></span>
- <span data-ttu-id="8e13b-239">Valeurs de type d’événement</span><span class="sxs-lookup"><span data-stu-id="8e13b-239">Event type values</span></span>

### <a name="details-table-view-for-the-spam-detections-report"></a><span data-ttu-id="8e13b-240">Vue de table Détails pour le rapport détections de courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="8e13b-240">Details table view for the Spam detections report</span></span>

<span data-ttu-id="8e13b-241">Si vous cliquez **sur Afficher le tableau des détails** dans un affichage de rapport, les informations suivantes sont affichées :</span><span class="sxs-lookup"><span data-stu-id="8e13b-241">If you click **View details table** in any report view, the following information is shown:</span></span>

- <span data-ttu-id="8e13b-242">**Date**</span><span class="sxs-lookup"><span data-stu-id="8e13b-242">**Date**</span></span>
- <span data-ttu-id="8e13b-243">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="8e13b-243">**Sender address**</span></span>
- <span data-ttu-id="8e13b-244">**Adresse du destinataire**</span><span class="sxs-lookup"><span data-stu-id="8e13b-244">**Recipient address**</span></span>
- <span data-ttu-id="8e13b-245">**Type d’événement**</span><span class="sxs-lookup"><span data-stu-id="8e13b-245">**Event type**</span></span>
- <span data-ttu-id="8e13b-246">**Action**</span><span class="sxs-lookup"><span data-stu-id="8e13b-246">**Action**</span></span>
- <span data-ttu-id="8e13b-247">**Subject**</span><span class="sxs-lookup"><span data-stu-id="8e13b-247">**Subject**</span></span>

<span data-ttu-id="8e13b-248">Si vous cliquez **sur Filtres** dans un tableau de détails, vous pouvez modifier les résultats avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="8e13b-248">If you click **Filters** in a details table, you can modify the results with the following filters:</span></span>

- <span data-ttu-id="8e13b-249">**Date de début et** **date de fin**</span><span class="sxs-lookup"><span data-stu-id="8e13b-249">**Start date** and **End date**</span></span>
- <span data-ttu-id="8e13b-250">Valeurs de direction</span><span class="sxs-lookup"><span data-stu-id="8e13b-250">Direction values</span></span>
- <span data-ttu-id="8e13b-251">Valeurs de type d’événement</span><span class="sxs-lookup"><span data-stu-id="8e13b-251">Event type values</span></span>

<span data-ttu-id="8e13b-252">Pour revenir à l’affichage du rapport, cliquez **sur Afficher le rapport.**</span><span class="sxs-lookup"><span data-stu-id="8e13b-252">To go back to the report view, click **View report**.</span></span>

## <a name="spoof-detections-report"></a><span data-ttu-id="8e13b-253">Rapport sur les détections d’usurpation d’usurpation</span><span class="sxs-lookup"><span data-stu-id="8e13b-253">Spoof detections report</span></span>

> [!NOTE]
> <span data-ttu-id="8e13b-254">Le rapport sur les détections d’usurpation d’usurpation d’informations amélioré, tel que décrit dans cet article, est disponible en prévisualisation, peut faire l’objet de changements et n’est pas disponible dans toutes les organisations.</span><span class="sxs-lookup"><span data-stu-id="8e13b-254">The improved Spoof detections report as described in this article is in Preview, is subject to change, and is not available in all organizations.</span></span> <span data-ttu-id="8e13b-255">L’ancienne version du rapport n’a affiché que les messages **électroniques de qualité** et les **courriers indésirables**.</span><span class="sxs-lookup"><span data-stu-id="8e13b-255">The older version of the report showed only **Good mail** and **Caught as spam**.</span></span>

<span data-ttu-id="8e13b-256">Le **rapport sur les détections d’usurpation d’informations** affiche des informations sur les messages qui ont été bloqués ou autorisés en raison de l’usurpation.</span><span class="sxs-lookup"><span data-stu-id="8e13b-256">The **Spoof detections** report shows information about messages that were blocked or allowed due to spoofing.</span></span> <span data-ttu-id="8e13b-257">Pour plus d’informations sur l’usurpation d’adresse, voir Protection contre l’usurpation [d’adresses dans EOP.](anti-spoofing-protection.md)</span><span class="sxs-lookup"><span data-stu-id="8e13b-257">For more information about spoofing, see [Anti-spoofing protection in EOP](anti-spoofing-protection.md).</span></span>

<span data-ttu-id="8e13b-258">L’affichage agrégé du rapport autorise 45 jours de filtrage, tandis que l’affichage détaillé ne permet que dix jours <sup>\*</sup> de filtrage.</span><span class="sxs-lookup"><span data-stu-id="8e13b-258">The aggregate view of the report allows for 45 days of filtering<sup>\*</sup>, while the detail view only allows for ten days of filtering.</span></span>

<span data-ttu-id="8e13b-259"><sup>\*</sup> Au final, vous pourrez utiliser jusqu’à 90 jours de filtrage.</span><span class="sxs-lookup"><span data-stu-id="8e13b-259"><sup>\*</sup> Eventually, you'll be able to use up to 90 days of filtering.</span></span>

<span data-ttu-id="8e13b-260">Pour afficher le rapport, ouvrez le portail  [Microsoft 365 Defender,](https://security.microsoft.com)allez à Rapports e-mail & \> **collaboration** \> **e-mail & rapports** de collaboration et cliquez sur Afficher les détails sous **détections** d’usurpation d’adresses .</span><span class="sxs-lookup"><span data-stu-id="8e13b-260">To view the report, open the [Microsoft 365 Defender portal](https://security.microsoft.com), go to **Reports** \> **Email & collaboration** \> **Email & collaboration reports** and click **View details** under **Spoof detections**.</span></span> <span data-ttu-id="8e13b-261">Pour aller directement dans le rapport, ouvrez <https://security.microsoft.com/reports/SpoofMailReport> .</span><span class="sxs-lookup"><span data-stu-id="8e13b-261">To go directly to the report, open <https://security.microsoft.com/reports/SpoofMailReport>.</span></span>

![Widget de détections d’usurpation d’informations dans le tableau de bord Rapports](../../media/spoof-detections-widget.png)

<span data-ttu-id="8e13b-263">Lorsque vous pointez sur un jour (point de données) dans le graphique, vous pouvez voir combien de messages usurpés ont été détectés et pourquoi.</span><span class="sxs-lookup"><span data-stu-id="8e13b-263">When you hover over a day (data point) in the chart, you can see how many spoofed messages were detected and why.</span></span>

<span data-ttu-id="8e13b-264">Vous pouvez filtrer le graphique et le tableau de détails en cliquant sur **Filtres** et en sélectionnant une ou plusieurs des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="8e13b-264">You can filter both the chart and the details table by clicking **Filters** and selecting one or more of the following values:</span></span>

- <span data-ttu-id="8e13b-265">**Date de début et** **date de fin**</span><span class="sxs-lookup"><span data-stu-id="8e13b-265">**Start date** and **End date**</span></span>

- <span data-ttu-id="8e13b-266">**Résultat**</span><span class="sxs-lookup"><span data-stu-id="8e13b-266">**Result**</span></span>
  - <span data-ttu-id="8e13b-267">**Pass**</span><span class="sxs-lookup"><span data-stu-id="8e13b-267">**Pass**</span></span>
  - <span data-ttu-id="8e13b-268">**Échec**</span><span class="sxs-lookup"><span data-stu-id="8e13b-268">**Fail**</span></span>
  - <span data-ttu-id="8e13b-269">**SoftPass**</span><span class="sxs-lookup"><span data-stu-id="8e13b-269">**SoftPass**</span></span>
  - <span data-ttu-id="8e13b-270">**Aucune**</span><span class="sxs-lookup"><span data-stu-id="8e13b-270">**None**</span></span>
  - <span data-ttu-id="8e13b-271">**Other**</span><span class="sxs-lookup"><span data-stu-id="8e13b-271">**Other**</span></span>

- <span data-ttu-id="8e13b-272">**Type d’usurpation :** **interne** et **externe**</span><span class="sxs-lookup"><span data-stu-id="8e13b-272">**Spoof type**: **Internal** and **External**</span></span>

![Affichage du rapport dans le rapport de détections d’usurpation d’usurpation d’état](../../media/spoof-detections-report-view.png)

<span data-ttu-id="8e13b-274">Si vous cliquez **sur Afficher le tableau des détails,** vous pouvez voir les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="8e13b-274">If you click **View details table**, you can see the following details:</span></span>

- <span data-ttu-id="8e13b-275">**Date**</span><span class="sxs-lookup"><span data-stu-id="8e13b-275">**Date**</span></span>
- <span data-ttu-id="8e13b-276">**Utilisateur usurpé**</span><span class="sxs-lookup"><span data-stu-id="8e13b-276">**Spoofed user**</span></span>
- <span data-ttu-id="8e13b-277">**Infrastructure d’envoi**</span><span class="sxs-lookup"><span data-stu-id="8e13b-277">**Sending infrastructure**</span></span>
- <span data-ttu-id="8e13b-278">**Type d’usurpation**</span><span class="sxs-lookup"><span data-stu-id="8e13b-278">**Spoof type**</span></span>
- <span data-ttu-id="8e13b-279">**Résultat**</span><span class="sxs-lookup"><span data-stu-id="8e13b-279">**Result**</span></span>
- <span data-ttu-id="8e13b-280">**Code de résultat**</span><span class="sxs-lookup"><span data-stu-id="8e13b-280">**Result code**</span></span>
- <span data-ttu-id="8e13b-281">**SPF**</span><span class="sxs-lookup"><span data-stu-id="8e13b-281">**SPF**</span></span>
- <span data-ttu-id="8e13b-282">**DKIM**</span><span class="sxs-lookup"><span data-stu-id="8e13b-282">**DKIM**</span></span>
- <span data-ttu-id="8e13b-283">**DMARC**</span><span class="sxs-lookup"><span data-stu-id="8e13b-283">**DMARC**</span></span>
- <span data-ttu-id="8e13b-284">**Nombre de messages**</span><span class="sxs-lookup"><span data-stu-id="8e13b-284">**Message count**</span></span>

<span data-ttu-id="8e13b-285">Pour revenir à l’affichage du rapport, cliquez **sur Afficher le rapport.**</span><span class="sxs-lookup"><span data-stu-id="8e13b-285">To go back to the report view, click **View report**.</span></span>

<span data-ttu-id="8e13b-286">Pour plus d’informations sur les codes de résultats d’authentification composite, consultez les [en-têtes de message anti-courrier](anti-spam-message-headers.md)indésirable Microsoft 365 .</span><span class="sxs-lookup"><span data-stu-id="8e13b-286">For more information about composite authentication result codes, see [Anti-spam message headers in Microsoft 365](anti-spam-message-headers.md).</span></span>

## <a name="threat-protection-status-report"></a><span data-ttu-id="8e13b-287">Rapport sur l’état de la protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="8e13b-287">Threat protection status report</span></span>

<span data-ttu-id="8e13b-288">Le **rapport d’état de la protection** contre les menaces est disponible dans EOP et Microsoft Defender pour Office 365 ; toutefois, les rapports contiennent des données différentes.</span><span class="sxs-lookup"><span data-stu-id="8e13b-288">The **Threat protection status** report is available in both EOP and Microsoft Defender for Office 365; however, the reports contain different data.</span></span> <span data-ttu-id="8e13b-289">Par exemple, les clients EOP peuvent afficher des informations sur les programmes malveillants détectés dans le courrier électronique, mais pas sur les fichiers malveillants détectés par les pièces [jointes sécurisées](mdo-for-spo-odb-and-teams.md)pour SharePoint, OneDrive et Microsoft Teams .</span><span class="sxs-lookup"><span data-stu-id="8e13b-289">For example, EOP customers can view information about malware detected in email, but not information about malicious files detected by [Safe Attachments for SharePoint, OneDrive, and Microsoft Teams](mdo-for-spo-odb-and-teams.md).</span></span>

<span data-ttu-id="8e13b-290">Le rapport indique le nombre de messages électroniques avec du contenu malveillant, tels que des fichiers ou des adresses web (URL) bloqués par le [](safe-links.md)moteur anti-programme malveillant, la purge automatique d’heure zéro [(ZAP)](zero-hour-auto-purge.md)et Defender pour les fonctionnalités de Office 365 telles que les liens [sécurisés,](safe-attachments.md)les pièces jointes et l’anti-hameçonnage. [](set-up-anti-phishing-policies.md)</span><span class="sxs-lookup"><span data-stu-id="8e13b-290">The report provides the count of email messages with malicious content, such as files or website addresses (URLs) that were blocked by the anti-malware engine, [zero-hour auto purge (ZAP)](zero-hour-auto-purge.md), and Defender for Office 365 features like [Safe Links](safe-links.md), [Safe Attachments](safe-attachments.md), and [Anti-phishing](set-up-anti-phishing-policies.md).</span></span> <span data-ttu-id="8e13b-291">Vous pouvez utiliser ces informations pour identifier les tendances ou déterminer si les stratégies d’organisation doivent être ajuster.</span><span class="sxs-lookup"><span data-stu-id="8e13b-291">You can use this information to identify trends or determine whether organization policies need adjustment.</span></span>

<span data-ttu-id="8e13b-292">**Remarque**: il est important de comprendre que si un message est envoyé à cinq destinataires, nous le compterons comme cinq messages différents et pas un seul message.</span><span class="sxs-lookup"><span data-stu-id="8e13b-292">**Note**: It's important to understand that if a message is sent to five recipients we count it as five different messages and not one message.</span></span>

<span data-ttu-id="8e13b-293">Pour afficher le rapport, ouvrez le portail  [Microsoft 365 Defender,](https://security.microsoft.com)allez à Rapports e-mail \> **& collaboration** \> **e-mail & rapports** de collaboration et cliquez sur Afficher les détails sous État de la protection contre les **menaces.** </span><span class="sxs-lookup"><span data-stu-id="8e13b-293">To view the report, open the [Microsoft 365 Defender portal](https://security.microsoft.com), go to **Reports** \> **Email & collaboration** \> **Email & collaboration reports** and click **View details** under **Threat protection status**.</span></span> <span data-ttu-id="8e13b-294">Pour aller directement dans le rapport, ouvrez l’une des URL suivantes :</span><span class="sxs-lookup"><span data-stu-id="8e13b-294">To go directly to the report, open one of the following URLs:</span></span>

- <span data-ttu-id="8e13b-295">Microsoft Defender pour Office 365 :<https://protection.office.com/reportv2?id=TPSAggregateReportATP></span><span class="sxs-lookup"><span data-stu-id="8e13b-295">Microsoft Defender for Office 365: <https://protection.office.com/reportv2?id=TPSAggregateReportATP></span></span>
- <span data-ttu-id="8e13b-296">EOP : <https://protection.office.com/reportv2?id=TPSAggregateReport></span><span class="sxs-lookup"><span data-stu-id="8e13b-296">EOP: <https://protection.office.com/reportv2?id=TPSAggregateReport></span></span>

![Widget d’état de la protection contre les menaces dans le tableau de bord Rapports](../../media/threat-protection-status-report-widget.png)

<span data-ttu-id="8e13b-298">Par défaut, le graphique affiche les données des 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="8e13b-298">By default, the chart shows data for the past 7 days.</span></span> <span data-ttu-id="8e13b-299">Si vous cliquez sur **Filtres,** vous pouvez sélectionner une plage de dates de 90 jours (les abonnements d’essai peuvent être limités à 30 jours).</span><span class="sxs-lookup"><span data-stu-id="8e13b-299">If you click **Filters**, you can select a 90 day date range (trial subscriptions might be limited to 30 days).</span></span> <span data-ttu-id="8e13b-300">L’affichage Tableau détails autorise le filtrage pendant 30 jours.</span><span class="sxs-lookup"><span data-stu-id="8e13b-300">The details table view allows filtering for 30 days.</span></span>

### <a name="report-view-for-the-threat-protection-status-report"></a><span data-ttu-id="8e13b-301">Affichage du rapport pour le rapport d’état de la protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="8e13b-301">Report view for the Threat protection status report</span></span>

<span data-ttu-id="8e13b-302">Les vues disponibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="8e13b-302">The following views are available:</span></span>

- <span data-ttu-id="8e13b-303">**Afficher les données par : Vue d’ensemble**: les informations de détection suivantes sont affichées :</span><span class="sxs-lookup"><span data-stu-id="8e13b-303">**View data by: Overview**: The following detection information is shown:</span></span>

  - <span data-ttu-id="8e13b-304">**Programme malveillant de messagerie**</span><span class="sxs-lookup"><span data-stu-id="8e13b-304">**Email malware**</span></span>
  - <span data-ttu-id="8e13b-305">**Hameçonnage par e-mail**</span><span class="sxs-lookup"><span data-stu-id="8e13b-305">**Email phish**</span></span>
  - <span data-ttu-id="8e13b-306">**Programme malveillant de contenu**</span><span class="sxs-lookup"><span data-stu-id="8e13b-306">**Content malware**</span></span>

  ![Vue d’ensemble dans le rapport d’état de la protection contre les menaces](../../media/threat-protection-status-report-overview-view.png)

- <span data-ttu-id="8e13b-308">**Afficher les données par : Contenu \> Programme**<sup>malveillant 1</sup>: les informations suivantes s’affiche pour Microsoft Defender pour Office 365 organisations :</span><span class="sxs-lookup"><span data-stu-id="8e13b-308">**View data by: Content \> Malware**<sup>1</sup>: The following information is shown for Microsoft Defender for Office 365 organizations:</span></span>

  - <span data-ttu-id="8e13b-309">**Moteur anti-programme** malveillant : fichiers malveillants détectés dans Sharepoint, OneDrive et Microsoft Teams par la détection de virus intégrée dans [Microsoft 365](virus-detection-in-spo.md).</span><span class="sxs-lookup"><span data-stu-id="8e13b-309">**Anti-malware engine**: Malicious files detected in Sharepoint, OneDrive, and Microsoft Teams by the [built-in virus detection in Microsoft 365](virus-detection-in-spo.md).</span></span>
  - <span data-ttu-id="8e13b-310">**Détonation de fichiers**: fichiers malveillants détectés par les pièces [jointes SharePoint, OneDrive et Microsoft Teams](mdo-for-spo-odb-and-teams.md).</span><span class="sxs-lookup"><span data-stu-id="8e13b-310">**File detonation**: Malicious files detected by [Safe Attachments for SharePoint, OneDrive, and Microsoft Teams](mdo-for-spo-odb-and-teams.md).</span></span>

  ![Affichage des programmes malveillants de contenu dans le rapport d’état de la protection contre les menaces](../../media/threat-protection-status-report-content-malware-view.png)

- <span data-ttu-id="8e13b-312">**Afficher les données par : Remplacement de message**: les informations de motif de remplacement suivantes sont affichées :</span><span class="sxs-lookup"><span data-stu-id="8e13b-312">**View data by: Message Override**: The following override reason information is shown:</span></span>

  - <span data-ttu-id="8e13b-313">**Ignorer l’local**</span><span class="sxs-lookup"><span data-stu-id="8e13b-313">**On-premises skip**</span></span>
  - <span data-ttu-id="8e13b-314">**IP Allow**</span><span class="sxs-lookup"><span data-stu-id="8e13b-314">**IP Allow**</span></span>
  - <span data-ttu-id="8e13b-315">**Règle de flux de messagerie**</span><span class="sxs-lookup"><span data-stu-id="8e13b-315">**Mail flow rule**</span></span>
  - <span data-ttu-id="8e13b-316">**Autoriser l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="8e13b-316">**Sender allow**</span></span>
  - <span data-ttu-id="8e13b-317">**Domaine autoriser**</span><span class="sxs-lookup"><span data-stu-id="8e13b-317">**Domain allow**</span></span>
  - <span data-ttu-id="8e13b-318">**ZAP non activé**</span><span class="sxs-lookup"><span data-stu-id="8e13b-318">**ZAP not enabled**</span></span>
  - <span data-ttu-id="8e13b-319">**Dossier Courrier indésirable non activé**</span><span class="sxs-lookup"><span data-stu-id="8e13b-319">**Junk Mail folder not enabled**</span></span>
  - <span data-ttu-id="8e13b-320">**Expéditeur sécurisé de l’utilisateur**</span><span class="sxs-lookup"><span data-stu-id="8e13b-320">**User Safe Sender**</span></span>
  - <span data-ttu-id="8e13b-321">**Domaine sécurisé de l’utilisateur**</span><span class="sxs-lookup"><span data-stu-id="8e13b-321">**User Safe Domain**</span></span>

  ![Affichage des remplacements de messages dans le rapport d’état de la protection contre les menaces](../../media/threat-protection-status-report-message-override-view.png)

- <span data-ttu-id="8e13b-323">**Décomposez par : technologie de détection et** affichage des données par : Hameçonnage de messagerie : les informations suivantes sont affichées : **\>**</span><span class="sxs-lookup"><span data-stu-id="8e13b-323">**Break down by: Detection technology** and **View data by: Email \> Phish**: The following information is shown:</span></span>

  - <span data-ttu-id="8e13b-324">**Réputation d’URL** générée par atp <sup>1</sup>: réputation d’URL malveillante générée à partir de Defender pour Office 365 détonations dans d’autres Microsoft 365 clients.</span><span class="sxs-lookup"><span data-stu-id="8e13b-324">**ATP-generated URL reputation**<sup>1</sup>: Malicious URL reputation generated from Defender for Office 365 detonations in other Microsoft 365 customers.</span></span>
  - <span data-ttu-id="8e13b-325">**Filtre de hameçonnage avancé**: signaux de hameçonnage basés sur l’apprentissage automatique.</span><span class="sxs-lookup"><span data-stu-id="8e13b-325">**Advanced phish filter**: Phishing signals based on machine learning.</span></span>
  - <span data-ttu-id="8e13b-326">**Anti-usurpation - Échec DMARC**: échec de l’authentification DMARC sur les messages.</span><span class="sxs-lookup"><span data-stu-id="8e13b-326">**Anti-spoof - DMARC failure**: DMARC authentication failure on messages.</span></span>
  - <span data-ttu-id="8e13b-327">**Anti-usurpation - intra-organisation**: l’expéditeur tente d’usurper le domaine du destinataire.</span><span class="sxs-lookup"><span data-stu-id="8e13b-327">**Anti-spoof - intra-org**: Sender is trying to spoof the recipient domain.</span></span>
  - <span data-ttu-id="8e13b-328">**Anti-usurpation - domaine externe**: l’expéditeur tente d’usurper un autre domaine.</span><span class="sxs-lookup"><span data-stu-id="8e13b-328">**Anti-spoof - external domain**: Sender is trying to spoof some other domain.</span></span>
  - <span data-ttu-id="8e13b-329">**Emprunt d’identité de marque**: emprunt d’identité de marques connues basées sur des expéditeurs.</span><span class="sxs-lookup"><span data-stu-id="8e13b-329">**Brand impersonation**: Impersonation of well-known brands based on senders.</span></span>
  - <span data-ttu-id="8e13b-330">**Emprunt d’identité**<sup>de domaine 1</sup>: emprunt d’identité des domaines que le client possède ou définit.</span><span class="sxs-lookup"><span data-stu-id="8e13b-330">**Domain impersonation**<sup>1</sup>: Impersonation of domains that the customer owns or defines.</span></span>
  - <span data-ttu-id="8e13b-331">**Réputation de l’URL EOP**: réputation d’URL malveillante.</span><span class="sxs-lookup"><span data-stu-id="8e13b-331">**EOP URL reputation**: Malicious URL reputation.</span></span>
  - <span data-ttu-id="8e13b-332">**Filtre d’hameçonnage général**: signaux de hameçonnage basés sur des règles d’analyste.</span><span class="sxs-lookup"><span data-stu-id="8e13b-332">**General phish filter**: Phishing signals based on analyst rules.</span></span>
  - <span data-ttu-id="8e13b-333">**Autres**</span><span class="sxs-lookup"><span data-stu-id="8e13b-333">**Others**</span></span>
  - <span data-ttu-id="8e13b-334">**Phish ZAP**<sup>2 :</sup>purge automatique zéro heure des messages de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="8e13b-334">**Phish ZAP**<sup>2</sup>: Zero hour auto purge of phishing messages.</span></span>
  - <span data-ttu-id="8e13b-335">**Détonation d’URL**<sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="8e13b-335">**URL detonation**<sup>1</sup></span></span>
  - <span data-ttu-id="8e13b-336">**Emprunt d’identité**<sup>d’utilisateur 1</sup>: emprunt d’identité des utilisateurs définis par l’administrateur ou appris par le biais de l’intelligence des boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="8e13b-336">**User impersonation**<sup>1</sup>: Impersonation of users defined by admin or learned through mailbox intelligence.</span></span>

  ![Affichage de la technologie de détection pour le courrier d’hameçonnage dans le rapport d’état de la protection contre les menaces](../../media/threat-protection-status-report-phishing-detection-tech-view.png)

- <span data-ttu-id="8e13b-338">**Décomposez par : technologie de détection et** affichage des données par : Programme malveillant de messagerie : les informations suivantes sont affichées : **\>**</span><span class="sxs-lookup"><span data-stu-id="8e13b-338">**Break down by: Detection technology** and **View data by: Email \> Malware**: The following information is shown:</span></span>

  - <span data-ttu-id="8e13b-339">Réputation de fichier générée **par atp**<sup>1</sup>: toutes les réputations de fichiers malveillants générées par Defender pour Office 365 détonations.</span><span class="sxs-lookup"><span data-stu-id="8e13b-339">**ATP-generated file reputation**<sup>1</sup>: All malicious file reputation generated by Defender for Office 365 detonations.</span></span>
  - <span data-ttu-id="8e13b-340">**Moteur anti-programme malveillant**<sup>1 :</sup>détection des moteurs anti-programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="8e13b-340">**Anti-malware engine**<sup>1</sup>: Detection from anti-malware engines.</span></span>
  - <span data-ttu-id="8e13b-341">Blocage du type de fichier de stratégie **anti-programme** malveillant : il s’adresse aux messages électroniques filtrés en raison du type de fichier malveillant identifié dans le message.</span><span class="sxs-lookup"><span data-stu-id="8e13b-341">**Anti-malware policy file type block**: These are email messages filtered out due to the type of malicious file identified in the message.</span></span>
  - <span data-ttu-id="8e13b-342">**Détonation de fichier**<sup>1</sup>: détection par pièces jointes fiables.</span><span class="sxs-lookup"><span data-stu-id="8e13b-342">**File detonation**<sup>1</sup>: Detection by Safe Attachments.</span></span>
  - <span data-ttu-id="8e13b-343">**Réputation d’un fichier malveillant**</span><span class="sxs-lookup"><span data-stu-id="8e13b-343">**Malicious file reputation**</span></span>
  - <span data-ttu-id="8e13b-344">**Programme malveillant ZAP**<sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="8e13b-344">**Malware ZAP**<sup>2</sup></span></span>
  - <span data-ttu-id="8e13b-345">**Autres**</span><span class="sxs-lookup"><span data-stu-id="8e13b-345">**Others**</span></span>

  ![Affichage de la technologie de détection pour les programmes malveillants dans le rapport d’état de la protection contre les menaces](../../media/threat-protection-status-report-malware-detection-tech-view.png)

- <span data-ttu-id="8e13b-347">**Décomposez par : Type** de stratégie et afficher les données par **: \> Hameçonnage** de messagerie ou Affichage des données par : Programme malveillant de messagerie : les informations suivantes sont affichées : **\>**</span><span class="sxs-lookup"><span data-stu-id="8e13b-347">**Break down by: Policy type** and **View data by: Email \> Phish** or **View data by: Email \> Malware**: The following information is shown:</span></span>

  - <span data-ttu-id="8e13b-348">**Anti-programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="8e13b-348">**Anti-malware**</span></span>
  - <span data-ttu-id="8e13b-349">**Pièces jointes sécurisées**<sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="8e13b-349">**Safe Attachments**<sup>1</sup></span></span>
  - <span data-ttu-id="8e13b-350">**Anti-hameçonnage**</span><span class="sxs-lookup"><span data-stu-id="8e13b-350">**Anti-phish**</span></span>
  - <span data-ttu-id="8e13b-351">**Anti-courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="8e13b-351">**Anti-spam**</span></span>
  - <span data-ttu-id="8e13b-352">**Règle de flux de messagerie** (également appelée règle de transport)</span><span class="sxs-lookup"><span data-stu-id="8e13b-352">**Mail flow rule** (also known as a transport rule)</span></span>
  - <span data-ttu-id="8e13b-353">**Autres**</span><span class="sxs-lookup"><span data-stu-id="8e13b-353">**Others**</span></span>

  ![Affichage du type de stratégie pour le courrier de hameçonnage dans le rapport d’état de la protection contre les menaces](../../media/threat-protection-status-report-phishing-policy-type-view.png)

- <span data-ttu-id="8e13b-355">**Décomposez par : État de** remise et affichage des données par : **\> Hameçonnage** de messagerie ou Affichage des données par : Programme malveillant de messagerie : les informations suivantes sont affichées : **\>**</span><span class="sxs-lookup"><span data-stu-id="8e13b-355">**Break down by: Delivery status** and **View data by: Email \> Phish** or **View data by: Email \> Malware**: The following information is shown:</span></span>

  - <span data-ttu-id="8e13b-356">**Échec de remise**</span><span class="sxs-lookup"><span data-stu-id="8e13b-356">**Delivery failed**</span></span>
  - <span data-ttu-id="8e13b-357">**Dropped**</span><span class="sxs-lookup"><span data-stu-id="8e13b-357">**Dropped**</span></span>
  - <span data-ttu-id="8e13b-358">**Forwarded**</span><span class="sxs-lookup"><span data-stu-id="8e13b-358">**Forwarded**</span></span>
  - <span data-ttu-id="8e13b-359">**Boîte aux lettres hébergée : dossier personnalisé**</span><span class="sxs-lookup"><span data-stu-id="8e13b-359">**Hosted mailbox: Custom folder**</span></span>
  - <span data-ttu-id="8e13b-360">**Boîte aux lettres hébergée : éléments supprimés**</span><span class="sxs-lookup"><span data-stu-id="8e13b-360">**Hosted mailbox: Deleted items**</span></span>
  - <span data-ttu-id="8e13b-361">**Boîte aux lettres hébergée : Boîte de réception**</span><span class="sxs-lookup"><span data-stu-id="8e13b-361">**Hosted mailbox: Inbox**</span></span>
  - <span data-ttu-id="8e13b-362">**Boîte aux lettres hébergée : courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="8e13b-362">**Hosted mailbox: Junk**</span></span>
  - <span data-ttu-id="8e13b-363">**Serveur local : remis**</span><span class="sxs-lookup"><span data-stu-id="8e13b-363">**On-premises server: Delivered**</span></span>
  - <span data-ttu-id="8e13b-364">**Mise en quarantaine**</span><span class="sxs-lookup"><span data-stu-id="8e13b-364">**Quarantine**</span></span>

  ![Affichage de l’état de remise du courrier de hameçonnage dans le rapport d’état de la protection contre les menaces](../../media/threat-protection-status-report-phishing-delivery-status-view.png)

<span data-ttu-id="8e13b-366"><sup>1</sup> Defender pour Office 365 uniquement</span><span class="sxs-lookup"><span data-stu-id="8e13b-366"><sup>1</sup> Defender for Office 365 only</span></span>

<span data-ttu-id="8e13b-367">La purge automatique de <sup>2</sup> heures zéro (ZAP) n’est pas disponible dans EOP autonome (elle fonctionne uniquement dans Exchange Online boîtes aux lettres).</span><span class="sxs-lookup"><span data-stu-id="8e13b-367"><sup>2</sup> Zero-hour auto purge (ZAP) isn't available in standalone EOP (it only works in Exchange Online mailboxes).</span></span>

<span data-ttu-id="8e13b-368">Si vous cliquez sur **Filtres,** les filtres disponibles dépendent du graphique que vous regardiez :</span><span class="sxs-lookup"><span data-stu-id="8e13b-368">If you click **Filters**, the filters available depends on the chart you were looking at:</span></span>

- <span data-ttu-id="8e13b-369">Pour **afficher les données par : Programme malveillant de \> contenu,** vous pouvez modifier le rapport par **date** de début et **de fin,** ainsi que la **valeur de** détection.</span><span class="sxs-lookup"><span data-stu-id="8e13b-369">For **View data by: Content \> Malware**, you can modify the report by **Start date** and **End date**, and the **Detection** value.</span></span>

- <span data-ttu-id="8e13b-370">Pour **afficher les données par : Remplacement de message,** vous pouvez modifier le rapport avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="8e13b-370">For **View data by: Message Override**, you can modify the report with the following filters:</span></span>

  - <span data-ttu-id="8e13b-371">**Date de début** et **date de fin**</span><span class="sxs-lookup"><span data-stu-id="8e13b-371">**Start date** and **End date**</span></span>
  - <span data-ttu-id="8e13b-372">**Override Reason**</span><span class="sxs-lookup"><span data-stu-id="8e13b-372">**Override Reason**</span></span>
  - <span data-ttu-id="8e13b-373">**Balise**: filtrer les résultats par utilisateurs ou groupes pour lesquels la balise utilisateur spécifiée a été appliquée (y compris les comptes de priorité).</span><span class="sxs-lookup"><span data-stu-id="8e13b-373">**Tag**: Filter the results by users or groups that have had the specified user tag applied (including priority accounts).</span></span> <span data-ttu-id="8e13b-374">Pour plus d’informations sur les balises utilisateur, voir [Balises utilisateur.](user-tags.md)</span><span class="sxs-lookup"><span data-stu-id="8e13b-374">For more information about user tags, see [User tags](user-tags.md).</span></span>
  - <span data-ttu-id="8e13b-375">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8e13b-375">**Domain**</span></span>

- <span data-ttu-id="8e13b-376">Pour tous les autres affichages, vous pouvez modifier le rapport avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="8e13b-376">For all other views, you can modify the report with the following filters:</span></span>

  - <span data-ttu-id="8e13b-377">**Date de début** et **date de fin**</span><span class="sxs-lookup"><span data-stu-id="8e13b-377">**Start date** and **End date**</span></span>
  - <span data-ttu-id="8e13b-378">**Détection**</span><span class="sxs-lookup"><span data-stu-id="8e13b-378">**Detection**</span></span>
  - <span data-ttu-id="8e13b-379">**Protégé par**: **ATP** ou **EOP**</span><span class="sxs-lookup"><span data-stu-id="8e13b-379">**Protected by**: **ATP** or **EOP**</span></span>
  - <span data-ttu-id="8e13b-380">**Balise**: filtrer les résultats par utilisateurs ou groupes pour lesquels la balise utilisateur spécifiée a été appliquée (y compris les comptes de priorité).</span><span class="sxs-lookup"><span data-stu-id="8e13b-380">**Tag**: Filter the results by users or groups that have had the specified user tag applied (including priority accounts).</span></span> <span data-ttu-id="8e13b-381">Pour plus d’informations sur les balises utilisateur, voir [Balises utilisateur.](user-tags.md)</span><span class="sxs-lookup"><span data-stu-id="8e13b-381">For more information about user tags, see [User tags](user-tags.md).</span></span>
  - <span data-ttu-id="8e13b-382">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8e13b-382">**Domain**</span></span>

### <a name="details-table-view-for-the-threat-protection-status-report"></a><span data-ttu-id="8e13b-383">Affichage du tableau détails pour le rapport d’état de la protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="8e13b-383">Details table view for the Threat protection status report</span></span>

<span data-ttu-id="8e13b-384">Si vous cliquez sur Afficher le tableau des **détails,** les informations affichées dépendent du graphique que vous regardiez :</span><span class="sxs-lookup"><span data-stu-id="8e13b-384">If you click **View details table**, the information that's shown depends on the chart you were looking at:</span></span>

- <span data-ttu-id="8e13b-385">**Afficher les données par : Vue d’ensemble**: aucun bouton de **table Afficher les détails** n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="8e13b-385">**View data by: Overview**: No **View details table** button is available.</span></span>

- <span data-ttu-id="8e13b-386">**Afficher les données par : Contenu \> Programmes malveillants**:</span><span class="sxs-lookup"><span data-stu-id="8e13b-386">**View data by: Content \> Malware**:</span></span>

  - <span data-ttu-id="8e13b-387">**Date**</span><span class="sxs-lookup"><span data-stu-id="8e13b-387">**Date**</span></span>
  - <span data-ttu-id="8e13b-388">**Emplacement**</span><span class="sxs-lookup"><span data-stu-id="8e13b-388">**Location**</span></span>
  - <span data-ttu-id="8e13b-389">**Dirigé par**</span><span class="sxs-lookup"><span data-stu-id="8e13b-389">**Directed by**</span></span>
  - <span data-ttu-id="8e13b-390">**Nom du programme malveillant**</span><span class="sxs-lookup"><span data-stu-id="8e13b-390">**Malware name**</span></span>

  <span data-ttu-id="8e13b-391">Si vous cliquez sur **Filtres** dans cet affichage, vous pouvez modifier le rapport par **date** de début et **de fin,** ainsi que la **valeur de** détection.</span><span class="sxs-lookup"><span data-stu-id="8e13b-391">If you click **Filters** in this view, you can modify the report by **Start date** and **End date**, and the **Detection** value.</span></span>

- <span data-ttu-id="8e13b-392">**Afficher les données par : Remplacement de message**:</span><span class="sxs-lookup"><span data-stu-id="8e13b-392">**View data by: Message Override**:</span></span>

  - <span data-ttu-id="8e13b-393">**Date**</span><span class="sxs-lookup"><span data-stu-id="8e13b-393">**Date**</span></span>
  - <span data-ttu-id="8e13b-394">**Subject**</span><span class="sxs-lookup"><span data-stu-id="8e13b-394">**Subject**</span></span>
  - <span data-ttu-id="8e13b-395">**Expéditeur**</span><span class="sxs-lookup"><span data-stu-id="8e13b-395">**Sender**</span></span>
  - <span data-ttu-id="8e13b-396">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="8e13b-396">**Recipients**</span></span>
  - <span data-ttu-id="8e13b-397">**Détecté par**</span><span class="sxs-lookup"><span data-stu-id="8e13b-397">**Detected by**</span></span>
  - <span data-ttu-id="8e13b-398">**Override Reason**</span><span class="sxs-lookup"><span data-stu-id="8e13b-398">**Override Reason**</span></span>
  - <span data-ttu-id="8e13b-399">**Source de compromis**</span><span class="sxs-lookup"><span data-stu-id="8e13b-399">**Source of Compromise**</span></span>
  - <span data-ttu-id="8e13b-400">**Tags**</span><span class="sxs-lookup"><span data-stu-id="8e13b-400">**Tags**</span></span>

  <span data-ttu-id="8e13b-401">Si vous cliquez **sur Filtres** dans cet affichage, vous pouvez modifier le rapport avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="8e13b-401">If you click **Filters** in this view, you can modify the report with the following filters:</span></span>

  - <span data-ttu-id="8e13b-402">**Date de début et** **date de fin**</span><span class="sxs-lookup"><span data-stu-id="8e13b-402">**Start date** and **End date**</span></span>
  - <span data-ttu-id="8e13b-403">**Override Reason**</span><span class="sxs-lookup"><span data-stu-id="8e13b-403">**Override Reason**</span></span>
  - <span data-ttu-id="8e13b-404">**Balise**: filtrer les résultats par utilisateurs ou groupes pour lesquels la balise utilisateur spécifiée a été appliquée (y compris les comptes de priorité).</span><span class="sxs-lookup"><span data-stu-id="8e13b-404">**Tag**: Filter the results by users or groups that have had the specified user tag applied (including priority accounts).</span></span> <span data-ttu-id="8e13b-405">Pour plus d’informations sur les balises utilisateur, voir [Balises utilisateur.](user-tags.md)</span><span class="sxs-lookup"><span data-stu-id="8e13b-405">For more information about user tags, see [User tags](user-tags.md).</span></span>
  - <span data-ttu-id="8e13b-406">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8e13b-406">**Domain**</span></span>
  - <span data-ttu-id="8e13b-407">**Destinataires** (notez que cette propriété filtrable est disponible uniquement dans l’affichage Tableau des détails)</span><span class="sxs-lookup"><span data-stu-id="8e13b-407">**Recipients** (Note that this filterable property is only available in the details table view)</span></span>

- <span data-ttu-id="8e13b-408">Tous les autres graphiques :</span><span class="sxs-lookup"><span data-stu-id="8e13b-408">All other charts:</span></span>

  - <span data-ttu-id="8e13b-409">**Date**</span><span class="sxs-lookup"><span data-stu-id="8e13b-409">**Date**</span></span>
  - <span data-ttu-id="8e13b-410">**Subject**</span><span class="sxs-lookup"><span data-stu-id="8e13b-410">**Subject**</span></span>
  - <span data-ttu-id="8e13b-411">**Expéditeur**</span><span class="sxs-lookup"><span data-stu-id="8e13b-411">**Sender**</span></span>
  - <span data-ttu-id="8e13b-412">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="8e13b-412">**Recipients**</span></span>
  - <span data-ttu-id="8e13b-413">**Détecté par**</span><span class="sxs-lookup"><span data-stu-id="8e13b-413">**Detected by**</span></span>
  - <span data-ttu-id="8e13b-414">**État de remise**</span><span class="sxs-lookup"><span data-stu-id="8e13b-414">**Delivery Status**</span></span>
  - <span data-ttu-id="8e13b-415">**Source de compromis**</span><span class="sxs-lookup"><span data-stu-id="8e13b-415">**Source of Compromise**</span></span>
  - <span data-ttu-id="8e13b-416">**Tags**</span><span class="sxs-lookup"><span data-stu-id="8e13b-416">**Tags**</span></span>

  <span data-ttu-id="8e13b-417">Si vous cliquez **sur Filtres,** vous pouvez modifier le rapport avec les filtres suivants :</span><span class="sxs-lookup"><span data-stu-id="8e13b-417">If you click **Filters**, you can modify the report with the following filters:</span></span>

  - <span data-ttu-id="8e13b-418">**Date de début et** **date de fin**</span><span class="sxs-lookup"><span data-stu-id="8e13b-418">**Start date** and **End date**</span></span>
  - <span data-ttu-id="8e13b-419">**Détection**</span><span class="sxs-lookup"><span data-stu-id="8e13b-419">**Detection**</span></span>
  - <span data-ttu-id="8e13b-420">**Protégé par**: **Defender pour Office 365** ou **EOP**</span><span class="sxs-lookup"><span data-stu-id="8e13b-420">**Protected by**: **Defender for Office 365** or **EOP**</span></span>
  - <span data-ttu-id="8e13b-421">**Balise**: filtrer les résultats par utilisateurs ou groupes pour lesquels la balise utilisateur spécifiée a été appliquée (y compris les comptes de priorité).</span><span class="sxs-lookup"><span data-stu-id="8e13b-421">**Tag**: Filter the results by users or groups that have had the specified user tag applied (including priority accounts).</span></span> <span data-ttu-id="8e13b-422">Pour plus d’informations sur les balises utilisateur, voir [Balises utilisateur.](user-tags.md)</span><span class="sxs-lookup"><span data-stu-id="8e13b-422">For more information about user tags, see [User tags](user-tags.md).</span></span>
  - <span data-ttu-id="8e13b-423">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="8e13b-423">**Domain**</span></span>
  - <span data-ttu-id="8e13b-424">**Destinataires** (notez que cette propriété filtrable est disponible uniquement dans l’affichage Tableau des détails)</span><span class="sxs-lookup"><span data-stu-id="8e13b-424">**Recipients** (Note that this filterable property is only available in the details table view)</span></span>

## <a name="top-malware-report"></a><span data-ttu-id="8e13b-425">Principaux rapports sur les programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="8e13b-425">Top malware report</span></span>

<span data-ttu-id="8e13b-426">Le **rapport des principaux programmes** malveillants présente les différents types de programmes malveillants détectés par la protection [anti-programme malveillant dans EOP.](anti-malware-protection.md)</span><span class="sxs-lookup"><span data-stu-id="8e13b-426">The **Top malware** report shows the various kinds of malware that was detected by [anti-malware protection in EOP](anti-malware-protection.md).</span></span>

<span data-ttu-id="8e13b-427">Pour afficher le rapport, ouvrez le portail  [Microsoft 365 Defender,](https://security.microsoft.com)allez à Rapports e-mail & collaboration e-mail & rapports de collaboration et cliquez sur Afficher les détails sous Principaux programmes \>  \>  **malveillants.** </span><span class="sxs-lookup"><span data-stu-id="8e13b-427">To view the report, open the [Microsoft 365 Defender portal](https://security.microsoft.com), go to **Reports** \> **Email & collaboration** \> **Email & collaboration reports** and click **View details** under **Top malware**.</span></span> <span data-ttu-id="8e13b-428">Pour aller directement dans le rapport, ouvrez <https://security.microsoft.com/reports/TopMalware> .</span><span class="sxs-lookup"><span data-stu-id="8e13b-428">To go directly to the report, open <https://security.microsoft.com/reports/TopMalware>.</span></span>

![Widget de programmes malveillants de premier niveau dans le tableau de bord Rapports](../../media/top-malware-report-widget.png)

<span data-ttu-id="8e13b-430">Lorsque vous pointez sur une souris dans le graphique en secteurs, vous pouvez voir le nom d’un type de programme malveillant et le nombre de messages détectés comme ayant ce programme malveillant.</span><span class="sxs-lookup"><span data-stu-id="8e13b-430">When you hover over a wedge in the pie chart, you can see the name of a kind of malware and how many messages were detected as having that malware.</span></span>

![Affichage du rapport sur les programmes malveillants le plus haut](../../media/top-malware-report-view.png)

<span data-ttu-id="8e13b-432">Si vous cliquez **sur Afficher le tableau des détails,** vous pouvez voir les détails suivants :</span><span class="sxs-lookup"><span data-stu-id="8e13b-432">If you click **View details table**, you can see the following details:</span></span>

- <span data-ttu-id="8e13b-433">**Principaux programmes malveillants**</span><span class="sxs-lookup"><span data-stu-id="8e13b-433">**Top malware**</span></span>
- <span data-ttu-id="8e13b-434">**Count**</span><span class="sxs-lookup"><span data-stu-id="8e13b-434">**Count**</span></span>

<span data-ttu-id="8e13b-435">Si vous cliquez sur **Filtres** dans l’affichage Rapport ou dans l’affichage Tableau détails, vous pouvez spécifier une plage de dates avec la **date** de début et la **date de fin.**</span><span class="sxs-lookup"><span data-stu-id="8e13b-435">If you click **Filters** in the report view or details table view, you can specify a date range with **Start date** and **End date**.</span></span>

## <a name="url-threat-protection-report"></a><span data-ttu-id="8e13b-436">Rapport sur la protection contre les menaces d’URL</span><span class="sxs-lookup"><span data-stu-id="8e13b-436">URL threat protection report</span></span>

<span data-ttu-id="8e13b-437">Le **rapport sur la protection contre les menaces d’URL** est disponible dans Microsoft Defender Office 365.</span><span class="sxs-lookup"><span data-stu-id="8e13b-437">The **URL threat protection report** is available in Microsoft Defender for Office 365.</span></span> <span data-ttu-id="8e13b-438">Pour plus d’informations, voir le rapport sur la [protection contre les menaces d’URL.](view-reports-for-mdo.md#url-threat-protection-report)</span><span class="sxs-lookup"><span data-stu-id="8e13b-438">For more information, see [URL threat protection report](view-reports-for-mdo.md#url-threat-protection-report).</span></span>

## <a name="user-reported-messages-report"></a><span data-ttu-id="8e13b-439">Rapport des messages signalés par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="8e13b-439">User reported messages report</span></span>

<span data-ttu-id="8e13b-440">Le rapport des **messages** signalés par l’utilisateur affiche des informations sur les messages électroniques que les utilisateurs ont signalés comme courrier indésirable, tentatives de hameçonnage ou courriers électroniques de qualité à l’aide du [add-in Signaler](enable-the-report-message-add-in.md) un message ou du module de signalement du hameçonnage. [](enable-the-report-phish-add-in.md)</span><span class="sxs-lookup"><span data-stu-id="8e13b-440">The **User reported messages** report shows information about email messages that users have reported as junk, phishing attempts, or good mail by using the [Report Message add-in](enable-the-report-message-add-in.md) or [The Report Phishing add-in](enable-the-report-phish-add-in.md).</span></span>

<span data-ttu-id="8e13b-441">Des détails sont disponibles pour chaque message, y compris la raison de la remise, une exception de stratégie de courrier indésirable ou une règle de flux de messagerie configurée pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8e13b-441">Details are available for each message, including the delivery reason, such a spam policy exception or mail flow rule configured for your organization.</span></span> <span data-ttu-id="8e13b-442">Pour afficher les détails, sélectionnez un élément dans la liste  des rapports utilisateur, puis affichez les informations sous les **onglets** Résumé et Détails.</span><span class="sxs-lookup"><span data-stu-id="8e13b-442">To view details, select an item in the user-reports list, and then view the information on the **Summary** and **Details** tabs.</span></span>

![Le rapport des messages signalés par l’utilisateur affiche les messages étiquetés comme courrier indésirable, non indésirable ou tentatives de hameçonnage.](../../media/ad5e9a3d-b833-419c-bcc9-3425d9604ead.png)

<span data-ttu-id="8e13b-444">Pour afficher ce rapport, dans le portail [Microsoft 365 Defender,](https://security.microsoft.com)go to **Reports** \> **Email & collaboration** Email & collaboration \> **reports** User \> **reported messages**.</span><span class="sxs-lookup"><span data-stu-id="8e13b-444">To view this report, in the [Microsoft 365 Defender portal](https://security.microsoft.com), go to **Reports** \> **Email & collaboration** \>**Email & collaboration reports** \> **User reported messages**.</span></span>

- <span data-ttu-id="8e13b-445">Go to **Reports** \> **Email & collaboration** Email & collaboration \> **reports** User \> **reported messages**.</span><span class="sxs-lookup"><span data-stu-id="8e13b-445">Go to **Reports** \> **Email & collaboration** \> **Email & collaboration reports** \> **User reported messages**.</span></span>

![In the Microsoft 365 Defender portal, choose Reports \> Email & collaboration Email & collaboration reports User reported \> \> messages](../../media/user-reported-messages.png)

> [!IMPORTANT]
> <span data-ttu-id="8e13b-447">Pour que le rapport des messages signalés par l’utilisateur fonctionne correctement, l’enregistrement **d’audit** doit être Office 365 votre environnement.</span><span class="sxs-lookup"><span data-stu-id="8e13b-447">In order for the User reported messages report to work correctly, **audit logging must be turned on** for your Office 365 environment.</span></span> <span data-ttu-id="8e13b-448">Cette tâche est généralement effectuée par une personne dont le rôle Journaux d’audit est Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="8e13b-448">This is typically done by someone who has the Audit Logs role assigned in Exchange Online.</span></span> <span data-ttu-id="8e13b-449">Pour plus d’informations, [voir Turn Microsoft 365 audit log search on or off](../../compliance/turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="8e13b-449">For more information, see [Turn Microsoft 365 audit log search on or off](../../compliance/turn-audit-log-search-on-or-off.md).</span></span>

## <a name="what-permissions-are-needed-to-view-these-reports"></a><span data-ttu-id="8e13b-450">Quelles autorisations sont nécessaires pour afficher ces rapports ?</span><span class="sxs-lookup"><span data-stu-id="8e13b-450">What permissions are needed to view these reports?</span></span>

<span data-ttu-id="8e13b-451">Pour afficher et utiliser les rapports décrits dans cet article, vous devez être membre de l’un des groupes de rôles suivants dans le portail Microsoft 365 Defender :</span><span class="sxs-lookup"><span data-stu-id="8e13b-451">In order to view and use the reports described in this article, you need to be a member of one of the following role groups in the Microsoft 365 Defender portal:</span></span>

- <span data-ttu-id="8e13b-452">**Gestion de l'organisation**</span><span class="sxs-lookup"><span data-stu-id="8e13b-452">**Organization Management**</span></span>
- <span data-ttu-id="8e13b-453">**Administrateur de sécurité**</span><span class="sxs-lookup"><span data-stu-id="8e13b-453">**Security Administrator**</span></span>
- <span data-ttu-id="8e13b-454">**Lecteur sécurité**</span><span class="sxs-lookup"><span data-stu-id="8e13b-454">**Security Reader**</span></span>
- <span data-ttu-id="8e13b-455">**Lecteur global**</span><span class="sxs-lookup"><span data-stu-id="8e13b-455">**Global Reader**</span></span>

<span data-ttu-id="8e13b-456">Pour plus d’informations, [voir Autorisations dans le portail Microsoft 365 Defender.](permissions-in-the-security-and-compliance-center.md)</span><span class="sxs-lookup"><span data-stu-id="8e13b-456">For more information, see [Permissions in the Microsoft 365 Defender portal](permissions-in-the-security-and-compliance-center.md).</span></span>

<span data-ttu-id="8e13b-457">Remarque : l’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne  aux utilisateurs les autorisations requises dans le portail Microsoft 365 Defender et les autorisations pour d’autres fonctionnalités dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="8e13b-457">**Note**: Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions in the Microsoft 365 Defender portal _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="8e13b-458">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="8e13b-458">For more information, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>

## <a name="what-if-the-reports-arent-showing-data"></a><span data-ttu-id="8e13b-459">Que se passe-t-il si les rapports n’affichent pas de données ?</span><span class="sxs-lookup"><span data-stu-id="8e13b-459">What if the reports aren't showing data?</span></span>

<span data-ttu-id="8e13b-460">Si vous ne voyez pas de données dans vos rapports, vérifiez que vos stratégies sont correctement définies.</span><span class="sxs-lookup"><span data-stu-id="8e13b-460">If you are not seeing data in your reports, double-check that your policies are set up correctly.</span></span> <span data-ttu-id="8e13b-461">Pour en savoir plus, [consultez La protection contre les menaces.](protect-against-threats.md)</span><span class="sxs-lookup"><span data-stu-id="8e13b-461">To learn more, see [Protect against threats](protect-against-threats.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e13b-462">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e13b-462">Related topics</span></span>

[<span data-ttu-id="8e13b-463">Protection contre le courrier indésirable et les programmes malveillants dans EOP</span><span class="sxs-lookup"><span data-stu-id="8e13b-463">Anti-spam and anti-malware protection in EOP</span></span>](anti-spam-and-anti-malware-protection.md)

[<span data-ttu-id="8e13b-464">Rapports intelligents et informations sur le portail Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8e13b-464">Smart reports and insights in the Microsoft 365 Defender portal</span></span>](reports-and-insights-in-security-and-compliance.md)

[<span data-ttu-id="8e13b-465">Afficher les rapports de flux de messagerie dans le portail Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8e13b-465">View mail flow reports in the Microsoft 365 Defender portal</span></span>](view-mail-flow-reports.md)

[<span data-ttu-id="8e13b-466">Afficher des rapports pour Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="8e13b-466">View reports for Defender for Office 365</span></span>](view-reports-for-mdo.md)
