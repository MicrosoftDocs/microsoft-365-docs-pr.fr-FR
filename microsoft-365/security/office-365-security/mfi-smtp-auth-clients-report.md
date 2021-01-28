---
title: Informations et rapport sur les clients SMTP Auth dans le tableau de bord de flux de messagerie
f1.keywords:
- NOCSH
ms.author: siosulli
author: siosulli
manager: dansimp
audience: ITPro
ms.topic: conceptual
localization_priority: Normal
ms.assetid: ''
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs peuvent apprendre à utiliser les informations d’authentification SMTP et le rapport dans le tableau de bord de flux de messagerie du Centre de sécurité & conformité pour surveiller les expéditeurs de messages électroniques de leur organisation qui utilisent SMTP authentifié (SMTP AUTH) pour envoyer des messages électroniques.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: afceb767f6ebfeed96deb6362e05bb088b548c3d
ms.sourcegitcommit: 537e513a4a232a01e44ecbc76d86a8bcaf142482
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/27/2021
ms.locfileid: "50029161"
---
# <a name="smtp-auth-clients-insight-and-report-in-the-security--compliance-center"></a><span data-ttu-id="1895f-103">Informations et rapports sur les clients d’th SMTP dans le Centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="1895f-103">SMTP Auth clients insight and report in the Security & Compliance Center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="1895f-104">Les informations sur les clients [](mail-flow-insights-v2.md) **SMTP Auth** dans le tableau de bord de flux de messagerie et le rapport des clients d’th [SMTP](#smtp-auth-clients-report) associés dans le Centre de sécurité [&](https://protection.office.com) conformité mettent en évidence l’utilisation du protocole d’envoi du client SMTP AUTH par les utilisateurs ou les comptes système de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1895f-104">The **SMTP Auth clients** insight in the [Mail flow dashboard](mail-flow-insights-v2.md) and the associated [SMTP Auth clients report](#smtp-auth-clients-report) in the [Security & Compliance Center](https://protection.office.com) highlight the use of the SMTP AUTH client submission protocol by users or system accounts in your organization.</span></span> <span data-ttu-id="1895f-105">Ce protocole hérité (qui utilise le point de terminaison smtp.office365.com) offre uniquement l’authentification de base et peut être utilisé par des comptes compromis pour envoyer des messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="1895f-105">This legacy protocol (which uses the endpoint smtp.office365.com) only offers Basic authentication, and is susceptible to being used by compromised accounts to send email.</span></span> <span data-ttu-id="1895f-106">Les informations et le rapport vous permettent de vérifier l’activité inhabituelle pour les envois de courrier ÉLECTRONIQUE SMTP AUTH.</span><span class="sxs-lookup"><span data-stu-id="1895f-106">The insight and report allow you to check for unusual activity for SMTP AUTH email submissions.</span></span> <span data-ttu-id="1895f-107">Il affiche également les données d’utilisation TLS pour les clients ou les appareils utilisant SMTP AUTH.</span><span class="sxs-lookup"><span data-stu-id="1895f-107">It also shows the TLS usage data for clients or devices using SMTP AUTH.</span></span>

<span data-ttu-id="1895f-108">Le widget indique le nombre d’utilisateurs ou de comptes de service qui ont utilisé le protocole SMTP Auth au cours des 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="1895f-108">The widget indicates the number of users or service accounts that have used the SMTP Auth protocol in the last 7 days.</span></span>

![Widget clients SMTP Auth dans le tableau de bord de flux de messagerie dans le Centre de sécurité & conformité](../../media/mfi-smtp-auth-clients-report-widget.png)

<span data-ttu-id="1895f-110">Si vous cliquez sur le nombre de messages sur le widget, un volant **de clients SMTP Auth** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="1895f-110">If you click the number of messages on the widget, an **SMTP Auth clients** flyout appears.</span></span> <span data-ttu-id="1895f-111">Le flyout fournit une vue agrégée de l’utilisation et des volumes TLS de la semaine dernière.</span><span class="sxs-lookup"><span data-stu-id="1895f-111">The flyout provides an aggregated view of the TLS usage and volumes for the last week.</span></span>

![Volant de détails après avoir cliqué sur le widget clients SMTP Auth dans le tableau de bord de flux de messagerie](../../media/mfi-smtp-auth-clients-report-details.png)

<span data-ttu-id="1895f-113">Vous pouvez cliquer sur le lien **du rapport des clients SMTP Auth** pour aller au rapport clients d’th SMTP, comme décrit dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="1895f-113">You can click the **SMTP Auth clients report** link to go to the SMTP Auth clients report as described in the next section.</span></span>

## <a name="smtp-auth-clients-report"></a><span data-ttu-id="1895f-114">Rapport de clients d’authentification SMTP</span><span class="sxs-lookup"><span data-stu-id="1895f-114">SMTP Auth clients report</span></span>

### <a name="report-view-for-the-smtp-auth-clients-report"></a><span data-ttu-id="1895f-115">Affichage du rapport pour le rapport des clients d’th SMTP</span><span class="sxs-lookup"><span data-stu-id="1895f-115">Report view for the SMTP Auth clients report</span></span>

<span data-ttu-id="1895f-116">Par défaut, le rapport affiche les données des 7 derniers jours, mais les données sont disponibles pour les 90 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="1895f-116">By default, the report shows data for the last 7 days, but data is available for the last 90 days.</span></span>

<span data-ttu-id="1895f-117">La section vue d’ensemble contient les graphiques suivants :</span><span class="sxs-lookup"><span data-stu-id="1895f-117">The overview section contains the following charts:</span></span>

- <span data-ttu-id="1895f-118">Afficher les données par : volume d’envoi : par défaut, le graphique affiche le nombre de messages clients SMTP Auth qui ont été envoyés à partir de tous les domaines ( Afficher les données pour : Tous les domaines des **expéditeurs** est sélectionné par défaut).</span><span class="sxs-lookup"><span data-stu-id="1895f-118">**View data by: Sending volume**: By default, the chart shows the number of SMTP Auth client messages that were sent from all domains (**Show data for: All sender domains** is selected by default).</span></span> <span data-ttu-id="1895f-119">Vous pouvez filtrer les résultats sur un  domaine d’expéditeur spécifique en cliquant sur Afficher les données pour et en sélectionnant le domaine de l’expéditeur dans la liste liste.</span><span class="sxs-lookup"><span data-stu-id="1895f-119">You can filter the results to a specific sender domain by clicking **Show data for** and selecting the sender domain from the dropdown list.</span></span> <span data-ttu-id="1895f-120">Si vous pointez sur un point de données spécifique (jour), le nombre de messages s’affiche.</span><span class="sxs-lookup"><span data-stu-id="1895f-120">If you hover a specific data point (day), the number of messages is shown.</span></span>

  ![Affichage en volume de l’envoi dans le rapport des clients d’th SMTP dans le Centre de conformité & sécurité](../../media/mfi-smtp-auth-clients-report-sending-volume-view.png)

- <span data-ttu-id="1895f-122">Afficher les données par : Utilisation du chiffrement **TLS**: le graphique affiche le pourcentage d’utilisation de TLS pour tous les messages clients SMTP Auth pendant la période sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="1895f-122">**View data by: TLS Usage**: The chart shows the percentage of TLS usage for all SMTP Auth client messages during the selected time period.</span></span> <span data-ttu-id="1895f-123">Ce graphique vous permet d’identifier les utilisateurs et les comptes système qui utilisent encore des versions antérieures de TLS et d’agir sur ces derniers.</span><span class="sxs-lookup"><span data-stu-id="1895f-123">This chart allows you to identify and take action on users and system accounts that are still using older versions of TLS.</span></span>

  ![Affichage de l’utilisation TLS dans le rapport des clients SMTP Auth dans le Centre de sécurité & conformité](../../media/mfi-smtp-auth-clients-report-tls-usage-view.png)

<span data-ttu-id="1895f-125">Si vous cliquez sur **Filtres** dans un affichage de rapport, vous pouvez spécifier une plage de dates avec la **date** de début et la **date de fin.**</span><span class="sxs-lookup"><span data-stu-id="1895f-125">If you click **Filters** in a report view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="1895f-126">Cliquez **sur Demander un** rapport pour recevoir une version plus détaillée du rapport dans un message électronique.</span><span class="sxs-lookup"><span data-stu-id="1895f-126">Click **Request report** to receive a more detailed version of the report in an email message.</span></span> <span data-ttu-id="1895f-127">Vous pouvez spécifier la plage de dates et les destinataires à recevoir.</span><span class="sxs-lookup"><span data-stu-id="1895f-127">You can specify the date range and the recipients to receive the report.</span></span>

### <a name="details-table-view-for-the-smtp-auth-clients-report"></a><span data-ttu-id="1895f-128">Vue de table Détails pour le rapport des clients d’th SMTP</span><span class="sxs-lookup"><span data-stu-id="1895f-128">Details table view for the SMTP Auth clients report</span></span>

<span data-ttu-id="1895f-129">Si vous cliquez sur Afficher le tableau des **détails,** les informations affichées dépendent du graphique que vous regardiez :</span><span class="sxs-lookup"><span data-stu-id="1895f-129">If you click **View details table**, the information that's shown depends on the chart you were looking at:</span></span>

- <span data-ttu-id="1895f-130">**Afficher les données par : volume d’envoi**: les informations suivantes sont affichées dans un tableau :</span><span class="sxs-lookup"><span data-stu-id="1895f-130">**View data by: Sending volume**: The following information is shown in a table:</span></span>

  - <span data-ttu-id="1895f-131">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="1895f-131">**Sender address**</span></span>
  - <span data-ttu-id="1895f-132">**Nombre de messages**</span><span class="sxs-lookup"><span data-stu-id="1895f-132">**Message count**</span></span>

  <span data-ttu-id="1895f-133">Si vous sélectionnez une ligne, les mêmes détails sont affichés dans un volant.</span><span class="sxs-lookup"><span data-stu-id="1895f-133">If you select a row, the same details are shown in a flyout.</span></span>

- <span data-ttu-id="1895f-134">**Afficher les données par : Utilisation de TLS**: les informations suivantes sont affichées dans un tableau :</span><span class="sxs-lookup"><span data-stu-id="1895f-134">**View data by: TLS Usage**: The following information is shown in a table:</span></span>

  - <span data-ttu-id="1895f-135">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="1895f-135">**Sender address**</span></span>
  - <span data-ttu-id="1895f-136">**TLS1.0%**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="1895f-136">**TLS1.0%**<sup>\*</sup></span></span>
  - <span data-ttu-id="1895f-137">**TLS1.1%**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="1895f-137">**TLS1.1%**<sup>\*</sup></span></span>
  - <span data-ttu-id="1895f-138">**TLS1.2%**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="1895f-138">**TLS1.2%**<sup>\*</sup></span></span>
  - <span data-ttu-id="1895f-139">**Nombre de messages**</span><span class="sxs-lookup"><span data-stu-id="1895f-139">**Message count**</span></span>

  <span data-ttu-id="1895f-140"><sup>\*</sup> Cette colonne indique le pourcentage et le nombre de messages de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="1895f-140"><sup>\*</sup> This column shows both the percentage and number of messages from the sender.</span></span>

<span data-ttu-id="1895f-141">Si vous cliquez sur **Filtres** dans une vue de tableau de détails, vous pouvez spécifier une plage de dates avec la **date** de début et la **date de fin.**</span><span class="sxs-lookup"><span data-stu-id="1895f-141">If you click **Filters** in a details table view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="1895f-142">Si vous sélectionnez une ligne, des détails similaires sont affichés dans un volant :</span><span class="sxs-lookup"><span data-stu-id="1895f-142">If you select a row, similar details are shown in a flyout:</span></span>

![Détails du tableau détails de l’affichage Utilisation du TLS dans le rapport clients d’th SMTP](../../media/mfi-smtp-auth-clients-report-tls-usage-view-view-details-table-details.png)

<span data-ttu-id="1895f-144">Cliquez **sur Demander un** rapport pour recevoir une version plus détaillée du rapport dans un message électronique.</span><span class="sxs-lookup"><span data-stu-id="1895f-144">Click **Request report** to receive a more detailed version of the report in an email message.</span></span> <span data-ttu-id="1895f-145">Vous pouvez spécifier la plage de dates et les destinataires à recevoir.</span><span class="sxs-lookup"><span data-stu-id="1895f-145">You can specify the date range and the recipients to receive the report.</span></span>

<span data-ttu-id="1895f-146">Pour revenir à l’affichage Rapports, cliquez **sur Afficher le rapport.**</span><span class="sxs-lookup"><span data-stu-id="1895f-146">To go back to the reports view, click **View report**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1895f-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1895f-147">Related topics</span></span>

<span data-ttu-id="1895f-148">Pour plus d’informations sur d’autres informations dans le tableau de bord de flux de messagerie, voir Informations sur le flux de messagerie dans le Centre de sécurité [& conformité.](mail-flow-insights-v2.md)</span><span class="sxs-lookup"><span data-stu-id="1895f-148">For information about other insights in the Mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
