---
title: Afficher les rapports de Defender pour Office 365
f1.keywords:
- CSH
ms.author: tracyp
author: msfttracyp
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: conceptual
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e47e838c-d99e-4c0b-b9aa-e66c4fae902f
ms.collection:
- M365-security-compliance
- m365initiative-defender-office365
description: Les administrateurs peuvent découvrir comment rechercher et utiliser les rapports Defender for Office 365 disponibles dans le portail Microsoft 365 Defender web.
ms.custom: seo-marvel-apr2020
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: f7eab856f22ac1c2282e83897db6e3f93d4d97e6
ms.sourcegitcommit: cd55fe6abe25b1e4f5fbe8295d3a99aebd97ce66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53083511"
---
# <a name="view-defender-for-office-365-reports-in-the-microsoft-365-defender-portal"></a><span data-ttu-id="1fd48-103">Afficher les rapports defender pour Office 365 dans le portail Microsoft 365 Defender web</span><span class="sxs-lookup"><span data-stu-id="1fd48-103">View Defender for Office 365 reports in the Microsoft 365 Defender portal</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="1fd48-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="1fd48-104">**Applies to**</span></span>
- [<span data-ttu-id="1fd48-105">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="1fd48-105">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="1fd48-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="1fd48-106">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="1fd48-107">Les organisations Microsoft Defender pour Office 365 (par exemple, les abonnements Microsoft 365 E5 ou Microsoft Defender pour Office 365 Plan 1 ou Microsoft Defender pour les modules de développement Office 365 Plan 2) contiennent de nombreux rapports de sécurité.</span><span class="sxs-lookup"><span data-stu-id="1fd48-107">Microsoft Defender for Office 365 organizations (for example, Microsoft 365 E5 subscriptions or Microsoft Defender for Office 365 Plan 1 or Microsoft Defender for Office 365 Plan 2 add-ons) contain a variety of security-related reports.</span></span> <span data-ttu-id="1fd48-108">Si vous avez les [autorisations](#what-permissions-are-needed-to-view-the-defender-for-office-365-reports)nécessaires, vous pouvez afficher ces  rapports dans le portail Microsoft 365 Defender en allant à Rapports e-mail & \> **collaboration** \> **e-mail & rapports de collaboration.**</span><span class="sxs-lookup"><span data-stu-id="1fd48-108">If you have the [necessary permissions](#what-permissions-are-needed-to-view-the-defender-for-office-365-reports), you can view these reports in the Microsoft 365 Defender portal by going to **Reports** \> **Email & collaboration** \> **Email & collaboration reports**.</span></span> <span data-ttu-id="1fd48-109">Pour aller directement à la page **e-mail & rapports** de collaboration, ouvrez <https://security.microsoft.com/emailandcollabreport> .</span><span class="sxs-lookup"><span data-stu-id="1fd48-109">To go directly to the **Email & collaboration reports** page, open <https://security.microsoft.com/emailandcollabreport>.</span></span>

![Page de & de collaboration par courrier électronique dans le portail Microsoft 365 Defender web](../../media/email-collaboration-reports.png)

> [!NOTE]
>
> <span data-ttu-id="1fd48-111">Les rapports de sécurité de messagerie qui ne nécessitent pas Defender pour Office 365 sont décrits dans l’affichage des rapports de sécurité de messagerie dans [le portail Microsoft 365 Defender messagerie.](view-email-security-reports.md)</span><span class="sxs-lookup"><span data-stu-id="1fd48-111">Email security reports that don't require Defender for Office 365 are described in [View email security reports in the Microsoft 365 Defender portal](view-email-security-reports.md).</span></span>
>
> <span data-ttu-id="1fd48-112">Les rapports liés au flux de messagerie sont désormais dans le Centre d’administration Exchange(EAC).</span><span class="sxs-lookup"><span data-stu-id="1fd48-112">Reports that are related to mail flow are now in the Exchange admin center (EAC).</span></span> <span data-ttu-id="1fd48-113">Pour plus d’informations sur ces rapports, voir Rapports de flux de messagerie dans le nouveau [centre d Exchange’administration.](/exchange/monitoring/mail-flow-reports/mail-flow-reports)</span><span class="sxs-lookup"><span data-stu-id="1fd48-113">For more information about these reports, see [Mail flow reports in the new Exchange admin center](/exchange/monitoring/mail-flow-reports/mail-flow-reports).</span></span>

## <a name="safe-attachments-file-types-report"></a><span data-ttu-id="1fd48-114">Coffre Rapport sur les types de fichiers de pièces jointes</span><span class="sxs-lookup"><span data-stu-id="1fd48-114">Safe Attachments file types report</span></span>

> [!NOTE]
> <span data-ttu-id="1fd48-115">Le **rapport Coffre types de fichiers pièces jointes** sera finalement absent.</span><span class="sxs-lookup"><span data-stu-id="1fd48-115">The **Safe Attachments file types report** will eventually go away.</span></span> <span data-ttu-id="1fd48-116">Les mêmes informations sont disponibles dans le rapport d’état [de la protection contre les menaces.](#threat-protection-status-report)</span><span class="sxs-lookup"><span data-stu-id="1fd48-116">The same information is available in the [Threat protection status report](#threat-protection-status-report).</span></span>

## <a name="safe-attachments-message-disposition-report"></a><span data-ttu-id="1fd48-117">Coffre Rapport de disposition des messages de pièces jointes</span><span class="sxs-lookup"><span data-stu-id="1fd48-117">Safe Attachments message disposition report</span></span>

> [!NOTE]
> <span data-ttu-id="1fd48-118">Le Coffre de disposition des messages de pièces **jointes** sera finalement absent.</span><span class="sxs-lookup"><span data-stu-id="1fd48-118">The **Safe Attachments message disposition report** will eventually go away.</span></span> <span data-ttu-id="1fd48-119">Les mêmes informations sont disponibles dans le rapport d’état [de la protection contre les menaces.](#threat-protection-status-report)</span><span class="sxs-lookup"><span data-stu-id="1fd48-119">The same information is available in the [Threat protection status report](#threat-protection-status-report).</span></span>

## <a name="mail-latency-report"></a><span data-ttu-id="1fd48-120">Rapport de latence du courrier</span><span class="sxs-lookup"><span data-stu-id="1fd48-120">Mail latency report</span></span>

<span data-ttu-id="1fd48-121">Le **rapport de latence de messagerie** vous présente une vue agrégée de la latence de remise et de détonation du courrier au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1fd48-121">The **Mail latency report** shows you an aggregate view of the mail delivery and detonation latency experienced within your organization.</span></span> <span data-ttu-id="1fd48-122">Les délais de remise du courrier dans le service sont affectés par un certain nombre de facteurs, et le temps de remise absolu en secondes n’est souvent pas un bon indicateur de réussite ou un problème.</span><span class="sxs-lookup"><span data-stu-id="1fd48-122">Mail delivery times in the service are affected by a number of factors, and the absolute delivery time in seconds is often not a good indicator of success or a problem.</span></span> <span data-ttu-id="1fd48-123">Un délai de remise lent d’un jour peut être considéré comme un délai de livraison moyen un autre jour, ou inversement.</span><span class="sxs-lookup"><span data-stu-id="1fd48-123">A slow delivery time on one day might be considered an average delivery time on another day, or vice-versa.</span></span> <span data-ttu-id="1fd48-124">Cela tente de qualifier la remise des messages en fonction de données statistiques sur les temps de remise observés d’autres messages.</span><span class="sxs-lookup"><span data-stu-id="1fd48-124">This tries to qualify message delivery based on statistical data about the observed delivery times of other messages.</span></span>

<span data-ttu-id="1fd48-125">La latence côté client et réseau n’est pas incluse.</span><span class="sxs-lookup"><span data-stu-id="1fd48-125">Client side and network latency are not included.</span></span>

<span data-ttu-id="1fd48-126">Pour afficher le rapport, ouvrez [le portail Microsoft 365 Defender,](https://security.microsoft.com)allez à Rapports e-mail &  \> **collaboration** \> **e-mail & rapports de collaboration.**</span><span class="sxs-lookup"><span data-stu-id="1fd48-126">To view the report, open the [Microsoft 365 Defender portal](https://security.microsoft.com), go to **Reports** \> **Email & collaboration** \> **Email & collaboration reports**.</span></span> <span data-ttu-id="1fd48-127">Dans la page **Rapports de collaboration &** courrier électronique, recherchez le rapport de latence de **messagerie,** puis cliquez sur **Afficher les détails.**</span><span class="sxs-lookup"><span data-stu-id="1fd48-127">On the **Email & collaboration reports** page, find **Mail latency report** and then click **View details**.</span></span> <span data-ttu-id="1fd48-128">Pour aller directement dans le rapport, ouvrez <https://security.microsoft.com/mailLatencyReport> .</span><span class="sxs-lookup"><span data-stu-id="1fd48-128">To go directly to the report, open <https://security.microsoft.com/mailLatencyReport>.</span></span>

![Widget de rapport de latence de messagerie sur la page rapports de collaboration & courrier électronique](../../media/mail-latency-report-widget.png)

<span data-ttu-id="1fd48-130">Dans la page **Rapport de latence de messagerie,** les onglets suivants sont disponibles dans la page Rapport de **latence de messagerie** :</span><span class="sxs-lookup"><span data-stu-id="1fd48-130">On the **Mail latency report** page, the following tabs are available on the **Mail latency report** page:</span></span>

- <span data-ttu-id="1fd48-131">**50e centile**: il s’agit du milieu pour les heures de remise des messages.</span><span class="sxs-lookup"><span data-stu-id="1fd48-131">**50th percentile**: This is the middle for message delivery times.</span></span> <span data-ttu-id="1fd48-132">Vous pouvez considérer cette valeur comme un délai de livraison moyen.</span><span class="sxs-lookup"><span data-stu-id="1fd48-132">You can consider this value as an average delivery time.</span></span> <span data-ttu-id="1fd48-133">Cet onglet est sélectionné par défaut.</span><span class="sxs-lookup"><span data-stu-id="1fd48-133">This tab is selected by default.</span></span>
- <span data-ttu-id="1fd48-134">**90e centile**: cela indique une latence élevée pour la remise des messages.</span><span class="sxs-lookup"><span data-stu-id="1fd48-134">**90th percentile**: This indicates a high latency for message delivery.</span></span> <span data-ttu-id="1fd48-135">Seuls 10 % des messages ont mis plus de temps que cette valeur à remettre.</span><span class="sxs-lookup"><span data-stu-id="1fd48-135">Only 10% of messages took longer than this value to deliver.</span></span>
- <span data-ttu-id="1fd48-136">**99e centile**: cela indique la latence la plus élevée pour la remise des messages.</span><span class="sxs-lookup"><span data-stu-id="1fd48-136">**99th percentile**: This indicates the highest latency for message delivery.</span></span>

<span data-ttu-id="1fd48-137">Quel que soit l’onglet que vous sélectionnez, le graphique affiche les messages organisés dans les catégories suivantes :</span><span class="sxs-lookup"><span data-stu-id="1fd48-137">Regardless of the tab you select, the chart shows messages organized into the following categories:</span></span>

- <span data-ttu-id="1fd48-138">**Latence de remise des messages**</span><span class="sxs-lookup"><span data-stu-id="1fd48-138">**Mail delivery latency**</span></span>
- <span data-ttu-id="1fd48-139">**Détonations**</span><span class="sxs-lookup"><span data-stu-id="1fd48-139">**Detonations**</span></span>

<span data-ttu-id="1fd48-140">Lorsque vous pointez sur une catégorie dans le graphique, vous pouvez voir une répartition de la latence dans chaque catégorie.</span><span class="sxs-lookup"><span data-stu-id="1fd48-140">When you hover over a category in the chart, you can see a breakdown of the latency in each category.</span></span>

![50e affichage des centiles du rapport de latence de messagerie](../../media/mail-latency-report-50th-percentile-view.png)

<span data-ttu-id="1fd48-142">Si vous cliquez **sur Filtre,** vous pouvez filtrer à la fois le graphique et le tableau de détails selon les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="1fd48-142">If you click **Filter**, you can filter both the chart and the details table by the following values:</span></span>

- <span data-ttu-id="1fd48-143">**Date (UTC)**: **date de début et date** de **fin**</span><span class="sxs-lookup"><span data-stu-id="1fd48-143">**Date (UTC)**: **Start date** and **End date**</span></span>
- <span data-ttu-id="1fd48-144">**Affichage des messages**: l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="1fd48-144">**Message view**: One of the following values:</span></span>
  - <span data-ttu-id="1fd48-145">**Tous les messages**</span><span class="sxs-lookup"><span data-stu-id="1fd48-145">**All messages**</span></span>
  - <span data-ttu-id="1fd48-146">**Messages contenant des pièces jointes ou des URL**</span><span class="sxs-lookup"><span data-stu-id="1fd48-146">**Messages that contain attachments or URLs**</span></span>
  - <span data-ttu-id="1fd48-147">**Messages détonés**</span><span class="sxs-lookup"><span data-stu-id="1fd48-147">**Detonated messages**</span></span>

<span data-ttu-id="1fd48-148">Lorsque vous avez terminé la configuration des filtres, cliquez sur **Appliquer,** **Annuler** ou **Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="1fd48-148">When you're finished configuring the filters, click **Apply**, **Cancel**, or **Clear filters**.</span></span>

<span data-ttu-id="1fd48-149">Dans le tableau de détails sous le graphique, les informations suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="1fd48-149">In the details table below the chart, the following information is available:</span></span>

- <span data-ttu-id="1fd48-150">**Date (UTC)**</span><span class="sxs-lookup"><span data-stu-id="1fd48-150">**Date (UTC)**</span></span>
- <span data-ttu-id="1fd48-151">**Percentiles**: **50,** **90** ou **99**</span><span class="sxs-lookup"><span data-stu-id="1fd48-151">**Percentiles**: **50**, **90**, or **99**</span></span>
- <span data-ttu-id="1fd48-152">**Nombre de messages**</span><span class="sxs-lookup"><span data-stu-id="1fd48-152">**Message count**</span></span>
- <span data-ttu-id="1fd48-153">**Latence globale**</span><span class="sxs-lookup"><span data-stu-id="1fd48-153">**Overall latency**</span></span>

## <a name="threat-protection-status-report"></a><span data-ttu-id="1fd48-154">Rapport sur l’état de la protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="1fd48-154">Threat protection status report</span></span>

<span data-ttu-id="1fd48-155">Le rapport d’état **de la protection** contre les menaces est un affichage unique qui regroupe des informations sur le contenu malveillant et les e-mails malveillants détectés et bloqués par [Exchange Online Protection](exchange-online-protection-overview.md) (EOP) et Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="1fd48-155">The **Threat protection status** report is a single view that brings together information about malicious content and malicious email detected and blocked by [Exchange Online Protection](exchange-online-protection-overview.md) (EOP) and Microsoft Defender for Office 365.</span></span> <span data-ttu-id="1fd48-156">Pour plus d’informations, consultez [le rapport d’état de la protection contre les menaces.](view-email-security-reports.md#threat-protection-status-report)</span><span class="sxs-lookup"><span data-stu-id="1fd48-156">For more information, see [Threat protection status report](view-email-security-reports.md#threat-protection-status-report).</span></span>

## <a name="url-threat-protection-report"></a><span data-ttu-id="1fd48-157">Rapport sur la protection contre les menaces d’URL</span><span class="sxs-lookup"><span data-stu-id="1fd48-157">URL threat protection report</span></span>

<span data-ttu-id="1fd48-158">Le **rapport sur la protection contre** les menaces d’URL fournit des affichages récapitulatifs et des tendances pour les menaces détectées et les actions entreprises sur les clics d’URL dans le cadre [Coffre liens.](safe-links.md)</span><span class="sxs-lookup"><span data-stu-id="1fd48-158">The **URL threat protection report** provides summary and trend views for threats detected and actions taken on URL clicks as part of [Safe Links](safe-links.md).</span></span> <span data-ttu-id="1fd48-159">Ce rapport ne dispose pas des données de clic des utilisateurs pour lequel l’option Ne pas suivre les **clics** utilisateur est sélectionnée pour la stratégie de liens Coffre appliquée.</span><span class="sxs-lookup"><span data-stu-id="1fd48-159">This report will not have click data from users where the Safe Links policy applied has the **Do not track user clicks** option selected.</span></span>

<span data-ttu-id="1fd48-160">Pour afficher le rapport, ouvrez [le portail Microsoft 365 Defender,](https://security.microsoft.com)allez à Rapports e-mail &  \> **collaboration** \> **e-mail & rapports de collaboration.**</span><span class="sxs-lookup"><span data-stu-id="1fd48-160">To view the report, open the [Microsoft 365 Defender portal](https://security.microsoft.com), go to **Reports** \> **Email & collaboration** \> **Email & collaboration reports**.</span></span> <span data-ttu-id="1fd48-161">Dans la page **Rapports de collaboration & courrier** électronique, recherchez la page protection des **URL,** puis cliquez sur **Afficher les détails.**</span><span class="sxs-lookup"><span data-stu-id="1fd48-161">On the **Email & collaboration reports** page, find **URL protection page** and then click **View details**.</span></span> <span data-ttu-id="1fd48-162">Pour aller directement dans le rapport, ouvrez <https://security.microsoft.com/reports/URLProtectionActionReport> .</span><span class="sxs-lookup"><span data-stu-id="1fd48-162">To go directly to the report, open <https://security.microsoft.com/reports/URLProtectionActionReport>.</span></span>

![Widget de rapport sur la protection des URL dans la page Rapports de collaboration & courrier électronique](../../media/url-protection-report-widget.png)

<span data-ttu-id="1fd48-164">Les vues disponibles sur la page du rapport sur la protection contre les menaces **d’URL** sont décrites dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="1fd48-164">The available views on the **URL threat protection** report page are described in the following sections.</span></span>

> [!NOTE]
> <span data-ttu-id="1fd48-165">Il s’agit *d’un rapport de tendance de protection,* ce qui signifie que les données représentent des tendances dans un jeu de données plus important.</span><span class="sxs-lookup"><span data-stu-id="1fd48-165">This is a *protection trend report*, meaning data represents trends in a larger dataset.</span></span> <span data-ttu-id="1fd48-166">Par conséquent, les données des graphiques ne sont pas disponibles en temps réel ici, mais les données du tableau de détails le sont, de sorte que vous pouvez voir une légère différence entre les deux.</span><span class="sxs-lookup"><span data-stu-id="1fd48-166">As a result, the data in the charts is not available in real time here, but the data in the details table is, so you may see a slight discrepancy between the two.</span></span> <span data-ttu-id="1fd48-167">Les graphiques sont actualisé toutes les quatre heures et contiennent des données pour les 90 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="1fd48-167">The charts are refreshed once every four hours and contain data for the last 90 days.</span></span>

### <a name="view-data-by-url-click-protection-action"></a><span data-ttu-id="1fd48-168">Afficher les données par action de protection par clic d’URL</span><span class="sxs-lookup"><span data-stu-id="1fd48-168">View data by URL click protection action</span></span>

![Url click protection action view in the URL threat protection report](../../media/url-threat-protection-report-url-click-protection-action-view.png)

<span data-ttu-id="1fd48-170">**L’affichage des données par url de l’action de protection** par clic affiche le nombre de clics d’URL par les utilisateurs de l’organisation et les résultats du clic :</span><span class="sxs-lookup"><span data-stu-id="1fd48-170">The **View data by URL click protection action** view shows the number of URL clicks by users in the organization and the results of the click:</span></span>

- <span data-ttu-id="1fd48-171">**Autorisé**: l’utilisateur a été autorisé à accéder à l’URL.</span><span class="sxs-lookup"><span data-stu-id="1fd48-171">**Allowed**: The user was allowed to navigate to the URL.</span></span>
- <span data-ttu-id="1fd48-172">**Bloqué**: l’accès à l’URL a été bloqué pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1fd48-172">**Blocked**: The user was blocked from navigating to the URL.</span></span>
- <span data-ttu-id="1fd48-173">**Bloqué et cliqué :** l’utilisateur a choisi de continuer à accéder à l’URL.</span><span class="sxs-lookup"><span data-stu-id="1fd48-173">**Blocked and clicked through**: The user has chosen to continue navigating to the URL.</span></span>
- <span data-ttu-id="1fd48-174">**Clicked through during scan**: The user has clicked on the link before the scan was complete.</span><span class="sxs-lookup"><span data-stu-id="1fd48-174">**Clicked through during scan**: The user has clicked on the link before the scan was complete.</span></span>

<span data-ttu-id="1fd48-175">Un clic indique que l’utilisateur a cliqué sur la page d’accès au site web malveillant (les administrateurs peuvent désactiver le clic dans les stratégies de liens Coffre web).</span><span class="sxs-lookup"><span data-stu-id="1fd48-175">A click indicates that the user has clicked through the block page to the malicious website (admins can disable click through in Safe Links policies).</span></span>

<span data-ttu-id="1fd48-176">Si vous cliquez sur **Filtres,** vous pouvez modifier le rapport et le tableau des détails en sélectionnant une ou plusieurs des valeurs suivantes dans le volant qui s’affiche :</span><span class="sxs-lookup"><span data-stu-id="1fd48-176">If you click **Filters**, you can modify the report and the details table by selecting one or more of the following values in the flyout that appears:</span></span>

- <span data-ttu-id="1fd48-177">**Date (UTC)**: **date de début et date** de **fin**</span><span class="sxs-lookup"><span data-stu-id="1fd48-177">**Date (UTC)**: **Start date** and **End date**</span></span>
- <span data-ttu-id="1fd48-178">**Détection**:</span><span class="sxs-lookup"><span data-stu-id="1fd48-178">**Detection**:</span></span>
  - <span data-ttu-id="1fd48-179">**Autorisé**</span><span class="sxs-lookup"><span data-stu-id="1fd48-179">**Allowed**</span></span>
  - <span data-ttu-id="1fd48-180">**Bloqué**</span><span class="sxs-lookup"><span data-stu-id="1fd48-180">**Blocked**</span></span>
  - <span data-ttu-id="1fd48-181">**Bloqué et cliqué**</span><span class="sxs-lookup"><span data-stu-id="1fd48-181">**Blocked and clicked through**</span></span>
  - <span data-ttu-id="1fd48-182">**Clics au cours de l’analyse**</span><span class="sxs-lookup"><span data-stu-id="1fd48-182">**Clicked through during scan**</span></span>
- <span data-ttu-id="1fd48-183">**Domaines :** les domaines d’URL répertoriés dans les résultats du rapport.</span><span class="sxs-lookup"><span data-stu-id="1fd48-183">**Domains**: The URL domains listed in the report results.</span></span>
- <span data-ttu-id="1fd48-184">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="1fd48-184">**Recipients**</span></span>

<span data-ttu-id="1fd48-185">Lorsque vous avez terminé la configuration des filtres, cliquez sur **Appliquer,** **Annuler** ou **Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="1fd48-185">When you're finished configuring the filters, click **Apply**, **Cancel**, or **Clear filters**.</span></span>

<span data-ttu-id="1fd48-186">Le tableau de détails sous le graphique fournit l’affichage en temps quasi réel suivant de tous les clics qui se sont produit au sein de l’organisation au cours des 7 derniers jours :</span><span class="sxs-lookup"><span data-stu-id="1fd48-186">The details table below the chart provides the following near-real-time view of all clicks that happened within the organization for the last 7 days:</span></span>

- <span data-ttu-id="1fd48-187">**Temps de clic**</span><span class="sxs-lookup"><span data-stu-id="1fd48-187">**Click time**</span></span>
- <span data-ttu-id="1fd48-188">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="1fd48-188">**User**</span></span>
- <span data-ttu-id="1fd48-189">**URL**</span><span class="sxs-lookup"><span data-stu-id="1fd48-189">**URL**</span></span>
- <span data-ttu-id="1fd48-190">**Action**</span><span class="sxs-lookup"><span data-stu-id="1fd48-190">**Action**</span></span>
- <span data-ttu-id="1fd48-191">**Application**</span><span class="sxs-lookup"><span data-stu-id="1fd48-191">**App**</span></span>

### <a name="view-data-by-url-click-by-application"></a><span data-ttu-id="1fd48-192">Afficher les données par URL en cliquant par application</span><span class="sxs-lookup"><span data-stu-id="1fd48-192">View data by URL click by application</span></span>

![Url click by application view in the URL threat protection report](../../media/url-threat-protection-report-url-click-by-application-view.png)

<span data-ttu-id="1fd48-194">L’affichage des données par clic URL par **vue d’application** indique le nombre de clics d’URL par les applications qui Coffre liens :</span><span class="sxs-lookup"><span data-stu-id="1fd48-194">The **View data by URL click by application** view shows the number of URL clicks by apps that support Safe Links:</span></span>

- <span data-ttu-id="1fd48-195">**Client de messagerie**</span><span class="sxs-lookup"><span data-stu-id="1fd48-195">**Email client**</span></span>
- <span data-ttu-id="1fd48-196">**PowerPoint**</span><span class="sxs-lookup"><span data-stu-id="1fd48-196">**PowerPoint**</span></span>
- <span data-ttu-id="1fd48-197">**Word**</span><span class="sxs-lookup"><span data-stu-id="1fd48-197">**Word**</span></span>
- <span data-ttu-id="1fd48-198">**Excel**</span><span class="sxs-lookup"><span data-stu-id="1fd48-198">**Excel**</span></span>
- <span data-ttu-id="1fd48-199">**OneNote**</span><span class="sxs-lookup"><span data-stu-id="1fd48-199">**OneNote**</span></span>
- <span data-ttu-id="1fd48-200">**Visio**</span><span class="sxs-lookup"><span data-stu-id="1fd48-200">**Visio**</span></span>
- <span data-ttu-id="1fd48-201">**Teams**</span><span class="sxs-lookup"><span data-stu-id="1fd48-201">**Teams**</span></span>
- <span data-ttu-id="1fd48-202">**Autres**</span><span class="sxs-lookup"><span data-stu-id="1fd48-202">**Others**</span></span>

<span data-ttu-id="1fd48-203">Si vous cliquez sur **Filtres,** vous pouvez modifier le rapport et le tableau des détails en sélectionnant une ou plusieurs des valeurs suivantes dans le volant qui s’affiche :</span><span class="sxs-lookup"><span data-stu-id="1fd48-203">If you click **Filters**, you can modify the report and the details table by selecting one or more of the following values in the flyout that appears:</span></span>

- <span data-ttu-id="1fd48-204">**Date (UTC)**: **date de début et date** de **fin**</span><span class="sxs-lookup"><span data-stu-id="1fd48-204">**Date (UTC)**: **Start date** and **End date**</span></span>
- <span data-ttu-id="1fd48-205">**Détection**: applications disponibles dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="1fd48-205">**Detection**: Available apps from the chart.</span></span>
- <span data-ttu-id="1fd48-206">**Domaines :** les domaines d’URL répertoriés dans les résultats du rapport.</span><span class="sxs-lookup"><span data-stu-id="1fd48-206">**Domains**: The URL domains listed in the report results.</span></span>
- <span data-ttu-id="1fd48-207">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="1fd48-207">**Recipients**</span></span>

<span data-ttu-id="1fd48-208">Lorsque vous avez terminé la configuration des filtres, cliquez sur **Appliquer,** **Annuler** ou **Effacer les filtres.**</span><span class="sxs-lookup"><span data-stu-id="1fd48-208">When you're finished configuring the filters, click **Apply**, **Cancel**, or **Clear filters**.</span></span>

<span data-ttu-id="1fd48-209">Le tableau de détails sous le graphique fournit l’affichage en temps quasi réel suivant de tous les clics qui se sont produit au sein de l’organisation au cours des 7 derniers jours :</span><span class="sxs-lookup"><span data-stu-id="1fd48-209">The details table below the chart provides the following near-real-time view of all clicks that happened within the organization for the last 7 days:</span></span>

- <span data-ttu-id="1fd48-210">**Temps de clic**</span><span class="sxs-lookup"><span data-stu-id="1fd48-210">**Click time**</span></span>
- <span data-ttu-id="1fd48-211">**Utilisateur**</span><span class="sxs-lookup"><span data-stu-id="1fd48-211">**User**</span></span>
- <span data-ttu-id="1fd48-212">**URL**</span><span class="sxs-lookup"><span data-stu-id="1fd48-212">**URL**</span></span>
- <span data-ttu-id="1fd48-213">**Action**</span><span class="sxs-lookup"><span data-stu-id="1fd48-213">**Action**</span></span>
- <span data-ttu-id="1fd48-214">**Application**</span><span class="sxs-lookup"><span data-stu-id="1fd48-214">**App**</span></span>

## <a name="additional-reports-to-view"></a><span data-ttu-id="1fd48-215">Rapports supplémentaires à afficher</span><span class="sxs-lookup"><span data-stu-id="1fd48-215">Additional reports to view</span></span>

<span data-ttu-id="1fd48-216">Outre les rapports décrits dans cet article, plusieurs autres rapports sont disponibles, comme décrit dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="1fd48-216">In addition to the reports described in this article, several other reports are available, as described in the following table:</span></span>

<br>

****

|<span data-ttu-id="1fd48-217">Rapport</span><span class="sxs-lookup"><span data-stu-id="1fd48-217">Report</span></span>|<span data-ttu-id="1fd48-218">Rubrique</span><span class="sxs-lookup"><span data-stu-id="1fd48-218">Topic</span></span>|
|---|---|
|<span data-ttu-id="1fd48-219">**Explorateur** (Microsoft Defender pour Office 365 Plan 2) ou **détections** en temps réel (Microsoft Defender pour Office 365 Plan 1)</span><span class="sxs-lookup"><span data-stu-id="1fd48-219">**Explorer** (Microsoft Defender for Office 365 Plan 2) or **real-time detections** (Microsoft Defender for Office 365 Plan 1)</span></span>|[<span data-ttu-id="1fd48-220">Explorateur de menaces (et détections en temps réel)</span><span class="sxs-lookup"><span data-stu-id="1fd48-220">Threat Explorer (and real-time detections)</span></span>](threat-explorer.md)|
|<span data-ttu-id="1fd48-221">**Rapports de sécurité du** courrier électronique, tels que le rapport Sur les principaux expéditeurs et destinataires, le rapport sur les courriers électroniques usurpés et le rapport sur les détections de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="1fd48-221">**Email security reports**, such as the Top senders and recipients report, the Spoof mail report, and the Spam detections report.</span></span>|[<span data-ttu-id="1fd48-222">Afficher les rapports de sécurité de messagerie dans le portail Microsoft 365 Defender messagerie</span><span class="sxs-lookup"><span data-stu-id="1fd48-222">View email security reports in the Microsoft 365 Defender portal</span></span>](view-email-security-reports.md)|
|<span data-ttu-id="1fd48-223">**Les rapports de flux de** messagerie, tels que le rapport de forwarding, le rapport d’état du flux de messagerie et le rapport des principaux expéditeurs et destinataires.</span><span class="sxs-lookup"><span data-stu-id="1fd48-223">**Mail flow reports**, such as the Forwarding report, the Mailflow status report, and the Top senders and recipients report.</span></span>|[<span data-ttu-id="1fd48-224">Rapports de flux de messagerie dans le nouveau centre d Exchange’administration</span><span class="sxs-lookup"><span data-stu-id="1fd48-224">Mail flow reports in the new Exchange admin center</span></span>](/exchange/monitoring/mail-flow-reports/mail-flow-reports)|
|<span data-ttu-id="1fd48-225">**Suivi d’URL Coffre liens (PowerShell** uniquement).</span><span class="sxs-lookup"><span data-stu-id="1fd48-225">**URL trace for Safe Links** (PowerShell only).</span></span> <span data-ttu-id="1fd48-226">Le résultat de cette cmdlet affiche les résultats des actions Coffre liens au cours des sept derniers jours.</span><span class="sxs-lookup"><span data-stu-id="1fd48-226">The output of this cmdlet shows you the results of Safe Links actions over the past seven days.</span></span>|[<span data-ttu-id="1fd48-227">Get-UrlTrace</span><span class="sxs-lookup"><span data-stu-id="1fd48-227">Get-UrlTrace</span></span>](/powershell/module/exchange/get-urltrace)|
|<span data-ttu-id="1fd48-228">**Résultats du trafic de messagerie pour EOP et Microsoft Defender pour Office 365** (PowerShell uniquement).</span><span class="sxs-lookup"><span data-stu-id="1fd48-228">**Mail traffic results for EOP and Microsoft Defender for Office 365** (PowerShell only).</span></span> <span data-ttu-id="1fd48-229">La sortie de cette cmdlet contient des informations sur le domaine, la date, le type d’événement, la direction, l’action et le nombre de messages.</span><span class="sxs-lookup"><span data-stu-id="1fd48-229">The output of this cmdlet contains information about Domain, Date, Event Type, Direction, Action, and Message Count.</span></span>|[<span data-ttu-id="1fd48-230">Get-MailTrafficATPReport</span><span class="sxs-lookup"><span data-stu-id="1fd48-230">Get-MailTrafficATPReport</span></span>](/powershell/module/exchange/get-mailtrafficatpreport)|
|<span data-ttu-id="1fd48-231">**Rapports de détails de courrier pour EOP et Defender pour Office 365 détections de** courrier indésirable (PowerShell uniquement).</span><span class="sxs-lookup"><span data-stu-id="1fd48-231">**Mail detail reports for EOP and Defender for Office 365 detections** (PowerShell only).</span></span> <span data-ttu-id="1fd48-232">La sortie de cette cmdlet contient des détails sur les fichiers ou URL malveillants, les tentatives d’hameçonnage, l’emprunt d’identité et d’autres menaces potentielles dans les e-mails ou les fichiers.</span><span class="sxs-lookup"><span data-stu-id="1fd48-232">The output of this cmdlet contains details about malicious files or URLs, phishing attempts, impersonation, and other potential threats in email or files.</span></span>|[<span data-ttu-id="1fd48-233">Get-MailDetailATPReport</span><span class="sxs-lookup"><span data-stu-id="1fd48-233">Get-MailDetailATPReport</span></span>](/powershell/module/exchange/get-maildetailatpreport)|
|

## <a name="what-permissions-are-needed-to-view-the-defender-for-office-365-reports"></a><span data-ttu-id="1fd48-234">Quelles autorisations sont nécessaires pour afficher les rapports Defender for Office 365 ?</span><span class="sxs-lookup"><span data-stu-id="1fd48-234">What permissions are needed to view the Defender for Office 365 reports?</span></span>

<span data-ttu-id="1fd48-235">Pour afficher et utiliser les rapports décrits dans cet article, vous devez être membre de l’un des groupes de rôles suivants dans le portail Microsoft 365 Defender:</span><span class="sxs-lookup"><span data-stu-id="1fd48-235">In order to view and use the reports described in this article, you need to be a member of one of the following role groups in the Microsoft 365 Defender portal:</span></span>

- <span data-ttu-id="1fd48-236">**Gestion de l'organisation**</span><span class="sxs-lookup"><span data-stu-id="1fd48-236">**Organization Management**</span></span>
- <span data-ttu-id="1fd48-237">**Administrateur de sécurité**</span><span class="sxs-lookup"><span data-stu-id="1fd48-237">**Security Administrator**</span></span>
- <span data-ttu-id="1fd48-238">**Lecteur sécurité**</span><span class="sxs-lookup"><span data-stu-id="1fd48-238">**Security Reader**</span></span>
- <span data-ttu-id="1fd48-239">**Lecteur global**</span><span class="sxs-lookup"><span data-stu-id="1fd48-239">**Global Reader**</span></span>

<span data-ttu-id="1fd48-240">Pour plus d’informations, consultez [Autorisations dans le portail Microsoft 365 Defender](permissions-microsoft-365-security-center.md).</span><span class="sxs-lookup"><span data-stu-id="1fd48-240">For more information, see [Permissions in the Microsoft 365 Defender portal](permissions-microsoft-365-security-center.md).</span></span>

<span data-ttu-id="1fd48-241">**Remarque**: l’ajout d’utilisateurs au rôle Azure Active Directory correspondant dans le Centre d’administration Microsoft 365 donne aux  utilisateurs les autorisations requises dans le portail Microsoft 365 Defender et les autorisations pour d’autres fonctionnalités dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1fd48-241">**Note**: Adding users to the corresponding Azure Active Directory role in the Microsoft 365 admin center gives users the required permissions in the Microsoft 365 Defender portal _and_ permissions for other features in Microsoft 365.</span></span> <span data-ttu-id="1fd48-242">Pour plus d’informations, consultez [À propos des rôles d’administrateur](../../admin/add-users/about-admin-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1fd48-242">For more information, see [About admin roles](../../admin/add-users/about-admin-roles.md).</span></span>

## <a name="what-if-the-reports-arent-showing-data"></a><span data-ttu-id="1fd48-243">Que se passe-t-il si les rapports n’affichent pas de données ?</span><span class="sxs-lookup"><span data-stu-id="1fd48-243">What if the reports aren't showing data?</span></span>

<span data-ttu-id="1fd48-244">Si vous ne voyez pas de données dans votre defender pour Office 365 rapports, vérifiez que vos stratégies sont correctement définies.</span><span class="sxs-lookup"><span data-stu-id="1fd48-244">If you are not seeing data in your Defender for Office 365 reports, double-check that your policies are set up correctly.</span></span> <span data-ttu-id="1fd48-245">Votre organisation doit avoir défini [des stratégies Coffre](set-up-safe-links-policies.md) liens et des stratégies Coffre pièces [jointes](set-up-safe-attachments-policies.md) pour que Defender pour Office 365 protection soit en place.</span><span class="sxs-lookup"><span data-stu-id="1fd48-245">Your organization must have [Safe Links policies](set-up-safe-links-policies.md) and [Safe Attachments policies](set-up-safe-attachments-policies.md) defined in order for Defender for Office 365 protection to be in place.</span></span> <span data-ttu-id="1fd48-246">Consultez également La protection contre [le courrier indésirable et les programmes malveillants.](anti-spam-and-anti-malware-protection.md)</span><span class="sxs-lookup"><span data-stu-id="1fd48-246">Also see [Anti-spam and anti-malware protection](anti-spam-and-anti-malware-protection.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1fd48-247">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1fd48-247">Related topics</span></span>

[<span data-ttu-id="1fd48-248">Rapports intelligents et informations sur le portail Microsoft 365 Defender web</span><span class="sxs-lookup"><span data-stu-id="1fd48-248">Smart reports and insights in the Microsoft 365 Defender portal</span></span>](reports-and-insights-in-security-and-compliance.md)

[<span data-ttu-id="1fd48-249">Autorisations de rôle (Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="1fd48-249">Role permissions (Azure Active Directory</span></span>](/azure/active-directory/users-groups-roles/directory-assign-admin-roles#role-permissions)
