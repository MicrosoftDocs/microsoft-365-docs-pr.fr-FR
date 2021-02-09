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
ms.openlocfilehash: 3476ee2f9388245fb105a0910fa7b7d11ec3aeee
ms.sourcegitcommit: e920e68c8d0eac8b152039b52cfc139d478a67b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2021
ms.locfileid: "50150242"
---
# <a name="smtp-auth-clients-insight-and-report-in-the-security--compliance-center"></a><span data-ttu-id="fd5d4-103">Informations et rapports sur les clients d’th SMTP dans le Centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="fd5d4-103">SMTP Auth clients insight and report in the Security & Compliance Center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="fd5d4-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="fd5d4-104">**Applies to**</span></span>
- [<span data-ttu-id="fd5d4-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="fd5d4-105">Exchange Online Protection</span></span>](https://go.microsoft.com/fwlink/?linkid=2148611)
- [<span data-ttu-id="fd5d4-106">Microsoft Defender pour Office 365 plan 1 et plan 2</span><span class="sxs-lookup"><span data-stu-id="fd5d4-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](https://go.microsoft.com/fwlink/?linkid=2148715)
- [<span data-ttu-id="fd5d4-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="fd5d4-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

<span data-ttu-id="fd5d4-108">Les informations sur les clients [](mail-flow-insights-v2.md) **SMTP Auth** dans le tableau de bord de flux de messagerie et le rapport des clients d’th [SMTP](#smtp-auth-clients-report) associés dans le Centre de sécurité [&](https://protection.office.com) conformité mettent en évidence l’utilisation du protocole d’envoi du client SMTP AUTH par les utilisateurs ou les comptes système de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="fd5d4-108">The **SMTP Auth clients** insight in the [Mail flow dashboard](mail-flow-insights-v2.md) and the associated [SMTP Auth clients report](#smtp-auth-clients-report) in the [Security & Compliance Center](https://protection.office.com) highlight the use of the SMTP AUTH client submission protocol by users or system accounts in your organization.</span></span> <span data-ttu-id="fd5d4-109">Ce protocole hérité (qui utilise le point de terminaison smtp.office365.com) offre uniquement l’authentification de base et peut être utilisé par des comptes compromis pour envoyer des messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="fd5d4-109">This legacy protocol (which uses the endpoint smtp.office365.com) only offers Basic authentication, and is susceptible to being used by compromised accounts to send email.</span></span> <span data-ttu-id="fd5d4-110">Les informations et le rapport vous permettent de vérifier l’activité inhabituelle pour les envois de courrier ÉLECTRONIQUE SMTP AUTH.</span><span class="sxs-lookup"><span data-stu-id="fd5d4-110">The insight and report allow you to check for unusual activity for SMTP AUTH email submissions.</span></span> <span data-ttu-id="fd5d4-111">Il affiche également les données d’utilisation TLS pour les clients ou les appareils utilisant SMTP AUTH.</span><span class="sxs-lookup"><span data-stu-id="fd5d4-111">It also shows the TLS usage data for clients or devices using SMTP AUTH.</span></span>

<span data-ttu-id="fd5d4-112">Le widget indique le nombre d’utilisateurs ou de comptes de service qui ont utilisé le protocole SMTP Auth au cours des 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="fd5d4-112">The widget indicates the number of users or service accounts that have used the SMTP Auth protocol in the last 7 days.</span></span>

![Widget clients SMTP Auth dans le tableau de bord de flux de messagerie dans le Centre de sécurité & conformité](../../media/mfi-smtp-auth-clients-report-widget.png)

<span data-ttu-id="fd5d4-114">Si vous cliquez sur le nombre de messages sur le widget, un volant **de clients SMTP Auth** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="fd5d4-114">If you click the number of messages on the widget, an **SMTP Auth clients** flyout appears.</span></span> <span data-ttu-id="fd5d4-115">Le flyout fournit une vue agrégée de l’utilisation et des volumes TLS de la semaine dernière.</span><span class="sxs-lookup"><span data-stu-id="fd5d4-115">The flyout provides an aggregated view of the TLS usage and volumes for the last week.</span></span>

![Volant de détails après avoir cliqué sur le widget clients SMTP Auth dans le tableau de bord de flux de messagerie](../../media/mfi-smtp-auth-clients-report-details.png)

<span data-ttu-id="fd5d4-117">Vous pouvez cliquer sur le lien **du rapport des clients SMTP Auth** pour aller au rapport clients d’th SMTP, comme décrit dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="fd5d4-117">You can click the **SMTP Auth clients report** link to go to the SMTP Auth clients report as described in the next section.</span></span>

## <a name="smtp-auth-clients-report"></a><span data-ttu-id="fd5d4-118">Rapport de clients d’authentification SMTP</span><span class="sxs-lookup"><span data-stu-id="fd5d4-118">SMTP Auth clients report</span></span>

### <a name="report-view-for-the-smtp-auth-clients-report"></a><span data-ttu-id="fd5d4-119">Affichage du rapport pour le rapport clients d’th SMTP</span><span class="sxs-lookup"><span data-stu-id="fd5d4-119">Report view for the SMTP Auth clients report</span></span>

<span data-ttu-id="fd5d4-120">Par défaut, le rapport affiche les données des 7 derniers jours, mais les données sont disponibles pour les 90 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="fd5d4-120">By default, the report shows data for the last 7 days, but data is available for the last 90 days.</span></span>

<span data-ttu-id="fd5d4-121">La section vue d’ensemble contient les graphiques suivants :</span><span class="sxs-lookup"><span data-stu-id="fd5d4-121">The overview section contains the following charts:</span></span>

- <span data-ttu-id="fd5d4-122">Afficher les données par : Volume d’envoi : par défaut, le graphique affiche le nombre de messages clients SMTP Auth qui ont été envoyés à partir de tous les domaines ( Afficher les données pour : Tous les domaines des **expéditeurs** est sélectionné par défaut).</span><span class="sxs-lookup"><span data-stu-id="fd5d4-122">**View data by: Sending volume**: By default, the chart shows the number of SMTP Auth client messages that were sent from all domains (**Show data for: All sender domains** is selected by default).</span></span> <span data-ttu-id="fd5d4-123">Vous pouvez filtrer les résultats sur un  domaine d’expéditeur spécifique en cliquant sur Afficher les données pour et en sélectionnant le domaine de l’expéditeur dans la liste liste.</span><span class="sxs-lookup"><span data-stu-id="fd5d4-123">You can filter the results to a specific sender domain by clicking **Show data for** and selecting the sender domain from the dropdown list.</span></span> <span data-ttu-id="fd5d4-124">Si vous pointez sur un point de données spécifique (jour), le nombre de messages s’affiche.</span><span class="sxs-lookup"><span data-stu-id="fd5d4-124">If you hover a specific data point (day), the number of messages is shown.</span></span>

  ![Affichage en volume de l’envoi dans le rapport des clients d’th SMTP dans le Centre de conformité & sécurité](../../media/mfi-smtp-auth-clients-report-sending-volume-view.png)

- <span data-ttu-id="fd5d4-126">Afficher les données par : Utilisation du chiffrement **TLS**: le graphique affiche le pourcentage d’utilisation de TLS pour tous les messages clients SMTP Auth pendant la période sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="fd5d4-126">**View data by: TLS Usage**: The chart shows the percentage of TLS usage for all SMTP Auth client messages during the selected time period.</span></span> <span data-ttu-id="fd5d4-127">Ce graphique vous permet d’identifier les utilisateurs et les comptes système qui utilisent encore des versions antérieures de TLS et d’agir sur ces derniers.</span><span class="sxs-lookup"><span data-stu-id="fd5d4-127">This chart allows you to identify and take action on users and system accounts that are still using older versions of TLS.</span></span>

  ![Affichage de l’utilisation TLS dans le rapport des clients SMTP Auth dans le Centre de sécurité & conformité](../../media/mfi-smtp-auth-clients-report-tls-usage-view.png)

<span data-ttu-id="fd5d4-129">Si vous cliquez sur **Filtres** dans un affichage de rapport, vous pouvez spécifier une plage de dates avec la **date** de début et la **date de fin.**</span><span class="sxs-lookup"><span data-stu-id="fd5d4-129">If you click **Filters** in a report view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="fd5d4-130">Cliquez **sur Demander un** rapport pour recevoir une version plus détaillée du rapport dans un message électronique.</span><span class="sxs-lookup"><span data-stu-id="fd5d4-130">Click **Request report** to receive a more detailed version of the report in an email message.</span></span> <span data-ttu-id="fd5d4-131">Vous pouvez spécifier la plage de dates et les destinataires à recevoir.</span><span class="sxs-lookup"><span data-stu-id="fd5d4-131">You can specify the date range and the recipients to receive the report.</span></span>

### <a name="details-table-view-for-the-smtp-auth-clients-report"></a><span data-ttu-id="fd5d4-132">Affichage de table Détails pour le rapport des clients d’th SMTP</span><span class="sxs-lookup"><span data-stu-id="fd5d4-132">Details table view for the SMTP Auth clients report</span></span>

<span data-ttu-id="fd5d4-133">Si vous cliquez sur Afficher le tableau des **détails,** les informations affichées dépendent du graphique que vous regardiez :</span><span class="sxs-lookup"><span data-stu-id="fd5d4-133">If you click **View details table**, the information that's shown depends on the chart you were looking at:</span></span>

- <span data-ttu-id="fd5d4-134">**Afficher les données par : volume d’envoi**: les informations suivantes sont affichées dans un tableau :</span><span class="sxs-lookup"><span data-stu-id="fd5d4-134">**View data by: Sending volume**: The following information is shown in a table:</span></span>

  - <span data-ttu-id="fd5d4-135">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="fd5d4-135">**Sender address**</span></span>
  - <span data-ttu-id="fd5d4-136">**Nombre de messages**</span><span class="sxs-lookup"><span data-stu-id="fd5d4-136">**Message count**</span></span>

  <span data-ttu-id="fd5d4-137">Si vous sélectionnez une ligne, les mêmes détails sont affichés dans un volant.</span><span class="sxs-lookup"><span data-stu-id="fd5d4-137">If you select a row, the same details are shown in a flyout.</span></span>

- <span data-ttu-id="fd5d4-138">**Afficher les données par : Utilisation de TLS**: les informations suivantes sont affichées dans un tableau :</span><span class="sxs-lookup"><span data-stu-id="fd5d4-138">**View data by: TLS Usage**: The following information is shown in a table:</span></span>

  - <span data-ttu-id="fd5d4-139">**Adresse de l’expéditeur**</span><span class="sxs-lookup"><span data-stu-id="fd5d4-139">**Sender address**</span></span>
  - <span data-ttu-id="fd5d4-140">**TLS1.0%**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="fd5d4-140">**TLS1.0%**<sup>\*</sup></span></span>
  - <span data-ttu-id="fd5d4-141">**TLS1.1%**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="fd5d4-141">**TLS1.1%**<sup>\*</sup></span></span>
  - <span data-ttu-id="fd5d4-142">**TLS1.2%**<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="fd5d4-142">**TLS1.2%**<sup>\*</sup></span></span>
  - <span data-ttu-id="fd5d4-143">**Nombre de messages**</span><span class="sxs-lookup"><span data-stu-id="fd5d4-143">**Message count**</span></span>

  <span data-ttu-id="fd5d4-144"><sup>\*</sup> Cette colonne indique le pourcentage et le nombre de messages de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="fd5d4-144"><sup>\*</sup> This column shows both the percentage and number of messages from the sender.</span></span>

<span data-ttu-id="fd5d4-145">Si vous cliquez sur **Filtres** dans une vue de tableau de détails, vous pouvez spécifier une plage de dates avec la **date** de début et la **date de fin.**</span><span class="sxs-lookup"><span data-stu-id="fd5d4-145">If you click **Filters** in a details table view, you can specify a date range with **Start date** and **End date**.</span></span>

<span data-ttu-id="fd5d4-146">Si vous sélectionnez une ligne, des détails similaires sont affichés dans un volant :</span><span class="sxs-lookup"><span data-stu-id="fd5d4-146">If you select a row, similar details are shown in a flyout:</span></span>

![Volant détails du tableau détails de l’affichage Utilisation du TLS dans le rapport clients d’th SMTP](../../media/mfi-smtp-auth-clients-report-tls-usage-view-view-details-table-details.png)

<span data-ttu-id="fd5d4-148">Cliquez **sur Demander un** rapport pour recevoir une version plus détaillée du rapport dans un message électronique.</span><span class="sxs-lookup"><span data-stu-id="fd5d4-148">Click **Request report** to receive a more detailed version of the report in an email message.</span></span> <span data-ttu-id="fd5d4-149">Vous pouvez spécifier la plage de dates et les destinataires à recevoir.</span><span class="sxs-lookup"><span data-stu-id="fd5d4-149">You can specify the date range and the recipients to receive the report.</span></span>

<span data-ttu-id="fd5d4-150">Pour revenir à l’affichage Rapports, cliquez **sur Afficher le rapport.**</span><span class="sxs-lookup"><span data-stu-id="fd5d4-150">To go back to the reports view, click **View report**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd5d4-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fd5d4-151">Related topics</span></span>

<span data-ttu-id="fd5d4-152">Pour plus d’informations sur d’autres informations dans le tableau de bord de flux de messagerie, voir Informations sur le flux de messagerie dans le Centre de sécurité [& conformité.](mail-flow-insights-v2.md)</span><span class="sxs-lookup"><span data-stu-id="fd5d4-152">For information about other insights in the Mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
