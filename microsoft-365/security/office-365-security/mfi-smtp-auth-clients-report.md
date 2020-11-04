---
title: Analyse des clients SMTP AUTH et rapports dans le tableau de bord de flux de messagerie
f1.keywords:
- NOCSH
ms.author: siosulli
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs peuvent apprendre à utiliser le rapport et l’analyseur d’authentification SMTP dans le tableau de bord de flux de messagerie dans le centre de sécurité & conformité afin de surveiller les expéditeurs de messages électroniques de leur organisation qui utilisent SMTP authentifié (authentification SMTP) pour envoyer des messages électroniques.
ms.openlocfilehash: 54798dfcad50c263705b027c879fdf71d0dabfba
ms.sourcegitcommit: b64f36d3873fa0041b24bec029deb73ccfdfdbac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48877560"
---
# <a name="smtp-auth-clients-insight-and-report-in-the-security--compliance-center"></a><span data-ttu-id="e85a4-103">Clients d’authentification SMTP Insight and report dans le centre de conformité & Security</span><span class="sxs-lookup"><span data-stu-id="e85a4-103">SMTP Auth clients insight and report in the Security & Compliance Center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="e85a4-104">Les **clients d’authentification SMTP** du [tableau de bord de flux de messagerie](mail-flow-insights-v2.md) et le [rapport clients SMTP AUTH](#smtp-auth-clients-report) associés dans le [Centre de conformité &](https://protection.office.com) mettent en surbrillance l’utilisation du protocole d’envoi de client SMTP AUTH par les utilisateurs ou les comptes système de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e85a4-104">The **SMTP Auth clients** insight in the [Mail flow dashboard](mail-flow-insights-v2.md) and the associated [SMTP Auth clients report](#smtp-auth-clients-report) in the [Security & Compliance Center](https://protection.office.com) highlight the use of the SMTP AUTH client submission protocol by users or system accounts in your organization.</span></span> <span data-ttu-id="e85a4-105">Ce protocole hérité (qui utilise le point de terminaison smtp.office365.com) offre uniquement l’authentification de base et est susceptible d’être utilisé par des comptes compromis pour envoyer des courriers électroniques.</span><span class="sxs-lookup"><span data-stu-id="e85a4-105">This legacy protocol (which uses the endpoint smtp.office365.com) only offers Basic authentication, and is susceptible to being used by compromised accounts to send email.</span></span> <span data-ttu-id="e85a4-106">L’aperçu et le rapport vous permettent de vérifier l’activité inhabituelle pour les envois de courrier électronique SMTP.</span><span class="sxs-lookup"><span data-stu-id="e85a4-106">The insight and report allow you to check for unusual activity for SMTP AUTH email submissions.</span></span> <span data-ttu-id="e85a4-107">Il indique également les données d’utilisation TLS pour les clients ou les appareils utilisant l’authentification SMTP.</span><span class="sxs-lookup"><span data-stu-id="e85a4-107">It also shows the TLS usage data for clients or devices using SMTP AUTH.</span></span>

<span data-ttu-id="e85a4-108">Le widget indique le nombre d’utilisateurs ou de comptes de service qui ont utilisé le protocole SMTP AUTH au cours des 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="e85a4-108">The widget indicates the number of users or service accounts that have used the SMTP Auth protocol in the last 7 days.</span></span>

![Widget clients SMTP AUTH dans le tableau de bord de flux de messagerie dans le centre de sécurité & conformité](../../media/mfi-smtp-auth-clients-report-widget.png)

<span data-ttu-id="e85a4-110">Si vous cliquez sur le nombre de messages dans le widget, un lanceur de **clients SMTP AUTH** apparaît.</span><span class="sxs-lookup"><span data-stu-id="e85a4-110">If you click the number of messages on the widget, an **SMTP Auth clients** flyout appears.</span></span> <span data-ttu-id="e85a4-111">La fenêtre mobile offre une vue agrégée de l’utilisation et des volumes TLS pour la semaine précédente.</span><span class="sxs-lookup"><span data-stu-id="e85a4-111">The flyout provides an aggregated view of the TLS usage and volumes for the last week.</span></span>

![Menu volant des détails après avoir cliqué sur le widget clients SMTP AUTH dans le tableau de bord de flux de messagerie](../../media/mfi-smtp-auth-clients-report-details.png)

<span data-ttu-id="e85a4-113">Vous pouvez cliquer sur le lien **rapport des clients d’authentification SMTP** pour accéder au rapport clients SMTP AUTH, comme décrit dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="e85a4-113">You can click the **SMTP Auth clients report** link to go to the SMTP Auth clients report as described in the next section.</span></span>

## <a name="smtp-auth-clients-report"></a><span data-ttu-id="e85a4-114">Rapport de clients d’authentification SMTP</span><span class="sxs-lookup"><span data-stu-id="e85a4-114">SMTP Auth clients report</span></span>

### <a name="report-view-for-the-smtp-auth-clients-report"></a><span data-ttu-id="e85a4-115">Affichage de rapport pour le rapport clients SMTP AUTH</span><span class="sxs-lookup"><span data-stu-id="e85a4-115">Report view for the SMTP Auth clients report</span></span>

<span data-ttu-id="e85a4-116">Par défaut, le rapport affiche les données des 7 derniers jours, mais les données sont disponibles pendant les 90 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="e85a4-116">By default, the report shows data for the last 7 days, but data is available for the last 90 days.</span></span>

<span data-ttu-id="e85a4-117">La section vue d’ensemble contient les graphiques suivants :</span><span class="sxs-lookup"><span data-stu-id="e85a4-117">The overview section contains the following charts:</span></span>

- <span data-ttu-id="e85a4-118">**Afficher les données par : volume d’envoi** : par défaut, le graphique indique le nombre de messages client SMTP AUTH qui ont été envoyés à partir de tous les domaines ( **afficher les données pour : tous les domaines des expéditeurs** sont sélectionnés par défaut).</span><span class="sxs-lookup"><span data-stu-id="e85a4-118">**View data by: Sending volume** : By default, the chart shows the number of SMTP Auth client messages that were sent from all domains ( **Show data for: All sender domains** is selected by default).</span></span> <span data-ttu-id="e85a4-119">Vous pouvez filtrer les résultats sur un domaine d’expéditeur spécifique en cliquant sur **afficher les données pour** et en sélectionnant le domaine de l’expéditeur dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="e85a4-119">You can filter the results to a specific sender domain by clicking **Show data for** and selecting the sender domain from the dropdown list.</span></span> <span data-ttu-id="e85a4-120">Si vous pointez sur un point de données spécifique (jour), le nombre de messages s’affiche.</span><span class="sxs-lookup"><span data-stu-id="e85a4-120">If you hover a specific data point (day), the number of messages is shown.</span></span>

  ![Affichage du volume d’envoi dans le rapport clients SMTP AUTH dans le centre de sécurité & conformité](../../media/mfi-smtp-auth-clients-report-sending-volume-view.png)

- <span data-ttu-id="e85a4-122">**Afficher les données par : utilisation de TLS** : le graphique indique le pourcentage d’utilisation TLS pour tous les messages client SMTP AUTH pendant la période sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="e85a4-122">**View data by: TLS Usage** : The chart shows the percentage of TLS usage for all SMTP Auth client messages during the selected time period.</span></span> <span data-ttu-id="e85a4-123">Ce graphique vous permet d’identifier et de prendre des mesures sur les utilisateurs et les comptes système qui utilisent encore des versions plus anciennes de TLS.</span><span class="sxs-lookup"><span data-stu-id="e85a4-123">This chart allows you to identify and take action on users and system accounts that are still using older versions of TLS.</span></span>

  ![Affichage de l’utilisation de TLS dans le rapport clients d’authentification SMTP dans le centre de sécurité & conformité](../../media/mfi-smtp-auth-clients-report-tls-usage-view.png)

<span data-ttu-id="e85a4-125">Si vous cliquez sur **filtres** dans un affichage de rapport, vous pouvez spécifier une plage de dates avec **Date de début** et date de **fin**.</span><span class="sxs-lookup"><span data-stu-id="e85a4-125">If you click **Filters** in a report view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="e85a4-126">Cliquez sur **demander un rapport** pour recevoir une version plus détaillée du rapport dans un message électronique.</span><span class="sxs-lookup"><span data-stu-id="e85a4-126">Click **Request report** to receive a more detailed version of the report in an email message.</span></span> <span data-ttu-id="e85a4-127">Vous pouvez spécifier la plage de dates et les destinataires qui recevront le rapport.</span><span class="sxs-lookup"><span data-stu-id="e85a4-127">You can specify the date range and the recipients to receive the report.</span></span>

### <a name="details-table-view-for-the-smtp-auth-clients-report"></a><span data-ttu-id="e85a4-128">Vue de la table Détails pour le rapport clients SMTP AUTH</span><span class="sxs-lookup"><span data-stu-id="e85a4-128">Details table view for the SMTP Auth clients report</span></span>

<span data-ttu-id="e85a4-129">Si vous cliquez sur **afficher les détails table** , les informations affichées dépendent du graphique que vous examinez :</span><span class="sxs-lookup"><span data-stu-id="e85a4-129">If you click **View details table** , the information that's shown depends on the chart you were looking at:</span></span>

- <span data-ttu-id="e85a4-130">**Afficher les données par : volume d’envoi** : les informations suivantes sont affichées dans un tableau :</span><span class="sxs-lookup"><span data-stu-id="e85a4-130">**View data by: Sending volume** : The following information is shown in a table:</span></span>

  - <span data-ttu-id="e85a4-131">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="e85a4-131">**Sender address**</span></span>
  - <span data-ttu-id="e85a4-132">**Nombre de messages**</span><span class="sxs-lookup"><span data-stu-id="e85a4-132">**Message count**</span></span>

  <span data-ttu-id="e85a4-133">Si vous sélectionnez une ligne, les mêmes détails s’affichent dans un menu volant.</span><span class="sxs-lookup"><span data-stu-id="e85a4-133">If you select a row, the same details are shown in a flyout.</span></span>

- <span data-ttu-id="e85a4-134">**Afficher les données par : utilisation de TLS** : les informations suivantes sont affichées dans un tableau :</span><span class="sxs-lookup"><span data-stu-id="e85a4-134">**View data by: TLS Usage** : The following information is shown in a table:</span></span>

  - <span data-ttu-id="e85a4-135">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="e85a4-135">**Sender address**</span></span>
  - <span data-ttu-id="e85a4-136">**TLS 1.0%**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="e85a4-136">**TLS1.0%**<sup>\*</sup></span></span>
  - <span data-ttu-id="e85a4-137">**TLS 1.1%**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="e85a4-137">**TLS1.1%**<sup>\*</sup></span></span>
  - <span data-ttu-id="e85a4-138">**TLS 1.2%**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="e85a4-138">**TLS1.2%**<sup>\*</sup></span></span>
  - <span data-ttu-id="e85a4-139">**Nombre de messages**</span><span class="sxs-lookup"><span data-stu-id="e85a4-139">**Message count**</span></span>

  <span data-ttu-id="e85a4-140"><sup>\*</sup> Cette colonne indique à la fois le pourcentage et le nombre de messages provenant de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="e85a4-140"><sup>\*</sup> This column shows both the percentage and number of messages from the sender.</span></span>

<span data-ttu-id="e85a4-141">Si vous cliquez sur **filtres** dans un affichage tableau détaillé, vous pouvez spécifier une plage de dates avec **Date de début** et date de **fin**.</span><span class="sxs-lookup"><span data-stu-id="e85a4-141">If you click **Filters** in a details table view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="e85a4-142">Si vous sélectionnez une ligne, des détails similaires s’affichent dans un menu volant :</span><span class="sxs-lookup"><span data-stu-id="e85a4-142">If you select a row, similar details are shown in a flyout:</span></span>

![Fenêtre mobile détails à partir de la table Détails de la vue utilisation TLS dans le rapport clients SMTP AUTH](../../media/mfi-smtp-auth-clients-report-tls-usage-view-view-details-table-details.png)

<span data-ttu-id="e85a4-144">Cliquez sur **demander un rapport** pour recevoir une version plus détaillée du rapport dans un message électronique.</span><span class="sxs-lookup"><span data-stu-id="e85a4-144">Click **Request report** to receive a more detailed version of the report in an email message.</span></span> <span data-ttu-id="e85a4-145">Vous pouvez spécifier la plage de dates et les destinataires qui recevront le rapport.</span><span class="sxs-lookup"><span data-stu-id="e85a4-145">You can specify the date range and the recipients to receive the report.</span></span>

<span data-ttu-id="e85a4-146">Pour revenir à l’affichage rapports, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="e85a4-146">To go back to the reports view, click **View report**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e85a4-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e85a4-147">Related topics</span></span>

<span data-ttu-id="e85a4-148">Pour plus d’informations sur les autres informations du tableau de bord de flux de messagerie, consultez [la rubrique mail Flow Insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span><span class="sxs-lookup"><span data-stu-id="e85a4-148">For information about other insights in the Mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
