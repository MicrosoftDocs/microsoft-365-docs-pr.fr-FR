---
title: Rapport de clients d’authentification SMTP
ms.author: chrisda
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
description: Les administrateurs peuvent en savoir plus sur le rapport clients d’authentification SMTP dans le tableau de bord de flux de messagerie dans le centre de sécurité & conformité.
ms.openlocfilehash: a273da9e0ebe7987a22669c54f3ebfe103e5933c
ms.sourcegitcommit: 84d88a857e82b1a8a0d466057a2e330e8b1692e4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/27/2019
ms.locfileid: "37306028"
---
# <a name="smtp-auth-clients-report"></a><span data-ttu-id="119a2-103">Rapport de clients d’authentification SMTP</span><span class="sxs-lookup"><span data-stu-id="119a2-103">SMTP Auth clients report</span></span>

<span data-ttu-id="119a2-104">Le rapport **clients d’authentification SMTP** met en évidence l’utilisation du protocole de soumission du client SMTP AUTH par les utilisateurs ou les comptes système de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="119a2-104">The **SMTP Auth clients** report highlights the use of the SMTP Auth client submission protocol by users or system accounts in your organization.</span></span> <span data-ttu-id="119a2-105">Ce protocole hérité (qui utilise le point de terminaison smtp.office365.com) offre uniquement l’authentification de base et est susceptible d’être utilisé par des comptes compromis pour envoyer des courriers électroniques.</span><span class="sxs-lookup"><span data-stu-id="119a2-105">This legacy protocol (which uses the endpoint smtp.office365.com) only offers Basic authentication, and is susceptible to being used by compromised accounts to send email.</span></span>  <span data-ttu-id="119a2-106">Ce rapport vous permet de vérifier l’activité inhabituelle.</span><span class="sxs-lookup"><span data-stu-id="119a2-106">This report allows you to check for unusual activity.</span></span> <span data-ttu-id="119a2-107">Il indique également les données d’utilisation TLS pour les clients ou les appareils utilisant l’authentification SMTP.</span><span class="sxs-lookup"><span data-stu-id="119a2-107">It also shows the TLS usage data for clients or devices using SMTP Auth.</span></span>

<span data-ttu-id="119a2-108">Le widget affiché dans le tableau de bord du flux de messagerie indique le nombre d’utilisateurs ou de comptes de service qui ont utilisé le protocole SMTP AUTH au cours des 7 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="119a2-108">The widget that's shown in the Mail Flow dashboard indicates the number of users or service accounts that have used the SMTP Auth protocol in the last 7 days.</span></span>

![Rapport sur les clients SMTP AUTH dans le tableau de bord de flux de messagerie dans le centre de sécurité & conformité](../media/smtp-auth-clients-report-selected.png)

<span data-ttu-id="119a2-110">Un clic sur le widget ouvre une fenêtre mobile qui offre une vue agrégée de l’utilisation et des volumes TLS pour la dernière semaine.</span><span class="sxs-lookup"><span data-stu-id="119a2-110">Clicking on the widget opens a flyout that provides an aggregated view of the TLS usage and volumes for the last week.</span></span>

![Le menu volant dans le rapport clients SMTP AUTH](../media/smtp-auth-clients-flyout.png)

<span data-ttu-id="119a2-112">Lorsque vous cliquez sur le lien du **rapport clients d’authentification SMTP** , deux vues de données principales et deux vues de données s’affichent.</span><span class="sxs-lookup"><span data-stu-id="119a2-112">When you click on the **SMTP Auth Clients Report** link, you'll see two main data pivots and two data views.</span></span> <span data-ttu-id="119a2-113">Les données croisées dynamiques représentent le **volume d’envoi** et l’utilisation de **TLS**.</span><span class="sxs-lookup"><span data-stu-id="119a2-113">The data pivots are the **Sending Volume** and **TLS Usage**.</span></span> <span data-ttu-id="119a2-114">Les vues de données sont le graphique et le tableau des détails.</span><span class="sxs-lookup"><span data-stu-id="119a2-114">The data views are the chart and the details table.</span></span>

<span data-ttu-id="119a2-115">L’affichage **volume d’envoi** indique le nombre de messages qui ont été envoyés à l’aide de l’authentification SMTP pour la plage de temps spécifiée.</span><span class="sxs-lookup"><span data-stu-id="119a2-115">The **Sending Volume** view shows the number of messages that were sent using SMTP Auth for the specified time range.</span></span> <span data-ttu-id="119a2-116">Vous pouvez ajuster la plage en cliquant sur **filtres**.</span><span class="sxs-lookup"><span data-stu-id="119a2-116">You can adjust the range by clicking **Filters**.</span></span> <span data-ttu-id="119a2-117">Le graphique est organisé par domaine d’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="119a2-117">The chart is organized by sender domain.</span></span> <span data-ttu-id="119a2-118">Vous pouvez voir les données séparées pour chaque domaine en sélectionnant le domaine dans la liste déroulante **afficher les données** .</span><span class="sxs-lookup"><span data-stu-id="119a2-118">You can see separate data for each domain by selecting the domain in the **Show data for** drop down.</span></span>

![Envoi de volume dans le rapport clients SMTP AUTH](../media/smtp-auth-clients-report-sending-volume.png)

<span data-ttu-id="119a2-120">Vous pouvez afficher des informations détaillées sur les expéditeurs et le nombre de messages en cliquant sur **afficher la table des détails**.</span><span class="sxs-lookup"><span data-stu-id="119a2-120">You can view detailed information about the senders and their message counts by clicking **View details table**.</span></span> <span data-ttu-id="119a2-121">Pour revenir au graphique, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="119a2-121">To return to the chart, click **View report**.</span></span>

![Table des détails pour l’envoi de volume dans le rapport clients SMTP AUTH](../media/smtp-auth-clients-report-details-sending-volume.png)

<span data-ttu-id="119a2-123">Le tableau croisé dynamique d' **utilisation TLS** est important en raison de la désapprobation à venir de TLS 1.0 et TLS 1.1 dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="119a2-123">The **TLS Usage** pivot is important due to the upcoming deprecation of TLS1.0 and TLS1.1 in Office 365.</span></span> <span data-ttu-id="119a2-124">De nombreux appareils et applications hérités ne peuvent pas envoyer de courrier électronique s’ils ne peuvent utiliser TLS 1.0 qu’avec l’authentification SMTP. Ce tableau croisé dynamique vous permet d’identifier et de prendre des mesures sur les utilisateurs et les comptes système qui utilisent encore des versions plus anciennes de TLS.</span><span class="sxs-lookup"><span data-stu-id="119a2-124">Many legacy devices and applications will be unable to send email if they are only capable of using TLS1.0 with SMTP Auth. This pivot allows you to identify and take action on users and system accounts that are still using older versions of TLS.</span></span>

![Utilisation de TLS dans le rapport clients d’authentification SMTP](../media/smtp-auth-clients-report-tls-usage.png)

<span data-ttu-id="119a2-126">Vous pouvez afficher des informations détaillées sur les expéditeurs, les versions de TLS qu’ils utilisent avec l’authentification SMTP et le nombre de messages en cliquant sur **afficher la table des détails**.</span><span class="sxs-lookup"><span data-stu-id="119a2-126">You can view detailed information about the senders, the versions of TLS they are using with SMTP Auth, and their message counts by clicking **View details table**.</span></span> <span data-ttu-id="119a2-127">Pour revenir au graphique, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="119a2-127">To return to the chart, click **View report**.</span></span>

<span data-ttu-id="119a2-128">Vous pouvez également télécharger une version plus détaillée du rapport en cliquant sur demander un rapport.</span><span class="sxs-lookup"><span data-stu-id="119a2-128">You can also download a more detailed version of the report by clicking Request report.</span></span>

![Table des détails pour l’utilisation de TLS dans le rapport clients SMTP AUTH](../media/smtp-auth-clients-report-details-tls-usage.png)

## <a name="see-also"></a><span data-ttu-id="119a2-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="119a2-130">See also</span></span>

<span data-ttu-id="119a2-131">Pour plus d’informations sur les autres flux de messagerie dans le tableau de bord de flux de messagerie, voir [mail Flow Insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span><span class="sxs-lookup"><span data-stu-id="119a2-131">For more information about other mail flow insights in the mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
